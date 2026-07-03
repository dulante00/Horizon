---
layout: default
title: "Horizon Summary: 2026-07-03 (ZH)"
date: 2026-07-03
lang: zh
---

> 从 67 条内容中筛选出 16 条重要资讯。

---

1. [Karpathy 发布 nanochat：100 美元打造 ChatGPT 克隆](#item-1) ⭐️ 8.0/10
2. [huggingface/transformers 发布 v5.13.0](#item-2) ⭐️ 7.0/10
3. [PostgreSQL 与 OOM killer：为何我们使用严格的内存超额提交策略](#item-3) ⭐️ 7.0/10
4. [Wordgard：ProseMirror 作者推出的全新富文本编辑器](#item-4) ⭐️ 7.0/10
5. [将代码转为图片利用 OCR 处理，LLM 成本降低 60%](#item-5) ⭐️ 7.0/10
6. [Mistral 发布 Leanstral-1.5-119B-A6B，专注形式化验证与自动定理证明](#item-6) ⭐️ 7.0/10
7. [希腊欧洲议会议员在调查间谍软件期间遭 Pegasus 入侵](#item-7) ⭐️ 6.0/10
8. [Jamesob 的本地运行 SOTA 大语言模型指南](#item-8) ⭐️ 6.0/10
9. [Valve 开源 Steam Machine 电子墨水屏设计供社区自制](#item-9) ⭐️ 6.0/10
10. [半生不熟的产品](#item-10) ⭐️ 6.0/10
11. [螺旋蝇的衰落与复兴](#item-11) ⭐️ 6.0/10
12. [Google DeepMind 与 A24 宣布建立开创性研究合作伙伴关系](#item-12) ⭐️ 6.0/10
13. [上海交大提出 HAT-4D：单目视频直接生成 4D 交互场景](#item-13) ⭐️ 6.0/10
14. [葡萄牙发布开源国家大语言模型 Amalia（90 亿参数）](#item-14) ⭐️ 6.0/10
15. [这下彻底结束了。英伟达 AI 先驱之一不认同通用人工智能（AGI），将 OpenAI 和 Anthropic 的封闭模型比作 AOL 和 Prodigy 的封闭互联网，并预言未来每家企业都将拥有定制化的开源模型。](#item-15) ⭐️ 6.0/10
16. [llama.cpp 的粒子散射采样器](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Karpathy 发布 nanochat：100 美元打造 ChatGPT 克隆](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy 在 GitHub 上发布了 nanochat，这是一个开源的全栈实验框架，可在单个 GPU 节点上训练并运行 ChatGPT 风格的 LLM，总训练成本目标约为 100 美元。 鉴于 Karpathy 在 nanoGPT 和 minbpe 等具有影响力的教育项目上的过往成绩，nanochat 有可能大幅降低 LLM 训练和实验的入门门槛，使没有大量计算预算的学生、爱好者和研究人员也能参与其中。 该仓库刻意保持精简且易于修改，覆盖了完整的 LLM 流程，包括分词、预训练、微调、评估、推理以及聊天 UI，运行于单个 GPU 节点之上。有报道称端到端训练可在五小时内完成，但初次发布时并未披露具体的模型规模、架构以及与更大模型的基准对比结果。

github · karpathy · 7月3日 17:47

**背景**: Andrej Karpathy 是一位知名的 AI 研究者和教育者，曾就职于 OpenAI 和 Tesla，以创建简洁、极简且具有教学价值的开源代码库而闻名，例如 nanoGPT（一个简单的 GPT 训练仓库）和 minbpe（一个极简的字节对编码分词器）。他的项目通常作为新手理解 LLM 内部机制的入门工具，而非生产级系统。nanochat 将这一理念延伸到了完整的训练后流程：它不只是预训练基础模型，而是整合了 ChatGPT 风格的完整工作流，包括微调和聊天界面。100 美元的成本目标令人瞩目，因为即便是从头训练小型 LLM 通常也需要数千美元的云 GPU 费用，所以在此价位下实现一个能进行连贯对话的模型将是一项重要的效率里程碑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy / nanochat : The best ChatGPT that $100 can buy.</a></li>
<li><a href="https://medium.com/@writeronepagecode/the-100-chatgpt-a-code-level-tour-of-andrej-karpathys-nanochat-729490982bcc">The $100 ChatGPT: A Code-Level Tour of Andrej Karpathy ’s nanochat</a></li>
<li><a href="https://www.linkedin.com/posts/arif-ansari-_github-karpathynanochat-the-best-chatgpt-activity-7384105782788853761-SBgv">Andrej Karpathy releases nanochat , a ChatGPT-style LLM... | LinkedIn</a></li>

</ul>
</details>

**标签**: `#karpathy`, `#nanochat`, `#LLM`, `#cost-efficient-training`, `#open-source`

---

<a id="item-2"></a>
## [huggingface/transformers 发布 v5.13.0](https://github.com/huggingface/transformers/releases/tag/v5.13.0) ⭐️ 7.0/10

Hugging Face Transformers v5.13.0 新增了对月之暗面 Moonshot AI 的 Kimi K2.5、K2.6 和 K2.7 多模态智能体模型架构的支持。

github · vasqu · 7月3日 16:06

**标签**: `#huggingface`, `#transformers`, `#kimi-k2`, `#multimodal-models`, `#release-notes`

---

<a id="item-3"></a>
## [PostgreSQL 与 OOM killer：为何我们使用严格的内存超额提交策略](https://www.ubicloud.com/blog/postgresql-and-the-oom-killer-why-we-use-strict-memory-overcommit) ⭐️ 7.0/10

Ubicloud 解释了为何采用严格的内存超额提交设置，以防止 Linux 的 OOM killer 终止 PostgreSQL 进程，社区讨论也指出了 Linux 内存管理中的一些陷阱。

hackernews · furkansahin · 7月3日 13:00 · [社区讨论](https://news.ycombinator.com/item?id=48774509)

**标签**: `#postgresql`, `#linux`, `#memory-management`, `#oom-killer`, `#devops`

---

<a id="item-4"></a>
## [Wordgard：ProseMirror 作者推出的全新富文本编辑器](https://wordgard.net/) ⭐️ 7.0/10

ProseMirror 的作者 Marijn Haverbeke 发布了 Wordgard 0.1，这是一个新的开源 JavaScript 库，用于实现浏览器内的富文本编辑器。Wordgard 被描述为 ProseMirror 风格系统的新一代迭代，整合了自 ProseMirror 稳定以来九年间积累的经验。 ProseMirror 为众多流行的编辑器产品提供底层支持（包括广泛使用的封装库 TipTap），因此其原作者推出的任何继任者或替代方案在 Web 编辑器生态中都举足轻重。Wordgard 的发布重新激发了 2025–2026 年编辑器框架选择的讨论，与 Lexical、Tiptap、BlockNote、Slate 等选项形成竞争。 Wordgard 的设计重点是为符合特定 schema 的内容提供可定制的编辑体验，而非通用的所见即所得或 HTML 编辑器。根据社区讨论，它与 ProseMirror 共享许多概念，但目前没有提供升级路径，这意味着迁移现有的基于 ProseMirror 的项目需要大量返工。

hackernews · indy · 7月3日 08:50 · [社区讨论](https://news.ycombinator.com/item?id=48772573)

**背景**: ProseMirror 是由 Marijn Haverbeke 于约 2015 年发布的成熟开源 Web 富文本编辑器工具包。它提供底层构件——schema、文档模型、事务和协同编辑原语——而非开箱即用的编辑器，这也是为什么会出现 TipTap 等封装库来提供更高级别的 API。Wordgard 代表着同一作者在近十年的实际反馈、使用模式和生态演变之后，对该问题空间的重新思考。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://marijnhaverbeke.nl/blog/wordgard-0.1.html">Wordgard Release 0.1</a></li>
<li><a href="https://wordgard.net/">Wordgard</a></li>
<li><a href="https://wordgard.net/docs/guide/">Wordgard System Guide</a></li>

</ul>
</details>

**社区讨论**: 评论者对 Wordgard 的设计和技思路表示强烈热情，一些人验证了他们自己的自定义解决方案与 Wordgard 的设计选择相吻合。主要担忧包括：缺少从 ProseMirror 迁移的升级路径、缺乏静态类型的 schema 表示（目前用户通常借助 Zod 等工具配合 ProseMirror 来解决这一问题），以及更广泛的不满——15 年后的今天，Web 仍然缺乏标准化的所见即所得编辑器接口。TipTap 用户被认为是最有可能评估迁移的受众。

**标签**: `#rich-text-editor`, `#prosemirror`, `#web-development`, `#javascript`, `#text-editing`

---

<a id="item-5"></a>
## [将代码转为图片利用 OCR 处理，LLM 成本降低 60%](https://github.com/teamchong/pxpipe) ⭐️ 7.0/10

一位开发者在 GitHub 上发布了名为 pxpipe 的工具，该工具将代码转换为图片，再交给 LLM（Claude Fable）通过 OCR 方式识别处理，相比直接发送文本令牌，实现了 60%的 API 成本降低。 如果该技术能够稳定生效，它可能大幅降低以代码为核心工作负载的 LLM 推理成本，使运行大规模代码分析的开发者与初创公司受益。但社区怀疑这是一种利用定价/计费漏洞的手段，厂商可能会修复该漏洞，因此它更可能只是临时性的优势，而非结构性的成本优化。 该工具已在 GitHub（teamchong/pxpipe）开源，专门针对 Claude 的定价模型。这个技巧很可能利用了图片/视觉令牌的计费费率低于等效文本令牌，或者后端 OCR 处理完全不对用户计费的机制。该 Reddit 原帖在短时间内获得了 190 个赞和 72 条评论。

hackernews · dimitropoulos · 7月3日 15:50 · [社区讨论](https://news.ycombinator.com/item?id=48776464)

**背景**: Claude 等大语言模型支持多模态输入，意味着它们既能处理文本也能处理图片。当发送一张包含文字的图片时，模型会执行光学字符识别（OCR）来提取其中的文字。不同厂商对视觉令牌和文本令牌的定价方式不同——例如 Claude Fable 5 的定价为每百万输入令牌 10 美元、每百万输出令牌 50 美元，但图片令牌的计费方式可能有所不同。这种不对称性使得将文本嵌入图片发送可能比直接发送纯文本更便宜，具体取决于厂商在内部如何核算 OCR 步骤的费用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.mindstudio.ai/blog/claude-fable-5-pricing-access-usage-limits">Claude Fable 5 Pricing, Access, and Usage Limits: What You Need to Know | MindStudio</a></li>
<li><a href="https://medium.com/@pvsravanth/next-gen-ocr-with-vision-llms-a-guide-to-using-phi-3-claude-and-gpt-4o-4c6fbabe92c8">Next-Gen OCR with Vision LLMs : A Guide to Using Phi-3, Claude, and GPT-4O | by Sravanth | Generative AI</a></li>
<li><a href="https://www.reddit.com/r/ClaudeAI/comments/1u4j86h/fable_5_what_600hour_of_productivity_looks_like/">Fable 5: What $600/Hour of Productivity Looks Like : r/ClaudeAI - Reddit</a></li>

</ul>
</details>

**社区讨论**: 社区普遍对这种技巧的持久性持怀疑态度。评论者将其与 Gemini 处理 PDF 的方式进行类比——Gemini 会执行内部 OCR 但不收取相应文本令牌的费用——他们认为 Claude 后端可能也在做类似的事情，因此这只是一个很可能被修复的计费漏洞。一位用户报告说去年曾用 OpenAI 模型尝试过类似方法，虽然减少了提示令牌，但输出令牌大幅增加，导致速度更慢且总成本反而更高。还有人指出 GitHub 上的 README 写得较差（可能是用 AI 生成的），并警告说一旦厂商关闭漏洞，OCR 定价可能会相应上涨。

**标签**: `#llm`, `#cost-optimization`, `#ocr`, `#prompt-engineering`, `#claude`

---

<a id="item-6"></a>
## [Mistral 发布 Leanstral-1.5-119B-A6B，专注形式化验证与自动定理证明](https://www.reddit.com/r/LocalLLaMA/comments/1umgdhx/mistral_released_leanstral15119ba6b/) ⭐️ 7.0/10

Mistral 发布了 Leanstral-1.5-119B-A6B，这是一个采用 Apache-2.0 许可证的混合专家（MoE）模型，激活参数为 6B，在多个形式化验证基准测试中取得了最先进的结果——在 miniF2F 上达到饱和、在 PutnamBench 上解决 587/672 道题、在 FATE-H 上达到 87%、在 FATE-X 上达到 34%。 此次发布标志着自动定理证明领域一项重要的开源进展，并具备在实际代码中发现真实漏洞的实用能力——具体来说，在 57 个测试仓库中发现了 5 个此前未知的 Bug——对软件正确性和安全研究具有直接价值。 该模型通过中训练、监督微调以及使用 CISPO 算法的强化学习构成的三阶段流程训练而成，擅长智能体化的证明工程，而非作为通用聊天模型使用。

reddit · r/LocalLLaMA · /u/Tall-Ad-7742 · 7月3日 14:44

**背景**: 形式化验证利用数学证明来保证软件的正确性，Lean 是最广泛采用的交互式定理证明器之一。混合专家（MoE）架构在每个 token 上仅激活总参数的一个子集，从而以较低的推理成本实现大模型容量——本模型激活参数为 60 亿，总参数量为 1190 亿。CISPO（Clipped Importance Sampling Policy Optimization）是一种强化学习算法，通过裁剪 token 级别的重要性采样权重来降低方差并稳定离策略训练。miniF2F（奥数级别的数学问题）、PutnamBench（以 Lean、Isabelle 和 Coq 形式化的 Putnam 竞赛题）以及 FATE-H/FATE-X 等基准是衡量模型形式推理能力的标准评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2109.00110">[2109.00110] MiniF 2 F : a cross-system benchmark for formal ...</a></li>
<li><a href="https://trishullab.github.io/PutnamBench/">PutnamBench : A Multilingual Mathematics Benchmark for Formal ...</a></li>
<li><a href="https://www.emergentmind.com/topics/cispo-algorithm">CISPO : Clipped Importance Sampling RL</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#theorem-proving`, `#Mistral`, `#open-source`, `#LLM`

---

<a id="item-7"></a>
## [希腊欧洲议会议员在调查间谍软件期间遭 Pegasus 入侵](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 6.0/10

Citizen Lab 报告称，正在调查间谍软件滥用问题的欧洲议会委员会成员、希腊议员 Stelios Kouloglou 本人于 2022 年 10 月 21 日前后及 2023 年 3 月 6 日至 7 日两次遭 Pegasus 间谍软件成功入侵。该取证分析是在他于 2026 年 5 月联系 Citizen Lab 后对其 iPhone 进行的。 此案凸显了国家级行为者对民主监督人物的肆无忌惮的攻击，动摇了本应调查监控滥用的机构本身。这暴露了即使是被委派审查间谍软件的立法者也同样脆弱，并对欧盟成员国境内的国家支持监控行为提出了严重质疑。 Pegasus 由 NSO 集团开发，是一种高级间谍软件，能够通过零点击感染入侵设备，无需用户任何交互即可攻陷目标。该议员多次在不同日期被攻击，表明这是持续且蓄意的监控行为，而非一次性操作，其时间节点与希腊更广泛的监控丑闻相吻合，该丑闻涉及总理办公室和国家情报部门。

hackernews · ledoge · 7月3日 20:38 · [社区讨论](https://news.ycombinator.com/item?id=48779683)

**背景**: Pegasus 间谍软件由以色列 NSO 集团开发，是目前最先进的商业监控工具之一，通常出售给政府客户用于执法和情报目的。它可以通过零点击漏洞入侵智能手机，将设备变为完整的监控工具，获取消息、摄像头、麦克风和位置数据。Citizen Lab 位于多伦多大学蒙克全球事务学院，是领先的研究机构，专门检测和揭露针对公民社会、记者和政治人物的数字威胁。在 Pegasus 及同类间谍软件在欧盟成员国被广泛滥用的消息曝光后，欧洲议会成立了专门委员会（PEGA）来调查相关情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://citizenlab.ca/about/">Who We Are - The Citizen Lab</a></li>
<li><a href="https://us.norton.com/blog/emerging-threats/pegasus-spyware">What is Pegasus spyware , and how to detect and remove it</a></li>

</ul>
</details>

**社区讨论**: 评论者将此事件置于希腊更大规模的未解监控丑闻背景中，指出许多政客都被入侵过，有证据表明这是由总理办公室和情报部门策划的，因此这并非专门针对欧洲议会的攻击。另一位评论者则对游说者将欧盟公民数据出售给美国公司的行为表示担忧，突显了对欧盟政策受外部影响的忧虑。

**标签**: `#spyware`, `#pegasus`, `#cybersecurity`, `#european-politics`, `#surveillance`

---

<a id="item-8"></a>
## [Jamesob 的本地运行 SOTA 大语言模型指南](https://github.com/jamesob/local-llm) ⭐️ 6.0/10

一份关于在本地运行最先进大语言模型的全面指南，涵盖硬件推荐，并附有关于成本权衡和统一内存架构等替代方案的实质性社区讨论。

hackernews · livestyle · 7月3日 15:03 · [社区讨论](https://news.ycombinator.com/item?id=48775921)

**标签**: `#LLM`, `#local-inference`, `#hardware`, `#GPU`, `#machine-learning`

---

<a id="item-9"></a>
## [Valve 开源 Steam Machine 电子墨水屏设计供社区自制](https://www.gamingonlinux.com/2026/07/valve-open-source-the-steam-machine-e-ink-screen-so-you-can-make-your-own/) ⭐️ 6.0/10

Valve 发布了 Steam Machine 可选电子墨水屏配件的开源硬件设计文件，使社区用户可以使用标准的 Adafruit 5.83 英寸 eInk 面板（产品编号 #6397）自行制作。 此举延续了 Valve 开源硬件的传统（继 Steam Deck 之后），让创客社区能够定制和扩展他们的设备，而非将配件锁定在专有设计中。它标志着硬件制造商即使对非核心配件也日益拥抱开源硬件理念的趋势。 该屏幕采用标准现成的 Adafruit 5.83 英寸单色 eInk/电子纸面板（可能是产品编号 #6397 下 648×480 分辨率的版本），采购方便。电子墨水屏仅在刷新图像时消耗电力，非常适合作为常亮状态显示屏而不会增加系统功耗。

hackernews · ahlCVA · 7月3日 13:01 · [社区讨论](https://news.ycombinator.com/item?id=48774518)

**背景**: 电子墨水屏（e-ink）显示技术利用含有带电粒子的微小胶囊来模拟印刷纸张的外观，可读性出色且功耗极低，因为图像无需持续供电即可保持显示。Adafruit 是一家知名的开源硬件公司，生产模块化电子元件、分线板和显示屏，深受爱好者和创客欢迎。Steam Machine 是 Valve 即将推出的游戏桌面设备，可选的电子墨水屏作为辅助状态显示屏，可能用于显示当前运行的游戏、温度或通知等系统信息。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@centralfinder.24/how-do-eink-readers-actually-work-edef91d69cf2">How do eInk Readers actually work ? | by Central Finder | Medium</a></li>
<li><a href="https://www.adafruit.com/product/6395">3.7" 416x240 Monochrome Black/White eInk / ePaper - Bare Display</a></li>
<li><a href="https://thepihut.com/products/adafruit-3-52-340x180-quad-colour-eink-epaper-bare-display">Adafruit 3.52" 340x180 Quad-Colour eInk / ePaper - Bare... - The Pi Hut</a></li>

</ul>
</details>

**社区讨论**: 社区反应普遍非常积极，用户赞扬 Valve 对可选配件采取的开放态度，并希望更多硬件公司效仿。一位用户直接给出了确切的 Adafruit 面板型号供不想搜索的人参考，另一位用户表达了热情支持（'Valve mi familia'），还有 Framework Desktop 用户询问如何将此设计适配到该机型。此外也有人实际询问是否有支持 HDMI 或 USB-C 输入的更大尺寸 A5（约 10 英寸）电子墨水屏用于其他用途。

**标签**: `#open-source`, `#hardware`, `#valve`, `#e-ink`, `#steam-machine`

---

<a id="item-10"></a>
## [半生不熟的产品](https://weli.dev/blog/half-baked-product/) ⭐️ 6.0/10

这是一个创业警示故事，讲述创始人在缺乏深厚领域专业知识的情况下打造产品，导致商业愿景、技术可行性和客户需求之间出现根本性的脱节。

hackernews · weli · 7月3日 08:23 · [社区讨论](https://news.ycombinator.com/item?id=48772388)

**标签**: `#startups`, `#entrepreneurship`, `#product-development`, `#founder-advice`, `#business-strategy`

---

<a id="item-11"></a>
## [螺旋蝇的衰落与复兴](https://www.construction-physics.com/p/the-fall-and-rise-of-screwworm) ⭐️ 6.0/10

使用不育昆虫技术根除螺旋蝇的历史回顾，探讨了这种害虫为何卷土重来以及当今遏制它所面临的挑战。

hackernews · crescit_eundo · 7月3日 12:58 · [社区讨论](https://news.ycombinator.com/item?id=48774492)

**标签**: `#biology`, `#agriculture`, `#biosecurity`, `#history-of-science`, `#pest-management`

---

<a id="item-12"></a>
## [Google DeepMind 与 A24 宣布建立开创性研究合作伙伴关系](https://deepmind.google/blog/google-deepmind-and-a24-announce-first-of-its-kind-research-partnership/) ⭐️ 6.0/10

Google DeepMind 宣布与电影制作公司 A24 建立开创性的研究合作伙伴关系，探索人工智能与电影制作领域的跨界合作。

rss · Google DeepMind Blog · 7月3日 14:25

**标签**: `#Google DeepMind`, `#A24`, `#AI partnerships`, `#film industry`, `#research collaboration`

---

<a id="item-13"></a>
## [上海交大提出 HAT-4D：单目视频直接生成 4D 交互场景](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247901356&idx=3&sn=54ee94026f76691a380cd3ea214e0def) ⭐️ 6.0/10

上海交通大学等机构的研究者提出了 HAT-4D 方法，能够直接从单目视频生成可交互的 4D 场景。该技术旨在通过普通单摄像头拍摄的视频重建出可操控的动态三维环境和物体，无需依赖专业动捕设备。 该方法可能大幅降低创建可交互 4D 内容的成本门槛，有望用普通视频取代价值百万的专业动捕棚。如果效果可靠，将惠及影视特效制作、游戏开发、AR/VR 应用，以及所有需要从日常拍摄中重建动态 3D 场景的领域。 原始 RSS 内容较为碎片化，混杂了多篇无关文章的片段，难以提取关于 HAT-4D 架构、训练数据或基准测试结果的具体技术细节。单目视频 4D 重建领域的相关工作（如 LIM 和 Vivid4D）表明这是一个活跃且竞争激烈的研究方向，目前正在探索基于扩散模型的多视角生成和大型插值模型等方案。

rss · 量子位 · 7月3日 03:43

**背景**: 4D 重建指的是随时间变化的动态 3D 场景重建（第四个维度是时间）。传统方法需要昂贵的多摄像头阵列或动捕棚来精确捕捉几何与运动信息。单目视频重建旨在仅通过单个摄像头的视角完成同样的任务，获取门槛低得多，但由于缺乏多视角几何约束，在数学上极具挑战性。神经辐射场（NeRF）、高斯散射（Gaussian Splatting）和扩散模型的最新进展推动了该领域的快速发展，目前已应用于医学内窥镜重建到动态图形资产生成等多种场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2504.11092">[2504.11092] Vivid 4 D : Improving 4 D Reconstruction from Monocular ...</a></li>
<li><a href="https://remysabathier.github.io/lim.github.io/">LIM: Large Interpolator Model for Dynamic Reconstruction</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/41719834/">4 D monocular surgical reconstruction under arbitrary camera motions</a></li>

</ul>
</details>

**标签**: `#4D-reconstruction`, `#computer-vision`, `#monocular-video`, `#research`, `#AI`

---

<a id="item-14"></a>
## [葡萄牙发布开源国家大语言模型 Amalia（90 亿参数）](https://www.reddit.com/r/LocalLLaMA/comments/1umhrn8/portugal_just_released_their_own_llm_amalia_9b/) ⭐️ 6.0/10

葡萄牙发布了 Amalia，一个拥有 90 亿参数的开源大语言模型，采用 Apache 2.0 许可证，是葡萄牙政府国家人工智能计划的一部分。模型在 Hugging Face 上提供了两个变体：AMALIA-9B-0626-SFT（监督微调版本）和 AMALIA-9B-0626-DPO（直接偏好优化版本），并附带了一篇 arxiv 论文。 Amalia 加入了由政府支持的国家大语言模型浪潮，表明各国越来越多地投资于针对本国语言和文化背景的主权人工智能能力。Apache 2.0 开源许可证允许全球研究人员和开发者在此模型基础上进行开发，有望加强葡萄牙语的人工智能工具生态。 帖子指出，发布时未提供明确的编程基准测试结果，这限制了对 Amalia 在现有 90 亿参数模型中表现的即时评估。SFT 和 DPO 两个变体都可供用户使用，提供了在特定任务监督微调和基于偏好的对齐之间的选择。

reddit · r/LocalLLaMA · /u/EveningIncrease7579 · 7月3日 15:38

**背景**: 监督微调（SFT）是一种使用标注示范数据对预训练模型进行细化的技术，以提高特定任务的表现。直接偏好优化（DPO）是一种较新的对齐方法，通过将奖励建模和 PPO 优化合并为单个监督训练目标，简化了传统的基于人类反馈的强化学习（RLHF）流程。国家大语言模型是由政府训练或调整的主权人工智能模型，旨在更好地代表本国语言、文化价值观和地区需求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cameronrwolfe.substack.com/p/understanding-and-using-supervised">Understanding and Using Supervised Fine - Tuning ( SFT ) for...</a></li>
<li><a href="https://toloka.ai/blog/direct-preference-optimization/">Direct Preference Optimization ( DPO ): a lightweight counterpart to...</a></li>
<li><a href="https://qubittool.com/blog/dpo-vs-rlhf-alignment-techniques">DPO vs RLHF : The Evolution of LLM Alignment Techniques | QubitTool</a></li>

</ul>
</details>

**标签**: `#LLM`, `#open-source`, `#Portugal`, `#national-AI`, `#LocalLLaMA`

---

<a id="item-15"></a>
## [这下彻底结束了。英伟达 AI 先驱之一不认同通用人工智能（AGI），将 OpenAI 和 Anthropic 的封闭模型比作 AOL 和 Prodigy 的封闭互联网，并预言未来每家企业都将拥有定制化的开源模型。](https://www.reddit.com/r/LocalLLaMA/comments/1ult0f4/its_officially_over_one_of_the_fathers_of_ai_at/) ⭐️ 6.0/10

英伟达一位资深 AI 研究员公开否定通用人工智能（AGI），将 OpenAI 和 Anthropic 等封闭式 AI 实验室比作昔日的 AOL 和 Prodigy，主张开源定制化模型将成为企业级 AI 的未来主流。

reddit · r/LocalLLaMA · /u/9gxa05s8fa8sh · 7月2日 20:06

**标签**: `#open-source-ai`, `#nvidia`, `#AGI`, `#ai-industry`, `#open-vs-closed`

---

<a id="item-16"></a>
## [llama.cpp 的粒子散射采样器](https://www.reddit.com/r/LocalLLaMA/comments/1umqgnl/particle_scattering_sampler_for_llamacpp/) ⭐️ 6.0/10

一个实验性的“散射”采样器，已添加到 llama.cpp 中。它通过局部扩散步骤在顶层候选词元之间重新分配概率质量，旨在降低生成僵化度，同时避免将概率泄漏到深层尾部。

reddit · r/LocalLLaMA · /u/Pristine_Income9554 · 7月3日 21:19

**标签**: `#llama.cpp`, `#sampling`, `#LLM inference`, `#token generation`, `#local LLMs`

---