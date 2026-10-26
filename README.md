# zcode-plugins

个人 ZCode 插件市场：收录自研插件，**各插件独立仓库维护**，本仓库只做编目（`marketplace.json`）。

## 添加市场

ZCode → **设置 → 插件管理 → Discover 页签 → `+` → 添加插件市场**，粘贴：

```
https://github.com/goubo/zcode-plugins
```

添加后在市场列表中浏览、安装、升级。

## 插件列表

| 插件 | 版本 | 说明 | 仓库 |
| --- | --- | --- | --- |
| Auto Rename Sessions（会话自动重命名） | 1.2.0 | Stop hook 自动生成「子项目｜主线目标」标题，规则/GLM 双引擎，支持 `/rename-session` 按需重命名 | [goubo/zcode-auto-rename](https://github.com/goubo/zcode-auto-rename) |

## 新插件发布流程

1. 新插件独立建仓（根目录含 `.zcode-plugin/plugin.json`，无需自带 marketplace.json）；
2. 本仓库 `marketplace.json` 追加一条：`source: { "source": "github", "repo": "<owner>/<repo>" }`，`version` 与插件清单版本保持同步；
3. 提交并 push 本仓库，用户侧刷新市场即可见。

版本升级：插件仓库发版后，同步更新编目里的 `version`。
