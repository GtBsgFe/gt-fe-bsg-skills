# 贡献指南

## 如何编写新的技能

1. 在对应类别目录（如 `skills/git/`）下创建技能目录，例如 `skills/git/my-skill/`
2. 在技能目录内创建 `SKILL.md`，按 [技能规范](./SKILL_SPEC.md) 填写
3. 更新 `skills/.meta/index.json`，添加技能索引条目
4. 如有版本变更，更新 `skills/.meta/version.json`

## 提交规范

- 保持目录结构与命名一致，使用短横线命名（kebab-case）
- 在 `SKILL.md` 顶部使用 YAML Front Matter 提供 `name` 与 `description`
- 提交前确保文档完整且能被工具正确发现

## PR 要求

- 描述新增或变更的技能及其用途
- 附带简单使用示例或链接到 `docs/examples`
- 若影响索引或版本，请同步更新对应文件
