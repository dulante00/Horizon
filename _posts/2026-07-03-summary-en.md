---
layout: default
title: "Horizon Summary: 2026-07-03 (EN)"
date: 2026-07-03
lang: en
---

> From 67 items, 16 important content pieces were selected

---

1. [Karpathy Launches nanochat: A ChatGPT Clone for $100](#item-1) ⭐️ 8.0/10
2. [huggingface/transformers released v5.13.0](#item-2) ⭐️ 7.0/10
3. [PostgreSQL and the OOM killer: Why we use strict memory overcommit](#item-3) ⭐️ 7.0/10
4. [Wordgard: New Rich-Text Editor from ProseMirror Creator](#item-4) ⭐️ 7.0/10
5. [60% Cost Cut: Converting Code to Images for LLM OCR Processing](#item-5) ⭐️ 7.0/10
6. [Mistral Releases Leanstral-1.5-119B-A6B for Formal Verification and Theorem Proving](#item-6) ⭐️ 7.0/10
7. [Greek MEP on Spyware Investigation Committee Hacked with Pegasus](#item-7) ⭐️ 6.0/10
8. [Jamesob's guide to running SOTA LLMs locally](#item-8) ⭐️ 6.0/10
9. [Valve open-sources Steam Machine e-ink screen design for community builds](#item-9) ⭐️ 6.0/10
10. [Half-Baked Product](#item-10) ⭐️ 6.0/10
11. [The Fall and Rise of Screwworm](#item-11) ⭐️ 6.0/10
12. [Google DeepMind and A24 announce first-of-its-kind research partnership](#item-12) ⭐️ 6.0/10
13. [SJTU Proposes HAT-4D: Interactive 4D Scenes from Monocular Video](#item-13) ⭐️ 6.0/10
14. [Portugal Releases Amalia, a 9B Open-Source National LLM](#item-14) ⭐️ 6.0/10
15. [It's officially over. One of the fathers of AI at Nvidia doesn't believe in AGI and compares OpenAI and Anthropic's closed models to AOL and Prodigy's closed internets. Says the future is every business having a customized open source model.](#item-15) ⭐️ 6.0/10
16. [Particle Scattering Sampler for llama.cpp](#item-16) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Karpathy Launches nanochat: A ChatGPT Clone for $100](https://github.com/karpathy/nanochat) ⭐️ 8.0/10

Andrej Karpathy has released nanochat on GitHub, an open-source, full-stack experimental harness for training and running a ChatGPT-style LLM on a single GPU node, with a total training cost targeted at roughly $100. Given Karpathy's track record with influential educational projects like nanoGPT and minbpe, nanochat could substantially lower the barrier to entry for LLM training and experimentation, potentially democratizing access for students, hobbyists, and researchers without large compute budgets. The repository is deliberately kept minimal and hackable, and covers the full LLM pipeline including tokenization, pretraining, finetuning, evaluation, inference, and a chat UI on a single GPU node. Reports indicate the end-to-end training can be completed in under five hours, though the exact model scale, architecture, and benchmark results compared to larger models have not been disclosed in the initial release.

github · karpathy · Jul 3, 17:47

**Background**: Andrej Karpathy is a well-known AI researcher and educator, formerly of OpenAI and Tesla, who has built a reputation for creating clear, minimal, and pedagogically valuable open-source codebases such as nanoGPT (a simple GPT training repository) and minbpe (a minimal byte-pair encoding tokenizer). His projects often serve as entry points for newcomers wanting to understand LLM internals rather than as production-grade systems. nanochat extends this philosophy to the entire post-training stack: instead of just pretraining a base model, it bundles the full ChatGPT-style workflow, including finetuning and a chat interface. The $100 cost target is striking because training even small LLMs from scratch typically requires thousands of dollars in cloud GPU time, so achieving a coherent conversational model at this price point would represent a significant efficiency milestone.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/karpathy/nanochat">GitHub - karpathy / nanochat : The best ChatGPT that $100 can buy.</a></li>
<li><a href="https://medium.com/@writeronepagecode/the-100-chatgpt-a-code-level-tour-of-andrej-karpathys-nanochat-729490982bcc">The $100 ChatGPT: A Code-Level Tour of Andrej Karpathy ’s nanochat</a></li>
<li><a href="https://www.linkedin.com/posts/arif-ansari-_github-karpathynanochat-the-best-chatgpt-activity-7384105782788853761-SBgv">Andrej Karpathy releases nanochat , a ChatGPT-style LLM... | LinkedIn</a></li>

</ul>
</details>

**Tags**: `#karpathy`, `#nanochat`, `#LLM`, `#cost-efficient-training`, `#open-source`

---

<a id="item-2"></a>
## [huggingface/transformers released v5.13.0](https://github.com/huggingface/transformers/releases/tag/v5.13.0) ⭐️ 7.0/10

Hugging Face Transformers v5.13.0 adds architecture support for Moonshot AI's Kimi K2.5, K2.6, and K2.7 multimodal agentic models.

github · vasqu · Jul 3, 16:06

**Tags**: `#huggingface`, `#transformers`, `#kimi-k2`, `#multimodal-models`, `#release-notes`

---

<a id="item-3"></a>
## [PostgreSQL and the OOM killer: Why we use strict memory overcommit](https://www.ubicloud.com/blog/postgresql-and-the-oom-killer-why-we-use-strict-memory-overcommit) ⭐️ 7.0/10

Ubicloud explains why they use strict memory overcommit settings to prevent the Linux OOM killer from terminating PostgreSQL processes, with community discussion highlighting Linux memory management pitfalls.

hackernews · furkansahin · Jul 3, 13:00 · [Discussion](https://news.ycombinator.com/item?id=48774509)

**Tags**: `#postgresql`, `#linux`, `#memory-management`, `#oom-killer`, `#devops`

---

<a id="item-4"></a>
## [Wordgard: New Rich-Text Editor from ProseMirror Creator](https://wordgard.net/) ⭐️ 7.0/10

Marijn Haverbeke, the creator of ProseMirror, has released Wordgard 0.1, a new open-source JavaScript library implementing an in-browser rich-text editor. Wordgard is described as a new iteration of a ProseMirror-style system, integrating lessons learned over the nine years since ProseMirror stabilized. ProseMirror powers many popular editor products (including through TipTap, a widely-used wrapper), so any successor or alternative from its original author carries significant weight in the web editor ecosystem. Wordgard's release reignites discussion about editor framework choices in 2025–2026, competing against options like Lexical, Tiptap, BlockNote, and Slate. Wordgard targets customizability for schema-specific content rather than being a generic WYSIWYG or HTML editor. According to community discussion, it shares many concepts with ProseMirror but currently offers no upgrade path, meaning migrating an existing ProseMirror-based project would require substantial rework.

hackernews · indy · Jul 3, 08:50 · [Discussion](https://news.ycombinator.com/item?id=48772573)

**Background**: ProseMirror is an established open-source toolkit for building rich-text editors on the web, released by Marijn Haverbeke around 2015. It provides low-level building blocks—schema, document model, transactions, and collaborative editing primitives—rather than a turnkey editor, which is why wrappers like TipTap exist to provide a higher-level API. Wordgard represents the same author's rethinking of this problem space after nearly a decade of accumulated feedback, real-world usage patterns, and ecosystem evolution.

<details><summary>References</summary>
<ul>
<li><a href="https://marijnhaverbeke.nl/blog/wordgard-0.1.html">Wordgard Release 0.1</a></li>
<li><a href="https://wordgard.net/">Wordgard</a></li>
<li><a href="https://wordgard.net/docs/guide/">Wordgard System Guide</a></li>

</ul>
</details>

**Discussion**: Commenters expressed strong enthusiasm for the design and technical approach, with some validating that their own custom solutions align with Wordgard's design choices. Key concerns include the lack of an upgrade path from ProseMirror, the absence of statically-typed schema representation (a pain point users currently solve with tools like Zod alongside ProseMirror), and broader frustration that the web still lacks a standardized WYSIWYG editor interface after 15+ years. TipTap users were identified as the most likely audience to evaluate migration.

**Tags**: `#rich-text-editor`, `#prosemirror`, `#web-development`, `#javascript`, `#text-editing`

---

<a id="item-5"></a>
## [60% Cost Cut: Converting Code to Images for LLM OCR Processing](https://github.com/teamchong/pxpipe) ⭐️ 7.0/10

A developer published a GitHub tool called pxpipe that converts code into images and feeds them to an LLM (Claude Fable) for OCR-based processing, achieving a 60% reduction in API costs compared to sending raw text tokens. If this technique works reliably, it could significantly lower LLM inference costs for code-heavy workloads, benefiting developers and startups running large-scale code analysis. However, the community suspects this exploits a pricing/accounting loophole that providers may close, making it a temporary rather than structural advantage. The tool is open-sourced on GitHub (teamchong/pxpipe) and specifically targets Claude's pricing model. The hack likely exploits the fact that vision/image tokens are billed at a lower effective rate than equivalent text tokens, or that backend OCR processing isn't charged to the user at all. The original Reddit post accumulated 190 upvotes and 72 comments within a short period.

hackernews · dimitropoulos · Jul 3, 15:50 · [Discussion](https://news.ycombinator.com/item?id=48776464)

**Background**: Large language models like Claude support multimodal input, meaning they can process both text and images. When an image containing text is sent, the model performs optical character recognition (OCR) to extract the text. Pricing for vision tokens differs from text tokens across providers — Claude Fable 5, for example, is priced at $10 per million input tokens and $50 per million output tokens, but image tokens may be metered differently. This creates an asymmetry where sending text as an embedded image can be cheaper than sending it as plain text, depending on how the provider accounts for the OCR step internally.

<details><summary>References</summary>
<ul>
<li><a href="https://www.mindstudio.ai/blog/claude-fable-5-pricing-access-usage-limits">Claude Fable 5 Pricing, Access, and Usage Limits: What You Need to Know | MindStudio</a></li>
<li><a href="https://medium.com/@pvsravanth/next-gen-ocr-with-vision-llms-a-guide-to-using-phi-3-claude-and-gpt-4o-4c6fbabe92c8">Next-Gen OCR with Vision LLMs : A Guide to Using Phi-3, Claude, and GPT-4O | by Sravanth | Generative AI</a></li>
<li><a href="https://www.reddit.com/r/ClaudeAI/comments/1u4j86h/fable_5_what_600hour_of_productivity_looks_like/">Fable 5: What $600/Hour of Productivity Looks Like : r/ClaudeAI - Reddit</a></li>

</ul>
</details>

**Discussion**: The community is largely skeptical that this is a lasting technique. Commenters compare it to how Gemini processes PDFs by running internal OCR without charging for the resulting text tokens, suggesting Claude's backend may be doing something similar and that this is a token-accounting loophole likely to be closed. One user reported trying a similar approach last year with OpenAI models and found it reduced prompt tokens but ballooned completion tokens, making it slower and ultimately more expensive. Others note the GitHub readme is poorly written (likely 'vibe-coded') and warn that once providers close the loophole, OCR pricing may rise to compensate.

**Tags**: `#llm`, `#cost-optimization`, `#ocr`, `#prompt-engineering`, `#claude`

---

<a id="item-6"></a>
## [Mistral Releases Leanstral-1.5-119B-A6B for Formal Verification and Theorem Proving](https://www.reddit.com/r/LocalLLaMA/comments/1umgdhx/mistral_released_leanstral15119ba6b/) ⭐️ 7.0/10

Mistral released Leanstral-1.5-119B-A6B, an Apache-2.0 licensed Mixture-of-Experts model with 6B active parameters, achieving state-of-the-art results across formal verification benchmarks — saturating miniF2F, solving 587 out of 672 PutnamBench problems, and reaching 87% on FATE-H and 34% on FATE-X. This release marks a major open-source advancement in automated theorem proving, with the practical ability to discover real bugs in real-world code — specifically 5 previously unknown bugs across 57 tested repositories — making it directly valuable for software correctness and security research. The model was trained through a pipeline of mid-training, supervised fine-tuning, and reinforcement learning using the CISPO algorithm, and it excels at agentic proof engineering rather than serving as a general-purpose chat model.

reddit · r/LocalLLaMA · /u/Tall-Ad-7742 · Jul 3, 14:44

**Background**: Formal verification uses mathematical proofs to guarantee software correctness, with Lean being one of the most widely adopted interactive theorem provers. Mixture-of-Experts (MoE) architectures activate only a subset of total parameters per token, enabling large model capacity with reduced inference cost — here 6B active out of 119B total. CISPO (Clipped Importance Sampling Policy Optimization) is a reinforcement learning algorithm that clips token-level importance sampling weights to reduce variance and stabilize off-policy training. Benchmarks like miniF2F (Olympiad-level mathematics problems), PutnamBench (Putnam competition problems formalized in Lean, Isabelle, and Coq), and the FATE-H/FATE-X suites are standard evaluations for measuring a model's formal reasoning capability.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2109.00110">[2109.00110] MiniF 2 F : a cross-system benchmark for formal ...</a></li>
<li><a href="https://trishullab.github.io/PutnamBench/">PutnamBench : A Multilingual Mathematics Benchmark for Formal ...</a></li>
<li><a href="https://www.emergentmind.com/topics/cispo-algorithm">CISPO : Clipped Importance Sampling RL</a></li>

</ul>
</details>

**Tags**: `#formal-verification`, `#theorem-proving`, `#Mistral`, `#open-source`, `#LLM`

---

<a id="item-7"></a>
## [Greek MEP on Spyware Investigation Committee Hacked with Pegasus](https://citizenlab.ca/research/member-of-committee-investigating-spyware-hacked-with-pegasus/) ⭐️ 6.0/10

Citizen Lab reported that Greek MEP Stelios Kouloglou, a member of a European Parliament committee investigating spyware abuse, was himself successfully targeted with Pegasus spyware on or around October 21, 2022, and again on March 6–7, 2023. The forensic analysis of his iPhone was conducted after he contacted Citizen Lab in May 2026. This case highlights the brazen targeting of democratic oversight figures by state-level actors, undermining the very institutions meant to investigate surveillance abuses. It underscores the vulnerability of even legislators tasked with scrutinizing spyware, and raises serious questions about state-sponsored surveillance within EU member states. Pegasus, developed by the NSO Group, is a sophisticated spyware capable of zero-click infections that require no user interaction to compromise a device. The repeated targeting of this MEP over multiple dates suggests persistent, deliberate surveillance rather than a one-off operation, and the timing coincides with the broader Greek surveillance scandal linked to the prime minister's office and national intelligence service.

hackernews · ledoge · Jul 3, 20:38 · [Discussion](https://news.ycombinator.com/item?id=48779683)

**Background**: Pegasus spyware, developed by the Israeli firm NSO Group, is one of the most advanced commercial surveillance tools available, typically sold to government clients for law enforcement and intelligence purposes. It can infiltrate smartphones via zero-click exploits, turning the device into a full surveillance tool with access to messages, camera, microphone, and location data. Citizen Lab, based at the Munk School of Global Affairs at the University of Toronto, is a leading research organization that specializes in detecting and exposing digital threats to civil society, journalists, and political figures. The European Parliament established a committee (PEGA) to investigate the use of Pegasus and equivalent spyware across EU member states following revelations of widespread abuse.

<details><summary>References</summary>
<ul>
<li><a href="https://citizenlab.ca/about/">Who We Are - The Citizen Lab</a></li>
<li><a href="https://us.norton.com/blog/emerging-threats/pegasus-spyware">What is Pegasus spyware , and how to detect and remove it</a></li>

</ul>
</details>

**Discussion**: Commenters contextualized the incident as part of a broader, unresolved Greek surveillance scandal in which many politicians were hacked, with evidence pointing to orchestration by the prime minister's office and intelligence service, suggesting this is not specifically an attack on the European Parliament. Another commenter raised concerns about lobbyists selling EU citizens' data to US corporations, highlighting concerns about external influence on EU policy.

**Tags**: `#spyware`, `#pegasus`, `#cybersecurity`, `#european-politics`, `#surveillance`

---

<a id="item-8"></a>
## [Jamesob's guide to running SOTA LLMs locally](https://github.com/jamesob/local-llm) ⭐️ 6.0/10

A comprehensive guide to running state-of-the-art LLMs locally with hardware recommendations, accompanied by substantive community discussion on cost tradeoffs and alternative setups like unified memory architectures.

hackernews · livestyle · Jul 3, 15:03 · [Discussion](https://news.ycombinator.com/item?id=48775921)

**Tags**: `#LLM`, `#local-inference`, `#hardware`, `#GPU`, `#machine-learning`

---

<a id="item-9"></a>
## [Valve open-sources Steam Machine e-ink screen design for community builds](https://www.gamingonlinux.com/2026/07/valve-open-source-the-steam-machine-e-ink-screen-so-you-can-make-your-own/) ⭐️ 6.0/10

Valve has released the open-source hardware design files for the optional e-ink screen accessory of its Steam Machine, enabling community members to build their own using a standard Adafruit 5.83-inch eInk panel (product #6397). This move continues Valve's track record of open-sourcing hardware (following the Steam Deck), empowering the maker community to customize and extend their devices rather than locking accessories behind proprietary designs. It signals a growing trend of hardware manufacturers embracing open hardware principles even for non-essential accessories. The screen uses a standard off-the-shelf Adafruit 5.83-inch monochrome eInk/ePaper panel (likely the 648×480 resolution variant under product #6397), making sourcing straightforward. E-ink displays consume power only when refreshing the image, making them well-suited for always-on status displays that don't contribute to system power draw.

hackernews · ahlCVA · Jul 3, 13:01 · [Discussion](https://news.ycombinator.com/item?id=48774518)

**Background**: E-ink (electronic ink) display technology uses tiny microcapsules containing charged particles to mimic the appearance of printed paper, providing excellent readability and ultra-low power consumption since the image persists without continuous power. Adafruit is a well-known open-source hardware company that produces modular electronic components, breakout boards, and displays commonly used by hobbyists and makers. The Steam Machine is Valve's upcoming gaming desktop/device, and the optional e-ink screen serves as a secondary status display, likely showing system information like currently playing games, temperatures, or notifications.

<details><summary>References</summary>
<ul>
<li><a href="https://medium.com/@centralfinder.24/how-do-eink-readers-actually-work-edef91d69cf2">How do eInk Readers actually work ? | by Central Finder | Medium</a></li>
<li><a href="https://www.adafruit.com/product/6395">3.7" 416x240 Monochrome Black/White eInk / ePaper - Bare Display</a></li>
<li><a href="https://thepihut.com/products/adafruit-3-52-340x180-quad-colour-eink-epaper-bare-display">Adafruit 3.52" 340x180 Quad-Colour eInk / ePaper - Bare... - The Pi Hut</a></li>

</ul>
</details>

**Discussion**: The community reaction is overwhelmingly positive, with users praising Valve's open approach to optional accessories and expressing hope that more hardware companies follow suit. One user identified the exact Adafruit panel part number for others who don't want to search, another expressed enthusiasm ('Valve mi familia'), and a Framework Desktop owner asked about adapting the design to that form factor. There was also a practical inquiry about larger A5-sized (~10 inch) eInk screens with HDMI or USB-C input for potential alternative applications.

**Tags**: `#open-source`, `#hardware`, `#valve`, `#e-ink`, `#steam-machine`

---

<a id="item-10"></a>
## [Half-Baked Product](https://weli.dev/blog/half-baked-product/) ⭐️ 6.0/10

A startup cautionary tale about founders building products without deep domain expertise, leading to fundamental disconnects between business vision, technical feasibility, and customer needs.

hackernews · weli · Jul 3, 08:23 · [Discussion](https://news.ycombinator.com/item?id=48772388)

**Tags**: `#startups`, `#entrepreneurship`, `#product-development`, `#founder-advice`, `#business-strategy`

---

<a id="item-11"></a>
## [The Fall and Rise of Screwworm](https://www.construction-physics.com/p/the-fall-and-rise-of-screwworm) ⭐️ 6.0/10

Historical account of the screwworm eradication effort using sterile insect technique, examining why the pest is making a comeback and the challenges of containing it today.

hackernews · crescit_eundo · Jul 3, 12:58 · [Discussion](https://news.ycombinator.com/item?id=48774492)

**Tags**: `#biology`, `#agriculture`, `#biosecurity`, `#history-of-science`, `#pest-management`

---

<a id="item-12"></a>
## [Google DeepMind and A24 announce first-of-its-kind research partnership](https://deepmind.google/blog/google-deepmind-and-a24-announce-first-of-its-kind-research-partnership/) ⭐️ 6.0/10

Google DeepMind announces a first-of-its-kind research partnership with film production company A24, exploring collaboration at the intersection of AI and filmmaking.

rss · Google DeepMind Blog · Jul 3, 14:25

**Tags**: `#Google DeepMind`, `#A24`, `#AI partnerships`, `#film industry`, `#research collaboration`

---

<a id="item-13"></a>
## [SJTU Proposes HAT-4D: Interactive 4D Scenes from Monocular Video](https://mp.weixin.qq.com/s?__biz=MzIzNjc1NzUzMw==&mid=2247901356&idx=3&sn=54ee94026f76691a380cd3ea214e0def) ⭐️ 6.0/10

Researchers from Shanghai Jiao Tong University and collaborators have proposed HAT-4D, a method that generates interactive 4D scenes directly from monocular video input. The technique aims to reconstruct dynamic, manipulable 3D environments and objects from ordinary single-camera footage without requiring specialized motion capture equipment. This approach could dramatically lower the cost barrier for creating interactive 4D content, potentially replacing million-dollar motion capture studios with standard video. If effective, it would benefit VFX production, game development, AR/VR applications, and any field requiring dynamic 3D scene reconstruction from casual recordings. The specific RSS content is fragmented, mixing snippets from multiple unrelated articles, making it difficult to extract concrete technical details about HAT-4D's architecture, training data, or benchmark results. Related work in 4D reconstruction from monocular video, such as LIM and Vivid4D, demonstrates that this is an active and competitive research area where diffusion-based multiview generation and large interpolator models are being explored.

rss · 量子位 · Jul 3, 03:43

**Background**: 4D reconstruction refers to reconstructing dynamic 3D scenes that change over time (the fourth dimension). Traditional methods require expensive multi-camera rigs or motion capture studios to capture precise geometry and movement. Monocular video reconstruction aims to accomplish this from a single camera's viewpoint, which is far more accessible but mathematically challenging due to the lack of multi-view geometric constraints. Recent advances in neural radiance fields (NeRF), Gaussian splatting, and diffusion models have accelerated progress in this area, enabling applications from medical endoscopic reconstruction to dynamic asset creation for graphics.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2504.11092">[2504.11092] Vivid 4 D : Improving 4 D Reconstruction from Monocular ...</a></li>
<li><a href="https://remysabathier.github.io/lim.github.io/">LIM: Large Interpolator Model for Dynamic Reconstruction</a></li>
<li><a href="https://pubmed.ncbi.nlm.nih.gov/41719834/">4 D monocular surgical reconstruction under arbitrary camera motions</a></li>

</ul>
</details>

**Tags**: `#4D-reconstruction`, `#computer-vision`, `#monocular-video`, `#research`, `#AI`

---

<a id="item-14"></a>
## [Portugal Releases Amalia, a 9B Open-Source National LLM](https://www.reddit.com/r/LocalLLaMA/comments/1umhrn8/portugal_just_released_their_own_llm_amalia_9b/) ⭐️ 6.0/10

Portugal has released Amalia, a 9-billion-parameter open-source large language model, under the Apache 2.0 license, as part of a national AI initiative announced by the Portuguese government. Two variants are available on Hugging Face: AMALIA-9B-0626-SFT (Supervised Fine-Tuning) and AMALIA-9B-0626-DPO (Direct Preference Optimization), accompanied by an arxiv paper. Amalia joins a growing wave of government-backed national LLMs, signaling that countries are increasingly investing in sovereign AI capabilities tailored to their own languages and cultural contexts. Open-source release under Apache 2.0 allows global researchers and developers to build on the model, potentially strengthening Portuguese-language AI tooling. The post notes that no concise coding benchmarks were provided alongside the release, limiting immediate assessment of Amalia's capabilities relative to existing 9B models. Both SFT and DPO variants are available, offering users choices between task-specific supervised fine-tuning and preference-based alignment.

reddit · r/LocalLLaMA · /u/EveningIncrease7579 · Jul 3, 15:38

**Background**: Supervised Fine-Tuning (SFT) is a technique that refines pre-trained models using labeled demonstration pairs to improve specialized task performance. Direct Preference Optimization (DPO) is a more recent alignment method that simplifies the traditional Reinforcement Learning from Human Feedback (RLHF) pipeline by collapsing reward modeling and PPO optimization into a single supervised training objective. National LLMs are sovereign AI models trained or adapted by governments to better represent local languages, cultural values, and regional needs.

<details><summary>References</summary>
<ul>
<li><a href="https://cameronrwolfe.substack.com/p/understanding-and-using-supervised">Understanding and Using Supervised Fine - Tuning ( SFT ) for...</a></li>
<li><a href="https://toloka.ai/blog/direct-preference-optimization/">Direct Preference Optimization ( DPO ): a lightweight counterpart to...</a></li>
<li><a href="https://qubittool.com/blog/dpo-vs-rlhf-alignment-techniques">DPO vs RLHF : The Evolution of LLM Alignment Techniques | QubitTool</a></li>

</ul>
</details>

**Tags**: `#LLM`, `#open-source`, `#Portugal`, `#national-AI`, `#LocalLLaMA`

---

<a id="item-15"></a>
## [It's officially over. One of the fathers of AI at Nvidia doesn't believe in AGI and compares OpenAI and Anthropic's closed models to AOL and Prodigy's closed internets. Says the future is every business having a customized open source model.](https://www.reddit.com/r/LocalLLaMA/comments/1ult0f4/its_officially_over_one_of_the_fathers_of_ai_at/) ⭐️ 6.0/10

A senior Nvidia AI researcher publicly dismisses AGI and compares closed AI labs like OpenAI and Anthropic to AOL/Prodigy, arguing open-source customized models will dominate enterprise AI.

reddit · r/LocalLLaMA · /u/9gxa05s8fa8sh · Jul 2, 20:06

**Tags**: `#open-source-ai`, `#nvidia`, `#AGI`, `#ai-industry`, `#open-vs-closed`

---

<a id="item-16"></a>
## [Particle Scattering Sampler for llama.cpp](https://www.reddit.com/r/LocalLLaMA/comments/1umqgnl/particle_scattering_sampler_for_llamacpp/) ⭐️ 6.0/10

An experimental 'scatter' sampler added to llama.cpp that redistributes probability mass among top token candidates via a local diffusion step, aiming to reduce generation rigidity without leaking probability into the deep tail.

reddit · r/LocalLLaMA · /u/Pristine_Income9554 · Jul 3, 21:19

**Tags**: `#llama.cpp`, `#sampling`, `#LLM inference`, `#token generation`, `#local LLMs`

---