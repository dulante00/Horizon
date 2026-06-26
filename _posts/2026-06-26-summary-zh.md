---
layout: default
title: "Horizon Summary: 2026-06-26 (ZH)"
date: 2026-06-26
lang: zh
---

> 从 58 条内容中筛选出 10 条重要资讯。

---

1. [OpenAI 预览 GPT-5.6 Sol，Cerebras 版本达 750 tokens/秒](#item-1) ⭐️ 8.0/10
2. [美国政府将决定谁可以使用 GPT-5.6](#item-2) ⭐️ 8.0/10
3. [Springer Nature 撤回了马克斯·普朗克研究所的两项研究](#item-3) ⭐️ 7.0/10
4. [混合模型在哪些词元上预测得更好？](#item-4) ⭐️ 7.0/10
5. [将智能体工作流蒸馏到小型语言模型权重，成本降低百倍](#item-5) ⭐️ 7.0/10
6. [crewAIInc/crewAI 发布了 1.15.0 版本](#item-6) ⭐️ 6.0/10
7. [一条命令在 HuggingFace Jobs 上部署 vLLM 推理服务器](#item-7) ⭐️ 6.0/10
8. [OpenRouter 推出面向编码 Agent 的 MCP 服务器](#item-8) ⭐️ 6.0/10
9. [一个用于强化学习奖励函数的调试器，可在训练期间检测奖励黑客 (P)](#item-9) ⭐️ 6.0/10
10. [CALHippo：基于机器学习管道的人脑海马体脑细胞三维映射](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [OpenAI 预览 GPT-5.6 Sol，Cerebras 版本达 750 tokens/秒](https://openai.com/index/previewing-gpt-5-6-sol/) ⭐️ 8.0/10

OpenAI 预览了 GPT-5.6 Sol，其中包括一个由 Cerebras 托管、可达每秒 750 tokens 的变体，初步仅向特定客户开放，容量将在七月逐步扩展。此外，OpenAI 还发布了相关的部署安全系统卡。 在专用硬件上以每秒 750 tokens 的速度运行前沿级别的模型，是推理速度方面的一个重要里程碑，可能改变实时编程助手和智能体工作流等对延迟敏感的应用场景。此次发布还表明 OpenAI 愿意与非英伟达（NVIDIA）芯片厂商合作，进一步拓展了顶级 AI 部署的硬件生态。 每秒 750 tokens 的速度是在 Cerebras 的晶圆级硬件上实现的，其 WSE-3 芯片面积为 46,225 平方毫米，包含 4 万亿晶体管，是有史以来最大的 AI 芯片。社区用户对价格的观察显示，OpenAI 仍在延续每一代模型都提高单 token 价格的模式（例如据称名为 'Luna' 的版本定价为 $1/$6），迫使用户迁移到更新、更昂贵的层级，而旧版本则被淘汰。

hackernews · OpenAI Blog · 6月26日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=48689028)

**背景**: Cerebras Systems 生产晶圆级 AI 加速器，这是一种尺寸异常巨大的单芯片处理器，旨在最大化片上内存带宽并减少芯片间通信，与英伟达的 GPU 集群形成鲜明对比。Tokens per second（TPS，即每秒生成的 token 数）是衡量大语言模型推理吞吐量的标准指标，受模型大小、硬件架构、量化和批处理占用率等因素影响。前沿模型要实现每秒数百 tokens 的推理速度，历来受限于内存带宽和互连瓶颈，而像 Cerebras 这样的专用加速器正是为了缓解这些限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://www.cerebras.ai/chip">Product - Chip - Cerebras</a></li>
<li><a href="https://flo2.com/blog/fastest-llm-inference">Fastest LLM Inference : What Makes Models Fast & How to Get It — flo 2</a></li>

</ul>
</details>

**社区讨论**: Hacker News 的评论者认为 Cerebras 速度里程碑是本次发布中最值得关注的部分；也有人对定价趋势表示担忧，认为每一代新模型价格都在上涨，而旧层级则被停用，实际上迫使用户升级。多位用户称赞 GPT 模型在编程方面的质量，并至少有一人指出 5.6 版本的行为可能在过去一天中已经悄悄推送给部分 5.5 用户。此外，还有一个单独的讨论帖用于讨论政策和政府访问相关话题。

**标签**: `#OpenAI`, `#GPT-5.6`, `#AI-models`, `#inference-speed`, `#Cerebras`

---

<a id="item-2"></a>
## [美国政府将决定谁可以使用 GPT-5.6](https://www.washingtonpost.com/technology/2026/06/26/openai-says-us-government-will-vet-users-its-latest-ai-model/) ⭐️ 8.0/10

据报道，OpenAI 要求 GPT-5.6 的用户必须接受美国政府的审查，这引发了人们对监管俘获、访问不平等以及开源人工智能未来的重大担忧。

hackernews · alain94040 · 6月26日 18:23 · [社区讨论](https://news.ycombinator.com/item?id=48690101)

**标签**: `#AI policy`, `#regulation`, `#OpenAI`, `#GPT-5`, `#government oversight`, `#regulatory capture`

---

<a id="item-3"></a>
## [Springer Nature 撤回了马克斯·普朗克研究所的两项研究](https://www.science.org/content/article/why-have-papers-one-history-s-most-famous-physicists-been-retracted) ⭐️ 7.0/10

Springer Nature 通过自动化流程撤回了马克斯·普朗克研究所的两项研究，将它们替换为空白页面，但仍对空白 PDF 收取 39.95 美元的费用，这引发了人们对学术出版中算法决策的担忧。

hackernews · adharmad · 6月26日 14:10 · [社区讨论](https://news.ycombinator.com/item?id=48686834)

**标签**: `#academic-publishing`, `#research-integrity`, `#springer-nature`, `#retraction`, `#open-access`

---

<a id="item-4"></a>
## [混合模型在哪些词元上预测得更好？](https://huggingface.co/blog/allenai/hybrid-token-prediction) ⭐️ 7.0/10

AllenAI 分析了结合自回归和扩散方法的混合模型，以确定每种组件分别在哪些词元上预测效果更佳，为混合架构设计提供了参考。

rss · HuggingFace Blog · 6月25日 16:11

**标签**: `#hybrid-models`, `#token-prediction`, `#language-models`, `#model-analysis`, `#allenai`

---

<a id="item-5"></a>
## [将智能体工作流蒸馏到小型语言模型权重，成本降低百倍](https://www.reddit.com/r/MachineLearning/comments/1ufgpnh/r_compiling_agentic_workflows_into_llm_weights/) ⭐️ 7.0/10

一篇新近被讨论的研究论文表明，通过在前沿大模型的执行轨迹上进行监督微调（SFT），可以将由前沿大模型编排的智能体工作流蒸馏到小型语言模型（SLM）的权重中，以约两个数量级（约 100 倍）的更低成本实现接近前沿水平的质量。 这一研究意义重大，因为前沿大模型的按 token 计费是主要的运营成本，企业正在积极寻求在不牺牲质量的前提下降低推理成本的方法。如果智能体能力能够被有效编译到紧凑的模型权重中，可能会从根本上改变大规模部署 AI 智能体的经济模型，使成本敏感型应用也能实现全天候运行的智能体系统。 该方法使用在前沿模型编排生成的轨迹上进行监督微调（SFT），而非传统的输出到输出的蒸馏方式——IBM 的资料指出后者在非智能体工作流中历来效果较差。该论文针对的是小型语言模型（SLM），其每次推理成本可大幅降低，但训练分布之外以及轨迹未覆盖的任务上的真实泛化能力仍是关键未解问题。

reddit · r/MachineLearning · /u/ThirdWaveCat · 6月25日 17:31

**背景**: 智能体工作流（agentic workflows）指的是由大语言模型自主决定控制流程的多步骤 AI 系统——包括调用工具、发起 API 请求和迭代执行——以完成超越简单单轮交互的复杂任务。
小型语言模型（SLM）是指参数量通常在 100 亿以下、运行成本更低但能力通常不如前沿模型的紧凑型模型。
模型蒸馏（model distillation）是指训练一个较小的模型来复制较大模型行为的过程；当应用于智能体系统时，其目标是捕获推理和工具使用模式，而不仅仅是最终答案。
基于前沿模型轨迹的监督微调（SFT）是一种特定的蒸馏策略，即学生模型学习模仿教师模型的完整逐步行为。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-workflows">What are Agentic Workflows? | IBM</a></li>
<li><a href="https://www.distillabs.ai/blog/using-custom-slms-in-agentic-ai/">distil labs: Small Models, Big Wins – Using SLMs in Agentic AI — distil labs</a></li>
<li><a href="https://github.com/Nardien/agent-distillation">GitHub - Nardien/agent-distillation: Official Code Repository for the paper "Distilling LLM Agent into Small Models with Retrieval and Code Tools" · GitHub</a></li>

</ul>
</details>

**标签**: `#llm`, `#model-distillation`, `#fine-tuning`, `#agentic-workflows`, `#cost-optimization`

---

<a id="item-6"></a>
## [crewAIInc/crewAI 发布了 1.15.0 版本](https://github.com/crewAIInc/crewAI/releases/tag/1.15.0) ⭐️ 6.0/10

crewAI 1.15.0 新增了声明式流程支持、用于业务流程建模的 DMN 模式，改进了对话流程的 CLI TUI，增强了遥测功能，并包含多项安全性和错误修复。

github · lorenzejay · 6月25日 23:17

**标签**: `#crewAI`, `#AI-agents`, `#multi-agent-systems`, `#framework-release`, `#LLM`

---

<a id="item-7"></a>
## [一条命令在 HuggingFace Jobs 上部署 vLLM 推理服务器](https://huggingface.co/blog/vllm-jobs) ⭐️ 6.0/10

HuggingFace 发布了一篇指南，演示如何通过一条命令在其 Jobs 平台上启动 vLLM 推理服务器。这将 vLLM 高吞吐量 LLM 服务引擎与 HuggingFace 托管的计算基础设施相结合，实现了简化的部署流程。 该集成降低了开发者大规模部署 LLM 服务的门槛，使其无需配置和管理自己的 GPU 基础设施。它反映了行业向交钥匙式 AI 部署解决方案发展的更广泛趋势，将基础设施复杂性抽象化。 该设置利用 HuggingFace Jobs 的类 Docker 接口，用户可以指定容器镜像和在可配置 GPU 或 TPU 硬件上执行的运行命令。它本质上是一个便利的封装器，将两个成熟的现有工具结合在一起，而非引入新技术。

rss · HuggingFace Blog · 6月26日 00:00

**背景**: vLLM 是一个最初在 UC Berkeley Sky Computing Lab 开发的开源 LLM 推理和服务库，以通过 PagedAttention、连续批处理和 CUDA/HIP 图优化等技术实现高吞吐量而闻名。HuggingFace Jobs 是 HuggingFace Hub 上的托管计算服务，在云端 GPU 和 TPU 上运行基于 Docker 的 AI 和数据工作负载，支持微调、批量推理和可复现的基准测试等用例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/">vLLM</a></li>
<li><a href="https://huggingface.co/docs/hub/jobs">Jobs · Hugging Face</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#HuggingFace`, `#LLM-inference`, `#deployment`, `#cloud-compute`

---

<a id="item-8"></a>
## [OpenRouter 推出面向编码 Agent 的 MCP 服务器](https://openrouter.ai/blog/announcements/openrouter-mcp-server/) ⭐️ 6.0/10

OpenRouter 推出了一个 MCP（Model Context Protocol）服务器，使编码 Agent 能够在编辑器内直接访问其实时模型目录、基准测试、文档和推理测试功能。这让 AI 编码助手可以在开发者不离开开发环境的前提下与 OpenRouter 平台进行交互。 此次集成简化了使用 AI 编码 Agent 的开发者的工作流程，使其能够在不切换上下文的情况下发现、评估和测试 OpenRouter 聚合的数百个 LLM。随着 MCP 成为连接 AI 助手与外部工具和数据源的事实标准，OpenRouter 的采用使其处于不断壮大的 AI 编码 Agent 生态系统的中心位置。 该 MCP 服务器提供对 OpenRouter 统一接口的访问，该接口可在多个模型提供商之间路由请求，帮助开发者避免供应商锁定并降低服务中断风险。编码 Agent 可以通过编程方式查询基准测试和文档，从而在开发过程中做出更明智的模型选择。

rss · OpenRouter Blog · 6月25日 00:00

**背景**: Model Context Protocol（MCP）是 Anthropic 于 2024 年 11 月推出的开放标准，旨在规范 LLM 等 AI 系统与外部工具、数据源和开发环境的集成方式。OpenRouter 是一个统一的 LLM 路由平台，聚合了来自不同提供商的数百个模型，为开发者提供单一 API 来访问不同的 AI 模型，同时避免供应商锁定。MCP 与 OpenRouter 模型聚合服务的结合，为 AI 编码 Agent 创造了一个强大的工具发现层。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>

</ul>
</details>

**标签**: `#MCP`, `#OpenRouter`, `#coding-agents`, `#LLM-infrastructure`, `#developer-tools`

---

<a id="item-9"></a>
## [一个用于强化学习奖励函数的调试器，可在训练期间检测奖励黑客 (P)](https://www.reddit.com/r/MachineLearning/comments/1uga687/a_debugger_for_rl_reward_functions_that_detects/) ⭐️ 6.0/10

一个名为'rewardspy'的开源调试库，它通过封装强化学习奖励函数，在 GRPO 训练过程中监控方差坍缩、组件不平衡和分组坍缩等指标，从而检测奖励黑客行为。

reddit · r/MachineLearning · /u/BaniyanChor · 6月26日 15:34

**标签**: `#reinforcement-learning`, `#reward-hacking`, `#GRPO`, `#debugging-tools`, `#RLHF`

---

<a id="item-10"></a>
## [CALHippo：基于机器学习管道的人脑海马体脑细胞三维映射](https://www.reddit.com/r/MachineLearning/comments/1uf8thw/calhippo_mapping_neurons_and_glial_cells_in_the/) ⭐️ 6.0/10

团队开发了 CALHippo 管道（已被 MICCAI 2026 接收），利用 CellPoseSAM 和自定义分割模型对高分辨率海马体切片中的神经元（兴奋性/抑制性）和胶质细胞进行分类，然后训练小型 UNet 进行密度估计，将这些标注映射到低分辨率切片上，最终重建出与解剖学 Cornu Ammonis（CA）区域对齐的整个海马体三维点云。 这项工作通过在 20 倍分辨率差距之间智能传递信息，弥合了细胞级精细标注与全器官尺度成像之间的鸿沟，使得人脑海马体的可扩展三维细胞图谱成为可能，有助于加深对神经退行性疾病、记忆障碍及脑区特异性细胞结构的理解。 该管道将 CellPoseSAM 的零样本分割能力与集成微调模型和合并算法相结合，实现三类细胞分类；然后小型 UNet 对细胞核仅 1 像素宽的低分辨率切片进行密度估计监督，生成的密度图经采样后得到概率点云，其生物学合理性已与此前海马体细胞计数估计结果进行了验证。

reddit · r/MachineLearning · /u/V_ector · 6月25日 12:37

**背景**: 海马体是与记忆和学习密切相关的脑区，理解其细胞组成需要亚微米级成像，而全器官尺度的此类成像成本极高。CellPoseSAM 是最近提出的基础模型，将 Meta 的 Segment Anything Model（SAM）扩展到细胞和细胞核分割领域，具有强大的零样本（zero-shot）泛化能力，即可以对训练时未明确见过的细胞类型进行分割。U-Net 是 Ronneberger 等人于 2015 年提出的经典编码器-解码器架构，广泛用于生物医学图像分割；本研究将其重新用于密度估计——一种在人群计数领域流行的方法，输出每像素的密度图，通过求和或采样即可估算目标的数量与位置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/wikk-chy/cellpose-SAM">GitHub - wikk-chy/cellpose-SAM: a generalist algorithm for ...</a></li>
<li><a href="https://www.biorxiv.org/content/10.1101/2025.04.28.651001.full.pdf">Cellpose-SAM: superhuman generalization for cellular segmentation</a></li>
<li><a href="https://en.wikipedia.org/wiki/Zero-shot_learning">Zero-shot learning - Wikipedia</a></li>

</ul>
</details>

**标签**: `#medical-imaging`, `#cell-segmentation`, `#computational-neuroscience`, `#deep-learning`, `#density-estimation`

---