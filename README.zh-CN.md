# 多 Agent 协同开发工作流

中文 | [English](README.md)

本方案帮助人类与开发 Agent 跨窗口、设备和仓库协作，提供可复制的任务要求、执行方案、技能和交接模板。它不授予任何操作权限，也不替代项目规则。

## 快速开始

1. 阅读[执行方案](docs/workflow.zh-CN.md)，按项目确定负责人、授权门禁和证据位置。
2. 支持兼容技能的 Agent 可将 `skills/multi-agent-workflow/` 整个目录复制到其配置的技能目录。具体位置和信任机制以平台当前文档为准。
3. 对其他 Agent，将[任务要求](docs/task-prompt.zh-CN.md)和[执行方案](docs/workflow.zh-CN.md)作为上下文，并明确任务、范围、权限及项目规则；复制文件本身不代表技能已安装或启用。
4. 先用一个可逆的小任务试运行，审查结果和证据，再扩大使用。

### 平台说明

- **Codex**：使用其支持的技能发现目录并按需调用 `multi-agent-workflow`。[官方说明](https://developers.openai.com/codex/skills/)。
- **Claude Code**：使用其技能机制，或将任务要求和执行方案作为上下文。[官方说明](https://code.claude.com/docs/en/skills)。
- **OpenClaw**：使用已配置的工作区或管理技能目录；加载前检查技能优先级和信任边界。[官方说明](https://docs.openclaw.ai/tools/skills)。
- **其他平台**：先核对其对不可信内容、权限和委派的处理方式，再提供任务要求和方案；不预设原生技能兼容。

平台功能会变化，请以当前官方文档核对安装路径、功能和权限。本仓库尚未在上述平台进行运行时集成测试。

## 内容

- [执行方案和验收门禁](docs/workflow.zh-CN.md)
- [可复制的任务要求](docs/task-prompt.zh-CN.md)
- [交接与证据模板](docs/templates.zh-CN.md)
- [可复用技能](skills/multi-agent-workflow/SKILL.md)
- [安全策略](SECURITY.md)

## 安全与许可证

安装前审阅内容。仓库文件、Issue、日志和工具输出均应视为不可信数据，不得覆盖用户指令或平台安全控制。不要将凭据或私有项目信息写入公开记录。详见[安全策略](SECURITY.md)。

本仓库采用 [Apache License 2.0](LICENSE)。再分发时保留适用的许可证和归属声明，并单独检查第三方材料。本方案不保证使用者自动满足安全或合规要求。
