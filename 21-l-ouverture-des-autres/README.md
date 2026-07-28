**English. Version française : [README.fr.md](README.fr.md)**

# Other People's Openness

### The letter of 24 July 2026, its 133 signatories, and the lab that did not sign

*Ismaël Joffroy Chandoutis*

*July 2026*

---

On 24 July 2026, an open letter titled "Open Weights and American AI Leadership" was published with twenty-five founding signatories. Four days later there were one hundred and thirty-three. Amazon, AMD, Google, Intel, OpenAI, SpaceX, Cisco, Cloudflare, Databricks, Red Hat, SAP, Siemens and Uber had joined Meta, Microsoft, NVIDIA, IBM, Mistral, Mozilla, Hugging Face, Palantir, the Linux Foundation and Y Combinator.

Three notable companies are missing: Apple, xAI, and Anthropic.

The same day, Jensen Huang published the first post of his life on X to promote the letter. Three days later, under pressure that had become personal, Dario Amodei published "Our position on open-weights models."

The sequence has been told as a confrontation between an industry unanimously in favour of openness and one lab seeking to restrict it to protect its business. That reading stands up, and several facts support it. It omits two that seriously complicate it: what each signatory keeps closed, and what happened to Anthropic six weeks earlier.

## What the letter says

The document is short and its argument is economic before it is political.

> "Our AI leadership will be judged not by one frontier AI model, but by whether the United States builds a strong, open ecosystem that diffuses into every sector."

> "Open weights let every organization match the right model to the right job at the right cost, **reserving frontier-scale capability for genuine frontier problems** and running efficient, specialized models everywhere else. That discipline is what will make AI economically sustainable as its use scales into the billions of everyday tasks."

This is the cost-segmentation argument: the frontier for frontier problems, cheap specialised models for everything else. It is sound, and it is true.

One material detail contradicts the media account. The PDF is hosted on **Microsoft's** Corporate Responsibility site. No dedicated site, no constituted coalition, no neutral third party. Microsoft is the de facto coordinator, while coverage overwhelmingly credited NVIDIA — a direct effect of Huang's post.

The timing is not innocent either. The letter appears the day after the AI Kill Switch Act was introduced and two days after Axios revealed OpenAI and Anthropic's aligned lobbying in Washington. It is a counter-offensive, and it is dated.

Note also that the Lieu-Moran bill mentions neither "open source" nor "open weights." It requires developers of the most powerful systems to retain the ability to "throttle, suspend, or shut them down." The incompatibility with open weights is structural, not intentional: you cannot remotely switch off weights already downloaded. The letter calls this "premature restrictions"; it is more precisely a mechanical consequence.

## What each signatory keeps closed

Here the word hypocrisy becomes tempting, and it should be handled with precision rather than indignation.

**NVIDIA.** Jensen Huang is the campaign's public face. His statements of 22 and 24 July leave no doubt about the nature of his interest:

> "These Chinese models are excellent. Open-source models that are excellent should be used."

> "**Whenever there's more use, you'll have to sell a lot more NVIDIA computers.**"

> "**Free AI should be great for hardware. Free AI should be great for chips. Free AI should be great for data centers.**"

The last sentence is the entire thesis, stated by its principal beneficiary. A free model is a model someone must run, and running a model requires buying hardware. NVIDIA is not arguing for open models against its interest: it is arguing for the commoditisation of its complement. That is textbook strategy, and perfectly rational.

Meanwhile, what NVIDIA keeps closed: CUDA, its drivers, most of its proprietary software stack. The company demanding that weights be freed does not free the layer that secures its lock-in.

**Microsoft** coordinates the letter while holding the sector's closest relationship with a closed lab, and developing its own unpublished in-house models.

**Google** signed later. Gemma is open; Gemini, which is the product, is not.

**Meta** is the signatory whose position has moved most, in the opposite direction from its rhetoric: after the Meta Superintelligence Labs reorganisation, the company that made Llama the banner of open weights has markedly closed its frontier.

**OpenAI** joined over the weekend. It published open models in 2025 and its CEO conceded he had been "on the wrong side of history" on the question — while keeping closed absolutely everything that constitutes its business.

The honest conclusion is this: **no signatory is arguing to open its own frontier product.** All are arguing to open a layer they do not monetise, or monetise only indirectly. That does not make the argument false — cost segmentation is right regardless of who says it. But it means the letter is not a manifesto about software freedom. It is an agreement between actors whose business models all benefit from a free layer located exactly where none of them makes money.

