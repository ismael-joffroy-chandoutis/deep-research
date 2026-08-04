**English. Version française : [README.fr.md](README.fr.md)**

# Just With Big Computers

### What the NVIDIA partnership reveals about Ilya Sutskever's thesis on the end of scaling

*Ismaël Joffroy Chandoutis*

*July 2026*

---

On 27 July 2026, at nine in the morning New York time, NVIDIA and Safe Superintelligence Inc. issued a joint release titled "Ilya Sutskever's Safe Superintelligence Inc. and NVIDIA Announce Long-Term Strategic Partnership." The subtitle says the essential thing: "Access to NVIDIA's Best-in-Class Vera Rubin Systems **Expands SSI's Compute by an Order of Magnitude**."

The announcement was immediately read as a contradiction. For two years Sutskever has been the public face of the thesis that the era of scaling is over and that progress once again depends on new scientific ideas. Now he is multiplying his compute tenfold.

The contradiction is real but it is not where people are placing it, and the charge of plain inconsistency would be lazy. What deserves examination is the qualifier everyone has systematically cut from his sentences.

## What the release says, and what it does not

The text is short and every phrase is weighed.

> "For the last two years, SSI has been quietly advancing a new research direction to unlock a powerful and robustly aligned artificial intelligence."

> "NVIDIA entered this partnership after obtaining **rare access into the company's closely guarded research**."

> "The two companies will also collaborate on the technical advancement of NVIDIA's current and future compute platforms, **leveraging SSI's unique insights into the future of AI**."

Sutskever, quoted:

> "**We have research that is worthy of scaling up**, and having access to a big NVIDIA computer will let us do so. […] we are confident that **our big bet on the Vera Rubin platform** will take us to the next level."

Jensen Huang, quoted:

> "Ilya has pioneered fundamental breakthroughs at the foundation of modern AI, beginning with AlexNet. We are excited to see what new breakthroughs SSI will discover powered by our Vera Rubin platform."

Two observations. First: Huang mentions neither safety, nor superintelligence, nor alignment. He mentions AlexNet, that is, 2012. NVIDIA is buying a bet on a person, not on a mission. Second: Sutskever does not say "our bet on scaling," he says "our big bet on the Vera Rubin platform." The distinction is rhetorically convenient, and it may well be sincere.

What the release omits is equally instructive. **No dollar figure.** The five-billion number that made every headline comes from anonymous sources reported by Bloomberg and Reuters, not from the official text, which can be checked on all three of its hostings. No equity percentage, no new valuation, no dated schedule — the "10x our compute in the next 12 months" comes from an SSI post on X, not the release. No board seat. Not a word about the existing Google Cloud arrangement.

A further editorial curiosity: the "About Safe Superintelligence Inc." boilerplate lists Andreessen Horowitz, DST Global, Greenoaks and Sequoia Capital as investors — omitting Alphabet, Lightspeed, SV Angel, and NVIDIA itself, even though Reuters established Alphabet's and NVIDIA's stakes back in April 2025. A release in which the investor announcing its investment does not appear on the list of investors.

Financial context, for the record: SSI was valued at $32 billion in April 2025, with no product, no revenue, no published research, and a few dozen employees split between Palo Alto and Tel Aviv. Estimates of total raised before NVIDIA diverge — three billion according to Sutskever himself in November 2025, roughly seven according to PitchBook and TechCrunch. Neither company is obliged to publish anything, and neither does.

## The three ages

The canonical formulation dates from the Dwarkesh Patel interview, November 2025:

> "Up until 2020, from 2012 to 2020, it was the age of research. Now, from 2020 to 2025, it was the age of scaling… But now the scale is so big… **it's back to the age of research again, just with big computers.**"

And, of his company: "We are squarely an 'age of research' company."

The most original passage of that interview is nonetheless almost always dropped from summaries. Asked why scaling came to dominate, Sutskever gives not a technical but a sociological answer:

> "The scaling insight arrived… everyone realized we should scale, and it's just — **this is an example of how language affects thought. 'Scaling' is just one word, but it's such a powerful word, because it informs people what to do.**"

Scaling won, he says, because it supplied thousands of people with an unambiguous operational instruction. That is a thesis about the economics of scientific attention, not about scaling laws. It deserves better than the oblivion it has fallen into.

## The qualifier everyone cuts

Here is where the inconsistency charge collapses.

Sutskever never said scaling does not work. His sentence is "back to the age of research again, **just with big computers**." And in November 2024, to Reuters, his formulation was: "**Scaling the right thing** matters more now than ever." That is not an anti-scaling position; it is a position about the order of operations: find the right idea first, then scale it.

The 27 July release is literally consistent with that programme. "We have research that is worthy of scaling up" means: the research phase has produced something, we are entering the scaling phase. That is the announced plan, executed in the announced order.

The informational value of that sentence is worth measuring. In 2026, Ilya Sutskever's only public words are a post on X on 27 February, court testimony on 11 May, and a quote in this press release. No interview, no paper, no publication. The many 2026 articles that appear to comment on a recent interview are in fact all commenting on the same November 2025 conversation. In that twenty-five-month silence, "we have research that is worthy of scaling up" is SSI's first communication about the state of its science. It says nothing about its content.

