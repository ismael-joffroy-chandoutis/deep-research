# NVIDIA and Huawei: The Two Chip Empires — the Private Central Banker and the State Champion

> Documented research report. Written June 5, 2026. Sources at the end of the document.
> Part 23: Part 16 placed NVIDIA within the material layer. This part goes into the mechanics: the **circular financing** that makes NVIDIA the financial guarantor of the entire industry (the "mafia with credit lines everywhere" question), its double game between Washington and Beijing, and its Chinese mirror, Huawei, the only actor in the world that single-handedly does what America distributes among NVIDIA, Apple, Google, OpenAI and Palantir.
> Key claims verified through adversarial counter-research (corrections incorporated, see methodological notes).

---

## Table of contents
1. [The NVIDIA web: anatomy of circular financing](#1-the-nvidia-web-anatomy-of-circular-financing)
2. [GPU-backed debt: the hidden leverage](#2-gpu-backed-debt-the-hidden-leverage)
3. [Burry, Cisco and the bubble debate](#3-burry-cisco-and-the-bubble-debate)
4. [The grip: CUDA, the kingmaker, the "fiction of competition"](#4-the-grip-cuda-the-kingmaker-the-fiction-of-competition)
5. [The China double game: from 95% to evacuation](#5-the-china-double-game-from-95-to-evacuation)
6. [Huawei: the full-stack counter-empire](#6-huawei-the-full-stack-counter-empire)
7. [Verdict: two architectures of the same power](#7-verdict-two-architectures-of-the-same-power)
8. [Sources](#8-sources)

---

## 1. The NVIDIA web: anatomy of circular financing

**The OpenAI textbook case.** September 22, 2025: NVIDIA announces a letter of intent to invest "up to $100B" in OpenAI, in tranches tied to the deployment of 10 GW of... NVIDIA systems. OpenAI CFO Sarah Friar acknowledges that most of the money will flow back to NVIDIA. What followed is instructive: the November 10-Q warns that "there can be no assurance that we will enter into definitive agreements"; in March 2026, Huang admits the $100B is "probably not in the cards." Final reality: **~$30B in equity** (reported by the press, not confirmed by the parties) in OpenAI's $110B round (closed at $852B post-money, March 2026). The "biggest investment in history" was first and foremost an announcement, one that propped up share prices on both sides for six months.

**The general mechanism.** NVIDIA committed **more than $40B in AI equity stakes over the first four months of 2026** ($17.5B in FY2026 into private companies and infrastructure funds), participated in ~70 VC deals in 2025 (vs. 54 in 2024). The web: OpenAI, CoreWeave ($2B), xAI (~$2B via an SPV), Mistral, AMI Labs (LeCun, Part 18), and dozens of others. The typical loop: NVIDIA invests in X → X buys NVIDIA GPUs → NVIDIA's revenue rises → its market cap finances the next investment.

**Better still: NVIDIA guarantees its customers' revenues.** A promise to buy back CoreWeave's unsold capacity for **$6.3B** (a backstop running through 2032); an equivalent $1.5B deal with Lambda; for xAI, an SPV buys the GPUs and leases them over 5 years, unlocking >$20B of infrastructure *off balance sheet*. Jay Goldberg (Seaport) sums up the function: an NVIDIA stake is "like asking your parents to co-sign your mortgage", it takes a buyer's cost of debt from ~15% down to 6-9% (near-Microsoft rates). NVIDIA is no longer a supplier: it is a **financial guarantor**, and the key metric does not publicly exist, there is *no disclosed figure* for the % of NVIDIA revenue coming from entities it finances. That is precisely the critics' central charge: without SEC-level disclosure, organic demand cannot be separated from round-tripping.

**Concentration in figures** (10-Q, quarter ended October 2025): 4 direct customers = **61% of revenue** (22+15+13+11%); data center = 92% of revenue; the largest customer owes ~$9.6B in receivables. On the other side: Bank of America calculates that hyperscaler capex consumes 94% of their operating cash flows after dividends/buybacks, and that AI services generate ~$25B in direct revenue, i.e. **~4% of what is being spent on infrastructure**. Goldman models ~$7.6 trillion of 2026-2031 capex with 75% going to compute. Daron Acemoglu (MIT): "house of cards."

## 2. GPU-backed debt: the hidden leverage

The layer the general public does not see: **more than $20B in loans collateralized by GPUs** by late 2025. CoreWeave: $21.6B in total debt (10-K), first investment-grade GPU facility ($8.5B, March 2026, non-recourse). Lambda: first GPU-backed ABS (securitization), $500M. Fluidstack: up to $10B via Macquarie. Lenders: BlackRock, Blackstone, PIMCO, Carlyle, JP Morgan (press attribution, medium confidence).

The structural risk is arithmetic: H100 rental prices fell from $7-10/h in early 2024 to **$2-4/h by late 2025** (-50 to -70%), while debt principal stays fixed. And GPU accounting lifespans diverge: Amazon *shortened* its from 6 to 5 years (a $920M accelerated depreciation charge) while CoreWeave, Microsoft and Alphabet maintain 6 years. If the real lifespan is Burry's (2-3 years), a wave of write-downs awaits the sector, the "GPU debt cliff" is not a date but a cluster of risks (refinancing + depreciation + Blackwell→Rubin upgrade cadence) hanging on compute demand.

## 3. Burry, Cisco and the bubble debate

- **November 2025**: Michael Burry (the "Big Short") takes >$1B in notional puts on NVIDIA and Palantir, then de-registers his fund. His line: "once again there is a Cisco at the center of it all… Its name is Nvidia." Reference: Cisco, ~$560B market cap at the 2000 peak, -80% afterwards, even though the internet itself was real. His technical argument: the real lifespan of GPUs is **2-3 years** (not the 4-6 declared), so depreciation is massively understated.
- **The exact historical analogy**: during the telecom bubble, Nortel/Lucent/Cisco lent to their customers to buy their own equipment; on the eve of 2001, that vendor financing exceeded 10% of annual revenue. The structure is repeating, equity investments, backstops, SPVs, at a larger scale.
- **The pushback**: NVIDIA sent a **7-page memo to analysts** naming "Michael Burry on Twitter/X," rejecting "circular financing" (investments = a "tiny percentage" of revenue). A $5 trillion company responding by name to a tweet is measuring its own exposure to the narrative.
- **The honest caveats**: NVIDIA has real free cash flow (~$97B/year) and 90% market share, Cisco is an analogy of *structure* (vendor financing, concentration), not an equivalence of *fragility*. Burry is a permabear (wrong on the market for years). Stacy Rasgon (Bernstein) deems the circularity "legitimate and not limited to NVIDIA." And the exit signals are real: in Q3 2025, **Peter Thiel sold his entire NVIDIA position** (~40% of his portfolio) and SoftBank sold its whole stake ($5.83B), to finance... OpenAI. The insiders of this dossier (Part 2) are exiting the silicon to enter the end-customer's debt.

## 4. The grip: CUDA, the kingmaker, the "fiction of competition"

- **The moat is not the silicon, it's CUDA**: 19 years of software ecosystem (cuDNN, NCCL, PyTorch optimization), 4M+ developers, 40,000+ companies. That is what the investigations target: raids by the French Autorité de la concurrence (Sept. 2023, CUDA flagged as a "concern," possible fine up to 10% of global revenue), reported DOJ subpoenas (2024, contested by NVIDIA), and China's SAMR preliminarily finding a violation of the anti-monopoly law (Sept. 2025, Mellanox file).
- **Groq, the limit case**: December 2025, NVIDIA absorbs Groq's assets (the inference competitor) for a reported ~$20B, via a **non-exclusive license** that recovers founder Jonathan Ross and ~90% of the engineers *without a formal acquisition*, hence without antitrust review. Stacy Rasgon: "the fiction of competition." The Warren-Wyden-Blumenthal letter (February 2026) targets exactly this mechanism (along with Meta-Scale and Google-Windsurf, Part 21): concentration reconfigures itself faster than the law.
- **The "kingmaker"**: NVIDIA captures ~90% of accelerator spending and decides, through its allocations (who gets GPUs, who gets capital, who gets a backstop), who exists in the AI economy. An "NVIDIA mafia" of former employees is spawning startups (74 companies tracked) but remains embryonic compared to the PayPal mafia (Part 2), single source, to be monitored.

## 5. The China double game: from 95% to evacuation

Jensen Huang's trajectory on China is the dossier's most instructive on US-China ambiguity:

1. **April 2025**: new H20 controls → a $4.5-5.5B charge. Huang publicly calls the export controls a "**failure**": NVIDIA's market share in China went "from 95% to 50% in 4 years," the controls subsidized Chinese autonomy. (This is the anti-Amodei thesis, Part 20: "mortgaging our future", the two men embody the two poles of the debate.)
2. **July 2025**: Trump authorizes resumed H20 sales in exchange for an unprecedented arrangement: **15% of Chinese H20 revenue remitted to the US government**, an "expectation" never codified into regulation (per CFO Kress). The state as de facto shareholder of a private company's exports: an unidentified legal object, at the heart of the "political capitalism" documented in Part 17.
3. **September 2025**: Beijing strikes back, the CAC bans major Chinese platforms from buying NVIDIA (RTX Pro 6000D, H20). China itself closes the market Washington was reopening.
4. **May 2026**: Huang capitulates, NVIDIA has "largely conceded" the Chinese market to Huawei ("we've evacuated that market"), "expect nothing." Meanwhile, the Warren/Banks letter (May 2025) against his Shanghai R&D center documented the other side: "Huang has spent the year lobbying the President to sell advanced chips to China."

Bottom line: Huang played Washington and Beijing simultaneously, lost both bets, and the final decision was made neither by him nor by the market, but by the two states. The Chinese market ("a $50B opportunity") became Huawei's exclusive territory, which was precisely the scenario both administrations claimed to be preventing.

## 6. Huawei: the full-stack counter-empire

**Resilience as established fact.** Entity List in May 2019; in August 2023, the Mate 60 Pro ships with a 7nm chip fabbed by SMIC *without EUV* (DUV multi-patterning, confirmed by TechInsights teardown), launched during Gina Raimondo's visit. More than 13,000 components replaced, 4,000 circuit boards redesigned. 2024 revenue: 862B yuan (+22.4%, near-record), R&D at 20.8% of revenue. The sanctions' "boomerang effect" is quantified (ITIF, a pro-free-trade think tank, to be weighted): ≥$33B in lost sales for US suppliers. But the retrenchment is real too: 71% of revenue now comes from China (vs. ~60% in 2019).

**AI by brute force.** The CloudMatrix 384 (384 Ascend 910C NPUs, 100% optical interconnect) beats NVIDIA's GB200 NVL72 in raw power (~300 vs ~180 PFLOPs BF16)... while consuming **4× more** (559 vs 145 kW), 2.3× less efficient per watt. The strategy is assumed and rational: no access to leading-edge → compensate through system scaling, in a country where electricity is abundant and *falling* ($90.7 → $56/MWh, 2022-2025). The exact inverse of the NVIDIA model (per-chip efficiency). Roadmap: 910C (~H100 level) → 950/960/970, targeting 4 ZettaFLOPS FP4 by 2028 through clusters (SuperCluster >500,000 NPUs). 2026 production: ~600,000 910C units targeted, real bottleneck: domestic HBM (CXMT, covering ~250-300k packages), with the TSMC die bank (2.9M dies obtained via Sophgo before detection, TSMC was fined $1B) now exhausted.

**Full-stack as global singularity.** Huawei is the only actor on the planet covering: chip (Ascend/Kirin) → proprietary memory (HiBL/HiZQ) → framework (MindSpore/CANN, **open-sourced in late 2025 to attack the CUDA moat**) → models (Pangu) → OS (**HarmonyOS NEXT**, the first OS without a single line of Android, ~1B devices, 18% of the Chinese market) → cloud → telecom equipment (world No. 1, 34%). The open-sourcing is not philanthropy: it is hardware-based monetization and the training of Global South developers on the Ascend ecosystem.

**Export and surveillance.** "Ascend diplomacy" versus H20 diplomacy: 4 data centers in Saudi Arabia (including NEOM, cited at $17B, single source, caution), the Arabic model AceGPT, cloud offerings to Brazil and Turkey. US response (May 13, 2025): BIS declares that using Ascend chips "anywhere in the world" violates the EAR, total extraterritoriality. The surveillance legacy is documented (73 "Safe City" agreements in 52 countries, CSIS; technology used to track Bobi Wine in Uganda, WSJ; facial-recognition interoperability tested with Megvii for Xinjiang, IPVM) with a factual nuance: it is Hikvision, not Huawei, that the US sanctioned on human rights grounds. The infrastructure role is attested; "the Chinese Palantir" would be inaccurate.

**Who owns Huawei?** A legally undecidable question (Balding & Clarke, 2019): 96,768 employee-shareholders via a trade-union committee that has never disclosed its members; Ren Zhengfei (ex-PLA) holds ~1.2% with veto power. Neither proof of state control, nor transparency sufficient to rule it out, the most refined reading (Journal of Corporate Law Studies): a "strange" structure born of survival mechanisms within a state ecosystem. What is certain: since the CAC directive of September 2025, **the state creates the captive market**, Huawei no longer needs performance parity, demand is administered. That is the signature of the state champion.

## 7. Verdict: two architectures of the same power

| | NVIDIA | Huawei |
|---|---|---|
| **Nature** | Dominant supplier turned **private credit system** (equity, backstops, SPVs, guarantees) | **Vertically integrated national champion**, full-stack |
| **Moat** | CUDA (software, 19 years) | Total integration + the state's captive market |
| **Chip strategy** | Per-chip efficiency | Brute force by system (4× the watts) |
| **Relation to the state** | Negotiates with two states, loses to both; 15% toll to Washington | Indistinguishable from the state in the domestic market; armed wing of "Ascend diplomacy" |
| **Systemic risk** | 61% of revenue on 4 customers; the sector's entire GPU debt converges on it | Unknown SMIC yields, HBM bottleneck, unpublished profitability |
| **If the bubble bursts** | First point of impact (Burry: the Cisco of the cycle) | Cushioned by the state, cannot "burst," only cost |

**Three conclusions for the dossier:**
1. **"A mafia with credit lines everywhere" is a sound intuition, to be requalified**: the exact term is generalized *vendor financing* plus *systemic credit guarantee*. It is not illegal; it is undisclosed. NVIDIA has become the de facto central bank of the AI economy, it sets access to compute (the currency), co-signs the ecosystem's debt, and supports the price of its own assets. A private central bank, pro-cyclical, and not regulated as one.
2. **The China ambiguity was not duplicity, it was a class position**: Huang rationally defended NVIDIA's interest (sell everywhere) against the two nationalisms. His defeat (the May 2026 evacuation) marks the end of the illusion of a global chip market: there are now two empires, two stacks, two zones, exactly the "technodiversity" by the worst that Yuk Hui feared (Part 19).
3. **Huawei is the mirror, not the clone**: where America has a fragmented oligopoly (NVIDIA + hyperscalers + labs + Palantir) bound by cross-shareholdings, China has a single integrated body backed by the state. Part 15 posed "state techno-authoritarianism vs oligarchic technofascism"; the silicon layer is its material demonstration. And the two structures converge on one point: in both cases, the citizen-user has no purchase on the infrastructure that computes them.

---

## 8. Sources

**Circular NVIDIA**
- [Fortune, circular financing](https://fortune.com/2025/09/28/nvidia-openai-circular-financing-ai-bubble/) · [OpenAI, partnership](https://openai.com/index/openai-nvidia-systems-partnership) · [TechTimes, $100B→$30B](https://www.techtimes.com/articles/317839/20260605/nvidia-openai-investment-shrinks-100b-30b-compute-lock-war-continues.htm) · [CNBC, $40B equity 2026](https://www.cnbc.com/2026/05/09/nvidia-embraces-ai-investor-topping-40-billion-in-equity-bets-2026.html) · [Techi, GPU debt cliff](https://www.techi.com/nvidia-stock-gpu-debt-cliff-blackwell-rubin/) · [Dave Friedman, neoclouds $20B](https://davefriedman.substack.com/p/neoclouds-hold-more-than-20-billion) · [SEC, CoreWeave 8-K](https://www.sec.gov/Archives/edgar/data/0001769628/000176962826000236/ex9912.htm) · [Fortune, Burry/Cisco](https://fortune.com/2025/11/24/big-short-investor-michael-burry-nvidia-cisco-ai-bubble/) · [CNBC, anti-Burry memo](https://www.cnbc.com/2025/11/25/nvidia-pushes-back-on-charges-that-ai-investment-is-a-bubble.html) · [NVIDIA 10-Q, customer concentration](https://www.sec.gov/Archives/edgar/data/0001045810/000104581025000230/nvda-20251026.htm) · [NBC, BofA 4%, Acemoglu](https://www.nbcnews.com/news/rcna234806) · [Goldman, tracking trillions](https://www.goldmansachs.com/insights/articles/tracking-trillions) · [CNBC, Groq](https://www.cnbc.com/2025/12/24/nvidia-buying-ai-chip-startup-groq) · [DCD, France raids](https://www.datacenterdynamics.com/en/news/nvidias-french-offices-raided) · [Jurist, SAMR](https://www.jurist.org/news/2025/09/china-finds-nvidia-violated-antimonopoly-law-in-preliminary-probe/) · [Fortune, Thiel sells](https://fortune.com/2026/03/10/peter-thiel-nvidia-shares-sold)

**NVIDIA-China**
- [CNBC, Huang "failure"](https://www.cnbc.com/2025/05/22/nvidias-jensen-huang) · [CNBC, H20 resumption/15%](https://www.cnbc.com/2025/07/15/) · [Warren/Banks letter (PDF)](https://www.banking.senate.gov/imo/media/doc/20250528bankswarrenlettertonvidiaonshanghairesearchdevcenter.pdf) · [TechCrunch, CAC bans NVIDIA](https://techcrunch.com/2025/09/17) · [CNBC, "we've evacuated that market"](https://www.cnbc.com/2026/05/21/nvidia-jensen-huang-china-ai-chip-market-huawei.html)

**Huawei**
- [TechInsights, Kirin 9000s teardown](https://www.techinsights.com/blog/smic-7nm-n2-huawei-mate-60-pro-uncovering-innovation-inside-chip) · [ITIF, Backfire](https://itif.org/publications/2025/10/27/backfire-export-controls-helped-huawei-and-hurt-us-firms/) · [CNBC, 2024 revenue](https://www.cnbc.com/2025/03/31/huawei-2024-revenue-surges-to-near-record-high-on-smartphone-comeback.html) · [Tom's Hardware, CloudMatrix brute force](https://www.tomshardware.com/tech-industry/artificial-intelligence/huaweis-new-ai-cloudmatrix-cluster-beats-nvidias-gb200-by-brute-force-uses-4x-the-power) · [Tom's Hardware, Ascend roadmap](https://www.tomshardware.com/tech-industry/artificial-intelligence/huawei-ascend-npu-roadmap-examined-company-targets-4-zettaflops-fp4-performance-by-2028-amid-manufacturing-constraints) · [SemiAnalysis, production ramp](https://newsletter.semianalysis.com/p/huawei-ascend-production-ramp) · [AI News, open source stack](https://www.artificialintelligence-news.com/news/huawei-open-source-ai-development-platform-technical-specs/) · [Wikipedia, HarmonyOS NEXT](https://en.wikipedia.org/wiki/HarmonyOS_NEXT) · [CSIS, Safe Cities](https://www.csis.org/analysis/watching-huaweis-safe-cities) · [QZ, surveillance in Africa](https://qz.com/africa/1822312/huaweis-surveillance-tech-in-africa-worries-activists) · [SCMP, Ascend exports to Middle East](https://www.scmp.com/tech/big-tech/article/3317966/huawei-eyes-export-of-ai-chips-to-middle-east-southeast-asia-to-rival-nvidia) · [Bloomberg, BIS worldwide rule](https://www.bloomberg.com/news/articles/2025-05-13/us-warns-that-using-huawei-ai-chip-anywhere-breaks-its-rules) · [ChinaFile, Who Owns Huawei?](https://www.chinafile.com/reporting-opinion/viewpoint/who-owns-huawei)

### Methodological notes
Adversarial verification, corrections incorporated: NVIDIA-OpenAI $30B / Groq ~$20B / Meta-Scale $14.3B = amounts reported by the press, not confirmed by the parties; GPU lifespan per Burry = **2-3 years** (not 2.5-3.5); Beijing's anti-NVIDIA directive confirmed (CAC, Sept. 17, 2025); "Huang evacuates the market" confirmed (May 21, 2026). Structurally missing metric: no public figure for the % of NVIDIA revenue coming from entities it finances.

### See also
[Part 2, Thiel/PayPal mafia](./peter-thiel-paypal-mafia.md) · [Part 15, China](./chine-ia-autre-modele.md) · [Part 16, The material empire](./empire-materiel-sud-global-compute.md) · [Part 17, The natsec bridge](./pont-natsec-doomers-faucons.md) · [Part 22, AI, ecology, nuclear](./ia-ecologie-limites-nucleaire.md)