## What Anthropic says

Amodei's 27 July post answers point by point, and its first move is a denial: Anthropic has never called for a ban on open weights.

His position rests on a distinction. Small open models bring real benefits to research and competition; frontier systems pose a problem of irreversibility. His exact wording — which must be quoted correctly, since the circulating "no undo button" is a journalist's phrase and not his — is that **"once weights are released they cannot be withdrawn."**

In place of a ban he proposes three policies: tighter controls on chips and chipmaking equipment flowing to authoritarian governments; a crackdown on "industrial-scale distillation," that is, training models on the outputs of more advanced systems; and mandatory safety testing for all sufficiently capable models, open and closed, regardless of country of origin — while acknowledging the condition that makes it hard: "testing would need to be **global**, which means even the CCP would need to be on board."

The third proposal is not opportunistic: Anthropic already recommended a "testing and auditing regime" in its written Senate testimony in 2023, with the comparison to cars and aircraft. On that point the continuity is verifiable across three years.

Responses were immediate and personal. David Sacks: "The entire tech industry (save for Anthropic) has come out in favor of open source AI… They won't stop until they kneecap open source." Bill Gurley, more economically: "Excited to see Anthropic acknowledge the real problem with open is it competes with their corporate economic strategy." Kai-Fu Lee: "Who DIDN'T sign the Open Weight letter is far more interesting than who did."

## The subtext, layer by layer

### What happened to Anthropic six weeks earlier

Almost nobody mentioned it during the controversy, and it is the central fact of the file.

On **12 June 2026**, the US government issued an export-control directive, invoking national security, requiring Anthropic to suspend all access by any foreign national to **Claude Fable 5 and Mythos 5** — inside and outside the United States, including its own foreign employees. The directive arrived at 5:21 p.m. Eastern, with no detail on the justification.

Since enforcing a nationality rule on a shared cloud service is impracticable, Anthropic switched both models off for everyone, worldwide. It appears to be the first export-control measure aimed at specific AI models rather than chips.

The stated motive was a method for circumventing Fable 5's guardrails, discovered by Amazon researchers. On examination Anthropic found only "minor vulnerabilities," a narrow and non-universal bypass that other publicly available models — it names Claude Opus 4.8, GPT-5.5 and Kimi K2.7 — could equally identify. Anthropic complied while contesting, warning that applying such a standard across the industry would "essentially halt all new model deployments," and asking that such actions follow transparent statutory processes grounded in technical fact.

Three days after the shutdown, around a hundred cybersecurity leaders signed a letter demanding reversal, arguing the measure had "taken the best models away from defenders, created market uncertainty, and risked America's AI leadership without any real risk to justify it."

Controls were lifted on 30 June; access was restored on 1 July.

The argument Anthropic made in June is, word for word, the structure of the argument in the letter it declines to sign in July: restricting one category of capable model does not remove the capability, it removes it from the people who follow the rules.

**Anthropic mentions this episode nowhere in its 27 July post.** It is its best available answer to the charge of being structurally pro-restriction — it was itself restricted, and publicly objected. It does not use it.

### The distinction that holds, and the contradiction that remains

The charge of formal inconsistency does not survive scrutiny, and this should be said plainly. Anthropic asked that its model remain **on sale**. It never asked to publish its weights. Selling access to a model you continue to control is not the same as publishing one anyone can copy and modify forever. Amodei has never argued frontier models should be unrestricted; he argues they should stay in the hands of a small number of accountable labs — which is an argument against the July letter *and* against the June order, simultaneously. That is coherent. It is also, as Gurley noted, extremely convenient.

What remains is a second-order contradiction that neither critics nor defenders have formulated, and which seems to me the post's real weak point.

Amodei's third pillar is mandatory safety testing for all sufficiently capable models. Yet in June a government applied to Anthropic a restriction founded precisely on a judgment of dangerous capability. Anthropic answered that the judgment was technically wrong, the capability banal, and the procedure opaque. The regime Amodei calls for therefore produced, in the only known case where it was applied to him, an outcome he judged disproportionate.

The disagreement is not settled by "there should be testing." It concerns **who interprets the tests, under what procedure, and with what recourse**. The 27 July post says nothing about this, though Anthropic is the only lab with direct experience of it.

