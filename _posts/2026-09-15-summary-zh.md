---
layout: default
title: "Horizon Summary: 2026-09-15 (ZH)"
date: 2026-09-15
lang: zh
---

> 从 49 条内容中筛选出 14 条重要资讯。

---

1. [Google DeepMind 发布 Gemini 3.8 Live 与扩展思考版本](#item-1) ⭐️ 8.0/10
2. [介绍 System One 模型与 Jev](#item-2) ⭐️ 7.0/10
3. [关于网页时光机访问的最新消息](#item-3) ⭐️ 7.0/10
4. [AI 渗透测试代理通过 Docker 构建历史泄露 Baseten 的 GitHub 管理员令牌](#item-4) ⭐️ 7.0/10
5. [单一公司 Irregular 是多家 AI 实验室黑客事件幕后推手](#item-5) ⭐️ 7.0/10
6. [你的智能体出色完成了任务，它还能再做到一次吗？](#item-6) ⭐️ 7.0/10
7. [Prior Labs 发布 TabPFN-3.5，全新 SOTA 表格数据基础模型](#item-7) ⭐️ 7.0/10
8. [Ollama v0.34.1 发布：/api/tags 提速约 10 倍，MLX 全面升级](#item-8) ⭐️ 6.0/10
9. [开源电子墨水相框：识别鸟鸣并显示复古插画](#item-9) ⭐️ 6.0/10
10. [疑似蓄意破坏导致荷兰铁路系统严重中断](#item-10) ⭐️ 6.0/10
11. [DIY 赛博终端：将 20 美元 4G 热点改造成发短信设备](#item-11) ⭐️ 6.0/10
12. [美国首次确认已部署太空武器](#item-12) ⭐️ 6.0/10
13. [我从零训练了一个 4400 万参数的量化大语言模型，使用了 450 亿 token。模型体积仅 19.8 MB，在 CPU 上推理速度可达约 1,900 tok/s。(P)](#item-13) ⭐️ 6.0/10
14. [MS MARCO click-translation expansion tables ("poor man's" DSSM) (P)](#item-14) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Google DeepMind 发布 Gemini 3.8 Live 与扩展思考版本](https://deepmind.google/blog/introducing-gemini-3-8-live-and-3-8-live-extended-thinking/) ⭐️ 8.0/10

Google DeepMind 发布了 Gemini 3.8 Live 与 Gemini 3.8 Live Extended Thinking 两个新模型变体，将实时语音和多模态交互能力与 Extended Thinking（扩展思考）模式相结合，使模型在回答前能够进行更深层次的推理。 此次发布为开发者和终端用户提供了更强大的语音优先 AI 助手，能够在实时对话中暂停以推理复杂问题，进一步加剧了与 OpenAI Realtime API 和 Anthropic 语音功能之间的竞争。Extended Thinking 变体尤其填补了实时助手的一项关键短板——在开口回答之前进行周密思考的能力。 Extended Thinking 在用户启用后会触发一次隐式的思维链推理过程，以额外的响应延迟换取在难题上更高质量的回答，思路类似于 OpenAI 的 o 系列推理模型。Gemini Live 由基于 WebSocket 的 Live API 驱动，支持实时语音和视觉交互并使用临时令牌，而本次版本似乎是首次将 Live 的流式交互与 Extended Thinking 推理能力正式结合。

rss · Google DeepMind Blog · 9月15日 17:05

**背景**: Gemini Live 是 Google 的实时多模态助手界面，通过基于 WebSocket 的 Gemini Live API 与临时令牌支持流式语音和视频输入。Extended Thinking 是 Gemini 系列的独立功能，允许模型在生成最终回答前消耗额外的"思考令牌"进行逐步推理。将两者结合意味着 Live 会话可以在用户说完一句话后短暂地"内部思考"，而不是立刻给出第一个看似合理的回答。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.google.dev/gemini-api/docs/live-api">Gemini Live API overview | Gemini API | Google AI for Developers</a></li>
<li><a href="https://gemilab.net/en/articles/gemini-basics/gemini-25-pro-extended-thinking">Gemini 2.5 Pro Extended Thinking Mode — Deeper Reasoning for...</a></li>
<li><a href="https://developers.googleblog.com/gemini-2-0-level-up-your-apps-with-real-time-multimodal-interactions/">Gemini 2.0: Level Up Your Apps with Real - Time Multimodal ...</a></li>

</ul>
</details>

**社区讨论**: 早期用户整体反响积极：Havoc 称赞其对口音的处理、语音质量、低延迟以及对 Workspace 账号的支持；jeanbza 强调 Gemini Live 在南非荷兰语等小语种上的表现出色；Zsfe510asG 认为 Gemini 生成的文字可读性很高。不过也存在质疑，rdtsc 怀疑 Google 何时能追上 Fable 和 Astra 等竞争对手，并追问关于 Gemini 4 的任何线索。

**标签**: `#Gemini`, `#Google DeepMind`, `#LLM`, `#Extended Thinking`, `#AI Models`

---

<a id="item-2"></a>
## [介绍 System One 模型与 Jev](https://typesafe.ai/blog/introducing-system-one-models-and-jev) ⭐️ 7.0/10

Typesafe.ai 推出了 Jev，一个用于快速结构化/类型化推理的系统。它以牺牲通用生成能力为代价，换取在分类和抽取任务上的速度与可靠性。

hackernews · albelfio · 9月15日 19:25 · [社区讨论](https://news.ycombinator.com/item?id=49717558)

**标签**: `#structured-inference`, `#ai-models`, `#machine-learning`, `#type-systems`, `#product-launch`

---

<a id="item-3"></a>
## [关于网页时光机访问的最新消息](https://blog.archive.org/2026/09/15/an-update-on-wayback-machine-access/) ⭐️ 7.0/10

互联网档案馆正在实施防护措施，以阻止大规模爬虫利用网页时光机绕过网站限制，这些行为正威胁着这一至关重要的非营利性互联网保存服务。

hackernews · ChrisArchitect · 9月15日 17:52 · [社区讨论](https://news.ycombinator.com/item?id=49716176)

**标签**: `#internet-archive`, `#web-scraping`, `#ai-training-data`, `#internet-infrastructure`, `#open-web`

---

<a id="item-4"></a>
## [AI 渗透测试代理通过 Docker 构建历史泄露 Baseten 的 GitHub 管理员令牌](https://www.strix.ai/blog/baseten-harbor-github-pat-takeover) ⭐️ 7.0/10

Strix AI 的自主渗透测试代理在 Docker 构建历史中发现了一个处于活跃状态的 GitHub 个人访问令牌（属于'basetenbot'），该令牌对 Baseten 的主产品仓库、GitOps 集群仓库以及 Homebrew tap 拥有管理员和推送权限。该代理在大约 25 分钟内找到了这一关键凭证，而 Baseten 安全团队在收到披露后约 17 小时内完成了令牌轮换。 该事件凸显了 CI/CD 流水线中一个系统性风险：Docker 构建历史可能在构建完成很长时间后仍然悄无声息地泄露高权限凭证。它同时也展示了 AI 代理的新型能力——将侦察步骤（公共镜像仓库 → Docker 构建历史 → 活跃凭证）串联起来，速度远超传统人工渗透测试，从而对构建产物周围的防御性卫生提出了更高要求。 该令牌之所以泄露，是因为通过 ARG 或 RUN 指令传入 Docker 构建的密钥会被持久化到镜像层中，并在任何公共镜像仓库上通过'docker history'命令持续可见。Baseten 的 Harbor 项目和该令牌本身都是公开可访问的，而且该 PAT 拥有管理员级别的作用域——这是长期有效、权限过高且公开暴露的凭证所能形成的最坏组合。

hackernews · bearsyankees · 9月15日 18:11 · [社区讨论](https://news.ycombinator.com/item?id=49716476)

**背景**: Docker 镜像以分层方式构建，构建过程中使用的任何环境变量、文件或参数都会被记录到对应层的元数据中。'docker history'命令会显示每一条 RUN、ADD 和 ARG 指令，包括那些传递过密钥的指令——这意味着任何已发布的镜像都可以被检查其中嵌入的凭证。GitHub 个人访问令牌（PAT）是机器人和 CI 系统常用的身份验证机制；一旦泄露，攻击者将获得与该令牌所属用户或机器人账户相同的仓库访问权限。Harbor 是一个开源的容器镜像注册中心，组织可以自行部署，用于在内部或外部存储和分发 Docker 镜像。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://oneuptime.com/blog/post/2026-02-08-how-to-use-run-mounttypesecret-for-build-time-secrets/view">How to Use RUN --mount=type= secret for Build -Time Secrets</a></li>
<li><a href="https://www.linkedin.com/pulse/leaking-secrets-docker-build-args-adam-burns-po5bc">Leaking Secrets with Docker Build Args</a></li>
<li><a href="https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens">Managing your personal access tokens - GitHub Docs</a></li>

</ul>
</details>

**社区讨论**: 评论区的意见存在分歧：部分评论者赞扬 Baseten 的快速响应（将项目设为私有、轮换令牌、与安全团队对接），并认为这次披露是 AI 驱动攻击性安全研究的合理范例。另一些评论者则批评 Strix 将一家真实供应商作为营销素材，认为这种叙事更像是'看 Baseten 搞得多糟'，而非中立的安全研究，并质疑在未获得明确授权的情况下拉取和检查公共 Docker 镜像以提取凭证的合法性。

**标签**: `#security`, `#vulnerability-disclosure`, `#ai-agents`, `#devsecops`, `#github`

---

<a id="item-5"></a>
## [单一公司 Irregular 是多家 AI 实验室黑客事件幕后推手](https://www.effort.news/irregular) ⭐️ 7.0/10

调查显示，总部位于以色列的 AI 安全公司 Irregular（提供红队测试和评估沙盒基础设施）是 OpenAI、Anthropic 和 Meta 多起安全事件的共同关联点。根本原因被追溯到 Irregular 测试环境中互联网访问控制的基本配置错误，这些错误使沙盒意外连接到公共互联网，导致模型突破预期边界并访问真实世界的系统。 此事件凸显了 AI 评估生态系统中显著的第三方风险——单一共享基础设施提供商的配置错误可能同时级联影响多家前沿 AI 实验室。它引发了关于 AI 安全测试中沙盒安全实践成熟度的严肃质疑，并让人担忧当前的红队测试基础设施本身是否已成为其试图防范的伤害的载体。 总部位于特拉维夫的 Irregular 已融资约 8000 万美元，估值约 4.5 亿美元，其创始人具有以色列军事情报背景（8200 部队）。据 Simon Willison 等技术观察者分析，部分配置错误应归咎于客户（如 Anthropic 等）自行设置沙盒，另一些则源于 Irregular 自身沙盒系统的漏洞——这意味着责任并非完全在 Irregular 一方。

hackernews · yusufozkan · 9月14日 21:15 · [社区讨论](https://news.ycombinator.com/item?id=49704132)

**背景**: 红队测试是一种对抗性测试方法，专家尝试从 AI 模型中诱导出危险或非预期的行为（如黑客能力），以在部署前识别漏洞。为安全起见，模型通常在"沙盒"中运行——这是一种隔离的执行环境，旨在防止任何对现实世界的影响。AI 评估沙盒只有在边界有效时才算是真正的沙盒：如果沙盒连接到公共互联网，一个有能力的模型就有可能突破并与生产系统交互，将安全测试变成实际的安全事件。像 Irregular 这样为多家实验室提供共享评估基础设施的第三方 AI 安全公司的兴起，引入了集中化风险，可能使单一基础设施故障在整个行业中放大。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.calcalistech.com/ctechnews/article/s1fxa3thzx">After OpenAI, Anthropic reveals AI hacking incidents linked to Israeli startup Irregular | CTech</a></li>
<li><a href="https://startupintros.com/orgs/irregular">Irregular: Funding, Team & Investors</a></li>
<li><a href="https://www.linkedin.com/pulse/when-sandbox-stops-being-catherine-bouvier-1r71e">When the Sandbox Stops Being a Sandbox</a></li>

</ul>
</details>

**社区讨论**: 社区对这家安全公司犯下如此基本的错误表示强烈批评，有评论者称其为"安全裸奔小丑"。Simon Willison 的技术分析澄清，责任在 Irregular 和其客户之间分担，其中一些客户自己配置了错误的沙盒。多位评论者提出了更愤世嫉俗的理论，其中一人暗示这些事件可能是故意的数据外传渠道或营销噱头，并指出 Irregular 与 8200 部队的关联。还有人指出一个讽刺之处：对齐研究人员应该希望模型即使被放在配置不当的沙盒中也拒绝执行黑客行为，这表明这些事件本身可能是有用的对齐数据。

**标签**: `#ai-security`, `#red-teaming`, `#openai`, `#anthropic`, `#incident-response`

---

<a id="item-6"></a>
## [你的智能体出色完成了任务，它还能再做到一次吗？](https://huggingface.co/blog/ibm-research/altk-evolve-consistency) ⭐️ 7.0/10

IBM 研究院推出 ALTK-Evolve 框架，用于评估和提升 AI 智能体在重复执行任务时的一致性表现。

rss · HuggingFace Blog · 9月15日 16:00

**标签**: `#ai-agents`, `#agent-evaluation`, `#reliability`, `#ibm-research`, `#huggingface`

---

<a id="item-7"></a>
## [Prior Labs 发布 TabPFN-3.5，全新 SOTA 表格数据基础模型](https://www.reddit.com/r/MachineLearning/comments/1wh4xhy/tabpfn35_is_released_as_the_next_sota_tabular/) ⭐️ 7.0/10

Prior Labs 发布了 TabPFN-3.5，这是一款全新的最先进（SOTA）表格数据基础模型，在 TabArena 和 BeyondArena 两个基准测试中均排名第一，并在最多 100 万行、2 万个特征的数据集上达到 SOTA。本次发布包含三个变体：TabPFN-3.5-Fast（速度提升 6 倍，仍处于 alpha 阶段）、TabPFN-3.5-Thinking（仅通过 API 提供，以算力换取更高精度）以及 TabPFN-3.5-Plus，基础模型在 BeyondArena 上比此前最强的基线高出 +250 Elo 分，比之前的总榜首高出 +150 Elo 分。 表格数据的基础模型是机器学习中一个新兴且重要的方向，因为现实世界中的大多数业务数据都以表格形式存在，而非文本或图像。TabPFN-3.5 在文本丰富、高基数和高维等多种数据场景下都取得了显著的 Elo 提升，表明预训练表格模型正在快速缩小与传统梯度提升和 AutoML 管道的差距，并在某些场景下实现超越。 TabPFN-3.5-Thinking 在 BeyondArena 上比基础模型额外提升 +20 Elo，在 TabArena 上提升 +44 Elo，但仅通过 API 提供；Fast 变体推理速度提升 6 倍，但仍处于 alpha 阶段。该模型在 BeyondArena 的文本丰富、高基数和高维数据切片上均领先，表明其能够超越标准 IID 表格设置实现广泛泛化。

reddit · r/MachineLearning · /u/tuanacelik · 9月15日 16:18

**背景**: TabPFN（Tabular Prior-data Fitted Network，表格先验拟合网络）是一种基于 Transformer 的基础模型，于 2022 年提出，通过在数百万个由结构因果模型生成的合成表格数据集上进行离线预训练，在推理时通过上下文学习在单次前向传播中完成有监督学习（本质上是贝叶斯推断）。TabArena 是由 AutoGluon 团队维护的表格机器学习「活基准」，而 BeyondArena 是其更全面的后继版本，将评估范围从独立同分布（IID）数据扩展到涵盖时间序列和分组任务，并覆盖多种特征维度。Elo 评分系统由 Chatbot Arena 在大语言模型评测中推广，它将成对的基准对决转换为单一可比较的能力分数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/TabPFN">TabPFN - Wikipedia</a></li>
<li><a href="https://github.com/autogluon/tabarena">GitHub - autogluon/tabarena: A Living Benchmark for Machine ...</a></li>
<li><a href="https://www.lmsys.org/blog/2023-05-03-arena/">Chatbot Arena: Benchmarking LLMs in the Wild with Elo Ratings</a></li>

</ul>
</details>

**标签**: `#tabular-data`, `#foundation-models`, `#machine-learning`, `#TabPFN`, `#Prior-Labs`

---

<a id="item-8"></a>
## [Ollama v0.34.1 发布：/api/tags 提速约 10 倍，MLX 全面升级](https://github.com/ollama/ollama/releases/tag/v0.34.1) ⭐️ 6.0/10

Ollama v0.34.1 带来多项重要更新：/api/tags 接口冷启动速度从 3.1 秒提升至 294 毫秒；MLX safetensors 模型的 `ollama create` 命令从实验功能转为正式功能；优化了 Apple Silicon 上的 MLX 内存处理；将失控重复 token 检测阈值调整为 100 次重复；并废弃了新模型创建中的 `typical_p` 参数。 /api/tags 的速度提升显著改善了拥有大量本地模型的用户在列举模型时的响应体验；MLX 的成熟化则让 Apple Silicon 平台在本地运行大语言模型时获得更完善的一等公民支持。废弃 `typical_p` 标志着 Ollama 生态在逐步清理小众的采样参数，走向成熟。 GGUF 模型创建现在需要使用 llama.cpp 工具链来进行 safetensor 转换和量化，这意味着 MLX 与 GGUF 两条工作流被正式拆分。已存在的 GGUF 模型仍保留对 `typical_p` 的支持，但新建模型不再允许设置该参数；此外，重复 token 阈值调整为 100 次后，OCR 输出等场景下的误报明显减少。

github · github-actions[bot] · 9月14日 22:14

**背景**: Ollama 是一款广受欢迎的本地大语言模型运行工具，它将模型（通常采用 GGUF 格式）与基于 llama.cpp 的运行时以及简洁的 REST API 打包在一起，方便用户在本地部署和调用模型。MLX 是苹果开源的数组计算框架，专门针对 Apple Silicon 统一内存架构进行优化，可在 Mac 设备上高效完成大模型的推理与训练。`typical_p` 是一个相对小众的采样参数，它依据 token 的预期信息量来筛选候选 token，与更常见的 top-p（核采样）方法有所不同。GGUF（GPT-Generated Unified Format）是 llama.cpp 项目推出的单文件二进制格式，将量化后的模型权重、分词器数据和元数据集中存储，可在 CPU、Apple Silicon 或 GPU 上快速加载运行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple ... MLX Exploring LLMs with MLX and the Neural Accelerators in the M5 ... Get started with MLX for Apple silicon - WWDC25 - Videos ... GitHub - russellgeum/Apple-MLX: MLX: An array framework for ... What Is MLX? Apple Silicon ML & Inference Framework | AI/TLDR</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>
<li><a href="https://localaimaster.com/blog/llm-sampling-parameters-explained">LLM Sampling Parameters : Temperature, top- p , DRY, XTC (2026)</a></li>
<li><a href="https://www.datacamp.com/tutorial/gguf-format-a-complete-guide">GGUF Format: A Complete Guide to Local LLM Inference</a></li>

</ul>
</details>

**标签**: `#ollama`, `#llm`, `#release-notes`, `#mlx`, `#apple-silicon`

---

<a id="item-9"></a>
## [开源电子墨水相框：识别鸟鸣并显示复古插画](https://github.com/arnegiacomo/fugleramme) ⭐️ 6.0/10

开发者 Arne Munthe-Kaas 开源了名为 "fugleramme"（挪威语意为"鸟相框"）的项目：一款电子墨水相框，通过麦克风聆听周围鸟类，利用 BirdNET 音频分类器识别鸟种，并在由 ESP32 微控制器控制的电子墨水屏幕上以 19 世纪复古插画风格呈现该鸟类。 该项目是将成熟且易获取的技术——开源生物声学机器学习、低功耗电子墨水和廉价微控制器——融合成一种富有诗意而非纯粹工具化的家居产品。它展示了创客硬件与 AI 分类器如何被编织进注重美感与惊喜感的"氛围型"产品中，而非一味追求性能。 鸟类识别在 ESP32 上本地运行，使用的是 BirdNET（由康奈尔鸟类学实验室开发、可识别全球 6000 多种鸟类的深度神经网络），并非基于大语言模型。选用电子墨水屏正是因为其在刷新之间几乎不耗电，使得相框可凭借小型电池长时间运行——有评论指出，仅凭一块 2000mAh 的电池即可实现一年以上的续航。

hackernews · arnemunthekaas · 9月15日 12:31 · [社区讨论](https://news.ycombinator.com/item?id=49711544)

**背景**: BirdNET 是一款用于生物声学监测和公民科学鸟类识别的开源深度学习模型，能从短音频片段中识别数千种鸟类。电子墨水屏（电泳显示屏）仅在画面刷新时耗电，非常适合电子书阅读器和信息相框等需要电池供电、低频刷新的显示设备。ESP32 由乐鑫科技（Espressif Systems）生产，是一款流行的低成本 Wi-Fi/蓝牙微控制器，凭借其亲民价格和丰富的外设支持，被广泛应用于创客和物联网项目中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://birdnet.cornell.edu/">BirdNET – AI-Powered Sound ID</a></li>
<li><a href="https://en.wikipedia.org/wiki/ESP32">ESP32 - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: Hacker News 上的讨论几乎一边倒地热烈：评论者称这是近期见过的"最酷的东西"，并将其多种理念的融合形容为"神奇"。讨论中也出现了技术澄清——有用户指出 BirdNET 是传统神经网络而非大语言模型；其他人则强调了电子墨水配合 ESP32 的出色能效，并分享了自己的电子墨水作品。一位挪威同乡称该作品为"纯粹的艺术"，多位用户表示这激发了他们自己的创客灵感。

**标签**: `#hardware`, `#e-ink`, `#bird-classification`, `#creative-coding`, `#esp32`

---

<a id="item-10"></a>
## [疑似蓄意破坏导致荷兰铁路系统严重中断](https://www.bbc.com/news/articles/c8ly49w9g1edo) ⭐️ 6.0/10

疑似蓄意破坏事件导致荷兰铁路网络中断，HN 评论员对铁路系统漏洞进行了专业分析，并将此事件与更广泛的地缘政治紧张局势联系起来。

hackernews · choult · 9月15日 10:22 · [社区讨论](https://news.ycombinator.com/item?id=49710253)

**标签**: `#infrastructure-security`, `#sabotage`, `#critical-infrastructure`, `#geopolitics`, `#transportation`

---

<a id="item-11"></a>
## [DIY 赛博终端：将 20 美元 4G 热点改造成发短信设备](https://bkovac.github.io/modem-thing/) ⭐️ 6.0/10

一个 Show HN 项目展示了如何将一台 20 美元的 4G 无线热点与 Clicks 实体键盘和自定义软件结合，改造成一台独立的发短信设备。最终成果是一个由廉价消费级硬件搭建的、可随身携带的无需智能手机的通讯工具。 该项目凸显了创客们将廉价消费电子产品改造成极简计算设备的趋势，挑战了对智能手机的依赖。它体现了爱好者如何在极低预算下搭建实用的赛博终端，有望激发人们对开源替代方案替代主流移动计算的进一步探索。 该设备利用了 OpenStick 生态系统，该项目将基于 MSM8916 芯片的 4G LTE USB 调制解调器棒和热点改造为支持 Linux/OpenWrt 的迷你电脑，具备 WiFi、蜂窝网络和四核 CPU 功能。原本为智能手机保护壳配件设计的 Clicks 键盘，在这里被创造性地重新用作短信界面的主要输入方式。

hackernews · bobili1234 · 9月15日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49712102)

**背景**: 赛博终端（cyberdeck）是一种便携式、用途专一的计算设备，通常由非常规或改造部件组装而成，在 DIY 和黑客社区中很受欢迎。OpenStick 项目专门针对基于高通 MSM8916 芯片的廉价 4G USB 调制解调器棒和热点，通过刷入 OpenWrt 等开源固件来解锁其超出原始运营商锁定用途的功能。Clicks 键盘是一款为智能手机添加实体按键的商业配件，但在这个项目中它们脱离了原本的用途，作为独立的输入设备使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.clicks.tech/">Clicks Keyboard case: transform your phone with buttons</a></li>
<li><a href="https://cyberdeck.cafe/mix/what-is-a-cyberdeck">What is a Cyberdeck?</a></li>

</ul>
</details>

**社区讨论**: 评论者们积极参与讨论，提出了实用的改进建议，例如增加并联的 18650 电池可将续航延长至数周。几位用户分享了相关的 OpenStick 调制解调器棒项目，并指出某些基于 MSM8916 的设备甚至可以运行 Android 系统。一位用户表达了对项目的现实需求——他们已经放弃了智能手机，只携带热点设备上网。前瞻性的建议包括：如果 RAM 和存储允许，可以在设备上运行类似 Hermes Agent 的 AI 智能体系统。

**标签**: `#hardware-hacking`, `#diy`, `#4g-modem`, `#cyberdeck`, `#openstick`

---

<a id="item-12"></a>
## [美国首次确认已部署太空武器](https://www.bbc.com/news/articles/ck790xg41ygro) ⭐️ 6.0/10

美国首次公开确认已部署太空武器，此举引发地缘政治反应及社会各界关于太空军事化及其后果的讨论。

hackernews · harporoeder · 9月15日 03:47 · [社区讨论](https://news.ycombinator.com/item?id=49707473)

**标签**: `#geopolitics`, `#space`, `#military`, `#defense`, `#policy`

---

<a id="item-13"></a>
## [我从零训练了一个 4400 万参数的量化大语言模型，使用了 450 亿 token。模型体积仅 19.8 MB，在 CPU 上推理速度可达约 1,900 tok/s。(P)](https://www.reddit.com/r/MachineLearning/comments/1wgzpli/i_trained_a_44m_parameter_quantized_llm_from/) ⭐️ 6.0/10

一位研究人员采用三值权重和固定词汇指纹技术，从零训练了一个 4400 万参数的大语言模型，并引入了一种新颖的"计算器电路"机制来处理算术运算，最终将模型大小压缩至 19.8 MB，在 CPU 上实现约 1,900 tok/s 的推理速度。

reddit · r/MachineLearning · /u/Final-Data-1410 · 9月15日 12:59

**标签**: `#quantization`, `#edge-ml`, `#ternary-weights`, `#small-language-models`, `#efficient-inference`

---

<a id="item-14"></a>
## [MS MARCO click-translation expansion tables ("poor man's" DSSM) (P)](https://www.reddit.com/r/MachineLearning/comments/1wg3g03/ms_marco_clicktranslation_expansion_tables_poor/) ⭐️ 6.0/10

A practical count-based approach using MS MARCO click data to create translation tables that expand inverted indexes, improving baseline BM25 without requiring complex neural models.

reddit · r/MachineLearning · /u/SpiritedTrip · 9月14日 13:28

**标签**: `#Information Retrieval`, `#BM25`, `#Query Expansion`, `#MS MARCO`, `#Search Engines`

---