# code_art_1

Quarto GitHub 模板仓库（`format_extension` 模式）。

## 使用方式

```bash
quarto use template <github_owner>/code_art_1
```

生成项目后可直接渲染：

```bash
quarto render template.qmd
```

## 仓库结构

```text
.
├── template.qmd
├── .quartoignore
└── _extensions
    └── code-art-1
        └── _extension.yml
```

## 自定义格式名

`template.qmd` 使用格式：

```yaml
format: code-art-1-pdf
```
