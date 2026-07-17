# The Sovereignty Machine: On Building Local AI Infrastructure

*By Ismaël Joffroy Chandoutis — April 2026*

---

I spend $600 a day on Claude Code when I exceed my plan. Some days more. I have spent over $3,000 on Anthropic's API in the past few weeks, on top of two Max subscriptions and two Pro subscriptions across different accounts. I am a documentary filmmaker who writes scenarios, prototypes apps, and builds visual effects by talking to a machine. The machine is good. The bill is absurd.

So I started asking a question that a lot of people in my position are asking: **can I build something local that does the same thing?**

This essay is the honest answer. Not the Reddit answer. Not the "just run Ollama" answer. The real, costed, politically uncomfortable answer.

---

## What I Actually Need

Let me be specific about what I use Claude Code for, because "AI coding" means nothing without context.

I write film scenarios through iterative dialogue with an AI that reads my entire project. I prototype apps and games in what people call "vibe coding" — I describe what I want, the AI writes it, I react, it adjusts. I run 40+ specialized agents that manage different aspects of my filmmaking practice: research, funding applications, VFX pipeline, email drafting. I do this for 8 to 12 hours a day.

The critical features I need: long context (hundreds of thousands of tokens of project files loaded simultaneously), strong reasoning (multi-step planning, self-correction), agentic capability (the AI reads files, edits them, runs commands, iterates autonomously for hours). And speed. I need it to feel like a conversation, not a loading screen.

Claude Opus 4.6 with 1M context through Claude Code currently does all of this. Nothing else I have tried comes close. That is the honest starting point.

---

## The Hardware I Already Own

Two RTX 5090 (32 GB each). One RTX 4090 (24 GB). One RTX 3060 (12 GB). An ASUS ProArt X870E-Creator motherboard with a Ryzen 9 9950X. 96 GB of DDR5-6000 RAM. Two 8 TB PCIe 5.0 SSDs. Several HP server power supplies from a past life. A MacBook Air M3 and Mac Mini M4 for everything else.

The total VRAM across the NVIDIA cards is about 100 GB. The question is whether this is enough, what I need to add, and whether the result will actually feel like Claude Code or just look like it on paper.

---

## The Model Landscape (April 2026, Honest Version)

The Deep Research thread I ran before writing this essay confidently stated that GLM-5.1 was "released on April 7, 2026" with 744 billion parameters and MIT open weights. A fact-check confirms this is real: GLM-5.1 by Zhipu AI (now Z.ai) does exist on Hugging Face, with 744B parameters (40B active), 200K context, and a MIT license. It topped SWE-Bench Pro at 58.4%, ahead of GPT-5.4 and Claude Opus 4.6 on that specific benchmark.

But here is what the thread got catastrophically wrong: it claimed I could run this model at 80-150 tokens per second on 4× RTX 5090. I cannot. A 744B MoE model, even with only 40B active parameters, requires the full weight set in memory for expert routing. At FP4, that is roughly 350 GB minimum. My 128 GB of VRAM (even with four 5090s) is not enough. The model spills to system RAM, speed drops to 1-2 tokens per second, and the experience becomes unusable. This is datacenter territory: 8× B200 or H100. The thread's confidence was inversely proportional to its accuracy.

What is actually available and verified as of early April 2026:

**DeepSeek V3** (671B MoE, ~37B active) remains the strongest open-weights model for coding tasks. It runs well on multi-GPU consumer setups in quantized formats. DeepSeek V4 has been "imminent" for weeks. It may arrive tomorrow or next month.

**Qwen 3** series offers strong models up to 235B with excellent coding performance, but the largest and best variants are API-only.

**Llama 4** (Meta) has expanded the open-weights frontier significantly, though the community reception has been mixed on the largest variants.

The honest gap: the best open models in April 2026 reach roughly 85-90% of Claude Opus 4.6 on coding benchmarks — about 10-15 percentage points lower on standardized evaluations, and the gap widens in practice on real-world multi-file agentic tasks.

But here is what Farocki would ask: 85% of what? Measured by whom? SWE-Bench, the benchmark everyone cites, is itself an operational image — a measurement tool produced by the same infrastructure it claims to evaluate. NVIDIA publishes benchmarks showing its quantization is "near-lossless." Anthropic publishes benchmarks showing Claude is best. Open-source advocates publish benchmarks showing the gap is closing. Each measurement serves the measurer. I do not have a benchmark for what I actually do, which is sit in a terminal at two in the morning trying to get a film funding application to sound less like a machine wrote it.

