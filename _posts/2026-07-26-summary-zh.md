---
layout: default
title: "Horizon Summary: 2026-07-26 (ZH)"
date: 2026-07-26
lang: zh
---

> 从 41 条内容中筛选出 8 条重要资讯。

---

1. [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](#item-1) ⭐️ 7.0/10
2. [揭秘为 LLM 代币倒卖和欺诈提供动力的中转市场](#item-2) ⭐️ 7.0/10
3. [消灭 Cookie 弹窗](#item-3) ⭐️ 7.0/10
4. [GrapheneOS 阐明锁屏设备取证防护机制](#item-4) ⭐️ 7.0/10
5. [一年从 3B 卷到 0.xB：MonkeyOCRv2 用 0.7B 拿下 17 语种文档解析开源第一](#item-5) ⭐️ 6.0/10
6. [本科生在树莓派 4 上用 ARM64 汇编从零实现 YOLO26n 推理](#item-6) ⭐️ 6.0/10
7. [开放权重 4B 模型在瑞典医学问答中接近 o3 水平](#item-7) ⭐️ 6.0/10
8. [我们对比了不同大语言模型在 2026 年国际数学奥林匹克中的表现(R)](#item-8) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 发布，新增 Inkling 模型支持与 DeepSeek-V4 性能优化](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 7.0/10

vLLM v0.26.0 版本正式发布，包含来自 212 位贡献者的 411 次提交，新增对 Inkling 模型家族的完整支持（包括基础建模、分段 CUDA 图、MTP=1 推测解码、LoRA 以及 ModelOpt NVFP4 量化），并在 CUDA/ROCm/XPU 上对 DeepSeek-V4 进行了跨厂商性能优化，同时新增通过 `head_dtype` 启用 fp32 lm_head 的选项以提升生成精度。 vLLM 是目前部署最广泛的开源大语言模型推理引擎之一，本次发布进一步扩展了其硬件覆盖范围和模型生态，正值 DeepSeek-V4 等大型 MoE 模型在生产环境中日益普及的阶段。Inkling 完整堆栈支持以及按 KV-cache 组选择注意力后端的能力，也表明 vLLM 正持续向灵活、混合模型服务的方向演进。 DeepSeek-V4 的优化包括专用路由内核（端到端 TPOT 提升 2.94%）、速度提升 1.5–2 倍的 `fused_topk_bias` 内核，以及带来 1.8% 端到端 TPOT 提升的冗余 repeat/copy 消除；fp32 `lm_head` 路径也扩展至 LoRA，并新增 ROCm `torch.mm` 快速通道。注意力后端现在可按 KV-cache 组进行选择，滑动窗口支持也被显式地作为后端能力暴露出来，以便更好地服务混合注意力模型。

github · khluu · 7月25日 10:38

**背景**: vLLM 是一个高吞吐量的大语言模型服务系统，采用 PagedAttention 和推测解码等技术来优化推理。MTP（多 token 预测）等推测解码方法允许模型使用轻量级 drafter 预测多个未来 token，再由重型目标模型进行验证，从而降低整体延迟。E2E TPOT（每个输出 token 的耗时）是衡量解码阶段 token 生成速度的关键推理延迟指标，与首 token 生成时间（TTFT）互补。NVFP4 是 NVIDIA 的 4 位浮点量化格式，通常通过 ModelOpt 库应用，可在保持推理精度的同时显著减少模型内存占用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/quantization/modelopt/">NVIDIA Model Optimizer - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**标签**: `#vllm`, `#llm-inference`, `#deepseek`, `#model-serving`, `#release-notes`

---

<a id="item-2"></a>
## [揭秘为 LLM 代币倒卖和欺诈提供动力的中转市场](https://vectoral.com/blog/token-relay-market) ⭐️ 7.0/10

Vectoral 发布了一项深度调查，揭露了一个灰色市场的 AI 代币中转服务生态系统。这些服务通过聚合被盗、泄露或欺诈获取的 API 密钥、滥用免费试用以及创业项目积分，以官方定价的 2%-6%转售 OpenAI、Anthropic 和 Google API 的访问权限。报告描绘了一条横跨虚拟卡商户、账号农场、中转运营商和最终经销商的四层供应链，主要面向中国大陆的 B2B 流量。 这一欺诈生态通过压低合法 API 定价，直接威胁到前沿 AI 厂商的单位经济效益，并扭曲了创业公司的竞争格局——正当付费的用户要与利用被盗或补贴算力的对手竞争。它还表明，AI 基础设施如今正吸引着历史上困扰数字广告业的那种复杂的账单滥用参与者。 调查识别出一条四层供应链（虚拟卡商户→账号农场→中转运营商→经销商），以及具体的滥用手段，包括虚假信用卡拒付、大规模免费试用滥用以及 AWS/Azure 的创业积分计划。一位评论者举例称，印度一家公司通过反复注册新实体获取云积分，仅以标价 4%的价格购买推理算力。

hackernews · mlenhard · 7月26日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49058993)

**背景**: OpenAI、Anthropic 和 Google 等前沿 AI 厂商通过按 token 计量的 API 出售其模型访问权限。为了培育开发者生态，云服务商（AWS、Azure、Google Cloud）和模型厂商推出了创业积分计划，向符合条件的新公司提供免费或大幅折扣的推理额度。这些计划加上免费试用和注册赠金，恰恰为倒卖欺诈者提供了原材料——他们将这些额度聚合后以极低折扣中转给那些不愿追问来源的买家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vectoral.com/blog/token-relay-market">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>
<li><a href="https://simonwillison.net/2026/Jul/26/relay-market/">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>
<li><a href="https://vectoral.com/">Vectoral — Catch the proxies reselling your LLM tokens | Vectoral</a></li>

</ul>
</details>

**社区讨论**: 评论者们普遍确认了调查的发现，并将其置于历史背景中。一位曾在大型广告公司负责财务完整性的工程师指出，这与多年来困扰数字广告业的复杂曝光量转售市场如出一辙。其他评论者补充了具体案例：一位朋友通过滥用 AWS 创业积分仅支付标价的 4%，中国某联盟营销网站在社交媒体上推广可疑的免费代币服务，以及与门票倒卖的类比。一位评论者划出了一条有用的道德界线：彻底的欺诈（假卡、拒付）、灰色地带的免费试用滥用，以及合法的订阅转售。

**标签**: `#ai-economics`, `#fraud`, `#api-pricing`, `#security`, `#cloud-credits`

---

<a id="item-3"></a>
## [消灭 Cookie 弹窗](https://killthecookiebanner.eu/) ⭐️ 7.0/10

欧盟委员会提议建立浏览器级别的隐私偏好系统，以消除烦人的 Cookie 弹窗，预计将于 2027 年生效。

hackernews · rapnie · 7月26日 11:53 · [社区讨论](https://news.ycombinator.com/item?id=49057175)

**标签**: `#privacy`, `#regulation`, `#eu-policy`, `#web-development`, `#cookies`

---

<a id="item-4"></a>
## [GrapheneOS 阐明锁屏设备取证防护机制](https://discuss.grapheneos.org/d/40700-grapheneos-protections-against-data-extraction-from-locked-devices) ⭐️ 7.0/10

GrapheneOS 社区成员阐明了该操作系统针对锁屏设备取证数据提取的防护机制，强调其 18 小时自动重启功能可强制设备进入首次解锁前（BFU）模式，从而使加密密钥无法被提取。该讨论由一起美国起诉案件和一篇关于 GrapheneOS 如何帮助记者保护机密消息来源的近期文章引发。 这一点很重要，因为从被扣押设备中进行取证数据提取对记者、活动人士、过境旅客以及任何面临设备被没收的人来说都是真实威胁，使自动进入 BFU 模式成为一项关键的防御功能。讨论还揭示了一个关键的安全性与易用性权衡：GrapheneOS 的保护机制可能被低熵的锁屏方式（如图案解锁）所削弱。 18 小时自动重启功能确保即使设备长时间未使用，也会转入 BFU 模式，使基于文件的加密密钥对取证工具保持不可访问。然而，社区分析显示 Android 的图案解锁仅提供约 18.57 位的熵——少于三个随机字符或四个小写字母——这使得锁屏方式的选择成为整体安全性的关键因素。

hackernews · Cider9986 · 7月26日 05:57 · [社区讨论](https://news.ycombinator.com/item?id=49055169)

**背景**: GrapheneOS 是一个基于 Android 开源项目（AOSP）构建的、注重隐私的开源移动操作系统，主要支持 Google Pixel 设备。现代 Android 和 iOS 设备采用基于文件的加密（FBE），在用户解锁设备前数据始终保持加密状态。移动取证学区分两种设备状态：首次解锁前（BFU），即设备已关机或重启且尚未解锁，加密密钥不可访问；首次解锁后（AFU），密钥驻留在内存中，可提取的数据显著增多。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://blogs.dsu.edu/digforce/2023/08/23/bfu-and-afu-lock-states/">BFU and AFU Lock States – Blog | DigForCE Lab - DSU</a></li>
<li><a href="https://teeltechcanada.com/understanding-mobile-device-lock-states-in-forensic-extractions/">Understanding Mobile Device Lock States in Forensic ...</a></li>

</ul>
</details>

**社区讨论**: 社区情绪总体上支持 GrapheneOS 的做法，用户称赞 18 小时自动重启是对抗强制取证的有效保护。建设性的批评集中在缺少一套完整的备份/恢复方案以便在过境前进行预防性擦除，以及 Android 图案解锁相较于字母数字密码的熵过低。有一位评论者指出，追求与苹果锁定模式（Lockdown Mode）同等安全性却常常被以怀疑眼光看待，这颇具讽刺意味；另一位用户则赞赏世界上存在不为用户设套的硬件。

**标签**: `#security`, `#privacy`, `#grapheneos`, `#mobile-security`, `#forensics`

---

<a id="item-5"></a>
## [一年从 3B 卷到 0.xB：MonkeyOCRv2 用 0.7B 拿下 17 语种文档解析开源第一](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247907283&idx=2&sn=5df8a52712c79f67232ca9672d4cc34e) ⭐️ 6.0/10

MonkeyOCRv2 仅用 0.7B 参数就在 17 种语言的文档解析任务上达到开源最优水平，证明精心设计的小模型能够超越大模型。

rss · 量子位 · 7月26日 04:30

**标签**: `#document-parsing`, `#OCR`, `#efficient-models`, `#open-source`, `#multilingual`

---

<a id="item-6"></a>
## [本科生在树莓派 4 上用 ARM64 汇编从零实现 YOLO26n 推理](https://www.reddit.com/r/MachineLearning/comments/1v6w394/i_implemented_the_yolo26n_model_inference_from/) ⭐️ 6.0/10

一名本科生在树莓派 4 上使用 ARM64 汇编语言和 C 语言（不依赖任何机器学习框架）从零实现了完整的 YOLO26n 目标检测推理引擎。该实现涵盖了 ARM NEON SIMD 向量化、Winograd 卷积、优化的 GEMM 内核、缓存感知的分块（cache-aware tiling）、自定义微内核、算子融合以及注意力机制，并实现了 YOLO26 的所有构建模块（Conv、C3K2、SPPF、C2PSA、PSA、BottleNeck、Detect）。 这个项目提供了一个难得且深入教学性的视角，展示了现代神经网络推理引擎在底层究竟是如何工作的，架起了高层机器学习框架与底层硬件优化之间的桥梁。对于边缘 AI 部署尤其有意义，因为 ARM 架构设备占主导地位，每个时钟周期都很宝贵，因此对于希望从资源受限的硬件中榨取最大性能的工程师来说，这是一个很有价值的参考。 作者提取了 YOLO26n 的模型参数，并将内存布局重新设计为针对推理流水线定制的自定义二进制格式，最终产生了正确的检测结果；但实际获得的性能提升低于最初的预期，这凸显了超越已有成熟优化生产框架的难度。YOLO26n 是 Ultralytics 较新发布的模型，声称在 Intel Xeon 硬件上 CPU ONNX 推理速度比 YOLO11n 快达 43%。

reddit · r/MachineLearning · /u/Forward_Confusion902 · 7月26日 06:43

**背景**: YOLO（You Only Look Once）是一系列单阶段目标检测模型，由 Joseph Redmon 于 2016 年首次提出，以实时检测速度著称。YOLO26 是 Ultralytics 最新发布的版本，引入了进一步的架构改进。ARM64 NEON 是 ARM 的高级 SIMD（单指令多数据）指令集扩展，允许一条指令并行处理多个数据元素，对于加速 ARM CPU 上的矩阵和向量运算至关重要。Winograd 卷积是一种通过将输入和滤波器变换到不同代数域来减少卷积运算所需乘法次数的算法，常用于加速 CNN 推理。在树莓派 4（采用四核 ARM Cortex-A72 CPU）这样的设备上运行边缘 AI，需要此类底层优化才能在没有 GPU 的情况下实现可用的推理延迟。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/ultralytics/ultralytics/blob/main/docs/en/models/yolo26.md">ultralytics/docs/en/models/yolo26.md at main · ultralytics ...</a></li>
<li><a href="https://developer.arm.com/documentation/dht0002/latest/Introducing-NEON/What-is-SIMD-/ARM-SIMD-instructions">ARM SIMD instructions - Neon</a></li>
<li><a href="https://arxiv.org/abs/2201.10369">[2201.10369] Winograd Convolution for Deep Neural Networks: Efficient Point Selection</a></li>

</ul>
</details>

**标签**: `#machine-learning`, `#edge-ai`, `#arm64-assembly`, `#yolo`, `#optimization`, `#computer-vision`

---

<a id="item-7"></a>
## [开放权重 4B 模型在瑞典医学问答中接近 o3 水平](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 6.0/10

实验表明，像 Qwen3.5-4B 这样的 4B 开放权重模型无需后训练即可在瑞典医学执照考试中达到 87%的准确率，接近 o3 的 88%，展示了小型模型能力的快速提升。

reddit · r/MachineLearning · /u/AccomplishedCat4770 · 7月26日 11:58

**标签**: `#LLMs`, `#open-weight-models`, `#medical-AI`, `#fine-tuning`, `#benchmarking`

---

<a id="item-8"></a>
## [我们对比了不同大语言模型在 2026 年国际数学奥林匹克中的表现(R)](https://www.reddit.com/r/MachineLearning/comments/1v6wskz/we_compared_different_llms_on_imo_2026_r/) ⭐️ 6.0/10

对前沿、商用及开源权重大语言模型在 2026 年国际数学奥林匹克题目上的对比研究表明，harness/编排工程能显著提升性能，其中前沿模型（sol、fable）取得了近乎满分的成绩，而作者提出的 AutoFyn 多智能体 harness 则帮助 Claude 和 GLM 缩小了与前沿模型的差距。

reddit · r/MachineLearning · /u/pequalnp92 · 7月26日 07:21

**标签**: `#LLM-benchmark`, `#math-reasoning`, `#model-evaluation`, `#harness-engineering`, `#multi-agent-systems`

---