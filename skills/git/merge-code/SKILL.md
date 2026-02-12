---
name: "merge-code"
description: "自动化合并代码流程，包括拉取最新代码、切换分支、合并代码、修改commit message、更新版本号和上传代码。当需要将代码合并到dev分支并发布新版本时调用。"
---

# Merge Code Skill

## 功能说明

此skill用于自动化执行代码合并流程，将指定分支的代码合并到dev分支，并完成版本更新和代码上传。

## 执行流程

1. **拉取当前分支最新代码**
   - **调用 pull-latest-code skill 拉取当前分支的最新代码**

2. **切换到dev分支并拉取最新代码**
   - 执行 `git checkout dev` 切换到dev分支
   - **调用 pull-latest-code skill 拉取dev分支的最新代码**

3. **合并代码**
   - 执行 `git merge --no-ff origin/xxx` 合并代码

4. **修改commit message**
   - 合并成功会弹出commit message编辑框
   - 将默认的 "Merge xxxxxx" 修改为 "[update]: merge xxxxxx"

5. **更新版本号**
   - 修改 `package.json` 文件，将版本号最后一位+1
   - 例如：从 "1.0.0" 更新为 "1.0.1"

6. **更新CHANGELOG.md**
   - 在CHANGELOG.md文件最上方添加新版本的变更记录
   - 格式参考之前的记录，需要包含：
     - 版本号
     - 迭代名称
     - 文档链接

7. **提交版本更新**
   - 提交 `package.json` 和 `CHANGELOG.md` 的修改
   - **调用 git-committer skill 生成并提交 commit message**

8. **上传代码**
   - **调用 push-code skill 推送代码到远程仓库**

## 使用场景

- 当需要将功能分支的代码合并到dev分支时
- 当需要发布新版本并更新版本号时
- 当需要标准化代码合并流程时

## 注意事项

- 确保当前分支有未合并的代码需要合并到dev分支
- 部分项目可能使用不同的开发分支名称(如develop)，请根据实际情况调整
- 更新CHANGELOG.md时需要用户提供迭代名称和文档链接
