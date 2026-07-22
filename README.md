# Tavo Plugins

Tavo AI 角色聊天的插件仓库。

## Tavo AI

Tavo 是一款手机端 AI 角色聊天应用，支持：
- 🎭 **角色卡** — 创建、导入、编辑 AI 角色
- 💬 **沉浸聊天** — 与 AI 角色进行自然对话
- 📚 **世界书** — 角色背景设定与世界观构建
- 🧩 **插件系统** — 第三方扩展（`.tpg` 格式）
- 🔌 **MCP Server** — 供 Claude Code / OpenCode 等 agent 远程调用

**安装 Tavo**: [Discord 邀请链接](https://discord.com/invite/tavo) | **版本**: v0.92.0+（需开启高级渲染）

## 插件列表

| 插件 | ID | 版本 | 说明 |
|------|-----|------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | [v1.9.0](https://github.com/Mariomoprc/tavo-plugins/releases/tag/com.cyoa.choices-v1.9.0) | 剧情分支选择，5 种差异化风格。浮动按钮，缓存选项 |
| 📖 角色资料面板 | `com.relationship.panel` | [v4.2.9](https://github.com/Mariomoprc/tavo-plugins/releases/tag/com.relationship.panel-v4.2.9) | 情报站/角色卡/世界书。AI 剧情分析，新消息自动刷新 |

> 下载 `.tpg` 请到 [Releases](https://github.com/Mariomoprc/tavo-plugins/releases) 页面。

## 安装方法

### Tavo 内安装

1. 打开 Tavo → 设置 → 插件管理 → +
2. 输入 Release 页面的 `.tpg` 文件直链
3. 安装成功后，在聊天界面操作

### Tavo MCP 安装

```powershell
$body = '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"tavo_plugin_install","arguments":{"zipBase64":"$(Get-Content plugin.tpg -AsByteStream | Convert-ToBase64)"}}}'
```

## 开发插件

- `.tpg` = 标准 zip 包，含 `manifest.json` + 插件文件
- 使用 [TavoJS API](https://docs.tavo.ai) 开发插件逻辑
- 需申请插件开发者权限
