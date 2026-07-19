**English (original). Version française : [README.fr.md](README.fr.md)**

# The Symphony and the Fortress

### Reading Xi Jinping's Shanghai AI speech from inside a working studio

*Ismaël Joffroy Chandoutis*

*July 2026*

---

On 17 July 2026, Xi Jinping walked onto the stage of the World Artificial Intelligence Conference in Shanghai and delivered the keynote himself. No Chinese head of state had ever done that. Since the conference began in 2018 the opening speech belonged to premiers and vice premiers; in 2025 it was Li Qiang. This year the general secretary took the microphone in person, in front of António Guterres, the presidents and prime ministers of Kazakhstan, Cambodia and Thailand, and delegations from more than a hundred countries. I set out to check what had actually been said and when, because the date circulating in my feeds was 18 July. The speech is from the 17th. The correction matters less than the fact: the leader of China decided that artificial intelligence now warrants his own body on stage, not a delegate's.

I make documentary films. My studio is a network of machines: some of what runs on them is American and rented, some of it is Chinese and free. This speech is, among other things, about my toolshed. So I read it the way I read any primary source for a film: first what it says, then what it does not say, then what everyone around it was doing while it was being said.

## What was said

The official title is "Joining Hands to Build a Just and Equitable System for Global AI Governance" ([full text via CGTN](https://news.cgtn.com/news/2026-07-17/Full-text-Xi-s-keynote-speech-at-the-2026-WAIC-opening-ceremony-1OQSfeoRvUs/p.html), [readout via the Ministry of Foreign Affairs](https://www.mfa.gov.cn/eng/xw/zyjh/202607/t20260717_11984910.html)). Four proposals structure it:

1. **Openness and shared innovation.** The line every wire service quoted: "A single string cannot make music, and a single tree does not make a forest. AI development should not be a solo performance by a single country but a symphony of international cooperation." The text explicitly encourages "open source, openness, collaboration and sharing."
2. **Security and controllability.** AI "should be a trusted tool for humanity," always "under human control," with laws, monitoring, early warning and emergency response. And one sharp edge inside the soft language: the call to "jointly oppose overstretching the national security concept in the field of AI and placing one country's security over that of others."
3. **Civilizational inclusiveness.** AI must not erode "the diversity of world civilizations"; it should serve exchange and mutual understanding.
4. **Solidarity and governance.** "True multilateralism," the central role of the United Nations, and capacity building for the Global South so that AI does not produce, in Xi's phrase reported by the [South China Morning Post](https://www.scmp.com/tech/policy/article/3360920/chinese-president-xi-jinping-warns-against-creating-new-historical-injustices-ai-era), "new historical injustices."

Around the four proposals, deliverables: 5,000 AI training places for developing countries over five years; access for 30 countries to MAZU, a Chinese AI meteorological early-warning system; AI application cooperation centers to be built with ASEAN, the Arab League, the African Union, CELAC, the Shanghai Cooperation Organisation and BRICS. And the centerpiece: the World Artificial Intelligence Cooperation Organization, WAICO, "has come into being in Shanghai," presented as "a major move by China to answer the call of the Global South." The founding agreement had been signed the previous day, 16 July, by 29 states ([Caixin](https://www.caixinglobal.com/2026-07-17/china-launches-shanghai-based-ai-governance-body-with-29-founding-nations-102465524.html), [The Standard](https://www.thestandard.com.hk/china/article/337474/World-AI-Cooperation-Organisation-launched-with-29-countries-signing-in-Shanghai)): Russia, Belarus, Serbia, Cuba, Venezuela, Brazil, Indonesia, Malaysia, Pakistan, South Africa, Senegal, Laos, Kazakhstan and others. No G7 member, no core EU state, no Five Eyes country signed ([Al Jazeera](https://www.aljazeera.com/news/2026/7/17/chinas-xi-jinping-launches-new-ai-alliance-what-is-it), [arXiv mapping study](https://arxiv.org/abs/2606.23860)).

Le Monde's two same-day readings frame the reception well: the official angle, a call for global cooperation on a "human-centered" AI ([Pixels](https://www.lemonde.fr/pixels/article/2026/07/17/xi-jinping-appelle-a-une-cooperation-mondiale-sur-l-ia-avec-une-approche-centree-sur-l-humain_6724134_4408996.html)), and the strategic angle, China selling an "open and accessible" counter-model against the United States ([Économie](https://www.lemonde.fr/economie/article/2026/07/17/ia-xi-jinping-vante-un-contre-modele-chinois-ouvert-et-accessible-face-aux-etats-unis_6724192_3234.html)). The second reading is the one that touches what I do every day, and it deserves the closest look.

## What was not said

The official text never names the United States. It never says the word chip. This is not restraint, it is technique. "Overstretching the national security concept" is the diplomatic name for American export controls on semiconductors; "a solo performance by a single country" is the name for the American frontier labs; "new historical injustices" reprises the vocabulary of colonialism for the age of compute. The absence of proper nouns is what lets 29 signatures happen: nobody in Jakarta or Dakar has to sign an anti-American text, only a pro-access one.

The other significant absence: no frontier-risk language of the kind that structures Western AI safety discourse. Where the American and European conversation oscillates between acceleration and extinction, Xi's security section is about control, sovereignty and social stability. Fred Gao's close reading of Xi's internal positions ([How Does Xi Jinping View AI Governance?](https://www.fredgao.com/p/how-does-xi-jinping-view-ai-governance)) notes that the domestic frame is "development first," with governance as the instrument that keeps development orderly, not as a brake.

## The subtext, layer by layer

### Open weights as foreign policy

The material fact under the speech is that China has become the default supplier of AI to anyone who cannot or will not pay for American APIs. The inflection point was DeepSeek-R1 in January 2025: reasoning quality comparable to the American frontier, weights downloadable by anyone. Since then, the flood: Qwen, Kimi, GLM, MiniMax, DeepSeek's successors. By spring 2026, one widely cited measurement had Chinese open-weight models at roughly 61 percent of tokens routed through OpenRouter, with four of the five most-used models Chinese ([Data Gravity](https://www.datagravity.dev/p/chinas-open-weight-takeover)); Alibaba's Qwen family passed a billion cumulative downloads on Hugging Face and overtook Meta's Llama as the most-forked base ([Stanford HAI had documented the ecosystem's breadth](https://hai.stanford.edu/assets/files/hai-digichina-issue-brief-beyond-deepseek-chinas-diverse-open-weight-ai-ecosystem-policy-implications.pdf) well before). The week of the speech, Moonshot released Kimi K3 to open acclaim. These numbers are proxies, not the whole market, and the strongest closed American models still lead on raw capability. But the direction is unambiguous: the open layer of the world's AI stack is becoming Chinese.

Xi's "encourage open source" line converts that industrial fact into doctrine. [Le Grand Continent](https://legrandcontinent.eu/fr/2026/07/17/la-doctrine-ai-le-plan-de-xi-jinping-pour-ruiner-la-silicon-valley/) calls the mechanism an inverted dumping: give away the weights, let anyone run, modify and integrate the models without permission or fees, and let state-adjacent capital absorb what private American investors never could. A closed model is a tap that can be shut off from San Francisco; an open-weight model, once downloaded in Nairobi or Jakarta, belongs to whoever runs it. For a government that spent a decade being cut off from technologies at another state's discretion, exporting un-cut-off-able software is not generosity. It is the weaponization of its own wound.

### Two treaties, two internets

The speech landed in the middle of an institutional race. In December 2025 the US State Department launched Pax Silica, its "flagship initiative on AI and supply chain security"; the second summit in Washington on 25 and 26 June 2026 brought the signatories to roughly 35, including the EU, Germany, Japan, South Korea, India and the United Kingdom ([State Department](https://www.state.gov/releases/office-of-the-spokesperson/2026/06/outcomes-of-the-second-pax-silica-summit)). WAICO's 29 founders and Pax Silica's 35 overlap, by the counts circulating among analysts, in exactly one country: Kazakhstan. Two clubs, two stacks, one shared member. The nonaligned space of the 20th century is being rebuilt around GPUs.

The asymmetry of the two offers is the real story. Pax Silica offers access to the American stack under American conditions: alignment on export controls, security vetting, integration into a supply chain that Washington explicitly intends to keep dominant. WAICO offers the Chinese stack with, in Beijing's words, no values test at the door: training programs, application centers, weather-warning systems, and models you can host yourself. One sells trust in the supplier; the other sells independence from any supplier, supplied by China. On 17 July, while Xi spoke about symphonies, President Trump was at a White House event accusing China of stealing American voter data ([NBC News](https://www.nbcnews.com/news/us-news/donald-trump-china-election-security-xi-jinping-ai-rcna587963), [CNN](https://www.cnn.com/2026/07/17/china/china-ai-conference-analysis-intl-hnk)). A tale of two speeches, and each one was the other's best argument.

### The chip paradox

The strangest fact of mid-2026, and the one that explains the speech's confidence, is that the chip blockade has partially inverted. The Trump administration, reportedly worried by Huawei's progress, cleared Nvidia's H200 for export to China; by 14 July a Commerce Department official told Congress that actual shipments were "trivial" despite some 10 billion dollars in approved licenses ([The Wire China](https://www.thewirechina.com/2026/07/02/nvidia-uses-the-specter-of-huawei-to-make-its-chip-exports-case/), [Tom's Hardware](https://www.tomshardware.com/tech-industry/white-house-u-turn-on-nvidia-h200-ai-accelerator-exports-down-to-huaweis-powerful-new-ascend-chips-report-claims-u-s-committed-to-dominance-of-the-american-tech-stack)). Beijing, having spent years denouncing the controls, now discourages its own champions from buying American: DeepSeek's V4, released in April, was adapted for Huawei's Ascend chips, and Huawei has been mass-producing its newest Ascend generation since March, targeting hundreds of thousands of units this year (reported figures, to be treated with the caution due to a company at war). Nvidia's own annual filing describes the company as "effectively foreclosed" from China's data center market ([Brookings](https://www.brookings.edu/articles/ball-games-over-the-us-is-out-of-the-ai-chip-market-in-china/)). The [Council on Foreign Relations](https://www.cfr.org/articles/chinas-ai-chip-deficit-why-huawei-cant-catch-nvidia-and-us-export-controls-should-remain) maintains that Huawei still cannot match Nvidia at the frontier and that the deficit is real. Both things can be true. What the controls demonstrably produced is not a Chinese collapse but a Chinese ecosystem that treats American silicon as a vulnerability to engineer away. When Xi denounces the overstretched "national security concept," he is describing the policy that built his talking point.

### The domestic signal

A first-person keynote is also a message inward. Xi appearing in person tells every ministry, province and bank where the priority sits. The speech's economic line, an "intelligent economy" whose core industries already exceed a trillion yuan, extends the AI Plus doctrine the State Council has pushed since 2025: AI integrated into manufacturing, agriculture, governance, everything, on a timetable running to 2030. Gao's reading of the internal record adds the tone: urgency, a window that will not stay open, technological self-reliance as the non-negotiable lesson of the sanctions years. The performance of serenity in Shanghai stands on a domestic apparatus that behaves as if the race were existential.

### The Global South as the prize

The offers in the speech, training places, weather systems, regional centers, are small money with precise targeting. They address states for whom the American debate about superintelligence is an abstraction and the cost of an API call is not. [Carnegie's May 2026 analysis](https://carnegieendowment.org/research/2026/05/chinas-pivot-on-global-ai) traces the pivot: from exporting infrastructure through the Digital Silk Road to exporting governance, norms and institutions, into the vacuum left by an American administration that walked out of multilateral digital bodies (the Freedom Online Coalition in January 2026, among others) and prices its technology as leverage. The BRICS states and the regional organizations named in the speech are not an afterthought; they are the constituency. WAICO's founding membership is the Digital Silk Road turned into a signature page.

## The adversarial file

Every strong claim above has a counter-file, and honesty requires assembling it.

**Openness is a tactic, not a principle.** Ten days before the speech, Reuters reported that China's Ministry of Commerce had held talks with Alibaba, ByteDance and Z.ai about restricting overseas access to their most advanced models, potentially including open-weight releases; a May gathering of legal scholars had proposed sorting models by sensitivity, with frontier systems kept domestic ([Quartz summary](https://qz.com/beijing-china-ai-model-export-restrictions-070726)). There is no draft rule and no timeline, but the direction of thought is documented: the state that preaches the symphony is privately drafting seating restrictions for its own orchestra. The generous reading is contingency planning. The cold reading is that China will stay open exactly as long as openness serves catch-up, and that the Global South's new independence-through-Chinese-weights has a clause it has not read yet.

**The talent is being locked in, not shared.** Since spring 2026, top researchers and executives at private Chinese AI firms reportedly need government approval to travel abroad, a regime previously reserved for nuclear scientists ([TechCrunch](https://techcrunch.com/2026/05/27/china-is-increasingly-keeping-its-best-ai-talent-to-itself/)). A country that treats its machine-learning researchers as strategic materiel is not describing its own behavior when it speaks of open collaboration among civilizations. Meanwhile the American side runs its own enclosure, visa friction and suspicion having measurably reduced the inflow of Chinese researchers who once powered US labs. Both fortresses are real; only one of them gave a speech about symphonies.

**The values ship with the weights.** Chinese models censor at the model layer: events, names, arguments absent from the training corpus or refused at inference. Carnegie and others warn that models embedding state-defined boundaries of the sayable are being installed as civic infrastructure across dozens of countries. The speech's third proposal, protecting "the diversity of world civilizations," reads differently from a country that operates the world's most sophisticated apparatus for narrowing its own. As a filmmaker whose material is precisely what states prefer unsaid, I take this point personally: a model that cannot discuss Tiananmen is not a neutral tool with a regrettable gap, it is an edit with a distribution network.

**WAICO may be a stage set.** Budget, decision rules, enforcement: undefined. The [arXiv mapping study](https://arxiv.org/html/2606.23860v1) is careful to call it an emerging institution whose authority is unproven. Analysts note that no state has ceded anything to it yet. The skeptical reading of 16 July is 29 signatures on a photograph.

**The energy advantage is smaller than advertised.** China generates over twice America's electricity and adds capacity faster, while roughly half of planned US data center capacity for 2026 is delayed or canceled for want of power equipment. But the [Oxford Institute for Energy Studies](https://www.oxfordenergy.org/wpcms/wp-content/uploads/2026/02/Comment-The-China-data-centre-advantage.pdf) cautions that inflexible pricing and grid rigidity shrink the Chinese edge in practice. The fortress has its own leaks.

**And the frontier is still American.** On the hardest benchmarks and the most capable closed systems, US labs lead. The gap has narrowed dramatically, to a few percentage points on standard indices by some counts, and to roughly six months in the estimate Gao attributes to the internal Chinese discussion. But narrowed is not closed, and a six-month gap at an exponential's steep section is not nothing. Xi's speech is the speech of a challenger who has decided that where you cannot yet win the race, you change what the race is about.

## What is actually at stake

Strip the ceremony and four material contests remain.

**Compute:** who can build and power the machines. China has the electricity and increasingly its own silicon; America has the best silicon and a grid that is now the binding constraint on its own expansion.

**Distribution:** whose models become the default. Closed American frontier models monetize excellence; Chinese open weights colonize ubiquity. These are different games. The first optimizes for the richest customers, the second for everyone else, and "everyone else" is most of the world.

**Talent:** both powers are walling in their researchers, one by exit permits, the other by visa hostility. The free circulation of minds that built this field is ending on both sides simultaneously.

**Norms:** whether the governance of AI is written in fora where liberal states hold a veto, or in a Shanghai-headquartered organization where they are not even members. The July split, Pax Silica against WAICO, makes the norm war institutional. It will not be won by declarations but by defaults: by which stack a health ministry in Africa or a court system in Southeast Asia happens to be running in 2030 when the question of what AI may say, remember and refuse gets settled in practice.

## Coda: the studio as border zone

I ran a Chinese open-weight model on my own hardware this morning, on a machine whose GPU is American, restricted for export to the country whose model it was running. Tonight I will pay an American lab for tokens from a closed model whose weights I will never see. My little studio is the entire conflict in miniature, and both sides would describe me as their beneficiary. Neither is doing it for me.

What I take from Shanghai is not the symphony and not the fortress, but a test I can actually apply. Openness that is a principle survives success: you keep publishing weights when you are ahead. Openness that is a tactic dies at the crossover: the Reuters report is the sound of that clause being drafted. The same test applies westward: an "open" American ecosystem that restricts, prices and vets access at every layer of the stack has already answered it. The honest summary of 17 July 2026 is that the two largest powers on earth have both concluded that intelligence is infrastructure, that infrastructure is power, and that power is not shared. Everything else was orchestration.

An artist's sovereignty, the kind I have argued for across this repository, means refusing to be the audience of either concert: own what can be owned, mirror what can be mirrored, and treat every tap, American or Chinese, as something that will one day be turned off. The weights on my disks do not care who I vote for. That is exactly why both states are so interested in which ones I download.

---

## Sources

Primary:

- [Full text of Xi Jinping's keynote, CGTN, 17 July 2026](https://news.cgtn.com/news/2026-07-17/Full-text-Xi-s-keynote-speech-at-the-2026-WAIC-opening-ceremony-1OQSfeoRvUs/p.html)
- [Ministry of Foreign Affairs readout, 17 July 2026](https://www.mfa.gov.cn/eng/xw/zyjh/202607/t20260717_11984910.html)
- [US State Department, Outcomes of the Second Pax Silica Summit, June 2026](https://www.state.gov/releases/office-of-the-spokesperson/2026/06/outcomes-of-the-second-pax-silica-summit)

Press:

- [Le Monde, Xi Jinping appelle à une coopération mondiale sur l'IA, 17 July 2026](https://www.lemonde.fr/pixels/article/2026/07/17/xi-jinping-appelle-a-une-cooperation-mondiale-sur-l-ia-avec-une-approche-centree-sur-l-humain_6724134_4408996.html)
- [Le Monde, IA : Xi Jinping vante un contre-modèle chinois ouvert et accessible, 17 July 2026](https://www.lemonde.fr/economie/article/2026/07/17/ia-xi-jinping-vante-un-contre-modele-chinois-ouvert-et-accessible-face-aux-etats-unis_6724192_3234.html)
- [South China Morning Post, Xi warns against new historical injustices, 17 July 2026](https://www.scmp.com/tech/policy/article/3360920/chinese-president-xi-jinping-warns-against-creating-new-historical-injustices-ai-era)
- [NBC News, Inside the room as Xi outlines China's global vision for AI](https://www.nbcnews.com/tech/tech-news/xi-jinping-outlines-chinas-global-vision-ai-landmark-speech-rcna587881) and [A tale of two speeches](https://www.nbcnews.com/news/us-news/donald-trump-china-election-security-xi-jinping-ai-rcna587963)
- [CNBC, Xi pitches China as AI partner to developing world, 17 July 2026](https://www.cnbc.com/2026/07/17/x-china-ai-summit-risks-security.html)
- [Fortune, Xi offers AI olive branch, 17 July 2026](https://fortune.com/2026/07/17/xi-jinping-ai-cooperation-organization-shanghai/)
- [Al Jazeera, China's Xi launches new AI alliance, 17 July 2026](https://www.aljazeera.com/news/2026/7/17/chinas-xi-jinping-launches-new-ai-alliance-what-is-it)
- [Caixin, China launches Shanghai-based AI governance body with 29 founding nations, 17 July 2026](https://www.caixinglobal.com/2026-07-17/china-launches-shanghai-based-ai-governance-body-with-29-founding-nations-102465524.html)
- [CNN, As Trump accuses China of stealing voter data, Xi pitches Beijing as a responsible tech leader, 17 July 2026](https://www.cnn.com/2026/07/17/china/china-ai-conference-analysis-intl-hnk)
- [Quartz, Beijing weighs limits on overseas access to its top AI models (Reuters report), 7 July 2026](https://qz.com/beijing-china-ai-model-export-restrictions-070726)
- [TechCrunch, China is increasingly keeping its best AI talent to itself, 27 May 2026](https://techcrunch.com/2026/05/27/china-is-increasingly-keeping-its-best-ai-talent-to-itself/)

Analysis:

- [Le Grand Continent, La doctrine AI+ : le plan de Xi Jinping pour ruiner la Silicon Valley, 17 July 2026](https://legrandcontinent.eu/fr/2026/07/17/la-doctrine-ai-le-plan-de-xi-jinping-pour-ruiner-la-silicon-valley/)
- [Carnegie Endowment, China's Pivot on Global AI, May 2026](https://carnegieendowment.org/research/2026/05/chinas-pivot-on-global-ai)
- [Council on Foreign Relations, China's AI Chip Deficit](https://www.cfr.org/articles/chinas-ai-chip-deficit-why-huawei-cant-catch-nvidia-and-us-export-controls-should-remain)
- [Brookings, The US is out of the AI chip market in China](https://www.brookings.edu/articles/ball-games-over-the-us-is-out-of-the-ai-chip-market-in-china/)
- [The Wire China, Nvidia uses the specter of Huawei, 2 July 2026](https://www.thewirechina.com/2026/07/02/nvidia-uses-the-specter-of-huawei-to-make-its-chip-exports-case/)
- [Fred Gao, How Does Xi Jinping View AI Governance?](https://www.fredgao.com/p/how-does-xi-jinping-view-ai-governance)
- [Stanford HAI DigiChina, Beyond DeepSeek: China's diverse open-weight AI ecosystem](https://hai.stanford.edu/assets/files/hai-digichina-issue-brief-beyond-deepseek-chinas-diverse-open-weight-ai-ecosystem-policy-implications.pdf)
- [Data Gravity, China's Open-Weight Takeover](https://www.datagravity.dev/p/chinas-open-weight-takeover)
- [arXiv 2606.23860, WAICO: Mapping an Emerging Institution](https://arxiv.org/abs/2606.23860)
- [Oxford Institute for Energy Studies, The China data centre advantage, February 2026](https://www.oxfordenergy.org/wpcms/wp-content/uploads/2026/02/Comment-The-China-data-centre-advantage.pdf)

Figures reported by a single outlet or without primary confirmation (Huawei Ascend production volumes, the exact Pax Silica and WAICO membership overlap, the six-month capability gap) are presented above as reported claims, not established facts.
