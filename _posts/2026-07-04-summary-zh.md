---
layout: default
title: "Horizon Summary: 2026-07-04 (ZH)"
date: 2026-07-04
lang: zh
---

> 从 69 条内容中筛选出 13 条重要资讯。

---

1. [Karpathy 发布 nanochat：用 100 美元打造最强的 ChatGPT 克隆](#item-1) ⭐️ 8.0/10
2. [泄露 YouTube 创作者的私密视频](#item-2) ⭐️ 8.0/10
3. [Claude Code 调查跨账户响应泄露报告](#item-3) ⭐️ 7.0/10
4. [Meta 数据中心因污染水源被暂停排水](#item-4) ⭐️ 7.0/10
5. [天体物理学家对韦伯望远镜揭示的新宇宙感到困惑](#item-5) ⭐️ 7.0/10
6. [告别百万级动捕棚！上海交大提出 HAT-4D，单目视频直出 4D 交互场景](#item-6) ⭐️ 7.0/10
7. [多块扩散语言模型弥合训练与推理间的差距](#item-7) ⭐️ 7.0/10
8. [Mistral 发布 Leanstral 1.5：专用于形式化验证的 119B MoE 模型](#item-8) ⭐️ 7.0/10
9. [huggingface/transformers 发布 v5.13.0](#item-9) ⭐️ 6.0/10
10. [每美元性能正在变得更快、更便宜](#item-10) ⭐️ 6.0/10
11. [Google DeepMind 与 A24 宣布建立开创性研究合作伙伴关系](#item-11) ⭐️ 6.0/10
12. [Google Research 发布 TabFM：零样本表格数据基础模型](#item-12) ⭐️ 6.0/10
13. [对 2 万美元本地 AI 设备盈亏平衡点的实际计算](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Karpathy 发布 nanochat：用 100 美元打造最强的 ChatGPT 克隆](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy 在 GitHub 上创建了一个名为 nanochat 的新项目，标语为「100 美元能买到的最强 ChatGPT」，目标是提供一套极简的全栈大语言模型训练系统，让用户在极低的算力预算下训练出类似 ChatGPT 的对话模型。 Karpathy 是 AI/ML 教育领域最具影响力的声音之一，此前推出的 nanoGPT 等项目广受开发者追捧，因此他的每一个新仓库都会引发社区高度关注，并影响开发者学习大模型训练的方式。而 100 美元这一极低预算目标，也重新定义了人们对低成本训练的关注 —— 在前沿模型研发被资金雄厚的实验室主导的当下，这一点尤为有意义。 该项目围绕「单一复杂度调节旋钮（single-complexity-dial）」的设计理念构建，仓库中还引入了「Time-to-GPT-2 排行榜」这一概念，用于对训练效率进行基准对比。不过由于项目尚处于早期阶段，公告中仅有一句极简描述，完整的技术细节、代码结构和训练流程还未公开。

github · karpathy · 7月4日 03:44

**背景**: Andrej Karpathy 是 OpenAI 的联合创始人之一、前特斯拉 AI 总监，被公认为现代深度学习领域最杰出的教育者之一。他此前推出的极简风格教学仓库 —— 如 nanoGPT（仅用几百行代码从零重新实现 GPT-2 的训练流程）—— 已成为希望深入理解大模型训练实践的开发者的首选学习资源。nanochat 沿用了同样的「nano」理念，但更进一步，涵盖从预训练到后训练（如指令微调）的完整端到端流程，以产出可用的对话助手。100 美元预算的主张也呼应了业界对「一个能用的聊天模型是否真的需要数亿美元训练成本」的广泛反思。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy/nanochat: The best ChatGPT that $100 can ...</a></li>
<li><a href="https://deepwiki.com/karpathy/nanochat">karpathy/nanochat | DeepWiki</a></li>

</ul>
</details>

**标签**: `#LLM`, `#fine-tuning`, `#Andrej Karpathy`, `#chat-models`, `#cost-efficient-training`

---

<a id="item-2"></a>
## [泄露 YouTube 创作者的私密视频](https://javoriuski.com/post/youtube) ⭐️ 8.0/10

一个已披露的 YouTube 漏洞利用 YouTube Studio 中 AI 建议评论回复的提示注入功能,从而泄露创作者的私密/未公开视频。

hackernews · javxfps · 7月4日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=48786781)

**标签**: `#security`, `#prompt-injection`, `#youtube`, `#vulnerability-disclosure`, `#ai-security`

---

<a id="item-3"></a>
## [Claude Code 调查跨账户响应泄露报告](https://github.com/anthropics/claude-code/issues/74066) ⭐️ 7.0/10

在 anthropics/claude-code 仓库的 GitHub issue #74066 中，用户报告了工作区实例之间可能存在的会话/缓存泄露问题，来自不同 LLM 提供商（Claude、GPT 和 Gemini）的多名用户描述了类似的跨账户响应污染现象。Claude Code 团队的 Thariq 回应称，他们相信这些报告是幻觉，但正在认真调查此事。 如果得到证实，跨账户响应污染将代表 LLM API 基础设施中的一个严重安全漏洞，可能在租户之间暴露用户私密数据——这是对基本多租户隔离保证的违反。来自多个提供商的独立报告的广泛性，引发了关于 LLM 网关、负载均衡器和缓存层如何处理并发请求和共享基础设施的系统性担忧。 一位技术评论者指出了一个可能的根本原因：API 网关错误地处理 HTTP 100（Continue）状态码，导致一个偏移错误（off-by-one），可能造成并发会话之间的响应交换。原始发帖者的场景包含超过 800K token 的上下文窗口，以及一个工具调用结果中文件路径包含 'minecraft.py'，一些人认为这更可能是幻觉而非实际泄露。

hackernews · chatmasta · 7月4日 14:03 · [社区讨论](https://news.ycombinator.com/item?id=48785485)

**背景**: Claude Code 是 Anthropic 推出的智能体命令行工具，允许开发者直接从终端与 Claude 模型交互来执行代码库操作。LLM API 通常通过共享基础设施（包括 API 网关、负载均衡器和缓存层）同时为多个用户提供服务。会话隔离是一项基本安全属性，确保一个用户的对话上下文和响应永远不会被另一个用户看到。相比之下，幻觉是一种众所周知的现象，即 LLM 生成看似合理但虚构的输出——通常由大上下文窗口或异常提示模式触发——这可能与真实的数据泄露相混淆。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48785485">Potential session/cache leakage between workspace instances or consumer accounts | Hacker News</a></li>
<li><a href="https://deepwiki.com/anthropics/claude-code/1.1-system-architecture">System Architecture | anthropics/claude-code | DeepWiki</a></li>
<li><a href="https://www.giskard.ai/knowledge/cross-session-leak-when-your-ai-assistant-becomes-a-data-breach">Cross Session Leak: LLM security vulnerability & detection guide</a></li>

</ul>
</details>

**社区讨论**: 社区意见在严肃的技术分析和怀疑态度之间分化。原始的临时账户和多位评论者提供了详细的技术证据，包括一家提供方的事后分析报告，将响应交换归因于 API 网关中 HTTP 100 状态码处理的 bug，增强了此担忧的可信度。然而，其他评论者——包括 Claude Code 团队本身——倾向于认为幻觉是更可能的解释，指出超大上下文（800K+ tokens）和特定提示模式可以触发看似合理但虚构的响应。Gemini 和 GPT 的多位用户也报告了类似经历，将调查范围扩大到 Claude 之外。

**标签**: `#claude-code`, `#security`, `#llm-infrastructure`, `#data-leakage`, `#anthropic`

---

<a id="item-4"></a>
## [Meta 数据中心因污染水源被暂停排水](https://www.tomshardware.com/tech-industry/data-centers/cheyenne-suspends-data-center-fill-and-flush-and-closed-loop-discharges-after-meta-contractor-contaminated-its-reuse-water-system) ⭐️ 7.0/10

Meta 的数据中心承包商使用添加剂污染了夏延市的水回用系统，导致该市暂停了水填充/冲洗作业及闭环排放作业。

hackernews · sensanaty · 7月4日 16:45 · [社区讨论](https://news.ycombinator.com/item?id=48786782)

**标签**: `#data-centers`, `#environment`, `#meta`, `#water-pollution`, `#ai-infrastructure`

---

<a id="item-5"></a>
## [天体物理学家对韦伯望远镜揭示的新宇宙感到困惑](https://www.quantamagazine.org/astrophysicists-puzzle-over-webbs-new-universe-20260702/) ⭐️ 7.0/10

詹姆斯·韦伯太空望远镜（JWST）在早期宇宙中观测到的神秘"小红点"令天体物理学家感到困惑，这些天体可能代表一种被称为"黑洞星"的新型天体类别，其周围的气体茧状结构像恒星大气一样发光。

hackernews · jnord · 7月4日 09:08 · [社区讨论](https://news.ycombinator.com/item?id=48783948)

**标签**: `#astronomy`, `#astrophysics`, `#jwst`, `#cosmology`, `#science-journalism`

---

<a id="item-6"></a>
## [告别百万级动捕棚！上海交大提出 HAT-4D，单目视频直出 4D 交互场景](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247901356&idx=3&sn=54ee94026f76691a380cd3ea214e0def) ⭐️ 7.0/10

上海交通大学研究者提出了 HAT-4D，一个智能体框架，能够直接从单目视频重建动态 4D 多物体交互场景，专门针对现有方法在严重遮挡和复杂多物体动态下表现不住的难题。 HAT-4D 通过将海量野外单目视频转换为可用于仿真的 4D 场景，为扩展具身智能和训练 VLA 模型提供了一条高效低成本的数据采集路径，有望替代昂贵的动捕工作室。 与以往主要聚焦于单物体的单目 4D 重建方法不同，HAT-4D 专为处理严重遮挡下的多物体交互而设计。它与 OVOW（实例级 4D 网格重建）和 ArtHOI（铰接式人-物交互）等工作一同，被定位为具身智能世界模型研究的基础数据设施。

rss · 量子位 · 7月3日 03:43

**背景**: 4D 场景重建指从视觉输入中恢复随时间变化的动态 3D 几何。单目视频重建尤其困难，因为单相机下深度本身具有内在歧义，而多物体交互引入的严重遮挡会严重影响深度估计。具身智能和 VLA（视觉-语言-动作）模型需要大量交互数据，传统上依赖多相机校准的动捕棚进行采集，成本高昂，使得大规模野外数据采集成为主要瓶颈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.28215">HAT-4D: Lifting Monocular Video for 4D Multi-Object ...</a></li>
<li><a href="https://arxiv.org/html/2606.28215v1">HAT-4D: Lifting Monocular Video for 4D Multi-Object ...</a></li>
<li><a href="https://onevideooneworld.github.io/">OVOW: One Video , One World — Turning Monocular Video into...</a></li>

</ul>
</details>

**标签**: `#4D-scene-generation`, `#computer-vision`, `#monocular-video`, `#human-object-interaction`, `#research`

---

<a id="item-7"></a>
## [多块扩散语言模型弥合训练与推理间的差距](https://www.reddit.com/r/LocalLLaMA/comments/1un8y5p/paper_multiblock_diffusion_language_models/) ⭐️ 7.0/10

该论文提出了多块扩散语言模型（MBD-LMs），通过一种新的多块教师强制（MultiTF）策略对块扩散语言模型进行后训练，使其匹配多块扩散（MultiBD）推理时的状态，并配套设计了一种块缓冲区（Block Buffer）解码算法，能够保留前缀缓存复用并保持输入形状固定。 这项研究直接解决了并行块扩散解码中训练与推理不匹配的痛点，在实现近 2 倍吞吐量提升（TPF 从 3.47 提升至 6.19）的同时还提高了准确率，使基于扩散的文本生成在生产中更实用，也与 LLaDA 和 Mercury 等同类并行生成方案形成直接竞争。 MBD-LLaDA2-Mini 将平均每次前向生成的 token 数（TPF）从 3.47 提升到 6.19，准确率从 79.95% 提高到 81.03%；结合 DMax 解码方案后，MBD-LLaDA2-Mini-DMax 在数学和代码基准测试上达到平均 9.34 的 TPF，而准确率仅下降 1.02%，其关键机制是能复用前缀 KV 缓存的块缓冲区。

reddit · r/LocalLLaMA · /u/pmttyji · 7月4日 13:21

**背景**: 块扩散语言模型（BD-LMs）作为 ICLR 2025 Oral 论文提出，将 token 序列划分为多个块并在每个块内执行离散去噪，在自回归与全序列扩散之间进行插值，从而兼具并行生成和灵活长度的优势。自回归 Transformer 在生成时通过 KV 缓存避免重复计算历史 token 的表征，这是推理速度的关键优化。Diffusion Forcing 是一种训练策略，允许每个 token 拥有不同的噪声水平，使因果下一 token 预测模型能够在不完全扩散过去 token 的情况下生成未来 token。MBD-LMs 在 BD-LMs 的基础上将单块解码扩展为一个由连续块组成的运行集合的并发解码，但现有训练方案（对单个噪声块的教师强制或扩散强制）都与这种多块推理状态不匹配，由此产生的训练-推理差距正是本文要解决的问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2503.09573">[2503.09573] Block Diffusion: Interpolating Between ... A arXiv:2503.09573v3 [cs.LG] 17 May 2025 Block Diffusion - m-arriola.com GitHub - kuleshov-group/bd3lms: [ICLR 2025 Oral] Block ... Awesome Diffusion Language Models - GitHub DiffusionGemma — Google DeepMind Encoder-Decoder Diffusion Language Models for Efficient ...</a></li>
<li><a href="https://github.com/kuleshov-group/bd3lms">GitHub - kuleshov-group/bd3lms: [ICLR 2025 Oral] Block ...</a></li>
<li><a href="https://arxiv.org/abs/2407.01392">[2407.01392] Diffusion Forcing : Next-token Prediction Meets...</a></li>

</ul>
</details>

**标签**: `#diffusion-models`, `#language-models`, `#research-paper`, `#text-generation`, `#parallel-decoding`

---

<a id="item-8"></a>
## [Mistral 发布 Leanstral 1.5：专用于形式化验证的 119B MoE 模型](https://www.reddit.com/r/LocalLLaMA/comments/1umgdhx/mistral_released_leanstral15119ba6b/) ⭐️ 7.0/10

Mistral 发布了 Leanstral 1.5 模型，这是一个采用 Apache-2.0 许可证的 119B（激活参数 6B）混合专家（MoE）模型，专门用于形式化验证和自动定理证明。它在 FATE-H（87%）和 FATE-X（34%）上达到了最先进水平，在 miniF2F 上达到饱和，解决了 PutnamBench 587/672 个问题，并在测试的 57 个代码仓库中发现了 5 个此前未知的 bug。 此次发布证明了专门的小激活参数模型能够在形式化验证这类细分领域达到前沿水平，为通用大语言模型提供了一种具有成本效益的开源替代方案。它还通过发现传统测试和模糊测试遗漏的 bug，展示了切实的实际应用价值，可能对软件验证工作流程产生重大影响。 该模型采用了三阶段训练流程：中训练、监督微调，以及使用 CISPO（Clipped Importance Sampling Policy Optimization，裁剪重要性采样策略优化）算法的强化学习。CISPO 通过裁剪重要性采样权重来限制方差，比 PPO 和 GRPO 等方法具有更好的稳定性。尽管总参数量为 119B，但每次推理仅激活 6B 参数，这使其在能力范围内具备较高的计算效率。

reddit · r/LocalLLaMA · /u/Tall-Ad-7742 · 7月3日 14:44

**背景**: Lean 是一个免费、开源的定理证明器和函数式编程语言，基于带归纳类型的构造演算，广泛用于数学化证明软件的正确性。miniF2F 是一个包含竞赛级数学问题（AMC、AIME、IMO）的基准测试，已被形式化到多个证明系统中，而 PutnamBench 是一个包含 640 道题的多语言基准套件，使用 Lean、Isabelle 和 Coq 对 Putnam 竞赛问题进行了形式化。FATE-H 和 FATE-X 是专门为评估大语言模型在 Lean 等形式化验证任务上的表现而设计的评测基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/cispo-algorithm">CISPO: Clipped Importance Sampling RL - emergentmind.com</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/putnambench">PutnamBench : Theorem Proving Benchmark</a></li>

</ul>
</details>

**社区讨论**: 社区反应褒贬不一。一些用户（如 u/InsideOutSanta）赞扬了 Mistral 的细分领域专业化策略，认为高质量的小模型对于特定任务非常有价值。然而，u/boulos 和 u/Groxx 对其中一个具体的 bug 发现示例提出了质疑，Groxx 指出在博客发布前一周，受影响仓库就已经提交了相同的 issue。u/andai 批评对比基准已经过时，所用模型都是半年前的，u/raphinou 则询问没有 Lean 经验的开发者如何上手使用。

**标签**: `#formal-verification`, `#theorem-proving`, `#Mistral`, `#open-source`, `#code-verification`

---

<a id="item-9"></a>
## [huggingface/transformers 发布 v5.13.0](https://github.com/huggingface/transformers/releases/tag/v5.13.0) ⭐️ 6.0/10

Hugging Face Transformers v5.13.0 新增了对 Kimi K2.5、K2.6 和 K2.7 开源多模态智能体模型的架构支持。

github · vasqu · 7月3日 16:06

**标签**: `#huggingface`, `#transformers`, `#kimi-k2`, `#model-release`, `#open-source`

---

<a id="item-10"></a>
## [每美元性能正在变得更快、更便宜](https://www.wafer.ai/blog/glm52-amd) ⭐️ 6.0/10

博客文章比较了 AMD 硬件上的 AI 推理性价比，社区讨论重点关注了 FP4 量化精度的关键问题以及缺失的性能功耗比指标。

hackernews · latchkey · 7月3日 21:49 · [社区讨论](https://news.ycombinator.com/item?id=48780417)

**标签**: `#AI-hardware`, `#GPU-benchmarking`, `#AMD`, `#quantization`, `#cost-optimization`

---

<a id="item-11"></a>
## [Google DeepMind 与 A24 宣布建立开创性研究合作伙伴关系](https://deepmind.google/blog/google-deepmind-and-a24-announce-first-of-its-kind-research-partnership/) ⭐️ 6.0/10

Google DeepMind 与 A24 宣布建立独特的合作伙伴关系，共同探索人工智能与电影制作领域的交叉融合。

rss · Google DeepMind Blog · 7月3日 14:25

**标签**: `#AI`, `#DeepMind`, `#creative-AI`, `#filmmaking`, `#industry-partnership`

---

<a id="item-12"></a>
## [Google Research 发布 TabFM：零样本表格数据基础模型](https://www.reddit.com/r/LocalLLaMA/comments/1un5hyi/googletabfm100/) ⭐️ 6.0/10

Google Research 发布了零样本表格数据基础模型 TabFM（1.0.0 版本），支持对包含混合数值型和类别型列的数据集进行分类和回归任务，无需微调或超参数搜索。只需通过一次前向传播，将训练样本作为上下文输入即可得到预测结果，模型已在 Hugging Face 和 GitHub 上发布，并即将集成到 BigQuery 中。 表格数据是企业机器学习工作负载的主要基础，但在从基础模型范式中获益方面一直落后于文本和图像领域。TabFM 通过消除针对特定数据集的训练和超参数调优过程，可能会大幅降低在结构化数据上部署机器学习的门槛，其定位相当于 Google TimesFM 时间序列模型在表格领域的对应物。 TabFM 在底层扩展了由 TabPFN 开创的 PFN 路线，采用对抗预训练 Transformer（APT）架构，通过合成数据智能体进行训练，从而在不使用任何真实数据集预训练的情况下实现零样本元学习。与传统表格机器学习流水线不同，它将预测视为上下文学习而非参数拟合，因此主要适用于分类和回归任务，而非生成式场景。

reddit · r/LocalLLaMA · /u/Balance- · 7月4日 10:20

**背景**: 表格基础模型是一类新兴的神经网络架构，在异构表格数据上进行预训练，为下游任务提供可迁移的先验知识。这一范式由 TabPFN 开创，它从贝叶斯视角构建表格数据上的上下文学习（ICL），近似合成数据集上的后验预测分布。后续工作如 TabICL 通过学习到的上下文蒸馏、样本选择、线性注意力以及基于超网络的任务特定生成等技术，将这一方法推向规模化。TabFM 携 Google 的工业级力量加入了这一发展轨迹。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM: A zero-shot foundation model for tabular data</a></li>
<li><a href="https://arxiv.org/abs/2502.04573">[2502.04573] Zero-shot Meta-learning for Tabular Prediction ... Google TabFM: Zero-Shot Foundation Model for Tabular ... Zero-shot Meta-learning for Tabular Prediction Tasks with ... Zero-shot Meta-learning for Tabular Prediction Tasks with ... Google's TabFM: Zero-shot tabular classification without tra google/tabfm-1.0.0-pytorch · Hugging Face</a></li>
<li><a href="https://www.explainx.ai/blog/google-tabfm-zero-shot-tabular-foundation-model-2026">Google TabFM: Zero-Shot Foundation Model for Tabular ...</a></li>

</ul>
</details>

**标签**: `#tabular-data`, `#foundation-models`, `#zero-shot-learning`, `#google-research`, `#machine-learning`

---

<a id="item-13"></a>
## [对 2 万美元本地 AI 设备盈亏平衡点的实际计算](https://www.reddit.com/r/LocalLLaMA/comments/1un6njn/doing_the_actual_math_on_a_20k_local_ai_rig/) ⭐️ 6.0/10

通过成本分析模型，对比 2 万美元本地 AI 设备的电力消耗和硬件前期成本与每月 200 美元的订阅服务，计算出实际的盈亏平衡交叉点。

reddit · r/LocalLLaMA · /u/shyaaaaaaaaaaam · 7月4日 11:27

**标签**: `#local-llm`, `#cost-analysis`, `#self-hosting`, `#hardware`, `#economics`

---