## The subtext, layer by layer

### The periodisation moves

Here is the element the sources reveal and which, as far as I can establish, has not been publicly noted.

In November 2024, to Reuters, Sutskever states that **the 2010s were the age of scaling**. In November 2025, with Dwarkesh Patel, he states that **2012–2020 was the age of research** and that scaling only began in 2020.

The two statements are incompatible. They do not concern different objects; they date the same transition to contradictory moments. The three-ages periodisation is therefore not a stable historical reading but a rhetorical construction revised from one year to the next — whose function stays constant: to place the present, whatever it is, at the threshold of a return to research. The boundaries move; the conclusion never does.

This is not dishonesty, and it does not refute the thesis on the merits. But it indicates that the thesis functions less as an observation than as a position: fundamental research is always what has just been neglected, and always what will decide what comes next. It is also, incidentally, the thesis that best values a laboratory of a few dozen researchers with no product, against companies spending hundreds of billions on infrastructure.

### What he actually holds against current models

Sutskever is not LeCun, and conflating the two is the most widespread distortion in this file.

His critique concerns **generalisation** and **sample efficiency**. Models learn far more slowly than humans from equal information, and generalise worse out of distribution. He does not say the architecture is a dead end; he says it is an incomplete foundation. He explicitly rejects the "complicated prior" hypothesis — the nativist thesis Gary Marcus defends — so the apparent convergence between them is superficial.

LeCun does use the word. His exact formulation, which must be quoted in full because the press truncates it systematically, is: "LLMs basically are a dead end **when it comes to superintelligence**." Not "LLMs are a dead end," but "LLMs do not lead to human-level intelligence." The qualifier changes everything, and it disappears in nine reproductions out of ten.

The difference between the two men shows in their companies. SSI is led by Sutskever as CEO and chief scientist, with no product and no date. AMI Labs, founded by LeCun with six others — including Alex LeBrun, Laurent Solly, Pascale Fung and Saining Xie — is headquartered in Paris with offices in New York, Montreal and Singapore, and advertises industrial applications: process control, automation, wearables, robotics, healthcare. LeCun is its scientific guarantor and doctrinal flag, not its operational head. Two bets on the post-LLM era, two opposite structures: one capitalising on secrecy, the other on the market. Part [12](../12-le-pari-lecun/) examines the second in detail.

### The economics of the bet

Sutskever's thesis has a financial consequence he never states and which his investors must.

According to Epoch AI's compilation from SEC filings, combined capex for Alphabet, Amazon, Meta, Microsoft and Oracle reached roughly $500 billion in 2025, growing at an average 72% per year since mid-2023. Projections for 2026 range from $630 to $770 billion depending on scope — and growth rates quoted without their scope should be distrusted, since circulating aggregations do not share a base.

One correction is rarely applied: Microsoft attributes $25 billion of its $190 billion, or 13%, to component price increases, and Meta cites the same cause first. A substantial share of the capex escalation is therefore not additional capacity but memory inflation. Raw figures overstate real capacity growth.

The hardest signal of 2026 lies elsewhere: Alphabet posted negative free cash flow. The best-capitalised company in the group, the one that designs its own TPUs and therefore carries the lowest unit costs, is burning cash. When the cheapest producer loses money, the question is no longer whether the spending is sustainable but who lasts longest.

In that landscape, a lab of a few dozen people announcing a tenfold compute increase with no product and no revenue is not an anomaly: it is an option position. If the bottleneck really has become scientific, a small team with a correct idea and ten times more machines is better placed than a hyperscaler with a hundred times more machines and no new idea. If the bottleneck remains industrial, SSI has no chance. NVIDIA, which sells the machines in both scenarios, takes no directional risk — it is buying a hedge on the hypothesis that would threaten it.

## The case against

**"He said scaling was dead" is false.** He said "pre-training as we know it *will* end" — future tense, for a specific reason: data exhaustion. And he always added "with big computers." No primary source shows him claiming that scaling no longer works.

**The NVIDIA partnership is therefore not a recantation.** It is the execution of the second half of a programme whose first half was silence. Reproaching someone who said "find the idea then scale it" for scaling after finding an idea is a badly prepared case.

**But nothing proves there is an idea.** "Research worthy of scaling up" is an unverifiable claim issued by an interested party, in a joint release with its new investor, on the day a financing is announced. SSI has published no paper, no result, no demonstration in twenty-five months. The only external attestation is NVIDIA's, which says it obtained "rare access" to that research — and which put money on it. That is a testimonial, not peer review.

**The five-billion figure is not confirmed.** Neither NVIDIA nor SSI states it. It circulates as established fact; it is not.

**Silence has commercial value.** A lab that publishes nothing can be neither refuted, nor copied, nor compared. Discretion claimed as scientific discipline — "quietly advancing a new research direction" — is also the informational regime that maximises a valuation. Both readings coexist and neither disqualifies the other.

**Several quotations attributed to Sutskever are apocryphal.** The lines about emotions as "highly efficient value functions," or about the regret felt after a bad chess move, widely reproduced, do not appear in the Dwarkesh transcript. They are commentators' paraphrases placed inside quotation marks. Not to be cited.

