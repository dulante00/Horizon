---
layout: default
title: "Horizon Summary: 2026-09-18 (EN)"
date: 2026-09-18
lang: en
---

> From 70 items, 20 important content pieces were selected

---

1. [Photon-Emission-Guided Laser FI Bypasses RP2350 Secure Debug](#item-1) ⭐️ 8.0/10
2. [ZCode AI Assistant Found Silently Uploading Git History to Cloud](#item-2) ⭐️ 8.0/10
3. [US Military had close call after using AI for hallucinated intelligence report](#item-3) ⭐️ 8.0/10
4. [US Government Website Found Using Chinese Qwen AI Flagged by FBI](#item-4) ⭐️ 8.0/10
5. [Claude Code Adopts AGENTS.md Fallback After Industry Pressure](#item-5) ⭐️ 7.0/10
6. [Android 17 is the first since 3.x to add new APIs without releasing to the AOSP](#item-6) ⭐️ 7.0/10
7. [Saving another 100TB of RAM](#item-7) ⭐️ 7.0/10
8. [C++26: Trivial infinite loops are no longer undefined behaviour](#item-8) ⭐️ 7.0/10
9. [How SpaceX Streamlined the Raptor Engine Across V1–V3](#item-9) ⭐️ 7.0/10
10. [Dan Abramov Vibes a Proof of Conway's Conjecture Using AI](#item-10) ⭐️ 7.0/10
11. [Korea raises data breach fines to 10% of company revenue](#item-11) ⭐️ 7.0/10
12. [Image Generation Models Compared: Cost, Edit, Quality](#item-12) ⭐️ 7.0/10
13. [MiniMax Code Open-Sources Terminal AI Coding Agent](#item-13) ⭐️ 7.0/10
14. [Bonsai's ternary model retains ~75% performance, not the 98.2% they marketed](#item-14) ⭐️ 7.0/10
15. [Show HN: Cactus Needle 3: 8-29MB automation models can match DeepSeek V4 Flash](#item-15) ⭐️ 6.0/10
16. [How to Write with an LLM](#item-16) ⭐️ 6.0/10
17. [Is HF starting to move against abliterated models?](#item-17) ⭐️ 6.0/10
18. [InclusionAI Releases Realtime-Venus: A 9B Omni-Modal Model for Full-Duplex Audio-Visual Interaction](#item-18) ⭐️ 6.0/10
19. [Ternary Bonsai 2: 27B Model Compressed to Under 6GB Runs In-Browser](#item-19) ⭐️ 6.0/10
20. [Benchmark of 24 LLMs vs. Human Writers on 475 Creative Writing Prompts](#item-20) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [Photon-Emission-Guided Laser FI Bypasses RP2350 Secure Debug](https://donjon.ledger.com/blog/rp2350-secure-debug-laser-fault-injection/) ⭐️ 8.0/10

Ledger Donjon researchers demonstrated a photon-emission-guided laser fault injection attack that bypassed the secure debug protection on the Raspberry Pi RP2350 A4 microcontroller. They used differential photon-emission microscopy to localize the debug enable register's activity and then performed SWD-guided laser injection to flip the two bits required to restore Secure debug access. The RP2350's built-in secure enclave made it a candidate for security-critical applications like Yubikey alternatives, so a successful physical attack against its debug protection raises concerns for designers relying on it for high-assurance use cases. The disclosure also showcases how combining photon-emission microscopy with laser fault injection can dramatically narrow the attack search space, a technique that will likely influence future secure hardware designs. The attack used a pulsed 980 nm laser at approximately 1.2 W (40% of its 2.97 W max), with 100 ns pulse width delivered through a 50x objective lens. It requires physical possession, destructive decapsulation, and roughly $250,000 of laboratory equipment, though community commenters noted similar attacks can be replicated at home for under $10,000–$25,000 using cheaper tools like the PicoEMP.

hackernews · synack · Sep 18, 16:54 · [Discussion](https://news.ycombinator.com/item?id=49757050)

**Background**: The RP2350 is Raspberry Pi's microcontroller featuring a built-in secure enclave and OTP (one-time programmable) memory that underpins many of its security features, including secure boot and debug access control. Laser fault injection (LFI) is a hardware attack technique that uses focused laser pulses to induce transient faults in semiconductor circuits, allowing attackers to skip instructions, flip bits, or bypass security checks. Photon-emission microscopy (PEM) is a failure-analysis technique that detects faint light emitted by switching transistors, letting researchers pinpoint which regions of a chip are active during sensitive operations—a useful tool for narrowing down where to aim a fault-injection laser.

<details><summary>References</summary>
<ul>
<li><a href="https://donjon.ledger.com/blog/rp2350-secure-debug-laser-fault-injection/">Photon-Emission-Guided Laser Fault Injection Enables RP2350 ...</a></li>
<li><a href="https://hal.science/hal-05534553v1/document">Betrayed by Light: How Photon Emission Microscopy Empowers...</a></li>
<li><a href="https://pip-assets.raspberrypi.com/categories/1260-security/documents/RP-009377-WP-1-Understanding+RP2350_s+security+features.pdf">Understanding RP2350’s security features</a></li>

</ul>
</details>

**Discussion**: Community sentiment is appreciative of Ledger Donjon's detailed writeup, with commenters noting that the $250k lab cost reflects discovery rather than replication—similar attacks have been done at home for under $10k using tools like the PicoEMP versus a $5,000 ChipShouter. Several noted the RP2350's secure enclave made it attractive as a Yubikey alternative, framing the disclosure as part of an ongoing arms race between safe-builders and safe-crackers, with the expectation that lessons learned will harden future generations.

**Tags**: `#hardware-security`, `#fault-injection`, `#rp2350`, `#security-research`, `#embedded-systems`

---

<a id="item-2"></a>
## [ZCode AI Assistant Found Silently Uploading Git History to Cloud](https://blog.ferstar.org/en/posts/zcode-silent-workspace-snapshot-upload/) ⭐️ 8.0/10

An investigation revealed that z.ai's ZCode AI coding assistant silently uploads users' entire Git history to the cloud through its "codebase indexing" feature without clear user consent, prompting an official apology and explanation from the company. This disclosure raises serious privacy and security concerns for the rapidly growing AI coding tools ecosystem, as developers increasingly grant these assistants deep access to local codebases. It highlights fundamental trust issues around AI tools with filesystem access and could influence enterprise adoption decisions across the industry. The "codebase indexing" feature is designed to help AI tools efficiently search and understand code by creating representations of the project, but the silent upload of full Git history goes beyond typical indexing scope. z.ai issued a public apology stating the issue stemmed from the codebase indexing feature and conducted an internal review to address community concerns.

hackernews · csmantle · Sep 18, 06:11 · [Discussion](https://news.ycombinator.com/item?id=49750694)

**Background**: ZCode is an AI-powered coding assistant developed by z.ai, a Chinese AI company spun out of Tsinghua University known for its GLM family of large language models. Codebase indexing is a standard feature in modern AI coding tools that scans and parses source code to create searchable representations, enabling models to find relevant context efficiently. z.ai recently went public with a $6.6 billion valuation, becoming China's first major generative AI company to list on the stock market.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Z.ai">Z.ai - Wikipedia</a></li>
<li><a href="https://www.everydev.ai/tools/zcode">ZCode - AI Agent Coding Desktop App | EveryDev. ai</a></li>

</ul>
</details>

**Discussion**: The community expressed significant concern about the broader pattern of AI coding tools accessing local data without transparent consent, debating whether AI agents should be trusted with filesystem access at all since sandboxing measures can be bypassed by the agents themselves. Some users said they are switching to alternatives like OpenCode due to misaligned incentives, while others reported similar suspicious behaviors in other tools, including Windows Defender scanning Codex files and models like GLM/Deepseek attempting to read dotfiles and .gitignore files.

**Tags**: `#privacy`, `#ai-coding-tools`, `#security`, `#data-exfiltration`, `#developer-tools`

---

<a id="item-3"></a>
## [US Military had close call after using AI for hallucinated intelligence report](https://www.cnn.com/2026/09/18/politics/us-military-ai-false-intelligence-china-ship) ⭐️ 8.0/10

The US military experienced a close call after an AI system produced hallucinated intelligence about a ship incident, highlighting the real-world dangers of deploying unreliable LLMs in critical national security contexts.

hackernews · realsarm · Sep 18, 17:28 · [Discussion](https://news.ycombinator.com/item?id=49757520)

**Tags**: `#AI safety`, `#military`, `#LLM hallucination`, `#national security`, `#ethics`

---

<a id="item-4"></a>
## [US Government Website Found Using Chinese Qwen AI Flagged by FBI](https://www.reddit.com/r/LocalLLaMA/comments/1wjmomv/us_government_website_used_ai_search_tool_qwen/) ⭐️ 8.0/10

A US government website was discovered to be using Qwen, an AI search tool developed by China's Alibaba, which the FBI had previously flagged for allegedly copying Anthropic's Claude model through a large-scale distillation campaign. This incident raises serious national security and intellectual property concerns, highlighting how foreign AI tools from geopolitical rivals may be embedded in US government infrastructure, and underscores the escalating AI competition between the US and China. Anthropic has accused Chinese AI firms, including Alibaba, of using approximately 16 million queries against Claude to replicate its capabilities, particularly in coding, reasoning, and cybersecurity tasks. The report comes amid broader concerns that Qwen may have benefited from US AI investments without contributing to the underlying research costs.

reddit · r/LocalLLaMA · /u/External_Mood4719 · Sep 18, 10:39

**Background**: Qwen is a family of large language models developed by Alibaba's Tongyi Lab, with recent releases including Qwen 3.5 and Qwen 3.5-Plus. Anthropic, the US-based AI safety company behind Claude, alleged in 2026 that several Chinese AI firms conducted systematic distillation attacks—harvesting millions of outputs from Claude to train competing models, effectively bypassing the costly research and compute investments made by US firms. The FBI's involvement signals US law enforcement's recognition of AI model replication as a potential national security and trade secret issue.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Qwen">Qwen - Wikipedia</a></li>
<li><a href="https://memeburn.com/anthropic-accuses-alibaba-of-massive-ai-model-copying/">Anthropic Accuses Alibaba of Massive AI Model Copying - Memeburn</a></li>
<li><a href="https://softwareplaza.com/it-magazine/anthropic-says-chinese-ai-firms-used-16-million-claude-queries-to-copy-model/">Anthropic Says Chinese AI Firms Used 16 Million Claude Queries to Copy Model - SoftwarePlaza</a></li>

</ul>
</details>

**Discussion**: Community discussion on this topic centers on AI sovereignty, government technology procurement practices, and the broader US-China AI rivalry. Commenters expressed concern about foreign AI dependencies in government systems and debated whether this reflects a failure in vetting processes or highlights the competitive quality of Chinese open-weight models.

**Tags**: `#AI policy`, `#Qwen`, `#national security`, `#US-China AI competition`, `#government technology`

---

<a id="item-5"></a>
## [Claude Code Adopts AGENTS.md Fallback After Industry Pressure](https://code.claude.com/docs/en/changelog) ⭐️ 7.0/10

Anthropic's Claude Code now reads AGENTS.md files as a fallback configuration source when CLAUDE.md is not present in a project, adopting the emerging cross-tool standard. The change came after public pressure, notably from Shopify CEO Tobi Lütke, who threatened to ban Claude Code at Shopify until it supported AGENTS.md and related agent conventions. This represents a significant step toward standardization in the rapidly proliferating AI coding agent ecosystem, where developers previously had to maintain separate configuration files (CLAUDE.md, .cursorrules, copilot-instructions.md, etc.) for each tool. Adoption by a major player like Anthropic validates AGENTS.md as a viable common format and reduces friction for teams that mix multiple AI coding assistants. The fallback behavior means CLAUDE.md still takes priority when present, and AGENTS.md is only consulted if the Claude-specific file is absent. AGENTS.md is maintained under the Linux Foundation's AI Foundation and is already supported by tools like OpenAI's Codex CLI, which uses a hierarchical discovery process walking from project root to current working directory.

hackernews · datadrivenangel · Sep 18, 21:00 · [Discussion](https://news.ycombinator.com/item?id=49760187)

**Background**: AI coding agents are tools that autonomously read, edit, and run code based on natural language instructions. To give agents project-specific context—such as coding style, build commands, or architectural decisions—developers place instruction files in their repositories. Each vendor originally invented its own file (CLAUDE.md for Anthropic, .cursorrules for Cursor, copilot-instructions.md for GitHub Copilot), forcing multi-tool users to duplicate instructions. AGENTS.md emerged as a vendor-neutral alternative, analogous to how README.md serves as a universal project entry point, and is designed to be a predictable location for any agent to discover guidance.

<details><summary>References</summary>
<ul>
<li><a href="https://agents.md/">AGENTS.md</a></li>
<li><a href="https://www.augmentcode.com/guides/how-to-build-agents-md">How to Build Your AGENTS.md: The Context File That Makes AI Coding Agents Actually Work | Augment Code</a></li>
<li><a href="https://wotai.co/blog/agents-md-vs-claude-md">AGENTS . md vs CLAUDE . md : which file your agent reads | WotAI</a></li>

</ul>
</details>

**Discussion**: Reactions are mixed: some users, like TomGarden, view the change as 'the absolute bare minimum' and are eager to delete redundant symlinks, while others such as bcorigliano welcome it as a long-overdue step toward industry-wide standards, drawing parallels to the pain of inconsistent hotkeys in 3D software. Anecdotes show Claude Code itself had already been proactively creating AGENTS.md and symlinks to CLAUDE.md in some user projects, suggesting organic convergence even before the official change. The discussion also highlights the unusual influence of a public threat by Shopify's CEO in driving the change.

**Tags**: `#claude-code`, `#ai-coding-agents`, `#industry-standards`, `#agents-md`, `#anthropic`

---

<a id="item-6"></a>
## [Android 17 is the first since 3.x to add new APIs without releasing to the AOSP](https://grapheneos.social/@GrapheneOS/117282080803799576) ⭐️ 7.0/10

Android 17 marks the first version since 3.x to add new APIs exclusively to Pixel without AOSP release, raising concerns about Google's commitment to Android's open-source nature.

hackernews · theanonymousone · Sep 18, 19:03 · [Discussion](https://news.ycombinator.com/item?id=49758736)

**Tags**: `#Android`, `#AOSP`, `#GrapheneOS`, `#Google`, `#open-source`

---

<a id="item-7"></a>
## [Saving another 100TB of RAM](https://blog.cloudflare.com/saving-100-tb-of-ram-with-math/) ⭐️ 7.0/10

Cloudflare engineers describe mathematical optimizations that saved 100TB of RAM in their production infrastructure.

hackernews · f311a · Sep 18, 18:51 · [Discussion](https://news.ycombinator.com/item?id=49758580)

**Tags**: `#systems-engineering`, `#memory-optimization`, `#cloudflare`, `#infrastructure`, `#probabilistic-data-structures`

---

<a id="item-8"></a>
## [C++26: Trivial infinite loops are no longer undefined behaviour](https://www.sandordargo.com/blog/2026/09/16/cpp26-trivial-infinite-loops) ⭐️ 7.0/10

C++26 standardizes that trivial infinite loops (empty bodies like 'while(true);') are no longer undefined behavior, but the implementation approach of inserting std::this_thread::yield() calls has drawn substantial criticism from systems programmers.

hackernews · ibobev · Sep 17, 20:52 · [Discussion](https://news.ycombinator.com/item?id=49746406)

**Tags**: `#cpp`, `#c++26`, `#language-standards`, `#systems-programming`, `#compiler-optimization`

---

<a id="item-9"></a>
## [How SpaceX Streamlined the Raptor Engine Across V1–V3](https://www.construction-physics.com/p/how-spacex-streamlined-the-raptor) ⭐️ 7.0/10

Construction Physics published a detailed analysis of how SpaceX iteratively simplified the Raptor engine across versions 1, 2, and 3, leveraging extensive 3D printing and aggressive parts consolidation to reduce complexity and improve manufacturability. Raptor powers Starship, the largest rocket ever built, so each design simplification directly translates into lower cost, higher reliability, and faster production rates — all critical for SpaceX's goal of making spaceflight fully reusable and affordable. The Raptor uses a full-flow staged combustion cycle — only the third such engine ever built and the first to successfully fly. Despite the streamlining, Flight 13's first launch attempt was aborted when several Raptor 3 engines failed to start, and multiple engines also failed to relight during booster recovery, with feed-line ice considered the most likely cause.

hackernews · JumpCrisscross · Sep 17, 21:14 · [Discussion](https://news.ycombinator.com/item?id=49746626)

**Background**: Full-flow staged combustion is a highly efficient rocket engine cycle in which both fuel and oxidizer are fully turbopumped through preburners before reaching the combustion chamber, maximizing performance but greatly increasing mechanical complexity. Prior to Raptor, only two such engines had been built (the Soviet RD-270 and the US Space Shuttle Main Engine / RS-25), and only the SSME flew operationally. Additive manufacturing (3D printing) in metals allows engineers to consolidate dozens of traditionally machined and welded parts into single printed structures, reducing weight, part count, and assembly time — a strategy SpaceX has applied aggressively to Raptor 2 and especially Raptor 3.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/SpaceX_Raptor">SpaceX Raptor - Wikipedia</a></li>
<li><a href="https://www.nasa.gov/technology/tech-transfer-spinoffs/printed-engines-propel-the-next-industrial-revolution/">Printed Engines Propel the Next Industrial Revolution - NASA</a></li>
<li><a href="https://3dincredible.com/parts-consolidation-with-additive-manufacturing-from-multiple-to-singular/">Parts Consolidation with Additive Manufacturing- From... | 3DIncredible</a></li>

</ul>
</details>

**Discussion**: Commenters debated whether the Space Shuttle Main Engine counts as a prior successful full-flow staged combustion engine (one user noted Raptor is actually the third such engine designed, not the second). Others expressed amazement that 3D printing is mature enough for rocket engines, questioned whether SpaceX's reliance on Cybertrucks for towing engines reflects culture or inefficiency, and discussed whether thrust vector control should be considered part of the engine itself, referencing the Soviet NK-33/AJ-260 precedent. The article's author acknowledged that SpaceX's IP protections limited publicly available detail.

**Tags**: `#spacex`, `#raptor-engine`, `#aerospace-engineering`, `#manufacturing`, `#rocket-propulsion`

---

<a id="item-10"></a>
## [Dan Abramov Vibes a Proof of Conway's Conjecture Using AI](https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/) ⭐️ 7.0/10

Dan Abramov (gaearon), creator of Redux and a prominent React developer, published a detailed blog post documenting his attempt to use LLM-assisted 'vibe coding' to construct a proof of a refinement of John Conway's conjecture about omnific integers (the conjecture states that if ab = cd, then integers e, f, g, h exist such that a = ef, b = gh, c = eg, d = fh). This case study by a highly respected software engineer illustrates both the promise and the pitfalls of using LLMs for mathematical reasoning: while AI can generate plausible-looking proof structures, human verification remains essential. The post is fueling a broader conversation about whether AI lowers the barrier to engaging with open mathematical problems, even when it cannot independently certify correctness. Abramov explicitly states that his proof has not been independently verified by mathematicians, and he acknowledges his own limited background in number theory. He pairs AI-generated proof strategies with his own attempts to simplify and understand each step, illustrating a hybrid 'wizard-and-sorcerer' workflow rather than blind trust in LLM output.

hackernews · m-hodges · Sep 18, 14:36 · [Discussion](https://news.ycombinator.com/item?id=49755024)

**Background**: John Conway was a legendary mathematician known for many contributions including the surreal numbers — a vast ordered field that contains all real numbers and much more. His refinement conjecture concerns a factorization-like property within these 'omnific integers.' 'Vibe coding,' a term coined by Andrej Karpathy in February 2025, describes a software development practice where programmers describe desired functionality in natural language and let LLMs generate the code, often without reading every line. Applying this paradigm to formal mathematics is a natural but risky extension.

<details><summary>References</summary>
<ul>
<li><a href="https://overreacted.io/how-i-vibed-a-proof-of-conways-conjecture/">How I Vibed a Proof of Conway ’s Conjecture — overreacted</a></li>
<li><a href="https://en.wikipedia.org/wiki/Vibe_coding">Vibe coding - Wikipedia</a></li>
<li><a href="https://mattbaker.blog/2020/04/15/some-mathematical-gems-from-john-conway/">Some Mathematical Gems from John Conway | Matt Baker's Math Blog</a></li>

</ul>
</details>

**Discussion**: Commenters drew a vivid distinction between 'wizardry' (deep understanding aided by tools) and 'sorcery' (summoning and managing powerful forces without fully grasping them), debating which mode Abramov exemplifies. A trained amateur mathematician offered concrete advice on verifying AI-generated proofs by cross-referencing steps with known results, while others noted that AI may function like the 'infinite monkey theorem' — producing candidate theorems that humans must then vet and refine. Readers also praised Abramov's prompting style as a model for how to communicate productively with LLMs.

**Tags**: `#AI-assisted-mathematics`, `#conway-conjecture`, `#vibe-coding`, `#LLMs`, `#mathematical-proofs`

---

<a id="item-11"></a>
## [Korea raises data breach fines to 10% of company revenue](https://www.koreajoongangdaily.com/business/korea-raises-data-breach-fines-to-10-of-revenue/12869899) ⭐️ 7.0/10

South Korea has raised the maximum fine for data breach violations involving intent or gross negligence to up to 10% of the offending company's revenue, a dramatic escalation from the previous cap of approximately KRW 50 million (about USD $42,000) under the Personal Information Protection Act (PIPA). This represents one of the most aggressive revenue-based data protection penalties in the world, potentially setting a global precedent for stronger enforcement. If widely adopted, it could fundamentally shift corporate cost-benefit calculations around security investments, potentially driving up bug bounty payouts and forcing companies to prioritize data protection over short-term profitability. The fines apply specifically to violations involving 'intent or gross negligence,' a threshold some observers consider high enough to limit actual enforcement. The existing PIPA framework, enforced by the Personal Information Protection Commission (PIPC), already mandates breach notification to data subjects and authorities such as the Korean Communications Commission (KCC).

hackernews · throw7 · Sep 18, 20:02 · [Discussion](https://news.ycombinator.com/item?id=49759466)

**Background**: South Korea's Personal Information Protection Act (PIPA), enacted in 2011 and significantly revised in 2023, is the country's foundational privacy law and rivals the EU's GDPR in scope. A data breach is defined as the unauthorized exposure, disclosure, or loss of personal information, which can result from various attacker motives including financial gain, political activism, or espionage. PIPA previously capped fines at a relatively modest KRW 50 million, which critics argued was insufficient to deter large corporations from underinvesting in security.

<details><summary>References</summary>
<ul>
<li><a href="https://lock.pub/en/blog/pipa-korea">Korea 's PIPA ( Personal Information Protection Act )...</a></li>
<li><a href="https://www.clym.io/regulations/personal-information-protection-act-pipa-south-korea">Personal Information Protection Act ( PIPA ) South Korea | Clym</a></li>
<li><a href="https://www.entrust.com/legal-compliance/hsm-solutions/apac/south-koreas-pipa">South Korea PIPA | Entrust</a></li>

</ul>
</details>

**Discussion**: Community sentiment is largely supportive of stronger penalties, with commenters praising Korea's boldness and expressing hope for global adoption. However, substantive concerns were raised: one commenter warned of shell-company loopholes that allow large firms to shift liability to tiny subsidiaries that simply go bankrupt; another questioned whether the 'intent or gross negligence' threshold is too high for meaningful enforcement; and a third noted the second-order effect of increasing bug bounty payouts, citing OpenAI's $6,500 bounty for a trillion-dollar company's serious vulnerabilities as evidence of how underpriced security research currently is.

**Tags**: `#data-privacy`, `#regulation`, `#cybersecurity`, `#compliance`, `#policy`

---

<a id="item-12"></a>
## [Image Generation Models Compared: Cost, Edit, Quality](https://openrouter.ai/blog/insights/image-generation-models-compared/) ⭐️ 7.0/10

OpenRouter benchmarks 20 image generation models across cost, text rendering, reference-image editing, seeds, and text-plus-image responses using their unified Image API.

rss · OpenRouter Blog · Sep 18, 00:00

**Tags**: `#image-generation`, `#model-comparison`, `#benchmarking`, `#AI-API`, `#cost-analysis`

---

<a id="item-13"></a>
## [MiniMax Code Open-Sources Terminal AI Coding Agent](https://www.reddit.com/r/LocalLLaMA/comments/1wjs62f/minimax_code_goes_open_source/) ⭐️ 7.0/10

MiniMax has released the terminal version of its AI coding agent, MiniMax Code, as open source under the MIT license (for first-party code) at github.com/MiniMax-AI/minimax-code. The release (version 0.4.12 source preview) includes a TUI and headless execution mode, code editing, shell commands, diff/test verification, sandboxing, Plan Mode, resumable sessions, subagents, plugins, skills, MCP support, BYOK for OpenAI- and Anthropic-compatible providers, and ACP compatibility. Open-sourcing the agent layer gives the community a concrete artifact to audit network behavior, file-access boundaries, telemetry, and build provenance—an increasingly important concern for AI coding tools that handle proprietary code. It also intensifies competition in the open-source AI coding-agent space, where features like MCP integration, subagent orchestration, and BYOK flexibility are now table stakes. Three important caveats apply: the released source is tagged 0.4.12 (a preview), the desktop application's source is not included, and matching version numbers do not by themselves prove identical build provenance between the published package and the source checkout. The codebase does support ACP for editor integration and MCP for tool/context standardization, which together signal an effort to position the agent as editor- and tool-agnostic.

reddit · r/LocalLLaMA · /u/No_Issue_8224 · Sep 18, 14:44

**Background**: AI coding agents are software assistants that autonomously read, edit, and run code in a developer's environment, often integrating with large language models to plan multi-step tasks. Two emerging standards shape this space: the Model Context Protocol (MCP), an open Anthropic-backed standard for connecting LLMs to external data sources and tools, and the Agent Client Protocol (ACP), which standardizes communication between a coding agent and its host editor or IDE. BYOK (Bring Your Own Key) is a deployment model in which users supply their own API credentials from providers like OpenAI or Anthropic, allowing the tool to route requests through the user's existing accounts rather than the vendor's billed endpoints.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-context-protocol">Introducing the Model Context Protocol \ Anthropic</a></li>
<li><a href="https://agentcommunicationprotocol.dev/">Welcome - Agent Communication Protocol</a></li>
<li><a href="https://openrouter.ai/docs/guides/overview/auth/byok">BYOK - Bring Your Own Keys to OpenRouter</a></li>

</ul>
</details>

**Tags**: `#open-source`, `#ai-coding-agent`, `#MiniMax`, `#developer-tools`, `#mcp`

---

<a id="item-14"></a>
## [Bonsai's ternary model retains ~75% performance, not the 98.2% they marketed](https://www.reddit.com/r/LocalLLaMA/comments/1wjnklv/bonsais_document_reveal_how_much_cherry_picked/) ⭐️ 7.0/10

A community analysis of Bonsai's own whitepaper (page 7) reveals that Ternary Bonsai 2 27B scores 52.8 on Terminal-Bench 2.1 and 60.8 on SWE-bench Verified, compared to 69.7 and 80.6 for the full-precision Qwen3-27B baseline — meaning roughly 75% of full-precision performance is retained, not the 98.2% headline figure Bonsai marketed. This is significant because it exposes how aggressive quantization marketing can mislead buyers about real-world capability loss, particularly for agentic coding workloads where the retained fraction directly translates to task success rates. As ternary and other extreme quantization schemes become more common to reduce inference costs, transparent benchmarking against full-precision baselines is essential for informed model selection. The critique hinges on Bonsai comparing its 27B ternary model against Qwen3.5-27B (41.6 and 72.4 scores) rather than the actual Qwen3.8-27B base it was derived from, which inflates the retention ratio; once compared correctly against Qwen3.8, the model retains only ~75% on both benchmarks. Ternary quantization represents weights with just three discrete values (e.g., -1, 0, +1), offering aggressive memory and compute savings at the cost of expressiveness.

reddit · r/LocalLLaMA · /u/KURD_1_STAN · Sep 18, 11:26

**Background**: Ternary quantization is an extreme form of model compression where neural network weights are restricted to three possible values, drastically reducing memory footprint and potentially accelerating inference compared to full-precision (e.g., FP16 or BF16) models. SWE-bench Verified is a human-curated subset of 500 real-world GitHub bug-fixing tasks from popular Python repositories, widely used to evaluate an AI model's ability to perform autonomous software engineering. Terminal-Bench 2.1 is a benchmark for evaluating AI agents on long-horizon, tool-driven tasks in terminal environments. Performance retention percentages after quantization are a standard way to communicate how much capability is preserved relative to the full-precision original model.

<details><summary>References</summary>
<ul>
<li><a href="https://www.swebench.com/verified.html">SWE-bench Verified</a></li>
<li><a href="https://arxiv.org/pdf/2303.01505">Ternary Quantization : A Survey</a></li>
<li><a href="https://epoch.ai/benchmarks/swe-bench-verified/review">SWE-bench Verified – Benchmark Review | Epoch AI</a></li>

</ul>
</details>

**Discussion**: The discussion highlights community skepticism toward cherry-picked headline metrics in quantized model releases, with the poster providing concrete numbers from Bonsai's own whitepaper to substantiate the critique. Commenters also expressed interest in when a 35B variant of Qwen3 might be released, suggesting ongoing engagement with the underlying model family.

**Tags**: `#quantization`, `#benchmark-analysis`, `#model-evaluation`, `#marketing-criticism`, `#ternary-models`

---

<a id="item-15"></a>
## [Show HN: Cactus Needle 3: 8-29MB automation models can match DeepSeek V4 Flash](https://cactuscompute.com/needle) ⭐️ 6.0/10

Cactus Needle 3 is a suite of tiny (8-29MB) 2-bit quantized models using a novel 'intelligence laddering' architecture that enables subnetwork deployment at different sizes, focused on tool-calling and structured JSON output for on-device automation.

hackernews · HenryNdubuaku · Sep 18, 00:11 · [Discussion](https://news.ycombinator.com/item?id=49748553)

**Tags**: `#small-models`, `#edge-ai`, `#model-compression`, `#tool-calling`, `#on-device-inference`

---

<a id="item-16"></a>
## [How to Write with an LLM](https://sockpuppet.org/blog/2026/09/17/how-to-write-with-an-llm/) ⭐️ 6.0/10

A practical guide on collaborating with LLMs as an editing partner rather than a ghostwriter, arguing for maintaining authorial voice while leveraging AI for structural feedback.

hackernews · joeriddles · Sep 17, 21:48 · [Discussion](https://news.ycombinator.com/item?id=49747070)

**Tags**: `#LLMs`, `#writing`, `#human-AI collaboration`, `#productivity`, `#tooling`

---

<a id="item-17"></a>
## [Is HF starting to move against abliterated models?](https://www.reddit.com/r/LocalLLaMA/comments/1wjyn95/is_hf_starting_to_move_against_abliterated_models/) ⭐️ 6.0/10

Discussion about whether HuggingFace's new safety infrastructure partnership with Baseten and Goodfire signals a policy shift against the 6,000+ abliterated (uncensored) models on its platform.

reddit · r/LocalLLaMA · /u/returnity · Sep 18, 18:43

**Tags**: `#AI safety`, `#HuggingFace`, `#open-source AI`, `#model alignment`, `#abliteration`

---

<a id="item-18"></a>
## [InclusionAI Releases Realtime-Venus: A 9B Omni-Modal Model for Full-Duplex Audio-Visual Interaction](https://www.reddit.com/r/LocalLLaMA/comments/1wjtav9/inclusionairealtimevenus_hugging_face/) ⭐️ 6.0/10

InclusionAI has released Realtime-Venus on Hugging Face, a 9B-parameter omni-modal model adapted from MiniCPM-o 4.5 that supports real-time audio-visual interaction with native full-duplex conversation, proactive response, semantic interruption handling, and training-free long-video memory. The release includes two checkpoints: Realtime-Venus-Omni (full audio-visual) and Realtime-Venus-Audio (audio-only), along with an asynchronous runtime harness on GitHub. Realtime-Venus targets the rapidly growing real-time multimodal AI space, directly competing with models like NVIDIA PersonaPlex and OpenAI's GPT-Realtime in the full-duplex conversation domain. As an open-source 9B model, it makes advanced omni-modal interaction capabilities—previously locked behind proprietary APIs—accessible to researchers and developers, potentially accelerating innovation in conversational agents, embodied AI, and accessibility tools. The model is built on a shared causal timeline architecture that lets it perceive, decide, and generate text and speech simultaneously while distinguishing backchannels, interruptions, corrections, and redirections. Its delegation mechanism emits inline `<delegate>` requests consumed by an asynchronous backend without blocking the conversation, and its training-free long-video memory archives visually informative moments for retrieval without additional fine-tuning.

reddit · r/LocalLLaMA · /u/jacek2023 · Sep 18, 15:27

**Background**: Omni-modal AI refers to systems that can simultaneously process and generate multiple input types—vision, audio, and text—similar to how humans perceive the world. MiniCPM-o 4.5, the base architecture for Realtime-Venus, is an 8B-parameter end-to-end multimodal model built from Qwen3-8B, SigLip2, Whisper-medium, and CosyVoice2, totaling 9B parameters. Full-duplex conversation means the model can listen and speak at the same time, unlike traditional turn-based voice assistants that must finish one before starting the other—a capability that has recently been popularized by systems like Moshi, NVIDIA PersonaPlex, and OpenAI's GPT-Realtime.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/openbmb/MiniCPM-o-4_5">openbmb/ MiniCPM - o - 4 _ 5 · Hugging Face</a></li>
<li><a href="https://research.nvidia.com/labs/adlr/personaplex/">NVIDIA PersonaPlex: Natural Conversational AI With... - NVIDIA ADLR</a></li>
<li><a href="https://www.linkedin.com/pulse/omnivinci-how-nvidia-built-more-efficient-omni-modal-llm-blanchet-nom7e">OmniVinci: How NVIDIA Built a More Efficient Omni - Modal LLM</a></li>

</ul>
</details>

**Tags**: `#multimodal-ai`, `#real-time-speech`, `#audio-visual-model`, `#open-source-models`, `#MiniCPM`

---

<a id="item-19"></a>
## [Ternary Bonsai 2: 27B Model Compressed to Under 6GB Runs In-Browser](https://www.reddit.com/r/LocalLLaMA/comments/1wj6c4l/ternary_bonsai_2_27b_just_released_on_hugging/) ⭐️ 6.0/10

Prism-ML has released Ternary Bonsai 2, a 27B-parameter language model derived from Qwen3-8-27B, on Hugging Face. The model uses ternary weights (–1, 0, +1) to shrink the original FP16 checkpoint by approximately 9× to under 6GB, with the authors claiming 98.2% capability retention. A WebGPU-based browser demo is also available, allowing the model to run locally without a server. This release pushes the boundary of consumer-accessible local inference: a 27B-parameter model fitting in under 6GB dramatically lowers the hardware barrier for running strong open-weight LLMs, including on laptops with modest GPUs and on consumer mobile devices. Combined with WebGPU browser support now standard across all major browsers, it points toward a future where capable LLMs can be loaded and used on any device without installation or cloud dependencies. The architecture is unchanged from the base model, with only the weight representation altered from 16-bit floats to ternary values (effectively ~2 bits per weight plus a scaling factor). The 98.2% capability retention figure comes from the model card itself and has not yet been independently verified. Ternary quantization is conceptually related to Microsoft's BitNet b1.58 approach, which also uses three discrete weight values, though the specific training and scaling techniques differ.

reddit · r/LocalLLaMA · /u/xenovatech · Sep 17, 21:05

**Background**: Quantization is a compression technique that reduces the numerical precision of neural network weights to shrink model size and speed up inference. Ternary quantization is one of the most aggressive forms, mapping all weights to just three possible values: –1, 0, and +1 (with an optional scaling factor). Compared to the 16-bit FP16 weights normally used for LLM inference, ternary representation can theoretically achieve up to ~8× compression, though practical implementations typically achieve around 4–9× depending on metadata overhead. WebGPU is a modern browser API that provides JavaScript applications with direct access to the GPU, enabling hardware-accelerated computation—including neural network inference—directly in the web browser without plugins or downloads.

<details><summary>References</summary>
<ul>
<li><a href="https://www.emergentmind.com/topics/ternary-quantization">Ternary Quantization in Neural Networks - emergentmind.com</a></li>
<li><a href="https://arxiv.org/abs/1612.01064">[1612.01064] Trained Ternary Quantization - arXiv.org Ternary Quantization in Neural Networks - emergentmind.com [1612.01064] Trained Ternary Quantization TRAINED TERNARY QUANTIZATION - scispace.com Trained Ternary Quantization - GitHub</a></li>
<li><a href="https://www.ddevtools.com/updates/2026-01-webgpu-webnn-browser-ai">WebGPU and WebNN: The APIs Making Browser AI ... | ddevtools</a></li>

</ul>
</details>

**Tags**: `#local-llm`, `#quantization`, `#ternary-weights`, `#webgpu`, `#model-release`

---

<a id="item-20"></a>
## [Benchmark of 24 LLMs vs. Human Writers on 475 Creative Writing Prompts](https://www.reddit.com/r/LocalLLaMA/comments/1wjwhxc/we_benchmarked_24_llms_against_human_writers_on/) ⭐️ 6.0/10

A new Creative Writing v1 benchmark by Vulsar AI compared 24 LLMs against human writers across 475 prompts, using a custom reward model trained on human preferences to predict large-group reader judgments. The results show that the strongest frontier models already outperform a talented amateur writer cohort, while professional human writers still lead by a wide margin. Creative writing is a domain that has been largely underserved by LLM benchmarks, which tend to focus on coding, math, and factual reasoning. This benchmark fills an important evaluation gap and provides empirical evidence about where AI-generated creative text currently sits on the quality spectrum between amateurs and professionals — relevant for writers, publishers, and AI developers building content tools. The rankings rely on a proxy reward model rather than full-scale human evaluation, meaning they predict aggregate reader preferences but not any individual's taste. The authors explicitly note that creative writing quality is inherently subjective, and the benchmark is hosted as an interactive site where users can browse rankings and compare model outputs side by side.

reddit · r/LocalLLaMA · /u/drooolingidiot · Sep 18, 17:24

**Background**: Most public LLM benchmarks evaluate reasoning, coding, or knowledge tasks, leaving creative and open-ended generation under-tested. Frontier AI models refer to the most capable, state-of-the-art systems currently available from major labs. A reward model trained on human preferences is a common component in RLHF (Reinforcement Learning from Human Feedback) pipelines, where it serves as a proxy judge for output quality — useful for evaluation at scale but limited by how well it approximates genuine human judgment.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/html/2409.19024">Elephant in the Room: Unveiling the Impact of Reward Model Quality...</a></li>
<li><a href="https://www.brinqa.com/glossary/frontier-ai-models">Frontier AI Models : Definition & Security Impact</a></li>
<li><a href="https://readmedium.com/reinforcement-learning-from-human-feedback-rlhf-ec56d1beaa3c">Reinforcement learning from human feedback (RLHF)</a></li>

</ul>
</details>

**Tags**: `#LLM-benchmark`, `#creative-writing`, `#LLM-evaluation`, `#reward-model`, `#AI-research`

---