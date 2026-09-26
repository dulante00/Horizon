---
layout: default
title: "Horizon Summary: 2026-09-26 (ZH)"
date: 2026-09-26
lang: zh
---

> 从 48 条内容中筛选出 15 条重要资讯。

---

1. [我们将需要远比以前更多的数学家](#item-1) ⭐️ 8.0/10
2. [Ollama v0.40.0-rc0 默认在 Apple Silicon 上启用 MLX 运行时](#item-2) ⭐️ 7.0/10
3. [Show HN：Reladraw——一种由你决定元素放置位置的图表语言](#item-3) ⭐️ 7.0/10
4. [ASML says it sold 'absolutely nothing' in Europe in 2026](#item-4) ⭐️ 7.0/10
5. [DeepSeek 弹性计算 (DSec)](#item-5) ⭐️ 6.0/10
6. [十五年后：Apple Cards 鲜为人知的起源故事](#item-6) ⭐️ 6.0/10
7. [在 LLM 编程代理时代如何保持对编程的热爱](#item-7) ⭐️ 6.0/10
8. [Conversations 通讯应用离开 Google Play 转向 F-Droid](#item-8) ⭐️ 6.0/10
9. [下滑的考试成绩是一场缓慢发生的灾难](#item-9) ⭐️ 6.0/10
10. [Jev AI 代理实时直播游玩《精灵宝可梦 红》并公开成本](#item-10) ⭐️ 6.0/10
11. [Automattic 重组董事会，此前罢免 CEO 未果](#item-11) ⭐️ 6.0/10
12. [KoboldCpp 内置轻量级 Agentic 框架发布](#item-12) ⭐️ 6.0/10
13. [改进并修复 GPT-OSS 的模板（再次更新）。包含 preserve_thinking 功能及对 Unsloth 引发 Bug 的修复](#item-13) ⭐️ 6.0/10
14. [在 4x3060ti 配置上获得惊人出色的结果](#item-14) ⭐️ 6.0/10
15. [Splash 1.1.0 发布，新增 GGUF 与 MLX 支持（Apple Silicon）](#item-15) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [我们将需要远比以前更多的数学家](https://terrytao.wordpress.com/2026/09/24/were-gonna-need-a-lot-more-mathematicians/) ⭐️ 8.0/10

陶哲轩认为，AI 时代将需要远超以往数量的数学家，很可能用于形式化验证和对 AI 系统的严格审查，因为当下对大语言模型生成代码敷衍盖章放行的做法非常危险。

hackernews · srcreigh · 9月26日 02:46 · [社区讨论](https://news.ycombinator.com/item?id=49852717)

**标签**: `#AI safety`, `#formal verification`, `#mathematics`, `#Terry Tao`, `#software engineering`

---

<a id="item-2"></a>
## [Ollama v0.40.0-rc0 默认在 Apple Silicon 上启用 MLX 运行时](https://github.com/ollama/ollama/releases/tag/v0.40.0-rc0) ⭐️ 7.0/10

Ollama 发布了 v0.40.0-rc0 候选版本，在 Apple Silicon 设备上为支持的模型架构默认启用 MLX 运行时。版本号从 0.34 跃升至 0.40，表明底层有大量改动，更多模型架构将在预发布期间逐步进行测试和启用。 这一改动有望显著提升 Mac 用户的 LLM 推理性能，因为 MLX 利用了原生的 Metal GPU 加速和 Apple Silicon 的统一内存架构，据称比 Ollama 之前的默认后端快 20-50%。这巩固了 Ollama 作为领先本地 LLM 运行工具的地位，并扩大了其对 Apple 开发者与爱好者社区的吸引力。 这是一个预发布版本（RC0），因此仍可能存在 bug 和不稳定问题；MLX 默认设置仅适用于 MLX 运行时支持的模型架构，更多模型将在候选版测试阶段逐步加入。完整更新日志涵盖了从 v0.34.4 到 v0.40.0-rc0 的所有提交，表明自上一个稳定版以来累积了大量变更。

github · github-actions[bot] · 9月25日 03:31

**背景**: Ollama 是一款广受欢迎的开源工具，允许用户在本地硬件上下载、运行和交互大语言模型（LLM），无需持续联网。MLX 是 Apple 机器学习研究团队于 2023 年 12 月发布的开源数组计算框架，专为 Apple Silicon 芯片设计，利用 Apple Silicon 的统一内存架构和 Metal GPU 加速来高效执行机器学习任务。据报道，在相同硬件上，MLX 比 Ollama 之前的默认后端快 20-50%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://llmcheck.net/guides/mlx-framework-apple-silicon/">Getting Started with MLX : Apple 's AI Framework for Mac — LLM Check</a></li>
<li><a href="https://www.linkedin.com/pulse/fine-tuning-open-source-llms-apples-mlx-framework-guide-vishnu-n-c-ylqrc">Fine-Tuning Open-Source LLMs with Apple 's MLX Framework ...</a></li>
<li><a href="https://www.freecodecamp.org/news/run-and-customize-llms-locally-with-ollama/">How to Run and Customize LLMs Locally with Ollama</a></li>

</ul>
</details>

**标签**: `#ollama`, `#release`, `#apple-silicon`, `#mlx`, `#local-llm`

---

<a id="item-3"></a>
## [Show HN：Reladraw——一种由你决定元素放置位置的图表语言](https://github.com/reladraw/reladraw) ⭐️ 7.0/10

Reladraw 是一种全新的图表 DSL（领域特定语言），融合了声明式语法与相对定位控制，同时面向人类和 AI 智能体的编写场景，旨在弥合自动布局工具与手动图表编辑器之间的差距。

hackernews · jpwalsh234 · 9月26日 17:10 · [社区讨论](https://news.ycombinator.com/item?id=49858513)

**标签**: `#diagram-tools`, `#dsl`, `#developer-tools`, `#ai-agents`, `#show-hn`

---

<a id="item-4"></a>
## [ASML says it sold 'absolutely nothing' in Europe in 2026](https://www.tomshardware.com/tech-industry/semiconductors/asml-says-its-sells-absolutely-nothing-in-europe-calls-on-eu-to-help-create-demand) ⭐️ 7.0/10

ASML reports zero sales in Europe for 2026, calling on the EU to stimulate domestic semiconductor demand amid regulatory and competitive challenges.

hackernews · MC995 · 9月25日 13:49 · [社区讨论](https://news.ycombinator.com/item?id=49844663)

**标签**: `#semiconductors`, `#ASML`, `#EU-industrial-policy`, `#lithography`, `#geopolitics`

---

<a id="item-5"></a>
## [DeepSeek 弹性计算 (DSec)](https://arxiv.org/abs/2609.22978) ⭐️ 6.0/10

DeepSeek 发布了一篇关于其弹性计算系统 (DSec) 的论文,该系统在 160 个基于 Epyc 的服务器节点上实现了 380,000 个并发沙盒,其规模之大和作者列表之长均十分引人注目。

hackernews · shenli3514 · 9月26日 18:22 · [社区讨论](https://news.ycombinator.com/item?id=49859112)

**标签**: `#deepseek`, `#infrastructure`, `#elastic-compute`, `#sandboxes`, `#scaling`

---

<a id="item-6"></a>
## [十五年后：Apple Cards 鲜为人知的起源故事](https://lexontech.org/fifteen-years-later-the-apple-cards-origin-story) ⭐️ 6.0/10

一篇回顾文章揭示了苹果在 2011 年前后推出 Apple Cards 实体贺卡服务时所克服的技术和物流挑战，包括发明喷涂在信封上的隐形紫外线条码，以在不破坏信封外观的前提下追踪邮寄的每一个环节。 这个故事展示了苹果如何利用其平台优势排挤提供类似功能的独立创业公司（即所谓的「Sherlocked」现象），并凸显了小型竞争对手无法复制的纵向整合与供应链谈判能力（包括与美国邮政署达成的协议）。 隐形条码被喷涂在信封上，仅在特定紫外线下可见，美国邮政署同意在从寄出到送达的多个节点扫描这些卡片。卡片采用凸版印刷风格的压凹工艺制作——这种工艺因 Martha Stewart 的推广而流行——以赋予实体产品高级的触感。

hackernews · ksec · 9月26日 09:13 · [社区讨论](https://news.ycombinator.com/item?id=49854693)

**背景**: Apple Cards（不要与 2019 年推出的 Apple Card 信用卡混淆）是一款 iPhone 应用，允许用户创建并邮寄带有自己照片的实体贺卡。与此同时，Sincerely 等几家创业公司也提供类似的「从 iPhone 到实体卡片」服务，包括 Postagram 和 Sincerely Ink。苹果将此类服务整合进其生态系统的能力，常常让第三方开发者难以竞争，社区成员将这种动态戏称为「Sherlocking」，得名于早期 macOS 中一项复制流行第三方工具的功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://angtech.com/invisible-uv-barcode-technology-5-tips/">Invisible UV Barcode Technology | Angstrom Technologies Inc.</a></li>
<li><a href="https://www.onlinetoolcenter.com/blog/Invisible-UV-Barcodes-The-Future-of-Secure-Product-Tracking.html">Invisible UV Barcodes: The Future of Secure Product Tracking</a></li>

</ul>
</details>

**社区讨论**: Sincerely 的联合创始人分享了一手经历，回忆在看到苹果发布会时感到被「Sherlocked」的恐惧与愤怒交织。其他评论者则赞赏隐形紫外线条码系统及与美国邮政署合作的工程壮举，有人怀念旅行时寄送卡片的流畅体验，还有人就压凹工艺与凸版印刷作为设计选择的文化意义展开了讨论。

**标签**: `#apple`, `#product-history`, `#hardware`, `#startups`, `#design`

---

<a id="item-7"></a>
## [在 LLM 编程代理时代如何保持对编程的热爱](https://discourse.haskell.org/t/how-to-keep-enjoying-programming-in-a-world-of-llms/14705) ⭐️ 6.0/10

一个广受欢迎的 Discourse 讨论（135 个赞，193 条评论）探讨了随着 LLM 编程代理日益普及，程序员如何保持技艺和对编程的热爱。评论者分享了技能退化、动力转变以及在代理辅助工作流中人类开发者角色变化的亲身经历。 随着 AI 辅助编程从新鲜事物变成日常工作流，这次讨论反映了开发者社区日益增长的关于存在与实践层面的担忧。工程师如何调整习惯、保留核心能力并从工作中找到意义，将塑造下一代软件工艺与开发者身份认同。 该帖子包含一个令人印象深刻的汽车机械师类比，将传统手写编码工作比作通过软件补丁调校现代汽车；评论者还指出，仅依赖代理几周后就会出现可衡量的技能退化。围绕"弥补编程代理盲区"而兴起的新技能与从零编写代码的传统能力形成了对比。

hackernews · signa11 · 9月26日 09:41 · [社区讨论](https://news.ycombinator.com/item?id=49854875)

**背景**: LLM 编程代理是构建在大语言模型（如 Claude 或 GPT）之上的 AI 系统，能够在开发者的环境中自主读取、编写、调试和重构代码。此领域的工具涵盖从 IDE 集成的助手到像 OpenCode 这样的完全代理系统，后者可以规划并执行多步骤任务。这些工具的兴起引发了关于其对开发者技能、生产力以及编程内在满足感影响的激烈讨论。2025 年一项经常被引用的研究测量了开发者在学习新 Python 库时使用和不使用 AI 辅助的表现差异，推动了关于依赖性和技能损失的更广泛关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tianpan.co/blog/2026/04/19/skill-atrophy-ai-augmented-engineering">The Skill Atrophy Trap: How AI Assistance Silently Erodes the...</a></li>
<li><a href="https://dev.to/jeremiah0616/ai-skill-atrophy-and-coding-by-hand-literally-3j9e">AI Skill Atrophy and Coding By Hand (Literally) - DEV Community</a></li>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>

</ul>
</details>

**社区讨论**: 社区情绪复杂但具有反思性。一些用户如 beej71 报告了具体的技能退化现象——在依赖 LLM 后甚至为小型项目做架构决策时感到困难；而 visarga 则认为真正的技能正在转向管理代理的局限性，而非手写代码。BizarreByte 持务实观点，认为 LLM 能去除繁琐的工作；chicken-stew 则分享了生成代码体验持续不佳的经历；TSiege 坦诚地指出使用代理编码后动力正在减退，凸显了这一转变中的情感层面。

**标签**: `#LLMs`, `#developer-experience`, `#programming-culture`, `#skill-development`, `#AI-assisted-coding`

---

<a id="item-8"></a>
## [Conversations 通讯应用离开 Google Play 转向 F-Droid](https://gultsch.de/posts/breaking-up-with-google-play/) ⭐️ 6.0/10

由 Daniel Gultsch 开发的知名开源 XMPP 即时通讯应用 Conversations 因对 Google 的政策、费用以及糟糕的开发者支持感到不满，正式离开 Google Play Store，转而通过 F-Droid 分发并改为免费应用。 这一案例凸显了独立开发者与主流应用商店把关者之间日益加剧的矛盾，说明了平台垄断如何在收取费用的同时提供低劣的支持服务，并可能促使更多开源项目寻求替代的分发渠道。 开发者指出 Google 收取的佣金和糟糕的支持服务是关键问题，而该应用转向 F-Droid——一个自由开源的 Android 应用仓库——也反映出 Google 同步通过警告提示让 Play Store 以外的应用安装变得越来越困难。

hackernews · ezst · 9月26日 10:55 · [社区讨论](https://news.ycombinator.com/item?id=49855315)

**背景**: XMPP（可扩展消息与出席协议）是一种最初名为 Jabber 的开放通信标准，用于即时通讯、出席状态和联系人列表管理，为专有通讯平台提供了可互操作的替代方案。F-Droid 是一个专门提供自由开源软件（FOSS）的 Android 替代应用商店，让用户无需依赖 Google 生态即可安装应用。Google Play Store 对应用销售和应用内购买收取佣金，这一费用长期以来在开发者中备受争议，他们认为平台以此换来的支持服务非常糟糕。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/XMPP">XMPP - Wikipedia</a></li>
<li><a href="https://f-droid.org/">F - Droid - Free and Open Source Android App Repository</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对开发者表示同情，认为如果 Google 能提供优质支持，合理的费用尚可接受，但 Google 的垄断地位使其可以无视开发者的需求。具体的痛点包括基于 IVR 的电话验证对使用自动电话系统的企业无法正常工作，以及人们担忧 Google Play 正在演变为对爱好者和小型企业开发者充满敌意的环境，同时通过各种警告让侧载安装变得更加困难。

**标签**: `#open-source`, `#android`, `#google-play`, `#app-distribution`, `#f-droid`

---

<a id="item-9"></a>
## [下滑的考试成绩是一场缓慢发生的灾难](https://www.economist.com/leaders/2026/09/10/plunging-test-scores-are-a-slow-moving-catastrophe) ⭐️ 6.0/10

经济学人文章及 Hacker News 讨论探讨学生考试成绩急剧下降的问题，评论者就 AI、注意力经济算法或校园内手机使用是否为主要原因展开辩论，并提出了政策干预建议。

hackernews · vinni2 · 9月26日 15:24 · [社区讨论](https://news.ycombinator.com/item?id=49857442)

**标签**: `#education`, `#social-media`, `#attention-economy`, `#society-and-technology`, `#policy`

---

<a id="item-10"></a>
## [Jev AI 代理实时直播游玩《精灵宝可梦 红》并公开成本](https://jev-pokemon.vercel.app/) ⭐️ 6.0/10

开发者 Christian Mat 开源了名为 "Jev-pokemon" 的项目，让 AI 代理实时游玩《精灵宝可梦 红》，并在直播中公开每次推理消耗的 token 数量和费用。该项目部署在 Vercel 上，代码托管在 GitHub，展示了 Jev 决策框架与 LLM 配合，在复杂游戏环境中尝试长程任务的表现。 该项目可作为一个公开基准，用于评估当前基于 LLM 的智能体在长程、部分可观测且奖励稀疏的任务上的表现——这类任务比单纯的益智游戏基准更贴近真实场景。实时公开的 token 和成本数据也提升了智能体部署中常被忽视的经济性透明度。 观众注意到该代理经常陷入行为循环（例如反复进出同一扇门），并且其执行框架大量依赖人工编写的脚手架（如寻路算法和文本里程碑提示），意味着 LLM 并不是纯粹从原始游戏画面进行推理。据观察，运行约六小时后代理解开了岩石隧道的推石谜题，但随后便卡在试图硬闯四天王处，未能重新调整队伍等级。

hackernews · pancomplex · 9月25日 14:28 · [社区讨论](https://news.ycombinator.com/item?id=49845172)

**背景**: Jev is an open-source agent architecture that offloads frequent, simple 'yes/no' decisions away from the LLM and into a lightweight typed runtime called 'System One', reserving the large model for harder reasoning. This design reduces latency and cost compared to routing every micro-decision through an LLM. Playing Pokémon Red has become a recurring informal benchmark for LLM agents because the game requires multi-step planning, navigation, combat strategy, and memory over very long horizons, exposing the limits of current models.

<details><summary>参考链接</summary>
<ul>
<li><a href="https://jev-agent.org/agent">Jev AI Agent : Build Fast Decision Loops | Jev Agent</a></li>
<li><a href="https://dev.to/trending/jev-and-system-one-models-for-agent-architecture">Jev and System One Models for Agent Architecture... - DEV Community</a></li>
<li><a href="https://github.com/THUDM/AgentBench">GitHub - THUDM/AgentBench: A Comprehensive Benchmark to...</a></li>

</ul>
</details>

**社区讨论**: The community was broadly enthusiastic but technically critical. Commenters praised the speed and cost efficiency initially, then flagged that the agent makes poor tactical decisions and gets stuck in repetitive loops. Several pointed out that the heavy hand-engineered harness (pathfinding, milestone hints) makes the run closer to a guided walkthrough than a pure LLM playthrough, with one suggesting the experiment would be far more compelling if run through vLLM with an abliterated open model that had no prior Pokémon knowledge.

**标签**: `#ai-agents`, `#llm`, `#gaming-ai`, `#open-source`, `#live-demo`

---

<a id="item-11"></a>
## [Automattic 重组董事会，此前罢免 CEO 未果](https://techcrunch.com/2026/09/25/automattic-has-a-new-board-after-failed-attempt-to-put-ceo-on-leave/) ⭐️ 6.0/10

Automattic 重组了董事会，此前试图让 CEO Matt Mullenweg 休行政假的行动以失败告终，尽管 Mullenweg 持有公司 84% 的有投票权股份。 这一事件凸显了董事会与采用双层股权结构、由创始人控制的公司之间的矛盾，引发了关于董事会问责制以及在创始人持有绝大多数投票权时公司治理实际效力的问题。 据报道，临时董事们在短暂的过渡期内为自己安排了丰厚的离职补偿金，这表明推动这次罢免行动的动机可能是经济利益，而非真正的治理关切。

hackernews · ilamont · 9月26日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=49857572)

**背景**: Automattic 是运营 WordPress.com、Tumblr、WooCommerce 等网络服务的公司，由 Matt Mullenweg 创立，他也是开源 WordPress 项目的联合创始人。双层股权结构使创始人的投票权远超其经济持股比例，这种安排在科技公司中很常见，旨在保护创始人免受短期市场压力的影响，但也常因削弱董事会效力而受到批评。近年来 WordPress 生态系统争议不断，包括商标使用和托管服务商之间的纠纷，已经影响了社区对公司的信任。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wptavern.com/automattic-is-migrating-tumblr-to-wordpress">Automattic is Migrating Tumblr to WordPress – WP Tavern</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍指出，考虑到 Mullenweg 持有 84% 的投票权，董事会的尝试注定会失败，一些人质疑在这种股权结构下董事会还有何存在意义。多位用户猜测，真正动机是临时董事们为自己安排的丰厚离职补偿金，一些人则对 WordPress 用户及公司声誉的更广泛影响表示担忧。少数评论者赞赏了 Mullenweg 对此事的果断处理。

**标签**: `#corporate-governance`, `#automattic`, `#wordpress`, `#startups`, `#business-news`

---

<a id="item-12"></a>
## [KoboldCpp 内置轻量级 Agentic 框架发布](https://www.reddit.com/r/LocalLLaMA/comments/1wqlyp8/introducing_koboldcpp_agent_and_a_plea_for_help/) ⭐️ 6.0/10

KoboldCpp 现在内置了 Agent Harness，捆绑了 9 个工具和约 2k token 的系统提示，可通过 GUI 中的复选框或 `--agent` 启动参数启用。它支持通过 `mcp.json` 加载 MCP 工具、兼容 OpenAI Chat Completions 协议的端点、AGENTS.md 以及上下文压缩，并提供三种工具调用审批模式（on/auto/off）。 它为本地 LLM 用户提供了一种比 OpenCode、Codex 或 Claude Code 等更重量级 Agent 工具更易上手的替代方案，消除了让爱好者感到沮丧的复杂配置过程。项目维护者还揭露了一个活跃的钓鱼网站（`kobolcpp.com`），该网站通过黑帽 SEO 分发恶意软件，这提醒我们开源 AI 工具正面临着真实的供应链威胁。 该 Agent 框架至少需要 28k 上下文和 8k 生成长度，建议配备 12GB 以上显存；MCP 工具在服务器端执行，而 Agent 工具在客户端执行。项目还提供了一个 `.kcppt` 模板，用于快速启动推荐的 Qwen 3.6 35B-A3B 模型。

reddit · r/LocalLLaMA · /u/HadesThrowaway · 9月26日 09:13

**背景**: KoboldCpp 是一个基于 llama.cpp 的单文件开源本地 LLM 推理引擎，因无需复杂配置即可在消费级硬件上运行模型而广受欢迎。Agentic 框架（agentic harness）是包裹在 LLM 外面的编排层，负责管理工具、状态和审批流程，从而让模型能够代替用户自主行动——将对话模型转变为自主 Agent。OpenCode 和 Claude Code 等工具已在编程场景中推广了这一模式，但通常需要较重的配置，而这正是 KoboldCpp 内置框架试图绕开的痛点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://koboldcpp.com/">KoboldCPP – Run AI Models Locally , Free & Open-Source</a></li>
<li><a href="https://kingy.ai/news/what-is-an-agentic-harness-the-missing-layer-between-llms-and-ai-agents/">What Is an Agentic Harness ? The Missing Layer Between LLMs and...</a></li>
<li><a href="https://github.com/opencode-ai/opencode">GitHub - opencode - ai / opencode : A powerful AI coding agent .</a></li>

</ul>
</details>

**社区讨论**: 这篇帖子本身将功能发布与社区呼吁结合起来，呼吁大家共同打击冒充 KoboldCpp 的钓鱼网站，表明该项目目前最关心的是保护用户免受通过假冒域名 `kobolcpp.com` 分发的恶意软件侵害。维护者请求用户协助举报该站点，因为此前向 Google 和托管商提交的举报均未生效。

**标签**: `#local-llm`, `#koboldcpp`, `#agentic-ai`, `#open-source-tools`, `#llm-infrastructure`

---

<a id="item-13"></a>
## [改进并修复 GPT-OSS 的模板（再次更新）。包含 preserve_thinking 功能及对 Unsloth 引发 Bug 的修复](https://www.reddit.com/r/LocalLLaMA/comments/1wr0wki/improved_and_fixed_template_for_gptoss_again/) ⭐️ 6.0/10

修复了 GPT-OSS 的 Jinja 模板，纠正了 Unsloth 版本中一个严重缺陷——该缺陷会导致推理时保留的推理历史降低模型输出质量。

reddit · r/LocalLLaMA · /u/arbv · 9月26日 20:35

**标签**: `#GPT-OSS`, `#LocalLLaMA`, `#Jinja-templates`, `#Unsloth`, `#bug-fix`

---

<a id="item-14"></a>
## [在 4x3060ti 配置上获得惊人出色的结果](https://www.reddit.com/r/LocalLLaMA/comments/1wqv9o8/getting_stupidly_good_results_on_my_4x3060ti_setup/) ⭐️ 6.0/10

一位注重预算的用户展示了使用 4x3060ti 设备通过 Exl3 和 HyperQwen 的张量并行技术，在 27B 模型上实现 70 t/s 推理速度，证明旧款消费级 GPU 在本地运行 LLM 仍然可行。

reddit · r/LocalLLaMA · /u/DontWinFrensWthSalad · 9月26日 16:47

**标签**: `#local-llm`, `#tensor-parallelism`, `#rtx-3060ti`, `#exl3`, `#hardware-optimization`

---

<a id="item-15"></a>
## [Splash 1.1.0 发布，新增 GGUF 与 MLX 支持（Apple Silicon）](https://www.reddit.com/r/LocalLLaMA/comments/1wqw9rn/splash_110_released_gguf_quants_support_mlx/) ⭐️ 6.0/10

Splash 1.1.0 正式发布，新增了对 GGUF 量化的支持以及 MLX 导入功能。在配备 64GB 统一内存的 M5 Pro 上，该工具对 27B Qwen3 模型（Unsloth UD-Q4_K_XL 量化）实现了约 50 tokens/s 的推理速度。 此次发布使得在消费级 Apple Silicon 硬件上以可用速度运行中等规模 27B 参数模型进行智能体本地工作流成为现实，降低了注重隐私的端侧 AI 开发门槛。它将多项性能优化技术整合到单一程序中，减少了本地 LLM 推理优化中常见的繁琐步骤。 Splash 将优化的内核、推测解码（speculative decoding）、精心实现的 prefix cache 以及混合权重支持整合到同一个程序中。50 t/s 的速度是在 Qwen3 27B 使用 Unsloth UD-Q4_K_XL 量化的条件下测得的，该量化方案以极小的精度损失换取显著的内存节省。

reddit · r/LocalLLaMA · /u/wojtek15 · 9月26日 17:27

**背景**: GGUF（GGML Unified Format）是一种二进制文件格式，将量化后的模型权重、分词器数据和架构元数据打包到单一可移植文件中，被 llama.cpp 及兼容的推理引擎所使用。MLX 是 Apple 开源的数组框架，专门为 Apple Silicon 上的机器学习设计，充分利用 CPU 与 GPU 共享的统一内存架构。推测解码（speculative decoding）是一种推理加速技术，它使用较小的草稿模型一次性预测多个 token，然后由大模型并行验证，通常能在不改变输出分布的前提下带来显著的速度提升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacamp.com/tutorial/gguf-format-a-complete-guide">GGUF Format : A Complete Guide to Local LLM Inference | DataCamp</a></li>
<li><a href="https://mlx-framework.org/">MLX</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>

</ul>
</details>

**标签**: `#apple-silicon`, `#local-llm`, `#gguf`, `#mlx`, `#inference-engine`

---