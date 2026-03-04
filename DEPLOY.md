# 智能计算器 - 部署指南

## ✅ 项目已完成！

**项目位置：** `/root/clawd/calculator/`

**包含文件：**
- `index.html` - 完整的单页面应用
- `README.md` - 项目说明
- `.gitignore` - Git 忽略配置

---

## 🚀 部署到 Vercel（推荐）

### 方法 1：通过 GitHub 部署

**步骤：**

1. **创建 GitHub 仓库**
   - 访问 https://github.com/new
   - 仓库名：`calculator`
   - 设置为 Public
   - 点击 "Create repository"

2. **推送代码到 GitHub**
   ```bash
   cd /root/clawd/calculator
   git branch -M main
   git push -u origin main
   ```

3. **连接 Vercel**
   - 访问 https://vercel.com
   - 点击 "New Project"
   - 选择刚创建的 GitHub 仓库 `calculator`
   - 配置：
     - Framework Preset: **Other**
     - Root Directory: `./`
     - Build Command: (留空)
     - Output Directory: `./`
   - 点击 "Deploy"

4. **获取部署 URL**
   - 部署完成后会得到类似：`https://calculator-xxx.vercel.app`
   - 复制这个 URL 并更新 README.md

---

### 方法 2：通过工蜂 + Vercel

如果你想使用工蜂仓库：

```bash
cd /root/clawd/calculator
git remote add origin https://git.woa.com/zhanzhanzhu/calculator.git
git push -u origin master
```

然后在 Vercel 导入工蜂仓库（需要先在 Vercel 中添加工蜂 Git 集成）。

---

## 🖥️ 本地预览

直接在浏览器中打开：

```bash
# 方式1：文件路径
file:///root/clawd/calculator/index.html

# 方式2：使用 Python 简易服务器
cd /root/clawd/calculator
python3 -m http.server 8000
# 然后访问 http://localhost:8000
```

---

## 📱 功能测试清单

### 基础计算器
- [x] 加法：`2 + 3 = 5`
- [x] 减法：`10 - 4 = 6`
- [x] 乘法：`5 × 3 = 15`
- [x] 除法：`8 ÷ 2 = 4`
- [x] 除零：`5 ÷ 0` → 显示错误
- [x] 小数：`1.5 + 2.3 = 3.8`
- [x] 连续运算：`2 + 3 + 4 = 9`
- [x] 清除 (C)
- [x] 退格 (←)

### 科学计算器
- [x] `sin(30°) = 0.5`
- [x] `cos(0°) = 1`
- [x] `tan(45°) = 1`
- [x] `log(100) = 2`
- [x] `ln(e) = 1`
- [x] `√16 = 4`
- [x] `2² = 4`
- [x] `π ≈ 3.14159`
- [x] deg/rad 切换

### 房贷计算器
- [x] 等额本息
- [x] 等额本金
- [x] 商业贷款
- [x] 公积金贷款
- [x] 组合贷款

### 键盘支持
- [x] 数字键 0-9
- [x] 运算符 + - * /
- [x] Enter（=）
- [x] Backspace（←）
- [x] Escape（C）
- [x] 科学模式快捷键（s, t, p, e）

---

## 🎨 特性亮点

- ✨ **现代 UI**：紫色渐变主题，流畅动画
- 📱 **响应式**：支持桌面、平板、手机
- ⌨️ **键盘友好**：完整的快捷键支持
- 🚀 **零依赖**：纯原生 JavaScript，无需构建
- 🌐 **国际化**：中文界面，友好易用

---

## 📦 部署后操作

部署成功后，记得：

1. 更新 `README.md` 中的部署链接
2. 测试在线版本所有功能
3. 分享给朋友使用 🎉

---

**作者：** zhanzhanzhu  
**日期：** 2026-03-04
