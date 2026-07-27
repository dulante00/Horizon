---
layout: default
title: "Horizon Summary: 2026-07-27 (ZH)"
date: 2026-07-27
lang: zh
---

> 从 48 条内容中筛选出 13 条重要资讯。

---

1. [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](#item-1) ⭐️ 8.0/10
2. [Kimi-K3 登陆 HuggingFace](#item-2) ⭐️ 8.0/10
3. [法官驳回谷歌针对搜索结果抓取的 DMCA 版权主张](#item-3) ⭐️ 7.0/10
4. [利用沃尔沃/艾彻车队平台控制所有用户和车辆](#item-4) ⭐️ 7.0/10
5. [Bun 的 Rust 重写进展顺利，v1.4 预计下周发布](#item-5) ⭐️ 7.0/10
6. [NVIDIA Cosmos-H-Dreams 为手术机器人带来实时生成式仿真](#item-6) ⭐️ 7.0/10
7. [OpenAI 拒绝加入 Nvidia 发起的开放安全 AI 联盟](#item-7) ⭐️ 7.0/10
8. [中国 DRAM 厂商长鑫存储上市首日飙升 500%，市值超越英特尔](#item-8) ⭐️ 7.0/10
9. [Langfuse 发布 v4.0.0-rc.3 候选版，迎接重大版本更新](#item-9) ⭐️ 6.0/10
10. [Paged Out #9：免费技术黑客杂志新一期发布](#item-10) ⭐️ 6.0/10
11. [Misago 论坛从 React.js 迁移到 HTMX](#item-11) ⭐️ 6.0/10
12. [libsm64：将超级马里奥 64 打包为外部游戏引擎可用库](#item-12) ⭐️ 6.0/10
13. [英伟达 CEO 黄仁勋为开源 AI 辩护，称蒸馏是学习的基础](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 8.0/10

vLLM v0.26.0 引入了全新的 Inkling 模型家族及其完整支持栈（包括 CUDA 图、Hopper FA4 注意力、MTP 推测解码、LoRA、NVFP4 量化），并在 NVIDIA、AMD、XPU 等多个厂商平台上对 DeepSeek-V4 进行了性能优化，端到端 TPOT 提升最高达 2.94%，内核速度提升 1.5–2 倍，同时新增通过 head_dtype 实现的 fp32 lm_head 支持以提升生成精度。 vLLM 是应用最广泛的开源大模型推理引擎之一，本次优化直接降低了生产环境中的服务成本与延迟，而 Inkling 支持和 fp32 lm_head 等精度改进则扩展了可被忠实服务的模型范围。针对 AMD ROCm 和 Intel XPU 的跨厂商收益也让不再局限于 NVIDIA 的运营方拥有了更丰富的硬件选择。 本版本包含 212 位贡献者（其中 61 位新加入）提交的 411 个提交。其他值得关注的特性包括：按 KV-cache 组选择注意力后端、将滑动窗口显式化为后端能力、KV 卸载指标与具备对象存储和 DP-replica 感知能力的分层二级存储、Rust 前端的多模态视频与音频支持，以及 Transformers 5.13.0 后端升级并完成 Olmo/Olmo2、MistralLarge3、HunyuanVL 的迁移。

github · khluu · 7月27日 01:06

**背景**: vLLM 是一个开源的大模型高吞吐量推理引擎，最初由加州大学伯克利分校开发，现已广泛应用于生产级大模型服务。推测解码（包括多 Token 预测 MTP）是一种使用草稿模型或辅助预测头在每一步生成多个候选 Token，并由主模型并行验证以降低延迟的技术。NVFP4 是 NVIDIA 的 4 位浮点量化格式，采用非 2 的幂次缩放因子以在低精度下保持更高精度，通常应用于 MoE 专家权重。FlashAttention-4（FA4）是面向 Hopper 和 Blackwell GPU 的最新一代内存高效注意力内核。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision Inference | NVIDIA Technical Blog</a></li>
<li><a href="https://pytorch.org/blog/flexattention-flashattention-4-fast-and-flexible/">FlexAttention + FlashAttention-4: Fast and Flexible – PyTorch</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#release-notes`, `#deepseek`, `#open-source`, `#cuda`

---

<a id="item-2"></a>
## [Kimi-K3 登陆 HuggingFace](https://huggingface.co/moonshotai/Kimi-K3) ⭐️ 8.0/10

Moonshot AI 在 HuggingFace 上发布了 Kimi-K3，这是一款拥有 3 万亿参数的开源大语言模型，同时可通过 Fireworks AI 提供第三方托管服务。

hackernews · nateb2022 · 7月27日 06:18 · [社区讨论](https://news.ycombinator.com/item?id=49065752)

**标签**: `#open-source-llm`, `#kimi-k3`, `#large-language-models`, `#huggingface`, `#moonshot-ai`

---

<a id="item-3"></a>
## [法官驳回谷歌针对搜索结果抓取的 DMCA 版权主张](https://www.techdirt.com/2026/07/27/judge-rejects-googles-attempt-to-dmca-its-way-out-of-being-scraped/) ⭐️ 7.0/10

一位法官驳回了谷歌针对 SerpAPI 提起的 DMCA 版权侵权主张，裁定搜索引擎结果页面缺乏足够的原创性，不符合版权保护的条件，从而确认了抓取谷歌搜索结果以获取结构化数据的合法性。 这一裁决为数据抓取生态系统树立了重要的法律先例，影响了搜索引擎和其他平台利用版权主张阻止第三方数据收集的方式。它波及 SEO 工具、AI 训练数据管道、竞争情报服务以及所有依赖程序化访问搜索结果的开发者。 此案的核心争议在于搜索结果页面在选择、协调或编排上是否具有足够的创意表达以获得版权保护——法院认定谷歌未达到这一标准。值得注意的是，谷歌此前已停用其公开的搜索 API，批评者指出这使得第三方抓取工具成为以编程方式访问搜索数据的少数选择之一。

hackernews · cdrnsf · 7月27日 18:15 · [社区讨论](https://news.ycombinator.com/item?id=49073513)

**背景**: DMCA（数字千年版权法）是美国的一项版权法，为版权持有人提供了对其认为侵权的内容发出下架通知的机制。SerpAPI 是一项商业服务，抓取谷歌、Bing、YouTube 等搜索引擎的结果，为 SEO、AI 和研究工作流返回结构化的 JSON 数据。谷歌此前曾提供公开的搜索 API，但已将其停用，使抓取成为以编程方式访问搜索结果的主要途径。这一裁决明确，搜索结果的事实性汇编可能达不到美国法律要求的创意表达门槛，无法获得版权保护。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://serpapi.com/">SerpApi: Google Search API</a></li>
<li><a href="https://www.howtogeek.com/what-is-serpapi-and-how-are-developers-using-it/">What is SerpApi, and how are developers using it?</a></li>
<li><a href="https://www.copyright.gov/">U.S. Copyright Office | U.S. Copyright Office</a></li>

</ul>
</details>

**社区讨论**: 评论者对谷歌的诉讼策略表示不满，指出谷歌在停用自家搜索 API、让开发者几乎别无选择后，又起诉抓取者，这一行为颇具讽刺意味。多位用户强调了抓取的现实必要性，例如用于检测搜索结果中的广告骗局。一位评论者对比了欧盟数据库保护（要求实质性投入）与美国版权法（要求创意原创性），指出何为合格的界限较为模糊。整体情绪普遍支持该裁决，并对谷歌的法律立场持批评态度。

**标签**: `#legal`, `#copyright`, `#data-scraping`, `#google`, `#search-apis`

---

<a id="item-4"></a>
## [利用沃尔沃/艾彻车队平台控制所有用户和车辆](https://eaton-works.com/2026/07/27/my-eicher-hack/) ⭐️ 7.0/10

负责任地披露沃尔沃/艾彻车队管理平台中的一个严重漏洞，该漏洞可能允许攻击者通过内部 API 访问控制所有车辆和用户。

hackernews · EatonZ · 7月27日 15:08 · [社区讨论](https://news.ycombinator.com/item?id=49070756)

**标签**: `#security`, `#vulnerability-disclosure`, `#automotive-security`, `#iot`, `#fleet-management`

---

<a id="item-5"></a>
## [Bun 的 Rust 重写进展顺利，v1.4 预计下周发布](https://lockwood.dev/ai/2026/07/27/how-is-the-bun-rewrite-in-rust-going.html) ⭐️ 7.0/10

Bun 的 Rust 重写已于一个多月前完成，整个翻译过程借助了 Anthropic 的 Claude Code，且几乎未引发问题。创始人 Jarred Sumner 表示，v1.4 很可能在下周二发布，前提是用于提升 Node.js 测试兼容性的待合并 PR 顺利合入。 Bun 是一个广泛使用的 JavaScript 运行时，定位为 Node.js 的直接替代品，因此它从 Zig 转向 Rust 的举动会影响庞大的开发者生态，也标志着 LLM 开始被用于生产级别的代码翻译。在短时间内借助 Claude Code 完成整个运行时代码库的翻译，是 AI 辅助软件工程领域的一个显著里程碑。 Bun 使用 Safari 的 JavaScriptCore 作为 JavaScript 引擎，这一点与使用 V8 的 Node.js 和 Deno 不同，使其 Rust 重写的复杂度更高。Jarred 还提到，团队目前正专注于在新翻译的 Rust 代码中排查和移除 'unsafe' 代码，这可能会暂时降低发布节奏。

hackernews · tomlockwood · 7月27日 11:12 · [社区讨论](https://news.ycombinator.com/item?id=49067854)

**背景**: Bun 是由 Jarred Sumner 创建的一款集 JavaScript 运行时、包管理器、打包器和测试运行器于一体的工具，于 2021 年 9 月首次发布，旨在作为更快的 Node.js 替代方案。该项目最初使用 Zig（一种底层系统编程语言）编写，但团队后来决定用 Rust 重写，部分原因是工具链和生态方面的考虑。Claude Code 是 Anthropic 推出的智能编码助手，运行在终端中，能够读取代码库、编辑文件并执行命令，帮助开发者更快交付功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Bun_(software)">Bun (software) - Wikipedia</a></li>
<li><a href="https://bun.com/">Bun — A fast all-in-one JavaScript runtime</a></li>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent, Terminal, IDE</a></li>

</ul>
</details>

**社区讨论**: 评论者指出，在重大重写刚结束后，commit 数量和发布节奏并不能真实反映项目健康度，因为团队仍在熟悉 Rust 代码库，并优先减少 'unsafe' 代码，而非赶功能发布。一些用户对 LLM 生成的产品表示怀疑，强调真正好的软件来自持续的功能开发、bug 修复和 UI 工作，而非一次性代码生成。还有人提到社区中有一个用 Zig 重写的项目号称实现了亚秒级构建，从而引发了对 Rust 重写是否必要的争论。

**标签**: `#bun`, `#rust`, `#javascript`, `#llm-assisted-development`, `#runtime`

---

<a id="item-6"></a>
## [NVIDIA Cosmos-H-Dreams 为手术机器人带来实时生成式仿真](https://huggingface.co/blog/nvidia/cosmos-h-dreams) ⭐️ 7.0/10

NVIDIA 展示了 Cosmos-H-Dreams，这是一个基于其 Cosmos 世界基础模型构建的实时生成式仿真框架，旨在加速手术机器人系统的开发与训练。该框架利用生成式世界模型，为手术机器人领域生成逼真且可交互的仿真环境。 将生成式世界模型应用于手术机器人，代表了前沿 AI 仿真技术在医疗领域的高风险、高影响力落地。通过实现实时、照片级逼真的仿真，该框架可以大幅缩短手术机器人训练和验证所需的时间与成本，并降低真实部署前的风险。 Cosmos-H-Dreams 基于 NVIDIA 开源的 Cosmos 世界基础模型平台构建，涵盖高级分词器和加速数据流水线，支持跨语言、图像、视频、音频和动作序列的多模态生成。其实时特性使其有别于速度较慢的生成方法，适合交互式机器人训练循环，而非仅限于离线数据合成。

rss · HuggingFace Blog · 7月27日 09:32

**背景**: 世界基础模型（WFM）是一类生成式 AI 模型，经过训练后能够理解并预测物理环境的动态，通常可根据动作生成视频、3D 场景或传感器数据。NVIDIA Cosmos 是一个面向物理 AI 应用（包括自动驾驶和机器人）的此类模型开源平台。生成式仿真利用这些模型创建合成训练环境，减少对昂贵的真实数据采集的依赖。在手术机器人领域，由于真实手术存在患者风险，高保真仿真对于安全训练和验证尤为有价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/ai/cosmos/">Physical AI with World Foundation Models | NVIDIA Cosmos</a></li>
<li><a href="https://github.com/NVIDIA/Cosmos">NVIDIA / cosmos : NVIDIA Cosmos is an open platform of world ...</a></li>
<li><a href="https://developer.nvidia.com/isaac/sim">Isaac Sim - Robotics Simulation and Synthetic Data Generation | NVIDIA Developer</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#Cosmos`, `#surgical-robotics`, `#world-models`, `#generative-simulation`

---

<a id="item-7"></a>
## [OpenAI 拒绝加入 Nvidia 发起的开放安全 AI 联盟](https://www.reddit.com/r/LocalLLaMA/comments/1v8e36c/openai_management_decided_earlier_today_not_to/) ⭐️ 7.0/10

OpenAI 管理层决定不加入由 Nvidia 及 CEO 黄仁勋联合 30 多家公司近期发起的开放安全 AI 联盟（Open Secure AI Alliance），该联盟旨在共建并共享开源 AI 安全工具。该决定在内部传达后，据报道遭到了 OpenAI 员工的强烈反对。 这一决定凸显了封闭式 AI 开发（OpenAI 的路线）与由 Nvidia 及其行业合作伙伴倡导的开源 AI 协作之间的持续张力。据报道的员工反对表明，OpenAI 内部在开放性与安全协作的战略方向上存在分歧。 开放安全 AI 联盟成员包括微软、SpaceX、IBM、Palantir、Linux 基金会、Cloudflare、Dell、Cisco、Adobe、Siemens 和 DoorDash 等主要科技公司，专注于网络安全防御工具的开发。据报道，OpenAI、Google 和 Anthropic 是该联盟中最引人注目的缺席 AI 实验室，这暗示了专注于 AI 安全的实验室之间在开放协作标准上可能存在分歧。

reddit · r/LocalLLaMA · /u/KickLassChewGum · 7月27日 21:37

**背景**: 开放安全 AI 联盟由 Nvidia 近期宣布成立，旨在开发和共享面向 AI 系统的开源安全工具，借鉴了成功的开源软件基金会模式。该联盟建立在 Nvidia 在 AI 硬件（GPU）领域占据主导地位的基础上，同时也是其向 AI 安全与安全基础设施领域更广泛拓展的一部分。OpenAI 历来倾向于采用更封闭的开发方式和专有模型，尽管它正越来越多地参与安全研究社区的活动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blogs.nvidia.com/blog/open-secure-ai-alliance/">Industry Leaders Join Open Secure AI Alliance for AI Safety ...</a></li>
<li><a href="https://www.helpnetsecurity.com/2026/07/27/nvidia-open-secure-ai-alliance/">Tech giants form alliance to put open AI in cyber defenders' hands - Help Net Security</a></li>
<li><a href="https://mangodeveloper.com/articles/nvidia-and-microsoft-launch-open-ai-security-alliance-openai-google-and-anthropi">Nvidia and Microsoft Launch Open AI Security Alliance , OpenAI...</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Nvidia`, `#AI industry`, `#alliances`, `#corporate strategy`

---

<a id="item-8"></a>
## [中国 DRAM 厂商长鑫存储上市首日飙升 500%，市值超越英特尔](https://www.reddit.com/r/LocalLLaMA/comments/1v7vdvg/chinese_chipmaker_cxmts_market_capitalization/) ⭐️ 7.0/10

中国 DRAM 芯片制造商长鑫存储（CXMT）在 A 股市场上市首日股价飙升近 500%，市值达到约 3.28 万亿元人民币（约合 4650 亿美元），超越了市值约 4656 亿美元（3.15 万亿元人民币）的英特尔。此次上市使长鑫存储成为 A 股市场市值最大的公司。 这一里程碑标志着全球半导体格局的重大转变——中国存储芯片厂商首次在市值上超越了长期占据行业主导地位的英特尔。DRAM 是人工智能基础设施、服务器和消费电子产品的关键组件，因此长鑫存储的崛起对全球内存供应链以及美中科技竞争背景下的芯片制造地缘政治具有直接影响。 长鑫存储总部位于安徽省合肥市，成立于 2016 年，目前是中国大陆唯一能够大规模量产通用型 DRAM 的垂直整合制造商（IDM）。其产品组合涵盖 DDR5、LPDDR5X、DDR4 和 LPDDR4X 内存，按产能计算大约是全球第四大 DRAM 制造商。

reddit · r/LocalLLaMA · /u/Fun-Doctor6855 · 7月27日 09:26

**背景**: DRAM（动态随机存取存储器）是一种易失性存储器，用于临时存储智能手机、个人电脑、服务器及其他计算设备正在处理的数据。垂直整合制造商（IDM）是一种半导体商业模式，由单一公司完成从芯片设计研发到制造销售的整个生产链条，从而对知识产权、质量和上市时间拥有严格控制。英特尔的 IDM 业务模式详解：英特尔和三星都是知名的 IDM 企业，但许多新兴企业采用无晶圆厂（fabless）或晶圆代工（foundry）模式，依赖台积电等第三方代工厂进行芯片制造。CXMT 是中国最大的 DRAM 制造商，也是中国推动半导体自给自足战略的重要组成部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cxmt.com/en/">About cxmt - cxmt</a></li>
<li><a href="https://chinaidb.com/companies/cxmt/">CXMT ( ChangXin Memory ) — China AI Index</a></li>
<li><a href="https://www.vyrian.com/blog/semiconductor-manufacturing-idm-fabless-foundry/">Semiconductor Manufacturing Demystified: IDM, Fabless, and Foundry Explained - Vyrian</a></li>

</ul>
</details>

**标签**: `#semiconductors`, `#DRAM`, `#CXMT`, `#Intel`, `#China-tech`

---

<a id="item-9"></a>
## [Langfuse 发布 v4.0.0-rc.3 候选版，迎接重大版本更新](https://github.com/langfuse/langfuse/releases/tag/v4.0.0-rc.3) ⭐️ 6.0/10

Langfuse 发布了 v4.0.0-rc.3，即重大 v4 版本的第三个候选版。该版本包含懒加载 JSON 查看器的性能遥测、改进的事件筛选选项、增强的 SDK 迁移检测、媒体保留租约修复、移动端 UI 间距调整，以及修复了 API key 权限范围查找的鉴权问题。此候选版还新增了 Claude Opus 5 默认定价，并移除了旧的 v4 迁移页面以使用改进后的迁移工具。 此版本修复了从已验证的 key（而非提交的 key）解析 publicKey 权限范围的问题（PR #15456），将缺失仪表板的错误从 500 改为 404，以及在 blob 清理过程中保留保留积压指标。v4 SDK 迁移检测的改进和旧迁移页面的移除表明，团队正在 v4 正式版发布前统一整合为单一、更新的迁移路径。

github · Steffen911 · 7月27日 08:32

**背景**: Langfuse 是一个面向 LLM 可观测性、链路追踪、提示词管理、评估和数据集的开源 AI 工程平台，被 Merck Group、Twilio 等众多构建生产级 LLM 应用的团队广泛采用。v4 SDK 是一次重大升级：TypeScript SDK 于 2025 年 8 月完全重写为基于 OpenTelemetry 的架构，引入了破坏性变更，给部分团队的迁移带来了挑战。Langfuse 于 2026 年初被 ClickHouse 收购，目前在 GitHub 上拥有约 26.6K stars，可通过 Docker、Kubernetes 或托管 Cloud 部署。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://langfuse.com/docs/observability/sdk/upgrade-path/python-v3-to-v4">Python v3 → v4 - Langfuse</a></li>
<li><a href="https://github.com/orgs/langfuse/discussions/14155">[Docs] Comprehensive TypeScript SDK v4 migration guide ...</a></li>

</ul>
</details>

**标签**: `#langfuse`, `#llm-observability`, `#release`, `#v4-migration`, `#tracing`

---

<a id="item-10"></a>
## [Paged Out #9：免费技术黑客杂志新一期发布](https://pagedout.institute/download/PagedOut_009.pdf) ⭐️ 6.0/10

Paged Out #9 作为免费技术黑客杂志的最新一期已发布，提供可下载的 PDF 版本，涵盖了从 C 语言编程、子像素渲染到可计算铺砖等多领域的文章。 Paged Out 持续作为分享深度且充满好奇心驱动型技术内容的重要平台，现在还提供印刷版，使其成为当代黑客文化中兼具数字与实体形式的珍贵文献。 该杂志被读者比作 Phrack 和 2600 杂志等经典黑客出版物，其中一篇关于可计算铺砖的文章被指出是无署名地重新发现了王浩（Hao Wang）1960 年代将铺砖问题与停机问题联系起来的研究成果。

hackernews · laurensr · 7月27日 14:22 · [社区讨论](https://news.ycombinator.com/item?id=49070138)

**背景**: Paged Out 是一份由社区驱动的黑客杂志，以其多样化、极具深度的技术文章和独特的设计风格而闻名。子像素渲染是一种利用独立的红、绿、蓝子像素来提升有效分辨率的显示技术，广泛应用于 LCD 和 OLED 屏幕上的字体渲染。可计算铺砖涉及王氏瓷砖（Wang tiles）和铺砖问题，王浩在 1960 年代证明了判断一组有限瓷砖能否铺满整个平面是不可判定的——这一结果在可计算性理论中等价于停机问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Subpixel_rendering">Subpixel rendering - Wikipedia</a></li>
<li><a href="https://link.springer.com/chapter/10.1007/978-0-387-09680-3_13">Computability of Tilings | Springer Nature Link</a></li>
<li><a href="https://arxiv.org/abs/1208.2759">[1208.2759] Local Rules for Computable Planar Tilings - arXiv.org</a></li>

</ul>
</details>

**社区讨论**: 社区反响非常积极，读者们赞扬该杂志的幽默感、设计和技术深度。一条引人注目的评论将可计算铺砖的文章与王浩 1960 年代的研究联系起来，其他评论则将其与 Phrack 和 2600 杂志等经典黑客出版物相提并论，并有多位读者表示将购买印刷版。

**标签**: `#zine`, `#hacker-culture`, `#programming`, `#computer-science`, `#tiling`

---

<a id="item-11"></a>
## [Misago 论坛从 React.js 迁移到 HTMX](https://misago-project.org/t/removing-reactjs-from-the-codebase-and-adapting-htmx-for-ui-interactivity/1267/) ⭐️ 6.0/10

基于 Django 的论坛项目 Misago 宣布从代码库中移除 React.js，改用 HTMX 来实现服务端渲染的 UI 交互功能。该案例研究在 Misago 社区论坛上分享，旨在记录迁移过程并收集关于 HTMX 实际权衡的反馈。 这次迁移的意义在于，Misago 是一个为真实社区提供服务的生产级论坛平台，使其成为团队权衡 SPA 与服务端渲染架构辩论时的可信实战案例。它为更广泛的 HTMX 采用趋势提供了实践证据，展示了一个中等复杂度的应用如何用更简单的超文本驱动交互来取代 JavaScript 重度前端。 HTMX 是一个轻量级（压缩后约 16KB）且无依赖的库，通过属性扩展 HTML，支持 AJAX、CSS 过渡、WebSockets 和 Server-Sent Events，据称相比 React 可减少 67% 的代码量。一位评论者指出，当一次性返回同时包含复杂筛选表单和结果列表的单一 HTML 响应时，页面会变得缓慢，这表明需要进行细致的页面拆分以保证性能。

hackernews · Ralfp · 7月27日 09:58 · [社区讨论](https://news.ycombinator.com/item?id=49067301)

**背景**: Misago 是一个基于 Django 构建的独立互联网论坛应用，可与 Discourse 或 Invision Community 相媲美，此前的非管理后台前端重度依赖由 Django API 支撑的 React.js 组件。HTMX 由 hyperscript 脚本语言背后的团队创建，采用了不同的架构思路：它不在浏览器端打包 JavaScript 来渲染 UI，而是让服务器返回 HTML 片段，由 HTMX 直接交换到 DOM 中。这种“超媒体作为应用状态引擎”（HATEOAS）风格吸引那些希望获得 SPA 般交互体验、但又不想承担完整客户端框架、构建流水线或 API 层复杂性的开发者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://htmx.org/">htmx - high power tools for html</a></li>
<li><a href="https://github.com/rafalp/Misago">GitHub - rafalp/Misago: Misago is fully featured modern forum ...</a></li>
<li><a href="https://forum.djangoproject.com/t/misago-forum-software/24024">Misago Forum Software - Show & Tell - Django Forum</a></li>

</ul>
</details>

**社区讨论**: 这个拥有 147 条评论的讨论帖反映出社区对 HTMX 总体持积极态度，开发者分享了将它与 DaisyUI 和 TailwindCSS 配合用于类 PWA 移动应用的成功经验，并普遍认同 HTMX 天然适合内容主要为文字和媒体的文件类论坛软件。主要担忧包括在返回包含复杂表单的大型 HTML 响应时会出现性能瓶颈，部分评论者推荐了诸如 PyView（灵感来自 Elixir Phoenix LiveView）等替代方案。多位用户指出，混合方案——大多数页面使用 HTMX，仅在确实需要复杂交互（如所见即所得编辑器）的场景嵌入小型 Vue 或 React 应用——是一种务实的折中做法。

**标签**: `#htmx`, `#react`, `#web-architecture`, `#server-side-rendering`, `#django`

---

<a id="item-12"></a>
## [libsm64：将超级马里奥 64 打包为外部游戏引擎可用库](https://github.com/libsm64/libsm64) ⭐️ 6.0/10

libsm64 是一个开源共享库，它封装了从《超级马里奥 64》逆向工程得到的角色机制、运动、物理和渲染代码，使开发者能够通过简洁的 C 接口将马里奥放入《半条命 2》等其他游戏引擎中。 它将多年积累的 SM64 反编译成果转化为可供 mod 玩家和独立开发者使用的实用工具，无需专有中间件即可实现跨游戏角色复用——这一理念常被“元宇宙”愿景所承诺，却在此通过草根逆向工程真正落地。 libsm64 构建于 n64decomp/sm64 反编译项目之上，仍然需要用户提供《超级马里奥 64》ROM 以提取资源；该反编译项目本身支持多个地区版本（日本、美版、欧版、Shindou 和神游机版），目标是通过编译生成与原始 ROM 字节完全一致的文件。

hackernews · klaussilveira · 7月27日 10:04 · [社区讨论](https://news.ycombinator.com/item?id=49067352)

**背景**: SM64 反编译项目是一个由社区驱动的计划，旨在从已编译的 N64 ROM 中重建游戏的原始 C 源代码，与模拟器不同的是，它生成的是人类可读、可修改的代码，而非模拟硬件运行。libsm64 在此重建代码库的基础上，将马里奥的角色逻辑分离出来并通过库 API 暴露给外部使用。由于任天堂的原始资源仍受版权保护，用户必须提供自己合法获取的 ROM 才能进行资源提取——反编译仅恢复代码，不涉及美术或音频资产。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/libsm64/libsm64">libsm 64 / libsm 64 : Mario 64 as a library for use in external game ...</a></li>
<li><a href="https://github.com/n64decomp/sm64">GitHub - n64decomp/sm64: A Super Mario 64 decompilation ... Nintendo 64 Decompilation Projects - GitHub SM64 Decompilation Super Mario 64 reverse engineering project - Ciro Santilli ... Nintendo 64 (Project Reality) Reversing github.com-n64decomp-sm64_-_2024-02-04_10-26-16 - Archive.org</a></li>
<li><a href="https://deepwiki.com/libsm64/libsm64">libsm64/libsm64 | DeepWiki</a></li>

</ul>
</details>

**社区讨论**: 社区反应总体上非常积极且充满趣味。评论者称赞这一概念是“《头号玩家》走进现实”，无需企业炒作就实现了元宇宙的设想，并分享了马里奥出现在《半条命 2》等引擎中的演示视频，还贴出了一个汇总 libsm64 应用项目的 GitHub 列表。有用户开玩笑说要把它包装成 API“即服务”，另一位用户则询问非引擎使用者上手的难易程度。

**标签**: `#reverse-engineering`, `#game-development`, `#n64`, `#open-source`, `#creative-coding`

---

<a id="item-13"></a>
## [英伟达 CEO 黄仁勋为开源 AI 辩护，称蒸馏是学习的基础](https://www.reddit.com/r/LocalLLaMA/comments/1v81nqt/nvidia_ceo_jensen_huang_defends_open_source_ai_by/) ⭐️ 6.0/10

英伟达 CEO 黄仁勋认为，蒸馏——即从其他 AI 模型中学习——是智能的基础，不应被视为窃取行为。他主张 AI 系统之间应该开放共享知识。

reddit · r/LocalLLaMA · /u/ImaginaryRea1ity · 7月27日 14:15

**标签**: `#nvidia`, `#open-source-ai`, `#distillation`, `#jensen-huang`, `#ai-policy`

---