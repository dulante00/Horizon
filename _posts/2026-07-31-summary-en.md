---
layout: default
title: "Horizon Summary: 2026-07-31 (EN)"
date: 2026-07-31
lang: en
---

> From 59 items, 13 important content pieces were selected

---

1. [Tailscale Details Hugging Face Intrusion via Leaked Auth Key](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash 0731 Intelligence, Performance and Price Analysis](#item-2) ⭐️ 8.0/10
3. [Gemini Robotics ER 2: powering robotics with video understanding, task orchestration, and multi-robot collaboration](#item-3) ⭐️ 8.0/10
4. [Kimi K3 Technical Deep Dive: Three Engineering Innovations Explained](#item-4) ⭐️ 8.0/10
5. [OpenAI Outlines Full-Stack Strategy for Abundant Intelligence](#item-5) ⭐️ 7.0/10
6. [OpenAI Disrupts Cambodia-Based Scam Operation Using ChatGPT](#item-6) ⭐️ 7.0/10
7. [MLVC: A Multi-Platform Learned Video Codec for Cross-NPU Deployment](#item-7) ⭐️ 7.0/10
8. [Elevators](#item-8) ⭐️ 6.0/10
9. [qm](#item-9) ⭐️ 6.0/10
10. [Achieving 25 Gbps Ethernet on Mac Studio via Thunderbolt](#item-10) ⭐️ 6.0/10
11. [SIGGRAPH Time-Test Award: Research Predicts Physical AI a Decade Early](#item-11) ⭐️ 6.0/10
12. [Developer Builds BERT-Style Transformer to Predict Personal Blood Sugar Levels](#item-12) ⭐️ 6.0/10
13. [Assistant Professor Loses PhD Candidates Over Toxic ML Peer Review](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Tailscale Details Hugging Face Intrusion via Leaked Auth Key](https://tailscale.com/blog/hugging-face-intrusion) ⭐️ 8.0/10

Tailscale published a transparent post-mortem explaining how an attacker found a reusable Tailscale auth key inside a Hugging Face environment file and used it over several days to enroll 181 malicious nodes into Hugging Face's tailnet, each granted the access permissions of a CI node. The incident highlights how even a dedicated security tool like Tailscale cannot prevent misuse when customers mishandle secrets, and it sets a new bar for vendor transparency by having Tailscale publicly take responsibility for an intrusion that did not exploit any Tailscale vulnerability. One of 136 leaked credentials was a reusable Tailscale auth key intended for automated CI node provisioning, and the attacker replicated it across multiple external sandboxes. Tailscale emphasizes that no Tailscale code was compromised but pledges to ship detection features, such as improved alerting for unusual node enrollment patterns, to catch similar attacks earlier.

hackernews · bluehatbrit · Jul 31, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49127306)

**Background**: A tailnet is Tailscale's term for the private mesh VPN network built on WireGuard that connects a user's authorized devices and services. Tailscale auth keys allow machines to be automatically enrolled into a tailnet without interactive login; reusable auth keys can be used multiple times to provision many nodes and are intended for CI/CD pipelines, but any leaked reusable key effectively acts as an open enrollment token that grants any machine the access rights its tags specify.

<details><summary>References</summary>
<ul>
<li><a href="https://tailscale.com/docs/concepts/tailnet">What is a tailnet ? · Tailscale Docs</a></li>
<li><a href="https://tailscale.com/docs/features/access-control/auth-keys/how-to/secure-auth-keys">Securely handle an auth key · Tailscale Docs</a></li>
<li><a href="https://selfhosting.sh/apps/tailscale/">How to Set Up Tailscale with Docker | selfhosting.sh</a></li>

</ul>
</details>

**Discussion**: The community largely praised Tailscale's transparency and the 'very Canadian apology' framing, though some commenters, such as ahofmann, argued the post doubles as savvy marketing by showcasing premium security features while implicitly blaming Hugging Face for an avoidable mistake. Practical suggestions emerged too, including Simon Willison's suggestion for alerting on unusual CI node enrollment and bumbledraven's request for a built-in security checkup tool.

**Tags**: `#security`, `#post-mortem`, `#tailscale`, `#devops`, `#incident-response`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash 0731 Intelligence, Performance and Price Analysis](https://artificialanalysis.ai/models/deepseek-v4-flash) ⭐️ 8.0/10

DeepSeek V4 Flash 0731 delivers frontier-level AI intelligence at very low cost, marking a significant new release in the price-performance frontier with viable local deployment options.

hackernews · theanonymousone · Jul 31, 07:59 · [Discussion](https://news.ycombinator.com/item?id=49120299)

**Tags**: `#deepseek`, `#llm`, `#ai-models`, `#price-performance`, `#open-source-ai`

---

<a id="item-3"></a>
## [Gemini Robotics ER 2: powering robotics with video understanding, task orchestration, and multi-robot collaboration](https://deepmind.google/blog/gemini-robotics-er-2-powering-robotics-with-video-understanding-task-orchestration-and-multi-robot-collaboration/) ⭐️ 8.0/10

Google DeepMind announces Gemini Robotics ER 2, a new model that advances robotic capabilities in video understanding, task orchestration, and multi-robot collaboration.

rss · Google DeepMind Blog · Jul 30, 15:00

**Tags**: `#robotics`, `#embodied-ai`, `#google-deepmind`, `#gemini`, `#multi-agent-systems`

---

<a id="item-4"></a>
## [Kimi K3 Technical Deep Dive: Three Engineering Innovations Explained](https://www.reddit.com/r/MachineLearning/comments/1vaysjf/how_kimi_k3_engineered_its_way_to_the_frontier_r/) ⭐️ 8.0/10

Moonshot's Kimi K3 has reached the frontier as an open-weight model, ranked 4th of 580 by Artificial Analysis. A detailed walkthrough of the 47-page technical report reveals three novel engineering contributions: Kimi Delta Attention replacing the KV cache in 69 of 93 layers, Quantile Balancing for 896 experts per layer, and the AgentENV Firecracker microVM infrastructure that created 51 million training sandboxes. Kimi K3 demonstrates that open-weight models can compete at the frontier while introducing architectural innovations that substantially reduce memory and compute costs. These engineering choices address core scaling bottlenecks—long-context memory, MoE load balancing at scale, and agentic RL infrastructure—that the broader AI community has been actively working to solve. Kimi Delta Attention reduces 1M-token context memory from 104.6 GiB to just 27.2 GiB using a single 128x128 matrix per head; Quantile Balancing computes the expert bias directly from one batch's router score margins rather than fixed-step nudging used in DeepSeek-V3; AgentENV achieves 133 ms checkpoint and 49 ms resume times via Firecracker microVMs with overlaybd OCI image loading.

reddit · r/MachineLearning · /u/noninertialframe96 · Jul 30, 16:37

**Background**: Traditional transformer attention scales quadratically with sequence length, and even though the KV (key-value) cache grows only linearly, at million-token scales it becomes a serious memory bottleneck. Mixture-of-Experts (MoE) models scale parameter count by routing each token to a small subset of experts, but require auxiliary load-balancing losses to prevent all tokens from collapsing onto a few popular experts. Agentic reinforcement learning trains models to use tools and execute multi-step plans, requiring massive numbers of isolated execution environments to roll out trajectories safely. Linear attention variants attempt to recover the expressiveness of softmax attention while reducing its compute and memory cost.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2510.26692">Kimi Linear: An Expressive, Efficient Attention Architecture</a></li>
<li><a href="https://www.banandre.com/blog/linear-attentions-revenge-how-kimi-delta-attention-smashes-the-kv-cache-bottleneck">Linear Attention ’s Revenge: How Kimi Delta Attention ... - Banandre</a></li>
<li><a href="https://kvcache.ai/blog/agentenv-open-sourced/">AgentENV: When LLMs Learn to Get the Job Done, We’re Open ...</a></li>

</ul>
</details>

**Tags**: `#Kimi-K3`, `#open-weight-models`, `#Mixture-of-Experts`, `#KV-cache-optimization`, `#frontier-models`

---

<a id="item-5"></a>
## [OpenAI Outlines Full-Stack Strategy for Abundant Intelligence](https://openai.com/index/building-abundant-intelligence) ⭐️ 7.0/10

OpenAI published a blog post titled 'Building abundant intelligence' outlining a full-stack approach to making advanced AI more capable, more affordable, and more widely useful across society. The post ties together OpenAI's work on compute infrastructure, model efficiency, and broad deployment as part of a unified strategic vision. This strategic positioning signals OpenAI's direction on compute infrastructure, model efficiency, and democratization of AI access, extending Sam Altman's earlier vision that AI access may become a fundamental human right. It also provides ideological grounding for the massive capital commitments—$400 billion from OpenAI, Oracle, and SoftBank—needed to build gigawatt-scale AI infrastructure. The 'abundant intelligence' framing serves as the ideological foundation for building gigawatt-scale data centers, securing vast energy supplies, and developing purpose-built AI chips costing hundreds of billions to trillions of dollars. The industry is also shifting from pre-training scaling, which has hit plateaus, toward 'test-time compute' approaches where models analyze problems and pursue multiple solution paths in parallel.

rss · OpenAI Blog · Jul 31, 15:00

**Background**: 'Abundant intelligence' is a concept articulated by OpenAI CEO Sam Altman in September 2025, describing a future in which AI is so widely available and inexpensive that access to it becomes a basic expectation, much like electricity or the internet. The 'full-stack approach' refers to OpenAI's strategy of influencing or controlling every layer of the AI stack—from custom silicon chips and data centers to foundation models and consumer applications—rather than relying solely on third-party infrastructure or off-the-shelf models.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.samaltman.com/abundant-intelligence">Abundant Intelligence - Sam Altman</a></li>
<li><a href="https://note.com/enhack_fumi/n/nce4cd86a97fe">'Abundant Intelligence': Meaning and Context｜Fumi AI</a></li>
<li><a href="https://www.humanityredefined.com/p/the-dream-of-abundant-intelligence">The Dream of Abundant Intelligence - by Conrad Gray</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#AI infrastructure`, `#AI strategy`, `#compute scaling`, `#AI economics`

---

<a id="item-6"></a>
## [OpenAI Disrupts Cambodia-Based Scam Operation Using ChatGPT](https://openai.com/index/disrupting-malicious-uses-of-ai-criminal-scam-operation) ⭐️ 7.0/10

OpenAI disrupted a Cambodia-based criminal scam operation that was leveraging ChatGPT to power investment fraud, romance scams, gambling schemes, and impersonation attacks. The takedown is part of OpenAI's ongoing threat intelligence work to identify and dismantle AI-enabled abuse at scale. This case demonstrates how generative AI tools are being weaponized by criminal enterprises to scale traditional scam playbooks, and highlights the growing role of AI companies as active defenders against misuse. It underscores the urgency of coordinated threat intelligence sharing between AI platforms, law enforcement, and industry partners to counter evolving AI-enabled fraud. The operation combined multiple fraud typologies—investment fraud, romance baiting, gambling, and impersonation—indicating a sophisticated multi-vector approach rather than a single scheme. OpenAI's intervention likely involved banning associated accounts and sharing threat indicators with partners, consistent with its published methodology of detecting policy violations and coordinating with external defenders.

rss · OpenAI Blog · Jul 31, 00:00

**Background**: Generative AI chatbots like ChatGPT can be misused by criminals to automate the most labor-intensive parts of scam operations, such as drafting convincing messages, translating across languages, and maintaining multiple fraudulent personas simultaneously. Romance and investment scams have historically relied on human operators managing dozens of conversations at once; LLMs now enable this social engineering to scale dramatically with fewer people. OpenAI has increasingly published threat reports documenting how malicious actors 'bolt AI onto old playbooks' to move faster, rather than gaining novel offensive capabilities from the models themselves.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/disrupting-malicious-ai-uses/">Disrupting malicious uses of AI | OpenAI</a></li>
<li><a href="https://openai.com/global-affairs/disrupting-malicious-uses-of-ai-october-2025/">Disrupting malicious uses of AI: October 2025 | OpenAI</a></li>
<li><a href="https://www.wired.com/story/ai-scammers-are-better-at-building-trust-than-humans/">AI Scammers Are Better at Building Trust Than Humans | WIRED</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#cybersecurity`, `#fraud prevention`, `#ChatGPT abuse`, `#AI policy`

---

<a id="item-7"></a>
## [MLVC: A Multi-Platform Learned Video Codec for Cross-NPU Deployment](https://www.reddit.com/r/MachineLearning/comments/1vb3xwd/mlvc_multiplatform_learned_video_codec_for/) ⭐️ 7.0/10

MLVC proposes a learned video codec that works across heterogeneous NPUs by explicitly transmitting entropy-model scale parameters through the hyperprior, removing the need for bit-exact neural network execution between encoder and decoder. Neural video codecs have struggled to displace traditional codecs like H.264, H.265, and AV1 in production; MLVC directly targets the cross-platform numerical incompatibility that currently blocks learned codecs from running across Apple, Intel, and other consumer NPUs, and achieves ~100 FPS at 360p/540p on those devices. On the Apple M3 Neural Engine, INT8 operations are simulated via FP16 rather than running on a true INT8 datapath; even hardware with native INT8 support offers no guaranteed control over rounding modes, accumulation types, or scale multiplication, so bit-exact inference is impossible. MLVC sidesteps this by sending the entropy-model scale through the bitstream, so the decoder always sees the exact parameters the encoder used.

reddit · r/MachineLearning · /u/tanelai · Jul 30, 19:40

**Background**: Traditional hand-engineered codecs such as H.264 (AVC), H.265 (HEVC, standardized in 2013), and AV1 still dominate real-world video because they have ubiquitous hardware acceleration and very low power consumption. Learned neural codecs tend to be larger and more power-hungry, but more importantly they rely on entropy models whose probability distributions must match exactly between encoder and decoder; any small numerical drift between the two sides, common when running inference on different NPUs, can break entropy decoding and corrupt the entire bitstream. Today's NPU toolchains (Apple Neural Engine, Intel NPU, etc.) are not standardized enough to guarantee bit-exact fixed-point arithmetic, so simply quantizing the model to INT8 does not reliably fix the problem.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Efficiency_Video_Coding">High Efficiency Video Coding - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2207.05894">Hybrid Spatial-Temporal Entropy Modelling for Neural Video ...</a></li>
<li><a href="https://fireworks.ai/blog/when-faster-not-identical-moe-numerics">Training- Inference Parity in MoE Models: Where Numerics Drift</a></li>

</ul>
</details>

**Discussion**: The original poster disclosed being one of the paper's authors and invited questions; no external community comments were included in the post.

**Tags**: `#video-compression`, `#learned-codecs`, `#neural-networks`, `#edge-deployment`, `#cross-platform`

---

<a id="item-8"></a>
## [Elevators](https://john.fun/elevators) ⭐️ 6.0/10

An interactive web-based elevator simulator demonstrating various scheduling algorithms, sparking quality discussion about connections to disk scheduling, destination dispatch systems, and game design.

hackernews · Jrh0203 · Jul 31, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49124218)

**Tags**: `#algorithms`, `#simulation`, `#elevator-scheduling`, `#interactive-learning`, `#computer-science`

---

<a id="item-9"></a>
## [qm](https://github.com/yc-software/qm) ⭐️ 6.0/10

qm is a YC-backed multiplayer agent harness for work that introduces per-person scopes and shared rooms to address the scoping challenge in enterprise multi-agent environments.

hackernews · tosh · Jul 31, 18:04 · [Discussion](https://news.ycombinator.com/item?id=49126604)

**Tags**: `#AI-agents`, `#multi-agent-systems`, `#developer-tools`, `#YC`, `#enterprise-software`

---

<a id="item-10"></a>
## [Achieving 25 Gbps Ethernet on Mac Studio via Thunderbolt](https://www.jeffgeerling.com/blog/2026/getting-25g-ethernet-mac-thunderbolt/) ⭐️ 6.0/10

Jeff Geerling published a technical exploration of connecting a 25 Gigabit Ethernet adapter to a Mac Studio via Thunderbolt. Testing revealed that the real-world throughput was limited not by the Thunderbolt connection itself, but by the Arm-based NAS (Ampere Altra) on the other end, which could only deliver about 1 GB/s even over its built-in 10 GbE link. This matters for content creators and professionals who need high-throughput local storage and network access on Apple Silicon Macs, which historically offer limited internal PCIe expansion. It highlights that even with the right adapters, end-to-end 25 GbE performance requires attention to every link in the chain, including NAS CPU power and protocol support. Community testing confirmed that the Sonnet Thunderbolt 25 GbE adapter achieves roughly 27 Gbps bidirectionally but supplies only 15W of upstream power, which can be limiting for laptops. A cheaper alternative discussed is putting a standard PCIe NIC into a Thunderbolt eGPU enclosure, though Thunderbolt 3/4 caps at PCIe 3.0 x4 bandwidth.

hackernews · speckx · Jul 31, 16:15 · [Discussion](https://news.ycombinator.com/item?id=49125034)

**Background**: 25 Gigabit Ethernet (25GbE) is a networking standard ratified in 2016 that provides a single-lane 25 Gbit/s alternative to 40G Ethernet, offering better port density for switches. Thunderbolt is a hardware interface developed by Intel and Apple that combines PCIe and DisplayPort over a single cable, with Thunderbolt 3 and 4 providing up to 40 Gbps of total bandwidth. Because Apple Silicon Macs lack internal PCIe slots for NIC upgrades, users must rely on Thunderbolt enclosures or purpose-built adapters to access 25 GbE networking.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/25_Gigabit_Ethernet">25 Gigabit Ethernet - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Thunderbolt_(interface)">Thunderbolt (interface) - Wikipedia</a></li>
<li><a href="https://www.reddit.com/r/eGPU/comments/1aggcq5/egpu_enclosure_for_standard_pcie_cards/">eGPU enclosure for standard PCIe cards? : r/eGPU - Reddit</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed and cautionary. User rconti strongly warned against cheap USB-C RealTek RTL8156 multi-gig dongles after burning through three unreliable units. Neywiny endorsed the more expensive Sonnet adapter for its reliability despite the 15W power limitation. randusername suggested a DIY PCIe NIC in an eGPU enclosure as a $150 alternative. GeekyBear and pzmarzly both pointed to software-side bottlenecks—the NAS CPU and macOS's apparent lack of SMB Direct (RDMA) support—as the likely real-world performance ceiling.

**Tags**: `#networking`, `#mac-studio`, `#thunderbolt`, `#hardware`, `#25gbps-ethernet`

---

<a id="item-11"></a>
## [SIGGRAPH Time-Test Award: Research Predicts Physical AI a Decade Early](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247908730&idx=2&sn=0b3a81693cb5f92800c95b7fc50939f1) ⭐️ 6.0/10

A research paper that won the SIGGRAPH Test-of-Time Award, recognized for its lasting impact on computer graphics over the past decade, is being highlighted for having anticipated today's physical AI developments. The award is part of an annual ACM SIGGRAPH tradition that began in 2023. This recognition highlights how foundational computer graphics research can seed breakthroughs in adjacent fields like robotics simulation, digital twins, and embodied AI. It underscores the growing convergence between computer graphics and physical AI, where rendering, simulation, and physics-based modeling are becoming core building blocks for training intelligent systems in virtual environments. The SIGGRAPH Test-of-Time Award has been given annually since 2023, now in its fourth year as of 2026, honoring papers with at least a decade of lasting impact on computer graphics and interactive techniques. Physical AI, as exemplified by platforms like NVIDIA Omniverse, relies heavily on computer graphics technologies including physics simulation and ray tracing.

rss · 量子位 · Jul 31, 06:32

**Background**: SIGGRAPH is the premier annual conference for computer graphics, organized by ACM since the 1970s, attracting tens of thousands of researchers, artists, and industry professionals at its peak. The Test-of-Time Award specifically recognizes papers published roughly a decade earlier whose influence has only grown over time. Physical AI refers to AI systems embedded in or interacting with the physical world — including robotics, autonomous vehicles, and industrial automation — where simulation environments built on graphics technologies play a critical role in training and validation.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.siggraph.org/2026/05/siggraph-2026-technical-papers-awards-best-papers-honorable-mentions-and-test-of-time.html/">SIGGRAPH 2026 Technical Papers Awards: Best Papers, Honorable Mentions, and Test-of-Time - ACM SIGGRAPH Blog</a></li>
<li><a href="https://blog.siggraph.org/2025/12/a-state-of-the-art-performance-withstanding-the-test-of-time.html/">A State-of-the-Art Performance Withstanding the Test-of-Time - ACM SIGGRAPH Blog</a></li>
<li><a href="https://www.nvidia.com/en-us/omniverse/">Develop Physical AI Applications | NVIDIA Omniverse</a></li>

</ul>
</details>

**Tags**: `#SIGGRAPH`, `#physical AI`, `#computer graphics`, `#research retrospective`, `#RSS aggregation`

---

<a id="item-12"></a>
## [Developer Builds BERT-Style Transformer to Predict Personal Blood Sugar Levels](https://www.reddit.com/r/MachineLearning/comments/1vc1txc/i_have_trained_a_model_to_predict_my_blood_sugar_p/) ⭐️ 6.0/10

A developer released an MIT-licensed project using a BERT-style encoder-only transformer to predict blood glucose 2+ hours ahead, trained across 4 model sizes (up to ~17M parameters) on simulator data and three real Type 1 Diabetes datasets (OhioT1DM, AZT1D, ShanghaiT1DM). The system combines DILATE and pinball losses via Kendall-Gal aggregation, operates in Kovatchev risk space reparameterized to [40, 400], and a personalized variant is currently running on the author's phone. The project showcases thoughtful engineering choices for a safety-critical healthcare forecasting task, demonstrating how transformer architectures originally designed for NLP can be adapted to physiological time-series prediction. Open-source release of code, weights, and evaluation data enables the community to reproduce, benchmark, and extend transformer-based glucose prediction, an area of active interest for closed-loop insulin delivery systems. The model uses bidirectional attention with future blood glucose masked (similar to masked language modeling), accepts announced meals and insulin as conditioning inputs, and predicts time implicitly from context without consuming it as a feature. A known limitation is that the model currently requires announced carbs and insulin to function, whereas an ideal system would also predict in their absence; pretraining on the largest model took ~48 hours while finetuning completed in under 10 minutes.

reddit · r/MachineLearning · /u/0xdeadf1sh · Jul 31, 20:09

**Background**: Blood glucose prediction is a well-studied problem with prior transformer-based approaches, and is particularly important for Type 1 Diabetes (T1D) management where patients must continuously balance insulin dosing against carbohydrate intake. DILATE (NeurIPS 2019) is a loss function designed for non-stationary multi-step time-series forecasting that explicitly penalizes both shape and temporal distortions. The Kovatchev risk space is a nonlinear transformation of glucose values (in mg/dL) that symmetrically emphasizes dangerous hypoglycemia and hyperglycemia by stretching the low range and compressing the high range, originally developed by Boris Kovatchev and colleagues. Kendall-Gal refers to a homoscedastic uncertainty-based method (Kendall, Gal & Cipolla, 2018) for automatically weighting multiple loss functions in multi-task learning by learning task-specific noise parameters.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/1909.09020">Shape and Time Distortion Loss for Training Deep Time Series ... GitHub - vincent-leguen/DILATE: Code for our NeurIPS 2019 ... Shape and Time Distortion Loss for Training Deep Time Series ... Shape and time distortion loss for training deep time series ... NeurIPS Poster Shape and Time Distortion Loss for Training ... Shape and Time Distortion Loss for Training Deep Time Series... Shape and Time Distortion Loss for Training Deep Time Series ...</a></li>
<li><a href="https://github.com/vincent-leguen/DILATE">GitHub - vincent-leguen/DILATE: Code for our NeurIPS 2019 ...</a></li>
<li><a href="https://arxiv.org/abs/1705.07115">[1705.07115] Multi-Task Learning Using Uncertainty to Weigh ... [1703.04977] What Uncertainties Do We Need in Bayesian Deep ... Multi-Task Learning Using Uncertainty to Weigh Losses for ... [1703.04977] What Uncertainties Do We Need in Bayesian Deep ... Investigating Uncertainty Weighting for Multi-Task Learning ... GitHub - ranandalon/mtl: Unofficial implementation of: Multi ... Multi-Task Learning Using Uncertainty to Weigh Losses for ...</a></li>

</ul>
</details>

**Discussion**: The Reddit post to r/MachineLearning presents this as a personal project sharing for community feedback, with the author inviting questions and opinions. The submission received a moderate score of 6.0/10, reflecting appreciation for the technical depth (DILATE/pinball loss combination, Kovatchev risk reparameterization, future masking) while noting that blood glucose prediction with transformer architectures is an established research area rather than a new breakthrough.

**Tags**: `#transformers`, `#time-series-forecasting`, `#healthcare-ML`, `#diabetes`, `#pytorch`

---

<a id="item-13"></a>
## [Assistant Professor Loses PhD Candidates Over Toxic ML Peer Review](https://www.reddit.com/r/MachineLearning/comments/1vawwb8/i_have_lost_three_and_a_half_potential_phd/) ⭐️ 6.0/10

An early-career assistant professor with over 10 years of 'big three' ML conference experience reports losing three-and-a-half potential PhD students who were discouraged by the conference peer review process, even though their papers received positive reviews including one with four unanimous weak accepts. This anecdote highlights how the increasingly contentious ML conference review culture may be actively driving talented researchers away from academia, threatening the long-term pipeline of ML researchers and raising urgent questions about the sustainability of current review practices at venues like NeurIPS, ICML, and ICLR. The professor notes that papers with no obvious flaws get attacked on 'random points' in successive resubmission cycles, creating an endless loop, whereas papers with clear weaknesses can be improved straightforwardly. He emphasizes the work was part of his own ongoing research, not speculative course projects, and that reviews were positive overall but still resulted in rejection.

reddit · r/MachineLearning · /u/AffectionateLife5693 · Jul 30, 15:30

**Background**: The 'big three' ML conferences—NeurIPS, ICML, and ICLR—are the most prestigious venues in machine learning research, and acceptance at these conferences is often critical for academic career advancement, including PhD admissions and faculty hiring. These conferences use OpenReview, a transparent peer review platform that publicly records reviews, rebuttals, and meta-reviews throughout the paper lifecycle. In recent years, submission volumes have surged dramatically, leading to widespread concerns about review randomness, reviewer fatigue, and the increasingly adversarial nature of the review process.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/International_Conference_on_Machine_Learning">International Conference on Machine Learning - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Conference_on_Neural_Information_Processing_Systems">Conference on Neural Information Processing Systems - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/openreview-platform">OpenReview: Transparent Peer Review Platform</a></li>

</ul>
</details>

**Tags**: `#peer-review`, `#ml-conferences`, `#phd-recruitment`, `#research-culture`, `#academic-mentorship`

---