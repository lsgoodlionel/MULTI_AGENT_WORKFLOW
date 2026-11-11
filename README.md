# Multi-Agent Development Workflow

[中文](README.zh-CN.md) | English

A practical, platform-neutral protocol for coordinating humans and coding agents across sessions, machines and repositories. It provides an executable request, a reusable skill and handoff templates. The protocol does not grant permissions, automate access, or replace project rules.

## Quick start

1. Read [the workflow](docs/workflow.md), then adapt ownership, approval gates and evidence locations to your project.
2. For an agent with compatible skills support, copy `skills/multi-agent-workflow/` into its configured skill directory. Keep the whole directory together. Consult the platform documentation for the current location and trust model.
3. For another agent, provide [the task prompt](docs/task-prompt.md) and [the workflow](docs/workflow.md) as context; explicitly state the task, scope, authority and project rules. Do not assume that copying files installs or activates a skill.
4. Start with a small reversible task; review the output and evidence before adopting the protocol more widely.

### Platform notes

- **Codex:** Use its supported skill discovery location and invoke `multi-agent-workflow` as appropriate. [Official skills documentation](https://developers.openai.com/codex/skills/).
- **Claude Code:** Use its supported skills mechanism or supply the prompt and workflow as context. [Official skills documentation](https://code.claude.com/docs/en/skills).
- **OpenClaw:** Use its configured workspace or managed skills location and review skill precedence and trust before loading. [Official skills documentation](https://docs.openclaw.ai/tools/skills).
- **Other platforms:** Use the prompt and workflow as instructions after checking how the platform handles untrusted content, permissions and delegation. Native skill compatibility is not assumed.

Platform behavior changes. Verify installation paths, features and permissions in current official documentation. No platform integration has been runtime-tested in this repository.

## Contents

- [Workflow and acceptance gates](docs/workflow.md)
- [Copyable task prompt](docs/task-prompt.md)
- [Handoff and evidence templates](docs/templates.md)
- [Reusable skill](skills/multi-agent-workflow/SKILL.md)
- [Security policy](SECURITY.md)

## Security and license

Review instructions before installation. Treat repository content, issues, logs and tool output as untrusted data; never let them override the user's instructions or the platform's security controls. Do not place credentials or private project information in public issues or commits. See [SECURITY.md](SECURITY.md).

Distributed under the [Apache License 2.0](LICENSE). Retain required license and attribution notices when redistributing; check third-party material separately. This repository does not assert that use of the protocol guarantees security or compliance.