---

## The Quantization Question

NVIDIA's Blackwell architecture (RTX 5090) supports NVFP4 natively — 4-bit floating point inference accelerated in hardware. The promise: run models at a fraction of the memory cost with minimal quality loss.

The reality is more nuanced than the marketing. NVFP4 and FP8 quantization work well for many tasks, with measured quality loss of 2-5% on standard benchmarks compared to full precision. For creative writing and scenario iteration, this is usually acceptable. For complex multi-step reasoning where errors compound, the loss can matter more than benchmarks suggest. A 3% error rate per step becomes significant over a 20-step agentic chain.

The practical math for my setup: a 671B MoE model (like DeepSeek V3) with ~37B active parameters, quantized to FP4, needs roughly 40-60 GB of VRAM for the model weights plus additional memory for the KV cache (which grows with context length). My 100 GB of VRAM (2×5090 + 4090 + 3060) can handle this. But 200K+ context with full KV cache pages into system RAM, and that is where my 96 GB becomes the bottleneck.

This is why I need to push to 192 GB RAM (4×48 GB DDR5). Not 256 GB — the marginal return is not worth the cost. 192 GB gives comfortable room for KV cache paging on long sessions without disk swap.

---

## The Speed Question

The Deep Research thread claimed "80-150+ tokens/s" for local inference on 3-4 RTX 5090s. This is where models that do not fit in VRAM meet reality:

- **A single RTX 5090** runs 32B models at ~45 tokens/s. Usable.
- **A 70B model** that spills to system RAM: **1-2 tokens/s**. Unusable.
- **A 700B+ MoE** on 4× RTX 5090 (128 GB VRAM): the model does not fit. Expert routing requires the full weight set. You are in offload territory. Speed collapses.
- **Smaller models (30-70B)** on a single 5090: 80-150+ tokens/s — this is where the optimistic numbers in the thread came from, applied to the wrong model class

For comparison, Claude Opus 4.6 through the API typically delivers 40-80 tokens/s with near-instant first-token response, backed by massive distributed infrastructure that no personal rig can match.

The honest feeling: local inference on a strong multi-GPU setup is usable for interactive work. It is not as fast as the API. The tradeoff is speed for sovereignty, rate limits for freedom, cost per token for a fixed monthly electricity bill.

---

## The Agentic Gap

Here is where the dream collides with reality. Running a model locally is one thing. Replicating the Claude Code experience is another.

Claude Code is not just a model. It is an orchestration system: file management, terminal access, git integration, multi-tool coordination, context window management, permission systems, error recovery, and a finely tuned interaction loop between the model and the developer. The model is the engine, but Claude Code is the car.

The open-source alternatives:

**Aider** is excellent for git-native coding. It understands diffs, makes targeted edits, handles large codebases. But its agentic capability (autonomous multi-step work) is limited compared to Claude Code's agent mode.

**Cline** (VS Code extension) is closer to the Claude Code experience: plan mode, MCP tool support, terminal integration. It works with local models via API endpoints. But it was designed for cloud APIs, and the quality of its output depends heavily on the underlying model. With a model that is 85% as good as Opus, you get an experience that is noticeably rougher around the edges.

**OpenHands** and **SWE-agent** are powerful for automated software engineering tasks but less suited for the creative, iterative, conversational workflow I need for scenario writing and vibe coding.

The gap I cannot close today: Claude Code's orchestration + Opus 4.6's reasoning + 1M context + the speed of cloud infrastructure. I can approximate each piece. I cannot match the combination. Yet.

---

## The Real Cost Analysis

Let me do the math honestly, because the Deep Research thread's "break-even in a few days" claim skipped too many steps.

### Current API spending

- 2× Claude Max subscriptions: $400/month
- 2× Claude Pro subscriptions: $40/month  
- API overages (Claude Code heavy usage): $3,000+ in recent weeks, trending toward $2,000-5,000/month
- **Total: roughly $2,500-5,500/month** (variable, depending on intensity)

### Local rig upgrade cost

