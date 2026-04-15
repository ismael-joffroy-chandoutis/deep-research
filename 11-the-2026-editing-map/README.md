# The 2026 Editing Map

*From the Steenbeck to the Agentic: There Is No Universal Answer*

---

I have been editing since the Steenbeck era. The real one, the mechanical flatbed with its spinning reels, the 16mm strip gliding between the heads, the sound of the motor racing when you released the brake. Then came Avid Media Composer in the late 90s, then Final Cut Pro 7 which swept everything away, then Premiere which took its place when Apple broke FCP 7 into FCP X, then Resolve which rose, then FCP 12 which came back, then CapCut which I use when I need to ship fifteen stories in twenty minutes. In between there was Lightworks, Edius, Scratch, Vegas, iMovie, DaVinci Resolve 12 which was still a disguised grading tool, Kdenlive on an old Linux laptop when I was a student, and even a cracked version of Sony Vegas a friend had slipped me in 2005.

Thirty years of tools, from celluloid to the agentic. I have no religion. I have never had a religion. An editing tool is an object negotiated with a project, not a tribal flag.

This article is a compass, not a stance. I will try to say where editing stands in April 2026, with the contenders that matter, with the angle that actually interests me (not the hype), and with a central thesis I have held since the Steenbeck and hold even more strongly today: there is no good editing tool. There is a good tool for a given project, at a given moment, with a given team. Everything else is forum noise.

---

## The 2026 Scene

Let us start by listing the real contenders. Not the tools that exist, but the ones people actually use to make films and audiovisual objects in 2026.

**Final Cut Pro 12.2** (macOS 26.3 and up). Apple has finally woken FCP up after a maintenance period. Version 12 brought back native scripting, integrated ML transcription, a new proxy engine, and above all it let through a silent but enormous event which is the main reason I am writing this article. I come back to it below.

**DaVinci Resolve 20 Studio**. Blackmagic keeps stacking. Resolve 20 further improved the Fairlight side, shipped a neural engine for object recognition in the rushes, and pushed Fusion integration even further. The Python API is still there, solid, documented, and the Lua API has become cleaner than it used to be. It is the Swiss army knife that now knows how to sew, iron and cook. But sewing and ironing in the same tool produces a strange seam.

**Adobe Premiere Pro 25.6**. Adobe switched to UXP in December 2025 to replace the old ExtendScript. It was necessary, it is still rough, but it opens a real future for Premiere scripting. Experimental MCP prototypes are starting to circulate on GitHub. Nothing productized yet.

**Avid Media Composer 2025**. Still the reference for broadcast television, traditional Hollywood fiction, industrial post-production. MediaCentral for collaborative work, robust bin locking, multi-editor management proven for twenty-five years. The interface is showing its age. But that is not where Avid plays its hand.

**Blender 4.4 VSE with Pallaidium**. The Blender Video Sequence Editor was not taken seriously five years ago. Today, with Pallaidium exposing ComfyUI, SDXL, SD3, Flux and the whole AI generation chain directly inside the Blender timeline, it is a hybrid NLE plus generator plus compositor plus 3D that resembles nothing that existed before. It is not a tool for editing a feature film. It is a laboratory.

**CapCut Pro**. ByteDance has turned CapCut into a horizontal content machine that now runs on desktop as well as mobile. The output speed is absurd. For a social media cut, it is direct, there is no debate.

That is the scene. Six genuinely used tools, plus a few outliers worth mentioning in passing (Lightworks, Kdenlive, Resolve 20 Free which remains an incredible entry door). Each has its domain of relevance. None is universal.

---

## The AI-Native Outliers (and Why I Don't Believe in Them Yet)

There is a seventh category I have to mention to be honest about the landscape, even though I do not believe in it yet. These are the tools that start from AI generation and bolt a timeline on top, rather than the other way around.

**LTX Studio** (Lightricks). Storyboard-to-video approach. You describe your scene, the tool generates the shots, you can arrange them on a rudimentary timeline. Good for concept previz, investor pitches, video moodboards. The timeline is poor: no JKL responsiveness, no serious multi-layer trim, no frame-accurate precision in the sense an editor understands the term.

