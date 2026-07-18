# Tavo Plugins

Tavo AI 插件仓库 — 自动发布与版本管理。

GitHub: https://github.com/Mariomoprc/tavo-plugins

## 插件列表

| 插件 | ID | 最新版本 | 下载 |
|------|-----|---------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | v1.5.2 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.cyoa.choices-v1.5.2/com.cyoa.choices-v1.5.2.tpg) |
| 📋 角色资料面板 | `com.relationship.panel` | v1.5.2 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.relationship.panel-v1.5.2/com.relationship.panel-v1.5.2.tpg) |

## 安装方式

1. 下载对应插件的 `.tpg` 文件
2. Tavo → 设置 → 插件 → +安装 → 选择 .tpg 文件
3. 开启 **高级渲染**（设置 → 聊天设置 → 高级渲染）
4. 重启聊天页面

## 已知问题

**Tavo v0.92.0 MCP bug**: `tavo_plugin_install` 和 `tavo_plugin_validate_manifest` 会丢弃 manifest 中的 `htmlFragments` 内容。
- 通过 MCP 安装的插件无法正确注册 HTML 片段
- **解决方法**: 从 GitHub Release 下载 `.tpg` 文件，用手机文件管理器安装
- 这是 Tavo 服务端 bug，等待修复

## 发布流程（给 AI 用）

```powershell
# 1. 更新 manifest.json 中的 version
# 2. 用 MCP 打包插件，保存 .tpg 文件
# 3. 创建 GitHub Release 并上传 .tpg
# 4. 推源码到 plugins/ 目录
# 5. 更新 README 中的下载链接
# 6. Discord 仅发 GitHub Release 链接
```

## 版本规范

- Tag: `<plugin-id>-v<semver>` (如 `com.cyoa.choices-v1.5.2`)
- 附件: `.tpg` 文件
- 发布说明: 记录所有变更
