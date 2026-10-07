# Xinchen Strategy Advisor

**xinchen 的战略顾问** · 调用名：`xinchen-strategy-advisor`

一个入口统筹五个方法：用户需求、产品战略、商业决策、SaaS 发布和分发渠道。默认输出「总判断 → 分项依据 → 人和 AI 的行动、产物与验收」。单点问题按需加载，深度评审整合五个视角。

## 安装一次，各项目调用

在运行 Codex 的客户端机器上执行：

```bash
npx --yes skills@1.7.0 add half-programmer/xinchen-strategy-advisor --global --agent codex --skill xinchen-strategy-advisor --copy --yes
```

`--global` 是关键：安装到用户级目录，而不是当前项目的 `.agents/skills/`。`--copy` 保留完整文件，避免依赖原仓库或临时下载目录。重新加载技能或新开会话后，可在该客户端的任意项目调用。

验证安装：

```bash
npx --yes skills@1.7.0 list --global --agent codex
```

列表中应出现 `xinchen-strategy-advisor`。本命令通过 `skills@1.7.0` 安装到 Codex 支持的通用用户技能目录 `~/.agents/skills/xinchen-strategy-advisor/`，无需逐个项目复制。客户端若使用自己的技能管理入口，以其安装路径和重新加载结果为准。

### 已有本地仓库或完整 ZIP

进入解压后含 `SKILL.md` 的目录，执行：

```bash
npx --yes skills@1.7.0 add . --global --agent codex --skill xinchen-strategy-advisor --copy --yes
```

不使用安装 CLI 时，将整个技能目录放入客户端支持的用户级技能目录，如 `~/.agents/skills/xinchen-strategy-advisor/`，保留 `references/` 和 `agents/` 后重新加载。只下载 `SKILL.md` 不足以读取五个方法。

### 不同机器和云环境

用户级安装对同一客户端/机器中的所有项目生效，不会自动同步到另一台机器或独立云环境。每台机器安装一次；云环境把上述全局安装命令加入该环境的 setup script，保存并发布配置，使后续使用该环境的项目获得技能。

如果客户端提供账户级自定义技能上传，也可导入完整 ZIP，以导入成功和技能列表可见为准。GitHub 发布、当前机器全局安装、账户级注册是三个分别验证的状态。

## 调用

```text
使用 $xinchen-strategy-advisor，深度评审这个项目。
先给总判断，再给分项分析，最后列出未来四周人和 AI
各自的任务、交付物、验收标准，以及三个关键待验证假设。
```

中文也可写：`用 xinchen 的战略顾问，帮我判断……`。

| 模式 | 适用情况 | 示例 |
| --- | --- | --- |
| 快速判断 | 一个明确问题，短答 | `快速判断：先做访谈还是做 Demo？` |
| 深度评审 | 整体项目与战略 | `深度评审：比较商业路径，给总分报告。` |
| 行动计划 | 已有方向，需排任务 | `行动计划：截止月底，拆解人和 AI 的任务。` |
| 阶段复盘 | 有计划和实际结果 | `阶段复盘：根据这两周的结果更新建议。` |

单点问题默认快速判断，整体项目评审默认深度评审。一页问题不会强制展开五篇报告。技能保存方法；项目背景来自本轮资料，续接同一项目时请提供最新材料或上一轮续接摘要。

## 五个方法

| 方法 | 分工 |
| --- | --- |
| `product-manager-toolkit` | 需求、访谈、任务闭环、MVP、优先级、PRD |
| `product-strategist` | 方向、目标、指标、阶段路线、OKR |
| `ceo-advisor` | 商业路径、资源、成本与重大取舍 |
| `saas-launch-playbook` | 付费意愿、楔子定位、发布与迭代 |
| `distribution-channel-picker` | 五维渠道选择和增长实验 |

五方法及所需参考文件随包提供，无需再次安装依赖。辅助协议仅作质量检查参考，不增加业务方法数量。未知输入保持未知，兴趣、使用和付款分开记录；建议目标与已批准决策分开。

## 更新与移除

更新时再次执行上面的 GitHub 全局安装命令。它会获取仓库最新版本并更新用户级副本。重新加载技能后生效。

移除：

```bash
npx --yes skills@1.7.0 remove xinchen-strategy-advisor --global --agent codex --yes
```

## 目录和来源

```text
SKILL.md
README.md
SOURCES.md
agents/openai.yaml
references/workflow.md
references/report-format.md
references/upstream/<method>/GUIDE.md
references/upstream/<method>/references/...
```

`GUIDE.md` 是上游入口的包内名称，避免参考方法被重复注册。只有通用方法、参考资料、工具和上游示例，不包含项目报告、上传材料、客户数据或凭据。固定来源、版本、许可与适配见 [SOURCES.md](SOURCES.md)。
