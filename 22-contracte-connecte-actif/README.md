**English. Version française : [README.fr.md](README.fr.md)**

# Contracted, Connected, Active

### The vocabulary of compute in 2026, and the gap between announced gigawatts and machines actually running

*Ismaël Joffroy Chandoutis*

*July 2026*

---

Public debate about AI infrastructure is saturated with unit errors. Gigawatts are added up as though they were consumption, FLOPS that measure different things are compared, Chinese 2025 figures are set against American 2024 ones. These errors are not harmless: they determine whether one believes in an imminent physical wall or in sustainable expansion.

As it happens, the industry publishes, in its own regulatory filings, the exact vocabulary needed to settle the question. It only has to be read.

## The three capacities

Nebius Group N.V., in its annual report filed with the SEC on 30 April 2026, defines not one notion of capacity but **three**:

> "**Contracted power** is capacity that has been secured by land and contracted power commitments. […] **Connected power** is capacity that has power connected into data centers; and […] **Active power** is capacity being consumed by IT equipment and available for revenue generation."

Contracted, connected, active. Three successive states which, in press releases, all go by the same name: gigawatts.

The gap between the first and the third is the most useful fact in the file. Nebius announces over 2 GW contracted in February 2026, against roughly **170 MW of active power** at 31 December 2025. A ratio of about twelve.

CoreWeave's 10-K, filed 2 March 2026, lets the calculation be redone at another company:

> "As of December 31, 2023, we operated 10 data centers with approximately 70 MW of active power. […] As of December 31, 2025, we operated 43 data centers with **over 850 MW of active power**. As of December 31, 2025, our **total contracted power capacity was approximately 3.1 GW**, which we expect to deploy over future periods."

Contracted to active: about 3.6.

Any media aggregation of "announced gigawatts" therefore overstates capacity actually in service by a factor of between three and twelve depending on the operator. This is not deception — the filings are public and precise — it is a failure of reading, and it is systematic.

The same care applies to converting power into energy. At full load over 8,760 hours a year, CoreWeave's 850 active MW cap out at 7.45 TWh per year; its 3.1 contracted GW at 27.2 TWh. These are theoretical ceilings: the real load factor is not published, and it is never one hundred percent.

## Power and energy

The debate's foundational confusion fits in a sentence one reads everywhere: "this data centre consumes one gigawatt." A gigawatt is not consumption, it is instantaneous power draw. Consumption is measured in terawatt-hours over a period.

Three further distinctions must be held throughout. Installed capacity, in nameplate gigawatts, says nothing about what is produced. Production, in terawatt-hours, never equals capacity times 8,760 hours. And peak load — the power drawn at the tightest moment — is what the grid must cover, not the average.

On the compute side, the dominant error of 2025–2026 is arithmetic in the literal sense: comparing FP4 or FP8 FLOPS to FP64 FLOPS. Recent accelerators' performance figures are published in low precisions that mechanically inflate the numbers. An "exaflop" means nothing without its precision, and without stating whether it is a theoretical peak or a sustained measurement.

## What is actually being compared when grids are compared

The most widespread claim about energy — China produces more than double American electricity — is true, but the figures circulating to support it are often heterogeneous.

China, 2025: **10,420 TWh produced**, 10,368 TWh consumed. The first country in history to exceed ten thousand terawatt-hours of annual consumption. The two numbers circulate interchangeably though they measure different things.

United States, 2025: **4,430 TWh** utility-scale, plus roughly 93 TWh of small-scale solar — which the American agency's main tables exclude, while China counts its distributed photovoltaics. Comparing without that correction distorts the result.

The figure of "4,300 TWh" for the United States, very widely cited, is **2024's**, not 2025's. Setting China 2025 against the US 2024 artificially inflates the gap. On consistent bases, the ratio is about 2.3, not 2.5.

Comparing installed capacity demands the same caution: China publishes nameplate figures and includes distributed solar; the American agency mainly publishes net summer capacity, about 7% below nameplate. The "three times" ratio one reads everywhere depends entirely on the convention chosen.

One number is more instructive than all the others: the **load factor**. China, 2025: about 30.6% across the fleet. United States: about 38.2%. The Chinese fleet is far larger and runs far less. Utilisation hours published by the China Electricity Council confirm it in detail — 4,346 hours for coal, 7,809 for nuclear, but 1,979 for wind and **1,088 for solar**. And curtailment is rising for the second consecutive year: 5.7% for wind, 5.2% for solar nationally, up to 16.6% for solar in Xinjiang.

