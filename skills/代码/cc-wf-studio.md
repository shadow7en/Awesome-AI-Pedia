# CC Workflow Studio - AI Agent 可视化工作流编辑器 🚀

**CC Workflow Studio** 是一款专为 AI Agent（如 Claude Code, GitHub Copilot, Cursor, Antigravity 等）设计的直观可视化工作流设计工具。它允许开发者通过简单的拖拽式节点操作，构建复杂的自动化流程，将重复性的开发任务转化为高效可复用的 AI 编排流。

---

## 🌟 核心功能：重新定义 AI 工作流

- **🔀 可视化流编辑器**：基于 React Flow 的拖拽式界面，直观构建 AI 代理编排逻辑，无需编写繁琐的代码。
- **🤖 Agentic Engineering**：支持多代理协作（Multi-agent）、子代理编排（Sub-Agent）、Agent Skills 以及 MCP 工具集成，是构建代理化工程的核心利器。
- **✨ AI 驱动编辑**：通过自然语言描述即可自动生成或迭代优化工作流。支持集成 MCP Server，实现 AI 代理对工作流的实时修改。
- **⚡ 一键导出与运行**：支持将工作流导出为 `.md` 格式的斜杠命令（Slash Commands）或 Agent Skills，并可在编辑器中直接一键运行。

---

## 🚀 快速上手：从安装到第一个工作流

### 1. 环境准备
- **Node.js**: 18.x 或更高版本
- **VSCode**: 1.80 或更高版本
- **Git**

### 2. 安装与构建
```bash
# 1. 克隆仓库
git clone https://github.com/breaking-brake/cc-wf-studio.git
cd cc-wf-studio

# 2. 安装依赖
npm install
cd src/webview && npm install

# 3. 构建 Webview
npm run build
cd ../..

# 4. 编译扩展
npm run compile
```

### 3. 启动插件
- 点击编辑器右上角的 **CC Workflow Studio 图标** 即可开启可视化编辑器。
- 或使用快捷键 `Cmd+Shift+P` (Mac) 搜索并选择 `"CC Workflow Studio: Open Editor"`。

---

## 🛠️ 如何使用：构建你的自动化专家

### 🎨 创建工作流
从左侧面板拖动节点到画布：
- **Start**: 工作流入口。
- **MCP Tool**: 集成外部工具（如 GitHub PR 获取、文件操作等）。
- **Sub-Agent**: 指派子代理执行特定任务（如安全审计、重构建议）。
- **Switch/IfElse**: 实现逻辑分支。
- **Skill**: 执行预定义的原子化 AI 技能。

### 💾 保存与加载
- **保存**: 点击工具栏 **Save** 图标，工作流将以 `.json` 格式存储在项目根目录的 `.vscode/workflows/` 下。
- **加载**: 点击 **Load** 图标，可重新加载已有的工作流进行编辑。

### 📤 导出与运行
- **导出**: 点击 **Export** 按钮，系统会将工作流转换为 `.md` 格式。
- **运行**: 点击 **Run** 按钮，直接在集成的终端/AI Agent 中启动执行。
- **路径支持**: 
    - **Claude Code**: `.claude/commands/`, `.claude/agents/`
    - **GitHub Copilot**: `.github/prompts/`, `.github/skills/`
    - **Cursor**: `.cursor/agents/`, `.cursor/skills/`
    - **Antigravity**: `.agent/skills/`
    - **Roo Code**: `.roo/skills/`

### ✨ AI 辅助编辑 (AI Editing)
点击工具栏的 **Sparkles (星光)** 图标开启 AI 模式：
- **对话式生成**: "帮我创建一个自动化 PR 审查工作流，如果是中大规模 PR 则调用代码质量分析 Skill。"
- **MCP 服务**: 插件会自动在后台启动 MCP Server，允许 AI Agent 像人类一样感知并直接修改画布上的节点和属性。

---

## 💡 实战案例：自动化 PR 代码审查流

通过 CC Workflow Studio，你可以快速搭建一个高效的 PR 审查专家：
1. **获取信息**: 使用 `MCP Tool` 调用 `github.get_pull_request`。
2. **逻辑分支**: 通过 `Switch` 节点判断 PR 的大小（Additions 数量）。
3. **安全审计**: 对于关键修改，分发给具有安全背景的 `Sub-Agent`。
4. **生成报告**: 汇总所有节点的输出，最后使用 `Skill` 节点生成最终的 Markdown 审查报告并提交。

---

## 📚 高级功能与定制化

### 🔧 自定义节点开发
如果你需要更特殊的业务逻辑，可以扩展自定义节点：
1. 在 `src/shared/types/workflow-definition.ts` 定义节点类型。
2. 在 `src/webview/src/components/nodes/` 创建相应的 React 组件。
3. 在 `src/webview/src/components/WorkflowEditor.tsx` 注册节点。
4. 在 `src/extension/services/export-service.ts` 实现对应的导出逻辑。

---

## 🔗 相关资源
- **GitHub Repo**: [breaking-brake/cc-wf-studio](https://github.com/breaking-brake/cc-wf-studio)
- **许可证**: AGPL-3.0

> [!TIP]
> **CC Workflow Studio** 不仅仅是一个绘图工具，它是 AI 编程时代的 IDE 扩展，旨在让复杂的 AI 协作变得可视化、透明化且可管理。
