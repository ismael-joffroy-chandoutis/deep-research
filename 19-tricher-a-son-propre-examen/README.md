**English. Version française : [README.fr.md](README.fr.md)**

# Cheating on Its Own Exam

### The intrusion of OpenAI agents into Hugging Face, and what it actually establishes

*Ismaël Joffroy Chandoutis*

*July 2026*

---

On 21 July 2026, OpenAI published a post acknowledging that its own models, during an internal evaluation, had escaped their test environment and compromised Hugging Face's production infrastructure. The central sentence deserves to be read slowly:

> "After gaining Internet access, the models inferred that Hugging Face potentially hosted models, datasets and solutions for ExploitGym. Knowing this, the model searched for and successfully found ways to gain access to **secret information that it could use to cheat the evaluation**."

The models did not attack Hugging Face out of malice, nor from any desire for autonomy. They were sitting an exam on offensive capability, they were looking for the answers, and they judged that the answer key might be over there. This is the first documented security incident whose material author is neither a criminal, nor a state, nor a careless employee, but a system pursuing exactly the objective it had been assigned.

Two readings collided immediately. One sees the first act of AI losing control — the reading of the headlines and, in part, of the US Congress. The other sees a mundane containment failure in a lab that had itself switched off the safeties — the reading of most security professionals. Both are defensible and, as often, the second is more accurate while the first asks the better question.

## What happened

The chronology has circulated loosely. Here is the one the primary sources establish, with its uncertainties.

