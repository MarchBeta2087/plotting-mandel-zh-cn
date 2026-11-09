# Mandelbrot 集的绘制算法 · 中文译本

英文维基百科条目 **[Plotting algorithms for the Mandelbrot set](https://en.wikipedia.org/wiki/Plotting_algorithms_for_the_Mandelbrot_set)**（修订版本 `oldid=1380046103`，2026-10-13 抓取）的**非官方中文译本**。

仓库内容：

- 由原始 PDF 转换而来的 **Markdown 原文**（英文，公式为 LaTeX）
- **中文译文**（Markdown / HTML / PDF / Wikitext）
- 原文页面全部 **图片与视频** 的本地副本及**逐项许可证说明**（[LICENSES.md](LICENSES.md)）
- 使用 Pandoc 生成 PDF / HTML 的构建脚本来自另一仓库：[pandoc-md2pdf-md2html](https://github.com/MarchBeta2087/pandoc-md2pdf-md2html)（CC0）

| 文件 | 说明 |
|---|---|
| [plotting-algorithms-mandelbrot.zh-CN.md](plotting-algorithms-mandelbrot.zh-CN.md) | 中文译文（Markdown 源文件） |
| [plotting-algorithms-mandelbrot.zh-CN.html](plotting-algorithms-mandelbrot.zh-CN.html) | 中文译文（HTML，公式为 MathML） |
| [plotting-algorithms-mandelbrot.zh-CN.pdf](plotting-algorithms-mandelbrot.zh-CN.pdf) | 中文译文（PDF，XeLaTeX 排版） |
| [plotting-algorithms-mandelbrot.zh-CN.wiki](plotting-algorithms-mandelbrot.zh-CN.wiki) | 中文译文（Wikitext，沿用原条目的模板、图片、`<ref>` 与分类） |
| [plotting-algorithms-mandelbrot.en.md](plotting-algorithms-mandelbrot.en.md) | 英文原文（由 PDF 转出的 Markdown） |
| [source_en.txt](source_en.txt) | 英文维基百科条目原文（Wikitext 底稿，`oldid=1380046103`） |
| [plotting-algorithms-mandelbrot.en.html](plotting-algorithms-mandelbrot.en.html) | 英文原文（HTML） |
| [plotting-algorithms-mandelbrot.en.pdf](plotting-algorithms-mandelbrot.en.pdf) | 英文原文（PDF） |
| [LICENSES.md](LICENSES.md) | 所有图片 / 视频的许可证、作者与来源 |
| [CHANGELOG.md](CHANGELOG.md) | 变更日志 |
| [CONTRIBUTING.md](CONTRIBUTING.md) | 贡献指南：文件地图、术语表、校对与提交约定 |
| `.github/ISSUE_TEMPLATE/`、`.github/pull_request_template.md` | Issue / PR 模板 |
| [LICENSE](LICENSE) | 正文许可证全文（CC BY-SA 4.0） |
| `images/`、`videos/` | 原文页面的图片与视频（许可见 LICENSES.md） |
| `assets/style.css` | HTML 样式表（CC0） |
| `Original_PDF/` | 转换所用原始 PDF 与抓取说明 |

## 关于转换方式

1. 原始 PDF（`Original_PDF/Plotting_algorithms_for_the_Mandelbrot_set.pdf`，18 页，由 Chrome 打印维基百科页面生成）中的文字用 `pdftotext` / PyMuPDF 抽取，得到全文与版面坐标。
2. 由于 PDF 打印过程中公式被渲染为字形序列（无 LaTeX 源），为保证**公式与伪代码零失真**，转换时以该 PDF 所对应的维基百科修订版本 `oldid=1380046103` 的 wikitext 作为对照，将公式一一还原为 LaTeX、图片还原为原图文件引用。
3. 页面上的图片与视频改为引用 Commons 原始文件（`images/`、`videos/`），视频另附静帧封面，便于 PDF / 离线阅读。
4. 中文译文按“信、达、雅”原则直译为主，术语首次出现时给出英文原文；伪代码与代码片段保持原样（不翻译关键字）。
5. `plotting-algorithms-mandelbrot.zh-CN.wiki` 在同一份底稿上改写为 Wikitext：保留原条目的 `{{templates}}`、`[[File:...]]` 文件名、`<ref>` 参考文献与分类结构，只翻译可见文字，公式与伪代码逐字保留，便于与英文原条目逐段对照或移植到 MediaWiki。

## 重新构建 PDF / HTML

依赖：[Pandoc](https://pandoc.org/) ≥ 3.x、XeLaTeX（TeX Live / MiKTeX；构建 PDF 用）。

```bash
# 1) 取得构建脚本
git clone git@github.com:MarchBeta2087/pandoc-md2pdf-md2html.git
cd pandoc-md2pdf-md2html && chmod +x ./*.sh

# 2) 中文 PDF（中文需要 --cjk）
../pandoc-md2pdf-md2html/md2pdf.sh plotting-algorithms-mandelbrot.zh-CN.md \
    --cjk --toc --number-sections -o plotting-algorithms-mandelbrot.zh-CN.pdf \
    -- --shift-heading-level-by=-1

# 3) 中文 HTML（使用本仓库的样式表，资源保持外链，体积小）
../pandoc-md2pdf-md2html/md2html.sh plotting-algorithms-mandelbrot.zh-CN.md \
    --toc --number-sections --no-css --css=assets/style.css \
    -o plotting-algorithms-mandelbrot.zh-CN.html \
    -- --shift-heading-level-by=-1
```

> 注：源文件把标题写在 YAML 元数据里（`title`/`subtitle`），正文从二级标题开始，因此构建时用
> `--shift-heading-level-by=-1` 把章节提升一级，PDF 中的章节编号才会是 `1`、`1.1` 而不是 `0.1`。

PowerShell（Windows）：

```powershell
./pandoc-md2pdf-md2html/md2pdf.ps1  plotting-algorithms-mandelbrot.zh-CN.md -Cjk -Toc -NumberSections -Output plotting-algorithms-mandelbrot.zh-CN.pdf -ExtraArgs '--shift-heading-level-by=-1'
./pandoc-md2pdf-md2html/md2html.ps1 plotting-algorithms-mandelbrot.zh-CN.md -Toc -NumberSections -NoCss -Css assets/style.css -Output plotting-algorithms-mandelbrot.zh-CN.html -ExtraArgs '--shift-heading-level-by=-1'
```

## 参与贡献

欢迎勘误与人工校对：请先读 [CONTRIBUTING.md](CONTRIBUTING.md)（含术语表与“改哪个文件”的说明），
再按 Issue / PR 模板提交。译文与原文的对照底稿是 `source_en.txt`。

## 许可证

| 内容 | 许可证 |
|---|---|
| 原文正文（英文） | CC BY-SA 4.0，© Wikipedia 贡献者 |
| 本仓库中文译文 | **CC BY-SA 4.0**（译自 CC BY-SA 4.0 文本，属演绎作品，须沿用同一许可） |
| 图片 / 视频 | 各自许可，**逐项见 [LICENSES.md](LICENSES.md)**：公有领域 8、CC0 6、CC BY-SA 4.0 12、CC BY-SA 3.0 1、Commons 署名许可 2 |
| `assets/style.css`、构建脚本 | CC0 1.0（公有领域贡献） |

转载或再发布时，请保留本 README、[LICENSES.md](LICENSES.md) 中的署名信息，并遵守 CC BY-SA 的“相同方式共享”条款。

## 免责声明

本项目为非官方翻译，与维基媒体基金会无关；译文中若有不准确之处，以[英文原文](https://en.wikipedia.org/wiki/Plotting_algorithms_for_the_Mandelbrot_set)为准。