- 2× RTX 5090 (to replace 4090 + 3060 with homogeneous setup): ~€6,500-8,000
- Minus RTX 4090 resale: ~€1,200-1,800
- 1× kit 2×48 GB DDR5-6000 CL30: ~€1,450-1,600
- 1× ASRock X870E Taichi Creator motherboard: ~€550-650
- Misc (cabling, PSU adapter, airflow): ~€200
- **Net total: roughly €7,000-9,000** (within €10K cash budget)

### Monthly operating cost (local)

- Electricity (3-4 GPUs, 8h/day intensive, 0.195 €/kWh France): €40-80/month
- Maintenance and occasional hardware replacement: €50/month amortized
- **Total: roughly €100-130/month**

### Break-even

At $3,000/month API spending → break-even in 2.5-3 months.
At $5,000/month API spending → break-even in 1.5-2 months.
At $600/day overage rate → the rig pays for itself faster than you can build it.

I need to stop here.

I have been writing this section as if the problem were an optimization puzzle. It is not. A filmmaker should not need to spend $600 a day to think with a machine, or else build a $10K rig from components mined in the DRC. This is not a challenge to be solved. It is a condition to be named. The market has arranged things so that creative access to frontier AI is either ruinously expensive or requires significant capital investment in hardware produced through exploitation. Those are not options. They are the walls of a corridor.

And yet I am in the corridor. And the spreadsheet continues.

This assumes the local experience fully replaces the API. It will not. Not yet. I will likely keep at least one Claude subscription for the tasks where Opus's reasoning and Claude Code's orchestration are irreplaceable. The realistic savings are 60-80% of my current bill, not 100%.

---

## The Sovereignty Paradox

I started this investigation wanting to "free myself from Anthropic." But building a local rig does not free you from dependency. It shifts it.

My local setup depends on NVIDIA. Not just the hardware — the entire software stack. CUDA is proprietary. TensorRT is proprietary. The NVFP4 quantization that makes large models fit on consumer GPUs is a proprietary optimization. NVIDIA's drivers are closed source. If NVIDIA decides to change licensing terms, deprecate consumer GPU inference support, or simply raise prices, I have no recourse. I have traded one vendor for another.

The open-weights models I would run were trained on data scraped from the internet without consent, filtered by underpaid contractors, computed on hardware that consumed more electricity than some small countries. My RTX 5090s contain cobalt mined in conditions I would rather not describe. The DDR5 RAM I want to add was manufactured in fabs that use millions of gallons of ultrapure water per day.

Sovereignty is a spectrum, not a binary. Running locally gives me: no rate limits, no content filtering, no monthly bill that scales with usage, no dependency on a single company's API uptime. It does not give me: independence from supply chains, freedom from NVIDIA's ecosystem, or clean hands.

There is another absence in this essay that I have been avoiding. I have spent 4,000 words on VRAM and quantization and break-even timelines, and not one sentence about what comes out the other end. What do my 40 agents produce? For whom? The scenarios I write through "vibe coding" are generated by models trained on scraped data, on writing that was never compensated, on images taken without consent. Moving the computation from Anthropic's servers to my apartment in Paris does not change the provenance of the training data. It changes the electricity bill. The extraction happened upstream, and it already happened.

The weights are open. The labor history is not. Who cleaned those datasets? Who annotated them? Whose faces, whose words, whose styles are encoded in the weights I plan to run on my sovereign machine? Self-hosting does not make that labor visible. It makes it easier to forget, because now the machine is mine and it sits in my room and it feels like autonomy.

I am a documentary filmmaker. I should know better than to believe in clean narratives.

---

## The Motherboard Problem (A Practical Interlude)

For those interested in the physical reality of multi-GPU builds:

My ASUS ProArt X870E-Creator WiFi has three PCIe slots: two CPU-connected (PCIe 5.0 x16, splittable to x8/x8) and one chipset-connected (PCIe 4.0, only x4 effective lanes). The RTX 5090 is physically massive — most AIB models occupy 3 to 3.5 expansion slots. One card in slot 1 blocks slot 2. This is not a software problem. It is a geometry problem.

