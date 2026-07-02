---
layout: default
title: "Horizon Summary: 2026-07-02 (EN)"
date: 2026-07-02
lang: en
---

> From 52 items, 11 important content pieces were selected

---

1. [Since Linux 6.9, LUKS suspend stopped wiping disk-encryption keys from memory](#item-1) ⭐️ 7.0/10
2. [Podman v6.0.0 Released with Networking and Quadlet Improvements](#item-2) ⭐️ 7.0/10
3. [Japan's Top Court Rules AI Cannot Be Listed as Patent Inventor](#item-3) ⭐️ 7.0/10
4. [Hugging Face and Cerebras Partner on Real-Time Gemma 4 Voice AI](#item-4) ⭐️ 7.0/10
5. [arXiv to Spin Out from Cornell as Independent Nonprofit in 2026](#item-5) ⭐️ 7.0/10
6. [Ollama v0.31.1: Up to 90% Faster Gemma 4 on Apple Silicon](#item-6) ⭐️ 6.0/10
7. [Virginia bans sale of geolocation data](#item-7) ⭐️ 6.0/10
8. [PeerTube: A Decentralized, Federated Open-Source Video Platform](#item-8) ⭐️ 6.0/10
9. [Spain Orders Blacklist of Palantir from Public and Private Companies](#item-9) ⭐️ 6.0/10
10. [Differential Geometry Perspective on Hamiltonian Neural Networks](#item-10) ⭐️ 6.0/10
11. [P Moth-Retrieval: Graph-Free Multi-Hop Retrieval via Query-Time Orchestration (Beating Graph-Based Systems on HotpotQA) (P)](#item-11) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Since Linux 6.9, LUKS suspend stopped wiping disk-encryption keys from memory](https://mathstodon.xyz/@iblech/116769502749142438) ⭐️ 7.0/10

A silent security regression in Linux 6.9 caused LUKS suspend to stop wiping disk-encryption keys from memory, discovered via NixOS tests and since fixed.

hackernews · IngoBlechschmid · Jul 2, 15:25 · [Discussion](https://news.ycombinator.com/item?id=48763035)

**Tags**: `#linux`, `#security`, `#luks`, `#encryption`, `#kernel`

---

<a id="item-2"></a>
## [Podman v6.0.0 Released with Networking and Quadlet Improvements](https://blog.podman.io/2026/07/introducing-podman-v6-0-0/) ⭐️ 7.0/10

Podman v6.0.0 has been released, introducing improved networking capabilities, enhanced quadlet management, and automatic migration from the legacy BoltDB store to SQLite. The release also adds the new `podman quadlet list` subcommand (originally added in v5.6.0) and a `podman system migrate --migrate-db` flag (added in v5.8.0) to ease database transitions. As a major version of a leading Docker alternative, Podman v6.0.0 reinforces the viability of daemonless, rootless container workflows for teams seeking reduced attack surfaces and Docker-compatible tooling. The automatic SQLite migration lowers the operational burden for existing users, while continued quadlet maturation makes systemd-native container management more practical for production deployments. The transition from BoltDB to SQLite resolves long-standing deprecation warnings and provides a more robust, widely-supported embedded database backend. Networking improvements enhance Podman's compatibility with Docker networking semantics, which matters for users migrating `docker-compose.yml` stacks without modification. Quadlets—declarative systemd unit files for managing containers, pods, volumes, and networks—remain the centerpiece of Podman's rootless-first philosophy.

hackernews · soheilpro · Jul 2, 14:23 · [Discussion](https://news.ycombinator.com/item?id=48762098)

**Background**: Podman is an open-source container management tool originally developed by Red Hat that runs containers without requiring a long-running daemon, in contrast to Docker's daemon-based architecture. This daemonless design reduces the attack surface and allows rootless container execution, where unprivileged users can run containers without elevated permissions. Quadlets, introduced in Podman 4.4, let users declare containers and related resources in systemd unit files, integrating container lifecycle management with the standard Linux init system. Podman maintains CLI compatibility with Docker, allowing many existing workflows and `docker-compose.yml` files to work with minimal or no changes.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.podman.io/en/latest/markdown/podman-quadlet.1.html">podman-quadlet — Podman documentation</a></li>
<li><a href="https://www.redhat.com/en/blog/quadlet-podman">Make systemd better for Podman with Quadlet</a></li>
<li><a href="https://www.freecodecamp.org/news/how-to-use-different-container-runtimes-docker-podman-and-containerd-explained/">How to Use Different Container Runtimes: Docker, Podman, and Containerd Explained</a></li>

</ul>
</details>

**Discussion**: Community sentiment is strongly positive, with users praising Podman as a superior implementation to Docker and sharing successful migration stories—particularly from teams driven away by Docker Desktop's memory consumption issues. Experienced users highlighted the SQLite migration tools and quadlet list command as long-awaited conveniences, while others discussed rootless image builds for CRI-compatible runtimes and shared Ansible-based quadlet deployment templates. No significant criticisms were raised.

**Tags**: `#podman`, `#containers`, `#devops`, `#rootless`, `#infrastructure`

---

<a id="item-3"></a>
## [Japan's Top Court Rules AI Cannot Be Listed as Patent Inventor](https://japannews.yomiuri.co.jp/science-nature/technology/20260306-314930/) ⭐️ 7.0/10

Japan's Supreme Court has ruled that artificial intelligence systems cannot be designated as inventors on patent applications, reinforcing that only natural persons can hold inventorship status under Japanese patent law. This ruling adds Japan to a growing list of major jurisdictions—including the US, UK, and EU—that have rejected AI inventorship, shaping international precedent and affecting how companies protect AI-generated innovations across global markets. The ruling aligns Japan with the conclusions reached in the landmark Thaler v. Comptroller-General case in the UK and consistent with USPTO guidance stating that AI-assisted inventions still require a human inventor. Companies using AI in R&D will need to identify human contributors to satisfy inventorship requirements, though AI-assisted inventions themselves may still be patentable.

hackernews · mushstory · Jul 2, 13:43 · [Discussion](https://news.ycombinator.com/item?id=48761536)

**Background**: The question of AI inventorship gained global prominence through the DABUS case, in which Dr. Stephen Thaler filed patent applications listing his AI system 'DABUS' (Device for the Autonomous Bootstrapping of Unified Sentence) as the inventor for inventions like a fractal-geometry food container. Courts in the US, UK, Australia, and Europe have all rejected the idea that AI can be a legal inventor, but the underlying issue remains contested. While AI cannot be an inventor, many jurisdictions allow patents on inventions where AI played a significant role, provided a human is named as the inventor.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/DABUS">DABUS - Wikipedia</a></li>
<li><a href="https://www.uspto.gov/subscription-center/2025/revised-inventorship-guidance-ai-assisted-inventions">Revised inventorship guidance for AI-assisted inventions</a></li>
<li><a href="https://www.congress.gov/crs_external_products/LSB/PDF/LSB11251/LSB11251.3.pdf">Artificial Intelligence and Patent Law - Congress.gov</a></li>

</ul>
</details>

**Discussion**: Community sentiment was largely supportive of the ruling, with commenters emphasizing that AI lacks accountability and therefore should not receive patent benefits. Some raised practical legal questions about whether AI-generated inventions can be re-filed with a human inventor's name. A few comments challenged the very premise of patents, citing economic research suggesting patents don't necessarily improve innovation outcomes, while others dismissed the debate as obvious given AI is merely a software program.

**Tags**: `#AI`, `#patent-law`, `#intellectual-property`, `#legal-ruling`, `#Japan`

---

<a id="item-4"></a>
## [Hugging Face and Cerebras Partner on Real-Time Gemma 4 Voice AI](https://huggingface.co/blog/cerebras-gemma4-voice-ai) ⭐️ 7.0/10

Hugging Face and Cerebras have announced a partnership to enable real-time voice AI using Google's open-source Gemma 4 model running on Cerebras's wafer-scale inference hardware. The integration specifically targets the low-latency requirements of conversational voice applications. Real-time voice AI requires end-to-end inference latency low enough for natural conversation — typically under about 150 ms — which has been a major deployment hurdle for open models. Pairing Gemma 4's encoder-free multimodal architecture with Cerebras's high-throughput inference hardware could make low-latency, open-weights voice agents significantly more practical and accessible. Cerebras's WSE-3 is the world's largest AI processor, a single chip the size of a full silicon wafer that delivers very high on-chip memory bandwidth — a key factor for fast LLM inference. Gemma 4 itself uses an encoder-free multimodal design that integrates audio and vision directly into the language model, eliminating the additional latency typically added by separate vision/audio encoders.

rss · HuggingFace Blog · Jul 1, 00:00

**Background**: Cerebras Systems builds wafer-scale processors — essentially entire silicon wafers used as single AI chips — that deliver very high memory bandwidth to accelerate both training and inference. Google's Gemma is a family of open-weights models derived from the Gemini line; Gemma 4 was released with both Dense and Mixture-of-Experts variants, a 256K-token context window, support for over 140 languages, and native multimodal capabilities. Hugging Face is the dominant hub for open-model distribution and inference tooling, making it a natural launch partner. For voice agents to feel natural in conversation, total end-to-end latency must stay below roughly 150 milliseconds — a tight budget that has historically pushed developers toward heavily optimized proprietary stacks.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Cerebras_Systems">Cerebras Systems - Wikipedia</a></li>
<li><a href="https://ai.google.dev/gemma/docs/core/model_card_4">Gemma 4 model card | Google AI for Developers</a></li>

</ul>
</details>

**Tags**: `#voice-ai`, `#hugging-face`, `#cerebras`, `#gemma`, `#real-time-inference`

---

<a id="item-5"></a>
## [arXiv to Spin Out from Cornell as Independent Nonprofit in 2026](https://www.reddit.com/r/MachineLearning/comments/1ukjtlm/on_july_1_2026_arxiv_will_spin_out_from_cornell/) ⭐️ 7.0/10

On July 1, 2026, arXiv will spin out from Cornell University—its institutional home for 25 years—to become an independent nonprofit organization, supported by major funding from the Simons Foundation and Schmidt Sciences. The transition also marks a visual change, with arXiv dropping its signature red branding for a new look. arXiv is the world's most widely used preprint server, hosting millions of papers across physics, mathematics, computer science, and other fields, making it critical research infrastructure for the global scientific community. Securing its financial and institutional independence under major philanthropic backers ensures its long-term sustainability and protects the open-access model that underpins modern scientific communication. The spin-out is backed by two major philanthropic organizations: the Simons Foundation, a longstanding supporter of mathematics and basic science research, and Schmidt Sciences, founded in 2024 by former Google CEO Eric Schmidt and Wendy Schmidt. The change in institutional structure is accompanied by a rebranding away from arXiv's long-familiar red color scheme.

reddit · r/MachineLearning · /u/Nunki08 · Jul 1, 12:07

**Background**: arXiv, founded in 1991 and hosted by Cornell University since the early 2000s, is an open-access repository of scientific preprints—papers shared publicly before or alongside formal peer review. It allows researchers to disseminate findings rapidly and is particularly dominant in fields like physics, astronomy, mathematics, and machine learning. Preprint servers like arXiv, bioRxiv, and medRxiv have become essential infrastructure for fast-moving scientific communities, though the papers posted are not peer reviewed. The Simons Foundation and Schmidt Sciences are both major philanthropies that fund scientific research and open science initiatives.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ArXiv">arXiv - Wikipedia</a></li>
<li><a href="https://www.schmidtsciences.org/">Home - Schmidt Sciences</a></li>
<li><a href="https://scienceinsights.org/what-is-a-preprint-meaning-servers-and-peer-review/">What Is a Preprint? Meaning, Servers, and Peer Review</a></li>

</ul>
</details>

**Tags**: `#arxiv`, `#open-science`, `#research-infrastructure`, `#preprint-server`, `#academic-publishing`

---

<a id="item-6"></a>
## [Ollama v0.31.1: Up to 90% Faster Gemma 4 on Apple Silicon](https://github.com/ollama/ollama/releases/tag/v0.31.1) ⭐️ 6.0/10

Ollama v0.31.1 delivers up to 90% faster Gemma 4 inference on Apple Silicon by automatically tuning multi-token prediction (MTP), with the speedup enabled by default and no model output changes. The release also includes a tightened Gemma 4 MoE model loading path, an updated MLX engine with a new small-batch matmul kernel, and an upstream llama.cpp bump to build 9840. For developers running local LLMs on Macs — especially coding agents built on Gemma 4 — this is one of the largest single-version inference speedups reported by Ollama, materially improving the responsiveness and viability of on-device agent workflows. It also signals that MTP-style speculative decoding is maturing as a default optimization in mainstream local runtimes rather than a niche experimental feature. The MTP speedup is auto-tuned at runtime — Ollama dynamically decides how many draft tokens to generate — so users get the benefit without configuration and without risking altered outputs. The underlying gains come from a combination of MLX engine improvements (including a new small-batch matmul kernel better suited to Gemma 4's MoE routing) and llama.cpp build 9840, suggesting the win is not solely from MTP but from co-tuned engine changes.

github · github-actions[bot] · Jun 30, 22:10

**Background**: Multi-Token Prediction (MTP) is a technique, popularized by Meta and DeepSeek, in which a model drafts several future tokens at once that are then verified in parallel, dramatically improving inference throughput without changing outputs. MLX is Apple's open-source array framework for machine learning on Apple Silicon, designed to run efficiently on M-series chips via unified memory. Gemma 4 is Google's open-weights model family that uses a Mixture-of-Experts (MoE) architecture for portions of its capacity, where only a subset of expert subnetworks is activated per token — making efficient small-batch kernels especially important. Ollama is a popular open-source runtime that packages llama.cpp and MLX backends to let users run large language models locally with simple commands.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/multi-token-prediction-mtp">Multi - Token Prediction ( MTP )</a></li>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/ mlx : MLX : An array framework for Apple silicon</a></li>
<li><a href="https://en.wikipedia.org/wiki/Mixture_of_experts">Mixture of experts - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#ollama`, `#apple-silicon`, `#gemma`, `#inference-optimization`, `#multi-token-prediction`

---

<a id="item-7"></a>
## [Virginia bans sale of geolocation data](https://www.hunton.com/privacy-and-cybersecurity-law-blog/virginia-bans-sale-of-geolocation-data) ⭐️ 6.0/10

Virginia has banned the sale of geolocation data, becoming one of the first states to enact such legislation, taking effect July 1.

hackernews · toomuchtodo · Jul 2, 21:03 · [Discussion](https://news.ycombinator.com/item?id=48767347)

**Tags**: `#privacy`, `#data-protection`, `#legislation`, `#geolocation`, `#cybersecurity`

---

<a id="item-8"></a>
## [PeerTube: A Decentralized, Federated Open-Source Video Platform](https://github.com/Chocobozzz/PeerTube) ⭐️ 6.0/10

A Hacker News discussion featuring 432 points and 190 comments surfaced PeerTube, an established open-source federated video platform built on the ActivityPub protocol, highlighting both its technical capabilities and practical adoption challenges. PeerTube represents one of the few viable alternatives to centralized video platforms like YouTube, and the community discussion reveals critical barriers — monetization, content discovery, and audience reach — that any decentralized video platform must overcome to compete with mainstream incumbents. PeerTube uses P2P technology (WebTorrent) to distribute bandwidth among concurrent viewers and leverages ActivityPub for federation across independently operated instances. One user successfully uses it to host open-source tutorial videos via embedded players on third-party sites, bypassing YouTube's identity verification requirements.

hackernews · doener · Jul 2, 11:17 · [Discussion](https://news.ycombinator.com/item?id=48759634)

**Background**: PeerTube is built on ActivityPub, a W3C-standardized protocol for decentralized social networking that defines both client-to-server and server-to-server APIs, forming the backbone of the Fediverse — a network of interconnected platforms like Mastodon and Pixelfed. Federated architecture allows independent servers (instances) to interoperate and share content while remaining autonomously operated. PeerTube applies this model specifically to video hosting, adding P2P bandwidth sharing to reduce server costs, which is critical for a media type far more resource-intensive than text or images.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/ActivityPub">ActivityPub - Wikipedia</a></li>
<li><a href="https://github.com/w3c/activitypub">GitHub - w3c/activitypub</a></li>
<li><a href="https://en.wikipedia.org/wiki/Federated_architecture">Federated architecture - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters converge on the view that PeerTube is technically promising but faces significant social and economic hurdles. A professional YouTuber with ~100K subscribers stresses that the absence of monetization makes it impractical for full-time creators, given that high-quality video production can demand 40+ hours of skilled labor per 20-minute video. Other users note that content ecosystems remain thin outside of open-source and privacy niches, and that competing with TikTok and YouTube's algorithmic feeds requires more than just a `<video>` element. However, one active user reports a successful niche use case hosting FOSS-produced tutorial videos for an open-source project.

**Tags**: `#open-source`, `#decentralization`, `#video-platform`, `#federation`, `#activitypub`

---

<a id="item-9"></a>
## [Spain Orders Blacklist of Palantir from Public and Private Companies](https://clashreport.com/world/articles/spain-orders-blacklist-of-us-tech-giant-palantir-from-public-and-private-companies-fsnc2z17gjv) ⭐️ 6.0/10

Spain has ordered public and private companies to blacklist US tech giant Palantir Technologies, citing national security concerns over the company's handling of classified data. The decision stems from growing official concern over potential misuse of classified information linked to national security. This move represents a significant geopolitical stance by a major EU member state against a prominent US defense and intelligence technology contractor. It could set a precedent for other European nations reassessing their dependence on American data analytics platforms for sensitive government workloads. The blacklist reportedly applies to both public and private sector companies, suggesting Spain is extending restrictions beyond just government procurement. Palantir, founded in 2003 by Peter Thiel, Alex Karp, and others, specializes in data integration and analytics software widely used by federal agencies for military intelligence and government operations.

hackernews · mgh2 · Jul 2, 15:02 · [Discussion](https://news.ycombinator.com/item?id=48762725)

**Background**: Palantir Technologies is an American publicly traded company headquartered in Miami, Florida, founded in 2003 by Peter Thiel, Stephen Cohen, Joe Lonsdale, Alex Karp, and Nathan Gettings. The company develops data integration and analytics software, and its customer base includes federal agencies, state and local governments, as well as private enterprises. Palantir is well known for providing intelligence and defense-related software to government clients, which has made it both strategically important and politically controversial, particularly regarding data privacy and sovereignty concerns in Europe.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Palantir">Palantir - Wikipedia</a></li>
<li><a href="https://builtin.com/articles/what-is-palantir">What Is Palantir? The Company Behind Government AI Tools ...</a></li>
<li><a href="https://www.palantir.com/">Home | Palantir</a></li>

</ul>
</details>

**Discussion**: Community sentiment is mixed. Some commenters praise Spain's direction and express interest in similar moves by other countries, while others are skeptical, suggesting the real motivation may be procurement preferences favoring domestic or allied vendors (such as China's Huawei equivalents or Spain's own Indra) rather than genuine security concerns. Several users requested more specific information about the actual national security threats cited, and one commenter pointed to Palantir's CEO as appearing out of touch.

**Tags**: `#palantir`, `#tech-policy`, `#national-security`, `#europe`, `#government-procurement`

---

<a id="item-10"></a>
## [Differential Geometry Perspective on Hamiltonian Neural Networks](https://www.reddit.com/r/MachineLearning/comments/1ukzdnj/hamiltonian_neural_networks_from_a_differential/) ⭐️ 6.0/10

A company blog post offers a differential-geometry reframing of Hamiltonian Neural Networks (Greydanus et al., 2019), arguing that Noether's Theorem provides the missing link between conservation laws and generalization in physics-informed neural networks. Most tutorials on HNNs focus on the loss function mechanics, leaving practitioners without intuition for why these architectures generalize. By tying the framework to symmetry principles via Noether's Theorem, the post offers a conceptual grounding that could help researchers design more effective physics-informed models and understand inductive biases in dynamical system learning. The post is math-heavy but includes interactive visuals and tension-relieving elements; it positions Noether's Theorem—the correspondence between continuous symmetries and conserved quantities—as central to understanding how physics-informed networks achieve generalization rather than overfitting.

reddit · r/MachineLearning · /u/FlameOfIgnis · Jul 1, 21:55

**Background**: Hamiltonian Neural Networks, introduced by Greydanus et al. in 2019, parameterize the Hamiltonian of a physical system with a neural network and learn it from data, using the canonical coordinates of position (q) and momentum (p). This structure guarantees conservation of energy by construction, addressing a key weakness of generic neural networks that can violate physical laws. Noether's Theorem, originally formulated by mathematician Emmy Noether, establishes that every continuous symmetry of a physical system corresponds to a conserved quantity, and has recently been connected to machine learning through works such as Noether's Razor and Noether Networks, which leverage symmetries as inductive biases to improve generalization.

<details><summary>References</summary>
<ul>
<li><a href="https://greydanus.github.io/2019/05/15/hamiltonian-nns/">Hamiltonian Neural Networks</a></li>
<li><a href="https://fabianfuchsml.github.io/noether/">Noether’s Theorem, Symmetries, and Invariant Neural Networks Noether’s Razor: Learning Conserved Quantities - arXiv.org Noether’s Razor: Learning Conserved Quantities AI Meets Noether’s Theorem – Symmetry, Conservation Laws, and ... [2105.02716] Noether's Learning Dynamics: Role of Symmetry ... Noether Networks: meta-learning useful conserved quantities</a></li>
<li><a href="https://arxiv.org/html/2410.08087v1">Noether’s Razor: Learning Conserved Quantities - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#Hamiltonian Neural Networks`, `#Differential Geometry`, `#Physics-Informed ML`, `#Noether's Theorem`, `#Neural ODEs`

---

<a id="item-11"></a>
## [P Moth-Retrieval: Graph-Free Multi-Hop Retrieval via Query-Time Orchestration (Beating Graph-Based Systems on HotpotQA) (P)](https://www.reddit.com/r/MachineLearning/comments/1ukotww/p_mothretrieval_graphfree_multihop_retrieval_via/) ⭐️ 6.0/10

MOTHRAG is an open-source graph-free multi-hop RAG framework using query-time orchestration over a dense index, reporting benchmark results that exceed GraphRAG, HippoRAG, and RAPTOR on HotpotQA, 2WikiMultiHopQA, and MuSiQue while supporting incremental updates without re-indexing.

reddit · r/MachineLearning · /u/Annual-Commercial563 · Jul 1, 15:26

**Tags**: `#RAG`, `#multi-hop-retrieval`, `#knowledge-graph`, `#dense-retrieval`, `#open-source`

---