# Tavo Plugins

Tavo AI 插件仓库 — 自动发布与版本管理。

GitHub: https://github.com/Mariomoprc/tavo-plugins

## 插件列表

| 插件 | ID | 最新版本 | 下载 |
|------|-----|---------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | v1.5.1 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.cyoa.choices-v1.5.1/com.cyoa.choices-v1.5.1.tpg) |
| 📋 角色资料面板 | `com.relationship.panel` | v1.5.1 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.relationship.panel-v1.5.1/com.relationship.panel-v1.5.1.tpg) |

## 安装方式

1. 下载对应插件的 `.tpg` 文件
2. Tavo → 设置 → 插件 → +安装 → 选择 .tpg 文件
3. 开启 **高级渲染**（设置 → 聊天设置 → 高级渲染）
4. 重启聊天页面

## 发布流程（给 AI 用）

```powershell
# 1. 更新 manifest.json 中的 version
# 2. 用 MCP 打包插件获取 zipBase64
# 3. 解码为 .tpg 文件
[System.IO.File]::WriteAllBytes("plugin.tpg", [System.Convert]::FromBase64String($zipBase64))

# 4. 创建 GitHub Release
gh release create "<plugin-id>-v<version>" --title "标题" --notes "变更说明" --repo Mariomoprc/tavo-plugins

# 5. 上传 .tpg 附件
gh release upload "<plugin-id>-v<version>" "plugin.tpg" --repo Mariomoprc/tavo-plugins --clobber

# 6. 更新 README 中的版本号和下载链接
# 7. 将源码推送到 plugins/<plugin-id>/ 目录
# 8. Discord 仅发 GitHub Release 链接
```

## 版本规范

- Tag: `<plugin-id>-v<semver>` (如 `com.cyoa.choices-v1.5.1`)
- 附件: `.tpg` 文件
- Discord: 仅发链接
