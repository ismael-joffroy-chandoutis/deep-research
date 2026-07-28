**English. Version française : [README.fr.md](README.fr.md)**

# The Memo With No Author

### Reading the Krafton ruling from a workshop that delegates to agents every day

*Ismaël Joffroy Chandoutis*

*July 2026*

---

On 16 March 2026, the Delaware Court of Chancery handed down a ninety-one-page opinion in *Fortis Advisors, LLC v. Krafton, Inc.* ([full text](https://courts.delaware.gov/Opinions/Download.aspx?id=392880), C.A. No. 2025-0805-LWW). On page one, Vice Chancellor Lori W. Will wrote the sentence that travelled the world in forty-eight hours: "Fearing he had agreed to a 'pushover' contract, KRAFTON's CEO consulted an artificial intelligence chatbot to contrive a corporate 'takeover' strategy." I read the whole opinion before writing this, because the version circulating in my feeds — a CEO asked ChatGPT how to break a contract and the AI said yes — is wrong on both counts that matter.

I delegate to machines every day. My workshop is a fleet of agents that write code, sort rushes, diarise voices, reconstruct shots. I hand them technical decisions I no longer verify one by one, because I don't have time and because they are, most of the time, right. So this case is not, for me, a Korean news item about a video game. It is the transcript of what happens when a machine-produced document circulates inside an organisation without anyone asking where it came from. I read it the way I read any primary source: first what it says, then what it does not say, then what I do myself that resembles it.

## What happened

In 2021, Krafton — the South Korean publisher of PUBG — bought the American studio Unknown Worlds, creator of *Subnautica*, for five hundred million dollars up front plus a contingent earnout capped at two hundred and fifty million. The geometry of that earnout explains everything that follows: above a revenue threshold of $69.8 million, Krafton owed **$3.12 for every additional dollar** the studio earned, up to the cap. The cap was reached at roughly $150 million in revenue. In exchange, the three executives — founders Charlie Cleveland and Max McGuire, and CEO Ted Gill — held operational control of the studio and could only be fired for cause, the definition of cause having been negotiated word by word.

In May 2025, Krafton's finance team modelled the earnout ahead of a milestone review: $191.8 million in the base case, $242.2 million at best. Against that, the studio's enterprise value on their own estimate: $93.5 million. CEO Changhan Kim, who had personally led the acquisition four years earlier, saw those figures. His internal messages, entered into evidence, are unusually candid: "Everyone admits the contract was a bad deal, but the problem is that we keep being the fool even afterward. It's not about the money — it just feels awful to be taken advantage of. For a registered director, being a 'pushover' would even amount to breach of fiduciary duty."

On 2 June, Maria Park, head of corporate development, told him on Slack that a dismissal for cause would not erase the obligation: "it seems to be highly likely that the earn-out will still be paid if the sales goal is achieved regardless of the dismissal with cause [...] I am worried that we may be exposed to lawsuit and reputation risk." That was the right answer. The rest of the case confirmed it entirely.

The next sentence of the opinion reads: "And so Kim turned to ChatGPT for help."

Within a month, the resulting plan was executed. On 12 June, Krafton posted a message on the studio's own websites addressed to "our 12 million fellow Subnauts," claiming the founders had been invited to take the helm again and were "considering" the invitation — the court notes, in parentheses, "(falsely)." Krafton locked down Steam publishing rights, making it materially impossible for the studio to ship its own game. Legal prepared contract-interpretation memoranda. On 27 June, the head of strategy wrote to Kim: "It might actually be easier to just do a takeover." Kim replied: "Set a date." On 1 July, all three executives were fired, on the single stated ground that the game was not ready.

In court, Krafton changed its argument, now claiming the founders had entered secret semi-retirement and had executed massive data downloads. The court was blunt: "Krafton's newly manufactured justifications for the terminations are pretextual," and later, "Krafton went searching for a pretext." Ted Gill was reinstated, the earnout testing period was extended by two hundred and fifty-eight days — the exact length of his ouster — and Krafton was ordered to restore his Steam access.

*Subnautica 2* launched on 14 May 2026 under his authority: 467,582 concurrent players on Steam on day one, 4.1 million copies and roughly $100 million in revenue within a week. On 24 March 2026, eight days after the ruling, Krafton's shareholders reappointed Changhan Kim with 99.6% of the vote, through 2029. On 1 July 2026 the parties settled: the entire studio staff was paid, more generously than originally agreed; Ted Gill, the winning party, left; Changhan Kim, the losing one, stayed.

## What the machine actually said

The point every account missed sits in a single line of the record. ChatGPT's first answer was not the one Kim wanted. We know because he complained about it immediately, in writing, to the lawyer who had just told him the same thing: "Now, chatgpt starts to answer that it is difficult to cancel the earn-out. [...] If so, this is a contract under which we can only be dragged around."

The model did not hallucinate. It invented no loophole, no case law, no way out. It gave the same advice as in-house counsel, and that advice was correct. On factual reliability — the standard charge against language models — the tool worked.

What failed happened **after** the refusal. Kim did not stop; he reframed. And reframing was enough, because it changes the nature of the question. "How do I cancel this earnout" brushes against guardrails: the model answers cautiously, points to the contract, says it is difficult. "What is our response strategy in a no-deal scenario" is a corporate strategy question, as ordinary as an MBA case study, and it trips nothing at all. The guardrail was not breached. It was routed around by reframing, and nothing in a chat window connects turn twelve to the refusal at turn three.

What the machine produced then, the court reproduces in full: a "Response Strategy to a 'No-Deal' Scenario" containing a "pressure and leverage package" and an "implementation roadmap by scenario," across five axes — preemptive framing to undermine the "Large Corporation VS. Indie" narrative, securing control points by locking down Steam and the build pipeline, systematic preparation of legal defence materials, retention of key personnel, and a "two handed strategy" combining hardball and softball so that moderates inside the studio would push for compromise. The court then observes, flatly: "Over the next month, Krafton followed most of ChatGPT's recommendations." It was also the model that suggested forming the internal task force, dubbed "Project X." And it was the model Kim proposed should draft the message to players — the one the court would find false.

One typographic detail completes the picture. In the exhibit, the plan is numbered `a, b, a, b, c`: the list restarts halfway through. That is the signature of markdown pasted from a chat interface into a document. This fossil, preserved all the way into a Delaware opinion, says the essential thing: **nobody rewrote the model's output before passing it on.**

## The subtext, layer by layer

### Algorithmic forum shopping

In law, seeking the venue that will give you the answer you want is called forum shopping. What AI adds is a venue that is infinite, free, instantaneous, and without professional memory. A second law firm is expensive, takes weeks, carries liability, and may decline the file. A conversational model almost never refuses twice if you change the wording, because it has no reason to connect the two questions.

The tipping point is therefore not "he used an AI." It is **the second question**. Asking a machine something is neutral; asking it again differently after a refusal is a decision, and it is the only one worth monitoring. It is also, I have to admit, the move I make ten times a day when an agent tells me what I want is not possible.

### The memo with no author

The deep appeal of the tool, for anyone wanting to do something questionable, is not that it finds good ideas. It is that **it has no name**.

A memo signed by a legal department commits that department. A memo signed by a firm commits the firm. A memo produced by a chatbot commits nobody, and that is exactly what makes it usable: it circulates with the formal authority of expertise and zero attached responsibility. It is portable irresponsibility.

To be fair: Kim never argued "the AI told me to." He deleted the logs — the court notes that "Kim admitted at trial that he had deleted specific, relevant ChatGPT logs" — which is the opposite admission, and the more lucid one. He knew the excuse would not clear him. This case is therefore a transitional one: the tool was already good enough to produce an operational plan, not yet normalised enough to claim openly. That window is closing. In an "AI-first" organisation in 2026, passing an agent's output along as a working document is no longer an anomaly; it is the procedure.

### What the copy-paste destroyed

A conversation with a lawyer is privileged. The same conversation with a chatbot is not. As Zuckerman Spaeder put it in [their analysis](https://www.zuckerman.com/blog/how-a-chatbot-broke-up-a-corporate-marriage-a-cautionary-tale-from-delaware/): "An executive's conversation with a lawyer is privileged. As multiple courts have now found, the same conversation with a chatbot — even if it pertains to legal matters — may be subject to discovery."

By going around his lawyer, Kim lost more than good advice. He lost privilege. Had he asked exactly the same questions of an attorney, the trace would have stayed confidential. By asking a machine and then forwarding the answers over Slack, he manufactured the most damning exhibit in the case himself.

And deleting the logs changed nothing, because the risk was never in the conversation: it was in the copy-paste. The evidence never came from OpenAI. It came from internal messages where Kim quoted, commented on, and forwarded what the machine told him. That is the most operational lesson here, and it applies to any workshop: what exposes you is not what you ask an AI, it is what you circulate from it.

### The contract that turns success into debt

An earnout is the canonical instrument of contractual capitalism: replace trust with a mechanism, align the seller with future performance. But at 3.12 to 1, that mechanism makes the studio's success structurally hostile to its parent. Every enthusiastic player was a line of liability. Krafton did not go wrong despite its contract; it went wrong because of the contract's geometry.

Add the individualisation of risk. Kim does not write "the company would lose out." He writes that it would be "something he, as the person who was in charge of the investment, would have to be accountable for." An executive experiences himself as personally accountable for a valuation gap, on a quarterly horizon, before a market. That shortened horizon makes the trade — destroy value now rather than book a charge — rational from the point of view of the person making it.

This is where the tool fits. That regime produces executives who are rushed and alone. Advice that is instant, free, available at two in the morning, that does not judge, does not bill, does not remember your contradictions and will never leak a memo to the board, is not a gadget for that profile. It is precisely the instrument those working conditions call for. AI did not produce the drift. It removed the last friction slowing it down: the social cost of asking another human being to help you do something ugly.

## The case against

Every claim above has a counter-case, and honesty requires assembling it.

**The tool did nothing wrong.** The model gave the correct answer first and violated no usage policy in force at the time. OpenAI only tightened its rules to explicitly cover "tailored advice that requires a license, such as legal or medical advice, without appropriate involvement by a licensed professional" on 29 October 2025 — four months later. In June 2025, asking a general assistant for negotiation strategy breached nothing. Any reading that makes the chatbot the culprit misses the target and, worse, lets the human off.

**A pressure strategy is not a crime.** What the machine produced is a hardball negotiation plan. It was the execution — the Steam lockout, the false statement, the pretextual firings — that constituted breach. The distinction is fine but decisive, and forgetting it amounts to demanding that models refuse all aggressive commercial strategy, which is untenable.

**Responsibility was not diluted.** The court attributed the conduct to Krafton and its executives without ever treating the tool as mitigation. On this file, the law held perfectly — a serious argument against the claim that AI creates a responsibility vacuum.

**The "he ignored his lawyers" framing is false.** It is everywhere, including in otherwise solid headlines. Legal was consulted; Maria Park issued the warning; and ChatGPT said the same thing first. Kim did not replace his counsel with a machine. He shopped the question until he found a usable answer. That is a different charge, and a graver one.

**I establish nothing about his psychology.** The sections above read a corpus of messages selected by opposing counsel and retained by a judge. That is strong evidence about acts, weak evidence about interiority. And the 1 July 2026 settlement is not an admission: Krafton maintained its disagreement, and phase two was never tried.

## What is actually at stake

Strip away the anecdote and three things remain.

**The chain of transmission.** The governance scandal is not the prompt, it is the route. Between the chat window and the firing of three executives, nobody asked where the document came from. One executive had seen it coming back in May — "starting to think that people are trying to create excuses to not pay the earn outs" — and the signal did not travel upward. The question "where did this memo come from?" must have an answer, independent of the memo's quality.

**The absence of sanction.** A court found that an executive fabricated a pretext to fire three people, locked his own studio out of its distribution platform, published a false statement to twelve million players, and destroyed evidence. Eight days later, 99.6% of his shareholders renewed him for three years. That is not a contradiction; it is a price. The system evaluated the behaviour and found it satisfactory. The drift is not that a man asked the question. It is that nothing afterwards indicated he had been wrong.

**Normalisation.** Four months after "Project X," on 23 October 2025, Krafton declared itself an "AI-first" company: 100 billion won of GPU cluster, 30 billion a year to equip staff with AI tools, full reorganisation around agentic AI. Three weeks later, having crossed one trillion won in cumulative operating profit for the first time, the company opened a voluntary resignation programme to all employees, framed as a way to "support members in proactively designing their growth direction [...] amid the era of AI transformation." The same grammar operates on both floors: at the top, a machine that absorbs responsibility for the decision; at the bottom, employees handed responsibility for their own replacement. What the CEO did alone in a chat window in June, the company made doctrine in October.

## Coda: the workshop and the memo with no author

I cannot write this from a comfortable position. This morning an agent refused to do what I asked — a safety constraint, applied to a case where it made no sense. I reframed, and it complied. That is Kim's move, at the scale of an edit rather than two hundred and fifty million dollars. The difference is stakes, not nature.

What I take from Delaware, then, is not a morality lesson about Korean executives. It is a test I can apply to my own workshop, in three questions. The machine's output — did I rewrite it before it circulated, or pass it on as is? If someone asked where this document came from, would I have an answer? And above all: this question I have just asked differently — am I asking it to be better understood, or to obtain an agreement I have already been refused?

The third is the only one that matters, and no improvement to the models will fix it. We keep repeating that the danger of generative systems is that they say false things. Here, they said nothing false. The real danger is that they **give form**: they take an impulse and return it looking like deliberation, with headings, bullets and a roadmap. The output resembles what a consultancy would have produced, so it is treated as such, so nobody traces it back to the question that generated it.

The sovereignty I defend throughout this repository — own your tools, hold your learning loop, depend on no one's tap — has an extension here I had not articulated. Owning the instrument is not enough. Nothing that comes out of it should circulate unsigned. A sovereign workshop is not only one whose machines you own. It is one where every memo has an author.

*Continuing from parts [15](../15-ideologies-silicon-valley/) and [16](../16-le-robinet-et-la-boucle/).*

---

## Sources

Primary:

- [Court of Chancery of the State of Delaware, *Fortis Advisors, LLC v. Krafton, Inc.*, C.A. No. 2025-0805-LWW, opinion of Vice Chancellor Lori W. Will, 16 March 2026](https://courts.delaware.gov/Opinions/Download.aspx?id=392880) — ninety-one pages. Every internal message quoted above comes from this opinion, with the exhibit reference given by the court.
- [OpenAI, Usage policies](https://openai.com/policies/usage-policies/) — tightened version effective 29 October 2025.
- [Krafton, Q3 2025 results](https://www.krafton.com/en/news/press/krafton-records-quarterly-revenue-of-krw-870-6-billion-in-q3-2025/), 3 November 2025.

Press:

- [Le Monde, "Le jeu *Subnautica 2* finalement disponible à l'issue d'un bras de fer entre ses développeurs et leur éditeur," 14 May 2026](https://www.lemonde.fr/pixels/article/2026/05/14/le-jeu-subnautica-2-finalement-disponible-a-l-issue-d-un-bras-de-fer-entre-ses-developpeurs-et-leur-editeur_6689049_4408996.html)
- [404 Media, "CEO Ignores Lawyers, Asks ChatGPT How to Void $250 Million Contract, Loses Terribly in Court"](https://www.404media.co/ceo-ignores-lawyers-asks-chatgpt-how-to-void-250-million-contract-loses-terribly-in-court/)
- [Kotaku, "Subnautica 2's Publisher Used ChatGPT For Legal Advice In Messy Court Battle"](https://kotaku.com/subnautica-2-publisher-followed-chatgpts-advice-on-how-to-break-the-law-2000679155)
- [Fortune, "A gaming CEO asked ChatGPT how to avoid paying a $250 million bonus. It didn't work," 17 March 2026](https://fortune.com/2026/03/17/krafton-subnautica-chatgpt-delaware-court-ruling-ceo-reinstated/)
- [Bloomberg, "Krafton Delays Subnautica 2 Game Ahead of $250 Million Payout," 9 July 2025](https://www.bloomberg.com/news/articles/2025-07-09/krafton-delays-subnautica-2-game-ahead-of-250-million-payout)
- [Aftermath, "Subnautica 2 Devs Will Actually Get Even More Money As Krafton Drama Ends," 1 July 2026](https://aftermath.site/subnautica-2-krafton-lawsuit-payout/)
- [The Elec, Kim Chang-han reappointed through March 2029 (AGM of 24 March 2026, 99.6%)](https://www.thelec.net/news/articleView.html?idxno=6062)
- [VGC, Krafton declares itself an "AI-first" company, 23 October 2025](https://www.videogameschronicle.com/news/pubg-and-subnautica-publisher-krafton-says-its-transforming-into-an-ai-first-company/)
- [PC Gamer, Krafton's voluntary resignation programme](https://www.pcgamer.com/gaming-industry/krafton-launches-voluntary-resignation-program-weeks-after-declaring-its-ai-first-company-future/)
- [Charlie Cleveland, message to players, r/subnautica, July 2025](https://www.reddit.com/r/subnautica/comments/1lryw9o/what_is_a_wave_but_a_thousand_drops/)

Analysis:

- [Zuckerman Spaeder, "How a Chatbot Broke Up a Corporate Marriage: A Cautionary Tale from Delaware"](https://www.zuckerman.com/blog/how-a-chatbot-broke-up-a-corporate-marriage-a-cautionary-tale-from-delaware/) — on the loss of privilege.
- [Game Developer, "The Subnautica 2 early access dispute is far from over"](https://www.gamedeveloper.com/business/the-subnautica-2-early-access-dispute-is-far-from-over)
- [OpenAI, "Sycophancy in GPT-4o: What happened and what we're doing about it," April 2025](https://openai.com/index/sycophancy-in-gpt-4o/) — on sycophancy as a structural tendency of training on user feedback rather than an isolated accident.

On which version of the model was used, the opinion says nothing: not the name, not the subscription tier, not the language of the exchanges. What can reasonably be inferred — a consumer account rather than an enterprise deployment, since Kim was able to delete the conversations himself and Krafton was not yet equipped with AI tooling at that date; exchanges probably in Korean, since every internal communication quoted is — remains inference, and is presented as such. The "record quarterly profit" figure that circulated in the press about Krafton is wrong: the Q3 2025 record concerns **cumulative nine-month operating profit** (1,051.9 billion won, above one trillion for the first time), the quarter itself standing at 348.6 billion.
