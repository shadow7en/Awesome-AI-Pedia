# baoyu-skills

`baoyu-skills` 是由知名技术专家宝玉老师自用并开源的一套 AI Agent Skill 集合。它深度集成了内容创作者从灵感、撰写、插图到发布的全流程工作流，旨在利用 AI 极大地提升内容生产效率。

---

## 🚀 快速开始

### 安装方式
在你的项目终端中运行：
```bash
npx skills add jimliu/baoyu-skills
```
或者在支持辅助工具（如 Claude Code）的插件市场中搜索并安装。

---

## 核心功能模块

### 1. 视觉辅助与创作
- **`baoyu-cover-image`**：自动化生成文章封面图，支持 10 种色盘、7 种渲染风格及多种尺寸比例。
- **`baoyu-article-illustrator`**：智能分析文章结构，根据内容自动生成具有高度相关性的插图。
- **`baoyu-infographic`**：将复杂的文本内容转换为精美的信息图，内置 20 种布局和 17 种视觉风格。
- **`baoyu-xhs-images`**：专为小红书设计的配图工具，可按风格和布局系统生成系列组图。
- **`baoyu-slide-deck`**：根据内容快速生成 PPT 演示文稿的大纲及幻灯片素材。

### 2. 内容优化与格式化
- **`baoyu-format-markdown`**：深度优化 Markdown 文档，包括公式化的标题建议、元数据 (frontmatter) 生成。
- **`baoyu-translate`**：具备工作流机制的高质量翻译，支持多种触发模式。
- **`baoyu-markdown-to-html`**：高度可定制的 Markdown 转 HTML 工具，支持自定义字体、颜色和代码主题。

### 3. 一键分发与工具类
- **`baoyu-post-to-wechat` & `baoyu-post-to-weibo`**：支持将处理好的内容一键同步发布到微信公众号和微博。
- **`baoyu-compress-image`**：轻量级图片压缩工具，处理生成后的视觉素材。

---

## 进阶玩法

可以通过项目根目录或用户目录下的 `EXTEND.md` 文件来自定义 Skill 的默认行为、覆盖配置或定义个性化预设。

---

**官方仓库**：[JimLiu/baoyu-skills](https://github.com/JimLiu/baoyu-skills)
