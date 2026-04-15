# The Timeline Becomes Readable

*Ismaël Joffroy Chandoutis — April 2026*

---

For a few weeks now, I have been able to talk to Final Cut Pro. Not through AppleScript, not through a brittle UI automation that clicks on buttons and hopes nothing moves, not through an external workflow that exports, transforms and reimports. I can speak to it directly, inside its own process. An Objective-C dylib injected into FCP exposes 78,000 classes, its entire runtime, over JSON-RPC on a local socket. The tool is called SpliceKit. Claude Code, via MCP, sends calls like `timeline_action("blade")`, `get_timeline_clips()`, `blade_at_times([3.0, 6.0, 11.2])`, `detect_scene_changes()`, `export_xml()`, `open_transcript()`. And FCP responds. It cuts, it splits, it returns data structures. It obeys, or rather it dialogues, because it is no longer really obedience when the agent on the other side can read what the application contains.

The phrasing that drifts everywhere, the one found in commercial brochures and LinkedIn threads, is "AI helps with editing". It is wrong. Or rather it misses what is happening. It is not that AI is becoming a slightly more competent assistant proposing rough cuts. It is that the timeline, this object that until now was opaque, locked inside a graphical interface designed for one human and one human at a time, becomes a data structure. Readable. Writable. Traversable by an agent that can, all at once, consult the screenplay, search the transcription, list the clips, decide where to cut, apply the effect, export the FCPXML to pass to Resolve, and start over. The difference is not one of degree. It is one of nature. A file that was a fortress becomes a database.

We have to stop for a second on what this concretely means. When I run `get_timeline_clips()`, I get back the full list of clips with their timestamps, their source file names, their durations, their positions in the timeline, the effects applied. When I run `get_transcript()`, I have the full text of what is being said, aligned to the thousandth of a second with the images. When I combine the two, I have something no editor before 2025 ever had in real time inside their editing software: a textual, searchable representation of the film as it exists at that very instant. I can ask the agent "find me the passages where Joshua lowers his voice for at least four seconds right after saying the word brother" and it finds them. Not because it is magical. Because the timeline has become text, and text is what these models know how to read.

---

`blade_at_times()`: the cut as instruction. No longer as a decision stemming from a perception, a hesitation, a backward glance in the editing room at three in the morning. The cut as a parameter passed to a function. This is not an acceleration of editing. It is a shift in ontological regime.

Farocki, in *Eye/Machine*, showed that the camera of a guided missile does not see. It calculates. It matches patterns to coordinates and triggers an action. What interested him was the absence of subjectivity in this process: no doubt, no ambiguity, no "maybe". Operational vision is binary by construction. It selects in order to act, not in order to understand.

`get_transcript()`: extracting the text of speech without listening to speech. `detect_scene_changes()`: perceiving discontinuity without ever having perceived continuity. The machine accesses the structure of the film without ever traversing the experience of the film. It reads the timeline like a database. What the editor constructs image by image, hesitation by hesitation, the agent walks through like a directed graph.

If `blade_at_times()` works, it is because the cut was already, at least partly, formalizable. Because the rules of classical editing had an operational logic buried under the discourse of intuition. What Kuleshov understood in 1920, the dylib injected into the FCP process confirms in 2026: editing obeys rules. AI does not invent them. It extracts them.

But here is what stops me: `export_xml()`. The film exits the machine. It becomes image, duration, experience again. It is going to be watched by a body. And that body will not know whether the cut was made by a trembling hand or by an instruction without hesitation. That is where the political begins. Not in the operation, but in the invisibility of the operation.

---

This shift dissolves boundaries I believed were stable. Pre-production, editing, post-production, these three regimes that have structured my work since I started making films, were not separated by nature. They were separated by infrastructure. The screenplay lived in a word processor, the rushes in a folder, the edit in FCP, the grade in Resolve, the VFX in After or Blender, the render in yet another chain. Each passage from one tool to the next was an airlock, an export, a loss, a friction that forced you to finish one step before moving on to the next. Now, a single agent reads the screenplay, queries the timeline, asks ComfyUI for a previz, calls back FCP to adjust the cut, exports to FCPXML, passes it to Resolve for a rough grade, gets the result back, reinjects it. The airlock no longer exists. What exists is a graph where each piece of software has become a node. FCP is no longer a destination, it is a callable function. Resolve the same with its Python API. Blender the same. ComfyUI already was, that is its essence.

The chain: `rush_indexer → story_structure → timeline_writer → color_grade → vfx → export`. A single call. An agent that traverses everything. This is not science fiction. It is plumbing. The plumbing is done.

There is something vertiginous in what this reveals, and it is not the technology. It is the speed at which we accept no longer seeing the difference.

