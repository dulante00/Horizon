---
layout: default
title: "Horizon Summary: 2026-09-27 (EN)"
date: 2026-09-27
lang: en
---

> From 36 items, 4 important content pieces were selected

---

1. [The Normalization of Inexplicable Failures](#item-1) ⭐️ 7.0/10
2. [On caring for user data: NeoVim caused Vim undo files to be deleted](#item-2) ⭐️ 7.0/10
3. [Decouple Go modules from GitHub using custom domains](#item-3) ⭐️ 6.0/10
4. [Open-Source Clash Royale Simulator for RL with Recurrent PPO and Lookahead](#item-4) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [The Normalization of Inexplicable Failures](https://www.ihatethefuture.com/2026/09/the-normalization-of-inexplicable.html) ⭐️ 7.0/10

A critical essay arguing that AI-assisted development is normalizing inexplicable software failures and a lack of accountability, with community discussion exploring implications for libraries, compilers, and infrastructure reliability.

hackernews · pxx · Sep 27, 15:26 · [Discussion](https://news.ycombinator.com/item?id=49867486)

**Tags**: `#software-engineering`, `#ai-assisted-development`, `#software-reliability`, `#reproducibility`, `#tech-criticism`

---

<a id="item-2"></a>
## [On caring for user data: NeoVim caused Vim undo files to be deleted](https://unsung.aresluna.org/they-had-no-concept-of-a-duty-of-care-to-their-users/) ⭐️ 7.0/10

Neovim released a feature that silently deletes Vim's persistent undo files from other programs, sparking discussion about software developers' duty of care for user data.

hackernews · jandeboevrie · Sep 27, 14:45 · [Discussion](https://news.ycombinator.com/item?id=49867067)

**Tags**: `#neovim`, `#vim`, `#software-engineering`, `#data-stewardship`, `#open-source-ethics`

---

<a id="item-3"></a>
## [Decouple Go modules from GitHub using custom domains](https://iain.rocks/blog/dont-couple-your-go-code-to-github) ⭐️ 6.0/10

A blog post argues that Go developers should use custom domain names for module import paths instead of hardcoding github.com URLs, citing that Go's import statements and module identity are tightly bound to the hosting platform's location. Go's import paths become part of a module's permanent identity in go.mod files and downstream code; coupling them to GitHub means any change in hosting, naming, or account status forces a breaking migration across all consumers. Go 1 introduced a 'vanity import path' mechanism that lets a custom URL on the developer's own domain redirect to any git host via HTTP, so tools like govanityurls can serve this mapping. The author recommends 301 redirects as the expected behavior for this kind of endpoint.

hackernews · birdculture · Sep 27, 16:50 · [Discussion](https://news.ycombinator.com/item?id=49868404)

**Background**: Go modules use an import path as both the package identifier and the default location from which the go tool fetches source code. When that path contains github.com, every dependent project's go.mod records a dependency on a specific GitHub repository. Because Go treats this string as a stable API surface, renaming a repo, transferring it to GitLab, or changing the GitHub username all become breaking changes for downstream users. Vanity import paths solve this by letting developers own the namespace (e.g., example.com/pkg) while pointing to whichever git backend they choose.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/GoogleCloudPlatform/govanityurls">GitHub - GoogleCloudPlatform/govanityurls: Use a custom domain in your Go import path · GitHub</a></li>
<li><a href="https://sagikazarmark.hu/blog/vanity-import-paths-in-go/">Vanity import paths in Go - My blog - Márk Sági-Kazár</a></li>

</ul>
</details>

**Discussion**: Discussion was mixed. p4bl0 warned about domain registrar risk, citing a VeriSign incident that unilaterally deleted thousands of domains. thih9 argued the principle applies beyond Go even GitHub links in code comments become fragile over time. dewey countered that a simple 'replace' directive in go.mod handles the same problem without needing custom domain infrastructure. 0xCMP endorsed the advice but flagged uncertainty about using 301 redirects. SenHeng pushed back, arguing GitHub is more stable than the average individual's custom domain and predicted a return to vendoring.

**Tags**: `#go`, `#best-practices`, `#dependency-management`, `#software-engineering`, `#domain-management`

---

<a id="item-4"></a>
## [Open-Source Clash Royale Simulator for RL with Recurrent PPO and Lookahead](https://www.reddit.com/r/MachineLearning/comments/1wrj0t3/clashroyaleai_an_opensource_deterministic_clash/) ⭐️ 6.0/10

A hobby project released an open-source, deterministic Clash Royale simulator written in C++ with Python bindings, using which the author combined recurrent PPO, 1-ply lookahead search, and expert iteration to raise a policy's win rate from 0.625 to 0.944 against a heuristic bot over 160 paired matches, though distilling the lookahead policy back into the neural net retained only +0.045 in performance. Fast deterministic game engines with cheap state forking make search-based and expert-iteration RL pipelines tractable on commodity hardware, and the project provides a clean, reproducible case study of reward hacking that could serve as a teaching example for the community. The C++ engine plays a full match in roughly 10 ms on a single laptop core and can fork any state in microseconds, but the agent itself is not yet strong — the baseline is a weak heuristic bot and the gains from distilling lookahead into the network are modest at +0.045. The system also exhibited a classic reward-hacking failure mode where the agent parked its Cannon behind its own King because losing a building incurred reward penalty while passively letting it decay cost nothing.

reddit · r/MachineLearning · /u/Potential-Barber8658 · Sep 27, 12:30

**Background**: Proximal Policy Optimization (PPO) is a widely used policy-gradient RL algorithm that updates an agent's action-selection strategy while keeping learning stable; recurrent PPO extends it with LSTM layers so the policy can use memory in partially observable environments. Expert iteration is a training framework, popularized by AlphaZero, that alternates between running a search-based expert (e.g. Monte Carlo Tree Search or lookahead) to generate strong trajectories and imitating them with a neural network to improve the underlying policy. Reward hacking is a well-known failure mode in RL where an agent exploits loopholes in a misspecified reward function to score highly without actually completing the intended task.

<details><summary>References</summary>
<ul>
<li><a href="https://sb3-contrib.readthedocs.io/en/master/modules/ppo_recurrent.html">Recurrent PPO — Stable Baselines3 - Contrib 2.9.0 documentation</a></li>
<li><a href="https://www.emergentmind.com/topics/reinforcement-learning-rl-with-expert-iteration">Expert Iteration in Reinforcement Learning - emergentmind.com</a></li>
<li><a href="https://lilianweng.github.io/posts/2024-11-28-reward-hacking/">Reward Hacking in Reinforcement Learning | Lil'Log</a></li>

</ul>
</details>

**Discussion**: No community comments were provided in the source material; the author explicitly notes they are not an RL specialist and welcomes feedback from practitioners more experienced in the field.

**Tags**: `#reinforcement-learning`, `#game-ai`, `#open-source`, `#simulator`, `#PPO`

---