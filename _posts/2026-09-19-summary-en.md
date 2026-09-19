---
layout: default
title: "Horizon Summary: 2026-09-19 (EN)"
date: 2026-09-19
lang: en
---

> From 56 items, 10 important content pieces were selected

---

1. [Android 17 is the first since 3.x to add new APIs without releasing to the AOSP](#item-1) ⭐️ 7.0/10
2. [Terry Tao: Mathematics Should Celebrate More Than Proof](#item-2) ⭐️ 7.0/10
3. [OpenRouter Compares 20 Image Generation Models on Cost and Capabilities](#item-3) ⭐️ 7.0/10
4. [I built non-autoregressive decision models with RL a year ago](#item-4) ⭐️ 6.0/10
5. [Two parallel neural ectoderm progenitors contribute to the developing brain](#item-5) ⭐️ 6.0/10
6. [Why You Should Almost Never Use AI to Write](#item-6) ⭐️ 6.0/10
7. [Alibaba open-sources medical AI model for cancer and 150 conditions](#item-7) ⭐️ 6.0/10
8. [User Warns Community Against Clore.AI Over Abuse and Unresponsive Support](#item-8) ⭐️ 6.0/10
9. [Halogen 0.12.0 restores long-context speed for Qwen3-Flash-Next on Strix Halo](#item-9) ⭐️ 6.0/10
10. [Asymmetric V100 PCIe Pair (16GB+32GB) Runs 27B LLM at ~1.38k Prompt tok/s](#item-10) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Android 17 is the first since 3.x to add new APIs without releasing to the AOSP](https://grapheneos.social/@GrapheneOS/117282080803799576) ⭐️ 7.0/10

Android 17 introduces new APIs exclusively for Pixel devices without releasing them to AOSP, marking the first such move since Android 3.x and raising concerns about Google's commitment to Android's open source ecosystem.

hackernews · theanonymousone · Sep 18, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49758736)

**Tags**: `#android`, `#aosp`, `#google`, `#open-source`, `#grapheneos`

---

<a id="item-2"></a>
## [Terry Tao: Mathematics Should Celebrate More Than Proof](https://terrytao.wordpress.com/2026/09/18/if-math-is-more-than-proof-we-need-to-better-celebrate-the-rest-of-it/) ⭐️ 7.0/10

In a September 2026 blog post, Fields Medalist Terry Tao argues that the mathematical community overemphasizes formal proof at the expense of other essential dimensions of the discipline, including intuition, computation, exploration, and discovery. Coming from one of the most influential living mathematicians, this commentary challenges the cultural norms of a discipline that shapes how mathematics is taught, published, and evaluated, and arrives at a moment when AI is already reshaping both mathematical research and perception of mathematical skill. Tao frames the piece as a manifesto calling for new genres of mathematical writing and recognition that highlight computational, experimental, and exploratory work, citing Michael Nielsen's concept of 'discovery fiction' as an inspirational example of narrative mathematical exposition.

hackernews · num42 · Sep 19, 06:28 · [Discussion](https://news.ycombinator.com/item?id=49763928)

**Background**: The tension Tao addresses echoes the early 20th-century debate between Henri Poincaré, who championed mathematical intuition and creativity, and David Hilbert, whose formalism drove the rigorous axiomatic foundations of modern mathematics. Hilbert's program ultimately prevailed in shaping academic mathematics, establishing proof as the gold standard for publication and tenure. Philosophies of mathematics such as formalism, intuitionism (founded by L.E.J. Brouwer), and Platonism have long contested what mathematics fundamentally is—whether it is a system of symbols, a mental construction, or the study of abstract objects.

<details><summary>References</summary>
<ul>
<li><a href="https://www.britannica.com/science/philosophy-of-mathematics/Logicism-intuitionism-and-formalism">Philosophy of mathematics - Logicism, Intuitionism, Formalism | Britannica</a></li>
<li><a href="https://www.encyclopedia.com/science/encyclopedias-almanacs-transcripts-and-maps/foundations-mathematics-hilberts-formalism-vs-brouwers-intuitionism">The Foundations of Mathematics: Hilbert's Formalism vs. Brouwer's Intuitionism | Encyclopedia.com</a></li>
<li><a href="https://www.quantamagazine.org/in-math-rigor-is-vital-but-are-digitized-proofs-taking-it-too-far-20260325/">In Math, Rigor Is Vital. But Are Digitized Proofs Taking It Too Far? | Quanta Magazine</a></li>

</ul>
</details>

**Discussion**: Commenters drew historical parallels to the 1900 Poincaré–Hilbert debate at the International Congress of Mathematicians, noting that Hilbert's path won out and intuition lost prominence in schooling. Others connected the discussion to software engineering's recent AI disruption, arguing that mathematicians face an even more violent version of the same existential challenge. One commenter linked Michael Nielsen's 'discovery fiction' writing style as a model Tao was inspired by, while another argued the Fields Medal's age limit favors raw brainpower over deep understanding, framing AI-driven change as a natural correction.

**Tags**: `#mathematics`, `#terry-tao`, `#math-education`, `#research-culture`, `#philosophy-of-math`

---

<a id="item-3"></a>
## [OpenRouter Compares 20 Image Generation Models on Cost and Capabilities](https://openrouter.ai/blog/insights/image-generation-models-compared/) ⭐️ 7.0/10

OpenRouter systematically evaluated 20 image generation models through its Image API by sending the same prompt to each, then reading the usage.cost field from every response to normalize pricing across models that charge per token, per megapixel, or per image. Beyond cost, the comparison also tested text rendering, reference-image editing, seed reproducibility, and text-plus-image multimodal responses. Developers choosing between image generation APIs have struggled to compare models fairly because vendors use incompatible pricing units, making headline rate comparisons meaningless. This type of apples-to-apples benchmark from an established AI routing platform gives engineering teams actionable data on both cost efficiency and practical capability gaps like text rendering fidelity and reference-image editing support. The benchmark normalizes three fundamentally different pricing schemes — per-token (typical for autoregressive or multimodal models), per-megapixel (common for diffusion models), and per-image (flat-rate) — by reading the actual billed cost returned in the API response rather than advertised list prices. Capability tests include whether models can render legible in-image text, accept reference images for editing, return reproducible outputs via seeds, and respond to mixed text-and-image prompts.

rss · OpenRouter Blog · Sep 18, 00:00

**Background**: OpenRouter is a unified API gateway launched in early 2023 that lets developers access hundreds of AI models from dozens of providers through a single interface, with costs routed and billed centrally. Image generation models have proliferated rapidly, but each provider structures pricing differently — diffusion models often charge by output resolution, multimodal models charge by token, and some providers simply charge per generated image — making it nearly impossible to compare rates from a price sheet alone. Reference-image editing is a specific capability where a user supplies an input image along with instructions, and the model modifies it while preserving desired elements; reliable text rendering inside generated images has also been a persistent weakness across many image models.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/">The unified interface for every model . Find the best models & prices...</a></li>
<li><a href="https://ai-tools-web-app.pages.dev/tools/openrouter">OpenRouter Features, Pricing, and Alternatives | AI Tools</a></li>
<li><a href="https://www.technology.org/2026/09/14/why-controlled-ai-editing-starts-with-a-reference-image/">Why Controlled AI Editing Starts with a Reference Image - Technology Org</a></li>

</ul>
</details>

**Tags**: `#image-generation`, `#model-comparison`, `#api-cost-analysis`, `#multimodal-ai`, `#developer-tools`

---

<a id="item-4"></a>
## [I built non-autoregressive decision models with RL a year ago](https://laya.convaiinnovations.com/) ⭐️ 6.0/10

HN discussion comparing a year-old non-autoregressive RL decision model with the recent 'Jev' product, highlighting that both appear to be BERT-based classification approaches repackaged with ambitious marketing.

hackernews · nandakishor_ml · Sep 19, 10:46 · [Discussion](https://news.ycombinator.com/item?id=49765348)

**Tags**: `#machine-learning`, `#nlp`, `#ai-hype`, `#classification`, `#reinforcement-learning`

---

<a id="item-5"></a>
## [Two parallel neural ectoderm progenitors contribute to the developing brain](https://med.stanford.edu/news/all-news/2026/09/two-separate-brains.html) ⭐️ 6.0/10

Stanford researchers find two distinct neural ectoderm progenitors contribute to brain development, though community discussion suggests the finding is less novel than PR implies, with notable potential implications for in vitro brain stem cell cultivation.

hackernews · emigre · Sep 19, 05:48 · [Discussion](https://news.ycombinator.com/item?id=49763697)

**Tags**: `#neuroscience`, `#developmental-biology`, `#research`, `#brain-development`, `#stem-cells`

---

<a id="item-6"></a>
## [Why You Should Almost Never Use AI to Write](https://erichgrunewald.substack.com/p/why-you-should-almost-never-use-ai) ⭐️ 6.0/10

A Substack opinion piece argues that writers should almost never use AI to generate prose, citing cognitive and quality concerns. The article, drawing on philosopher Eric Schwitzgebel's analysis, highlights how passive reading of AI-generated text differs fundamentally from the effortful thinking involved in producing writing. As AI writing tools become ubiquitous in workplaces and creative workflows, this piece challenges the prevailing assumption that AI is a productivity booster for writing tasks. It has implications for how individuals and organizations should think about delegation, quality control, and the cognitive costs of outsourcing thought to machines. The article draws on cognitive science research suggesting that the act of generating text is itself a form of thinking, and that passively accepting AI-suggested words short-circuits this cognitive process. The piece also warns that AI-generated prose tends to be vague and subtly wrong in ways that are difficult for readers to notice upon casual review.

hackernews · erwald · Sep 19, 16:35 · [Discussion](https://news.ycombinator.com/item?id=49767937)

**Background**: Large language models (LLMs) like GPT-4 and Claude have made AI-assisted writing widely accessible, with many professionals now using these tools to draft emails, reports, and articles. The debate over whether AI augments or undermines human writing centers on questions of voice, originality, and the cognitive processes involved in composition. Eric Schwitzgebel is a philosopher of mind known for work on consciousness and cognition, which lends philosophical weight to the article's arguments.

**Discussion**: Commenters offered nuanced frameworks rather than blanket rejections of AI writing. The most popular advice was to use AI for reading-oriented tasks (summaries, reports) rather than for producing content for others, and to use AI as a critic of your own writing rather than as a generator. One commenter extended the argument to AI-generated code, noting similar risks of vague, subtly incorrect output that costs the human reader later. A workplace user reported losing significant time correcting AI prose that had stripped nuance from a collaborative white paper.

**Tags**: `#ai`, `#writing`, `#productivity`, `#llm`, `#workflow`

---

<a id="item-7"></a>
## [Alibaba open-sources medical AI model for cancer and 150 conditions](https://www.reddit.com/r/LocalLLaMA/comments/1wk9fag/alibaba_opensources_medical_ai_model_that_can/) ⭐️ 6.0/10

Alibaba has open-sourced a medical AI model capable of detecting cancer and approximately 150 other medical conditions, making it freely available for researchers and developers to use, modify, and build upon. The release appears to extend Alibaba's broader Qwen open-source ecosystem into the healthcare domain. This release marks another major step in the democratization of medical AI, allowing hospitals, clinics, and researchers — especially those in resource-limited settings — to access advanced diagnostic capabilities without expensive licensing fees. It also intensifies competition in the open medical AI space, where Google (MedGemma) and Meta (Llama-based healthcare tools) are already active. The model builds on Alibaba's Qwen family of open-weight models, which range from 0.6B edge models to a 397B flagship. Alibaba's DAMO Academy has also released MedEvalKit, a unified evaluation framework for benchmarking large medical models, suggesting the ecosystem includes both models and evaluation tooling.

reddit · r/LocalLLaMA · /u/giveen · Sep 19, 02:08

**Background**: Open-source medical AI models are large language or multimodal models trained or fine-tuned on medical data that can be freely downloaded and modified, unlike proprietary systems from companies like OpenAI or Anthropic. Recent examples include Google's MedGemma (released August 2025), which can interpret medical images, and open models that Harvard Medical School found can match proprietary LLMs on tough diagnostic cases. Alibaba's Qwen series has been one of the most comprehensive open-source AI ecosystems, spanning text, vision, audio, and coding capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/alibaba-damo-academy/MedEvalKit">alibaba -damo-academy/MedEvalKit: MedEvalKit: A Unified Medical ...</a></li>
<li><a href="https://qwen-ai.com/">Qwen AI — Open - Source LLMs, Vision, Audio & Coding Models (2026)</a></li>
<li><a href="https://www.artificialintelligence-news.com/news/google-open-medgemma-ai-models-healthcare/">Google's open MedGemma AI models could transform healthcare</a></li>

</ul>
</details>

**Discussion**: The Reddit submission is a low-effort link post with minimal technical detail or analysis from the submitter, who expressed hope that such AI applications would help the public recognize positive uses of AI. No substantive community discussion or technical breakdown was visible in the provided content.

**Tags**: `#medical-ai`, `#open-source`, `#alibaba`, `#cancer-detection`, `#diagnostics`

---

<a id="item-8"></a>
## [User Warns Community Against Clore.AI Over Abuse and Unresponsive Support](https://www.reddit.com/r/LocalLLaMA/comments/1wkgs01/general_warning_about_cloreai/) ⭐️ 6.0/10

A Reddit user on r/LocalLLaMA reported that a renter on the Clore.AI GPU marketplace used their hosted machine to scan for vulnerabilities and attempt to post malware to a Colombian betting site. When the user reported the abuse with hard evidence—including vulnerability scan logs, exploit attempts, and AI agent reports—Clore.AI refused to cancel the order, block the abusive renter, or blacklist the offending account, and subsequently blocked the user from both in-app support and Telegram. Decentralized GPU rental platforms like Clore.AI, Vast.ai, and Akash are increasingly popular among AI/ML practitioners looking to monetize idle hardware or access affordable compute. This incident highlights the legal and security risks hosts face—potentially becoming liable for cybercrimes committed through their home internet connections—and raises serious questions about the responsibility of marketplaces to moderate abusive renters. The user invoked Clore.AI's own Terms & Conditions, which permit hosts to inspect a renter's environment when legally required, and mounted the filesystem offline to find exploit logs and malware payloads. The user has preserved the renter's Docker volume as forensic evidence for potential security researchers or legal authorities, and notes that they have no basis to compare Clore.AI's conduct to competitors like Vast.ai or Akash.

reddit · r/LocalLLaMA · /u/anomaly256 · Sep 19, 08:37

**Background**: Clore.AI is a decentralized GPU marketplace that connects GPU owners with renters who need affordable compute for AI/ML workloads, claiming access to over 20,000 GPUs. Hosts configure their machines with Docker images and port forwarding, then earn revenue when renters spin up containers on their hardware. Similar platforms include Vast.ai and Akash. Because renters typically have shell-level or container-level access to the host machine, hosts risk their IP addresses and network connections being used for any activity the renter chooses—including potentially illegal actions—making moderation and renter vetting critical platform responsibilities.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.clore.ai/gpu-marketplace/overview">Overview | Clore.ai</a></li>
<li><a href="https://docs.clore.ai/help/faq">FAQ | Clore.ai</a></li>
<li><a href="https://probsee.com/p/Rented_GPU_Computing">Rented GPU Computing | ProbWiki | ProbSee</a></li>

</ul>
</details>

**Tags**: `#gpu-rental`, `#security`, `#clore-ai`, `#warning`, `#community-alert`

---

<a id="item-9"></a>
## [Halogen 0.12.0 restores long-context speed for Qwen3-Flash-Next on Strix Halo](https://www.reddit.com/r/LocalLLaMA/comments/1wkyny9/qwen38flashnext_at_1m_context_on_strix_halo_38/) ⭐️ 6.0/10

Halogen 0.12.0 fixes a context-depth performance regression, boosting Qwen3-Flash-Next decode throughput at 1,004,581 tokens of context from 27.3 to 38.3 tok/s on a Ryzen AI Max+ 395 with 128GB, while also shaving cold prefill at 1M from 21.2 to 17.9 minutes. Local LLM runners targeting million-token contexts on AMD's Strix Halo APU can now sustain usable interactive decode rates, narrowing the gap between local inference and datacenter-class long-context performance without requiring hardware upgrades. The fix was validated using greedy decoding with a 64-token output and YaRN-style RoPE extension (HALOGEN_ROPE_YARN=4, HALOGEN_CTX=1048576) under the default speculative drafter; the 32k benchmark row was unchanged, and a cached follow-up turn at 1M context reaches the first token in roughly 0.55 seconds.

reddit · r/LocalLLaMA · /u/peonist-ai · Sep 19, 21:49

**Background**: AMD's Strix Halo (Ryzen AI Max+ 395) is an APU with 16 Zen 5 CPU cores and up to 128GB of unified LPDDR5X memory, making it one of the few consumer platforms capable of holding very large models entirely in memory. Qwen3-Flash-Next is a hybrid linear-attention model in the Qwen3 family designed for long-context inference. To serve beyond its native training window it relies on YaRN (Yet another RoPE extensioN), a position-embedding interpolation method that lets RoPE-based models extrapolate to much longer contexts with minimal fine-tuning. Halogen is an inference server/runtime used here alongside speculative decoding, an optimization where a small draft model proposes tokens that the larger target model then verifies in parallel.

<details><summary>References</summary>
<ul>
<li><a href="https://www.amd.com/en/products/processors/laptop/ryzen/ai-300-series/amd-ryzen-ai-max-plus-395.html">AMD Ryzen ™ AI Max + 395 | The ultimate next gen AI PCs</a></li>
<li><a href="https://medium.com/@rcrajatchawla/understanding-yarn-extending-context-window-of-llms-3f21e3522465">Understanding YaRN: Extending Context Window of LLMs | by RAJAT CHAWLA | Medium</a></li>
<li><a href="https://aman.ai/primers/ai/speculative-decoding/">Aman's AI Journal • Primers • Speculative Decoding</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#qwen3`, `#strix-halo`, `#long-context`, `#inference-optimization`

---

<a id="item-10"></a>
## [Asymmetric V100 PCIe Pair (16GB+32GB) Runs 27B LLM at ~1.38k Prompt tok/s](https://www.reddit.com/r/LocalLLaMA/comments/1wkwec5/i_turned_an_asymetric_pair_of_tesla_v100s_pcie/) ⭐️ 6.0/10

A user benchmarked an asymmetric pair of Tesla V100 PCIe GPUs (16 GB + 32 GB, 48 GB total) running llama.cpp inside Proxmox/LXC containers, achieving 1,376.9 prompt tok/s and 39.9 decode tok/s on Qwen3.8 27B Q6_K_M, and even running a 177 B/6 B-active MoE model at ~26 decode tok/s across the same two cards. With modern GPU prices extremely high, this report shows that older, mismatched V100 cards—often available cheaply on the second-hand market—can still deliver usable throughput for local LLM inference, democratizing access for hobbyists and small labs. It also provides concrete configuration guidance for anyone running multi-GPU setups on uneven hardware. Tensor split with the 32 GB V100 as the main GPU decisively beat layer split (1,376.87 vs 981.79 pp tok/s), and enabling Flash Attention, Q8 KV cache, NUMA distribution, and large batches (ubatch 2,048) with only 20 threads were all critical. The 177 B/6 B MoE GGUF (103.68 GiB) required graph split 1:1.75 and ik_llama.cpp rather than mainline llama.cpp to function.

reddit · r/LocalLLaMA · /u/OkBase5453 · Sep 19, 20:16

**Background**: The Tesla V100 is a datacenter GPU based on NVIDIA's Volta architecture (compute capability 7.0), released in 2017, and remains capable for many workloads despite being superseded by Ampere, Hopper, and Blackwell generations. llama.cpp is the de facto open-source inference engine for local LLMs, and GGUF is its standard file format that supports multiple quantization levels (Q4, Q6, Q8, etc.) to trade model size against quality. Mixture-of-Experts (MoE) models like the 177 B/6 B variant tested here contain many specialized sub-networks but only activate a small subset per token, reducing compute cost while still demanding large total VRAM. Flash Attention is a memory-efficient algorithm that computes attention in tiles to avoid materializing full attention matrices in GPU memory.

<details><summary>References</summary>
<ul>
<li><a href="https://lobehub.com/skills/47thstreet-clawdagent-gguf">gguf - quantization | Skills Marketplace · LobeHub</a></li>
<li><a href="https://localmodel.run/guides/mixture-of-experts">Mixture of experts ( MoE ) explained for local LLMs · localmodel.run</a></li>
<li><a href="https://ai.plainenglish.io/flash-attention-kernels-the-hidden-engine-powering-modern-ai-speed-13f840800868">Flash Attention Kernels: The Hidden Engine Powering Modern AI...</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#llama.cpp`, `#gpu-benchmarks`, `#tesla-v100`, `#vllm-inference`

---