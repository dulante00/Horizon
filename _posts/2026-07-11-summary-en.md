---
layout: default
title: "Horizon Summary: 2026-07-11 (EN)"
date: 2026-07-11
lang: en
---

> From 42 items, 8 important content pieces were selected

---

1. [vLLM v0.25.0: MRv2 Default, PagedAttention Removed, FP8 MoE Added](#item-1) ⭐️ 8.0/10
2. [Apple Sues OpenAI Over Alleged Trade Secret Theft by Former Employees](#item-2) ⭐️ 8.0/10
3. [ClickHouse Scales PgBouncer to 4x Throughput with Process Peering](#item-3) ⭐️ 7.0/10
4. [HuggingFace's Guide to Profiling Attention in PyTorch](#item-4) ⭐️ 7.0/10
5. [Prefer strict tables in SQLite](#item-5) ⭐️ 6.0/10
6. [Einstein's Relativity Shapes Chemical Bonds in Heavy Elements](#item-6) ⭐️ 6.0/10
7. [AI 2040 and the cult of intelligence](#item-7) ⭐️ 6.0/10
8. [VultronRetriever Embedding Models Claim #1 on MTEB Across Size Classes](#item-8) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [vLLM v0.25.0: MRv2 Default, PagedAttention Removed, FP8 MoE Added](https://github.com/vllm-project/vllm/releases/tag/v0.25.0) ⭐️ 8.0/10

vLLM v0.25.0 ships 558 commits from 232 contributors, making Model Runner V2 the default execution path for all dense models, completely removing the legacy PagedAttention implementation, and bringing the Transformers backend to parity with native vLLM performance. The release also adds FP8 MoE support, a unified Streaming Parser Engine, universal speculative decoding for heterogeneous vocabularies (TLI), new DSpark and DFlash drafters, and several new models including LLaVA-OneVision-2, GLM-5, and DeepSeek-V3.2. vLLM is one of the most widely deployed open-source LLM inference engines, so this release directly affects serving stacks across the industry. The removal of legacy PagedAttention and the promotion of MRv2 signal architectural maturation, while Transformers-backend parity lowers the barrier for supporting new models without custom kernels. FP8 MoE and new speculative decoding drafters further push inference efficiency, which matters for cost and latency at scale. Notable technical details include multimodal-prefix bidirectional attention, Mamba hybrid prefix caching, dynamic speculative decoding compatible with full CUDA graphs, and a new Triton R-SWA backend for Unlimited OCR. MRv2 now supports EVS and realtime embeddings, while the Rust frontend gained HTTPS/mTLS, a DP supervisor, and profiler control routes. NVFP4 support was added for MiniMax-M3 alongside pipeline parallelism.

github · khluu · Jul 11, 20:06

**Background**: vLLM is an open-source high-throughput LLM serving engine whose original performance advantage came from PagedAttention, a technique that partitions the KV cache into non-contiguous blocks—inspired by virtual memory paging in operating systems—to reduce GPU memory waste and improve throughput. Model Runner V2 (MRv2) is the next-generation execution path that supersedes the V0/V1 runners and enables features like CUDA-graph-friendly speculative decoding. Speculative decoding accelerates inference by using a smaller draft model to predict multiple tokens that the target model then verifies in parallel, while FP8 quantization stores weights and activations in 8-bit floating point to shrink memory footprint and speed up computation, especially for Mixture-of-Experts (MoE) models.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@abonia/vllm-and-pagedattention-a-comprehensive-overview-20046d8d0c61">vLLM and PagedAttention : A Comprehensive Overview | Medium</a></li>
<li><a href="https://www.spheron.network/blog/fp8-quantization-inference-performance-hardware-explained/">What is FP8 Quantization? AI Inference Performance, Accuracy, and Hardware Support Explained (2026) | Spheron Blog</a></li>
<li><a href="https://developer.nvidia.com/blog/an-introduction-to-speculative-decoding-for-reducing-latency-in-ai-inference/">An Introduction to Speculative Decoding for Reducing Latency in AI Inference | NVIDIA Technical Blog</a></li>

</ul>
</details>

**Tags**: `#vllm`, `#llm-inference`, `#model-serving`, `#open-source`, `#release-notes`

---

<a id="item-2"></a>
## [Apple Sues OpenAI Over Alleged Trade Secret Theft by Former Employees](https://9to5mac.com/2026/07/10/apple-sues-openai-trade-secret-theft/) ⭐️ 8.0/10

Apple has filed a lawsuit against OpenAI, accusing former Apple employees of stealing confidential hardware and AI-related trade secrets when they moved to OpenAI, including evidence of systematic efforts to conceal the theft such as instructing new hires not to disclose their OpenAI employment. This lawsuit represents a major escalation in the legal and competitive tensions between two of the most powerful companies in AI, and could set important precedents for how employee mobility and intellectual property are handled in the rapidly evolving AI industry. Apple alleges that OpenAI recruits emailed themselves confidential information before leaving Apple, and that OpenAI used confidential Apple hardware information when approaching Apple's suppliers. The case reportedly centers on employees including one named Tan, with Apple claiming OpenAI actively coached new hires on how to avoid detection.

hackernews · stock_toaster · Jul 10, 20:47 · [Discussion](https://news.ycombinator.com/item?id=48865019)

**Background**: Trade secret lawsuits between tech companies over employee poaching are not uncommon, with notable precedents such as the Waymo v. Uber case that effectively ended Uber's self-driving program. The AI industry has been particularly contentious regarding intellectual property, with ongoing debates about the use of copyrighted material for training models. Apple's AI efforts have been developing hardware and software integration, making hardware-related secrets particularly valuable to competitors.

**Discussion**: Community sentiment is strongly critical of OpenAI, with commenters describing the allegations as 'damning' and characterizing the company's behavior as part of a pattern of disregarding legal boundaries. Some users draw parallels to the Waymo vs. Uber lawsuit and warn that this could effectively end OpenAI's hardware ambitions. Others raise broader concerns about the ethical foundations of generative AI companies and advise businesses using OpenAI models to reconsider due to fears that proprietary code and IP might be compromised.

**Tags**: `#apple`, `#openai`, `#trade-secrets`, `#legal`, `#ai-industry`

---

<a id="item-3"></a>
## [ClickHouse Scales PgBouncer to 4x Throughput with Process Peering](https://clickhouse.com/blog/pgbouncer-clickhouse-managed-postgres) ⭐️ 7.0/10

ClickHouse published a technical deep-dive detailing how they scaled PgBouncer to 4x throughput for their managed PostgreSQL service by combining process peering with the Linux SO_REUSEPORT socket option. The peering mechanism allows multiple PgBouncer processes to forward PostgreSQL query cancel requests to the correct process that owns the session, solving a critical limitation when running multiple pooler instances behind the same port. This is significant for any organization running managed PostgreSQL at scale, as connection pooling bottlenecks are a common pain point. The technique enables horizontal scaling of PgBouncer — a tool widely deployed but historically difficult to scale beyond a single process — making it viable for high-throughput cloud environments without switching to alternative poolers. The key insight is that when multiple PgBouncer instances share a port via SO_REUSEPORT (a Linux kernel 3.9+ socket option allowing multiple sockets to bind the same address:port), a query cancel may land on the wrong process; peering solves this by having processes forward cancels to the owning session. The setup requires configuring peering within PgBouncer and is deployable in Kubernetes by running multiple PgBouncer processes per pod or across multiple machines.

hackernews · saisrirampur · Jul 11, 15:28 · [Discussion](https://news.ycombinator.com/item?id=48872874)

**Background**: PostgreSQL uses a process-per-connection architecture, meaning each client connection spawns a dedicated backend process, which becomes expensive at high concurrency. PgBouncer is the most widely used connection pooler that sits between applications and PostgreSQL, multiplexing many client connections onto a small pool of actual database connections. Historically, PgBouncer was limited to a single process per instance, creating a throughput ceiling; alternatives like Odyssey and pgdog have attempted to address scalability differently.

<details><summary>References</summary>
<ul>
<li><a href="https://man7.org/linux/man-pages/man7/socket.7.html">socket(7) - Linux manual page</a></li>
<li><a href="https://dev.to/planetscale/scaling-postgres-connections-with-pgbouncer-aff">Scaling Postgres Connections With PgBouncer - DEV Community</a></li>
<li><a href="https://www.mafiree.com/blog/postgresql-connection-pooling-pgbouncer-vs-odyssey">PostgreSQL Connection Pooling Guide: PgBouncer vs Odyssey</a></li>

</ul>
</details>

**Discussion**: Community sentiment was engaged and technical. One commenter recommended Odyssey as an already-scalable PgBouncer alternative, while another praised pgdog. A Kubernetes user shared practical experience running multiple PgBouncer processes both within and across machines, noting Azure's rolling outages as motivation for multi-machine setups. Several commenters asked for clarification on how peering is configured within PgBouncer, indicating it is a relatively lesser-known technique.

**Tags**: `#postgresql`, `#pgbouncer`, `#performance-optimization`, `#connection-pooling`, `#database-infrastructure`

---

<a id="item-4"></a>
## [HuggingFace's Guide to Profiling Attention in PyTorch](https://huggingface.co/blog/torch-attention-profile) ⭐️ 7.0/10

HuggingFace has published Part 3 of its PyTorch profiling series, titled 'Profiling in PyTorch (Part 3): Attention is all you profile,' which provides a detailed technical walkthrough of profiling attention mechanisms to optimize transformer model performance. Attention is one of the most significant computational bottlenecks in transformer architectures, making it a prime target for performance optimization. This guide equips ML engineers with practical profiling techniques to identify inefficiencies and accelerate both training and inference workloads. The post leverages PyTorch's built-in torch.profiler module, which supports features such as customizable scheduling (wait/warmup/active phases), stack tracing, and trace export for visual analysis. As part of a structured series, it builds upon prior profiling concepts while focusing specifically on attention-specific bottlenecks such as memory access patterns and kernel-level GPU utilization.

rss · HuggingFace Blog · Jul 10, 00:00

**Background**: The Transformer architecture, introduced by Vaswani et al. in 2017, relies entirely on attention mechanisms to capture relationships between input and output tokens, dispensing with recurrent connections. While highly effective, the attention operation scales quadratically with sequence length and is known as a major performance bottleneck. PyTorch's torch.profiler provides a native toolkit for capturing detailed execution traces of model operations, enabling developers to measure GPU/CPU time, memory consumption, and kernel-level performance for individual operations, which is essential for diagnosing and resolving such bottlenecks in large-scale models.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.pytorch.org/tutorials/recipes/recipes/profiler_recipe.html">PyTorch Profiler — PyTorch Tutorials 2.13.0+cu130 documentation</a></li>
<li><a href="https://huggingface.co/docs/transformers/en/performance">Performance and Scalability</a></li>
<li><a href="https://www.aussieai.com/research/attention">Attention Optimization</a></li>

</ul>
</details>

**Tags**: `#pytorch`, `#profiling`, `#attention`, `#transformers`, `#performance-optimization`

---

<a id="item-5"></a>
## [Prefer strict tables in SQLite](https://evanhahn.com/prefer-strict-tables-in-sqlite/) ⭐️ 6.0/10

A blog post advocating for using SQLite's STRICT tables feature to enforce declared column types and prevent silent data corruption from type coercion.

hackernews · ingve · Jul 11, 17:33 · [Discussion](https://news.ycombinator.com/item?id=48873940)

**Tags**: `#sqlite`, `#databases`, `#best-practices`, `#data-types`, `#schema-design`

---

<a id="item-6"></a>
## [Einstein's Relativity Shapes Chemical Bonds in Heavy Elements](https://www.brown.edu/news/2026-07-09/chemical-bonds-relativity) ⭐️ 6.0/10

Research published in Science (DOI: 10.1126/science.aei1285) from Brown University characterizes how relativistic effects—specifically spin-orbit coupling—directly influence σ (sigma) and π (pi) bonding behavior in heavy elements, providing a more detailed mechanistic picture of how relativity governs chemistry in the lower rows of the periodic table. Heavy-element chemistry underpins superheavy element synthesis, catalysis, materials science, and nuclear waste processing, and accurate models of relativistic bonding are essential for predicting the behavior of elements that cannot be intuitively extrapolated from lighter analogs. The key physical mechanism is that as nuclear charge grows, inner electrons reach velocities approaching a significant fraction of the speed of light (e.g., ~60% for mercury), making relativistic corrections to their orbitals non-negligible. In this regime, an electron's spin magnetic moment and its orbital motion couple together (spin-orbit coupling), which alters how atomic orbitals overlap and form σ and π bonds.

hackernews · hhs · Jul 10, 22:30 · [Discussion](https://news.ycombinator.com/item?id=48866134)

**Background**: Relativistic quantum chemistry is a well-established subfield that combines special relativity with quantum mechanics to model systems where electrons move fast enough for Einstein's corrections to matter—primarily for heavier elements on the periodic table. Familiar textbook examples include mercury's liquid state at room temperature and gold's distinctive yellowish color, both rooted in relativistic contraction of inner orbitals. Spin-orbit interaction, first derived by Llewellyn Thomas in 1926, describes how an electron's intrinsic spin couples with its motion through an electric field—a purely relativistic phenomenon that becomes strong in heavy atoms. Sigma (σ) and pi (π) bonds are the two fundamental types of covalent bonds: σ bonds arise from head-on orbital overlap, while π bonds come from sideways overlap of p or d orbitals.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Relativistic_quantum_chemistry">Relativistic quantum chemistry - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Spin–orbit_interaction">Spin–orbit interaction - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/1506.07239">1 Origin of the Spin-Orbit Interaction</a></li>

</ul>
</details>

**Discussion**: Commenters largely appreciated the topic but debated its novelty: several, like nanolith, argued the core idea has been known for decades (citing gold's color and mercury being liquid as textbook examples), while gcanyon provided popular-science context about mercury's ~60% light-speed inner electrons. kristianp welcomed learning about σ/π bonds in this context, seanhunter added a tangential connection to the periodic table's symmetry group, and de6u99er framed it as continued validation of Einstein's century-old work.

**Tags**: `#chemistry`, `#physics`, `#relativity`, `#quantum-mechanics`, `#research`

---

<a id="item-7"></a>
## [AI 2040 and the cult of intelligence](https://geohot.github.io//blog/jekyll/update/2026/07/11/ai-2040.html) ⭐️ 6.0/10

George Hotz's contrarian essay critiquing AI doomerism and the 'cult of intelligence,' arguing against recursive self-improvement hard takeoff narratives and exploring AI's likely 2040 trajectory.

hackernews · rvz · Jul 11, 18:04 · [Discussion](https://news.ycombinator.com/item?id=48874200)

**Tags**: `#ai-safety`, `#ai-debate`, `#geohot`, `#doomerism`, `#agentic-ai`

---

<a id="item-8"></a>
## [VultronRetriever Embedding Models Claim #1 on MTEB Across Size Classes](https://www.reddit.com/r/MachineLearning/comments/1utmxq8/vultronretriever_family_of_models_released_on/) ⭐️ 6.0/10

Vultron released a family of three embedding models on HuggingFace—VultronRetrieverPrime-8B, Core-4.5B, and Flash-0.8B (all based on Qwen3.5)—each claiming the #1 position in its respective size class on the MTEB Leaderboard, with Prime-8B as the global leader. The models were demonstrated running Q&A and document embedding fully offline on an iPhone during the Raise Summit Paris event. If the MTEB rankings hold, this represents a significant advance in retrieval model efficiency, with Prime-8B claiming 16x smaller index storage and 12x higher throughput than previous 9B-class leaders. The demonstrated offline on-device capability could enable privacy-preserving, low-latency retrieval applications without cloud dependencies. The models use Vultron's 'Hydra Architecture' which combines late interaction retrieval (similar to ColBERT-style token-level matching) with generation capabilities at up to half the memory of comparable models. The Flash-0.8B variant reportedly indexes up to 60 images per minute offline, and the training methodology claims 0% cross-dataset duplication and 0% evaluation contamination with no overfitting on privately run MTEB evaluations.

reddit · r/MachineLearning · /u/madkimchi · Jul 11, 15:22

**Background**: MTEB (Massive Text Embedding Benchmark) is the standard benchmark for evaluating text embedding models across diverse tasks including classification, clustering, and retrieval, covering over 1000 languages. Late interaction retrieval is a paradigm that sits between bi-encoders (fast encoding but less precise matching) and cross-encoders (precise but computationally expensive), enabling token-level similarity computation while keeping query and document encoding independent. Edge AI deployment of retrieval models is increasingly important for privacy-sensitive and latency-critical applications.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/mteb">mteb ( Massive Text Embedding Benchmark )</a></li>
<li><a href="https://weaviate.io/blog/late-interaction-overview">An Overview of Late Interaction Retrieval Models: ColBERT , ColPali...</a></li>
<li><a href="https://jina.ai/news/what-is-colbert-and-late-interaction-and-why-they-matter-in-search/">What is ColBERT and Late Interaction and Why They Matter in Search?</a></li>

</ul>
</details>

**Tags**: `#retrieval`, `#embeddings`, `#MTEB`, `#edge-AI`, `#model-release`

---