### The distillation charge, and its fragility

On 22 July, White House science adviser Michael Kratsios accused Moonshot of distilling Claude Fable 5 to build Kimi K3, and Treasury Secretary Scott Bessent floated sanctions. Trade Representative Jamieson Greer indicated that USTR treats Chinese distillation as a form of IP theft.

The next day, named experts contested the claim on timing grounds. Braden Hancock: "You can't distill that much data, train a model, and release it in two weeks." Fable 5 was redeployed on 1 July; Kimi K3 shipped on the 16th.

Two distinct accusations collided in the coverage and must be separated: Anthropic accuses **Alibaba** of a distillation campaign running April to June, with quantified but non-public evidence; the White House accuses **Moonshot** in July, without producing evidence. The timing objection tells against the second, not the first.

The structural objection to the anti-distillation pillar lies elsewhere and is more serious: treating distillation as IP theft would lead to de facto restrictions on open-weight models, including independently developed ones. You cannot prove a model was *not* distilled.

### What the Hugging Face incident did to this debate

On 24 July it emerged that Hugging Face, analysing the breach caused by OpenAI's agents, had to abandon closed models — **Claude Fable 5 by name** — whose classifiers refused to distinguish a defender from an attacker, and switch to self-hosted Chinese open-weight GLM 5.2.

That refusal was not an anomaly. It was the nominal behaviour of the widened classifier Anthropic deliberately installed at the 1 July redeployment, explicitly accepting more false positives: "Users experience the safety margin as a model refusing to respond to some reasonable, non-harmful requests."

The causal chain is complete, and remarkable. An export control in June leads Anthropic to harden its guardrails in July; that hardening blocks a legitimate defender during a major incident three weeks later; and that episode becomes the most concrete argument for open weights the July campaign produced. A safety constraint imposed on a closed model manufactured, in three steps, the best advertisement for open ones. Part [19](../19-tricher-a-son-propre-examen/) covers that episode in detail.

## The case against

**The letter's argument is right, independent of the interests carrying it.** Cost segmentation is an economic reality, not a slogan. An ecosystem where you must call a frontier model to sort email will not scale. That NVIDIA profits does not make the proposition false.

**"Hypocrisy" is too short a word.** No signatory claims to be opening its frontier product. The letter asks nobody to open anything: it asks that openness not be *banned*. That is a regulatory position, not a corporate commitment. The contradiction would be flagrant if the signatories presented themselves as champions of free software; they present themselves as opponents of a legislative restriction.

**Anthropic is isolated by exposure, not ideology.** It is the only major lab whose model was named in an export control, whose model is named in a distillation accusation, and whose guardrails named-and-blocked a defender. That gives it both experience nobody else has and a direct commercial interest in the outcome. Both at once — which is exactly what makes its testimony valuable and suspect.

**The silence did not last.** Anthropic was accused of not responding for three days; it published a reasoned position on the 27th. Reproaching a three-day delay to a company that then publishes a detailed argument is a trial of intent.

**Several spectacular elements rest on a single source.** The letter from a hundred cyber leaders and its signatories, the 33% rise in Zhipu's shares the day after Fable 5 went dark, the founding of the Open Secure AI Alliance in the wake of the Hugging Face incident: all come from one article and are uncorroborated. They are noted here as reported, not established.

## What is actually at stake

**The question is not "open versus closed" but "who decides on capability."** The three camps agree on more than they admit: nobody is asking for frontier weights to be published, nobody is asking for a complete ban. The real disagreement concerns the capability threshold beyond which an authority may intervene, and who that authority is. June shows what happens when that is unsettled: a directive arrives at 5:21 p.m. with no technical reasoning, and a model vanishes from the planet.

**Openness as principle is distinguished from openness as tactic by a single test:** are you still for openness when you are ahead? Part [17](../17-xi-jinping-ai-geopolitics/) applies that test to China, where the answer is currently being written into draft export restrictions on its best models. The same test applies here: one hundred and thirty-three signatories argue for opening a layer none of them depends on. The day one of them publishes the weights of the model that constitutes its revenue, the argument changes nature.

**Amodei's strongest pillar is the least discussed.** Mandatory testing for all sufficiently capable models, open and closed, regardless of origin, is the only proposal in the debate that structurally favours nobody. That is probably why it interests so few people.

## What remains

