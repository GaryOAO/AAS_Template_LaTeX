# 《自动化学报》LaTeX模板

这是一个模块化的《自动化学报》LaTeX模板，基于[Passer-montanus/AAS_Template_LaTeX](https://github.com/Passer-montanus/AAS_Template_LaTeX)进行了结构化调整。

## 文件结构

- `main.tex`: 主文件，用于设置文档的整体结构和包含其他部分。
- `sections/`: 存放各个章节的文件夹。
  - `introduction.tex`: 引言部分。
  - `methods.tex`: 方法或模型部分。
  - `conclusion.tex`: 结论部分。
- `Image/`: 存放图片文件的文件夹。
- `refs.bib`: BibTeX参考文献数据库。
- `aas.cls`: 《自动化学报》的LaTeX class文件。
- `picins.sty`: 用于图文混排的宏包。

## 如何使用

1.  **安装LaTeX发行版**

    确保你的电脑上已经安装了LaTeX发行版，例如[TeX Live](https://www.tug.org/texlive/)、[MiKTeX](https://miktex.org/)或[MacTeX](https://www.tug.org/mactex/)。

2.  **克隆仓库**

    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

3.  **编辑内容**

    -   在`main.tex`中修改标题、作者、摘要等信息。
    -   在`sections/`目录下的相应文件中撰写正文内容。
    -   将图片文件（如`.png`, `.jpg`, `.eps`等）放入`Image/`目录，并在`.tex`文件中使用相对路径引用，例如`\includegraphics[width=0.8\textwidth]{Image/figure1.png}`。
    -   在`refs.bib`文件中添加BibTeX格式的参考文献条目。

4.  **编译**

    推荐使用`xelatex`进行编译，以支持中文显示。完整的编译过程如下：

    ```bash
    xelatex main.tex
    bibtex main
    xelatex main.tex
    xelatex main.tex
    ```

    编译完成后，会生成`main.pdf`文件。

## 注意事项

-   请确保你的LaTeX发行版中包含`ctex`宏包，以便正确显示中文。
-   如果需要添加或删除章节，可以在`main.tex`中通过`\input{sections/new_section.tex}`来添加新的章节文件，或者注释掉/删除相应的`\input`命令。
-   参考文献的引用格式为`\cite{citation_key}`，其中`citation_key`对应`refs.bib`文件中的条目-key。

