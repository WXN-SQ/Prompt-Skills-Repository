# AGENTS.md

本文件面向 Codex 及其他代码/文档 Agent，定义在本仓库中查找、调用与维护 Prompt 和 Skill 的行为规范。

## 1. 仓库定位与硬性边界

- 本仓库是个人 Prompt 与 Skill 资料库，**不是**具体业务项目的开发工作区。
- **仅在收到明确的新项目需求且指定目标目录时**，才从本仓库选取相关 Prompt、Skill 和模板，在指定目标目录组装项目；禁止在本仓库根目录直接创建业务项目代码或临时产物。
- 全仓使用纯文本文件（默认 Markdown），**禁止**引入数据库、静态网站框架、构建工具链或自动生成索引的脚本。

## 2. 查找与调用流程

1. **先查索引**：接到任务后，优先阅读 [INDEX.md](INDEX.md) 了解现有 Prompt、Skill 和模板，不要盲目全仓扫描。
2. **按需加载**：
   - 使用 Prompt 时，读取 `prompts/` 下对应的 Markdown 文件并按其中的输入要求与输出规范执行。
   - 使用 Skill 时，读取 `.agents/skills/<skill-name>/SKILL.md` 及其引用的 `assets/` 文件，严格按其工作流执行。
3. **项目组装**：当用户提出明确新项目需求时，结合 [.agents/skills/project-bootstrap/SKILL.md](.agents/skills/project-bootstrap/SKILL.md) 与 [prompts/codex/assemble-project.md](prompts/codex/assemble-project.md) 在目标目录完成组装。
4. **跨线程交接**：当任务需要切换到新线程继续时，按 [prompts/codex/cross-thread-handoff.md](prompts/codex/cross-thread-handoff.md) 生成交接摘要。

## 3. 仓库维护规范

- **新增 Prompt**：
  - 按用途放入 `prompts/writing/`、`prompts/engineering/`、`prompts/codex/`（或经确认的新增子目录）。
  - 文件名使用小写 kebab-case（例如 `review-embedded-code.md`）。
  - 结构参照 [templates/prompt-template.md](templates/prompt-template.md)。
- **新增 Skill**：
  - 按独立能力放入 `.agents/skills/<skill-name>/SKILL.md`，目录名使用小写 kebab-case 且与 frontmatter 中的 `name` 一致。
  - 结构参照 [templates/skill-template/SKILL.md](templates/skill-template/SKILL.md)。
- **暂存草稿**：未定稿的想法或片段放入 `inbox/`，避免污染正式目录。
- **同步索引**：每次新增、重命名、移动或删除正式 Prompt/Skill/模板后，必须**手动更新** [INDEX.md](INDEX.md)，保持索引与实际文件一一对应。

## 4. 修改前后的验证清单

- 确认所有新增或修改的文件均为 UTF-8 纯文本且符合目标目录规范。
- 确认每个 `SKILL.md` 包含合法的 YAML frontmatter（至少含 `name` 和 `description`）。
- 确认 [INDEX.md](INDEX.md)、[README.md](README.md) 与 `AGENTS.md` 中的相对链接均指向真实存在的文件。
