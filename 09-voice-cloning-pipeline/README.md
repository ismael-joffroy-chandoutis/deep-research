# Voice Cloning & Audio Analysis Pipeline for Documentary Cinema

*April 2026 — A filmmaker's field notes*

---

## The question

You have hundreds of hours of raw documentary audio scattered across half a dozen drives. Some of it is studio-clean interview. Some of it is iPhone voice memos at 3am. Some of it is a Zoom H8 left running while someone walks into a room. You want to do three things with it, and you want to do them on a laptop instead of waiting six weeks for a post house:

1. Know what is inside it.
2. Clean it enough to use it.
3. Rebuild a voice from it.

This is what I learned trying to do that at the level of a feature film, using a mix of free open-source tools, one big cloud API, and a local RTX 5090.

---

## Part I — The stack I ended up with

### Layer 1: Know what is inside

**Gemini 3 Flash Preview.** This is the single most useful tool I found in April 2026. You upload a 30-second sample of any audio file through the Python SDK, you pass it a JSON-strict prompt asking who speaks, about what, in what language, with what emotional register, and you get back a structured classification in about 10 seconds for half a cent per file. It reads prosody and content together. It will tell you that someone is critiquing Scorsese in a reflective register with light background wind. It will also, and this is the part you have to guard against, confidently hallucinate the same speaker on a file that turns out to contain nothing but the hiss of an unplugged microphone.

The lesson is obvious in retrospect: a language model will always prefer to answer than to say nothing, and an audio model trained on the entire internet has opinions about what a documentary rush is supposed to contain. If you give it silence and tell it the film is about a specific person, it will fill in the blanks. The fix is cheap and mandatory: measure peak and RMS with soundfile before you send anything to the model, drop anything where peak is below −30 dBFS or RMS is below −50 dBFS. Out of 298 files I triaged, six came back as confident CORE classifications that were, on inspection, dead channels. Six out of 298 sounds small until you imagine it multiplied across a feature.

**Alternatives I considered and why I chose Gemini.** emotion2vec is a specialized open-source model that gives you a numerical score for vocal emotion based purely on acoustics. It's SOTA on paper and it runs on a local GPU for free. But it doesn't understand content. It will tell you the person sounds sad without telling you whether they're talking about their mother or about traffic. For a film where I need both, Gemini's combined content-plus-prosody read wins. emotion2vec would be a good second pass for files where I want a numerical confirmation of the emotional register, but it can't replace the first pass.

NVIDIA VSS Blueprint is a different thing altogether. It's a RAG system over video with dense captioning and vector search. It's not a replacement for a triage pipeline, it's an indexing layer you build on top of one. It would make sense once the triage is done and you want to ask "show me every moment where the subject discusses [topic] with [register]" across the entire rushes library. For now it's a phase 2 consideration.

