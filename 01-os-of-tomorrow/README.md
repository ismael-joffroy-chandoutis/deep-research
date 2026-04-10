# The OS of Tomorrow: A Filmmaker's Investigation

*By Ismaël Joffroy Chandoutis — April 2026*

---

I run three machines across two continents. A MacBook Air M3 in my bag, a Mac Mini M4 in my Paris studio, a Windows PC with an RTX 5090 wherever I need raw GPU power. I orchestrate them through Tailscale, talk to all of them through Claude Code, and spend most of my day in a terminal writing prompts instead of code.

I am a documentary filmmaker. I use AI to generate images, process archives, transcribe interviews, analyze 35,000 social media posts, build visual effects. My "studio" is not a room. It is a network of machines, a mesh of processes, an accumulation of environments that took months to configure and that I dread having to rebuild.

This is my investigation into what comes next. Not a tutorial. Not a product review. A personal attempt to answer a question that keeps me up at night: **what is the operating system of tomorrow, when the AI is the interface and the machine is just substrate?**

---

## The Question

Here is what changed: I no longer interact with my operating system. I interact with Claude Code. Claude reads my files, writes my scripts, manages my git repos, sends my emails, searches my databases. The OS is there, underneath, but I rarely see it. I see a prompt.

Andrej Karpathy called this out in 2023 when he described LLMs as "the kernel process of a new Operating System." By 2025, he had hardened this into a framework: Software 1.0 is code, Software 2.0 is learned weights, Software 3.0 is prompts.

> "LLMs are a new kind of computer, and you program them in English."

This is a seductive framing. It is also a corporate one. Karpathy works for OpenAI. The analogy between an LLM and a kernel naturalizes a very specific arrangement of power: your "new computer" is owned by someone else, runs on someone else's servers, and can change its behavior or pricing without your consent. A kernel you do not compile is not your kernel.

Linus Torvalds, predictably, is more grounded. He calls AI "just another tool, the same way compilers freed people from writing assembly code," and dismisses 90% of the discourse as marketing. But even he released AudioNoise in January 2026 with AI-generated Python code, using a Windsurf fork. His rule: vibe coding is fine for personal projects, "horrible to maintain" in production.

I sit somewhere between Karpathy's vision and Torvalds' pragmatism. I vibe code everything. I have Claude build my tools, manage my infrastructure, even draft my funding applications. But when a CUDA driver breaks or an FFmpeg build differs between machines, the substrate snaps back into focus. The OS still matters. It just matters differently.

---

## What I Use Today

### macOS: The Command Center

Both my Macs run macOS. It is where I live. Final Cut, DaVinci Resolve, the creative tools are here. Apple Silicon's unified memory is genuinely remarkable: an M3 with 24GB can run 7B models locally through Ollama and MLX. The M4 Mac Mini serves as always-on inference and automation hub.

But macOS has a ceiling. No NVIDIA means no CUDA means no serious training. LoRA fine-tuning is possible but slow. Apple's MLX ecosystem is growing but remains a fraction of the CUDA world. The Mac is where I think. It is not where I compute.

### Windows: The GPU Box

My RTX 5090 runs Windows. ComfyUI, Stable Diffusion, model inference at scale. Windows is not where I want to be, but it is where the GPU drivers are. I SSH in from my Mac, run processes, pull results.

WSL2 helps but carries ~10% performance overhead and uses ~1GB more VRAM than native. For pure GPU workloads, native Windows is fine because the OS overhead disappears when the GPU does the work. But as a development environment, Windows remains hostile: path issues, symlink limitations, POSIX gaps, rsync needing Cygwin wrappers.

### The Glue: Tailscale + Claude Code

Tailscale creates an encrypted mesh where every machine gets a stable IP. In February 2026, Tailscale and LM Studio launched LM Link, which treats a remote NVIDIA rig as if it were directly connected to your laptop. All traffic encrypted end-to-end via WireGuard.