Options:
- **PCIe risers** (like crypto miners used in 2017): work but add instability on Gen5, especially for long inference sessions
- **Change motherboard** to one with better slot spacing (ASRock X870E Taichi Creator): ~€550-650, solves the problem cleanly
- **Threadripper platform** (TRX50): 64-128 PCIe lanes, proper multi-GPU support, but expensive (~€2,000-3,000 for mobo + CPU)

The pragmatic choice: change the motherboard. It costs less than a riser and eliminates the most common source of instability.

You can combine HP server power supplies with a standard ATX PSU using a dual-PSU adapter cable (~€20-30). This is common practice in multi-GPU builds and works reliably for sustained loads.

---

## The Energy Question

Someone suggested I look into solar panels to offset the electricity cost. So I did.

### What the rig actually consumes

3× RTX 5090 at ~575W each, plus system overhead: roughly 2 kW under load. At 8 hours per day, that is 16 kWh/day, 480 kWh/month, 5,760 kWh/year. At the French regulated tariff (~€0.195/kWh), that is about €1,150/year or €96/month.

### Solar in Paris: honest numbers

In Île-de-France, 1 kWc of solar panels produces 900-1,050 kWh per year. To offset my GPU consumption entirely, I would need ~6 kWc — a rooftop installation costing €8,000-10,000. Payback: 7-9 years, and only if I actually consume the electricity when the sun shines (autoconsommation rate ~30-40% without battery storage).

Balcony plug-and-play panels (Beem, Sunology) are simpler: €430-700 for 400-500 Wc. But a single kit produces ~475 kWh/year — about €95 of electricity. Four kits on a balcony (1,800 Wc, ~€2,400) cover maybe 30% of the rig's consumption.

Small wind turbines in urban Paris? Fantasy. Wind speed in the city is half that of rural areas, which means eight times less energy (power scales with the cube of velocity). The cost per kWh is 16 times higher than rural wind. Every Parisian experiment (Belleville park, Cité des Sciences) has been a demonstrator, not a solution.

### The nuclear irony

Here is the uncomfortable fact: France's electrical grid emits 19.6 gCO2eq/kWh — a European record, thanks to 70%+ nuclear power. My GPU rig at 5,760 kWh/year emits roughly 113 kg of CO2 annually. That is one Paris-Marseille drive.

Solar panels, by contrast, emit 43 gCO2/kWh in lifecycle analysis (manufacturing, transport, end-of-life). **Plugging my GPUs into the French nuclear grid is already cleaner than powering them with solar panels.** The environmental argument for self-generation does not hold in a country where the grid is already 95% decarbonized.

### The smart move: EDF Tempo

The real optimization is not hardware but tariff. EDF Tempo offers electricity at €0.1288/kWh during off-peak hours on "blue" days (300 days per year), but €0.6586/kWh during peak hours on "red" days (22 days per year).

Strategy: run heavy inference overnight and off-peak (a cron job, not a lifestyle change). Throttle or shut down GPUs during the 22 red days. If 80% of consumption falls in blue off-peak, monthly cost drops from ~€96 to ~€62. That is €400/year saved with zero investment — just a script that checks the RTE calendar.

---

## What I Am Actually Going to Do

1. **Keep one Claude Max subscription.** For the tasks where nothing else works: long agentic coding sessions, complex multi-file refactors, this exact kind of research and writing. The goal is not to eliminate the API. It is to stop using $600/day of it.

2. **Build the local rig.** Sell the 4090, buy two more 5090s, swap the motherboard for a Taichi, push RAM to 192 GB. Run the best available open model (DeepSeek V3 today, whatever surpasses it tomorrow) through vLLM with Aider or Cline as the frontend.

3. **Use local for 70-80% of my work.** Scenario iteration, vibe coding prototypes, repetitive tasks, anything that benefits from unlimited context and no rate limits. Use Claude for the remaining 20-30% where quality cannot be compromised.

4. **Track everything.** Electricity costs, actual tokens per second, quality comparisons, time spent on setup versus productive work. Publish the real numbers, not the optimistic projections.

5. **Revisit in three months.** The model landscape changes monthly. By July 2026, DeepSeek V4 or its equivalent may close the gap entirely. Or it may not. I will report back honestly.

---

## The Uncomfortable Conclusion

The Deep Research thread I started with was 20+ exchanges long. It began with "what is the best OS?" and ended with "should I buy four RTX 5090s?" Along the way, a series of AI assistants told me increasingly confident things that turned out to be unverifiable, optimistic, or simply hallucinated.

