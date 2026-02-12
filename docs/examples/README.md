# 示例与最佳实践

## Git 技能示例

### 生成规范化提交信息（git-committer）
- 触发语句：如“帮我生成本次变更的提交信息”
- 步骤：分析变更 → 拆分提交 → 展示 commit message → 等待确认

### 拉取最新代码（pull-latest-code）
- 触发语句：如“拉取当前分支最新代码”
- 步骤：stash 未提交 → `git pull --rebase` → 恢复更改

### 合并代码到 dev（merge-code）
- 触发语句：如“把 feature/x 合并到 dev 并发布”
- 步骤：拉取 → 切分支 → 合并 → 更新版本与 CHANGELOG → 提交 → 推送

### 推送代码（push-code）
- 触发语句：如“推送到远程进行代码评审”
- 步骤：检查状态 → 拉取最新 → 推送到 `refs/for/<branch>`