Claude Code sits on top of everything. It is, in practice, my operating system. It reads files across machines, manages processes, orchestrates workflows. I have 40+ specialized AI agents for different aspects of my work: film research, CNC funding applications, VFX pipeline management, email drafting. The underlying OS is plumbing.

I should be honest about what this means. Forty agents means forty systems trained on my behavior, my files, my decisions. I have built something that looks like a studio but functions like a dependency. When Anthropic's API goes down, my studio goes dark. When they change pricing, my budget changes. I chose this. But I chose it the way you choose a landlord: from a limited set of options, under pressure, hoping the terms hold.

But here is the more immediate problem: **plumbing breaks**. And when it breaks, I lose days.

---

## The Reproducibility Crisis

Here is the formula no one talks about: **prompt + environment = result**.

If your Python version differs, if your CUDA driver is a point release behind, if your FFmpeg was compiled with different flags, you get different outputs from the same instructions. This is not theoretical. I have lost entire days to environment drift between my machines.

Last month, a ComfyUI workflow that ran perfectly on my RTX 5090 produced corrupted outputs when I tried to replicate it on a cloud GPU. Same model weights, same workflow JSON, same prompt. Different CUDA version. Three hours of debugging.

This is where NixOS enters the conversation.

---

## NixOS: The Promise

NixOS is a Linux distribution built on a radical idea: **your entire system is declared in configuration files, built atomically, and stored immutably.** One file describes everything: packages, services, users, kernel modules, firewall rules. Apply it. Get the same system. Every time.

Think of it as treating your entire machine like a Git repo.

### What makes it different

- **Declarative**: You do not install packages. You declare that packages exist in your configuration, then rebuild the system. The gap between "what I want" and "what I have" is a diff.
- **Reproducible**: Every package build is sandboxed. No network access, no host filesystem. Same inputs produce same outputs. Builds are content-addressed by hash.
- **Atomic upgrades**: Each rebuild creates a new "generation." If an update breaks the system, reboot and select the previous generation from GRUB. Zero-risk upgrades.
- **Flakes**: Pin all inputs (package versions, overlays) via a lock file. Your CUDA version, your Python version, your FFmpeg build, all frozen and shareable.

Nixpkgs has over 122,000 packages, the largest repository in the world according to Repology. Most of them maintained by volunteers.

### For AI/ML specifically

NVIDIA and CUDA support is first-class, maintained by a dedicated team. The CUDA toolkit, cuDNN, and TensorRT are all available. Python environment management replaces conda/venv/pyenv entirely: environments are fully reproducible and shareable as a lock file.

Multi-machine deployment is where NixOS truly shines. Tools like deploy-rs (by Serokell) and Colmena support parallel deployment with automatic rollback if a target becomes unreachable after activation. You write one configuration, deploy to ten machines, and they all converge to the same state.

In practice, developers using Nix shells report faster setup and fewer dependency conflicts. The tradeoff is weeks of learning a language that looks like nothing else you have ever written.

### For creative work

DaVinci Resolve (Free and Studio) is packaged. Blender works with CUDA/OptiX GPU rendering. FFmpeg, Kdenlive, everything I need for post-production.

