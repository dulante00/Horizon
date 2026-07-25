---
layout: default
title: "Horizon Summary: 2026-07-25 (ZH)"
date: 2026-07-25
lang: zh
---

> 从 46 条内容中筛选出 9 条重要资讯。

---

1. [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](#item-1) ⭐️ 7.0/10
2. [Langfuse v4.0.0-rc.2 候选版引入重大架构变更](#item-2) ⭐️ 7.0/10
3. [Android 或将限制设备端 ADB 访问](#item-3) ⭐️ 7.0/10
4. [开放权重 AI 正迎来它的 Kubernetes 时刻](#item-4) ⭐️ 7.0/10
5. [Tile 缺乏端到端加密，使追踪器沦为 stalker 工具](#item-5) ⭐️ 7.0/10
6. [英伟达、Meta、微软、Palantir 和 Hugging Face 等 20 多家公司签署公开信，敦促政策制定者避免对开放权重模型过早施加限制](#item-6) ⭐️ 7.0/10
7. [数学的至暗时刻：LLM 自动化定理证明，数学家面临存在危机](#item-7) ⭐️ 6.0/10
8. [Fedora 45 发布流程端到端详解文章发布](#item-8) ⭐️ 6.0/10
9. [Inflect v2 发布：两个参数低于 1000 万的完整 TTS 模型](#item-9) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 7.0/10

vLLM v0.26.0 正式发布，包含 212 位贡献者的 411 次提交，新增对 Thinking Machines Lab 新推出的 Inkling 多模态模型家族的完整支持，以及跨 CUDA、ROCm 和 XPU 平台的 DeepSeek-V4 重大性能优化（内核加速 1.5–2 倍，端到端 TPOT 提升 2.94%），同时引入 fp32 lm_head 以提升生成精度，并支持按 KV-cache 组灵活选择注意力后端。 Inkling 集成包括分段式 CUDA 图、Hopper FA4 相对注意力、MTP=1 投机解码、LoRA 支持以及 ModelOpt NVFP4 量化；DeepSeek-V4 则获得了专用路由内核、fused_topk_bias、冗余 repeat/copy 消除以及在 AMD 和 XPU 上的 DSpark 投机解码。KV 卸载现在支持带工作负载身份的对象存储二级层级以及 DP 副本感知的分层机制，Rust 前端新增了多模态视频和音频处理以及原生 vllm-bench 移植版本。

github · khluu · 7月25日 10:38

**背景**: vLLM 是由加州大学伯克利分校最初开发、目前由广泛社区维护的一款广泛使用的开源大语言模型高吞吐量推理与服务引擎。Inkling 是 Thinking Machines Lab 于 2026 年 7 月发布的 1T 参数多模态模型，原生支持文本、图像和音频输入，上下文长度可达 100 万，引入了相对注意力、短卷积和共享专家池等新颖架构组件。DSpark 是一种基于置信度调度的投机解码框架，据报道通过结合并行草稿生成与自适应验证，可使 DeepSeek V4 提速高达 85%。NVFP4 是 NVIDIA 随 Blackwell GPU 推出的 4 位浮点格式，采用共享指数保留浮点语义，以实现精确的低精度推理。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vllm.ai/blog/2026-07-15-inkling">TML Inkling on vLLM: Day-0 Support with Optimized Performance</a></li>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our Open-Weights Model - Thinking Machines Lab</a></li>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://arxiv.org/abs/2607.05147">DSpark: Confidence-Scheduled Speculative Decoding with Semi ...</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#deepseek`, `#cuda`, `#release-notes`

---

<a id="item-2"></a>
## [Langfuse v4.0.0-rc.2 候选版引入重大架构变更](https://github.com/langfuse/langfuse/releases/tag/v4.0.0-rc.2) ⭐️ 7.0/10

Langfuse 发布了 v4.0.0-rc.2，这是 v4.0.0 主版本的第二个候选版本。此次更新带来重大架构变更，包括删除已废弃的 Postgres 与 ClickHouse 表、用于高性能查看大型负载的异步虚拟化 JSON 渲染器、智能体的后台执行支持，以及针对会话和追踪页面的移动端 UI 全面重构。 作为广泛使用的开源 LLM 可观测性平台，Langfuse 的 v4 版本意味着现有用户在规划升级时将面临重大变更，尤其是涉及 Postgres（OLTP）与 ClickHouse（分析查询）双数据库架构的调整。异步 JSON 渲染器和后台执行功能的引入表明 Langfuse 正在扩展以承载更大规模的企业级工作负载。 此版本还包括 Salesforce 同步机制的重写，支持按组织粒度的回填单元和 CSV 控制，以及若干安全相关修复（不再记录公共 API 请求负载、修改 base URL 时要求提供新密钥）。删除数据表相关的 PR 上的重大变更标记意味着 v4 需要预先规划 schema 迁移方案，而 RC.2 标识也表明这并非最终的稳定发布版本。

github · Steffen911 · 7月24日 12:34

**背景**: Langfuse 是一个开源的 AI 工程平台，为基于大语言模型的应用提供可观测性、评估和提示词管理功能，可捕获追踪、延迟与成本等指标，并与 OpenAI、LangChain、LlamaIndex 等框架集成。它采用双数据库架构：PostgreSQL 负责事务型数据（OLTP），而 ClickHouse 作为列式数据库，专门承担对追踪数据的高性能分析查询。由于只读取查询所需的列，ClickHouse 的列式存储在分析聚合场景下比 PostgreSQL 快 100 到 1000 倍。候选发布版（RC）是正式稳定版本发布之前供测试的预发布版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://langfuse.com/docs/observability/overview">LLM Observability & Application Tracing (Open Source) - Langfuse</a></li>
<li><a href="https://langfuse.com/docs">Overview - Langfuse</a></li>
<li><a href="https://oneuptime.com/blog/post/2026-03-31-clickhouse-vs-postgresql-analytics/view">How to Compare ClickHouse vs PostgreSQL for Analytics</a></li>

</ul>
</details>

**标签**: `#langfuse`, `#llm-observability`, `#release-notes`, `#major-version`, `#breaking-changes`

---

<a id="item-3"></a>
## [Android 或将限制设备端 ADB 访问](https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/) ⭐️ 7.0/10

据报道，Google 正在考虑限制设备端 ADB（Android 调试桥）连接，这将限制开发者在没有独立主机的情况下直接在其 Android 设备上运行 ADB 命令的能力。该提议的变更将要求在允许 ADB 访问之前进行额外的用户确认或身份验证步骤。 这一变更直接影响 Android 开发者的工流程，尤其是那些依赖设备端调试进行测试和开发的开发者。它也引发了关于平台锁定（platform lock-in）的更广泛担忧，因为开发者们感到自己越来越依赖 Google 的开发者接口来完成基本的计算任务。 该提议的限制针对的是一个相对狭窄的攻击向量，因为启用远程 ADB 已经需要用户解锁开发者选项并明确激活无线调试。一些开发者建议，将 ADB 限制在特定 IP 地址或接口上，将是一种比全面限制更为适度的安全措施。

hackernews · shscs911 · 7月25日 06:57 · [社区讨论](https://news.ycombinator.com/item?id=49045159)

**背景**: Android 调试桥（ADB）是 Google Android SDK 附带的一个命令行工具，允许开发者从计算机与 Android 设备进行通信。它可以安装和卸载应用程序、复制文件、运行 shell 命令以及检索日志。最初 ADB 需要主机计算机与 Android 设备之间通过 USB 连接，但 Android 11 及更高版本支持通过 Wi-Fi 进行无线 ADB。设备端 ADB 指的是完全在 Android 设备本身上运行 ADB 连接，无需独立计算机，这对于不涉及传统 PC 的开发工作流程非常有用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Android_Debug_Bridge">Android Debug Bridge - Wikipedia</a></li>
<li><a href="https://developer.android.com/tools/adb">Android Debug Bridge ( adb ) | Android Studio | Android Developers</a></li>
<li><a href="https://kitsumed.github.io/blog/posts/android-may-soon-restrict-on-device-adb/">Android May Soon Restrict On - Device ADB , Affecting... | Kitsumed Blog</a></li>

</ul>
</details>

**社区讨论**: 社区对此问题存在分歧。像 microtonal 这样的开发者认为安全收益微乎其微，因为该攻击向量需要用户已经启用了开发者选项和远程 ADB。像 jimrandomh 这样的开发者则认为，将 ADB 限制在特定网络（例如通过 VPN）而非全面禁止更有价值。0x_rs 持更为愤世嫉俗的观点，认为这是 Google 更广泛战略的一部分，旨在将开发者锁定在需要付费开发者账户的模式中，而 eviks 则反驳说批评这一变更不会导致 Google 锁定问题跟踪器。

**标签**: `#android`, `#mobile-development`, `#platform-security`, `#developer-tools`, `#adb`

---

<a id="item-4"></a>
## [开放权重 AI 正迎来它的 Kubernetes 时刻](https://tobi.knaup.me/2026-07-25-open-weight-ai-is-having-its-kubernetes-moment/) ⭐️ 7.0/10

这是一篇发人深省的论文，将开放权重 AI 模型的崛起与 Kubernetes 进行了类比，论证了开放权重模型正在成为 AI 基础设施中商品化、标准化的基础层。

hackernews · tknaup · 7月25日 14:49 · [社区讨论](https://news.ycombinator.com/item?id=49048034)

**标签**: `#open-source-ai`, `#open-weight-models`, `#ai-infrastructure`, `#kubernetes`, `#ai-economics`

---

<a id="item-5"></a>
## [Tile 缺乏端到端加密，使追踪器沦为 stalker 工具](https://blog.adafruit.com/2026/03/05/tiles-security-is-so-bad-its-a-feature-for-stalkers/) ⭐️ 7.0/10

一篇学术论文（arxiv 2510.00350）揭示了 Tile 蓝牙追踪器缺乏端到端加密，使其位置数据容易被用于跟踪骚扰，而 Apple 和 Google 的追踪器则在 BLE 广播中嵌入公钥以实现位置不可区分性。 这一安全漏洞影响着数百万 Tile 用户，凸显了蓝牙追踪器市场上隐私保护的不一致性可能带来现实世界的安全风险，尤其是对跟踪骚扰受害者而言，并可能促使 Tile 及其母公司 Life360 采用更强的加密保护措施。 该论文对比了 Tile 的架构——位置数据流经 Tile 服务器且缺乏端到端加密，对服务商可见——与 Apple 和 Google 的设计：只有持有对应私钥的配对设备才能解密 BLE 广播中嵌入的位置报告。

hackernews · sambellll · 7月25日 18:18 · [社区讨论](https://news.ycombinator.com/item?id=49050152)

**背景**: 蓝牙追踪器是一种可以附加在钥匙或钱包等物品上的小型设备，通过蓝牙低功耗（BLE）信号广播，让智能手机能够定位它们。端到端加密（E2EE）是一种安全方法，只有发送方和预期接收方才能读取数据，防止服务提供商访问。Apple 的 AirTag 和 Google 的 Find My Device 网络都在跟踪软件滥用成为公众担忧后实施了 E2EE。Tile 现在由 Life360 拥有，是消费级蓝牙追踪器市场上历史最久的厂商之一。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/End-to-end_encryption">End-to-end encryption - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/end-to-end-encryption">What is end-to-end encryption (E2EE)? - IBM</a></li>
<li><a href="https://intl.life360.com/blog/which-is-the-best-bluetooth-tracker-tile-for-you">Which Tile Bluetooth Tracker is Right For You? | Tile</a></li>

</ul>
</details>

**社区讨论**: 该论文的最后一位作者参与了讨论，提供技术问答，引发了关于 BLE 广播中公钥/私钥分发机制的有意义讨论。一个值得注意的反观点认为，网上廉价可买到的专用 GPS 跟踪设备比利用 Tile 追踪器构成更紧迫的威胁，反映了在真诚的技术参与之外，对该漏洞现实影响的怀疑态度。

**标签**: `#security`, `#privacy`, `#iot`, `#bluetooth-tracking`, `#research`

---

<a id="item-6"></a>
## [英伟达、Meta、微软、Palantir 和 Hugging Face 等 20 多家公司签署公开信，敦促政策制定者避免对开放权重模型过早施加限制](https://www.reddit.com/r/LocalLLaMA/comments/1v5c3vt/more_than_20_companies_including_nvidia_meta/) ⭐️ 7.0/10

包括英伟达、Meta 和微软在内的 20 多家主要公司签署了一封公开信，敦促政策制定者避免对开放权重 AI 模型过早施加限制，而前沿实验室明显缺席。

reddit · r/LocalLLaMA · /u/etherd0t · 7月24日 13:55

**标签**: `#AI policy`, `#open-source AI`, `#open-weight models`, `#AI regulation`, `#industry news`

---

<a id="item-7"></a>
## [数学的至暗时刻：LLM 自动化定理证明，数学家面临存在危机](https://kirwinhampshire.substack.com/p/the-dark-night-of-mathematics) ⭐️ 6.0/10

这篇发表于 Substack 的评论文章探讨了在大型语言模型（LLM）日益自动化定理证明和证明验证的背景下，数学家所面临的存在危机。该文引发了关于创造力、新颖性以及人类数学家在 AI 快速进步中未来角色的哲学思考。 该文将数学（历来被视为人类智力成就的巅峰）定位为 AI 驱动的劳动力替代的下一个前沿领域，对所有知识工作者都有重要影响。它提出了根本性的问题：真正的数学新颖性能否被自动化？真正创造性的概念飞跃是否需要人类思维？ 文章引用康托尔对角线方法作为 LLM 尚未达到的概念性突破范例，并探讨了一个更广泛的问题：AI 工具会取代定理证明者，还是会让数学家能够创造全新的子领域。近期 AI 系统如 DeepMind 的 AlphaProof 在 2024 年国际数学奥林匹克竞赛中已达到银牌水平，DeepSeek-Prover 在 Lean 4 miniF2F 测试中实现了 52% 的累积准确率。

hackernews · rmdmphilosopher · 7月25日 15:54 · [社区讨论](https://news.ycombinator.com/item?id=49048681)

**背景**: 自动定理证明一直是 AI 研究的目标，而近期使用 LLM 的进展显著加速了这一领域。Lean、Coq（现已更名为 Rocq）和 Isabelle 等形式化证明系统允许数学家编写机器可验证的证明，DeepSeek-Prover 和 Google 的 AlphaProof 等 AI 工具已展示出令人印象深刻的能力——AlphaProof 甚至解决了 2024 年国际数学奥林匹克竞赛中最难的问题。这些系统通过将非形式化的数学陈述自动形式化为形式化语言，然后运行 AI 引导的证明搜索来实现。本文以此技术背景为基础，探讨 AI 究竟是仅仅辅助数学家，还是从根本上改变数学实践的内涵。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2405.14333v1">DeepSeek-Prover: Advancing Theorem Proving in LLMs through Large-Scale Synthetic Data</a></li>
<li><a href="https://deepmind.google/blog/ai-solves-imo-problems-at-silver-medal-level/">AI achieves silver-medal standard solving... — Google DeepMind</a></li>
<li><a href="https://arxiv.org/html/2412.16075">Formal Mathematical Reasoning: A New Frontier in AI</a></li>

</ul>
</details>

**社区讨论**: 评论中反映了丰富多样的观点。一些评论者提出了关于 LLM 能否产生真正新颖概念（如康托尔对角线方法）的哲学问题，主流看法认为真正的数学综合与统一很可能仍超出当前 AI 的能力范围。另一些评论者则提出了务实的重新框架——建议数学家应该利用 AI 协助去创造全新的子领域，而不仅仅是单个定理——并将 1951 年的电影《白衣人》作为技术取代熟练工人的警示故事进行了历史类比。还有一种不同观点认为，数学本质上是有趣的，无关乎新颖性的有无，寻找新结果就像是游览已经被探索过的地方并在其中找到个人意义。

**标签**: `#AI`, `#mathematics`, `#LLM`, `#philosophy`, `#knowledge-work`

---

<a id="item-8"></a>
## [Fedora 45 发布流程端到端详解文章发布](https://supakeen.com/weblog/the-fedora-45-sausage-factory/) ⭐️ 6.0/10

Fedora 贡献者 Simon de Vlieger（supakeen）发布了一篇题为《The Fedora 45 Sausage Factory》的详细端到端文档，追踪了一个软件包从维护者执行 git push 到最终合成版本发布的完整过程，涵盖了 ISO、云镜像、容器镜像和 OSTree 部署。 这是截至 Fedora 45 版本的首份完整公开发布基础设施文档，对于想要了解如何参与贡献的新人，以及在调试源自构建管线问题的用户来说，都具有极高的参考价值。 该文档涵盖了连接 dist-git、Koji、Pungi 和镜像构建器以生成 Fedora 合成版本的工具链，并指出该流程在不断演进——作者打算持续更新。一位评论者回忆了一个历史案例：一个软件包之所以能成功构建，仅仅是因为在非干净的构建机上依赖项按字母顺序排列时偶然满足了依赖。

hackernews · 6581 · 7月25日 11:04 · [社区讨论](https://news.ycombinator.com/item?id=49046525)

**背景**: Fedora 是一个社区赞助的 Linux 发行版，是 Red Hat Enterprise Linux 的上游项目。其发布管线涉及超过一千名软件包维护者，他们将源码变更推送到 dist-git 仓库，然后通过 Koji 构建系统进行构建，并使用 Pungi 等工具合成为可安装的制品。Fedora 发布版本会经历 Rawhide（开发）阶段，然后进入 Beta 和最终发布阶段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://supakeen.com/weblog/the-fedora-45-sausage-factory/">The Fedora 45 Sausage Factory | supakeen's homepage</a></li>
<li><a href="https://lwn.net/Articles/1084920/">De Vlieger: The Fedora 45 sausage factory [LWN.net]</a></li>
<li><a href="https://docs.fedoraproject.org/en-US/infra/release_guide/">Fedora Release Engineering</a></li>

</ul>
</details>

**社区讨论**: 评论者们称赞了这份文档在故障排查方面的实用价值，一位用户反馈说它帮助自己定位了 Fedora 不同版本之间根文件系统权限变化的来源。一位相对较新的 Fedora 用户询问了如何在发布管线中寻找贡献机会，另一位评论者则表达了对项目中所谓企业影响的担忧。还有人分享了一个历史趣闻：过去的构建曾悄无声息地依赖了上次非干净构建机留下的残留产物。

**标签**: `#linux`, `#fedora`, `#release-engineering`, `#open-source`, `#documentation`

---

<a id="item-9"></a>
## [Inflect v2 发布：两个参数低于 1000 万的完整 TTS 模型](https://www.reddit.com/r/LocalLLaMA/comments/1v5ve6v/i_released_inflect_v2_two_ultratiny_complete_tts/) ⭐️ 6.0/10

独立开发者 owensong 发布了 Inflect v2，包含两个端到端神经文本转语音模型：Inflect-Nano-v2 拥有 396 万参数（FP32 下 15.97 MB），Inflect-Micro-v2 拥有 936 万参数（FP32 下 37.53 MB）。两个模型均包含完整流程——文本处理、时长预测、语音生成和波形解码器——直接输出 24 kHz 语音，无需任何外部声码器或托管 API。 这一发布对边缘 AI 和嵌入式部署场景具有重要意义，因为在这些场景下运行数百 MB 的 TTS 系统不切实际，而一个完整的 16 MB TTS 模型可以在 CPU 上实时运行。它也为在不影响可用性的前提下压缩神经 TTS 这一活跃研究方向做出了贡献，据报道 Nano 版本在 CPU 上可达到 10.72 倍实时速度。 Inflect-Micro-v2 取得了 4.395 的 UTMOS22 分数和 3.99% 的语义 WER，而 Nano 得分分别为 4.386 和 4.21%；两者在盲测社区对比中分别获得第二和第三名。这些模型仅支持英语，使用单一固定的男性声音，不支持语音克隆，并且在处理陌生姓名、缩写、数字和同形异义词时仍有困难——尤其是 Nano 听起来可能更薄，偶尔会产生金属感或截断的伪影。

reddit · r/LocalLLaMA · /u/b111ue · 7月25日 02:17

**背景**: 文本转语音（TTS）系统将书面文本转换为口语音频。现代神经 TTS 流程通常由两个阶段组成：一个声学模型从文本预测中间特征（如梅尔频谱图），以及一个独立的声码器将这些特征转换为最终的音频波形。由于这种两阶段设计，许多已部署的 TTS 系统需要在推理时加载多个模型并协调它们。一个"完整"或"端到端"的神经 TTS 模型将所有这些组件整合到单个网络中，从而简化部署。FP32 指的是 32 位浮点精度，是神经网络权重的标准数值格式；模型在 FP32 下的体积大约是每个参数 4 字节。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speech_synthesis">Speech synthesis - Wikipedia</a></li>
<li><a href="https://deepwiki.com/coqui-ai/TTS/4.5-vocoder-models">Vocoder Models | coqui-ai/ TTS | DeepWiki</a></li>
<li><a href="https://www.databasemart.com/blog/fp32-fp16-bf16-int8">FP32, FP16, BF16 & INT8 for AI Deep Learning - databasemart.com</a></li>

</ul>
</details>

**标签**: `#TTS`, `#edge-AI`, `#open-source`, `#speech-synthesis`, `#small-models`

---