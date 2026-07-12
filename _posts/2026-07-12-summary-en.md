---
layout: default
title: "Horizon Summary: 2026-07-12 (EN)"
date: 2026-07-12
lang: en
---

> From 40 items, 16 important content pieces were selected

---

1. [vLLM v0.25.0 Released: MRv2 Default, Legacy PagedAttention Removed](#item-1) ⭐️ 8.0/10
2. [Study: Claude Code Has 33k Token Overhead vs OpenCode's 7k](#item-2) ⭐️ 7.0/10
3. [Old and new apps, via modern coding agents](#item-3) ⭐️ 7.0/10
4. [George Hotz: Frontier Labs Can't Capture LLM Value](#item-4) ⭐️ 7.0/10
5. [The shingles vaccine may reduce the risk of dementia](#item-5) ⭐️ 7.0/10
6. [DeepSeek Reportedly Developing Its Own AI Chip to Reduce US Dependency](#item-6) ⭐️ 7.0/10
7. [I mapped Anthropic’s J-Space Hallucination signal across 7 datasets on Qwen3-4B to find out where it works and where it breaks](#item-7) ⭐️ 7.0/10
8. [Ghostel: A New Emacs Terminal Emulator Powered by libghostty](#item-8) ⭐️ 6.0/10
9. [MLX Port of Hunyuan3D Runs Image-to-3D Locally on Apple Silicon](#item-9) ⭐️ 6.0/10
10. [Moondream 3.1: 9B MoE Vision Language Model Released](#item-10) ⭐️ 6.0/10
11. [Apple sues OpenAI alleging trade secret theft, says scheme was 'at every level'](#item-11) ⭐️ 6.0/10
12. [Xiaomi quietly uploads MiMo-V2.5-DFlash weights to Hugging Face](#item-12) ⭐️ 6.0/10
13. [Three-line fix resolves years-old fp16 precision bug on Tesla P100 in llama.cpp](#item-13) ⭐️ 6.0/10
14. [Voodoo Quant Claims 95% KLD Improvement Over Unsloth Dynamic 2.0](#item-14) ⭐️ 6.0/10
15. [Interactive Jacobian-Lens Tool Brings Anthropic's Interpretability to GGUF Models](#item-15) ⭐️ 6.0/10
16. [Zer0Fit: A Local MCP Server Wrapping Google's TabFM and TimesFM for Zero-Shot ML](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0 Released: MRv2 Default, Legacy PagedAttention Removed](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 ships as a major release containing 558 commits from 232 contributors, with Model Runner V2 (MRv2) becoming the default execution path for all dense models, the legacy PagedAttention implementation being removed entirely, and the Transformers modeling backend achieving parity with native vLLM performance. This release signals a decisive architectural transition for one of the most widely deployed open-source LLM serving frameworks: removing the foundational PagedAttention code path and making MRv2 universal consolidates the codebase and unlocks higher throughput, while Transformers parity dramatically lowers the barrier for users who depend on Hugging Face ecosystem integrations for production inference. MRv2 brings support for EVS, realtime embeddings, prefix caching for Mamba hybrid models, multimodal-prefix bidirectional attention, and dynamic speculative decoding with full CUDA graph compatibility. New speculative decoding includes universal heterogeneous-vocabulary TLI support plus DSpark and DFlash drafters, while the Rust frontend matures with HTTPS/mTLS and a DP supervisor for distributed serving.

github · khluu · Jul 11, 20:06

**Background**: vLLM is an open-source high-throughput LLM inference and serving engine originally built around PagedAttention, a memory management technique inspired by OS virtual-memory paging that virtualizes the KV cache to drastically reduce fragmentation and improve serving throughput. Model Runner V2 is a redesigned execution engine that succeeded the V1 runner and unlocks better hardware utilization across architectures such as GB200, H100, and A100. Speculative decoding accelerates inference by having a smaller draft model generate candidate tokens that the larger target model verifies in parallel, and frameworks like vLLM expose configurable drafters (e.g., DFlash, DSpark, Medusa-style heads) to improve tokens-per-second without changing output distributions.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2309.06180">[2309.06180] Efficient Memory Management for Large Language...</a></li>
<li><a href="https://www.spheron.network/blog/vllm-model-runner-v2-mrv2-deployment-guide/">vLLM Model Runner V 2 on GPU Cloud: Deploy MRV 2 for Faster LLM...</a></li>
<li><a href="https://www.alphaxiv.org/abs/2607.05147">DSpark: Confidence-Scheduled Speculative Decoding with... | alphaXiv</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#model-serving`, `#paged-attention`, `#release-notes`

---

<a id="item-2"></a>
## [Study: Claude Code Has 33k Token Overhead vs OpenCode's 7k](https://systima.ai/blog/claude-code-vs-opencode-token-overhead) ⭐️ 7.0/10

An empirical study by Systima added logging between Anthropic's API and two agentic coding tools (Claude Code and OpenCode), finding that Claude Code sends approximately 33,000 tokens of overhead before processing a user prompt, compared to roughly 7,000 tokens for OpenCode. For developers paying per-token, a nearly 5x difference in fixed overhead per request translates to significant cost differences, and the findings raise questions about whether the overhead is justified by cache-hit savings or driven by vendor pricing incentives that push users toward subscriptions. The study measured only fixed overhead (tokens sent before the user's prompt) and did not measure actual work performed, meaning it cannot determine cost-per-task efficiency. Cache-hit tokens are billed at roughly 1/10th the price of cache-miss tokens, so high overhead may be partially amortized across subsequent turns if cached.

hackernews · systima · Jul 12, 18:25 · [Discussion](https://news.ycombinator.com/item?id=48883275)

**Background**: Claude Code is Anthropic's proprietary agentic coding CLI, while OpenCode is an open-source alternative (with over 160k GitHub stars) that can connect to various model providers including Anthropic. Both tools send system prompts, tool definitions, and agent instructions to the LLM before the user's actual request, and this fixed payload is called 'token overhead.' Prompt caching is a technique where frequently reused prompt prefixes (like system instructions) are stored and re-served at reduced cost, which can make large overheads more economical if the same prefix recurs across turns.

<details><summary>References</summary>
<ul>
<li><a href="https://claude.com/product/claude-code">Claude Code by Anthropic | AI Coding Agent , Terminal, IDE</a></li>
<li><a href="https://opencode.ai/">OpenCode | The open source AI coding agent</a></li>
<li><a href="https://www.ibm.com/think/topics/prompt-caching">What is Prompt Caching? | IBM</a></li>

</ul>
</details>

**Discussion**: Commenters raised several key points: sub-agents dramatically inflate token usage (one user reported 7 sub-agents burning through a budget instantly), some suspected Anthropic deliberately inflates overhead to push users toward subscriptions, others argued cache-hit pricing (1/10 cost) may justify the overhead, and the study's author acknowledged via UPDATE that comparing fixed costs without measuring actual work is misleading, promising more thorough follow-up tests.

**Tags**: `#claude-code`, `#opencode`, `#token-optimization`, `#ai-coding-agents`, `#anthropic`

---

<a id="item-3"></a>
## [Old and new apps, via modern coding agents](https://terrytao.wordpress.com/2026/07/11/old-and-new-apps-via-modern-coding-agents/) ⭐️ 7.0/10

Terry Tao discusses his experience using modern LLM coding agents to build supplementary apps and visualizations for mathematical work, offering a balanced view on their utility.

hackernews · subset · Jul 12, 11:09 · [Discussion](https://news.ycombinator.com/item?id=48880170)

**Tags**: `#AI`, `#LLM-coding-agents`, `#Terry-Tao`, `#mathematics`, `#software-tools`

---

<a id="item-4"></a>
## [George Hotz: Frontier Labs Can't Capture LLM Value](https://geohot.github.io//blog/jekyll/update/2026/07/12/i-love-llms.html) ⭐️ 7.0/10

In a blog post titled "I love LLMs, I hate hype," George Hotz (geohot) argues that frontier AI labs will fail to capture the economic value that large language models create, even as the technology itself dramatically boosts personal productivity through easily customizable open-source forks. This contrarian analysis challenges the prevailing AI investment narrative by separating the genuine technical usefulness of LLMs from the questionable business prospects of frontier labs, which matters for investors, developers, and anyone evaluating AI's real-world impact versus market hype. Hotz highlights a shift toward a "have it your way" era where individual developers fork or modify open-source projects rather than upstreaming changes, raising concerns about open-source sustainability. Commenters also note that current LLM costs remain heavily subsidized, leaving uncertainty about long-term affordability and local inference viability.

hackernews · therepanic · Jul 12, 18:31 · [Discussion](https://news.ycombinator.com/item?id=48883343)

**Background**: George Hotz, known online as geohot, is a prominent American security hacker and entrepreneur who first gained fame for jailbreaking the iPhone and reverse-engineering the PlayStation 3. He later founded Comma.ai, an autonomous driving company. "Frontier AI labs" refers to the leading organizations building the most advanced AI models, commonly identified in 2026 as OpenAI, Anthropic, Google DeepMind, Meta, and xAI. In open-source software, a "fork" is a new codebase created by copying and independently modifying an existing project, which can fragment community contributions if maintained separately from the original.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/George_Hotz">George Hotz - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Fork_(software_development)">Fork ( software development ) - Wikipedia</a></li>
<li><a href="https://blog.magmalabs.io/2026/05/29/who-are-the-big-5-in-ai-a-2026-field-guide-for-tech-leaders.html">Who Are the Big 5 in AI ? A 2026 Field Guide for Tech Leaders - The...</a></li>

</ul>
</details>

**Discussion**: Commenters largely agree with Hotz's central thesis that frontier labs will struggle to capture the value LLMs create, with several sharing personal anecdotes of dramatic productivity gains from running models on home servers and forking open-source projects for bespoke needs. The discussion surfaces a tension between enthusiasm for LLM capabilities and concerns about subsidized pricing sustainability, code quality, and the erosion of traditional open-source collaboration norms.

**Tags**: `#AI`, `#LLMs`, `#open-source`, `#tech-economics`, `#frontier-labs`

---

<a id="item-5"></a>
## [The shingles vaccine may reduce the risk of dementia](https://www.economist.com/leaders/2026/07/09/a-no-brainer-for-protecting-your-brain) ⭐️ 7.0/10

Replicated observational studies suggest the shingles vaccine significantly reduces dementia risk, though community discussion raises important concerns about confounding from reduced hospital visits.

hackernews · saikatsg · Jul 12, 15:23 · [Discussion](https://news.ycombinator.com/item?id=48881874)

**Tags**: `#health`, `#dementia`, `#vaccines`, `#epidemiology`, `#neuroscience`

---

<a id="item-6"></a>
## [DeepSeek Reportedly Developing Its Own AI Chip to Reduce US Dependency](https://www.reddit.com/r/LocalLLaMA/comments/1uu15mz/chinas_deepseek_developing_its_own_ai_chip/) ⭐️ 7.0/10

Chinese AI company DeepSeek is reportedly developing its own AI chip to reduce reliance on US semiconductor technology amid ongoing export restrictions. The move signals a significant step toward hardware self-sufficiency for one of China's most prominent AI startups. DeepSeek's effort to build proprietary AI silicon could reshape the competitive landscape of AI hardware, particularly if it succeeds in producing chips capable of training and running frontier models without Nvidia or AMD hardware. It also highlights how US export controls are accelerating China's domestic semiconductor capabilities, with broad geopolitical and supply chain implications. The report indicates DeepSeek's chip effort is driven primarily by geopolitical constraints rather than purely commercial considerations. Developing competitive AI accelerators requires access to advanced fabrication nodes, which remain a major bottleneck for Chinese firms given restrictions on advanced lithography equipment from companies like ASML and leading-edge foundries like TSMC.

reddit · r/LocalLLaMA · /u/TheRealMasonMac · Jul 12, 01:04

**Background**: DeepSeek, founded in 2023 and headquartered in Hangzhou, rose to global prominence after its R1 model, released in January 2025, was shown to rival leading US models while reportedly being trained at a fraction of the cost. AI accelerators are specialized chips—such as Nvidia's H100 GPU—designed with heterogeneous architectures optimized for the massive parallel computation required by deep learning workloads. Since 2022, the US government has imposed increasingly strict export controls on advanced semiconductors and chipmaking equipment destined for China, aiming to slow the country's progress in frontier AI development. These restrictions have pushed Chinese tech companies to invest heavily in domestic chip design and alternative fabrication pathways.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DeepSeek">DeepSeek - Wikipedia</a></li>
<li><a href="https://www.bbc.com/news/articles/c5yv5976z9po">What is DeepSeek - and why is everyone talking about it?</a></li>
<li><a href="https://stealthcloud.ai/policy/us-export-controls-china/">US Semiconductor Export Controls on China ... — STEALTH CLOUD</a></li>

</ul>
</details>

**Tags**: `#AI hardware`, `#DeepSeek`, `#semiconductors`, `#China tech`, `#export controls`

---

<a id="item-7"></a>
## [I mapped Anthropic’s J-Space Hallucination signal across 7 datasets on Qwen3-4B to find out where it works and where it breaks](https://www.reddit.com/r/LocalLLaMA/comments/1uu61wb/i_mapped_anthropics_jspace_hallucination_signal/) ⭐️ 7.0/10

A rigorous empirical evaluation mapping where Anthropic's J-Space internal entropy signal successfully detects hallucinations versus where output logprobs suffice, tested across 7 datasets on Qwen3-4B.

reddit · r/LocalLLaMA · /u/dasjomsyeet · Jul 12, 05:06

**Tags**: `#hallucination-detection`, `#LLM-evaluation`, `#interpretability`, `#Anthropic`, `#empirical-study`

---

<a id="item-8"></a>
## [Ghostel: A New Emacs Terminal Emulator Powered by libghostty](https://dakra.github.io/ghostel/) ⭐️ 6.0/10

Ghostel is a new terminal emulator for Emacs built on libghostty-vt, the embeddable terminal engine extracted from the Ghostty terminal. It promises faster rendering and more reliable input handling compared to existing Emacs terminal emulators like vterm and eat. This represents the first real-world use of libghostty-vt as an embeddable library, validating Mitchell Hashimoto's vision of making Ghostty's terminal engine available to third-party applications. For Emacs users who frequently run TUI applications or shells inside their editor, it offers a meaningful upgrade path from the aging vterm. Ghostel leverages libghostty-vt for VT sequence parsing and state management, delegating the heavy lifting to a native C/Zig library rather than parsing escape sequences in Emacs Lisp. Users report that TUI apps which refresh every frame now work smoothly, though occasional bugs like incomplete terminal clearing and rare freezes have been noted.

hackernews · signa11 · Jul 12, 08:52 · [Discussion](https://news.ycombinator.com/item?id=48879504)

**Background**: Ghostty is a fast, native, GPU-accelerated terminal emulator created by Mitchell Hashimoto. Its core engine, libghostty-vt, is a zero-dependency C and Zig library that handles the complex task of parsing VT (Virtual Terminal) sequences such as ANSI and XTERM escape codes, managing cursor state, and handling text reflow. Emacs users have long relied on terminal emulators like vterm (the traditional choice) and eat (a newer alternative offering complete mouse and clipboard support) to run shell commands and TUI applications inside Emacs buffers. By embedding libghostty-vt into Emacs, Ghostel bypasses the limitations of Emacs Lisp-based terminal parsing.

<details><summary>References</summary>
<ul>
<li><a href="https://mitchellh.com/writing/libghostty-is-coming">Libghostty Is Coming – Mitchell Hashimoto</a></li>
<li><a href="https://repo-explainer.com/ghostty-org/ghostling">Ghostling: Stripping the Terminal to its... — Repo Explainer</a></li>
<li><a href="https://akib.ami.bd/blog/introducing-eat.html">Introducing Eat: A New Terminal Emulator for Emacs | Akib Azmain Turja</a></li>

</ul>
</details>

**Discussion**: The community response is overwhelmingly positive, with users praising the noticeable performance improvements over vterm and the cleaner ELisp API. Early adopters highlight practical benefits like clickable code references in Codex summaries opening directly in Emacs buffers. However, some users report rough edges including incomplete terminal clearing and occasional freezes, indicating the project is still maturing.

**Tags**: `#emacs`, `#terminal-emulator`, `#libghostty`, `#developer-tools`, `#open-source`

---

<a id="item-9"></a>
## [MLX Port of Hunyuan3D Runs Image-to-3D Locally on Apple Silicon](https://www.reddit.com/r/LocalLLaMA/comments/1uuga40/local_image_to_3d_2gb_ram_20s_apple_silicon_iphone/) ⭐️ 6.0/10

Developer ZimengXiong released an open-source MLX-based port of Tencent's Hunyuan3D-Paint and Hunyuan3D-Shape models, packaged as a standalone macOS/iOS app called Modelr. On an M4 Max in FP16, shape generation completes in roughly 20–22 seconds using 5.6–7.3 GB of peak memory, while the texturing (paint) stage is far heavier at 231–344 seconds and 38–39 GB. It is the first end-to-end image-to-3D desktop app for Apple Silicon, demonstrating that Tencent's diffusion-based 3D pipeline can run entirely on-device without PyTorch overhead, making the technology accessible on consumer Macs and even iPhones via quantization. This lowers the barrier for developers wanting to embed fast 3D generation directly into Swift applications. Despite the '<2 GB RAM' claim in the post title, FP16 benchmarks show shape inference needs 5.6–7.3 GB and paint inference needs 38–39 GB; sub-2 GB usage is only achievable via aggressive Q4 or Q8 quantization on recent Macs/iPhones. The app integrates Apple's SwiftVision for background removal and streams diffusion progress in real time, but the paint stage's memory footprint remains a serious limitation for most consumer hardware.

reddit · r/LocalLLaMA · /u/arduinoRPi4 · Jul 12, 14:00

**Background**: MLX is Apple's open-source array framework for machine learning on Apple Silicon, similar to NumPy/PyTorch but designed to take advantage of Apple's unified memory architecture and GPU. Hunyuan3D is Tencent's open-source suite for generating 3D meshes and textures from a single 2D image, consisting of a shape-generation diffusion model (Shape) and a texture-synthesis model (Paint) that supports both standard RGB and physically based rendering (PBR) workflows. PBR texturing simulates realistic light-material interaction, producing assets that look correct under varied lighting conditions but at significantly higher computational cost.

<details><summary>References</summary>
<ul>
<li><a href="https://opensource.apple.com/projects/mlx/">Apple Open Source</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>
<li><a href="https://huggingface.co/spaces/tencent/Hunyuan3D-2">Hunyuan 3 D -2.0 - a Hugging Face Space by tencent</a></li>

</ul>
</details>

**Tags**: `#image-to-3d`, `#apple-silicon`, `#mlx`, `#hunyuan3d`, `#on-device-ai`

---

<a id="item-10"></a>
## [Moondream 3.1: 9B MoE Vision Language Model Released](https://www.reddit.com/r/LocalLLaMA/comments/1uunqcz/moondream319ba2b/) ⭐️ 6.0/10

Moondream has released version 3.1, an open-weight vision language model built on a mixture-of-experts (MoE) architecture with 9 billion total parameters and 2 billion active parameters per inference. The model supports native query, detect, point, and caption capabilities, all returning structured output, and claims state-of-the-art performance in visual reasoning and object detection. MoE architectures in vision language models are still relatively uncommon, so Moondream 3.1 represents a notable technical approach that aims to balance capability with deployment efficiency by activating only a fraction of total parameters per token. As an open-weight release with structured outputs for detection and pointing, it could become a practical option for developers building grounded multimodal applications locally. The 'A2B' suffix indicates that 2B parameters are active out of 9B total, which reduces compute cost compared to a dense 9B model while preserving the representational capacity of a larger network. All four capabilities—query, detect, point, and caption—are implemented natively rather than as adapters, meaning they are built directly into the model's training rather than bolted on afterwards.

reddit · r/LocalLLaMA · /u/secopsml · Jul 12, 18:40

**Background**: Vision language models (VLMs) are multimodal AI systems that take images as input and produce text or structured outputs describing them; modern examples include Molmo and Qwen-VL. Mixture of Experts (MoE) is an architecture where a gating network routes each input to a subset of specialized sub-networks, allowing very large total parameter counts while keeping per-token compute low—most famously used in text LLMs like Mixtral and DeepSeek. 'Open-weight' means the trained model parameters are released for download, but unlike fully open-source releases, training code and data may not be made public. Pointing, in the VLM sense, refers to outputting pixel coordinates that locate referenced objects in an image, enabling grounded interactions.

<details><summary>References</summary>
<ul>
<li><a href="https://mtiosavljevic.com/p/mixture-of-experts-the-architecture-revolutionizing-large-language-models/">Mixture of Experts : The Architecture Revolutionizing Large...</a></li>
<li><a href="https://www.bentoml.com/blog/multimodal-ai-a-guide-to-open-source-vision-language-models">Multimodal AI: The Best Open-Source Vision Language Models in 2026</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llms">Best Open - Source LLM Models in 2026: Coding, Local, Agentic AI...</a></li>

</ul>
</details>

**Discussion**: The Reddit submission received limited discussion and primarily served as a launch announcement without substantive technical details or benchmarks from the community. No significant disagreements or counterarguments were surfaced in the provided content.

**Tags**: `#vision-language-model`, `#mixture-of-experts`, `#open-source`, `#multimodal-AI`, `#model-release`

---

<a id="item-11"></a>
## [Apple sues OpenAI alleging trade secret theft, says scheme was 'at every level'](https://www.reddit.com/r/LocalLLaMA/comments/1uus189/apple_sues_openai_alleging_trade_secret_theft/) ⭐️ 6.0/10

Apple has filed a lawsuit against OpenAI alleging systematic trade secret theft 'at every level' of the organization.

reddit · r/LocalLLaMA · /u/fallingdowndizzyvr · Jul 12, 21:25

**Tags**: `#legal`, `#openai`, `#apple`, `#trade-secrets`, `#ai-industry`

---

<a id="item-12"></a>
## [Xiaomi quietly uploads MiMo-V2.5-DFlash weights to Hugging Face](https://www.reddit.com/r/LocalLLaMA/comments/1uu8d1v/xiaomi_quietly_uploaded_mimov25dflash_official/) ⭐️ 6.0/10

Xiaomi has quietly uploaded MiMo-V2.5-DFlash weights to Hugging Face, including a dedicated dflash directory with the DFlash draft model, alongside a separate MTP (Multi-Token Prediction) model. The 300B+ parameter base model currently runs at roughly 8-10 tokens per second on dual 24GB GPUs with RAM offload, and DFlash speculative decoding is expected to roughly double that throughput. For local LLM enthusiasts, a viable speculative decoding draft model for a 300B+ parameter base could dramatically improve inference speeds on consumer hardware, making otherwise unwieldy large models much more practical to run at home. It also signals that major Chinese AI labs like Xiaomi are increasingly investing in open-weight releases tailored to community inference stacks. DFlash differs from token-by-token speculative decoding by using a block diffusion model that drafts K candidate tokens in a single forward pass, and the draft is shipped as a separately trained external checkpoint rather than embedded in the base model. The original Reddit poster notes that the model's shared MTP head does not yet work in llama.cpp because the runtime has trouble identifying MTP layers, but DFlash may sidestep that issue, which is why community members are eager to see a GGUF conversion.

reddit · r/LocalLLaMA · /u/nasone32 · Jul 12, 07:11

**Background**: Speculative decoding is an inference acceleration technique in which a small 'draft' model proposes several candidate tokens and the large base model verifies them in parallel, turning the autoregressive bottleneck into a faster draft-then-verify step. DFlash is a specific variant that replaces the token-by-token drafter with a block diffusion model capable of generating multiple tokens in a single forward pass. MTP (Multi-Token Prediction) is a related but distinct training paradigm, notably used in DeepSeek-V3, that has auxiliary heads to predict several future tokens and which can also be repurposed for speculation. GGUF is the de facto model format used by llama.cpp for running LLMs locally on CPUs and consumer GPUs.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datacamp.com/tutorial/how-to-speed-up-local-llms-with-dflash-speculative-decoding">How to Speed Up Local LLMs with DFlash Speculative Decoding</a></li>
<li><a href="https://www.spheron.network/blog/dflash-block-diffusion-speculative-decoding-gpu-cloud/">DFlash on GPU Cloud: 6x Faster LLM Inference with... | Spheron Blog</a></li>
<li><a href="https://nvidia.github.io/TensorRT-Edge-LLM/user_guide/examples/speculative-decoding.html">Speculative Decoding — TensorRT Edge-LLM</a></li>

</ul>
</details>

**Discussion**: The Reddit thread centers on technical speculation rather than settled benchmarks: the original poster and commenters are enthusiastic but unable to immediately GGUF-ify the weights, and they debate whether the shared MTP head or the newly uploaded separate MTP model could already work in llama.cpp, with the consensus being that llama.cpp struggles to identify MTP layers. Participants hope that the standalone DFlash draft model is the path that actually unlocks faster local inference for this base.

**Tags**: `#Xiaomi`, `#MiMo`, `#DFlash`, `#speculative-decoding`, `#local-llm`, `#huggingface`

---

<a id="item-13"></a>
## [Three-line fix resolves years-old fp16 precision bug on Tesla P100 in llama.cpp](https://www.reddit.com/r/LocalLLaMA/comments/1uu6p9o/your_80_tesla_p100_has_been_doing_silently_noisy/) ⭐️ 6.0/10

A developer identified and shipped a fix for a long-standing numerical precision bug in llama.cpp's CUDA backend that affected Tesla P100 GPUs (sm_60 architecture). The P100 was incorrectly using a fast-fp16 math path despite needing higher precision, while the sm_61-based GTX 10-series and P40 had been exempted years ago. The patch is just three lines, already merged in two forks (turboquant v0.3.0 and spiritbuun's buun-llama-cpp), and an issue has been filed upstream with GGML. The bug silently degraded inference quality on P100 cards — about 1 in 29 of the model's next-token predictions differed from what full-precision math would have selected — yet performance was not actually improved by the fast path on real workloads. With used P100s now selling for ~$80, 16GB of HBM2, and 732 GB/s bandwidth amid the current DRAM price crisis, this fix makes the P100 a dramatically more viable budget option for local LLM inference, potentially closing the perceived quality gap with the P40. Benchmarks on Qwen3-27B with wikitext-2 show KL divergence dropping from 0.0023 to 0.000001 (~2300× tighter) and top-token agreement rising from 96.5% to 99.9% after the fix. Decode throughput was actually ~1.4% faster patched because real workloads on P100 are bound by GEMM and memory bandwidth rather than the fp16 vector path. The fix only affects sm_60 — Volta and newer architectures use different kernels and are untouched; a Blackwell build produced bit-identical perplexity confirming zero collateral effects.

reddit · r/LocalLLaMA · /u/apollo_mg · Jul 12, 05:41

**Background**: llama.cpp is a popular open-source C/C++ library for running large language models locally on consumer hardware, with backends for CPUs and GPUs including CUDA. NVIDIA GPUs are identified by a compute capability version (e.g., sm_60, sm_61) that maps to their underlying architecture; sm_60 corresponds to Pascal (P100) and sm_61 to the GTX 10-series and P40. Fast fp16 (half-precision) math paths in CUDA trade numerical precision for throughput, which is usually acceptable but can degrade inference quality when models depend on fine-grained logit differences between candidate tokens.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ggml-org/llama.cpp">GitHub - ggml-org/ llama . cpp : LLM inference in C/C++ · GitHub</a></li>
<li><a href="https://www.myzhar.com/blog/tutorials/tutorial-nvidia-gpu-cuda-compute-capability/">[Tutorial CUDA] Nvidia GPU : CUDA Compute Capability</a></li>
<li><a href="https://gist.github.com/CyberSys/9e65d4c7c92cc9d6fa12c7bae133ce50">CUDA GPU Compute Capability - Compatibility · GitHub</a></li>

</ul>
</details>

**Tags**: `#llama.cpp`, `#CUDA`, `#GPU-computing`, `#Tesla-P100`, `#numerical-precision`

---

<a id="item-14"></a>
## [Voodoo Quant Claims 95% KLD Improvement Over Unsloth Dynamic 2.0](https://www.reddit.com/r/LocalLLaMA/comments/1uua3jd/voodoo_quant_beats_unsloth_dynamic_20_kld_by_95/) ⭐️ 6.0/10

A new quantization method called Voodoo Quant has been released, with GGUF model uploads for Qwen3.5 0.8B and Qwen3.5 2B on Hugging Face. The author claims Voodoo Quant outperforms Unsloth Dynamic 2.0 by 95% on KLD metrics by using per-tensor optimization rather than block-level optimization, and reports that Voodoo generalizes more consistently across both PyTorch and llama.cpp backends. If independently validated, Voodoo Quant could meaningfully improve the quality of aggressively quantized small models used in local LLM deployments, especially on consumer hardware where running larger models at low bit-widths is the only practical option. Mixed-precision quantization is central to fitting capable models into limited VRAM, so even modest gains at the 2-bit level could expand what users can run locally. The author emphasizes that the 95% headline figure partly reflects Unsloth Dynamic's poor KLD performance on PyTorch, where Voodoo remains competitive, while on llama.cpp both methods perform well — suggesting Unsloth's block-level selection may overfit to llama.cpp's graph structure. Voodoo's sweet spot is reported to be around the 2-bit level, and the technique is claimed to be more transferable across backends. The current uploads are described as primarily research-oriented, with larger targets like a 27B-class model mentioned as future work.

reddit · r/LocalLLaMA · /u/1ncehost · Jul 12, 08:52

**Background**: Quantization reduces the numerical precision of a model's weights (e.g., from 16-bit to 4-bit or 2-bit) to shrink file size and memory use, at the cost of some accuracy loss. GGUF is the file format used by llama.cpp to distribute and run quantized models locally, and it bundles weights, tokenizer, and metadata into a single portable artifact. Kullback–Leibler Divergence (KLD) is a common metric for measuring how much a quantized model's output distribution deviates from the full-precision reference. Per-tensor quantization assigns one scale/zero-point to an entire weight tensor, while per-block (or per-group) quantization divides tensors into smaller blocks with their own parameters, allowing finer adaptation in the presence of outliers — at the cost of more metadata and potentially overfitting to a specific inference backend.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Llama.cpp">llama.cpp - Wikipedia</a></li>
<li><a href="https://developer.nvidia.com/blog/model-quantization-concepts-methods-and-why-it-matters/">Model Quantization : Concepts, Methods, and Why It Matters</a></li>

</ul>
</details>

**Tags**: `#quantization`, `#gguf`, `#qwen`, `#local-llm`, `#model-optimization`

---

<a id="item-15"></a>
## [Interactive Jacobian-Lens Tool Brings Anthropic's Interpretability to GGUF Models](https://www.reddit.com/r/LocalLLaMA/comments/1uu32z6/interactive_jacobianlens_visualizer_and_live/) ⭐️ 6.0/10

A community developer released jlens-gguf, an interactive Jacobian-Lens visualizer and live steerer that adapts Anthropic's J-Lens interpretability technique to GGUF models running on llama.cpp. The tool includes a native GGUF server (closely based on llama.cpp) and supports both dense and MoE models, enabling observation, J-space swapping, abliteration, and steering of quantized models. Previously, Jacobian-Lens interpretability tools existed only for HuggingFace and PyTorch workflows, leaving users of the widely-deployed GGUF/llama.cpp ecosystem (serving millions via Ollama, LM Studio, and similar tools) without an equivalent local option. By lowering the barrier to inspecting and steering model internals, this tool makes cutting-edge interpretability research accessible to the open-source community running quantized models on consumer hardware. The lens memory overhead scales at roughly 1/8 of the model size, so a 160 GB model such as Qwen3.5-397B UD-Q3_K_XL would require about 20 GB additional RAM for the lens. The tool can observe running llama-server models in real time, but steering (abliteration/vector swapping) only works when using its own server.

reddit · r/LocalLLaMA · /u/Responsible_Fig_1271 · Jul 12, 02:37

**Background**: Anthropic's Jacobian Lens (J-Lens) is an interpretability technique introduced to surface a low-dimensional 'J-space' inside Claude, representing concepts the model is poised to verbalize—allowing researchers to read what a model is 'thinking' before it writes. GGUF is a quantized model file format natively consumed by llama.cpp, the dominant local-LLM inference engine whose ecosystem includes Ollama, LM Studio, GPT4All, and Jan.ai. Abliteration is a model-steering technique, originating from mid-2024 research by Arditi et al., that removes refusal behavior by ablating a single direction in the model's residual stream without retraining—part of a broader class of residual-stream steering methods that also includes representation engineering and DARLING-style novelty steering.

<details><summary>References</summary>
<ul>
<li><a href="https://explainx.ai/blog/what-is-j-lens-jacobian-lens-claude-interpretability-2026">What Is the J-Lens? Anthropic Jacobian Lens Guide | explainx.ai</a></li>
<li><a href="https://explainx.ai/blog/what-is-llama-cpp-run-models-locally-2026">What Is llama . cpp ? Run GGUF Models Locally | explainx.ai</a></li>
<li><a href="https://www.banandre.com/blog/abliteration-llm-slop-reduction-technique">Abliteration : Performing Brain Surgery on LLMs to Cure... - Banandre</a></li>

</ul>
</details>

**Tags**: `#llama.cpp`, `#GGUF`, `#interpretability`, `#Anthropic`, `#model-steering`

---

<a id="item-16"></a>
## [Zer0Fit: A Local MCP Server Wrapping Google's TabFM and TimesFM for Zero-Shot ML](https://www.reddit.com/r/LocalLLaMA/comments/1uudxi8/zer0fit_i_took_googles_new_tabfm_timesfm_ml/) ⭐️ 6.0/10

A graduate student built Zer0Fit, an open-source MCP server that wraps Google's recently released TabFM and TimesFM foundation models into a single Docker container, enabling zero-shot forecasting, classification, and regression tasks running entirely locally on an Nvidia GPU with 16GB+ VRAM. Zer0Fit lowers the barrier to using Google's new tabular and time-series foundation models by exposing them through the standardized MCP protocol, allowing developers to chain zero-shot ML capabilities directly into LLM-driven chat workflows (Open WebUI, Claude Code, Codex CLI) without writing bespoke training pipelines or wrangling hyperparameters. Initial benchmarks report 94.7% accuracy on the Iris classification dataset and an R² of 0.87 on California Housing regression, comparing favorably to traditionally tuned ML models. The project is PyTorch-based and CUDA-only (no Mac support), dynamically loads/unloads models into VRAM with a 5-minute TTL to conserve memory, and currently supports CSV input with XLS, XLSX, JSON, and JSONL planned.

reddit · r/LocalLLaMA · /u/Porespellar · Jul 12, 12:18

**Background**: Google Research recently introduced TabFM, a zero-shot foundation model for tabular data—essentially an 'LLM for tables' that performs classification and regression without any fine-tuning on the target dataset—and TimesFM, a decoder-only foundation model pretrained on 100 billion real-world time points for time-series forecasting (ICML 2024). The Model Context Protocol (MCP) is an open standard introduced by Anthropic in November 2024 that lets LLM-based clients (like Claude Code or Open WebUI) connect to external tools and data sources in a uniform way. Zer0Fit sits at the intersection of these two trends by packaging both Google models behind a single MCP interface.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/introducing-tabfm-a-zero-shot-foundation-model-for-tabular-data/">Introducing TabFM : A zero-shot foundation model for tabular data</a></li>
<li><a href="https://github.com/google-research/timesfm">google -research/ timesfm : TimesFM ( Time Series Foundation ...)</a></li>
<li><a href="https://en.wikipedia.org/wiki/Model_Context_Protocol">Model Context Protocol - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#MCP`, `#foundation-models`, `#zero-shot-learning`, `#local-llm`, `#time-series`, `#tabular-data`

---