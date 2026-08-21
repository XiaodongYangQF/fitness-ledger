# Fitness Ledger — GitHub Pages 部署

这个文件夹已经可以直接作为一个 GitHub repository 使用。

## 你只需要完成一次的步骤

### 方法 A：终端（推荐）

在 Mac Terminal 中运行：

```bash
cd ~/Downloads/fitness-ledger-github-pages

git init
git branch -M main
git add .
git commit -m "Deploy Fitness Ledger PWA"

gh repo create fitness-ledger --private --source=. --remote=origin --push
```

如果你没有安装 GitHub CLI (`gh`)，可以用：

```bash
brew install gh
gh auth login
```

登录后再运行 `gh repo create ...`。

然后：

1. 打开 GitHub 上刚创建的 `fitness-ledger` repository
2. Settings → Pages
3. Source 选择 **GitHub Actions**
4. 等待 Actions 完成部署
5. GitHub Pages 地址通常是：
   `https://<你的GitHub用户名>.github.io/fitness-ledger/`

## iPhone

Safari 打开上述网址 → 分享 → 添加到主屏幕。

以后主屏幕会显示 `Fitness Ledger`，可以像 App 一样使用。

## 数据

当前版本使用浏览器 localStorage。
iPhone 和 Mac 不自动同步；建议每周导出一次 JSON 备份。
