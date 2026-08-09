---
layout: default
title: "Horizon Summary: 2026-08-09 (ZH)"
date: 2026-08-09
lang: zh
---

> 从 38 条内容中筛选出 12 条重要资讯。

---

1. [Lophius：面向语言模型研究的混合式工作台发布](#item-1) ⭐️ 7.0/10
2. [Google DeepMind 开源 WeatherNext 2 AI 气象预测模型](#item-2) ⭐️ 7.0/10
3. [独立验证确认 DeepSeek V4 Flash 在 Terminal-Bench 2.1 上取得 82.7% 成绩](#item-3) ⭐️ 7.0/10
4. [两个 vLLM 参数使 Ling-3.0-flash INT4 在 DGX Spark 上推理速度近翻倍](#item-4) ⭐️ 7.0/10
5. [AMD llama.cpp：减少 MTP 缓冲区开销，让 Qwen 27B 的上下文从 64K 提升到 149K](#item-5) ⭐️ 7.0/10
6. [CKA-QAD：在 NVFP4 大模型蒸馏中保留内部表征几何结构](#item-6) ⭐️ 7.0/10
7. [我如何利用大语言模型学习复杂主题](#item-7) ⭐️ 6.0/10
8. [开发者因抄袭开源应用「Dark Hours」并误导 John Gruber 发表空洞「道歉声明」](#item-8) ⭐️ 6.0/10
9. [稳定的 URI 不会改变 (1998)](#item-9) ⭐️ 6.0/10
10. [任意阶魔幻六边形均存在](#item-10) ⭐️ 6.0/10
11. [难怪 Qwen 和 Gemma 差异如此之大](#item-11) ⭐️ 6.0/10
12. [F2LLM 8B + Zerank 2 4B 在多语言嵌入+重排序基准测试中夺冠](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Lophius：面向语言模型研究的混合式工作台发布](https://www.reddit.com/r/LocalLLaMA/comments/1vjt4vi/lophius_a_workbench_for_language_model_research/) ⭐️ 7.0/10

Heretic 的作者 p-e-w 发布了 Lophius，这是一款运行在 notebook 中的混合式代码/GUI 研究工作台，涵盖几乎所有常见的 LLM 研究任务，包括模型检视、架构分析、tokenizer 检查、推理、logits、熵、注意力分数、隐藏状态以及对话功能。该项目可在 lophius.org 获取，源代码托管在 GitHub（github.com/p-e-w/lophius），据称是作者两年多来与 Jupyter 和 Transformers「搏斗」的结晶。 Lophius 直击 transformer 可解释性与行为研究中繁琐样板代码的工作流痛点，既能降低新手门槛，也能为有经验的研究者每个项目节省数小时时间。由于 p-e-w 是社区中备受信任的知名开源贡献者，该工具很可能被 r/LocalLLaMA 社区广泛采用，并有望成为未来更多工具的基础层——Heretic 未来也可能基于它构建。 该工作台在推理过程中能够智能管理 GPU 显存，并支持懒加载（lazy-loading）输出信号，研究者可以之后再进行检视，许多工作流无需任何配置即可使用。它附带高质量文档和完整的教程，同时在 Hugging Face 上以 lophius-org 组织开设了镜像账号，表明作者希望让语言模型研究变得人人可及。

reddit · r/LocalLLaMA · /u/-p-e-w- · 8月9日 15:43

**背景**: 语言模型研究工作台是一种集成环境，将研究者在探查 transformer 时反复执行的小步骤整合在一起——加载权重、检查 tokenizer 行为、运行推理，以及读取 logits、注意力分数和隐藏状态等中间信号。注意力分数衡量序列中每个 token 对其他所有 token 的「关注」程度，隐藏状态则是 transformer 各层产生的中间向量表示；两者都是机制可解释性与模型行为研究的核心。帖子中提到的 Heretic 是同一作者的另一个知名开源工具，专注于修改 LLM，因此 Lophius 代表着从「编辑模型」到「检视模型」的一个互补性转向。在 Jupyter 风格的 notebook 中运行，意味着研究者可以在同一环境中把 Lophius 的 GUI 组件与任意 Python 代码混合使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/p-e-w/lophius">Lophius: A workbench for language model research - GitHub</a></li>
<li><a href="https://huggingface.co/lophius-org">lophius-org (Lophius) - Hugging Face</a></li>

</ul>
</details>

**标签**: `#llm-research`, `#developer-tools`, `#open-source`, `#pytorch`, `#jupyter`

---

<a id="item-2"></a>
## [Google DeepMind 开源 WeatherNext 2 AI 气象预测模型](https://www.reddit.com/r/LocalLLaMA/comments/1vjwwrs/open_model_google_weather_next_2/) ⭐️ 7.0/10

Google DeepMind 开源了 WeatherNext 2，一个在《Nature》期刊上发表的 AI 气象预测模型，代码已在 GitHub 上发布。该模型比现有系统多出一天的气旋预测提前期——也就是说，它对三天的预测结果与此前模型两天的预测准确度相当。 传统的数值天气预报通常需要昂贵的超级计算机，而 WeatherNext 2 可以仅在单块 NVIDIA H100 GPU 上运行，这将高精度天气预报的访问门槛大幅降低。额外一天的飓风预测提前期具有直接的人道主义意义，能让社区和应急救援人员有更多时间对危险风暴做好准备。 WeatherNext 2 可以在不到一分钟的时间内生成数百种天气情景，其预测数据可通过 Google Earth Engine、BigQuery 以及 Google Cloud 上的 Vertex AI 获取。该模型将原本需要超级计算机的基础设施需求替换为单块 H100，使 AI 气象预测从专门的机构应用转向更广泛的研究与企业可访问性。

reddit · r/LocalLLaMA · /u/Rick_06 · 8月9日 18:12

**背景**: 天气预报传统上依赖数值天气预报（NWP），即在大型超级计算机上求解大气运动的物理方程——成本高昂，通常只有国家气象机构才能使用。以 DeepMind 早期的 GraphCast 以及现在的 WeatherNext 2 为代表，基于 AI 的气象模型利用机器学习（通常是图神经网络或 Transformer），在数十年的历史气象数据上进行训练，以更低的成本生成预报。NVIDIA H100 是基于 Hopper 架构的数据中心 GPU，广泛用于训练和运行大型 AI 模型；将预报模型从超级计算机迁移到单块 H100 上运行，代表着计算成本的显著降低。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/weathernext-2/">WeatherNext 2: Google DeepMind’s most advanced forecasting model</a></li>
<li><a href="https://deepmind.google/science/weathernext/">WeatherNext 2 — Google DeepMind</a></li>
<li><a href="https://developers.google.com/weathernext">WeatherNext | Google for Developers</a></li>

</ul>
</details>

**标签**: `#weather-forecasting`, `#google-deepmind`, `#open-source`, `#machine-learning`, `#scientific-research`

---

<a id="item-3"></a>
## [独立验证确认 DeepSeek V4 Flash 在 Terminal-Bench 2.1 上取得 82.7% 成绩](https://www.reddit.com/r/LocalLLaMA/comments/1vjklwo/deepseek_v4_flash_0731_hits_827_on_terminalbench/) ⭐️ 7.0/10

使用 Ante 0.preview.71 公开 harness 进行的独立测试确认了 DeepSeek 此前公布的 Terminal-Bench 2.1 82.7% 成绩——在 89 个任务上共进行 445 次试验，成功 368 次（标准误差 ±1.79），模型为通过 OpenRouter 调用的 deepseek-v4-flash-0731。完整的 Harbor 任务已公开，包含固定配置、reward、异常、用时与 token 使用情况在内的全部 445 条试验记录均可下载。 这一结果具有重要意义，因为 DeepSeek 最初的评测使用了尚未发布的"DeepSeek Harness minimal mode"，存在可复现性方面的疑虑。独立结果在严谨的统计条件下与官方数据吻合，证明第三方 harness 可以复现厂商公布的数据，同时揭示了 LLM 基准测试成绩对 harness 设计选择的敏感性。 测试在最大推理力度下、每个任务运行 5 次试验，并禁用了所有 skills，作者也披露了自己是 Ante 的创建者。445 次试验给出 ±1.79 的标准误差，统计上具有足够的支撑力；而公开的 Harbor 工件允许任何人查看或重新运行完全相同的配置。

reddit · r/LocalLLaMA · /u/Exciting-Camera3226 · 8月9日 08:39

**背景**: Terminal-Bench 2.1 是一项通过终端交互来评估 AI 智能体完成长时间跨度、真实任务能力的基准，是衡量前沿模型"终端使用能力"的关键指标。Harbor 是 Terminal-Bench 团队创建的沙箱化智能体任务框架，可通过 `uv tool install harbor` 安装，并与 LiteLLM 集成以访问众多 LLM 提供商。LLM 评测 harness——负责协调 prompt、工具调用和评分的软件——会显著影响所公布的成绩，这就是为什么 Ante 这类可复现、开放的 harness 对社区而言非常重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.harborframework.com/">Harbor</a></li>
<li><a href="https://www.vellum.ai/llm-leaderboard">LLM Leaderboard 2026</a></li>
<li><a href="https://docs.litellm.ai/docs/projects/Harbor">Harbor | liteLLM</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#benchmark-evaluation`, `#Terminal-Bench`, `#LLM-evaluation`, `#reproducibility`

---

<a id="item-4"></a>
## [两个 vLLM 参数使 Ling-3.0-flash INT4 在 DGX Spark 上推理速度近翻倍](https://www.reddit.com/r/LocalLLaMA/comments/1vjttcc/two_flags_took_the_official_ling30flash_int4_from/) ⭐️ 7.0/10

两项 vLLM 配置变更——移除 --enforce-eager 以启用 CUDA graphs，以及通过 --speculative-config 启用 method 为 'bailing_hybrid_v3_mtp' 的 MTP 投机解码——使官方 Ling-3.0-flash INT4 在单台 NVIDIA DGX Spark 上的推理速度从 20.8 提升至 38.7 tok/s，同时支持完整的 256K 上下文窗口，速度超过了社区 GGUF 的 35.2 tok/s。发帖者在 inclusionAI 从事 Ling 相关工作，他同时发出关键警告：原版 vLLM 缺少对 V3 注意力的正确支持，会静默地产生错误输出，用户必须使用 inclusionAI 的 vllm-ling-v3 分支（ling_3_0 分支）才能避免该问题。 这为拥有 DGX Spark 并运行 inclusionAI 的 Ling-3.0-flash 模型的用户提供了一个可直接采用的方案，仅通过参数调优即可获得近 2 倍的加速，同时揭示了一个严重的可靠性隐患，可能导致生产环境中静默的输出错误。它也凸显了厂商特定模型架构（如 V3 注意力机制）与 vLLM 等开源推理框架之间支持滞后的更广泛矛盾。 MTP 草稿层已内嵌在模型权重中（无需额外加载草稿模型），投机解码仅需将 num_speculative_tokens 设为 1 即可启用。作者指出，在约 30K 上下文以内 INT4 是最快的选择，而在长上下文场景下社区 Q5 GGUF 的衰减更为平滑。配套仓库（sudoingX/dgx-spark-ling）提供了启动脚本、用于冷启动分片冻结的 watchdog、基准测试方法以及详细的 FINDINGS.md 文档。

reddit · r/LocalLLaMA · /u/AcanthisittaOk1699 · 8月9日 16:10

**背景**: NVIDIA DGX Spark 是基于 Grace Blackwell 架构构建的桌面级 AI 工作站，配备 128 GB 统一内存和约 1 PetaFLOP 的算力。vLLM 是主流的开源高吞吐量 LLM 推理引擎，而 CUDA graphs（通过移除 --enforce-eager 来启用）通过重放已捕获的 kernel 序列来降低每次启动的 CPU 开销，避免每步重新构建。投机解码（包括 MTP，即 Multi-Token Prediction）通过让小型'草稿'模型预测候选 token，再由主模型批量验证来加速推理；MTP 变体直接复用主模型权重中的预测头，无需加载独立的草稿模型。DeepSeek 风格的 V3 架构使用了特殊的注意力路径，可能与上游 vLLM 的默认实现不一致，这就是为什么这里需要使用厂商定制分支来保证正确性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nvidia.com/en-us/products/workstations/dgx-spark/">Personal AI Supercomputer Powered by Blackwell | NVIDIA DGX Spark</a></li>
<li><a href="https://lmstudio.ai/docs/app/advanced/speculative-decoding">Speculative Decoding | LM Studio</a></li>
<li><a href="https://localllm.in/blog/mtp-lm-studio">Multi-Token Prediction ( MTP ) LM Studio Tutorial - Boost... | LocalLLM.in</a></li>
<li><a href="https://deepwiki.com/vllm-project/vllm-project.github.io/7.1-deepseek-model-family">DeepSeek Model Family | vllm-project/vllm-project.github.io ...</a></li>

</ul>
</details>

**标签**: `#vllm`, `#inference-optimization`, `#dgx-spark`, `#speculative-decoding`, `#model-correctness`

---

<a id="item-5"></a>
## [AMD llama.cpp：减少 MTP 缓冲区开销，让 Qwen 27B 的上下文从 64K 提升到 149K](https://www.reddit.com/r/LocalLLaMA/comments/1vjmay5/amd_llamacpp_reducing_mtp_buffer_overhead_gave_me/) ⭐️ 7.0/10

一个针对 llama.cpp 的补丁，修正了被高估的 MTP 缓冲区分配问题，在使用双卡（16GB + 12GB）的 AMD ROCm 平台上，将 Qwen 27B 的可用上下文长度近乎翻倍（例如从 64K 提升至 149K）。

reddit · r/LocalLLaMA · /u/ea_man · 8月9日 10:21

**标签**: `#llama.cpp`, `#AMD`, `#ROCm`, `#context-length`, `#optimization`, `#local-llm`

---

<a id="item-6"></a>
## [CKA-QAD：在 NVFP4 大模型蒸馏中保留内部表征几何结构](https://www.reddit.com/r/LocalLLaMA/comments/1vk08zl/260605682_beyond_output_matching_preserving/) ⭐️ 7.0/10

一篇新论文（arXiv 2606.05682）指出，针对 NVFP4 大语言模型的标准 KL 散度量化感知蒸馏（QAD）虽然能保持输出分布，却会悄然破坏模型内部的逐层表征。作者提出了 CKA-QAD 方法，通过在蒸馏过程中加入轻量级的 CKA 正则化项，将量化学生模型的逐层 Gram 矩阵与 BF16 教师模型对齐，并在 Nemotron 3 Nano 和 Qwen3-4B-Thinking-2507 上进行了验证。 随着大语言模型在延迟与成本受限的生产环境中大规模部署，NVFP4 推理正成为 NVIDIA Blackwell 硬件上的标配，量化感知蒸馏（QAD）成为恢复精度损失的关键。仅依赖输出匹配会掩盖严重的内部表征漂移，尤其是对于本身就较脆弱的 RL 后训练模型，这一发现对生产环境的精度和推理可靠性具有直接影响。 该方法使用居中核对齐（CKA）来量化表征漂移，仅增加少量训练开销即可显著提升推理与代码任务的准确率。研究发现，RL 后训练模型遭受的逐层漂移尤为严重，并且这种漂移与推理和代码基准测试中的下游性能瓶颈相关。

reddit · r/LocalLLaMA · /u/Aaaaaaaaaeeeee · 8月9日 20:22

**背景**: NVFP4 是 NVIDIA 为 Blackwell 架构推出的 4 位浮点格式，采用两级微缩放方案（细粒度 E4M3 加一个 FP32 缩放因子），以在超低精度下保持模型精度。量化感知蒸馏（QAD）通过 KL 散度损失让量化后的学生模型在输出 logits 上模仿全精度教师模型，从而帮助恢复低比特量化带来的精度损失。居中核对齐（CKA）是一种基于核函数的相似度度量方法，通过分析居中 Gram 矩阵来比较神经网络或各层之间的内部激活模式，广泛应用于表征诊断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>
<li><a href="https://arxiv.org/abs/1905.00414">[1905.00414] Similarity of Neural Network Representations ... Similarity of Neural Network Representations Revisited Centered Kernel Alignment (CKA) Overview - emergentmind.com Centered Kernel Alignment (CKA) in Detail | Neha Verma Centered Kernel Alignment (CKA) Similarity - emergentmind.com Centered Kernel Alignment (CKA) Demystified: From Theory to ... Similarity of Neural Network Representations Revisited</a></li>
<li><a href="https://research.nvidia.com/labs/nemotron/files/NVFP4-QAD-Report.pdf">Quantization-Aware Distillation for NVFP4 Inference Accuracy ...</a></li>

</ul>
</details>

**标签**: `#quantization`, `#NVFP4`, `#knowledge-distillation`, `#LLM`, `#low-precision-inference`

---

<a id="item-7"></a>
## [我如何利用大语言模型学习复杂主题](https://laurentiugabriel.github.io/blog/articles/how-i-use-llms-to-learn/) ⭐️ 6.0/10

一份实用指南，介绍如何借助大语言模型（结合可视化动画和结构化笔记）来学习复杂的技术主题，引发了关于 AI 辅助学习的优势与局限的讨论。

hackernews · laurentiurad · 8月9日 19:16 · [社区讨论](https://news.ycombinator.com/item?id=49234675)

**标签**: `#LLMs`, `#learning`, `#education`, `#AI-tools`, `#productivity`

---

<a id="item-8"></a>
## [开发者因抄袭开源应用「Dark Hours」并误导 John Gruber 发表空洞「道歉声明」](https://blog.terrygodier.com/2026/08/09/mea-culpa-dark-hours.html) ⭐️ 6.0/10

一名开发者的占星/塔罗应用被苹果 App Store 拒绝后，发布了一款几乎逐字复制的开源天文应用「Dark Hours」的克隆版本——甚至连名字都照搬——并误导知名科技记者 John Gruber 在不知情的情况下撰写了一篇关于苹果审核流程的文章。事件曝光后，该开发者发表了「mea culpa」（我的过错）博客声明，但批评者认为该声明未向 Gruber 正式道歉，也没有真正承担责任。 该事件暴露了 AI 辅助软件开发中的抄袭问题、科技新闻业在面对误导性信息源时的公信力问题，以及开源归属的伦理责任。同时也引发了更深层的质疑：开发者是否可以合乎情理地将逐字复制整个项目（包括名称和 bug）的责任推给 AI 工具。 原版「Dark Hours」是一款免费开源的天文摄影规划应用，托管在 darkhours.app，提供月相、天气和光污染预报功能。苹果 App Store 禁止占星类应用，这正是开发者最初被拒的原因。John Gruber 随后在 Daring Fireball 上撤回了相关文章。被抄袭的克隆版本据称不仅复刻了内容，甚至连原版中的某些特定 bug 都原样保留了下来。

hackernews · satvikpendem · 8月9日 13:20 · [社区讨论](https://news.ycombinator.com/item?id=49231154)

**背景**: 苹果 App Store 长期以来对某些内容类别执行严格政策，包括禁止占星类应用，这促使部分开发者试图通过重新包装或伪装其应用来规避审核。John Gruber 是最具影响力的苹果领域科技记者之一，其博客 Daring Fireball 被开发者和苹果爱好者广泛阅读，因此在该平台上的更正或撤稿声明格外引人注目。「Dark Hours」是一款开源项目，其源代码在许可协议下公开，并要求复用时注明出处——而克隆版本显然违反了这些条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://darkhours.app/">DarkHours — Dark Sky & Astrophotography Planner</a></li>
<li><a href="https://www.linkedin.com/pulse/what-happened-dark-hours-open-source-alternative-revealed-yogesh-b-js6kc">What Happened to Dark Hours? Open Source Alternative Revealed</a></li>

</ul>
</details>

**社区讨论**: 社区舆论普遍持怀疑和批评态度。评论员广泛驳斥开发者将抄袭归咎于 AI 的说法，一位用户讽刺地评论道：「那个可怕的大 AI 让你连名字都照抄了。」其他人指出，这份「mea culpa」甚至没有提及 John Gruber，更遑论向他为误导行为道歉。一位评论员援引公关术语「limited hangout」（有限曝光策略，即在掩盖方案失败后只承认部分丑闻以控制损失）来形容这份道歉，认为它本质上是危机公关，而非真诚的悔过。

**标签**: `#app-store`, `#plagiarism`, `#open-source`, `#ai-ethics`, `#tech-journalism`

---

<a id="item-9"></a>
## [稳定的 URI 不会改变 (1998)](https://www.w3.org/Provider/Style/URI) ⭐️ 6.0/10

这是 1998 年 W3C 关于持久 URI 重要性的经典文章，伴随 HN 讨论中关于现实中断链接及现代缓解措施（如重定向）的重新审视。

hackernews · Klaster_1 · 8月9日 14:32 · [社区讨论](https://news.ycombinator.com/item?id=49231809)

**标签**: `#web-architecture`, `#uri-design`, `#http`, `#link-rot`, `#classic`

---

<a id="item-10"></a>
## [任意阶魔幻六边形均存在](https://gukov.dev/math/2026/08/02/new-magic-hexagons.html) ⭐️ 6.0/10

一项数学探索，证明了任意阶魔幻六边形都存在，并引入了一种优雅的势场技术来求解这一组合难题。

hackernews · gukoff · 8月9日 07:19 · [社区讨论](https://news.ycombinator.com/item?id=49229174)

**标签**: `#mathematics`, `#combinatorics`, `#algorithms`, `#optimization`, `#puzzles`

---

<a id="item-11"></a>
## [难怪 Qwen 和 Gemma 差异如此之大](https://www.reddit.com/r/LocalLLaMA/comments/1vjb15v/no_wonder_qwen_and_gemma_are_so_different/) ⭐️ 6.0/10

有用户观察到，Qwen 将 330 行 HTML/JS 代码分词为 1609 个标记，而 Gemma 则需 4258 个标记。这表明分词效率的差异解释了为何 Qwen 擅长编码任务，而 Gemma 在语言任务上表现更强。

reddit · r/LocalLLaMA · /u/WhoRoger · 8月9日 00:04

**标签**: `#tokenization`, `#qwen`, `#gemma`, `#llm`, `#code-models`

---

<a id="item-12"></a>
## [F2LLM 8B + Zerank 2 4B 在多语言嵌入+重排序基准测试中夺冠](https://www.reddit.com/r/LocalLLaMA/comments/1vjk57h/best_embedding_reranking_model/) ⭐️ 6.0/10

一位 Reddit 用户对多种嵌入模型与重排序模型组合进行了基准测试，用于跨 15 种语言的翻译记忆 RAG 场景，结果显示 F2LLM V2 8B 与 Zerank 2 4B 的组合表现最佳，MRR 达到 0.922，Recall@20 达到 99.20%，超越了更大的商业 API 以及其他开源组合。 该基准测试为构建多语言 RAG 系统的从业者提供了实用的对比参考，尤其针对翻译记忆这类依赖跨语言语义匹配的应用场景。F2LLM 和 Zerank 2 完全开源（包括许可证、数据和代码），使得这一顶级组合在生产部署中无需 API 费用，格外具有吸引力。 所有本地模型均在 Llama CPP 上以 Q8_0 量化精度运行；作者指出，将 F2LLM V2 从 4B 升级到 8B 仅带来微弱的 MRR 提升（0.919 → 0.922），不值得为此付出额外的延迟代价。Zerank 2 此前采用非宽松许可证，最近在 Notion 收购 Zeroentropy 后转为开源。

reddit · r/LocalLLaMA · /u/seamonn · 8月9日 08:10

**背景**: 嵌入模型将文本转换为稠密向量表示，以便通过相似度搜索检索语义相近的段落；重排序模型则对初步候选集进行重新排序以提高精度。RAG（检索增强生成）系统将此类检索流程与语言模型结合，将输出锚定在外部知识上。翻译记忆系统存储已翻译的片段，依赖跨语言语义匹配来推荐已有译文。MRR（平均倒数排名）衡量首个正确答案的排名位置，Recall@20 则衡量正确答案是否出现在前 20 个检索结果中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/codefuse-ai/CodeFuse-Embeddings/blob/main/F2LLM/README.md">CodeFuse-Embeddings/F2LLM/README.md at main - GitHub</a></li>
<li><a href="https://huggingface.co/zeroentropy/zerank-2-reranker">zeroentropy/ zerank - 2 -reranker · Hugging Face</a></li>
<li><a href="https://medium.com/@rajnish_khatri/retrieval-metrics-tutorial-recall-k-and-mrr-explained-d2f12afb9c89">Retrieval Metrics Tutorial: Recall@k and MRR Explained</a></li>

</ul>
</details>

**标签**: `#RAG`, `#embedding-models`, `#reranking`, `#benchmarks`, `#multilingual`

---