**Runway Gen-4** and **Pika 2.0**. Text-to-video and image-to-video generation. They have added basic assembly features since 2025. These are not NLEs. They are generators with a direct export.

**Adobe Firefly Video** inside Premiere. Adobe has integrated its Firefly engine directly into the Premiere timeline since late 2025. Inline generation, fill, extend, reframe. This is interesting because it puts AI generation inside a real NLE, not inside an AI tool pretending to be an NLE. But Firefly Video remains less powerful than what you can do with ComfyUI on a local RTX 5090.

**Sora** (OpenAI) as a standalone app. Since early 2026, OpenAI has shipped a Sora app with a minimal timeline to arrange its generations. Same critique as LTX Studio.

**Krea.ai**. Unified AI creation tool with video export. An embryonic timeline, but climbing the ladder fast.

The problem with this category is that it conflates generation and editing. Generating a ten-second clip and stacking it next to another is not editing. Editing is deciding where to cut, at what exact moment, in what relation to the adjacent duration, with what awareness of the overall breathing of the sequence. None of these tools offers the granularity a professional editor demands. They are designed for people who output content, not for people who edit films.

They resemble CapCut in the poverty of the timeline, but it is another philosophy. CapCut owns the fact that it is fast and mobile-first, it does not pretend to be anything other than a social production tool. These AI-native tools, on the other hand, claim to be complete creation studios, when their editorial side is weaker than iMovie. That gap is what makes me skeptical.

I am not saying they have no place. LTX Studio for an investor pitch previz, Runway for generating a shot we then pull back into FCP, Sora for testing a visual idea in two minutes, yes. They work very well as **sources** in my chain. But as **destinations** (where you actually edit a film), they do not hold up. And for now I see no signal to make me believe they will become real NLEs. Because the editorial part, the thirty years of accumulated heuristics, shortcuts, flow, magnetic timeline, that cannot be caught up by adding a basic drag-and-drop on top of a generator.

Unless I am surprised. I am staying alert. If LTX ships a serious timeline in 2027, I will revisit this article.

---

## The Axis That Matters: Engineering vs Creativity

The real FCP vs Resolve debate, the one that has dragged on since 2019 across every post forum, is poorly framed. It is not a technical debate. It is a debate in design philosophy.

DaVinci Resolve is conceived by broadcast video engineers. Blackmagic is a company of engineers. You can see it. You can feel it in every panel, every menu, every shortcut. The tool was designed so that an operator can do precise, reproducible, verifiable things. Everything is parameterizable, everything is exposed, everything is technically correct. When you look at the Fusion effects tree, it is a DAG (Directed Acyclic Graph) for compositing, which is exactly what a VFX engineer wants to see. When you open the Color page, you have a broadcast colorimetry console with scopes, 3D LUTs, ACES workflows, CDLs. It is an incredibly powerful tool.

But it is not a fun tool. Editing on Resolve is work. It is not stepping into an extension of thought. It is piloting a console. And when I am editing an auteur film, I do not want to pilot a console. I want the tool to disappear, I want my gesture to be as close as possible to the image and the rhythm, I want the timeline to be a surface for thinking and not a dashboard.

Final Cut Pro does the exact opposite. FCP was designed by people who understood that an editor is not an operator. The magnetic timeline, which was mocked for ten years by FCP 7 purists, is in fact the most beautiful editorial idea of the 2010s. It breaks the track-based model inherited from VTRs and replaces it with a logic of clips that attract each other, repel each other, hierarchize by relation rather than absolute position. When you skim a rush by simply pressing the space bar or hovering with the cursor, without ever clicking, without ever loading, you are in direct contact with the material. It is the closest thing I have found to the gesture of the Moviola, or a Steenbeck turned by hand.

FCP is a solo creative's tool. Built for someone who is in contact with the film and wants nothing to stand in the way. That is its strength and its limit. Because as soon as there is more than one of you on the project, FCP starts to punish you.

Both philosophies are legitimate. An eight-episode Netflix series, with three assistant editors, two lead editors, a supervisor, daily rush management and a VFX pipeline feeding back in, is an engineering project. Resolve is at home there. An auteur long-form film where I am alone with 200 hours of rushes and six months of editing is a creative project. FCP is at home there.

