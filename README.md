# Tavo Plugins

Tavo AI 插件仓库 - 自定义扩展功能集合

GitHub: https://github.com/Mariomoprc/tavo-plugins

## 插件列表

| 名称 | ID | 最新版本 | 下载 |
|------|-----|---------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | v1.5.5 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.cyoa.choices-v1.5.5/com.cyoa.choices-v1.5.5.tpg) |
| 📖 角色资料面板 | `com.relationship.panel` | v1.9.2 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.relationship.panel-v1.9.2/rel-panel.tpg) |

## 安装方式

1. 下载对应的 `.tpg` 文件
2. Tavo 中 → 我的 → +安装 → 选择 .tpg 文件
3. 启用 **高级渲染**（设置 → 显示设置 → 高级渲染）
4. 重启聊天页面

## 发布流程

```powershell
# 1. 创建 Release
gh release create "<plugin-id>-v<version>" --repo "Mariomoprc/tavo-plugins" --title "标题" --notes "说明"

# 2. 上传 .tpg 文件
gh release upload "<plugin-id>-v<version>" "plugin.tpg" --repo "Mariomoprc/tavo-plugins" --clobber

# 3. 更新 README.md 中的版本号和下载链接
```

## 参考来源

### tavo-card-craft v3.0.0
- **作者**: 永夜太白金
- **来源**: [Discord 帖子](https://discord.com/channels/1356606095207960616/1519670672341598208/1523697830764609576)
- **用途**: Tavo/SillyTavern 角色卡片制作者专用
- **路径**: `skills/tavo-card-craft/`
