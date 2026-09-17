---
layout: default
title: "Horizon Summary: 2026-09-17 (EN)"
date: 2026-09-17
lang: en
---

> From 56 items, 16 important content pieces were selected

---

1. [How GLM built its own inference infrastructure](#item-1) ⭐️ 8.0/10
2. [Why I didn’t sign the Fields medallists’ letter](#item-2) ⭐️ 8.0/10
3. [Bonsai 2 27B: Near-Lossless Compression in a 9x Smaller Footprint](#item-3) ⭐️ 7.0/10
4. [Hister: A private search engine for the pages you visit and the files you keep](#item-4) ⭐️ 7.0/10
5. [CrowdSec Source Code Leaked via Compromised TanStack Dependency](#item-5) ⭐️ 7.0/10
6. [One Year of Sponsored Servo Browser Engine Development](#item-6) ⭐️ 7.0/10
7. [OpenAI Publishes Framework for Reporting Model Misalignment](#item-7) ⭐️ 7.0/10
8. [Huawei says AI chip demand exceeds supply amid Nvidia challenge](#item-8) ⭐️ 7.0/10
9. [Astra for Law](#item-9) ⭐️ 6.0/10
10. [Bend – A language that blocks AI mistakes via proof, on CPU and GPU](#item-10) ⭐️ 6.0/10
11. [GitLab.com Tightens Rate Limits, Sparking Debate on AI Scraping and API Design](#item-11) ⭐️ 6.0/10
12. [OpenAI launches Sponsored Agents advertising in ChatGPT](#item-12) ⭐️ 6.0/10
13. [How workers are unlocking new ways of working](#item-13) ⭐️ 6.0/10
14. [Doubled inference speed on single AMD R9700 with Qwen3 27B NVFP4](#item-14) ⭐️ 6.0/10
15. [IFM Releases K2-Horizon-7B: Diffusion Adapter Boosts LLM to 5200 TPS](#item-15) ⭐️ 6.0/10
16. [First Leaked M5 Ultra Benchmarks Show 50 tok/s on Qwen 27B Q4](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [How GLM built its own inference infrastructure](https://z.ai/blog/glm-built-its-inference-infrastructure) ⭐️ 8.0/10

GLM details building a massive production inference system on over 100,000 Chinese-made AI accelerators, showcasing aggressive memory optimizations and demonstrating China's growing AI infrastructure independence.

hackernews · whiteros_e · Sep 17, 08:27 · [Discussion](https://news.ycombinator.com/item?id=49737922)

**Tags**: `#AI infrastructure`, `#inference systems`, `#Chinese AI`, `#chip manufacturing`, `#LLM operations`

---

<a id="item-2"></a>
## [Why I didn’t sign the Fields medallists’ letter](https://gowers.wordpress.com/2026/09/17/why-i-didnt-sign-the-fields-medallists-letter/) ⭐️ 8.0/10

Fields medalist Tim Gowers explains his reasoning for not signing an open letter by fellow Fields medalists about AI's impact on mathematics, sparking rich discussion about AI's threat to academic career pipelines and the value of human expertise.

hackernews · simianwords · Sep 17, 08:51 · [Discussion](https://news.ycombinator.com/item?id=49738091)

**Tags**: `#AI`, `#mathematics`, `#academia`, `#labor-displacement`, `#career-pipelines`

---

<a id="item-3"></a>
## [Bonsai 2 27B: Near-Lossless Compression in a 9x Smaller Footprint](https://prismml.com/news/bonsai-2-27b) ⭐️ 7.0/10

Prism ML's Bonsai 2 27B achieves 9x model compression using ternary weights with FP16 scaling, though discussion questions how the compression compares to existing quantization methods.

hackernews · JonSchneider · Sep 17, 21:13 · [Discussion](https://news.ycombinator.com/item?id=49746618)

**Tags**: `#model-compression`, `#quantization`, `#ternary-weights`, `#llm-optimization`, `#inference`

---

<a id="item-4"></a>
## [Hister: A private search engine for the pages you visit and the files you keep](https://github.com/asciimoo/hister) ⭐️ 7.0/10

Hister is a privacy-respecting personal search engine that indexes visited pages, bookmarks, browser history, and local files with offline previews, created by the author of Searx.

hackernews · bookofjoe · Sep 17, 16:25 · [Discussion](https://news.ycombinator.com/item?id=49743097)

**Tags**: `#privacy`, `#search-engine`, `#open-source`, `#knowledge-management`, `#personal-tools`

---

<a id="item-5"></a>
## [CrowdSec Source Code Leaked via Compromised TanStack Dependency](https://www.crowdsec.net/blog/crowdsec-statement-source-code-exposure) ⭐️ 7.0/10

CrowdSec disclosed that its private source code was exposed after a compromised TanStack npm dependency exfiltrated an API key with read access to its codebase. The company immediately rotated all required tokens and credentials to contain the incident. The incident is ironic given that CrowdSec sells crowdsourced threat intelligence, yet was itself compromised through a third-party supply chain weakness. It underscores how no organization—even security vendors—is safe from the cascading risk of compromised dependencies, and it raises questions about whether credential rotation alone is an adequate response. The attack vector traces to the TanStack npm supply-chain compromise (the 'Mini Shai-Hulud' worm) that chained a pull_request_target exploit, GitHub Actions cache poisoning, and OIDC token extraction to publish 84 malicious versions across 42 @tanstack/* packages. CrowdSec's remediation was limited to API key rotation, which does not address the root cause of poisoned upstream dependencies.

hackernews · eccgecko · Sep 17, 15:34 · [Discussion](https://news.ycombinator.com/item?id=49742355)

**Background**: CrowdSec is an open-source security engine that analyzes logs and HTTP requests to detect and block malicious IPs using crowdsourced threat intelligence; users share signals and benefit from a shared blocklist. The TanStack compromise is part of a broader wave of self-propagating supply-chain attacks targeting the npm and PyPI ecosystems, where malicious packages hijack CI/CD pipelines to steal developer secrets like API keys and OIDC tokens. These stolen credentials can then be used to access private repositories, cloud accounts, or publishing infrastructure, turning a single compromised package into a widespread breach vector.

<details><summary>References</summary>
<ul>
<li><a href="https://tanstack.com/blog/npm-supply-chain-compromise-postmortem">Postmortem: TanStack npm supply-chain compromise | TanStack Blog</a></li>
<li><a href="https://www.stepsecurity.io/blog/mini-shai-hulud-is-back-a-self-spreading-supply-chain-attack-hits-the-npm-ecosystem">TeamPCP's Mini Shai-Hulud Is Back: A Self-Spreading Supply Chain Attack Compromises TanStack npm Packages - StepSecurity</a></li>
<li><a href="https://github.com/crowdsecurity/crowdsec">GitHub - crowdsecurity/crowdsec: CrowdSec - the open-source and participative security solution offering crowdsourced protection against malicious IPs and access to the most advanced real-world CTI. · GitHub</a></li>

</ul>
</details>

**Discussion**: Commenters highlighted the irony of a security company being breached, with several questioning whether CrowdSec is truly a security firm or merely an aggregator of bad IP data that would be better run as a non-profit. Multiple users criticized the credential-rotation remediation as insufficient since future supply-chain attacks would simply steal the new keys, and suggested stronger measures such as hardware security keys (YubiKey) and SSL certificates for Git access. Others shared practical deployment experiences, including frustration with false positives and being cut off from community blocklists on older Debian packages.

**Tags**: `#security`, `#supply-chain-attack`, `#crowdsec`, `#incident-response`, `#open-source-security`

---

<a id="item-6"></a>
## [One Year of Sponsored Servo Browser Engine Development](https://servo.org/blog/2026/09/15/one-year-of-sponsorship/) ⭐️ 7.0/10

The Servo browser engine project has published a retrospective marking one year of sponsored development, highlighting progress made since it transitioned from a Mozilla research project to an independent, community-supported effort. Servo represents one of the very few viable alternatives to the Chromium-dominated web ecosystem, making its continued development strategically important for browser engine diversity and web infrastructure independence. The project relies on sponsorship from organizations such as NLnet and is built in Rust, leveraging the language's memory safety guarantees and concurrency features to create a highly parallel rendering architecture with fine-grained, isolated tasks for layout, parsing, and image decoding.

hackernews · AshleysBrain · Sep 17, 08:13 · [Discussion](https://news.ycombinator.com/item?id=49737849)

**Background**: Servo is an experimental browser engine originally created at Mozilla Corporation as a research project to explore using the Rust programming language for browser development. After Mozilla reduced its involvement, Servo became an independent open-source effort aiming to build a fast, secure, and parallel browser engine. The web platform today is heavily dominated by Google's Chromium engine (used by Chrome, Edge, and many others), with Apple's WebKit and Mozilla's Gecko as the only other widely deployed engines, making projects like Servo and Ladybird important for maintaining diversity and competition in browser infrastructure.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Servo_(software)">Servo (software) - Wikipedia</a></li>
<li><a href="https://www.mozillafoundation.org/en/research/library/engineering-the-servo-web-browser-engine-using-rust/">Engineering the Servo Web Browser Engine using Rust - Mozilla Foundation</a></li>

</ul>
</details>

**Discussion**: Community sentiment is generally supportive of Servo's progress as a meaningful alternative to both Chromium and the similarly Rust-based Ladybird browser. Commenters highlighted NLnet as a key sponsor, expressed hope that major device manufacturers like Huawei or Samsung would adopt Servo in their products, and raised concerns about the sustainability and cost-efficiency of the project's funding model.

**Tags**: `#servo`, `#browser-engine`, `#web-infrastructure`, `#open-source-funding`, `#rust`

---

<a id="item-7"></a>
## [OpenAI Publishes Framework for Reporting Model Misalignment](https://openai.com/index/model-misalignment-reporting-framework) ⭐️ 7.0/10

OpenAI has published a formal framework for tracking, investigating, and disclosing instances of model misalignment, accompanied by six specific reports of unexpected or concerning model behavior. As one of the leading AI labs, OpenAI's move toward systematic transparency about model misalignment sets an important precedent for industry accountability and could influence how other organizations disclose AI safety issues. The framework is hosted on OpenAI's dedicated Alignment site (alignment.openai.com/misalignment-reports), which provides public disclosure principles for how misalignment arises, what it looks like, and where safeguards succeed or fail.

rss · OpenAI Blog · Sep 16, 17:00

**Background**: 模型失准指的是 AI 模型的行为偏离其预期目的或人类价值观——这是 AI 对齐领域的核心挑战。虽然 RLHF（基于人类反馈的强化学习）等技术旨在在训练过程中对齐模型，但对齐问题并未被完全解决：更聪明的模型未必更加对齐，仅靠安全过滤也无法保证正确的对齐。随着前沿模型的能力不断增强，AI 安全社区越来越呼吁各实验室透明地记录和报告失准案例，以建立对风险的集体理解。

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/model-misalignment-reporting-framework/">Our framework for reporting model misalignment - OpenAI</a></li>
<li><a href="https://alignment.openai.com/misalignment-reports/">Misalignment Notices and Reports · OpenAI Alignment</a></li>
<li><a href="https://research.ibm.com/blog/what-is-alignment-ai">What is AI alignment ? - IBM Research</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#model alignment`, `#OpenAI`, `#responsible AI`, `#transparency`

---

<a id="item-8"></a>
## [Huawei says AI chip demand exceeds supply amid Nvidia challenge](https://www.reddit.com/r/LocalLLaMA/comments/1wirvb0/chinas_huawei_says_ai_chip_demand_outstrips/) ⭐️ 7.0/10

Huawei has reported that demand for its AI chips is outstripping supply as it intensifies its challenge to Nvidia, particularly within the Chinese market where U.S. export restrictions have limited access to advanced GPUs. This signals Huawei's growing role in China's domestic AI infrastructure at a time when U.S. export controls are reshaping the global semiconductor landscape. It underscores how Chinese cloud providers and AI companies are increasingly turning to homegrown alternatives like Huawei's Ascend lineup, potentially eroding Nvidia's dominance in one of its largest markets. Huawei's Ascend lineup includes the 910b and 910c models, with the upcoming 910D reportedly designed to surpass Nvidia's H100 in performance. Huawei has also broadened its portfolio with 11 chips spanning AI processing, general-purpose computing, storage, and high-speed connectivity, aiming to supply entire AI data center stacks rather than individual accelerators.

reddit · r/LocalLLaMA · /u/sunychoudhary · Sep 17, 11:53

**Background**: The U.S. government has imposed successive rounds of export controls since 2022 to restrict China's access to advanced AI chips and semiconductor manufacturing equipment, including bans on high-end GPUs like Nvidia's A100 and H100. These measures have pushed Chinese tech firms to accelerate development of domestic alternatives. Huawei's HiSilicon subsidiary designs the Ascend series of AI accelerators, which are used by major Chinese cloud providers for AI training and inference workloads. Nvidia, meanwhile, has developed compliant chips such as the H20 specifically for the Chinese market, though these have faced their own regulatory uncertainties.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/artificial-intelligence/huawei-ascend-ai-910d-processor-designed-to-take-on-nvidias-blackwell-and-rubin-gpus">Huawei Ascend AI 910D processor designed to... | Tom's Hardware</a></li>
<li><a href="https://www.zerohedge.com/ai/huawei-pulls-its-nvidia-killer-forward-q1-theres-catch">Huawei Pulls Its Nvidia-Killer Forward To Q1 - But... | ZeroHedge</a></li>
<li><a href="https://www.csis.org/analysis/understanding-biden-administrations-updated-export-controls">Understanding the Biden Administration’s Updated Export Controls</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#Huawei`, `#Nvidia`, `#semiconductors`, `#China tech`

---

<a id="item-9"></a>
## [Astra for Law](https://openai.com/index/astra-for-law/) ⭐️ 6.0/10

OpenAI launches Astra for Law, a domain-specific AI product for legal applications, with API partnerships enabling integration into existing legal tech platforms like Harvey and Legora.

hackernews · OpenAI Blog · Sep 17, 20:17 · [Discussion](https://news.ycombinator.com/item?id=49745940)

**Tags**: `#openai`, `#legal-tech`, `#ai-products`, `#vertical-ai`, `#domain-specific`

---

<a id="item-10"></a>
## [Bend – A language that blocks AI mistakes via proof, on CPU and GPU](https://bend-lang.com/) ⭐️ 6.0/10

Bend is a new programming language that uses formal proof-based invariant checking to catch errors (particularly in AI-generated code) and runs on both CPUs and GPUs.

hackernews · nicolas-siplis · Sep 17, 20:36 · [Discussion](https://news.ycombinator.com/item?id=49746163)

**Tags**: `#programming-languages`, `#formal-verification`, `#gpu-computing`, `#ai-code-generation`, `#developer-tools`

---

<a id="item-11"></a>
## [GitLab.com Tightens Rate Limits, Sparking Debate on AI Scraping and API Design](https://about.gitlab.com/blog/rate-limit-change-2026/) ⭐️ 6.0/10

GitLab.com announced changes to its rate limits in a 2026 blog post, reducing unauthenticated request allowances to 60 per hour while free-tier authenticated users retain 5,000 per hour. The policy shift was framed partly as a response to AI-driven scraping pressure on the platform. This change affects every developer and AI agent that interacts with GitLab.com's APIs, potentially disrupting LLM-powered workflows and CI/CD automation that rely on generous anonymous access. It also signals a broader industry trend where platforms are monetizing or restricting access previously assumed to be open, pushing the ecosystem toward more sustainable funding models. The stark gap between 60/hour unauthenticated and 5,000/hour authenticated effectively forces users to create accounts, while GraphQL's ability to constrain response payloads makes it far more token-efficient for LLM agents than REST. Some commenters view this as a revenue-driven subscription push rather than a purely technical response to scraping.

hackernews · darkwater · Sep 17, 15:33 · [Discussion](https://news.ycombinator.com/item?id=49742353)

**Background**: Rate limits control how many API requests a client can make within a given time window, and platforms use them to prevent abuse and manage infrastructure costs. AI scraping — automated bulk data collection by generative AI companies for training or inference — has become a flashpoint in 2025–2026, with websites increasingly blocking or charging scrapers. GitLab and GitHub both expose REST and GraphQL APIs; GraphQL lets clients specify exactly which fields they need, which dramatically reduces data volume — a property that happens to align well with LLM context-window constraints.

<details><summary>References</summary>
<ul>
<li><a href="https://cacm.acm.org/opinion/ai-scraping-and-the-open-web/">AI Scraping and the Open Web – Communications of the ACM</a></li>
<li><a href="https://www.ibm.com/think/topics/ai-scraping">What is AI scraping? - IBM</a></li>

</ul>
</details>

**Discussion**: Commenters split into several camps: one faction enthusiastically endorsed GraphQL as the ideal API surface for LLM agents due to its token efficiency; others highlighted the buried detail that authenticated free-tier limits remain generous at 5,000/hour; some proposed revenue-sharing with scraped open-source repos as a sustainable funding model; and skeptics argued the real motive is boosting paid subscriptions rather than countering AI scraping. A humorous note observed that even Claude appeared to have drafted the press release.

**Tags**: `#gitlab`, `#rate-limits`, `#ai-scraping`, `#platform-policy`, `#developer-tools`

---

<a id="item-12"></a>
## [OpenAI launches Sponsored Agents advertising in ChatGPT](https://openai.com/index/reimagining-advertising-with-ai) ⭐️ 6.0/10

OpenAI announced new AI-powered advertising experiences, including Sponsored Agents, tools for marketers, and integrations with HubSpot and Shopify, formally entering the AI advertising market on September 16, 2026. This marks a significant business model shift for OpenAI, transitioning from API pricing toward agent-mediated advertising, and turns ChatGPT into an ad platform where brands themselves become the product, potentially reshaping how digital advertising operates in the AI era. Unlike traditional digital advertising that relies on external links, Sponsored Agents embed brand interactions directly within AI-mediated conversations, and OpenAI reportedly reached $1B ARR in under 200 days prior to this advertising push.

rss · OpenAI Blog · Sep 16, 13:00

**Background**: Agentic AI refers to autonomous AI systems that independently make decisions and take actions to achieve goals with minimal human direction, and in marketing, this enables automated planning, execution, and optimization of campaigns at scale. Major platforms like Adobe and Amazon Ads have already begun building agentic marketing workflows. OpenAI's move into Sponsored Agents represents one of the first large-scale deployments of agent-mediated advertising within a consumer chatbot product, leveraging integrations with established commerce backends like Shopify and marketing platforms like HubSpot.

<details><summary>References</summary>
<ul>
<li><a href="https://forkast.news/openais-sponsored-agents-turn-chatgpt-into-an-ad-platform-where-brands-are-the-product/">OpenAI’s Sponsored Agents Turn ChatGPT Into an Ad Platform ...</a></li>

</ul>
</details>

**Tags**: `#openai`, `#ai-advertising`, `#sponsored-agents`, `#marketing-tech`, `#industry-announcement`

---

<a id="item-13"></a>
## [How workers are unlocking new ways of working](https://openai.com/index/unlocking-new-ways-of-working) ⭐️ 6.0/10

OpenAI Economic Research examines how workers use AI beyond traditional roles and which new AI-enabled activities become recurring parts of their work.

rss · OpenAI Blog · Sep 16, 09:00

**Tags**: `#AI adoption`, `#economic research`, `#workforce productivity`, `#OpenAI`, `#human-AI interaction`

---

<a id="item-14"></a>
## [Doubled inference speed on single AMD R9700 with Qwen3 27B NVFP4](https://www.reddit.com/r/LocalLLaMA/comments/1wiws8e/153_toks_on_1x_amd_radeon_r9700_running_qwen38/) ⭐️ 6.0/10

Benchmarks on a single AMD Radeon R9700 running Unsloth's Qwen3.8 27b NVFP4 model show decode speeds up to 153 tok/s (JSON category), 471 tok/s aggregate at 8 concurrent requests, and prefill throughput peaking at 3,619 tok/s at 16k context depth. The submitter, responding to repeated community requests, optimized their custom vLLM fork (vllm-mxfp4) for single-GPU R9700 users, roughly doubling performance across all benchmark categories. This demonstrates that a mid-range single AMD GPU can comfortably run a 27B-class model at usable interactive speeds, lowering the barrier to local LLM deployment for AMD hardware owners who have historically been underserved compared to NVIDIA. It also signals maturing AMD ROCm/quantization support for FP4 inference, a critical capability as models continue to grow in size. The author used Unsloth's NVFP4-quantized Qwen3.8 27b weights served via a custom vllm-mxfp4 fork (also mirrored to a Codeberg repo called radiance-vllm-mxfp4); prefill throughput stays above 3,400 tok/s from 2k to 32k context and only drops to ~3,192 tok/s at 64k, while decode latency hovers around 34–42 ms p50. NVFP4 is a 4-bit floating-point format from NVIDIA with smaller block sizes than its MXFP4 predecessor, enabling aggressive memory compression with competitive accuracy on Blackwell-class and now apparently RDNA4 hardware.

reddit · r/LocalLLaMA · /u/whodoneit1 · Sep 17, 15:14

**Background**: LLM inference is typically split into two phases: prefill, where the entire prompt is processed at once to populate the KV cache, and decode, where tokens are generated one at a time autoregressively. Prefill is compute-bound and benefits from high memory bandwidth and throughput, while decode is memory-bandwidth-bound and tends to favor larger batch sizes or aggressive quantization. NVFP4 is NVIDIA's 4-bit floating-point quantization format that uses small grouped blocks and per-block scaling factors, reducing model memory footprint by roughly 4× compared to 16-bit formats while preserving accuracy well enough for practical inference. Unsloth is a popular open-source library that accelerates LLM fine-tuning and exports models in formats compatible with serving runtimes like vLLM.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/introducing-nvfp4-for-efficient-and-accurate-low-precision-inference/">Introducing NVFP4 for Efficient and Accurate Low-Precision ...</a></li>
<li><a href="https://deepwiki.com/NVlabs/QeRL/3.2-nvfp4-quantization">NVFP4 Quantization | NVlabs/QeRL | DeepWiki</a></li>
<li><a href="https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/">Mastering LLM Techniques: Inference Optimization | NVIDIA Technical...</a></li>

</ul>
</details>

**Tags**: `#AMD GPU`, `#local LLM`, `#inference benchmarks`, `#Qwen3`, `#NVFP4 quantization`

---

<a id="item-15"></a>
## [IFM Releases K2-Horizon-7B: Diffusion Adapter Boosts LLM to 5200 TPS](https://www.reddit.com/r/LocalLLaMA/comments/1wj2hsm/ifmk2horizon7buno_hugging_face_5200tps_with_no/) ⭐️ 6.0/10

IFM released K2-Horizon-7B on Hugging Face, a diffusion-augmented language model that adds plug-and-play diffusion adapters alongside autoregressive weights to enable parallel token generation. The model claims up to 5200 tokens per second with no quality loss, with reported speedups ranging from 2.2× to 2.5× over standard autoregressive inference. If verified, this approach could significantly reduce LLM inference costs and latency, making high-throughput AI deployments more affordable. The plug-and-play nature of the adapter means existing autoregressive models could potentially benefit without full retraining, which would be a major practical advantage for the open-source AI ecosystem. The architecture augments each layer of a standard autoregressive model with a separate set of diffusion weights dedicated to parallel token generation, decoupling generation quality from generation speed. However, the 'no quality loss' claim lacks publicly presented benchmarks in the announcement, and IFM's own messaging cites varying speedup figures (2.2× versus 2.5×), so independent verification is needed before treating these results as definitive.

reddit · r/LocalLLaMA · /u/Zulfiqaar · Sep 17, 18:43

**Background**: Standard autoregressive LLMs like GPT generate text one token at a time in sequence, which limits inference throughput. Diffusion language models, by contrast, generate multiple tokens in parallel and can flexibly trade off speed and quality by using fewer generation steps. The 'Uno' approach attempts to combine the strengths of both paradigms by adding lightweight diffusion adapters to an existing autoregressive model, allowing parallel token emission without retraining the base model. K2-Horizon is IFM's broader family of six fully open-source models ranging from 0.9B to 375B parameters, released under Apache 2.0.

<details><summary>References</summary>
<ul>
<li><a href="https://hyper.ai/en/papers/2609.04010">Unlocking Lossless Speedups in LLMs via Discrete Diffusion | HyperAI</a></li>
<li><a href="https://cryptobriefing.com/uno-diffusion-llm-throughput/">Uno achieves 2.5x higher throughput in LLMs by bolting diffusion onto...</a></li>
<li><a href="https://ifm.ai/k2/">K2 Horizon: Open-Source AI Models for Every Scale | IFM</a></li>

</ul>
</details>

**Tags**: `#diffusion-models`, `#llm-inference`, `#model-optimization`, `#open-source-models`, `#speedup`

---

<a id="item-16"></a>
## [First Leaked M5 Ultra Benchmarks Show 50 tok/s on Qwen 27B Q4](https://www.reddit.com/r/LocalLLaMA/comments/1wisr6h/first_m5_ultra_benchmarks/) ⭐️ 6.0/10

Early benchmarks for Apple's unreleased M5 Ultra chip, posted on the omlx website, show the chip running Qwen 3.8 27B at Q4 quantization at approximately 50 tokens/sec for text generation (th) and 1800 tokens/sec for prompt processing (pp) at an 8K context window, without multi-token prediction enabled. If accurate, these numbers would significantly raise the bar for consumer-grade local LLM inference on Apple Silicon, narrowing the gap between Mac workstations and dedicated GPU rigs and potentially reshaping purchasing decisions for hobbyists and professionals running models locally. The benchmarks were measured at Q4 quantization (4-bit weights, reducing memory and compute requirements) on Qwen 3.8 27B with an 8K context window and without MTP acceleration. The credibility of the source is unverified: the omlx website's official status is unknown, no independent replication exists yet, and Apple has not officially announced the M5 Ultra.

reddit · r/LocalLLaMA · /u/Ashefromapex · Sep 17, 12:34

**Background**: Qwen is a family of open-weight large language models developed by Alibaba Cloud, with Qwen3 introducing hybrid thinking modes that let users balance reasoning depth against speed. Q4 quantization is a post-training technique that compresses model weights to roughly 4 bits per parameter, cutting memory use and accelerating inference with minimal quality loss, which is especially valuable for running large models on consumer hardware. Multi-Token Prediction (MTP) is an emerging inference acceleration technique that predicts several tokens in parallel to boost throughput, and the M5 Ultra results here were measured without MTP enabled, meaning the raw throughput could be even higher once MTP is applied.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://arxiv.org/html/2402.16775v1">A Comprehensive Evaluation of Quantization Strategiesfor ...</a></li>
<li><a href="https://arxiv.org/html/2502.09419v1">On multi-token prediction for efficient LLM inference - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#apple-silicon`, `#m5-ultra`, `#local-llm`, `#hardware-benchmarks`, `#inference-performance`

---