China's energy advantage is therefore real in volume, and far more fragile in availability at the right place and time — which is precisely a compute centre's constraint, since it will not accept being curtailed.

## What the projections are worth

The International Energy Agency's *Energy and AI*, published April 2025, remains the reference. Its figures deserve quoting in full:

> "In total, electricity consumption from data centres is estimated to amount to around **415 terawatt hours (TWh)**, or about **1.5% of global electricity consumption in 2024**. It has grown at 12% per year over the last five years."

> "In the Base Case, electricity consumption from data centres rises to around **945 TWh by 2030**, more than doubling from the 2024 level."

But the agency publishes four scenarios, and the spread is what matters: **670 TWh** in *Headwinds*, **1,260 TWh** in *Lift-Off* — a factor of 1.9 between the bounds. By 2035 the range widens from 700 to 1,720 TWh.

Citing "945 TWh by 2030" without the range, which is the dominant practice, turns a confidence interval into a prophecy. The uncertainty is not a flaw in the report: it is its principal result.

The first figure also deserves holding in mind whenever a physical wall is invoked. In 2024, all the world's data centres — not only AI ones — accounted for **1.5% of global electricity consumption**. Considerable in growth, modest in level.

## The vocabulary is moving

One lexical shift is worth noting, because it is not merely cosmetic.

The industry used to say **data centre**. It increasingly says **AI factory** or **compute centre**. The shift captures something true: a building that trains models does not store data, it converts electricity into parameters. Its dimensioning constraint is no longer floor area or bandwidth but available electrical power and heat rejection. It is a factory in the literal sense: a machine for converting energy.

The split between **training** and **inference** further redistributes the problem. Training is a concentrated peak, latency-tolerant, indifferent to location — it can happen far away, where energy is cheap. Inference is diffuse, permanent, latency-sensitive, and must sit near users. That second load is what pushes toward **edge compute** and hybrid architectures, and it is the one growing fastest as usage becomes ordinary. Reasoning solely from the training cost of large models therefore misses half the question.

## Campus AI, or sovereignty in the conditional

France has its project, and it concentrates every ambiguity in the field.

**Campus AI** brings together Bpifrance, Mistral, the Emirati fund **MGX** and **NVIDIA** in a joint venture targeting up to **3 GW** of compute capacity across the country, presented as Europe's largest AI campus. The pilot site is planned at **Fouju**, in Seine-et-Marne, east of Paris. Construction is to begin in the second half of 2026, operations by 2028.

Three remarks follow directly from the above.

First, "3 GW" is a target capacity — at best *contracted* power, and at this stage not even that. On the ratios observed at Nebius and CoreWeave, active power at commissioning will be of an entirely different order. This is not a criticism of the project, it is a correct reading of its announcement.

Second, the shareholding raises questions about the word sovereignty. Capital comes partly from Abu Dhabi, hardware from NVIDIA, the model from Mistral. Across the three layers — capital, silicon, weights — one is French. That is better than none, and it is exactly Europe's position: sovereign over the layer that copies, dependent on the two that do not.

Third, the real constraint will be grid connection. In France as elsewhere, the limiting factor is no longer land or capital but connection lead times and the availability of high-voltage electrical equipment. That is why roughly half the American data centres planned for 2026 are delayed or cancelled — not for want of demand, but for want of transformers and connection slots.

## The case against

**Companies are not lying about their numbers.** Nebius and CoreWeave publish all three capacity notions in filings that carry legal liability. The gap between contracted and active is documented by the parties themselves. The problem is on the reading side, not the emitting side.

**Contracted capacity is not fictional.** It represents secured land and real supply commitments that will convert into active capacity over several years. Treating contracted gigawatts as vapour would be the symmetrical error to treating them as active. They are collateralised promises with uncertain maturities.

**China's low load factor is not only a weakness.** An oversized fleet with a great deal of intermittent renewable mechanically produces a low load factor. That is the price of a fast transition, not necessarily a symptom of inefficiency. The honest conclusion is that the advantage is harder to convert into stable supply for compute centres than it looks — not that it is illusory.

**The IEA's range is wide because the future is open.** Faulting a scenario set for having a factor of two between its bounds amounts to faulting uncertainty for existing. What is criticisable is the selective use of whichever bound suits the argument — in both directions.

## What is actually at stake

**The bottleneck has moved from silicon to copper.** For three years the question was access to accelerators. It has become access to electrical power, transformers, substations and permitting timelines. This is a domain where money accelerates almost nothing: high-voltage equipment lead times and interconnection queues cannot be paid to go faster.

