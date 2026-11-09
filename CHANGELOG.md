# 更新日志

本文件记录本仓库（Mandelbrot 集绘制算法中文译本）的所有重要变更。

格式参考 [Keep a Changelog](https://keepachangelog.com/zh-CN/1.1.0/)，
版本号遵循 [语义化版本](https://semver.org/lang/zh-CN/)。

## [未发布]

### 新增

- `plotting-algorithms-mandelbrot.zh-CN.wiki`：中文 **Wikitext** 译本。以英文维基百科条目
  `Plotting algorithms for the Mandelbrot set`（`oldid=1380046103`）的 Wikitext 为蓝本，
  沿用原条目的模板、图片文件名、`<ref>` 参考文献与分类结构，仅将可见文字译为中文；
  LaTeX 公式与伪代码保持原样（118 处 `<math>`、21 条参考文献、20 处图片引用与原条目一一对应）。
- `source_en.txt`：上述英文条目的 Wikitext 原文，作为译本的对照底稿一并入库。
- `CHANGELOG.md`：本文件。

### 变更

- `README.md`：新增 Wikitext 译本与英文 Wikitext 底稿的文件说明。

## [0.2.0] - 2026-11-08

### 修复

- 章节编号：将条目标题移入 YAML 元数据（`title` / `subtitle`），正文从二级标题开始，
  构建时使用 `--shift-heading-level-by=-1` 提升标题层级，使 PDF / HTML 中的章节编号
  从 `1`、`1.1` 起而非 `0.1` 起。
- 随之重新生成 `plotting-algorithms-mandelbrot.zh-CN.html` / `.pdf`。

## [0.1.0] - 2026-11-08

### 新增

- Mandelbrot 集绘制算法中文译本：
  - `plotting-algorithms-mandelbrot.zh-CN.md`（Markdown 源文件，公式为 LaTeX）
  - `plotting-algorithms-mandelbrot.zh-CN.html`（HTML，公式为 MathML）
  - `plotting-algorithms-mandelbrot.zh-CN.pdf`（PDF，XeLaTeX 排版）
- 英文原文（由原始 PDF 转出的 Markdown / HTML / PDF）：
  `plotting-algorithms-mandelbrot.en.md` / `.html` / `.pdf`
- `LICENSES.md`：原文页面全部图片与视频的许可证、作者及来源逐项清单。
- `LICENSE`：正文许可证全文（CC BY-SA 4.0）。
- `images/`、`videos/`：原文页面图片与视频的本地副本（含视频静帧封面）。
- `assets/style.css`：HTML 样式表（CC0）。
- `Original_PDF/`：转换所用原始 PDF 与抓取说明。
- `README.md`：仓库说明、转换方式、重新构建 PDF / HTML 的步骤与许可证汇总。

[未发布]: https://github.com/MarchBeta2087/plotting-mandel-zh-cn/compare/v0.2.0...HEAD
[0.2.0]: https://github.com/MarchBeta2087/plotting-mandel-zh-cn/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/MarchBeta2087/plotting-mandel-zh-cn/releases/tag/v0.1.0