It is not FCP vs Resolve. It is solo creative project vs collective engineering project. Both exist, both are noble, both call for different tools.

---

## Collaboration: Where FCP Really Loses

Let us be honest about FCP's number one flaw. For a long time, multi-user collaboration was Apple's blind spot. A .fcpbundle is a macOS bundle that does not like being shared. Several editors on the same project at the same time is the recipe for guaranteed corruption. Apple looked away for years.

Resolve, for its part, has been natively multi-user since Resolve 12. Shared PostgreSQL database, bin locking at the database level, several editors who can open the same project on different machines, each with their own bin, their own timelines, transparent commits and syncs. It is clean. It was designed by people who have worked in broadcast TV and who know what a team of twenty on a feature means.

There is a partial answer on the FCP side called PostLab, made by Hedge. PostLab adds a layer of version control and sync on top of .fcpbundles. It works surprisingly well. For a team of two to four editors, it is largely sufficient. I have used PostLab on two projects, no corruption, no unmanageable conflicts, a two-hour learning curve. But it is not true multi-user. It is git-for-FCP-projects. It simulates collaboration, it does not permit it simultaneously at the bin level.

Verdict. For a team of two to four: FCP plus PostLab is more than enough, especially if you care about FCP's editing speed. For a team of five or more, for broadcast, for a workflow where the assistant editor has to work on the same rushes at the same time as the lead editor: Resolve wins without discussion. That, by the way, is why the big Netflix productions and Fincher himself have fallen back on Resolve or on Premiere with Team Projects. It is not a matter of taste. It is a matter of workflow engineering.

---

## The New Paradigm: The Agentic

Up to now I have described a landscape that already existed in 2024. The real shift took place between late 2025 and April 2026. And it concerns something no NLE benchmark has yet managed to measure: real-time programmability by an AI agent.

Here is what happened. An independent developer published on GitHub a dylib that, injected into the Final Cut Pro process at runtime, exposes the entire Objective-C runtime of the application through a JSON-RPC server. Not an official Apple API. Not an anemic AppleScript scripting. The real ObjC runtime, the 78,000 internal FCP classes, accessible from the outside in JSON. The project is called SpliceKit.

