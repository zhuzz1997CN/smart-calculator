# GitHub + Vercel 部署完整指南

## 前置准备

### 1. 创建 GitHub 账号（如果还没有）
- 访问 https://github.com/signup
- 填写邮箱、用户名、密码
- 完成验证

### 2. 创建仓库
- 访问 https://github.com/new
- 仓库名：`smart-calculator` 或 `calculator`
- 描述：智能计算器 - 支持基础、科学、房贷计算
- 设置为 **Public**（公开）
- **不要** 勾选 "Add a README file"
- 点击 "Create repository"

### 3. 生成 Personal Access Token
- 访问 https://github.com/settings/tokens
- 点击 "Generate new token (classic)"
- Note: `calculator-deploy`
- Expiration: `90 days`
- 勾选权限：
  - ✅ `repo` (完整的仓库访问权限)
- 点击 "Generate token"
- **重要：** 复制生成的 token（类似：`ghp_xxxxxxxxxxxxxxxxxxxx`）

---

## 第一步：推送代码到 GitHub

在你的终端或 SSH 会话中执行：

```bash
# 进入项目目录
cd /root/clawd/calculator

# 添加远程仓库（替换 YOUR_USERNAME 为你的 GitHub 用户名）
git remote add origin https://github.com/YOUR_USERNAME/calculator.git

# 重命名分支为 main
git branch -M main

# 推送代码（会要求输入用户名和密码）
# 用户名：你的 GitHub 用户名
# 密码：使用上面生成的 Personal Access Token（不是 GitHub 密码！）
git push -u origin main
```

**推送成功的标志：**
```
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (7/7), done.
Writing objects: 100% (8/8), 31.32 KiB | 5.22 MiB/s, done.
Total 8 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/YOUR_USERNAME/calculator.git
 * [new branch]      main -> main
```

---

## 第二步：部署到 Vercel

### 方式 A：通过 Vercel 网站（推荐）

1. **注册/登录 Vercel**
   - 访问 https://vercel.com/signup
   - 选择 "Continue with GitHub"
   - 授权 Vercel 访问你的 GitHub

2. **导入项目**
   - 登录后点击 "Add New..." → "Project"
   - 在列表中找到 `calculator` 仓库
   - 点击 "Import"

3. **配置项目（使用默认配置）**
   - Project Name: `calculator` （或自定义）
   - Framework Preset: **Other**
   - Root Directory: `./` （默认）
   - Build Command: （留空）
   - Output Directory: `./` （默认）
   - Install Command: （留空）

4. **部署**
   - 点击 "Deploy"
   - 等待 30-60 秒

5. **获取 URL**
   - 部署成功后会显示：
     ```
     🎉 Your project is ready!
     https://calculator-xxx.vercel.app
     ```
   - 点击链接访问你的在线计算器！

---

### 方式 B：通过 Vercel CLI（命令行）

如果你熟悉命令行，也可以使用 Vercel CLI：

```bash
# 安装 Vercel CLI
npm install -g vercel

# 登录 Vercel
vercel login

# 部署
cd /root/clawd/calculator
vercel --prod

# 按照提示操作：
# - Link to existing project? No
# - Project name? calculator
# - Deploy to production? Yes
```

---

## 第三步：更新 README

部署成功后，更新项目的 README.md：

```bash
cd /root/clawd/calculator

# 编辑 README.md，将部署链接替换为实际的 Vercel URL
nano README.md

# 提交更新
git add README.md
git commit -m "docs: 更新部署链接"
git push
```

在 README.md 中找到这一行：
```markdown
[部署链接]（待部署后填入）
```

替换为：
```markdown
🌐 **在线访问：** https://calculator-xxx.vercel.app
```

---

## 常见问题

### Q1: 推送时提示 "authentication failed"
**A:** 确保你使用的是 **Personal Access Token**，而不是 GitHub 密码。

### Q2: Vercel 部署失败
**A:** 检查：
- 仓库是否为 Public
- index.html 是否在仓库根目录
- Build Command 是否留空

### Q3: 访问 Vercel URL 显示 404
**A:** 等待 1-2 分钟，DNS 需要时间生效。

### Q4: 想要自定义域名
**A:** 在 Vercel 项目设置中 → Domains → 添加自己的域名

---

## 🎉 完成！

部署成功后，你将拥有：
- ✅ GitHub 仓库：`https://github.com/YOUR_USERNAME/calculator`
- ✅ 在线计算器：`https://calculator-xxx.vercel.app`
- ✅ 自动部署：每次 git push 后 Vercel 会自动重新部署

---

**需要帮助？** 如果遇到任何问题，把错误信息发给我。
