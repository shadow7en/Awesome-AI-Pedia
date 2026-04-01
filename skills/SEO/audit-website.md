# audit-website

`audit-website` 是基于 `squirrelscan` 工具的强大网站审计 Skill。它专为开发者、SEO 专家和 AI 辅助编程环境设计，能够全方位扫描网站并生成详尽的体检报告。

---

## 🚀 快速开始

### 安装方式
在你的项目终端中运行：
```bash
npx skills add squirrelscan/skills --skill audit-website
```
或者在支持辅助工具（如 Claude Code/Cowork）中运行：
```bash
/plugin install squirrelscan/skills
```

### 使用方式
安装后，可以通过以下命令对指定网站进行审计：
- **核心命令**：`/audit-website [URL]`

---

## 核心功能

1.  **全方位审计**：包含 **230+ 条** 审计规则，覆盖 **21 个** 类别。
2.  **多维度覆盖**：
    - **SEO**：检查 Meta 标签、 broken links、关键词密度等。
    - **性能**：分析加载速度和资源瓶颈。
    - **可访问性 (Accessibility)**：确保网站符合 a11y 标准。
    - **内容质量**：检测重复内容和拼写错误。
3.  **深度安全检测**：能够识别并扫描出 **96 种** 常见的泄露密钥（如 AWS, Stripe, GitHub 等 API Keys）。
4.  **AI 原生优化**：生成的报告经过专门优化，方便 LLM 理解并提供针对性的修复建议。

---

## 使用场景

- **网站上线前体检**：确保没有死链，SEO 标签完整。
- **安全合规检查**：防止敏感密钥被意外暴露。
- **SEO 问题诊断**：当网站排名下降或流量异常时进行深度分析。
- **竞品分析**：通过审计了解竞争对手网站的技术参数。

---

**官方仓库**：[squirrelscan/skills](https://github.com/squirrelscan/skills)