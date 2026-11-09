# 更新日志

本文件记录本仓库（Mandelbrot 集绘制算法中文译本）的所有重要变更。

格式参考 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## [1.0.0] - 2026-11-09

首个正式版本：Mandelbrot 集绘制算法条目（英文维基百科 `oldid=1380046103`）的完整中文译本与配套工具。

### 新增

**中文译本**

- `plotting-algorithms-mandelbrot.zh-CN.md`：Markdown 源文件，公式为 LaTeX。
- `plotting-algorithms-mandelbrot.zh-CN.html`：HTML，公式为 MathML。
- `plotting-algorithms-mandelbrot.zh-CN.pdf`：PDF，XeLaTeX 排版，章节编号从 `1` / `1.1` 起。
- `plotting-algorithms-mandelbrot.zh-CN.wiki`：Wikitext 译本，沿用原条目的模板、`[[File:...]]` 文件名、
  `<ref>` 参考文献与分类结构；118 处 `<math>`、21 条参考文献、20 处图片引用与原条目一一对应，
  公式与伪代码逐字保留。

**英文对照**

- `source_en.txt`：英文维基百科条目的 Wikitext 底稿，译本对照基准。
- `plotting-algorithms-mandelbrot.en.md` / `.html` / `.pdf`：由原始 PDF 转出的英文原文。

**许可证与媒体**

- `LICENSE`：正文许可证全文（CC BY-SA 4.0）。
- `LICENSES.md`：原文页面全部图片与视频的许可证、作者及来源逐项清单。
- `images/`、`videos/`：原文页面图片与视频的本地副本（含视频静帧封面）。
- `Original_PDF/`：转换所用原始 PDF 与抓取说明。

**文档与协作**

- `README.md`：仓库说明、转换方式、重新构建 PDF / HTML 的步骤、许可证汇总。
- `CHANGELOG.md`：本文件。
- `CONTRIBUTING.md`：文件地图（源文件 vs 构建产物）、校对与翻译约定、术语对照表、
  提交规范、媒体许可证要求、贡献许可声明。
- `.github/ISSUE_TEMPLATE/`：译文问题 / 校对建议模板、构建与文件问题模板，关闭空白 issue。
- `.github/pull_request_template.md`：改动说明与核对清单。
- `assets/style.css`：HTML 样式表（CC0）。

### 说明

- 译文按“信、达、雅”直译为主，术语首次出现时给出英文原文；伪代码与代码片段不翻译关键字。
- 中文译文为 CC BY-SA 4.0 文本的演绎作品，沿用 CC BY-SA 4.0；媒体文件许可逐项见 `LICENSES.md`。

[1.0.0]: https://github.com/MarchBeta2087/plotting-mandel-zh-cn/releases/tag/v1.0.0
