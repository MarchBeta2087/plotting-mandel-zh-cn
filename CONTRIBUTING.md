# 贡献指南

本仓库是英文维基百科条目 [Plotting algorithms for the Mandelbrot set](https://en.wikipedia.org/wiki/Plotting_algorithms_for_the_Mandelbrot_set)
（`oldid=1380046103`）的**非官方中文译本**。欢迎提交勘误、人工校对、术语统一、构建修复等改动。

## 文件地图：改哪个文件

| 文件 | 角色 | 可否手改 |
|---|---|---|
| `source_en.txt` | 英文 Wikitext 底稿，**唯一权威原文** | ❌ 只作对照 |
| `plotting-algorithms-mandelbrot.zh-CN.md` | 中文 Markdown 源文件（HTML/PDF 的生成源） | ✅ 主要改这里 |
| `plotting-algorithms-mandelbrot.zh-CN.wiki` | 中文 Wikitext 译本（用于对照原条目 / 移植到 MediaWiki） | ✅ |
| `.zh-CN.html` / `.zh-CN.pdf`、`.en.*` | 构建产物 | ❌ 改 `.md` 后重新生成 |
| `LICENSES.md` | 图片 / 视频的许可证与作者 | ✅ 增删媒体时同步 |
| `CHANGELOG.md` | 变更日志 | ✅ 用户可见的改动请补一条 |

> `.md` 与 `.wiki` 是同一份译文的两种标记：改译文时**两处都要改**，否则两份会漂移。

## 校对与翻译约定

1. **对照 `source_en.txt` 逐段核对**，不要只读中文。落笔前确认原文段落、列表层级、脚注编号。
2. **公式（LaTeX / `<math>`）与伪代码一字不改**，包括变量名、关键字、注释与缩进。只翻译公式两侧的说明文字。
3. **术语统一**（首次出现时给出英文原文）：

   | 英文 | 本仓库译法 |
   |---|---|
   | Mandelbrot set | 曼德尔布罗集（正文标题沿用 “Mandelbrot 集”） |
   | escape time / bailout | 逃逸时间 / 逃逸判据（跳出） |
   | normal / normalized iteration count | 归一化迭代次数 |
   | potential function | 势函数 |
   | cardioid / period-2 bulb | 心形线 / 二阶周期球 |
   | lemniscate | 双纽线 |
   | distance estimation | 距离估计 |
   | perturbation theory / series approximation | 摄动理论 / 级数近似 |
   | interior、exterior、boundary | 内部、外部、边界 |

4. **行文**：直译优先，通顺其次，不增删原意；避免机翻腔；中文标点用全角，数字与英文术语两侧留空格（如 `500 次迭代`）。
5. **链接与图片**：保留原文件名与链接目标；图注中的作者与许可证信息不要删。
6. **参考文献**：条目名、作者、URL、日期保持原文，不翻译文献标题。

## 提交改动

```bash
git switch -c fix/terminology-xxx      # 分支名：fix/、docs/、chore/ + 简短说明
# 修改文件
git commit -m "docs: 统一 '势函数' 译法"
git push -u origin fix/terminology-xxx
```

- 提交信息格式：`类型: 简述`，类型取 `docs`（译文/文档）、`fix`（错误修正）、`chore`（构建、杂务）。
- 一次提交只做一类改动；纯排版修正与译文修正分开。
- 改动了 `.md` 就请重新生成 HTML / PDF（步骤见 [README](README.md)），或在 PR 中说明未重建。
- 新增或替换图片 / 视频时，**必须**在 `LICENSES.md` 补上作者、来源与许可证。

## 提 Issue 还是直接 PR？

- **直接 PR**：错别字、术语不一致、漏译、格式与构建修复。
- **先开 Issue**：涉及译法取舍、是否保留某段、术语表调整等需要讨论的改动；或用「译文问题」模板指出具体段落。
- 不确定原文某句含义时，在 PR 里贴出英文原句并说明你的理解，方便 reviewer 判断。

## 许可证

投稿即表示你同意以 **CC BY-SA 4.0** 发布你的贡献（与原文及本译文一致）。请勿引入版权不明的内容。
