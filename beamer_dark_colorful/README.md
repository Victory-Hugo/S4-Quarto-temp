# 群体遗传学（mtDNA / chrY）幻灯片模板

深紫霓虹风 Beamer 模板。**只改 `main.tex` 的内容，版式都在 `theme.tex`。**

## 文件结构

| 文件 | 作用 |
|---|---|
| `main.tex` | 幻灯片内容（日常只改这个） |
| `theme.tex` | 配色、页脚进度条、组件宏（一般不用动） |
| `image/` | 图片目录，在 `\PicLeft` 里直接写文件名 |

## 编译

```bash
xelatex main.tex && xelatex main.tex   # 两遍：生成页码和进度条
```

字体由 ctex 按系统自动选择（Windows / macOS / Linux 均可）。

## 常用改法

1. **基本信息**：改 `main.tex` 开头的 `\title` `\author` `\institute` `\date`，以及封面、结语页里的文字。
2. **新增左图右文页**：复制下面这段，换图、换文字：

   ```latex
   \begin{frame}{标题}{副标题}
     \Badge{pink}{pinkL}{小标签}

     \PicLeft{1.png}{图 1 · 图注}{
       \Point{pinkL}{要点标题}{一两句解读}
       \Point{blueL}{要点标题}{一两句解读}
       \Point{goldL}{要点标题}{一两句解读}
     }
   \end{frame}
   ```

   - 想图在右、文在左：把 `\PicLeft` 换成 `\PicRight`，参数不变。
   - 每页 **3–4 个 `\Point`**，每条说明控制在一两行，否则会溢出页面。
3. **换图**：把图放进 `image/`，改 `\PicLeft{文件名}{图注}{...}` 的第一个参数。图片按比例自动缩放，宽图（16:9）效果最好。
4. **其他版式**（都在 `main.tex` 里有示例，复制后改字即可）：
   - 三栏卡片：`card` 环境（见第 2 页）
   - 左右对比：`cardc{颜色}` 环境（第 3 页）
   - 流程步骤：`\stepnode` / `\stepnodeH`（高亮）（分析流程页）
   - 底部提示条：`\notebox{描边色}{文字色}{内容}`
5. **颜色名**：`pinkL` `violetL` `blueL` `cyanL` `goldL` `greenL` `redL`。想整体换配色，改 `theme.tex` 中「主题色板」的 HTML 色值。
6. **页面太满**：给该页加 `[shrink=6]`（如 `\begin{frame}[shrink=6]{...}{...}`），数字越大缩得越多。

## 注意

- 示例中的数值（突变率、基因组大小等）和文字只是**占位**，使用前请按自己的数据和文献核对。
- `image/` 里的占位图已压缩到长边 1600 px；正式用图建议同样压缩，避免 PDF 过大、编译变慢。