Editing has always been, at its core, a political gesture. It says: the meaning was not in the image, it was in the order we chose for it. Changing the order is changing what can be thought. What changes with an agentic system is that this political gesture is now made within a frame the author no longer sees entirely. The timeline becomes a data structure, we say. But a timeline is an argument. It is a decision about what precedes what, about what is cause and what is effect, about which face you see just before hearing certain words. These decisions have always been political. They still are. Except that now they can present themselves as the outputs of optimization.

The tool that frees you is the one whose constraints you can see. The system that captures you is the one that convinces you it has none.

---

The rush index is the keystone. Without it, everything else is just slightly faster automation. With it, it is something else. Indexing a rush does not mean sticking a label on it. It means extracting several layers from it: recognition of scenes and characters, diarization that separates voices, aligned transcription, analysis of camera movements, shot-by-shot compositional analysis, affect analysis, mapping of silences, mapping of light, mapping of chromatic dominants. Each clip becomes a small dense document. The entire film, before even being edited, becomes a searchable library. And this library is the memory of the film, the real one, not the one I build for myself by rewatching rushes in no particular order at two in the morning. The agent does not get tired. The agent remembers everything.

For Goldberg, this changes the film. Not metaphorically. The film has several image regimes that do not naturally speak to one another: messy internet archives, glitched streams, YouTube videos re-edited hundreds of times, reconstructions shot on a clean digital stage, direct footage of Joshua when he is available, PACER fragments, screenshots, documents. Each of these regimes has its texture, its rhythm, its rules. Editing Goldberg by hand is trying to hold together six or seven different cinemas with a single brain that forgets half of what it saw the day before.

What becomes possible, and was impossible before: treating the personas as voices in the Bachian sense. MoonMetropolis, AustraliWitness, Emily\_Americana are not parallel timelines to cut side by side. They are counter-subjects that answer each other, contradict each other, imitate each other. An agent that has indexed the 35,507 posts can treat the database like a score and search for moments when several personas coexist within the same week, or even the same day. What the human eye cannot do on 23 megabytes of raw JSON. It can propose cross-editing between a 2014 stream and a 2026 reconstruction based not on narrative content but on correspondences of texture, cadence, dominant tone. Make a previz in ten seconds of what would take two days. Generate fifty variants according to fifty parameters.

The liquid writing becomes liquid in both senses: the narrative structure flows back up into the shoot, and the shoot can now inform the structure in real time. The border between research and editing dissolves. This is not a tech promise. It is the description of what is already happening.

---

What strikes me, and what seems to me to be what the film must absolutely look in the face, is that Goldberg talks about identity fragmentation online, about multiple personas, about a presence that dissolves into regimes, and the tool with which I am editing it is exactly that too. The subject of the film and the technical device enter into resonance. Joshua, as Mark Fisher might have written, is a figure of digital hauntology, a presence that persists as an echo in thousands of forums, threads, removed and reuploaded videos, dead and resurrected accounts. Editing this film with an agent that itself navigates between regimes, that brings to life simultaneously shots filmed in 2026 and captures from 2014, that holds the memory of every fragment, is no coincidence. It is one of the rare times I have the impression that the tool is not merely executing the film but embodying something of it. The liquid timeline for a film about a liquid identity.

---

There remains the question that keeps you awake, the one you have to ask because it will not go away on its own. When the agent can read the film and write it, who is editing? If I ask for fifty variants and choose one, am I editing, or am I selecting? And what if the distinction between editing and selecting was itself a retrospective illusion, a way of telling ourselves that our editorial gesture had a pure, unique origin when it has always been a negotiation with the material, with time, with fatigue?

Deleuze said that the time-image is never reducible to what the editor decides, that it emerges from a relationship to duration that exceeds intention. Perhaps the agent does not dispossess. Perhaps it simply makes visible what was already the case, namely that editing has never been only about imposing a will on raw matter, but listening to what the matter was asking for, and that now there is a collaborator who listens at a speed no human can reach.

Or perhaps it really does dispossess, and we have to accept it, and look in that dispossession for a new form of authorship that is no longer the one who makes but the one who decides what counts. I don't know. I know that tomorrow I will open FCP, launch an MCP call, ask the agent to show me the passages where Joshua talks about his father, and it will show them to me in three seconds. And there, in front of the list, with the whole film opening like a database under my fingers, I will have to decide something.

The question is not whether the agent replaces the editor. The question is what form of decision remains to be made when everything else has been read, written, indexed, proposed. And what do we call a film when the film lets itself be read?

---

*Written with Claude Opus (Anthropic), Harun Farocki, Adam Curtis, Ismaël Joffroy Chandoutis. FCP 12.2 / macOS 26.3 / SpliceKit MCP — April 2026.*
