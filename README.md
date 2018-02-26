搭建步骤参考文章[使用 Pandoc Markdown 进行学术论文写作](http://www.zale.site/articles/2016/05/Academia-Writing-Using-Markdown-and-Pandoc.html#quick-start-demo)

致谢博主

### 编译指令

```
pandoc --filter pandoc-citeproc --biblio reference.bib --pdf-engine=xelatex  --csl chinese-gb7714-2005-numeric.csl  --template=template.tex test1.md -s -o test1.pdf
```


```
pandoc --filter pandoc-citeproc --biblio reference.bib --pdf-engine=xelatex  --csl chinese-gb7714-2005-numeric.csl  --template=template.tex main.md -s -o main.docx
```

### 可能出现的问题

* 中文乱码问题

按照pandoc 官方文档安装最终会出现中文乱码的问题。首先要注意使用`--latex-engine=xelatex `, 其次在模板文件中要定义中文字的字体，要注意字体一定是系统中已经安装的。

最简便的方法是直接使用网友整理好的模板文件，本仓库中的模板文件经测试是可以兼容中文的。