Hypocrisy does not quite describe the situation, which is a pity because it would be convenient. What is happening is more ordinary and more instructive: one hundred and thirty-three companies discovered a convergent interest in one specific layer of the stack being free — precisely the layer where none of them makes money. They are right on the merits, and they deserve no credit for being right.

The company that did not sign is the one whose frontier product is most directly at stake, and it defends a position that protects its business. It was also, six weeks earlier, the only documented victim of the kind of arbitrary state intervention the letter warns against — and it chose not to say so, because saying so would have forced it to specify who, under its own mandatory testing regime, holds the pen.

*Continuing from parts [15](../15-ideologies-silicon-valley/), [17](../17-xi-jinping-ai-geopolitics/) and [19](../19-tricher-a-son-propre-examen/).*

---

## Sources

Primary:

- ["Open Weights and American AI Leadership," 24 July 2026, PDF hosted by Microsoft](https://www.microsoft.com/en-us/corporate-responsibility/wp-content/uploads/2026/07/open-weight-models-letter-1.pdf) — [page and living signatory list](https://www.microsoft.com/en-us/corporate-responsibility/topics/open-weight/).
- [Dario Amodei, "Our position on open-weights models," Anthropic, 27 July 2026](https://www.anthropic.com/news/position-open-weights-models).
- [Anthropic, "Statement on the US government directive to suspend access to Fable 5 and Mythos 5," 12 June 2026](https://www.anthropic.com/news/fable-mythos-access).
- [Anthropic, "Redeploying Claude Fable 5," 30 June 2026 (updated 1 July)](https://www.anthropic.com/news/redeploying-fable-5).
- [Rep. Ted W. Lieu's press release on the AI Kill Switch Act, 23 July 2026](https://lieu.house.gov/media-center/press-releases/reps-lieu-and-moran-introduce-bill-require-kill-switch-ai-systems-can).

Press:

- [The Next Web (Ana Maria Constantin), "Anthropic won't defend open weights. In June it made the same argument for itself.", 27 July 2026](https://thenextweb.com/news/anthropic-open-weights-letter-holdout-fable-5-shutdown) — the piece that establishes the parallel.
- [Axios, "OpenAI and Anthropic unite against open-weight AI risks," 22 July 2026](https://www.axios.com/2026/07/22/openai-anthropic-open-models-trump-china).
- [TechCrunch, "Treasury threatens sanctions after White House claims Moonshot distilled Anthropic's Fable," 22 July 2026](https://techcrunch.com/2026/07/22/treasury-threatens-sanctions-after-white-house-claims-moonshot-distilled-anthropics-fable/).
- [TechCrunch, "Experts say exploiting Anthropic's Fable isn't how Kimi K3 got so good," 23 July 2026](https://techcrunch.com/2026/07/23/experts-say-exploiting-anthropics-fable-isnt-how-kimi-k3-got-so-good/).
- [Business Insider (Tom Carter), "Anthropic Is Getting Heat for Staying Silent on Open Source AI," 27 July 2026](https://www.businessinsider.com/anthropic-open-source-ai-model-weights-criticism-2026-7).
- [CNBC (Ashley Capoot), "Anthropic CEO Dario Amodei isn't advocating open-weight model ban," 27 July 2026](https://www.cnbc.com/2026/07/27/anthropic-ceo-dario-amodei-isnt-advocating-open-weight-model-ban.html).
- [Yahoo Tech / Tom's Hardware, on the letter and Jensen Huang's first post, 24 July 2026](https://tech.yahoo.com/ai/articles/nvidia-24-other-companies-sign-183148703.html).
- [CNBC, "Chinese AI model used to analyse OpenAI cyber attack," 24 July 2026](https://www.cnbc.com/2026/07/24/chinese-ai-model-openai-cyber-attack.html).

The phrase "no undo button," widely attributed to Dario Amodei, is a journalist's formulation: his actual wording is "once weights are released they cannot be withdrawn." A longer quotation about losing the ability to revoke access and push patches, placed in quotation marks by at least one outlet, has no identifiable source and is not used here. The text of Jensen Huang's first X post comes from a search index rather than direct reading. The cybersecurity leaders' letter demanding reversal of the June directive, the 33% rise in Zhipu's shares, and the Hugging Face incident's role in founding the Open Secure AI Alliance rest on a single source and are not established. The count of 133 signatories was taken on 28 July 2026 from Microsoft's page; that list is live and continues to change.