**Component inflation pollutes the figures.** A significant share of the capex increases announced by hyperscalers for 2026 is memory and component inflation rather than additional capacity. Raw capex figures overstate real capacity growth — a correction rarely applied in the bubble debate.

**Metrology is a political position.** Choosing to speak in announced gigawatts rather than active megawatts, in FP4 rather than FP64, in nameplate capacity rather than load factor, is not neutral: each choice multiplies the number by a known factor, and serves an argument. Regulatory filings, by contrast, are constrained to precision. They are boring and they are accurate, which is why nobody reads them.

## What remains

The vocabulary the industry built for its own accounting needs — contracted, connected, active — is more useful to public debate than anything public debate has produced on the subject. It says that between the announcement and the running machine lie three states, several years, and a factor of three to twelve.

That does not settle whether the trajectory is sustainable. It merely moves the cursor: the physical wall discussed for two years is not yet a constraint on electricity production, it is already a constraint on grid connection and equipment. That is not the same thing, it does not call for the same responses, and it is measured on a timescale neither press releases nor quarterly cycles know how to represent.

*Continuing from parts [02](../02-sovereignty-machine/), [16](../16-le-robinet-et-la-boucle/) and [20](../20-avec-de-gros-ordinateurs/).*

---

## Sources

Primary:

- [Nebius Group N.V., Form 20-F, FY2025, filed 30 April 2026](https://www.sec.gov/Archives/edgar/data/1513845/000110465926052948/nbis-20251231x20f.htm) — definitions of contracted, connected and active power.
- [CoreWeave, Inc., Form 10-K, FY2025, filed 2 March 2026](https://www.sec.gov/Archives/edgar/data/1769628/000176962826000104/crwv-20251231.htm) — historical series of active power and contracted capacity.
- [International Energy Agency, *Energy and AI*, April 2025](https://www.iea.org/reports/energy-and-ai) — [full PDF](https://iea.blob.core.windows.net/assets/dd7c2387-2f60-4b60-8c5f-6563b6aa1e4c/EnergyandAI.pdf).
- [U.S. Energy Information Administration, *Electric Power Monthly*, Table 1.1 (published 23 July 2026)](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_1_01) and [Table 1.1.A for small-scale solar](https://www.eia.gov/electricity/monthly/epm_table_grapher.php?t=epmt_1_01_a).
- [EIA, "U.S. electricity generation in 2025 hit a record, again," 5 March 2026](https://www.eia.gov/todayinenergy/detail.php?id=67284).
- [China National Energy Administration, 2025 statistics, 17 January 2026](https://www.nea.gov.cn/20260121/715f79826488476a9162da7c8bd77c80/c.html) and [China Electricity Council, 2 February 2026](https://cec.org.cn/detail/index.html?3-353833); [official English summary](https://english.www.gov.cn/archive/statistics/202601/17/content_WS696b548ec6d00ca5f9a08a0e.html).

On Campus AI:

- [École polytechnique press release, "MGX, Bpifrance, Mistral AI and NVIDIA launch joint venture to build Europe's largest AI campus in France"](https://polytechnique.edu/en/press-room/press-releases/mgx-bpifrance-mistral-ai-and-nvidia-launch-joint-venture-build-europes-largest-ai-campus-france).
- [DataCenterDynamics, "MGX, Bpifrance, Nvidia and Mistral AI plan 1.4GW Paris data center campus"](https://www.datacenterdynamics.com/en/news/mgx-bpifrance-nvidia-and-mistral-ai-plan-14gw-paris-data-center-campus/).
- [L'Usine digitale, on the project's acceleration to 3 GW](https://www.usine-digitale.fr/intelligence-artificielle/ia-generative/jusqua-3-gw-de-capacite-de-calcul-un-an-apres-le-projet-de-campus-ia-soutenu-par-bpifrance-mistral-ai-et-nvidia-saccelere.DKSA2S2V6NACDO5LFZMIYBJB5Y.html).

Hyperscaler capex figures cited here come from compilations of SEC filings rather than the filings themselves. Chinese curtailment and utilisation-hour data come from a Chinese planning centre relayed through a third-party summary, not the original publication. Power-to-energy conversions are theoretical ceilings at full load: no operator publishes its real load factor, so actual consumption is necessarily lower by an unknown margin. Campus AI's timeline and capacity are targets announced by the project's backers, at a date when no construction has begun.
