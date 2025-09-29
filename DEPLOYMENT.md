# 善治美系统部署指南

## 🚀 GitHub Pages 部署步骤（简化版）

### 方法一：使用部署脚本（推荐）

1. **运行部署脚本**
   ```bash
   ./deploy-simple.sh
   ```

2. **启用 GitHub Pages**
   - 访问: https://github.com/mx9702098-glitch/-/settings/pages
   - 在 "Source" 部分选择 "Deploy from a branch"
   - 选择 "gh-pages" 分支
   - 选择 "/ (root)" 文件夹
   - 点击 "Save"

3. **等待部署完成**
   - 几分钟后，您的网站将在以下地址可用：
   - `https://mx9702098-glitch.github.io/-/`

### 方法二：手动部署

1. **创建 gh-pages 分支**
   ```bash
   git checkout --orphan gh-pages
   git add .
   git commit -m "部署到 GitHub Pages"
   git push -f origin gh-pages
   git checkout main
   ```

2. **启用 GitHub Pages**
   - 访问仓库设置页面
   - 选择从 gh-pages 分支部署

### 2. 访问地址

- **主页面**: https://mx9702098-glitch.github.io/-/index.html
- **移动端版本**: https://mx9702098-glitch.github.io/-/shan-zhi-mei-mobile.html

### 3. 本地测试

如果您想在本地测试，可以运行：

```bash
# 启动本地服务器
python3 -m http.server 8080

# 或者使用项目提供的部署脚本
./deploy.sh
```

然后访问 http://localhost:8080

### 4. 故障排除

如果遇到部署问题：

1. **检查 GitHub Pages 设置**
   - 确保在仓库设置中启用了 Pages
   - 确保选择了 "GitHub Actions" 作为源

2. **查看 Actions 日志**
   - 在仓库页面点击 "Actions" 标签
   - 查看最新的工作流运行日志

3. **重新触发部署**
   - 推送新的提交到 main 分支
   - 或在 Actions 页面手动重新运行工作流

## 📱 功能特色

- ✅ 移动端优先的响应式设计
- ✅ 村两委和村民双角色界面
- ✅ 完整的六步数字化工作流程
- ✅ 智能数据预填和OCR识别模拟
- ✅ 任务看板和进度管理
- ✅ 现代化的用户界面设计

## 🔧 技术栈

- **前端**: HTML5 + CSS3 + JavaScript
- **样式**: 响应式设计，移动端优化
- **图标**: Font Awesome
- **部署**: GitHub Pages + GitHub Actions