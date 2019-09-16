# 1-0-latex

## 编译
使用 `XeLaTeX` 编译 `1-0-latex.tex` 文件。

如果遇到 "PDF 文件写入权限" 问题，
很可能是因为你使用的 PDF 阅读器不支持自动更新。

两种可能的解决方法：
- 仅使用编辑器内置的 PDF 阅读器打开 `1-0-latex.pdf`。
(如果你用其它阅读器打开了 `1-0-latex.pdf`，需要先关闭。)
- 使用 [Sumatra PDF](https://download.cnet.com/Sumatra-PDF/3000-18497_4-10698785.html) 阅读器。


## 目录结构
- `1-0-latex.tex`: 

  主文件 (main file)。一般来讲，在做作业的时候，你只需要修改、编译该文件。
- `1-0-latex.pdf`: 

  主文件编译后生成的 PDF 文件。也是你需要提交的文件。
- `hw-preamble.tex`: 

  这个文件主要用于导入包、定义命令、定义环境、定义格式等。
  主文件里导入 (`input`) 了该文件。

  如果你想自定义作业模板，可以修改该文件；否则，可以忽略该文件。
- `1-0-latex.tex.latexmain`: 空文件。

  仅对使用 Vim LatexSuite 插件的同学有用，如果不用 Vim 编辑器，可忽略该文件。

  它表示 `1-0-latex.tex` 是主文件。

  设置主文件的好处是，你不必在每次需要编译的时候，都要切换到 `1-0-latex.tex` 文件。
  同时也避免不小心编译了一个无法编译的非完全的 `.tex` 文件 (比如 `hw-preamble.tex`)，
  导致一堆编译错误。

  LaTeX 编辑器一般都有"设置某个文件为主文件"的功能，这个需要大家摸索一下。
- `tufte-book.cls`、`tufte-common.def`、`tufte-handout.cls`、`tufte-preamble.tex`:

  这是与 `tufte` 格式相关的文件。
  本作业模板是基于 `tufte-handout.cls` 
  (`tufte-book.cls` 是用来写书的，这里没有用到; `tufte-preamble.tex` 暂时也没有用到) 修改的。
  除非你清楚地知道自己在做什么，否则不要修改这些文件 (尤其是 `tufte-common.def` 与 `tufte-handout.cls`)。
