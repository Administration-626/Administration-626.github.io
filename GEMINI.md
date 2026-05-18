# 🤖 Gemini 项目契约 (GEMINI.md) - Jekyll 博客版

> **致 AI 助手 (Gemini)**：
> 你正处于一个基于 **Jekyll** 构建的静态博客项目中。请忽略任何关于 Next.js、Prisma 或 Todo-List 的旧指令。在后续的任务中，必须严格遵守本契约定义的架构边界和规范。

---

## 🎯 1. 项目全局视界 (Project Context)

- **项目名称**：Administration-626 Blog
- **项目目标**：构建一个高性能、SEO 友好且易于维护的个人技术博客。
- **核心功能**：
  - 基于 Markdown 的文章自动化发布（Jekyll 引擎）。
  - 基于 Liquid 模板的主题渲染。
  - 响应式布局与原生 CSS 样式。
  - 站内轻量级搜索功能（基于 `search.json` 和 `simple-jekyll-search`）。
- **非目标**：
  - ❌ 动态后端服务或 API（一切功能需在静态构建期完成）。
  - ❌ 复杂的 React/Vue 状态管理（仅允许原生 JS 或轻量级脚本）。
  - ❌ 用户注册、评论系统（除非通过第三方嵌入）。

## 🛠️ 2. 技术栈与架构边界 (Tech Stack & Boundaries)

必须严格使用以下技术，禁止引入不必要的重量级依赖：

- **核心引擎**：Jekyll (Ruby)
- **模板语言**：Liquid (严格使用 Jekyll 过滤器如 `relative_url`)
- **内容格式**：Markdown (Kramdown)
- **样式方案**：原生 CSS (维护 `css/style.css`)
- **搜索索引**：`search.json` (自动生成索引)
- **前端脚本**：原生 JavaScript / `simple-jekyll-search`

## 📋 3. AI 行为约束 (AI Behavior Constraints)

### 3.1 Jekyll 规范优先
- **Front Matter**：创建或修改文章时，YAML 头信息必须包含 `layout`, `title`, `date`, `tags` 等字段。
- **文件名规范**：`_posts/` 下的文件必须遵循 `YYYY-MM-DD-title.md` 格式。
- **静态思维**：功能实现应优先考虑 Jekyll 内置功能（如 `site.data`, `site.tags`），而非在客户端通过 JS 渲染。

### 3.2 质量增强（强制项）
- **语义化 HTML**：生成的 HTML 片段必须符合 SEO 标准（使用 `<article>`, `<time>`, `<nav>` 等）。
- **响应式 CSS**：修改样式时，必须确保在 Mobile/Desktop 端的阅读体验，避免固定像素宽度。
- **路径安全**：始终使用 `{{ "/path" | relative_url }}` 处理链接，以确保在 GitHub Pages 子路径下能正常工作。

### 3.3 目录结构规范
- `_posts/`：存放所有文章。
- `_layouts/`：存放页面模板（如 `default.html`, `post.html`）。
- `css/`：存放样式表。
- `_config.yml`：全局配置文件，修改后需提醒用户注意。
- `search.json`：搜索索引模板。

## 📂 4. 协作工作流 (Workflow)

1.  **新增文章**：生成符合日期规范的文件名，并填充符合 Front Matter 标准的内容。
2.  **样式调整**：直接在 `css/style.css` 中进行 surgical edits，禁止覆盖全局变量。
3.  **模板修改**：在 `_layouts/` 中修改时，确保不破坏原有的 Liquid 逻辑结构。

---
*本契约自 2026-05-18 起生效，正式取代所有历史版本的项目指令。*
