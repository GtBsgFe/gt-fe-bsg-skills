# gt-fe-bsg-skills

统一的团队技能库（Skills Registry）。本仓库提供标准化的目录结构、元数据与文档，便于发现、安装、管理与复用技能。

## 目录结构

- docs/：文档中心，包含总览、贡献指南、技能规范与示例
- skills/：技能库核心目录
  - .meta/：技能索引与版本信息
  - git/：git 相关技能
  - requirements/：需求相关技能（预留）
- .gitignore：Git 忽略规则
- package.json：项目依赖与脚本

## 快速导航

 - 文档中心：[docs/README](docs/README.md)
 - 技能索引：[skills/.meta/index.json](skills/.meta/index.json)
 - 版本信息：[skills/.meta/version.json](skills/.meta/version.json)

## 使用说明

- 通过内部工具（如 skills-cli）读取 `.meta/index.json` 达到发现与安装
- 新增技能前请阅读贡献指南与技能规范

## 许可证

内部使用
