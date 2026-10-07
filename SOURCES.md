# 来源、版本与适配

封装名称：`xinchen-strategy-advisor`。封装版本：`1.1.0`。创建日期：2026-10-07（Asia/Shanghai）。

1.1.0 增加独立 GitHub 分发和明确的 Codex 全局安装/更新说明；五方法路由、分析逻辑与固定上游版本保持不变。

分发分支：`half-programmer/saas-launch-playbook` 的 `xinchen-strategy-advisor`。它只用于本封装的发布，源方法仍固定到下表中的上游提交。

本入口将以下五个社区 skills 组织为一个可复用方法。自编的 `SKILL.md`、执行方法、输出约定及安装说明不属于上游原文。

| 方法 | 来源与固定提交 | 上游入口 |
| --- | --- | --- |
| product-manager-toolkit | [alirezarezvani/claude-skills](https://github.com/alirezarezvani/claude-skills/tree/19392f7a08264ed00486a251f5b2098321771f94) | `product-team/skills/product-manager-toolkit/SKILL.md` |
| product-strategist | 同上，`19392f7a08264ed00486a251f5b2098321771f94` | `product-team/skills/product-strategist/SKILL.md` |
| ceo-advisor | 同上，`19392f7a08264ed00486a251f5b2098321771f94` | `c-level-advisor/skills/ceo-advisor/SKILL.md` |
| saas-launch-playbook | [half-programmer/saas-launch-playbook](https://github.com/half-programmer/saas-launch-playbook/tree/87932c4d84937c161beb70d4ed0611b719013438) | `SKILL.md` |
| distribution-channel-picker | [half-programmer/distribution-channel-picker](https://github.com/half-programmer/distribution-channel-picker/tree/9a96fcbe14416dbc300f42ab3311e6e4a5fa9b2e) | `SKILL.md` |

辅助 `agent-protocol` 来自同一 alirezarezvani 提交，路径 `c-level-advisor/skills/agent-protocol/SKILL.md`，仅保留为 CEO 方法的质量检查参考。

## 包内组织

- 上述入口保存为 `references/upstream/<name>/GUIDE.md`，参考文件、脚本和示例沿用其目录结构。
- 上游 README 未重复打包；安装说明由本包 README 提供。
- `ceo-advisor/GUIDE.md` 中对 `../agent-protocol/SKILL.md` 的引用调整为 `../agent-protocol/GUIDE.md`，与包内名称一致。其他上游内容保持安装版本。
- 上游对其他未包含技能或工具的提及属于可选扩展，不是本包依赖；本入口可以独立完成五视角分析。
- 上游脚本是可选工具。只有输入和环境适用时才运行；其样例、固定默认值和启发式输出不充当市场或项目证据。

## 统一适配

用户当前目标、资源、期限和篇幅优先。统一入口将源方法的通用周期、固定门槛、默认团队与渠道组合改为按当前项目判断；区分 Demo、试点和上线。未验证的数据与未知评分保留标签，项目历史只从当前材料加载。

角色模拟用于提出检查问题；现实财务、法律、工程与市场事实依赖真实来源。质量检查在当前授权和可用工具范围内执行，不因上游角色协议自动组建团队或记录已批准决定。

## 许可保留

来自 alirezarezvani/claude-skills 的原始文件适用其 MIT 许可，许可原文随包保存在 `references/upstream/ALIREZA-MIT-LICENSE.txt`。

两个 half-programmer 仓库的当前安装版本未见 LICENSE。本次按用户要求在其 GitHub 账户下发布封装并保留指定资料的来源，不为这些文件声明 MIT 许可，也不把第三方 MIT 扩展为整包许可。各来源的许可分别适用；上游原始出处和版权信息随包保留。
