---
layout: default
title: "Horizon Summary: 2026-07-05 (ZH)"
date: 2026-07-05
lang: zh
---

> 从 49 条内容中筛选出 7 条重要资讯。

---

1. [LongCat 2.0（1.6T 参数，约 480 亿激活参数）权重现以 MIT 许可证开源](#item-1) ⭐️ 8.0/10
2. [Karpathy 发布 nanochat：仅需 100 美元训练 ChatGPT 级模型](#item-2) ⭐️ 7.0/10
3. [蒸馏版 LivePortrait 在浏览器中通过 WebGPU 达到 25fps](#item-3) ⭐️ 7.0/10
4. [长上下文基准测试揭示：预填充速度与 KV 头数量是智能体工作负载的关键](#item-4) ⭐️ 7.0/10
5. [问题不在于实体游戏还是数字游戏，而在于所有权](#item-5) ⭐️ 6.0/10
6. [编译器与语言设计导论（2021）](#item-6) ⭐️ 6.0/10
7. [高通发布 GenieX SDK，在 Windows ARM 笔记本上实现本地大模型推理](#item-7) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [LongCat 2.0（1.6T 参数，约 480 亿激活参数）权重现以 MIT 许可证开源](https://www.reddit.com/r/LocalLLaMA/comments/1unyvnz/longcat_20_16t_48b_active_weights_are_now_open/) ⭐️ 8.0/10

LongCat 2.0 是一个拥有 1.6T 参数、约 480 亿激活参数的混合专家（MoE）模型，现已以 MIT 许可证开源发布其权重。

reddit · r/LocalLLaMA · /u/Nunki08 · 7月5日 10:35

**标签**: `#open-source`, `#LLM`, `#Mixture-of-Experts`, `#model-release`, `#MIT-license`

---

<a id="item-2"></a>
## [Karpathy 发布 nanochat：仅需 100 美元训练 ChatGPT 级模型](https://github.com/karpathy/nanochat) ⭐️ 7.0/10

Andrej Karpathy 发布了 nanochat，这是一个开源的全栈大语言模型实现项目，目标是在仅 100 美元的计算成本内端到端训练出一个具备实用能力的类 ChatGPT 模型。该项目包含一个自动化的「speedrun」脚本，可在单台机器上完成从预训练到微调的全流程，transformer 宽度、学习率等超参数均会自动以最优方式计算。 该项目大幅降低了训练具备实用能力的大语言模型的门槛，表明前沿级 AI 开发可能很快不再只是资金充裕的大实验室的专利，个人研究者和小型团队也能参与其中。Karpathy 此前凭借 nanoGPT 和大量教学内容积累的声誉，使这一项目在引导社区探索低成本大模型训练方法方面具有重要影响力。 该仓库目前主要聚焦于调优消耗算力最多的预训练阶段，并设有一个「GPT-2 speedrun」排行榜，以训练到 GPT-2 级能力所需的实际训练时长为指标进行排名，能力通过 DCLM CORE 基准进行衡量。开发所用算力由 Lambda 提供，Alec Radford 担任顾问，Sofie 负责仓库管理。

github · karpathy · 7月4日 03:44

**背景**: nanochat 是 Karpathy 此前 nanoGPT 项目（2022 年末发布）的精神续作，后者提供了用于训练中等规模 GPT 模型的极简教学代码库。「nano」的命名风格强调极简与易用性，而 100 美元的训练目标代表着对极致低成本的大胆追求——相比之下，GPT-3 级别模型的训练成本通常高达数百万美元。「speedrun」概念借鉴自竞速游戏文化以及 modded-nanogpt 等类似项目，在这些项目中研究者竞相以最短训练时间达到指定能力水平。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy/nanochat: The best ChatGPT that $100 can buy. · GitHub</a></li>
<li><a href="https://github.com/karpathy/nanochat/discussions/1">Introducing nanochat: The best ChatGPT that $100 can buy. · karpathy/nanochat · Discussion #1</a></li>
<li><a href="https://medium.com/data-science-in-your-pocket/andrej-karpathys-nanochat-a-chatgpt-clone-for-100-8d052b219989">Andrej Karpathy’s NanoChat: A ChatGPT clone for $100 | by Mehul Gupta | Data Science in Your Pocket | Medium</a></li>

</ul>
</details>

**社区讨论**: 社区反应普遍热烈，许多开发者将 nanochat 视为推动大模型研究民主化的重要力量。GitHub 上的讨论主要围绕扩展 speedrun 脚本和改进预训练效率展开，更广泛的舆论则强调 Karpathy 将复杂机器学习概念转化为可运行、易上手代码的独特能力。

**标签**: `#AI`, `#LLM`, `#Karpathy`, `#cost-efficiency`, `#open-source`

---

<a id="item-3"></a>
## [蒸馏版 LivePortrait 在浏览器中通过 WebGPU 达到 25fps](https://www.reddit.com/r/LocalLLaMA/comments/1uodoli/liveportrait_distilled_model_that_can_run_at/) ⭐️ 7.0/10

一位开发者创建了 LivePortrait 的蒸馏版概念验证，可在一帧不到 30 毫秒的时间内生成人像动画帧，通过 WebGPU 在浏览器中完全实现 25fps 的实时性能，相比原先每帧需 30 秒的 ONNX 版本实现了巨大的速度提升。 这证明复杂的人像动画模型可以被压缩到在消费级硬件上的浏览器中实时运行，为零安装、保护隐私、无需服务器端 GPU 基础设施的虚拟形象/动画应用打开了大门。 该模型仅使用少量人像数据训练了数小时，因此输出质量被描述为「还行」，不同人像的效果也会有所差异。作者在 NVIDIA 5090 上进行了测试，并明确呼吁社区在不同 GPU 上进行基准测试，以评估实际可用性。

reddit · r/LocalLLaMA · /u/stephen_holograf · 7月5日 21:12

**背景**: LivePortrait 是 KlingAI Research 开源的人像动画系统，可以将驱动视频中的面部动作迁移到静态人像照片上。模型蒸馏是一种机器学习技术，将大型「教师」模型压缩为更小的「学生」模型，同时保留大部分能力，从而使推理更快、成本更低。WebGPU 是现代浏览器 API，通过 Vulkan、Metal 或 Direct3D 12 将系统 GPU 暴露给 Web 应用程序，使其能够在浏览器中直接运行高性能图形和机器学习任务，作为 WebGL 的继任者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/KlingAIResearch/LivePortrait">GitHub - KlingAIResearch/LivePortrait: Bring portraits to life! · GitHub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Knowledge_distillation">Knowledge distillation - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/WebGPU">WebGPU - Wikipedia</a></li>

</ul>
</details>

**标签**: `#LivePortrait`, `#model-distillation`, `#WebGPU`, `#browser-ml`, `#real-time-animation`

---

<a id="item-4"></a>
## [长上下文基准测试揭示：预填充速度与 KV 头数量是智能体工作负载的关键](https://www.reddit.com/r/LocalLLaMA/comments/1unrse9/i_benchmarked_13_models_at_65k128k_context_to/) ⭐️ 7.0/10

一位实践者在 RX 7900 XT 上使用 llama.cpp 对 13 个大语言模型（5 个稠密、6 个 MoE、1 个 Mamba2 混合、1 个 MLA MoE）进行了从 512 到 131K token 上下文长度的基准测试，发现在 65K 以上上下文时预填充（prompt 处理）占总耗时的 94–99%，且 KV 头数量比总参数量或 MoE 与稠密架构更能预测长上下文预填充的速度保持率。 这一发现挑战了以 token 生成速度（tg128）作为模型选择主要指标的惯例，并重新定义了本地智能体工作负载的优化优先级——在这些场景中工具调用响应通常很短但上下文窗口很大。在消费级 GPU 上运行本地编程智能体、RAG 流水线或工具调用工作流的实践者，应将基准测试的重心转向预填充吞吐量。 该 21 小时基准测试涵盖三种 KV 缓存量化等级（Q8_0 K/Q4_0 V、Q8_0/Q8_0、F16）以及纯预填充和提示+生成两种模式；Devstral-24B 无法完成 131K 测试（仅 KV 缓存就约 21GB），GLM-4.7-Flash 因 MLA 问题在 16K 以上崩溃；Trinity-Mini（MoE 3B/26B）在 131K 上下文下以 923 tok/s 的预填充速度领先。

reddit · r/LocalLLaMA · /u/linuxid10t · 7月5日 03:37

**背景**: 预填充（prefill）指的是将输入提示通过大语言模型进行的初始处理，与逐 token 自回归生成输出的解码步骤相对。KV 缓存存储先前 token 的键值注意力状态，避免模型在生成过程中重复计算，其内存大小随序列长度、层数和注意力头数量线性扩展。智能体工作负载——即大语言模型编排工具调用、代码生成或检索增强查询的场景——通常涉及庞大的上下文窗口但输出较短，使得预填充阶段成为主要开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/not-lain/kv-caching">KV Caching Explained: Optimizing Transformer Inference Efficiency</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#benchmarking`, `#long-context`, `#agentic-ai`, `#kv-cache`

---

<a id="item-5"></a>
## [问题不在于实体游戏还是数字游戏，而在于所有权](https://popcar.bearblog.dev/its-about-ownership/) ⭐️ 6.0/10

这篇博文认为，数字游戏的核心问题并非发行形式的实体化或数字化，而是玩家失去了真正的所有权。此观点引发了关于数字版权管理（DRM）、消费者权益以及游戏行业实践的大量讨论。

hackernews · popcar2 · 7月5日 14:56 · [社区讨论](https://news.ycombinator.com/item?id=48794750)

**标签**: `#digital-ownership`, `#gaming`, `#DRM`, `#consumer-rights`, `#software-distribution`

---

<a id="item-6"></a>
## [编译器与语言设计导论（2021）](https://dthain.github.io/books/compiler/) ⭐️ 6.0/10

Thain 博士编写的一本免费在线编译器设计教材，以实践项目为基础介绍如何构建一个 C 风格编译器，社区反响总体积极，但也因内容范围较窄而受到一些批评。

hackernews · AlexeyBrin · 7月5日 11:54 · [社区讨论](https://news.ycombinator.com/item?id=48793454)

**标签**: `#compilers`, `#education`, `#language-design`, `#textbook`, `#self-study`

---

<a id="item-7"></a>
## [高通发布 GenieX SDK，在 Windows ARM 笔记本上实现本地大模型推理](https://www.reddit.com/r/LocalLLaMA/comments/1uo9z3c/qualcomm_launches_geniex_to_run_llms_on_their/) ⭐️ 6.0/10

高通发布了 GenieX SDK，通过 llama.cpp 支持 GGUF 模型，可在 Windows ARM 笔记本上实现本地大模型推理。早期基准测试显示，Gemma 3 26B 可达 20 tokens/秒，Qwen 3 27B（多 token 预测）可达 10 tok/s，使用 GPU 或 NPU 加速时首 token 延迟为 0.5 秒。 这为本地大模型用户提供了一个超越 NVIDIA 和 AMD GPU 的新硬件选项，特别是针对 Windows ARM 生态系统——此前该领域一直由 Apple Silicon 占据主导。它降低了在设备端完全运行开源大模型的门槛，无需依赖云端。 该 SDK 可在任何 Q4_0 量化的 GGUF 模型上运行，支持 CPU、GPU 或 NPU，以 llama.cpp 作为推理后端。性能因模型而异：Gemma 3 26B 可达 20 tok/s，而带有多 token 预测的 Qwen 3 27B 仅达 10 tok/s，表明吞吐量因模型架构和功能支持而差异显著。

reddit · r/LocalLLaMA · /u/DerpSenpai · 7月5日 18:43

**背景**: 高通是 Windows 笔记本 ARM 处理器（通过其 Snapdragon X 系列）的主要供应商，在端侧 AI 领域被视为 Apple M 系列芯片的天然竞争对手。llama.cpp 是一个广泛使用的开源 C++ 推理引擎，支持 GGUF 格式模型——后者已成为量化开源大模型的事实标准。由于隐私、成本和延迟方面的优势，在消费级硬件上本地运行大模型正变得越来越流行。

**标签**: `#Qualcomm`, `#local-llm`, `#edge-inference`, `#Windows-ARM`, `#llama.cpp`

---