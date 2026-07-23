---
layout: default
title: "Horizon Summary: 2026-07-23 (ZH)"
date: 2026-07-23
lang: zh
---

> 从 67 条内容中筛选出 19 条重要资讯。

---

1. [Langfuse 发布 v4.0.0-rc.1，新增 MCP 反馈工具](#item-1) ⭐️ 7.0/10
2. [美国创业公司创始人游说政府勿封禁中国开源权重 AI 模型](#item-2) ⭐️ 7.0/10
3. [500 行裸 C++软渲染器教程](#item-3) ⭐️ 7.0/10
4. [Learn OpenGL：全面的现代 OpenGL 教程资源](#item-4) ⭐️ 7.0/10
5. [天文学家可能发现了首颗系外卫星](#item-5) ⭐️ 7.0/10
6. [DARPA 与美国空军试飞人工智能控制的 F-16 战斗机](#item-6) ⭐️ 7.0/10
7. [2026 年菲尔兹奖](#item-7) ⭐️ 7.0/10
8. [人工智能公司正试图隐瞒巨额债务](#item-8) ⭐️ 7.0/10
9. [OpenAI 在 ChatGPT 中推出健康功能，面向美国用户开放](#item-9) ⭐️ 7.0/10
10. [Nunchaku 4 位扩散模型推理集成至 HuggingFace Diffusers](#item-10) ⭐️ 7.0/10
11. [DeepSeek 创始人四小时投资人会议：AGI 优先于商业化](#item-11) ⭐️ 7.0/10
12. [Apple M5 INT8 激活支持未被利用；自定义内核实现 1.4 倍加速](#item-12) ⭐️ 7.0/10
13. [DeepSeek V4 Flash 通过 Triton 重写 Blackwell 内核在双 4090d 上达到约 105 t/s](#item-13) ⭐️ 7.0/10
14. [Langfuse 发布 v4.0.0-rc.0，引入 ClickHouse 迁移支持](#item-14) ⭐️ 6.0/10
15. [AI 代理与安全漏洞重创 TheNumbers.com：独立数据网站的警示](#item-15) ⭐️ 6.0/10
16. [OpenAI 宣布在乔治亚州启动 Project Camellia 数据中心项目](#item-16) ⭐️ 6.0/10
17. [推进国家科学的新时代](#item-17) ⭐️ 6.0/10
18. [OpenRouter 新增音频转录 API 接口](#item-18) ⭐️ 6.0/10
19. [在 100 美元的 Celeron N5095 单板机上进行 CPU 纯 LLM 推理基准测试](#item-19) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Langfuse 发布 v4.0.0-rc.1，新增 MCP 反馈工具](https://github.com/langfuse/langfuse/releases/tag/v4.0.0-rc.1) ⭐️ 7.0/10

Langfuse 发布了 v4.0.0-rc.1，这是 v4 主版本的候选发布版本。该版本引入了 v4 迁移入口（侧边栏卡片和迁移侧边面板），支持通过公共 API 和新的 MCP 工具提交反馈，并附带多项针对移动端和搜索栏的 UI 改进。 作为最广泛使用的开源 LLM 可观测性平台之一，Langfuse 升级到 v4 主版本预示着重大架构变更，用户需要为此做好准备，应用内提供的迁移入口也将引导用户完成过渡。新增的 MCP 工具集成使 Langfuse 与快速发展的 Model Context Protocol 生态系统接轨，允许 AI 助手以编程方式向 Langfuse 提交反馈。 该版本中的可靠性修复包括提高 PostHog SDK 的 maxQueueSize 以防止静默事件丢失，以及防止 worker 中 PostHog 导出事件丢失。移动端体验也得到优化——Assistant 启动器被提升到顶部栏，traces 工具栏被合并到 Filters 抽屉中。

github · niklassemmler · 7月23日 19:07

**背景**: Langfuse 是一个开源的 LLM 工程平台，为开发者提供针对 AI 应用的可观测性、追踪、评估、提示词管理、实验和人工反馈收集等工具。Model Context Protocol（MCP）由 Anthropic 于 2024 年 11 月推出，是一个开放标准，用于规范 LLM 等 AI 系统与外部工具、系统和数据源的集成方式。这两项技术结合在一起，使 AI 助手能够以编程方式与 Langfuse 等平台交互，例如通过 MCP 暴露的工具直接提交用户反馈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**标签**: `#langfuse`, `#llm-observability`, `#release`, `#mcp`, `#developer-tools`

---

<a id="item-2"></a>
## [美国创业公司创始人游说政府勿封禁中国开源权重 AI 模型](https://www.politico.com/news/2026/07/22/startup-founders-urge-trump-not-to-shut-off-chinese-open-weight-ai-01008992) ⭐️ 7.0/10

美国创业公司创始人通过名为"Little Tech"的倡导组织向特朗普政府递交公开信，恳请政府不要限制中国开源权重 AI 模型的可访问性。此次游说正值财政部长 Scott Bessent 表示政府将调查中国 AI 公司是否不当蒸馏了美国前沿模型之际。 这一政策的走向将重塑全球 AI 竞争格局，决定美国初创企业能否继续使用成本低廉的中国模型，还是被迫进入由少数美国前沿实验室主导的集中化市场。同时也将考验中美科技脱钩的边界——开源权重 AI 是否会沦为这场博弈中的新战场。 开源权重模型仅发布训练好的模型参数供用户微调，并不公开源代码或训练数据，这与完整的开源软件有本质区别。公开信还警告存在"监管俘获"风险，可能进一步固化前沿模型供应商的市场垄断地位；而政府则以蒸馏涉嫌侵犯知识产权为由展开调查，但法律评论者认为，仅凭模型输出就认定侵犯知识产权缺乏先例支撑。

hackernews · theanonymousone · 7月23日 15:18 · [社区讨论](https://news.ycombinator.com/item?id=49023016)

**背景**: 开源权重 AI 模型介于完全封闭的专有系统（仅有提供商可运行）和完全开源软件（公开源代码与训练数据）之间。发布权重允许任何人下载、微调并在本地部署模型，这使得 Zhipu（Z.ai）等中国实验室的模型在寻求低成本替代方案的初创企业中颇受欢迎。"前沿 AI 模型"指的是由资金充裕的实验室（如 OpenAI、Anthropic、Google DeepMind 及中国主要竞品）开发的最先进系统，具备智能体和工具调用能力。中美科技竞争此前已对先进芯片实施出口管制，如今正扩展到模型权重本身是否应被视为受管制技术的讨论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.businessinsider.com/china-ai-boom-terrible-business-open-weight-models-2026-7">Why China's ' Open ' AI Boom Is a Terrible Business - Business Insi...</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/frontier-models/">What Are Frontier AI Models and How They Work | NVIDIA Glossary</a></li>
<li><a href="https://a2dgc.com/the-open-weight-language-model/">The Open Weight Language Model - A2DGC</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍支持创业公司创始人的立场，但在具体细节上存在分歧：部分人质疑封禁中国模型是否能实现其声称的安全目标，因为恶意行为者无论如何都会绕过限制。其他人则围绕"蒸馏等于侵犯知识产权"的法律依据展开辩论，认为模型输出本身不受知识产权法保护，唯一站得住脚的理由只是违反服务条款。反复出现的主题是担忧少数"估值过高"的美国前沿模型供应商实施监管俘获，有人呼吁将此事提交 FTC 或法院审理。怀疑论者指出，创业公司创始人缺乏大型科技公司的政治影响力；而政府的批评者则认为，这场政策辩论暴露出对底层技术的根本性误解。

**标签**: `#AI policy`, `#open-source AI`, `#US-China tech relations`, `#AI regulation`, `#startups`

---

<a id="item-3"></a>
## [500 行裸 C++软渲染器教程](https://haqr.eu/tinyrenderer/) ⭐️ 7.0/10

一个名为"500 行裸 C++软渲染"的教程带领读者使用极简的 C++代码（不依赖外部库）从头构建一个完整的软渲染器。该帖在 Hacker News 上获得了大量讨论，成员分享了 Rust 移植版本、像素化着色器和色差等额外视觉效果，并指出教程遗漏了三角形裁剪等技术主题。 这个资源为理解计算机图形学基础提供了一个易于上手的学习入口，无需面对现代 GPU API 的抽象层。它帮助开发者建立对渲染管线内部真实运作过程的直觉，而随着硬件 API 变得越来越不透明，这类知识正变得越来越稀缺。 该教程被称为"裸 C++"，意味着它避免使用外部库或框架，纯粹专注于线段光栅化、三角形填充和纹理映射等核心渲染算法。值得注意的是，原教程似乎省略了针对视锥体的三角形裁剪，有经验的评论者指出这是任何实用渲染器的关键缺口。

hackernews · mpweiher · 7月23日 14:17 · [社区讨论](https://news.ycombinator.com/item?id=49022038)

**背景**: 软渲染指的是在 CPU 上执行所有渲染计算，而不是依赖 GPU。虽然现代应用出于性能考虑几乎普遍使用硬件加速的 GPU 渲染，但软渲染在教育、嵌入式系统以及无法访问 GPU 的情况下仍然具有价值。这里的"裸 C++"意味着编写代码时不使用外部图形或实用库，迫使程序员从基本线段绘制、三角形光栅化到光照和纹理采样的每一个算法都从原理出发自行实现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stackoverflow.com/questions/59358538/what-is-the-difference-between-software-rendering-vs-gpu-rendering">What is the difference between software rendering vs . gpu rendering</a></li>
<li><a href="https://softlinked.com/software-fundamentals/is-software-rendering-better-than-gpu-rendering">Is Software Rendering Better Than GPU Rendering ? A Guide</a></li>
<li><a href="https://arobenko.github.io/bare_metal_cpp/">Practical Guide to Bare Metal C++</a></li>

</ul>
</details>

**社区讨论**: 社区的回应热情且富有建设性。一位评论者分享了完整的 Rust 移植版本，并附上额外的视觉效果和开发过程中的截图；另一位推荐了补充资源并链接到自己的软渲染器项目；一位技术导向的评论者指出缺少三角形裁剪是一个重要的遗漏话题。总体情绪是积极的，该教程被誉为一个有趣且有教育意义的练习，不过也有人指出它省略了一些构建真正实用渲染器所需的高级主题。

**标签**: `#computer-graphics`, `#software-rendering`, `#c++`, `#tutorial`, `#education`

---

<a id="item-4"></a>
## [Learn OpenGL：全面的现代 OpenGL 教程资源](https://learnopengl.com/) ⭐️ 7.0/10

Learn OpenGL 是一个全面的免费教程资源，用于学习现代 OpenGL 图形编程，被社区公认为权威的入门首选。

hackernews · ibobev · 7月23日 14:53 · [社区讨论](https://news.ycombinator.com/item?id=49022634)

**标签**: `#opengl`, `#graphics-programming`, `#tutorial`, `#computer-graphics`, `#education`

---

<a id="item-5"></a>
## [天文学家可能发现了首颗系外卫星](https://www.eso.org/public/news/eso2610/) ⭐️ 7.0/10

天文学家报告了可能发现首颗系外卫星的消息，不过学界讨论认为该天体或许应被归类为一个独特的双褐矮星系统的一部分，而非传统意义上的卫星。

hackernews · MarcoDewey · 7月23日 14:02 · [社区讨论](https://news.ycombinator.com/item?id=49021783)

**标签**: `#astronomy`, `#exoplanet`, `#exomoon`, `#brown-dwarf`, `#space-discovery`

---

<a id="item-6"></a>
## [DARPA 与美国空军试飞人工智能控制的 F-16 战斗机](https://www.darpa.mil/news/2026/darpa-us-air-force-fly-ai-controlled-f-16) ⭐️ 7.0/10

DARPA 和美国空军成功试飞了一架由人工智能控制的 F-16 战斗机，展示了一种新型界面，允许飞行员在飞行过程中在人类驾驶和人工智能驾驶之间切换。

hackernews · r2sk5t · 7月23日 13:51 · [社区讨论](https://news.ycombinator.com/item?id=49021597)

**标签**: `#AI`, `#defense`, `#autonomous-systems`, `#aviation`, `#military-technology`

---

<a id="item-7"></a>
## [2026 年菲尔兹奖](https://www.mathunion.org/imu-awards/fields-medal/fields-medals-2026) ⭐️ 7.0/10

2026 年菲尔兹奖得主揭晓，这是数学界最负盛名的奖项，旨在表彰 40 岁以下数学家所做出的杰出贡献。

hackernews · nill0 · 7月23日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=49022137)

**标签**: `#mathematics`, `#fields-medal`, `#academic-awards`, `#pure-math`, `#science-news`

---

<a id="item-8"></a>
## [人工智能公司正试图隐瞒巨额债务](https://futurism.com/artificial-intelligence/ai-companies-hide-debt-off-balance-sheet) ⭐️ 7.0/10

对人工智能公司表外债务的审查,社区讨论这些金额是否真的异常、私人信贷敞口的系统性风险,以及其对人工智能行业的影响。

hackernews · technewssss · 7月23日 13:09 · [社区讨论](https://news.ycombinator.com/item?id=49020999)

**标签**: `#ai-industry`, `#finance`, `#off-balance-sheet-debt`, `#private-credit`, `#tech-economics`

---

<a id="item-9"></a>
## [OpenAI 在 ChatGPT 中推出健康功能，面向美国用户开放](https://openai.com/index/health-in-chatgpt) ⭐️ 7.0/10

OpenAI 已推出 ChatGPT 健康功能（Health in ChatGPT），这是一项新功能，允许符合条件的美国用户安全地连接其医疗记录和 Apple Health 数据，从而获得更个性化的健康洞察并更好地了解自身健康状况。 此次发布标志着 ChatGPT 正式进入受到严格监管的医疗健康领域，在这一领域 AI 的准确性和数据隐私具有重大的现实影响。它将 OpenAI 直接置于与现有健康科技企业的竞争之中，并表明消费级 AI 工具正越来越多地被用于医疗决策辅助。 该功能最初仅限于符合条件的美国用户使用，并强调了对健康数据的隐私保护、安全性和用户控制权。与 Apple Health 的集成使 ChatGPT 能够访问活动、心率及其他可穿戴设备收集的生物特征数据，以及来自医疗服务提供商的临床记录。

rss · OpenAI Blog · 7月23日 00:00

**背景**: Apple Health 是苹果公司的健康数据平台，可从 iPhone、Apple Watch 及连接的三方应用中汇总生物特征和健康数据。医疗 AI 中的病历集成通常依赖于 FHIR（快速医疗互操作性资源）标准，该标准定义了患者状况、检验结果、用药等临床数据在系统间交换的通用结构。像 ChatGPT 这样的大语言模型可以利用 FHIR 格式的数据提供具有上下文感知的回答，但在将通用 AI 应用于医疗信息时，临床准确性和类似 HIPAA 标准的合规性仍是关键挑战。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/health-in-chatgpt/">Launching Health in ChatGPT | OpenAI</a></li>
<li><a href="https://spsoft.com/tech-insights/fhir-llm-applications-in-healthcare/">FHIR LLM In Healthcare - Pros & Implementation Challenges</a></li>
<li><a href="https://www.linkedin.com/pulse/chatgpt-health-here-treat-like-new-front-door-dominic-b2bue">ChatGPT Health Is Here, Treat It Like a New Front Door</a></li>

</ul>
</details>

**社区讨论**: 早期评论认为，ChatGPT 健康功能被视为一个重要的信号而非新鲜事物，因为患者已经在大规模地使用 ChatGPT 来咨询健康问题。观察人士强调，需要清晰的患者教育、明确说明该工具不应被用于哪些场景，并建立毫不含糊的危急症状升级协议，以降低临床风险。

**标签**: `#OpenAI`, `#ChatGPT`, `#healthcare`, `#health-tech`, `#personalization`

---

<a id="item-10"></a>
## [Nunchaku 4 位扩散模型推理集成至 HuggingFace Diffusers](https://huggingface.co/blog/nunchaku-diffusers) ⭐️ 7.0/10

HuggingFace 已将 Nunchaku 的 4 位量化方法集成到其广泛使用的 Diffusers 库中，实现了与架构无关的扩散模型低位推理。配套的 diffuse-compressor 工具包提供了端到端的 SVDQuant 工作流程，涵盖 Diffusers 模型的校准、量化、打包和发布。 Stable Diffusion 等扩散模型需要大量 GPU 内存且推理延迟较高，限制了它们在消费级硬件上的部署。通过将权重和激活值都降至 4 位精度（W4A4），Nunchaku 在保持视觉保真度的同时大幅降低了内存需求，使在更易获取的硬件上运行先进的扩散模型成为可能。 Nunchaku 实现了 SVDQuant——一种源自 MIT 和 NVIDIA 研究的训练后量化技术，通过低秩分量吸收激活值中的异常值，从而实现真正的 W4A4（4 位权重和 4 位激活值），而不仅仅是权重量化。该集成利用 Nunchaku 的融合低位内核来加速推理，diffuse-compressor 工具包则简化了从全精度模型到可部署量化产物的完整流程。

rss · HuggingFace Blog · 7月23日 00:00

**背景**: 扩散模型是通过迭代去噪随机噪声来生成图像、音频或视频的生成式 AI 系统，是 Stable Diffusion 等流行工具的基础。量化是一种模型压缩技术，通过降低模型参数的数值精度（例如从 16 位降至 4 位）来减少内存使用并通常加快计算速度。SVDQuant 是一种特定的训练后量化方法，它解决了 4 位量化中的关键挑战——处理通常会导致严重质量下降的异常激活值——其做法是将这些异常值吸收到低秩分量中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/huggingface/blog/blob/main/nunchaku-diffusers.md">blog/ nunchaku -diffusers.md at main · huggingface/blog · GitHub</a></li>
<li><a href="https://deepwiki.com/nunchaku-ai/nunchaku">nunchaku -ai/ nunchaku | DeepWiki</a></li>
<li><a href="https://research.nvidia.com/labs/eai/publication/svdquant/">SVDQuant : Absorbing Outliers by Low-Rank Components for 4-Bit...</a></li>

</ul>
</details>

**标签**: `#diffusion-models`, `#quantization`, `#huggingface`, `#inference-optimization`, `#stable-diffusion`

---

<a id="item-11"></a>
## [DeepSeek 创始人四小时投资人会议：AGI 优先于商业化](https://www.reddit.com/r/LocalLLaMA/comments/1v49lxp/deepseek_founders_4hour_investor_meeting_deepseek/) ⭐️ 7.0/10

DeepSeek 创始人梁文锋在一场长达四小时的投资人会议上透露，公司的核心目标是实现 AGI（通用人工智能），而非追求用户增长、商业化或打造下一个超级应用，他将"克制"定义为一种深思熟虑的战略选择。 这一立场与 OpenAI、Anthropic 和 Google 等积极追求企业收入和消费级产品的西方 AI 实验室形成鲜明对比。作为以 R1 等具有竞争力的开源权重模型著称的最具影响力的中国 AI 实验室之一，DeepSeek 将长期 AGI 研究置于近期变现之上的优先排序，可能重塑业界对中国头部 AI 参与者战略角色的预期。 梁文锋表示中美 AI 之间的差距主要是资源差距，DeepSeek 之所以训练当前规模的模型，完全是因为受到资源限制——并非因为他们认为这个规模已经足够。他还强调，开源发布的模型与 DeepSeek 内部部署的模型完全一致，不存在"公开较差、内部更好"的双轨做法，并列出 AGI、团队稳定性以及"克制"为唯一不可妥协的优先事项。

reddit · r/LocalLLaMA · /u/MagicZhang · 7月23日 10:09

**背景**: DeepSeek 是一家总部位于杭州的中国 AI 公司，于 2025 年 1 月因其 R1 模型可与西方领先系统相媲美并引发美国科技股大规模抛售而声名鹊起。通用人工智能（AGI）指的是一种假设性的 AI 系统，能够在几乎所有认知任务上匹敌或超越人类能力——这是各大实验室都在追求的目标，但业界对其时间线和可行性并无共识。DeepSeek 通过发布具有竞争力的开源权重模型而脱颖而出，同时据报道以较低的开销和相对较小的研究导向团队运作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Artificial_general_intelligence">Artificial general intelligence - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/articles/c5yv5976z9po">What is DeepSeek - and why is everyone talking about it?</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AGI`, `#open-source`, `#AI-strategy`, `#industry-news`

---

<a id="item-12"></a>
## [Apple M5 INT8 激活支持未被利用；自定义内核实现 1.4 倍加速](https://www.reddit.com/r/LocalLLaMA/comments/1v4iw0n/apple_m5_isnt_making_full_use_of_its_matmul_cores/) ⭐️ 7.0/10

一位开发者为 Apple M5 构建了自定义的 w8a8（8 位权重、8 位激活）内核，在 M5 MacBook Air 上运行 Gemma4 prefill 任务实现了 1.4 倍加速（在 130,173 个输入 token 上从 2193 tps 提升至 3029 tps），在小上下文长度下接近 10k tps。尽管 M5 芯片原生支持 INT8 激活（包括 w4a8 d_type），但当前的 MLX 和 Llama.cpp 等推理框架仍全部使用 16 位激活。 这一发现表明，主流的 Apple Silicon 推理框架由于未启用 M5 原生的 INT8 matmul 能力，正在损失显著的性能，这对在 Mac 上运行本地大语言模型的用户有直接影响。它为框架维护者（MLX、Llama.cpp）提供了清晰的路线图来解锁可观的加速效果，并证明在 Apple Silicon 上的底层内核优化能够带来类似 CUDA 生态中已有的实际收益。 这些内核采用 w8a8（8 位权重、8 位激活）方案，而 M5 同时还支持 w4a8 模式；INT8 GEMM 通过 per-tensor 缩放将权重和激活映射到 8 位整数。加速效果在小上下文长度下最为显著，因为 prefill 在此时对延迟最敏感，随着上下文超过测试的 130k token 负载，加速幅度会逐渐减小。

reddit · r/LocalLLaMA · /u/maddie-lovelace · 7月23日 16:28

**背景**: 大语言模型推理包含两个阶段：prefill 一次性处理整个输入提示以填充 KV 缓存，decode 则逐个生成输出 token。Prefill 通常是计算密集型的，最受益于原始 matmul 吞吐量，因此成为量化优化的主要目标。量化方案以 W{权重位数}A{激活位数} 命名，因此 W8A8 表示 8 位权重和 8 位激活，而 W4A8 则使用 4 位权重配合 8 位激活。Apple Silicon 较新的代次（M3/M4/M5）包含专用的 matmul/神经网络加速器硬件，能够原生执行低精度整数运算，但要真正获得这些加速，推理框架必须显式地针对这些数据类型进行优化，而不是默认使用 16 位浮点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wesbrown18.medium.com/the-rtx-spark-is-not-an-apple-silicon-competitor-6789ca8452ff">The RTX Spark Is Not an Apple Silicon Competitor | Medium</a></li>
<li><a href="https://redis.io/blog/prefill-vs-decode/">Prefill vs Decode : LLM Inference Phases Explained</a></li>
<li><a href="https://www.emergentmind.com/topics/w8a8-per-tensor-static-quantization">W 8 A 8 Static Quantization in Neural Networks</a></li>

</ul>
</details>

**标签**: `#apple-silicon`, `#mlx`, `#quantization`, `#kernel-optimization`, `#local-llm`

---

<a id="item-13"></a>
## [DeepSeek V4 Flash 通过 Triton 重写 Blackwell 内核在双 4090d 上达到约 105 t/s](https://www.reddit.com/r/LocalLLaMA/comments/1v4n8wj/deepseek_v4_flash_105_ts_on_two_nvidia_4090d_48g/) ⭐️ 7.0/10

开发者使用 Triton 重新实现了 DeepSeek 仅支持 Blackwell 的内核（包括 DeepGEMM、FlashInfer sparse-MLA 和 block-scaled FP8），将其移植到 sm89（Ada）架构，使 DeepSeek V4 Flash 能够在两张 RTX 4090d 48G GPU 上运行，并通过 vLLM 达到约 105 tokens/秒的速度，相比 llama.cpp 在并行代理工作流中提升 2–3 倍。 这项工作使得在最先进 DeepSeek 模型上运行不再局限于 Blackwell 硬件，可以在更普及且更便宜的 Ada 时代显卡上完成，显著降低了本地高吞吐量推理的门槛。 模型被压缩到约 IQ2-XXS 量化以适配 96 GB 总显存（一次性过程最长约 60 分钟），两张 GPU 之间的 P2P 通信通过修补版 open-gpu-kernel-modules 驱动（595.71.05-p2p-48g）启用，并使用定制的 vLLM-Moet Docker 镜像（Dockerfile.sm89-v0251），配置张量并行 TP=2、MTP_TOKENS=1 和 FORCE_RESIDENT=1，实现了 262k 上下文窗口，并发性能优于 llama.cpp。

reddit · r/LocalLLaMA · /u/iSevenDays · 7月23日 19:01

**背景**: Nvidia 的 Ada Lovelace 架构（如 RTX 4090，sm89）早于新一代 Blackwell 架构（sm100/sm120），并且原生不支持现代前沿大模型使用的多项高级特性：DeepGEMM 是一个支持 FP8/BF16 的高性能 tensor core 内核库，集成了融合 MoE 和 MQA 等基础算子；FlashInfer sparse-MLA 支持 DeepSeek 的多头潜在注意力（Multi-head Latent Attention）机制，该机制将 KV 缓存压缩为低秩潜在向量以实现内存高效推理；block-scaled FP8 使用逐块缩放因子（而非逐张量）以在低精度下保持精度。由于这些内核仅针对 Blackwell 编写，Ada 硬件用户无法使用优化版的 DeepSeek 推理，直到此次 Triton 重写弥补了这一空白。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/deepseek-ai/DeepGEMM">GitHub - deepseek-ai/ DeepGEMM : DeepGEMM : clean and efficient...</a></li>
<li><a href="https://liorsinai.github.io/machine-learning/2025/02/22/mla.html">DeepSeek 's Multi - Head Latent Attention - Lior Sinai</a></li>
<li><a href="https://ralphmao.github.io/quantization/">A Dive into LLM Quantization – Huizi Mao</a></li>

</ul>
</details>

**标签**: `#deepseek`, `#vllm`, `#triton`, `#nvidia-ada`, `#kernel-optimization`, `#quantization`

---

<a id="item-14"></a>
## [Langfuse 发布 v4.0.0-rc.0，引入 ClickHouse 迁移支持](https://github.com/langfuse/langfuse/releases/tag/v4.0.0-rc.0) ⭐️ 6.0/10

Langfuse 发布了 v4.0.0-rc.0，这是其新主版本的预发布版本，相较 v3 引入了破坏性变更，包括默认环境变量和 ClickHouse 迁移，以支持自托管 v4 部署。该版本包含多项新功能（在 PR 预览上启用云端 AI 功能、OpenTelemetry 媒体字节支持、为 Ask AI 功能使用托管 Langfuse 提示词）以及修复（安全凭证遮罩、移动端体验改进、数据集运行处理）。 对于众多自托管 Langfuse 以实现 LLM 可观测性的团队而言，这意义重大，因为它预示着一项重大的架构转变即将到来，需要仔细规划迁移。使用 ClickHouse 作为核心分析存储表明 Langfuse 正在扩展其数据层，以应对生产环境 LLM 应用中高吞吐量的追踪和评估工作负载。 作者明确建议在稳定版本发布之前，暂缓在生产环境中进行 v3 到 v4 的迁移，不过全新部署被描述为经过充分测试。值得注意的变更包括：将事件表提升到 ClickHouse 迁移路径、启用 v4 环境默认值、为旧版 API 端点添加对智能体友好的弃用响应，以及修复 OpenTelemetry 仪表化中的 Python 字节流媒体解码问题。

github · Steffen911 · 7月23日 15:53

**背景**: Langfuse 是一个开源的 LLM 工程平台，为构建大语言模型应用的团队提供可观测性、追踪、提示词管理、评估和实验工具。ClickHouse 是一个面向大规模数据集实时分析设计的列式开源数据库，非常适合用于高吞吐量的追踪和事件存储。像 Langfuse 这样的 LLM 可观测性平台通过收集模型调用中的追踪、Span 和评估数据，帮助开发人员调试、监控和改进 AI 应用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://langfuse.com/">Langfuse</a></li>
<li><a href="https://clickhouse.com/docs/intro">What is ClickHouse ? | ClickHouse Docs</a></li>
<li><a href="https://signoz.io/blog/llm-observability/">Understanding LLM Observability - Key Insights, Best... | SigNoz</a></li>

</ul>
</details>

**标签**: `#langfuse`, `#llm-observability`, `#release`, `#self-hosting`, `#migration`

---

<a id="item-15"></a>
## [AI 代理与安全漏洞重创 TheNumbers.com：独立数据网站的警示](https://stephenfollows.com/p/what-just-happened-to-thenumberscom-should-worry-us-all) ⭐️ 6.0/10

长期运营的独立电影数据网站 TheNumbers.com 丢失了大量数据并丧失部分功能，相关分析文章调查了激进的 AI 代理爬取行为与潜在安全漏洞是否是导致该网站退化的原因。 这一案例揭示了自主 AI 浏览代理的大规模出现如何压垮或攻击小型独立运营的公共数据网站，威胁到现代互联网所依赖的、由广告或捐赠资助的细分领域独立资源。 文章推测攻击者可能利用了潜在的漏洞来获取特权数据访问权限（可能是为了在票房预测市场中获得优势），随后该网站以数据大幅缩减、设计简化的形式重新上线。

hackernews · nickthegreek · 7月23日 16:53 · [社区讨论](https://news.ycombinator.com/item?id=49024691)

**背景**: AI 代理是可以自主浏览网页、点击链接、填写表单并提取信息的软件程序，只需极少的人工监督。browser-use、Crawl4AI 以及各种由大语言模型驱动的爬虫工具使得大规模、类人化的浏览变得轻而易举。TheNumbers.com 是一个提供电影预算、票房和票房收入统计数据的免费公开数据库——这类细分领域的参考网站历来依靠捐赠、广告或运营者的热情维持运营，而非机构资金支持。当 AI 代理开始大规模访问其接口或探测漏洞时，这类没有企业级安全预算的网站尤其脆弱。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://voidmob.com/blog/how-to-build-web-scraping-ai-agent">How to Build Web Scraping AI Agent : Scrape Any... | VoidMob Blog</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍将此事件视为一个警示故事：primitivesuave 分享了运营类似公共 COVID 贷款数据集网站在经济上不可持续的经历；ethagnawl 建议使用静态站点生成器配合具备反机器人能力的 CDN 作为可行的缓解方案；abetusk 强调核心问题更可能是对安全漏洞的恶意利用（与预测市场的利益动机相关），而不仅仅是流量压力；podgietaru 则提出了更广泛的担忧——部分运营者可能会故意降低免费服务的质量，以推动用户转向付费产品。

**标签**: `#ai-agents`, `#web-scraping`, `#data-sites`, `#site-security`, `#internet-ecosystem`

---

<a id="item-16"></a>
## [OpenAI 宣布在乔治亚州启动 Project Camellia 数据中心项目](https://openai.com/index/building-ai-infrastructure-with-the-effingham-county-community) ⭐️ 6.0/10

OpenAI 宣布了在乔治亚州 Effingham 县的长期 AI 基础设施项目 Project Camellia，与 Georgia Power 签约获取 3.2 吉瓦电力，预计将在 2028 年至 2032 年间分阶段交付，并承诺进行社区投资、创造就业机会以及提供 Codex 的访问权限。 3.2 吉瓦的电力承诺使 Project Camellia 成为迄今为止已公布的最大的 AI 基础设施项目之一，标志着 OpenAI 在算力需求持续增长背景下的巨大扩展雄心。强调非补贴能源成本和社区福利为 AI 公司如何应对当地对电力消耗和经济影响的关切树立了潜在的样板。 OpenAI 承诺全额承担基础设施和电力服务的费用，这意味着乔治亚州的电力用户将不会补贴该项目。3.2 吉瓦的容量将在 2028 年至 2032 年间分阶段交付，OpenAI 还向社区提供其能够读写和执行代码的智能编程系统 Codex 的访问权限。

rss · OpenAI Blog · 7月22日 13:00

**背景**: Project Camellia 是一个超大规模数据中心园区，旨在容纳训练和运行 GPT-4 等大型 AI 模型所需的庞大 GPU 集群。3.2 吉瓦是一个巨大的电力规模——大约相当于三座大型核反应堆的输出——凸显了前沿 AI 开发对能源需求的不断升级。OpenAI 的 Codex 是一款能够自主读取、编写和执行代码以辅助开发人员的智能编程工具。位于乔治亚州海岸萨凡纳附近的 Effingham 县一直致力于将其打造为数据中心发展中心，因为那里有可用的土地和电力基础设施。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://projectcamellia.com/">Project Camellia</a></li>
<li><a href="https://openai.com/index/building-ai-infrastructure-with-the-effingham-county-community/">Building AI infrastructure with the Effingham County ... | OpenAI</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI infrastructure`, `#data centers`, `#Project Camellia`, `#Codex`

---

<a id="item-17"></a>
## [推进国家科学的新时代](https://openai.com/index/advancing-the-next-era-of-national-science) ⭐️ 6.0/10

OpenAI 宣布致力于与美国能源部及国家实验室合作，应用前沿 AI 加速科学发现。

rss · OpenAI Blog · 7月22日 12:00

**标签**: `#OpenAI`, `#national-science`, `#government-partnership`, `#AI-research`, `#scientific-discovery`

---

<a id="item-18"></a>
## [OpenRouter 新增音频转录 API 接口](https://openrouter.ai/blog/tutorials/transcription-on-openrouter/) ⭐️ 6.0/10

OpenRouter 推出了音频转录功能，开发者可以将 base64 编码的音频发送到 POST /api/v1/audio/transcriptions 端点，并使用现有的 OpenRouter API 密钥获取包含文本内容和用量信息的 JSON 响应。 这一更新将 OpenRouter 的统一 API 网关能力从聊天补全扩展到了语音转文本工作流，使开发者能够在现有管线中集成转录功能，而无需为每个底层语音模型单独管理供应商凭证或 SDK。 音频必须以 base64 编码形式放入请求体中，响应会同时返回转录文本和用于成本追踪的用量对象。该端点与 OpenRouter 其他 API 共享同一认证机制，简化了密钥管理，但开发者在设计集成方案时需注意文件大小限制和所支持的音频格式。

rss · OpenRouter Blog · 7月22日 00:00

**背景**: OpenRouter 是一个 AI 模型聚合平台，提供与 OpenAI Chat Completions 格式兼容的统一 API 接口，可标准化访问 OpenAI、Anthropic、Google、Meta 等供应商的 400 多个模型。Base64 编码是一种常用的技术，用于在 JSON 请求中嵌入音频等二进制数据，因为 JSON 本身只支持文本格式。通过采用这一模式，OpenRouter 复刻了 OpenAI 自身音频转录 API 的设计，使得已经熟悉该生态的开发者能够轻松采用新端点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/models">Compare AI Models : Pricing, Context & Benchmarks | OpenRouter</a></li>
<li><a href="https://developer.puter.com/encyclopedia/openrouter/">OpenRouter</a></li>
<li><a href="https://pkg.go.dev/github.com/hra42/openrouter-go/examples/audio-inputs">audio -inputs command...</a></li>

</ul>
</details>

**标签**: `#openrouter`, `#api`, `#speech-to-text`, `#transcription`, `#developer-tools`

---

<a id="item-19"></a>
## [在 100 美元的 Celeron N5095 单板机上进行 CPU 纯 LLM 推理基准测试](https://www.reddit.com/r/LocalLLaMA/comments/1v4lgo3/cpuonly_inference_on_a_celeron_n5095_sbc_6_models/) ⭐️ 6.0/10

一位用户在搭载 Intel Celeron N5095（Jasper Lake，4 核 4 线程，15W）、配备 16GB 内存的优奕拓 Youyeetoo X1S 单板机（售价 100–130 美元）上，通过 Ollama 以纯 CPU 方式对六个开源 LLM（参数量从 0.6B 到 8B）进行了基准测试。Qwen3 0.6B 平均达到 6.788 tok/s，仍可交互使用；而 8B 模型降至 0.924 tok/s；15 分钟满载压力测试平均温度 74.66°C，峰值 77°C，未出现降频。 该基准测试表明，超低价（100–130 美元）的 x86 单板机已具备本地运行小型 LLM 的能力，可用于分类、路由、摘要等轻量任务，有望替代部分付费 API 调用。它同时揭示了 15W 以下 CPU 的实际性能上限——8B 模型遇到的是内存带宽瓶颈而非容量限制，这对考虑在廉价硬件上部署边缘 AI 的用户具有参考价值。 尽管 Ollama 检测到了 Jasper Lake 的核显，但仍自动选择了 CPU 后端，因此所有数据均为纯 CPU 推理结果。作者指出 8B 模型的瓶颈在于内存带宽而非内存容量——模型能在 16GB 系统上加载运行，但在低于 1 tok/s 的速度下基本不可用。作者计划后续使用 llama.cpp 配合 Vulkan 在 Jasper Lake 核显上进行 CPU 与 GPU 的对比测试。

reddit · r/LocalLLaMA · /u/tre7744 · 7月23日 17:59

**背景**: Ollama 是基于 llama.cpp 构建的开源运行时，可简化本地 LLM 的下载与运行流程，同时支持 CPU 和 GPU 后端。Intel Celeron N5095 是一款低功耗 Jasper Lake 处理器，具有 4 核 4 线程、15W TDP 以及集成 UHD 核显，常见于售价低于 150 美元的廉价迷你主机和单板机。Qwen3 是阿里巴巴开源的 LLM 系列，其中 0.6B 是该系列中最小的稠密模型之一，适合设备端的轻量任务。"SBC"（单板机）指的是体积小巧的 x86 或 ARM 开发板（如树莓派），常用于嵌入式或爱好者项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@techwithpraisejames/how-to-run-llms-locally-with-ollama-and-docker-model-runner-a-complete-guide-for-developers-ffa56b59d299">How to run LLMs locally with Ollama and Docker Model... | Medium</a></li>
<li><a href="https://www.cpu-world.com/CPUs/Celeron/Intel-Mobile+Celeron+N5095.html">Intel Celeron N 5095 - DC8069704609810</a></li>
<li><a href="https://github.com/QwenLM/Qwen3">GitHub - QwenLM/ Qwen 3 : Qwen 3 is the large language model series...</a></li>

</ul>
</details>

**标签**: `#local-llm`, `#cpu-inference`, `#ollama`, `#benchmark`, `#edge-computing`

---