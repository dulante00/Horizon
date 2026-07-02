---
layout: default
title: "Horizon Summary: 2026-07-02 (ZH)"
date: 2026-07-02
lang: zh
---

> 从 52 条内容中筛选出 11 条重要资讯。

---

1. [自 Linux 6.9 起，LUKS 挂起功能停止清除内存中的磁盘加密密钥](#item-1) ⭐️ 7.0/10
2. [Podman v6.0.0 发布，网络与 Quadlet 功能升级](#item-2) ⭐️ 7.0/10
3. [日本最高法院裁定 AI 不能被列为专利发明人](#item-3) ⭐️ 7.0/10
4. [Hugging Face 与 Cerebras 合作推出基于 Gemma 4 的实时语音 AI](#item-4) ⭐️ 7.0/10
5. [arXiv 将于 2026 年从康奈尔大学分拆为独立非营利组织](#item-5) ⭐️ 7.0/10
6. [Ollama v0.31.1：苹果芯片上 Gemma 4 推理速度提升高达 90%](#item-6) ⭐️ 6.0/10
7. [弗吉尼亚州禁止出售地理位置数据](#item-7) ⭐️ 6.0/10
8. [PeerTube：去中心化的联邦式开源视频平台](#item-8) ⭐️ 6.0/10
9. [西班牙下令将 Palantir 从公私企业中拉入黑名单](#item-9) ⭐️ 6.0/10
10. [从微分几何视角看哈密顿神经网络](#item-10) ⭐️ 6.0/10
11. [P 蛾子检索：通过查询时编排实现无图多跳检索（在 HotpotQA 上击败基于图的系统）(P)](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [自 Linux 6.9 起，LUKS 挂起功能停止清除内存中的磁盘加密密钥](https://mathstodon.xyz/@iblech/116769502749142438) ⭐️ 7.0/10

Linux 6.9 中一个静默的安全回归导致 LUKS 挂起功能不再清除内存中的磁盘加密密钥，该问题通过 NixOS 测试发现并已修复。

hackernews · IngoBlechschmid · 7月2日 15:25 · [社区讨论](https://news.ycombinator.com/item?id=48763035)

**标签**: `#linux`, `#security`, `#luks`, `#encryption`, `#kernel`

---

<a id="item-2"></a>
## [Podman v6.0.0 发布，网络与 Quadlet 功能升级](https://blog.podman.io/2026/07/introducing-podman-v6-0-0/) ⭐️ 7.0/10

Podman v6.0.0 正式发布，带来了改进的网络功能、增强的 Quadlet 管理，以及从旧版 BoltDB 存储自动迁移到 SQLite 的能力。该版本还引入了新的 `podman quadlet list` 子命令（最初在 v5.6.0 中加入）和 `podman system migrate --migrate-db` 标志（在 v5.8.0 中加入），以便简化数据库迁移。 作为主流 Docker 替代方案的重要版本，Podman v6.0.0 进一步验证了无守护进程（daemonless）、无 root 容器工作流的可行性，帮助团队降低攻击面并保持与 Docker 兼容的工具链。自动 SQLite 迁移降低了现有用户的运维成本，而持续完善的 Quadlet 功能让基于 systemd 的容器管理在生产环境中更加实用。 从 BoltDB 迁移到 SQLite 解决了长期存在的弃用警告，并提供了更健壮、社区支持更广泛的嵌入式数据库后端。网络方面的改进增强了 Podman 与 Docker 网络语义的兼容性，这对无需修改即可迁移 `docker-compose.yml` 栈的用户来说非常重要。Quadlet——用于管理容器、Pod、卷和网络的声明式 systemd 单元文件——仍然是 Podman 坚持无 root 优先理念的核心特性。

hackernews · soheilpro · 7月2日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=48762098)

**背景**: Podman 是由 Red Hat 最初开发的开源容器管理工具，运行容器无需长期运行的守护进程，这与 Docker 基于守护进程的架构形成对比。这种无守护进程（daemonless）设计降低了攻击面，并支持无 root（rootless）容器执行，让非特权用户无需提升权限即可运行容器。Quadlet 在 Podman 4.4 中引入，允许用户在 systemd 单元文件中声明容器及相关资源，将容器生命周期管理与 Linux 标准 init 系统集成在一起。Podman 保持了与 Docker 的 CLI 兼容性，许多现有工作流和 `docker-compose.yml` 文件几乎无需修改即可使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.podman.io/en/latest/markdown/podman-quadlet.1.html">podman-quadlet — Podman documentation</a></li>
<li><a href="https://www.redhat.com/en/blog/quadlet-podman">Make systemd better for Podman with Quadlet</a></li>
<li><a href="https://www.freecodecamp.org/news/how-to-use-different-container-runtimes-docker-podman-and-containerd-explained/">How to Use Different Container Runtimes: Docker, Podman, and Containerd Explained</a></li>

</ul>
</details>

**社区讨论**: 社区整体情绪非常积极，用户称赞 Podman 是优于 Docker 的实现，并分享了成功的迁移经验——尤其是那些因 Docker Desktop 内存占用问题而转向 Podman 的团队。有经验的用户强调 SQLite 迁移工具和 quadlet list 命令是期待已久的功能改进，另一些人则讨论了用于 CRI 兼容运行时的无 root 镜像构建，并分享了基于 Ansible 的 Quadlet 部署模板。讨论中未出现重大批评意见。

**标签**: `#podman`, `#containers`, `#devops`, `#rootless`, `#infrastructure`

---

<a id="item-3"></a>
## [日本最高法院裁定 AI 不能被列为专利发明人](https://japannews.yomiuri.co.jp/science-nature/technology/20260306-314930/) ⭐️ 7.0/10

日本最高法院裁定人工智能系统不能被指定为专利申请的发明人，进一步确认根据日本专利法，只有自然人才能拥有发明人身份。 此裁定使日本加入了包括美国、英国和欧盟在内的越来越多拒绝承认 AI 发明人身份的主要司法管辖区行列，塑造了国际先例，并影响企业如何在全球市场中保护 AI 生成的创新成果。 该裁定与英国 Thaler 诉专利总局长案的结论一致，也符合美国专利商标局（USPTO）的指南——即 AI 辅助的发明仍需要人类发明人。在研发中使用 AI 的公司需要确定人类贡献者以满足发明人要求，尽管 AI 辅助的发明本身仍可能获得专利授权。

hackernews · mushstory · 7月2日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=48761536)

**背景**: AI 发明人问题因 DABUS 案而引起全球关注。在该案中，Stephen Thaler 博士提交了专利申请，将他的 AI 系统"DABUS"（Device for the Autonomous Bootstrapping of Unified Sentience，自主引导统一意识装置）列为分形几何食品容器等发明的发明人。美国、英国、澳大利亚和欧洲的法院均已裁定 AI 不能成为法律意义上的发明人，但根本问题仍然存在争议。虽然 AI 不能作为发明人，但只要有自然人被列为发明人，许多司法管辖区仍允许对 AI 在过程中发挥重要作用的发明授予专利。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DABUS">DABUS - Wikipedia</a></li>
<li><a href="https://www.uspto.gov/subscription-center/2025/revised-inventorship-guidance-ai-assisted-inventions">Revised inventorship guidance for AI-assisted inventions</a></li>
<li><a href="https://www.congress.gov/crs_external_products/LSB/PDF/LSB11251/LSB11251.3.pdf">Artificial Intelligence and Patent Law - Congress.gov</a></li>

</ul>
</details>

**社区讨论**: 社区对该裁定普遍持支持态度，评论者强调 AI 缺乏问责能力，因此不应获得专利权益。一些人提出了实际的法律问题，即 AI 生成的发明是否可以以人类发明人的名义重新提交申请。少数评论质疑专利制度本身的前提，引用经济学研究表明专利并不一定能改善创新结果；也有评论认为这一争论完全没有必要，因为 AI 只是一个软件程序。

**标签**: `#AI`, `#patent-law`, `#intellectual-property`, `#legal-ruling`, `#Japan`

---

<a id="item-4"></a>
## [Hugging Face 与 Cerebras 合作推出基于 Gemma 4 的实时语音 AI](https://huggingface.co/blog/cerebras-gemma4-voice-ai) ⭐️ 7.0/10

Hugging Face 与 Cerebras 宣布合作，利用 Google 开源的 Gemma 4 模型运行在 Cerebras 的晶圆级推理硬件上，实现实时语音 AI 能力。该集成专门针对对话式语音应用对低延迟的要求。 实时语音 AI 要求端到端推理延迟足够低以支持自然对话（通常低于约 150 毫秒），这一直是开源模型部署的主要障碍。将 Gemma 4 的无编码器多模态架构与 Cerebras 的高吞吐推理硬件相结合，可能使低延迟、使用开源权重的语音助手变得显著更加实用和易于获取。 Cerebras 的 WSE-3 是全球最大的 AI 处理器，是一块大小相当于整块硅晶圆的单个芯片，可提供非常高的片上内存带宽——这是大语言模型快速推理的关键因素。Gemma 4 本身采用无编码器的多模态设计，将音频和视觉直接集成到语言模型中，消除了通常由独立视觉/音频编码器带来的额外延迟。

rss · HuggingFace Blog · 7月1日 00:00

**背景**: Cerebras Systems 构建晶圆级处理器——本质上把整块硅晶圆用作单个 AI 芯片——提供非常高的内存带宽以加速训练和推理。Google 的 Gemma 是源自 Gemini 线的开源权重模型系列；Gemma 4 同时发布了稠密版和混合专家（MoE）版本，支持 256K token 上下文窗口、超过 140 种语言以及原生多模态能力。Hugging Face 是开源模型分发和推理工具的主要枢纽，因此成为天然的发布合作伙伴。对于语音助手来说，端到端总延迟必须保持在约 150 毫秒以下才能在对话中感觉自然——这是一个紧张的时间预算，历史上一直推动开发者采用高度优化的专有技术栈。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://ai.google.dev/gemma/docs/core/model_card_4">Gemma 4 model card | Google AI for Developers</a></li>

</ul>
</details>

**标签**: `#voice-ai`, `#hugging-face`, `#cerebras`, `#gemma`, `#real-time-inference`

---

<a id="item-5"></a>
## [arXiv 将于 2026 年从康奈尔大学分拆为独立非营利组织](https://www.reddit.com/r/MachineLearning/comments/1ukjtlm/on_july_1_2026_arxiv_will_spin_out_from_cornell/) ⭐️ 7.0/10

2026 年 7 月 1 日，arXiv 将结束其在康奈尔大学 25 年的隶属关系，转型为一家独立的非营利组织，主要资金来源为 Simons Foundation 和 Schmidt Sciences。此次转型还伴随着视觉品牌的调整，arXiv 将弃用标志性的红色配色，采用全新的视觉形象。 arXiv 是全球使用最广泛的预印本服务器，托管着数百万篇涵盖物理、数学、计算机科学等领域的论文，是全球科研界关键的基础设施。在主要慈善基金的支持下确保其财务和制度上的独立，保障了其长期可持续发展，并保护了支撑现代科学交流的开放获取模式。 此次分拆得到了两大慈善机构的支持：长期资助数学和基础科学研究的 Simons Foundation，以及由前谷歌 CEO Eric Schmidt 和 Wendy Schmidt 于 2024 年创立的 Schmidt Sciences。机构结构的变化伴随着品牌重塑，arXiv 将放弃其长期使用的红色配色方案。

reddit · r/MachineLearning · /u/Nunki08 · 7月1日 12:07

**背景**: arXiv 创立于 1991 年，自 21 世纪初由康奈尔大学托管，是一个科学预印本开放获取仓库——研究者在正式同行评审之前或同时公开分享论文的平台。它使研究者能够快速传播研究成果，在物理、天文学、数学和机器学习等领域占据主导地位。arXiv、bioRxiv 和 medRxiv 等预印本服务器已成为快节奏科学社区的重要基础设施，尽管所发布的论文未经同行评审。Simons Foundation 和 Schmidt Sciences 都是资助科学研究和开放科学倡议的主要慈善机构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ArXiv">arXiv - Wikipedia</a></li>
<li><a href="https://www.schmidtsciences.org/">Home - Schmidt Sciences</a></li>
<li><a href="https://scienceinsights.org/what-is-a-preprint-meaning-servers-and-peer-review/">What Is a Preprint? Meaning, Servers, and Peer Review</a></li>

</ul>
</details>

**标签**: `#arxiv`, `#open-science`, `#research-infrastructure`, `#preprint-server`, `#academic-publishing`

---

<a id="item-6"></a>
## [Ollama v0.31.1：苹果芯片上 Gemma 4 推理速度提升高达 90%](https://github.com/ollama/ollama/releases/tag/v0.31.1) ⭐️ 6.0/10

Ollama v0.31.1 通过自动调优的多 token 预测（MTP），在苹果芯片上将 Gemma 4 推理速度提升高达约 90%，该加速默认开启且不改变模型输出。此次发布还包含 Gemma 4 MoE 模型加载路径的收紧、升级后的 MLX 引擎（新增小批量矩阵乘法 kernel）以及底层 llama.cpp 升级至 build 9840。 对于在 Mac 上运行本地大模型的开发者（尤其是基于 Gemma 4 构建的编程代理），这是 Ollama 报告过的最大单版本推理加速之一，显著提升了端侧代理工作流的速度与可用性。同时也表明 MTP 式的投机解码正在主流本地运行框架中成熟为默认优化，而非小众实验性特性。 MTP 加速在运行时自动调优——Ollama 动态决定生成多少个草稿 token——因此用户无需任何配置即可获得收益，且不会改变输出结果。底层增益来自 MLX 引擎的改进（包括更适合 Gemma 4 MoE 路由的新小批量矩阵乘法 kernel）以及 llama.cpp build 9840 的升级，这意味着提速并非仅源自 MTP，而是引擎协同调优的结果。

github · github-actions[bot] · 6月30日 22:10

**背景**: 多 token 预测（MTP）是一种由 Meta 和 DeepSeek 推广的技术，模型一次起草多个未来 token，然后并行验证，从而在不改变输出的前提下显著提升推理吞吐。MLX 是苹果开源的面向 Apple Silicon 的数组框架，旨在通过统一内存高效运行于 M 系列芯片。Gemma 4 是谷歌的开源权重模型系列，其部分容量采用混合专家（MoE）架构——每个 token 仅激活一小部分专家子网络——因此高效的小批量 kernel 尤为重要。Ollama 是一个流行的开源运行框架，集成了 llama.cpp 和 MLX 后端，让用户通过简单命令在本地运行大语言模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/multi-token-prediction-mtp">Multi - Token Prediction ( MTP )</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/ mlx : MLX : An array framework for Apple silicon</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**标签**: `#ollama`, `#apple-silicon`, `#gemma`, `#inference-optimization`, `#multi-token-prediction`

---

<a id="item-7"></a>
## [弗吉尼亚州禁止出售地理位置数据](https://www.hunton.com/privacy-and-cybersecurity-law-blog/virginia-bans-sale-of-geolocation-data) ⭐️ 6.0/10

弗吉尼亚州已禁止出售地理位置数据，成为首批颁布此类立法的州之一，该法律将于 7 月 1 日生效。

hackernews · toomuchtodo · 7月2日 21:03 · [社区讨论](https://news.ycombinator.com/item?id=48767347)

**标签**: `#privacy`, `#data-protection`, `#legislation`, `#geolocation`, `#cybersecurity`

---

<a id="item-8"></a>
## [PeerTube：去中心化的联邦式开源视频平台](https://github.com/Chocobozzz/PeerTube) ⭐️ 6.0/10

一个获得 432 点赞和 190 条评论的 Hacker News 讨论让 PeerTube 重新受到关注。PeerTube 是一个基于 ActivityPub 协议的成熟开源联邦式视频平台，讨论中既展示了其技术能力，也指出了实际采用中面临的挑战。 PeerTube 代表了少数可行的 YouTube 等中心化视频平台替代方案之一，社区讨论揭示了任何去中心化视频平台要与主流平台竞争所必须克服的关键障碍——变现、内容发现和受众覆盖。 PeerTube 利用 P2P 技术（WebTorrent）在同时观看的用户之间分摊带宽，并通过 ActivityPub 协议在独立运营的实例之间实现联邦化。有用户成功利用它通过第三方网站嵌入播放器来托管开源教程视频，从而绕过了 YouTube 的身份验证要求。

hackernews · doener · 7月2日 11:17 · [社区讨论](https://news.ycombinator.com/item?id=48759634)

**背景**: PeerTube 基于 ActivityPub 构建，ActivityPub 是 W3C 标准化的去中心化社交网络协议，定义了客户端到服务器（C2S）和服务器到服务器（S2S）两套 API，是 Fediverse（联邦宇宙）的核心协议，连接着 Mastodon、Pixelfed 等平台。联邦式架构允许独立服务器（实例）在保持自治的同时实现互操作和内容共享。PeerTube 将这一模式专门应用于视频托管，并加入了 P2P 带宽共享以降低服务器成本——这对于远比文本和图片更耗费资源的媒体类型至关重要。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ActivityPub">ActivityPub - Wikipedia</a></li>
<li><a href="https://github.com/w3c/activitypub">GitHub - w3c/activitypub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Federated_architecture">Federated architecture - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍认为 PeerTube 技术上有前景，但面临着巨大的社会和经济障碍。一位拥有约 10 万订阅者的专业 YouTuber 强调，缺乏变现机制使其对全职创作者来说不切实际，因为高质量视频制作每 20 分钟可能需要 40 小时以上的熟练劳动。其他用户指出，除开源和隐私类小众领域外，平台内容生态仍显薄弱，与 TikTok 和 YouTube 算法推荐流竞争，仅靠一个 `<video>` 元素远远不够。不过，一位活跃用户报告了一个成功的细分用例——为一个开源项目托管使用自由软件制作的教程视频。

**标签**: `#open-source`, `#decentralization`, `#video-platform`, `#federation`, `#activitypub`

---

<a id="item-9"></a>
## [西班牙下令将 Palantir 从公私企业中拉入黑名单](https://clashreport.com/world/articles/spain-orders-blacklist-of-us-tech-giant-palantir-from-public-and-private-companies-fsnc2z17gjv) ⭐️ 6.0/10

西班牙已下令公私企业将美国科技巨头 Palantir Technologies 拉入黑名单，理由是对该公司处理机密数据的方式存在国家安全方面的担忧。该决定源于官方对与国家安全相关的机密信息可能被滥用日益增长的担忧。 此举代表了一个重要欧盟成员国对一家著名美国国防与情报技术承包商采取的重大地缘政治立场。它可能为其他欧洲国家重新评估其在敏感政府工作负载中对美国数据分析平台的依赖开创先例。 据报道，该黑名单同时适用于公共和私营部门企业，这意味着西班牙的限制范围超出了政府采购领域。Palantir 于 2003 年由 Peter Thiel、Alex Karp 等人创立，专注于数据集成和分析软件，广泛被联邦机构用于军事情报和政府运营。

hackernews · mgh2 · 7月2日 15:02 · [社区讨论](https://news.ycombinator.com/item?id=48762725)

**背景**: Palantir Technologies 是一家总部位于佛罗里达州迈阿密的美国上市公司，由 Peter Thiel、Stephen Cohen、Joe Lonsdale、Alex Karp 和 Nathan Gettings 于 2003 年创立。该公司开发数据集成和分析软件，客户群包括联邦机构、州和地方政府以及私营企业。Palantir 以向政府客户提供情报和国防相关软件而闻名，这使其既具有战略重要性，又存在政治争议，尤其是在欧洲的数据隐私和主权问题上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Palantir">Palantir - Wikipedia</a></li>
<li><a href="https://builtin.com/articles/what-is-palantir">What Is Palantir? The Company Behind Government AI Tools ...</a></li>
<li><a href="https://www.palantir.com/">Home | Palantir</a></li>

</ul>
</details>

**社区讨论**: 社区情绪呈现两极化。部分评论者赞扬西班牙的方向，并表示有兴趣看到其他国家采取类似行动；但也有评论者持怀疑态度，认为真正动机可能是采购偏好——倾向于选择国内或盟国供应商（如华为的对标产品或西班牙本国的 Indra），而非出于真正的安全考虑。多位用户要求提供关于所引用的具体国家安全威胁的更详细信息，一位评论者指出 Palantir 的 CEO 似乎与现实脱节。

**标签**: `#palantir`, `#tech-policy`, `#national-security`, `#europe`, `#government-procurement`

---

<a id="item-10"></a>
## [从微分几何视角看哈密顿神经网络](https://www.reddit.com/r/MachineLearning/comments/1ukzdnj/hamiltonian_neural_networks_from_a_differential/) ⭐️ 6.0/10

一篇公司博客文章从微分几何的角度重新诠释了哈密顿神经网络（Greydanus 等人，2019 年），认为诺特定理是连接守恒定律与物理信息神经网络泛化能力之间缺失的桥梁。 大多数关于 HNN 的教程都侧重于损失函数的机制，使实践者缺乏对这类架构为何能够泛化的直觉。通过诺特定理将该框架与对称性原理联系起来，本文提供了概念基础，可能帮助研究者设计更有效的物理信息模型，并理解动力系统学习中的归纳偏置。 该文章数学内容较深，但包含了交互式可视化元素；它将诺特定理（连续对称性与守恒量之间的对应关系）置于核心位置，用以理解物理信息网络如何实现泛化而非过拟合。

reddit · r/MachineLearning · /u/FlameOfIgnis · 7月1日 21:55

**背景**: 哈密顿神经网络由 Greydanus 等人于 2019 年提出，用神经网络参数化物理系统的哈密顿量并直接从数据中学习，使用广义坐标 q（位置）和 p（动量）。这一结构从设计上保证了能量守恒，解决了通用神经网络可能违反物理定律的关键缺陷。诺特定理由数学家 Emmy Noether 提出，确立了物理系统的每个连续对称性都对应一个守恒量；近年来通过 Noether's Razor 和 Noether Networks 等工作与机器学习联系起来，利用对称性作为归纳偏置来提升泛化能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://greydanus.github.io/2019/05/15/hamiltonian-nns/">Hamiltonian Neural Networks</a></li>
<li><a href="https://fabianfuchsml.github.io/noether/">Noether’s Theorem, Symmetries, and Invariant Neural Networks Noether’s Razor: Learning Conserved Quantities - arXiv.org Noether’s Razor: Learning Conserved Quantities AI Meets Noether’s Theorem – Symmetry, Conservation Laws, and ... [2105.02716] Noether's Learning Dynamics: Role of Symmetry ... Noether Networks: meta-learning useful conserved quantities</a></li>
<li><a href="https://arxiv.org/html/2410.08087v1">Noether’s Razor: Learning Conserved Quantities - arXiv.org</a></li>

</ul>
</details>

**标签**: `#Hamiltonian Neural Networks`, `#Differential Geometry`, `#Physics-Informed ML`, `#Noether's Theorem`, `#Neural ODEs`

---

<a id="item-11"></a>
## [P 蛾子检索：通过查询时编排实现无图多跳检索（在 HotpotQA 上击败基于图的系统）(P)](https://www.reddit.com/r/MachineLearning/comments/1ukotww/p_mothretrieval_graphfree_multihop_retrieval_via/) ⭐️ 6.0/10

MOTHRAG 是一个开源的无图多跳 RAG 框架，通过在密集索引上进行查询时编排，在 HotpotQA、2WikiMultiHopQA 和 MuSiQue 数据集上的基准测试结果优于 GraphRAG、HippoRAG 和 RAPTOR，同时支持增量更新而无需重新索引。

reddit · r/MachineLearning · /u/Annual-Commercial563 · 7月1日 15:26

**标签**: `#RAG`, `#multi-hop-retrieval`, `#knowledge-graph`, `#dense-retrieval`, `#open-source`

---