# Prompt & Skills Repository

用于长期积累个人 Prompt 和可复用 Skill 的纯文本资料库。Prompt 按用途组织，Skill 按独立能力组织，兼顾人工查阅与 Codex 查找、调用和维护。

## 定位与原则

- **纯文本优先**：默认使用 Markdown（`.md`），配套模板与资源使用必要的纯文本格式，不引入数据库、网站、构建框架或自动生成索引脚本。
- **资料库与业务项目分离**：本仓库只用于沉淀、维护和复用资产。只有在收到明确的新项目需求并指定目标目录时，才从本仓库选取相关 Prompt、Skill 与模板，在目标目录中组装项目。
- **人工与 Codex 共用**：顶层提供 `AGENTS.md`（给 Codex 的操作规范）和 `INDEX.md`（手动维护的资产总表），保证查找路径短、结构稳定。

## 目录结构

```text
<REPO>/
├── README.md                                  # 仓库定位、结构与维护说明
├── AGENTS.md                                  # Codex 查找、调用与维护指南
├── INDEX.md                                   # 手动维护的 Prompt / Skill / 模板总索引
├── .gitignore                                 # 基础忽略规则
├── prompts/                                   # 按用途组织的 Prompt
│   ├── writing/
│   │   └── technical-report.md                # 技术报告撰写
│   ├── engineering/
│   │   ├── review-embedded-code.md            # 嵌入式代码审查
│   │   └── analyze-capture-data.md            # 采集/抓包数据分析
│   └── codex/
│       ├── assemble-project.md                # 按需在目标目录组装新项目
│       └── cross-thread-handoff.md            # 跨线程任务交接
├── .agents/
│   └── skills/                                # 按独立能力组织的可复用 Skill
│       └── project-bootstrap/
│           ├── SKILL.md                       # 项目启动组装 Skill
│           └── assets/
│               └── project-brief.md           # 项目简报模板
├── templates/                                 # 新增资产时使用的标准模板
│   ├── prompt-template.md                     # Prompt 模板
│   └── skill-template/
│       └── SKILL.md                           # Skill 模板
└── inbox/
    └── README.md                              # 未整理草稿暂存区说明
```

## 快速使用

1. **查找已有资产**：先查看 [INDEX.md](INDEX.md)，按分类定位需要的 Prompt 或 Skill。
2. **新增 Prompt**：复制 [templates/prompt-template.md](templates/prompt-template.md) 到 `prompts/<分类>/` 下，填写完成后手动更新 [INDEX.md](INDEX.md)。
3. **新增 Skill**：复制 [templates/skill-template/SKILL.md](templates/skill-template/SKILL.md) 到 `.agents/skills/<skill-name>/SKILL.md`（必要时附带 `assets/` 或 `references/`），完成后更新 [INDEX.md](INDEX.md)。
4. **临时记录想法**：尚未成型的片段先放入 [inbox/](inbox/README.md)，成熟后再归档。
5. **组装新项目**：向 Codex 提供明确的新项目需求和目标目录，配合 [prompts/codex/assemble-project.md](prompts/codex/assemble-project.md) 与 [.agents/skills/project-bootstrap/SKILL.md](.agents/skills/project-bootstrap/SKILL.md) 完成项目初始化。
