# Ghostty

> **Ghostty** 是由 Mitchell Hashimoto 开发的一个快速、极致原生、且由 GPU 加速的终端终端模拟器。它旨在将高性能渲染与原生操作系统的 UI 体验完美结合。


## ✨ 核心特性

- **极致性能**：利用 GPU 加速（macOS 上使用 Metal，Linux 上使用 OpenGL），即便是在处理海量日志时也能保持丝滑流畅。
- **原生体验**：不使用自定义渲染的小部件，而是使用平台原生的 UI 组件来处理窗口、标签页和分屏。
- **现代协议支持**：支持 Kitty 图形协议、超链接、同步渲染、连字（Ligatures）等。
- **开箱即用**：无需繁琐配置即可获得极佳的默认体验，并内置对 Nerd Fonts 的支持。
- **嵌入式核心**：共享核心库 `libghostty`，确保跨平台逻辑一致且高效。

---

## 📦 安装指南

### macOS
推荐使用 Homebrew 安装：
```bash
brew install --cask ghostty
```
或者从 [Ghostty 官网](https://ghostty.org) 下载 `.dmg` 文件手动安装。

### Linux
支持通过 Nix、Snap 或从源码编译。
- **Nix**: `nix-env -iA nixpkgs.ghostty`
- **Snap**: `sudo snap install ghostty --edge --classic`

---

## ⚙️ 配置与定义

Ghostty 即使没有配置文件也能运行，但你可以通过简单的 `key = value` 文本文件进行个性化定制。

### 配置文件路径
- **macOS**: `~/Library/Application Support/com.mitchellh.ghostty/config`
- **通用**: `~/.config/ghostty/config`

### 配置示例
```text
theme = Monokai Soda
font-family = JetBrains Mono
font-size = 14
window-padding-x = 15
window-padding-y = 15
cursor-style = block
```

### 常用快捷键 (macOS)
- **热重载配置**：`Cmd + Shift + ,` (修改配置文件后无需重启终端)
- **显示所有配置说明**：在终端运行 `ghostty +show-config --default --docs`

---

## 🔗 相关资源
- [官方网站](https://ghostty.org)
- [GitHub 仓库](https://github.com/ghostty-org/ghostty)