Tim McAleer at Florentine Films (Ken Burns' production company) built a custom Python pipeline with OpenAI Vision and vector embeddings to make tens of thousands of archival images searchable. His stack is Claude for the code, OpenAI for the images, Whisper for the audio, vector embeddings for the search. It's described in a Lenny's Newsletter article and a "How I AI" podcast episode. This is the closest existing case to what I'm trying to build. My approach is parallel but uses Gemini for audio understanding instead of Whisper alone, because I want the emotional and acting dimensions in the same pass.

### Layer 2: Clean it enough to use

Here the landscape is more fragmented.

**DeepFilterNet3** is widely cited as the real-time SOTA for denoising, and for good reason. It's small, it's fast, it gets good PESQ scores. But in April 2026 it has a specific compatibility problem on Windows: it imports `torchaudio.backend`, which was removed from torchaudio 2.11. If you install torch 2.11+cu128 for your RTX 5090 so you can run pyannote.audio 4.0 on GPU, DeepFilterNet stops working. You either downgrade torchaudio (and possibly break pyannote) or you use a different denoiser.

**ClearerVoice-Studio** from Alibaba's ModelScope is the open-source toolkit I'd recommend if I could install it. FRCRN, MossFormer2, speech super-resolution 16 kHz to 48 kHz, all in one package, 2 800 stars on GitHub. But its pip install depends on git clone from a source that wasn't available on the network I was on, and I didn't want to debug that path right then.

**Resemble Enhance** is open-source, two stages (denoiser plus enhancer), trained on 44.1 kHz data, and works if you install it from its repo. It's the same company that makes Chatterbox.

**noisereduce** is the fallback that always works. It's a pure scipy/numpy implementation of non-stationary spectral gating. No torchaudio dependency, no torchcodec, no GPU required, no installation drama. It's not the most sophisticated denoiser in 2026, but it handles the typical documentary problems (fridge hum, traffic rumble, steady room tone) well enough to move files from unusable to usable. When I ran it on seventy-five isolated speaker tracks, my heuristic DNSMOS scores went from a floor around 2.5 (untreated copies) to 64% of files scoring above 4.0. That's not studio-quality transformation, but it's the difference between flagging everything for manual repair and flagging nothing.

**iZotope RX 11 Advanced.** The real question people ask me is whether I found an open-source replacement for RX 11. The honest answer is no, and I'm not sure one is coming in 2026. RX 11 does things that none of the machine-learning-based denoisers do, because it's not really a denoiser: it's a spectral editor. You look at the spectrogram, you select the exact time and frequency range where the airplane passes over the interview, you apply Spectral Repair, and the airplane is gone without touching the voice underneath. No AI model does this as well as a human operator with RX 11, because the problem isn't statistical noise, it's a specific event that needs to be surgically erased.

The practical conclusion is that RX 11 is what you keep for the 5-10% of files that survive everything else. Automate the first 90% with noisereduce or ClearerVoice. Route the difficult cases to a queue you open manually in RX 11, one at a time, with Repair Assistant as your first diagnostic.

**Auphonic is not the same thing.** People sometimes suggest Auphonic as a cheaper alternative to RX 11 because both process audio and both cost money. They are not the same category. Auphonic is a batch mastering tool: it takes audio that is already reasonably clean, applies loudness normalization, EQ matching between speakers, and exports to broadcast standards. It does not do surgical spectral repair. It does not remove a passing airplane from under a voice. Its strength is automation of the last 20% of the work, not the first 20%. If your file has a fridge hum and a clipped consonant and a reverb issue, Auphonic will make the fridge hum evenly loud and normalize the level. That is not what you want.

For the documentary use case, you probably want both, at different stages: noisereduce + RX 11 for repair, then pyloudnorm or Auphonic for final leveling.

### Layer 3: Rebuild a voice

This is the part everyone asks about and the part I'm least qualified to generalize, because what you need depends on what you're doing with the clone and under what ethical framework.

**For a feature film where you need a specific real person's voice preserved across impossible shoots.** Respeecher is still the only company with verifiable feature credits in April 2026 (Mandalorian, Obi-Wan Kenobi, The Brutalist, Emilia Pérez, Better Man). They do speech-to-speech, not text-to-speech. An actor performs the line, Respeecher transforms the voice while preserving timing, breath, micro-expression. The performance is a real performance. The voice is the target voice. It's an industrial workflow, not a self-service tool. Budget accordingly.

**For a documentary where you want to generate new utterances in a real person's voice.** This is where it gets philosophically complicated. The technology is ready. ElevenLabs Professional Voice Cloning needs 30 minutes minimum (ideally 2-3 hours) of clean, mono, 44.1 or 48 kHz audio of a single speaker, with diverse intonation and emotional registers, no background music or other voices, SNR above 40 dB, no compression, no EQ, normalized to about -23 LUFS with true peak at -1 dBFS. Those specs are real specs, not marketing. They're what the model needs to extract a faithful representation. Fish Audio S2 Pro is the open-source counterpart that approaches ElevenLabs quality from 10-30 seconds of reference audio. Qwen3-TTS clones from 3 seconds under Apache 2.0. Chatterbox Multilingual (from Resemble AI, MIT license) adds perceptual watermarking that survives MP3 compression and editing — this is actually useful for documentary ethics, because it provides technical proof that a given piece of audio was AI-generated, which matters if your film is about to be scrutinized by people who will ask whether you fabricated a statement.

None of these tools answer the question of whether you should clone a voice. That's a separate conversation that I'll leave to a different essay.

---

## Part II — The pipeline

Here is the ten-phase pipeline I ended up with. Each phase produces a JSON artifact and a set of files in a known workspace location. Each phase can be re-run independently with a `--force` flag if you want to replay it with different parameters. Each phase has a fallback when its primary tool fails.

```
Phase 0  — scan_all_audio.py        walk drives, collect metadata, hash for dedup
Phase 0b — filter_by_date.py        scope restriction by capture date
Phase 0c — filter_real_signal.py    peak/rms validation, reject silent channels
Phase 1  — gemini_triage.py         30-sec sample → structured JSON classification
Phase 1b — filter_triage_results.py cross-reference triage with signal validation
Phase 3  — diarize_pyannote.py      who speaks when, per file
Phase 4  — extract_speaker.py       isolate per-speaker WAV tracks from diarization
Phase 5  — clean_chain.py           hum filter → noisereduce → quality gate
Phase 6  — (manual queue for iZotope RX 11)
Phase 7  — leveling_lufs.py         EBU R128 -23 LUFS, true peak -1 dBFS
Phase 8  — transcribe_align.py      Parakeet v3 or WhisperX + forced alignment
Phase 9  — segment_and_datasets.py  Silero VAD segments, per-model dataset builders
Phase 10 — quality_report.py        HTML report over all intermediate artifacts
```

The total code is about 2 500 lines of Python across thirteen scripts plus one PowerShell orchestrator. I'll publish the whole thing in a separate repository once it's stable. For now the interesting parts are the design decisions, not the code.

### The design decisions that mattered

**One JSON manifest per phase.** Every phase reads a JSON from the previous phase and writes a new JSON for the next. This sounds obvious but it's the thing that saved me the most time when I had to re-run specific phases after fixing a bug, because I could always resume from the last valid artifact without recomputing the earlier ones.

**Hash-based dedup at scan time.** A partial SHA-256 over the first 4 MB of each file is enough to detect mirrored drives. Two 18 TB drives that are supposedly mirrors turn out to be about 95% identical; the 5% that differ are often the interesting files. The scan produces a dedup report, downstream phases use one copy per hash group.

**Signal validation before semantic triage.** This is the fix for the Gemini hallucination problem. Measure peak dBFS, measure RMS dBFS, measure clipping percentage, measure an SNR heuristic. Anything below reasonable thresholds gets marked silent before it reaches the expensive API. Silent files are not "bad" — they're often room tone, ambient recordings, placeholder files — but they should be classified by stat, not by hallucination.

**Bypass torchaudio.load.** Three separate tools in my stack failed on the same root cause in April 2026: a missing `libtorchcodec_core4.dll` that torchaudio.load tries to use on Windows. pyannote, Silero VAD through its default loader, and DeepFilterNet's audio IO all hit this. The workaround is the same everywhere: load audio with soundfile, convert to a torch tensor, pass a `{"waveform": tensor, "sample_rate": sr}` dict to the model, and never let torchaudio touch a file path. This sounds like a workaround and it is, but it also happens to be more portable, because soundfile is stable across platforms in a way that torchaudio isn't.

**Peak normalize before VAD.** Pyannote's speaker diarization uses a VAD internally that has a threshold. If you feed it a low-level signal — say, a lavalier track recorded at -25 dBFS with -50 dBFS noise floor — the VAD can miss everything and return zero speakers. The fix is to peak-normalize to about -3 dBFS before sending the audio to the pipeline. You're not amplifying noise, you're bringing the signal into the range the model was trained on.

**Resample to 16 kHz for pyannote.** Pyannote community-1 is trained at 16 kHz. If you send it 48 kHz audio in a dict, it won't automatically resample — you have to do it yourself with `torchaudio.functional.resample`. This isn't documented anywhere obvious; I found it by diffing the internals of the file-path loader with the dict loader.

**Include the parent folder in output filenames.** A Zoom H8 session produces files called `Tr1.WAV`, `Tr2.WAV`, `Tr3.WAV`, `TrLR.WAV` in a directory called `F260228_003.zprj`. If you extract segments with stems like `Tr1`, you collide across sessions. The fix is `{drive}_{parent_folder}_{stem}`, which turns out to be also more readable.

**Signal validation shows you which channels are dead.** I filtered 298 H8 files by peak and RMS and discovered that 98% of `Tr3.WAV` files were below -80 dBFS — dead channels, microphone never plugged in for that input. Meanwhile TrLR.WAV (the stereo mix) and Mic12.WAV (the built-in MS pair) had real signal in 88 and 31 of the 190 surviving files respectively. If I had run Gemini on Tr3 first without signal validation, I would have gotten confident content classifications for silent files and built a dataset of nothing.

**Diversity selection for the cloning dataset.** Zero-shot cloning (Fish Audio S2, Qwen3-TTS, Chatterbox) needs 5-30 seconds of reference and doesn't care about diversity. Professional Voice Cloning (ElevenLabs) needs 30 minutes to 3 hours and cares a lot. For the PVC dataset I split the Silero VAD segments by duration buckets — short (3-8s), medium (8-15s), long (15-30s), any — and sampled proportionally to hit a target distribution of 40% neutral narration, 30% intonation variation, 20% emotional register, 10% natural pauses. This is where Gemini's `emotional_register` field from the triage phase becomes load-bearing.

---

## Part III — Costs, timings, and honest numbers

Running this pipeline on 298 audio files totalling 25 hours of material:

| Phase | Tool | Duration | Cost |
|-------|------|----------|------|
| Scan 34 TB across 6 drives | Python + ffprobe | 22 minutes | 0 |
| Signal validation | soundfile | 2 minutes | 0 |
| Gemini triage 298 files | gemini-3-flash-preview | ~60 minutes | ~$0.50 |
| Diarization 48 files on RTX 5090 | pyannote.audio 4.0.4 | 4 minutes | 0 |
| Extract 75 speaker tracks | ffmpeg filter_complex | 40 seconds | 0 |
| noisereduce clean 75 tracks | scipy | 2 minutes | 0 |
| Leveling LUFS 75 tracks | pyloudnorm | 30 seconds | 0 |
| Segment + build 42 cloning datasets | Silero VAD + concat | 5 minutes | 0 |
| HTML report | Python | 3 seconds | 0 |
| **Total** | | **~95 minutes** | **~$0.50** |

The scan is the longest step and it's a one-time cost. The Gemini triage scales linearly with file count; at my rate of $2 per 1 000 files, a 10 000-file triage costs $20. That's the order of magnitude. Everything else is bounded by disk I/O and local GPU throughput.

What those 95 minutes produce: 42 cloning datasets (six target models × seven diarized speakers), with the largest single-speaker dataset containing 66 minutes of clean, leveled, segmented speech ready for ElevenLabs Professional Voice Cloning. From zero to PVC-ready in an afternoon.

---

## Part IV — What I didn't do yet and why

**Transcription.** I have MacWhisper transcripts from an earlier pass on some of the material, and the pipeline supports Parakeet v3 via NVIDIA NeMo or WhisperX, but I haven't run it end-to-end on the full dataset yet. For voice cloning you don't strictly need the transcription unless you're fine-tuning (GPT-SoVITS benefits from aligned transcripts via Montreal Forced Aligner 3.3.9). For zero-shot cloning you don't need it at all.

**Embedding-based search.** Twelve Labs Marengo 3.0 is the tool I'd reach for if I wanted semantic search over the whole rushes library. The NVIDIA VSS Blueprint is the self-hosted equivalent for a local GPU. Neither of these is in the current pipeline, but both would fit as a phase 11 that builds a vector index over the outputs of phase 1.

**The legal and ethical layer.** This essay is about the technical pipeline. The question of whose voice you have the right to rebuild, under what consent framework, with what disclosure to your audience, is a separate question that I've had to think about in parallel and that I'm not going to resolve in a technical essay. For a documentary subject, SAG-AFTRA's four pillars (Transparency, Consent, Compensation, Control) are a starting point even if the subject is non-union. In an EU context, GDPR Article 9 applies because voice is a biometric identifier. Chatterbox's perceptual watermarking is an interesting technical contribution to this conversation because it provides forensic traceability, but watermarking is not consent.

**The spectral audit.** I have a `mine_all_audio.py` script running in the background as I write this that does a broader pass — 1 191 audio files across a fev-avril 2026 scope, with both signal measurement and Gemini triage — and produces an HTML report sorted like a script supervisor log. That report is what I'll use to select the final segments for the PVC upload. But at the time of writing, that's 4 hours of Gemini calls I haven't finished yet.

---

## Sources

- Fish Audio S2 release (March 2026): https://fish.audio
- Qwen3-TTS release (January 2026): https://github.com/QwenLM/Qwen3-TTS
- ElevenLabs v3 general availability (March 2026): https://elevenlabs.io/blog/eleven-v3-is-now-generally-available
- Voxtral TTS (Mistral, March 2026): https://mistral.ai/news/voxtral-tts
- pyannote.audio 4.0: https://github.com/pyannote/pyannote-audio
- noisereduce: https://github.com/timsainb/noisereduce
- DeepFilterNet: https://github.com/Rikorose/DeepFilterNet
- iZotope RX 11: https://www.izotope.com/en/products/rx
- Tim McAleer / Florentine Films interview: https://www.lennysnewsletter.com/p/nobody-wanted-to-do-this-work-how
- Twelve Labs Marengo 3.0: https://www.twelvelabs.io
- NVIDIA VSS Blueprint: https://github.com/NVIDIA-AI-Blueprints/video-search-and-summarization
- emotion2vec (ACL 2024): https://github.com/ddlBoJack/emotion2vec
- Chatterbox Multilingual (Resemble AI): https://www.resemble.ai/introducing-chatterbox-multilingual-open-source-tts-for-23-languages/
- Respeecher film credits: https://www.respeecher.com/voice-cloning-film-tv

---

*This essay is part of the [deep-research](https://github.com/12georgiadis/deep-research) series. It describes a pipeline built for a specific film project but written so the technique is portable. The specifics of that project, including the identity of the subject whose voice is being processed, are not part of this essay and will not be until the film is finished.*
