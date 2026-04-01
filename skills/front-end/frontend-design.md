# frontend-design

`frontend-design` 是 Anthropic 官方推出的 AI Agent Skill，旨在帮助 AI 开发具有**高辨识度、生产级质量**的前端界面。它超越了通用的“AI 审美”，通过明确的设计思维和美美学指南，让 AI 能够创作出富有创意且细节考究的 Web UI。

---

## 🚀 快速开始

### 安装方式
在你的项目终端中运行：
```bash
npx skills add anthropics/skills --skill frontend-design
```
*注：该 Skill 兼容 Claude Code 等支持 Skill 系统的人工智能辅助工具。*

---

## 🎨 设计哲学

该 Skill 引导 AI 避免平庸的“AI 风格”，并遵循以下设计逻辑：

1.  **明确调性**：在编码前确定极端风格（如：极致极简、复古未来感、高级精致、报刊杂志风、粗犷主义等）。
2.  **独特性**：寻找让界面“令人难忘”的记忆点。
3.  **工程化**：实现真正可运行、具备生产环境质量的代码。

---

## 📐 审美指南

### 1. 字体排版 (Typography)
*   **拒绝通用**：避免使用 Arial、Inter 或 Roboto 等常见系统字体。
*   **独特搭配**：使用极具个性的显示字体（Display Font）搭配精致的正文文字。

### 2. 颜色与主题 (Color & Theme)
*   **强一致性**：使用 CSS 变量确保色调统一。
*   **鲜明对比**：倾向于使用具有强烈视觉冲击力的主色调配合精准的强调色。

### 3. 动态交互 (Motion)
*   **CSS 优先**：优先使用 CSS 动画实现丝滑的揭示效果。
*   **高光时刻**：通过交错加载（staggered reveals）和令人惊喜的悬停状态提升用户愉悦感。

### 4. 空间布局 (Spatial Composition)
*   **打破常规**：尝试不对称布局、元素重叠、对角线流向或网格留白，创造节奏感。

### 5. 视觉细节 (Visual Details)
*   **深度感**：使用梯度网格（Gradient Mesh）、噪点纹理、几何图案或磨砂玻璃效果替代纯色背景。

---

## 🛠️ 使用场景

*   **网页/组件开发**：构建 Landing Page、仪表盘、复杂的 React/Vue 组件。
*   **UI 美化**：对现有的 Web 界面进行重构或视觉升级。
*   **创意演示**：制作海报级布局、数据可视化或互动演示。

---

> [!IMPORTANT]
> **切记**：`frontend-design` 的核心是**意图 (Intentionality)**。无论是极致的简洁还是华丽的繁复，每一行代码和样式都应为整体视觉愿景服务。

---
**官方仓库**：[anthropics/skills](https://github.com/anthropics/skills)