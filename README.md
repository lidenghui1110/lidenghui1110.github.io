# 🚀 Lidenghui's Digital Garden

这是基于 **Hugo** 搭建的个人博客，使用了 **PaperMod** 主题。

## 🛠 技术架构
- **静态网站生成器**: [Hugo (Extended)](https://gohugo.io/)
- **主题**: [PaperMod](https://github.com/adityatelange/hugo-PaperMod)
- **托管**: GitHub Pages
- **自动化部署**: GitHub Actions

---

## 📝 日常维护指南

### 1. 撰写新文章
使用以下命令创建新博文（文件将生成在 `content/posts/` 目录下）：
```bash
hugo new content posts/your-post-title.md
```

### 2. 本地预览
在发布前，运行本地服务器实时查看效果：
```bash
hugo server -D
```
- 访问地址: `http://localhost:1313`
- `-D` 参数表示包括草稿 (draft: true) 的文章。

### 3. 发布更新
将更改推送到 GitHub，系统会自动触发部署：
```bash
git add .
git commit -m "feat: 新增文章/修改配置"
git push
```
> **注意**: 部署进度可以在 GitHub 仓库的 `Actions` 标签页查看。

---

## ⚙️ 核心配置说明

- **基础配置**: 修改 `hugo.yaml` 可以更改站点标题、作者信息、社交链接等。
- **自定义样式**: 在 `layouts/partials/extend_footer.html` 中可以添加自定义的 JS 脚本（如已配置的 Mermaid 支持）。
- **图片管理**: 将图片存放在 `static/images/` 目录下，在 Markdown 中引用路径为 `/images/filename.jpg`。

---

## 🆘 常见问题 (FAQ)

- **文章没显示？**
  检查 Markdown 顶部的 `draft` 是否为 `false`。如果是 `true`，生产环境不会显示。
- **Mermaid 图表不渲染？**
  确保文章中使用的是 ```mermaid 代码块。系统已配置自动检测并加载渲染引擎。
- **想要修改首页头像？**
  在 `hugo.yaml` 的 `params.profileMode` 部分配置 `imageUrl`。

---

祝你写作愉快！✨
