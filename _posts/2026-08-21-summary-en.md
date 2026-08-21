---
layout: default
title: "Horizon Summary: 2026-08-21 (EN)"
date: 2026-08-21
lang: en
---

> From 41 items, 13 important content pieces were selected

---

1. [Felony charges for citizen deleting phone data at US Border](#item-1) ⭐️ 7.0/10
2. [Researcher accidentally logs military phone calls via legacy ENUM DNS](#item-2) ⭐️ 7.0/10
3. [DeepSeek Releases Experimental Vision Capabilities for V4 Flash Model](#item-3) ⭐️ 7.0/10
4. [AI companies destroy physical books – let's scan rare books before it's too late](#item-4) ⭐️ 7.0/10
5. [Measuring Benchmark Over-Optimization in ASR Models](#item-5) ⭐️ 7.0/10
6. [Liquid AI Launches LFM2.5-DSpark: Up to 3.2x Faster Inference](#item-6) ⭐️ 7.0/10
7. [Ox Alpha reportedly hits 96% on SWE-bench Verified Mini, but author urges skepticism](#item-7) ⭐️ 7.0/10
8. [The Rise of AI-Blindness: Why Readers Dismiss AI Text](#item-8) ⭐️ 6.0/10
9. [DeepMind Partners with Game Studios on AI Prototypes After 15 Years](#item-9) ⭐️ 6.0/10
10. [NVIDIA AVO Achieves Perfect Score on ARC-AGI-3 Benchmark](#item-10) ⭐️ 6.0/10
11. [FireRedTeam Releases FireRedAudio and FireRedTTS3 Open-Source Audio Models](#item-11) ⭐️ 6.0/10
12. [Fastest NVFP4 quant of Qwen3.8 27B out there](#item-12) ⭐️ 6.0/10
13. [model: add dots3-note by ngxson · Pull Request #27060 · ggml-org/llama.cpp](#item-13) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Felony charges for citizen deleting phone data at US Border](https://www.nytimes.com/2026/08/21/us/politics/samuel-tunick-deleted-phone-felony.html) ⭐️ 7.0/10

A US citizen faces felony charges for deleting phone data at a US border, raising serious concerns about digital privacy rights and border search authority.

hackernews · floathub · Aug 21, 12:10 · [Discussion](https://news.ycombinator.com/item?id=49386895)

**Tags**: `#digital-privacy`, `#civil-liberties`, `#border-security`, `#smartphone-security`, `#legal-policy`

---

<a id="item-2"></a>
## [Researcher accidentally logs military phone calls via legacy ENUM DNS](https://lina.sh/blog/hijacking-e164-arpa) ⭐️ 7.0/10

A security researcher discovered that they had inadvertently logged hundreds of thousands of phone calls—including ones to military bases—by running what they thought was a personal experiment against the legacy e164.arpa ENUM DNS system, which still processes real telephony routing queries despite being considered obsolete. This incident highlights that supposedly 'dead' telecom infrastructure still carries live, sensitive traffic—including government and military communications—without active stewardship. It raises urgent questions about who is responsible for maintaining legacy systems like public ENUM and what other neglected infrastructure may be silently routing classified or private data. A 2026 RIPE Labs operational review found that half of all current public ENUM delegations under e164.arpa exhibit some form of DNS problem, underscoring the systemic neglect of this infrastructure. ENUM was originally designed by the IETF to map E.164 telephone numbers to SIP URIs via DNS, enabling convergence between traditional telephony and VoIP, but the public tier essentially collapsed while private/infrastructure ENUM persisted behind VPNs for number porting lookups.

hackernews · gavide · Aug 21, 13:11 · [Discussion](https://news.ycombinator.com/item?id=49387570)

**Background**: ENUM (Telephone Number Mapping) is a suite of protocols that maps international E.164 telephone numbers to internet resources such as SIP URIs using the DNS system, with the special domain e164.arpa reserved for this purpose. The concept was envisioned in the late 1990s as a way to unify the global telephone numbering system with internet addressing, but public ENUM deployments never gained meaningful adoption. Meanwhile, a parallel 'infrastructure ENUM' use case—where carriers use ENUM-style DNS queries over private networks for number portability lookups—continued to operate quietly, meaning real call signaling traffic has been flowing through infrastructure originally meant for an entirely different purpose.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ripe.net/manage-ips-and-asns/dns/enum/">ENUM — RIPE Network Coordination Centre</a></li>
<li><a href="https://en.wikipedia.org/wiki/Telephone_number_mapping">Telephone number mapping - Wikipedia</a></li>
<li><a href="https://labs.ripe.net/author/hisham_ibrahim/operational-review-of-public-enum-under-e164arpa/">Operational Review of Public ENUM Under e164.arpa | RIPE Labs</a></li>

</ul>
</details>

**Discussion**: Community commenters provided rich insider context: toast0 clarified that e164.arpa/ENUM is not truly dead but continues to operate privately via VPN for number porting services; chaz6 lamented the author didn't set up a SIP server to see if any calls actually terminated and pointed to the related TRIP protocol; dmd expressed surprise the researcher wasn't jailed for possessing logs of military calls; cryptolobster noted it took military involvement to get anyone to address the long-standing issue, while dkga praised the article as a great example of how things simply fall through the cracks.

**Tags**: `#security`, `#telecom-infrastructure`, `#DNS`, `#vulnerability-disclosure`, `#ENUM`

---

<a id="item-3"></a>
## [DeepSeek Releases Experimental Vision Capabilities for V4 Flash Model](https://api-docs.deepseek.com/guides/vision/) ⭐️ 7.0/10

DeepSeek has launched experimental vision capabilities for its DeepSeek-V4-Flash model, allowing images to be tokenized and billed alongside text tokens via API. Images smaller than roughly 384×384 pixels are upscaled, while larger images are downscaled to approximately 800×800 total pixels while preserving aspect ratio. This brings multimodal capabilities to one of the most capable open-weight models at highly competitive pricing ($0.14/$0.28 per million tokens), potentially lowering the barrier for developers building vision-enabled workflows. It directly addresses a long-standing limitation where DeepSeek models would hallucinate vision capabilities despite lacking them, causing broken agent sessions. The 800×800 downscaling limit may be insufficient for OCR tasks involving full A4/Letter-sized documents, as noted by community testers. Early evaluations show the model struggles with simple visual reasoning like reading analog clock times, where smaller open models like Qwen 8B-27B perform better.

hackernews · dares2573 · Aug 21, 10:33 · [Discussion](https://news.ycombinator.com/item?id=49386163)

**Background**: DeepSeek-V4-Flash is a 304B-parameter sparse Mixture-of-Experts (MoE) language model designed for text generation, coding, reasoning, and agentic workflows, with a 1M token context window. Vision Language Models (VLMs) extend standard LLMs by adding the ability to process images alongside text: images are typically split into patches, converted into embeddings, and then tokenized so the model can reason over visual content just as it does over words. Prior DeepSeek models lacked native vision support, meaning developers had to use separate models for image understanding, which complicated agent workflows that needed to interpret screenshots or UI elements.

<details><summary>References</summary>
<ul>
<li><a href="https://deepseek-v4.io/architecture">DeepSeek V4 Architecture: MoE, Parameters & 1M Context</a></li>
<li><a href="https://build.nvidia.com/deepseek-ai/deepseek-v4-flash-0731/modelcard">deepseek-v4-flash-0731 Model by Deepseek-ai | NVIDIA NIM</a></li>

</ul>
</details>

**Discussion**: Community sentiment is cautiously optimistic. Developers welcome the addition for coding workflows involving Playwright screenshots, where it fills a notable gap compared to models like Claude Sonnet. However, testers report concrete failures on simple tasks like reading analog clocks, and note that the 800×800 downscaling resolution may be too limiting for OCR and document scanning applications. Several users also highlight that prior DeepSeek versions would hallucinate vision capabilities, creating session-breaking behavior in agent workflows that this update directly addresses.

**Tags**: `#DeepSeek`, `#vision-models`, `#multimodal-AI`, `#LLM`, `#open-source-models`

---

<a id="item-4"></a>
## [AI companies destroy physical books – let's scan rare books before it's too late](https://annas-archive.gl/blog/physical-destruction.html) ⭐️ 7.0/10

Anna's Archive calls for crowdsourced digitization of rare books before AI companies purchase and physically destroy them for training data, sparking debate about copyright, preservation, and AI ethics.

hackernews · Cider9986 · Aug 21, 02:37 · [Discussion](https://news.ycombinator.com/item?id=49383026)

**Tags**: `#AI`, `#copyright`, `#knowledge-preservation`, `#training-data`, `#ethics`

---

<a id="item-5"></a>
## [Measuring Benchmark Over-Optimization in ASR Models](https://huggingface.co/blog/asr-benchmark-optimization) ⭐️ 7.0/10

HuggingFace published a blog analyzing how automatic speech recognition (ASR) models become over-optimized for specific benchmarks like LibriSpeech, and proposed methods to measure and address the resulting generalization gap between benchmark performance and real-world deployment. Benchmark overfitting in ASR is a significant reproducibility and deployment concern: models that report state-of-the-art numbers on LibriSpeech may underperform on diverse real-world audio, misleading practitioners about real capabilities and slowing progress toward robust voice interfaces. The analysis focuses on LibriSpeech, a ~1,000-hour corpus of read English from LibriVox audiobooks that has become the de facto ASR benchmark, and highlights how models can be tuned to exploit its specific acoustic and linguistic characteristics rather than learning generalizable recognition skills.

rss · HuggingFace Blog · Aug 21, 00:00

**Background**: Automatic Speech Recognition (ASR) converts spoken language into text and underpins applications such as voice assistants, live captioning, and meeting transcription. LibriSpeech, derived from public-domain LibriVox audiobook recordings, has long served as the primary benchmark for English ASR due to its standardized train/test splits and clean studio-quality audio. However, because the field has converged on LibriSpeech for evaluation, there is a well-known risk—mirroring overfitting in other ML domains—that models are increasingly tailored to its idiosyncrasies rather than generalizing to the noisy, accented, and domain-diverse speech encountered in production settings. Multilingual LibriSpeech (MLS) partially extended the methodology to eight languages, but benchmark dependence remains a core methodological challenge.

<details><summary>References</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/librispeech">LibriSpeech | AI Wiki</a></li>
<li><a href="https://www.ibm.com/think/topics/overfitting">What is Overfitting? | IBM</a></li>
<li><a href="https://huggingface.co/docs/transformers/tasks/asr">Automatic speech recognition · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#speech-recognition`, `#benchmarking`, `#ASR`, `#model-evaluation`, `#HuggingFace`

---

<a id="item-6"></a>
## [Liquid AI Launches LFM2.5-DSpark: Up to 3.2x Faster Inference](https://huggingface.co/blog/LiquidAI/lfm25-dspark) ⭐️ 7.0/10

Liquid AI has released LFM2.5-DSpark, a speculative decoding optimization that delivers up to 3.2x faster inference for its LFM2.5 model family. Draft models for LFM2.5-1.2B-Instruct, LFM2.5-2.6B, and LFM2.5-8B-A1B are available on Hugging Face, with integration open-sourced in llama.cpp and SGLang. A 3.2x inference speedup at no loss in output quality directly reduces latency and compute costs for production LLM deployments, making it highly impactful for serving Liquid's models at scale. By open-sourcing the integration across llama.cpp and SGLang, Liquid AI makes the optimization accessible across two of the most widely used open-source inference frameworks. The DSpark drafters use a simplified attention-only architecture with five layers and a block size of nine draft tokens per speculative step, topped by a Markov head over a 128,000-token vocabulary. For example, the LFM2.5-2.6B-DSpark draft model has 327.7M parameters in BF16, with hidden_size=2048 and intermediate_size=6144, far smaller than its target model.

rss · HuggingFace Blog · Aug 20, 16:52

**Background**: Speculative decoding is an inference-time optimization technique for autoregressive large language models: a small draft model proposes several candidate tokens ahead of the target model, which then verifies all of them in a single forward pass via a modified rejection sampling scheme. Because the verification preserves the target model's original output distribution, the speedup comes without sacrificing output quality. DSpark is Liquid AI's specific instantiation of this approach, applying it to their LFM2.5 family.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Speculative_decoding">Speculative decoding - Wikipedia</a></li>
<li><a href="https://www.liquid.ai/blog/lfm2.5-dspark">LFM 2 . 5 - DSpark : Up to 3.2x Faster Inference from H100... — Liquid AI</a></li>
<li><a href="https://huggingface.co/LiquidAI/LFM2.5-2.6B-DSpark">LiquidAI/ LFM 2 . 5 -2.6B- DSpark · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#inference-optimization`, `#liquid-ai`, `#model-performance`, `#huggingface`, `#speculative-decoding`

---

<a id="item-7"></a>
## [Ox Alpha reportedly hits 96% on SWE-bench Verified Mini, but author urges skepticism](https://www.reddit.com/r/LocalLLaMA/comments/1vuke8o/i_benchmarked_ox_alpha_on_swebench_verified_mini/) ⭐️ 7.0/10

A Reddit user benchmarked the free-tier 'Ox Alpha' model on the 50-task SWE-bench Verified Mini subset and reported 48/50 (96%) resolved, using the official mini-swe-agent Bash-Only scaffold and the official SWE-bench Docker harness on a single Windows 11 machine with 4 parallel workers, completing the run in roughly 2 hours and 4 minutes. If independently confirmed, a free/open model surpassing Claude Opus 5 (97%), Claude Fable 5 (95%), and Claude Opus 4.8 (88.6%) would be a watershed moment for open-source coding agents, dramatically shifting expectations about the gap between proprietary and free models on agentic software engineering tasks. The run scored django 23/25 (failing django__django-11790 and django__django-11815) and sphinx-doc 25/25, with an average of 40 steps per task and a max of 116 steps; the author's caveats emphasize that the mini-50 subset covers only django and sphinx (two heavily represented repos in training data), n=50 implies roughly ±3 percentage points of sampling noise, and the free serving endpoint cannot be audited for caching or rate-limiting.

reddit · r/LocalLLaMA · /u/No_Tip9917 · Aug 21, 16:00

**Background**: SWE-bench Verified is a human-validated 500-task subset of the original SWE-bench dataset, used industry-wide to evaluate how well AI systems can resolve real GitHub issues by producing patches that pass hidden tests. The 'Verified-Mini' variant is a well-known 50-task slice curated to match the full set's difficulty distribution. The mini-swe-agent is a minimalist ~100-line Bash-Only agent scaffold maintained by the SWE-agent team; it intentionally strips away tool-calling layers so that the language model's own capabilities — not agent engineering — determine the score, making it the de facto baseline on the swebench.com Bash-Only leaderboard. Ox Alpha is a recently surfaced 'stealth' reasoning model advertised as a coding-focused model with a 1M-token context, accessed via a free tier on a third-party gateway.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/datasets/SWE-bench/SWE-bench_Verified">SWE-bench/SWE-bench_Verified · Datasets at Hugging Face</a></li>
<li><a href="https://github.com/SWE-agent/mini-swe-agent">GitHub - SWE-agent/mini-swe-agent: The 100 line AI agent that ...</a></li>
<li><a href="https://benchable.ai/models/stealth/ox-alpha">Ox Alpha - AI Model Details & Benchmarks</a></li>

</ul>
</details>

**Tags**: `#SWE-bench`, `#benchmarking`, `#open-source-LLMs`, `#code-agents`, `#Ox-Alpha`

---

<a id="item-8"></a>
## [The Rise of AI-Blindness: Why Readers Dismiss AI Text](https://cymerys.com/w/im-becoming-ai-blind) ⭐️ 6.0/10

A personal essay describes a growing psychological phenomenon in which readers automatically recognize and dismiss AI-generated text as low-value, forcing their brains into exhausting interpretive work. The Hacker News discussion (191 upvotes, 193 comments) elaborates on the underlying causes, pointing to AI's weakness in structural thinking and top-down synthesis as root reasons the text feels hollow. This shift in reader perception poses a strategic challenge for the billions of pieces of AI-generated content being published and for the businesses deploying LLMs for communication tasks. As audiences develop an unconscious filter against AI writing, the marginal value of raw LLM output drops sharply, potentially eroding trust in AI-assisted tools and pushing creators toward more carefully humanized workflows. Community commenters identified a specific LLM failure pattern: models like Claude tend to produce 'flattened spaghetti' code and group details without generalizing or synthesizing unifying concepts, resulting in writing that lacks top-down explanatory structure. One developer reported that AI-generated pull request comments are so structurally overwrought that they need to be replaced with manually written one-liners.

hackernews · rcymerys · Aug 21, 11:48 · [Discussion](https://news.ycombinator.com/item?id=49386699)

**Background**: The phenomenon described in the essay connects to a well-documented behavioral bias called 'algorithm aversion,' coined in 2015 by Berkeley Dietvorst and colleagues, which describes people's tendency to distrust algorithmic output even when it performs as well as or better than humans. The 'AI-blindness' framing extends this concept specifically to text generation, where the issue is not statistical accuracy but perceived depth of thought. Related research on LLM failure modes, such as a 2025 arXiv taxonomy of fifteen hidden system-level failures, helps explain why AI text often feels structurally deficient rather than merely wrong.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Algorithm_aversion">Algorithm aversion - Wikipedia</a></li>
<li><a href="https://arxiv.org/abs/2511.19933">[2511.19933] Failure Modes in LLM Systems: A System-Level Taxonomy for ...</a></li>
<li><a href="https://www.chicagobooth.edu/review/even-when-algorithms-outperform-humans-people-often-reject-them">Even When Algorithms Outperform Humans, People Often Reject Them | Chicago Booth Review</a></li>

</ul>
</details>

**Discussion**: The HN thread is notably substantive, with commenters converging on the idea that AI writing triggers a psychological short-circuit because the reader must supply missing meaning through creative interpretation. A recurring technical criticism is that LLMs like Claude cannot perceive the 'big picture,' producing flattened or overly detailed output that lacks the top-down synthesis a human expert would provide. Several developers shared concrete pain points, particularly around AI-generated code comments being structurally opaque and requiring manual replacement.

**Tags**: `#ai-generated-content`, `#human-ai-interaction`, `#perception`, `#llm-limitations`, `#content-quality`

---

<a id="item-9"></a>
## [DeepMind Partners with Game Studios on AI Prototypes After 15 Years](https://deepmind.google/blog/from-atari-to-eve-online-building-on-15-years-of-ai-research-in-games/) ⭐️ 6.0/10

Google DeepMind announced new partnerships with game studios to prototype breakthrough AI gameplay, marking a retrospective milestone of 15 years of AI research in games — from the original Atari DQN breakthrough to complex modern titles like EVE Online. This signals DeepMind's shift from purely academic benchmarks like Atari and StarCraft toward real-world commercial game environments, which could accelerate the deployment of reinforcement learning in production game systems and influence how future games are designed and tested. The announcement spans the evolution from DQN (Deep Q-Network), which played 49 Atari games with the same unmodified algorithm using only raw pixels and scores, to Agent57 — the first deep RL agent to beat the human baseline on all 57 Atari 2600 games — and now extends to massively multiplayer environments like EVE Online.

rss · Google DeepMind Blog · Aug 21, 11:59

**Background**: Deep reinforcement learning combines deep neural networks with reinforcement learning, allowing AI agents to learn optimal behaviors through trial-and-error interaction with an environment. DeepMind's 2013 DQN paper demonstrated that a single algorithm, given only screen pixels and a score signal, could master dozens of Atari games without game-specific engineering — a watershed moment that launched the modern deep RL research program. Subsequent milestones included AlphaGo, AlphaStar (StarCraft II), and Agent57, each tackling environments with progressively larger state spaces, longer time horizons, and multi-agent dynamics. EVE Online represents a particularly challenging frontier due to its massively multiplayer nature, persistent economy, and complex social interactions.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/blog/agent57-outperforming-the-human-atari-benchmark/">Agent57: Outperforming the human Atari ... — Google DeepMind</a></li>
<li><a href="https://medium.com/@sakethyalamanchili/deepminds-dqn-when-deep-learning-finally-learned-to-play-and-changed-everything-58b0e9db0b90">DeepMind ’s DQN : When Deep Learning Finally Learned to... | Medium</a></li>
<li><a href="https://vertexdigest.com/blogs/reinforcement-learning-games-deepmind">From Atari to StarCraft: How Reinforcement Learning Mastered...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Reinforcement Learning`, `#Game AI`, `#DeepMind`, `#Research`

---

<a id="item-10"></a>
## [NVIDIA AVO Achieves Perfect Score on ARC-AGI-3 Benchmark](https://www.reddit.com/r/LocalLLaMA/comments/1vuh7to/nvidia_avo_got_100_on_arcagi3_it_completed_all/) ⭐️ 6.0/10

NVIDIA's AVO, a general-purpose coding agent system, achieved 100% on the public ARC-AGI-3 benchmark, completing all 183 levels across 25 interactive environments without any instructions, stated rules, or defined goals. ARC-AGI-3 is specifically designed to resist memorization and test genuine generalization, so a perfect score—if verified—would mark a notable milestone in agentic AI capabilities. It also suggests that coding-agent architectures can be repurposed as general-purpose reasoning systems capable of autonomously exploring unfamiliar interactive environments. AVO operates like a modern coding agent—inspecting and editing code, running commands, consulting documentation, and validating work through execution—rather than as a specialized puzzle-solver. The result applies only to the public set, and the underlying methodology, model architecture, and compute requirements have not yet been publicly disclosed in detail.

reddit · r/LocalLLaMA · /u/theologi · Aug 21, 14:01

**Background**: ARC (Abstraction and Reasoning Corpus) is a benchmark series created by AI researcher François Chollet in 2019 to measure fluid, sample-efficient reasoning—the ability to solve novel problems with minimal prior exposure. While ARC-AGI-1 and ARC-AGI-2 used static grid puzzles, ARC-AGI-3 shifted to interactive agentic environments that require an AI system to explore, experiment, and adapt without explicit instructions. The benchmark is explicitly engineered to resist memorization and reward genuine generalization, making it one of the leading tests for progress toward artificial general intelligence.

<details><summary>References</summary>
<ul>
<li><a href="https://developer.nvidia.com/blog/nvidia-avo-reaches-100-on-arc-agi-3-demonstrating-a-frontier-level-general-purpose-architecture-for-long-horizon-autonomous-agents/">NVIDIA AVO Reaches 100% on ARC-AGI-3, Demonstrating...</a></li>
<li><a href="https://runtimewire.com/article/nvidia-avo-arc-agi-3-perfect-public-score">NVIDIA 's AVO scores 100% on ARC-AGI-3's public set</a></li>
<li><a href="https://www.emergentmind.com/topics/arc-agi-3">ARC - AGI - 3 : Interactive AGI Benchmark</a></li>

</ul>
</details>

**Tags**: `#ARC-AGI`, `#NVIDIA`, `#AGI-benchmark`, `#reasoning`, `#general-intelligence`

---

<a id="item-11"></a>
## [FireRedTeam Releases FireRedAudio and FireRedTTS3 Open-Source Audio Models](https://www.reddit.com/r/LocalLLaMA/comments/1vukj3m/fireredaudio_fireredtts3_by_fireredteam/) ⭐️ 6.0/10

FireRedTeam has open-sourced FireRedAudio, a 9B-parameter unified audio language model with decoupled continuous representations for understanding and generation tasks including ASR, zero-shot TTS, instruct TTS, speech editing, and temporal grounding of recordings up to one hour long. Alongside it, they released FireRedTTS3, a speech generation and editing system supporting zero-shot voice cloning across 24 languages and 21 Chinese dialects. This release consolidates a full audio stack—understanding, generation, editing, and temporal grounding—into open-source models with competitive benchmark results, potentially lowering barriers for developers building voice assistants, multilingual applications, and audio analysis tools. The architectural choice of decoupled representations sharing a single backbone could also influence future multimodal audio model design. FireRedAudio uses a shared 9B LLM backbone with two decoupled pathways: an Audio Encoder for understanding and a RedAE-Patch pathway for generation, claimed to be the first publicly disclosed design of its kind in a unified audio-language model. FireRedTTS3-Base achieves leading average WER/CER (3.754%) on MiniMax-MLS-Test and cloning WER/CER (3.04%) on Seed-TTS-eval, while the Instruct variant adds natural-language voice design plus both semantic (insertion/deletion/substitution) and acoustic (speed/pitch/volume) editing.

reddit · r/LocalLLaMA · /u/pmttyji · Aug 21, 16:05

**Background**: Audio language models extend text-based LLMs to handle speech and audio as both input and output. Traditional pipelines often relied on separate models for tasks such as ASR (automatic speech recognition) and TTS (text-to-speech), but recent research has moved toward unified architectures that share a single backbone across multiple audio tasks. Operating in a continuous latent space—rather than with discrete tokens—helps preserve fine-grained acoustic information for high-fidelity synthesis. Temporal grounding is an emerging capability that links events in long audio to specific timestamps, extending general audio understanding with precise time-to-content alignment.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2509.06926">[2509.06926] Continuous Audio Language Models - arXiv.org Bridging semantics across modalities: Decoupled ... Continuous Audio Language Models GitHub - HarunoriKawano/HEAR: Official implementation of "A ... (PDF) Continuous Audio Language Models - ResearchGate Continuous Audio Language Models - OpenReview</a></li>
<li><a href="https://arxiv.org/html/2602.10230v1">Frame-Level Internal Tool Use for Temporal Grounding in Audio LMs</a></li>
<li><a href="https://arxiv.org/html/2511.11039v1">TimeAudio: Bridging Temporal Gaps in Large Audio-Language Models</a></li>

</ul>
</details>

**Tags**: `#audio-language-model`, `#text-to-speech`, `#multimodal-AI`, `#open-source`, `#speech-recognition`

---

<a id="item-12"></a>
## [Fastest NVFP4 quant of Qwen3.8 27B out there](https://www.reddit.com/r/LocalLLaMA/comments/1vub9od/fastest_nvfp4_quant_of_qwen38_27b_out_there/) ⭐️ 6.0/10

New Blackwell-native NVFP4 quantization of a Qwen 27B model claims to be the fastest available, running 50% faster than Q4 and 4-7% faster than other NVFP4 quants on RTX 5090, with bonus MTP draft head optimization.

reddit · r/LocalLLaMA · /u/ionsago · Aug 21, 09:19

**Tags**: `#quantization`, `#NVFP4`, `#Blackwell`, `#RTX-5090`, `#local-llama`, `#speculative-decoding`

---

<a id="item-13"></a>
## [model: add dots3-note by ngxson · Pull Request #27060 · ggml-org/llama.cpp](https://www.reddit.com/r/LocalLLaMA/comments/1vunrrp/model_add_dots3note_by_ngxson_pull_request_27060/) ⭐️ 6.0/10

llama.cpp PR adds support for dots3-note, a new open-weight 280B MoE multimodal model with 16B active parameters and 512K context length.

reddit · r/LocalLLaMA · /u/jacek2023 · Aug 21, 18:03

**Tags**: `#llama.cpp`, `#open-source-models`, `#mixture-of-experts`, `#multimodal`, `#dots3-note`

---