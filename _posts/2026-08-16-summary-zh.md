---
layout: default
title: "Horizon Summary: 2026-08-16 (ZH)"
date: 2026-08-16
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [Anthropic 公开 Claude 系统提示词及版本演进记录](#item-1) ⭐️ 7.0/10
2. [美国国立卫生研究院将终止一项面向临床研究新人的重要资助](#item-2) ⭐️ 7.0/10
3. [Cloudflare 向所有使用其域名服务器的用户静默注入分析 JavaScript](#item-3) ⭐️ 7.0/10
4. [AI 改写工具导致学术论文中充斥"被折磨的短语"](#item-4) ⭐️ 7.0/10
5. [重审高效通道注意力论文（2019 年，引用量 12000 次）——其核心假设并不完全正确 (D)](#item-5) ⭐️ 7.0/10
6. [第三世界嵌入式工程师为 RISC-V 的发展中国家价值辩护](#item-6) ⭐️ 6.0/10
7. [AI 模型正在主动减少记忆的知识](#item-7) ⭐️ 6.0/10
8. [线性注意力在 DNA 建模中的长程召回能力不足](#item-8) ⭐️ 6.0/10
9. [适者生存：Qwen3.6-27B 的雅可比透镜无需重新拟合即可读取和引导 Qwen3.8-27B](#item-9) ⭐️ 6.0/10
10. [BDH-CQ：用于上下文学习的循环潜在推理系统](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Anthropic 公开 Claude 系统提示词及版本演进记录](https://platform.claude.com/docs/en/release-notes/system-prompts) ⭐️ 7.0/10

Anthropic 正式发布了记录各版本 Claude 模型系统提示词的发布说明，使公众可以追踪提示词的演变过程。社区成员 Simon Willison 构建了一个基于 Git 提交历史的工具，可以对比 Opus 4.8 与 Opus 5（代号 Fable 5 和 Mythos 5）等版本之间的提示词差异，使行为设计决策变得可审查。 系统提示词是塑造 Claude 行为的主要机制，将其公开使研究人员、开发者和竞争对手能够以前所未有的视角了解 Anthropic 的对齐和安全策略。这种透明度水平在前沿 AI 实验室中极为罕见，可能会影响围绕披露模型行为塑造技术的行业规范。 提示词中包含行为准则，例如在用户处于困境或表达痛苦时优先考虑用户福祉而非完成任务，以及诸如验证图片是否实际上传等基本常识检查。Simon Willison 的 diff 工具显示，即使是像 Opus 4.8 这样强大的模型，Anthropic 仍然依赖系统提示词来处理简单的检查，一位评论者认为这暗示了在该类边缘场景中模型并未被视为具有强通用智能。

hackernews · tosh · 8月16日 12:48 · [社区讨论](https://news.ycombinator.com/item?id=49319556)

**背景**: 系统提示词是附加在每次与大语言模型对话开头的隐藏指令集，用于设定上下文、语气和行为约束。Anthropic 是一家由前 OpenAI 研究人员创立的 AI 安全与研究公司，专注于构建可靠、可解释且可操控的 AI 系统。公开系统提示词符合 Anthropic 所倡导的透明度理念，帮助外部研究人员审查对齐决策，而不仅仅依赖公司的自我报告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://platform.claude.com/docs/en/release-notes/system-prompts">System Prompts - Claude Platform Docs</a></li>
<li><a href="https://github.com/Piebald-AI/claude-code-system-prompts">GitHub - Piebald-AI/claude-code-system-prompts: All parts of Claude Code's system prompt, 27 builtin tool descriptions, sub agent prompts (Plan/Explore/Task), utility prompts (CLAUDE.md, compact, statusline, magic docs, WebFetch, Bash cmd, security review, agent creation). Updated for each Claude Code version. · GitHub</a></li>
<li><a href="https://www.anthropic.com/company">Company \ Anthropic</a></li>

</ul>
</details>

**社区讨论**: 讨论内容具有实质性的技术深度。Simon Willison 贡献了通过 Git 提交来追踪提示词演变的工具，trjordan 则对困境处理指令如何作为嵌入提示文本中的软性策略杠杆进行了细致分析。ololobus 质疑依赖系统提示词来处理基本检查（如验证图片上传）是否反映了 Anthropic 在概念化模型智能方面的局限。quaintdev 发表的另一段离题帖子则声称该论坛正在压制关于 AI 的负面报道。

**标签**: `#AI`, `#Claude`, `#Anthropic`, `#system-prompts`, `#AI-safety`, `#transparency`

---

<a id="item-2"></a>
## [美国国立卫生研究院将终止一项面向临床研究新人的重要资助](https://www.science.org/content/article/nih-ending-key-grant-budding-clinical-researchers) ⭐️ 7.0/10

美国国立卫生研究院正终止一项支持早期职业临床研究者的重要资助项目，引发了人们对美国医学研究可能出现代际人才流失的担忧。

hackernews · brandonb · 8月16日 16:14 · [社区讨论](https://news.ycombinator.com/item?id=49321353)

**标签**: `#NIH`, `#research-funding`, `#clinical-research`, `#science-policy`, `#US-research`

---

<a id="item-3"></a>
## [Cloudflare 向所有使用其域名服务器的用户静默注入分析 JavaScript](https://news.ycombinator.com/item?id=49322107) ⭐️ 7.0/10

一位用户发现，在将自己的域名服务器切换到 Cloudflare 以启用 R2 存储桶服务后，Cloudflare 静默地向其一个不包含 JavaScript 的纯 HTML 网站注入了 Web Analytics JavaScript 信标（来自 static.cloudflareinsights.com 的 beacon.min.js）。用户必须在 Analytics 控制台中主动选择退出，而非默认开启。 这一行为引发了严重的隐私和信任问题，因为明确维护无 JavaScript 网站的站主，其网站在未经同意的情况下被注入了代码，可能违反了站主向其用户做出的不进行追踪的承诺。它还涉及法律层面的问题——Cloudflare 对其并未托管的域名的 HTTP 响应进行了修改，部分评论者认为这可能构成未经授权的访问，违反《计算机欺诈与滥用法案》（CFAA）等相关法律。 被注入的脚本从 static.cloudflareinsights.com/beacon.min.js 加载，带有包含 token 和版本号（如 2024.11.0）的 data-cf-beacon 属性。注入发生在 CDN/反向代理层面，对经过 Cloudflare 反向代理的 HTML 响应进行修改，这正是不托管站点的 Cloudflare 仍然能够向 HTTPS 网站注入代码的原因。

hackernews · stagas · 8月16日 17:49

**背景**: Cloudflare 是主流的 CDN 和 DNS 服务提供商；将域名服务器切换到 Cloudflare 后，域名的 DNS 查询会经过其基础设施路由，同时可能激活其反向代理功能。Web Analytics（基于 Real User Monitoring，即 RUM 构建）是 Cloudflare 的隐私导向分析产品，传统上需要用户自行添加 JavaScript 代码片段——但该公司似乎对所有经过代理的域名自动注入了该脚本。CSP（内容安全策略）是浏览器提供的一种机制，允许网站所有者设置允许执行的脚本来源白名单，可以用来阻止被注入的第三方脚本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://burgeonlab.com/blog/cloudflare-web-analytics-rum-injected-tracking-beacon-script-into-my-sites/">Cloudflare Auto Injected Tracking Scripts To My Sites</a></li>
<li><a href="https://unwrite.co/blog/cloudflare-hardening-zero-client-javascript/">Zero client-side JavaScript from your CDN: a Cloudflare ... | Unwrite</a></li>
<li><a href="https://developers.cloudflare.com/r2/">Overview · Cloudflare R2 docs</a></li>

</ul>
</details>

**社区讨论**: 社区对此表示担忧并确认了这一行为：purpleidea 分享了他们观察到的完整 beacon.min.js 代码片段，dchest 链接到 Cloudflare 官方的 Web Analytics 博客文章（《The RUM Diaries》），okzgn 建议使用 CSP meta 标签来阻止未授权的脚本，Animats 则提出了法律层面的质疑——对于 Cloudflare 并未托管的站点，向其 HTTPS 响应中注入代码是否构成《计算机欺诈与滥用法案》（CFAA）下的未经授权访问。

**标签**: `#cloudflare`, `#privacy`, `#web-security`, `#analytics`, `#nameservers`

---

<a id="item-4"></a>
## [AI 改写工具导致学术论文中充斥"被折磨的短语"](https://scholar.google.com/scholar?q=%22kidney+disappointment%22) ⭐️ 7.0/10

知名科学期刊的学术论文中越来越多地充斥着荒谬的"被折磨的短语"（tortured phrases），例如将"kidney failure"（肾衰竭）写成"kidney disappointment"，将"neural networks"（神经网络）写成"fake neural organizations"。这些混乱的术语可能由 AI 驱动的改写或翻译工具产生，目的是规避抄袭检测，暴露了科学出版领域的严重诚信问题。 这一现象削弱了同行评审科学文献的可信度和可靠性，可能使有缺陷或欺诈性的研究通过审查流程。它影响到依赖准确科学文献进行决策的研究人员、临床医生和政策制定者，并凸显了改进检测方法和加强编辑监督的迫切需求。 该现象已通过"Problematic Paper Screener"（问题论文筛查器）被系统地记录和追踪，该工具可扫描已发表论文中的数千个被折磨的短语。有证据表明这种现象可能早于现代大语言模型出现——2021 年的一篇论文已包含"kidney disappointment"这一表述，这引发了关于翻译误差、前 LLM 改写软件还是论文工厂是主要原因的疑问。

hackernews · Alifatisk · 8月16日 12:22 · [社区讨论](https://news.ycombinator.com/item?id=49319389)

**背景**: "被折磨的短语"（tortured phrases）是指用荒谬或无意义的词语替换标准技术术语的现象，通常产生于文本通过不完善的改写或翻译算法处理的过程。AI 改写工具在试图绕过 Turnitin 等抄袭检测软件的研究人员中日渐流行，但它们往往会对既有的专业术语产生错误的表述。该概念由网络安全研究员 Cyril Labbé大力推广，他在已发表的科学文献中发现了数千个此类短语。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://link.springer.com/article/10.1186/s43067-025-00219-8">‘Tortured phrases’ in artificial intelligence (AI) literature ...</a></li>
<li><a href="https://proofreaderpro.ai/blog/tortured-phrases-paper-mill-detection">\"Tortured Phrases\": Why Bad Paraphrasers Get Papers ...</a></li>
<li><a href="https://www.turnitin.com/blog/what-are-ai-plagiarism-changers-and-how-do-they-work-what-administrators-need-to-know">AI plagiarism changers: What administrators need to know</a></li>

</ul>
</details>

**社区讨论**: 社区讨论探讨了该现象的多种可能解释：故意改写以规避抄袭检测、非英语母语作者造成的翻译问题（有评论者将其类比为老旧俄罗斯工程文献中将"hydraulic ram"翻译成"water goat"的现象），以及 AI 生成。有评论者发现 2021 年的论文就已使用"kidney disappointment"，鉴于当时现有的大语言模型尚未出现，这挑战了 AI 生成假说。另一位评论者则突出展示了一个特别惊人的例子：某化学论文将"the final solution"改写成了"the mass killing of an ethnic group"。

**标签**: `#scientific-publishing`, `#academic-integrity`, `#ai-paraphrasing`, `#plagiarism-detection`, `#tortured-phrases`

---

<a id="item-5"></a>
## [重审高效通道注意力论文（2019 年，引用量 12000 次）——其核心假设并不完全正确 (D)](https://www.reddit.com/r/MachineLearning/comments/1vptaw9/revisiting_the_efficient_channel_attention_paper/) ⭐️ 7.0/10

本文对《高效通道注意力》（ECA）论文进行了概念性批判，指出其设计原理存在缺陷：沿通道维度的一维卷积缺乏能够证明卷积运算合理性的拓扑结构。

reddit · r/MachineLearning · /u/arkuto · 8月16日 10:13

**标签**: `#attention-mechanisms`, `#deep-learning`, `#CNN-architectures`, `#paper-critique`, `#computer-vision`

---

<a id="item-6"></a>
## [第三世界嵌入式工程师为 RISC-V 的发展中国家价值辩护](https://rvembedded.com/blog_post/12/) ⭐️ 6.0/10

一位来自特立尼达和多巴哥的嵌入式工程师发表了一篇回应文章，反驳此前一篇批评 RISC-V 的文章，辩称 RISC-V 开源指令集架构的真正价值在于让发展中国家的硬件项目变得可及。评论者迅速指出其成本与运费分析中的逻辑矛盾——他一方面抱怨 1 美元的芯片运费高达 60 至 200 美元，另一方面却同时赞扬 RISC-V 零件在当地以十美分的价格送达。 这场争论凸显了 RISC-V 社区中日益增长的分歧：一方面是针对高性能计算应用的技术批评，另一方面是嵌入式开发者在供应链受限地区面临的实际现实。它还表明，地理和经济背景可以深刻影响人们对开源 ISA 与 ARM 等专有 ISA 的成本效益分析，而以西方为中心的讨论往往忽视了这些视角。 原始的批评文章似乎认为，RISC-V 可选的 ISA 扩展导致二进制分发碎片化过多，且性能落后于 ARM64，因此 RISC-V 仅限于嵌入式用途。而这篇回应文章则将这一局限性重新诠释为面向发展中国家项目的优势，尽管评论者指出作者自相矛盾——在运费远超芯片本身成本的情况下，却仍将芯片价格视为决定性因素。

hackernews · Narishma · 8月16日 17:01 · [社区讨论](https://news.ycombinator.com/item?id=49321717)

**背景**: RISC-V 是一种基于 RISC 原理的开放、免版税指令集架构（ISA），起源于加州大学伯克利分校，现由 RISC-V International 维护。与 x86 和 ARM 等专有 ISA 不同，RISC-V 无需授权费即可实现，因此对从微控制器到高性能 SoC 的自定义处理器设计都具有吸引力。其模块化特性允许实现者仅包含所需的扩展，一些批评者认为这导致了碎片化，而支持者则认为这是灵活性。嵌入式系统是在更大设备内执行专用功能的专用计算系统，常见于物联网、汽车和消费电子产品中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RISC-V">RISC-V - Wikipedia</a></li>
<li><a href="https://www.stromasys.com/resources/risc-v-vs-arm-processors-comparative-analysis/">RISC - V vs ARM : Complete Architecture Comparison Guide 2026</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为这篇回应文章与原文的论点不同——原文批评的是 RISC-V 在嵌入式领域之外的前景，而这篇文章赞扬的则是其在嵌入式领域的用途。最主要的批评集中在一个明显的逻辑矛盾上：作者抱怨 1 美元零件的运费高达 60 至 200 美元，却又声称 RISC-V 芯片在当地以十美分的价格送达，却未解释运费经济为何突然不再适用。一位评论者将这种修辞结构比作一边批评 Unity 一边承认 Godot 优势的矛盾。

**标签**: `#RISC-V`, `#embedded-systems`, `#hardware-economics`, `#developing-world-tech`, `#ARM-alternatives`

---

<a id="item-7"></a>
## [AI 模型正在主动减少记忆的知识](https://w4g1.dev/blog/models-are-getting-dumber-on-purpose) ⭐️ 6.0/10

本文分析了 AI 模型架构中一个日益增长的趋势：开发者刻意减少存储在模型权重中的事实性知识，转而优先提升推理能力和外部工具调用能力。在 SimpleQA 等不允许使用工具的事实性回忆基准测试中，表现最好的模型仍有近一半的问题回答错误，体现了这种权衡取舍。 这一转变重塑了 AI 系统获取和提供事实信息的方式，有可能减少幻觉问题，但同时也使模型越来越依赖搜索引擎、数据库和 API 等外部基础设施。这对企业部署、成本结构以及知识密集型应用的基本设计都具有重要影响。 分析以 SimpleQA 作为主要基准测试，其中 Gemini 2.5 Pro 在不使用工具的情况下以 53%的准确率领先——尽管该数据据称已有 16 个月之久。这种权衡意味着未来的模型卡可能不再列出知识截止日期，因为权重中残留的知识越来越容易过时。

hackernews · hruvhwe · 8月16日 19:04 · [社区讨论](https://news.ycombinator.com/item?id=49322695)

**背景**: 现代大型语言模型将知识存储在其权重中——这些是在训练过程中学习到的数值参数，编码了模式和事实。随着模型规模不断扩大，关于是否将更多知识直接打包到权重中（即参数化知识），还是构建更小、更高效、依赖外部工具（如搜索引擎和数据库）来查询信息的模型，业界一直存在架构上的争论。本文认为，业界越来越倾向于选择后者，用原始回忆能力换取更好的推理能力和更新的信息访问能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2507.08034v1">Integrating External Tools with Large Language Models (LLM ...</a></li>
<li><a href="https://machinelearningmastery.com/mastering-llm-tool-calling-the-complete-framework-for-connecting-models-to-the-real-world/">Mastering LLM Tool Calling: The Complete Framework for ...</a></li>
<li><a href="https://icymi.in/article/thinking-to-recall-how-reasoning-unlocks-parametric-knowledge-in-llms">Thinking to recall : How reasoning unlocks parametric knowledge in...</a></li>

</ul>
</details>

**社区讨论**: 社区在提出建设性方案的同时也发表了强烈的批评观点。COAGULOPATH 指出了文中的事实错误，并指出该文章是 AI 生成的且信息过时（SimpleQA 基准测试久未更新，Gemini 2.5 Pro 已是 16 个月前的模型）。kennywinker 提出了一种可插拔知识库架构，允许用户在基础推理模型上组合专门的知识模块。msdz 以 Cactus 公司的 Needle（一个专注于工具调用的 14 MB 模型）为例，展示了这一趋势的具体实践。pulkitsh1234 则提出了哲学层面的反驳，认为推理与事实无法干净地分离——要对人类历史或行为等复杂主题进行有意义的推理，需要事实作为基础。

**标签**: `#ai-models`, `#model-architecture`, `#knowledge-retrieval`, `#tool-calling`, `#llm-trends`

---

<a id="item-8"></a>
## [线性注意力在 DNA 建模中的长程召回能力不足](https://www.reddit.com/r/MachineLearning/comments/1vpqwdc/how_can_we_solve_longrange_recall_in_linear/) ⭐️ 6.0/10

一位从事 DNA 序列建模的研究者在实践中证实了线性注意力存在严重的长程召回能力退化：在长上下文下的 Needle-in-a-Haystack 基准测试中，召回率仅约 25%（对于 A/C/G/T 四种词汇几乎等同于随机猜测）。同样的糟糕表现也在 HyenaDNA 上被复现，且召回率从 16K 上下文时的约 50–60%下降至上下文更长时的约 25%。 DNA 序列的长度常常达到 100 万个 token，在这种情况下标准的 softmax 注意力在内存和计算上变得极其昂贵，使得线性注意力成为一种颇具前景的替代方案。如果线性注意力无法在长上下文中可靠地检索信息，那么它在基因组学及其他超长序列应用中的可行性将受到根本性挑战。 研究者测试了一种改进的线性架构，召回率仅约 27%，仍然接近随机水平。已探索的解决方案——外部记忆、滑动窗口/最近 token 机制、以及 softmax 与线性的混合架构——均因成本过高或无法扩展到百万级 token 的 DNA 序列而被排除。

reddit · r/MachineLearning · /u/No-Coffee-8227 · 8月16日 07:47

**背景**: 线性注意力通过用基于特征映射的线性运算近似 softmax 注意力，将序列长度上的复杂度从 O(n²)降低到 O(n)，代价是将所有历史信息压缩到一个固定大小的状态中。这种压缩状态表示被认为是其长程召回能力不如 softmax 注意力的根本原因，因为 softmax 注意力保留了完整的 token 到 token 的交互矩阵。Needle-in-a-Haystack 基准测试通过在长上下文的不同位置和深度插入目标 token 或短语来评估检索能力。HyenaDNA 是一个基于隐式卷积（Hyena）算子的 decoder-only 基因组基础模型，专为单核苷酸分辨率的长程建模而设计，是一种无注意力的替代方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2310.11685">[2310.11685] Superiority of Softmax: Unveiling the ... Bridging the Divide: Reconsidering Softmax and Linear Attention Linear Attention Is All You Need - Towards Data Science Why Softmax Attention Outperforms Linear Attention Linear Attention Fundamentals | Hailey Schoelkopf Why is Linear Attention more efficient than Softmax? What’s ... [2310.11685] Superiority of Softmax: Unveiling the ...</a></li>
<li><a href="https://arxiv.org/pdf/2306.15794">HyenaDNA : Long-Range Genomic Sequence</a></li>
<li><a href="https://towardsdatascience.com/linear-attention-is-all-you-need-5fa9c845c1b5/">Linear Attention Is All You Need - Towards Data Science</a></li>

</ul>
</details>

**标签**: `#linear-attention`, `#long-range-recall`, `#dna-sequences`, `#efficient-attention`, `#machine-learning`

---

<a id="item-9"></a>
## [适者生存：Qwen3.6-27B 的雅可比透镜无需重新拟合即可读取和引导 Qwen3.8-27B](https://www.reddit.com/r/MachineLearning/comments/1vpa5cv/survival_of_the_fitted_qwen3627bs_jacobian_lens/) ⭐️ 6.0/10

实证测试表明，基于雅可比的解释性透镜在 Qwen3.6-27B 上拟合后，无需重新拟合即可部分迁移到 Qwen3.8-27B，表明已拟合的解释性工具可在模型版本更新中延续使用。

reddit · r/MachineLearning · /u/imstilllearningthis · 8月15日 18:24

**标签**: `#interpretability`, `#mechanistic-interpretability`, `#qwen`, `#jacobian-lens`, `#model-transferability`

---

<a id="item-10"></a>
## [BDH-CQ：用于上下文学习的循环潜在推理系统](https://www.reddit.com/r/MachineLearning/comments/1vov5r5/bdhcq_incontext_learning_with_recurrent_latent/) ⭐️ 6.0/10

研究人员推出了 BDH-CQ，一个拥有 1.5 亿参数的推理系统，将循环潜在推理与上下文学习相结合，在 ARC-AGI-1 基准测试上以每任务 0.00070 美元的计算成本实现了 29.5% 的 pass@2。该系统在推理时通过展示的样例更新其循环记忆，然后在高维潜在空间中通过迭代计算求解查询，无需将中间推理步骤显式表达为语言。 BDH-CQ 打破了此前报告的 ARC-AGI-1 成本-精度帕累托前沿，证明具有循环潜在动态的紧凑模型能够以极低的成本提供具有竞争力的推理性能。该方法为不依赖庞大参数规模或昂贵的思维链解码的高效、可部署推理系统提供了一条实用路径。 任务标识符和评估任务演示对均不参与训练，且推理时不更新任何参数——记忆、适应和推理被统一在同一计算框架内。中间推理状态保留在连续的潜在工作空间中，而非被解码为自然语言 token。

reddit · r/MachineLearning · /u/moschles · 8月15日 06:18

**背景**: ARC-AGI-1 是由 François Chollet 设计的手工抽象网格推理基准，用于衡量系统从极少量输入中快速习得新技能的能力，通常被视为对流体通用推理能力的测试。pass@2 指标意味着系统可以尝试两次，只要其中一次正确即认为任务完成，这是减少基准评分方差的常用方法。潜在推理指的是完全在模型内部隐藏状态中执行多步推理，而非生成显式的语言化思维链 token，这一范式作为大规模语言推理的替代方案正日益受到关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.09888v1">BDH-CQ: In-Context Learning with Recurrent Latent Reasoning</a></li>
<li><a href="https://arcprize.org/arc-agi/1">ARC - AGI - 1</a></li>
<li><a href="https://arxiv.org/abs/2507.06203">[2507.06203] A Survey on Latent Reasoning - arXiv.org Latent Recurrent Thinking A Paradigm Shift in AI Reasoning ... Latent Recurrent Thinking: A Paradigm Shift in AI Reasoning ... Latent Reasoning in Neural Models - emergentmind.com Latent circuit inference from heterogeneous neural responses ... Recurrent neural networks with explicit representation of ...</a></li>

</ul>
</details>

**标签**: `#in-context-learning`, `#recurrent-neural-networks`, `#ARC-AGI`, `#reasoning-systems`, `#efficiency`

---