# 大模型安全日报

该日报与原 Horizon 日报是两个独立任务：使用独立配置、独立 GitHub Actions workflow 和独立飞书 Webhook Secret。

## 调度与配置

| 项目 | 原日报 | 大模型安全日报 |
| --- | --- | --- |
| Workflow | `daily-summary.yml` | `daily-security-summary.yml` |
| 配置 | `data/config.github.json` | `data/security/config.json` |
| 飞书 Secret | `HORIZON_WEBHOOK_URL` | `HORIZON_SECURITY_WEBHOOK_URL` |
| 时间 | 05:00（北京时间） | 06:17（北京时间） |
| 输出语言 | 中英双语 | 中文 |

在 GitHub 仓库的 **Settings → Secrets and variables → Actions** 新增
`HORIZON_SECURITY_WEBHOOK_URL`。它可以指向新的飞书机器人；如果仍发到同一个群，
也要保留独立 Secret，便于以后单独迁移或停用。

## 来源分级

- `T1`：政府、标准组织等官方原文，可作为决策依据。
- `T2`：厂商一手信息、预印本或站点检索线索，需要交叉验证。
- `T3`：公开社区线索，只用于发现事件，不直接作为事实依据。

每个 RSS 信息源通过 `source_class` 标记六类来源，通过 `credibility` 标记可信度。
这两个字段会进入 AI 评分上下文，并显示在飞书日报条目的来源行中。

初始配置覆盖六类来源，其中 MITRE ATLAS 的官方数据更新用于补充真实攻击知识库，
Hugging Face 社区博客按 T3 线索源处理。

当前国家网信办、TC260、中国信通院和 EU AI Office 没有在本项目中使用稳定的官方 RSS，
暂时以站点限定新闻 RSS 发现线索，并明确标为 T2。正式决策必须点击回查官网原文。

## 手动验证

```bash
MINIMAX_API_KEY=... \
HORIZON_SECURITY_WEBHOOK_URL=... \
uv run horizon --data-dir data/security --hours 30
```

也可以在 GitHub Actions 页面手动运行 **Daily LLM Security Summary**。
