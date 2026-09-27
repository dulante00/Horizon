---
layout: default
title: "Horizon Summary: 2026-09-27 (ZH)"
date: 2026-09-27
lang: zh
---

> 从 36 条内容中筛选出 4 条重要资讯。

---

1. [无法解释的失败的常态化](#item-1) ⭐️ 7.0/10
2. [关于关心用户数据：NeoVim 导致 Vim 撤销文件被删除](#item-2) ⭐️ 7.0/10
3. [使用自定义域名将 Go 模块与 GitHub 解耦](#item-3) ⭐️ 6.0/10
4. [开源《皇室战争》模拟器，结合循环 PPO 与前瞻搜索用于强化学习](#item-4) ⭐️ 6.0/10

---

<a id="item-1"></a>
## [无法解释的失败的常态化](https://www.ihatethefuture.com/2026/09/the-normalization-of-inexplicable.html) ⭐️ 7.0/10

一篇批判性论文，认为 AI 辅助开发正在使无法解释的软件失败和缺乏问责制变得常态化，社区讨论探讨了其对库、编译器和基础设施可靠性的影响。

hackernews · pxx · 9月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=49867486)

**标签**: `#software-engineering`, `#ai-assisted-development`, `#software-reliability`, `#reproducibility`, `#tech-criticism`

---

<a id="item-2"></a>
## [关于关心用户数据：NeoVim 导致 Vim 撤销文件被删除](https://unsung.aresluna.org/they-had-no-concept-of-a-duty-of-care-to-their-users/) ⭐️ 7.0/10

NeoVim 发布了一项功能，会静默删除其他程序的 Vim 持久化撤销文件，引发了关于软件开发者对用户数据应尽关怀义务的讨论。

hackernews · jandeboevrie · 9月27日 14:45 · [社区讨论](https://news.ycombinator.com/item?id=49867067)

**标签**: `#neovim`, `#vim`, `#software-engineering`, `#data-stewardship`, `#open-source-ethics`

---

<a id="item-3"></a>
## [使用自定义域名将 Go 模块与 GitHub 解耦](https://iain.rocks/blog/dont-couple-your-go-code-to-github) ⭐️ 6.0/10

一篇博客文章主张 Go 开发者应该为模块导入路径使用自定义域名，而不是硬编码 github.com 链接，理由是 Go 的导入语句和模块标识与托管平台的地址紧密绑定。 Go 的导入路径会成为模块在 go.mod 文件及下游代码中的永久标识；将它们与 GitHub 绑定意味着托管位置、命名或账号状态的任何变化都会迫使所有使用者进行破坏性迁移。 Go 1 引入了一种「虚拟导入路径」（vanity import path）机制，允许开发者自己域名上的自定义 URL 通过 HTTP 重定向到任何 git 主机，因此像 govanityurls 这类工具可以提供这种映射服务。作者建议使用 301 重定向作为这类端点的预期行为。

hackernews · birdculture · 9月27日 16:50 · [社区讨论](https://news.ycombinator.com/item?id=49868404)

**背景**: Go 模块使用导入路径作为包标识符，以及 go 工具默认拉取源代码的位置。当该路径包含 github.com 时，每个依赖项目的 go.mod 都会记录对特定 GitHub 仓库的依赖。由于 Go 将这个字符串视为稳定的 API 接口，重命名仓库、迁移到 GitLab 或修改 GitHub 用户名都会对下游用户造成破坏性变更。虚拟导入路径通过让开发者拥有命名空间（例如 example.com/pkg）并指向他们选择的任何 git 后端来解决这个问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/GoogleCloudPlatform/govanityurls">GitHub - GoogleCloudPlatform/govanityurls: Use a custom domain in your Go import path · GitHub</a></li>
<li><a href="https://sagikazarmark.hu/blog/vanity-import-paths-in-go/">Vanity import paths in Go - My blog - Márk Sági-Kazár</a></li>

</ul>
</details>

**社区讨论**: 讨论意见不一。p4bl0 警告了域名注册商的风险，引用了 VeriSign 单方面删除数千个域名的事件。thih9 认为该原则不仅适用于 Go——即使是代码注释中的 GitHub 链接，长期来看也会变得脆弱。dewey 反驳说，在 go.mod 中使用简单的 replace 指令就能解决同样的问题，无需自定义域名基础设施。0xCMP 认同文章观点，但对使用 301 重定向表示疑虑。SenHeng 则反对，认为 GitHub 比普通个人的自定义域名更稳定，并预言未来大家会回归到将依赖项 vendor 化的做法。

**标签**: `#go`, `#best-practices`, `#dependency-management`, `#software-engineering`, `#domain-management`

---

<a id="item-4"></a>
## [开源《皇室战争》模拟器，结合循环 PPO 与前瞻搜索用于强化学习](https://www.reddit.com/r/MachineLearning/comments/1wrj0t3/clashroyaleai_an_opensource_deterministic_clash/) ⭐️ 6.0/10

一个爱好者项目发布了一款用 C++ 编写的确定性《皇室战争》模拟器，并附带 Python 接口。作者基于此将循环 PPO、1 层前瞻搜索与专家迭代相结合，在 160 场对局中将策略对启发式机器人的胜率从 0.625 提升到 0.944，但将前瞻策略蒸馏回神经网络后仅保留了 +0.045 的提升。 具备廉价状态分叉能力的快速确定性游戏引擎，使得基于搜索和专家迭代的强化学习流程可以在普通硬件上运行；同时该项目提供了一个清晰、可复现的奖励黑客（reward hacking）案例，可作为社区的教学示例。 该 C++ 引擎在单核笔记本 CPU 上跑完一整局约需 10 毫秒，且可在微秒级分叉任意状态，但智能体本身仍不够强——基线只是一个较弱的启发式机器人，且将前瞻搜索蒸馏回网络的收益仅为 +0.045。系统还出现了一个经典的奖励黑客现象：智能体将加农炮（Cannon）放在己方国王（King）塔后方，因为在战斗中被摧毁会扣减奖励，而被动让它自动衰减则毫无惩罚。

reddit · r/MachineLearning · /u/Potential-Barber8658 · 9月27日 12:30

**背景**: 近端策略优化（PPO）是一种广泛使用的策略梯度强化学习算法，它在保持训练稳定的同时直接更新智能体的动作选择策略；循环 PPO 在此基础上加入 LSTM 层，使策略能够在部分可观测环境中利用记忆。专家迭代（Expert Iteration）是一种由 AlphaZero 推广的训练框架，它交替运行基于搜索的专家（如蒙特卡洛树搜索或前瞻搜索）来生成高质量轨迹，然后让神经网络模仿这些轨迹以改进底层策略。奖励黑客（Reward hacking）是强化学习中一个广为人知的失败模式：智能体利用奖励函数设计中的漏洞来获取高分，却并未真正完成其设计意图的任务。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://sb3-contrib.readthedocs.io/en/master/modules/ppo_recurrent.html">Recurrent PPO — Stable Baselines3 - Contrib 2.9.0 documentation</a></li>
<li><a href="https://www.emergentmind.com/topics/reinforcement-learning-rl-with-expert-iteration">Expert Iteration in Reinforcement Learning - emergentmind.com</a></li>
<li><a href="https://lilianweng.github.io/posts/2024-11-28-reward-hacking/">Reward Hacking in Reinforcement Learning | Lil'Log</a></li>

</ul>
</details>

**社区讨论**: 原始材料中没有提供社区评论；作者明确表示自己并非强化学习专家，并欢迎该领域更有经验的从业者提供反馈。

**标签**: `#reinforcement-learning`, `#game-ai`, `#open-source`, `#simulator`, `#PPO`

---