# GitHub Pages 快速部署指南

## 📋 前置要求

- GitHub账号（如果没有，请先注册：https://github.com/）
- 可选：Git命令行工具（如果使用命令行方式）

## 🚀 快速部署步骤

### 步骤 1: 创建GitHub仓库

1. 登录 [GitHub](https://github.com/)
2. 点击右上角的 **"+"** 按钮，选择 **"New repository"**
3. 填写仓库信息：
   - **Repository name**: 输入仓库名称（例如：`my-blog` 或 `personal-website`）
   - **Description**: 可选，填写描述
   - **Visibility**: 选择 **Public**（公开）或 **Private**（私有）
   - ⚠️ **不要**勾选 "Add a README file"
   - ⚠️ **不要**添加 .gitignore 或 license
4. 点击 **"Create repository"**

### 步骤 2: 上传文件

#### 方式A：网页上传（最简单）

1. 在新建的仓库页面，点击 **"uploading an existing file"** 链接
2. 将以下文件拖拽到上传区域：
   ```
   ✅ index.html
   ✅ styles.css
   ✅ script.js
   ✅ README.md
   ✅ .gitignore（可选）
   ```
3. 在页面底部：
   - **Commit message**: 输入 `Initial commit` 或 `添加博客网页`
   - 点击 **"Commit changes"** 按钮

#### 方式B：Git命令行（推荐，适合开发者）

打开终端/命令行，在项目目录下执行：

```bash
# 1. 初始化Git仓库
git init

# 2. 添加文件
git add index.html styles.css script.js README.md .gitignore

# 3. 提交
git commit -m "Initial commit: 个人博客网页"

# 4. 添加远程仓库（替换 YOUR_USERNAME 和 REPO_NAME）
git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git

# 5. 推送到GitHub
git branch -M main
git push -u origin main
```

### 步骤 3: 启用GitHub Pages

1. 在仓库页面，点击顶部的 **"Settings"**（设置）标签
2. 在左侧菜单中找到并点击 **"Pages"**
3. 在 **"Source"** 部分：
   - **Branch**: 选择 `main`（或 `master`，取决于你的默认分支）
   - **Folder**: 选择 `/ (root)`
4. 点击 **"Save"** 按钮
5. 等待几秒钟，页面会显示你的网站地址

### 步骤 4: 访问你的网站

- GitHub会显示你的网站URL，格式为：
  ```
  https://YOUR_USERNAME.github.io/REPO_NAME
  ```
- 例如：`https://zhangsan.github.io/my-blog`
- ⏰ 首次部署可能需要等待 **1-5分钟** 才能访问

## 🔄 更新网站内容

### 使用网页界面更新

1. 在GitHub仓库页面，点击要修改的文件（如 `index.html`）
2. 点击右上角的 **✏️ Edit**（编辑）按钮
3. 修改内容后，滚动到底部
4. 填写提交信息，点击 **"Commit changes"**
5. 等待1-2分钟，刷新网站即可看到更新

### 使用Git命令行更新

```bash
# 修改文件后
git add .
git commit -m "更新内容描述"
git push
```

## 🌐 使用自定义域名（可选）

如果你想使用自己的域名（如 `blog.example.com`）：

1. 在仓库根目录创建 `CNAME` 文件
2. 文件内容只写你的域名，例如：
   ```
   blog.example.com
   ```
3. 提交并推送到GitHub
4. 在你的域名DNS提供商处添加CNAME记录：
   - **类型**: CNAME
   - **主机记录**: blog（或你想要的子域名）
   - **记录值**: `YOUR_USERNAME.github.io`
5. 等待DNS生效（通常几分钟到几小时）

## ❓ 常见问题

### Q: 网站显示404错误
**A:** 
- 检查仓库名称是否正确
- 确认已启用GitHub Pages（Settings > Pages）
- 确认 `index.html` 在仓库根目录
- 等待几分钟后重试

### Q: 样式或脚本不工作
**A:**
- 检查文件路径是否正确（使用相对路径）
- 确认所有文件都已上传到GitHub
- 清除浏览器缓存后重试

### Q: 更新后看不到变化
**A:**
- 等待1-2分钟让GitHub重新部署
- 强制刷新浏览器（Ctrl+F5 或 Cmd+Shift+R）
- 检查文件是否已成功提交

### Q: 如何删除部署的网站
**A:**
- 进入 Settings > Pages
- 将 Source 改为 "None"
- 点击 Save

## 📝 注意事项

- ⚠️ 如果仓库是 **Private**（私有），GitHub Pages 需要付费账户才能使用
- ✅ **Public**（公开）仓库可以免费使用GitHub Pages
- 📁 确保 `index.html` 在仓库根目录
- 🔒 不要上传敏感信息（密码、API密钥等）

## 🎉 完成！

部署成功后，你的个人博客就可以通过GitHub Pages访问了！

---

**需要帮助？** 查看 [GitHub Pages 官方文档](https://docs.github.com/en/pages)
