---
layout: default
title: "Horizon Summary: 2026-06-23 (EN)"
date: 2026-06-23
lang: en
---

> From 42 items, 14 important content pieces were selected

---

1. [Valve Launches Steam Machine Gaming PC Today](#item-1) ⭐️ 7.0/10
2. [VibeThinker: 3B param model that beats Opus 4.5 on reasoning with novel SFT+GRPO](#item-2) ⭐️ 7.0/10
3. [Police Chiefs Abused Flock ALPR Systems to Stalk Women](#item-3) ⭐️ 7.0/10
4. [OpenAI Launches Daybreak: AI Security Suite for Vulnerability Discovery and Patching](#item-4) ⭐️ 7.0/10
5. [Samsung Electronics Rolls Out ChatGPT Enterprise and Codex Globally](#item-5) ⭐️ 7.0/10
6. [PaddlePaddle Releases PP-OCRv6 on Hugging Face with 50-Language Support](#item-6) ⭐️ 7.0/10
7. [GLM-5.2 – How to Run Locally](#item-7) ⭐️ 6.0/10
8. [Blog Post Argues for Memcached's Simplicity Over Redis Complexity](#item-8) ⭐️ 6.0/10
9. [Moebius: 0.2B image inpainting model with 10B-level performance](#item-9) ⭐️ 6.0/10
10. [Canada plans 'nuclear renaissance' with up to 10 reactors built by 2040](#item-10) ⭐️ 6.0/10
11. [OpenAI Launches 'Patch the Planet' to Secure Open Source with AI](#item-11) ⭐️ 6.0/10
12. [HuggingFace Reveals Weekly Release Workflow for huggingface_hub](#item-12) ⭐️ 6.0/10
13. [HuggingFace Uses Local Models to Triage OpenClaw PRs for Free](#item-13) ⭐️ 6.0/10
14. [Papers with Code Adds SOTA Badges, Trending Scores, and External Eval Support](#item-14) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Valve Launches Steam Machine Gaming PC Today](https://store.steampowered.com/news/group/45479024/view/685257114654870245) ⭐️ 7.0/10

Valve has launched its new Steam Machine, a living-room gaming PC powered by AMD Zen 4 and RDNA3 hardware, with a starting price of $1,049. The device uses a randomized reservation system for purchases rather than a traditional first-come, first-served launch, with randomization occurring on June 25. This launch represents Valve's renewed push into living-room PC gaming and challenges both traditional consoles and the gaming PC market with a hybrid approach. The transparent pricing rationale, open platform commitment, and anti-bot reservation system signal a deliberate philosophy shift that could pressure competitors to rethink launch practices and hardware openness. The $1,049 starting price is notably higher than Valve's original expectations, driven by rising RAM and storage costs since component sourcing began in 2023. Valve explicitly states buyers can install any operating system or software, and the reservation lottery is designed to combat bots and resellers while acknowledging supply will be limited at launch.

hackernews · theschwa · Jun 22, 17:09 · [Discussion](https://news.ycombinator.com/item?id=48632884)

**Background**: The Steam Machine is Valve's second attempt at a living-room gaming device, following the original Steam Machine initiative from the mid-2010s that struggled to gain traction. Unlike a traditional game console, it runs SteamOS but functions as a full PC with standardized x86 hardware, allowing it to play the entire Steam library at up to 4K resolution. Valve's randomized reservation approach departs from typical hardware launches, where scalper bots often buy out inventory within seconds of availability.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/video-games/console-gaming/valve-steam-machine-review">Valve Steam Machine review: Couch gaming unboxed, but not ...</a></li>
<li><a href="https://www.pchardwarepro.com/en/Full-analysis-of-Valve's-new-Steam-Machine/">Steam Machine: Technical Specifications and Details from Valve</a></li>
<li><a href="https://en.as.com/meristation/news/steam-machine-pricing-explained-why-valves-console-style-pc-costs-over-1000-f202606-n/">Steam Machine pricing explained: Why Valve’s console-style PC ...</a></li>

</ul>
</details>

**Discussion**: Community reaction has been largely positive, with particular praise for Valve's randomized reservation system as a fairer alternative to bot-dominated launches. Many commenters highlighted the open platform philosophy—allowing any OS or software installation—as a refreshing and surprisingly uncommon stance in modern hardware. A few users pointed out the unusually authentic gameplay footage in Valve's marketing, and some simply expressed intent to purchase the device.

**Tags**: `#Steam Machine`, `#Valve`, `#gaming hardware`, `#PC gaming`, `#product launch`

---

<a id="item-2"></a>
## [VibeThinker: 3B param model that beats Opus 4.5 on reasoning with novel SFT+GRPO](https://arxiv.org/abs/2606.16140) ⭐️ 7.0/10

A 3B parameter model (VibeThinker) trained with SFT+GRPO reportedly outperforms Opus 4.5 on reasoning benchmarks, suggesting efficient small models can achieve strong reasoning capabilities.

hackernews · timhigins · Jun 23, 02:01 · [Discussion](https://news.ycombinator.com/item?id=48639240)

**Tags**: `#small-language-models`, `#reasoning`, `#SFT`, `#GRPO`, `#model-efficiency`

---

<a id="item-3"></a>
## [Police Chiefs Abused Flock ALPR Systems to Stalk Women](https://ipvm.com/reports/police-chiefs-track) ⭐️ 7.0/10

An IPVM investigation has revealed that multiple police chiefs used Flock Safety's automatic license plate reader (ALPR) systems to track and stalk women, exploiting law enforcement surveillance tools for personal purposes. The findings highlight critical gaps in oversight and fuel urgent calls for warrant requirements before accessing such surveillance data. This case demonstrates the dual-use nature of surveillance technology: the same tools that help solve crimes can be weaponized by those entrusted to use them, underscoring the urgent need for judicial oversight, warrant requirements, and active auditing of police access to tracking databases. It has implications for every community using ALPR systems, raising fundamental questions about accountability and the balance between public safety and civil liberties. Flock Safety's products include the Falcon and Sparrow cameras, which use optical character recognition to automatically capture and read vehicle license plates, storing data that can be searched retroactively. The abuse uncovered by IPVM reportedly involved senior law enforcement officials exploiting query access to ALPR databases without judicial authorization or documented law enforcement justification, illustrating how administrative access to surveillance data can enable abuse even without warrant requirements.

hackernews · jhonovich · Jun 22, 19:13 · [Discussion](https://news.ycombinator.com/item?id=48634694)

**Background**: Automatic License Plate Readers (ALPRs) are camera systems that use optical character recognition to automatically capture, log, and search vehicle license plates. Companies like Flock Safety have deployed these systems widely across U.S. cities, marketed to law enforcement for tracking stolen vehicles, solving crimes, and providing court-admissible evidence. Because ALPR data is stored in searchable databases, any user with query access can look up the location history of any vehicle, making the systems powerful but vulnerable to abuse. Unlike body cameras, whose footage is often subject to retention and review policies, ALPR database queries typically lack comparable audit trails, making misuse harder to detect.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://www.cnet.com/home/security/when-flock-comes-to-town-why-cities-are-axing-the-controversial-surveillance-technology/">When Flock Surveillance Comes to Your Town: Everything ... - CNET</a></li>
<li><a href="https://vehicledatabases.com/articles/how-do-license-plate-reader-works">How Do Automatic License Plate Readers (ALPR) Work?</a></li>

</ul>
</details>

**Discussion**: Commenters broadly agreed that warrants and active monitoring of surveillance technology are essential, drawing parallels to body camera audit practices. Several users emphasized the universal risk of abuse when monitoring is absent, referencing Scott Adams' maxim about fraud. Others warned individuals about the personal safety risks of dating law enforcement personnel, given their access to tracking systems, and noted that such abuse is not unique to this case—a Swedish case was cited where a cop used public CCTV access to check a meeting point before meeting a decoy. The overall sentiment strongly favored implementing checks, balances, and transparency for ALPR systems.

**Tags**: `#surveillance`, `#privacy`, `#law-enforcement`, `#civil-liberties`, `#technology-ethics`

---

<a id="item-4"></a>
## [OpenAI Launches Daybreak: AI Security Suite for Vulnerability Discovery and Patching](https://openai.com/index/daybreak-securing-the-world) ⭐️ 7.0/10

OpenAI has launched Daybreak, a suite of AI security tools comprising Codex Security and GPT-5.5-Cyber, designed to help organizations find, validate, and patch vulnerabilities at scale across enterprise and open-source codebases. This move marks OpenAI's most significant expansion into autonomous cybersecurity, offering an end-to-end pipeline from vulnerability detection to patch generation that could reshape how defenders respond to threats at machine speed. Codex Security scans connected repositories commit by commit, builds contextual awareness of the codebase, and validates high-signal findings in an isolated environment before surfacing them; GPT-5.5-Cyber is a specialized model tuned for advanced vulnerability detection, patch synthesis, and automated remediation.

rss · OpenAI Blog · Jun 22, 10:00

**Background**: Application security has traditionally relied on static and dynamic analysis tools plus human review, often producing large volumes of low-confidence alerts that require manual triage. Agentic AI systems—AI agents that can autonomously reason through multi-step tasks—offer the possibility of not just flagging potential bugs but validating them and proposing or applying fixes. OpenAI previously entered this space with Codex Security in research preview in early 2026 and expanded Trusted Access for Cyber with GPT-5.5 and GPT-5.5-Cyber in May 2026; Daybreak now packages these capabilities into a unified product aimed at defending organizations and critical infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://openai.com/index/codex-security-now-in-research-preview/">Codex Security: now in research preview - OpenAI</a></li>
<li><a href="https://cybersecuritynews.com/gpt-5-5-cyber/">OpenAI Releases GPT‑5.5‑Cyber With Full Automation for ...</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#cybersecurity`, `#vulnerability-management`, `#Codex`, `#AI-security`

---

<a id="item-5"></a>
## [Samsung Electronics Rolls Out ChatGPT Enterprise and Codex Globally](https://openai.com/index/samsung-electronics-chatgpt-codex-deployment) ⭐️ 7.0/10

Samsung Electronics is deploying ChatGPT Enterprise and OpenAI's Codex coding agent to its employees worldwide, marking one of OpenAI's largest enterprise AI rollouts to date. This deployment signals deepening enterprise confidence in generative AI for both productivity and software engineering at one of the world's largest technology manufacturers, potentially setting a benchmark for large-scale AI adoption across global corporations. ChatGPT Enterprise provides enterprise-grade privacy, security, and centralized admin controls, while Codex is an AI coding agent powered by codex-1 (an o3 reasoning model variant) that can write features, answer codebase questions, fix bugs, and propose code changes for human review.

rss · OpenAI Blog · Jun 21, 23:00

**Background**: ChatGPT Enterprise is OpenAI's managed plan for organizations, offering unlimited higher-speed GPT-4 access, longer context windows, advanced data analysis, and customization options beyond the consumer version. Codex, originally introduced in 2021 as a natural-language-to-code model, has been relaunched as an AI coding agent capable of autonomous software engineering tasks. Samsung Electronics, a major global technology conglomerate, is among the largest single organizations to commit to deploying these tools across its entire workforce.

<details><summary>References</summary>
<ul>
<li><a href="https://help.openai.com/en/articles/8265053">What is ChatGPT Enterprise? | OpenAI Help Center</a></li>
<li><a href="https://openai.com/index/introducing-chatgpt-enterprise/">Introducing ChatGPT Enterprise - OpenAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Codex_(AI_agent)">Codex (AI agent) - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#enterprise-ai`, `#openai`, `#chatgpt`, `#codex`, `#samsung`

---

<a id="item-6"></a>
## [PaddlePaddle Releases PP-OCRv6 on Hugging Face with 50-Language Support](https://huggingface.co/blog/PaddlePaddle/pp-ocrv6) ⭐️ 7.0/10

PaddlePaddle has released PP-OCRv6, the latest generation of its PP-OCR universal text recognition system, now available on Hugging Face. The new version supports 50 languages and offers parameter-efficient models ranging from 1.5M to 34.5M parameters, built on the newly designed PPLCNetV4 unified backbone across tiny, small, and medium tiers. PP-OCRv6 achieves a +4.6% improvement in detection accuracy and +5.1% in recognition accuracy over its predecessor PP-OCRv5, reportedly surpassing mainstream billion-scale Vision-Language Models on OCR tasks. This makes production-grade multilingual OCR more accessible for edge devices, mobile apps, and server deployments without requiring massive compute resources. The model family uses a tiered deployment strategy: tiny (1.5M params) targets edge/IoT, small targets mobile/desktop, and medium (34.5M params) targets server scenarios. The system is part of the broader PaddleOCR toolkit, which bridges images/PDFs to LLMs and supports over 100 languages across its full suite of tools.

rss · HuggingFace Blog · Jun 22, 13:18

**Background**: OCR (Optical Character Recognition) converts text in images into machine-readable characters, forming a critical pipeline for document digitization, accessibility, and AI data ingestion. PaddleOCR is an open-source OCR toolkit developed by Baidu under the PaddlePaddle deep learning framework, widely used in both academic and industrial settings. Vision-Language Models (VLMs) have recently demonstrated strong OCR capabilities but typically require billions of parameters and significant compute, making lightweight dedicated OCR systems like PP-OCRv6 valuable for resource-constrained deployments.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/collections/PaddlePaddle/pp-ocrv6">PP-OCRv6 - a PaddlePaddle Collection</a></li>
<li><a href="https://www.paddleocr.ai/latest/en/version3.x/algorithm/PP-OCRv6/PP-OCRv6.html">PP-OCRv6 Introduction - PaddleOCR Documentation</a></li>

</ul>
</details>

**Tags**: `#OCR`, `#PaddlePaddle`, `#multilingual`, `#HuggingFace`, `#computer-vision`

---

<a id="item-7"></a>
## [GLM-5.2 – How to Run Locally](https://unsloth.ai/docs/models/glm-5.2) ⭐️ 6.0/10

Guide on running the GLM-5.2 large language model locally, with community discussion revealing the significant hardware requirements (512GB+ RAM, multiple high-end GPUs) and cost considerations for running MoE models at home.

hackernews · TechTechTech · Jun 22, 21:21 · [Discussion](https://news.ycombinator.com/item?id=48636377)

**Tags**: `#local-llm`, `#glm-5.2`, `#moe-models`, `#hardware-requirements`, `#self-hosting`

---

<a id="item-8"></a>
## [Blog Post Argues for Memcached's Simplicity Over Redis Complexity](https://jchri.st/blog/in-praise-of-memcached/) ⭐️ 6.0/10

A blog post by Christian Christensen argues that memcached's deliberately minimal feature set makes it more reliable in production than Redis or Valkey, which have accumulated features over time that can lead to unexpected failure modes. The post sparked substantive community discussion about real-world production experiences with both systems. 这场讨论揭示了基础设施软件中一个根本性的设计哲学矛盾：功能丰富性与运行可预测性之间的取舍。运行大规模系统的工程师可以从这一提醒中获益——范围更窄的简单工具往往故障模式更少，而 Redis 这类流行系统的复杂性在生产环境中可能成为负担。 Memcached guarantees O(1) time complexity for all operations by design, meaning no operation can stall the entire system, while Redis's single-threaded core can block on arbitrarily complex commands. Real production incidents reported include Valkey running out of memory with no eviction policy, AOF write failures filling the disk, and applications lacking fallback paths when Redis becomes unavailable.

hackernews · j03b · Jun 23, 01:15 · [Discussion](https://news.ycombinator.com/item?id=48638886)

**Background**: Memcached and Redis are both in-memory key-value stores widely used as caching layers to speed up web applications. Memcached was designed in 2003 as a simple, distributed memory cache with a deliberately limited API. Redis, introduced in 2009, started as a simple cache but evolved into a versatile data structure server supporting sorted sets, hashes, pub/sub, Lua scripting, persistence (RDB snapshots and AOF logs), and transactions. Valkey is a Linux Foundation-governed fork of Redis created after Redis changed its license. The debate over simplicity versus feature richness is a recurring theme in infrastructure software design.

**Discussion**: Community commenters largely validated the author's thesis with first-hand production war stories: multiple users reported Redis/Valkey outages caused by AOF disk exhaustion and unbounded memory growth, and praised memcached's O(1) guarantee as a deliberate design choice that prevents stalls. One commenter noted that open-source projects inevitably accumulate features over time, and that Redis's persistence layer (AOF) is often misunderstood—most users treat Redis as a simple cache but enable AOF by default, inheriting complexity they don't need. A contrarian view pointed out that Redis issues are often exacerbated by misconfiguration and granting excessive access rather than being inherent flaws of the software itself.

**Tags**: `#memcached`, `#redis`, `#caching`, `#system-design`, `#infrastructure`

---

<a id="item-9"></a>
## [Moebius: 0.2B image inpainting model with 10B-level performance](https://hustvl.github.io/Moebius/) ⭐️ 6.0/10

Moebius is a 0.2B parameter image inpainting model small enough to run in the browser, though community testing reveals notable quality and resolution limitations compared to its performance claims.

hackernews · DSemba · Jun 22, 13:53 · [Discussion](https://news.ycombinator.com/item?id=48630171)

**Tags**: `#image-inpainting`, `#small-models`, `#computer-vision`, `#browser-ml`, `#onnx`

---

<a id="item-10"></a>
## [Canada plans 'nuclear renaissance' with up to 10 reactors built by 2040](https://www.cbc.ca/news/politics/federal-nuclear-strategy-9.7244509) ⭐️ 6.0/10

Canada announces plans to build up to 10 nuclear reactors by 2040 as part of a nuclear energy strategy, leveraging its uranium reserves and CANDU reactor expertise.

hackernews · geox · Jun 22, 19:06 · [Discussion](https://news.ycombinator.com/item?id=48634585)

**Tags**: `#nuclear-energy`, `#energy-policy`, `#infrastructure`, `#canada`, `#climate`

---

<a id="item-11"></a>
## [OpenAI Launches 'Patch the Planet' to Secure Open Source with AI](https://openai.com/index/patch-the-planet) ⭐️ 6.0/10

OpenAI 推出了「Patch the Planet」计划，这是其 Daybreak 安全项目下的新举措，旨在通过 AI 辅助分析结合人类专家审查，帮助开源维护者发现、验证并修复安全漏洞。 Open-source software underpins much of the modern digital infrastructure, yet most projects are maintained by small teams with limited resources to address growing security threats. By applying frontier AI models like GPT-5.5-Cyber and Codex Security at scale, this initiative could meaningfully narrow the gap between vulnerability discovery and patching—an urgent need as AI-assisted attackers reduce the effective time-to-exploitation to near zero days. The initiative is part of the broader Daybreak security suite, which also includes Codex Security—an application security agent capable of autonomously identifying and remediating complex vulnerabilities—and GPT-5.5-Cyber, a specialized model released to trusted defenders. The 'Patch the Planet' program specifically targets the maintainer experience by combining automated detection with human expert validation to reduce false positives and ensure high-quality patches.

rss · OpenAI Blog · Jun 22, 10:00

**Background**: Daybreak is OpenAI's umbrella cybersecurity initiative that combines frontier AI models, automated security agents, and ecosystem partnerships to help defenders keep pace with an evolving threat landscape. Codex Security, announced earlier in 2026, is an AI agent built to autonomously discover, validate, and remediate vulnerabilities in both enterprise and open-source codebases. GPT-5.5-Cyber is a specialized variant of OpenAI's flagship model fine-tuned for cybersecurity tasks. The urgency of such tools is underscored by reports from projects like FreeBSD, which have begun receiving vulnerability reports attributable to AI-enabled offensive security tools, signaling that defensive AI must keep pace with offensive AI.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/daybreak/">Daybreak | OpenAI for cybersecurity</a></li>
<li><a href="https://thehackernews.com/2026/06/openai-expands-daybreak-with-gpt-55.html">OpenAI Expands Daybreak With GPT-5.5-Cyber to Help Defenders ...</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#security`, `#openai`, `#vulnerability-management`, `#ai-applications`

---

<a id="item-12"></a>
## [HuggingFace Reveals Weekly Release Workflow for huggingface_hub](https://huggingface.co/blog/huggingface-hub-release-ci) ⭐️ 6.0/10

HuggingFace published an engineering blog detailing how the team ships a new release of the huggingface_hub Python library every week, using a combination of AI-assisted development, open tools, and a human-in-the-loop review process. This workflow offers a concrete, real-world example of how a major ML platform balances rapid release velocity with quality control in the AI era, making it valuable for MLOps and DevOps practitioners looking to modernize their own continuous delivery pipelines. The blog emphasizes a weekly cadence and the deliberate use of AI tooling augmented by human oversight, rather than full automation, to ship reliable updates to one of the most widely used ML client libraries.

rss · HuggingFace Blog · Jun 23, 00:00

**Background**: The huggingface_hub library is the official Python client for the Hugging Face Hub, a platform for sharing pre-trained models, datasets, and machine learning applications. Release engineering is the discipline of building, testing, and delivering software releases in a consistent and repeatable way, and it is a core concern for large platforms like Google's SRE teams. Human-in-the-loop (HITL) workflows combine AI speed with human judgment through checkpoints such as approvals and verification steps, helping teams move quickly without sacrificing safety or quality.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/docs/huggingface_hub/index">Hub client library - Hugging Face</a></li>
<li><a href="https://github.com/huggingface/huggingface_hub">GitHub - huggingface/huggingface_hub: The official Python ...</a></li>
<li><a href="https://sre.google/sre-book/release-engineering/">Google SRE: Role of Release Engineer and Best Practices</a></li>

</ul>
</details>

**Tags**: `#huggingface`, `#release-engineering`, `#ci-cd`, `#mlops`, `#developer-workflow`

---

<a id="item-13"></a>
## [HuggingFace Uses Local Models to Triage OpenClaw PRs for Free](https://huggingface.co/blog/local-models-pr-triage) ⭐️ 6.0/10

HuggingFace published a blog post demonstrating how to use local language models to automatically triage pull requests on the OpenClaw GitHub repository, showcasing a no-cost automated workflow for open-source maintainers. This matters because it provides open-source maintainers with a practical, cost-free alternative to paid API-based solutions for automating PR triage, potentially reducing the burden of code review and lowering the barrier for smaller projects to adopt AI-assisted workflows. The 'FREE*' caveat likely refers to hidden costs such as local hardware requirements, electricity consumption, and the engineering effort needed to set up and maintain the local inference pipeline. The workflow leverages self-hosted LLMs rather than cloud-based APIs like OpenAI or Anthropic.

rss · HuggingFace Blog · Jun 22, 00:00

**Background**: Local LLMs are language models that are downloaded and run on a user's own machine or on-premise infrastructure, rather than being accessed via remote cloud APIs. This approach offers greater privacy, control, and potentially lower long-term costs, though it requires sufficient hardware. OpenClaw is a free, open-source autonomous AI agent that executes tasks via LLMs and interacts with users through messaging platforms. PR triage is the process of reviewing, categorizing, and prioritizing incoming pull requests in a repository, which is a time-consuming task for open-source maintainers managing large volumes of contributions.

<details><summary>References</summary>
<ul>
<li><a href="https://mljourney.com/cloud-based-vs-local-llms-which-is-right-for-you/">Cloud-Based vs Local LLMs: Which Is Right for You?</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenClaw">OpenClaw - Wikipedia</a></li>
<li><a href="https://github.com/openclaw/openclaw">OpenClaw — Personal AI Assistant - GitHub</a></li>

</ul>
</details>

**Tags**: `#local-models`, `#llm`, `#github`, `#developer-tools`, `#open-source`

---

<a id="item-14"></a>
## [Papers with Code Adds SOTA Badges, Trending Scores, and External Eval Support](https://www.reddit.com/r/MachineLearning/comments/1ucm508/some_new_updates_to_papers_with_code_p/) ⭐️ 6.0/10

Hugging Face's open-source team has rolled out several new features to the revived Papers with Code platform, including SOTA (state-of-the-art) badges displayed on papers when they rank in the top 3 of a benchmark, a new trending score that combines GitHub star velocity with Hugging Face artifact trending, support for third-party 'external' evals, additional benchmarks such as ImageNet-10%, 3D semantic segmentation, and object counting, and a new alternate domain at paperswithco.de. Papers with Code is a critical research discovery and reproducibility resource for the ML community, bridging the gap between academic papers and their code implementations. The continued revival and feature expansion by Hugging Face ensures researchers can more easily track SOTA results, discover trending work, and assess model performance through community-driven evaluations. The new trending score now factors in the trending signals of linked Hugging Face models, datasets, and Spaces alongside GitHub star velocity, allowing papers like IndexCache (a core technique behind GLM-5.2) to surface. External eval support is a new capability beyond the legacy Papers with Code site, enabling third-party benchmarks like FrontierSWE, PostTrainBench, and Artificial Analysis results to be displayed alongside a paper's own reported numbers.

reddit · r/MachineLearning · /u/NielsRogge · Jun 22, 14:29

**Background**: Papers with Code was originally launched in 2018 as a community-driven platform linking ML research papers to their open-source code implementations, benchmarks, and leaderboards. It was acquired by Facebook AI Research in 2019 but was eventually shut down in 2023. Hugging Face subsequently relaunched the platform at paperswithcode.co, aiming to restore and expand this essential research infrastructure. SOTA badges visually highlight papers that achieve top-ranked results on standard benchmarks, helping researchers quickly identify the best-performing methods in a given area.

<details><summary>References</summary>
<ul>
<li><a href="https://paperswithcode.co/">Papers with Code</a></li>
<li><a href="https://posttrainbench.com/">PostTrainBench</a></li>

</ul>
</details>

**Discussion**: The post is a promotional announcement directly from Niels Rogge of Hugging Face's open-source team, who actively invites community feedback, bug reports, feature requests, and contributions. No external community comments are included in the provided content.

**Tags**: `#papers-with-code`, `#hugging-face`, `#machine-learning`, `#research-tools`, `#open-source`

---