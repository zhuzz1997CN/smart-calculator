# 🧮 智能计算器

一个功能丰富的在线计算器，支持基础运算、科学计算和房贷计算。

## 🌐 在线访问

**🔗 https://zhuzz1997cn.github.io/smart-calculator/**

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/zhuzz1997CN/smart-calculator)

## ✨ 功能特性

- 🧮 **基础计算器**：四则运算、小数点、连续计算、清除、退格
- 🔬 **科学计算器**：三角函数、对数、指数、数学常数（π, e）、角度/弧度切换
- 🏠 **房贷计算器**：等额本息/等额本金、商业/公积金/组合贷款
- ⌨️ **键盘支持**：完整的快捷键系统（数字、运算符、Enter、Backspace、Esc）
- 📱 **响应式设计**：完美适配桌面、平板、手机

## 🎨 技术栈

- HTML5 + CSS3 + 原生 JavaScript (ES6+)
- 无外部依赖（零依赖！）
- 单文件应用（789 行代码）
- 现代简约 UI（紫色渐变主题）
- 模块化架构（state、ui、calculator 三层分离）

## 🚀 快速部署

### GitHub Pages（已部署）

本项目已部署到 GitHub Pages，访问：https://zhuzz1997cn.github.io/smart-calculator/

### Vercel（一键部署）

点击上方的 "Deploy with Vercel" 按钮，30秒内完成部署！

## 💻 本地运行

直接在浏览器中打开 `index.html` 即可，无需任何依赖或构建步骤。

或使用本地服务器：

```bash
python3 -m http.server 8000
# 访问 http://localhost:8000
```

## 📂 项目结构

```
smart-calculator/
├── index.html              # 主文件（包含所有功能）
├── README.md               # 项目说明
├── vercel.json             # Vercel 配置
├── .github/
│   └── workflows/
│       └── deploy.yml      # GitHub Pages 自动部署
└── DEPLOY.md               # 部署指南
```

## 📖 使用指南

### 基础计算器
- 点击数字和运算符按钮进行计算
- 支持连续计算（如：`2 + 3 + 4 = 9`）
- 键盘快捷键：数字、`+`、`-`、`*`、`/`、`Enter`、`Backspace`、`Esc`

### 科学计算器
- 切换到"科学"标签
- 支持三角函数、对数、指数等高级运算
- 键盘快捷键：`s`=sin, `c`=cos, `t`=tan, `p`=π, `e`=e
- 点击 `deg`/`rad` 切换角度/弧度模式

### 房贷计算器
- 切换到"房贷"标签
- 输入贷款金额、利率、年限
- 选择还款方式（等额本息/等额本金）
- 点击"计算"查看月供、总利息、总还款

## 🔗 链接

- 🌐 **在线访问：** https://zhuzz1997cn.github.io/smart-calculator/
- 📦 **GitHub：** https://github.com/zhuzz1997CN/smart-calculator
- 📝 **部署指南：** [DEPLOY.md](DEPLOY.md)

## 👨‍💻 作者

**zhanzhanzhu**

## 📄 许可

MIT License

---

⭐ 如果觉得有用，欢迎 Star！
