# 资料库总索引

手动维护的仓库内容索引。新增、重命名或删除正式资产时，请同步更新本文件。

## Prompts

### Writing（写作）

| 名称 | 路径 | 用途 | 状态 |
| --- | --- | --- | --- |
| 技术报告撰写 | [prompts/writing/technical-report.md](prompts/writing/technical-report.md) | 撰写结构清晰、结论先行的技术报告与实验总结 | Active |

### Engineering（工程）

| 名称 | 路径 | 用途 | 状态 |
| --- | --- | --- | --- |
| 嵌入式代码审查 | [prompts/engineering/review-embedded-code.md](prompts/engineering/review-embedded-code.md) | 审查嵌入式 C/C++ 代码的实时性、内存、外设与边界风险 | Active |
| 采集与抓包数据分析 | [prompts/engineering/analyze-capture-data.md](prompts/engineering/analyze-capture-data.md) | 分析示波器、逻辑分析仪、总线抓包与传感器时序数据 | Active |

### Codex（协作与工作流）

| 名称 | 路径 | 用途 | 状态 |
| --- | --- | --- | --- |
| 新项目组装指令 | [prompts/codex/assemble-project.md](prompts/codex/assemble-project.md) | 收到明确项目需求后，按需选取资产并在目标目录组装项目 | Active |
| 跨线程任务交接 | [prompts/codex/cross-thread-handoff.md](prompts/codex/cross-thread-handoff.md) | 生成结构化交接文档，便于新线程无缝接续上下文 | Active |

## Skills

| Skill 名称 | 路径 | 能力说明 | 配套资源 | 状态 |
| --- | --- | --- | --- | --- |
| `project-bootstrap` | [.agents/skills/project-bootstrap/SKILL.md](.agents/skills/project-bootstrap/SKILL.md) | 在指定目标目录初始化新项目并按需引入资料库中的 Prompt 与 Skill | [.agents/skills/project-bootstrap/assets/project-brief.md](.agents/skills/project-bootstrap/assets/project-brief.md) | Active |

## Templates

| 名称 | 路径 | 用途 |
| --- | --- | --- |
| Prompt 模板 | [templates/prompt-template.md](templates/prompt-template.md) | 创建新 Prompt 时的标准结构模板 |
| Skill 模板 | [templates/skill-template/SKILL.md](templates/skill-template/SKILL.md) | 创建新 Skill 时的标准 `SKILL.md` 模板 |

## Inbox

- [inbox/README.md](inbox/README.md)：暂存尚未归类或待打磨的草稿与想法。
