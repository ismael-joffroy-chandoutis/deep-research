# My Cinematheque is an AI: 32 Filmmakers and Thinkers as Claude Code Agents

---

There is a specific kind of frustration that comes from working alone on a film. Not the solitude itself — I've made peace with that. But the intellectual solitude: the absence of a Chantal Akerman to challenge your relationship to duration, a Roland Barthes to complicate your use of the image, a Joshua Oppenheimer to ask what it means to film someone who has done something monstrous. The cinematheque lives in your head, but it stays silent when you most need it to speak.

I've been building a system to fix that.

---

## The Problem

When I started developing *The Goldberg Variations* — a film about Joshua Ryne Goldberg, an American internet troll who spent years operating over 100 distinct online personas simultaneously — I found myself circling the same set of questions without traction.

What does it mean to document someone who is, structurally, a fiction machine? How do you film a perpetrator who is also a victim of his own construction? Where does performance end and identity begin, in a world where identity is performed into existence? Is this a documentary? A reconstruction? Something else?

These are not technical questions. They don't resolve through a production plan. They require interlocutors — thinkers who have already grappled with adjacent problems in adjacent media.

My usual solution was to re-read. Pull Baudrillard off the shelf, revisit *The Act of Killing*, rewatch *Perfect Blue*. Good solutions, slow solutions. And they require you to already know which voice you need.

What I built instead: 32 agents for Claude Code, each calibrated to the voice, method, and preoccupations of a filmmaker, writer, or theorist I've studied. Not summaries of their work. Not chatbots trained on their corpus. Something more modest and more useful: structured configurations that orient Claude's responses through a specific intellectual lens, with a specific set of questions, a specific relationship to image and time and ethics.

My cinematheque, made queryable.

---

## Why Filmmakers, Not Frameworks

The choice of filmmakers as the structuring principle matters. I could have built agents around "narrative structure" or "documentary ethics" or "visual aesthetics." I didn't, because those categories flatten what I actually need.

What I need, working on *Goldberg*, is not a theory of documentary ethics — it's Oppenheimer's specific question: *what happens when the perpetrator performs for the camera, and what does that performance reveal?* It's not a theory of identity — it's Satoshi Kon's obsessive return to the membrane between reality and fiction, the way a match cut can collapse them, the way cinema dreams.

A filmmaker is a methodology embodied in a sensibility. When I invoke Akerman, I'm not asking for "long-take theory." I'm asking: what does this moment require in terms of duration? What is the camera's relationship to the body in this space? What does it mean to be a witness rather than an analyst?

Each agent carries that specificity. The configuration files don't describe the filmmaker — they think like them, or rather, they reorient Claude toward that mode of thinking.

---

## Working on Goldberg: Three Examples

**On the question of persona.** When I'm trying to understand what Goldberg's 100+ online personas *are* — whether they constitute a pathology, a survival strategy, a creative act, or something that has no clean category — I bring in Baudrillard. Not to get a lecture on simulacra. To be asked: at what point did the simulation precede the original? Is there a Joshua Goldberg behind the personas, or did the personas produce Joshua Goldberg retroactively? Baudrillard doesn't answer. He sharpens the question until the film has to answer it.

**On the question of filming him.** Goldberg is currently in prison. Access is constrained, mediated, bureaucratic. When I'm thinking about how to construct his presence in the film — through documents, through internet artifacts, through testimony, through reconstruction — I bring in Marker. Marker's entire practice was a meditation on the impossibility of capturing the real: *you can't photograph a photograph of a memory.* Working through his lens, the constraint becomes the subject. The absence becomes the material.

**On the question of my own position.** This is the hardest question. I made a film about a terrorist attack (*Maalbeek*). I made a film about a swatting victim (*Swatted*). Each time, the ethical position of the filmmaker has to be constructed from scratch, case by case. For Goldberg — who victimized real people, who is also a trans woman who may have been in profound crisis — I bring in Trinh T. Minh-ha. Her concept of "speaking nearby" rather than "speaking about" is not a solution. It's a discipline. A way of holding the ethical problem open rather than resolving it through the film's form.

