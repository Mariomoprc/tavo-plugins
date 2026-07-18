# Tavo Plugins

Tavo AI 插件仓库 — 自动发布与版本管理。

## 插件列表

| 插件 | ID | 最新版本 | 简介 |
|------|-----|---------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | [v1.5.0](https://github.com/Mariomoprc/tavo-plugins/releases/tag/com.cyoa.choices-v1.5.0) | 互动小说式行动选项生成 |
| 📋 角色资料面板 | `com.relationship.panel` | [v1.5.0](https://github.com/Mariomoprc/tavo-plugins/releases/tag/com.relationship.panel-v1.5.0) | 角色资料与故事线分析 |

## 安装方式

1. 从 [Releases](https://github.com/Mariomoprc/tavo-plugins/releases) 下载 `.tpg` 文件
2. Tavo → 设置 → 插件 → +安装 → 选择 .tpg 文件
3. 开启 **高级渲染**（设置 → 聊天设置 → 高级渲染）

## 开发指南

插件源码在 `plugins/` 目录下，每个插件一个子目录。

### 打包发布

```powershell
# 使用 MCP 打包
$body = '{"jsonrpc":"2.0","id":1,"method":"tools/call","params":{"name":"tavo_plugin_package","arguments":{"files":[{"path":"manifest.json","text":"..."}],"includeZipBase64":true}}}'
# 然后创建 GitHub Release 上传 .tpg
```

### 版本规范

- 格式：`<plugin-id>-v<semver>` (如 `com.cyoa.choices-v1.5.0`)
- 发布说明：记录所有变更
- 附件：打包好的 `.tpg` 文件

## 自研插件详情

### 剧情选择器 (com.cyoa.choices)

**功能**: CYOA 互动小说式选项生成器。点击工具栏骰子按钮，AI 根据对话生成 5 个行动选项。

**版本历史**: v1.3.0 → v1.3.1 → v1.4.0 → v1.5.0 → v1.5.1

**特点**:
- 面板可拖动，选项缓存秒出
- 智能刷新（消息变化自动重新生成）
- 生成计时 + 多格式 fallback
- 并发安全（genSeq 计数器）

### 角色资料面板 (com.relationship.panel)

**功能**: 角色卡资料与故事线分析面板，5 个标签页。

**版本历史**: v1.3.0 → v1.4.0 → v1.5.0 → v1.5.1

**特点**:
- 角色设定 / 性格 / 场景 / 备注 / 故事线
- 角色颜色标记
- AI 故事线分析
- 多角色自动识别
