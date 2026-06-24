---
layout: default
title: "Horizon Summary: 2026-06-24 (EN)"
date: 2026-06-24
lang: en
---

> From 70 items, 30 important content pieces were selected

---

1. [OpenAI Unveils 'Jalapeno,' Its First Custom AI Inference Chip](#item-1) ⭐️ 9.0/10
2. [Show HN: Nub – A Bun-like all-in-one toolkit for Node.js](#item-2) ⭐️ 8.0/10
3. [Krea 2: SOTA open-weights 12B image model](#item-3) ⭐️ 8.0/10
4. [OpenAI and Broadcom unveil Jalapeño, a custom LLM inference chip](#item-4) ⭐️ 8.0/10
5. [Google DeepMind Brings Computer Use to Gemini 3.5 Flash](#item-5) ⭐️ 8.0/10
6. [NSA lost access to Mythos amid Anthropic dispute](#item-6) ⭐️ 7.0/10
7. [HuggingFace and NVIDIA Launch NeMo AutoModel for Faster Transformer Fine-Tuning](#item-7) ⭐️ 7.0/10
8. [Introducing the FFASR Leaderboard: Benchmarking ASR in the Real World](#item-8) ⭐️ 7.0/10
9. [Build real agentic apps using CUGA: two dozen working examples on a lightweight harness](#item-9) ⭐️ 7.0/10
10. [OpenRouter Launches Unified Image API for 30+ Models](#item-10) ⭐️ 7.0/10
11. [TRM思考奖励模型上线，大模型推理质量终于能量化了 | ICML‘26 Oral](#item-11) ⭐️ 7.0/10
12. [The Swiss Federal Supreme Court is evaluating Heretic](#item-12) ⭐️ 7.0/10
13. [20x GLM-4.5 inference speedup on dual GH200 via MTP-AWQ model surgery](#item-13) ⭐️ 7.0/10
14. [OpenAI and Broadcom unveil LLM-optimized inference chip](#item-14) ⭐️ 7.0/10
15. [Qwen Releases 3B-Active MoE World Model for Agent Environment Simulation](#item-15) ⭐️ 7.0/10
16. [US Chip Security Act Mandates Location Tracking for AI Chips](#item-16) ⭐️ 7.0/10
17. [Baidu Releases Unlimited-OCR with R-SWA for Multi-Page Transcription](#item-17) ⭐️ 7.0/10
18. [RubyLLM: Unified Ruby Framework for Major AI Providers](#item-18) ⭐️ 6.0/10
19. [We’re making Bunny DNS free](#item-19) ⭐️ 6.0/10
20. [PR Spam in Open Source Mirrors Early 2000s Email Spam](#item-20) ⭐️ 6.0/10
21. [Google Adds Computer Use to Gemini 3.5 Flash Amid Criticism](#item-21) ⭐️ 6.0/10
22. [John Carmack Reflects on Early id Software Management Mistakes](#item-22) ⭐️ 6.0/10
23. [GPT-5 Pro Helps Immunologist Solve 3-Year-Old T Cell Mystery](#item-23) ⭐️ 6.0/10
24. [HuggingFace Ships huggingface_hub Weekly with AI-Assisted CI/CD](#item-24) ⭐️ 6.0/10
25. [HuggingFace Experiments with Cross-Origin Storage API in Transformers.js](#item-25) ⭐️ 6.0/10
26. [Baidu Releases Unlimited-OCR: 3.3B MIT-Licensed Document Parsing Model](#item-26) ⭐️ 6.0/10
27. [The Bank of Korea just released a report about AI productivity](#item-27) ⭐️ 6.0/10
28. [Developer Reverse-Engineers Windows Copilot into Free GPT-4 API](#item-28) ⭐️ 6.0/10
29. [Open-source browser extension runs SDXL image generation locally via WebGPU](#item-29) ⭐️ 6.0/10
30. [Italy's Domyn to Build 400B-Parameter EU Sovereign AI Model](#item-30) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI Unveils 'Jalapeno,' Its First Custom AI Inference Chip](https://techcrunch.com/2026/06/24/openai-unveils-its-first-custom-chip-built-by-broadcom/) ⭐️ 9.0/10

OpenAI announced 'Jalapeno,' its first custom AI inference chip co-designed with Broadcom and manufactured by TSMC, reportedly achieving roughly 50% cost savings compared with typical AI GPUs according to Broadcom CEO Hock Tan. The chip was developed from design to production in just nine months, with parts of the design and optimization workflow accelerated using OpenAI's own AI models. Jalapeno marks OpenAI's most significant step toward vertical integration in AI infrastructure, reducing its dependence on NVIDIA for running (rather than training) large language models at scale. A 50% cost reduction on inference—the bulk of ongoing AI compute spending—could reshape margins across the AI industry and intensify pressure on NVIDIA's dominant GPU business. The chip is manufactured by TSMC (not Intel), uses a 3.5D chiplet-based packaging approach typical of Broadcom's custom AI silicon, and is narrowly optimized for inference workloads rather than training. Community commenters noted that OpenAI was vague about exactly how its own models contributed to the design process, leaving the claim of AI-assisted chip design more as a marketing hint than a substantiated technical detail.

hackernews · jamdesk · Jun 24, 17:47 · [Discussion](https://news.ycombinator.com/item?id=48663324)

**Background**: AI workloads are broadly split into two stages: training, where models learn from data (compute-intensive, dominated by NVIDIA GPUs), and inference, where trained models answer user queries in production (a much larger and ongoing cost). Custom AI silicon, known as ASICs or XPUs, are chips designed for a specific customer's workloads and can dramatically improve efficiency for targeted tasks. Broadcom and Marvell together control roughly 95% of the custom AI ASIC co-design market, serving hyperscalers like Google, Meta, and now OpenAI, with Broadcom's AI revenue surging 106% year-over-year to $8.4B in Q1 FY2026. By building its own inference chip, OpenAI is following the playbook of other large AI labs seeking to reduce reliance on NVIDIA's general-purpose GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/custom-ai-asics-examined-from-broadcom-to-mtia">The custom AI ASIC state of play (May 2026) — Broadcom deals, Google ...</a></li>
<li><a href="https://tech-insider.org/broadcom-ai-revenue-custom-chips-2026/">Broadcom AI Revenue Surges 106%: Custom Chip Strategy 2026</a></li>
<li><a href="https://www.broadcom.com/info/ai/3point5d">AI Accelerator | XPU | Custom Compute - Broadcom Inc.</a></li>

</ul>
</details>

**Discussion**: Community sentiment is highly engaged and technically curious. Commenters debated whether OpenAI's claim of using its own models to accelerate chip design is substantive or merely marketing; welcomed the confirmed TSMC manufacturing partnership; and speculated about more radical architectures, such as chips with model weights burned into ROM for ultra-dense, ultra-low-cost inference. Several posters emphasized that the 50% cost reduction suggests significant remaining efficiency headroom in AI hardware, undermining arguments about vendor moats.

**Tags**: `#OpenAI`, `#custom-silicon`, `#AI-infrastructure`, `#Broadcom`, `#inference-chip`

---

<a id="item-2"></a>
## [Show HN: Nub – A Bun-like all-in-one toolkit for Node.js](https://github.com/nubjs/nub) ⭐️ 8.0/10

Nub is a Bun-like all-in-one toolkit for Node.js that uses `--require` hooks and module resolution hooks to additively augment stock Node with transpilation (oxc) and polyfills, without replacing Node's engine.

hackernews · colinmcd · Jun 24, 14:14 · [Discussion](https://news.ycombinator.com/item?id=48660267)

**Tags**: `#nodejs`, `#javascript`, `#developer-tools`, `#bun`, `#oxc`

---

<a id="item-3"></a>
## [Krea 2: SOTA open-weights 12B image model](https://www.krea.ai/blog/krea-2-technical-report) ⭐️ 8.0/10

Krea releases open-weights for their 12B SOTA text-to-image model along with a comprehensive technical report detailing training methodology, data infrastructure, and post-training pipelines.

hackernews · mattnewton · Jun 23, 15:31 · [Discussion](https://news.ycombinator.com/item?id=48646659)

**Tags**: `#open-source-ai`, `#image-generation`, `#text-to-image`, `#machine-learning`, `#model-release`

---

<a id="item-4"></a>
## [OpenAI and Broadcom unveil Jalapeño, a custom LLM inference chip](https://openai.com/index/openai-broadcom-jalapeno-inference-chip) ⭐️ 8.0/10

On June 24, OpenAI and Broadcom announced Jalapeño, OpenAI's first custom AI inference chip designed from scratch in nine months specifically for LLM inference. The chip was designed by OpenAI leveraging its deep knowledge of model architectures, kernels, and serving systems, while Broadcom and Celestica handled industrialization including chip implementation, board and rack system integration, and high-performance networking. Jalapeño represents a major strategic move toward vertical integration of AI infrastructure for OpenAI, similar to Google's path with TPUs, and could meaningfully reduce OpenAI's dependency on NVIDIA while exerting downward pressure on GPU pricing. The commitment to deploy 10 gigawatts of OpenAI capacity using this custom silicon signals an industry-shifting scale that could reshape the AI hardware landscape. The chip is designed for inference rather than training, targeting substantially better performance-per-watt than current NVIDIA GPUs. OpenAI collaborated with Broadcom for silicon implementation and Celestica for board, rack, and networking integration, meaning OpenAI controls the chip architecture and model co-design while outsourcing manufacturing and system-level engineering.

rss · OpenAI Blog · Jun 24, 06:00

**Background**: LLM inference refers to the process of running a trained large language model to generate outputs in production, which differs from training (where models learn from data) and has distinct hardware requirements favoring throughput and efficiency. Custom AI silicon has become a strategic priority for hyperscalers: Google's TPUs, Amazon's Inferentia/Trainium, and Meta's MTIA chips all target inference workloads to reduce costs and avoid NVIDIA dependency. Inference-optimized architectures often differ from training chips, with some designs (like Groq's LPU) using on-chip SRAM instead of HBM to achieve deterministic, low-latency responses.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/openai-broadcom-jalapeno-inference-chip/">OpenAI and Broadcom unveil LLM-optimized inference chip</a></li>
<li><a href="https://investors.broadcom.com/news-releases/news-release-details/openai-and-broadcom-unveil-llm-optimized-intelligence-processor">OpenAI and Broadcom Unveil LLM-Optimized Intelligence Processor</a></li>
<li><a href="https://startupfortune.com/openai-and-broadcom-unveil-jalapeo-a-custom-inference-chip-that-puts-nvidias-pricing-power-on-notice/">OpenAI and Broadcom unveil Jalapeño, a custom inference chip that puts ...</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#inference chips`, `#OpenAI`, `#Broadcom`, `#silicon`

---

<a id="item-5"></a>
## [Google DeepMind Brings Computer Use to Gemini 3.5 Flash](https://deepmind.google/blog/introducing-computer-use-in-gemini-3-5-flash/) ⭐️ 8.0/10

Google DeepMind has introduced computer use capabilities in Gemini 3.5 Flash, enabling the model to interact with and control computer interfaces—such as clicking, typing, and navigating UIs—to perform agentic tasks autonomously. This brings a previously premium-tier capability to one of Google's most widely accessible and cost-effective models. This move significantly lowers the barrier to building agentic AI applications by making computer use available on a cheaper, faster model tier. It intensifies competition in the agentic AI landscape, where Anthropic pioneered the capability with Claude 3.5 Sonnet, OpenAI offers Operator, and Microsoft integrates Copilot into Office 365. Computer use is an API-level capability that enables AI agents to operate software through its visual interface, the same way a human would. Gemini 3.5 Flash is optimized for speed and cost efficiency, meaning developers can now prototype and deploy agentic workflows at significantly lower expense compared to running such tasks on larger frontier models.

rss · Google DeepMind Blog · Jun 24, 16:30

**Background**: Computer use is an AI capability that allows models to perceive and act on graphical user interfaces—reading screens, moving cursors, clicking buttons, and typing text—rather than relying solely on structured APIs. Agentic AI refers to AI systems that can observe, reason, act, and learn autonomously to accomplish goals, going beyond traditional generative AI that only produces text or images in response to prompts. Anthropic first popularized computer use with Claude 3.5 Sonnet in late 2024, and competitors have since been racing to offer comparable or superior agentic capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://atxp.ai/blog/anthropic-computer-use-explained/">Anthropic Computer Use Explained: What It Is and What... — ATXP</a></li>
<li><a href="https://www.grammarly.com/agentic-ai">What is Agentic AI ? | Agentic AI 101</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-agents">What Are AI Agents? | IBM</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Gemini`, `#Computer Use`, `#Agentic AI`, `#Google DeepMind`

---

<a id="item-6"></a>
## [NSA lost access to Mythos amid Anthropic dispute](https://www.nytimes.com/2026/06/23/us/politics/nsa-lost-access-anthropic-tool.html) ⭐️ 7.0/10

The NSA has lost access to Anthropic's Mythos AI tool amid a contract dispute, raising questions about government access to powerful AI cybersecurity tools and Anthropic's positioning of the model as a significant security capability.

hackernews · thm · Jun 24, 11:45 · [Discussion](https://news.ycombinator.com/item?id=48658300)

**Tags**: `#AI`, `#national-security`, `#Anthropic`, `#cybersecurity`, `#government-tech`

---

<a id="item-7"></a>
## [HuggingFace and NVIDIA Launch NeMo AutoModel for Faster Transformer Fine-Tuning](https://huggingface.co/blog/nvidia/accelerating-fine-tuning-nvidia-nemo-automodel) ⭐️ 7.0/10

HuggingFace and NVIDIA have jointly introduced NeMo AutoModel, a new framework designed to accelerate the fine-tuning of transformer-based large language models. The tool is positioned as an open-source, PyTorch DTensor-native SPMD training library within the NVIDIA NeMo Framework ecosystem, streamlining and scaling LLM training and fine-tuning workflows. Fine-tuning large transformer models is computationally expensive and complex, creating a barrier for many ML practitioners and organizations. By combining NVIDIA's GPU-optimized NeMo infrastructure with HuggingFace's widely-adopted model hub, this collaboration significantly lowers the barrier to entry for customizing state-of-the-art LLMs and could accelerate applied AI development across industries. NeMo AutoModel is implemented as a PyTorch-native library using DTensor for distributed training, following the SPMD (Single Program, Multiple Data) parallelism model. It is tightly coupled to NVIDIA GPUs and the CUDA platform, meaning teams without compatible NVIDIA hardware cannot fully leverage its acceleration features.

rss · HuggingFace Blog · Jun 24, 16:00

**Background**: Transformer fine-tuning is the process of adapting a pre-trained model such as GPT or BERT to a specific downstream task or dataset, typically following a workflow of loading a pre-trained model, training it on task-specific data, and saving the customized version. NVIDIA NeMo is an end-to-end framework for building, customizing, and deploying generative AI models across language, speech, and vision modalities, with deep integration into the CUDA ecosystem. HuggingFace serves as the de facto hub for open-source transformer models, making collaborations like this strategically important for reaching the broader ML community.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/NVIDIA-NeMo/Automodel">GitHub - NVIDIA- NeMo / Automodel : Pytorch Distributed native...</a></li>
<li><a href="https://docs.nvidia.com/nemo-framework/user-guide/latest/automodel/index.html">NeMo AutoModel — NVIDIA NeMo Framework User Guide</a></li>
<li><a href="https://aiwiki.ai/wiki/nvidia_nemo">NVIDIA NeMo | AI Wiki</a></li>

</ul>
</details>

**Tags**: `#transformers`, `#fine-tuning`, `#NVIDIA`, `#NeMo`, `#optimization`

---

<a id="item-8"></a>
## [Introducing the FFASR Leaderboard: Benchmarking ASR in the Real World](https://huggingface.co/blog/ffasr-leaderboard) ⭐️ 7.0/10

HuggingFace introduces the FFASR Leaderboard, a new benchmark for evaluating automatic speech recognition models under realistic real-world conditions.

rss · HuggingFace Blog · Jun 24, 00:00

**Tags**: `#ASR`, `#speech-recognition`, `#benchmarking`, `#HuggingFace`, `#leaderboard`

---

<a id="item-9"></a>
## [Build real agentic apps using CUGA: two dozen working examples on a lightweight harness](https://huggingface.co/blog/ibm-research/cuga-apps) ⭐️ 7.0/10

IBM Research's CUGA framework offers two dozen working examples for building agentic applications on a lightweight harness, published on HuggingFace's blog.

rss · HuggingFace Blog · Jun 23, 12:51

**Tags**: `#agentic-ai`, `#ibm-research`, `#code-examples`, `#llm-agents`, `#huggingface`

---

<a id="item-10"></a>
## [OpenRouter Launches Unified Image API for 30+ Models](https://openrouter.ai/blog/announcements/image-api/) ⭐️ 7.0/10

OpenRouter has launched a dedicated Unified Image API that aggregates more than 30 image generation models from 8 providers behind a single endpoint, with automatic capability discovery so developers can query what each model supports without manual lookup. This significantly lowers the integration burden for developers building image generation features, eliminating the need to maintain separate API clients, authentication, and routing logic for each provider. It positions OpenRouter as a one-stop shop not just for LLMs but for the full multimodal stack, accelerating multi-model experimentation and fallback strategies. The API supports automatic capability discovery, meaning applications can programmatically query supported resolutions, aspect ratios, reference image inputs, and other model-specific features at runtime. This extends OpenRouter's existing unified chat API pattern to the image generation domain, following the same single-endpoint abstraction that has already attracted 250k+ apps and 4.2M+ users.

rss · OpenRouter Blog · Jun 23, 00:00

**Background**: OpenRouter is a gateway platform that provides developers with a single unified API to access many different AI models, originally focused on large language models. API aggregation platforms like this solve a common pain point: different AI providers each have their own authentication schemes, request formats, and feature sets, forcing developers to write and maintain bespoke integration code for every model they want to use. Capability discovery is a pattern where an API exposes metadata about what features it supports, allowing client code to adapt dynamically rather than hardcoding model-specific assumptions.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/docs/guides/overview/multimodal/image-generation">OpenRouter Image Generation | Complete Documentation</a></li>
<li><a href="https://medium.com/@chidarasuma/what-is-openrouter-9cb5c0f8ce76">What is OpenRouter ?. OpenRouter . ai is a gateway platform | Medium</a></li>

</ul>
</details>

**Tags**: `#image-generation`, `#api`, `#openrouter`, `#developer-tools`, `#multi-model`

---

<a id="item-11"></a>
## [TRM思考奖励模型上线，大模型推理质量终于能量化了 | ICML‘26 Oral](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247899199&idx=3&sn=b0d6764e50d881295fd85b75f8f9434a) ⭐️ 7.0/10

TRM (Thinking Reward Model) accepted as ICML'26 Oral introduces a method to quantify and evaluate the quality of LLM reasoning processes beyond final answer correctness.

rss · 量子位 · Jun 24, 04:00

**Tags**: `#LLM`, `#reasoning`, `#reward-model`, `#ICML-2026`, `#evaluation`

---

<a id="item-12"></a>
## [The Swiss Federal Supreme Court is evaluating Heretic](https://www.reddit.com/r/LocalLLaMA/comments/1ueeund/the_swiss_federal_supreme_court_is_evaluating/) ⭐️ 7.0/10

The Swiss Federal Supreme Court is evaluating Heretic, an LLM abliteration tool, to address over-refusal issues in legitimate multilingual criminal law queries, as documented in a new research paper.

reddit · r/LocalLLaMA · /u/-p-e-w- · Jun 24, 14:19

**Tags**: `#abliteration`, `#LLM-safety`, `#legal-AI`, `#Heretic`, `#over-refusal`

---

<a id="item-13"></a>
## [20x GLM-4.5 inference speedup on dual GH200 via MTP-AWQ model surgery](https://www.reddit.com/r/LocalLLaMA/comments/1uedlas/i_did_some_model_hacks_and_got_glm52_from_about/) ⭐️ 7.0/10

A hobbyist achieved a 20x inference speedup for GLM-4.5 (referred to as 'GLM5.2' by the author), going from roughly 2.5 tok/s to over 50 tok/s on a dual GH200 system by grafting the Multi-Token Prediction (MTP) head from Zhipu AI's official FP8 release onto the AWQ-quantized weights from community quantizer CyanKiwi, combined with NUMA tuning and vLLM patches. This demonstrates that hybrid architectures—mixing full-precision specialized modules with aggressively quantized base weights—can yield outsized inference gains on high-end but misconfigured hardware. For operators of Grace Hopper systems running large models, this reproducible workaround could unlock usable throughput where naive deployments were previously stuck below interactive speeds. Best-case throughput reached ~55 tok/s at 4x concurrency and ~45 tok/s for single-stream inference, with weights streaming from 960GB of LPDDR5X host memory into 192GB of combined HBM3. The procedure requires pulling the full AWQ weight set from CyanKiwi but only a few files from Z.ai's FP8 repo, then running a merge script alongside a vLLM patch to handle the resulting architectural changes.

reddit · r/LocalLLaMA · /u/Reddactor · Jun 24, 13:30

**Background**: GLM-4.5 is a large open-weight language model from Chinese AI lab Zhipu AI (Z.ai). AWQ (Activation-aware Weight Quantization) is a post-training quantization method that protects salient weights by analyzing activation magnitudes, enabling aggressive low-bit quantization with minimal accuracy loss. Multi-Token Prediction (MTP) is an architectural extension, popularized by DeepSeek-V3, that uses independent projection modules to predict several future tokens per step instead of the standard one-at-a-time autoregressive decoding. The NVIDIA GH200 Grace Hopper Superchip pairs an ARM-based Grace CPU with a Hopper H100 GPU connected via NVLink-C2C, unifying CPU-GPU memory access and enabling large models to spill into abundant host LPDDR5X memory when VRAM is insufficient.

<details><summary>References</summary>
<ul>
<li><a href="https://pyimagesearch.com/2026/03/30/autoregressive-model-limits-and-multi-token-prediction-in-deepseek-v3/">Autoregressive Model Limits and Multi - Token Prediction in...</a></li>
<li><a href="https://leimao.github.io/blog/AWQ-Activation-Aware-Weight-Quantization/">AWQ : Activation - Aware Weight Quantization - Lei Mao's Log Book</a></li>
<li><a href="https://www.spheron.network/gpu-rental/gh200/">NVIDIA GH 200 Grace Hopper : Specs & Cloud Rental | Spheron</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#vllm`, `#gh200`, `#model-optimization`, `#quantization`

---

<a id="item-14"></a>
## [OpenAI and Broadcom unveil LLM-optimized inference chip](https://www.reddit.com/r/LocalLLaMA/comments/1ueexbr/openai_and_broadcom_unveil_llmoptimized_inference/) ⭐️ 7.0/10

OpenAI and Broadcom announce 'Jalapeno,' a custom inference chip designed for LLMs, developed in 9 months using AI-driven design, to be deployed at gigawatt scale.

reddit · r/LocalLLaMA · /u/z_latent · Jun 24, 14:22

**Tags**: `#OpenAI`, `#Broadcom`, `#AI hardware`, `#inference chips`, `#AI infrastructure`

---

<a id="item-15"></a>
## [Qwen Releases 3B-Active MoE World Model for Agent Environment Simulation](https://www.reddit.com/r/LocalLLaMA/comments/1ue5149/qwenagentworld35ba3b_a_3bactive_moe_trained_to/) ⭐️ 7.0/10

Qwen has released Qwen-AgentWorld-35B-A3B, a 35B-parameter Mixture of Experts (MoE) language world model with only about 3B active parameters per token, specifically trained to predict environment responses across seven agent interaction domains: MCP/tool calling, search, terminal, software engineering, Android, web, and operating-system GUI. Unlike a standard chat or instruction model, it is not positioned as a fully autonomous agent but rather as a learned environment simulator: given an action history and a new tool or GUI action, it predicts the next observation or state. This release gives agent developers a practical tool for training, offline evaluation, synthetic trajectory generation, and sandbox testing without repeatedly invoking real tools, APIs, or GUIs. By using an efficient 3B-active MoE architecture instead of a full dense 35B model, it aims to deliver world-model capabilities at significantly lower compute and memory cost, which could lower the barrier to building robust agent training and evaluation pipelines. The model activates only about 3B of its 35B total parameters per token via MoE routing, so per-request compute and memory bandwidth are closer to a 3B dense model than a 35B one. It is explicitly framed as a world model rather than a chat or instruction-tuned model, with its sole role being to predict the next observation from action histories across heterogeneous domains such as MCP calls, terminal commands, Android GUI actions, and OS interactions.

reddit · r/LocalLLaMA · /u/nikhilprasanth · Jun 24, 05:52

**Background**: A language world model for agents is trained to predict what an environment will return (its next state or observation) given the current state and an action, complementing the policy model that decides which action to take. This separation lets developers train and evaluate agents offline, generate synthetic experience, or build sandbox environments without always hitting real tools or GUIs. The Model Context Protocol (MCP), introduced by Anthropic in November 2024, is an emerging open standard for connecting LLMs to external tools and data sources, and MCP/tool-calling is one of the seven domains this model simulates. Mixture of Experts (MoE) architectures split a model into many specialized sub-networks called experts and only activate a small subset per token via a routing layer, allowing large total parameter counts while keeping per-token compute and active memory much lower — a pattern now common in models such as DeepSeek and Gemma 4.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2606.24597">Qwen-AgentWorld: Language World Models for General Agents</a></li>
<li><a href="https://www.automataai.com.au/blog/moe-architecture-active-vs-total-parameters-explained">MoE Architecture: Active vs Total Parameters Explained</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#world-models`, `#agent-simulation`, `#qwen`, `#moe-architecture`, `#agent-development`

---

<a id="item-16"></a>
## [US Chip Security Act Mandates Location Tracking for AI Chips](https://www.reddit.com/r/LocalLLaMA/comments/1ue2fd7/seems_this_community_might_have_missed_it_bill/) ⭐️ 7.0/10

The Chip Security Act, a U.S. bill that would require location-tracking mechanisms for America's most advanced AI computing chips, has gained support from at least six companies. A U.S. senator introduced the bill, which would direct the Commerce Department to mandate location verification for export-controlled AI chips in order to prevent them from ending up in China. This legislation represents a significant escalation in U.S. efforts to control the global distribution of advanced AI hardware, potentially affecting chip availability, pricing, and supply chains for the open-source and local AI communities. If enacted, it could set a precedent for hardware-level surveillance on commercial semiconductors and reshape how AI compute resources are allocated globally. The bill specifically targets export-controlled AI chips and aims to close loopholes exploited by adversarial nations to obtain advanced semiconductors through intermediaries. Location tracking could be implemented at the hardware level (e.g., GPS or network-based verification), and the bill builds on existing Biden-era export controls from 2022 that prompted companies like Nvidia to create China-specific chips like the H20.

reddit · r/LocalLLaMA · /u/alex20_202020 · Jun 24, 03:35

**Background**: The U.S. has progressively tightened export controls on advanced semiconductors to China since 2022, restricting the sale of cutting-edge AI chips that could enhance China's military and AI capabilities. Companies like Nvidia have navigated these rules by designing compliant variants of their chips for the Chinese market. The Chip Security Act addresses a critical gap: even with export bans, chips can be diverted to restricted destinations through shell companies and smuggling. Location tracking would provide real-time verification that exported chips remain in approved locations, similar to how high-value goods or restricted weapons are tracked internationally.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nbcnews.com/tech/tech-news/chips-security-act-gains-industry-support-letter-rcna350500">Chips Security Act gains industry support: letter</a></li>
<li><a href="https://news.slashdot.org/story/25/05/09/1850212/us-senator-introduces-bill-calling-for-location-tracking-on-ai-chips-to-limit-china-access">US Senator Introduces Bill Calling For Location - Tracking on AI ...</a></li>
<li><a href="https://www.bbc.com/news/articles/cedy6gl99eno">Nvidia , the chip giant caught between the US and China</a></li>

</ul>
</details>

**Discussion**: The Reddit post itself is a cross-post noting that the r/LocalLLaMA community may have missed this news, with no original analysis or detailed discussion provided. The brief content only references related posts in r/politics and r/LocalLLM without summarizing community sentiment.

**Tags**: `#AI policy`, `#hardware regulation`, `#export controls`, `#AI chips`, `#national security`

---

<a id="item-17"></a>
## [Baidu Releases Unlimited-OCR with R-SWA for Multi-Page Transcription](https://www.reddit.com/r/LocalLLaMA/comments/1ueanx0/how_baidus_newly_released_unlimitedocr/) ⭐️ 7.0/10

Baidu released Unlimited-OCR, an end-to-end OCR model that uses Reference Sliding Window Attention (R-SWA) to transcribe dozens of pages in a single forward pass. The model is built on DeepSeek-OCR as a baseline, replacing its decoder attention layers with R-SWA while inheriting the encoder, 16x image compression, and MoE architecture (3B total parameters, 500M active per token). This addresses a fundamental limitation of end-to-end OCR models, where KV cache accumulation causes memory usage and latency to grow progressively with output length, making long-document processing increasingly expensive. By enabling efficient multi-page transcription in a single pass, Unlimited-OCR could streamline document digitization pipelines and reduce the need for page-by-page chunking and stitching commonly used in industry. R-SWA treats visual tokens as fixed reference tokens that remain fully visible to every generated token, while generated text only attends to a sliding window of the previous 128 tokens—mimicking how humans glance at surrounding context when copying. Baidu reports 93.92% on OmniDocBench v1.6, though this should be treated cautiously since DeepSeek-OCR was evaluated on v1.5 with slightly different conditions. The model is MIT licensed and available on Hugging Face and ModelScope.

reddit · r/LocalLLaMA · /u/Hour-Entertainer-478 · Jun 24, 11:17

**Background**: End-to-end OCR models encode an image into visual tokens and then generate text tokens one at a time, with each new token attending to all previously generated tokens via autoregressive decoding. This process requires storing key-value (KV) cache pairs for each transformer layer, so memory consumption grows linearly with output length—often making page 20 of a document far more expensive to process than page 1. Most production OCR pipelines work around this by chunking documents page by page and stitching results, but this loses cross-page context. DeepSeek-OCR, released earlier by DeepSeek, uses aggressive 16x image compression to encode a 1024×1024 page into roughly 256 visual tokens and serves as the encoder backbone for Unlimited-OCR.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/reference-sliding-window-attention-r-swa">Reference Sliding Window Attention ( R - SWA )</a></li>
<li><a href="https://www.digitalocean.com/community/tutorials/sliding-window-attention-efficient-long-context-models">Sliding Window Attention : Efficient Long-Context... | DigitalOcean</a></li>
<li><a href="https://mett29.github.io/posts/kv-cache/">What is the KV cache ? | Matt Log</a></li>

</ul>
</details>

**Discussion**: The Reddit submission on r/LocalLLaMA was authored by a user who read the original research paper and provided a clear technical breakdown. No specific community comments are available in the provided content, but the post attracted interest given its practical relevance and MIT-licensed open-source release.

**Tags**: `#OCR`, `#document-processing`, `#attention-mechanism`, `#Baidu`, `#long-context`

---

<a id="item-18"></a>
## [RubyLLM: Unified Ruby Framework for Major AI Providers](https://rubyllm.com/) ⭐️ 6.0/10

RubyLLM is a Ruby framework that provides a single, consistent interface for interacting with major AI providers including OpenAI, Anthropic, Claude, Gemini, and local models like Ollama. It requires only three lightweight dependencies—Faraday, Zeitwerk, and Marcel—and allows developers to build a working AI chat in minutes. For Ruby developers, RubyLLM eliminates the need to learn and maintain multiple provider-specific SDKs, offering an experience comparable to Vercel's AI SDK for the JavaScript ecosystem. This lowers the barrier to integrating AI features into Ruby and Rails applications, making multi-provider AI development more accessible. The framework is built on just three dependencies and abstracts provider differences so that switching between GPT, Claude, or local models requires minimal code changes. Community feedback highlights limitations including unreliable caching for xAI (completions API only), delayed native support for the Responses API, and challenges with trace-level observability and retry behavior that can obscure the true sequence of API calls.

hackernews · doener · Jun 24, 14:41 · [Discussion](https://news.ycombinator.com/item?id=48660711)

**Background**: Most AI providers (OpenAI, Anthropic, Google, etc.) ship their own bloated client libraries with inconsistent APIs, forcing developers to write provider-specific integration code. Unified frameworks like Vercel AI SDK for JavaScript and now RubyLLM for Ruby aim to abstract these differences behind a single interface. LLM observability refers to the practice of tracing and monitoring model requests—including inputs, context, reasoning chains, and outputs—which is essential for debugging, evaluating, and optimizing AI applications in production.

<details><summary>References</summary>
<ul>
<li><a href="https://rubyllm.com/">RubyLLM | One beautiful Ruby framework for all major AI providers .</a></li>
<li><a href="https://github.com/crmne/ruby_llm">crmne/ ruby _ llm : One delightful Ruby framework for every major AI ...</a></li>
<li><a href="https://galileo.ai/blog/understanding-llm-observability">Master LLM Observability for Peak AI Performance & Security</a></li>

</ul>
</details>

**Discussion**: The community is largely positive about RubyLLM's ease of use, with several developers praising it as comparable to Vercel's AI framework. However, users raised concrete technical concerns: caching issues with xAI's completions API, lack of native Responses API support (though this may have been recently added), and difficulties with trace observability and retry behavior that obscures the real sequence of API calls. One developer noted that Raix is an open-source gem built on top of RubyLLM's abstractions, indicating a growing ecosystem.

**Tags**: `#ruby`, `#ai-framework`, `#llm`, `#developer-tools`, `#multi-provider`

---

<a id="item-19"></a>
## [We’re making Bunny DNS free](https://bunny.net/blog/were-making-bunny-dns-free/) ⭐️ 6.0/10

Bunny.net has eliminated DNS query fees and now offers free DNS hosting for up to 500 domains, positioning as an EU-based Cloudflare alternative.

hackernews · dabinat · Jun 24, 08:50 · [Discussion](https://news.ycombinator.com/item?id=48657030)

**Tags**: `#dns`, `#bunny.net`, `#cloud-infrastructure`, `#cloudflare-alternative`, `#pricing-change`

---

<a id="item-20"></a>
## [PR Spam in Open Source Mirrors Early 2000s Email Spam](https://www.greptile.com/blog/prs-on-openclaw) ⭐️ 6.0/10

A blog post by Greptile draws a detailed analogy between the rising wave of PR (pull request) spam targeting open source repositories and the email spam crisis of the early 2000s, exploring whether solutions like sender reputation systems can be adapted to decentralized code collaboration on platforms like GitHub. PR spam—increasingly driven by AI-generated low-quality or malicious contributions—drowns maintainers in triage work, threatens the sustainability of critical open source projects, and risks pushing maintainers to lock down contributions, which could damage the open and collaborative culture of software development. Unlike email spam, where reputation is tied to organizations running mail servers (IPs and domains), PR spam involves individual users on decentralized platforms, making traditional reputation models harder to apply. GitHub has recently introduced configurable PR limits for maintainers as a partial mitigation, but a complete solution remains elusive.

hackernews · dakshgupta · Jun 24, 14:32 · [Discussion](https://news.ycombinator.com/item?id=48660579)

**Background**: Open source projects on platforms like GitHub rely on pull requests—proposed code changes submitted by contributors—for collaboration. As AI coding tools have become widely accessible, bad actors and opportunistic contributors have flooded popular repositories with automated, low-quality, or even malicious PRs, a phenomenon starkly illustrated by the Express.js spam PR incident. The early 2000s email spam problem was eventually addressed through a combination of IP/domain reputation, blacklists, and legal frameworks like CAN-SPAM, providing a useful historical lens for tackling the current crisis.

<details><summary>References</summary>
<ul>
<li><a href="https://socket.dev/blog/express-js-spam-prs-commoditization-of-open-source">Express.js Spam PRs Incident Highlights the Commoditization ..</a></li>

</ul>
</details>

**Discussion**: Commenters highlighted that email spam relied on organization-level reputation (IPs and domains), which doesn't translate cleanly to PR spam since each GitHub user acts independently. Others pointed to GitHub's new configurable PR limits as a partial fix, shared firsthand experience fighting email spam via CAN-SPAM enforcement, and proposed creative solutions such as token credit donations to maintainers and requiring new contributors to meet maintainers via non-textual (e.g., video) formats before merging their first PR.

**Tags**: `#open-source`, `#spam`, `#github`, `#developer-experience`, `#community-management`

---

<a id="item-21"></a>
## [Google Adds Computer Use to Gemini 3.5 Flash Amid Criticism](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-computer-use-gemini-3-5-flash/) ⭐️ 6.0/10

Google has introduced a computer use capability in Gemini 3.5 Flash, enabling the model to autonomously interact with computer interfaces by mimicking human actions. However, the announcement has been met with significant community criticism over misleading benchmark visualizations, overly aggressive guardrails, and practical task failures. This release intensifies the competitive race in agentic AI, where Anthropic pioneered computer use with Claude 3.5 Sonnet and OpenAI followed with GPT-5.4's native implementation. The credibility issues raised by the community highlight how benchmark presentation and real-world reliability remain critical challenges for AI agent deployment. Community members pointed out that in Google's own comparison graph, Gemini 3.5 Flash actually loses to both Opus 4.8 and GPT 5.5, yet the visualization is drawn in a way that implies Gemini wins. Users also reported that the Gemini app still lacks MCP (Model Context Protocol) support, and that overly conservative guardrails cause the model to refuse legitimate tasks like SIM transfer questions and code evaluation.

hackernews · swolpers · Jun 24, 17:21 · [Discussion](https://news.ycombinator.com/item?id=48662999)

**Background**: Computer use is an AI agent capability that allows models to autonomously control a computer interface—clicking buttons, typing text, and navigating applications—similar to how a human would. Anthropic first introduced this feature with Claude 3.5 Sonnet in late 2024, and it has since become a key competitive differentiator in the agentic AI space. MCP (Model Context Protocol) is an emerging standard that allows AI models to connect with external tools and data sources seamlessly. Benchmark graphs are a common way for AI companies to demonstrate model superiority, but how data is visualized can significantly influence perception even when raw numbers tell a different story.

<details><summary>References</summary>
<ul>
<li><a href="https://theoutpost.ai/news-story/anthropic-unveils-groundbreaking-computer-use-ai-for-autonomous-task-performance-7482/">Anthropic Unveils Groundbreaking ' Computer Use ' AI for Autonomous...</a></li>
<li><a href="https://agentx01.com/post/gpt-54-openai-computer-use-2026-03-07">OpenAI GPT-5.4: Native Computer Use , 1M Token Context | Agent X01</a></li>
<li><a href="https://inblog.ai/glossary/guardrails">What Are LLM Guardrails ? | GEO Glossary | inblog</a></li>

</ul>
</details>

**Discussion**: The community response was notably critical rather than celebratory. Users reported Gemini failing at simple tasks like PDF table extraction after multiple iterations, criticized the benchmark graph as misleading, highlighted the absence of MCP support as a significant gap, and complained about overly aggressive guardrails refusing legitimate requests. One commenter questioned the entire computer use paradigm as slow, insecure, error-prone, and expensive.

**Tags**: `#gemini`, `#google-ai`, `#computer-use`, `#ai-agents`, `#llm-benchmarks`

---

<a id="item-22"></a>
## [John Carmack Reflects on Early id Software Management Mistakes](https://twitter.com/ID_AA_Carmack/status/2069799283369345247) ⭐️ 6.0/10

John Carmack publicly reflected on his early management mistakes at id Software, admitting he pushed employees too hard by maintaining startup-level intensity even as the company matured. The resurfaced tweet prompted community members to share Sandy Petersen's own perspective on the demanding work environment. This reflection from one of the most influential figures in game development history offers rare, candid management wisdom about scaling a creative company sustainably. It resonates beyond gaming, touching on universal startup-to-mature-company transition challenges that many tech founders face. Carmack specifically noted that maturing companies need more slack and that running people at startup intensity constantly wears them out. The community referenced Sandy Petersen's interviews, including a Medium article and a YouTube interview, to provide the employee-side perspective that balances Carmack's management reflection.

hackernews · shadowtree · Jun 24, 15:56 · [Discussion](https://news.ycombinator.com/item?id=48661825)

**Background**: id Software was founded in 1991 by John Carmack, John Romero, Tom Hall, and Adrian Carmack, and is credited with creating the first-person shooter genre through Wolfenstein 3D (1992), Doom (1993), and Quake (1996). The development of Quake was notably troubled, resulting in major staffing changes by 2000 as several key figures from the Doom era departed the company. Sandy Petersen, known for his work on Doom and Quake, later shared his own accounts of the intense work culture in interviews.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Doom_(franchise)">Doom (franchise) - Wikipedia</a></li>
<li><a href="https://www.skulltag.com/id-software/">id Software – Skulltag.com</a></li>

</ul>
</details>

**Discussion**: The community responded with a mix of appreciation for Carmack's candor and acknowledgment that the intense culture produced legendary games like Quake. One commenter noted that Quake III Arena still felt innovative despite Doom 3 lacking the same energy, while others emphasized Quake's multiplayer, QuakeC modding system, and groundbreaking renderer as worth the human cost. Sandy Petersen's side of the story was highlighted as an important counterpoint to Carmack's management reflection.

**Tags**: `#game-development`, `#id-software`, `#john-carmack`, `#management`, `#tech-history`

---

<a id="item-23"></a>
## [GPT-5 Pro Helps Immunologist Solve 3-Year-Old T Cell Mystery](https://openai.com/index/gpt-5-immunology-mystery) ⭐️ 6.0/10

OpenAI published a case study claiming that GPT-5 Pro helped immunologist Derya Unutmaz resolve a three-year-old puzzle about T cell behavior that he had been unable to crack. The insight could have implications for research into cancer immunotherapy and autoimmune diseases. This case study illustrates how advanced AI reasoning models could meaningfully accelerate biomedical research by helping domain experts interpret complex biological data or generate novel hypotheses. If validated, it signals a new paradigm of AI-augmented scientific discovery where LLMs serve as collaborative research partners rather than mere writing or coding assistants. The report is published as an OpenAI promotional blog post rather than a peer-reviewed paper, so the specific mechanism by which GPT-5 Pro contributed and the biological details of the T cell finding have not yet been independently verified. GPT-5 Pro is the highest-capability reasoning tier of the GPT-5 model family, designed for complex multi-step problem solving rather than general chat use.

rss · OpenAI Blog · Jun 23, 17:00

**Background**: GPT-5 Pro is the top-tier variant of OpenAI's GPT-5 model family, offering enhanced reasoning capabilities compared to standard GPT-5. T cells are a critical component of the adaptive immune system, and 'T cell exhaustion' is a well-documented state in which T cells become dysfunctional due to chronic stimulation—this phenomenon is central to tumor immunology because exhausted T cells limit the effectiveness of cancer immunotherapy, and it also plays a role in chronic inflammation and autoimmune diseases. Unutmaz is a well-known immunologist whose work spans T cell biology and cancer immunology, making him a credible subject for such a case study.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-5/">Introducing GPT - 5 | OpenAI</a></li>
<li><a href="https://aiwiki.ai/wiki/gpt-5-pro">GPT - 5 Pro | AI Wiki</a></li>
<li><a href="https://www.frontiersin.org/journals/immunology/articles/10.3389/fimmu.2026.1841281/full">Frontiers | T - cell exhaustion in tumor immunology : mechanisms...</a></li>

</ul>
</details>

**Tags**: `#GPT-5`, `#AI-in-science`, `#immunology`, `#biomedical-research`, `#LLM-applications`

---

<a id="item-24"></a>
## [HuggingFace Ships huggingface_hub Weekly with AI-Assisted CI/CD](https://huggingface.co/blog/huggingface-hub-release-ci) ⭐️ 6.0/10

HuggingFace published a blog post detailing how they ship their huggingface_hub Python library on a weekly cadence using AI-assisted CI/CD pipelines, open tooling, and human-in-the-loop oversight. The post documents their engineering workflow as a practical case study for open source maintainers. This case study is significant for open source maintainers and DevOps engineers who want to adopt AI-augmented release workflows at scale. It demonstrates how a high-traffic ML infrastructure library can maintain a fast release cadence without sacrificing quality by combining automation with human review. The pipeline reportedly leverages AI to assist with tasks such as build prioritization, test selection, and deployment decisions, while human reviewers remain responsible for final validation. The post emphasizes the use of open tooling, making the workflow reproducible for other projects.

rss · HuggingFace Blog · Jun 23, 00:00

**Background**: The huggingface_hub library is the official Python client for the Hugging Face Hub, a platform that enables developers to share, download, and manage machine learning models, datasets, and other artifacts programmatically. CI/CD pipelines automate the steps from code commit to production deployment, including testing and building. AI-assisted CI/CD extends this by using AI to automate decisions such as which tests to run and which builds to prioritize. Human-in-the-loop refers to keeping humans engaged at key checkpoints in an otherwise automated process to catch errors and apply judgment that AI alone cannot.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/huggingface/huggingface_hub">GitHub - huggingface/ huggingface _ hub : The official Python client for...</a></li>
<li><a href="https://dev.to/agenticdevops/cicd-pipelines-how-your-code-goes-from-a-laptop-to-the-real-world-c76">CI / CD Pipelines : How Your Code Goes from... - DEV Community</a></li>
<li><a href="https://en.wikipedia.org/wiki/Human-in-the-loop">Human - in - the - loop - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#ci-cd`, `#release-engineering`, `#ai-assisted-development`, `#huggingface`, `#devops`

---

<a id="item-25"></a>
## [HuggingFace Experiments with Cross-Origin Storage API in Transformers.js](https://huggingface.co/blog/cross-origin-storage) ⭐️ 6.0/10

HuggingFace is experimenting with the proposed Cross-Origin Storage (COS) API in Transformers.js to improve how ML models are cached and loaded in the browser. Since the COS API is not yet natively implemented in any browser, they provide a Chrome extension that implements the proposed API so developers can test it today. Browser-based ML inference relies on downloading large model weights, which is slow and bandwidth-intensive. A standardized cross-origin storage mechanism would allow models to be cached once and reused across sites, dramatically reducing load times and enabling richer on-device AI experiences in web applications. The COS API is an early-stage WICG (Web Incubator Community Group) proposal that has not shipped in any browser; Emscripten also provides COS support as a progressive enhancement that falls back to standard fetch() when unavailable. Transformers.js runs inference using ONNX Runtime inside the browser, making efficient caching particularly impactful given that model files can be hundreds of megabytes.

rss · HuggingFace Blog · Jun 23, 00:00

**Background**: Transformers.js is a JavaScript port of HuggingFace's popular Python Transformers library, enabling pretrained models to run directly in the browser via ONNX Runtime. The Cross-Origin Storage API is a proposed web platform feature that would allow websites to store and share large resources (like ML models) across origins with user consent, addressing the lack of a standard cross-origin caching mechanism beyond the same-origin browser cache. Emscripten's adoption of the proposal signals broader interest from the WebAssembly and compiled-to-web ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/cross-origin-storage">Experimenting with the proposed Cross - Origin Storage API in...</a></li>
<li><a href="https://emscripten.org/docs/compiling/CrossOriginStorage.html">Cross - Origin Storage (COS) - Emscripten 6.0.2-git (dev) documentation</a></li>
<li><a href="https://medium.com/@kenzic/run-models-in-the-browser-with-transformers-js-2d0983ba3ce9">Run Models in the Browser With Transformers . js | by Chris... | Medium</a></li>

</ul>
</details>

**Tags**: `#transformers-js`, `#web-platform`, `#browser-ml`, `#cross-origin-storage`, `#huggingface`

---

<a id="item-26"></a>
## [Baidu Releases Unlimited-OCR: 3.3B MIT-Licensed Document Parsing Model](https://www.reddit.com/r/LocalLLaMA/comments/1ue51uk/unlimitedocr_is_now_on_modelscope_a_33b/) ⭐️ 6.0/10

Baidu has released Unlimited-OCR on ModelScope, a 3.3B-parameter multilingual OCR model under the MIT license that performs one-shot full-document parsing for single images, multi-page documents, and PDFs with 32K output length. The model supports both 'base' and 'gundam' image modes for different layouts, runs via Transformers inference with SGLang serving, and exposes an OpenAI-compatible streaming API. By offering full-document parsing in a single forward pass instead of the typical crop-then-OCR pipeline, Unlimited-OCR simplifies document AI workflows and reduces latency for long or multi-page inputs. The permissive MIT license and OpenAI-compatible serving make it practical for both researchers and production teams to self-host a capable OCR system without proprietary restrictions. Unlimited-OCR is built on the DeepSeek-OCR baseline and replaces all decoder attention layers with Reference Sliding Window Attention (R-SWA) to emulate human parsing working memory at constant memory cost. The 32K output length enables parsing of very long documents in one shot, while the two image modes let users trade resolution against context for different layout complexities.

reddit · r/LocalLLaMA · /u/Sporeboss · Jun 24, 05:53

**Background**: Traditional OCR systems typically detect text regions first, then crop and recognize each region separately—a pipeline that struggles with multi-page or complex-layout documents. DeepSeek-OCR pioneered a vision-language-model approach that reads an entire page and emits text-like output directly, treating OCR as a generative task. SGLang is an open-source, high-performance serving framework for LLMs and multimodal models that enables fast, scalable inference with features like RadixAttention. ModelScope is Alibaba-affiliated platform that hosts pretrained models for exploration, inference, and deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.xugj520.cn/en/archives/unlimited-ocr-constant-memory.html">Unlimited OCR : One-Shot Long-Horizon Document Parsing with...</a></li>
<li><a href="https://chat-deep.ai/models/deepseek-ocr/">DeepSeek OCR Guide: Setup, API, Benchmarks & OCR 2</a></li>
<li><a href="https://github.com/sgl-project/sglang">sgl-project/ sglang : SGLang is a high-performance serving framework ...</a></li>

</ul>
</details>

**Tags**: `#OCR`, `#document-parsing`, `#multilingual-models`, `#open-source`, `#ModelScope`

---

<a id="item-27"></a>
## [The Bank of Korea just released a report about AI productivity](https://www.reddit.com/r/LocalLLaMA/comments/1uecytz/the_bank_of_korea_just_released_a_report_about_ai/) ⭐️ 6.0/10

A Bank of Korea report finds that while AI saves workers about 1 hour per week, this time savings does not translate into actual productivity gains, as faster output leads to increased workload demands.

reddit · r/LocalLLaMA · /u/UsedMorning9886 · Jun 24, 13:04

**Tags**: `#AI productivity`, `#economic research`, `#Bank of Korea`, `#workplace AI`, `#Jevons paradox`

---

<a id="item-28"></a>
## [Developer Reverse-Engineers Windows Copilot into Free GPT-4 API](https://www.reddit.com/r/LocalLLaMA/comments/1uekiyp/i_reverse_engineered_windows_copilot_into_a_free/) ⭐️ 6.0/10

A developer has released an open-source tool that reverse-engineers Windows Copilot's backend and exposes it as a local OpenAI-compatible API at http://localhost:8000/v1. The tool logs into the user's Microsoft account once, persists the session, and provides drop-in GPT-4 access without API keys or billing. This offers hobbyists and developers a way to access GPT-4 capabilities for free through existing OpenAI SDKs, useful for automation, side projects, and lightweight workloads where burning real API credits is undesirable. However, the approach likely violates Microsoft's Terms of Service, risks account bans, and is inherently fragile since Microsoft can patch the underlying endpoints at any time. The tool supports streaming responses and multi-turn conversations, and is designed as a drop-in replacement that works with any OpenAI-compatible client. The author strongly recommends using a separate Microsoft account on a spare Windows machine rather than a primary account to mitigate ban risk, and explicitly disclaims any affiliation with Microsoft or commercial use.

reddit · r/LocalLLaMA · /u/whatisonearth · Jun 24, 17:47

**Background**: Windows Copilot is Microsoft's AI assistant built into Windows 11, providing free consumer access to large language models including GPT-4 without requiring a paid API plan. The OpenAI API has become the de facto standard interface for LLM-powered applications, with many third-party SDKs and tools built around its request and response schemas, which is why OpenAI-compatible local endpoints are so widely supported. Reverse-engineering consumer AI products to reuse their backend as a programmatic API is a common hobbyist practice, though it typically sits in a legal and ethical gray area regarding the product's Terms of Service.

<details><summary>References</summary>
<ul>
<li><a href="https://www.microsoft.com/en-us/windows/ai-features">AI Tools, Features, & Assistance in Windows 11 | Microsoft Windows</a></li>
<li><a href="https://lmstudio.ai/docs/developer/openai-compat">OpenAI Compatibility Endpoints | LM Studio</a></li>
<li><a href="https://developers.openai.com/api/reference/overview">API Overview | OpenAI API Reference</a></li>

</ul>
</details>

**Tags**: `#reverse-engineering`, `#openai-api`, `#gpt-4`, `#windows-copilot`, `#ai-tools`

---

<a id="item-29"></a>
## [Open-source browser extension runs SDXL image generation locally via WebGPU](https://www.reddit.com/r/LocalLLaMA/comments/1uemzsb/sdxl_running_locally_in_the_browser_on_webgpu/) ⭐️ 6.0/10

Developer d0grr released an open-source browser extension called "Generate AI Images" that runs SDXL-Lighting image generation entirely in the browser using WebGPU and ONNX, with no installation or virtual environment required. The extension is available on both Firefox and Chrome Web Store and currently supports SDXL-Lighting in fp16 (~7 GB) and 4-bit quantized (~3.6 GB) variants. This project demonstrates a zero-friction path to local AI image generation by eliminating the traditional setup burden of Python environments, ComfyUI workflows, or executable installers. It lowers the barrier for non-technical users who want to experiment with stable diffusion models privately on their own hardware, and showcases the growing maturity of WebGPU as a viable ML inference target. The extension reports that loading the model freezes the browser for about 10 seconds and generation also causes brief freezes, both attributed to synchronous WebGPU shader compilation within Chrome's GPU process—a limitation Web Workers cannot circumvent. Performance is modest at roughly 50–60 seconds per image on a 14-inch MacBook M4, and users need Chrome/Edge 122+ or the latest Firefox, plus approximately 8 GB VRAM for the fp16 model or 4–5 GB VRAM for the 4-bit variant.

reddit · r/LocalLLaMA · /u/xoqq · Jun 24, 19:15

**Background**: WebGPU is a low-level web API developed by the W3C as the successor to WebGL, designed to give JavaScript applications modern GPU compute capabilities comparable to Vulkan, Metal, and Direct3D 12. ONNX (Open Neural Network Exchange) is an open, interoperable format for representing machine learning models, allowing models trained in one framework to be deployed across different runtimes. SDXL-Lighting is a distilled version of Stable Diffusion XL that produces images in fewer denoising steps, making it more suitable for resource-constrained environments like browser-based inference.

<details><summary>References</summary>
<ul>
<li><a href="https://gpuweb.github.io/gpuweb/explainer/">WebGPU Explainer</a></li>
<li><a href="https://onnx.ai/">ONNX | Home</a></li>

</ul>
</details>

**Tags**: `#WebGPU`, `#SDXL`, `#Stable Diffusion`, `#ONNX`, `#Browser ML`

---

<a id="item-30"></a>
## [Italy's Domyn to Build 400B-Parameter EU Sovereign AI Model](https://www.reddit.com/r/LocalLLaMA/comments/1ue7cl5/new_eu_model_domyn_will_be_400b/) ⭐️ 6.0/10

Italian startup Domyn is developing a 400B-parameter sovereign AI model for the European Union as part of a project called the 'Frontier Grand Challenge.' The company already offers a closed 260B enterprise model (Domyn Large) and an open 10B model (Domyn Small) available on HuggingFace. This represents a significant European investment in frontier AI capabilities, signaling the EU's ambition to build sovereign alternatives to models from US and Chinese tech giants. A 400B-parameter model would compete at the frontier of current AI and could reduce European dependence on foreign AI systems for sensitive governmental and industrial applications. The 400B model has not yet been released, and publicly available technical details remain limited. Domyn Small is already open-weight on HuggingFace, while Domyn Large remains closed-source and restricted to enterprise customers.

reddit · r/LocalLLaMA · /u/Rick_06 · Jun 24, 08:08

**Background**: Sovereign AI refers to AI systems in which the underlying data, infrastructure, and model control reside within a specific jurisdiction, giving that entity full authority over how the AI operates and learns. Frontier AI models represent the most advanced, large-scale models available, capable of performing a wide variety of tasks at or beyond the level of any existing model. A 400B-parameter model would place Domyn in the same league as other frontier-scale systems such as Meta's Llama 4 Behemoth, Mistral Large, or DeepSeek V3, which have set the current bar for open and proprietary large language models.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/pulse/sovereign-ai-what-actually-means-why-conversation-we-having-scott-6hese">Sovereign AI : What It Actually Means, and Why the Conversation We...</a></li>
<li><a href="https://techglimmer.io/frontier-ai-review-2026-frontier-ai-models-2026/">What Is Frontier AI and Why Is Everyone Talking About It?</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llms">Best Open -Source LLM Models in 2026: Coding, Local, Agentic AI ...</a></li>

</ul>
</details>

**Tags**: `#EU-AI`, `#sovereign-AI`, `#large-language-models`, `#Domyn`, `#frontier-AI`

---