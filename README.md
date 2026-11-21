# My AI Icons

自用 AI 图标库，首版收录 6 个从 [Lobe Icons](https://icons.lobehub.com/) 下载的 Logo。PNG 为 256 × 256 透明背景，保留原有颜色，四边留 16 px 空白；原 SVG 保存在 `sources/`。

## 图标合集订阅

兼容 Qure 的 `name`、`description`、`icons: [{name, url}]` 结构。将下列地址添加到支持该格式的客户端的图标合集 / 图标订阅入口：

```text
https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons.json
```

JSON 是图标索引，不是代理节点订阅或规则订阅。各客户端是否提供合集导入入口，以客户端实际版本为准。

| 图标 | 预览 | 直链 |
| --- | --- | --- |
| OpenAI | ![OpenAI](icons/openai.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/openai.png) |
| Claude | ![Claude](icons/claude.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/claude.png) |
| Claude Code | ![Claude Code](icons/claudecode.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/claudecode.png) |
| Anthropic | ![Anthropic](icons/anthropic.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/anthropic.png) |
| Antigravity | ![Antigravity](icons/antigravity.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/antigravity.png) |
| Muse | ![Muse](icons/muse.png) | [PNG](https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/muse.png) |

## Surge 用法

在现有配置的 `[Proxy Group]` 下，找到要设置图标的策略组，在该行末尾追加：

```ini
icon-url=https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/claude.png
```

若原策略组为 `Claude = select, 美国节点, 自动选择`，完整示例为：

```ini
[Proxy Group]
Claude = select, 美国节点, 自动选择, icon-url=https://raw.githubusercontent.com/Jay-make8/my-icons/main/icons/claude.png
```

`美国节点`、`自动选择` 仅为示例，请使用自己配置中已经存在的节点或策略组名称，保留原有组类型和成员。已存在 `icon-url` 时替换旧值即可。Surge 这里使用单张 PNG 链接；不要把 `icons.json` 填进 `icon-url`。Surge Mac 从 6.5.0 起支持此参数，参见 [Surge 官方手册](https://manual.nssurge.com/policy-groups/parameters.html)。

## 以后添加图标

1. 将新的透明 PNG 上传到 `icons/`，建议 256 × 256，使用英文小写文件名。
2. 将对应 SVG 原件保存到 `sources/`。
3. 在 `icons.json` 的 `icons` 数组末尾添加一项，`name` 为显示名称，`url` 为该 PNG 的 GitHub Raw 直链；注意 JSON 逗号格式。
4. 在客户端刷新图标合集。若图片被缓存，可暂时在 PNG 链接后追加 `?v=2`。

大小写必须与仓库中的文件名一致。若某个网络无法访问 GitHub Raw，先换到可以访问该域名的网络重试。

## 来源和记录

来源说明及原文件 SHA-256 见 [SOURCES.md](SOURCES.md)，LobeHub 的 MIT 许可原文见 [LICENSE-LobeHub.txt](LICENSE-LobeHub.txt)。品牌 Logo 及商标权归各权利人所有。

2026-11-21：建立公开自用图标库；仅收录本次下载的 6 个 Logo；保留 SVG，生成 PNG 和 Qure 结构的索引。文件名固定，后续更新尽量沿用原链接。
