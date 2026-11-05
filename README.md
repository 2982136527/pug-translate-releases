# Pug 翻译

Safari / Chrome 网页翻译扩展：按浏览器语言自动翻译网页，默认只显示译文。

## 功能

- 打开网页自动翻译，也可以切换为手动翻译；支持按站点设置自动/不自动。
- 仅译文或“原文 + 译文”双语显示；目标语言默认跟随浏览器，也可以手动固定。
- 优先翻译当前屏幕，滚动到哪里继续翻译；保留链接、图片、按钮和代码。
- 界面翻译：只翻译导航、按钮、表单，不动正文；目标语言跟随浏览器。固定界面文案内置多语言词表，新增文案使用 AI 兜底并缓存。
- 视频字幕翻译：YouTube 打开视频后默认自动翻译字幕，也可点控制栏“译”按钮关闭或重新开启；HTML5 播放器下方按钮；支持有字幕轨的站点，默认后台预翻译整条字幕轨，字号随播放器大小缩放。
- 翻译服务：内置接口（无需配置）、自建 DeepLX、OpenAI 兼容接口。

## 界面翻译站点

界面翻译和整页翻译共用目标语言，默认跟随浏览器。目前覆盖：

| 站点 | 域名 |
| --- | --- |
| GitHub | `github.com` |
| Stack Overflow | `stackoverflow.com`（含 `meta.stackoverflow.com`） |
| Stack Exchange | `stackexchange.com`（含 `meta.stackexchange.com`） |
| Super User | `superuser.com`（含 `meta.superuser.com`） |
| Server Fault | `serverfault.com`（含 `meta.serverfault.com`） |
| Ask Ubuntu | `askubuntu.com`（含 `meta.askubuntu.com`） |
| MathOverflow | `mathoverflow.net`（含 `meta.mathoverflow.net`） |
| Stack Apps | `stackapps.com` |
| Hacker News | `news.ycombinator.com` |
| Discord | `discord.com` |
| TED | `ted.com` |
| Vimeo | `vimeo.com` |
| Figma | `figma.com` |

界面翻译与整页翻译是两件事：前者只改导航、按钮、表单等界面文字，后者处理网页正文。

## 安装

### Safari（macOS）

1. 下载 `Pug-Translate-0.11.29-universal.dmg`，打开并把 `Pug 翻译.app` 拖入“应用程序”。
2. 打开 Safari → 设置 → 扩展，勾选 `Pug 翻译`，并允许访问网站。
3. 如果扩展没有出现：Safari 设置 → 高级 → 勾选“显示网页开发者功能”，再到菜单栏“开发” → 勾选“允许未签名的扩展”。
4. 未签名版每次退出 Safari 后，需要重新允许未签名扩展；如果 macOS 拦截 App，右键 App → 打开，或到“系统设置 → 隐私与安全性”点“仍要打开”。

### Chrome

1. 下载 `Pug-Translate-Chrome-0.11.29.zip` 并解压。
2. 打开 `chrome://extensions`，开启右上角“开发者模式”。
3. 点“加载已解压的扩展程序”，选择解压后的目录。
4. 固定 Pug 翻译，点图标或按 `Alt/Option+T` 翻译。

Chrome 版暂未上架应用商店。

## 使用

1. **翻译网页**：点工具栏 Pug 图标 → “翻译本页”，或按 `Option+T`。
2. **还原原文**：再按一次 `Option+T`，或在弹窗里点“还原”。
3. **自动翻译**：默认开启；设置 → 触发方式可改成手动，也可以只对指定网站自动翻译。
4. **某站不自动翻译**：在设置里加入“不自动翻译的网站”，或在弹窗点“本站不自动翻译”。这些站点仍可手动翻译。
5. **换翻译服务**：设置 → 选择内置接口 / DeepLX / OpenAI 兼容接口，填写地址和 Key 后点“测试连接”。
6. **界面翻译**：设置 → 高级 → 界面翻译；站点清单每行一个域名。固定界面文案已内置多语言词表，站点新增文案才调用 AI 并缓存。
7. **视频字幕**：YouTube 点控制栏里的“译”按钮，HTML5 播放器点视频下方“翻译字幕”；默认后台预翻译整条字幕轨，可在设置里关闭。

## 版本

0.11.29

## 说明

- 只翻译网页文字，不识别图片里的文字。
- 视频字幕只翻译网站已经提供的字幕；没有字幕或受 DRM 保护的视频无法翻译。
- 本仓库只提供安装包和使用说明，不包含源码。

## 第三方组件

GitHub 中文界面词表部分数据来自 [github-hans](https://github.com/52cik/github-hans)（MIT）。完整版权与许可声明见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
