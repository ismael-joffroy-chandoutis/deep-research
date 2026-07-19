# The LeCun Bet

**Are world models the after-LLM, and what happens if the bubble bursts.**

*Speculative reflection, 16 June 2026. French version: [README.fr.md](README.fr.md).*

---

## The verdict in brief

> **On direction, LeCun is right: the world that comes next is one of models that understand, not models that complete text. On his method and his timeline, he is too absolute. The LLM will not disappear, it will be demoted from the throne to a component. And an economic correction is likely, one that will level nothing: it will impoverish the weakest first.**

The bet is serious and it is in Paris. What remains to be seen is whether "world model" names the future, or only the next word everyone will say to raise money.

## The thesis, plainly

In November 2025, Yann LeCun left Meta. In March 2026, his company AMI Labs raised 1.03 billion dollars at a 3.5 billion valuation, the largest seed round in European history ([TechCrunch](https://techcrunch.com/2026/03/09/yann-lecuns-ami-labs-raises-1-03-billion-to-build-world-models/)). The bet is frontally anti-LLM. For LeCun, large language models are "an off ramp on the road to human-level AI" ([X, 1 June 2024](https://x.com/ylecun/status/1796982509567180927)): they complete text out of statistical habit, with no model of the world, no plan. His answer is the JEPA-based world model: predict an abstract latent state of the world rather than pixels or tokens. The LeWM paper (arXiv:2603.19312, March 2026) is the proof of concept, a small fifteen-million-parameter model that plans in its latent space forty-eight times faster than its competitors. The field's fault line is right there: predict the abstract in order to act, against generate the visible in order to show.

## Is it the future?

The diagnosis is right, and it is no longer even contrarian. The pure LLM has plateaued, everyone sees it, starting with the labs that pile reasoning, memory, and tools on top to make up for what they lack: a persistent world. Saying that intelligence will not come out of text alone has become a given of 2026.

Where I do not follow LeCun is on his solution. His bet is the pure abstract latent, anti-generative. Two things weaken it. First, a theoretical hole acknowledged by his own supporters: applied recursively, a JEPA becomes an autoregressive model in latent space, and nothing proves that predicting a latent beats predicting a pixel ([arXiv:2507.05169](https://arxiv.org/abs/2507.05169)). Second, the empirical record: it is the generative camp that delivers the world models that work today, Genie 3, Cosmos, and above all this result that is awkward for him, "video models are zero-shot reasoners", a model like Veo that solves mazes and infers physics without being taught to ([arXiv:2509.20328](https://arxiv.org/abs/2509.20328)). In other words, pixel generation, which he declares "doomed to failure" ([X, 19 February 2024](https://x.com/ylecun/status/1759486703696318935)), already produces part of what he reserves for the latent.

My take: LeCun is right about the destination, probably wrong about the purity of the path. The future is not "latent versus generative", it is their fusion, planning in the latent and rendering in pixels. He is directionally right and specifically too dogmatic, which is exactly his history. He held on to convolutional networks twenty years before the world agreed with him, and he has also bet on specific forms that did not pan out as such. The world model will win. LeCun's world model, in this form, is less certain.

## Will the LLM disappear?

No. It will be dethroned, not deleted. The cost per token is collapsing by roughly a factor of ten per year, the language model becomes a commodity, the language and interface layer of a larger system, not the seat of intelligence. "Off ramp to AGI", perhaps; "useless technology", no. The right parallel is the database: nobody talks about it anymore, everybody has one. The wrong word is "disappear". The right one is "demoted". The mistake would be to believe one paradigm switches off another like a light. Paradigms stack, they do not replace each other.

## An AI economic crisis?

A correction is likely, and AMI is its clearest symptom. Three and a half billion in valuation for a dozen people with no product, and it is the CEO himself, Alexandre LeBrun, who warns that "in six months, every company will call itself a world model to raise funding." Add the circular financing, NVIDIA investing in its own customers to prop up demand for its chips, and you have the signature of a bubble. But two things must be separated. The technology is not a bubble, the prices and the timeline are. It is the internet in 1999: the web was real, the 1999 valuations were not. The crash did not kill the web, it killed the prices.

The trap, and this is in direct continuity with what I describe in [`souverainete-ia`](https://github.com/ismael-joffroy-chandoutis/souverainete-ia), is that a bursting bubble does not level the field, it impoverishes the weakest first. Europe, already on the edge of recession, would cut its patient capital before the others. So a crash of American AI would not be good news for the European sovereign bet, it would be its main threat. The world dreams of a correction that would punish the giants, it forgets that the small are always punished first.

## What remains

One observation, to close, that says everything. LeCun raises a billion dollars to declare that the dominant paradigm is a dead end, with the money that paradigm made rain down. AMI is funded by the rush it announces is over. It is the most lucid and the most fragile position at once.

I believe in the world that comes next. I believe that models which build themselves a world will surpass those that complete text, and even those that settle for generating a beautiful surface. On that point, LeCun sees clearly. The rest, the exact form, the date, the price of entry, is the part where we almost always get it wrong.

---

*Ismaël Joffroy Chandoutis*

*In continuity with [souverainete-ia](https://github.com/ismael-joffroy-chandoutis/souverainete-ia) and [decentralized-compute-sota](https://github.com/ismael-joffroy-chandoutis/decentralized-compute-sota). License: [CC BY-NC-ND 4.0](LICENSE.md).*
