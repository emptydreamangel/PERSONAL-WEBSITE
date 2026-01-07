# Personal Website

一个现代化、响应式的个人介绍博客网页，展示我的技能、项目和经历。

🌐 **在线访问**: [https://emptydreamangel.github.io/PERSONAL-WEBSITE](https://emptydreamangel.github.io/PERSONAL-WEBSITE)

## ✨ 功能特点

- 🎨 现代化的UI设计，渐变色彩和流畅动画
- 📱 完全响应式，完美适配桌面、平板和移动设备
- ⚡ 快速加载，纯静态页面，无需后端服务
- 🎯 包含完整的个人展示模块：首页、关于我、技能、项目、联系方式
- 🔍 SEO友好，语义化HTML结构
- ♿ 无障碍设计，良好的可访问性

## 📁 项目结构

```
PERSONAL-WEBSITE/
├── index.html      # 主页面
├── styles.css      # 样式文件
├── script.js       # 交互脚本
├── README.md       # 项目说明
├── DEPLOY.md       # 部署指南
├── .gitignore      # Git忽略文件
└── deploy.ps1      # PowerShell部署脚本
```

## 🚀 快速开始

### 本地运行

**方式一：直接打开**
直接在浏览器中打开 `index.html` 文件即可查看效果。

**方式二：使用本地服务器**

```bash
# Python 3
python -m http.server 8000

# 然后在浏览器访问 http://localhost:8000
```

或者使用Node.js：

```bash
# 使用 npx serve
npx serve

# 或使用 http-server
npx http-server -p 8000
```

## 📦 部署

本项目已部署在 GitHub Pages 上。

**仓库地址**: [https://github.com/emptydreamangel/PERSONAL-WEBSITE](https://github.com/emptydreamangel/PERSONAL-WEBSITE)  
**网站地址**: [https://emptydreamangel.github.io/PERSONAL-WEBSITE](https://emptydreamangel.github.io/PERSONAL-WEBSITE)

### 更新内容

每次修改后，推送到GitHub即可自动更新：

```bash
git add .
git commit -m "更新内容描述"
git push origin main
```

GitHub Pages会自动重新部署，通常1-2分钟内生效。

### 部署到其他平台

详细的部署指南请查看 [DEPLOY.md](./DEPLOY.md) 文件，包含：
- GitHub Pages 详细步骤
- Netlify 部署
- Vercel 部署
- 其他静态托管服务

### 使用自定义域名（可选）

如果你想使用自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 在文件中写入你的域名（例如：`blog.example.com`）
3. 在你的域名DNS设置中添加CNAME记录，指向 `emptydreamangel.github.io`
4. 在GitHub Pages设置中会自动识别CNAME文件

### 常见问题

- **网站显示404**: 检查仓库名称是否正确，确保已启用Pages功能
- **样式不显示**: 确保所有CSS/JS文件路径正确，使用相对路径
- **更新不生效**: 等待几分钟，清除浏览器缓存后重试


## 🎨 自定义内容

### 修改个人信息

编辑 `index.html` 文件，找到以下部分进行修改：

- **姓名和标题**: 在 `<h1 class="hero-title">` 标签中修改（第47行）
- **关于我**: 在 `#about` 部分的 `<p>` 标签中修改文本内容
- **技能标签**: 在 `#skills` 部分的 `<span class="skill-tag">` 中修改技能标签
- **项目信息**: 在 `#projects` 部分的 `.project-card` 中修改项目卡片
- **联系方式**: 在 `#contact` 部分修改邮箱和社交媒体链接

### 修改颜色主题

编辑 `styles.css` 文件中的 `:root` 变量（第6-15行）：

```css
:root {
    --primary-color: #6366f1;      /* 主色调 */
    --secondary-color: #8b5cf6;    /* 辅助色 */
    --text-primary: #1e293b;       /* 主文本颜色 */
    --text-secondary: #64748b;     /* 次要文本颜色 */
    /* ... 其他颜色变量 */
}
```

### 添加头像

将头像图片放到项目根目录，然后在 `index.html` 中找到（第38-44行）：

```html
<div class="avatar-placeholder">
    <!-- 替换为 -->
    <img src="your-avatar.jpg" alt="Avatar" style="width: 100%; height: 100%; object-fit: cover; border-radius: 50%;">
</div>
```

## 🌐 浏览器支持

- ✅ Chrome (最新版)
- ✅ Firefox (最新版)
- ✅ Safari (最新版)
- ✅ Edge (最新版)
- ✅ 移动端浏览器（iOS Safari, Chrome Mobile等）

## 🛠️ 技术栈

- **HTML5** - 语义化标记
- **CSS3** - Grid布局、Flexbox、CSS变量、渐变、动画
- **JavaScript (ES6+)** - 原生JS，无框架依赖
- **Git & GitHub** - 版本控制和部署
- **GitHub Pages** - 静态网站托管

## 📝 开发说明

本项目采用纯原生技术栈，无任何框架依赖，确保：
- ⚡ 极快的加载速度
- 📦 极小的文件体积
- 🔧 易于维护和修改
- 🎯 完全可控的代码

## 📄 许可证

MIT License - 可自由使用和修改

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

如果你觉得这个项目对你有帮助，欢迎：
- ⭐ Star 这个仓库
- 🐛 提交 Bug 报告
- 💡 提出功能建议
- 📖 改进文档

---

**感谢访问！** 🎉
