---
layout: default
title: "Horizon Summary: 2026-07-15 (ZH)"
date: 2026-07-15
lang: zh
---

> 从 52 条内容中筛选出 18 条重要资讯。

---

1. [Linus Torvalds 呼吁人们停止因使用 AI 而攻击他人](#item-1) ⭐️ 8.0/10
2. [Pluralis 在 4 国 14 台 Mac 上完成 RL 后训练](#item-2) ⭐️ 8.0/10
3. [ExLlamaV3 v1.0.0 正式发布，性能大幅提升](#item-3) ⭐️ 8.0/10
4. [Inkling：我们的开放权重模型](#item-4) ⭐️ 7.0/10
5. [据消息人士透露，Stripe 与 Advent 已联合出价收购 PayPal](#item-5) ⭐️ 7.0/10
6. [Gemma 4 26B 在无 GPU 的 13 年老旧 Xeon 上实现 5 tok/s 推理速度](#item-6) ⭐️ 7.0/10
7. [Show HN：misa77 - 解码速度比 LZ4 快 2 倍（且压缩率更优）的编解码器](#item-7) ⭐️ 7.0/10
8. [睡眠规律性比睡眠时长更能预测死亡风险（2023）](#item-8) ⭐️ 7.0/10
9. [OpenAI 发布 GPT-Red：基于自博弈的自动化红队 AI 安全系统](#item-9) ⭐️ 7.0/10
10. [AllenAI 分享构建 Shippy 智能体的工程经验](#item-10) ⭐️ 7.0/10
11. [模型路由看似简单，实际却暗藏玄机](#item-11) ⭐️ 7.0/10
12. [HuggingFace 发布 Real World VoiceEQ 语音 AI 评测基准](#item-12) ⭐️ 7.0/10
13. [腾讯发布 RxBrain：面向具身智能的统一多模态模型](#item-13) ⭐️ 7.0/10
14. [Transformers v5.14.0 新增 Thinking Machines 的 975B 多模态模型 Inkling](#item-14) ⭐️ 6.0/10
15. [Telegram 数据中心的奥秘 (2022)](#item-15) ⭐️ 6.0/10
16. [Google is updating Gemma 4's chat templates, bringing major fixes to tool calling and reducing "laziness", and enabling Flash Attention 4 on Hopper GPUs, plus an interactive guide on how to work with and improve its vision!](#item-16) ⭐️ 6.0/10
17. [德国 AI 联盟发布 Soofi S：一款在英语和德语基准测试中均名列前茅的开源 300 亿参数模型](#item-17) ⭐️ 6.0/10
18. [苹果与 PrismML 洽谈 AI 模型压缩技术以适配 iPhone](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Linus Torvalds 呼吁人们停止因使用 AI 而攻击他人](https://www.reddit.com/r/LocalLLaMA/comments/1uxbrw4/linus_torvalds_tells_people_to_stop_attacking/) ⭐️ 8.0/10

Linus Torvalds 宣布 Linux 内核开发将接受 AI 生成的代码，并警告贡献者停止因使用 AI 工具而攻击他人，称 AI 是一个明显有用的工具，尽管偶尔存在一些问题。

reddit · r/LocalLLaMA · /u/Illustrious_Car344 · 7月15日 16:59

**标签**: `#Linux`, `#AI`, `#OpenSource`, `#LinusTorvalds`, `#SoftwareEngineering`

---

<a id="item-2"></a>
## [Pluralis 在 4 国 14 台 Mac 上完成 RL 后训练](https://www.reddit.com/r/LocalLLaMA/comments/1uxb3zn/rl_posttraining_on_14_macs_across_4_countries/) ⭐️ 8.0/10

Pluralis Research 展示了据信是首次完全在开放互联网上的消费级 Mac 上运行 rollout 的强化学习后训练实验。分布于 4 个国家的 14 台 Mac 通过 int8 MLX 推理生成 rollout，部署在另一大洲的单一 B200 GPU 执行 bf16 Megatron 梯度更新，两端仅通过 Cloudflare R2 在普通家庭宽带上同步。 在智能体 RL 中，rollout 生成约占总算力的 80%，因此将其外包给闲置的消费级 Mac 改变了谁能负担得起大规模 RL 训练。通过证明数据中心和一群 MacBook 可以跨大洲协作完成后训练，Pluralis 预示着一个不再需要拥有 GPU 集群就能进行前沿级 RL 训练的未来。 两个机制控制了离策略偏差：PULSE 传输 int8 权重增量而非完整检查点，由于版本间只有约 0.5%的 int8 数值会变化，典型传输量从 9 GB 降至约 82 MB；DPPO 风格的概率门控丢弃约 0.3%的 token，这些 token 在 rollout 模型和训练器之间的概率漂移过大。在 PaperSearchQA 多轮生物医学搜索任务上，Stoa 模型的 cover pass@1 从 29%提升到 63%，搜索率从 22%提升到 84%。

reddit · r/LocalLLaMA · /u/erfan_mhi · 7月15日 16:36

**背景**: RL 后训练是指在预训练之后使用强化学习对模型进行微调，而「智能体 RL」专门训练模型调用工具并串联多轮交互。在这类工作负载中，生成 rollout 轨迹占据了绝大部分算力，梯度更新反而相对廉价。跨消费级硬件部署面临两项技术约束：Apple 的 MLX 框架仅在 Apple Silicon 上高效运行，且通常使用 int8 等低精度；而 NVIDIA 的 Megatron 等训练框架通常在数据中心 GPU 上使用 bf16。所谓「离策略偏差」是指生成数据的策略与当前正在训练的策略之间的分布漂移，当 rollout 由过时的或经过不同精度量化的权重生成时，这种偏差会增大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple ... Exploring LLMs with MLX and the Neural Accelerators in the M5 ... MLX mlx · PyPI MLX — MLX 0.31.2 documentation - GitHub Pages GitHub - frankgmail/apple-mlx: MLX: An array framework for ...</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>
<li><a href="https://machinelearning.apple.com/research/exploring-llms-mlx-m5">Exploring LLMs with MLX and the Neural Accelerators in the M5 ...</a></li>
<li><a href="https://zoeyli.com/reinforcement+learning/Off-Policy-Corrections-LLM-RL/">Off - Policy Corrections in LLM RL Training - Zoey Li’s Personal Webpage</a></li>

</ul>
</details>

**标签**: `#reinforcement-learning`, `#distributed-computing`, `#MLX`, `#model-training`, `#open-source`

---

<a id="item-3"></a>
## [ExLlamaV3 v1.0.0 正式发布，性能大幅提升](https://www.reddit.com/r/LocalLLaMA/comments/1uwylut/exllamav3_v100_major_performance_upgrades/) ⭐️ 8.0/10

经过一年多的开发，ExLlamaV3 迎来了首个正式版本（v1.0.0），带来了支持在线 KV 缓存量化的全新注意力内核、新版 INT8 GEMV 内核、MoE 内核调度器，并扩展了张量并行和模型支持范围。该版本移除了对 flash-attention-2 和 xformers 的依赖，并新增了原生 conv1d、GptOssForCausalLM 和 NemotronHForCausalLM 支持。 ExLlamaV3 是消费级 GPU 本地运行大语言模型最广泛使用的推理库之一，因此这些性能和架构改进直接影响所有在个人硬件上运行大模型的用户的体验。通过消除外部注意力依赖并引入在线 KV 缓存量化，新版本使本地推理更快、更省内存，且更易于安装。 全新注意力内核支持在线 KV 缓存量化，且不会出现以往量化缓存路径常见的减速问题，同时支持滑动窗口注意力（SWA）层和注意力汇聚（attention sinks）的双输入处理；Ampere 架构 GPU（如 RTX 30 系列）从改进的 GEMM/GEMV 内核中获益尤为显著。张量并行支持现已覆盖包括 Gemma4 在内的大部分架构，图捕获路径覆盖所有 attn/GDN 模块。

reddit · r/LocalLLaMA · /u/Unstable_Llama · 7月15日 07:17

**背景**: ExLlamaV3 是一个专为在 NVIDIA GPU 上本地运行量化大语言模型而优化的高性能推理引擎。KV 缓存量化可减少 Transformer 在生成过程中存储的键值缓存的内存占用，从而在有限的显存下支持更长上下文或更大批量；在线量化在推理过程中直接执行量化，而非作为单独的预处理步骤。混合专家（MoE）模型将每个 token 路由到部分专家子网络，需要专门的内核来高效调度哪些专家处理哪些 token——GPT-OSS 和 DeepSeek 等模型采用此架构时，这是一个关键挑战。注意力汇聚（attention sinks）指的是 Transformer 模型中初始 token 持续吸收不成比例注意力权重的现象，专门的内核必须正确处理这一特性以维持生成质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/quantization/quantized_kvcache/">Quantized KV Cache - vLLM</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://arxiv.org/abs/2604.10098">[2604.10098] Attention Sink in Transformers: A Survey on ...</a></li>

</ul>
</details>

**标签**: `#ExLlamaV3`, `#LLM-inference`, `#local-llama`, `#GPU-optimization`, `#model-quantization`

---

<a id="item-4"></a>
## [Inkling：我们的开放权重模型](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 7.0/10

Thinking Machines 发布 Inkling，这是一款全新的大型开放权重多模态模型，是目前最大的原生支持音频功能的开放权重模型之一。

hackernews · vimarsh6739 · 7月15日 18:12 · [社区讨论](https://news.ycombinator.com/item?id=48924912)

**标签**: `#open-source-ai`, `#multimodal-models`, `#thinking-machines`, `#audio-ai`, `#llm-release`

---

<a id="item-5"></a>
## [据消息人士透露，Stripe 与 Advent 已联合出价收购 PayPal](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 7.0/10

Stripe 与 Advent 已联合出价超过 530 亿美元收购 PayPal，有望将两家主要支付处理商整合为一家。

hackernews · rvz · 7月15日 03:32 · [社区讨论](https://news.ycombinator.com/item?id=48915953)

**标签**: `#fintech`, `#payments`, `#mergers-acquisitions`, `#stripe`, `#paypal`

---

<a id="item-6"></a>
## [Gemma 4 26B 在无 GPU 的 13 年老旧 Xeon 上实现 5 tok/s 推理速度](https://www.neomindlabs.com/2026/06/08/running-gemma-4-26b-at-5-tokens-sec-on-a-13-year-old-xeon-with-no-gpu/) ⭐️ 7.0/10

一位开发者在约 2013 年的双路 Xeon 服务器上、无 GPU 加速的情况下，实现了 Google Gemma 4 26B（激活参数 4B 的混合专家模型）约 5 tokens/秒的推理速度。 这一基准测试凸显了 CPU LLM 推理技术的进步，表明 200 亿以上参数级别的模型已可在老旧企业级硬件上运行。同时，它也提出了一个重要问题：在将电费和硬件折旧成本纳入考量后，本地推理相比云端 API 的真正成本效益究竟如何。 Gemma 4 26B 是 Google DeepMind 基于 Gemini 3 研究构建的多模态 MoE 模型，每次推理仅激活约 40 亿参数——这正是它能装入有限内存的关键原因。社区估算负载下的双路 Xeon 系统功耗为 300–500W，使得本地推理每 token 成本比云端推理提供商高出约 10–30 倍，甚至还未计入散热费用。

hackernews · neomindryan · 7月15日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=48922434)

**背景**: Gemma 4 是 Google 在 2025–2026 年发布的开源权重模型系列，源自 Gemini 3 的研究成果，包含预训练和指令微调版本。混合专家（MoE）架构保持了较高的总参数量，但每次推理仅激活一小部分参数，从而大幅降低内存带宽和推理计算需求。在纯 CPU 硬件上运行 LLM 通常依赖量化后的模型权重和 llama.cpp 等优化推理引擎，以原始速度换取可访问性，避免对昂贵 GPU 的依赖。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/google/gemma-4-26B-A4B/blob/main/README.md">README.md · google/ gemma - 4 - 26 B -A 4 B at main</a></li>
<li><a href="https://insiderllm.com/guides/cpu-only-llms-what-actually-works/">CPU-Only LLMs: What Actually Works | InsiderLLM</a></li>
<li><a href="https://www.baseten.co/blog/comparing-tokens-per-second-across-llms/">Comparing tokens per second across LLMs</a></li>

</ul>
</details>

**社区讨论**: 社区进行了严谨的成本效益分析：多位评论者（hagen8、Aurornis）计算出 300–500W Xeon 服务器的电费使本地推理每 token 成本比云端 API 高出 10–30 倍，即使云端每百万 token 价格与本地持平。乐观派如 dwa3592 预测到 2027 年中前将有超过 200B 的 MoE 模型可在普通消费级硬件上运行，理由是他在 16GB MacBook Air 上以 7–9 t/s 运行了 Qwen 35B-A3B 的亲身经验。多位评论者分享了其他基准测试数据，throwaway2027 报告在类似老旧硬件上达到 8–12 t/s，hparadiz 则发布了在配备 256GB DDR4 的双路 Xeon 上的详细 gist 基准测试结果。

**标签**: `#local-llm`, `#hardware-benchmarks`, `#cost-analysis`, `#inference-optimization`, `#hacker-news`

---

<a id="item-7"></a>
## [Show HN：misa77 - 解码速度比 LZ4 快 2 倍（且压缩率更优）的编解码器](https://github.com/welcome-to-the-sunny-side/misa77) ⭐️ 7.0/10

Show HN 推介 misa77，这是一款实验性压缩编解码器，号称解压速度比 LZ4 快 2 倍，且压缩率更优，但代价是编码速度大幅降低。

hackernews · nonadhocproblem · 7月15日 15:58 · [社区讨论](https://news.ycombinator.com/item?id=48922838)

**标签**: `#compression`, `#lz4`, `#performance`, `#systems`, `#optimization`

---

<a id="item-8"></a>
## [睡眠规律性比睡眠时长更能预测死亡风险（2023）](https://academic.oup.com/sleep/article/47/1/zsad253/7280269) ⭐️ 7.0/10

一项 2023 年的同行评议研究发现，基于大型队列的加速度计数据，稳定的睡眠规律性比总睡眠时长更能预测全因死亡风险。

hackernews · bilsbie · 7月15日 11:46 · [社区讨论](https://news.ycombinator.com/item?id=48919363)

**标签**: `#health`, `#sleep-research`, `#epidemiology`, `#longevity`, `#public-health`

---

<a id="item-9"></a>
## [OpenAI 发布 GPT-Red：基于自博弈的自动化红队 AI 安全系统](https://openai.com/index/unlocking-self-improvement-gpt-red) ⭐️ 7.0/10

OpenAI 推出了 GPT-Red，一个利用自博弈强化学习（self-play reinforcement learning）的自动化红队系统，能够在多种红队场景下同时训练攻击模型和一系列多样化的防御 LLM。该系统旨在增强 AI 的安全性、对齐能力以及对提示注入攻击的抵御力。 自动化红队解决了 AI 安全中的一个关键扩展瓶颈：人工对抗测试无法跟上新模型和应用快速部署的步伐。通过让模型自主地相互攻防，GPT-Red 可以大幅加速漏洞发现与加固进程，从而惠及整个 AI 生态系统以及依赖更强大基础模型的下游开发者。 GPT-Red 基于自博弈强化学习构建，红队攻击模型和多个防御 LLM 通过对抗训练共同进化，而非依赖静态的人工策划攻击数据集。相关学术工作（如 Safety Self-Play, SSP）表明，单个 LLM 可以在统一的强化学习循环中同时充当攻击者和防御者，动态演化攻击策略同时增强防御能力——这一范式可能对 GPT-Red 的设计有所启发。

rss · OpenAI Blog · 7月15日 10:00

**背景**: 红队演练是从网络安全领域借鉴而来的一种结构化对抗测试方法，用于探测 AI 系统的不安全行为、漏洞和失效模式。提示注入是一种特定攻击手段，攻击者精心构造输入以覆盖模型指令并引发非预期行为，其利用了 LLM 无法清晰区分开发者指令与用户输入这一弱点。自博弈（self-play）是一种在 AlphaGo 等博弈 AI 中声名鹊起的技术，近来被引入安全领域，让模型同时扮演对抗和防御角色，从而在无需大量人工生成对抗样本的情况下迭代提升鲁棒性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/unlocking-self-improvement-gpt-red/">GPT-Red: Unlocking Self-Improvement for Robustness | OpenAI</a></li>
<li><a href="https://arxiv.org/html/2601.10589">Be Your Own Red Teamer: Safety Alignment via Self-Play and Reflective Experience Replay</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#red teaming`, `#OpenAI`, `#alignment`, `#prompt injection`

---

<a id="item-10"></a>
## [AllenAI 分享构建 Shippy 智能体的工程经验](https://huggingface.co/blog/allenai/shippy-tech-blog) ⭐️ 7.0/10

AllenAI 在 HuggingFace 博客上发表了一篇技术深度文章，详细介绍了在构建 Shippy（其 Skylight 海洋监测平台上的海事 AI 智能体）过程中积累的工程经验。核心洞见是：可靠的智能体更多依赖于确定性工具、明确的护栏、隔离的基础设施以及基于真实工作流和实时数据的评估，而非模型本身。 这篇回顾文章提供了来自一家受人尊敬的 AI 实验室的罕见而坦诚的指导，介绍了真正使生产级智能体可靠的因素，将讨论焦点从模型能力转向了工程纪律。为海事监测、医疗或金融等高风险领域构建 AI 智能体的从业者，将从中获得关于护栏、评估和基础设施隔离方面的可操作模式。 Shippy 专为高风险海事决策而设计，错误答案会带来真实后果，它利用实时船舶追踪数据回答分析人员的自然语言问题。博客强调，展示其推理过程——引用边界来源、数据截止时间和查询时间戳，并提供返回 Skylight 地图的深层链接——对于建立用户信任和可验证性至关重要。

rss · HuggingFace Blog · 7月15日 17:29

**背景**: 艾伦人工智能研究所（Ai2）是由已故微软联合创始人保罗·艾伦于 2014 年创立的非营利研究机构，专注于高影响力的开放式 AI 研究。Shippy 构建于 Ai2 的 Skylight 平台之上，该平台是一个跟踪船舶活动和海事边界的免费海洋监测系统。AI 智能体是由大语言模型驱动的系统，能够通过调用外部工具自主采取行动或回答复杂查询；在错误会带来现实后果的情况下，构建可靠的智能体仍然是应用 AI 中最难解决的问题之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/allenai/shippy-tech-blog">What building Shippy taught us about building agents</a></li>
<li><a href="https://allenai.org/blog/shippy-deep-dive">What building Shippy taught us about building agents | Ai2</a></li>
<li><a href="https://www.geekwire.com/2026/ai2s-skylight-project-launches-shippy-an-ai-agent-that-dives-into-ocean-data/">Ai2’s Skylight project launches ‘Shippy,’ an AI agent that ...</a></li>

</ul>
</details>

**标签**: `#AI-agents`, `#engineering`, `#LLM`, `#HuggingFace`, `#lessons-learned`

---

<a id="item-11"></a>
## [模型路由看似简单，实际却暗藏玄机](https://huggingface.co/blog/ibm-research/model-routing-is-simple-until-it-isnt) ⭐️ 7.0/10

Hugging Face 与 IBM Research 联合发布了一篇技术博客文章，深入探讨了模型路由系统中那些容易被忽视的复杂性，重点分析了从简单原型迈向生产级智能模型选型时所面临的挑战。 随着企业在生产环境中部署多个大语言模型以权衡成本、延迟和质量，模型路由已逐渐成为关键基础设施。然而，朴素的路由实现可能在不知不觉中降低性能或推高成本，因此这一话题对生产环境中的机器学习工程师和平台架构师具有重要价值。 该文章将模型路由视为一个涉及成本、能力、延迟和语义等多维度的优化问题，并可能进一步讨论路由层、模型注册表以及回退逻辑等生产系统必须处理的机制，远超简单的基于规则的请求分发。

rss · HuggingFace Blog · 7月15日 17:27

**背景**: 模型路由指的是根据任务复杂度、成本、性能和延迟等因素，为每个传入查询动态选择最合适的大语言模型。随着组织越来越多地运行复合 AI 系统（即串联多次大语言模型调用的流水线），每一步调用哪个模型会对输出质量和运营成本产生巨大影响。arXiv 上的论文《Optimizing Model Selection for Compound AI Systems》(2502.14815) 已经证明，每次调用的模型选择对输出质量影响显著，但搜索空间会呈指数级增长。为此，LLMRouter 等开源项目和各类商业平台纷纷涌现，提供具备智能选型、回退处理和供应商排序功能的路由层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.14815">Optimizing Model Selection for Compound AI Systems</a></li>
<li><a href="https://www.braintrust.dev/articles/best-llm-routers-2026">Best LLM routers and model routing platforms in 2026</a></li>

</ul>
</details>

**标签**: `#model-routing`, `#llm-infrastructure`, `#production-ml`, `#cost-optimization`, `#huggingface`

---

<a id="item-12"></a>
## [HuggingFace 发布 Real World VoiceEQ 语音 AI 评测基准](https://huggingface.co/blog/real-world-voiceeq) ⭐️ 7.0/10

HuggingFace 推出了 Real World VoiceEQ，这是一款用于评估语音 AI 系统在真实场景下人类感知质量的基准，基于超过 100 万条来自不同人群、说话风格和声学环境的人类评分数据构建而成。 该基准填补了语音 AI 评测中的一项公认空白——传统技术指标往往无法判断系统是否真正听起来自然、能否传递恰当的情感，以及是否能满足真实用户期望——而这些因素在语音 AI 越来越多地部署到生产应用中时至关重要。 当前基准包含 78.5 万条 TTS（文本转语音）评分和 4.8 万条 STS（语音转语音）评分，是迄今为止规模最大的人类语音 AI 评测之一。它评估的是纯文字转录无法体现的维度，包括语调、情感、说话人身份以及背景噪声处理能力。

rss · HuggingFace Blog · 7月15日 00:00

**背景**: 语音 AI 系统通常使用技术指标进行评估，例如语音识别中的词错误率（WER）或语音合成中的平均意见分（MOS）。然而，研究者越来越注意到这些指标存在缺陷，无法全面反映语音 AI 系统在实际使用中的自然度和有效性。Real World VoiceEQ 将评测范式从纯粹的技术准确性转向以人为中心的质量维度，引入了人口多样性多样化的声学环境，更贴近真实部署场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hume.ai/blog/introducing-real-world-voiceeq-measuring-the-human-quality-of-voice-ai">Introducing Real World VoiceEQ: Measuring the Human Quality ...</a></li>
<li><a href="https://github.com/huggingface/blog/blob/main/real-world-voiceeq.md">blog/real-world-voiceeq.md at main · huggingface/blog · GitHub</a></li>
<li><a href="https://www.zal-group.com/news/product-model-releases/hugging-face-real-world-voiceeq-voice-ai-benchmark">Hugging Face Launches Real World VoiceEQ Benchmark for Voice AI</a></li>

</ul>
</details>

**标签**: `#voice-ai`, `#evaluation`, `#huggingface`, `#benchmark`, `#speech-synthesis`

---

<a id="item-13"></a>
## [腾讯发布 RxBrain：面向具身智能的统一多模态模型](https://www.reddit.com/r/LocalLLaMA/comments/1ux0x0v/tencenthyembodiedrxbrain10_hugging_face/) ⭐️ 7.0/10

腾讯发布了 RxBrain（Hy-Embodied-RxBrain-1.0），这是一个约 62 亿参数的 Mixture-of-Transformers 模型，能够在单一自回归序列中统一语言推理与视觉想象，用于具身 AI 任务，包括世界状态预测和子目标规划。 通过在单一模型中交错文本推理与流匹配生成的想象帧，RxBrain 为具身 AI 提供了一种新颖的架构方案，有望减少对独立视觉和语言模块的依赖，使机器人应用中的符号规划与视觉目标预测实现更紧密的耦合。 该模型采用 Mixture-of-Transformers（MoT）主干，针对文本、视觉和生成任务设有模态特定路径。想象帧通过流匹配头解码到冻结的 FLUX VAE 潜空间，自回归序列中学习得到的 <Image> token 决定何时生成视觉内容而非文本推理。

reddit · r/LocalLLaMA · /u/jacek2023 · 7月15日 09:30

**背景**: Mixture-of-Transformers（MoT）是一种稀疏多模态 Transformer 架构，旨在解决跨文本、图像和语音模态训练统一模型时的扩展性挑战。流匹配是一种生成建模范式，结合了连续归一化流和扩散模型的优点，采样速度更快、训练更简单。交错文本-图像自回归生成以 Chameleon、Anole 和 Orthus 等模型为代表，使单一模型能够按序列同时生成离散文本 token 和连续图像特征。RxBrain 将这些思路扩展到具身 AI，将符号化的子目标规划与视觉预测的目标帧耦合在一起。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2411.04996">Mixture-of-Transformers: A Sparse and Scalable Architecture ... Mixture-of-Transformers: A Sparse and Scalable Architec ... Mixture of Experts Explained - Hugging Face Transformers vs Mixture of Experts: What’s the Real Difference? Transformer vs. Mixture of Experts in LLMs - by Avi Chawla Mixture of Experts Architecture in Transformer Models</a></li>
<li><a href="https://arxiv.org/abs/2210.02747">[2210.02747] Flow Matching for Generative Modeling - arXiv.org An introduction to Flow Matching · Cambridge MLG Blog Flow matching for generative modelling in bioinformatics and ... Understanding Flow Matching Generative Modeling with Continuous Flows: Sample Complexity ... Flow matching meets biology and life science: a survey</a></li>
<li><a href="https://arxiv.org/abs/2412.00127">[2412.00127] Orthus: Autoregressive Interleaved Image-Text ...</a></li>

</ul>
</details>

**标签**: `#multimodal`, `#embodied-ai`, `#tencent`, `#world-models`, `#robotics`

---

<a id="item-14"></a>
## [Transformers v5.14.0 新增 Thinking Machines 的 975B 多模态模型 Inkling](https://github.com/huggingface/transformers/releases/tag/v5.14.0) ⭐️ 6.0/10

Hugging Face Transformers v5.14.0 正式发布，新增对 Inkling 模型的支持——这是 Thinking Machines Lab 推出的 975B 总参数（41B 激活参数）的多模态 MoE 模型，支持文本、图像和音频输入，以开放权重形式发布。此次更新还加入了 TIPSv2 和 TIPSv2 DPT 模型，对 GPTNeoX 和 GPTBigCode 进行了破坏性变更以兼容 vLLM，优化了内核性能（SDPA prefill 配合 FlashAttention 最高提速 260%），并新增了多 token 预测（MTP）解码支持。 这一版本意义重大，因为 Inkling 是前 OpenAI CTO Mira Murati 创立的 Thinking Machines Lab 推出的首款自研 AI 模型，其被纳入 Transformers 使得一款备受关注的开放权重多模态模型能够立即被更广泛的开发者社区用于微调和集成。此外，该版本还带来了显著的推理加速（FlashAttention prefill 性能提升）和更强的推测解码能力，惠及所有在生产环境中部署大模型的开发者。 Inkling 采用混合专家（MoE）架构，每个 token 仅激活 975B 总参数中的 41B，使其在保持大模型表征能力的同时，计算成本接近一个规模小得多的稠密模型。Thinking Machines 将 Inkling 定位为一款灵活的可定制开放权重基础模型（而非追求最强性能），可通过其 Tinker 平台进行微调；本次 Transformers 集成由 molbap、Cyrilvallez、eustlb 和 zucchini-nlp 贡献。

github · ArthurZucker · 7月15日 19:02

**背景**: Hugging Face Transformers 是目前最广泛使用的开源机器学习模型库，支持文本、视觉、音频及多模态任务的推理与训练。混合专家（MoE）是一种将模型总容量与每个 token 实际激活计算量解耦的架构——例如，一个 975B 参数的 MoE 模型每个 token 可能仅激活约 41B 参数，从而以更低的推理成本实现前沿水平的模型能力。Thinking Machines Lab 是由前 OpenAI CTO Mira Murati 创立的 AI 初创公司，Inkling 是其首款开放权重模型，专为构建智能体系统、编程助手、聊天机器人和 RAG 流水线的开发者设计。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://techcrunch.com/2026/07/15/thinking-machines-amps-up-its-bet-against-one-size-fits-all-ai-with-its-first-open-model-inkling/">Thinking Machines amps up its bet against one-size-fits-all ...</a></li>
<li><a href="https://huggingface.co/docs/transformers/index">Transformers · Hugging Face</a></li>

</ul>
</details>

**标签**: `#huggingface`, `#transformers`, `#multimodal-model`, `#open-weights`, `#model-release`

---

<a id="item-15"></a>
## [Telegram 数据中心的奥秘 (2022)](https://dev.moe/en/3025) ⭐️ 6.0/10

对 Telegram 如何按地理位置组织和分配用户至其数据中心的深入技术探讨，揭示了数据中心分布与区域服务的规律。

hackernews · theanonymousone · 7月15日 13:22 · [社区讨论](https://news.ycombinator.com/item?id=48920475)

**标签**: `#telegram`, `#infrastructure`, `#data-centers`, `#distributed-systems`, `#networking`

---

<a id="item-16"></a>
## [Google is updating Gemma 4's chat templates, bringing major fixes to tool calling and reducing "laziness", and enabling Flash Attention 4 on Hopper GPUs, plus an interactive guide on how to work with and improve its vision!](https://www.reddit.com/r/LocalLLaMA/comments/1uxfu4k/google_is_updating_gemma_4s_chat_templates/) ⭐️ 6.0/10

Google announces updates to Gemma 4's chat templates, fixing tool calling issues, reducing model laziness, enabling Flash Attention 4 on Hopper GPUs, and releasing an interactive vision token budget guide.

reddit · r/LocalLLaMA · /u/Iwaku_Real · 7月15日 19:26

**标签**: `#Gemma`, `#Google`, `#LLM`, `#Flash Attention`, `#tool-calling`

---

<a id="item-17"></a>
## [德国 AI 联盟发布 Soofi S：一款在英语和德语基准测试中均名列前茅的开源 300 亿参数模型](https://www.reddit.com/r/LocalLLaMA/comments/1uxao7y/german_ai_consortium_releases_soofi_s_an_open_30b/) ⭐️ 6.0/10

德国 AI 联盟发布了开源 300 亿参数语言模型 Soofi S，该模型在英语和德语基准测试中均取得了领先成绩。

reddit · r/LocalLLaMA · /u/yogthos · 7月15日 16:21

**标签**: `#open-source`, `#LLM`, `#multilingual`, `#German-AI`, `#model-release`

---

<a id="item-18"></a>
## [苹果与 PrismML 洽谈 AI 模型压缩技术以适配 iPhone](https://www.reddit.com/r/LocalLLaMA/comments/1ux4cn2/apple_in_talks_with_startup_prismml_that_shrinks/) ⭐️ 6.0/10

据报道，苹果正在与加州理工学院孵化的初创公司 PrismML 进行早期洽谈，评估其 AI 模型压缩技术，该技术可将大型模型压缩至直接在 iPhone 上运行，内存占用减少最高达 15 倍。 这表明苹果正将端侧 AI 作为战略差异化方向持续加码，有望降低对云端推理的依赖，并与谷歌、三星的边缘 AI 布局形成竞争。对于本地大模型社区而言，这印证了面向消费级设备运行的压缩模型市场需求正在快速增长。 据报道，PrismML 的技术已可将一个 270 亿参数的模型压缩后在 iPhone 上运行，并在一次演示中将一个 54 GB 的模型压缩至不足 4 GB。双方洽谈仍处于早期阶段，尚未确认收购或合作，其具体的压缩方法（如量化、剪枝或知识蒸馏）也未公开披露。

reddit · r/LocalLLaMA · /u/Ready_Performance_35 · 7月15日 12:23

**背景**: AI 模型压缩涵盖量化（降低模型权重的数值精度）、剪枝（移除冗余连接）和知识蒸馏（训练小模型模仿大模型）等技术。端侧 AI（又称边缘推理）指直接在手机或物联网设备上运行模型，而非依赖远程服务器，从而在延迟、隐私和离线可用性方面具有优势。PrismML 是众多致力于实现激进压缩比的初创公司之一，竞品还包括 OctoML 和 Deeplite，它们的目标都是让十亿参数级的大语言模型能够在消费级硬件上运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/14/apple-prismml-ai-compression-iphone.html">Apple in talks with startup that shrinks AI models to run on ...</a></li>
<li><a href="https://thenextweb.com/news/apple-prismml-on-device-ai-compression-iphone">Apple eyes PrismML’s on-device AI for the iPhone - TNW</a></li>
<li><a href="https://cryptobriefing.com/apple-prismml-ai-model-compression-iphone/">Apple in talks with PrismML to shrink AI models for iPhone ...</a></li>

</ul>
</details>

**标签**: `#Apple`, `#model-compression`, `#on-device-AI`, `#PrismML`, `#edge-AI`

---