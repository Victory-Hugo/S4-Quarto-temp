# 重庆医科大学中文信函 Quarto 模板

这是一个基于 XeLaTeX 的一页式中文推荐信/申请信 Quarto 模板，包含校徽页眉、
联系信息、淡色水印、签名和日期。

## 渲染

安装 Quarto 与 TeX Live（或 TinyTeX）后运行：

```bash
quarto render template.qmd
```

生成的 PDF 位于 `_output/template.pdf`。为便于排错，Quarto 会在根目录保留
`template.tex`，但该文件已加入 `.gitignore`。

若本目录发布为 GitHub 仓库，其他用户可运行：

```bash
quarto use template <GitHub用户名>/<仓库名>
quarto render template.qmd
```

## 编辑位置

- `template.qmd`：收件人、称呼、正文和结束语。
- `letter-config.tex`：姓名、单位、地址、邮箱、电话、日期和签名。
- `assets/logo+文字.png`：页眉校名组合标志。
- `assets/logo.svg`：用户提供的矢量校徽源文件。
- `assets/logo-watermark.pdf`：由 `logo.svg` 生成的 7% 透明度水印。
- `assets/signature_block.pdf`：签名图片。
- `_extensions/cqmu-letter/`：Quarto PDF format 与 `CQMUletter.cls`。

## 目录结构

```text
.
├── template.qmd
├── letter-config.tex
├── _quarto.yml
├── _extensions/cqmu-letter/
│   ├── _extension.yml
│   ├── preamble.tex
│   └── CQMUletter.cls
├── assets/
│   ├── logo+文字.png
│   ├── logo.svg
│   ├── logo-watermark.pdf
│   └── signature_block.pdf
└── README.md
```
