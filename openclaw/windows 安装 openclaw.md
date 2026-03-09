# Windows 环境安装 OpenClaw 指南

本文档将引导你在 Windows 系统上安装并配置 **OpenClaw**。

---

## 📋 环境准备

在开始之前，请确保你的系统满足基本要求。

### 第一步：安装 Git

1. **下载与安装**：访问 [Git 官网](https://git-scm.com/) 下载并安装适用于 Windows 的版本。
2. **验证安装**：安装完成后，打开 **PowerShell** 或 **命令提示符 (CMD)**，运行以下命令：
   ```powershell
   git --version
   ```
   *如果能看到版本号（如 `git version 2.x.x`），说明安装成功。*

### 第二步：安装 Node.js

> [!IMPORTANT]
> 请确保安装较新版本的 Node.js（建议使用 LTS 版本或最新稳定版）。

1. **下载与安装**：访问 [Node.js 官网](https://nodejs.org/) 下载并安装。
2. **验证安装**：在终端运行以下命令：
   ```powershell
   node -v
   npm -v
   ```
   *两条命令都应返回对应的版本号。*

---

## 🚀 安装 OpenClaw

### 第三步：全局安装 Clawdbot

使用 `npm` 进行全局安装：

```powershell
npm install -g clawdbot
```

**验证安装**：
```powershell
clawdbot --version
```
*如果看到版本号，说明 Clawdbot 已成功安装到你的系统中。*

---

## ⚙️ 配置与启动

### 第四步：初始化配置

执行启动命令进入初始化流程：

```powershell
clawdbot onboard
```

**操作指南**：
1. **确认初始化**：根据提示选择 `yes`。
2. **选择模型**：建议选择 `qwen` (通义千问)。
3. **完成授权**：
   - 程序将自动打开浏览器，请登录/注册通义千问账号。
   - 支持使用 **GitHub 账号** 直接登录。
4. **开始体验**：完成登录后，回到终端即可开始对话。

### 常用命令

- **重启服务**：
  ```powershell
  clawdbot restart
  ```