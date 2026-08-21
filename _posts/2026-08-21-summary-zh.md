---
layout: default
title: "Horizon Summary: 2026-08-21 (ZH)"
date: 2026-08-21
lang: zh
---

> 从 41 条内容中筛选出 13 条重要资讯。

---

1. [美国边境删除手机数据美国公民面临重罪指控](#item-1) ⭐️ 7.0/10
2. [研究人员意外通过遗留 ENUM DNS 记录军方电话](#item-2) ⭐️ 7.0/10
3. [DeepSeek 发布 V4 Flash 模型的实验性视觉能力](#item-3) ⭐️ 7.0/10
4. [AI 公司销毁实体书——趁还来得及，让我们扫描珍本](#item-4) ⭐️ 7.0/10
5. [衡量 ASR 模型中的基准测试过度优化问题](#item-5) ⭐️ 7.0/10
6. [Liquid AI 发布 LFM2.5-DSpark：推理速度最高提升 3.2 倍](#item-6) ⭐️ 7.0/10
7. [Ox Alpha 据称在 SWE-bench Verified Mini 上取得 96%，但作者呼吁保持怀疑](#item-7) ⭐️ 7.0/10
8. [AI 盲现象的兴起：为何读者本能地忽略 AI 生成文本](#item-8) ⭐️ 6.0/10
9. [DeepMind 与游戏工作室合作，十五年游戏 AI 研究再出发](#item-9) ⭐️ 6.0/10
10. [NVIDIA AVO 在 ARC-AGI-3 基准测试中取得满分](#item-10) ⭐️ 6.0/10
11. [FireRedTeam 开源 FireRedAudio 与 FireRedTTS3 音频模型](#item-11) ⭐️ 6.0/10
12. [目前最快的 Qwen3.8 27B NVFP4 量化版本](#item-12) ⭐️ 6.0/10
13. [模型：添加 dots3-note，提交者为 ngxson](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [美国边境删除手机数据美国公民面临重罪指控](https://www.nytimes.com/2026/08/21/us/politics/samuel-tunick-deleted-phone-felony.html) ⭐️ 7.0/10

一名美国公民因在美国边境删除手机数据而面临重罪指控，此案引发了对数字隐私权和边境搜查权限的严重担忧。

hackernews · floathub · 8月21日 12:10 · [社区讨论](https://news.ycombinator.com/item?id=49386895)

**标签**: `#digital-privacy`, `#civil-liberties`, `#border-security`, `#smartphone-security`, `#legal-policy`

---

<a id="item-2"></a>
## [研究人员意外通过遗留 ENUM DNS 记录军方电话](https://lina.sh/blog/hijacking-e164-arpa) ⭐️ 7.0/10

一名安全研究人员发现，自己在运行针对遗留 e164.arpa ENUM DNS 系统的个人实验时，无意中记录了数十万通电话——其中包括通往军事基地的通话——而该系统尽管被视为过时，却仍在处理真实的电话路由查询。 这一事件凸显出，那些被认为已经"消亡"的电信基础设施仍在传输真实的敏感流量——包括政府和军方通信——却无人主动管理。这引发了一个紧迫的问题：谁应该负责维护像公共 ENUM 这样的遗留系统？还有哪些被忽视的基础设施可能正在悄无声息地路由机密或私人数据？ RIPE Labs 在 2026 年的一项运营审查发现，e164.arpa 下当前所有公共 ENUM 委派中有一半存在某种 DNS 问题，这凸显了该基础设施被系统性忽视的事实。ENUM 最初由 IETF 设计，用于通过 DNS 将 E.164 电话号码映射到 SIP URI，从而实现传统电话网与 VoIP 的融合，但公共层基本已经崩溃，而私有/基础设施 ENUM 仍然通过 VPN 用于号码携带查询。

hackernews · gavide · 8月21日 13:11 · [社区讨论](https://news.ycombinator.com/item?id=49387570)

**背景**: ENUM（电话号码映射）是一套协议套件，通过 DNS 系统将国际 E.164 电话号码映射到互联网资源（如 SIP URI），其中 e164.arpa 这一特殊域名专为此用途而保留。该概念在 1990 年代末被提出，旨在将全球电话编号系统与互联网寻址统一起来，但公共 ENUM 部署从未获得广泛采用。与此同时，并行存在的"基础设施 ENUM"用例——即运营商通过专用网络使用 ENUM 风格的 DNS 查询进行号码携带查询——一直安静地运行着，这意味着真实的通话信令流量一直在通过原本为完全不同的目的而设计的基础设施传输。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ripe.net/manage-ips-and-asns/dns/enum/">ENUM — RIPE Network Coordination Centre</a></li>
<li><a href="https://en.wikipedia.org/wiki/Telephone_number_mapping">Telephone number mapping - Wikipedia</a></li>
<li><a href="https://labs.ripe.net/author/hisham_ibrahim/operational-review-of-public-enum-under-e164arpa/">Operational Review of Public ENUM Under e164.arpa | RIPE Labs</a></li>

</ul>
</details>

**社区讨论**: 社区评论者提供了丰富的内幕信息：toast0 澄清说 e164.arpa/ENUM 并非真正消亡，而是仍通过 VPN 以私有方式用于号码携带服务；chaz6 遗憾作者没有搭建 SIP 服务器来查看是否有通话实际接通，并指出了相关的 TRIP 协议；dmd 对作者因持有军方通话记录而未被捕表示惊讶；cryptolobster 指出直到军方介入才有人去处理这一长期存在的问题，而 dkga 则称赞这篇文章是展示事物如何被遗漏的绝佳案例。

**标签**: `#security`, `#telecom-infrastructure`, `#DNS`, `#vulnerability-disclosure`, `#ENUM`

---

<a id="item-3"></a>
## [DeepSeek 发布 V4 Flash 模型的实验性视觉能力](https://api-docs.deepseek.com/guides/vision/) ⭐️ 7.0/10

DeepSeek 为其 DeepSeek-V4-Flash 模型推出了实验性视觉能力，允许通过 API 将图像进行 token 化并与文本 token 合并计费。小于约 384×384 像素的图像会被放大，而较大的图像会被缩放至约 800×800 总像素，同时保持原始宽高比。 此次更新为最具竞争力的开源权重模型之一带来了多模态能力，且定价极低（每百万 token 输入 $0.14、输出 $0.28），有望降低开发者构建视觉应用工作流的门槛。它直接解决了 DeepSeek 模型长期存在的问题——模型会幻觉自己拥有视觉能力而实际并不具备，导致智能体会话中断。 据社区测试者反馈，800×800 的缩放上限对于包含完整 A4/Letter 尺寸文档的 OCR 任务来说可能不够用。初步评估显示，模型在简单的视觉推理任务（如读取模拟时钟时间）上表现欠佳，而较小的开源模型如 Qwen 8B-27B 在这些任务上反而表现更好。

hackernews · dares2573 · 8月21日 10:33 · [社区讨论](https://news.ycombinator.com/item?id=49386163)

**背景**: DeepSeek-V4-Flash 是一个拥有 304B 参数的稀疏混合专家（MoE）语言模型，专为文本生成、编程、推理和智能体工作流设计，上下文窗口可达 100 万 token。视觉语言模型（VLM）在标准大语言模型的基础上增加了同时处理图像和文本的能力：图像通常被分割为小块，转换为嵌入向量，再进行 token 化，使模型能够像处理文字一样对视觉内容进行推理。此前 DeepSeek 模型缺乏原生视觉支持，开发者需要使用单独的模型来处理图像理解，这给需要解读截图或 UI 元素的智能体工作流带来了复杂性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepseek-v4.io/architecture">DeepSeek V4 Architecture: MoE, Parameters & 1M Context</a></li>
<li><a href="https://build.nvidia.com/deepseek-ai/deepseek-v4-flash-0731/modelcard">deepseek-v4-flash-0731 Model by Deepseek-ai | NVIDIA NIM</a></li>

</ul>
</details>

**社区讨论**: 社区情绪持谨慎乐观态度。开发者们对这一新增功能表示欢迎，因为它填补了 Playwright 截图编码工作流中相较于 Claude Sonnet 等模型的明显缺口。然而，测试者报告了模型在读取模拟时钟等简单任务上的具体失败案例，并指出 800×800 的缩放分辨率对于 OCR 和文档扫描应用来说可能过于有限。多位用户还提到，此前版本的 DeepSeek 模型会幻觉自己拥有视觉能力，在智能体工作流中导致会话中断——而此次更新正是直接针对这一问题。

**标签**: `#DeepSeek`, `#vision-models`, `#multimodal-AI`, `#LLM`, `#open-source-models`

---

<a id="item-4"></a>
## [AI 公司销毁实体书——趁还来得及，让我们扫描珍本](https://annas-archive.gl/blog/physical-destruction.html) ⭐️ 7.0/10

Anna's Archive 呼吁在 AI 公司购买并物理销毁珍本以获取训练数据之前，对其进行众包数字化，此举引发了关于版权、保护和 AI 伦理的讨论。

hackernews · Cider9986 · 8月21日 02:37 · [社区讨论](https://news.ycombinator.com/item?id=49383026)

**标签**: `#AI`, `#copyright`, `#knowledge-preservation`, `#training-data`, `#ethics`

---

<a id="item-5"></a>
## [衡量 ASR 模型中的基准测试过度优化问题](https://huggingface.co/blog/asr-benchmark-optimization) ⭐️ 7.0/10

HuggingFace 发布了一篇博客文章，分析了自动语音识别（ASR）模型如何针对 LibriSpeech 等特定基准测试产生过度优化，并提出了衡量和解决基准测试性能与真实部署之间泛化差距的方法。 ASR 中的基准测试过拟合是一个重要的可复现性和部署问题：在 LibriSpeech 上报告最先进数字的模型，在多样化的真实音频上可能表现不佳，从而误导从业者对模型实际能力的判断，并阻碍鲁棒语音交互界面的发展。 该分析聚焦于 LibriSpeech——一个来自 LibriVox 有声书的约 1,000 小时英语朗读语料库，它已成为事实上的 ASR 标准基准，并指出模型如何被调优以利用其特定的声学和语言特征，而非学习可泛化的识别能力。

rss · HuggingFace Blog · 8月21日 00:00

**背景**: 自动语音识别（ASR）将口语转换为文本，是语音助手、实时字幕和会议转录等应用的基础。LibriSpeech 源自公共领域的 LibriVox 有声书录音，由于其标准化的训练/测试划分和干净的录音棚音质，长期以来一直是英语 ASR 的主要基准。然而，由于该领域已统一使用 LibriSpeech 进行评估，存在一个广为人知的风险——类似于其他机器学习领域中的过拟合——即模型越来越针对其特有的特征进行定制，而非泛化到生产环境中遇到的嘈杂、带口音和领域多样的语音。多语种 LibriSpeech（MLS）将该方法部分扩展到了八种语言，但对基准的依赖性仍然是一个核心的方法论挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/librispeech">LibriSpeech | AI Wiki</a></li>
<li><a href="https://www.ibm.com/think/topics/overfitting">What is Overfitting? | IBM</a></li>
<li><a href="https://huggingface.co/docs/transformers/tasks/asr">Automatic speech recognition · Hugging Face</a></li>

</ul>
</details>

**标签**: `#speech-recognition`, `#benchmarking`, `#ASR`, `#model-evaluation`, `#HuggingFace`

---

<a id="item-6"></a>
## [Liquid AI 发布 LFM2.5-DSpark：推理速度最高提升 3.2 倍](https://huggingface.co/blog/LiquidAI/lfm25-dspark) ⭐️ 7.0/10

Liquid AI 发布了 LFM2.5-DSpark，这是一种推测解码（speculative decoding）优化方案，可为其 LFM2.5 模型系列带来最高 3.2 倍的推理加速。针对 LFM2.5-1.2B-Instruct、LFM2.5-2.6B 和 LFM2.5-8B-A1B 的草稿模型已在 Hugging Face 上开放下载，相关集成已开源到 llama.cpp 和 SGLang 中。 在不损失输出质量的前提下实现 3.2 倍推理加速，能够直接降低 LLM 生产部署的延迟和计算成本，对大规模部署 Liquid 模型的场景影响显著。同时将集成开源到 llama.cpp 和 SGLang 这两个最广泛使用的开源推理框架，使得该优化方案易于在生态中推广使用。 DSpark 草稿模型采用简化的纯注意力（attention-only）架构，仅含 5 层，每步推测 9 个候选 token，并以一个基于 128,000 词表的 Markov 头进行预测。例如，LFM2.5-2.6B-DSpark 的草稿模型仅有 3.277 亿（327.7M）BF16 精度参数，hidden_size=2048，intermediate_size=6144，远小于目标模型。

rss · HuggingFace Blog · 8月20日 16:52

**背景**: 推测解码（speculative decoding）是一种针对自回归大语言模型的推理时优化技术：由一个较小的草稿模型提前生成若干候选 token，再由目标大模型通过改进的拒绝采样方案在单次前向传播中统一验证这些候选。由于验证过程保留了目标模型原有的输出分布，因此加速不会牺牲生成质量。DSpark 是 Liquid AI 针对自家 LFM2.5 系列对该技术的具体实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding - Wikipedia</a></li>
<li><a href="https://www.liquid.ai/blog/lfm2.5-dspark">LFM 2 . 5 - DSpark : Up to 3.2x Faster Inference from H100... — Liquid AI</a></li>
<li><a href="https://huggingface.co/LiquidAI/LFM2.5-2.6B-DSpark">LiquidAI/ LFM 2 . 5 -2.6B- DSpark · Hugging Face</a></li>

</ul>
</details>

**标签**: `#inference-optimization`, `#liquid-ai`, `#model-performance`, `#huggingface`, `#speculative-decoding`

---

<a id="item-7"></a>
## [Ox Alpha 据称在 SWE-bench Verified Mini 上取得 96%，但作者呼吁保持怀疑](https://www.reddit.com/r/LocalLLaMA/comments/1vuke8o/i_benchmarked_ox_alpha_on_swebench_verified_mini/) ⭐️ 7.0/10

一位 Reddit 用户在 50 题的 SWE-bench Verified Mini 子集上对免费版"Ox Alpha"模型进行了基准测试，报告 48/50（96%）解析率，使用官方的 mini-swe-agent Bash-Only 脚手架和官方 SWE-bench Docker 评测工具，在一台 Windows 11 机器上以 4 个并行 worker 完成，总耗时约 2 小时 4 分钟。 如果经独立验证，免费/开源模型超越 Claude Opus 5（97%）、Claude Fable 5（95%）和 Claude Opus 4.8（88.6%）将成为开源编程 Agent 的分水岭时刻，彻底改变人们对专有模型与免费模型在智能体软件工程任务上差距的预期。 本次运行 django 得 23/25（失败 django__django-11790 和 django__django-11815），sphinx-doc 得 25/25，平均每题 40 步、最多 116 步；作者的免责声明强调：mini-50 子集仅包含 django 和 sphinx（两个在训练数据中高度曝光的代码库），n=50 意味着约 ±3 个百分点的采样噪声，且免费接口无法审计是否存在缓存或限速问题。

reddit · r/LocalLLaMA · /u/No_Tip9917 · 8月21日 16:00

**背景**: SWE-bench Verified 是原始 SWE-bench 数据集中经人工核验的 500 题子集，被业界广泛用于评估 AI 系统通过生成补丁以通过隐藏测试来解决真实 GitHub issue 的能力。"Verified-Mini"是其广为人知的 50 题精简版，经策展以匹配完整集的难度分布。mini-swe-agent 是 SWE-agent 团队维护的极简（约 100 行）Bash-Only Agent 脚手架；它刻意剥离工具调用层，使语言模型自身的能力——而非 Agent 工程——决定得分，因而成为 swebench.com Bash-Only 排行榜的事实基准。Ox Alpha 是一个近期浮出水面的"stealth"推理模型，宣传为面向编程的模型，上下文窗口 1M token，通过第三方网关提供免费档访问。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/datasets/SWE-bench/SWE-bench_Verified">SWE-bench/SWE-bench_Verified · Datasets at Hugging Face</a></li>
<li><a href="https://github.com/SWE-agent/mini-swe-agent">GitHub - SWE-agent/mini-swe-agent: The 100 line AI agent that ...</a></li>
<li><a href="https://benchable.ai/models/stealth/ox-alpha">Ox Alpha - AI Model Details & Benchmarks</a></li>

</ul>
</details>

**标签**: `#SWE-bench`, `#benchmarking`, `#open-source-LLMs`, `#code-agents`, `#Ox-Alpha`

---

<a id="item-8"></a>
## [AI 盲现象的兴起：为何读者本能地忽略 AI 生成文本](https://cymerys.com/w/im-becoming-ai-blind) ⭐️ 6.0/10

一篇个人随笔描述了一种日益普遍的心理现象：读者会自动识别并忽略 AI 生成的文本，认为其缺乏价值，并迫使大脑进行费力的解读工作。Hacker News 上的讨论（191 个赞，193 条评论）深入探讨了其根本原因，指出 AI 在结构化思维和自上而下的综合能力上的薄弱是文本显得空洞的症结所在。 读者认知的这种转变对数十亿篇正在发布的 AI 生成内容以及部署大语言模型进行沟通任务的企业构成了战略性挑战。随着受众对 AI 写作形成无意识的过滤机制，原始大语言模型输出的边际价值急剧下降，可能削弱人们对 AI 辅助工具的信任，并推动创作者转向更精细的人性化工作流程。 社区评论者指出了大语言模型的一种具体失败模式：像 Claude 这样的模型倾向于产生"扁平化的意大利面式"代码，将细节罗列在一起而无法归纳或综合出统一概念，导致写作缺乏自上而下的解释结构。一位开发者报告说，AI 生成的拉取请求评论在结构上过于冗长复杂，以至于需要用人工编写的单行注释来替换。

hackernews · rcymerys · 8月21日 11:48 · [社区讨论](https://news.ycombinator.com/item?id=49386699)

**背景**: 随笔中描述的现象与一个被充分记录的行为偏差相关——即"算法厌恶"（algorithm aversion），该概念由 Berkeley Dietvorst 等人于 2015 年提出，描述了人们倾向于不信任算法输出，即使其表现与人类相当甚至更优。"AI 盲"这一概念特别将这一现象扩展到文本生成领域，其问题不在于统计准确性，而在于人们所感知到的思维深度不足。关于大语言模型失败模式的相关研究（例如 2025 年 arXiv 上提出的十五种隐藏的系统级失败分类法）有助于解释为什么 AI 文本常常在结构上显得有缺陷，而不仅仅是事实错误。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Algorithm_aversion">Algorithm aversion - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2511.19933">[2511.19933] Failure Modes in LLM Systems: A System-Level Taxonomy for ...</a></li>
<li><a href="https://www.chicagobooth.edu/review/even-when-algorithms-outperform-humans-people-often-reject-them">Even When Algorithms Outperform Humans, People Often Reject Them | Chicago Booth Review</a></li>

</ul>
</details>

**社区讨论**: HN 讨论帖的评论质量异常深入，评论者趋于一致地认为，AI 写作会触发一种心理短路反应，因为读者必须通过创造性解读来填补缺失的意义。一个反复出现的技术批评是，像 Claude 这样的大语言模型无法感知"全局图景"，产生扁平化或过度细节化的输出，缺少人类专家会提供的自上而下的综合能力。多位开发者分享了具体的痛点，特别是 AI 生成的代码注释在结构上晦涩难懂，必须用人工编写的注释来替换。

**标签**: `#ai-generated-content`, `#human-ai-interaction`, `#perception`, `#llm-limitations`, `#content-quality`

---

<a id="item-9"></a>
## [DeepMind 与游戏工作室合作，十五年游戏 AI 研究再出发](https://deepmind.google/blog/from-atari-to-eve-online-building-on-15-years-of-ai-research-in-games/) ⭐️ 6.0/10

Google DeepMind 宣布与游戏工作室建立新合作，共同原型化突破性的 AI 游戏玩法，标志着其游戏 AI 研究走过 15 周年——从最初的 Atari DQN 突破，到如今 EVE Online 等复杂现代游戏。 这标志着 DeepMind 从 Atari 和 StarCraft 等纯学术基准测试，转向真实的商业游戏环境，可能加速强化学习在生产级游戏系统中的部署，并影响未来游戏的设计与测试方式。 这一历程横跨从 DQN（深度 Q 网络）到 Agent57 的演进：DQN 使用同一套未经修改的算法，仅凭原始像素和分数就能玩 49 款 Atari 游戏；Agent57 是首个在全部 57 款 Atari 2600 游戏上都超越人类基准的深度强化学习智能体；如今更进一步延伸到 EVE Online 这类大型多人在线游戏环境。

rss · Google DeepMind Blog · 8月21日 11:59

**背景**: 深度强化学习将深度神经网络与强化学习相结合，使 AI 智能体能够通过与环境反复试错的交互来学习最优行为策略。DeepMind 在 2013 年发表的 DQN 论文证明，单一算法仅凭屏幕像素和分数信号就能掌握数十款 Atari 游戏，无需针对特定游戏进行工程化改造——这是现代深度强化学习研究兴起的分水岭。随后的里程碑包括 AlphaGo、AlphaStar（《星际争霸 II》）和 Agent57，每一项突破所面对的状态空间、时间跨度和多智能体动态都更加复杂。EVE Online 因其大型多人在线特性、持久存在的经济体系以及复杂的社会交互，成为一个尤其具有挑战性的前沿领域。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/blog/agent57-outperforming-the-human-atari-benchmark/">Agent57: Outperforming the human Atari ... — Google DeepMind</a></li>
<li><a href="https://medium.com/@sakethyalamanchili/deepminds-dqn-when-deep-learning-finally-learned-to-play-and-changed-everything-58b0e9db0b90">DeepMind ’s DQN : When Deep Learning Finally Learned to... | Medium</a></li>
<li><a href="https://vertexdigest.com/blogs/reinforcement-learning-games-deepmind">From Atari to StarCraft: How Reinforcement Learning Mastered...</a></li>

</ul>
</details>

**标签**: `#AI`, `#Reinforcement Learning`, `#Game AI`, `#DeepMind`, `#Research`

---

<a id="item-10"></a>
## [NVIDIA AVO 在 ARC-AGI-3 基准测试中取得满分](https://www.reddit.com/r/LocalLLaMA/comments/1vuh7to/nvidia_avo_got_100_on_arcagi3_it_completed_all/) ⭐️ 6.0/10

NVIDIA 的通用编码智能体系统 AVO 在 ARC-AGI-3 公开基准测试中取得 100% 满分，在没有任何指令、明确规则或既定目标的前提下，完成了全部 25 个交互式环境中的 183 个关卡。 ARC-AGI-3 专门设计用于抵抗记忆化并检验真正的泛化能力，因此如果该满分成绩得到验证，将标志着智能体 AI 能力的一个重大里程碑。这也表明编码智能体架构可以被重新用作通用推理系统，自主探索陌生的交互式环境。 AVO 的工作方式类似现代编码智能体——检查和编辑代码、运行命令、查阅文档并通过执行来验证工作——而非专门设计的解题程序。该结果仅适用于公开测试集，其底层方法、模型架构和计算资源需求尚未公开详细披露。

reddit · r/LocalLLaMA · /u/theologi · 8月21日 14:01

**背景**: ARC（抽象与推理语料库）是由 AI 研究员 François Chollet 于 2019 年创建的基准测试系列，用于衡量流体推理和样本高效推理能力——即在极少先验接触的情况下解决新颖问题的能力。ARC-AGI-1 和 ARC-AGI-2 使用的是静态网格谜题，而 ARC-AGI-3 则转向交互式智能体环境，要求 AI 系统在没有明确指令的情况下进行探索、实验和适应。该基准明确设计用于抵抗记忆化，并奖励真正的泛化能力，是衡量通往通用人工智能进展的重要测试之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/nvidia-avo-reaches-100-on-arc-agi-3-demonstrating-a-frontier-level-general-purpose-architecture-for-long-horizon-autonomous-agents/">NVIDIA AVO Reaches 100% on ARC-AGI-3, Demonstrating...</a></li>
<li><a href="https://runtimewire.com/article/nvidia-avo-arc-agi-3-perfect-public-score">NVIDIA 's AVO scores 100% on ARC-AGI-3's public set</a></li>
<li><a href="https://www.emergentmind.com/topics/arc-agi-3">ARC - AGI - 3 : Interactive AGI Benchmark</a></li>

</ul>
</details>

**标签**: `#ARC-AGI`, `#NVIDIA`, `#AGI-benchmark`, `#reasoning`, `#general-intelligence`

---

<a id="item-11"></a>
## [FireRedTeam 开源 FireRedAudio 与 FireRedTTS3 音频模型](https://www.reddit.com/r/LocalLLaMA/comments/1vukj3m/fireredaudio_fireredtts3_by_fireredteam/) ⭐️ 6.0/10

FireRedTeam 开源了 FireRedAudio，这是一款 90 亿参数的统一音频语言模型，采用解耦的连续表示分别处理理解与生成任务，支持 ASR、零样本 TTS、指令式 TTS、语音编辑以及对长达一小时的录音进行时间定位。同时发布的还有 FireRedTTS3 语音生成与编辑系统，支持 24 种语言和 21 种中国方言的零样本声音克隆。 此次发布将完整的音频能力栈（理解、生成、编辑、时间定位）整合为开源模型，并在多个基准上取得有竞争力的结果，可能降低语音助手、多语言应用及音频分析工具的开发门槛。解耦表示共享单一骨干网络的架构设计，也可能影响未来多模态音频模型的研发思路。 FireRedAudio 使用共享的 90 亿参数 LLM 骨干网络，配合两条解耦的通路：用于理解的 Audio Encoder 和用于生成的 RedAE-Patch 通路，据称是首个公开披露的此类统一音频语言模型设计。FireRedTTS3-Base 在 MiniMax-MLS-Test 上取得最佳平均 WER/CER（3.754%），在 Seed-TTS-eval 上的克隆 WER/CER 为 3.04%；Instruct 版本进一步支持基于自然语言的音色设计以及语义级（增删改）和声学级（语速、音量、音调）的编辑。

reddit · r/LocalLLaMA · /u/pmttyji · 8月21日 16:05

**背景**: 音频语言模型旨在将基于文本的大语言模型扩展到语音和音频的输入与输出处理。传统流水线通常依赖独立模型分别处理 ASR（自动语音识别）和 TTS（语音合成）等任务，而近年来的研究开始转向共享单一骨干网络的多任务统一架构。在连续潜在空间（而非离散 token）中进行运算，有助于保留细粒度的声学信息以实现高保真合成。时间定位是一项新兴能力，它将长音频中的事件与具体时间戳关联起来，通过精确的时间-内容对齐扩展了通用音频理解能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2509.06926">[2509.06926] Continuous Audio Language Models - arXiv.org Bridging semantics across modalities: Decoupled ... Continuous Audio Language Models GitHub - HarunoriKawano/HEAR: Official implementation of "A ... (PDF) Continuous Audio Language Models - ResearchGate Continuous Audio Language Models - OpenReview</a></li>
<li><a href="https://arxiv.org/html/2602.10230v1">Frame-Level Internal Tool Use for Temporal Grounding in Audio LMs</a></li>
<li><a href="https://arxiv.org/html/2511.11039v1">TimeAudio: Bridging Temporal Gaps in Large Audio-Language Models</a></li>

</ul>
</details>

**标签**: `#audio-language-model`, `#text-to-speech`, `#multimodal-AI`, `#open-source`, `#speech-recognition`

---

<a id="item-12"></a>
## [目前最快的 Qwen3.8 27B NVFP4 量化版本](https://www.reddit.com/r/LocalLLaMA/comments/1vub9od/fastest_nvfp4_quant_of_qwen38_27b_out_there/) ⭐️ 6.0/10

基于 Blackwell 原生 NVFP4 量化的 Qwen 27B 新模型号称目前最快，在 RTX 5090 上运行速度比 Q4 快 50%，比其它 NVFP4 量化版本快 4-7%，还附带 MTP 预测头优化。

reddit · r/LocalLLaMA · /u/ionsago · 8月21日 09:19

**标签**: `#quantization`, `#NVFP4`, `#Blackwell`, `#RTX-5090`, `#local-llama`, `#speculative-decoding`

---

<a id="item-13"></a>
## [模型：添加 dots3-note，提交者为 ngxson](https://www.reddit.com/r/LocalLLaMA/comments/1vunrrp/model_add_dots3note_by_ngxson_pull_request_27060/) ⭐️ 6.0/10

llama.cpp 此次 PR 新增对 dots3-note 模型的支持。这是一款开源权重的多模态 MoE 模型，总参数量 280B，激活参数 16B，上下文长度达 512K。

reddit · r/LocalLLaMA · /u/jacek2023 · 8月21日 18:03

**标签**: `#llama.cpp`, `#open-source-models`, `#mixture-of-experts`, `#multimodal`, `#dots3-note`

---