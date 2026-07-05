---
layout: default
title: "Horizon Summary: 2026-07-05 (EN)"
date: 2026-07-05
lang: en
---

> From 49 items, 7 important content pieces were selected

---

1. [longcat 2.0 (1.6T, ~48B active) weights are now open under MIT license](#item-1) ⭐️ 8.0/10
2. [Karpathy Launches nanochat: A ChatGPT Clone for $100](#item-2) ⭐️ 7.0/10
3. [Distilled LivePortrait Runs at 25fps in Browser via WebGPU](#item-3) ⭐️ 7.0/10
4. [Long-context benchmark reveals prefill speed and KV head count dominate agentic LLM performance](#item-4) ⭐️ 7.0/10
5. [It's not about physical vs. digital games, it's about ownership](#item-5) ⭐️ 6.0/10
6. [Introduction to Compilers and Language Design (2021)](#item-6) ⭐️ 6.0/10
7. [Qualcomm launches GenieX SDK for local LLM inference on Windows ARM laptops](#item-7) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [longcat 2.0 (1.6T, ~48B active) weights are now open under MIT license](https://www.reddit.com/r/LocalLLaMA/comments/1unyvnz/longcat_20_16t_48b_active_weights_are_now_open/) ⭐️ 8.0/10

LongCat 2.0, a 1.6T parameter MoE model with ~48B active parameters, has been released with open weights under the MIT license.

reddit · r/LocalLLaMA · /u/Nunki08 · Jul 5, 10:35

**Tags**: `#open-source`, `#LLM`, `#Mixture-of-Experts`, `#model-release`, `#MIT-license`

---

<a id="item-2"></a>
## [Karpathy Launches nanochat: A ChatGPT Clone for $100](https://github.com/karpathy/nanochat) ⭐️ 7.0/10

Andrej Karpathy released nanochat, an open-source full-stack LLM implementation designed to train a capable ChatGPT-like model end-to-end for only $100 in compute costs. The project includes an automated 'speedrun' script that handles everything from pretraining to fine-tuning on a single machine, with hyperparameters like transformer width and learning rates calculated automatically. This project dramatically lowers the barrier to entry for training capable language models, suggesting that frontier-quality AI development may soon be accessible to individual researchers and small teams, not just well-funded labs. Karpathy's track record with nanoGPT and educational content gives this initiative significant credibility and influence in shaping how the community approaches cost-efficient LLM training. The repo currently focuses on tuning the pretraining stage, which consumes the most compute, and features a 'GPT-2 speedrun' leaderboard ranking submissions by wall-clock training time to reach GPT-2 grade capability as measured by the DCLM CORE benchmark. Compute for development was provided by Lambda, and the project was advised by Alec Radford with repo management by Sofie.

github · karpathy · Jul 4, 03:44

**Background**: nanochat is a spiritual successor to Karpathy's earlier nanoGPT project (released in late 2022), which provided a minimal, educational codebase for training medium-sized GPT models. The 'nano' naming convention emphasizes minimalism and accessibility, while the $100 target represents an extreme push toward cost-efficiency—training GPT-3-scale models typically costs millions of dollars. The 'speedrun' concept is borrowed from competitive gaming culture and similar efforts like the modded-nanogpt repo, where researchers compete to minimize training time for a given capability level.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy/nanochat: The best ChatGPT that $100 can buy. · GitHub</a></li>
<li><a href="https://github.com/karpathy/nanochat/discussions/1">Introducing nanochat: The best ChatGPT that $100 can buy. · karpathy/nanochat · Discussion #1</a></li>
<li><a href="https://medium.com/data-science-in-your-pocket/andrej-karpathys-nanochat-a-chatgpt-clone-for-100-8d052b219989">Andrej Karpathy’s NanoChat: A ChatGPT clone for $100 | by Mehul Gupta | Data Science in Your Pocket | Medium</a></li>

</ul>
</details>

**Discussion**: The community response has been largely enthusiastic, with many developers viewing nanochat as a democratizing force for LLM research. Discussions on GitHub center on extending the speedrun script and improving pretraining efficiency, while broader sentiment highlights Karpathy's unique ability to translate complex ML concepts into accessible, runnable code.

**Tags**: `#AI`, `#LLM`, `#Karpathy`, `#cost-efficiency`, `#open-source`

---

<a id="item-3"></a>
## [Distilled LivePortrait Runs at 25fps in Browser via WebGPU](https://www.reddit.com/r/LocalLLaMA/comments/1uodoli/liveportrait_distilled_model_that_can_run_at/) ⭐️ 7.0/10

A developer created a proof-of-concept distilled version of LivePortrait that generates portrait animation frames in under 30ms, enabling real-time 25fps performance entirely in the browser via WebGPU — a dramatic speedup from the original ONNX version that took 30 seconds per frame. This demonstrates that complex portrait animation models can be compressed enough to run in real time on consumer hardware inside a web browser, opening the door to zero-install, privacy-preserving, and widely accessible avatar/animation applications without requiring server-side GPU infrastructure. The model was trained on a small number of portraits for only a few hours, so output quality is described as 'just ok' and performance varies across portraits. The author tested on an NVIDIA 5090 and is explicitly requesting community benchmarking across different GPUs to gauge real-world viability.

reddit · r/LocalLLaMA · /u/stephen_holograf · Jul 5, 21:12

**Background**: LivePortrait is an open-source portrait animation system from KlingAI Research that transfers facial movements from a driving video onto a still portrait photo. Model distillation is a machine learning technique that compresses a large 'teacher' model into a smaller 'student' model while preserving much of its capability, making inference faster and cheaper. WebGPU is a modern browser API that exposes a system's GPU (via Vulkan, Metal, or Direct3D 12) to web applications, enabling high-performance graphics and ML workloads directly in the browser as a successor to WebGL.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/KlingAIResearch/LivePortrait">GitHub - KlingAIResearch/LivePortrait: Bring portraits to life! · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#LivePortrait`, `#model-distillation`, `#WebGPU`, `#browser-ml`, `#real-time-animation`

---

<a id="item-4"></a>
## [Long-context benchmark reveals prefill speed and KV head count dominate agentic LLM performance](https://www.reddit.com/r/LocalLLaMA/comments/1unrse9/i_benchmarked_13_models_at_65k128k_context_to/) ⭐️ 7.0/10

A practitioner benchmarked 13 LLMs (5 dense, 6 MoE, 1 Mamba2 hybrid, 1 MLA MoE) at context lengths from 512 to 131K tokens on an RX 7900 XT using llama.cpp, finding that prefill (prompt processing) accounts for 94–99% of wall-clock time at 65K+ context, and that KV head count is a stronger predictor of long-context prefill retention than total parameter count or MoE vs dense architecture. This challenges the conventional focus on token generation speed (tg128) as the headline metric for choosing models, and reframes optimization priorities for local agentic workloads—where tool-use responses are typically short but context windows are large. Practitioners running local coding agents, RAG pipelines, or tool-use workflows on consumer GPUs should reweight their benchmarks toward prefill throughput. The 21-hour benchmark covered three KV cache quant tiers (Q8_0 K/Q4_0 V, Q8_0/Q8_0, F16) and both pure prefill and prompt+generation modes; Devstral-24B could not complete 131K (KV cache alone ~21GB) and GLM-4.7-Flash crashed above 16K due to an MLA issue; Trinity-Mini (MoE 3B/26B) led prefill at 923 tok/s at 131K context.

reddit · r/LocalLLaMA · /u/linuxid10t · Jul 5, 03:37

**Background**: Prefill refers to the initial processing of an input prompt through an LLM, as opposed to the autoregressive decode step that generates output tokens one at a time. KV cache stores the key-value attention states from previous tokens so the model doesn't recompute them during generation, and its memory size scales with sequence length, number of layers, and number of attention heads. Agentic workloads—where an LLM orchestrates tool calls, code generation, or retrieval-augmented queries—typically involve massive context windows but produce short outputs, making the prefill phase the dominant cost.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/not-lain/kv-caching">KV Caching Explained: Optimizing Transformer Inference Efficiency</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#benchmarking`, `#long-context`, `#agentic-ai`, `#kv-cache`

---

<a id="item-5"></a>
## [It's not about physical vs. digital games, it's about ownership](https://popcar.bearblog.dev/its-about-ownership/) ⭐️ 6.0/10

A blog post arguing that the core issue with digital games isn't physical vs. digital distribution but the loss of true ownership rights, sparking substantial discussion on DRM, consumer rights, and gaming industry practices.

hackernews · popcar2 · Jul 5, 14:56 · [Discussion](https://news.ycombinator.com/item?id=48794750)

**Tags**: `#digital-ownership`, `#gaming`, `#DRM`, `#consumer-rights`, `#software-distribution`

---

<a id="item-6"></a>
## [Introduction to Compilers and Language Design (2021)](https://dthain.github.io/books/compiler/) ⭐️ 6.0/10

A free online textbook on compiler design from Dr. Thain that provides a practical, project-based introduction to building a C-style compiler, with mostly positive community reception but some criticism for its narrow focus.

hackernews · AlexeyBrin · Jul 5, 11:54 · [Discussion](https://news.ycombinator.com/item?id=48793454)

**Tags**: `#compilers`, `#education`, `#language-design`, `#textbook`, `#self-study`

---

<a id="item-7"></a>
## [Qualcomm launches GenieX SDK for local LLM inference on Windows ARM laptops](https://www.reddit.com/r/LocalLLaMA/comments/1uo9z3c/qualcomm_launches_geniex_to_run_llms_on_their/) ⭐️ 6.0/10

Qualcomm has launched the GenieX SDK, enabling local LLM inference on Windows ARM laptops via llama.cpp with GGUF model support. Early benchmarks show 20 tokens/second on Gemma 3 26B and 10 tok/s on Qwen 3 27B with Multi-Token Prediction, with a first-token latency of 0.5 seconds using GPU or NPU acceleration. This gives local LLM users a new hardware option beyond NVIDIA and AMD GPUs, specifically targeting the Windows ARM ecosystem where Apple Silicon has dominated. It lowers the barrier for running capable open-weight models entirely on-device without cloud dependencies. The SDK runs any Q4_0 quantized GGUF model on CPU, GPU, or NPU, leveraging llama.cpp as the inference backend. Performance is model-dependent: Gemma 3 26B hits 20 tok/s while Qwen 3 27B with MTP only reaches 10 tok/s, suggesting throughput varies significantly based on model architecture and feature support.

reddit · r/LocalLLaMA · /u/DerpSenpai · Jul 5, 18:43

**Background**: Qualcomm is the dominant supplier of ARM-based processors for Windows laptops (via its Snapdragon X series), positioning it as a natural competitor to Apple's M-series chips in the on-device AI space. llama.cpp is a widely used open-source C++ inference engine that supports GGUF format models, the de facto standard for quantized open-weight LLMs. Running LLMs locally on consumer hardware has become increasingly popular due to privacy, cost, and latency benefits compared to cloud APIs.

**Tags**: `#Qualcomm`, `#local-llm`, `#edge-inference`, `#Windows-ARM`, `#llama.cpp`

---