ComfyUI is not in nixpkgs yet (open issue #227006), but a community flake (comfyui-nix) supports NixOS, standard Linux, and macOS Apple Silicon with curated custom nodes.

Audio production has musnix, a NixOS module for real-time audio that configures the RT kernel and fixes VST plugin paths.

---

## The Honest Assessment

NixOS is not a simple tool. Let me be direct about the costs.

### The learning curve is real

The Nix language is lazy, purely functional, with unusual syntax. You must learn the language, the module system, flakes, overlays, overrides, and the contribution model. This is weeks of investment, not hours.

### FHS incompatibility

NixOS does not follow the standard Linux filesystem layout. Pre-compiled binaries (AppImages, proprietary software) do not work out of the box. Solutions exist (patchelf, steam-run, buildFHSUserEnv) but add friction. This is the number one blocker for creative professionals who rely on proprietary tools.

### The community split

This one matters beyond NixOS. In May 2024, a governance crisis fractured the project. The core issue: Eelco Dolstra, the original creator, sat on the NixOS Foundation board while also running Determinate Systems, a venture-funded company building proprietary tools on top of the community's unpaid work. Add a sponsorship from Anduril, a defense contractor, and the community revolted.

The result: three competing implementations. Upstream Nix, increasingly influenced by Determinate Systems. Lix, a community fork focused on governance and contributor experience. And Determinate Nix 3.0, which dropped upstream entirely in January 2026.

This is not a footnote. It is the recurring pattern of open source: volunteers build the commons, a company captures the value. Flakes, the feature that makes Nix usable for most people, remain officially "experimental" despite universal adoption. The ecosystem is powerful but politically fractured. The question of who owns the tools you depend on does not stop at the application layer.

### Disk usage

The Nix store grows aggressively. Each generation stores a full closure. No automatic garbage collection by default.

### The verdict

NixOS is exceptionally powerful for reproducible, multi-machine AI/ML infrastructure. For creative workflows involving proprietary tools, it adds significant friction compared to Ubuntu or Fedora. It is best suited for someone who values infrastructure-as-code and is willing to invest weeks in learning the system. It is not recommended as a first Linux for a creative professional.

---

## The Competition

### Ubuntu: The Default

Every ML tutorial, Docker image, and cloud instance assumes Ubuntu. CUDA installation is well-documented. The largest community means the largest knowledge base. But kernels can be old, packages sometimes stale, and LTS releases lag behind the cutting edge.

If NixOS is a precision instrument, Ubuntu is a reliable truck. It gets you there. It is not elegant.

### Fedora Silverblue / Universal Blue: The Middle Path

The immutable Linux trend is accelerating. Fedora Silverblue provides atomic updates with rollback, much like NixOS but without the learning curve. Bazzite (a Universal Blue variant) bakes in NVIDIA drivers. Flatpak and Distrobox handle apps.

This is Fedora's strategic direction. SteamOS proved immutable works for millions of consumers. The friction is lower than NixOS, the guarantees are weaker but still transformative compared to traditional mutable systems.

### Docker: The Real Portable Unit

Here is an uncomfortable truth: for a multi-machine setup, Docker images might be the actual operating system. The same container runs on my Mac Mini, my Windows GPU box, and any cloud instance. The host OS becomes infrastructure plumbing.

GitHub Codespaces spins up fully configured environments in ~30 seconds. NVIDIA Container Toolkit provides production-grade GPU passthrough. Dev Containers (devcontainer.json) standardize per-project environments.

The pattern emerging at scale: **thin base OS + all work in containers**. Docker Compose pins CUDA version, Python version, frameworks per project. This converges with both the immutable OS trend and NixOS's isolation philosophy.

### macOS + nix-darwin: Having It Both Ways

You do not need to switch to NixOS to use Nix. nix-darwin brings declarative package management to macOS. Your Homebrew becomes a Nix configuration. Your development shells become reproducible. You get 80% of the benefit with 20% of the disruption.

This might be the pragmatic answer for someone like me: keep macOS for creative tools, use Nix for environment management, and deploy NixOS only on headless compute nodes.

---

## Where This Is Going

### The OS becomes a runtime

The Hacker News consensus, distilled from years of threads: the OS is becoming a **runtime**, not an experience. What matters is the toolchain above it (Claude Code, Cursor, AI agents) and the substrate below it (drivers, GPU access, container runtime). The traditional desktop OS is squeezed from both sides.

### The AI layer thickens

Microsoft is embedding Copilot into Windows at the hardware level (NPU requirements, on-device models). Apple is weaving LLMs into macOS fabric with Private Cloud Compute. Google is doing the same with Android and ChromeOS.

But Linux takes a different path. No single corporate AI integration, maximum flexibility. Torvalds refuses "AI statements" in kernel documentation. The Linux Foundation launched the Agentic AI Foundation. Government adoption accelerates: Denmark is replacing Microsoft Office on 30,000 computers with open-source alternatives.

### The personal cluster

The multi-machine future is already here. A filmmaker in 2026 might run: an Apple Silicon laptop for mobility, an NVIDIA workstation for training and inference, a Mini as always-on server, cloud bursts for rendering. The challenge is orchestration.

The missing piece: a unified declaration layer. NixOps handles multi-machine Nix deployments. Ansible handles imperative tasks on non-Nix machines. Tailscale handles networking. But no single tool yet lets you write: "I have a MacBook, a Mini, and a Windows GPU box. Here is my studio. Deploy it."

### The convergence

Immutable OS + declarative config + containers + AI agents. These four trends are converging. NixOS anticipated this convergence a decade ago. Whether NixOS itself wins or its ideas permeate other systems, the direction is clear: your system becomes a description of itself.

---

## Who Operates the Operating System?

I have written most of this essay as if infrastructure were a technical problem. It is not. It is a political one.

The M3 in my bag contains cobalt mined in the DRC. The RTX 5090 rendering my images was assembled in a supply chain I cannot trace. The AI model that reads my files was trained on data scraped without consent, filtered by content moderators paid less than I spend on cloud compute in a month. The Nixpkgs repository I praised has 122,000 packages maintained largely by unpaid volunteers, while Determinate Systems raises venture capital on top of their labor.

I cite Karpathy, Torvalds, Altman, Amodei in this essay. Four men who build or control the infrastructure I depend on. Not one of them will be affected by the choices I make. I will be affected by theirs.

When I write "Claude Code is my operating system," I should hear what that sentence actually says. It says: a corporation mediates my relationship to my own tools, my own files, my own creative process. I have replaced Apple's walled garden with something more intimate and less visible. The plumbing metaphor I used earlier is wrong. Plumbing is infrastructure you own. This is infrastructure that owns you.

NixOS gestures toward genuine autonomy. Reproducibility, self-sovereignty, the ability to rebuild without anyone's permission. But even NixOS runs on hardware I did not make, connects to networks I do not control, and builds packages from source code written by people whose labor I benefit from without compensating.

I am a documentary filmmaker. I know how to trace a bullet from the body to the manufacturer. I should be doing the same with my GPU, my API key, my terminal prompt. The essay underneath this one is the one that follows those traces. I have not written it yet.

---

## My Plan

After this research, here is what I am going to do:

1. **Now**: Install nix-darwin on my MacBook. Declarative package management without leaving macOS. Start versioning my development environment.

2. **Next month**: Set up a NixOS partition on my BeQuiet PC (RTX 4090). Use it as a headless compute node. Deploy via Colmena from my Mac.

3. **This summer**: Write a `flake.nix` that describes my entire studio. Three machines, all services, all environments. Version it. Share it.

4. **The goal**: Rebuild my entire creative infrastructure from a single configuration file after a disaster. In minutes, not days.

Here is what I am actually afraid of: that one morning I will open my terminal and Claude will not respond, and I will realize I do not remember how to do any of this myself. That my studio, which I built with such care, was never mine. That the declaration file describes a system that only works as long as someone else's servers stay on.

The OS of tomorrow is not a brand. It might be a text file. But the question is not what the file says. The question is who can read it when the lights go out.

---

## Sources

### NixOS & Nix Ecosystem
- [NixOS Official Site](https://nixos.org/)
- [Flakes — NixOS Wiki](https://wiki.nixos.org/wiki/Flakes)
- [CUDA — NixOS Wiki](https://wiki.nixos.org/wiki/CUDA)
- [DaVinci Resolve — NixOS Wiki](https://wiki.nixos.org/wiki/DaVinci_Resolve)
- [DaVinci Resolve 19 on NixOS Guide (September 2025)](https://ca4mi.net/posts/2025-09-07-davinci-resolve-on-nixos/)
- [comfyui-nix Flake](https://github.com/utensils/comfyui-nix)
- [deploy-rs by Serokell](https://serokell.io/blog/deploy-rs)
- [Colmena](https://github.com/zhaofengli/colmena)
- [Determinate Nix 3.0 — NixOS Discourse](https://discourse.nixos.org/t/determinate-nix-3-0/61202)
- [Lix Project](https://git.lix.systems/lix-project)
- [NixOS + Framework Partnership (2025)](https://nixos.org/blog/announcements/2026/framework-partnership-announcement/)
- [Why Nix Is Having Its Moment (2025)](https://icloudcentral.com/why-nix-is-finally-having-its-moment-and-what-that-means-for-infrastructure-in-2025/)
- [NixOS: Declarative Linux Revolution](https://www.webpronews.com/nixos-declarative-linux-revolution-with-reproducible-systems-and-rollbacks/)
- [NixOS as Git Repo](https://www.webpronews.com/the-operating-system-that-treats-your-entire-machine-like-a-git-repo-and-why-hardcore-engineers-cant-stop-talking-about-it/)
- [Three Years of Nix — Pierre Zemb](https://pierrezemb.fr/posts/nixos-good-bad-ugly/)

### OS Landscape
- [Karpathy: LLMs as OS Kernel (2023)](https://x.com/karpathy/status/1707437820045062561)
- [Karpathy: LLM OS Blog (2025)](https://karpathy.ai/blog/2025-llm-os.html)
- [Torvalds on AI — The New Stack](https://thenewstack.io/linus-torvalds-gets-candid-about-windows-workflows-and-ai/)
- [Torvalds on Vibe Coding — The Register](https://www.theregister.com/2025/11/18/linus_torvalds_vibe_coding/)
- [Apple Intelligence 2026 Deep Dive](https://applemagazine.com/apple-intelligence-2026-deep-dive/)
- [Microsoft Copilot+ AI in Windows](https://techcommunity.microsoft.com/blog/windows-itpro-blog/evolving-windows-new-copilot-and-ai-experiences-at-ignite-2025/4469466)
- [Immutable Linux Trends 2026](https://linuxlap.com/news/key-trends-shaping-the-linux-in-2026/)
- [Linux Future Predictions 2026](https://itsfoss.com/news/linux-future-prediction-2026/)

### AI & Creative Workflows
- [Tailscale + LM Link (February 2026)](https://dataforcee.us/2026/02/26/tailscale-and-lm-studio-launch-lm-link-to-give-you-end-to-point-encrypted-access-to-your-private-gpu-computing-asset/)
- [Multi-Agent Orchestration — Gartner 2025](https://www.onabout.ai/p/mastering-multi-agent-orchestration-architectures-patterns-roi-benchmarks-for-2025-2026)
- [AI Filmmaking Workflow 2026](https://www.601media.com/ai-film-workflow-from-script-to-final-cut-no-camera-no-crew/)
- [AI Filmmaking Cost Reduction](https://studio.aifilms.ai/blog/ai-filmmaking-revolution-2025-cost-reduction-democratization)
- [Cursor vs Claude Code vs Windsurf 2026](https://dev.to/pockit_tools/cursor-vs-windsurf-vs-claude-code-in-2026-the-honest-comparison-after-using-all-three-3gof)
- [Amodei: Machines of Loving Grace](https://darioamodei.com/essay/machines-of-loving-grace)
- [Altman on AGI — TIME](https://time.com/7205596/sam-altman-superintelligence-agi/)

---

*This essay is part of [deep-research](https://github.com/12georgiadis/deep-research), a collection of investigations into the tools, systems, and ideas shaping AI-native creative practice.*
