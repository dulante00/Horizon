---
layout: default
title: "Horizon Summary: 2026-07-12 (ZH)"
date: 2026-07-12
lang: zh
---

> 从 40 条内容中筛选出 16 条重要资讯。

---

1. [vLLM v0.25.0 发布：MRv2 成为默认，移除旧版 PagedAttention](#item-1) ⭐️ 8.0/10
2. [研究：Claude Code 启动开销达 33k token，OpenCode 仅 7k](#item-2) ⭐️ 7.0/10
3. [古今应用，借助现代编码代理](#item-3) ⭐️ 7.0/10
4. [George Hotz：前沿 AI 实验室无法捕获 LLM 创造的价值](#item-4) ⭐️ 7.0/10
5. [带状疱疹疫苗可能降低痴呆症风险](#item-5) ⭐️ 7.0/10
6. [DeepSeek 据报道正在自研 AI 芯片以减少对美依赖](#item-6) ⭐️ 7.0/10
7. [我在 Qwen3-4B 上的 7 个数据集中映射了 Anthropic 的 J-Space 幻觉信号，以找出它的有效范围与失效场景](#item-7) ⭐️ 7.0/10
8. [Ghostel：基于 libghostty 的全新 Emacs 终端模拟器](#item-8) ⭐️ 6.0/10
9. [Hunyuan3D 的 MLX 移植版在 Apple Silicon 上实现本地图像转 3D](#item-9) ⭐️ 6.0/10
10. [Moondream 3.1：90 亿参数 MoE 视觉语言模型发布](#item-10) ⭐️ 6.0/10
11. [Apple sues OpenAI alleging trade secret theft, says scheme was 'at every level'](#item-11) ⭐️ 6.0/10
12. [小米悄然在 Hugging Face 上传 MiMo-V2.5-DFlash 模型权重](#item-12) ⭐️ 6.0/10
13. [三行代码修复 llama.cpp 在 Tesla P100 上存在多年的 fp16 精度 Bug](#item-13) ⭐️ 6.0/10
14. [Voodoo Quant 声称在 KLD 指标上超越 Unsloth Dynamic 2.0 达 95%](#item-14) ⭐️ 6.0/10
15. [交互式 Jacobian-Lens 工具将 Anthropic 可解释性技术引入 GGUF 模型](#item-15) ⭐️ 6.0/10
16. [Zer0Fit：将 Google TabFM 与 TimesFM 封装为本地方零样本机器学习的 MCP 服务器](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0 发布：MRv2 成为默认，移除旧版 PagedAttention](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 是一个重大版本，包含来自 232 位贡献者的 558 次提交，Model Runner V2（MRv2）成为所有稠密模型的默认执行路径，旧版 PagedAttention 实现被完全移除，Transformers 后端实现了与原生 vLLM 相当的性能。 此次发布标志着这一最广泛部署的开源 LLM 推理框架之一完成了决定性的架构转型：移除作为基础的 PagedAttention 代码路径并统一采用 MRv2，整顿了代码库并释放了更高吞吐量，而 Transformers 性能对齐则大幅降低了依赖 Hugging Face 生态进行生产推理用户的使用门槛。 MRv2 新增对 EVS、实时嵌入、Mamba 混合模型的前缀缓存、多模态前缀双向注意力，以及兼容完整 CUDA Graph 的动态推测解码的支持。新推测解码功能包括通用异构词表 TLI 支持以及 DSpark 和 DFlash 草稿模型，Rust 前端则通过 HTTPS/mTLS 和 DP 监督器进一步成熟，用于分布式推理服务。

github · khluu · 7月11日 20:06

**背景**: vLLM 是一个开源的高吞吐量 LLM 推理与服务引擎，最初基于 PagedAttention 构建——一种受操作系统虚拟内存分页启发的内存管理技术，将 KV 缓存虚拟化以大幅减少碎片并提升服务吞吐量。Model Runner V2 是重新设计的执行引擎，取代了 V1 runner，能在 GB200、H100 和 A100 等架构上提供更好的硬件利用率。推测解码通过让较小的草稿模型先生成候选 token、再由较大的目标模型并行验证来加速推理，vLLM 等框架提供可配置的草稿器（如 DFlash、DSpark、类 Medusa 的预测头）来在不改变输出分布的前提下提升每秒 token 数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2309.06180">[2309.06180] Efficient Memory Management for Large Language...</a></li>
<li><a href="https://www.spheron.network/blog/vllm-model-runner-v2-mrv2-deployment-guide/">vLLM Model Runner V 2 on GPU Cloud: Deploy MRV 2 for Faster LLM...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2607.05147">DSpark: Confidence-Scheduled Speculative Decoding with... | alphaXiv</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#model-serving`, `#paged-attention`, `#release-notes`

---

<a id="item-2"></a>
## [研究：Claude Code 启动开销达 33k token，OpenCode 仅 7k](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 7.0/10

Systima 进行了一项实证研究，通过在 Anthropic API 与两款代理式编程工具（Claude Code 和 OpenCode）之间加入日志记录，发现 Claude Code 在处理用户提示前会发送约 33,000 个 token 的开销，而 OpenCode 仅约 7,000 个 token。 对于按 token 计费的开发者来说，每次请求固定开销近 5 倍的差异意味着显著的成本差距，同时研究结果也引发了质疑：这些开销究竟是由缓存命中所节省的成本所合理化，还是受供应商定价策略驱动、迫使用户转向订阅模式。 该研究仅测量了固定开销（用户提示之前发送的 token 数），并未衡量实际完成的工作量，因此无法判断单位任务的成本效率。缓存命中的 token 计费约为缓存未命中的 1/10，因此较高的开销如果在后续轮次中被缓存复用，可能部分被摊薄。

hackernews · systima · 7月12日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=48883275)

**背景**: Claude Code 是 Anthropic 专有的代理式编程命令行工具，而 OpenCode 是一款开源替代品（GitHub star 数超过 16 万），可以连接包括 Anthropic 在内的多种模型提供商。两款工具都会在用户实际请求之前向大语言模型发送系统提示、工具定义和代理指令，这部分固定载荷被称为「token 开销」。提示缓存是一种技术，会将频繁复用的提示前缀（如系统指令）存储并以更低成本重新提供，如果同一前缀在多轮中重复出现，则可以让较大的开销变得更加经济。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent , Terminal, IDE</a></li>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-caching">What is Prompt Caching? | IBM</a></li>

</ul>
</details>

**社区讨论**: 评论者提出了几个关键观点：子代理会大幅增加 token 消耗（一位用户报告 7 个子代理瞬间烧光了预算），部分人怀疑 Anthropic 故意膨胀开销以推动用户订阅，另一些人则认为缓存命中的定价（1/10 成本）可能使开销合理，同时研究作者在更新中承认，仅比较固定成本而不衡量实际工作具有误导性，并承诺进行更详尽的后续测试。

**标签**: `#claude-code`, `#opencode`, `#token-optimization`, `#ai-coding-agents`, `#anthropic`

---

<a id="item-3"></a>
## [古今应用，借助现代编码代理](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 7.0/10

陶哲轩分享了他使用现代大语言模型编码代理为数学工作构建辅助应用和可视化的体验，并对其实用性给出了客观评价。

hackernews · subset · 7月12日 11:09 · [社区讨论](https://news.ycombinator.com/item?id=48880170)

**标签**: `#AI`, `#LLM-coding-agents`, `#Terry-Tao`, `#mathematics`, `#software-tools`

---

<a id="item-4"></a>
## [George Hotz：前沿 AI 实验室无法捕获 LLM 创造的价值](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 7.0/10

在一篇题为《I love LLMs, I hate hype》的博客文章中，George Hotz（网名 geohot）认为前沿 AI 实验室将无法捕获大语言模型所创造的经济价值，尽管这项技术本身通过易于定制的开源分支极大地提升了个人生产力。 这种逆向分析将 LLM 的真实技术实用性与前沿实验室的可疑商业前景区分开来，挑战了主流的 AI 投资叙事，对投资者、开发人员以及任何评估 AI 实际影响与市场炒作的人士都具有重要意义。 Hotz 强调了向"随心定制"（have it your way）时代的转变，个人开发者会选择 fork 或修改开源项目，而不是将更改提交回上游，引发了关于开源可持续性的担忧。评论者也指出，当前 LLM 的成本仍然严重依赖补贴，长期的可负担性和本地推理可行性仍存在不确定性。

hackernews · therepanic · 7月12日 18:31 · [社区讨论](https://news.ycombinator.com/item?id=48883343)

**背景**: George Hotz，网名 geohot，是一位著名的美国安全研究人员和企业家，最初因破解 iPhone 和逆向工程 PlayStation 3 而闻名，后来创办了自动驾驶公司 Comma.ai。"前沿 AI 实验室"指的是构建最先进 AI 模型的领先机构，2026 年通常被认定为 OpenAI、Anthropic、Google DeepMind、Meta 和 xAI。在开源软件中，"fork"是指通过复制现有项目并独立修改而创建的新代码库，如果与原始项目分开维护，可能会分散社区贡献。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/George_Hotz">George Hotz - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fork_(software_development)">Fork ( software development ) - Wikipedia</a></li>
<li><a href="https://blog.magmalabs.io/2026/05/29/who-are-the-big-5-in-ai-a-2026-field-guide-for-tech-leaders.html">Who Are the Big 5 in AI ? A 2026 Field Guide for Tech Leaders - The...</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认同 Hotz 的核心论点——前沿实验室将难以捕获 LLM 创造的价值，多人分享了通过在家庭服务器上运行模型和为定制需求 fork 开源项目而获得巨大生产力提升的个人经历。讨论揭示了对 LLM 能力的热情与对补贴定价可持续性、代码质量以及传统开源协作规范被侵蚀之间的矛盾。

**标签**: `#AI`, `#LLMs`, `#open-source`, `#tech-economics`, `#frontier-labs`

---

<a id="item-5"></a>
## [带状疱疹疫苗可能降低痴呆症风险](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 7.0/10

多项重复的观察性研究表明，带状疱疹疫苗可显著降低痴呆症风险，但社区讨论提出了重要担忧，即疫苗接种者就诊次数减少可能造成混杂偏倚。

hackernews · saikatsg · 7月12日 15:23 · [社区讨论](https://news.ycombinator.com/item?id=48881874)

**标签**: `#health`, `#dementia`, `#vaccines`, `#epidemiology`, `#neuroscience`

---

<a id="item-6"></a>
## [DeepSeek 据报道正在自研 AI 芯片以减少对美依赖](https://www.reddit.com/r/LocalLLaMA/comments/1uu15mz/chinas_deepseek_developing_its_own_ai_chip/) ⭐️ 7.0/10

中国人工智能公司 DeepSeek 据报道正在自研 AI 芯片，以减少在中美出口管制持续收紧背景下对美国半导体技术的依赖。这一举措标志着这家中国最具影响力的 AI 初创企业之一迈向了硬件自给自足的重要一步。 DeepSeek 自研 AI 芯片的努力可能会重塑 AI 硬件的竞争格局，尤其是如果它能成功生产出无需英伟达或 AMD 硬件即可训练和运行前沿模型的芯片。它同时也凸显了美国出口管制正在如何加速中国本土半导体能力的提升，具有广泛的地缘政治和供应链影响。 报道表明，DeepSeek 的芯片研发主要是由地缘政治约束驱动，而非纯粹的商业考量。开发具有竞争力的 AI 加速器需要先进的制程工艺，而由于 ASML 等公司先进光刻设备以及台积电等顶级晶圆厂的限制，这仍然是中国企业面临的主要瓶颈。

reddit · r/LocalLLaMA · /u/TheRealMasonMac · 7月12日 01:04

**背景**: DeepSeek 成立于 2023 年，总部位于杭州，其 R1 模型于 2025 年 1 月发布后全球瞩目，该模型据称能与美国顶级模型媲美，但训练成本仅为后者的零头。AI 加速器是专用芯片（如英伟达 H100 GPU），采用异构架构，针对深度学习所需的大规模并行计算进行了优化。自 2022 年以来，美国政府不断收紧对华先进半导体和芯片制造设备的出口管制，试图减缓中国在前沿 AI 领域的发展步伐。这些限制促使中国科技公司大力投资本土芯片设计和替代制造路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/articles/c5yv5976z9po">What is DeepSeek - and why is everyone talking about it?</a></li>
<li><a href="https://stealthcloud.ai/policy/us-export-controls-china/">US Semiconductor Export Controls on China ... — STEALTH CLOUD</a></li>

</ul>
</details>

**标签**: `#AI hardware`, `#DeepSeek`, `#semiconductors`, `#China tech`, `#export controls`

---

<a id="item-7"></a>
## [我在 Qwen3-4B 上的 7 个数据集中映射了 Anthropic 的 J-Space 幻觉信号，以找出它的有效范围与失效场景](https://www.reddit.com/r/LocalLLaMA/comments/1uu61wb/i_mapped_anthropics_jspace_hallucination_signal/) ⭐️ 7.0/10

一项严谨的实证评估，映射了 Anthropic 的 J-Space 内部熵信号在哪些场景下能成功检测幻觉，以及在哪些场景下仅使用输出 logprobs 便已足够，测试基于 Qwen3-4B 上的 7 个数据集完成。

reddit · r/LocalLLaMA · /u/dasjomsyeet · 7月12日 05:06

**标签**: `#hallucination-detection`, `#LLM-evaluation`, `#interpretability`, `#Anthropic`, `#empirical-study`

---

<a id="item-8"></a>
## [Ghostel：基于 libghostty 的全新 Emacs 终端模拟器](https://dakra.github.io/ghostel/) ⭐️ 6.0/10

Ghostel 是一款基于 libghostty-vt 构建的全新 Emacs 终端模拟器，libghostty-vt 是从 Ghostty 终端中提取的可嵌入终端引擎。它承诺比现有的 Emacs 终端模拟器（如 vterm 和 eat）提供更快的渲染速度和更可靠的输入处理。 这是 libghostty-vt 作为可嵌入库的首个实际应用案例，验证了 Mitchell Hashimoto 将 Ghostty 终端引擎开放给第三方应用的愿景。对于经常在 Emacs 中运行 TUI 应用程序或 Shell 的用户来说，它提供了一条从老旧的 vterm 升级的实质性路径。 Ghostel 利用 libghostty-vt 进行 VT 序列解析和状态管理，将繁重工作委托给原生 C/Zig 库，而非用 Emacs Lisp 解析转义序列。用户报告称每帧刷新的 TUI 应用程序现在可以流畅运行，但也注意到偶尔会出现终端清除不彻底和罕见冻结的问题。

hackernews · signa11 · 7月12日 08:52 · [社区讨论](https://news.ycombinator.com/item?id=48879504)

**背景**: Ghostty 是由 Mitchell Hashimoto 创建的一款快速、原生、GPU 加速的终端模拟器。其核心引擎 libghostty-vt 是一个零依赖的 C 和 Zig 库，负责解析 VT（虚拟终端）序列（如 ANSI 和 XTERM 转义码）、管理光标状态以及处理文本重排等复杂任务。Emacs 用户长期以来依赖 vterm（传统选择）和 eat（提供完整鼠标和剪贴板支持的新选择）等终端模拟器在 Emacs 缓冲区中运行 Shell 命令和 TUI 应用程序。通过将 libghostty-vt 嵌入 Emacs，Ghostel 绕过了基于 Emacs Lisp 的终端解析的局限性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://repo-explainer.com/ghostty-org/ghostling">Ghostling: Stripping the Terminal to its... — Repo Explainer</a></li>
<li><a href="https://akib.ami.bd/blog/introducing-eat.html">Introducing Eat: A New Terminal Emulator for Emacs | Akib Azmain Turja</a></li>

</ul>
</details>

**社区讨论**: 社区反馈总体非常积极，用户称赞相比 vterm 的显著性能提升和更简洁的 ELisp API。早期采用者强调了实际使用中的好处，例如 Codex 摘要中的代码引用可以直接在 Emacs 缓冲区中点击打开。然而，也有用户报告了终端清除不完整和偶尔冻结等瑕疵，表明该项目仍在完善中。

**标签**: `#emacs`, `#terminal-emulator`, `#libghostty`, `#developer-tools`, `#open-source`

---

<a id="item-9"></a>
## [Hunyuan3D 的 MLX 移植版在 Apple Silicon 上实现本地图像转 3D](https://www.reddit.com/r/LocalLLaMA/comments/1uuga40/local_image_to_3d_2gb_ram_20s_apple_silicon_iphone/) ⭐️ 6.0/10

开发者 ZimengXiong 发布了基于 MLX 的腾讯 Hunyuan3D-Paint 和 Hunyuan3D-Shape 模型开源移植版，并将其打包为独立的 macOS/iOS 应用 Modelr。在 M4 Max 上以 FP16 运行时，形状生成阶段约需 20–22 秒，峰值内存 5.6–7.3 GB；而贴图（paint）阶段则耗时 231–344 秒，占用内存高达 38–39 GB。 这是首个面向 Apple Silicon 的端到端图像转 3D 桌面应用，证明腾讯基于扩散模型的 3D 管线可以完全在本地设备上运行，无需 PyTorch 开销，使得普通 Mac 甚至 iPhone（通过量化）也能使用该技术。这降低了开发者在 Swift 应用中嵌入快速 3D 生成功能的门槛。 尽管帖子标题宣称「<2GB 内存」，但 FP16 基准测试显示形状推理需要 5.6–7.3 GB，贴图推理需要 38–39 GB；只有通过激进的 Q4 或 Q8 量化才能在较新的 Mac/iPhone 上实现低于 2 GB 的内存占用。该应用集成了 Apple 的 SwiftVision 进行背景移除，并能实时流式显示扩散进度，但贴图阶段的内存占用对大多数消费级硬件来说仍是重大限制。

reddit · r/LocalLLaMA · /u/arduinoRPi4 · 7月12日 14:00

**背景**: MLX is Apple's open-source array framework for machine learning on Apple Silicon, similar to NumPy/PyTorch but designed to take advantage of Apple's unified memory architecture and GPU. Hunyuan3D is Tencent's open-source suite for generating 3D meshes and textures from a single 2D image, consisting of a shape-generation diffusion model (Shape) and a texture-synthesis model (Paint) that supports both standard RGB and physically based rendering (PBR) workflows. PBR texturing simulates realistic light-material interaction, producing assets that look correct under varied lighting conditions but at significantly higher computational cost.

<details><summary>参考链接</summary>
<ul>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>
<li><a href="https://huggingface.co/spaces/tencent/Hunyuan3D-2">Hunyuan 3 D -2.0 - a Hugging Face Space by tencent</a></li>

</ul>
</details>

**标签**: `#image-to-3d`, `#apple-silicon`, `#mlx`, `#hunyuan3d`, `#on-device-ai`

---

<a id="item-10"></a>
## [Moondream 3.1：90 亿参数 MoE 视觉语言模型发布](https://www.reddit.com/r/LocalLLaMA/comments/1uunqcz/moondream319ba2b/) ⭐️ 6.0/10

Moondream 发布了 3.1 版本，这是一款采用混合专家（MoE）架构的开放权重视觉语言模型，总参数量为 90 亿，每次推理激活 20 亿参数。该模型原生支持 query、detect、point 和 caption 四种能力，且均返回结构化输出，并宣称在视觉推理和目标检测任务上达到业界领先水平。 在视觉语言模型中采用 MoE 架构目前仍较为少见，因此 Moondream 3.1 代表了一种值得关注的技术路线——通过每次仅激活一小部分参数，在能力与部署效率之间取得平衡。作为一款对检测和指向能力提供结构化输出的开放权重模型，它有望成为开发者在本地构建多模态定位应用的实用选择。 其中 'A2B' 后缀表示总参数量为 90 亿、激活参数为 20 亿，相比同等规模的稠密模型显著降低了推理计算成本，同时保留了更大网络的表征能力。query、detect、point 和 caption 四项能力均为模型原生内置，并非通过适配器或插件的方式额外添加。

reddit · r/LocalLLaMA · /u/secopsml · 7月12日 18:40

**背景**: 视觉语言模型（VLM）是一类以图像为输入并生成文本或结构化输出的多模态 AI 系统，Molmo 和 Qwen-VL 都是当前较知名的代表。混合专家（MoE）是一种通过门控网络将每个输入路由到部分专家子网络的架构，使得模型总参数量很大但每次推理的计算量较小，Mixtral 和 DeepSeek 是其在文本大模型领域的典型应用。"开放权重"指训练好的模型参数公开发布供下载，但与完全开源不同，训练代码和数据通常不会被公开。指向（pointing）能力在 VLM 中指输出像素坐标来定位图像中被引用的对象，从而实现与图像内容的实际交互。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mtiosavljevic.com/p/mixture-of-experts-the-architecture-revolutionizing-large-language-models/">Mixture of Experts : The Architecture Revolutionizing Large...</a></li>
<li><a href="https://www.bentoml.com/blog/multimodal-ai-a-guide-to-open-source-vision-language-models">Multimodal AI: The Best Open-Source Vision Language Models in 2026</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llms">Best Open - Source LLM Models in 2026: Coding, Local, Agentic AI...</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子的讨论较为有限，主要作为一条发布公告出现，社区中并未提供深入的技术细节或基准测试。提供的内容中也没有出现明显的分歧或反对意见。

**标签**: `#vision-language-model`, `#mixture-of-experts`, `#open-source`, `#multimodal-AI`, `#model-release`

---

<a id="item-11"></a>
## [Apple sues OpenAI alleging trade secret theft, says scheme was 'at every level'](https://www.reddit.com/r/LocalLLaMA/comments/1uus189/apple_sues_openai_alleging_trade_secret_theft/) ⭐️ 6.0/10

Apple has filed a lawsuit against OpenAI alleging systematic trade secret theft 'at every level' of the organization.

reddit · r/LocalLLaMA · /u/fallingdowndizzyvr · 7月12日 21:25

**标签**: `#legal`, `#openai`, `#apple`, `#trade-secrets`, `#ai-industry`

---

<a id="item-12"></a>
## [小米悄然在 Hugging Face 上传 MiMo-V2.5-DFlash 模型权重](https://www.reddit.com/r/LocalLLaMA/comments/1uu8d1v/xiaomi_quietly_uploaded_mimov25dflash_official/) ⭐️ 6.0/10

小米悄悄在 Hugging Face 上传了 MiMo-V2.5-DFlash 的模型权重，其中包含一个独立的 dflash 目录存放 DFlash 草稿模型，同时还有一个独立的 MTP（多 token 预测）模型。该 300B+ 参数的基础模型目前在双 24GB GPU 加显存卸载的情况下大约每秒可生成 8-10 个 token，DFlash 推测解码预计可将这一速度提升约一倍。 对于本地大模型爱好者来说，一个可用于 300B+ 参数基础模型的推测解码草稿模型，能显著提升消费级硬件上的推理速度，让原本难以运行的大模型在本地部署变得可行。这同时也表明小米等中国大型 AI 实验室正越来越多地投入面向社区推理栈的开源权重发布。 DFlash 与逐 token 的推测解码不同，它使用块扩散模型在单次前向传播中起草 K 个候选 token，并且该草稿模型作为独立训练的外部检查点提供，而非嵌入在基础模型中。原帖作者指出，该模型共享的 MTP head 目前在 llama.cpp 上还无法工作，因为运行时分不清 MTP 层，但 DFlash 可能绕过这个问题，这也是社区成员急切希望看到 GGUF 转换版本的原因。

reddit · r/LocalLLaMA · /u/nasone32 · 7月12日 07:11

**背景**: 推测解码是一种推理加速技术，它由一个小型"草稿"模型提议若干候选 token，再由大型基础模型并行验证，从而将自回归的逐 token 生成瓶颈转变为更快的"先草拟、再验证"流程。DFlash 是该方案的一种具体变体，它用块扩散模型取代逐 token 的草稿器，能够在单次前向传播中生成多个 token。MTP（多 token 预测）是另一个相关但不同的训练范式，DeepSeek-V3 等模型就采用了带有辅助头来预测多个未来 token 的方式，也可被改用于推测解码。GGUF 则是 llama.cpp 在本地 CPU 和消费级 GPU 上运行大模型的事实标准格式。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.datacamp.com/tutorial/how-to-speed-up-local-llms-with-dflash-speculative-decoding">How to Speed Up Local LLMs with DFlash Speculative Decoding</a></li>
<li><a href="https://www.spheron.network/blog/dflash-block-diffusion-speculative-decoding-gpu-cloud/">DFlash on GPU Cloud: 6x Faster LLM Inference with... | Spheron Blog</a></li>
<li><a href="https://nvidia.github.io/TensorRT-Edge-LLM/user_guide/examples/speculative-decoding.html">Speculative Decoding — TensorRT Edge-LLM</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子的讨论集中在技术层面的推测上，而非确定的基准测试结果：原帖作者和评论者都很兴奋但暂时无法把权重转成 GGUF，并争论共享的 MTP head 或新上传的独立 MTP 模型是否已经能在 llama.cpp 中跑通，比较一致的看法是 llama.cpp 在识别 MTP 层时存在困难。参与者希望独立的 DFlash 草稿模型才是真正为该基础模型解锁更快本地推理的途径。

**标签**: `#Xiaomi`, `#MiMo`, `#DFlash`, `#speculative-decoding`, `#local-llm`, `#huggingface`

---

<a id="item-13"></a>
## [三行代码修复 llama.cpp 在 Tesla P100 上存在多年的 fp16 精度 Bug](https://www.reddit.com/r/LocalLLaMA/comments/1uu6p9o/your_80_tesla_p100_has_been_doing_silently_noisy/) ⭐️ 6.0/10

一位开发者发现并发布了一个修复方案，解决了 llama.cpp 的 CUDA 后端中影响 Tesla P100 GPU（sm_60 架构）的一个长期存在的数值精度 Bug。P100 被错误地使用了快速 fp16 计算路径，尽管它需要更高精度，而基于 sm_61 的 GTX 10 系列和 P40 多年前就已被豁免。补丁仅三行代码，已在两个分支（turboquant v0.3.0 和 spiritbuun 的 buun-llama-cpp）中合并，GGML 上游也已提交了 Issue。 这个 Bug 在 P100 显卡上悄无声息地降低了推理质量——模型约有 1/29 的下一个 token 预测与全精度计算结果不同，但在实际工作负载中，快速路径并没有带来真正的性能提升。在当前 DRAM 价格危机中，二手 P100 售价仅约 80 美元，配备 16GB HBM2 和 732 GB/s 带宽，这一修复使 P100 成为本地 LLM 推理的极具性价比的选择，有望缩小其与 P40 之间长期被认为存在的质量差距。 在 Qwen3-27B 和 wikitext-2 上的基准测试显示，修复后 KL 散度从 0.0023 降至 0.000001（约 2300 倍精度提升），首 token 一致性从 96.5% 提升至 99.9%。解码吞吐反而快了约 1.4%，因为 P100 上的实际工作负载受 GEMM 和内存带宽限制，而非 fp16 向量路径。此修复仅影响 sm_60——Volta 及更新架构使用不同的计算内核，完全不受影响；Blackwell 构建产生位一致的困惑度结果，证实无附带影响。

reddit · r/LocalLLaMA · /u/apollo_mg · 7月12日 05:41

**背景**: llama.cpp 是一个流行的开源 C/C++ 库，用于在消费级硬件上本地运行大语言模型，支持 CPU 和 GPU（包括 CUDA）后端。NVIDIA GPU 通过计算能力版本（如 sm_60、sm_61）标识其底层架构；sm_60 对应 Pascal（P100），sm_61 对应 GTX 10 系列和 P40。CUDA 中的快速 fp16（半精度）计算路径以数值精度换取吞吐量，通常可以接受，但当模型依赖候选 token 之间细微的 logit 差异时，可能降低推理质量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/ llama . cpp : LLM inference in C/C++ · GitHub</a></li>
<li><a href="https://www.myzhar.com/blog/tutorials/tutorial-nvidia-gpu-cuda-compute-capability/">[Tutorial CUDA] Nvidia GPU : CUDA Compute Capability</a></li>
<li><a href="https://gist.github.com/CyberSys/9e65d4c7c92cc9d6fa12c7bae133ce50">CUDA GPU Compute Capability - Compatibility · GitHub</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#CUDA`, `#GPU-computing`, `#Tesla-P100`, `#numerical-precision`

---

<a id="item-14"></a>
## [Voodoo Quant 声称在 KLD 指标上超越 Unsloth Dynamic 2.0 达 95%](https://www.reddit.com/r/LocalLLaMA/comments/1uua3jd/voodoo_quant_beats_unsloth_dynamic_20_kld_by_95/) ⭐️ 6.0/10

一种名为 Voodoo Quant 的新型量化方法已发布，并在 Hugging Face 上提供了 Qwen3.5 0.8B 和 Qwen3.5 2B 的 GGUF 模型文件。作者声称 Voodoo Quant 通过采用逐张量（per-tensor）优化而非块级（block-level）优化，在 KLD 指标上比 Unsloth Dynamic 2.0 提升了 95%，并称 Voodoo 在 PyTorch 和 llama.cpp 两个后端上都表现得更一致。 如果经过独立验证，Voodoo Quant 有可能显著提升本地 LLM 部署中激进量化小型模型的质量，尤其是在消费级硬件上只能以低位宽运行较大模型的场景下。混合精度量化是将能力较强的模型塞进有限显存的核心技术，因此即使在 2-bit 级别上的小幅提升，也可能拓展用户在本地可运行的模型范围。 作者强调，95% 这一醒目数字部分反映了 Unsloth Dynamic 在 PyTorch 后端上 KLD 表现较差，而 Voodoo 在该后端仍保持竞争力；在 llama.cpp 上两者表现都不错，这意味着 Unsloth 的块级选择可能对 llama.cpp 的图结构存在过拟合。Voodoo 的最佳区间据称在 2-bit 左右，该技术据称在不同后端之间具有更好的可迁移性。目前上传的模型被描述为主要用于研究目的，27B 级别的更大模型被列为未来工作。

reddit · r/LocalLLaMA · /u/1ncehost · 7月12日 08:52

**背景**: 量化通过降低模型权重的数值精度（例如从 16-bit 降到 4-bit 或 2-bit）来压缩文件大小和显存占用，代价是一定的精度损失。GGUF 是 llama.cpp 用来分发和本地运行量化模型的文件格式，它将权重、分词器和元数据打包到单一的可移植文件中。Kullback–Leibler 散度（KLD）是衡量量化模型输出分布与全精度参考分布之间偏差的常用指标。逐张量（per-tensor）量化为整个权重张量分配一组 scale/zero-point，而逐块（per-block）或逐组（per-group）量化则将张量分成更小的块，每块拥有独立的参数，从而在存在离群值时实现更精细的适应 —— 代价是更多的元数据开销，并且可能对特定推理后端过拟合。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">llama.cpp - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/blog/model-quantization-concepts-methods-and-why-it-matters/">Model Quantization : Concepts, Methods, and Why It Matters</a></li>

</ul>
</details>

**标签**: `#quantization`, `#gguf`, `#qwen`, `#local-llm`, `#model-optimization`

---

<a id="item-15"></a>
## [交互式 Jacobian-Lens 工具将 Anthropic 可解释性技术引入 GGUF 模型](https://www.reddit.com/r/LocalLLaMA/comments/1uu32z6/interactive_jacobianlens_visualizer_and_live/) ⭐️ 6.0/10

一位社区开发者发布了 jlens-gguf，一个交互式 Jacobian-Lens 可视化和实时引导工具，将 Anthropic 的 J-Lens 可解释性技术适配到 llama.cpp 上运行的 GGUF 模型。该工具包含一个基于 llama.cpp 的原生 GGUF 服务器，支持稠密模型和 MoE 模型，可对量化模型进行观察、J-space 向量替换、abliteration 以及引导操控。 此前，Jacobian-Lens 可解释性工具仅支持 HuggingFace 和 PyTorch 工作流，使用 GGUF/llama.cpp 生态（通过 Ollama、LM Studio 等为数百万用户提供服务）的用户一直缺少对应的本地方案。该工具通过降低检查和操控模型内部状态的门槛，让前沿的可解释性研究可以被在消费级硬件上运行量化模型的开源社区所使用。 Lens 自身的内存开销大约为模型大小的 1/8，因此像 Qwen3.5-397B UD-Q3_K_XL 这种 160 GB 的模型大约需要额外 20 GB 内存来运行 Lens。该工具可以实时观察正在运行的 llama-server 模型，但引导操控（abliteration/向量替换）仅在使用其自带服务器时可用。

reddit · r/LocalLLaMA · /u/Responsible_Fig_1271 · 7月12日 02:37

**背景**: Jacobian Lens（J-Lens）是 Anthropic 提出的可解释性技术，用于揭示 Claude 内部一个低维的「J-space」，表征模型即将表达的概念，从而让研究者在模型「写下」之前就能读取其「想法」。GGUF 是由 llama.cpp 原生消费的量化模型文件格式，llama.cpp 是本地 LLM 推理领域占主导地位的引擎，其生态涵盖 Ollama、LM Studio、GPT4All 和 Jan.ai 等。Abliteration 是一种模型引导技术，源自 Arditi 等人 2024 年中期的研究，通过在模型的残差流中抹除单一方向来移除拒绝行为，无需重新训练，是残差流引导方法（还包括表征工程和 DARLING 式的新颖性引导）中的代表性手段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/what-is-j-lens-jacobian-lens-claude-interpretability-2026">What Is the J-Lens? Anthropic Jacobian Lens Guide | explainx.ai</a></li>
<li><a href="https://explainx.ai/blog/what-is-llama-cpp-run-models-locally-2026">What Is llama . cpp ? Run GGUF Models Locally | explainx.ai</a></li>
<li><a href="https://www.banandre.com/blog/abliteration-llm-slop-reduction-technique">Abliteration : Performing Brain Surgery on LLMs to Cure... - Banandre</a></li>

</ul>
</details>

**标签**: `#llama.cpp`, `#GGUF`, `#interpretability`, `#Anthropic`, `#model-steering`

---

<a id="item-16"></a>
## [Zer0Fit：将 Google TabFM 与 TimesFM 封装为本地方零样本机器学习的 MCP 服务器](https://www.reddit.com/r/LocalLLaMA/comments/1uudxi8/zer0fit_i_took_googles_new_tabfm_timesfm_ml/) ⭐️ 6.0/10

一位研究生开发了开源项目 Zer0Fit，将 Google 近期发布的 TabFM 和 TimesFM 基础模型封装进一个 Docker 容器，包装为 MCP 服务器，从而实现完全在本地运行零样本预测、分类和回归任务，只需一张显存 16GB 以上的 Nvidia GPU。 Zer0Fit 通过标准化的 MCP 协议暴露 Google 新发布的表格和时间序列基础模型，使开发者能够将零样本机器学习能力直接接入由 LLM 驱动的聊天工作流（Open WebUI、Claude Code、Codex CLI），无需编写定制训练流程或调试超参数，大幅降低了使用门槛。 初步基准测试显示，在 Iris 分类数据集上达到 94.7% 的准确率，在 California Housing 回归任务上 R² 达到 0.87，性能可与经过传统调参的机器学习模型相媲美。该项目基于 PyTorch，仅支持 CUDA（不支持 Mac），通过 5 分钟 TTL 动态加载与卸载模型以节省显存，目前支持 CSV 输入，XLS、XLSX、JSON、JSONL 格式即将推出。

reddit · r/LocalLLaMA · /u/Porespellar · 7月12日 12:18

**背景**: Google Research 近期推出了 TabFM——一种面向表格数据的零样本基础模型，本质上可视为「表格领域的 LLM」，无需在目标数据集上微调即可完成分类与回归任务；以及 TimesFM——一种基于解码器架构的时间序列预测基础模型，在 1000 亿个真实世界时间点上预训练（ICML 2024）。Model Context Protocol（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，使基于 LLM 的客户端（如 Claude Code 或 Open WebUI）能够以统一方式连接外部工具和数据源。Zer0Fit 正是立足于这两大趋势的交汇点，将 Google 的两个模型打包在统一的 MCP 接口之后。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM : A zero-shot foundation model for tabular data</a></li>
<li><a href="https://github.com/google-research/timesfm">google -research/ timesfm : TimesFM ( Time Series Foundation ...)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**标签**: `#MCP`, `#foundation-models`, `#zero-shot-learning`, `#local-llm`, `#time-series`, `#tabular-data`

---