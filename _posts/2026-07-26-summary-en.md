---
layout: default
title: "Horizon Summary: 2026-07-26 (EN)"
date: 2026-07-26
lang: en
---

> From 41 items, 8 important content pieces were selected

---

1. [vLLM v0.26.0 Released with Inkling Support and DeepSeek-V4 Optimizations](#item-1) ⭐️ 7.0/10
2. [Inside the Relay Market Fueling LLM Token Reseller Fraud](#item-2) ⭐️ 7.0/10
3. [Kill The Cookie Banner](#item-3) ⭐️ 7.0/10
4. [GrapheneOS Clarifies Locked-Device Forensic Protections](#item-4) ⭐️ 7.0/10
5. [一年从3B卷到0.xB：MonkeyOCRv2用0.7B拿下17语种文档解析开源第一](#item-5) ⭐️ 6.0/10
6. [YOLO26n Inference Implemented from Scratch in ARM64 Assembly on Raspberry Pi 4](#item-6) ⭐️ 6.0/10
7. [Open-weight 4B models approach o3-level medical question answering in Swedish (P)](#item-7) ⭐️ 6.0/10
8. [We compared different LLMs on IMO 2026 (R)](#item-8) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.26.0 Released with Inkling Support and DeepSeek-V4 Optimizations](https://github.com/vllm-project/vllm/releases/tag/v0.26.0) ⭐️ 7.0/10

vLLM v0.26.0 has been released with 411 commits from 212 contributors, introducing full support for the new Inkling model family (including base modeling, piecewise CUDA graphs, MTP=1 speculative decoding, LoRA, and ModelOpt NVFP4 quantization), cross-vendor DeepSeek-V4 performance optimizations on CUDA/ROCm/XPU, and a new fp32 lm_head option via `head_dtype` to improve generation accuracy. vLLM is one of the most widely deployed open-source LLM inference engines, and this release broadens its hardware coverage and model ecosystem at a time when serving large MoE models like DeepSeek-V4 in production is increasingly common. The Inkling full-stack support and per-KV-cache-group attention backend selection also signal vLLM's continued evolution toward flexible, hybrid-model serving. DeepSeek-V4 optimizations include a specialized routing kernel yielding 2.94% E2E TPOT improvement, a `fused_topk_bias` kernel running 1.5–2x faster, and redundant repeat/copy removal giving 1.8% E2E TPOT gains; the fp32 `lm_head` path also extends to LoRA and gains a ROCm `torch.mm` fast path. Attention backends can now be selected per KV-cache group, and sliding-window support is exposed as an explicit backend capability to better serve hybrid attention models.

github · khluu · Jul 25, 10:38

**Background**: vLLM is a high-throughput LLM serving system that uses techniques like PagedAttention and speculative decoding to optimize inference. Speculative decoding methods such as MTP (Multi-Token Prediction) allow a model to predict multiple future tokens with a lightweight drafter that the heavy target model then verifies, reducing overall latency. E2E TPOT (Time Per Output Token) is a key inference latency metric that measures how quickly each generated token is produced during the decoding phase, complementing metrics like time-to-first-token (TTFT). NVFP4 is NVIDIA's 4-bit floating-point quantization format, typically applied via the ModelOpt library to shrink model memory footprint while preserving accuracy for inference.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.vllm.ai/en/latest/features/quantization/modelopt/">NVIDIA Model Optimizer - vLLM</a></li>
<li><a href="https://docs.vllm.ai/en/latest/features/speculative_decoding/mtp/">MTP (Multi-Token Prediction) - vLLM</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#deepseek`, `#model-serving`, `#release-notes`

---

<a id="item-2"></a>
## [Inside the Relay Market Fueling LLM Token Reseller Fraud](https://vectoral.com/blog/token-relay-market) ⭐️ 7.0/10

Vectoral published an in-depth investigation into a gray-market ecosystem of AI token relay services that resell access to OpenAI, Anthropic, and Google APIs at 94–98% discounts by aggregating stolen, leaked, or fraudulently obtained API keys, free-trial abuse, and startup-program credit exploitation. The report maps a four-layer supply chain spanning virtual card merchants, account farmers, relay operators, and end resellers, and primarily targets mainland-China-based B2B traffic. This fraud ecosystem directly threatens the unit economics of frontier AI providers by undercutting legitimate API pricing, and it distorts competitive dynamics for startups who pay full price while rivals piggyback on stolen or subsidized capacity. It also signals that AI infrastructure is now attracting the same kind of sophisticated billing-abuse actors that historically plagued digital advertising. The investigation identifies a four-layer supply chain (virtual card merchants → account farmers → relay operators → resellers) and specific abuse vectors including fake-credit-card chargebacks, mass free-trial abuse, and AWS/Azure startup-credit programs. A commenter cited an Indian company purchasing inference at just 4% of list price by repeatedly registering entities to harvest fresh cloud credits.

hackernews · mlenhard · Jul 26, 15:17 · [Discussion](https://news.ycombinator.com/item?id=49058993)

**Background**: Frontier AI providers like OpenAI, Anthropic, and Google sell access to their models via metered APIs priced per million tokens. To stimulate the developer ecosystem, cloud providers (AWS, Azure, Google Cloud) and model vendors offer startup-credit programs that grant free or heavily discounted inference to eligible new companies. These programs, combined with free-tier trials and account sign-up bonuses, create the raw material that reseller fraudsters aggregate and relay at steep discounts to buyers willing to look the other way on provenance.

<details><summary>References</summary>
<ul>
<li><a href="https://vectoral.com/blog/token-relay-market">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>
<li><a href="https://simonwillison.net/2026/Jul/26/relay-market/">An Inside Look at the Relay Market Powering Token Resellers ...</a></li>
<li><a href="https://vectoral.com/">Vectoral — Catch the proxies reselling your LLM tokens | Vectoral</a></li>

</ul>
</details>

**Discussion**: Commenters broadly confirm the investigation's findings and place them in historical context. A former financial-integrity engineer at a large ads company notes this mirrors the sophisticated impression-resale markets that plagued digital advertising for years. Others add concrete examples: a friend paying 4% of list via AWS startup credit abuse, Chinese affiliate sites pushing suspicious free-token offers, and analogies to ticket touting. One commenter draws a useful moral line between outright fraud (fake cards, chargebacks), gray-area free-trial abuse, and legitimate subscription resale.

**Tags**: `#ai-economics`, `#fraud`, `#api-pricing`, `#security`, `#cloud-credits`

---

<a id="item-3"></a>
## [Kill The Cookie Banner](https://killthecookiebanner.eu/) ⭐️ 7.0/10

EU Commission proposes a browser-level privacy preference system to eliminate annoying cookie banners, set to take effect by 2027.

hackernews · rapnie · Jul 26, 11:53 · [Discussion](https://news.ycombinator.com/item?id=49057175)

**Tags**: `#privacy`, `#regulation`, `#eu-policy`, `#web-development`, `#cookies`

---

<a id="item-4"></a>
## [GrapheneOS Clarifies Locked-Device Forensic Protections](https://discuss.grapheneos.org/d/40700-grapheneos-protections-against-data-extraction-from-locked-devices) ⭐️ 7.0/10

GrapheneOS community members clarified the operating system's protections against forensic data extraction from locked devices, emphasizing its 18-hour auto-reboot feature that forces devices into Before First Unlock (BFU) mode, where encryption keys cannot be extracted. The discussion was prompted by a US prosecution case and a recent article on how GrapheneOS helped a journalist protect confidential sources. This matters because forensic data extraction from seized devices is a real threat to journalists, activists, travelers at borders, and anyone facing device confiscation, making automatic BFU transitions a critical defensive feature. The discussion also surfaces a key usability-security trade-off: GrapheneOS's protections can be undermined by weak lock methods like pattern unlock, which provide very low entropy. The 18-hour auto-reboot ensures that even if a device sits unused, it transitions to BFU mode where file-based encryption keys remain inaccessible to forensic tools. However, community analysis shows that Android's pattern lock only provides approximately 18.57 bits of entropy — less than three random characters or four lowercase letters — making the choice of lock method a critical factor in overall security.

hackernews · Cider9986 · Jul 26, 05:57 · [Discussion](https://news.ycombinator.com/item?id=49055169)

**Background**: GrapheneOS is an open-source, privacy-focused mobile operating system built on the Android Open Source Project (AOSP), available primarily on Google Pixel devices. Modern Android and iOS devices use file-based encryption (FBE), which keeps data encrypted until the user unlocks the device. Mobile forensics distinguishes two device states: Before First Unlock (BFU), where the device has been powered off or rebooted and not yet unlocked, making encryption keys inaccessible; and After First Unlock (AFU), where keys are in memory and significantly more data can be extracted.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GrapheneOS">GrapheneOS - Wikipedia</a></li>
<li><a href="https://blogs.dsu.edu/digforce/2023/08/23/bfu-and-afu-lock-states/">BFU and AFU Lock States – Blog | DigForCE Lab - DSU</a></li>
<li><a href="https://teeltechcanada.com/understanding-mobile-device-lock-states-in-forensic-extractions/">Understanding Mobile Device Lock States in Forensic ...</a></li>

</ul>
</details>

**Discussion**: Community sentiment is broadly supportive of GrapheneOS's approach, with users praising the 18-hour auto-reboot as a meaningful protection against forced extraction. Constructive criticism focused on the lack of a complete backup/restore solution for preventive wiping before border crossings, and on the low entropy of Android's pattern lock compared to alphanumeric passwords. One commenter noted the irony that seeking security comparable to Apple's Lockdown Mode is often treated with suspicion, while another celebrated the existence of hardware that does not work against its user.

**Tags**: `#security`, `#privacy`, `#grapheneos`, `#mobile-security`, `#forensics`

---

<a id="item-5"></a>
## [一年从3B卷到0.xB：MonkeyOCRv2用0.7B拿下17语种文档解析开源第一](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247907283&idx=2&sn=5df8a52712c79f67232ca9672d4cc34e) ⭐️ 6.0/10

MonkeyOCRv2 achieves state-of-the-art open-source document parsing across 17 languages with only 0.7B parameters, demonstrating that smaller, well-designed models can outperform larger ones.

rss · 量子位 · Jul 26, 04:30

**Tags**: `#document-parsing`, `#OCR`, `#efficient-models`, `#open-source`, `#multilingual`

---

<a id="item-6"></a>
## [YOLO26n Inference Implemented from Scratch in ARM64 Assembly on Raspberry Pi 4](https://www.reddit.com/r/MachineLearning/comments/1v6w394/i_implemented_the_yolo26n_model_inference_from/) ⭐️ 6.0/10

A Bachelor's student implemented the full YOLO26n object detection inference engine from scratch using ARM64 Assembly Language and C (without any ML framework), targeting the Raspberry Pi 4. The implementation covers ARM NEON SIMD vectorization, Winograd convolution, optimized GEMM kernels, cache-aware tiling, custom micro-kernels, operator fusion, and the attention mechanism, along with all YOLO26 building blocks (Conv, C3K2, SPPF, C2PSA, PSA, BottleNeck, Detect). This project offers a rare, deeply educational look at how modern neural network inference engines actually work under the hood, bridging the gap between high-level ML frameworks and low-level hardware optimization. It is particularly relevant for edge-AI deployment, where ARM-based devices dominate and every cycle counts, making it a valuable reference for engineers seeking to squeeze maximum performance out of resource-constrained hardware. The author extracted YOLO26n model parameters and redesigned the memory layout into a custom binary format tailored for the inference pipeline, producing correct detection results; however, actual performance gains were lower than initially expected, highlighting the difficulty of beating well-optimized production frameworks. YOLO26n is a relatively recent Ultralytics model that claims up to 43% faster CPU ONNX inference versus YOLO11n on Intel Xeon hardware.

reddit · r/MachineLearning · /u/Forward_Confusion902 · Jul 26, 06:43

**Background**: YOLO (You Only Look Once) is a family of single-stage object detection models first proposed by Joseph Redmon in 2016, known for real-time detection speeds. YOLO26 is a recent Ultralytics release that introduces further architectural refinements. ARM64 NEON is ARM's Advanced SIMD instruction set extension, allowing a single instruction to operate on multiple data elements in parallel, which is crucial for accelerating matrix and vector operations on ARM CPUs. Winograd convolution is an algorithm that reduces the number of multiplications needed for convolution operations by transforming inputs and filters into a different algebraic domain, commonly used to accelerate CNN inference. Edge AI on devices like the Raspberry Pi 4 (which uses a quad-core ARM Cortex-A72 CPU) demands such low-level optimizations to achieve usable inference latency without GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ultralytics/ultralytics/blob/main/docs/en/models/yolo26.md">ultralytics/docs/en/models/yolo26.md at main · ultralytics ...</a></li>
<li><a href="https://developer.arm.com/documentation/dht0002/latest/Introducing-NEON/What-is-SIMD-/ARM-SIMD-instructions">ARM SIMD instructions - Neon</a></li>
<li><a href="https://arxiv.org/abs/2201.10369">[2201.10369] Winograd Convolution for Deep Neural Networks: Efficient Point Selection</a></li>

</ul>
</details>

**Tags**: `#machine-learning`, `#edge-ai`, `#arm64-assembly`, `#yolo`, `#optimization`, `#computer-vision`

---

<a id="item-7"></a>
## [Open-weight 4B models approach o3-level medical question answering in Swedish (P)](https://www.reddit.com/r/MachineLearning/comments/1v71wds/openweight_4b_models_approach_o3level_medical/) ⭐️ 6.0/10

Experiments show that 4B open-weight models like Qwen3.5-4B can achieve 87% accuracy on Swedish medical licensing exams without post-training, approaching o3's 88%, demonstrating rapid improvement in small model capabilities.

reddit · r/MachineLearning · /u/AccomplishedCat4770 · Jul 26, 11:58

**Tags**: `#LLMs`, `#open-weight-models`, `#medical-AI`, `#fine-tuning`, `#benchmarking`

---

<a id="item-8"></a>
## [We compared different LLMs on IMO 2026 (R)](https://www.reddit.com/r/MachineLearning/comments/1v6wskz/we_compared_different_llms_on_imo_2026_r/) ⭐️ 6.0/10

A comparison of frontier, commercial, and open-weight LLMs on IMO 2026 problems showing that harness/orchestration engineering substantially improves performance, with frontier models (sol, fable) achieving near-perfect scores while the authors' AutoFyn multi-agent harness helps close the gap for Claude and GLM.

reddit · r/MachineLearning · /u/pequalnp92 · Jul 26, 07:21

**Tags**: `#LLM-benchmark`, `#math-reasoning`, `#model-evaluation`, `#harness-engineering`, `#multi-agent-systems`

---