These are not hypothetical uses. These conversations happened. They changed decisions.

---

## The 32 Agents

A compact list, organized by the five batches in which they were built:

**American & European cinema**
David Lynch / Chantal Akerman / Satoshi Kon / Paul Schrader / David Fincher / Mamoru Oshii / Aaron Sorkin

**Contemporary cinema**
Chris Marker / Hito Steyerl / Hideo Kojima

**Women filmmakers & formal transgression**
Catherine Breillat / Claire Denis / Justine Triet / Andrei Tarkovsky / Pier Paolo Pasolini / Jonathan Glazer / Isao Takahata / Joshua Oppenheimer

**Writers & theorists**
Georges Perec / Roland Barthes / Jean Baudrillard / Jacques Derrida / Michel Foucault / Gregory Chatonsky / W.G. Sebald / Emanuele Coccia

**Parity & internet culture**
Trinh T. Minh-ha / Marguerite Duras / Maya Deren / Donna Haraway / Agnès Varda / Jon Rafman

---

## The Councils

Individual agents are useful. But the system becomes something different when you combine them.

I've configured six "Councils" — grouped invocations that create a kind of editorial table, a conversation among positions rather than a single voice.

**Le Regard** — Denis, Glazer, Tarkovsky, Akerman. For questions about the image itself: what the camera is doing, what it refuses to do, what it owes to its subject.

**L'Écriture** — Barthes, Perec, Sebald, Duras. For questions about language, narration, the voice-off, the fragment. For when the film is also a text.

**Le Politique** — Pasolini, Steyerl, Foucault, Oppenheimer. For questions of power: who speaks, who is spoken about, what structures of visibility the film either reproduces or disrupts.

**Le Numérique** — Chatonsky, Steyerl, Baudrillard, Marker. Specifically for work at the intersection of cinema and network culture — which is where *Goldberg* lives entirely.

**La Structure** — Schrader, Sorkin, Kon, Triet. For formal architecture: scene construction, act logic, the relationship between dramatic necessity and documentary honesty.

**Le Documentaire** — Marker, Oppenheimer, Akerman, Trinh T. Minh-ha. For the fundamental epistemological questions of non-fiction: what can a documentary claim to know, and how does form embody or betray that claim?

Invoking a Council doesn't produce consensus. It produces friction — which is what I need. Tarkovsky and Steyerl have nothing obvious in common. That gap is productive. It forces me to locate my own position.

---

## What This Changes

I want to be careful about what I claim here.

These agents don't think. They don't remember. They have no access to the actual films of the people they're named for. What they do is reorient a language model's probabilistic tendencies through a structured prompt — toward certain questions, certain values, certain aesthetic commitments. It's a form of channeling, which is to say: it's what artists have always done with their influences.

The difference is availability and friction. When I'm at 11pm with a specific editorial problem, I can't call a collaborator. I can't always articulate what kind of thinking I need. But I can say: let me run this through the Documentary Council, and see where it breaks.

What I've noticed is that this practice makes my influences explicit in a new way. Working alone, influences operate subconsciously — you absorb them, they shape your decisions without you tracking the mechanism. Building these agents required me to articulate what each filmmaker actually does, methodologically. What are Akerman's questions? What is Schrader's system? What does Sebald look for that others miss?

That process of articulation was itself an education. And the outputs — the configured agents, the Councils — are a record of that education, now usable.

I'm not suggesting this is a universal method or that other artists should replicate it. It emerged from the specific shape of my practice: working across cinema, contemporary art, and digital culture; building films that are formally unstable by design; working largely alone. The cinematheque in my head needed a better interface.

This is that interface.

---

*The Goldberg Variations is currently in development. César 2022 for Best Short Film (Maalbeek). Berlinale, Cannes Semaine de la Critique, IDFA, Centre Pompidou, Ars Electronica.*