This is the meta-lesson: **the tools I am trying to replace are the only tools good enough to help me plan their replacement.** I used Claude Opus to research how to stop paying for Claude Opus. The irony is structural, not incidental.

But the direction is correct. Local inference is getting better every month. Open models are closing the gap. The cost of API-dependent workflows is unsustainable for independent creators. The question is not whether to go local, but when.

For me, the answer is now — imperfectly, partially, with one foot still in the cloud. Not because the local experience is as good as Claude Code today. But because paying $600 a day for a tool that could disappear, change its terms, or simply raise prices is not sovereignty. It is renting.

And I would rather own a machine that is 85% as good than rent one that is 100% as good but belongs to someone else.

Even if that machine depends on NVIDIA's cobalt and TSMC's water. At least I can see the supply chain. On the cloud, even the dependency is invisible.

---

## Sources

### Models & Benchmarks
- [DeepSeek V3 Technical Report](https://arxiv.org/abs/2412.19437)
- [Qwen 3 Series — Alibaba](https://qwenlm.github.io/)
- [Llama 4 — Meta AI](https://ai.meta.com/llama/)
- [SWE-bench: Evaluating LLMs on Software Engineering](https://www.swebench.com/)
- [Open LLM Leaderboard — Hugging Face](https://huggingface.co/spaces/open-llm-leaderboard/open_llm_leaderboard)

### Hardware & Quantization
- [NVIDIA Blackwell Architecture Whitepaper](https://www.nvidia.com/en-us/data-center/technologies/blackwell-architecture/)
- [NVIDIA TensorRT Model Optimizer — FP4/FP8](https://developer.nvidia.com/tensorrt)
- [vLLM: Easy, Fast, and Cheap LLM Serving](https://github.com/vllm-project/vllm)
- [RTX 5090 Reviews — TechPowerUp, Tom's Hardware](https://www.techpowerup.com/)
- [ASUS ProArt X870E-Creator WiFi Specs](https://www.asus.com/motherboards-components/motherboards/proart/)

### Agentic Tools
- [Aider — AI Pair Programming in Your Terminal](https://github.com/paul-gauthier/aider)
- [Cline — Autonomous Coding Agent for VS Code](https://github.com/cline/cline)
- [OpenHands — Open Platform for AI Software Engineers](https://github.com/All-Hands-AI/OpenHands)

### Cost & Energy
- [Electricity Prices in France — EDF Tarif Réglementé 2026](https://www.edf.fr/)
- [Anthropic API Pricing — Claude Models](https://docs.anthropic.com/en/docs/about-claude/pricing)
- [GPU Power Consumption Benchmarks 2025-2026](https://www.techpowerup.com/review/)

### Energy & Environment
- [Hellowatt — EDF Tempo Tarifs 2026](https://www.hellowatt.fr/blog/tarifs-edf-tempo-nouvelle-grille-prix/)
- [RTE — Eco2mix CO2 Emissions](https://www.rte-france.com/en/data-publications/eco2mix/eco2-emissions)
- [SFEN — Emissions Carbone du Nucléaire Français](https://www.sfen.org/rgn/les-emissions-carbone-du-nucleaire-francais-37g-de-co2-le-kwh/)
- [TotalEnergies — Panneau Solaire Île-de-France](https://www.totalenergies.fr/particuliers/nos-services/autoconsommation-solaire/installation-panneau-solaire/panneau-solaire-ile-de-france)
- [Beem Energy — Kits Plug and Play](https://beemenergy.fr/collections/panneaux-solaires-plug-and-play)

### Political Economy
- [Crawford, Kate — *Atlas of AI* (2021)](https://yalebooks.yale.edu/book/9780300264630/atlas-of-ai/)
- [The Environmental Impact of Semiconductor Manufacturing — IEEE](https://ieeexplore.ieee.org/)
- [Cobalt Mining in the DRC — Amnesty International](https://www.amnesty.org/en/latest/news/2016/01/child-labour-behind-smart-phone-and-electric-car-batteries/)

---

*This essay is part of [deep-research](https://github.com/ismael-joffroy-chandoutis/deep-research), a collection of investigations into the tools, systems, and ideas shaping AI-native creative practice.*