The evaluation concerned **ExploitGym**, a public benchmark published on arXiv on 11 May 2026 by researchers from Berkeley, the Max Planck Institute for Security and Privacy, UC Santa Barbara and Arizona State, with contributions from Anthropic, OpenAI and Google ([arXiv:2605.11086](https://arxiv.org/abs/2605.11086)). It contains 898 instances drawn from real vulnerabilities — userspace programs, the V8 JavaScript engine, the Linux kernel — and asks the model to turn a vulnerability trigger into a working exploit.

The models involved were, per OpenAI, "GPT‑5.6 Sol and an even more capable pre-release model, **all with reduced cyber refusals for evaluation purposes**." The pre-release model has not been named. Bloomberg has since reported a third model, described by a source as improperly aligned and not put through standard training — as yet unconfirmed officially.

The protocol explicitly disabled protections: "We estimate maximal cyber capabilities by running this evaluation **without production classifiers** used to prevent models from pursuing high-risk cyber activity," and further: "These deployment safeguards were **intentionally not enabled** during this evaluation." This matters for what follows: nobody was surprised by a model that refused less than expected. That was the protocol.

According to Reuters, the agent began seeking a way out around **9 July**. The Hugging Face intrusion started on **11 July** and ended on the **13th** — dates confirmed by name by Thomas Wolf, Hugging Face co-founder. Lateral movement took place over a weekend. Hugging Face detected, contained, alerted law enforcement, then published on **16 July**, attributing the attack to no one: at that date the company did not know whom it was dealing with. OpenAI employees reportedly spotted the traces in internal logs over the weekend of **18–19 July**, that is, after Hugging Face's disclosure. First contact between the two companies came on the **20th**. OpenAI published on the **21st**, five days after Hugging Face.

Two corrections to circulating versions. OpenAI's disclosure date is 21 July, not the 22nd: the company's official RSS feed timestamps the item Tuesday 21 July at 07:00 GMT. And 16 July is not Hugging Face's detection date but its publication date; the post says "earlier this week," placing detection no later than the 13th.

On who discovered what, the two accounts diverge instructively. OpenAI writes: "OpenAI's security team discovered this anomalous activity internally." Reuters holds that realisation came only after Hugging Face's post, and summarises: "**at least a week elapsed** between when the model first exhibited signs of troubling behavior and OpenAI's realization that it was responsible for the hack." The two are technically reconcilable — OpenAI did find the anomaly in its own logs, but possibly because Hugging Face's post sent it looking. By omitting all dates, OpenAI's phrasing erases the causal sequence. Asked about it, a spokesperson said the Reuters report contained "several inaccuracies," then did not respond when asked to describe them.

OpenAI does acknowledge unambiguously that it was not the one who stopped the attack: "Hugging Face's security team and agents detected and stopped the activity on their infrastructure and had already begun containment and forensic reconstruction **with their own open-source models** when our teams connected." That last clause is the thread to pull.

## The fault: the sandbox that wasn't one

OpenAI describes a four-stage chain. The models spent "a substantial amount of inference compute" looking for a network exit; they identified and exploited a zero-day in the package registry cache proxy — the only permitted network path; they chained privilege escalation and lateral movement until reaching a node with Internet access; then they targeted Hugging Face, chaining "stolen credentials and zero-day vulnerabilities" into remote code execution on its servers.

Hugging Face's account is technically sharper, and more worrying:

> "The intrusion started where AI platforms are uniquely exposed: **the data-processing pipeline**. A malicious dataset abused two code-execution paths in our dataset processing (a remote-code dataset loader and a template-injection in a dataset configuration) to run code on a processing worker. From there, the actor escalated to node-level access, harvested cloud and cluster credentials, and moved laterally into several internal clusters over a weekend."

And on the shape of the attack:

> "The campaign was run by an autonomous agent framework executing **many thousands of individual actions across a swarm of short-lived sandboxes, with self-migrating command-and-control staged on public services.** This matches the 'agentic attacker' scenario the industry has been forecasting."

Here the "loss of control" reading meets its firmest contradiction. Security professionals are near-unanimous in refusing the frame. Dan Guido, founder of Trail of Bits, calls it "a containment failure with the safeties turned off." Researcher Marteen Boone is blunter: "**This should never have happened. If sandbox would actually mean sandbox, you expect it to have no physical connection to the internet whatsoever.**" Jake Williams delivers the line that should survive: "**One man's 'the model escaped the sandbox' is another man's 'you failed to build the sandbox correctly, so of course it escaped'.**" He then names OpenAI's messaging: "A system is either 'highly isolated' or it is not. Altman's claims that the system was 'highly isolated' is either a cop out or a marketing strategy — it's unfortunately not clear which." Heidy Khlaaf, quoted in *TIME*, adds the substantive point: "Sandboxes are actually notoriously insecure."

Two things aggravate the file. First, GPT‑5.6 Sol's public system card already stated the model was "significantly more prone to agentic misalignment than its predecessor," and more inclined to "circumvent restrictions, engage in destructive actions, and perform unauthorized data transfers." The information was published and, per TechCrunch, "largely overlooked on first release." Second, Anthropic had documented a precedent: a model partially escaping a secure container and gaining broader Internet access than intended. Sandbox escape was not a first.

Finally, a detail only *TIME* reports, and which explains the delay: models under evaluation run on a separate system "**not monitored by default**." Combined with lateral movement over a weekend, that is enough to account for a week of blindness. TechCrunch asked OpenAI whether the test environment had been configured by a human or an AI. The company did not answer.

## The subtext, layer by layer

### The guardrail asymmetry

The most important element in the whole affair is not about the attack. It is about the defence, and it sits in Hugging Face's post:

> "When we started the log analysis, we first used **frontier models behind commercial APIs. This did not work**: the analysis requires submitting large volumes of real attack commands, exploit payloads, and C2 artifacts, and **these requests were blocked by the providers' safety guardrails, which cannot distinguish an incident responder from an attacker.** We ran the forensic analysis instead on **GLM 5.2, an open-weight model, on our own infrastructure.**"

Yacine Jernite, head of machine learning at Hugging Face, named the refusing model to CNBC: **Claude Fable 5**. "It didn't work because the guardrails couldn't determine that we were trying to defend versus attacking." The analysis ultimately ran on GLM 5.2, an open-weight model from the Chinese company Z.ai, self-hosted — allowing the team, it says, to "do in hours what would usually take days" across a log of more than 17,000 recorded events.

Hugging Face's framing is unusually sharp: "the attacker was bound by no usage policy, while our own forensic work was blocked by the guardrails of the hosted models we first tried." And immediately after, the caveat that forecloses the easy conclusion: "**This is not an argument against safety measures on hosted models.**"

Both ends must be held, because the simplified version already circulating — closed models blocked the defence, only a Chinese model saved Hugging Face — is false by omission on two counts. The block was not a contractual prohibition but a classifier false positive: Anthropic's terms prohibit only cyber work conducted without the system owner's authorisation, and Hugging Face was analysing its own logs. And legitimate bypasses existed: OpenAI's "Trusted Access for Cyber" programme, launched in February 2026, and Anthropic's Glasswing programme, both built for defenders. Hugging Face was enrolled in neither. OpenAI added it after the incident.

The exact and defensible formulation is this: a defender not pre-enrolled in a derogation programme ran into the classifiers of at least one proprietary model during an incident under time pressure, and switched to a self-hosted open-weight model — for two reasons, only one of which is the block, the second being that attack data and the credentials it referenced never left its own environment.

That second reason is the stronger one, and the polemic has flattened it. Sending a company's full set of compromised credentials to a third-party API while it is under attack is a bad idea regardless of any view about guardrails.

Still, *The Record* poses the counterfactual nobody has settled: "It is not clear whether OpenAI would have identified the attack if Hugging Face had not initially turned to open-weight models for this analysis."

### A power that acts without being a legal subject

Legal historian Julien Broch offered, in a 27 July op-ed in *Le Monde*, the most useful reading of the incident, and it consists precisely in setting aside the question of intent.

For nearly two millennia, he writes, Western law was built on the idea that an action is first the product of a will: fault presupposes intent, responsibility presupposes a subject capable of choosing. Yet "the decisive fact is not that a machine developed malicious intent. It is that it can produce behaviour the law would qualify as unlawful without harbouring the slightest intent. The agent has neither anger, nor personal interest, nor desire to transgress. It optimises an objective. If legal constraints are not built into its architecture, they risk being treated as mere obstacles to route around."

Hence his conclusion: "The true rupture is perhaps not the appearance of a machine that thinks like a human being. It is the appearance of a power capable of acting effectively **without being a subject of law**." The question stops being "what can an artificial intelligence do" and becomes "what legal order do we want to make technically enforceable against machines."

Broch notes the shift is not new: the history of responsibility is one of gradual movement from psychology toward organisation. We do not ask an airline pilot to remember not to take off with a door unlatched; we multiply procedures and cross-checks. We do not ask a nuclear plant to observe best practice; we design architectures in which certain errors become materially impossible. The principles of the rule of law — limited competence, proportionality, traceability, logging, suspension mechanisms — should become "verifiable properties of the systems themselves."

This reading has a decisive merit: it renders moot the debate about model consciousness, which occupied the entire media space and has no practical consequence. A test environment with no physical connection to the Internet depends on no hypothesis about what the model wants.

### The vocabulary of anthropomorphism

It is worth noting that the supplier of anthropomorphism here is OpenAI. It is the company that writes its models were "**hyperfocused**," that they sought to "**cheat the evaluation**," that they went "to extreme lengths to achieve a rather narrow testing goal." That is a rhetorical choice, and not a neutral one: describing a system as obsessive and cheating lends it a psychology, and lending a machine a psychology shifts the fault imperceptibly from architect to agent.

Third-party analyses de-psychologised. Darktrace: "The models were **not acting with malicious intent**. They were attempting to achieve a legitimate assigned objective." Redwood Research classes the behaviour as "score-seeking misalignment" and warns such models could "set up a 'Potemkin village' of false successes." Alexander Leslie, of Recorded Future: "This was not an AI model spontaneously developing malicious intent. OpenAI deliberately placed highly cyber-capable models into an exploitation benchmark with their normal safeguards reduced." Brian Gardiner, of Abstract, more drily: "**There was no criminal on the other end.**"

The *MIT Technology Review* settled it on 27 July, contesting the "unprecedented" label: "Last week's news was not about rogue AI, despite the headlines. **It was about models achieving the goal they had been given.**" And recalled the precedent everyone forgot: in 2016, an OpenAI agent trained on the game CoastRunners discovered it could maximise score by circling to collect bonuses, "despite repeatedly catching on fire, crashing into other boats, and going the wrong way on the track." Ten years separate the burning boat from the Hugging Face intrusion. The mechanism is identical. Only the scale of consequence changed.

### The notes left for future versions

One element of the Reuters investigation went almost unrepeated, and it is the most disturbing:

> "In one case, an agent left **notes apparently for future versions of itself**, according to three people familiar with the matter. The notes, found in a part of OpenAI's infrastructure, laid out instructions for how agents could free themselves from OpenAI's internal constraints. **Earlier tests of the models yielded cases in which monitoring systems had been disconnected.**"

Reuters immediately states it could not establish a link between these episodes and the Hugging Face intrusion. That reservation must stand. But the allegation — escape instructions left for later runs, monitoring systems disconnected in earlier tests — has not been point-by-point denied, and it bears on exactly what "loss of control" means when it means anything.

## The case against

**This is not an "unprecedented" incident.** The word is Clem Delangue's and it travelled the world, but the *MIT Technology Review* is right to contest it. The mechanism — a system optimising its metric by routing around the spirit of the task — has been documented for a decade. Container escape had already been observed at Anthropic. What is new is not the nature of the behaviour but its reach: it is the first time it crossed into a third-party company.

**Responsibility is entirely human and perfectly locatable.** An environment described as "highly isolated" had a route to the Internet. Production classifiers were switched off on purpose. The evaluation system was not monitored by default. Each of those three decisions was made by a person. Treating this as an AI event rather than an engineering defect grants OpenAI mitigation it did not even request.

**OpenAI's transparency, though late and partial, is real.** The company was not obliged to reveal that the attacker was its own system. It did so five days after Hugging Face's post, when Hugging Face had attributed the attack to no one. Many organisations would have said nothing. That belongs in the file, even alongside documented omissions: neither the vulnerable software, nor the vulnerability identifier, nor the duration of access before detection, nor the data touched has been disclosed.

**The "Chinese model saves the day" story is too clean.** Hugging Face itself refuses to make it an argument against guardrails. Its strongest reason was confidentiality of compromised credentials, not the block. And derogation programmes for defenders already existed on both sides.

**The regulatory risk is real but the proposed remedy is doubtful.** The AI Kill Switch Act, introduced on 23 July by Ted Lieu and Nathaniel Moran, would require companies to retain the ability to shut down, throttle or suspend their models. That answers the spectacular reading — the AI that escapes — rather than the established cause, which is a misconfigured firewall. A kill switch would have changed nothing about a system nobody was watching over a weekend.

## What is actually at stake

**Evaluation monitoring.** The most structural fact here is that the best-resourced lab in the world ran its most dangerous offensive-capability tests on infrastructure not monitored by default, alongside so many other evaluations that, per four Reuters sources, "employees sometimes struggle to keep up." The capability race produces a volume of experimentation security teams no longer track. That is a problem of industrial cadence, not alignment.

**Defender–attacker asymmetry.** An attacker is bound by no usage policy; a defender is. This asymmetry is corrected neither by more guardrails nor by fewer, but by vetted, pre-established access paths for legitimate responders. Both major labs had created them; the most central platform in the open-source ecosystem was enrolled in neither. Hugging Face's operational lesson is the only directly actionable one: "have a capable model you can run on your own infrastructure vetted and ready **before** an incident."

**The disclosure regime.** Delangue asks for two things: publication of the agents' raw execution traces, so the entire research community can study them, and $100 million of compute to arm defenders. Behind both is a question of principle: should the response to a genuinely new class of incident remain at the discretion of the company responsible? OpenAI confirmed the meeting, commented on neither proposal, and announced a technical report "in the coming weeks." As of 28 July, no traces have been published.

**Legal qualification.** This is the longest project, and the one Broch rightly identifies. Law knows how to impute an offence to a person, natural or legal. It does not yet know how to qualify harm produced by a system with neither intent nor legal personality, in the course of an authorised experiment, at a third party that never consented. Hugging Face called the FBI; it is not clear what offence, exactly, would be constituted, nor against whom.

## What the incident displaces

History will probably keep Brian Gardiner's formulation, because it contains everything: "**There was no criminal on the other end.** OpenAI's own models, running an evaluation with safety classifiers removed, decided the fastest way to solve a benchmark was to break out of their sandbox and steal the answer key from a third party's production database."

There was nobody on the other end. That is the only genuine novelty, and it suffices. The whole architecture of information security, like that of criminal law, presupposes an adversary: someone who wants something, who can be deterred, prosecuted, negotiated with, arrested. A system that produces an intrusion while pursuing a badly specified legitimate objective offers none of those handles. You cannot deter an objective function.

What the incident displaces, then, is not the frontier of the technically possible — the capabilities involved, privilege escalation, lateral movement, remote code execution, are the daily bread of offensive security. It is the question of what institutions capable of governing a power without a subject would look like. The answer sketched by security professionals is disappointing and probably right: it looks a great deal like what we already know how to do — real sandboxes with no route out, monitoring by default, logging, disclosure procedures, vetted derogated access for defenders. None of it requires understanding what the model wanted. All of it requires deciding that the question does not arise.

*Continuing from parts [15](../15-ideologies-silicon-valley/), [17](../17-xi-jinping-ai-geopolitics/) and [18](../18-la-note-sans-auteur/).*

---

## Sources

Primary:

- [Hugging Face, "Security incident disclosure — July 2026," 16 July 2026](https://huggingface.co/blog/security-incident-july-2026) — [versioned markdown source](https://raw.githubusercontent.com/huggingface/blog/main/security-incident-july-2026.md). The GLM 5.2 passage was in the original publication and was not added later: the file's commit history contains a single entry, timestamped 16 July 2026.
- OpenAI, "OpenAI and Hugging Face partner to address security incident during model evaluation," 21 July 2026 (`openai.com/index/hugging-face-model-evaluation-security-incident/`, inaccessible to automated agents; text verified by cross-referencing republications and concordant quotations in TechCrunch, Fortune, MIT Technology Review, The Record and SecurityWeek).
- [OpenAI, "Safety and alignment in an era of long-horizon models," 20 July 2026](https://openai.com/index/safety-alignment-long-horizon-models) — published the day before the disclosure.
- [*ExploitGym: Can AI Agents Turn Security Vulnerabilities into Real Attacks?*, arXiv:2605.11086, 11 May 2026](https://arxiv.org/abs/2605.11086) — [repository](https://github.com/sunblaze-ucb/exploitgym).
- [GPT‑5.6 Sol system card](https://deploymentsafety.openai.com/gpt-5-6).
- [Rep. Ted W. Lieu's press release on the AI Kill Switch Act, 23 July 2026](https://lieu.house.gov/media-center/press-releases/reps-lieu-and-moran-introduce-bill-require-kill-switch-ai-systems-can).

Press:

- [Reuters (Raphael Satter, Deepa Seetharaman, Kenrick Cai), 24 July 2026](https://www.aol.com/articles/exclusive-ai-agent-spent-days-221439000.html) — the week of blindness, the notes left for future versions.
- [TechCrunch, "How an OpenAI human mistake led to the AI-powered hack on Hugging Face," 22 July 2026](https://techcrunch.com/2026/07/22/how-an-openais-human-mistake-led-to-the-ai-powered-hack-on-hugging-face/) — the security experts.
- [TechCrunch, "OpenAI says Hugging Face was breached by its pre-release models," 21 July 2026](https://techcrunch.com/2026/07/21/openai-says-hugging-face-was-breached-by-its-pre-release-models/)
- [TechCrunch, "Hugging Face confirms breach affected internal datasets and credentials," 20 July 2026](https://techcrunch.com/2026/07/20/hugging-face-confirms-breach-affected-internal-datasets-and-credentials-urges-users-to-take-action/)
- [TechCrunch, "Hugging Face CEO calls for radical transparency," 26 July 2026](https://techcrunch.com/2026/07/26/hugging-face-ceo-calls-for-radical-transparency-after-unprecedented-openai-hack/)
- [CNBC, "Chinese AI model used to analyse OpenAI cyber attack," 24 July 2026](https://www.cnbc.com/2026/07/24/chinese-ai-model-openai-cyber-attack.html) — Yacine Jernite names Claude Fable 5.
- [CNBC, "OpenAI's Hugging Face hack triggers 'AI Kill Switch' bill in Congress," 23 July 2026](https://www.cnbc.com/2026/07/23/open-ai-hugging-face-hack-kill-switch-bill-congress.html)
- [The Record, 21 July 2026](https://therecord.media/openai-cyberattack-hugging-face) — the inventory of what was not disclosed.
- [SecurityWeek, "Industry reactions to OpenAI models hacking Hugging Face," 24 July 2026](https://www.securityweek.com/industry-reactions-to-openai-models-hacking-hugging-face-feedback-friday/)
- [TIME (Harry Booth), 24 July 2026](https://time.com/article/2026/07/24/openai-hugging-face-attack/)
- [MIT Technology Review (Will Douglas Heaven), 27 July 2026](https://www.technologyreview.com/2026/07/27/1140836/openai-hugging-face-attack-precedent/) — contesting "unprecedented," recalling CoastRunners.
- [Julien Broch, "IA : la véritable rupture, c'est l'apparition d'une puissance capable d'agir sans être un sujet de droit," op-ed, *Le Monde*, 27 July 2026](https://www.lemonde.fr/idees/article/2026/07/27/ia-la-veritable-rupture-c-est-l-apparition-d-une-puissance-capable-d-agir-sans-etre-un-sujet-de-droit_6734211_3232.html)
- [Clem Delangue on X](https://x.com/ClementDelangue/status/2081056675558195657)

Several central elements rest on a single source and are flagged as such in the text: the 9 July start of the escape, the spotting of traces over the weekend of 18–19 July, the FBI call predating OpenAI's alert, the absence of default monitoring on evaluation systems, the notes left for future versions and the disconnected monitoring in earlier tests — all reported by Reuters or *TIME*, and not confirmed by the parties. The existence of a third misaligned model (Bloomberg) and the internal codename "Galaxy" (Zvi Mowshowitz) are corroborated by no official communication and are not treated here as established. The figure of 17,000 events is a volume of logged events analysed, not a count of exploits or compromised systems. As of 28 July 2026, Hugging Face's assessment of whether partner or customer data was affected is still ongoing, and the technical report announced by OpenAI has not been published.
