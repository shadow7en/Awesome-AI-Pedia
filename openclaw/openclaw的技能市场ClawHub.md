# OpenClaw 技能市场：ClawHub 指南 🎡

**ClawHub** 是 OpenClaw 的官方公共技能注册表（Registry），可以将其看作是 AI Agent 的“App Store”。它为全球开发者提供了一个分发、托管和管理 AI 技能（Skills）的中心化平台，让你的 AI 能够动态扩展处理各种特定任务的能力。

目前，ClawHub 拥有超过 **17,000+** 个各种类别的技能插件。

---

## 🚀 快速上手

### 1. 安装 ClawHub CLI
ClawHub 主要通过命令行界面进行操作。如果尚未安装，可以通过以下命令安装：

```bash
# 使用 npm 安装
npm install -g clawhub@latest

# 或使用 pnpm 安装
pnpm add -g clawhub
```
或直接 给小龙虾说 帮我安装 ClawHub

### 2. 搜索技能 (Search)
ClawHub 的搜索基于语义向量嵌入，支持使用自然语言或关键词搜索：

```bash
# 语义搜索：例如寻找日历相关技能
clawhub search "calendar helper"
```

### 3. 安装技能 (Install)
找到心仪的技能后，使用 `slug`（技能标识符）进行安装：

```bash
# 安装最新版
clawhub install <skill-slug>

# 安装指定版本
clawhub install <skill-slug>@<version>
```
*提示：安装完成后，建议重启 OpenClaw 会话以加载新技能。*

---

## 🛠️ 常用管理指令

| 命令 | 功能描述 |
| :--- | :--- |
| `clawhub list` | 查看已安装的所有技能列表 |
| `clawhub update <name>` | 更新指定技能到最新版本 |
| `clawhub update --all` | 一键更新本地所有已安装技能 |
| `clawhub uninstall <name>` | 移除不再需要的技能 |
| `clawhub whoami` | 查看当前登录的账户信息 |
| `clawhub login` | 通过浏览器授权登录 ClawHub 账户 |

---

## 🔒 核心安全建议 (必读)

ClawHub 是一个开放社区，为了防止恶意脚本（如键盘记录或数据泄露），请务必遵循以下**安全三原则**：

### 第一步：安装安全防护套件
在安装任何其他功能性技能前，**必须**优先安装安全审查工具：
```bash
# 安全审查协议：用于审计新 Skill 的源码
clawhub install skill-vetter

# 执行守护：防止在高风险环境下运行恶意命令
clawhub install exec-guard
```

### 第二步：按需配置 API Key
许多高级技能（如 Tavily 搜索、Github 操作）需要 API Key。
- **推荐做法**：运行 `openclaw dashboard` 通过 Web UI 界面进行可视化配置。
- **手动做法**：编辑 `~/.openclaw/skills/<技能名>/meta.json` 里的 `env` 字段。

### 第三步：定期审计
定期运行 `clawhub update --all` 以获取安全补丁，并对不再使用的、权限过高的技能及时进行 `uninstall`。

---

## 🌟 推荐必装技能组合

- **基础搜索**：`tavily-search`（解锁联网实时搜索）
- **长效记忆**：`bio-memory-pro`（让 AI 记住你的偏好和过往习惯）
- **代码增强**：`github` & `code-review`（开发者效率翻倍）
- **自动化**：`agent-browser`（允许 AI 直接操作浏览器执行任务）

---

> [!TIP]
> **想为社区做贡献？**
> 你编写的任何 Skill 都可以通过 `clawhub publish` 推送到市场，让全球用户受益。只需确保你的 Skill 符合 OpenClaw 的 [元数据规范](https://openclaw.ai/docs)。
