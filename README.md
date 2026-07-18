# Tavo Plugins

Tavo AI 插件仓库 — 自动发布与版本管理。

GitHub: https://github.com/Mariomoprc/tavo-plugins

## 插件列表

| 插件 | ID | 最新版本 | 下载 |
|------|-----|---------|------|
| 🎲 剧情选择器 | `com.cyoa.choices` | v1.5.4 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.cyoa.choices-v1.5.4/com.cyoa.choices-v1.5.4.tpg) |
| 📋 角色资料面板 | `com.relationship.panel` | v1.5.4 | [下载 .tpg](https://github.com/Mariomoprc/tavo-plugins/releases/download/com.relationship.panel-v1.5.4/com.relationship.panel-v1.5.4.tpg) |

## 安装方式

1. 下载对应插件的 `.tpg` 文件
2. Tavo → 设置 → 插件 → +安装 → 选择 .tpg 文件
3. 开启 **高级渲染**（设置 → 聊天设置 → 高级渲染）
4. 重启聊天页面

## 发布流程

```powershell
# 1. 更新 manifest.json 版本号
# 2. 用 MCP tavo_plugin_package 打包
# 3. 创建 GitHub Release 并上传 .tpg
# 4. 推源码到 plugins/ 目录
# 5. 更新 README
# 6. Discord 仅发链接
```

## 版本规范

- Tag: `<plugin-id>-v<semver>`
- 附件: `.tpg` 文件
- 发布说明: 记录所有变更

## 版本历史

### 剧情选择器

| 版本 | 日期 | 说明 |
|------|------|------|
| v1.5.4 | 7/18 | 修复计时器闪烁、从1开始计数 |
| v1.5.3 | 7/18 | 修复 manifest 格式（contributes.htmlFragments） |
| v1.5.0 | 7/17 | 首发（原始工作版本） |

### 角色资料面板

| 版本 | 日期 | 说明 |
|------|------|------|
| v1.5.3 | 7/18 | 修复 manifest 格式（contributes.htmlFragments） |
| v1.5.0 | 7/17 | 首发（原始工作版本） |
