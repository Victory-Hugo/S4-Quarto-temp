# Quarto Templates Collection

这个仓库用于托管多个 Quarto 模板。每个模板放在独立子目录中。

## 可用模板

- `ctexart_1`: 中文 XeLaTeX 预印本模板

## 使用方法

```bash
quarto use template Victory-Hugo/S4-Quarto-temp/ctexart_1
quarto use template Victory-Hugo/S4-Quarto-temp/cbook_1
```

生成后可渲染：

```bash
quarto render <你的文件名>.qmd --to pdf
```
