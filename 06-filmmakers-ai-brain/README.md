# The Filmmaker's AI Brain

> A living architecture for cinema memory. Built in public, updated as it's built.
> By [Ismaël Joffroy Chandoutis](https://ismaeljoffroychandoutis.com)

---

## Manifesto

I film real people.

My subjects are people who used the internet as a machine for self-invention, who produced fictions so dense they became indistinguishable from the real. Dozens of identities, thousands of posts, mythologies built from nothing.

I film them with tools that do exactly the same thing.

This tension — between the documentary gaze and the generative instrument — is where I work. Not post-documentary in the academic sense. Something closer to what I call **traboulage**: the permanent passage between real and fiction, maintaining a vortex rather than a boundary. The image recognizes both its origin in the real and its passage through a synthetic process.

The problem is not technical. The problem is memory.

---

### What cinema memory looks like today

Years of research on a single subject. Tens of thousands of posts across multiple platforms. Dozens of interview files. Court documents. Screenshots of deleted accounts. Articles in three languages. Voice recordings. Academic papers. My own notes written at 2am when something clicked.

And a folder structure that makes none of it findable.

I know what I filmed last Tuesday. I don't know what I read three years ago that would change how I understand what I filmed last Tuesday.

Existing tools solve the wrong problem. They organize. They sync. They tag. They build hierarchies I don't have time to maintain. They assume I know, at the moment of capture, where something belongs and why it matters.

I don't. Nobody does. That's not how research works. That's not how cinema works.

---

### The real problem: keyword search is dead for creative work

When I need to understand how a subject's self-mythology connects to the Narcissus archetype I encountered in a paper three years ago — neither the subject's name nor "Narcissus" will find it if I didn't use those exact words.

Cinema operates on **resonances**, not keywords. Between an image seen twenty years ago, a sentence read last week, and a face filmed this morning. The connection that produces a film is almost never the one you were looking for. It's the one you stumble into because your memory is structured the right way.

My memory is not structured the right way. No human memory is.

---

### The instrument I'm building

A local, private, AI-native knowledge base that understands **meaning**, not keywords.

Not a productivity system. Not a second brain in the self-help sense. Not another app competing for my attention.

A creative instrument. Built from the premise that **alteration matters more than augmentation** — I don't use AI to do things faster or better. I use it to displace my own thinking, to create productive friction, to find connections I would have missed.

This instrument runs entirely locally. On a Mac Mini M4 that never sleeps.
No cloud lock-in. No subscription that breaks when I need it most.
The files are markdown on disk. The models are local when possible.
Data sovereignty is not a technical preference — it's part of the practice.

This connects to what I've been calling **permacomputing** in my work: local AI, reuse over replacement, carbon footprint as an aesthetic and ethical position. The filmmaker's brain should not depend on a server farm in Oregon.

---

### Liquid writing, extended

My method is **liquid writing**: the dissolution of boundaries between research, writing, shooting, and editing. These are not discrete stages. They are continuous flows that contaminate each other. A research note becomes a scene. A scene becomes a theoretical position. A theoretical position changes what I'm looking for in the archive.

The AI brain I'm building is an extension of this method into memory itself.

When Claude Code can search across five years of research by meaning — not by folder, not by filename, not by keyword — liquid writing becomes possible at a scale it couldn't reach before.

Query: *"What do I know about the relationship between physical space and psychological state in confined environments?"*

The system returns: chunks from a research archive, a fragment of a Bachelard essay I saved years ago, three frames from a reference film I described in a note, a voice memo I recorded walking in a city, an architectural diagram.

None of these contain the same words. All of them belong to the same question.

---

### Why local. Why now. Why this.

The cloud solutions exist. Claude Projects handles up to 2 million tokens. Notion AI organizes. Readwise remembers what you highlighted.

But they are **web-only**. They are someone else's infrastructure. They can change their pricing, their terms, their availability. They cannot be integrated deeply into a creative workflow that runs on custom scripts, local models, and a terminal.

And crucially: they cannot be queried by an AI agent *during* the work. I want Claude Code, while writing a treatment, to silently reach into years of research and pull up what is relevant — without me having to ask, without me switching tabs, without me breaking the flow of thought.

That's not possible with a web app. That requires a local vector database exposed through an MCP server.

---

### External signal (February 2026)

The CEO of Google DeepMind publicly named Claude Code as doing *"something special"* in the developer market — and described the industry's broader direction as building *"a kind of universal digital assistant that helps you in your everyday life, that needs to understand the world, the context around you, the physical world."*

That's the industry's answer to interface fragmentation: one surface that reasons across everything. Smart glasses, ambient AI, the physical world as input.

The CLI is the same answer, from a different direction — and for a different purpose. Not ambient. Not worn. Deliberate. A single surface where Claude Code reasons across five years of research, an open archive, three projects, a vault, without switching tabs, without being asked, without breaking the flow of thought.

He also identified multimodal — image, video, audio as *native* I/O, not add-ons — as the foundational capability for assistants that understand the physical world. Cinema has always been this. This stack is designed to reflect that: not text retrieval with media bolted on, but a memory where text, image, sound, and moving image are searched in the same semantic space.

The universal assistant the industry is racing to build for everyday life — this is the filmmaker's version. Local. Intentional. Built for the work.

---

## Architecture

```
                         INPUT
┌──────────────────────────────────────────────────────┐
│  Telegram Bot      │  Web Clipper    │  Manual import │
│  links, text,      │  articles,      │  rushes, PDFs, │
│  voice notes,      │  web pages      │  transcripts,  │
│  images from phone │                 │  court docs    │
└──────────────────────────────────────────────────────┘
                            ↓
                         STORAGE
┌──────────────────────────────────────────────────────┐
│                 Obsidian Vault                       │
│           Local markdown files on disk               │
│    Readable by Claude Code natively, no API needed   │
│    Structured with CLAUDE.md navigation per folder   │
└──────────────────────────────────────────────────────┘
                            ↓
                        EMBEDDING
┌──────────────────────────────────────────────────────┐
│  Text      →  text-embedding-3-large (OpenAI)        │
│  Images    →  CLIP (semantic visual search)          │
│  Audio     →  Whisper (transcription) → text → embed │
│  Video     →  Gemini Flash 3.1 (analysis) → text → embed│
└──────────────────────────────────────────────────────┘
                            ↓
                        RETRIEVAL
┌──────────────────────────────────────────────────────┐
│         Qdrant — local vector database               │
│         Running in Docker on Mac Mini M4             │
│         Always on. Never synced to cloud.            │
└──────────────────────────────────────────────────────┘
                            ↓
                          ACCESS
┌──────────────────────────────────────────────────────┐
│         Custom MCP Server → Claude Code              │
│   Semantic search native in every working session    │
│   No context switch. No tab switching. No friction.  │
└──────────────────────────────────────────────────────┘
```

---

## Roadmap

### Phase 1 — Text RAG
*The foundation. Research, articles, scripts, transcripts, notes.*

- [ ] Obsidian vault structure with `CLAUDE.md` navigation files per project folder
- [ ] Telegram bot: link or text → scrape/process → Claude API categorize → save as `.md` in correct folder
- [ ] Embedding pipeline: vault contents → Qdrant (local Docker)
- [ ] Custom MCP server exposing semantic search to Claude Code
- [ ] Auto-sync: new or modified files trigger re-embedding

**Concrete use case:** During a writing session, ask: *"What do I know about the gap between public persona and private reality?"* — returns relevant chunks from archived research material, interview transcripts, academic papers, and personal notes. Without me leaving the terminal.

### Phase 2 — Image RAG
*Visual memory. Film stills, reference images, moodboards, scanned documents.*

- [ ] CLIP embedding pipeline for images stored in vault
- [ ] Unified vector space: text and image searchable together
- [ ] Cross-modal queries: describe a visual atmosphere, retrieve matching images

**Concrete use case:** *"Find all my visual references with industrial light, surveillance, and loneliness"* → returns images from my reference folder, stills I saved from other films, moodboard captures — even if none of them are labeled that way.

### Phase 3 — Audio RAG
*Dialogue, field recordings, music references, voice notes.*

- [ ] Whisper transcription pipeline (automatic for all new audio files)
- [ ] CLAP embeddings for atmospheric sound search (beyond transcribed speech)
- [ ] Voice note captured on phone → transcribed → embedded → searchable within minutes

**Concrete use case:** I recorded a voice memo walking in a neighborhood that felt right for a scene. Six months later, I can find it by describing the feeling, not by remembering the filename.

### Phase 4 — Video RAG
*Rushes, reference footage, interview recordings, found footage.*

- [ ] Gemini Flash 3.1 integration for scene-level video description
- [ ] Keyframe extraction + CLIP embedding
- [ ] Timecode-level search: retrieve the exact moment, not just the file

**Concrete use case:** *"Find the moment in my rushes where the subject stops performing and something true comes through"* — this is a montage decision that currently requires watching everything. With video RAG, it becomes a query.

This is the promise of AI for cinema that nobody has delivered yet. Not as a filter effect. Not as a generation tool. As a **memory instrument for the editing room**.

### Phase 5 — Active Intelligence
*The system works without being asked.*

- [ ] Morning briefing: reads vault + current projects + deadlines → surfaces what matters today
- [ ] Project-specific context: `/project-brief` synthesizes everything relevant to the current project state
- [ ] Pattern detection: *"You've been saving a lot about identity fragmentation this week"*
- [ ] Automatic cross-project connections: finds when research on one project illuminates something in another
- [ ] Opportunity surfacing: flags calls for projects, festivals, residencies that match current work

---

## Stack

| Layer | Tool | Why |
|-------|------|-----|
| Notes | Obsidian (local markdown) | Claude Code reads files directly, zero API |
| Capture | Custom Telegram Bot | Frictionless, mobile-first, handles text + links + voice + images |
| Text embeddings | OpenAI `text-embedding-3-large` | Best quality/cost for semantic search |
| Image embeddings | CLIP | Open source, text-image unified vector space |
| Video understanding | Gemini Flash 3.1 API | Long-context video analysis, multimodal natif |
| Audio transcription | Whisper (local) | Privacy, speed, no data leaving the machine |
| Vector DB | Qdrant (Docker, local, Mac Mini M4) | Best local performance, open source, free |
| Retrieval interface | Custom MCP Server | Native Claude Code integration |
| Orchestration | Claude Code | The creative collaborator, not just the query interface |
| Compute (current) | Mac Mini M4 (always-on, Paris) | Local, private, permacomputing-aligned |
| Compute (target) | Mac Studio M5 Ultra, 512GB RAM | Full local model inference at scale |

---

## Philosophy

Memory is not storage. Storage is passive. Memory is generative — it creates connections that were not there before.

The difference between a filmmaker who forgets and a filmmaker who remembers is not talent. It is architecture.

What I'm building here is not a database. It is an attempt to give artificial memory the **associative quality of human memory** — the capacity to connect what was experienced, what was read, and what is being made right now — without the forgetting.

The difference between keyword search and vector search is, philosophically, the difference between an index and a mind. An index knows where things are. A mind knows what things mean in relation to each other.

For cinema, this distinction is everything. A film is not made from what you remember. It is made from what you remember **connecting to something else**.

---

### On sovereignty

This system is built to be owned, not rented.

Every tool in this stack can run locally. Every file is a readable text file. Nothing lives in someone else's database. The creative memory of an artist should not be a line item in a SaaS subscription that can be discontinued, acquired, or price-hiked.

This is not paranoia. It is a lesson from the subjects I film: what happens to identity when it exists only on platforms that can delete it.

The filmmaker's brain should not have the same vulnerability.

#### On local models

The current stack uses Claude Code as the orchestration layer and OpenAI for embeddings. This is a pragmatic starting point — the best tools available now, running on a Mac Mini M4.

The target is different: a **Mac Studio M5 Ultra with 512GB unified memory**, running frontier-scale open models locally. DeepSeek, Kimi, and whatever comes next. At that scale, the entire stack — embeddings, retrieval, generation, orchestration — runs on one machine, air-gapped from any cloud if needed.

The architecture is designed for this transition. Swap the model endpoints. Keep everything else.

This is not a preference for complexity. It is the logical conclusion of the sovereignty argument: if the creative memory of a filmmaker should not depend on a SaaS subscription, neither should the intelligence that queries it.

---

### On the architecture question

This stack uses LLMs — Claude Code, OpenAI embeddings — because they are the best current tools. That's a pragmatic position, not a theoretical one.

The underlying position is closer to Yann LeCun than to the labs betting on scaling alone: LLMs are limited architectures. Autoregressive token prediction is not how intelligence works. Not how cinema works. Not how memory works. World models — systems that reason in abstract representation space, that understand the physical world through prediction rather than surface completion — is where the structurally interesting work is.

Two modes coexist in this practice. One is operational: use current LLMs as instruments for structured tasks — retrieval, writing, categorization, research. The other is experimental, and dominant: treat the model's limits as material. Work with what the architecture *cannot* do. Let the gap between what an LLM claims to understand and what it actually models become the subject. This is the riskier mode. It's also the more artistically honest one.

The filmmaker's AI brain belongs mostly to the operational mode — it's infrastructure. But it is built to serve a practice where the experimental mode leads.

This system is also built to survive the architecture transition. When world models exist that can be run locally, the vault, the MCP layer, the retrieval structure remain. The intelligence changes. The memory persists.

---

### On building in public

This repository is a living document. It is updated as the system is built — not as a demonstration of something finished, but as the record of something becoming.

The architecture *is* the work, as much as the films it serves.

---

## Status

**Current phase:** Pre-implementation. Architecture defined. Phase 1 in progress.

Active projects this system will serve: two feature documentaries currently in development.

---

## Author

**Ismaël Joffroy Chandoutis**
Filmmaker and artist. Paris.
César 2022 (short documentary).
Working at the intersection of post-documentary cinema, contemporary art, and artificial intelligence.

[ismaeljoffroychandoutis.com](https://ismaeljoffroychandoutis.com)
