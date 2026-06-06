# uPic Fork 使用指南

## 📌 当前状态

✅ 已成功同步到 GitHub: https://github.com/graylogo/uPic

## 🔄 远程仓库配置

```bash
# 查看远程仓库
git remote -v

# 结果：
# origin    git@github.com:graylogo/uPic.git    # 你的 Fork
# upstream  git@github.com:gee1k/uPic.git        # 原作者仓库
```

## 📥 如何同步原作者的更新

当原作者有新版本发布时，执行以下命令：

```bash
# 1. 切换到 master 分支
git checkout master

# 2. 获取上游更新
git fetch upstream

# 3. 合并上游更新到本地
git merge upstream/master

# 4. 如果有冲突，解决冲突后：
git add .
git commit -m "merge: 合并上游更新"

# 5. 推送到你的 Fork
git push origin master
```

## 🔧 日常开发工作流程

### 方式一：基于 master 分支修改
```bash
# 1. 先同步上游最新代码
git checkout master
git fetch upstream
git merge upstream/master

# 2. 创建功能分支
git checkout -b feature/your-feature

# 3. 进行修改...
# ... 编辑代码 ...

# 4. 提交
git add .
git commit -m "feat: 添加新功能"

# 5. 推送
git push origin feature/your-feature

# 6. 在 GitHub 上创建 Pull Request（可选）
```

### 方式二：直接在 master 修改
```bash
# 1. 同步上游
git checkout master
git fetch upstream
git merge upstream/master

# 2. 直接修改
# ... 编辑代码 ...

# 3. 提交并推送
git add .
git commit -m "feat: 你的修改"
git push origin master
```

## 🔍 如何查看差异

```bash
# 查看你的 Fork 和原作者仓库的差异
git log upstream/master..origin/master --oneline

# 或者用 GitHub 比较
# 访问：https://github.com/graylogo/uPic/compare/upstream/master...master
```

## 📤 如何提交 Pull Request 给原作者

如果你想贡献代码给原作者：

```bash
# 1. 确保你的分支是基于最新的 upstream/master
git checkout master
git fetch upstream
git merge upstream/master

# 2. 创建功能分支
git checkout -b feature/your-awesome-feature

# 3. 修改并提交
git add .
git commit -m "feat: 添加awesome功能"

# 4. 推送到你的 Fork
git push origin feature/your-awesome-feature

# 5. 在 GitHub 上：
#    - 进入你的 Fork 仓库
#    - 点击 "Compare & pull request"
#    - 选择 base: master, compare: feature/your-awesome-feature
#    - 填写 PR 描述
#    - 点击 "Create pull request"
```

## 🔙 如何撤销修改

```bash
# 撤销工作区的修改
git checkout -- <file>

# 或者
git restore <file>

# 撤销已暂存的修改
git reset HEAD <file>

# 撤销最后一次提交（保留修改）
git reset --soft HEAD~1

# 撤销最后一次提交（不保留修改）
git reset --hard HEAD~1
```

## 📋 备份信息

- **修改备份位置**: ~/Desktop/upic-macOS-compatibility.patch
- **编译产物位置**: ./build/Build/Products/Release/uPic.app

## ⚠️ 重要提示

1. **保持 Fork 更新**: 定期从 upstream 合并更新，避免分支偏离太远
2. **先拉取再推送**: 推送前先确保本地代码是最新的
3. **查看日志**: 使用 `git log` 查看提交历史，了解项目发展
4. **分支命名**: 建议使用有意义的分支名，如 `feature/xxx`、`fix/xxx`

## 🆘 获取帮助

- 原作者仓库: https://github.com/gee1k/uPic
- 你的 Fork: https://github.com/graylogo/uPic
- 查看 Git 常用命令: https://git-scm.com/docs
