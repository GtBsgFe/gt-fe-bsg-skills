# 文档中心

欢迎来到 gt-fe-bsg-skills 文档中心。本项目用于统一管理团队技能（skills），提供规范化的目录结构、元数据与使用示例，便于发现、安装与复用。

## 快速开始

1. 克隆仓库并打开项目根目录
2. 在 `skills/` 目录中浏览已提供的技能
3. 通过 `.meta/index.json` 发现技能索引并接入到内部工具（如 skills-cli）
4. 如需新增技能，请阅读 [CONTRIBUTING](./CONTRIBUTING.md) 与 [SKILL_SPEC](./SKILL_SPEC.md)

## 目录结构

```
gt-fe-bsg-skills/
├── docs/
│   ├── README.md
│   ├── CONTRIBUTING.md
│   ├── SKILL_SPEC.md
│   └── examples/
├── skills/
│   ├── .meta/
│   │   ├── index.json
│   │   └── version.json
│   ├── git/
│   │   ├── git-committer/
│   │   ├── merge-code/
│   │   ├── pull-latest-code/
│   │   └── push-code/
│   └── requirements/
├── .gitignore
├── package.json
└── README.md
```

## 约定

- 所有技能统一存放于 `skills/` 下的具体类别目录中
- 每个技能至少包含一份 `SKILL.md`，定义元数据与使用说明
- 元数据索引存放于 `skills/.meta/`，用于工具发现与版本管理
- 文档与示例统一维护在 `docs/` 下

## 相关链接
 
- 项目入口文档：[根目录 README](../README.md)
