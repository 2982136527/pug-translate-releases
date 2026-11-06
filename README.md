# Pug 翻译

Safari / Chrome / Edge / Firefox 网页翻译扩展：按浏览器语言自动翻译网页，默认只显示译文。

## 功能

- 打开网页自动翻译，也可以切换为手动翻译；支持按站点设置自动/不自动。
- 仅译文或“原文 + 译文”双语显示；目标语言默认跟随浏览器，也可以手动固定。
- 优先翻译当前屏幕，滚动到哪里继续翻译；保留链接、图片、按钮和代码。
- 界面翻译：只翻译导航、按钮、表单，不动正文；目标语言跟随浏览器。固定界面文案内置多语言词表，新增文案使用 AI 兜底并缓存。
- 视频字幕翻译：YouTube 打开视频后默认自动翻译字幕，也可点控制栏“译”按钮关闭或重新开启；HTML5 播放器下方按钮；支持有字幕轨的站点，默认后台预翻译整条字幕轨，字号随播放器大小缩放。
- 划词/悬停/输入框翻译：选中文字点“译”；按住 Alt 悬停段落；输入框连按三次空格翻译并替换。
- 视频双语字幕与导出：字幕可显示“原文 + 译文”；弹窗可导出 SRT/VTT。
- PDF/EPUB 翻译：PDF 保排版覆盖译文，EPUB 阅读器支持目录、图片和章节翻译；从弹窗“PDF 翻译 / EPUB 翻译”进入。
- 精翻：自动生成全篇术语表，首遍译文先显示，后台按领域风格二次润色，去掉翻译腔并统一专名/术语；覆盖电影对白、小说叙事、技术、学术、新闻等，可在设置关闭。精翻需要内置接口或 OpenAI 兼容接口。
- 33 种目标语言 + 自定义；OpenAI 兼容接口提供 DeepSeek、OpenRouter、Groq、Gemini、Ollama 等预设。
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

1. 下载 `Pug-Translate-0.11.43-universal.dmg`，打开并把 `Pug 翻译.app` 拖入“应用程序”。
2. 打开 Safari → 设置 → 扩展，勾选 `Pug 翻译`，并允许访问网站。
3. 如果扩展没有出现：Safari 设置 → 高级 → 勾选“显示网页开发者功能”，再到菜单栏“开发” → 勾选“允许未签名的扩展”。
4. 未签名版每次退出 Safari 后，需要重新允许未签名扩展；如果 macOS 拦截 App，右键 App → 打开，或到“系统设置 → 隐私与安全性”点“仍要打开”。

### Chrome / Edge

1. 下载 `Pug-Translate-Chrome-0.11.43.zip`（Edge 用 `Pug-Translate-Edge-0.11.43.zip`）并解压。
2. Chrome 打开 `chrome://extensions`，Edge 打开 `edge://extensions`，开启“开发者模式”。
3. 点“加载已解压的扩展程序”，选择解压后的目录。
4. 固定 Pug 翻译，点图标或按 `Alt/Option+T` 翻译。

Chrome / Edge 版暂未上架应用商店。

### Firefox

1. 下载 `Pug-Translate-Firefox-0.11.43.zip`。
2. Firefox 地址栏打开 `about:debugging#/runtime/this-firefox`，点“临时载入附加组件”，选择 ZIP。
3. 临时载入在重启 Firefox 后失效；正式分发需要签名。

## 使用

1. **翻译网页**：点工具栏 Pug 图标 → “翻译本页”，或按 `Option+T`。
2. **还原原文**：再按一次 `Option+T`，或在弹窗里点“还原”。
3. **自动翻译**：默认开启；设置 → 触发方式可改成手动，也可以只对指定网站自动翻译。
4. **某站不自动翻译**：在设置里加入“不自动翻译的网站”，或在弹窗点“本站不自动翻译”。这些站点仍可手动翻译。
5. **换翻译服务**：设置 → 选择内置接口 / DeepLX / OpenAI 兼容接口，填写地址和 Key 后点“测试连接”。
6. **界面翻译**：设置 → 高级 → 界面翻译；站点清单每行一个域名。固定界面文案已内置多语言词表，站点新增文案才调用 AI 并缓存。
7. **视频字幕**：YouTube 点控制栏里的“译”按钮，HTML5 播放器点视频下方“翻译字幕”；设置可打开双语字幕；弹窗可导出 SRT/VTT。
8. **交互翻译**：设置可关闭划词/悬停/输入框翻译；划词后点“译”，Alt+悬停段落，输入框连按三次空格。
9. **文档翻译**：弹窗点“PDF 翻译”或“EPUB 翻译”，选择文件或粘贴 PDF 链接。

## 版本

0.11.43

## 说明

- 只翻译网页文字，不识别图片里的文字。
- 扫描版 PDF 没有文本层，暂不支持 OCR；PDF 译文按文本坐标覆盖，复杂版式可能与原排版有偏差。
- EPUB 阅读器保留目录/图片/基础阅读样式，出版社的复杂 CSS 版式会简化。
- 视频字幕只翻译网站已经提供的字幕；没有字幕或受 DRM 保护的视频无法翻译。
- 本仓库只提供安装包和使用说明，不包含源码。

## 第三方组件

GitHub 中文界面词表部分数据来自 [github-hans](https://github.com/52cik/github-hans)（MIT）。完整版权与许可声明见 [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)。
