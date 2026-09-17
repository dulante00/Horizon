---
layout: default
title: "Horizon Summary: 2026-09-17 (ZH)"
date: 2026-09-17
lang: zh
---

> 从 56 条内容中筛选出 16 条重要资讯。

---

1. [GLM 如何构建自己的推理基础设施](#item-1) ⭐️ 8.0/10
2. [为什么我没有签署菲尔兹奖得主的联名信](#item-2) ⭐️ 8.0/10
3. [Bonsai 2 27B：以 9 倍更小的体积实现近乎无损的压缩](#item-3) ⭐️ 7.0/10
4. [Hister：一款针对您访问的网页和保存的文件的私人搜索引擎](#item-4) ⭐️ 7.0/10
5. [CrowdSec 源码因 TanStack 依赖被入侵而泄露](#item-5) ⭐️ 7.0/10
6. [Servo 浏览器引擎赞助开发一周年回顾](#item-6) ⭐️ 7.0/10
7. [OpenAI 发布模型失准报告框架](#item-7) ⭐️ 7.0/10
8. [华为称 AI 芯片供不应求，加大对英伟达的挑战力度](#item-8) ⭐️ 7.0/10
9. [Astra for Law](#item-9) ⭐️ 6.0/10
10. [Bend – 一种通过形式化证明阻止 AI 错误的编程语言，可运行于 CPU 和 GPU](#item-10) ⭐️ 6.0/10
11. [GitLab.com 收紧速率限制，引发 AI 抓取与 API 设计讨论](#item-11) ⭐️ 6.0/10
12. [OpenAI 在 ChatGPT 中推出 Sponsored Agents 广告产品](#item-12) ⭐️ 6.0/10
13. [工作者如何解锁新的工作方式](#item-13) ⭐️ 6.0/10
14. [单卡 AMD R9700 运行 Qwen3 27B NVFP4 推理速度翻倍](#item-14) ⭐️ 6.0/10
15. [IFM 发布 K2-Horizon-7B：扩散适配器将 LLM 提速至每秒 5200 tokens](#item-15) ⭐️ 6.0/10
16. [首批泄露的 M5 Ultra 基准测试：Qwen 27B Q4 达 50 tok/s](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [GLM 如何构建自己的推理基础设施](https://z.ai/blog/glm-built-its-inference-infrastructure) ⭐️ 8.0/10

GLM 详细介绍了在超过 10 万颗中国制造的 AI 加速器上构建大规模生产推理系统的过程，展示了激进的内存优化，并彰显了中国 AI 基础设施日益增强的独立性。

hackernews · whiteros_e · 9月17日 08:27 · [社区讨论](https://news.ycombinator.com/item?id=49737922)

**标签**: `#AI infrastructure`, `#inference systems`, `#Chinese AI`, `#chip manufacturing`, `#LLM operations`

---

<a id="item-2"></a>
## [为什么我没有签署菲尔兹奖得主的联名信](https://gowers.wordpress.com/2026/09/17/why-i-didnt-sign-the-fields-medallists-letter/) ⭐️ 8.0/10

菲尔兹奖得主蒂姆·高尔斯解释了为何未与其他菲尔兹奖得主一同签署关于人工智能对数学影响的公开信，此举引发了关于 AI 对学术职业发展通道威胁及人类专业价值的重要讨论。

hackernews · simianwords · 9月17日 08:51 · [社区讨论](https://news.ycombinator.com/item?id=49738091)

**标签**: `#AI`, `#mathematics`, `#academia`, `#labor-displacement`, `#career-pipelines`

---

<a id="item-3"></a>
## [Bonsai 2 27B：以 9 倍更小的体积实现近乎无损的压缩](https://prismml.com/news/bonsai-2-27b) ⭐️ 7.0/10

Prism ML 的 Bonsai 2 27B 通过三值权重和 FP16 缩放实现了 9 倍的模型压缩，不过讨论中有人质疑该压缩方法与现有量化方法的对比情况。

hackernews · JonSchneider · 9月17日 21:13 · [社区讨论](https://news.ycombinator.com/item?id=49746618)

**标签**: `#model-compression`, `#quantization`, `#ternary-weights`, `#llm-optimization`, `#inference`

---

<a id="item-4"></a>
## [Hister：一款针对您访问的网页和保存的文件的私人搜索引擎](https://github.com/asciimoo/hister) ⭐️ 7.0/10

Hister 是一款注重隐私的个人搜索引擎，由 Searx 的作者创建，可索引访问过的网页、书签、浏览器历史记录和本地文件，并提供离线预览功能。

hackernews · bookofjoe · 9月17日 16:25 · [社区讨论](https://news.ycombinator.com/item?id=49743097)

**标签**: `#privacy`, `#search-engine`, `#open-source`, `#knowledge-management`, `#personal-tools`

---

<a id="item-5"></a>
## [CrowdSec 源码因 TanStack 依赖被入侵而泄露](https://www.crowdsec.net/blog/crowdsec-statement-source-code-exposure) ⭐️ 7.0/10

CrowdSec 披露，其私有源码因一个被入侵的 TanStack npm 依赖项窃取了具有代码库读取权限的 API 密钥而遭到泄露。公司立即轮换了所有相关令牌和凭证以控制事件影响。 考虑到 CrowdSec 自身销售众包威胁情报服务，却因第三方供应链弱点被攻破，这一事件颇具讽刺意味。它凸显了没有任何组织——即便是安全厂商——能够免受被入侵依赖项带来的连锁风险的影响，同时也引发了仅靠轮换凭证是否足以应对的质疑。 攻击路径可追溯至 TanStack npm 供应链入侵事件（即"Mini Shai-Hulud"蠕虫），攻击者串联了 pull_request_target 漏洞、GitHub Actions 缓存投毒以及 OIDC 令牌提取，在 42 个 @tanstack/* 包中发布了 84 个恶意版本。CrowdSec 的修复措施仅限于轮换 API 密钥，并未解决上游依赖被投毒这一根本原因。

hackernews · eccgecko · 9月17日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=49742355)

**背景**: CrowdSec 是一款开源安全引擎，通过分析日志和 HTTP 请求，利用众包威胁情报来检测和阻止恶意 IP；用户之间共享威胁信号，并共同受益于共享的封禁列表。TanStack 被入侵事件是针对 npm 和 PyPI 生态系统的更广泛自传播式供应链攻击浪潮的一部分，恶意包会劫持 CI/CD 流水线以窃取开发者的 API 密钥和 OIDC 令牌等敏感凭证。这些被盗凭证随后可用于访问私有代码仓库、云账户或发布基础设施，使单个被入侵的包成为大范围的入侵媒介。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tanstack.com/blog/npm-supply-chain-compromise-postmortem">Postmortem: TanStack npm supply-chain compromise | TanStack Blog</a></li>
<li><a href="https://www.stepsecurity.io/blog/mini-shai-hulud-is-back-a-self-spreading-supply-chain-attack-hits-the-npm-ecosystem">TeamPCP's Mini Shai-Hulud Is Back: A Self-Spreading Supply Chain Attack Compromises TanStack npm Packages - StepSecurity</a></li>
<li><a href="https://github.com/crowdsecurity/crowdsec">GitHub - crowdsecurity/crowdsec: CrowdSec - the open-source and participative security solution offering crowdsourced protection against malicious IPs and access to the most advanced real-world CTI. · GitHub</a></li>

</ul>
</details>

**社区讨论**: 评论者指出一家安全公司遭到入侵颇具讽刺意味，多人质疑 CrowdSec 究竟是真正的安全公司，还是仅仅是一个恶意 IP 数据聚合者，认为这类业务更适合由非营利性组织来运营。多位用户批评仅轮换凭证的修复措施不够充分，因为未来的供应链攻击仍会轻易窃取新密钥，并建议采用更强的措施，如硬件安全密钥（YubiKey）和 SSL 证书来保护 Git 访问。还有用户分享了实际部署经验，包括误报率过高以及在旧版 Debian 包装上被切断社区封禁列表等不满。

**标签**: `#security`, `#supply-chain-attack`, `#crowdsec`, `#incident-response`, `#open-source-security`

---

<a id="item-6"></a>
## [Servo 浏览器引擎赞助开发一周年回顾](https://servo.org/blog/2026/09/15/one-year-of-sponsorship/) ⭐️ 7.0/10

Servo 浏览器引擎项目发布了一周年赞助开发回顾，总结了它从 Mozilla 研究项目转型为独立、社区支持项目以来所取得的进展。 Servo 是为数不多的可行替代方案之一，有望打破 Chromium 在 Web 生态系统中的垄断地位，因此其持续开发对于浏览器引擎多样性和 Web 基础设施的独立性具有重要的战略意义。 该项目依赖 NLnet 等组织的赞助，并使用 Rust 语言构建，利用该语言的内存安全保证和并发特性，创建了一个高度并行的渲染架构，将布局、解析和图像解码等任务细粒度地隔离执行。

hackernews · AshleysBrain · 9月17日 08:13 · [社区讨论](https://news.ycombinator.com/item?id=49737849)

**背景**: Servo 是一个实验性的浏览器引擎，最初由 Mozilla 公司创建，作为使用 Rust 编程语言进行浏览器开发的研究项目。在 Mozilla 减少参与后，Servo 成为独立的开源项目，致力于构建快速、安全且并行的浏览器引擎。当今的 Web 平台严重受 Google 的 Chromium 引擎（被 Chrome、Edge 等众多浏览器使用）主导，Apple 的 WebKit 和 Mozilla 的 Gecko 是另外两个广泛部署的引擎，这使得 Servo 和 Ladybird 等项目对于维护浏览器基础设施的多样性和竞争力非常重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Servo_(software)">Servo (software) - Wikipedia</a></li>
<li><a href="https://www.mozillafoundation.org/en/research/library/engineering-the-servo-web-browser-engine-using-rust/">Engineering the Servo Web Browser Engine using Rust - Mozilla Foundation</a></li>

</ul>
</details>

**社区讨论**: 社区总体上对 Servo 作为 Chromium 和同样基于 Rust 的 Ladybird 浏览器的重要替代方案所取得的进展表示支持。评论者强调了 NLnet 作为主要赞助方的作用，并表达了希望华为或三星等大型设备制造商在其产品中采用 Servo 的期望，同时也对该项目资助模式的可持续性和成本效益提出了担忧。

**标签**: `#servo`, `#browser-engine`, `#web-infrastructure`, `#open-source-funding`, `#rust`

---

<a id="item-7"></a>
## [OpenAI 发布模型失准报告框架](https://openai.com/index/model-misalignment-reporting-framework) ⭐️ 7.0/10

OpenAI 发布了一套用于追踪、调查和披露模型失准的正式框架，并附带了六份关于模型异常或令人担忧行为的具体报告。 作为领先的 AI 实验室之一，OpenAI 向系统性披露模型失准问题迈出的这一步，为行业问责制树立了重要先例，并可能影响其他组织披露 AI 安全问题的方式。 该框架托管在 OpenAI 专门的 Alignment 网站（alignment.openai.com/misalignment-reports）上，该网站提供了关于失准如何产生、表现如何以及安全防护在何处成功或失败的公开披露原则。

rss · OpenAI Blog · 9月16日 17:00

**背景**: 模型失准指的是 AI 模型的行为偏离其预期目的或人类价值观——这是 AI 对齐领域的核心挑战。虽然 RLHF（基于人类反馈的强化学习）等技术旨在在训练过程中对齐模型，但对齐问题并未被完全解决：更聪明的模型未必更加对齐，仅靠安全过滤也无法保证正确的对齐。随着前沿模型的能力不断增强，AI 安全社区越来越呼吁各实验室透明地记录和报告失准案例，以建立对风险的集体理解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/model-misalignment-reporting-framework/">Our framework for reporting model misalignment - OpenAI</a></li>
<li><a href="https://alignment.openai.com/misalignment-reports/">Misalignment Notices and Reports · OpenAI Alignment</a></li>
<li><a href="https://research.ibm.com/blog/what-is-alignment-ai">What is AI alignment ? - IBM Research</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#model alignment`, `#OpenAI`, `#responsible AI`, `#transparency`

---

<a id="item-8"></a>
## [华为称 AI 芯片供不应求，加大对英伟达的挑战力度](https://www.reddit.com/r/LocalLLaMA/comments/1wirvb0/chinas_huawei_says_ai_chip_demand_outstrips/) ⭐️ 7.0/10

华为表示其 AI 芯片需求已超过供应能力，尤其是在美国出口管制限制了中国获取先进 GPU 的背景下，华为正加大对英伟达的竞争力度。 这表明在美国出口管制重塑全球半导体格局的背景下，华为在中国本土 AI 基础设施中扮演的角色日益重要。它凸显了中国云服务商和 AI 公司越来越倾向于选择华为昇腾等国产替代方案，可能侵蚀英伟达在其最大市场之一的统治地位。 华为昇腾产品线包括 910b 和 910c 型号，即将推出的 910D 据称性能设计超越英伟达 H100。华为还扩展了其产品组合，推出涵盖 AI 处理、通用计算、存储和高速互联的 11 款芯片，旨在提供完整的 AI 数据中心整体解决方案，而非单一的加速器。

reddit · r/LocalLLaMA · /u/sunychoudhary · 9月17日 11:53

**背景**: 自 2022 年以来，美国政府已实施多轮出口管制，限制中国获取先进 AI 芯片和半导体制造设备，包括禁止向中国出售英伟达 A100 和 H100 等高端 GPU。这些措施促使中国科技公司加速开发国产替代方案。华为旗下海思半导体设计昇腾系列 AI 加速器，已被中国主要云服务商用于 AI 训练和推理工作负载。与此同时，英伟达为中国市场开发了 H20 等合规芯片，但这些产品也面临着监管方面的不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/huawei-ascend-ai-910d-processor-designed-to-take-on-nvidias-blackwell-and-rubin-gpus">Huawei Ascend AI 910D processor designed to... | Tom's Hardware</a></li>
<li><a href="https://www.zerohedge.com/ai/huawei-pulls-its-nvidia-killer-forward-q1-theres-catch">Huawei Pulls Its Nvidia-Killer Forward To Q1 - But... | ZeroHedge</a></li>
<li><a href="https://www.csis.org/analysis/understanding-biden-administrations-updated-export-controls">Understanding the Biden Administration’s Updated Export Controls</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#Huawei`, `#Nvidia`, `#semiconductors`, `#China tech`

---

<a id="item-9"></a>
## [Astra for Law](https://openai.com/index/astra-for-law/) ⭐️ 6.0/10

OpenAI 推出了 Astra for Law，这是一款面向法律应用的专业领域 AI 产品，通过 API 合作伙伴关系实现与 Harvey 和 Legora 等现有法律科技平台的集成。

hackernews · OpenAI Blog · 9月17日 20:17 · [社区讨论](https://news.ycombinator.com/item?id=49745940)

**标签**: `#openai`, `#legal-tech`, `#ai-products`, `#vertical-ai`, `#domain-specific`

---

<a id="item-10"></a>
## [Bend – 一种通过形式化证明阻止 AI 错误的编程语言，可运行于 CPU 和 GPU](https://bend-lang.com/) ⭐️ 6.0/10

Bend 是一门新兴的编程语言，它利用基于形式化证明的不变式检查来捕获错误（尤其是 AI 生成代码中的错误），并且能够在 CPU 和 GPU 上运行。

hackernews · nicolas-siplis · 9月17日 20:36 · [社区讨论](https://news.ycombinator.com/item?id=49746163)

**标签**: `#programming-languages`, `#formal-verification`, `#gpu-computing`, `#ai-code-generation`, `#developer-tools`

---

<a id="item-11"></a>
## [GitLab.com 收紧速率限制，引发 AI 抓取与 API 设计讨论](https://about.gitlab.com/blog/rate-limit-change-2026/) ⭐️ 6.0/10

GitLab.com 在 2026 年的博客文章中宣布调整速率限制，将未认证请求额度降至每小时 60 次，而免费认证用户仍保留每小时 5,000 次。此次政策调整部分被定位为应对 AI 驱动的抓取行为对平台造成的压力。 此次变更影响所有与 GitLab.com API 交互的开发者和 AI 智能体，可能扰乱依赖宽松匿名访问的 LLM 驱动工作流和 CI/CD 自动化。它也标志着更广泛的行业趋势：平台正在对过去被视为开放的访问进行变现或限制，推动生态系统走向更可持续的融资模式。 未认证每小时 60 次与认证每小时 5,000 次之间的巨大差距，实际上迫使用户创建账户；而 GraphQL 能够限制响应负载大小，使其对 LLM 智能体远比 REST 更加 token 高效。部分评论者认为这本质上是出于收入驱动的订阅推广，而非纯粹针对抓取行为的技术应对。

hackernews · darkwater · 9月17日 15:33 · [社区讨论](https://news.ycombinator.com/item?id=49742353)

**背景**: 速率限制用于控制客户端在给定时间窗口内可发出的 API 请求数量，平台借此防止滥用并管理基础设施成本。AI 抓取——即生成式 AI 公司为训练或推理而进行的自动化批量数据采集——在 2025 至 2026 年间成为争议焦点，网站越来越频繁地封锁或向抓取方收费。GitLab 和 GitHub 都提供 REST 和 GraphQL API；GraphQL 允许客户端精确指定所需字段，从而大幅减少数据量，这一特性恰好与 LLM 上下文窗口限制高度契合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cacm.acm.org/opinion/ai-scraping-and-the-open-web/">AI Scraping and the Open Web – Communications of the ACM</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-scraping">What is AI scraping? - IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者分为几派：一派热情推崇 GraphQL，称其因 token 效率高而成为 LLM 智能体的理想 API 接口；另一派则强调被忽略的细节——免费认证用户每小时仍可获得 5,000 次的宽裕额度；还有人提议与被抓取的开源仓库分享收益，作为可持续的融资模式；持怀疑态度者则认为此举的真实目的是推动付费订阅增长，而非遏制 AI 抓取。也有评论幽默地指出，连新闻稿本身似乎也是由 Claude 撰写的。

**标签**: `#gitlab`, `#rate-limits`, `#ai-scraping`, `#platform-policy`, `#developer-tools`

---

<a id="item-12"></a>
## [OpenAI 在 ChatGPT 中推出 Sponsored Agents 广告产品](https://openai.com/index/reimagining-advertising-with-ai) ⭐️ 6.0/10

OpenAI 宣布推出全新 AI 驱动的广告体验，包括 Sponsored Agents、营销人员工具，以及与 HubSpot 和 Shopify 的集成，于 2026 年 9 月 16 日正式进入 AI 广告市场。 这标志着 OpenAI 商业模式的重大转变，从 API 定价转向代理中介式广告，使 ChatGPT 成为一个品牌本身成为产品的广告平台，可能重塑 AI 时代数字广告的运作方式。 与依赖外部链接的传统数字广告不同，Sponsored Agents 将品牌互动直接嵌入 AI 驱动的对话中，而据报道 OpenAI 在此次广告业务推进之前不到 200 天内就达到了 10 亿美元的年化收入。

rss · OpenAI Blog · 9月16日 13:00

**背景**: Agentic AI（代理式 AI）指的是能够自主做出决策并采取行动以实现目标的 AI 系统，在营销领域，它可以实现广告活动的大规模自动规划、执行和优化。Adobe 和 Amazon Ads 等主要平台已经开始构建代理式营销工作流程。OpenAI 进入 Sponsored Agents 领域是消费者聊天机器人产品中首批大规模部署代理中介式广告的尝试之一，借助 Shopify 和 HubSpot 等成熟商业后台和营销平台的集成来实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://forkast.news/openais-sponsored-agents-turn-chatgpt-into-an-ad-platform-where-brands-are-the-product/">OpenAI’s Sponsored Agents Turn ChatGPT Into an Ad Platform ...</a></li>

</ul>
</details>

**标签**: `#openai`, `#ai-advertising`, `#sponsored-agents`, `#marketing-tech`, `#industry-announcement`

---

<a id="item-13"></a>
## [工作者如何解锁新的工作方式](https://openai.com/index/unlocking-new-ways-of-working) ⭐️ 6.0/10

OpenAI 经济研究探讨了工作者如何在传统角色之外使用 AI，以及哪些由 AI 赋能的新活动会成为他们工作中的常规部分。

rss · OpenAI Blog · 9月16日 09:00

**标签**: `#AI adoption`, `#economic research`, `#workforce productivity`, `#OpenAI`, `#human-AI interaction`

---

<a id="item-14"></a>
## [单卡 AMD R9700 运行 Qwen3 27B NVFP4 推理速度翻倍](https://www.reddit.com/r/LocalLLaMA/comments/1wiws8e/153_toks_on_1x_amd_radeon_r9700_running_qwen38/) ⭐️ 6.0/10

在单张 AMD Radeon R9700 上运行 Unsloth 的 Qwen3.8 27b NVFP4 模型的基准测试显示，解码速度最高达 153 tok/s（JSON 类别），8 并发请求时聚合吞吐达 471 tok/s，在 16k 上下文深度下预填充吞吐峰值达 3,619 tok/s。发布者针对社区反复提出的需求，优化了其定制的 vLLM 分支（vllm-mxfp4），使单卡 R9700 用户在所有基准类别中的性能大约翻倍。 这表明一块中端单卡 AMD GPU 可以轻松以可用的交互速度运行 27B 级别的模型，降低了历史上相对于 NVIDIA 支持较弱的 AMD 硬件用户部署本地 LLM 的门槛。它还标志着 AMD ROCm 与 FP4 推理量化支持的日趋成熟，随着模型规模持续增长，这一能力至关重要。 作者使用了 Unsloth 的 NVFP4 量化 Qwen3.8 27b 权重，通过定制的 vllm-mxfp4 分支（也镜像到了名为 radiance-vllm-mxfp4 的 Codeberg 仓库）进行推理服务；在 2k 到 32k 上下文范围内预填充吞吐保持在 3,400 tok/s 以上，在 64k 时仅下降至约 3,192 tok/s，解码延迟在 p50 上徘徊于 34–42 毫秒之间。NVFP4 是 NVIDIA 推出的 4 位浮点格式，相比前代 MXFP4 具有更小的块大小，可在 Blackwell 级硬件上实现激进的内存压缩并保持有竞争力的精度，现在显然也可用于 RDNA4 硬件。

reddit · r/LocalLLaMA · /u/whodoneit1 · 9月17日 15:14

**背景**: 大语言模型推理通常分为两个阶段：预填充（prefill），即一次性处理整个提示以填充 KV 缓存；和解码（decode），即以自回归方式逐个生成 token。预填充属于计算密集型，受益于高显存带宽和高吞吐，而解码则受显存带宽限制，通常青睐更大的批处理规模或激进的量化方案。NVFP4 是 NVIDIA 推出的 4 位浮点量化格式，采用小的分组块和每块缩放因子，相比 16 位格式可将模型显存占用减少约 4 倍，同时保持足够实际的推理精度。Unsloth 是一个流行的开源库，可加速大语言模型的微调，并导出与 vLLM 等推理服务框架兼容的模型格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>
<li><a href="https://deepwiki.com/NVlabs/QeRL/3.2-nvfp4-quantization">NVFP4 Quantization | NVlabs/QeRL | DeepWiki</a></li>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization | NVIDIA Technical...</a></li>

</ul>
</details>

**标签**: `#AMD GPU`, `#local LLM`, `#inference benchmarks`, `#Qwen3`, `#NVFP4 quantization`

---

<a id="item-15"></a>
## [IFM 发布 K2-Horizon-7B：扩散适配器将 LLM 提速至每秒 5200 tokens](https://www.reddit.com/r/LocalLLaMA/comments/1wj2hsm/ifmk2horizon7buno_hugging_face_5200tps_with_no/) ⭐️ 6.0/10

IFM 在 Hugging Face 上发布了 K2-Horizon-7B，这是一款扩散增强型语言模型，在自回归权重旁添加了即插即用的扩散适配器以实现并行 token 生成。据称该模型可达到每秒 5200 tokens 的生成速度且无质量损失，相比标准自回归推理提速约 2.2× 至 2.5×。 如果这些声明得到验证，这种方法可以显著降低 LLM 的推理成本和延迟，使高吞吐量 AI 部署更加经济实惠。适配器的即插即用特性意味着现有的自回归模型无需完全重新训练即可受益，这对开源 AI 生态系统而言将是一个重要的实际优势。 该架构在标准自回归模型的每一层添加了一组专用于并行 token 生成的独立扩散权重，从而将生成质量与生成速度解耦。然而，发布内容中“无质量损失”的声明缺乏公开的基准测试数据，且 IFM 自身在不同渠道分别引用了 2.2× 和 2.5× 等不同的加速数字，因此仍需独立验证才能将结果视为定论。

reddit · r/LocalLLaMA · /u/Zulfiqaar · 9月17日 18:43

**背景**: 标准的自回归 LLM（如 GPT）按顺序逐个生成 token，这限制了推理吞吐量。相比之下，扩散语言模型可以并行生成多个 token，并通过减少生成步骤来灵活地在速度和质量之间进行权衡。“Uno”方法试图结合两种范式的优势，在现有自回归模型上添加轻量级扩散适配器，从而无需重新训练基础模型即可实现并行 token 输出。K2-Horizon 是 IFM 更广泛的模型家族，包含六款参数规模从 0.9B 到 375B、以 Apache 2.0 协议发布的完全开源模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://hyper.ai/en/papers/2609.04010">Unlocking Lossless Speedups in LLMs via Discrete Diffusion | HyperAI</a></li>
<li><a href="https://cryptobriefing.com/uno-diffusion-llm-throughput/">Uno achieves 2.5x higher throughput in LLMs by bolting diffusion onto...</a></li>
<li><a href="https://ifm.ai/k2/">K2 Horizon: Open-Source AI Models for Every Scale | IFM</a></li>

</ul>
</details>

**标签**: `#diffusion-models`, `#llm-inference`, `#model-optimization`, `#open-source-models`, `#speedup`

---

<a id="item-16"></a>
## [首批泄露的 M5 Ultra 基准测试：Qwen 27B Q4 达 50 tok/s](https://www.reddit.com/r/LocalLLaMA/comments/1wisr6h/first_m5_ultra_benchmarks/) ⭐️ 6.0/10

苹果尚未发布的 M5 Ultra 芯片的早期基准测试数据出现在 omlx 网站上，显示该芯片在 8K 上下文窗口、Q4 量化、未启用多令牌预测的情况下，运行 Qwen 3.8 27B 模型时文本生成速度约为 50 tokens/sec，提示处理速度达 1800 tokens/sec。 如果数据属实，这些成绩将大幅提升 Apple Silicon 上消费级本地大语言模型推理的性能上限，缩小 Mac 工作站与专用 GPU 平台之间的差距，并可能改变本地运行模型的爱好者和专业人士的硬件选购决策。 基准测试在 Q4 量化（4 比特权重，可降低显存与计算需求）下对 Qwen 3.8 27B 模型、8K 上下文窗口、未启用 MTP 加速进行了测量。数据来源可信度未经证实：omlx 网站的官方身份不明，目前尚无独立复现测试，且苹果官方尚未正式发布 M5 Ultra。

reddit · r/LocalLLaMA · /u/Ashefromapex · 9月17日 12:34

**背景**: Qwen 是阿里巴巴云开发的开源权重大语言模型系列，Qwen3 引入了混合思考模式，允许用户在推理深度与速度之间灵活权衡。Q4 量化是一种训练后压缩技术，将模型权重压缩到每个参数约 4 比特，以极小的质量损失换取显存占用降低和推理加速，这对在消费级硬件上运行大模型尤为重要。多令牌预测（MTP）是一种新兴的推理加速技术，通过并行预测多个令牌来提升吞吐量，而本次 M5 Ultra 的测试未启用 MTP，意味着在启用 MTP 后实际吞吐量还可能更高。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2402.16775v1">A Comprehensive Evaluation of Quantization Strategiesfor ...</a></li>
<li><a href="https://arxiv.org/html/2502.09419v1">On multi-token prediction for efficient LLM inference - arXiv.org</a></li>

</ul>
</details>

**标签**: `#apple-silicon`, `#m5-ultra`, `#local-llm`, `#hardware-benchmarks`, `#inference-performance`

---