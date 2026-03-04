# 🚀 Vercel 一键部署

## 最简单的方式：点击按钮部署

由于 Vercel CLI 需要交互式登录，我为你准备了更简单的方案：

---

## 方案 A：Deploy Button（推荐，30秒完成）

### 步骤：

1. **点击下面的按钮：**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/zhuzz1997CN/smart-calculator)

或者访问这个链接：
```
https://vercel.com/new/clone?repository-url=https://github.com/zhuzz1997CN/smart-calculator
```

2. **登录 Vercel**
   - 选择 "Continue with GitHub"
   - 授权 Vercel 访问你的 GitHub

3. **配置项目**
   - Repository Name: `smart-calculator` (默认)
   - Private: 取消勾选（保持公开）
   - 直接点击 "Deploy"

4. **等待 30-60 秒**

5. **完成！** 获得 URL：`https://smart-calculator-xxx.vercel.app`

---

## 方案 B：从 Vercel Dashboard 导入（2分钟）

如果上面的按钮不工作，手动操作：

1. **访问：** https://vercel.com/new

2. **Import Git Repository**
   - 点击 "Import Git Repository"
   - 粘贴仓库 URL：`https://github.com/zhuzz1997CN/smart-calculator`
   - 或者从列表中选择 `smart-calculator`

3. **配置（保持默认）**
   - Project Name: `smart-calculator`
   - Framework Preset: `Other`
   - Root Directory: `./`
   - Build Command: (留空)
   - Output Directory: `./`

4. **点击 Deploy**

5. **等待部署完成**

---

## 方案 C：使用 Vercel CLI（需要你的 Token）

如果你有 Vercel Access Token，我可以直接部署：

1. 访问 https://vercel.com/account/tokens
2. 创建新 Token
3. 把 Token 给我

然后我可以执行：
```bash
vercel --token YOUR_TOKEN --prod
```

---

## 🎯 推荐操作

**最快速度：** 直接访问这个链接，点击 Deploy：

```
https://vercel.com/new/clone?repository-url=https://github.com/zhuzz1997CN/smart-calculator
```

**预计时间：** 30 秒 - 1 分钟

---

部署成功后，把 Vercel URL 告诉我，我会：
- ✅ 更新 README.md
- ✅ 推送到 GitHub
- ✅ 生成完整项目报告
