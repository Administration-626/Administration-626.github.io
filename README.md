# Administration-626 的个人博客

这是一个基于 Jekyll 搭建的个人网站，采用深色主题，支持标签和全文搜索。

## 📂 目录结构说明

- `_posts/`: **文章存放地**。所有的博客文章（Markdown格式）都放在这里。
- `_layouts/`: 页面模板。定义了首页和文章页的布局。
- `css/`: 样式表。定义了夜间模式的色调。
- `_config.yml`: 网站全局配置文件。
- `search.json`: 搜索功能的索引文件。
- `index.html`: 首页内容及搜索逻辑。

## ✍️ 如何撰写博客

1. **新建文件**：在 `_posts/` 目录下创建文件，命名格式为 `YYYY-MM-DD-title.md`。
2. **添加头部 (Front Matter)**：文件开头必须包含以下内容：
   ```yaml
   ---
   layout: post
   title: "你的文章标题"
   date: 2026-05-18 12:00:00 +0800
   tags: [标签1, 标签2]
   ---
   ```
3. **编写正文**：在头部下方使用标准 Markdown 语法编写内容。

## 💻 本地预览测试

在上传到 GitHub 之前，可以在本地查看效果：

1. **安装环境** (仅首次):
   ```bash
   gem install jekyll bundler
   ```

2. **启动预览**:
   在项目根目录下运行：
   ```bash
   jekyll serve --host 0.0.0.0
   ```

3. **访问地址**:
   - 本机访问：`http://localhost:4000`
   - 局域网访问：`http://192.168.2.151:4000` (或你的实际IP)
