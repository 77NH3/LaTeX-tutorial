# LaTeX Tutorial 闪击拉泰克

This is a lecture note prepared for the $\LaTeX$ crash course in 2502 sem by Ethan Quanrun Wu(武一石) in the Academic Team, Physics Society, XMUM. The spirit of this tutorial class is to let everyone learn the essential knowledge that could help physics freshman use $\LaTeX$ in everyone's daily life. Also, I will introduce my personal suggestions and my workflow as a reference.

## 1. LaTeX简介 / Introduction to LaTeX  
### LaTeX 的特点与应用场景 *Features and use cases of LaTeX*  

What is $\LaTeX$? **LaTeX** ([/ˈlɑːtɛk/](https://en.wikipedia.org/wiki/Help:IPA/English) [ⓘ](https://en.wikipedia.org/wiki/File:En-us-LaTeX.ogg)[*LAH-tek*](https://en.wikipedia.org/wiki/Help:Pronunciation_respelling_key) or [/ˈleɪtɛk/](https://en.wikipedia.org/wiki/Help:IPA/English) [*LAY-tek*](https://en.wikipedia.org/wiki/Help:Pronunciation_respelling_key), often stylized as $\LaTeX$) is a software system for typesetting documents and publications. 

It could easily produce high-quality, professional-looking documents. 

It is powerful in writing complex math expressions and is widely used in academia for documents. It supplies the most widely accepted method for typing math math expressions, which is employed by Microsoft word, markdown, 知乎, etc.

Also, it has a vast ecosystem to extend its functionality.

When we are using $\LaTeX$, we write code, use an compiler to generate a PDF file, and then modify the code if necessary

### 实际案例展示（论文、报告、幻灯片等排版效果）  *Show case of practical examples (e.g., academic papers, reports, slides)*  

LaTeX can be used to generate professional-looking papers and reports,  and a type of slides that is useful for academia called *beamer*. It is required by the famous preprint platform [arXiv](https://arxiv.org/) to submit the original TeX file of your paper.

You may also use LaTeX to write your CV if you have to.

Another famous advanced application is to use it is provided by the educational youtuber *3 Blue 1 Brown* ([example](https://www.bilibili.com/video/BV1ys411472E/?spm_id_from=333.1387.homepage.video_card.click&vd_source=d929d65742059d71741b3cc0254da11f)). You guys may have watched his video for your study of linear algebra. The formula part of his video is supported by LaTeX.

### 为什么选择 LaTeX（对比 Word 或其他工具的优劣）  *Why choose LaTeX? (Comparison with Word and other tools)*  

Then a natural question is: why do we choose $\LaTeX$? The most commonly used text editing software is no doubt Microsoft Word and its equivalents, like Google Docs and WPS Writer. They are obviously easier to use, and more generally accepted (you should not expect to show off your LaTeX skills in a common company). 

| Feature                      | Microsoft Word, Google Docs, WPS Writer      | LaTeX                                                        |
| ---------------------------- | -------------------------------------------- | ------------------------------------------------------------ |
| **Ease of Use**              | User-friendly interface                      | Steeper learning curve                                       |
| **Editing Mode**             | WYSIWYG “所见即所得”                         | Code-based                                                   |
| **Collaboration**            | Real-time collaboration (Google Docs excels) | Not generally available, but accessible via platforms like Overleaf |
| **Document Format**          | `.docx`, `.pdf`                              | Primarily `.pdf`                                             |
| **Mathematical Expressions** | Basic support                                | Superior support for complex equations                       |
| **Templates and Formatting** | Wide range of templates                      | Highly customizable with package                             |
| **Floating Figures and Tables** | Managed automatically                                        | Managed with precise control                 |
| **Bibliography Management**     | Supported with plugins                                       | Integrated with BibTeX and BibLaTeX          |
| **Output Quality**              | High-quality documents                                       | Professional-grade typesetting               |
| **Customization**               | Limited customization                                        | Extensive customization through packages     |
| **Integration**                 | Integrates with Microsoft Office suite, Google ecosystem, and WPS Office suite | Limited integration, requires external tools |
| **Learning Curve**              | Smooth                                       | Challenging                             |

The sheet above shows a detailed comparison between Word and its equivalents with LaTeX. But in practice, the reasons we choose LaTeX are simple: its formula-typing is irreplaceable, commonly LaTeX is your only way to type a complex formula; it is widely accepted in academia. Some lecturers would recommend you to submit your report with LaTeX, you could use it for your final year thesis. A more important personal reason is, it could help you to write in the same professional way of the textbooks and papers you've been reading.

Also, we should note that there are significant drawbacks of LaTeX in the 

Also, recently, we get an ambitious new challenger [Typst](https://typst.app/). It has easier syntax, supports real-time collaboration, has "understandable error feedback", and is determined to replace LaTeX. However, as a new comer, Typst's community is still developing and does not have the sufficient extensive packages like LaTeX. If you've had enough of LaTeX, you might try to play with Typst and keep up with its development.

## 2. 如何建立一个 LaTeX 工程 / Setting Up a LaTeX Project  
### 本地安装与配置（进阶）*Local installation and setup (Advanced)*  

It is a private and extensive way to set up an environment for LaTeX in your PC. The core of LaTeX is in the distributes of TeX, like MikTeX and TeXLive. With this installed, we need some software to assist you to edit your project, called IDE(Integrated Development Environment，集成开发环境). The most commonly used one is to use **VS code**. It supports many programming languages. My personal receipt is VS code + MikTeX + LaTeX workshop(a VS code plugin). You may use the links [to be added] as a reference if you are hardcore.

Advantages: 

private, extensive, offline supported, allows multi-person collaborative work

Disadvantages:

Troublesome to set up (especially for beginners), very difficult to debug

### 在线编辑工具（推荐 Overleaf，步骤演示）  *Online editing tools (recommend Overleaf, step-by-step demo)*  

My personal recommendation, after these semesters, is to use the online platform, [**Overleaf**](https://overleaf.com/). By this you could easily create a basic document.

### 快速创建一个简单文档（如生成带标题、段落和公式的文档）  *Quickly creating a basic document (e.g., a title page with paragraphs and equations)*  

Click **New Project**. Click **Example Project**, then you can see a complete example of a LaTeX project, which includes all the daily used features including common contents, math expression, table, picture and reference.

To demonstrate it more clearly, I will use a new blank file.



## 3. 常用功能 / Commonly Used Features  

### 段落 *Paragraphs*

You could use common texts between the ```\begin{document}``` and ```\end{document}```. To break a line you have two methods, the first is to break two or more times.

The other is to use ```\\```  

```latex
This is the first line. \\
This is the second line.
```

This is called forced line break. If you want to break more than one time you can use this

To include a paragraph you need 

```latex
\section{}
\subsection{}
\subsubsection{}
\paragraph{}
```

You can insert content everywhere in between them. Note the effect of the line breaking. 

### 图片排版（使用 `graphicx`）  *Image placement (using `graphicx`)*  

To include an graph, we need to first upload the file to Overleaf, then we need the following commands:

```latex
\paragraph{Include a picture}
\begin{figure}[htbp!]
    \centering
    \includegraphics[width=0.5\linewidth]{example.jpg}
    \caption{Caption}
    \label{fig:enter-label}
\end{figure}
```

Where h means "here", t means "top", b means "bottom", page means 

### 表格（使用 `tabular`）  *Tables (using `tabular` )*  

It is a little bit of hard to include a table in LaTeX. To include it, we need  the code

```latex
\begin{table}[htpb!]
  \centering
  \begin{tabular}{|c|c|c|}
    \hline
    Quantity & Symbol & Value \\ \hline
    Speed of light & \(c\) & \(3 \times 10^8 \, \text{m/s}\) \\ \hline
    Gravitational constant & \(G\) & \(6.674 \times 10^{-11} \, \text{m}^3\text{kg}^{-1}\text{s}^{-2}\) \\ \hline
    Planck's constant & \(h\) & \(6.626 \times 10^{-34} \, \text{Js}\) \\ \hline
  \end{tabular}
  \caption{Fundamental Physical Constants}
  \label{tab:constants}
\end{table}
```

where we use `&` to open a new column, use `\\`to open a new row. we use `{|c|c|c|}` is used to show the table has 3 columns with 4 vertical lines, `\hline` is used to draw a horizontal. 

Although this is troublesome to directly write a table, it is commonly easy to paste a table into latex with some tools line [Create LaTeX tables online – TablesGenerator.com](https://www.tablesgenerator.com/). There are also some Excel plugins to generate the LaTeX code of a form.

### 引用与参考文献  *Citations and references:*  

- 文献管理工具介绍（如 BibTeX 或 `biblatex` 的基础用法）  
  *Introduction to bibliography management tools (e.g., BibTeX or `biblatex`)*
  
  There are several ways of doing references in LaTeX. Here we use BibTeX. We create a new `.bib`file in Overleaf, and then add the BibTeX information of your reference into that. BibTeX information could be found in [Google Scholar](https://scholar.google.com/), or you could create your own reference following the rules of it, when you are citing non-published references like a bachelor thesis. You could add `\cite{citation key}` in the body where you want to do the citation. Then you can add 
  
  ```latex
  \bibliographystyle{plain}
  \bibliography{references}
  ```
  
  to include the reference list. Note that BibTeX has a poor support on Chinese references.

## 4. 数学功能介绍 / Introduction to Mathematical Functions  
### 数学公式的环境与语法  *Mathematical environments and syntax:*  

To include a math expression you could use```$(math)$``` to insert an inline formula, and ```$$(math)$$``` or

```latex
\begin{equation}
E = mc^2
\end{equation}
```

to do it. Using the equation environment will use automatic equation numbering.  By adding an ```\label{eq:this is a label}```, you can refer to the equation when you use the command ```\ref{eq:this is a label}```. We recommend using the formula environment when writing a paper.

To get a formula of the form

$$\begin{aligned}a+b = c\\a+c = d\end{aligned}$$

you should use 

```latex
\begin{align}
	formula11&formula12\\
	formula21&formula22
\end{align}
```

Using the package `amsmath`

### 矩阵排版 *Matrix Formatting*

To include a matrix, you need to use the package `amsmath`. Then use `\begin{matrix} ... \end{matrix}` with `&` for column separation and `\\` for row separation.

```latex
\[
\begin{matrix}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{matrix}
\]
```

There are also other environments provide different brackets:

- `bmatrix`: Brackets `[ ]`
- `pmatrix`: Parentheses `( )`
- `Bmatrix`: Curly braces `{ }`
- `vmatrix`: Vertical bars `| |`
- `Vmatrix`: Double vertical bars `‖ ‖`

Then we will introduce the symbols in LaTeX

### 常用数学符号  *Common mathematical symbols*

#### Basic Math Notation in LaTeX

| **Symbol/Operation**     | **LaTeX Command** | **Example Usage**      | **Example Output**     |
| ------------------------ | ----------------- | ---------------------- | ---------------------- |
| **Fraction**             | `\frac{num}{den}` | `\frac{a}{b}`          | $\frac{a}{b}$          |
| **Superscript**          | `^{}`             | `x^{2}`                | $x^{2}$                |
| **Subscript**            | `_{}`             | `x_{1}`                | $x_{1}$                |
| **Square Root**          | `\sqrt{}`         | `\sqrt{x}`             | $\sqrt{x}$             |
| **n-th Root**            | `\sqrt[n]{}`      | `\sqrt[3]{x}`          | $\sqrt[3]{x}$          |
| **Summation**            | `\sum`            | `\sum_{i=1}^{n} x_i`   | $\sum_{i=1}^{n} x_i$   |
| **Product**              | `\prod`           | `\prod_{i=1}^{n} x_i`  | $\prod_{i=1}^{n} x_i$  |
| **Integral**             | `\int`            | `\int_{a}^{b} f(x) dx` | $\int_{a}^{b} f(x) dx$ |
| **Limit**                | `\lim`            | `\lim_{x \to \infty}`  | $\lim_{x \to \infty}$  |
| **Binomial Coefficient** | `\binom{n}{k}`    | `\binom{n}{k}`         | $\binom{n}{k}$         |
| **Exponential Function** | `e^{x}`           | `e^{x}`                | $e^{x}$                |

#### Basic Math Symbols
| Symbol | LaTeX Command     | Markdown Usage          |
|--------|-------------------|-------------------------|
| +      | `+`               | `$a + b$`               |
| −      | `-`               | `$c - d$`               |
| ×      | `\times`          | `$e \times f$`          |
| ÷      | `\div`            | `$g \div h$`            |
| ±      | `\pm`             | `$\alpha \pm \beta$`    |
| ∓      | `\mp`             | `$\gamma \mp \delta$`   |

**Example Code:**

```latex
$a + b$, $c - d$, $e \times f$, $g \div h$, $\alpha \pm \beta$, $\gamma \mp \delta$
```

#### Greek Letters

| Lowercase | Uppercase | LaTeX Command  |
| :-------- | :-------- | :------------- |
| α         | Α         | \alpha, \Alpha |
| β         | Β         | \beta, \Beta   |
| γ         | Γ         | \gamma, \Gamma |
| δ         | Δ         | \delta, \Delta |

**Example Code:**

```latex
$\alpha$, $\Beta$, $\Gamma$, $\delta$
```

#### Special Characters

| Character | LaTeX Command     | Markdown Usage      |
| :-------- | :---------------- | :------------------ |
| <         | < or \textless    | $<$ or \textless    |
| >         | > or \textgreater | $>$ or \textgreater |
| &         | \&                | \&                  |
| #         | \#                | \#                  |
| %         | \%                | \%                  |
| {         | \{                | \{                  |
| }         | \}                | \}                  |

**Example Code:**

```latex
Less than: `<` or `$<$`
- Hash: `\#`
- Curly braces: `\{ \}`
```

#### Mathematical Relations

| Symbol | LaTeX Command | Markdown Usage |
| :----- | :------------ | :------------- |
| =      | =             | $x = y$        |
| ≠      | \neq          | $x \neq z$     |
| ≤      | \leq          | $y \leq w$     |
| ≥      | \geq          | $w \geq v$     |
| ≈      | \approx       | $u \approx t$  |
| ∈      | \in           | $p \in o$      |

**Example Code:**

```latex
$x = y$, $x \neq z$, $y \leq w$, $w \geq v$, $u \approx t$, $p \in o$
```

#### Automatic Sizing with `\left` and `\right`
```latex
\left( x + y \right)
\left\{ x + y \right\}
\left| x + y \right|
```

#### Mathematical Operators

| **Symbol** | **LaTeX Command** | **Markdown Usage** |
| :--------- | :---------------- | :----------------- |
| $\ln$      | `\ln`             | `\ln`              |
| $\log⁡$     | `\log`            | `\log`             |
| $\sin$⁡     | `\sin`            | `\sin`             |
| $\cos⁡$     | `\cos`            | `\cos`             |
| $\tan⁡$     | `\tan`            | `\tan`             |
| $\arcsin⁡$  | `\arcsin`         | `\arcsin`          |
| $\arccos⁡$  | `\arccos`         | `\arccos`          |
| $\arctan⁡$  | `\arctan`         | `\arctan`          |
| $\sinh⁡$    | `\sinh`           | `\sinh`            |
| $\cosh⁡$    | `\cosh`           | `\cosh`            |
| $\tanh⁡$    | `\tanh`           | `\tanh`            |
| $\exp⁡$     | `\exp`            | `\exp`             |
| $\lim$     | `\lim`            | `\lim`             |
| $\max$     | `\max`            | `\max`             |
| $\min⁡$     | `\min`            | `\min`             |
| $\sup⁡$     | `\sup`            | `\sup`             |
| $\inf⁡$     | `\inf`            | `\inf`             |
| $\arg⁡$     | `\arg`            | `\arg`             |
| $\det⁡$     | `\det`            | `\det`             |
| $\gcd⁡$     | `\gcd`            | `\gcd`             |
| $\deg$     | `\deg`            | `\deg`             |
| $\dim⁡$     | `\dim`            | `\dim`             |
| $\hom⁡$     | `\hom`            | `\hom`             |
| $\ker⁡$     | `\ker`            | `\ker`             |
| $\Pr⁡$      | `\Pr`             | `\Pr`              |
| $\tr$      | `\tr`             | `\tr`              |

#### 数学注音 *Mathematical Accents*


| **Symbol**         | **LaTeX Command** | **Example Output** |
| :--------- | :---------------- | :----------------- |
| **Hat** (Accent)   | `\hat{}`          | $\hat{x}$          |
| **Bar** (Overline) | `\bar{}`          | $\bar{x}$          |
| **Tilde**          | `\tilde{}`        | $\tilde{x}$        |
| **Vector**         | `\vec{}`          | $\vec{x}$          |
| **Dot**            | `\dot{}`          | $\dot{x}$          |
| **Double Dot**     | `\ddot{}`         | $\ddot{x}$         |
| **Overline**       | `\overline{}`     | $\overline{x}$     |
| **Underline**      | `\underline{}`    | $\underline{x}$    |
| **Overbrace**      | `\overbrace{}`    | $\overbrace{x}$    |
| **Underbrace**     | `\underbrace{}`   | $\underbrace{x}$   |
| **Acute Accent**   | `\acute{}`        | $\acute{x}$        |
| **Grave Accent**   | `\grave{}`        | $\grave{x}$        |
| **Check**          | `\check{}`        | $\check{x}$        |
| **Breve**          | `\breve{}`        | $\breve{x}$        |
| **Mathring**       | `\mathring{}`     | $\mathring{x}$     |
| **Wide Hat**       | `\widehat{}`      | $\widehat{x}$      |
| **Wide Tilde**     | `\widetilde{}`    | $\widetilde{xyz}$ |

### 结合具体例子进行应用  *Practical examples and applications*  

You might provide any equation you like for me as and example to demonstrate. The best way to practice it is to type whatever you see.

## 5. 常用 package 介绍 / Overview of Common Packages  
- 排版辅助：`geometry`、`graphicx`、`xcolor`  
  *Formatting: `geometry`, `graphicx`, `xcolor`*  
- 数学支持：`amsmath`、`amssymb`  
  *Mathematics: `amsmath`, `amssymb`*  
- 文献与超链接：`biblatex`、`hyperref`  
  *Citations and hyperlinks: `biblatex`, `hyperref`*  
- 模板与其他扩展：如 Beamer、`multicol` 等  
  *Advanced use cases: Beamer, `multicol`, etc.*  

## 6. 其他常用格式 / Other Common Formats  
- 页面布局设置（如页边距、页眉页脚）  
  *Page layout settings (e.g., margins, headers, and footers)*  
  
- 多栏排版和分章节结构  
  *Multi-column formatting and structuring chapters*  
  
- 自定义命令与宏  
  *Custom commands and macros*  

## 7. 我的工作流/My Work Flow

Here I want to introduce a **lightweight markup language**, or more simply markdown. This can be treated as lightweight software. It basically only has, The compiler is integrated into VS code.  It uses the same set of syntax of math expressions of LaTeX, and abandons its tedious code. It is also a good tool to take notes when the formula is not too complex(such as math texts. Some physics is too hard for it) 

Commonly, I will use markdown to setup my paper, and transform it into LaTeX by pasting the formula or via tools like [Pandoc](https://pandoc.org/). Then, if I need to do a presentation, I will change the file type to beamer, which shares the advantage that it supports LaTeX recently. To change the file type with Pandoc, you could open the command in the folder and use the code

``` sh
pandoc -s input.md -o optput.tex
```

This will provide a standalone TeX file in the current folder. Based on my own painful experience, I recommend using different file names for the input and output files.

The essence of my LaTeX life and : *\include{\physics}*([link](http://mirrors.ctan.org/macros/latex/contrib/physics/physics.pdf)). It simplifies the code of many useful notations in and beyond physics, $\dv{a}{t}$, $\vb{v}$, $\pdv{U}{x}$, $\dv{a}$, $\pdv{a}$,$\bra{a}$, $\ket{b}$, $\braket{z}{a}$. 

## 8. 后续学习途径 / Further Learning Resources  

As this is an really brief introduction, I cannot and do not intend to tell you all the features of LaTeX. The right way to use it is to learn it when you need it after you've learned all the basic setup.

- 推荐资源与工具：  *Recommended resources and tools:*  
  
  - 官方文档、在线速查表、模板库  
    *Official documentation, online cheatsheets, template repositories*  
    
    Package List: [CTAN: Packages](https://ctan.org/pkg)
    
    
  
- 进阶应用：  *Advanced applications:*  
  - 幻灯片（Beamer）、专业排版（如报告、书籍）、manim、 
    *Slides (Beamer), professional layouts (e.g., reports, books)*, manim[【Manim_4】ManimCE的安装与在线使用_哔哩哔哩_bilibili](https://www.bilibili.com/video/BV18S4y1r73H?spm_id_from=333.788.videopod.sections&vd_source=d929d65742059d71741b3cc0254da11f)
  
- LaTeX 社区与论坛资源  *Community and forums for LaTeX support*
  
  Stack Exchange  [TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/)
  
  ChatGPT / DeepSeek
  
  知乎



[https://overleaf.com/]: 