## What is actually at stake

**An empirical question, not a doctrinal one.** The "scaling versus research" debate is badly posed while it stays doctrinal. It becomes decidable the day SSI publishes something, or does not. A tenfold compute increase is precisely the apparatus that makes the thesis falsifiable: if the idea is good, it will produce a visible result; if not, SSI will have consumed an extra order of magnitude of compute for nothing, which is about as clean a refutation as this field permits.

**The displacement of scarcity.** What the three positions — Sutskever, LeCun, the hyperscalers — share is more interesting than what divides them: all concede that compute alone no longer suffices. They differ on what is missing. For the hyperscalers, more compute and more electricity. For LeCun, an architecture that represents the world rather than text. For Sutskever, a theory of generalisation. These three answers do not cost the same: the first is financed by capex, the second by applied research, the third by patience — and patience is the sector's most expensive resource right now.

**The supplier's paradox.** NVIDIA simultaneously funds the thesis that validates it and the one that threatens it. It sells machines to hyperscalers convinced compute is the answer, and invests in a man who publicly argues it no longer is. That is not a contradiction on its part; it is the definition of a well-run arms dealer. But it means the appeal to authority — NVIDIA invested in Sutskever, therefore his thesis is sound — is worthless. NVIDIA would have invested either way.

## What remains

The title of this part is the half of the sentence everyone cuts. "Back to the age of research again, **just with big computers**" — the subordinate clause is the opposite of a detail: it says the return to research happens not against compute but with it, at a scale that has never existed. That is a far less spectacular position than the one attributed to him, and far harder to refute.

The unstable periodisation, on the other hand, licenses a less generous reading. A thesis whose dates move while its conclusion holds is not a historical observation: it is an interpretive frame that will always yield the same diagnosis. That the diagnosis is correct remains possible. That it was reached by examining the facts is less so.

The 27 July partnership settles nothing. It merely sets a deadline: within twelve months, a team of a few dozen people will hold ten times the compute and a public claim to have found something. At that point there will be no position left, only a result or its absence.

*Continuing from parts [12](../12-le-pari-lecun/) and [16](../16-le-robinet-et-la-boucle/).*

---

## Sources

Primary:

- [NVIDIA / SSI, "Ilya Sutskever's Safe Superintelligence Inc. and NVIDIA Announce Long-Term Strategic Partnership," 27 July 2026, 09:00 ET](https://nvidianews.nvidia.com/news/ilya-sutskevers-safe-superintelligence-inc-and-nvidia-announce-long-term-strategic-partnership) — also on [GlobeNewswire](https://www.globenewswire.com/news-release/2026/07/27/3333561/0/en/Ilya-Sutskever-s-Safe-Superintelligence-Inc-and-NVIDIA-Announce-Long-Term-Strategic-Partnership.html) and [NVIDIA investor relations](https://investor.nvidia.com/news/press-release-details/2026/Ilya-Sutskevers-Safe-Superintelligence-Inc--and-NVIDIA-Announce-Long-Term-Strategic-Partnership/default.aspx).
- Ilya Sutskever, interview with Dwarkesh Patel, November 2025 — source of the three-ages thesis and the analysis of the word "scaling."
- Statement to Reuters, November 2024: "Scaling the right thing matters more now than ever."
- [AMI Labs](https://amilabs.xyz/) — founding members, positioning, application domains.
- [Epoch AI, hyperscaler capex trend](https://epoch.ai/data-insights/hyperscaler-capex-trend) — compiled from SEC filings (10-Q, 10-K) for Alphabet, Amazon, Meta, Microsoft and Oracle.

Press and analysis:

- [TechCrunch, "Ilya Sutskever's Safe Superintelligence partners with Nvidia to scale its AI research," 27 July 2026](https://techcrunch.com/2026/07/27/ilya-sutskevers-safe-superintelligence-partners-with-nvidia-to-scale-its-ai-research/)
- [Calcalist, on the amount and the absence of a product](https://www.calcalistech.com/ctechnews/article/qy9eg5jw4)
- [Unite.ai, "Nvidia Takes a Stake in Sutskever's Safe Superintelligence"](https://www.unite.ai/nvidia-takes-a-stake-in-sutskevers-safe-superintelligence/)
- [Yann LeCun on Threads, November 2024](https://www.threads.com/@yannlecun/post/DCTebu7tmNG) — "We've been working on 'the next thing' for a while now at FAIR."

The five-billion figure, the exact size of NVIDIA's share-price move on 27 July, SSI's total raised before this transaction and its real headcount are all points where sources contradict one another or rest on anonymous informants; they are given above with their ranges rather than as single values. Capex figures come from compilations of SEC filings rather than the filings themselves. The quotations attributed to Sutskever about emotions as value functions, widely reproduced online, cannot be found in the November 2025 transcript and are not used here. No reaction from Sutskever to the July 2026 OpenAI–Hugging Face incident was found; the calendar proximity between that incident and the partnership announcement is an apparent coincidence, and nothing establishes a link.