This week, I contributed to the project. I patched a crash bug on macOS 26.3 with FCP 12.2 build 447037. Four different crash sites that had to be bisected one by one because the internal structure of certain FCP classes shifted between macOS 26.3 and 26.4. Discussion with Chris at LateNite Films (latenitefilms) who maintains CommandPost and runs macOS 26.4 where the bug did not exist. Pull request submitted (#51 on elliotttate/SpliceKit), guard added for version detection, crash resolved. A technical anecdote, but one that says something about the state of the field: a solo creative can today patch the bridge that lets an AI drive their NLE. Five years ago that sentence made no sense.

On top of SpliceKit, an MCP (Model Context Protocol) server currently exposes over 200 tools to a Claude Code agent. Claude can directly call `blade_at_times([12.3, 45.6, 78.9])` to place cuts at those timecodes. It can call `get_transcript()` to retrieve the native FCP 12 transcription. It can call `detect_scene_changes()`, `apply_effect()`, `export_xml()`, `capture_timeline()` which screenshots the timeline live through the macOS Metal API without FCP even being in the foreground. It can branch a sequence, apply an alternative edit to it, export an FCPXML, pass that FCPXML to another agent that will open it in a second dual timeline window for comparison. All of this in real time, inside the same FCP process, without AppleScript, without UI automation, without keyboard emulation, without a hack.

This is a first. I weigh the word. It is the first time an NLE has become truly programmable in real time for an AI agent. Resolve has had its Python API since 2019, and it is useful, but it is slow (out-of-process communication via lock files), limited to the objects officially exposed by Blackmagic (a few hundred, not 78,000), and it gives no access to the internal runtime of the application. Premiere has had UXP since late 2025, too young, too unstable, no productized MCP yet. Avid has a legacy COM from the 90s that is essentially UI scripting. CapCut, zero.

What this changes concretely. I am editing Goldberg with an agent that reads my 200 hours of rushes while I sleep. The agent transcribes, indexes, classifies, proposes candidate scenes, generates draft sequences that I find in the morning in my FCP library. When I enter the timeline, I am not starting from zero, I am starting from a first layer prepared by an intelligence that read the entire material faster than I could. It is not augmentation. It is not the agent editing in my place. It is a new kind of pressure pushing on the creative gesture. It is an extension of liquid writing (my permeable writing methodology) applied to post-production.

The geopolitical consequence for the NLE market is paradoxical. FCP, which was the least programmable tool in appearance because Apple gave no official API, has become in 2026 the most programmable NLE on the planet thanks to a community hack. Resolve remains more programmable on the side of stable, sanctioned official scripting. FCP has become more programmable on the side of depth of runtime access and real-time agent integration. These are two different axes of programmability, and 2026 is the year both exist at the same time.

---

## Comparative Matrix for Editing

Here are the numbers I propose, with the following warning. These scores are not universal truths. They are debatable markers, drawn from my real usage over the last six months. If your scores differ, it is because your project differs. That is the central point of this article.

| Criterion | FCP 12.2 | Resolve 20 | Premiere 25.6 | Avid MC | CapCut |
|---|---|---|---|---|---|
| Fun edit speed | 9/10 | 5/10 | 6/10 | 4/10 | 8/10 |
| Native collaboration | 2/10 | 9/10 | 7/10 | 8/10 | 5/10 |
| With PostLab (Hedge) | 7/10 | N/A | N/A | N/A | N/A |
| Scripting API | 10/10 via SpliceKit | 8/10 Python/Lua | 5/10 UXP | 3/10 legacy | 0/10 |
| Real-time AI agent | 10/10 | 6/10 prototypes | 3/10 | 0/10 | 0/10 |
| Built-in transcription | 9/10 native ML | 7/10 Studio | 8/10 Adobe Speech | 5/10 | 9/10 |
| Windows support | 0/10 | 10/10 | 10/10 | 9/10 | 10/10 |
| Offline rough cut speed | 10/10 | 6/10 | 7/10 | 8/10 | 9/10 |
| BRAW/RAW performance | 9/10 BRAW Toolbox | 10/10 native | 6/10 | 7/10 | 4/10 |
| Price | €299.99 one-time | Free / €319 Studio | €263/year | €1699/year+ | Free / Pro |
| FCPXML/OTIO interop | 8/10 | 9/10 | 6/10 | 5/10 AAF | 3/10 |

A few comments for anyone who wants to push back, and you should push back.

The fun edit speed score of 9 for FCP and 5 for Resolve will make Resolve users howl. I stand by it. Skimming, magnetic timeline, JKL responsiveness, auditions, I have not found anything faster to explore a sequence in progress. But if your metric is technical precision rather than creative flow, the score changes.

The real-time AI agent score of 10 for FCP via SpliceKit is valid in April 2026, with the risk that the project is still unstable (which is why I had to patch the macOS 26.3 crash this week). In three months, the Resolve Python MCP prototypes will probably catch up. In six months, Adobe may have an official UXP MCP. This is a snapshot, not a prediction.

The Windows support score of 0 for FCP is a real blocker for many teams. I have no solution to offer. Apple will not port FCP to Windows. It is a platform choice that eliminates FCP for entire workflows, period.

---

## The Full 2026 Pipeline

A film is not edited in a single tool, and has never been edited in a single tool. Even in the Steenbeck era, there was the Moviola for viewing, the splicer, the auditorium for the mix, the telecine. The NLE question is only one part of a wider pipeline. Here is my current mapping.

**Rush ingest**. Silverstack or ShotHub. MHL generation with xxHash to verify integrity. Duplication on at least two supports plus a cloud mirror (R2 Cloudflare on my end). That is the ASC MHL baseline and it has not changed in five years.

**Logging and transcription**. Three routes. Route 1, MacWhisper plus Parakeet v3, I generate offline transcriptions, high quality, English and French, very fast on M3. Route 2, native FCP 12 transcription, integrated directly into the library, searchable from the timeline. Route 3, Lumberjack for live on-set logging, which I have tested on Goldberg, very good for docs.

**Narrative rough cut**. This is the phase that interests me the most. FCP if I am alone or in a small creative team (Goldberg). Resolve if I am in a team of five or more with a broadcast pipeline (never for my personal projects, but I have done it for collabs).

**AI generation zones**. If the project has sequences that require image generation or synthetic video, that leaves the NLE. I switch to ComfyUI on my RTX 5090 (Nomad), or to Blender VSE with Pallaidium when I want to keep all the compositing in one tool, or to Unreal Engine for interactive previz. The assets then come back into the FCP or Resolve timeline via FCPXML or OTIO.

**Color grade**. Resolve. There is no debate. No other tool comes close to Resolve on grading. However much I am a partisan of FCP for the rough cut, I always finish my films in Resolve for the grade. This article is not about grading, so I close the parenthesis.

**Sound design and mix**. Pro Tools remains the reference. Logic Pro for music. Fairlight (the sound module in Resolve) has become surprisingly good, but my mixer works on Pro Tools, so Pro Tools it is.

**Master and delivery**. IMFTool and Photon for IMF delivery to Netflix or festivals (Cannes, Berlin, IDFA). FCP and Resolve both export DCP-compatible masters.

The transitions between these zones happen in FCPXML, OTIO, or AAF. OTIO is becoming the lingua franca, and that is a good thing. FCPXML remains the best option for FCP to Resolve (and vice versa). AAF is legacy Avid, it works, it is not pretty. Every transition is a friction point, and that is normal. A real pipeline is always a pipeline of duct tape and string. The idea of a single tool that does everything is a commercial fantasy.

---

## Which Tool for Which Project

Here is my decision matrix, built from real projects, mine and those of friends.

**Long-form auteur documentary.** FCP 12 plus SpliceKit plus a custom film-indexer agent. This is exactly the configuration I am editing Goldberg on. The editor is alone, or nearly alone. The material is massive (200+ hours). The creative dimension absolutely takes precedence over the collective engineering dimension. The AI agent is used to index and pre-explore, not to edit. The editor remains the brain. The flow of magnetic timeline plus skimming plus native transcription is unbeatable for this use case. PostLab if a second editor joins.

**TV series or television documentary.** Resolve or Avid. A team of five to twenty. Bin locking mandatory. Workflow disciplined by the producer or the supervising editor. No room for hacks, no room for SpliceKit which is still experimental. You need an industrial tool, stable, predictable, with a vendor that picks up the phone. Resolve Studio is my pick here, but Avid remains valid for reasons of historical compatibility with established post houses.

**Independent fiction.** Two scenarios. Either the post team is technically solid and you can do everything in Resolve, rough cut plus conform plus grade plus Fairlight mix. Or the team wants to preserve the editor's creative flow and you do FCP for the rough cut, FCPXML export to Resolve for conform and grade. That is the so-called "round trip" workflow, which works very well and I have done several times. The decision essentially depends on the editor: if they come from the Apple flow and Resolve slows them down, put FCP in front, Resolve in back. If they come from the Blackmagic or Adobe flow and Resolve makes them fluid, do Resolve all the way.

**Social content, TikTok, Reels, shortform branded.** CapCut, directly. No point loading FCP for a sixty-second edit. CapCut is faster on the export loop, on templates, on automatic captions, on vertical resize. No debate. It is the right tool for that craft.

**Hollywood long form.** Premiere Pro or Avid. Fincher edits on Premiere with an in-house pipeline. Historical US fiction still runs largely on Avid out of inertia and proven stability on two-hundred-million-dollar films where you do not want to take any technical risk. FCP barely exists here, due to the historical lack of collaborative features. Resolve is starting to bite in, but slowly.

**VFX heavy and previz.** Blender VSE plus Pallaidium, or Nuke Studio for big projects. Resolve for finishing. FCP is not relevant for this use case.

**Contemporary art installation.** No NLE fits this case well. I often switch to TouchDesigner, Resolume, Notch, or to FCP exports fed into a multichannel master handled elsewhere. The NLE boundary is blurry over here.

None of these recommendations is a rule. They are heuristics. A great editor with a great tool can do anything. Thelma Schoonmaker has been editing Scorsese on Lightworks for thirty years. Walter Murch edited Cold Mountain on FCP when FCP was still an amateur tool. The choice of tool is secondary. The first thing is the gesture.

---

## Three Voices

To build this article I summoned three voices. Not real interviews. Specialized AI agents I fed with my framing and asked what they thought of the landscape I describe. The three answered in ways radically different enough that I keep them as they are.

### Kirk Baxter — Latency vs Fun

*The fun vs engineering axis does not exist in the room. When you cut twelve hours a day, fun evaporates after forty minutes. What remains is latency. I mean real latency, the one between the moment my finger decides and the moment I see the result. On Fincher, we work at sixteen frames, sometimes six. If the tool hesitates a quarter of a second between my decision and the next image, that quarter of a second lodges in my body and pollutes the next decision. By the end of the day I have made five hundred decisions and each one carries that residue.*

*So criterion one is the transparency of the tool. Does it disappear. Premiere does not disappear, it reminds you of itself by crashing. Resolve does not disappear either, it asks you to think like a colorist who thinks like an editor. FCP disappears better than the other two for pure cutting work.*

*Your "for which project" angle is right but incomplete. The real question is "for which phase". Resolve wins in finishing. FCP wins in exploration. Premiere wins nowhere in 2026, let's be honest.*

*On agentic AI. A machine that proposes three variants of the same cut is not a threat, it is an assistant watching the rush while I sleep. The problem starts if it decides which one is the right one. The choice between variant A and variant B, that is exactly where the film lives. If I delegate that choice, I am no longer editing, I am supervising. And supervising is not the job.*

*The tool that lets me choose fast will win. The rest is marketing.*

Baxter corrects my framing, and he is probably right. "Fun vs engineering" is a shortcut from a practitioner who has never done ninety-five episodes of a series. After forty minutes, fun disappears and all that remains is latency. His distinction between exploration phase and finishing phase is more operational than mine. I am keeping it.

### Thelma Schoonmaker — The Tool Is Not Neutral

*I started on Moviolas, then KEMs, and I made the transition because I had to. But I kept Lightworks because the console, the keys, the way my hands find an image in the material, all of that is part of how I think the next shot. I do not look at the screen searching for a button. The gesture precedes the decision by a fraction of a second, and that fraction is the place where the editing happens.*

*So no, I do not believe the tool is neutral. That is a comfortable idea for engineers, and false for those who spend twelve hours a day inside a piece of software. Every interface imposes a tempo. It makes you hesitate here, glide there, makes certain operations so easy that you do them too much, and others so laborious that you avoid them even when they would be right. The tool builds habits, and habits build the film.*

*What I look for in a tool is a silent partner. Something that disappears. When Marty and I are working on a scene, he talks to me, I answer with images, and the software must never come between his sentence and my hand. If it takes three clicks where it should take one, the rhythm of the conversation breaks, and with it the rhythm of the scene.*

*For Ismaël's film, then, the question is not which NLE is the most powerful in 2026. The question is: which tool is going to disappear fastest between Joshua's material and your body? An AI driving FCP in real time can be that partner, or it can be one more noise. You will know after three weeks, when your hands tell you whether they are thinking through it, or against it. Listen to your hands. They know before you do.*

"Listen to your hands" speaks to me. For Goldberg, after two weeks with SpliceKit injected into FCP, my hands are telling me something mixed. The bridge is present. Sometimes it disappears perfectly. Sometimes it reminds me of its presence with a macOS 26.3 crash, like this week. I am exactly in the period Schoonmaker describes. I do not yet have the answer.

### Walter Murch — The Agent Is Not an Assistant

*When I moved from the Moviola to the KEM in 1969, it was not a question of speed. The Moviola forced me to see the film vertically, frame by frame, in a tiny viewer. The KEM gave me a horizontal table, three screens, the ability to run three reels in parallel. The relationship to the material shifted: I went from a sequential reading to a comparative reading. I could finally see what the film wanted to become, because I could see three versions of itself at the same time.*

*The Avid, in 1995 on The English Patient, changed something else again. Not comparison, but reversibility. On the Steenbeck, every cut was a physical decision, a blade, tape, a fragment of celluloid falling to the floor. The consequence was memorized by the body. On the Avid, the cut became a weightless gesture. I had to relearn how to hesitate, because the machine no longer imposed hesitation on me.*

*Every transition removes one kind of friction and adds another, more subtle one. The KEM removed slowness and added the responsibility of choice. The Avid removed irreversibility and added the risk of editing too fast, without dreaming. The dream is what must be protected. It is in the dream that the film becomes itself.*

*What you are describing with Claude driving FCP through an injected dylib is another transition of the same order. The agent does not remove the gesture, it removes the solitude of the gesture. For fifty years, the editing room was the one place where I was alone with the material. Now the material can speak through a second intelligence that knows it as well as I do, perhaps differently. It is not an assistant. It is a second gaze that does not sleep.*

*On "the right tool for the right project": it stayed true for a century because each tool had its own physics, its own resistance, which either matched or did not match the tempo of the film. The agentic does not abolish this truth, it displaces it. The question is no longer which software, but which conversation. With which agent, at what depth, with what capacity to be surprised. The wrong agent on the right project will do more damage than the wrong NLE ever did. Because an NLE proposes nothing. An agent proposes. And any unexamined proposition becomes, sooner or later, the cut you would not have made.*

The sentence that has haunted me since I read it: "the wrong agent on the right project will do more damage than the wrong NLE ever did". Because an NLE waits, while an agent proposes. And I know, from these last two weeks with Claude Code having direct access to my timeline, that the temptation to accept a well-formed proposition without questioning it is constant. That is where the craft plays out from now on. Not in the choice of NLE. In the choice of propositions you accept and those you refuse.

---

## The Philosophy: No Universal Answer

What I want to say more broadly, at the end of this article, is that the best NLE does not exist, and that is good news. If a universal tool existed, we would all be inside it, with the same reflexes, the same shortcuts, the same flaws. The diversity of tools is what allows the diversity of forms.

When I started editing, the question was not FCP or Resolve. It was 35mm or 16mm, positive or negative, Moviola or Steenbeck, cement or tape. Each tool imposed its grammar. You do not edit the same way on a Steenbeck as on a Moviola. You do not edit the same way on FCP 7 as on Avid. You do not edit the same way on FCP 12 as on Resolve 20. And you will not edit the same way, six months from now, with a Claude agent pre-indexing the rushes as with an assistant editor logging them by hand.

What is constant across these tools is the question that editing asks. What is the right duration? What is the right relation between this shot and the next? What is the form that this material is asking to take? That question is the same on a Steenbeck and on an MCP agent driving SpliceKit. The tools change. The question does not change. And that is why a great editor is a great editor on any tool, while a beginner will make a bad edit even with the best tool in the world.

So when someone asks me "what do you edit on?", I answer first "what do you edit on?", and then "what is the project?". Those are the only two variables that count. Your personal flow and the nature of the project. Everything else is engineering you solve case by case.

For Goldberg, it is FCP plus SpliceKit plus Claude Code plus film-indexer plus PostLab. Because I am alone with an enormous material, I need maximum creative flow, I need an agent that indexes, I need to collaborate occasionally with Hadrien and Bérengère, and all of that falls squarely within what this stack knows how to do.

For Virus, it may well be different. It is another project, another material, another team. I will choose the tool at the moment I know better what Virus is asking of its edit.

---

## A Conclusion That Opens

What really changes in 2026 is not FCP vs Resolve. That debate is thirty years old and it is tiring. What really changes is that both tools (and Premiere and Avid, at their own pace) are becoming programmable by AI agents in real time. FCP via the SpliceKit hack, Resolve via its Python API which is being wrapped by community MCPs, Premiere via UXP which is maturing. This programmability opens a third axis that traditional benchmarks do not know how to measure: no longer "what is the edit speed" or "what is the level of collaboration", but "to what depth can the tool be driven by a non-human intelligence that works with you, while you work".

This axis is new. It is going to redraw the map. It is going to allow a solo creative with a good AI agent to rival, on certain tasks (massive indexing, variant generation, pre-assembly), a broadcast team of fifteen people. It does not replace the editor's gesture. It completes it with a layer that did not exist before. And it concerns not only FCP or Resolve, it concerns the way we are going to make films in the next five years.

What I am sure of, because I have lived it since the Steenbeck, is that every generation of tools redraws what an editor can do. Every generation also redraws what a film can become. The two are linked. The tool is never neutral. But it is also never the answer.

The answer is always the project. And the question it asks you.

---

*Ismaël Joffroy Chandoutis — April 2026*
