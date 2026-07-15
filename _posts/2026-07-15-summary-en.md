---
layout: default
title: "Horizon Summary: 2026-07-15 (EN)"
date: 2026-07-15
lang: en
---

> From 52 items, 18 important content pieces were selected

---

1. [Linus Torvalds tells people to stop attacking others for using AI](#item-1) ⭐️ 8.0/10
2. [Pluralis Runs RL Post-Training on 14 Macs Across 4 Countries](#item-2) ⭐️ 8.0/10
3. [ExLlamaV3 v1.0.0 Released with Major Performance Upgrades](#item-3) ⭐️ 8.0/10
4. [Inkling: Our Open-Weights Model](#item-4) ⭐️ 7.0/10
5. [Stripe and Advent have made a joint offer to acquire PayPal – sources](#item-5) ⭐️ 7.0/10
6. [Gemma 4 26B Runs at 5 tok/s on 13-Year-Old Xeon Without GPU](#item-6) ⭐️ 7.0/10
7. [Show HN: misa77 - a codec that decodes 2x faster than LZ4 (at better ratios)](#item-7) ⭐️ 7.0/10
8. [Sleep regularity is a stronger predictor of mortality risk than sleep duration (2023)](#item-8) ⭐️ 7.0/10
9. [OpenAI Unveils GPT-Red: Self-Play Automated Red Teaming for AI Safety](#item-9) ⭐️ 7.0/10
10. [AllenAI Shares Engineering Lessons from Building Shippy Agent](#item-10) ⭐️ 7.0/10
11. [Model Routing Is Simple — Until It Isn't](#item-11) ⭐️ 7.0/10
12. [HuggingFace Launches Real World VoiceEQ Benchmark for Voice AI](#item-12) ⭐️ 7.0/10
13. [Tencent Releases RxBrain: A Unified Multimodal Model for Embodied AI](#item-13) ⭐️ 7.0/10
14. [Transformers v5.14.0 Adds Thinking Machines' 975B Inkling Multimodal Model](#item-14) ⭐️ 6.0/10
15. [Mysteries of Telegram Data Centers (2022)](#item-15) ⭐️ 6.0/10
16. [Google is updating Gemma 4's chat templates, bringing major fixes to tool calling and reducing "laziness", and enabling Flash Attention 4 on Hopper GPUs, plus an interactive guide on how to work with and improve its vision!](#item-16) ⭐️ 6.0/10
17. [German AI consortium releases Soofi S, an open 30B model that tops benchmarks in both English and German](#item-17) ⭐️ 6.0/10
18. [Apple in Talks with PrismML to Shrink AI Models for iPhones](#item-18) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Linus Torvalds tells people to stop attacking others for using AI](https://www.reddit.com/r/LocalLLaMA/comments/1uxbrw4/linus_torvalds_tells_people_to_stop_attacking/) ⭐️ 8.0/10

Linus Torvalds declares that Linux kernel development will accept AI-generated code and warns contributors to stop attacking others for using AI tools, calling AI a clearly useful tool despite its occasional pain points.

reddit · r/LocalLLaMA · /u/Illustrious_Car344 · Jul 15, 16:59

**Tags**: `#Linux`, `#AI`, `#OpenSource`, `#LinusTorvalds`, `#SoftwareEngineering`

---

<a id="item-2"></a>
## [Pluralis Runs RL Post-Training on 14 Macs Across 4 Countries](https://www.reddit.com/r/LocalLLaMA/comments/1uxb3zn/rl_posttraining_on_14_macs_across_4_countries/) ⭐️ 8.0/10

Pluralis Research demonstrated what appears to be the first RL post-training run whose rollout fleet ran entirely on consumer Macs over the open internet. A fleet of 14 Macs across 4 countries generated rollouts via int8 MLX inference, while a single B200 on another continent performed bf16 Megatron gradient updates; the two sides synchronized only through Cloudflare R2 over ordinary home internet. Rollout generation accounts for roughly 80% of the compute in agentic RL, so the ability to farm it out to idle consumer Macs reshapes who can afford large-scale RL training. By showing that a datacenters and a phone-network of MacBooks can collaborate across continents for post-training, Pluralis points toward a future where frontier-grade RL no longer requires owning a GPU cluster. Two mechanisms keep the off-policy gap manageable: PULSE ships int8 weight deltas rather than full checkpoints — since only ~0.5% of int8 values change between versions, typical transfers were ~82 MB instead of 9 GB — and a DPPO-style probability gate discards ~0.3% of tokens whose probabilities drift too far between rollout and trainer. On the PaperSearchQA multi-turn biomedical search task, the Stoa model's cover pass@1 rose from 29% to 63% and search rate from 22% to 84%.

reddit · r/LocalLLaMA · /u/erfan_mhi · Jul 15, 16:36

**Background**: RL post-training uses reinforcement learning to refine a model after pretraining, and 'agentic RL' specifically trains the model to call tools and chain multi-turn interactions. In such workloads, generating rollout trajectories dominates compute, while gradient updates are comparatively cheap. Two technical constraints make this hard across consumer hardware: Apple's MLX framework only runs well on Apple Silicon and at quantized precisions like int8, whereas training frameworks such as NVIDIA's Megatron typically run bf16 on datacenter GPUs. The 'off-policy gap' is the distributional drift between the policy that produced the data and the policy currently being trained, which grows when rollouts are produced by stale or differently quantized weights.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple ... Exploring LLMs with MLX and the Neural Accelerators in the M5 ... MLX mlx · PyPI MLX — MLX 0.31.2 documentation - GitHub Pages GitHub - frankgmail/apple-mlx: MLX: An array framework for ...</a></li>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>
<li><a href="https://machinelearning.apple.com/research/exploring-llms-mlx-m5">Exploring LLMs with MLX and the Neural Accelerators in the M5 ...</a></li>
<li><a href="https://zoeyli.com/reinforcement+learning/Off-Policy-Corrections-LLM-RL/">Off - Policy Corrections in LLM RL Training - Zoey Li’s Personal Webpage</a></li>

</ul>
</details>

**Tags**: `#reinforcement-learning`, `#distributed-computing`, `#MLX`, `#model-training`, `#open-source`

---

<a id="item-3"></a>
## [ExLlamaV3 v1.0.0 Released with Major Performance Upgrades](https://www.reddit.com/r/LocalLLaMA/comments/1uwylut/exllamav3_v100_major_performance_upgrades/) ⭐️ 8.0/10

ExLlamaV3 has reached its first production release (v1.0.0) after over a year of development, delivering a new attention kernel with online KV cache quantization, a new INT8 GEMV kernel, an MoE kernel ticket scheduler, and expanded tensor-parallel and model support. The release removes dependencies on flash-attention-2 and xformers and adds native conv1d, GptOssForCausalLM, and NemotronHForCausalLM support. ExLlamaV3 is one of the most widely used inference libraries for running LLMs locally on consumer GPUs, so these performance and architectural improvements directly affect the experience of anyone running large models on personal hardware. By eliminating external attention dependencies and introducing online KV cache quantization, the release makes local inference faster, more memory-efficient, and easier to install. The new attention kernel supports online KV cache quantization without the slowdown typical of quantized cache paths, and includes dual input handling for sliding window attention (SWA) layers and attention sinks; Ampere GPUs (e.g., RTX 30-series) see especially large gains from the improved GEMM/GEMV kernels. Tensor-parallel support now extends to most architectures including Gemma4, and the graph capture path covers all attn/GDN modules.

reddit · r/LocalLLaMA · /u/Unstable_Llama · Jul 15, 07:17

**Background**: ExLlamaV3 is a high-performance inference engine specifically optimized for running quantized large language models on NVIDIA GPUs locally. KV cache quantization reduces the memory footprint of the key-value cache that transformers store during generation, enabling longer contexts or larger batch sizes on limited VRAM; online quantization performs this step during inference rather than as a separate preprocessing pass. Mixture-of-Experts (MoE) models route each token to a subset of expert sub-networks, requiring specialized kernels to efficiently schedule which experts process which tokens—a key challenge as models like GPT-OSS and DeepSeek use this architecture. Attention sinks refer to initial tokens that consistently absorb disproportionate attention weights in transformer models, an artifact that specialized kernels must handle to maintain generation quality.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/quantization/quantized_kvcache/">Quantized KV Cache - vLLM</a></li>
<li><a href="https://huggingface.co/blog/moe">Mixture of Experts Explained</a></li>
<li><a href="https://arxiv.org/abs/2604.10098">[2604.10098] Attention Sink in Transformers: A Survey on ...</a></li>

</ul>
</details>

**Tags**: `#ExLlamaV3`, `#LLM-inference`, `#local-llama`, `#GPU-optimization`, `#model-quantization`

---

<a id="item-4"></a>
## [Inkling: Our Open-Weights Model](https://thinkingmachines.ai/news/introducing-inkling/) ⭐️ 7.0/10

Thinking Machines releases Inkling, a new large open-weights multimodal model notable for being among the largest open-weight models with native audio support.

hackernews · vimarsh6739 · Jul 15, 18:12 · [Discussion](https://news.ycombinator.com/item?id=48924912)

**Tags**: `#open-source-ai`, `#multimodal-models`, `#thinking-machines`, `#audio-ai`, `#llm-release`

---

<a id="item-5"></a>
## [Stripe and Advent have made a joint offer to acquire PayPal – sources](https://www.reuters.com/business/finance/stripe-advent-offer-buy-paypal-more-than-53-billion-sources-say-2026-07-15/) ⭐️ 7.0/10

Stripe and Advent have made a joint offer to acquire PayPal for over $53 billion, potentially consolidating two major payment processors into one.

hackernews · rvz · Jul 15, 03:32 · [Discussion](https://news.ycombinator.com/item?id=48915953)

**Tags**: `#fintech`, `#payments`, `#mergers-acquisitions`, `#stripe`, `#paypal`

---

<a id="item-6"></a>
## [Gemma 4 26B Runs at 5 tok/s on 13-Year-Old Xeon Without GPU](https://www.neomindlabs.com/2026/06/08/running-gemma-4-26b-at-5-tokens-sec-on-a-13-year-old-xeon-with-no-gpu/) ⭐️ 7.0/10

A developer demonstrated running Google's Gemma 4 26B — a Mixture-of-Experts model with 4B active parameters — at approximately 5 tokens per second on a dual Xeon server from around 2013 with no GPU acceleration. This benchmark highlights how far CPU-based LLM inference has advanced, showing that 20B+ class models can be usable on legacy enterprise hardware. It also raises important questions about the true cost-effectiveness of local inference versus cloud APIs once electricity and hardware amortization are factored in. Gemma 4 26B is a multimodal MoE model from Google DeepMind built on Gemini 3 research, with only ~4B parameters active per token — a key reason it fits into limited RAM. Community estimates put a loaded dual Xeon system at 300–500W, making local inference roughly 10–30× more expensive per token than a cloud inference provider, even before factoring in cooling costs.

hackernews · neomindryan · Jul 15, 15:34 · [Discussion](https://news.ycombinator.com/item?id=48922434)

**Background**: Gemma 4 is Google's open-weights model family released in 2025–2026, derived from Gemini 3 research, and includes both pretrained and instruction-tuned variants. Mixture-of-Experts (MoE) architectures keep total parameter counts high while only activating a small subset per token, dramatically reducing memory bandwidth and compute requirements for inference. Running LLMs on CPU-only hardware typically relies on quantized model weights and optimized inference engines like llama.cpp, trading raw speed for accessibility and avoiding the need for expensive GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/google/gemma-4-26B-A4B/blob/main/README.md">README.md · google/ gemma - 4 - 26 B -A 4 B at main</a></li>
<li><a href="https://insiderllm.com/guides/cpu-only-llms-what-actually-works/">CPU-Only LLMs: What Actually Works | InsiderLLM</a></li>
<li><a href="https://www.baseten.co/blog/comparing-tokens-per-second-across-llms/">Comparing tokens per second across LLMs</a></li>

</ul>
</details>

**Discussion**: The community engaged in rigorous cost-benefit analysis: multiple commenters (hagen8, Aurornis) calculated that electricity costs for a 300–500W Xeon server make local inference 10–30× more expensive per token than cloud APIs, even when cloud prices match local costs per million tokens. Optimists like dwa3592 predict >200B MoE models running on basic consumer hardware by mid-2027, citing their own experience running Qwen 35B-A3B at 7–9 t/s on a 16GB MacBook Air. Several commenters shared alternative benchmarks, with throwaway2027 reporting 8–12 t/s on similar old hardware and hparadiz publishing detailed gist benchmarks on a dual Xeon with 256GB DDR4.

**Tags**: `#local-llm`, `#hardware-benchmarks`, `#cost-analysis`, `#inference-optimization`, `#hacker-news`

---

<a id="item-7"></a>
## [Show HN: misa77 - a codec that decodes 2x faster than LZ4 (at better ratios)](https://github.com/welcome-to-the-sunny-side/misa77) ⭐️ 7.0/10

Show HN for misa77, an experimental compression codec claiming 2x faster decompression than LZ4 with better ratios, at the cost of much slower encoding.

hackernews · nonadhocproblem · Jul 15, 15:58 · [Discussion](https://news.ycombinator.com/item?id=48922838)

**Tags**: `#compression`, `#lz4`, `#performance`, `#systems`, `#optimization`

---

<a id="item-8"></a>
## [Sleep regularity is a stronger predictor of mortality risk than sleep duration (2023)](https://academic.oup.com/sleep/article/47/1/zsad253/7280269) ⭐️ 7.0/10

A 2023 peer-reviewed study finds that consistent sleep regularity is a stronger predictor of all-cause mortality risk than total sleep duration, based on accelerometer data from a large cohort.

hackernews · bilsbie · Jul 15, 11:46 · [Discussion](https://news.ycombinator.com/item?id=48919363)

**Tags**: `#health`, `#sleep-research`, `#epidemiology`, `#longevity`, `#public-health`

---

<a id="item-9"></a>
## [OpenAI Unveils GPT-Red: Self-Play Automated Red Teaming for AI Safety](https://openai.com/index/unlocking-self-improvement-gpt-red) ⭐️ 7.0/10

OpenAI has introduced GPT-Red, an automated red teaming system that uses self-play reinforcement learning to simultaneously train an attacking model alongside a diverse collection of defender LLMs across a broad set of red-teaming scenarios. The system is designed to enhance AI safety, alignment, and resilience against prompt injection attacks. Automated red teaming addresses a critical scaling bottleneck in AI safety: human-led adversarial testing cannot keep pace with the rapid deployment of new models and applications. By having models attack and defend against each other autonomously, GPT-Red could significantly accelerate vulnerability discovery and hardening, benefiting the broader AI ecosystem and downstream developers who rely on more robust foundation models. GPT-Red is built on self-play reinforcement learning, where the red-teaming attacker model and multiple defender LLMs co-evolve through adversarial training rather than relying on static, human-curated attack datasets. Related academic work, such as Safety Self-Play (SSP), demonstrates that a single LLM can simultaneously serve as both attacker and defender within a unified RL loop, dynamically evolving attack strategies while strengthening defenses—a paradigm that may inform GPT-Red's design.

rss · OpenAI Blog · Jul 15, 10:00

**Background**: Red teaming is a structured adversarial testing methodology borrowed from cybersecurity, used to probe AI systems for unsafe behaviors, vulnerabilities, and failure modes. Prompt injection is a specific attack vector where adversaries craft inputs designed to override a model's instructions and cause unintended behavior, exploiting the fact that LLMs do not clearly separate developer instructions from user inputs. Self-play, a technique famously used in game-playing AI like AlphaGo, has recently been adapted to the safety domain by having models play both adversarial and defensive roles to iteratively improve robustness without requiring large amounts of human-generated adversarial examples.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/unlocking-self-improvement-gpt-red/">GPT-Red: Unlocking Self-Improvement for Robustness | OpenAI</a></li>
<li><a href="https://arxiv.org/html/2601.10589">Be Your Own Red Teamer: Safety Alignment via Self-Play and Reflective Experience Replay</a></li>
<li><a href="https://en.wikipedia.org/wiki/Prompt_injection">Prompt injection - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#red teaming`, `#OpenAI`, `#alignment`, `#prompt injection`

---

<a id="item-10"></a>
## [AllenAI Shares Engineering Lessons from Building Shippy Agent](https://huggingface.co/blog/allenai/shippy-tech-blog) ⭐️ 7.0/10

AllenAI published a technical deep-dive on HuggingFace Blog detailing the engineering lessons learned while building Shippy, a maritime AI agent on its Skylight ocean-monitoring platform. The core insight is that reliable agents depend less on the model itself and more on deterministic tools, explicit guardrails, isolated infrastructure, and evaluations grounded in real-world workflows and live data. This retrospective offers rare, candid guidance from a respected AI lab about what actually makes production-grade agents reliable, shifting the conversation from model capability to engineering discipline. Practitioners building AI agents for high-stakes domains—such as maritime monitoring, healthcare, or finance—will find actionable patterns around guardrails, evaluation, and infrastructure isolation. Shippy is designed for high-stakes maritime decisions where incorrect answers carry real consequences, and it answers plain-language questions from analysts using live vessel tracking data. The blog emphasizes that showing its work—citing boundary sources, data cutoffs, and query timestamps with deep links back to the Skylight map—is critical for user trust and verifiability.

rss · HuggingFace Blog · Jul 15, 17:29

**Background**: The Allen Institute for AI (Ai2) is a non-profit research institute founded in 2014 by the late Microsoft co-founder Paul Allen, focused on high-impact, open AI research. Shippy is built on Ai2's Skylight platform, a free ocean-monitoring system that tracks vessel activity and maritime boundaries. AI agents are LLM-powered systems that can take autonomous actions or answer complex queries by invoking external tools; building reliable agents remains one of the hardest unsolved problems in applied AI, especially when errors carry real-world consequences.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/blog/allenai/shippy-tech-blog">What building Shippy taught us about building agents</a></li>
<li><a href="https://allenai.org/blog/shippy-deep-dive">What building Shippy taught us about building agents | Ai2</a></li>
<li><a href="https://www.geekwire.com/2026/ai2s-skylight-project-launches-shippy-an-ai-agent-that-dives-into-ocean-data/">Ai2’s Skylight project launches ‘Shippy,’ an AI agent that ...</a></li>

</ul>
</details>

**Tags**: `#AI-agents`, `#engineering`, `#LLM`, `#HuggingFace`, `#lessons-learned`

---

<a id="item-11"></a>
## [Model Routing Is Simple — Until It Isn't](https://huggingface.co/blog/ibm-research/model-routing-is-simple-until-it-isnt) ⭐️ 7.0/10

Hugging Face and IBM Research have published a technical blog post examining the hidden complexities of model routing systems, focusing on challenges that arise when moving beyond trivial implementations to production-grade intelligent model selection in LLM deployments. As enterprises deploy multiple LLMs to balance cost, latency, and quality, model routing becomes critical infrastructure — yet naive routing implementations can silently degrade performance or inflate costs, making this a high-impact topic for production ML engineers and platform architects. The post frames routing as a multi-dimensional optimization problem spanning cost-based, capability-based, latency-based, and semantic routing strategies, and likely discusses router layers, model registries, and fallback logic that production systems must handle beyond simple rule-based dispatch.

rss · HuggingFace Blog · Jul 15, 17:27

**Background**: Model routing refers to dynamically selecting the most suitable LLM for each incoming query based on factors such as task complexity, cost, performance, and latency requirements. As organizations increasingly run compound AI systems — pipelines that chain multiple LLM calls — the choice of which model to invoke at each step has an outsized impact on both quality and operating cost. Research such as the arXiv paper 'Optimizing Model Selection for Compound AI Systems' (2502.14815) has shown that these per-call model decisions have large effects on output quality, but the search space grows exponentially. Open-source projects like LLMRouter and commercial platforms have emerged to provide routing layers with smart selection, fallback handling, and provider ordering.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.14815">Optimizing Model Selection for Compound AI Systems</a></li>
<li><a href="https://www.braintrust.dev/articles/best-llm-routers-2026">Best LLM routers and model routing platforms in 2026</a></li>

</ul>
</details>

**Tags**: `#model-routing`, `#llm-infrastructure`, `#production-ml`, `#cost-optimization`, `#huggingface`

---

<a id="item-12"></a>
## [HuggingFace Launches Real World VoiceEQ Benchmark for Voice AI](https://huggingface.co/blog/real-world-voiceeq) ⭐️ 7.0/10

HuggingFace has introduced Real World VoiceEQ, a benchmark designed to evaluate the human quality of voice AI systems in real-world conditions, built from over 1 million individual human ratings collected across different demographics, speaking styles, and acoustic environments. This benchmark addresses a recognized gap in voice AI evaluation, where traditional technical metrics often fail to capture whether a system actually sounds natural, conveys appropriate emotion, or meets real user expectations — critical factors as voice AI is increasingly deployed in production applications. The current benchmark includes 785,000 TTS (text-to-speech) ratings and 48,000 STS (speech-to-speech) ratings, making it one of the largest human evaluations of voice AI to date. It assesses qualities that transcripts alone cannot capture, such as tone, emotion, speaker identity, and background noise handling.

rss · HuggingFace Blog · Jul 15, 00:00

**Background**: Voice AI systems are typically evaluated using technical metrics such as Word Error Rate (WER) for speech recognition or Mean Opinion Score (MOS) for synthesis quality. However, researchers have increasingly noted that these metrics are flawed and cannot fully capture how natural or effective a voice AI system sounds in practice. Real World VoiceEQ shifts the evaluation paradigm from purely technical accuracy toward human-centered quality dimensions, incorporating demographic diversity and varied acoustic environments that better reflect deployment scenarios.

<details><summary>References</summary>
<ul>
<li><a href="https://www.hume.ai/blog/introducing-real-world-voiceeq-measuring-the-human-quality-of-voice-ai">Introducing Real World VoiceEQ: Measuring the Human Quality ...</a></li>
<li><a href="https://github.com/huggingface/blog/blob/main/real-world-voiceeq.md">blog/real-world-voiceeq.md at main · huggingface/blog · GitHub</a></li>
<li><a href="https://www.zal-group.com/news/product-model-releases/hugging-face-real-world-voiceeq-voice-ai-benchmark">Hugging Face Launches Real World VoiceEQ Benchmark for Voice AI</a></li>

</ul>
</details>

**Tags**: `#voice-ai`, `#evaluation`, `#huggingface`, `#benchmark`, `#speech-synthesis`

---

<a id="item-13"></a>
## [Tencent Releases RxBrain: A Unified Multimodal Model for Embodied AI](https://www.reddit.com/r/LocalLLaMA/comments/1ux0x0v/tencenthyembodiedrxbrain10_hugging_face/) ⭐️ 7.0/10

Tencent has released RxBrain (Hy-Embodied-RxBrain-1.0), a ~6.2B-parameter Mixture-of-Transformers model that unifies language reasoning and visual imagination within a single autoregressive sequence for embodied AI tasks including world state prediction and subgoal planning. By interleaving text reasoning with flow-matched imagined frames in one model, RxBrain offers a novel architectural approach for embodied AI, potentially reducing the need for separate vision and language towers and enabling tighter coupling between symbolic planning and visual goal prediction for robotics applications. The model uses a Mixture-of-Transformers (MoT) backbone with modality-specific pathways for text, vision, and generation. Imagined frames are decoded by a flow-matching head into a frozen FLUX VAE latent space, and a learned <Image> token within the autoregressive sequence decides when to produce visual content versus textual reasoning.

reddit · r/LocalLLaMA · /u/jacek2023 · Jul 15, 09:30

**Background**: Mixture-of-Transformers (MoT) is a sparse multi-modal transformer architecture introduced to address the scaling challenges of training unified models across text, image, and speech modalities. Flow matching is a generative modeling paradigm that combines aspects of Continuous Normalizing Flows and diffusion models, offering faster sampling and simpler training. Interleaved text-image autoregressive generation, exemplified by models like Chameleon, Anole, and Orthus, enables a single model to produce both discrete text tokens and continuous image features in sequence. RxBrain extends these ideas to embodied AI by coupling symbolic subgoal plans with visually predicted goal frames.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2411.04996">Mixture-of-Transformers: A Sparse and Scalable Architecture ... Mixture-of-Transformers: A Sparse and Scalable Architec ... Mixture of Experts Explained - Hugging Face Transformers vs Mixture of Experts: What’s the Real Difference? Transformer vs. Mixture of Experts in LLMs - by Avi Chawla Mixture of Experts Architecture in Transformer Models</a></li>
<li><a href="https://arxiv.org/abs/2210.02747">[2210.02747] Flow Matching for Generative Modeling - arXiv.org An introduction to Flow Matching · Cambridge MLG Blog Flow matching for generative modelling in bioinformatics and ... Understanding Flow Matching Generative Modeling with Continuous Flows: Sample Complexity ... Flow matching meets biology and life science: a survey</a></li>
<li><a href="https://arxiv.org/abs/2412.00127">[2412.00127] Orthus: Autoregressive Interleaved Image-Text ...</a></li>

</ul>
</details>

**Tags**: `#multimodal`, `#embodied-ai`, `#tencent`, `#world-models`, `#robotics`

---

<a id="item-14"></a>
## [Transformers v5.14.0 Adds Thinking Machines' 975B Inkling Multimodal Model](https://github.com/huggingface/transformers/releases/tag/v5.14.0) ⭐️ 6.0/10

Hugging Face Transformers v5.14.0 has been released, adding support for Inkling, a 975B-parameter (41B active) multimodal MoE model from Thinking Machines Lab that handles text, image, and audio inputs and is released with open weights. The release also includes TIPSv2 and TIPSv2 DPT models, breaking changes to GPTNeoX and GPTBigCode for vLLM compatibility, kernel performance improvements (SDPA prefill with FlashAttention up to 260% faster), and new Multi-Token Prediction decoding support. This is significant because Inkling is Thinking Machines Lab's first in-house AI model, founded by former OpenAI CTO Mira Murati, and its inclusion in Transformers makes a high-profile open-weights multimodal model immediately accessible to the broader developer ecosystem for fine-tuning and integration. The release also delivers meaningful inference speedups (FlashAttention prefill gains) and expands speculative decoding capabilities, benefiting anyone deploying large models in production. Inkling uses a Mixture of Experts (MoE) architecture where only 41B of its 975B total parameters are active per token, giving it the representational capacity of a large model at the compute cost of a much smaller dense model. Thinking Machines positions Inkling not as the strongest overall model but as a flexible open-weights base for customization, available on their Tinker platform for fine-tuning; the Transformers integration was contributed by molbap, Cyrilvallez, eustlb, and zucchini-nlp.

github · ArthurZucker · Jul 15, 19:02

**Background**: Hugging Face Transformers is the most widely used open-source library for state-of-the-art machine learning models across text, vision, audio, and multimodal tasks, supporting both inference and training. Mixture of Experts (MoE) is an architecture that decouples total model capacity from active compute per token—for example, a 975B-parameter MoE may activate only ~41B parameters per token, enabling frontier-scale capability at lower inference cost. Thinking Machines Lab is an AI startup founded by former OpenAI CTO Mira Murati, and Inkling is their first open-weight model release, designed for developers building AI applications including agentic systems, coding assistants, chatbots, and RAG pipelines.

<details><summary>References</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/introducing-inkling/">Inkling: Our open-weights model - Thinking Machines Lab</a></li>
<li><a href="https://techcrunch.com/2026/07/15/thinking-machines-amps-up-its-bet-against-one-size-fits-all-ai-with-its-first-open-model-inkling/">Thinking Machines amps up its bet against one-size-fits-all ...</a></li>
<li><a href="https://huggingface.co/docs/transformers/index">Transformers · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#huggingface`, `#transformers`, `#multimodal-model`, `#open-weights`, `#model-release`

---

<a id="item-15"></a>
## [Mysteries of Telegram Data Centers (2022)](https://dev.moe/en/3025) ⭐️ 6.0/10

A technical exploration of how Telegram organizes and assigns users to its data centers geographically, revealing patterns in DC distribution and regional service.

hackernews · theanonymousone · Jul 15, 13:22 · [Discussion](https://news.ycombinator.com/item?id=48920475)

**Tags**: `#telegram`, `#infrastructure`, `#data-centers`, `#distributed-systems`, `#networking`

---

<a id="item-16"></a>
## [Google is updating Gemma 4's chat templates, bringing major fixes to tool calling and reducing "laziness", and enabling Flash Attention 4 on Hopper GPUs, plus an interactive guide on how to work with and improve its vision!](https://www.reddit.com/r/LocalLLaMA/comments/1uxfu4k/google_is_updating_gemma_4s_chat_templates/) ⭐️ 6.0/10

Google announces updates to Gemma 4's chat templates, fixing tool calling issues, reducing model laziness, enabling Flash Attention 4 on Hopper GPUs, and releasing an interactive vision token budget guide.

reddit · r/LocalLLaMA · /u/Iwaku_Real · Jul 15, 19:26

**Tags**: `#Gemma`, `#Google`, `#LLM`, `#Flash Attention`, `#tool-calling`

---

<a id="item-17"></a>
## [German AI consortium releases Soofi S, an open 30B model that tops benchmarks in both English and German](https://www.reddit.com/r/LocalLLaMA/comments/1uxao7y/german_ai_consortium_releases_soofi_s_an_open_30b/) ⭐️ 6.0/10

A German AI consortium releases Soofi S, an open 30B parameter language model that achieves top benchmark scores in both English and German.

reddit · r/LocalLLaMA · /u/yogthos · Jul 15, 16:21

**Tags**: `#open-source`, `#LLM`, `#multilingual`, `#German-AI`, `#model-release`

---

<a id="item-18"></a>
## [Apple in Talks with PrismML to Shrink AI Models for iPhones](https://www.reddit.com/r/LocalLLaMA/comments/1ux4cn2/apple_in_talks_with_startup_prismml_that_shrinks/) ⭐️ 6.0/10

Apple is reportedly in early-stage talks with PrismML, a Caltech spinout startup, to evaluate its AI model compression technology that can shrink large models to run directly on an iPhone using up to 15x less memory. This signals Apple's deepening commitment to on-device AI as a strategic differentiator, potentially reducing dependence on cloud-based inference and rivaling Google's and Samsung's edge-AI efforts. For the local LLM community, it validates the growing market demand for compressed, consumer-device-runnable models. PrismML's technology has reportedly compressed a 27-billion parameter model to run on an iPhone, and in one demonstration shrunk a 54 GB model to under 4 GB. The talks are described as early-stage, meaning no acquisition or partnership has been confirmed, and the specific compression methods (e.g., quantization, pruning, or distillation) have not been publicly disclosed in detail.

reddit · r/LocalLLaMA · /u/Ready_Performance_35 · Jul 15, 12:23

**Background**: AI model compression encompasses techniques such as quantization (reducing numerical precision of model weights), pruning (removing redundant connections), and knowledge distillation (training a smaller model to mimic a larger one). On-device AI, also called edge inference, runs models directly on phones or IoT devices rather than remote servers, offering benefits in latency, privacy, and offline availability. PrismML is one of several startups—including competitors like OctoML and Deeplite—pursuing aggressive compression ratios to make billion-parameter LLMs feasible on consumer hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/07/14/apple-prismml-ai-compression-iphone.html">Apple in talks with startup that shrinks AI models to run on ...</a></li>
<li><a href="https://thenextweb.com/news/apple-prismml-on-device-ai-compression-iphone">Apple eyes PrismML’s on-device AI for the iPhone - TNW</a></li>
<li><a href="https://cryptobriefing.com/apple-prismml-ai-model-compression-iphone/">Apple in talks with PrismML to shrink AI models for iPhone ...</a></li>

</ul>
</details>

**Tags**: `#Apple`, `#model-compression`, `#on-device-AI`, `#PrismML`, `#edge-AI`

---