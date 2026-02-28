# Quarto 模板 1

这是一个可通过 `quarto use template` 安装的中文 XeLaTeX 预印本模板。

## 使用方法

```bash
quarto use template Victory-Hugo/S4-Quarto-temp
```

执行后会在当前目录生成一个新的 `.qmd` 文件（来自 `template.qmd`），并自动拉取模板依赖的 `_extensions/quarto-template1`。

## 渲染

```bash
quarto render <你的文件名>.qmd --to quarto-template1-pdf
```

## 目录结构

- `template.qmd`: 模板正文
- `_extensions/quarto-template1/_extension.yml`: 格式定义
- `_extensions/quarto-template1/preamble.tex`: LaTeX 样式
- `example.bib`: 参考文献示例
