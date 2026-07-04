---
layout: default
title: "Horizon Summary: 2026-07-04 (EN)"
date: 2026-07-04
lang: en
---

> From 69 items, 13 important content pieces were selected

---

1. [Karpathy Launches nanochat: Building the Best ChatGPT Clone for $100](#item-1) ⭐️ 8.0/10
2. [Leaking YouTube creators' private videos](#item-2) ⭐️ 8.0/10
3. [Claude Code Investigates Reports of Cross-Account Response Leakage](#item-3) ⭐️ 7.0/10
4. [Meta data center water discharges suspended for contaminating water supply](#item-4) ⭐️ 7.0/10
5. [Astrophysicists Puzzle over Webb’s New Universe](#item-5) ⭐️ 7.0/10
6. [SJTU Proposes HAT-4D: 4D Interactive Scenes from Monocular Video](#item-6) ⭐️ 7.0/10
7. [Multi-Block Diffusion Language Models Bridge Training-Inference Gap](#item-7) ⭐️ 7.0/10
8. [Mistral Releases Leanstral 1.5: A Specialized 119B MoE Model for Formal Verification](#item-8) ⭐️ 7.0/10
9. [huggingface/transformers released v5.13.0](#item-9) ⭐️ 6.0/10
10. [Performance per dollar is getting faster and cheaper](#item-10) ⭐️ 6.0/10
11. [Google DeepMind and A24 announce first-of-its-kind research partnership](#item-11) ⭐️ 6.0/10
12. [Google Research Releases TabFM, a Zero-Shot Tabular Foundation Model](#item-12) ⭐️ 6.0/10
13. [Doing the actual math on a $20k local AI rig breakeven](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Karpathy Launches nanochat: Building the Best ChatGPT Clone for $100](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy has created a new GitHub repository called nanochat, described as 'the best ChatGPT that $100 can buy,' aimed at providing a minimal full-stack LLM training system for building a ChatGPT-like conversational model on an extremely tight compute budget. Because Karpathy is one of the most influential voices in AI/ML education — known for projects like nanoGPT and the original GPT-2/4 training exercises — any new repo from him draws major community attention and shapes how developers learn LLM training. A $100-budget target also reframes the conversation around cost-efficient training at a time when frontier model development is dominated by well-funded labs. The project is built around a 'single-complexity-dial' design philosophy, and the repository introduces a 'Time-to-GPT-2 leaderboard' concept for benchmarking training efficiency. As an early-stage repo with only a minimal one-line description, the full technical details, code structure, and training pipeline are not yet documented in the announcement.

github · karpathy · Jul 4, 03:44

**Background**: Andrej Karpathy is a former co-founder of OpenAI and former Director of AI at Tesla, widely regarded as one of the most effective educators in modern deep learning. His previous minimal-style educational repos — such as nanoGPT, which reimplemented GPT-2 training from scratch in a few hundred lines of code — have become go-to learning resources for practitioners who want to understand LLM training hands-on rather than just calling APIs. nanochat extends this same 'nano' philosophy to an end-to-end chat model, including not just pretraining but the post-training steps (such as instruction tuning) needed to produce a usable conversational assistant. The $100 budget claim also reflects a broader industry shift toward questioning whether competitive chat models really require hundred-million-dollar training runs.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy/nanochat: The best ChatGPT that $100 can ...</a></li>
<li><a href="https://deepwiki.com/karpathy/nanochat">karpathy/nanochat | DeepWiki</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#fine-tuning`, `#Andrej Karpathy`, `#chat-models`, `#cost-efficient-training`

---

<a id="item-2"></a>
## [Leaking YouTube creators' private videos](https://javoriuski.com/post/youtube) ⭐️ 8.0/10

A disclosed YouTube vulnerability exploits prompt injection via AI-suggested comment responses in YouTube Studio to leak creators' private/unlisted videos.

hackernews · javxfps · Jul 4, 16:45 · [Discussion](https://news.ycombinator.com/item?id=48786781)

**Tags**: `#security`, `#prompt-injection`, `#youtube`, `#vulnerability-disclosure`, `#ai-security`

---

<a id="item-3"></a>
## [Claude Code Investigates Reports of Cross-Account Response Leakage](https://github.com/anthropics/claude-code/issues/74066) ⭐️ 7.0/10

A GitHub issue (#74066) on the anthropics/claude-code repository reports potential session/cache leakage between workspace instances, with multiple users across different LLM providers (Claude, GPT, and Gemini) describing similar cross-account response contamination. Thariq from the Claude Code team responded that they are confident the reports are hallucinations but are investigating the issue seriously. If confirmed, cross-account response contamination would represent a critical security vulnerability in LLM API infrastructure, potentially exposing private user data across tenants—a breach of fundamental multi-tenant isolation guarantees. The breadth of independent reports across multiple providers raises systemic concerns about how LLM gateways, load balancers, and caching layers handle concurrent requests and shared infrastructure. One technical commenter identified a plausible root cause: an API gateway incorrectly handling HTTP 100 (Continue) status codes, creating an off-by-one error that could cause response swapping between concurrent sessions. The original poster's scenario included an 800K+ token context window and a tool call result containing 'minecraft.py' in a file path, which some argue increases the likelihood of hallucination rather than actual leakage.

hackernews · chatmasta · Jul 4, 14:03 · [Discussion](https://news.ycombinator.com/item?id=48785485)

**Background**: Claude Code is Anthropic's agentic CLI tool that allows developers to interact with Claude models directly from the terminal for codebase operations. LLM APIs typically serve multiple users simultaneously through shared infrastructure including API gateways, load balancers, and caching layers. Session isolation is a fundamental security property ensuring that one user's conversation context and responses are never visible to another user. Hallucination, in contrast, is a well-known phenomenon where LLMs generate plausible but fabricated outputs—often triggered by large context windows or unusual prompt patterns—which can be confused with genuine data leakage.

<details><summary>References</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=48785485">Potential session/cache leakage between workspace instances or consumer accounts | Hacker News</a></li>
<li><a href="https://deepwiki.com/anthropics/claude-code/1.1-system-architecture">System Architecture | anthropics/claude-code | DeepWiki</a></li>
<li><a href="https://www.giskard.ai/knowledge/cross-session-leak-when-your-ai-assistant-becomes-a-data-breach">Cross Session Leak: LLM security vulnerability & detection guide</a></li>

</ul>
</details>

**Discussion**: Community sentiment is divided between serious technical analysis and skepticism. The original throwaway account and several commenters provided detailed technical evidence including a postmortem from one provider attributing response swapping to HTTP 100 status code handling bugs in API gateways, lending credibility to the concern. However, other commenters—including the Claude Code team itself—lean toward hallucination as the more likely explanation, noting that very large contexts (800K+ tokens) and specific prompt patterns can trigger fabricated but plausible-looking responses. Several users across Gemini and GPT also reported similar experiences, broadening the scope of the investigation beyond just Claude.

**Tags**: `#claude-code`, `#security`, `#llm-infrastructure`, `#data-leakage`, `#anthropic`

---

<a id="item-4"></a>
## [Meta data center water discharges suspended for contaminating water supply](https://www.tomshardware.com/tech-industry/data-centers/cheyenne-suspends-data-center-fill-and-flush-and-closed-loop-discharges-after-meta-contractor-contaminated-its-reuse-water-system) ⭐️ 7.0/10

Meta's data center contractor contaminated Cheyenne's water reuse system with additives, prompting the city to suspend water fill/flush operations and closed-loop discharges.

hackernews · sensanaty · Jul 4, 16:45 · [Discussion](https://news.ycombinator.com/item?id=48786782)

**Tags**: `#data-centers`, `#environment`, `#meta`, `#water-pollution`, `#ai-infrastructure`

---

<a id="item-5"></a>
## [Astrophysicists Puzzle over Webb’s New Universe](https://www.quantamagazine.org/astrophysicists-puzzle-over-webbs-new-universe-20260702/) ⭐️ 7.0/10

JWST observations of mysterious 'little red dots' in the early universe are puzzling astrophysicists, potentially representing a new class of object called 'black hole stars' where gas cocoons emit light like stellar atmospheres.

hackernews · jnord · Jul 4, 09:08 · [Discussion](https://news.ycombinator.com/item?id=48783948)

**Tags**: `#astronomy`, `#astrophysics`, `#jwst`, `#cosmology`, `#science-journalism`

---

<a id="item-6"></a>
## [SJTU Proposes HAT-4D: 4D Interactive Scenes from Monocular Video](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247901356&idx=3&sn=54ee94026f76691a380cd3ea214e0def) ⭐️ 7.0/10

Researchers from Shanghai Jiao Tong University proposed HAT-4D, an agentic framework that reconstructs dynamic 4D multi-object interactions directly from monocular video, targeting the challenge of severe occlusions and complex dynamics that trip up prior isolated-object reconstruction methods. HAT-4D offers an efficient, low-cost data collection pathway for scaling Embodied AI and training Vision-Language-Action (VLA) models by converting massive in-the-wild monocular videos into simulation-ready 4D scenes, potentially replacing expensive motion capture studios. Unlike prior monocular 4D reconstruction methods that focus primarily on isolated objects, HAT-4D is designed to handle multi-object interactions under heavy occlusion. It is positioned as infrastructure for embodied AI world-model research, alongside related efforts like OVOW (instance-level 4D mesh reconstruction) and ArtHOI (articulated human-object interaction).

rss · 量子位 · Jul 3, 03:43

**Background**: 4D scene reconstruction refers to recovering dynamic 3D geometry over time from visual input. Monocular video reconstruction is particularly challenging because depth is inherently ambiguous from a single camera, and multi-object interactions introduce severe occlusions that confuse depth estimation. Embodied AI and VLA (Vision-Language-Action) models require large amounts of interaction data, traditionally collected via costly motion capture studios with multiple calibrated cameras, making scalable in-the-wild data collection a major bottleneck.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2606.28215">HAT-4D: Lifting Monocular Video for 4D Multi-Object ...</a></li>
<li><a href="https://arxiv.org/html/2606.28215v1">HAT-4D: Lifting Monocular Video for 4D Multi-Object ...</a></li>
<li><a href="https://onevideooneworld.github.io/">OVOW: One Video , One World — Turning Monocular Video into...</a></li>

</ul>
</details>

**Tags**: `#4D-scene-generation`, `#computer-vision`, `#monocular-video`, `#human-object-interaction`, `#research`

---

<a id="item-7"></a>
## [Multi-Block Diffusion Language Models Bridge Training-Inference Gap](https://www.reddit.com/r/LocalLLaMA/comments/1un8y5p/paper_multiblock_diffusion_language_models/) ⭐️ 7.0/10

The paper introduces Multi-Block Diffusion Language Models (MBD-LMs) trained via a new Multi-block Teacher Forcing (MultiTF) strategy that post-trains Block Diffusion LMs to match MultiBD inference states, along with a Block Buffer decoding algorithm that preserves prefix-cache reuse and keeps input shapes static. This work directly tackles a real training-inference mismatch in parallel block-wise diffusion decoding, delivering nearly 2× throughput (TPF 3.47→6.19) with simultaneous accuracy gains, making diffusion-based text generation more practical for production and relevant to competing approaches like LLaDA and Mercury. MBD-LLaDA2-Mini raises average Tokens Per Forward from 3.47 to 6.19 and accuracy from 79.95% to 81.03%; combined with the DMax decoding scheme, MBD-LLaDA2-Mini-DMax reaches an average TPF of 9.34 with only a 1.02% accuracy drop on math and code benchmarks, using a Block Buffer that reuses prefix KV cache.

reddit · r/LocalLLaMA · /u/pmttyji · Jul 4, 13:21

**Background**: Block Diffusion Language Models (BD-LMs), introduced as an ICLR 2025 Oral, decompose token sequences into blocks and run discrete denoising within each block, interpolating between autoregressive and full-sequence diffusion to combine parallel generation with flexible length. Standard autoregressive transformers use KV caching to avoid recomputing past token representations during generation, which is critical for inference speed. Diffusion Forcing is a training strategy that lets each token carry a different noise level, enabling causal next-token prediction models to generate future tokens without fully diffusing past ones. MBD-LMs build on BD-LMs by extending single-block decoding to a running-set of consecutive blocks decoded concurrently, but existing training schemes (teacher forcing on one noisy block, or diffusion forcing) do not match this multi-block inference regime, creating a training-inference gap that the paper aims to close.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2503.09573">[2503.09573] Block Diffusion: Interpolating Between ... A arXiv:2503.09573v3 [cs.LG] 17 May 2025 Block Diffusion - m-arriola.com GitHub - kuleshov-group/bd3lms: [ICLR 2025 Oral] Block ... Awesome Diffusion Language Models - GitHub DiffusionGemma — Google DeepMind Encoder-Decoder Diffusion Language Models for Efficient ...</a></li>
<li><a href="https://github.com/kuleshov-group/bd3lms">GitHub - kuleshov-group/bd3lms: [ICLR 2025 Oral] Block ...</a></li>
<li><a href="https://arxiv.org/abs/2407.01392">[2407.01392] Diffusion Forcing : Next-token Prediction Meets...</a></li>

</ul>
</details>

**Tags**: `#diffusion-models`, `#language-models`, `#research-paper`, `#text-generation`, `#parallel-decoding`

---

<a id="item-8"></a>
## [Mistral Releases Leanstral 1.5: A Specialized 119B MoE Model for Formal Verification](https://www.reddit.com/r/LocalLLaMA/comments/1umgdhx/mistral_released_leanstral15119ba6b/) ⭐️ 7.0/10

Mistral released Leanstral 1.5, an Apache-2.0 licensed 119B (6B active) Mixture-of-Experts model specialized for formal verification and automated theorem proving. It achieves state-of-the-art results on FATE-H (87%) and FATE-X (34%), saturates miniF2F, solves 587/672 PutnamBench problems, and uncovered 5 previously unknown bugs across 57 tested repositories. This release demonstrates that specialized small-active-parameter models can reach frontier-class performance in niche domains like formal verification, offering a cost-effective, open-source alternative to general-purpose LLMs. It also delivers tangible real-world value by finding bugs that traditional testing and fuzzing missed, which could meaningfully impact software verification workflows. The model was trained through a three-stage pipeline: mid-training, supervised fine-tuning, and reinforcement learning with the CISPO (Clipped Importance Sampling Policy Optimization) algorithm, which clips importance sampling weights to bound variance and improve stability over methods like PPO and GRPO. Despite having 119B total parameters, only 6B are active per inference, making it computationally efficient for its capability level.

reddit · r/LocalLLaMA · /u/Tall-Ad-7742 · Jul 3, 14:44

**Background**: Lean is a free, open-source theorem prover and functional programming language based on the calculus of constructions with inductive types, widely used to mathematically prove software correctness. miniF2F is a benchmark of competition-level mathematics problems (AMC, AIME, IMO) formalized across multiple proof systems, while PutnamBench is a multilingual suite of 640 formalized problems from the Putnam Competition expressed in Lean, Isabelle, and Coq. FATE-H and FATE-X are evaluation benchmarks specifically designed to test LLMs on formal verification tasks involving Lean and similar proof assistants.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/cispo-algorithm">CISPO: Clipped Importance Sampling RL - emergentmind.com</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_(proof_assistant)">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://www.emergentmind.com/topics/putnambench">PutnamBench : Theorem Proving Benchmark</a></li>

</ul>
</details>

**Discussion**: Community reaction was mixed. Some users (e.g., u/InsideOutSanta) praised Mistral's niche specialization strategy, arguing that high-quality small models are valuable for specific tasks. However, u/boulos and u/Groxx questioned the validity of one specific bug-finding example, with Groxx pointing out an identical issue was filed on the affected repository a week before the blog post was published. u/andai criticized the benchmark comparisons as outdated, featuring models from half a year ago, while u/raphinou asked about practical usability for developers with no Lean experience.

**Tags**: `#formal-verification`, `#theorem-proving`, `#Mistral`, `#open-source`, `#code-verification`

---

<a id="item-9"></a>
## [huggingface/transformers released v5.13.0](https://github.com/huggingface/transformers/releases/tag/v5.13.0) ⭐️ 6.0/10

Hugging Face Transformers v5.13.0 adds architecture support for Kimi K2.5, K2.6, and K2.7 open-source multimodal agentic models.

github · vasqu · Jul 3, 16:06

**Tags**: `#huggingface`, `#transformers`, `#kimi-k2`, `#model-release`, `#open-source`

---

<a id="item-10"></a>
## [Performance per dollar is getting faster and cheaper](https://www.wafer.ai/blog/glm52-amd) ⭐️ 6.0/10

Blog post comparing AI inference performance per dollar on AMD hardware, with community discussion highlighting critical concerns about FP4 quantization accuracy and missing performance-per-watt metrics.

hackernews · latchkey · Jul 3, 21:49 · [Discussion](https://news.ycombinator.com/item?id=48780417)

**Tags**: `#AI-hardware`, `#GPU-benchmarking`, `#AMD`, `#quantization`, `#cost-optimization`

---

<a id="item-11"></a>
## [Google DeepMind and A24 announce first-of-its-kind research partnership](https://deepmind.google/blog/google-deepmind-and-a24-announce-first-of-its-kind-research-partnership/) ⭐️ 6.0/10

Google DeepMind and A24 announce a unique research partnership exploring the intersection of AI and filmmaking.

rss · Google DeepMind Blog · Jul 3, 14:25

**Tags**: `#AI`, `#DeepMind`, `#creative-AI`, `#filmmaking`, `#industry-partnership`

---

<a id="item-12"></a>
## [Google Research Releases TabFM, a Zero-Shot Tabular Foundation Model](https://www.reddit.com/r/LocalLLaMA/comments/1un5hyi/googletabfm100/) ⭐️ 6.0/10

Google Research has released TabFM (version 1.0.0), a zero-shot foundation model for tabular data that supports classification and regression tasks on datasets with mixed numerical and categorical columns, requiring no fine-tuning or hyperparameter search. Predictions are made in a single forward pass by passing training examples as in-context examples, with the model now available on Hugging Face and GitHub and slated for BigQuery integration. Tabular data underpins a large fraction of enterprise machine learning workloads, yet it has lagged behind text and images in benefiting from foundation-model-style zero-shot workflows. By eliminating dataset-specific training and hyperparameter tuning, TabFM could dramatically lower the barrier to deploying ML on structured data, positioning itself as the tabular counterpart to Google's TimesFM time-series model. Under the hood, TabFM extends the Prior-Data Fitted Networks (PFN) lineage pioneered by TabPFN, using an Adversarially Pre-trained Transformer (APT) trained on synthetic data agents to perform zero-shot meta-learning without pre-training on any real-world dataset. Unlike traditional tabular ML pipelines, it treats prediction as in-context learning rather than parameter fitting, which constrains it primarily to classification and regression tasks rather than generative use cases.

reddit · r/LocalLLaMA · /u/Balance- · Jul 4, 10:20

**Background**: Tabular foundation models are an emerging class of neural architectures pre-trained on heterogeneous table data to provide transferable priors for downstream tasks. The paradigm was pioneered by TabPFN, which framed in-context learning (ICL) for tabular data from a Bayesian perspective, approximating the posterior predictive distribution over synthetic datasets. Successors such as TabICL have pushed this approach toward scalability via techniques including learned context distillation, example selection, linear attention, and hypernetwork-based task-specific generation. TabFM joins this trajectory with Google's industrial-scale weight.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM: A zero-shot foundation model for tabular data</a></li>
<li><a href="https://arxiv.org/abs/2502.04573">[2502.04573] Zero-shot Meta-learning for Tabular Prediction ... Google TabFM: Zero-Shot Foundation Model for Tabular ... Zero-shot Meta-learning for Tabular Prediction Tasks with ... Zero-shot Meta-learning for Tabular Prediction Tasks with ... Google's TabFM: Zero-shot tabular classification without tra google/tabfm-1.0.0-pytorch · Hugging Face</a></li>
<li><a href="https://www.explainx.ai/blog/google-tabfm-zero-shot-tabular-foundation-model-2026">Google TabFM: Zero-Shot Foundation Model for Tabular ...</a></li>

</ul>
</details>

**Tags**: `#tabular-data`, `#foundation-models`, `#zero-shot-learning`, `#google-research`, `#machine-learning`

---

<a id="item-13"></a>
## [Doing the actual math on a $20k local AI rig breakeven](https://www.reddit.com/r/LocalLLaMA/comments/1un6njn/doing_the_actual_math_on_a_20k_local_ai_rig/) ⭐️ 6.0/10

A cost analysis modeling electricity consumption and upfront hardware costs of a $20k local AI rig against a $200/month subscription to determine the actual breakeven crossover point.

reddit · r/LocalLLaMA · /u/shyaaaaaaaaaaam · Jul 4, 11:27

**Tags**: `#local-llm`, `#cost-analysis`, `#self-hosting`, `#hardware`, `#economics`

---