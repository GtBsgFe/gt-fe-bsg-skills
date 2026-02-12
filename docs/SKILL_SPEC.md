# 技能编写规范（SKILL_SPEC）

## 命名规范

- 使用英文短横线（kebab-case）命名技能目录，例如：`git-committer`
- `name` 字段与目录名保持一致

## 目录与文件

- 每个技能目录必须包含 `SKILL.md`
- `SKILL.md` 顶部使用 YAML Front Matter：
  ```
  ---
  name: "skill-name"
  description: "一句话用途说明"
  ---
  ```

## 元数据

- 必填字段：`name`、`description`
- 可选扩展：`tags`、`category`、`version`
- 技能索引在 `skills/.meta/index.json` 维护，字段示例：
  ```json
  {
    "id": "git-committer",
    "name": "git-committer",
    "category": "git",
    "path": "skills/git/git-committer/SKILL.md",
    "version": "1.0.0",
    "description": "分析变更生成 commit message"
  }
  ```

## 文档要求

- 至少包含：用途、何时使用、执行流程/使用方法、注意事项、示例
- 中文编写，术语保持统一

## 质量要求

- 操作步骤清晰、可复用
- 避免含糊其辞或缺少关键前置条件
- 变更需同步更新索引与版本文件
