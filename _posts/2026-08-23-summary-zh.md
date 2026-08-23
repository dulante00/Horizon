---
layout: default
title: "Horizon Summary: 2026-08-23 (ZH)"
date: 2026-08-23
lang: zh
---

> 从 41 条内容中筛选出 12 条重要资讯。

---

1. [复杂系统为何会失败 (1998)](#item-1) ⭐️ 8.0/10
2. [恶意软件入侵安卓车载主机固件](#item-2) ⭐️ 7.0/10
3. [什么是编排框架（Harness）？](#item-3) ⭐️ 7.0/10
4. [GLM-5.3 一天内完成平板 Root，美国模型却被安全护栏拦下](#item-4) ⭐️ 7.0/10
5. [斯洛伐克在交通测速摄像头中发现俄罗斯后门](#item-5) ⭐️ 7.0/10
6. [MartyPC：用 Rust 编写的周期精确早期 IBM PC 模拟器](#item-6) ⭐️ 7.0/10
7. [Qwen 3 8B（27B MoE）30 分钟逆向工程商业应用许可证验证](#item-7) ⭐️ 7.0/10
8. [Kimi K3（2.8 万亿参数）在 8 张 B300 上以 92 tok/s 运行，每百万 token 成本 190 美元](#item-8) ⭐️ 7.0/10
9. [ollama/ollama 发布了 v0.33.0-rc2 版本](#item-9) ⭐️ 6.0/10
10. [Wi-Fi 8 是多年来首次不再一味追求速度的无线升级](#item-10) ⭐️ 6.0/10
11. [“All Spark”集群：从 16 到 36 台 DGX Spark 的升级之路](#item-11) ⭐️ 6.0/10
12. [在 5 万张浏览器截图上微调 4.5 亿参数 VLM，UI 理解准确率大幅提升](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [复杂系统为何会失败 (1998)](https://how.complexsystems.fail/) ⭐️ 8.0/10

关于复杂系统失败固有特性的经典论文，主张在复杂系统中根本原因分析往往具有误导性，灾难性失败源于正常运行中的漂移，而非单一原因。

hackernews · shortcrct · 8月23日 15:13 · [社区讨论](https://news.ycombinator.com/item?id=49409473)

**标签**: `#complex-systems`, `#reliability-engineering`, `#incident-analysis`, `#sre`, `#systems-thinking`

---

<a id="item-2"></a>
## [恶意软件入侵安卓车载主机固件](https://securelist.com/android-head-unit-malware/121106/) ⭐️ 7.0/10

安全研究人员发现，恶意软件通过官方第一方 OTA（空中下载）固件更新，分发至廉价的中国安卓后市场车载主机中。该恶意软件无法自我传播到其他安卓车载主机，也不会影响 Android Auto，因为后者本质上是一个屏幕镜像协议。 这一发现凸显了严重的汽车和物联网网络安全风险，因为许多后市场车载主机直接连接车辆的 CAN 总线，而 CAN 总线控制着刹车和转向等关键功能。被入侵的车载主机有可能被武器化，用于直接导致车祸，这引发了人们对日益软件化的汽车安全性的紧迫担忧。 目前威胁范围仅限于碰巧运行安卓系统的特定廉价中国后市场产品，恶意软件通过合法的 OTA 渠道分发，而非利用 OTA 机制本身的漏洞。然而，由于这些车载主机通常与用户手机配对，并且可能具有 CAN 总线访问权限，研究人员警告未来的变种可能会横向传播或直接干扰车辆控制。

hackernews · campuscodi · 8月23日 13:05 · [社区讨论](https://news.ycombinator.com/item?id=49408550)

**背景**: 后市场安卓车载主机是车主安装的第三方信息娱乐系统，通常用于为旧车增添导航和智能手机互联等现代功能。CAN（控制器局域网）总线是由博世于 1983 年开发并于 1986 年标准化的车载通信协议，允许车内各种微控制器和电子控制单元（ECU）无需主机即可相互通信。由于 CAN 总线在车辆内部网络中默认受到信任，任何连接到它的设备——包括信息娱乐车载主机——都有可能发送影响转向、刹车或加速的指令。OTA 更新允许制造商远程推送固件修复和新功能，但如果更新渠道遭到入侵或缺乏适当的身份验证，它们也会形成一个极具吸引力的攻击面。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/CAN_bus">CAN bus - Wikipedia</a></li>
<li><a href="https://www.bytesnap.com/news-blog/beware-ota-dangers-over-the-air-updates/">Beware the OTA: The Dangers of Over the Air Updates</a></li>
<li><a href="https://www.atotodirect.com/en-gb/blogs/news/oem-vs-aftermarket-car-infotainment-upgrade-guide">OEM vs. Aftermarket Car Infotainment : Is It Time to Upgrade?</a></li>

</ul>
</details>

**社区讨论**: 社区情绪混合但参与度高：评论者澄清说，即时威胁范围较窄（仅限于廉价中国后市场设备，不涉及 Android Auto 或主流系统），但提出了令人警惕的前瞻性担忧。Retr0id 指出，由于车载主机与手机配对，未来的恶意软件可能会横向传播；dzdt 警告 CAN 总线连接可能允许恶意软件直接导致车祸；jackdecker 表示驻留在汽车中的恶意软件比手机恶意软件更令人恐惧；davoneus 预测未来会出现"汽车杀毒软件"市场。

**标签**: `#android`, `#automotive-security`, `#malware`, `#iot-security`, `#vulnerability-research`

---

<a id="item-3"></a>
## [什么是编排框架（Harness）？](https://earendil.com/posts/what-is-a-harness/) ⭐️ 7.0/10

本文以通俗易懂的方式解释了大语言模型智能体（LLM Agent）语境下的 "harness" 是什么，将其视为将模型的原始能力转化为可用智能体系统的关键脚手架。

hackernews · tosh · 8月23日 14:24 · [社区讨论](https://news.ycombinator.com/item?id=49409092)

**标签**: `#llm-agents`, `#ai-infrastructure`, `#agent-frameworks`, `#prompt-engineering`, `#tooling`

---

<a id="item-4"></a>
## [GLM-5.3 一天内完成平板 Root，美国模型却被安全护栏拦下](https://ericpardee.github.io/fire-hd-ownership/) ⭐️ 7.0/10

一项独立实验对比了四款 AI 模型在为一台价值 266 美元的 Fire HD 平板进行 Root 操作时的表现，结果发现智谱 AI 开发的中国模型 GLM-5.3 成功发现了未修补的漏洞并构建了可用的漏洞利用程序，在大约一天内完成了 Root，而美国模型则因安全护栏而拒绝协助。 这一真实场景基准测试凸显了中美 AI 模型在攻防安全这类双重用途任务上日益扩大的能力和政策分歧，迫使人们思考安全护栏会如何影响合法网络安全研究的竞争力，以及严格的限制政策是否会将漏洞发现工作推向透明度更低的参与者。 GLM-5.3 由智谱 AI 于 2026 年 8 月 14 日发布，基于与 GLM-5.2 相同的基座模型，所有改进均来自后训练，在 Z.ai Code Bench 上取得了 50%的性能提升，并具备更强的长链路智能体能力，特别适合多步骤漏洞利用开发。

hackernews · dr_pardee · 8月23日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=49409073)

**背景**: Rooting 是为 Android 设备获取管理员（root）权限的过程，使用户可以卸载预装应用、安装自定义操作系统并完全控制文件系统——类似于 iOS 上的越狱。攻防安全与漏洞研究是指主动探测软硬件中未修补的安全缺陷并开发概念验证漏洞利用，这是一项合法但具有双重用途的学科，伦理黑客、渗透测试人员和安全研究人员都在从事。AI 模型正越来越多地通过智能体工作流来完成这些工作，将逆向工程、代码分析和漏洞利用生成串联起来，使其成为网络安全能力格局中的新变量。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://z.ai/blog/glm-5.3">GLM-5.3: Frontier Coding with Emergent Cyber Capabilities - z.ai</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.3">GLM-5.3 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>
<li><a href="https://en.wikipedia.org/wiki/Rooting_(Android)">Rooting (Android) - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍对 GLM-5.3 的表现印象深刻，但围绕其影响展开了讨论：一些人赞扬 AI 辅助逆向工程对开源和 Linux 硬件支持的价值，另一些人则指出过度严格的安全护栏（一位用户提到 Opus 4.8 似乎也已加入安全分类器）与可能助长有害攻击之间的取舍。几位用户分享了实用替代方案，包括无需 Root 即可去广告和精简系统的 Fire Toolbox，还有用户分享了自家 AI 智能体完成逆向工程 iOS dyld 缓存等惊人任务的经历。

**标签**: `#AI models`, `#cybersecurity`, `#vulnerability research`, `#AI safety`, `#model comparison`

---

<a id="item-5"></a>
## [斯洛伐克在交通测速摄像头中发现俄罗斯后门](https://risky.biz/risky-bulletin-slovakia-finds-russian-backdoor-in-traffic-speed-cameras/) ⭐️ 7.0/10

斯洛伐克在为全国部署采购的交通测速摄像头中发现了俄罗斯植入的后门。此前有人指出这些设备外观与俄罗斯制造的摄像头完全一致，且序列号与已知的俄方库存相符，调查后发现这些摄像头向任何知晓其广播 IP 地址的人开放实时视频流，无需任何身份验证或密码。 这一事件凸显了关键基础设施领域供应链被入侵的系统性风险——攻击者可以在设备尚未到达采购国之前就植入漏洞。除了直接的国家安全问题外，该案例还引发了一个更深层的问题：还有多少其他国家的监控或物联网设备可能正在不知不觉中运行被篡改的硬件。 这些摄像头通过开放的 IP 地址广播未经身份验证的实时视频流，意味着任何互联网用户无需凭证即可查看交通监控画面。由于独立观察者将设备序列号与已知的俄罗斯库存进行交叉比对，后门才被发现——此前政府还曾否认任何与俄罗斯原产设备的关联。

hackernews · dredmorbius · 8月23日 14:38 · [社区讨论](https://news.ycombinator.com/item?id=49409200)

**背景**: 硬件后门是指直接嵌入设备固件或芯片中的恶意功能，相比软件后门更难被发现和清除。对关键基础设施的供应链攻击——例如政府机构、监控系统以及物联网网络——已成为公认的攻击向量，CISA 等机构多次将俄罗斯和中国的国家级行为体认定为主要的实施者。SecureBoot（安全启动）和可信启动链旨在通过加密签名验证固件完整性，但其有效性取决于签名密钥属于部署方组织还是仍由制造商控制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.startupdefense.io/blog/what-is-backdoor">What is Backdoor</a></li>
<li><a href="https://www.cisa.gov/news-events/cybersecurity-advisories/aa20-352a">Advanced Persistent Threat Compromise of Government ... - CISA</a></li>
<li><a href="https://www.exiger.com/perspectives/fortifying-critical-infrastructure-5-insights-on-securing-supply-chains/">Fortifying Critical Infrastructure: 5 Insights from ... - Exiger</a></li>

</ul>
</details>

**社区讨论**: 评论者强调了对可审计开源固件的需求，并认为 SecureBoot 应当使用部署国的密钥而非制造商的密钥进行签名。多名用户指出，斯洛伐克因长期亲俄的政治立场而更容易遭受此类攻击。另一些用户将讨论范围扩大，认为这种供应链问题并非斯洛伐克独有，同样适用于美国各地使用的 Flock 等西方监控系统的部署。

**标签**: `#cybersecurity`, `#supply-chain-security`, `#IoT-security`, `#geopolitics`, `#critical-infrastructure`

---

<a id="item-6"></a>
## [MartyPC：用 Rust 编写的周期精确早期 IBM PC 模拟器](https://martypc.net/) ⭐️ 7.0/10

MartyPC 是一款用 Rust 编写的跨平台、周期精确的早期 IBM PC 模拟器，其独特之处在于使用真实 CPU 物理测试平台来验证模拟的准确性，覆盖原版硬件的每一个时序细节和怪异行为。 它代表了复古计算模拟领域的高质量工程实践，展示了一种在业余模拟器项目中罕见的硬件在环验证方法论，并体现了 Rust 在底层系统模拟工作中的优势。 该模拟器在周期级别而非仅仅指令级别上复现时序和硬件怪异行为，并且除了其他硬件模拟外还包含对 Adlib 声卡的支持。开发者利用 LLM 辅助编程来加速开发，同时受益于 Rust 的内存安全保证。

hackernews · boilerupnc · 8月23日 03:13 · [社区讨论](https://news.ycombinator.com/item?id=49405816)

**背景**: 周期精确模拟器会模拟构成每条 CPU 指令的每一个内部步骤，确保对时序敏感的软件（如延时循环或精确计时的汇编代码）在模拟器上与真实硬件产生完全相同的结果——这与指令精确模拟器不同，后者将指令视为不可分割的单元。基于 Intel 8088/8086 处理器的早期 IBM PC 拥有大量 1980 年代至 1990 年代初的软件库，包括常常依赖精确硬件时序的游戏和生产力软件。物理 CPU 测试平台是定制的电路，将真实的古董处理器与现代测量设备连接起来，使开发者能够捕获真实硬件的行为作为验证软件模拟的基准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://retrocomputing.stackexchange.com/questions/1191/what-exactly-is-a-cycle-accurate-emulator/1194">emulation - What exactly is a cycle - accurate emulator ?</a></li>
<li><a href="https://news.ycombinator.com/item?id=13052964">What does " cycle - accurate " mean? The README... | Hacker News</a></li>

</ul>
</details>

**社区讨论**: 开发者（GloriousCow）积极与评论者互动，直接回答问题。社区成员称赞物理硬件验证方法是突出的亮点，对包含 Adlib 支持表示赞赏（指出 Soundblaster 并非唯一相关的声卡），并强调了 Rust 因其线程模型、内存安全性以及与 LLM 辅助编程的良好兼容性而非常适合模拟器开发。

**标签**: `#rust`, `#emulator`, `#retro-computing`, `#hardware-validation`, `#ibm-pc`

---

<a id="item-7"></a>
## [Qwen 3 8B（27B MoE）30 分钟逆向工程商业应用许可证验证](https://www.xda-developers.com/qwen-3-8-27b-reverse-engineering-job-frontier-model/) ⭐️ 7.0/10

一位开发者让 Qwen 3 8B（一个 27B 参数的 MoE 模型）逆向分析一款商业应用的许可证验证逻辑，该模型在 30 分钟内完成了任务，并自主发现了一个完整性哈希不匹配的问题，最终逐字节修正成功。 这表明较小的开源权重模型正日益具备执行逆向工程等复杂技术任务的能力，对软件安全研究、AI 辅助分析的民主化，以及降低合法安全工作与潜在滥用的门槛都具有重要意义。 该模型表现出显著的坚持性和自我修正能力：当其首次密钥恢复尝试生成了一个可用的密钥但未通过完整性哈希校验时，它识别出该不匹配并迭代修正，直至逐字节匹配成功。作为 MoE 模型，它共有 27B 参数，但每个 token 仅激活约 8B 参数，在能力与计算效率之间取得了平衡。

hackernews · raybb · 8月23日 10:02 · [社区讨论](https://news.ycombinator.com/item?id=49407507)

**背景**: 混合专家（Mixture of Experts, MoE）是一种模型架构，其中模型包含大量"专家"子网络，但每次只激活其中的一部分来处理给定的 token，从而在保持较小计算开销的同时拥有更大的总参数规模。Qwen 3 是阿里巴巴开发的开源权重模型系列，采用 Apache 2.0 许可证发布。逆向工程许可证验证涉及反汇编已编译的二进制代码、理解加密操作（密钥恢复、签名验证、哈希校验）以及重建验证逻辑——这项任务传统上需要深厚的汇编语言和密码学专业知识，一直被视为只有大型前沿模型才能胜任的基准测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained - Hugging Face</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-27B">Qwen/Qwen3.8-27B · Hugging Face</a></li>
<li><a href="https://arxiv.org/abs/2507.11181">[2507.11181] Mixture of Experts in Large Language Models Mixture of Experts Explained - Hugging Face A Closer Look into Mixture-of-Experts in Large Language Models A Closer Look into Mixture-of-Experts in Large Language Models Understanding Mixture of Experts (MoE): The Architecture ... Applying Mixture of Experts in LLM Architectures | NVIDIA ...</a></li>

</ul>
</details>

**社区讨论**: 评论者表达了多元且积极的观点。一些人赞扬了该模型令人印象深刻的自我修正行为，指出它识别并修复了其他模型可能会忽略的完整性哈希不匹配问题。其他人则对"最难任务"的表述提出反驳，认为具有明确真假判定条件的任务实际上是 AI 辅助编码获益最大的领域，而非面临最大挑战的领域。多位评论者讨论了更广泛的影响，包括对本地模型内置拒绝机制的挫败感——这些限制可能只约束普通用户，而有组织犯罪却能在没有这些限制的情况下使用最佳模型。一位评论者还将此与类似的测试进行比较，其中 GLM-5.3 在一天内完成了平板 root 任务。

**标签**: `#reverse-engineering`, `#open-source-llms`, `#qwen`, `#ai-assisted-coding`, `#software-security`

---

<a id="item-8"></a>
## [Kimi K3（2.8 万亿参数）在 8 张 B300 上以 92 tok/s 运行，每百万 token 成本 190 美元](https://www.reddit.com/r/LocalLLaMA/comments/1vw1j2p/i_hosted_kimi_k3_28t_parameters_using_8_b300s_92/) ⭐️ 7.0/10

一位工程师使用 vLLM 和原生 MXFP4 量化，在 8 张 NVIDIA B300 GPU 上部署了 Kimi K3（2.8 万亿参数）模型，实现了稳态 92 tok/s 的解码吞吐，每百万输出 token 成本为 190 美元。同时对比测试的 Unsloth 1-bit Dynamic GGUF（UD-IQ1_S，594 GB）在 8 张 A100-80GB 上仅能达到约 9 tok/s，首 token 延迟 7-60 秒，每百万 token 成本约 620 美元——尽管硬件时租便宜 2.8 倍，单 token 成本反而高出 3.3 倍。 这是首次公开的在 NVIDIA 新一代 B300 硬件上对 2.8 万亿参数 MoE 前沿模型进行的大规模实测基准，为考虑自托管的从业者提供了具体的成本和吞吐数据。原生 MXFP4（高端 GPU）与 1-bit GGUF（普通 GPU）的直接对比表明，廉价的时租价格在解码吞吐较低的情况下可能产生误导，这改变了团队评估万亿参数模型部署经济性的方式。 B300 配置使用 8 路张量并行，冷启动约 27 分钟（加载 1.56 TB 权重、JIT 编译、51 次 CUDA graph 捕获）；首 token 延迟 0.92-1.02 秒，4 个提示词的解码平均速度为 83 tok/s。单次干净运行的 GPU 成本约为 36 美元，而集群保持热备 24 小时在 Modal 上的费用为 1,363 美元/天（时租 56.79 美元）。Unsloth 的 1-bit 量化出人意料地保持了质量——算术正确、文本连贯——表明瓶颈在于 llama.cpp 的串行解码速度，而非模型保真度。

reddit · r/LocalLLaMA · /u/OtherRaisin3426 · 8月23日 08:25

**背景**: Kimi K3 是月之暗面（Moonshot AI）发布的 2.8 万亿参数混合专家（MoE）语言模型，在原生 4 位精度下需要约 1.56 TB 显存，因此需要多 GPU 配置。MXFP4（微缩放 FP4）是一种硬件加速的 4 位浮点格式，采用共享块指数，在将内存占用减半（相比 FP8）的同时保持动态范围；它在 NVIDIA 最新一代数据中心 GPU 上获得原生支持。vLLM 是一个开源推理引擎，通过张量并行将模型权重分片到多张 GPU 上；而 llama.cpp 配合 GGUF（一种量化容器格式）通常用于本地或量化部署，常以 1-3 位低精度运行以便在消费级硬件上容纳大模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2509.23202">Bridging the Gap Between Promise and Performance for Microscaling ...</a></li>
<li><a href="https://unsloth.ai/docs/basics/dynamic-3.0-ggufs">Unsloth Dynamic 3.0 GGUFs | Unsloth Documentation</a></li>
<li><a href="https://docs.vllm.ai/en/latest/serving/parallelism_scaling/">Parallelism and Scaling - vLLM</a></li>

</ul>
</details>

**标签**: `#Kimi-K3`, `#large-model-deployment`, `#vLLM`, `#GPU-benchmarks`, `#model-quantization`

---

<a id="item-9"></a>
## [ollama/ollama 发布了 v0.33.0-rc2 版本](https://github.com/ollama/ollama/releases/tag/v0.33.0-rc2) ⭐️ 6.0/10

Ollama v0.33.0-rc2 发布候选版本，改进了 Claude Desktop 集成，并显著修复了预填充恢复点和 KV 缓存处理相关的缓存问题。

github · github-actions[bot] · 8月21日 22:52

**标签**: `#ollama`, `#release-notes`, `#llm-infrastructure`, `#caching`, `#claude-integration`

---

<a id="item-10"></a>
## [Wi-Fi 8 是多年来首次不再一味追求速度的无线升级](https://www.xda-developers.com/wi-fi-8-first-wireless-upgrade-years-isnt-chasing-speed-home-networks-need-it/) ⭐️ 6.0/10

Wi-Fi 8 标志着无线标准的一次理念转变，它优先考虑可靠性、漫游能力以及真实使用场景下的性能，而非那些在实践中很少能达到的理论峰值速度。

hackernews · taubek · 8月23日 06:41 · [社区讨论](https://news.ycombinator.com/item?id=49406539)

**标签**: `#wifi-8`, `#networking`, `#wireless-standards`, `#802.11`, `#infrastructure`

---

<a id="item-11"></a>
## [“All Spark”集群：从 16 到 36 台 DGX Spark 的升级之路](https://www.reddit.com/r/LocalLLaMA/comments/1vvv7iv/the_all_spark_cluster_upgrading_from_16_36_dgx/) ⭐️ 6.0/10

一位家用实验室爱好者将其个人 DGX Spark 集群从 16 个节点扩展到 36 个节点（4.6TB 统一内存），通过自定义编排技术同时运行最先进模型以及嵌入、视频/图像生成和音频工作负载，打造多智能体能力集群。

reddit · r/LocalLLaMA · /u/Kurcide · 8月23日 02:38

**标签**: `#DGX-Spark`, `#GPU-clustering`, `#local-llama`, `#homelab`, `#agent-infrastructure`

---

<a id="item-12"></a>
## [在 5 万张浏览器截图上微调 4.5 亿参数 VLM，UI 理解准确率大幅提升](https://www.reddit.com/r/LocalLLaMA/comments/1vw9k4k/1100_44100_finetuning_a_450m_vlm_on_50k_browser/) ⭐️ 6.0/10

一位实践者在 5 万张浏览器截图上对一个 4.5 亿参数的视觉语言模型（VLM）进行了微调，使其在 UI 理解任务上的准确率从 1/100 提升到 44/100，从接近零的基线表现实现了显著的相对改进。 这一实验表明，即使是参数量较小（4.5 亿）的开源 VLM，也可以通过适度的微调数据集有效专门用于浏览器自动化和 UI 理解任务，这对于构建轻量级、可本地运行工具、且不依赖大型前沿模型的开发者来说是一个令人鼓舞的信号。 该模型参数量仅为 4.5 亿，远小于典型的前沿 VLM（通常为 70 亿以上），所使用的基准是一个包含 100 个样本的 UI 理解测试，因此最终的绝对得分（44/100）表明该任务的能力有意义但仍然有限。

reddit · r/LocalLLaMA · /u/ButtercupLyn100 · 8月23日 15:04

**背景**: 视觉语言模型（VLM）是一种多模态人工智能，可以同时处理图像和文本，从而回答关于图片的问题或描述视觉场景。微调是一种技术，即在预训练模型的基础上用较小的、任务特定的数据集进一步训练，使其适应新领域——在本案例中是解读浏览器截图以理解 UI。传统的浏览器自动化任务通常需要大型通用模型或手工构建的计算机视觉流水线，因此专门化的小型 VLM 可能为本地部署提供一种更高效的中间方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://voxel51.com/glossary/vision-language-model-vlm">What is a vision - language model ( VLM )?</a></li>
<li><a href="https://www.nvidia.com/en-us/glossary/vision-language-models/">What are Vision - Language Models ? | NVIDIA Glossary</a></li>
<li><a href="https://magazine.sebastianraschka.com/p/finetuning-large-language-models">Finetuning Large Language Models</a></li>

</ul>
</details>

**标签**: `#vlm`, `#fine-tuning`, `#browser-automation`, `#computer-vision`, `#local-llm`

---