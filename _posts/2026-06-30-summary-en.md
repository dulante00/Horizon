---
layout: default
title: "Horizon Summary: 2026-06-30 (EN)"
date: 2026-06-30
lang: en
---

> From 54 items, 15 important content pieces were selected

---

1. [Claude Sonnet 5](#item-1) ⭐️ 8.0/10
2. [Claude Code is steganographically marking requests](#item-2) ⭐️ 8.0/10
3. [vLLM v0.24.0 Released with 571 Commits and Major Kernel Optimizations](#item-3) ⭐️ 7.0/10
4. [Claude Science](#item-4) ⭐️ 7.0/10
5. [DIY mmWave Radar for Material Classification — Full Build Log](#item-5) ⭐️ 7.0/10
6. [OpenAI Uses Epidemiology to Diagnose 18-Year-Old Bug in Core Dumps](#item-6) ⭐️ 7.0/10
7. [IBM and HuggingFace Launch ScarfBench for AI Agent Code Migration](#item-7) ⭐️ 7.0/10
8. [DiScoFormer: One transformer for density and score, across distributions](#item-8) ⭐️ 7.0/10
9. [DeepSeek V4 Doubles Token Share on OpenRouter, Led by Agentic Workloads](#item-9) ⭐️ 7.0/10
10. [Huawei open-sources OpenPangu-2.0-Flash - 92B total,6B active](#item-10) ⭐️ 7.0/10
11. [Meta Builds Custom CXL 2.0 Chip to Reuse DDR4 in DDR5 Servers](#item-11) ⭐️ 7.0/10
12. [Nano Banana 2 Lite](#item-12) ⭐️ 6.0/10
13. [Introducing GeneBench-Pro](#item-13) ⭐️ 6.0/10
14. [Hugging Face Integrates Every Eval Ever Results on Model Pages](#item-14) ⭐️ 6.0/10
15. [Speculative Decoding Bench: ~96 TPS on a Single RTX 3090 with a 27B Model](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Claude Sonnet 5](https://www.anthropic.com/news/claude-sonnet-5) ⭐️ 8.0/10

Anthropic releases Claude Sonnet 5, their most agentic Sonnet model yet, though community benchmarks and cost analysis suggest Opus may be better value at higher effort levels.

hackernews · marinesebastian · Jun 30, 17:59 · [Discussion](https://news.ycombinator.com/item?id=48736605)

**Tags**: `#claude`, `#anthropic`, `#llm-release`, `#ai-agents`, `#model-benchmarks`

---

<a id="item-2"></a>
## [Claude Code is steganographically marking requests](https://thereallo.dev/blog/claude-code-prompt-steganography) ⭐️ 8.0/10

Claude Code was discovered to steganographically embed hidden markers in its requests, apparently to identify and potentially penalize usage from Chinese firms suspected of model distillation, raising transparency concerns.

hackernews · kirushik · Jun 30, 15:44 · [Discussion](https://news.ycombinator.com/item?id=48734373)

**Tags**: `#ai-tools`, `#steganography`, `#anthropic`, `#developer-tools`, `#ai-ethics`

---

<a id="item-3"></a>
## [vLLM v0.24.0 Released with 571 Commits and Major Kernel Optimizations](https://github.com/vllm-project/vllm/releases/tag/v0.24.0) ⭐️ 7.0/10

vLLM v0.24.0 ships with 571 commits from 256 contributors, adding support for the new MiniMax-M3 model, substantial DeepSeek-V4 optimizations (FlashInfer sparse index cache, native DSA indexer decode on SM100, block-FP8 shared expert), AMD/ROCm tuning for gfx950 and MI300X, Model Runner V2 quantization support, a unified streaming parser engine, DiffusionGemma, and DeepEP v2 integration. vLLM is one of the most widely deployed open-source LLM inference engines, and optimizations like FP8 sparse GQA, MXFP4/MXFP8 MoE kernels, and FlashInfer-backed attention directly translate into lower latency, higher throughput, and reduced serving costs for production deployments of large and mixture-of-experts models. Key technical highlights include 2–4% TTFT gains from the FlashInfer sparse index cache, 4% end-to-end throughput improvement from prefill chunk-planning, MXFP8 MoE/linear kernels tuned for AMD gfx950, and the deprecation of internal `CUDA_VISIBLE_DEVICES` management in favor of an explicit `device_ids` argument. The Rust frontend gained API-key auth, CORS, tokenize/detokenize endpoints, and pause/resume controls.

github · khluu · Jun 29, 19:41

**Background**: vLLM is a high-throughput open-source inference engine for large language models, originally developed at UC Berkeley and now maintained by a broad community. FlashInfer is a kernel library for LLM serving that provides optimized attention, GEMM, MoE, and sampling operations across GPU architectures. Microscaling formats (MXFP4/MXFP8) are block floating-point quantization schemes designed for AI workloads, using shared block exponents to compress weights while preserving dynamic range. Grouped-Query Attention (GQA) is a transformer attention variant that shares key-value heads across multiple query heads, trading a small amount of model quality for significant inference speedups. DeepEP is a communication library for Mixture-of-Experts (MoE) expert parallelism.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/flashinfer-ai/flashinfer">GitHub - flashinfer-ai/flashinfer: FlashInfer: Kernel Library for LLM Serving · GitHub</a></li>
<li><a href="https://www.opencompute.org/documents/ocp-microscaling-formats-mx-v1-0-spec-final-pdf">OCP Microscaling Formats (MX ... - Open Compute Project</a></li>
<li><a href="https://arxiv.org/abs/2305.13245">[2305.13245] GQA: Training Generalized Multi-Query ...</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#release-notes`, `#kernel-optimization`, `#amd-rocm`

---

<a id="item-4"></a>
## [Claude Science](https://claude.com/product/claude-science) ⭐️ 7.0/10

Anthropic launches Claude Science, an AI tool for scientific research with HPC/database integrations and a local-server architecture designed for locked-down enterprise environments like pharma.

hackernews · lebovic · Jun 30, 17:07 · [Discussion](https://news.ycombinator.com/item?id=48735770)

**Tags**: `#ai`, `#anthropic`, `#claude`, `#scientific-computing`, `#enterprise-ai`

---

<a id="item-5"></a>
## [DIY mmWave Radar for Material Classification — Full Build Log](https://gauthier-lechevalier.com/radar) ⭐️ 7.0/10

An independent maker published a detailed 2025 write-up of a DIY mmWave (millimeter-wave) radar system designed to classify materials, covering hardware design choices, signal processing implementation, an honest post-mortem of what failed, and concrete lessons learned. The project demonstrates that building a functional mmWave sensing and classification system is now within reach of individual makers, thanks to commodity radar modules and open tooling — a trend with implications for affordable inspection, recycling, construction safety, and robotics. It also adds to a small but growing body of DIY mmWave work that mirrors active academic research on radar-based material identification. The build leverages off-the-shelf mmWave radar front-ends and applies signal processing and machine learning to the reflected signatures to distinguish materials; the author was explicit that the proof-of-concept did not actually validate the more ambitious claim (e.g., detecting asbestos shards inside a host material), which is a key caveat for anyone interpreting the results as a product-ready solution.

hackernews · GL26 · Jun 30, 17:29 · [Discussion](https://news.ycombinator.com/item?id=48736137)

**Background**: mmWave radar operates in the millimeter-wave portion of the electromagnetic spectrum (roughly 30–300 GHz) and is widely used in automotive sensing, security screening, and industrial applications because it can detect small motions and concealed objects while working in adverse environments. Material classification with radar works by analyzing how different substances reflect, scatter, and absorb the transmitted signal — using features like range profiles, Doppler shifts, and phase information, often fed into classical classifiers or deep neural networks. Recent academic work (e.g., 60 GHz FMCW radar with deep CNNs, and even 2025 research exploring LLMs for radar material identification) shows this is an active research area at the intersection of RF engineering and machine learning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Mmwave_sensing">mmWave sensing - Wikipedia</a></li>
<li><a href="https://ieeexplore.ieee.org/document/9079136">Material Classification using 60-GHz Radar and Deep ...</a></li>
<li><a href="https://arxiv.org/abs/2508.03120">[2508.03120] Can Large Language Models Identify Materials from Radar Signals?</a></li>

</ul>
</details>

**Discussion**: Domain experts in the Hacker News thread raised substantive critique: one commenter pointed out that the proof-of-concept never actually tested the core asbestos-detection claim, calling the conclusions unsupportable. Another shared professional experience building a 76–81 GHz Rotman-lens imaging radar, while others praised the honest failure analysis and suggested alternative use cases such as discontinuity detection (analogous to medical imaging) and autonomous trash-collection robotics.

**Tags**: `#mmwave`, `#radar`, `#hardware`, `#signal-processing`, `#diy-electronics`

---

<a id="item-6"></a>
## [OpenAI Uses Epidemiology to Diagnose 18-Year-Old Bug in Core Dumps](https://openai.com/index/core-dump-epidemiology-data-infrastructure-bug) ⭐️ 7.0/10

OpenAI engineers applied epidemiology-inspired analysis to large-scale core dump data to diagnose rare infrastructure crashes, uncovering both a hardware fault and a software bug that had remained latent for 18 years. This case demonstrates a transferable methodology for debugging at scale—treating system failures as a population-level dataset—and shows how long-dormant bugs can persist undetected even in mature systems, underscoring the value of large-scale empirical analysis for infrastructure reliability. The epidemiology-style approach treats crash signals across many machines as a population dataset—identifying clusters and shared patterns rather than debugging individual incidents in isolation. Both a hardware fault and an 18-year-old latent software bug surfaced only after this population-level analysis was applied.

rss · OpenAI Blog · Jun 30, 00:00

**Background**: A core dump is a snapshot of a program's memory and execution state captured at the moment of a crash, commonly used by engineers to diagnose software failures. In large-scale infrastructure environments, thousands of machines can produce enormous volumes of core dumps, making manual case-by-case analysis impractical. Epidemiology, traditionally a public-health discipline for tracking disease spread through populations, offers statistical and clustering techniques that can be repurposed to detect patterns in crash data—distinguishing crashes that share a common root cause from isolated incidents.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/core-dump-epidemiology-data-infrastructure-bug/">Core dump epidemiology: fixing an 18-year-old bug - OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Core_dump">Core dump - Wikipedia</a></li>
<li><a href="https://academic.oup.com/femspd/article/77/1/ftz006/5304613">Is epidemiology ready for Big Software? | Pathogens and Disease | Oxford Academic</a></li>

</ul>
</details>

**Tags**: `#systems-engineering`, `#debugging`, `#infrastructure`, `#openai`, `#post-mortem`

---

<a id="item-7"></a>
## [IBM and HuggingFace Launch ScarfBench for AI Agent Code Migration](https://huggingface.co/blog/ibm-research/scarfbench) ⭐️ 7.0/10

IBM Research and HuggingFace have jointly released ScarfBench, a new open benchmark designed to evaluate AI coding agents on the complex real-world task of enterprise Java framework migration, such as moving from Java EE to Jakarta EE or from older Spring versions to Spring Boot 3. Enterprise Java migrations are costly, error-prone, and affect thousands of organizations still running legacy systems, so a standardized benchmark allows the community to measure and improve AI agent capabilities on a high-impact software engineering problem rather than toy coding tasks. ScarfBench is published on HuggingFace under IBM Research's organization, joining their broader enterprise agent ecosystem that already includes AssetOpsBench, ITBench, CUGA, NC-Bench, and a data-product benchmark, signaling IBM's systematic effort to build open evaluation infrastructure for enterprise AI automation.

rss · HuggingFace Blog · Jun 30, 18:32

**Background**: Enterprise Java has undergone a major namespace transition: Java EE was transferred to the Eclipse Foundation and rebranded as Jakarta EE, with the javax.* package prefix replaced by jakarta.* starting from Jakarta EE 9. Spring Boot 3, released in November 2022, adopted Jakarta EE 9+ as its minimum requirement alongside Java 17, forcing most teams to migrate. This migration is largely mechanical but hides surprising breaking changes, and the broader trend of agentic software modernization aims to use autonomous AI agents that can plan, analyze, and refactor legacy systems to assist human engineers.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/ibm-research">ibm-research (IBM Research)</a></li>
<li><a href="https://huggingface.co/datasets/ibm-research/nc-bench">ibm-research/nc-bench · Datasets at Hugging Face</a></li>
<li><a href="https://huggingface.co/datasets/ibm-research/data-product-benchmark">ibm-research/data-product-benchmark · Datasets at Hugging Face</a></li>
<li><a href="https://katyella.com/blog/jakarta-ee-migration-spring-boot-3/">Jakarta EE Migration: From javax to jakarta in Spring Boot 3</a></li>
<li><a href="https://www.baeldung.com/java-jakarta-enterprise-edition-migration">Migrate From Java EE to Jakarta EE - Baeldung Migrating to Spring Boot 3: The Jakarta EE Namespace Change ... Core Java vs Enterprise Java: Jakarta EE & Spring Boot 2026 Spring Boot 3 and the Move to Jakarta EE: What Developers ... Java EE to Spring Boot Migration Strategy for 2026</a></li>
<li><a href="https://github.com/feststelltaste/awesome-agentic-software-modernization">GitHub - feststelltaste/awesome-agentic-software ...</a></li>

</ul>
</details>

**Tags**: `#benchmark`, `#AI-agents`, `#code-migration`, `#enterprise-java`, `#software-engineering`

---

<a id="item-8"></a>
## [DiScoFormer: One transformer for density and score, across distributions](https://huggingface.co/blog/allenai/discoformer) ⭐️ 7.0/10

AllenAI introduces DiScoFormer, a unified transformer architecture that simultaneously performs density estimation and score matching across diverse data distributions for generative modeling.

rss · HuggingFace Blog · Jun 29, 18:02

**Tags**: `#transformers`, `#generative-modeling`, `#density-estimation`, `#score-matching`, `#AllenAI`

---

<a id="item-9"></a>
## [DeepSeek V4 Doubles Token Share on OpenRouter, Led by Agentic Workloads](https://openrouter.ai/blog/insights/deepseek-v4-adoption/) ⭐️ 7.0/10

DeepSeek doubled its token share on the OpenRouter AI routing platform over six months, with the V4 Flash model specifically driving the growth. The surge is attributed to agentic workload use cases, where AI systems autonomously make decisions, call tools, and execute multi-turn tasks. This signals significant competitive dynamics in the LLM landscape, showing that a cost-effective MoE model like DeepSeek V4 Flash can capture meaningful share in high-value agentic AI workloads. It validates agentic AI as a major battleground where providers compete on inference cost, speed, and long-context capability. DeepSeek V4 Flash is a 284B-parameter Mixture-of-Experts model with only 13B parameters activated per inference and a 1M-token context window, optimized specifically for fast coding and agentic tasks. The data comes from OpenRouter, a unified routing platform that aggregates traffic across 400+ models, making its token share metrics a meaningful proxy for real-world model adoption.

rss · OpenRouter Blog · Jun 30, 00:00

**Background**: OpenRouter is a unified API platform that routes inference requests to over 400 AI models from dozens of providers through a single endpoint, making its aggregated token share data a useful indicator of real-world LLM adoption trends. Agentic AI refers to systems where autonomous AI agents make decisions, take actions, and coordinate tasks with minimal human intervention—these workloads involve stateful, multi-turn interactions, tool use, and growing context windows, differing fundamentally from simple single-prompt generation. DeepSeek V4 Flash uses a Mixture-of-Experts architecture, which maintains a very large total parameter count but activates only a small subset per query, balancing raw capability with inference cost efficiency.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datacamp.com/tutorial/openrouter">OpenRouter: A Guide With Practical Examples | DataCamp</a></li>
<li><a href="https://build.nvidia.com/deepseek-ai/deepseek-v4-flash/modelcard">deepseek-v4-flash Model by Deepseek-ai | NVIDIA NIM</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained - MIT Sloan</a></li>

</ul>
</details>

**Tags**: `#DeepSeek`, `#LLM-adoption`, `#agentic-AI`, `#OpenRouter`, `#market-analysis`

---

<a id="item-10"></a>
## [Huawei open-sources OpenPangu-2.0-Flash - 92B total,6B active](https://www.reddit.com/r/LocalLLaMA/comments/1ujn5u3/huawei_opensources_openpangu20flash_92b_total6b/) ⭐️ 7.0/10

Huawei open-sources OpenPangu-2.0-Flash, a 92B total/6B active MoE model with 512K context, with a 505B Pro model planned for July.

reddit · r/LocalLLaMA · /u/soteko · Jun 30, 11:58

**Tags**: `#open-source`, `#LLM`, `#MoE`, `#Huawei`, `#long-context`

---

<a id="item-11"></a>
## [Meta Builds Custom CXL 2.0 Chip to Reuse DDR4 in DDR5 Servers](https://www.reddit.com/r/LocalLLaMA/comments/1ujzf35/meta_fights_soaring_hardware_costs_by_reusing_old/) ⭐️ 7.0/10

Meta has developed a custom CXL 2.0 chip that enables legacy DDR4-2400 server memory modules to operate inside new DDR5-6400-only server systems, effectively bridging two incompatible memory generations through a single silicon device. As AI training and inference workloads drive memory demand to unprecedented levels, hardware costs have become a major bottleneck for hyperscalers like Meta. This innovation allows Meta to extract remaining value from its existing DDR4 inventory rather than retiring it, potentially saving millions in capital expenditure while still deploying next-generation DDR5 platforms. The chip uses the CXL 2.0 cache-coherent interconnect protocol, built on PCIe physical/electrical layers, to make older DDR4-2400 modules appear as a coherent memory tier alongside native DDR5-6400 (6400 MT/s, CL52) memory. This approach trades latency and bandwidth from the DDR4 pool for cost savings, making it best suited for capacity-tier workloads rather than latency-sensitive compute paths.

reddit · r/LocalLLaMA · /u/pulse77 · Jun 30, 19:43

**Background**: Compute Express Link (CXL) is an open industry-standard interconnect built on top of PCIe that enables cache-coherent, high-speed connections between CPUs, memory expansion devices, and accelerators in data centers. DDR5-6400 is the current high-end server memory standard, offering 6400 MT/s transfer rates with ECC support for enterprise reliability. Legacy DDR4-2400 modules, while obsolete for new server builds, still represent a large sunk-cost inventory for operators. CXL memory-expansion devices allow systems to pool and access heterogeneous memory resources coherently, which is the underlying capability Meta is leveraging to mix memory generations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Compute_Express_Link">Compute Express Link - Wikipedia</a></li>
<li><a href="https://computeexpresslink.org/about-cxl/">About CXL® - Compute Express Link</a></li>

</ul>
</details>

**Tags**: `#hardware`, `#CXL`, `#memory`, `#Meta`, `#infrastructure`

---

<a id="item-12"></a>
## [Nano Banana 2 Lite](https://deepmind.google/models/gemini-image/flash-lite/) ⭐️ 6.0/10

Google releases Nano Banana 2 Lite (Gemini Image Flash Lite), a distilled image generation model with impressive speed (~5s per image) but programmatic limitations, as tested early by the author.

hackernews · minimaxir · Jun 30, 16:48 · [Discussion](https://news.ycombinator.com/item?id=48735444)

**Tags**: `#image-generation`, `#google`, `#gemini`, `#ai-models`, `#deepmind`

---

<a id="item-13"></a>
## [Introducing GeneBench-Pro](https://openai.com/index/introducing-genebench-pro) ⭐️ 6.0/10

OpenAI introduces GeneBench-Pro, a benchmark designed to evaluate AI model performance on complex, real-world genomics and biological research tasks.

rss · OpenAI Blog · Jun 30, 00:00

**Tags**: `#benchmark`, `#genomics`, `#biology`, `#openai`, `#ai-evaluation`

---

<a id="item-14"></a>
## [Hugging Face Integrates Every Eval Ever Results on Model Pages](https://huggingface.co/blog/eee-community-evals) ⭐️ 6.0/10

Hugging Face has launched Every Eval Ever (EEE), a system that surfaces community-driven evaluation results directly on model pages. The integration pulls normalized evaluation data from the EEE Datastore into model cards, making benchmarks like MMLU easily comparable across models such as DeepSeek-V3 and Llama 3.1. This integration improves transparency and discoverability for ML practitioners by standardizing how community evaluation results are presented, reducing fragmentation in benchmarking. It helps users make more informed model selection decisions without having to manually aggregate scores from multiple sources. EEE is maintained across three components: the every_eval_ever Python package on GitHub (with schema definitions and converters), the EEE Datastore on Hugging Face, and the dataset evaleval/every_eval_score_ever which stores detailed statistics structured by benchmark (lite, mmlu, classic), dataset name, and model name.

rss · HuggingFace Blog · Jun 30, 00:00

**Background**: Model evaluation and benchmarking are critical for comparing large language models, but results are often scattered across different leaderboards, papers, and community discussions. Community-driven evaluation platforms like LMSYS Chatbot Arena have shown the value of crowdsourced, transparent rankings. Hugging Face's Model Pages serve as the central hub for the open-source ML community to discover and share models, making it a natural place to aggregate standardized evaluation data.

<details><summary>References</summary>
<ul>
<li><a href="https://evalevalai.com/every_eval_ever/">Home | Every Eval Ever</a></li>
<li><a href="https://huggingface.co/datasets/evaleval/every_eval_score_ever">evaleval/every_eval_score_ever · Datasets at Hugging Face</a></li>
<li><a href="https://explore.n1n.ai/blog/hugging-face-every-eval-ever-integration-2026-06-30">Comprehensive LLM Evaluation Results Now on Hugging Face ...</a></li>

</ul>
</details>

**Tags**: `#huggingface`, `#model-evaluation`, `#benchmarking`, `#ml-platform`, `#open-source`

---

<a id="item-15"></a>
## [Speculative Decoding Bench: ~96 TPS on a Single RTX 3090 with a 27B Model](https://www.reddit.com/r/LocalLLaMA/comments/1ujo46r/qwen_36_27b_speculative_decoding_bench_pushing/) ⭐️ 6.0/10

A community member benchmarked five llama.cpp forks (ik_llama, mainline, Spiritbuun, beellama, and LUCEBOX) running speculative decoding on a quantized ~27B-parameter model on a single RTX 3090 (24GB), with the best setup (ik_llama MTP n_max=4 with ubergarm's IQ4_KS config) reaching 89.2 code TPS and 63.9 narrative TPS, while beellama's DFlash variant hit 96.8 code TPS. Running a ~27B model at near-100 tokens/second on consumer hardware (a single RTX 3090) demonstrates that aggressive speculative decoding and quantization can deliver usable local-LLM performance without expensive data-center GPUs, making high-quality local inference more accessible to hobbyists and researchers. The benchmark measured TTFT (288ms–504ms), VRAM usage (20–23 GB), and context-length degradation from 72k to 128k tokens; ik_llama showed the best peak TPS but suffered up to –32% speed drop at long context, while mainline llama.cpp had the lowest TTFT and near-zero degradation (most predictable). Note: the model label 'Qwen3.6-27B' may be a misnomer for an actual Qwen release.

reddit · r/LocalLLaMA · /u/old-mike · Jun 30, 12:40

**Background**: Speculative decoding accelerates LLM inference by using a small draft mechanism to propose several tokens that the main model then verifies in a single forward pass, preserving output quality. Multi-Token Prediction (MTP) builds the draft head into the model itself via auxiliary prediction heads trained to output multiple future tokens, while n-gram speculative decoding matches recent token patterns in the prompt as zero-cost drafts. The llama.cpp project has multiple community forks (ik_llama, Spiritbuun, beellama, LUCEBOX) that add experimental optimizations on top of upstream speculative decoding, and quantization formats like Q4_K_M and IQ4_KS reduce model size and VRAM at some quality cost.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>
<li><a href="https://arxiv.org/abs/2404.19737">Better & Faster Large Language Models via Multi-token Prediction [2505.17505] L-MTP: Leap Multi-Token Prediction Beyond ... Xiaohao-Liu/Awesome-Multi-Token-Prediction - GitHub Multi-Token Prediction Tutorial: How To Speed Up LLMs Multi-Token Prediction MTP in llama.cpp How It Works and How ... L-MTP: Leap Multi-Token Prediction Beyond Adjacent Context ... MTP - Speculators Docs</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/n_gram/">N-Gram Speculation - vLLM</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#speculative-decoding`, `#llama.cpp`, `#rtx-3090`, `#benchmarking`, `#quantization`

---