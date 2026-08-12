# Generic Colorized IEEE Journal Quarto template

这是一个可直接编辑、渲染和发布到 GitHub 的 Quarto PDF 模板。IEEE 类文件、
样式与期刊标志统一封装在 extension 中，正文入口为 `template.qmd`。

## 使用方式

安装 Quarto、TeX Live（或 TinyTeX）后，在项目根目录运行：

```bash
quarto render template.qmd
```

PDF 会写入 `_output/`；为便于排错，Quarto 生成的 `template.tex` 会保留在
项目根目录，但已由 `.gitignore` 排除。

若该目录作为 GitHub 仓库发布，其他用户可运行：

```bash
quarto use template <GitHub用户名>/<仓库名>
quarto render template.qmd
```

## 目录结构

```text
.
├── template.qmd                  # 正文与作者信息入口
├── biographies.tex               # 参考文献之后的作者简介
├── _quarto.yml                   # Quarto 项目配置
├── _extensions/generic-color/    # 可安装的 PDF format
│   ├── _extension.yml
│   ├── preamble.tex
│   ├── ieeecolor.cls
│   ├── generic.sty
│   └── LOGO-generic-web.eps
├── data/references.bib           # BibTeX 文献库
├── image/                        # 正文图片与作者照片
└── README.md                     # 使用说明
```

## 编辑提示

- 标题、作者、单位、摘要和关键词位于 `template.qmd` 开头的原生 LaTeX 块；
  作者简介位于 `biographies.tex`。
- 普通章节、公式、图、表、交叉引用和文献引用使用 Quarto Markdown。
- `image/fig1.png` 是示例正文图；`image/a1.png` 至 `a3.png` 是作者照片。
- 期刊名、颜色和页眉标志由 `generic.sty` 控制。
- 投稿前请以目标期刊最新 author guidelines 为准；本仓库保留的是原始 2017
  示例类文件，不代表 IEEE 当前官方模板。
