---
layout: default
title: "Horizon Summary: 2026-07-09 (ZH)"
date: 2026-07-09
lang: zh
---

> 从 66 条内容中筛选出 26 条重要资讯。

---

1. [OpenAI 发布 GPT-5.6：提升 Token 效率并在 ARC-AGI-3 取得 SOTA](#item-1) ⭐️ 9.0/10
2. [欧洲议会通过《聊天监控 1.0》法案](#item-2) ⭐️ 8.0/10
3. [OpenAI 揭示 SWE-Bench Pro 编码基准测试的可靠性问题](#item-3) ⭐️ 8.0/10
4. [OpenAI 发布 GPT-Live，新一代实时语音模型](#item-4) ⭐️ 8.0/10
5. [FlashAttention-3/4 优化无法迁移到 RTX 消费级 GPU](#item-5) ⭐️ 8.0/10
6. [Muse Spark 1.1](#item-6) ⭐️ 7.0/10
7. [NVIDIA 发布用于 AI 智能体训练的开放数据集](#item-7) ⭐️ 7.0/10
8. [HuggingFace 为 Transformers 添加原生 vLLM 后端](#item-8) ⭐️ 7.0/10
9. [OpenMed 1.8：Apache-2.0 临床去识别，完全本地运行，现已支持 Android、iOS 和浏览器。想参与 1.9 版本？这里有 400+ 个开放问题](#item-9) ⭐️ 7.0/10
10. [Dify 1.16.0-rc1 实验性推出基于 Linux 沙箱的 Dify Agent](#item-10) ⭐️ 6.0/10
11. [Show HN：让 GLM 5.2 在我这台慢速电脑上运行起来](#item-11) ⭐️ 6.0/10
12. [Hy3](#item-12) ⭐️ 6.0/10
13. [IERS 确认 2026 年 12 月底不引入闰秒](#item-13) ⭐️ 6.0/10
14. [玻璃脊梁：为何美国陆军的后勤体系将在下一场战争中崩溃](#item-14) ⭐️ 6.0/10
15. [GLM 5.2 的准确度几乎与人类簿记员相当](#item-15) ⭐️ 6.0/10
16. [内部服务 TLS 证书配置实践指南](#item-16) ⭐️ 6.0/10
17. [OpenAI 将 ChatGPT 与 Codex 合并为统一的「ChatGPT Work」应用](#item-17) ⭐️ 6.0/10
18. [GPT-5.6 成为 Microsoft 365 Copilot 的首选模型](#item-18) ⭐️ 6.0/10
19. [GPT-5.5 生物安全漏洞赏金计划](#item-19) ⭐️ 6.0/10
20. [OpenAI 阐述其政府与国家安全合作原则](#item-20) ⭐️ 6.0/10
21. [本科生一作论文实现 7.92 倍投机解码加速](#item-21) ⭐️ 6.0/10
22. [现在兄弟们，我们总算知道自己为啥这么惨了](#item-22) ⭐️ 6.0/10
23. [Puzzle-75B-A9B NVFP4 在 3×3090 上达 132 t/s，凸显开源模型尺寸断层](#item-23) ⭐️ 6.0/10
24. [Reasoning-Medical0.1-27B（基于 Qwen3.5-27B 的医疗微调模型，声称超越 MedGemma）](#item-24) ⭐️ 6.0/10
25. [OpenMOSS-Team/MOSS-Transcribe-Diarize · Hugging Face](#item-25) ⭐️ 6.0/10
26. [MiMo v2.5 在 192GB 显存本地推理基准测试中表现亮眼](#item-26) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI 发布 GPT-5.6：提升 Token 效率并在 ARC-AGI-3 取得 SOTA](https://openai.com/index/gpt-5-6/) ⭐️ 9.0/10

OpenAI 发布了 GPT-5.6，这是一款新的前沿模型，强调每个 Token 的更高智能、更强的性价比以及面向开发者的增强功能，例如更好的意图推断和保留原始图像尺寸。GPT-5.6 Sol 在 ARC-AGI-3 交互式推理基准上创下新的最先进水平，得分 7.8%，成为首个在 ARC-AGI-3 游戏中击败人类水平的前沿模型。 此次发布延续了前沿模型的快速迭代节奏，并加剧了与 Anthropic Claude Code 的竞争，尤其是在编程 Agent 工作流方面。ARC-AGI-3 的成绩具有重要意义，因为该基准旨在抵抗记忆化并测试流式的交互式推理能力——此前的前沿模型在该基准上得分低于 1%——这表明在更困难的推理任务上取得了可衡量的进展。 开发者指南突出了两项显著能力：(1) 改进的意图理解，GPT-5.6 能够在无需逐步提示的情况下推断用户的潜在目标，但仍建议用户明确说明约束条件和审批边界；(2) 保留视觉输入的原始图像尺寸。批评者指出，OpenAI 在 GeneBench 和 LifeSciBench 对比中排除了「Fable 5」，理由据称是「它无法回答高级生物学问题并拒绝该评测中的大多数问题」，引发了关于精选基准的质疑。

hackernews · OpenAI Blog · 7月9日 17:04 · [社区讨论](https://news.ycombinator.com/item?id=48849066)

**背景**: 前沿模型是指在特定时期能力最强、最通用的 AI 系统，通常在极大规模上训练，并展现出高级推理和零样本学习等涌现能力。ARC-AGI-3 于 2026 年 3 月发布，是一个交互式推理基准，由数百个手工设计的回合制游戏式环境组成，没有说明、没有规则、没有明确目标——旨在测试智能体是否能探索新环境、即时推断目标、构建可适应的世界模型并持续学习。截至 2026 年初，前沿模型在 ARC-AGI-3 上的得分低于 1%，而人类玩家可以解决这些游戏，因此任何非平凡的得分都值得关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi/3">ARC-AGI-3</a></li>
<li><a href="https://arcprize.org/blog/arc-agi-3-launch">Announcing ARC-AGI-3 - ARC Prize</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work - NVIDIA</a></li>

</ul>
</details>

**社区讨论**: 社区情绪褒贬不一但参与度很高。开发者赞赏开发者指南中的实际改进（意图推断、图像尺寸保留），而 ARC-AGI-3 的关注者则将 Sol 得分 7.8% 视为交互式推理领域的重要里程碑。长期使用 Claude Code 的用户讨论了是否应该转向 Codex，表明对 Anthropic 形成了竞争压力。批评者指责 OpenAI 通过在生物学评估中排除 Fable 5 来精选基准，一条半开玩笑的评论则捕捉了社区对 OpenAI 相对于 Anthropic 矛盾心态。

**标签**: `#OpenAI`, `#GPT-5`, `#LLM`, `#frontier-models`, `#AI-release`

---

<a id="item-2"></a>
## [欧洲议会通过《聊天监控 1.0》法案](https://www.patrick-breyer.de/en/eu-parliament-greenlights-chat-control-1-0-breyer-our-children-lose-out/) ⭐️ 8.0/10

欧洲议会批准了《聊天监控 1.0》法案，允许在 2028 年前对 Discord、Instagram、Gmail 和 iCloud 等平台上的私人信息进行无证大规模扫描。该法案借助程序性策略获通过——要求绝对多数票才能否决，而非通过法案。

hackernews · rapnie · 7月9日 11:03 · [社区讨论](https://news.ycombinator.com/item?id=48843923)

**标签**: `#privacy`, `#EU-regulation`, `#mass-surveillance`, `#digital-rights`, `#encryption`

---

<a id="item-3"></a>
## [OpenAI 揭示 SWE-Bench Pro 编码基准测试的可靠性问题](https://openai.com/index/separating-signal-from-noise-coding-evaluations) ⭐️ 8.0/10

OpenAI 发布了一项分析报告，指出广泛使用的 AI 编码能力评估基准 SWE-Bench Pro 存在可靠性和准确性问题。该分析对 AI 模型在真实软件工程任务上的评估方式提出了质疑，并强调了可能扭曲模型性能比较的方法论缺陷。 像 SWE-Bench Pro 这样的编码基准是衡量 AI 在软件工程领域进展的基础，其完整性直接影响研究方向、模型开发重点以及关于 AI 能力的声明。如果一个流行的基准产生噪声大或不可靠的信号，整个社区就有可能错误分配精力并对模型的改进得出错误结论。 该分析专门针对 SWE-Bench Pro，它是原始 SWE-Bench 基准的更具挑战性的变体，旨在通过真实 GitHub 问题来测试模型。所发现的问题可能涉及评分方法、数据集污染风险或评估结果的方差，这些问题使得区分模型的真正进步与随机噪声变得困难。

rss · OpenAI Blog · 7月8日 13:00

**背景**: SWE-Bench 最初由普林斯顿大学的研究人员提出，是一个通过真实 GitHub 仓库中实际软件工程任务来评估大语言模型解决能力的基准。SWE-Bench Pro 是该基准的演进版本，旨在更加严谨并抵御数据污染，因此成为评估前沿编码模型的首选工具。这类基准的可靠性至关重要，因为它们是 AI 公司衡量和宣传其模型编码能力的主要标尺。

**标签**: `#benchmarks`, `#evaluation`, `#AI-research`, `#OpenAI`, `#SWE-Bench`

---

<a id="item-4"></a>
## [OpenAI 发布 GPT-Live，新一代实时语音模型](https://openai.com/index/introducing-gpt-live) ⭐️ 8.0/10

2026 年 7 月 8 日，OpenAI 发布了 GPT-Live 和 GPT-Live mini，这是一代全新的全双工语音模型，能够同时听和说，现已为 ChatGPT Voice 提供支持。OpenAI 同时推出了 GPT-Realtime-Translate 实时翻译模型，支持 70 多种输入语言和 13 种输出语言。 此次发布标志着向真正自然、类人化的 AI 语音交互迈出了重要一步，解决了延迟、轮换发言和对话流畅性方面的长期痛点。随着 Google、Anthropic 等竞争对手竞相改进语音 AI，GPT-Live 让 OpenAI 在这个竞争日益激烈、商业价值日益重要的领域保持领先地位。 GPT-Live 是一个全双工模型，意味着它可以在生成回复的同时处理用户的语音输入，而无需等待用户说完。OpenAI 还提供了较小的 GPT-Live mini 版本；ChatGPT Voice 目前提供 22 种神经 TTS 语音，支持调节语速并提供实时文字转录。

rss · OpenAI Blog · 7月8日 00:00

**背景**: 传统的语音助手通常采用回合制流水线：用户说话→语音转文字→语言模型处理→文字转语音（TTS）。这种流水线会引入明显的延迟，听起来往往不够自然。全双工语音模型旨在消除这种延迟，让 AI 能够像真人对话一样同时听和说。ChatGPT Voice 于 2023 年上线，此后逐步更新，语音越来越自然、功能越来越丰富。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/advancing-voice-intelligence-with-new-models-in-the-api/">Advancing voice intelligence with new models in the API - OpenAI</a></li>
<li><a href="https://techcrunch.com/2026/07/08/openai-releases-new-voice-models-for-more-natural-live-conversations/">OpenAI releases new voice models for more natural live ...</a></li>
<li><a href="https://theaidude.net/blog/gpt-live-openais-new-real-time-voice-models-explained">GPT-Live: OpenAI's Real-Time Voice Models Explained</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#voice-AI`, `#ChatGPT`, `#conversational-AI`, `#speech-models`

---

<a id="item-5"></a>
## [FlashAttention-3/4 优化无法迁移到 RTX 消费级 GPU](https://www.reddit.com/r/LocalLLaMA/comments/1urucz1/exploring_flashattention34_optimizations_on_rtx/) ⭐️ 8.0/10

一位开发者从零重建了注意力内核，测试 FlashAttention-3 和 FA-4 的优化能否应用于消费级 RTX GPU，在 RTX 5090 上达到与 FA-2 持平的 206μs 性能，但未能获得实质性提速。实验表明，FA-3/4 的关键优化手段——WGMMA 张量核指令、Warp 特化、TMA 以及基于 FMA 的 exp 模拟——要么在消费级芯片上根本不存在，要么因为瓶颈在张量管道而非内存传输或特殊函数单元而起不到作用。 这对在消费级硬件上运行大语言模型推理的社区非常重要，因为 vLLM 和 SGLang 在消费卡上已经回退到 FA-2，社区此前并不确定是否还有进一步优化空间。FA-2 实际即为性能上限这一明确结论，可以避免研究者在死胡同上浪费时间，同时也暗示未来在 RTX 上的性能提升需要以牺牲精度为代价来使用更快的低精度张量核。 测试在 RTX 5090 上使用 batch=1、heads=8、seq_len=4096、head_dim=64 的配置；Warp 特化反而降低了性能（213 微秒 vs 206 微秒）；即便是用 exp2f 替代 expf 这种基础优化也几乎没有效果；该分析仅针对 prefill/计算密集场景，而面向大 KV cache 的内存受限解码则是另一个问题，主要由 split-KV/Flash-Decoding 等技术主导。

reddit · r/LocalLLaMA · /u/NoVibeCoding · 7月9日 15:56

**背景**: FlashAttention 通过分块计算并将中间值保存在片上高速 SRAM 中而非缓慢的 HBM，将显存占用降至 O(N) 并带来 2-4 倍加速；FlashAttention-2 已广泛部署，而 FlashAttention-3 主要面向 NVIDIA Hopper（H100）数据中心 GPU，利用 WGMMA（Warpgroup 矩阵乘累加）异步张量核指令和 TMA（张量内存加速器）等新硬件特性。WGMMA 是 Hopper 独有的指令族，由 128 个线程（一个 warpgroup）协作发起单条异步 D=A×B+C 矩阵乘累加，TMA 则是专用硬件单元，可在不占用线程执行资源的情况下完成全局内存与共享内存之间的数据搬运——两者都是 FA-3 提速的核心，但在消费级 RTX 上要么不可用，要么收益有限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://localaimaster.com/blog/flash-attention-guide">FlashAttention Guide 2026: FA-2, FA-3, Hopper Optimizations ...</a></li>
<li><a href="https://research.colfax-intl.com/cutlass-tutorial-wgmma-hopper/">CUTLASS Tutorial: Fast Matrix-Multiplication with WGMMA on ...</a></li>
<li><a href="https://research.colfax-intl.com/tutorial-hopper-tma/">CUTLASS Tutorial: Mastering the NVIDIA® Tensor Memory Accelerator (TMA) - Colfax Research</a></li>

</ul>
</details>

**标签**: `#flash-attention`, `#gpu-optimization`, `#rtx`, `#cuda-kernels`, `#llm-inference`

---

<a id="item-6"></a>
## [Muse Spark 1.1](https://ai.meta.com/blog/introducing-muse-spark-meta-model-api/) ⭐️ 7.0/10

Meta 发布了其代理式 AI 模型 API——Muse Spark 1.1，正式进入付费 AI 市场，并可能通过开放权重使编码模型商品化，尽管其基准测试方法仍受到社区审视。

hackernews · ot · 7月9日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48846184)

**标签**: `#meta`, `#ai-api`, `#agentic-models`, `#business-strategy`, `#benchmark-criticism`

---

<a id="item-7"></a>
## [NVIDIA 发布用于 AI 智能体训练的开放数据集](https://huggingface.co/blog/nvidia/open-data-for-agents) ⭐️ 7.0/10

NVIDIA 发布了一组专为训练 AI 智能体设计的开放数据集，并在 HuggingFace 平台上公开提供。此举为开发者和研究人员提供了针对智能体开发流程精心策划的训练资源。 来自 NVIDIA 这家领先软硬件企业的开放数据集显著降低了智能体开发的准入门槛，并加速了自主 AI 系统的研究。借助 NVIDIA 在全栈技术上的深厚积累，这些数据集可以作为高质量的基准和训练语料库，服务于更广泛的社区。 这些数据集托管在 HuggingFace 上，该平台已拥有超过 90,000 个数据集和 900,000 个预训练模型，使此次发布能够立即获得广泛的关注和访问。聚焦智能体训练满足了快速增长的社区需求，包括精心策划的演示数据、强化学习信号以及任务分解示例，这些都是构建可靠自主智能体的关键要素。

rss · HuggingFace Blog · 7月8日 17:16

**背景**: AI 智能体是能够感知环境、做出决策并以最少人工干预执行复杂任务的自主系统。训练此类智能体通常需要结合强化学习、精心策划的演示数据以及在沙箱环境中的迭代评估。高质量的开放数据集至关重要，因为它们支持可复现的研究，并使缺乏大规模数据采集基础设施的较小团队也能构建具有竞争力的智能体系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets">Datasets – Hugging Face</a></li>
<li><a href="https://medium.com/@tahirbalarabe2/what-is-hugging-face-models-datasets-and-open-source-ai-platform-929a59e56fa5">🤗What is Hugging Face? Models, Datasets, and Open-Source AI Platform | by Tahir | Medium</a></li>
<li><a href="https://www.intellectyx.com/best-approaches-to-train-autonomous-ai-agents-for-task-execution/">Best Approaches to Train Autonomous AI Agents for Task ...</a></li>

</ul>
</details>

**标签**: `#ai-agents`, `#open-data`, `#nvidia`, `#training-datasets`, `#agent-framework`

---

<a id="item-8"></a>
## [HuggingFace 为 Transformers 添加原生 vLLM 后端](https://huggingface.co/blog/native-speed-vllm-transformers-backend) ⭐️ 7.0/10

HuggingFace 宣布为 transformers 库推出原生 vLLM 后端，使开发者可以直接在 transformers 内部获得高吞吐量的大语言模型推理能力，无需切换框架。该集成将 vLLM 优化的推理引擎作为任何兼容 transformers 模型的标配推理选项。 此举打通了当前最主流的两个机器学习推理生态，极大降低了数百万 transformers 用户部署生产级大语言模型的门槛。用户无需在易用性与推理性能之间做取舍，从而加速了 PagedAttention 等高效推理技术在 HuggingFace 社区中的普及。 该后端利用了 vLLM 的 PagedAttention 显存管理机制和连续批处理（continuous batching）技术，以最大化 GPU 利用率和吞吐量。用户在加载 transformers 模型时只需选择 vLLM 后端即可启用，现有推理管线无需重写代码。

rss · HuggingFace Blog · 7月8日 00:00

**背景**: HuggingFace 的 transformers 库是加载和使用预训练模型的事实标准，但其内置推理路径并未针对高吞吐量服务进行优化。vLLM 最初由加州大学伯克利分校的 Sky Computing Lab 开发，是一款专用推理引擎，它引入了受虚拟内存分页机制启发的 PagedAttention 显存管理技术，大幅减少了 KV 缓存的浪费。此前，vLLM 已支持将兼容 transformers 的模型加载到自己的引擎中；而本次公告则是将该集成方向反过来，将 vLLM 的高性能直接嵌入 transformers 库内部。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/vllm-project/vllm">GitHub - vllm-project/vllm: A high-throughput and memory-efficient inference and serving engine for LLMs · GitHub</a></li>
<li><a href="https://vllm.ai/blog/2025-04-11-transformers-backend">Transformers modeling backend integration in vLLM</a></li>
<li><a href="https://opendatascience.com/vllm-transformers-backend-bridging-hugging-face-compatibility-and-high-performance-inference/">vLLM Transformers Backend: Bridging Hugging Face ...</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#HuggingFace`, `#transformers`, `#LLM-inference`, `#performance-optimization`

---

<a id="item-9"></a>
## [OpenMed 1.8：Apache-2.0 临床去识别，完全本地运行，现已支持 Android、iOS 和浏览器。想参与 1.9 版本？这里有 400+ 个开放问题](https://www.reddit.com/r/LocalLLaMA/comments/1urt5o4/openmed_18_apache20_clinical_deidentification/) ⭐️ 7.0/10

OpenMed 1.8 提供 Apache-2.0 临床去识别模型，可完全本地运行于 Android、iOS、React Native 和浏览器，并配备 PDF 涂黑验证器，可捕获常见的纯视觉涂黑失败问题。

reddit · r/LocalLLaMA · /u/dark-night-rises · 7月9日 15:13

**标签**: `#clinical-NLP`, `#de-identification`, `#privacy`, `#edge-AI`, `#healthcare`, `#open-source`, `#ONNX`

---

<a id="item-10"></a>
## [Dify 1.16.0-rc1 实验性推出基于 Linux 沙箱的 Dify Agent](https://github.com/langgenius/dify/releases/tag/1.16.0-rc1) ⭐️ 6.0/10

Dify 发布了 1.16.0-rc1 版本，实验性地推出了 Dify Agent——一个在 Linux 沙箱内运行的基于 Shell 的 LLM Agent。该版本包含用于创建 Agent 的 UI 构建器、与 Dify Workflow 的集成、全新的 Web 应用体验，以及基于 Skills 的能力封装。 Dify 是一个被广泛采用的开源 LLM 应用开发平台，此次发布标志着它迈出了进入由 Anthropic Claude computer use 等工具推广的 Shell-based Agent 范式的第一步。对于 Dify 用户而言，它提供了一种更易用的可视化方式来构建强大的、可与工具、文件和知识库交互的编程型 Agent。 该版本明确警告所有 Dify Agent 共享同一个沙箱且尚未实现隔离，这意味着一个 Agent 可以读取或干扰另一个 Agent 的环境和用户数据，因此该服务应仅暴露给受信任的用户。升级需要运行新的数据库迁移、更新环境变量以及调整 Docker Compose 配置；用户还必须启动新的 `dify-agent` 和 `shellctl` 服务。

github · QuantumGhost · 7月9日 14:06

**背景**: Shell-based LLM Agent 范式指的是让语言模型直接访问命令行 Shell，使其能够执行任意命令、读写文件、安装软件包并编排复杂的多步骤任务——这一模式由 Anthropic 的 Claude computer use 推广开来。此处的「Skills」指的是一种标准化的方式来封装 Agent 的能力和提示词，从而便于分发和复用。针对 LLM Agent 的 Linux 沙箱通常利用 Docker 等容器技术提供文件系统隔离、网络限制和细粒度的路径控制，但 Dify 当前实现中尚未完成严格的隔离。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/siawkz/llm-sandbox">GitHub - siawkz/llm-sandbox: Secure Docker-based sandbox ...</a></li>
<li><a href="https://github.com/limyewjin/llm-bash">GitHub - limyewjin/llm-bash: A Bash framework following UNIX ...</a></li>

</ul>
</details>

**标签**: `#dify`, `#llm-agents`, `#release`, `#open-source`, `#ai-tooling`

---

<a id="item-11"></a>
## [Show HN：让 GLM 5.2 在我这台慢速电脑上运行起来](https://github.com/JustVugg/colibri) ⭐️ 6.0/10

一个实践项目，演示如何通过 int4 量化、MTP 和 DSA 等技术，在仅有 32GB 内存的机器上运行 GLM 5.2，并探讨了其中的性能权衡与替代方案。

hackernews · vforno · 7月9日 08:05 · [社区讨论](https://news.ycombinator.com/item?id=48842459)

**标签**: `#llm`, `#quantization`, `#local-inference`, `#glm`, `#performance-optimization`

---

<a id="item-12"></a>
## [Hy3](https://hy.tencent.com/research/hy3) ⭐️ 6.0/10

腾讯发布 Hy3，这是一款紧凑型大语言模型，在 OpenRouter 上免费开放至 7 月 21 日，但社区分析认为它相比 DeepSeek V4 Flash 等竞品并无明显优势。

hackernews · andai · 7月9日 15:27 · [社区讨论](https://news.ycombinator.com/item?id=48847552)

**标签**: `#AI`, `#LLM`, `#Tencent`, `#OpenRouter`, `#model-release`

---

<a id="item-13"></a>
## [IERS 确认 2026 年 12 月底不引入闰秒](https://datacenter.iers.org/data/latestVersion/bulletinC.txt) ⭐️ 6.0/10

国际地球自转与参考系统服务（IERS）通过其公告 C 宣布，2026 年 12 月底不会引入闰秒。这意味着 UTC 与 TAI 之间的偏移将保持在-37 秒，与自 2016 年 12 月最后一次添加闰秒以来的状态一致。 虽然这是例行公告，但闰秒的插入对计算系统来说历来是一个具有破坏性的事件，会导致无法妥善处理这一额外秒数的软件出现故障。此决定为系统管理员提供了六个月的提前确定性，同时也反映了地球自转速率持续的不确定性。 闰秒仅提前六个月宣布，因为地球自转速度因地质活动、天气模式及其他无法精确预测的地球物理因素而不规则变化。当前的 UTC-GPS 偏移保持在-18 秒，这源于 TAI 与 GPS 时间之间恒定的 19 秒偏移加上 TAI 与 UTC 之间 37 秒的差值。

hackernews · ChrisArchitect · 7月9日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=48846281)

**背景**: 协调世界时（UTC）基于由极其稳定的原子钟测量的国际原子时（TAI），但会通过定期插入闰秒来与 UT1 保持同步——UT1 是基于地球实际自转的天文时间尺度。每当 UTC 与 UT1 之间的差值即将超过 0.9 秒时，就会插入闰秒，这些操作由监测地球定向参数的 IERS 负责管理。近年来关于闰秒的争论日益激烈，2022 年国际计量大会决定在 2035 年前取消闰秒，但该变更尚未生效。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Leap_second">Leap second - Wikipedia</a></li>
<li><a href="https://www.nist.gov/pml/time-and-frequency-division/leap-seconds-faqs">Leap Seconds FAQs | NIST</a></li>
<li><a href="https://www.britannica.com/topic/leap-second">Leap second | Definition, UTC, & Facts | Britannica</a></li>

</ul>
</details>

**社区讨论**: 社区评论者提出了实质性的技术问题：有人询问是什么导致了地球自转的不可预测性（地质活动和天气确实是影响因素），另有人询问闰秒如何影响 Unix 时间戳，尤其是在遗留系统或维护最少的系统中。一位评论者很有帮助地指出，如果 UTC-TAI 保持在-37 秒，那么 UTC-GPS 就保持在-18 秒，并注意到 TAI 与 GPS 之间恒定的 19 秒偏移。还有人幽默地建议沿着赤道安装喷气发动机来手动控制时间。

**标签**: `#timekeeping`, `#leap-second`, `#UTC`, `#IERS`, `#systems`

---

<a id="item-14"></a>
## [玻璃脊梁：为何美国陆军的后勤体系将在下一场战争中崩溃](https://mwi.westpoint.edu/the-glass-backbone-why-the-armys-logistics-will-break-in-the-next-war/) ⭐️ 6.0/10

西点军校的一项分析指出，美国陆军对后勤投入不足（战斗部队与后勤人员比例失衡）已造成脆弱的供应链依赖关系，可能在现代势均力敌的冲突需求下彻底瓦解。

hackernews · baud147258 · 7月9日 13:24 · [社区讨论](https://news.ycombinator.com/item?id=48845442)

**标签**: `#military-strategy`, `#logistics`, `#systems-thinking`, `#defense-policy`, `#supply-chain`

---

<a id="item-15"></a>
## [GLM 5.2 的准确度几乎与人类簿记员相当](https://toot-books.pages.dev/blog/glm-5-2-vat-benchmark) ⭐️ 6.0/10

GLM 5.2 在增值税基准测试上的准确度几乎与人类簿记员持平，但评论者指出该基准测试的范围比真实簿记工作更窄，并提出了尚未解决的责任归属问题。

hackernews · adamkurkiewicz · 7月9日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=48850414)

**标签**: `#LLM`, `#benchmarks`, `#accounting`, `#automation`, `#liability`

---

<a id="item-16"></a>
## [内部服务 TLS 证书配置实践指南](https://tuxnet.dev/posts/tls-for-internal-services/) ⭐️ 6.0/10

一篇博客文章提供了为内部服务配置 TLS 证书的实践指南，随后的社区讨论中，许多资深从业者强烈反对使用 split-horizon DNS（分裂视图 DNS），转而推荐使用 DNS-01 ACME 质询、Let's Encrypt 通配符证书以及集中式反向代理方案。 为内部服务启用 TLS 是系统管理员和 DevOps 团队日常运维中的痛点，选择错误的架构（如 split-horizon DNS 或自签名 CA）会带来长期的维护负担和安全隐患。 DNS-01 质询要求对 DNS 提供商拥有 API 访问权限才能自动化签发证书，非常适合为不可公开访问的内部服务签发通配符证书。Let's Encrypt 仅通过 DNS-01 支持通配符证书，且除非使用通配符证书，否则子域名信息会公开记录在 CT（证书透明度）日志中。

hackernews · mrl5 · 7月9日 14:57 · [社区讨论](https://news.ycombinator.com/item?id=48846995)

**背景**: TLS（传输层安全协议）用于加密客户端与服务器之间的网络流量，但传统上内部服务要么使用自签名证书（导致信任错误），要么直接运行明文 HTTP。ACME 协议（Let's Encrypt 所采用）通过域名验证质询来自动化签发证书：HTTP-01 要求有可访问的 Web 服务器，而 DNS-01 通过 DNS 记录验证域名所有权。Split-horizon DNS（分裂视图 DNS）会根据查询来自内部还是外部网络，对同一域名返回不同的解析结果，这使得组织可以在内部使用公网域名，但会带来运维复杂性。反向代理则将 TLS 终止集中化，使各内部服务无需自行管理证书。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://letsencrypt.org/docs/challenge-types/">Challenge Types - Let's Encrypt</a></li>
<li><a href="https://en.wikipedia.org/wiki/Split-horizon_DNS">Split-horizon DNS - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 讨论中对 split-horizon DNS 形成了强烈的反对共识，多位评论者称其为可维护性陷阱。推荐的替代方案包括：通过 VPN/WireGuard 路由公网域名、使用 DNS-01 质询配合 Let's Encrypt 通配符证书、完全避免 HTTP-01，以及部署集中式反向代理来终止 TLS。还有评论者提出了一个更宏观的观点：在不同编程语言中信任内部 CA 的过程本应更加简便，因为目前每种语言都有自己的证书存储约定。

**标签**: `#tls`, `#security`, `#infrastructure`, `#dns`, `#ssl-certificates`

---

<a id="item-17"></a>
## [OpenAI 将 ChatGPT 与 Codex 合并为统一的「ChatGPT Work」应用](https://openai.com/index/chatgpt-for-your-most-ambitious-work/) ⭐️ 6.0/10

OpenAI 已将独立的 ChatGPT 和 Codex 桌面应用合并为一款名为「ChatGPT Work」的统一应用，取消了独立的 Codex 应用。传统的 ChatGPT 界面被更名为「ChatGPT Classic」，这表明公司围绕编码和企业工作流进行了战略性整合。 此次整合反映了 OpenAI 希望与 Anthropic 整合后的 Claude 品牌（Claude Code、Claude Cowork 等）展开竞争，也表明 OpenAI 将企业收入重点放在了编码和工作效率领域。它直接影响此前拥有专用编码任务界面和通用 AI 聊天界面的开发者及企业用户。 用户反馈，在「ChatGPT Work」和「ChatGPT Codex」模式之间切换几乎看不到任何变化，非编程类对话现在被限制在一个无法搜索的小弹窗中。原始 ChatGPT 被改名为「Classic」意味着旧界面最终将被淘汰，而企业管理功能（如管理员控制、数据驻留和保留策略）因套餐和所连接系统而异。

hackernews · OpenAI Blog · 7月9日 17:03 · [社区讨论](https://news.ycombinator.com/item?id=48849059)

**背景**: Codex 是 OpenAI 基于云的 AI 软件工程代理，最早于 2025 年 5 月 16 日作为独立应用推出，向 ChatGPT Pro、Business 和 Enterprise 用户开放。它可以在多个环境中并行运行编码任务，并能够连接工具和代码仓库。在此次合并之前，用户需要同时使用两款不同的应用：ChatGPT 用于日常对话，Codex 用于开发工作。而 Anthropic 则一贯采取统一品牌战略，将 Claude Code、Claude Cowork 等产品统一在 Claude 品牌下，一些观察人士认为这种方式对用户更加友好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Codex_(AI_agent)">Codex (AI agent) - Wikipedia</a></li>
<li><a href="https://openai.com/index/introducing-codex/">Introducing Codex - OpenAI</a></li>
<li><a href="https://openai.com/academy/what-is-codex/">What is ChatGPT Codex? - OpenAI</a></li>

</ul>
</details>

**社区讨论**: 社区情绪明显偏负面，用户表达了对界面改动的困惑，并对非编程类聊天被降级到一个微小弹窗感到不满。多位评论者指出 Anthropic 的整合方式更合理——将所有功能统一在 Claude 品牌下，同时保留了聊天体验。也有评论者警告，将原应用改名为「Classic」预示着它即将被弃用。一些用户承认 ChatGPT 和 Codex 分裂的状态确实不可持续、合并是迟早的事，但批评 OpenAI 未能保留先前运转良好的使用体验。

**标签**: `#OpenAI`, `#ChatGPT`, `#Codex`, `#product-update`, `#developer-tools`

---

<a id="item-18"></a>
## [GPT-5.6 成为 Microsoft 365 Copilot 的首选模型](https://openai.com/index/gpt-5-6-preferred-model-microsoft-365-copilot) ⭐️ 6.0/10

OpenAI 宣布 GPT-5.6 现已成为 Microsoft 365 Copilot 在 Word、Excel、PowerPoint、Chat 和 Cowork 中的首选驱动模型。此次升级将 OpenAI 最新的大语言模型带到了部署最广泛的企业 AI 助手之一中。 此举进一步深化了 OpenAI 与 Microsoft 的合作关系，并将 GPT-5.6 在推理和智能体能力方面的改进带给数以亿计的 Microsoft 365 用户。这一转变有望显著提升核心企业生产力工具中 AI 辅助工作的质量和自主性。 GPT-5.6 由 OpenAI 于 2026 年 6 月 26 日发布，其模型家族包含 Sol、Terra 和 Luna 三个变体。被升级的 Copilot Cowork 由 Work IQ 提供支持，能够从 Outlook、Teams、Excel 等 Microsoft 365 应用中获取信号，从而在每一步获得用户批准的前提下执行多步骤任务。

rss · OpenAI Blog · 7月9日 13:00

**背景**: Microsoft 365 Copilot 是一款嵌入到 Microsoft 生产力应用（包括 Word、Excel、PowerPoint 和 Teams）中的生成式 AI 助手，可帮助用户撰写文档、分析数据、汇总邮件和管理项目。Copilot Cowork 于 2026 年初推出，进一步扩展了这些能力，允许助手代表用户在多个 Microsoft 365 应用中执行更长的多步骤工作流，每一步都需要用户批准。GPT-5.6 是 OpenAI 最新的旗舰大语言模型，是 GPT 系列早期版本的升级，在推理、智能体任务执行和综合能力方面均有改进。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.6">GPT-5.6 - Wikipedia</a></li>
<li><a href="https://learn.microsoft.com/en-us/microsoft-365/copilot/cowork/">Copilot Cowork overview | Microsoft Learn</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/03/09/copilot-cowork-a-new-way-of-getting-work-done/">Copilot Cowork: A new way of getting work done | Microsoft ...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Microsoft`, `#Copilot`, `#Enterprise AI`, `#Product Announcement`

---

<a id="item-19"></a>
## [GPT-5.5 生物安全漏洞赏金计划](https://openai.com/index/bio-bug-bounty) ⭐️ 6.0/10

OpenAI 宣布推出一项漏洞赏金计划，旨在发现其生物人工智能系统中的安全漏洞。

rss · OpenAI Blog · 7月9日 10:00

**标签**: `#OpenAI`, `#AI Safety`, `#Bug Bounty`, `#Responsible AI`, `#Biosecurity`

---

<a id="item-20"></a>
## [OpenAI 阐述其政府与国家安全合作原则](https://openai.com/index/government-national-security-partnerships) ⭐️ 6.0/10

OpenAI 发布了一份正式声明，阐述了其与政府机构及国家安全实体合作的原则与方法，重点关注负责任的 AI 部署、民主问责制以及公共安全。 作为领先的 AI 开发方，OpenAI 与政府的合作框架树立了行业先例，可能会影响 AI 能力在公共部门和国防领域的整合方式，进而塑造政策规范以及 AI 提供商之间的竞争格局。 该公告强调了三大核心支柱——负责任的使用、民主问责制和公共安全——表明 OpenAI 意在参与政府工作，同时围绕其参与国家安全相关应用设立保障措施。

rss · OpenAI Blog · 7月8日 13:30

**背景**: OpenAI 的原始章程承诺确保通用人工智能广泛造福全人类，这在历史上一直与军事和情报应用场景存在矛盾。大型语言模型及其他 AI 工具日益深入政府运作——包括国防、情报分析和公共行政——促使主要 AI 公司就其可接受的使用方式和合作条款表达更明确的立场。Anthropic 和 Google DeepMind 等竞争对手也已发布了类似的政府合作政策框架。

**标签**: `#AI policy`, `#OpenAI`, `#government`, `#national security`, `#responsible AI`

---

<a id="item-21"></a>
## [本科生一作论文实现 7.92 倍投机解码加速](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247902587&idx=3&sn=879066ecce663ab9daba5d73fe2dc27b) ⭐️ 6.0/10

一位大三本科生作为第一作者发表了投机解码论文，实现了 7.92 倍的推理加速，该工作已被 DeepSeek 和阶跃星辰双双引用。文章指出并行 draft 的速度优势已经很明显，下一步需要解决的是 block 内部的因果一致性问题。 这表明前沿的大模型推理优化研究正变得对本科研究者越来越开放，而被国内顶级 AI 实验室引用则证明了其实际价值。投机解码是降低大模型部署延迟和成本的关键技术，直接影响用户体验和推理经济性。 该论文聚焦于并行 draft 模型策略，即用一个小而快的模型提出 token，再用大的目标模型并行验证。文中指出的剩余挑战是在 block 内部维持因果一致性——确保并行的投机预测不会违反自回归生成所需的序列依赖关系。

rss · 量子位 · 7月9日 04:17

**背景**: 投机解码通过使用一个小型 draft 模型预测多个即将到来的 token，再由更大的目标模型在一次并行前向传播中验证这些 token，在保持输出分布完全一致的同时减少序列生成的开销，从而加速大模型推理。并行投机解码（如 PEARL 框架）通过同时运行多条解码轨迹进一步扩展了这一思路。Block 级别的方法（如 JetSpec）则试图通过 block 级别的注意力机制来训练因果并行 draft 头，在保留分支级因果条件的同时打破因果性与效率之间的矛盾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency ...</a></li>
<li><a href="https://arxiv.org/abs/2408.11850">[2408.11850] PEARL: Parallel Speculative Decoding with ... Top Stories Speculative Decoding: How a Small Draft Model Makes Large ... GitHub - smart-lty/ParallelSpeculativeDecoding: [ICLR 2025 ... Speculative Decoding Explained: How Draft Models Make AI ... Speculative Speculative Decoding - arXiv.org</a></li>
<li><a href="https://arxiv.org/html/2606.18394v3">JetSpec: Breaking the Scaling Ceiling of Speculative Decoding ...</a></li>

</ul>
</details>

**标签**: `#speculative-decoding`, `#LLM-inference`, `#research`, `#DeepSeek`, `#performance-optimization`

---

<a id="item-22"></a>
## [现在兄弟们，我们总算知道自己为啥这么惨了](https://www.reddit.com/r/LocalLLaMA/comments/1urh2mg/now_brothers_we_know_why_we_are_so_fucked_up/) ⭐️ 6.0/10

三星芯片部门利润预计在 2026 年将超过其过去 40 年的总和，这得益于 AI 驱动的内存需求激增，同时也解释了当前 AI/ML 从业者面临的硬件成本危机。

reddit · r/LocalLLaMA · /u/perelmanych · 7月9日 05:32

**标签**: `#AI hardware`, `#semiconductors`, `#memory pricing`, `#GPU shortage`, `#market dynamics`

---

<a id="item-23"></a>
## [Puzzle-75B-A9B NVFP4 在 3×3090 上达 132 t/s，凸显开源模型尺寸断层](https://www.reddit.com/r/LocalLLaMA/comments/1uru9ja/nvidia_puzzle75ba9b_nvfp4_at_132_ts_on_33090_why/) ⭐️ 6.0/10

一位用户在由三张 RTX 3090 组成（第四张用于语音副进程）的机器上演示了 NVIDIA 的 Nemotron-3-Puzzle-75B-A9B MoE 模型的 NVFP4 量化推理，在三个并发 256K 上下文流下达到 132 t/s 的解码速度，prefill 速度为 1,949 t/s，整机功耗约 500W。该方案借助 vLLM 0.22.1 引入的全新 Marlin 内核回退机制，将本属于 Blackwell 时代的 NVFP4 格式带到了 Ampere 硬件上。 该帖揭示了开源模型生态中的一个真实空白：恰好能填满约 72GB 量化显存（三张 24GB 显卡）的 70–80B 总参 / ~10B 激活 MoE 甜点区间几乎没有模型可选，用户要么只能用 30B-A3B 小模型让显存闲置，要么被迫使用 120B+ 大模型导致溢出到内存并需激进量化。同时也展示了 vLLM 的新 Marlin 回退机制让 NVFP4 不再局限于 Blackwell，延长了老一代 Ampere 硬件的实际使用价值。 三张 3090 通过流水线并行运行，每张卡功耗上限设为 200W，整机功耗约 500W；FP8 KV 缓存加上模型的混合 Mamba-Transformer 架构让 256K 上下文下的显存占用保持在极低水平。据称该方案替换了此前使用四张 3090 的 Nemotron Super 120B GGUF 配置，速度功耗比提升约一倍且指令跟随能力更好，并由此释放出一张显卡。

reddit · r/LocalLLaMA · /u/Important_Quote_1180 · 7月9日 15:53

**背景**: NVFP4 是 NVIDIA 随 Blackwell 架构推出的 4 位浮点量化格式，采用两级缩放策略（细粒度 E4M3 微缩放 + FP32 块级标量），在超低精度下仍能保持准确率。Marlin 内核最初是为 Ampere GPU（算力 ≥ 8.0）设计的高性能 FP16×INT4 矩阵乘法内核，vLLM 0.22.1 引入的 Marlin 回退机制将其扩展，使同一硬件也能支持 FP8 和 FP4 权重量化。Puzzle 模型采用混合 Mamba-Transformer（SSM + 注意力）架构，其中 Mamba 状态空间部分维护固定大小的循环状态，而非不断增长的 KV 缓存，从而大幅降低长上下文推理的显存占用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>
<li><a href="https://github.com/IST-DASLab/marlin">GitHub - IST-DASLab/marlin: FP16xINT4 LLM inference kernel ... AutoAWQ+Marlin: Efficient INT4 Inference - emergentmind.com Images AWQ-Marlin INT4 Weight Quantization | dkhokhlov/Qwen_3_6_on ... [Feature] Support NVIDIA Ampere (A100, 3090, A6000) MoE FP8 ... MARLIN: Mixed-Precision Auto-Regressive Parallel Inference on ... nvidia/Qwen3.6-27B-NVFP4 · Fallback to marlin kernel give ...</a></li>
<li><a href="https://arxiv.org/pdf/2510.26912">Understanding and Enhancing Mamba-Transformer Hybrids for ...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#moe`, `#nvfp4-quantization`, `#gpu-inference`, `#vllm`

---

<a id="item-24"></a>
## [Reasoning-Medical0.1-27B（基于 Qwen3.5-27B 的医疗微调模型，声称超越 MedGemma）](https://www.reddit.com/r/LocalLLaMA/comments/1urni78/reasoningmedical0127b_qwen3527b_medical_finetune/) ⭐️ 6.0/10

社区发布的 Reasoning-Medical0.1-27B 是基于 Qwen 的 27B 模型的医疗领域微调版本，据称在 Google MedGemma 基准测试中表现更优。

reddit · r/LocalLLaMA · /u/beneath_steel_sky · 7月9日 11:27

**标签**: `#medical-ai`, `#llm-finetune`, `#open-weights`, `#qwen`, `#local-llama`

---

<a id="item-25"></a>
## [OpenMOSS-Team/MOSS-Transcribe-Diarize · Hugging Face](https://www.reddit.com/r/LocalLLaMA/comments/1uru6wf/openmossteammosstranscribediarize_hugging_face/) ⭐️ 6.0/10

OpenMOSS 发布了一个拥有 0.9B 参数的端到端模型，可在单次处理中完成长篇多说话人转写、说话人分离、时间戳标注以及声学事件检测。

reddit · r/LocalLLaMA · /u/pmttyji · 7月9日 15:50

**标签**: `#speech-recognition`, `#speaker-diarization`, `#open-source`, `#audio-ai`, `#hugging-face`

---

<a id="item-26"></a>
## [MiMo v2.5 在 192GB 显存本地推理基准测试中表现亮眼](https://www.reddit.com/r/LocalLLaMA/comments/1us4gim/mimo_v25_is_underrated_feels_like_the_tokens_are/) ⭐️ 6.0/10

一位 Reddit 用户分享了小米 MiMo v2.5 在 192GB 4090 显存上的本地推理基准测试结果，比较了多种 4-bit 量化格式，并称赞该模型是速度最快的本地大语言模型，token 吞吐量超越云端服务提供商。该用户在 ik_llama.cpp 中测试了 Bartowski IQ4_XS、IQ4_NL、Unsloth UD-Q4_K_S 以及 gghfez IQ4_XS 等变体，发现 Bartowski IQ4_NL 在质量和速度方面取得了最佳平衡。 MiMo v2.5 是一个具有 310B 总参数、150 亿激活参数的稀疏 MoE 模型，填补了作者所描述的 30B 至 400B 本地模型之间关键的能力空白，使其成为运行多 GPU 推理集群用户的有力选择。如果这一结论得到验证，可能会促使更多从业者选择自托管而非付费使用云端推理服务，尤其在智能体和编程类工作负载场景下。 重复输出/陷入循环是一个显著问题，模型对采样参数极为敏感；推荐的参数设置为 --temp 1.0 --top-p 0.95 --repeat-penalty 1.2 --repeat-last-n 128，效果良好，而激进的存在性惩罚/频率惩罚会使模型丧失调用工具的能力。MiMo v2.5 在 llama.cpp 中仍存在多项功能缺失，包括多 token 预测（MTP）、--split-mode tensor、多模态视觉和 ASR 支持，不过 --split-mode graph 在 ik_llama 分支中可与未融合的张量配合使用。

reddit · r/LocalLLaMA · /u/dangerous_inference · 7月9日 21:59

**背景**: MiMo v2.5 是小米于 2026 年 4 月发布的开源全模态语言模型，采用稀疏混合专家（MoE）架构，总参数 3100 亿，但每个 token 仅激活 150 亿参数，在 48 万亿 token 上训练而成。它具有 100 万 token 的上下文窗口，继承了 MiMo-V2-Flash 的混合滑动窗口注意力设计，并配备了小米自研的视觉和音频编码器。ik_llama.cpp 是 llama.cpp 的一个性能优化分支，支持更新的量化类型和混合 GPU/CPU 推理，可在多卡 4090 等消费级硬件上实现更快的吞吐量。IQ4_NL（重要性量化，4-bit，非线性映射）和 UD-Q4_K_S 等量化格式是 llama.cpp 较新的创新，可在将模型权重压缩至 4 bit 的同时尽量保留质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mimo.xiaomi.com/mimo-v2-5">MiMo-V2.5 | Xiaomi</a></li>
<li><a href="https://github.com/ikawrakow/ik_llama.cpp/">GitHub - ikawrakow/ik_llama.cpp: llama.cpp fork with ...</a></li>
<li><a href="https://deepwiki.com/ikawrakow/ik_llama.cpp/1.1-key-features-and-performance-improvements">Key Features and Performance Improvements | ikawrakow/ik ...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#MiMo`, `#quantization`, `#inference-benchmarking`, `#GPU`

---