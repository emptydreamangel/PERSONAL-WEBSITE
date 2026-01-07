# 个人介绍博客网页

一个现代化、响应式的个人介绍博客网页，支持多种部署方式。

## 功能特点

- ✨ 现代化的UI设计
- 📱 完全响应式，支持移动端
- 🎨 渐变色彩和动画效果
- 🚀 快速加载，纯静态页面
- 📄 包含：首页、关于我、技能、项目、联系方式等模块

## 文件结构

```
voice-trial/
├── index.html      # 主页面
├── styles.css      # 样式文件
├── script.js       # 交互脚本
└── README.md       # 说明文档
```

## 本地运行

直接在浏览器中打开 `index.html` 文件即可查看效果。

或者使用Python内置服务器：

```bash
# Python 3
python -m http.server 8000

# 然后在浏览器访问 http://localhost:8000
```

## 部署方式

### 1. GitHub Pages（推荐，免费）

#### 方法一：通过GitHub网页界面部署

1. **创建GitHub仓库**
   - 访问 [GitHub](https://github.com/) 并登录
   - 点击右上角 "+" 号，选择 "New repository"
   - 输入仓库名称（例如：`my-blog`）
   - 选择 Public（公开）或 Private（私有）
   - **不要**勾选 "Initialize this repository with a README"
   - 点击 "Create repository"

2. **上传文件到GitHub**
   - 在仓库页面，点击 "uploading an existing file"
   - 将以下文件拖拽上传：
     - `index.html`
     - `styles.css`
     - `script.js`
     - `README.md`
   - 在页面底部填写提交信息（例如："Initial commit"）
   - 点击 "Commit changes"

3. **启用GitHub Pages**
   - 进入仓库 Settings（设置）
   - 在左侧菜单找到 "Pages"
   - 在 "Source" 部分：
     - 选择 Branch: `main`（或 `master`）
     - 选择 Folder: `/ (root)`
   - 点击 "Save"
   - 等待1-2分钟，GitHub会显示你的网站地址

4. **访问你的网站**
   - 地址格式：`https://你的用户名.github.io/仓库名`
   - 例如：`https://username.github.io/my-blog`

#### 方法二：通过Git命令行部署（推荐）

如果你已经安装了Git，可以使用命令行：

```bash
# 1. 初始化Git仓库
git init

# 2. 添加所有文件（除了.gitignore中的文件）
git add index.html styles.css script.js README.md .gitignore

# 3. 提交文件
git commit -m "Initial commit: 个人博客网页"

# 4. 在GitHub上创建仓库后，添加远程仓库
# 将 YOUR_USERNAME 和 REPO_NAME 替换为你的实际信息
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 5. 推送到GitHub
git branch -M main
git push -u origin main
```

然后按照方法一的第3步启用GitHub Pages。

#### 使用自定义域名（可选）

如果你想使用自己的域名：

1. 在仓库根目录创建 `CNAME` 文件
2. 在文件中写入你的域名（例如：`blog.example.com`）
3. 在你的域名DNS设置中添加CNAME记录，指向 `你的用户名.github.io`
4. 在GitHub Pages设置中会自动识别CNAME文件

#### 更新网站内容

每次修改文件后，只需：

```bash
git add .
git commit -m "更新内容"
git push
```

GitHub Pages会自动重新部署，通常1-2分钟内生效。

#### 常见问题

- **网站显示404**: 检查仓库名称是否正确，确保已启用Pages功能
- **样式不显示**: 确保所有CSS/JS文件路径正确，使用相对路径
- **更新不生效**: 等待几分钟，清除浏览器缓存后重试

### 2. Netlify（推荐，免费）

1. 访问 [Netlify](https://www.netlify.com/)
2. 注册/登录账号
3. 点击 "Add new site" > "Deploy manually"
4. 拖拽项目文件夹到部署区域
5. 自动部署完成

### 3. Vercel（推荐，免费）

1. 访问 [Vercel](https://vercel.com/)
2. 注册/登录账号
3. 点击 "New Project"
4. 导入GitHub仓库或直接上传项目
5. 一键部署

### 4. 其他静态托管服务

- **Cloudflare Pages**: [cloudflare.com](https://pages.cloudflare.com/)
- **Surge.sh**: `surge` 命令行工具
- **Firebase Hosting**: Google Firebase
- **AWS S3 + CloudFront**: 适合有AWS账号的用户

## 自定义内容

### 修改个人信息

编辑 `index.html` 文件，找到以下部分进行修改：

- **姓名和标题**: 在 `<h1>` 标签中修改
- **关于我**: 在 `#about` 部分修改文本内容
- **技能标签**: 在 `#skills` 部分修改技能标签
- **项目信息**: 在 `#projects` 部分修改项目卡片
- **联系方式**: 在 `#contact` 部分修改邮箱和社交媒体链接

### 修改颜色主题

编辑 `styles.css` 文件中的 `:root` 变量：

```css
:root {
    --primary-color: #6366f1;      /* 主色调 */
    --secondary-color: #8b5cf6;    /* 辅助色 */
    /* ... 其他颜色变量 */
}
```

### 添加头像

将头像图片放到项目根目录，然后在 `index.html` 中找到：

```html
<div class="avatar-placeholder">
    <!-- 替换为 <img src="your-avatar.jpg" alt="Avatar"> -->
</div>
```

## 浏览器支持

- Chrome (最新版)
- Firefox (最新版)
- Safari (最新版)
- Edge (最新版)
- 移动端浏览器

## 技术栈

- HTML5
- CSS3 (Grid, Flexbox, 渐变, 动画)
- JavaScript (ES6+)
- 无依赖框架，纯原生实现

## 许可证

MIT License - 可自由使用和修改

## 贡献

欢迎提交Issue和Pull Request！

---

祝你部署顺利！🎉
