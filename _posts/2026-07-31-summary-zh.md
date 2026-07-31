---
layout: default
title: "Horizon Summary: 2026-07-31 (ZH)"
date: 2026-07-31
lang: zh
---

> 从 59 条内容中筛选出 13 条重要资讯。

---

1. [Tailscale 公开 Hugging Face 遭入侵事件：可复用认证密钥泄露](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash 0731 智能、性能与价格分析](#item-2) ⭐️ 8.0/10
3. [Gemini Robotics ER 2：以视频理解、任务编排与多机器人协作赋能机器人技术](#item-3) ⭐️ 8.0/10
4. [Kimi K3 技术深度解析：三大工程创新详解](#item-4) ⭐️ 8.0/10
5. [OpenAI 阐述实现充裕智能的全栈战略](#item-5) ⭐️ 7.0/10
6. [OpenAI 捣毁柬埔寨利用 ChatGPT 的诈骗团伙](#item-6) ⭐️ 7.0/10
7. [MLVC：面向跨平台 NPU 部署的多平台学习型视频编解码器](#item-7) ⭐️ 7.0/10
8. [电梯](#item-8) ⭐️ 6.0/10
9. [qm](#item-9) ⭐️ 6.0/10
10. [通过 Thunderbolt 在 Mac Studio 上实现 25 Gbps 以太网](#item-10) ⭐️ 6.0/10
11. [SIGGRAPH 时间检验奖揭晓：这项研究提前十年押中物理 AI](#item-11) ⭐️ 6.0/10
12. [开发者构建 BERT 风格 Transformer 预测个人血糖水平](#item-12) ⭐️ 6.0/10
13. [助理教授因机器学习会议审稿毒害而失去博士生候选人](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Tailscale 公开 Hugging Face 遭入侵事件：可复用认证密钥泄露](https://tailscale.com/blog/hugging-face-intrusion) ⭐️ 8.0/10

Tailscale 发布了一份透明的事件复盘报告，详细说明了攻击者如何在 Hugging Face 的环境变量文件中发现一个可复用的 Tailscale 认证密钥，并在数天内利用它向 Hugging Face 的 tailnet 中注册了 181 个恶意节点，每个节点都被授予了 CI 节点的访问权限。 这一事件表明，即使像 Tailscale 这样专门的安全工具，也无法在客户不当处理密钥的情况下阻止其被滥用；同时 Tailscale 主动公开承担这次并非由其漏洞导致的安全事件责任，设立了供应商透明披露的新标杆。 在被泄露的 136 个凭证中，其中一个是用于自动化 CI 节点配置的可复用 Tailscale 认证密钥，攻击者将其复制到多个外部沙箱中使用。Tailscale 强调其代码本身并未被攻破，但承诺推出新的检测功能（例如对异常节点注册行为的告警），以便更早发现类似攻击。

hackernews · bluehatbrit · 7月31日 19:03 · [社区讨论](https://news.ycombinator.com/item?id=49127306)

**背景**: tailnet 是 Tailscale 用来描述基于 WireGuard 构建的私有 mesh VPN 网络的术语，用于连接用户授权的设备和服务器。Tailscale 认证密钥允许机器无需交互登录即可自动加入 tailnet；可复用认证密钥可以被多次使用来批量配置节点，常用于 CI/CD 流水线，但一旦泄露，任何获取密钥的机器都将获得该密钥所关联标签所赋予的全部访问权限，实质上等同于一张开放注册的入场券。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tailscale.com/docs/concepts/tailnet">What is a tailnet ? · Tailscale Docs</a></li>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys/how-to/secure-auth-keys">Securely handle an auth key · Tailscale Docs</a></li>
<li><a href="https://selfhosting.sh/apps/tailscale/">How to Set Up Tailscale with Docker | selfhosting.sh</a></li>

</ul>
</details>

**社区讨论**: 社区普遍赞扬了 Tailscale 的透明度以及「非常加拿大的道歉」这种表达方式，但像 ahofmann 这样的评论员认为，这篇文章同时也是一种巧妙的营销——在展示其高级安全功能的同时，将责任隐性地归咎于 Hugging Face 自身可以避免的失误。讨论中也出现了一些实操层面的建议，例如 Simon Willison 提出应该对异常的 CI 节点注册行为发出告警，bumbledraven 则请求 Tailscale 提供内置的安全检查工具。

**标签**: `#security`, `#post-mortem`, `#tailscale`, `#devops`, `#incident-response`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731 智能、性能与价格分析](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 8.0/10

DeepSeek V4 Flash 0731 以极低的成本提供前沿水平的 AI 智能，标志着性价比前沿的重大新突破，并具备可行的本地部署选项。

hackernews · theanonymousone · 7月31日 07:59 · [社区讨论](https://news.ycombinator.com/item?id=49120299)

**标签**: `#deepseek`, `#llm`, `#ai-models`, `#price-performance`, `#open-source-ai`

---

<a id="item-3"></a>
## [Gemini Robotics ER 2：以视频理解、任务编排与多机器人协作赋能机器人技术](https://deepmind.google/blog/gemini-robotics-er-2-powering-robotics-with-video-understanding-task-orchestration-and-multi-robot-collaboration/) ⭐️ 8.0/10

Google DeepMind 发布 Gemini Robotics ER 2，这是一款在视频理解、任务编排和多机器人协作方面提升机器人能力的新模型。

rss · Google DeepMind Blog · 7月30日 15:00

**标签**: `#robotics`, `#embodied-ai`, `#google-deepmind`, `#gemini`, `#multi-agent-systems`

---

<a id="item-4"></a>
## [Kimi K3 技术深度解析：三大工程创新详解](https://www.reddit.com/r/MachineLearning/comments/1vaysjf/how_kimi_k3_engineered_its_way_to_the_frontier_r/) ⭐️ 8.0/10

Moonshot 公司的 Kimi K3 作为开源权重模型已跻身前沿，在 Artificial Analysis 评测的 580 个模型中排名第四。对其 47 页技术报告的详细解读揭示了三大新颖工程贡献：用 Kimi Delta Attention 替换 93 层中 69 层的 KV 缓存、为每层 896 个专家设计的 Quantile Balancing 负载均衡，以及支撑创建 5100 万个训练沙箱的 AgentENV Firecracker 微虚拟机基础设施。 Kimi K3 证明开源权重模型能够在前沿水平竞争，同时引入显著降低内存和计算成本的架构创新。这些工程选择针对长上下文内存、大规模 MoE 负载均衡以及智能体强化学习基础设施等核心扩展瓶颈——而这些都是整个 AI 社区正在积极攻克的难题。 Kimi Delta Attention 通过每头一个 128×128 矩阵将 100 万 token 上下文所需内存从 104.6 GiB 降至仅 27.2 GiB；Quantile Balancing 直接根据单批次路由器得分边际计算专家偏置，而非 DeepSeek-V3 所用的固定步长扰动；AgentENV 通过 Firecracker 微虚拟机结合 overlaybd OCI 镜像按需加载，实现了 133 毫秒检查点和 49 毫秒恢复。

reddit · r/MachineLearning · /u/noninertialframe96 · 7月30日 16:37

**背景**: 传统 Transformer 注意力机制随序列长度呈二次方扩展，尽管 KV（键值）缓存仅线性增长，但在百万 token 规模下仍成为严重的内存瓶颈。混合专家（MoE）模型通过对每个 token 路由到一小部分专家来扩展参数量，但需要辅助负载均衡损失以防止所有 token 坍缩到少数热门专家。智能体强化学习训练模型使用工具并执行多步规划，需要海量隔离执行环境以安全地展开轨迹。线性注意力变体试图在降低计算和内存成本的同时恢复 softmax 注意力的表达能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://www.banandre.com/blog/linear-attentions-revenge-how-kimi-delta-attention-smashes-the-kv-cache-bottleneck">Linear Attention ’s Revenge: How Kimi Delta Attention ... - Banandre</a></li>
<li><a href="https://kvcache.ai/blog/agentenv-open-sourced/">AgentENV: When LLMs Learn to Get the Job Done, We’re Open ...</a></li>

</ul>
</details>

**标签**: `#Kimi-K3`, `#open-weight-models`, `#Mixture-of-Experts`, `#KV-cache-optimization`, `#frontier-models`

---

<a id="item-5"></a>
## [OpenAI 阐述实现充裕智能的全栈战略](https://openai.com/index/building-abundant-intelligence) ⭐️ 7.0/10

OpenAI 发布了题为《构建充裕智能》的博客文章，阐述了一种全栈方法，旨在让先进 AI 变得更强大、更便宜、更广泛地服务于社会。该文章将 OpenAI 在算力基础设施、模型效率和广泛部署方面的工作整合为一个统一的战略愿景。 这一战略定位表明了 OpenAI 在算力基础设施、模型效率提升和 AI 访问民主化方面的方向，延伸了 Sam Altman 此前关于 AI 访问可能成为基本人权的愿景。它也为 OpenAI、Oracle 和软银达成的 4000 亿美元巨额资本承诺——用于建设吉瓦级 AI 基础设施——提供了意识形态基础。 "充裕智能"的表述为建设吉瓦级数据中心、保障庞大能源供应以及开发专用 AI 芯片提供了意识形态基础，整体投入高达数千亿乃至数万亿美元。行业也正在从已遇瓶颈的预训练扩展，转向"测试时计算"方法，即模型分析问题并并行探索多种解题路径。

rss · OpenAI Blog · 7月31日 15:00

**背景**: "充裕智能"是 OpenAI CEO Sam Altman 于 2025 年 9 月提出的概念，描绘了一个 AI 如此广泛可得且廉价，以至于访问它成为像电力或互联网一样基本需求的未来。"全栈方法"指的是 OpenAI 影响或控制 AI 技术栈每一层的战略——从定制硅芯片和数据中心，到基础模型和消费级应用——而不仅仅依赖第三方基础设施或现成模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.samaltman.com/abundant-intelligence">Abundant Intelligence - Sam Altman</a></li>
<li><a href="https://note.com/enhack_fumi/n/nce4cd86a97fe">'Abundant Intelligence': Meaning and Context｜Fumi AI</a></li>
<li><a href="https://www.humanityredefined.com/p/the-dream-of-abundant-intelligence">The Dream of Abundant Intelligence - by Conrad Gray</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#AI infrastructure`, `#AI strategy`, `#compute scaling`, `#AI economics`

---

<a id="item-6"></a>
## [OpenAI 捣毁柬埔寨利用 ChatGPT 的诈骗团伙](https://openai.com/index/disrupting-malicious-uses-of-ai-criminal-scam-operation) ⭐️ 7.0/10

OpenAI 捣毁了一个总部位于柬埔寨的犯罪诈骗组织，该组织利用 ChatGPT 实施投资欺诈、恋爱诈骗、赌博骗局和冒充攻击。此次打击行动是 OpenAI 持续威胁情报工作的一部分，旨在识别和瓦解大规模 AI 驱动的滥用行为。 此案例表明生成式 AI 工具正被犯罪团伙武器化，以规模化其传统诈骗剧本，并凸显了 AI 公司作为主动防御者在遏制滥用方面日益重要的角色。它也强调了 AI 平台、执法部门和行业合作伙伴之间协调共享威胁情报的紧迫性，以应对不断演变的 AI 驱动型欺诈。 该诈骗组织结合了多种欺诈类型——投资欺诈、恋爱诱骗、赌博和身份冒充——表明其采用了复杂的多向量攻击手法，而非单一骗局。OpenAI 的干预很可能涉及封禁相关账户，并与合作伙伴共享威胁指标，这与其已发布的检测违规行为和与外部防御者协调的方法论一致。

rss · OpenAI Blog · 7月31日 00:00

**背景**: ChatGPT 等生成式 AI 聊天机器人可能被犯罪分子滥用，以自动化诈骗运营中最耗费人力的环节，例如撰写令人信服的消息、跨语言翻译以及同时维持多个欺诈身份。恋爱和投资诈骗历来依赖人工操作员同时管理数十场对话；如今大语言模型使这种社会工程学能够以更少的人力实现大规模扩展。OpenAI 越来越多地发布威胁报告，记录恶意行为者如何"将 AI 嫁接到旧剧本上"以加快速度，而非从模型本身获得全新的攻击能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/disrupting-malicious-ai-uses/">Disrupting malicious uses of AI | OpenAI</a></li>
<li><a href="https://openai.com/global-affairs/disrupting-malicious-uses-of-ai-october-2025/">Disrupting malicious uses of AI: October 2025 | OpenAI</a></li>
<li><a href="https://www.wired.com/story/ai-scammers-are-better-at-building-trust-than-humans/">AI Scammers Are Better at Building Trust Than Humans | WIRED</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#cybersecurity`, `#fraud prevention`, `#ChatGPT abuse`, `#AI policy`

---

<a id="item-7"></a>
## [MLVC：面向跨平台 NPU 部署的多平台学习型视频编解码器](https://www.reddit.com/r/MachineLearning/comments/1vb3xwd/mlvc_multiplatform_learned_video_codec_for/) ⭐️ 7.0/10

MLVC 提出了一种学习型视频编解码器，通过超先验（hyperprior）显式传输熵模型的缩放参数，使编码端和解码端的神经网络无需在不同 NPU 上保持比特级一致即可协同工作。 神经视频编解码器长期无法在实际场景中取代 H.264、H.265 和 AV1 等传统编解码器，主要瓶颈之一就是跨平台数值不兼容；MLVC 直接解决了这一问题，让学习型编解码器可在 Apple、Intel 等消费级 NPU 上互通，并在 360p/540p 分辨率下达到约 100 FPS。 在 Apple M3 神经引擎上，INT8 运算是通过 FP16 模拟的，并非走真正的 INT8 数据通路；即便硬件原生支持 INT8，也无法保证对舍入模式、累加数据类型和缩放乘法的完全控制，因此无法做到比特级一致。MLVC 通过在码流中传递熵模型缩放参数来规避该问题，确保解码端始终使用与编码端完全一致的参数。

reddit · r/MachineLearning · /u/tanelai · 7月30日 19:40

**背景**: 传统手工设计的编解码器（如 H.264/AVC、2013 年标准化的 H.265/HEVC，以及 AV1）之所以仍主导实际部署，是因为它们拥有几乎无处不在的硬件加速且功耗极低。学习型神经编解码器虽然压缩性能更优，但模型通常较大、功耗较高，且严重依赖熵模型：其概率分布必须在编码端和解码端之间完全一致，而不同 NPU 上推理产生的微小数值漂移就会破坏熵解码，甚至导致整个码流崩溃。当前的 NPU 工具链（包括 Apple Neural Engine、Intel NPU 等）远未标准化到能保证定点运算结果比特级一致的程度，因此仅仅将模型量化到 INT8 并不能可靠地解决该问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Efficiency_Video_Coding">High Efficiency Video Coding - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2207.05894">Hybrid Spatial-Temporal Entropy Modelling for Neural Video ...</a></li>
<li><a href="https://fireworks.ai/blog/when-faster-not-identical-moe-numerics">Training- Inference Parity in MoE Models: Where Numerics Drift</a></li>

</ul>
</details>

**社区讨论**: 原帖作者主动披露自己是论文作者之一并欢迎提问，帖子中未提供其他社区评论。

**标签**: `#video-compression`, `#learned-codecs`, `#neural-networks`, `#edge-deployment`, `#cross-platform`

---

<a id="item-8"></a>
## [电梯](https://john.fun/elevators) ⭐️ 6.0/10

一个基于网页的交互式电梯模拟器，演示各种调度算法，并引发了关于其与磁盘调度、目的地调度系统以及游戏设计之间联系的高质量讨论。

hackernews · Jrh0203 · 7月31日 15:17 · [社区讨论](https://news.ycombinator.com/item?id=49124218)

**标签**: `#algorithms`, `#simulation`, `#elevator-scheduling`, `#interactive-learning`, `#computer-science`

---

<a id="item-9"></a>
## [qm](https://github.com/yc-software/qm) ⭐️ 6.0/10

qm 是一款获 YC 投资支持的多人协作代理工作框架，通过引入个人作用域和共享房间机制，解决企业多代理环境中的作用域难题。

hackernews · tosh · 7月31日 18:04 · [社区讨论](https://news.ycombinator.com/item?id=49126604)

**标签**: `#AI-agents`, `#multi-agent-systems`, `#developer-tools`, `#YC`, `#enterprise-software`

---

<a id="item-10"></a>
## [通过 Thunderbolt 在 Mac Studio 上实现 25 Gbps 以太网](https://www.jeffgeerling.com/blog/2026/getting-25g-ethernet-mac-thunderbolt/) ⭐️ 6.0/10

Jeff Geerling 发布了一篇关于通过 Thunderbolt 将 25 Gigabit 以太网适配器连接到 Mac Studio 的技术探索文章。测试发现，实际吞吐量并非受限于 Thunderbolt 连接本身，而是受到对端 Arm 架构 NAS（Ampere Altra）的限制——其内置 10 GbE 链路也只能提供约 1 GB/s 的速度。 这对于需要在 Apple Silicon Mac 上获得高吞吐量本地存储和网络访问的内容创作者和专业用户非常重要，因为这类 Mac 历来内部 PCIe 扩展能力有限。文章指出，即使使用正确的适配器，端到端 25 GbE 性能也需要关注链路中的每一环，包括 NAS 的 CPU 性能和协议支持。 社区测试确认，Sonnet Thunderbolt 25 GbE 适配器可实现约 27 Gbps 的双向传输，但只能提供 15W 的上游供电，这对笔记本电脑来说是一个限制。讨论中提到的更便宜的替代方案是将标准 PCIe NIC 放入 Thunderbolt eGPU 扩展箱中，但 Thunderbolt 3/4 带宽上限为 PCIe 3.0 x4。

hackernews · speckx · 7月31日 16:15 · [社区讨论](https://news.ycombinator.com/item?id=49125034)

**背景**: 25 Gigabit Ethernet（25GbE）是 2016 年批准的网络标准，提供单通道 25 Gbit/s 速率，是 40G 以太网的替代方案，可为交换机提供更高的端口密度。Thunderbolt 是由 Intel 和 Apple 联合开发的硬件接口，通过单根线缆整合 PCIe 和 DisplayPort，其中 Thunderbolt 3 和 4 提供高达 40 Gbps 的总带宽。由于 Apple Silicon Mac 缺少用于升级 NIC 的内部 PCIe 插槽，用户必须依赖 Thunderbolt 扩展箱或专用适配器才能使用 25 GbE 网络。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/25_Gigabit_Ethernet">25 Gigabit Ethernet - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Thunderbolt_(interface)">Thunderbolt (interface) - Wikipedia</a></li>
<li><a href="https://www.reddit.com/r/eGPU/comments/1aggcq5/egpu_enclosure_for_standard_pcie_cards/">eGPU enclosure for standard PCIe cards? : r/eGPU - Reddit</a></li>

</ul>
</details>

**社区讨论**: 社区反馈褒贬不一且充满警示。rconti 强烈建议不要购买廉价的 RealTek RTL8156 USB-C 多速率以太网适配器，因为他在三个不同品牌的设备上都遇到了问题。Neywiny 推荐更昂贵的 Sonnet 适配器，称其可靠性值得信赖，尽管只有 15W 上游供电。randusername 建议将 PCIe NIC 放入 eGPU 扩展箱作为约 150 美元的 DIY 替代方案。GeekyBear 和 pzmarzly 都指出软件端的瓶颈——NAS 的 CPU 以及 macOS 似乎缺少 SMB Direct（RDMA）支持——才是实际性能的上限。

**标签**: `#networking`, `#mac-studio`, `#thunderbolt`, `#hardware`, `#25gbps-ethernet`

---

<a id="item-11"></a>
## [SIGGRAPH 时间检验奖揭晓：这项研究提前十年押中物理 AI](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247908730&idx=2&sn=0b3a81693cb5f92800c95b7fc50939f1) ⭐️ 6.0/10

一篇获得 SIGGRAPH 时间检验奖（Test-of-Time Award）的论文因其过去十年对计算机图形学的持久影响而获奖，并被认为提前预言了当今物理 AI 的发展方向。该奖项是 ACM SIGGRAPH 自 2023 年起设立的年度荣誉。 这一认可凸显了基础计算机图形学研究如何为机器人仿真、数字孪生和具身智能等相邻领域播下突破的种子。它表明计算机图形学与物理 AI 之间的融合日益加深——渲染、仿真和基于物理的建模正成为在虚拟环境中训练智能系统的核心基石。 SIGGRAPH 时间检验奖自 2023 年起每年颁发，至 2026 年已是第四年，表彰那些对计算机图形学与交互技术产生至少十年持久影响的论文。物理 AI（以 NVIDIA Omniverse 等平台为代表）在很大程度上依赖包括物理仿真和光线追踪在内的计算机图形学技术。

rss · 量子位 · 7月31日 06:32

**背景**: SIGGRAPH 是由 ACM 自 1970 年代以来举办的顶级计算机图形学年会，巅峰时期吸引数万名研究人员、艺术家和行业人士参与。时间检验奖专门表彰大约十年前发表、影响力随时间持续增长的论文。物理 AI 是指嵌入物理世界或与物理世界交互的 AI 系统——包括机器人、自动驾驶汽车和工业自动化——其中基于图形技术的仿真环境在训练和验证中发挥着关键作用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.siggraph.org/2026/05/siggraph-2026-technical-papers-awards-best-papers-honorable-mentions-and-test-of-time.html/">SIGGRAPH 2026 Technical Papers Awards: Best Papers, Honorable Mentions, and Test-of-Time - ACM SIGGRAPH Blog</a></li>
<li><a href="https://blog.siggraph.org/2025/12/a-state-of-the-art-performance-withstanding-the-test-of-time.html/">A State-of-the-Art Performance Withstanding the Test-of-Time - ACM SIGGRAPH Blog</a></li>
<li><a href="https://www.nvidia.com/en-us/omniverse/">Develop Physical AI Applications | NVIDIA Omniverse</a></li>

</ul>
</details>

**标签**: `#SIGGRAPH`, `#physical AI`, `#computer graphics`, `#research retrospective`, `#RSS aggregation`

---

<a id="item-12"></a>
## [开发者构建 BERT 风格 Transformer 预测个人血糖水平](https://www.reddit.com/r/MachineLearning/comments/1vc1txc/i_have_trained_a_model_to_predict_my_blood_sugar_p/) ⭐️ 6.0/10

一位开发者发布了一个 MIT 许可证项目，使用 BERT 风格仅编码器 Transformer 预测未来 2 小时以上的血糖，在 4 个模型规模（最大约 1700 万参数）上分别在仿真器和三个真实 1 型糖尿病数据集（OhioT1DM、AZT1D、ShanghaiT1DM）上训练。该系统通过 Kendall-Gal 聚合方法结合 DILATE 损失和分位数损失（pinball loss），在重新参数化到 [40, 400] 区间的 Kovatchev 风险空间中运行，且一个个性化微调版本目前正在作者手机上运行。 该项目展示了对安全关键的医疗预测任务的深思熟虑的工程选择，证明了最初为 NLP 设计的 Transformer 架构如何被适配到生理时间序列预测。代码、权重和评估数据的开源发布使社区能够复现、基准测试并扩展基于 Transformer 的血糖预测——这是闭环胰岛素输送系统中一个活跃的研究方向。 该模型使用双向注意力并对未来血糖进行掩码（类似于掩码语言建模），接受已声明的餐食和胰岛素作为条件输入，并从上下文中隐式推断时间，而不将时间作为特征输入。一个已知的局限是模型目前需要已声明的碳水化合物和胰岛素才能运行，而理想的系统也应能在没有这些输入的情况下进行预测；最大模型的预训练耗时约 48 小时，而微调在 10 分钟内完成。

reddit · r/MachineLearning · /u/0xdeadf1sh · 7月31日 20:09

**背景**: 血糖预测是一个已被广泛研究的领域，且已有基于 Transformer 的先前方法，对 1 型糖尿病（T1D）的管理尤其重要，因为患者必须持续平衡胰岛素剂量与碳水摄入。DILATE（NeurIPS 2019）是一种专为非平稳多步时间序列预测设计的损失函数，明确惩罚形状和时间扭曲两方面。Kovatchev 风险空间是血糖值（以 mg/dL 为单位）的非线性变换，通过拉伸低血糖区间并压缩高血糖区间来对称地强调危险的低血糖和高血糖，最初由 Boris Kovatchev 及其同事开发。Kendall-Gal 指的是 Kendall、Gal 和 Cipolla 在 2018 年提出的基于同方差不确定性的方法，通过学习任务特定的噪声参数在多任务学习中自动加权多个损失函数。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1909.09020">Shape and Time Distortion Loss for Training Deep Time Series ... GitHub - vincent-leguen/DILATE: Code for our NeurIPS 2019 ... Shape and Time Distortion Loss for Training Deep Time Series ... Shape and time distortion loss for training deep time series ... NeurIPS Poster Shape and Time Distortion Loss for Training ... Shape and Time Distortion Loss for Training Deep Time Series... Shape and Time Distortion Loss for Training Deep Time Series ...</a></li>
<li><a href="https://github.com/vincent-leguen/DILATE">GitHub - vincent-leguen/DILATE: Code for our NeurIPS 2019 ...</a></li>
<li><a href="https://arxiv.org/abs/1705.07115">[1705.07115] Multi-Task Learning Using Uncertainty to Weigh ... [1703.04977] What Uncertainties Do We Need in Bayesian Deep ... Multi-Task Learning Using Uncertainty to Weigh Losses for ... [1703.04977] What Uncertainties Do We Need in Bayesian Deep ... Investigating Uncertainty Weighting for Multi-Task Learning ... GitHub - ranandalon/mtl: Unofficial implementation of: Multi ... Multi-Task Learning Using Uncertainty to Weigh Losses for ...</a></li>

</ul>
</details>

**社区讨论**: 该 Reddit 帖子发布在 r/MachineLearning，是作者分享的个人项目以寻求社区反馈，并邀请大家提出问题和意见。该帖得分为 6.0/10（中等），反映出社区对其技术深度（DILATE/分位数损失组合、Kovatchev 风险重新参数化、未来掩码）的赞赏，同时也注意到基于 Transformer 的血糖预测已是一个成熟的研究方向，而非新突破。

**标签**: `#transformers`, `#time-series-forecasting`, `#healthcare-ML`, `#diabetes`, `#pytorch`

---

<a id="item-13"></a>
## [助理教授因机器学习会议审稿毒害而失去博士生候选人](https://www.reddit.com/r/MachineLearning/comments/1vawwb8/i_have_lost_three_and_a_half_potential_phd/) ⭐️ 6.0/10

一位在机器学习「三大顶会」拥有超过十年经验的助理教授表示，他因学术会议同行评审流程失去了三到四位潜在的博士生候选人，尽管这些学生的论文获得了积极的评审意见（包括一篇获得四位审稿人一致评为「弱接收」的论文），最终还是被拒稿。 这一案例揭示了日益激烈的机器学习会议评审文化可能正在主动将优秀人才驱赶出学术界，对机器学习研究者的长期培养管线构成威胁，并引发了关于 NeurIPS、ICML、ICLR 等顶会现行评审实践可持续性的紧迫质疑。 该教授指出，那些没有明显缺陷的论文在反复重投过程中会被审稿人针对「随机的小问题」不断攻击，形成无止境的循环；而有明显弱点的论文反而能通过直接修改得到改善。他强调这些工作来自他自己的在研项目，而非投机性的课程作业，且整体评审意见积极却依然被拒。

reddit · r/MachineLearning · /u/AffectionateLife5693 · 7月30日 15:30

**背景**: 机器学习「三大顶会」——NeurIPS、ICML 和 ICLR——是机器学习研究领域最具声望的学术会议，在这些会议上发表论文通常对学术职业发展至关重要，包括申请博士和教职。这些会议使用 OpenReview 平台，一个透明的同行评审系统，会公开记录整个论文生命周期中的评审、回复和元评审。近年来投稿量急剧增加，引发了人们对评审随机性、审稿人疲劳以及评审过程日益对抗性的广泛担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/International_Conference_on_Machine_Learning">International Conference on Machine Learning - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Conference_on_Neural_Information_Processing_Systems">Conference on Neural Information Processing Systems - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/openreview-platform">OpenReview: Transparent Peer Review Platform</a></li>

</ul>
</details>

**标签**: `#peer-review`, `#ml-conferences`, `#phd-recruitment`, `#research-culture`, `#academic-mentorship`

---