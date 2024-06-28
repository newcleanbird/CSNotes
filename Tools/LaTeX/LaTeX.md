# LaTeX

## LaTeX简介

### TeX 格式

最基本的 TeX 程序只是由一些很原始的命令组成，它们可以完成简单的排版操作和程序设计功能。然而，TeX 也允许用这些原始命令定义一些更复杂的高级命令。这样就可以利用低级的块结构，形成一个用户界面相当友好的环境。

在处理器运行期间，该程序首先读取所谓的格式文件，其中包含各种以原始语言写成的高级命令，也包含分割单词的连字号安排模式。接着处理程序就处理源文件，其中包含要处理的真正文本，以及在格式文件中已定义了的格式命令。

创建新格式是一件需要由具有丰富知识程序员来做的事情。把定义写到一个源文件中，这个文件接着被一个名叫 initex 的特殊版本的 TeX 程序处理。它采用一种紧凑的方式存贮这些新格式，这样就可以被通常 TeX 程序很快地读取。

#### Plain TeX

Knuth 设计了一个名叫 Plain TeX 的基本格式，以与低层次的原始 TeX 呼应。这种格式是用 TeX 处理文本时相当基本的部分，以致于我们有时都分不清到底哪条指令是真正的处理程序 TeX 的原始命令，哪条是 Plain TeX 格式的。大多数声称只使用 TeX 的人，实际上指的是只用 Plain TeX 。

Plain TeX 也是其它格式的基础，这进一步加深了很多人认为 TeX 和 Plain TeX 是同一事物的印象。

#### LaTeX排版

Plain TeX 的重点还只是在于如何排版的层次上，而不是从一位作者的观点出发。对它的深层功能的进一步发掘，需要相当丰富的编程技巧。因此它的应用就局限于高级排版和程序设计人员。

Leslie Lamport 开发的 LaTeX 是当今世界上最流行和使用最为广泛的 TeX 格式。它构筑在 Plain TeX 的基础之上，并加进了很多的功能以使得使用者可以更为方便的利用 TeX 的强大功能。使用 LaTeX 基本上不需要使用者自己设计命令和宏等，因为 LaTeX 已经替你做好了。因此，即使使用者并不是很了解 TeX ，也可以在短短的时间内生成高质量的文档。对于生成复杂的数学公式，LaTeX 表现的更为出色。

#### LaTeX2e

LaTeX 自从二十世纪八十年代初问世以来，也在不断的发展。最初的正式版本为 2.09，在经过几年的发展之后，许多新的功能，机制被引入到 LaTeX 中。在享受这些新功能带来的便利的同时，它所伴随的副作用也开始显现，这就是不兼容性。标准的 LaTeX 2.09，引入了“新字体选择框架”(NFSS)的 LaTeX，””SLiTeX””，””AMSLaTeX”” 等等，相互之间并不兼容。这给使用者和维护者都带来很大的麻烦。

为结束这中糟糕的状况，Frank Mittelbach 等人成立了 LaTeX3 项目小组，目标是建立一个最优的，有效的，统一的，标准的命令集合。即得到 LaTeX 的一个新版本 3。这是一个长期目标，向这个目标迈出第一步就是在 1994 年发布的 LaTeX2e 。LaTeX2e 采用了 NFSS 作为标准，加入了很多新的功能，同时还兼容旧的 LaTeX 2.09。LaTeX2e 每 6 个月更新一次，修正发现的错误并加入一些新的功能。在 LaTeX3 最终完成之前，LaTeX2e 将是标准的 LaTeX 版本。

### LaTeX 的主要特点

1. 文档结构：

   - LaTeX 使用一种结构化的方法来组织文档。文档被分为章节、小节、子小节等，并且有专门的命令来定义标题、段落、列表、引用、交叉引用等。
2. 命令与环境：

   - 命令：LaTeX 中的命令通常以反斜杠 \ 开头，后跟命令名称。例如，\section{Introduction} 用来创建一个章节标题。
   - 环境：环境是用 \begin{environment} 和 \end{environment} 包围的一段代码，例如，\begin{itemize} 和 \end{itemize} 用于创建项目列表。
3. 数学模式：

   - LaTeX 提供了强大的数学排版功能。有两种基本的数学模式：内联模式（在文本行中）和显示模式（独立于文本行的数学公式）。内联模式使用单个美元符号 $ 来包围数学表达式，显示模式则使用双美元符号 $$ 或者 \[ ... \]。
4. 宏与包：

   - 宏：允许用户定义自己的命令，简化重复任务或自定义样式。
   - 包：是扩展 LaTeX 功能的模块，可以添加新的命令、环境和选项。例如，amsmath 包提供了更多的数学排版功能，graphicx 包则用于图形插入和操作。
5. 编译过程：

   - LaTeX 文档需要通过编译器（如 pdflatex、xelatex 或 lualatex）处理，将 LaTeX 源文件转换成 PDF 或其他格式的输出文件。通常，一个完整的编译过程可能需要多次运行编译器，以正确处理交叉引用和索引。
6. 文档类与风格文件：

   - LaTeX 提供了多种文档类，如 article、report、book 等，每种文档类都有其特定的布局和结构。用户还可以使用 .sty 文件来自定义文档样式。
7. 国际化与多语言支持：

   - LaTeX 支持多语言排版，包括复杂的脚本和字符集。例如，使用 babel 包可以轻松地在文档中切换不同的语言。
8. 图形与表格：

   - LaTeX 提供了创建复杂表格和图形的能力，例如使用 tabular 环境来制作表格，或者使用 TikZ 和 PGFPlots 等图形包来绘制矢量图和数据图表。
9. 注释与调试：

   - 使用 % 符号可以添加注释，不会在最终文档中显示。此外，LaTeX 提供了各种工具和命令来帮助诊断和解决编译错误。

#### 对比word

- 完全自定义，自主设计，比 Word 更专业的排版超文本标记语言；
- 设计效率高，不需频繁操作鼠标；
- 复用性强，利用已有模板可实现快速专业的论文排版；
- 对数学公式的支持性更好，不会像 Word 跑版；
- 可更加专注于文章内容本身；
- 大部分期刊要求 LaTeX 版本；
- 可进行注释，且不显示在 pdf 中；
- 不会像 Word 一样崩掉，不会因版本问题跑版；
- 方便代码插入，可插入热门语言代码；
- 开源。

## 学习网站和论坛

1. [LaTeX 官方文档](https://www.latex-project.org/help/documentation/)
2. CTeX 中文套装软件
   [CTeX](https://ctex.org/) 是一个针对中文用户的 LaTeX 发行版，包含了多种中文支持的字体和宏包，以及编辑和编译 LaTeX 文档所需的工具。
3. LaTeX 工作室
   [LaTeX 工作室](https://www.latexstudio.net/) 提供在线 LaTeX 编辑和编译服务，支持中文，适合快速编写和查看 LaTeX 文档的效果。
4. ShareLaTeX
   [ShareLaTeX](https://www.sharelatex.com/) 是一个在线 LaTeX 编辑器，支持中文，提供实时协作和项目管理功能。
5. Overleaf
   [Overleaf](https://www.overleaf.com/) 类似于 ShareLaTeX，也是一个在线 LaTeX 编辑平台，支持中文和其他多种语言。
6. LaTeX 表格生成器
   [Tablesgenerator](https://www.tablesgenerator.com/) 可以在线生成 LaTeX 表格代码，适用于需要快速创建复杂表格的场景。
7. LaTeX 公式编辑器
   [Latexlive](https://www.latexlive.com/) 和 [Codecogs](https://editor.codecogs.com/) 提供在线 LaTeX 公式编辑器，可以创建并下载数学公式的图像。
8. [OI Wiki 文档](https://oi-wiki.org/tools/latex/)

### 文档和入门书

- [lshort-zh-cn](http://mirrors.ctan.org/info/lshort/chinese/lshort-zh-cn.pdf) 文档，这个文档译名是：一份（不太）简短的 LaTeX2e 介绍或 112 分钟了解 LaTeX2e，新版本又 CTeX 社区维护这里，本书是绝好的中文入门文档。
- LaTeX Notes 雷太赫排版系统简介, 包太雷, 2019 [lnotes2.pdf](https://pics.latexstudio.net/uploads/20210525/408a56c37299cd17d9580b6dbef99255.pdf) 其[源代](https://github.com/huangxg/lnotes)码在这里，这是非常容易读下去的中文文档，语言比较生动活泼，相比较老版本，新版本更加丰富了，推荐大家从这一篇文献开启你的 LaTeX 学习生活。
- 简单粗暴 LaTeX， LaTeX-cn.pdf，代码 这是真正出版了的书稿，本手册的稿件已经交由中国工信出版集团、人民邮电出版社完成出版，这本电子书只有不到一百页，非常短小精悍。

如果你有余力可以购买刘海洋的《LaTeX 入门》纸质版，时间有点久了，也可以看看他的视频讲座：[https://www.bilibili.com/video/BV1s7411U7Pr](https://www.bilibili.com/video/BV1s7411U7Pr)

### 中文讲义

- 华东师范大学的讲义可以说是经历了十几年的沉淀了，绝对是值得读读学习的资料，讲义读起来比较提纲挈领结合电子书，入门肯定可以加速。潘建瑜老师的 LaTeX 课程讲义地址：[http://math.ecnu.edu.cn/~jypan/Teaching/Latex/](http://math.ecnu.edu.cn/~jypan/Teaching/Latex/)
- 吕荐瑞老师的 LaTeX 讲稿，制作也是非常用心的，可以观瞻观瞻。PDF 讲义
- 清华大学每年都举办的 LaTeX 讲座也非常不错，在这里：[https://github.com/tuna/thulib-latex-talk](https://github.com/tuna/thulib-latex-talk) 这里有汪彧之的讲解版本：[https://www.bilibili.com/video/BV1sf4y1q7HK](https://www.bilibili.com/video/BV1sf4y1q7HK) 可以看看。

另外，中文解决方案的 [CTeX](http://mirrors.ctan.org/language/chinese/ctex/ctex.pdf) 宏集都是中文的说明，看这里：PDF 文件，更多中文文档还有很多，比如：xeCJK，diagbox 等，更多的大家一起去探索吧，另外，[latexstudio站点](https://www.latexstudio.net/index/lists/index/type/1/cate/16.html)也在不断进行中文宏包说明的汉化翻译，看看这里，希望对于大家学习有更多帮助。

### 视频教程

如上的这些资料入门足够了，希望大家的入门更简单，更加轻松，我们这里还有大量的视频来指导大家。
[https://space.bilibili.com/209746320](https://space.bilibili.com/209746320)

## 语法

### 数学公式编辑 Displaying a formula

#### 符号与字母 Symbol and Alphabet

##### 希腊字母 Greek alphabet

| 序号 | 小写 | LaTeX       | 读音                         | 序号 | 大写 | LaTeX    | 读音            |
| ---- | ---- | ----------- | ---------------------------- | ---- | ---- | -------- | --------------- |
| 1    | 𝛼   | \alpha      | /ˈælfə/                   | 31   | Γ   | \Gamma   | /ˈɡæmə/     |
| 2    | 𝛽   | \beta       | /ˈbiːtə/, US: /ˈbeɪtə/ | 32   | Δ   | \Delta   | /ˈdɛltə/     |
| 3    | 𝛾   | \gamma      | /ˈɡæmə/                  | 33   | Θ   | \Theta   | /ˈθiːtə/    |
| 4    | 𝛿   | \delta      | /ˈdɛltə/                  | 34   | Λ   | \Lambda  | /ˈlæmdə/     |
| 5    | 𝜖   | \epsilon    | /ˈɛpsɪlɒn/               | 35   | Ξ   | \Xi      | /zaɪ, ksaɪ/   |
| 6    | 𝜀   | \varepsilon | /ˈɛpsɪlɒn/               | 36   | Π   | \Pi      | /paɪ/          |
| 7    | 𝜁   | \zeta       | /ˈzeɪtə/                  | 37   | Σ   | \Sigma   | /ˈsɪɡmə/    |
| 8    | 𝜂   | \eta        | /ˈeɪtə/                   | 38   | Υ   | \Upsilon | /ˈʌpsɪlɒn/  |
| 9    | 𝜃   | \theta      | /ˈθiːtə/                 | 39   | Φ   | \Phi     | /faɪ/          |
| 10   | 𝜗   | \vartheta   | /ˈθiːtə/                 | 40   | Ψ   | \Psi     | /psaɪ/         |
| 11   | 𝜄   | \iota       | /aɪˈoʊtə/                | 41   | Ω   | \Omega   | /oʊˈmeɪɡə/ |
| 12   | 𝜅   | \kappa      | /ˈkæpə/                   |      |      |          |                 |
| 13   | 𝜆   | \lambda     | /ˈlæmdə/                  |      |      |          |                 |
| 14   | 𝜇   | \mu         | /mjuː/                      |      |      |          |                 |
| 15   | 𝜈   | \nu         | /njuː/                      |      |      |          |                 |
| 16   | 𝜉   | \xi         | /zaɪ, ksaɪ/                |      |      |          |                 |
| 17   | 𝑜   | o           | /ˈɒmɪkrɒn/               |      |      |          |                 |
| 18   | 𝜋   | \pi         | /paɪ/                       |      |      |          |                 |
| 19   | 𝜛   | \varpi      | /paɪ/                       |      |      |          |                 |
| 20   | 𝜌   | \rho        | /roʊ/                       |      |      |          |                 |
| 21   | 𝜚   | \varrho     | /roʊ/                       |      |      |          |                 |
| 22   | 𝜎   | \sigma      | /ˈsɪɡmə/                 |      |      |          |                 |
| 23   | 𝜍   | \varsigma   | /ˈsɪɡmə/                 |      |      |          |                 |
| 24   | 𝜏   | \tau        | /taʊ, tɔː/                |      |      |          |                 |
| 25   | 𝜐   | \upsilon    | /ˈʌpsɪlɒn/               |      |      |          |                 |
| 26   | 𝜙   | \phi        | /faɪ/                       |      |      |          |                 |
| 27   | 𝜑   | \varphi     | /faɪ/                       |      |      |          |                 |
| 28   | 𝜒   | \chi        | /kaɪ/                       |      |      |          |                 |
| 29   | 𝜓   | \psi        | /psaɪ/                      |      |      |          |                 |
| 30   | 𝜔   | \omega      | /oʊˈmeɪɡə/              |      |      |          |                 |

- 注意: MathJax支持的大写希腊字母有限，如需其他（如大写Alpha），可使用罗马体转换，如 `\mathrm{A}`表示大写Alpha：$\mathrm{A}$。

##### 希伯来字母 Hebrew alphabet

| 序号 | 图标 | LaTeX   | 英文   |
| ---- | ---- | ------- | ------ |
| 1    | ℵ   | \aleph  | aleph  |
| 2    | ℶ   | \beth   | beth   |
| 3    | ℷ   | \gimel  | gimel  |
| 4    | ℸ   | \daleth | daleth |

##### 二元运算符 Binary operations

| 序号 | 图标 | LaTeX                             | 序号 | 图标 | LaTeX            |
| ---- | ---- | --------------------------------- | ---- | ---- | ---------------- |
| 1    | +    | +                                 | 20   | ∙   | \bullet          |
| 2    | −   | -                                 | 21   | ⊕   | \oplus           |
| 3    | ×   | \times                            | 22   | ⊖   | \ominus          |
| 4    |      | \div``(在physics扩展开启状态下为) | 23   | ⊙   | \odot            |
| 5    | ±   | \pm                               | 24   | ⊘   | \oslash          |
| 6    | ∓   | \mp                               | 25   | ⊗   | \otimes          |
| 7    | ◃   | \triangleleft                     | 26   | ◯   | \bigcirc         |
| 8    | ▹   | \triangleright                    | 27   | ⋄   | \diamond         |
| 9    | ⋅   | \cdot                             | 28   | ⊎   | \uplus           |
| 10   | ∖   | \setminus                         | 29   | △   | \bigtriangleup   |
| 11   | ⋆   | \star                             | 30   | ▽   | \bigtriangledown |
| 12   | ∗   | \ast                              | 31   | ⊲   | \lhd             |
| 13   | ∪   | \cup                              | 32   | ⊳   | \rhd             |
| 14   | ∩   | \cap                              | 33   | ⊴   | \unlhd           |
| 15   | ⊔   | \sqcup                            | 34   | ⊵   | \unrhd           |
| 16   | ⊓   | \sqcap                            | 35   | ⨿   | \amalg           |
| 17   | ∨   | \vee                              | 36   | ≀   | \wr              |
| 18   | ∧   | \wedge                            | 37   | †   | \dagger          |
| 19   | ∘   | \circ                             | 38   | ‡   | \ddagger         |

##### 二元关系符 Binary relations

| 序号 | 图标    | LaTeX                                  | 序号 | 图标 | LaTeX        |
| ---- | ------- | -------------------------------------- | ---- | ---- | ------------ |
| 1    | =       | =                                      | 49   | ⪈   | \gneq        |
| 2    | ≠      | \ne                                    | 50   | ≧   | \geqq        |
| 3    | ≠      | \neq                                   | 51   | ≱   | \ngeq        |
| 4    | ≡      | \equiv                                 | 52   | ≱   | \ngeqq       |
| 5    | ≢      | \not\equiv                             | 53   | ≩   | \gneqq       |
| 6    | ≐      | \doteq                                 | 54   | ≩   | \gvertneqq   |
| 7    | ≑      | \doteqdot                              | 55   | ≶   | \lessgtr     |
| 8    | =def    | \overset{\underset{\mathrm{def}}{}}{=} | 56   | ⋚   | \lesseqgtr   |
| 9    | :=      | :=                                     | 57   | ⪋   | \lesseqqgtr  |
| 10   | ∼      | \sim                                   | 58   | ≷   | \gtrless     |
| 11   | ≁      | \nsim                                  | 59   | ⋛   | \gtreqless   |
| 12   | ∽      | \backsim                               | 60   | ⪌   | \gtreqqless  |
| 13   | ∼      | \thicksim                              | 61   | ⩽   | \leqslant    |
| 14   | ≃      | \simeq                                 | 62   | ⪇   | \nleqslant   |
| 15   | ⋍      | \backsimeq                             | 63   | ⪕   | \eqslantless |
| 16   | ≂      | \eqsim                                 | 64   | ⩾   | \geqslant    |
| 17   | ≅      | \cong                                  | 65   | ⪈   | \ngeqslant   |
| 18   | ≇      | \ncong                                 | 66   | ⪖   | \eqslantgtr  |
| 19   | ≈      | \approx                                | 67   | ≲   | \lesssim     |
| 20   | ≈      | \thickapprox                           | 68   | ⋦   | \lnsim       |
| 21   | ≊      | \approxeq                              | 69   | ⪅   | \lessapprox  |
| 22   | ≍      | \asymp                                 | 70   | ⪉   | \lnapprox    |
| 23   | ∝      | \propto                                | 71   | ≳   | \gtrsim      |
| 24   | ∝      | \varpropto                             | 72   | ⋧   | \gnsim       |
| 25   | << /td> | <                                      | 73   | ⪆   | \gtrapprox   |
| 26   | ≮      | \nless                                 | 74   | ⪊   | \gnapprox    |
| 27   | ≪      | \ll                                    | 75   | ≺   | \prec        |
| 28   | ≪̸    | \not\ll                                | 76   | ⊀   | \nprec       |
| 29   | ⋘      | \lll                                   | 77   | ⪯   | \preceq      |
| 30   | ⋘̸    | \not\lll                               | 78   | ⋠   | \npreceq     |
| 31   | ⋖      | \lessdot                               | 79   | ⪵   | \precneqq    |
| 32   | >       | >                                      | 80   | ≻   | \succ        |
| 33   | ≯      | \ngtr                                  | 81   | ⊁   | \nsucc       |
| 34   | ≫      | \gg                                    | 82   | ⪰   | \succeq      |
| 35   | ≫̸    | \not\gg                                | 83   | ⋡   | \nsucceq     |
| 36   | ⋙      | \ggg                                   | 84   | ⪶   | \succneqq    |
| 37   | ⋙̸    | \not\ggg                               | 85   | ≼   | \preccurlyeq |
| 38   | ⋗      | \gtrdot                                | 86   | ⋞   | \curlyeqprec |
| 39   | ≤      | \le                                    | 87   | ≽   | \succcurlyeq |
| 40   | ≤      | \leq                                   | 88   | ⋟   | \curlyeqsucc |
| 41   | ⪇      | \lneq                                  | 89   | ≾   | \precsim     |
| 42   | ≦      | \leqq                                  | 90   | ⋨   | \precnsim    |
| 43   | ≰      | \nleq                                  | 91   | ⪷   | \precapprox  |
| 44   | ≰      | \nleqq                                 | 92   | ⪹   | \precnapprox |
| 45   | ≨      | \lneqq                                 | 93   | ≿   | \succsim     |
| 46   | ≨      | \lvertneqq                             | 94   | ⋩   | \succnsim    |
| 47   | ≥      | \ge                                    | 95   | ⪸   | \succapprox  |
| 48   | ≥      | \geq                                   | 96   | ⪺   | \succnapprox |

##### 几何符号 Geometric symbols

| 序号 | 图标 | LaTeX             | 序号 | 图标 | LaTeX               |
| ---- | ---- | ----------------- | ---- | ---- | ------------------- |
| 1    | ∥   | \parallel         | 14   | ◊   | \lozenge            |
| 2    | ∦   | \nparallel        | 15   | ⧫   | \blacklozenge       |
| 3    | ∥   | \shortparallel    | 16   | ★   | \bigstar            |
| 4    | ∦   | \nshortparallel   | 17   | ◯   | \bigcirc            |
| 5    | ⊥   | \perp             | 18   | △   | \triangle           |
| 6    | ∠   | \angle            | 19   | △   | \bigtriangleup      |
| 7    | ∢   | \sphericalangle   | 20   | ▽   | \bigtriangledown    |
| 8    | ∡   | \measuredangle    | 21   | △   | \vartriangle        |
| 9    | 45∘ | 45^\circ          | 22   | ▽   | \triangledown       |
| 10   | ◻   | \Box              | 23   | ▴   | \blacktriangle      |
| 11   | ◼   | \blacksquare      | 24   | ▾   | \blacktriangledown  |
| 12   | ⋄   | \diamond          | 25   | ◂   | \blacktriangleleft  |
| 13   | ◊   | \Diamond \lozenge | 26   | ▸   | \blacktriangleright |

##### 逻辑符号 Logic symbols

| 序号 | 图标     | LaTeX          | 序号 | 图标 | LaTeX                |
| ---- | -------- | -------------- | ---- | ---- | -------------------- |
| 1    | ∀       | \forall        | 20   | ¬   | \neg                 |
| 2    | ∃       | \exists        | 21   | R̸  | \not\operatorname{R} |
| 3    | ∄       | \nexists       | 22   | ⊥   | \bot                 |
| 4    | ∴       | \therefore     | 23   | ⊤   | \top                 |
| 5    | ∵       | \because       | 24   | ⊢   | \vdash               |
| 6    | &        | \And           | 25   | ⊣   | \dashv               |
| 7    | ∨       | \lor           | 26   | ⊨   | \vDash               |
| 8    | ∨       | \vee           | 27   | ⊩   | \Vdash               |
| 9    | ⋎       | \curlyvee      | 28   | ⊨   | \models              |
| 10   | ⋁       | \bigvee        | 29   | ⊪   | \Vvdash              |
| 11   | ∧       | \land          | 30   | ⊬   | \nvdash              |
| 12   | ∧       | \wedge         | 31   | ⊮   | \nVdash              |
| 13   | ⋏       | \curlywedge    | 32   | ⊭   | \nvDash              |
| 14   | ⋀       | \bigwedge      | 33   | ⊯   | \nVDash              |
| 15   | 𝑞¯     | \bar{q}        | 34   | ⌜   | \ulcorner            |
| 16   | 𝑎𝑏𝑐¯ | \bar{abc}      | 35   | ⌝   | \urcorner            |
| 17   | 𝑞―     | \overline{q}   | 36   | ⌞   | \llcorner            |
| 18   | 𝑎𝑏𝑐― | \overline{abc} | 37   | ⌟   | \lrcorner            |
| 19   | ¬       | \lnot          |      |      |                      |

##### 集合 Sets

| 序号 | 图标 | LaTeX          | 序号 | 图标 | LaTeX          |
| ---- | ---- | -------------- | ---- | ---- | -------------- |
| 1    | {}   | {}             | 23   | ⊏   | \sqsubset      |
| 2    | ∅   | \emptyset      | 24   | ⊃   | \supset        |
| 3    | ∅   | \varnothing    | 25   | ⋑   | \Supset        |
| 4    | ∈   | \in            | 26   | ⊐   | \sqsupset      |
| 5    | ∉   | \notin         | 27   | ⊆   | \subseteq      |
| 6    | ∋   | \ni            | 28   | ⊈   | \nsubseteq     |
| 7    | ∩   | \cap           | 29   | ⊊   | \subsetneq     |
| 8    | ⋒   | \Cap           | 30   | ⊊   | \varsubsetneq  |
| 9    | ⊓   | \sqcap         | 31   | ⊑   | \sqsubseteq    |
| 10   | ⋂   | \bigcap        | 32   | ⊇   | \supseteq      |
| 11   | ∪   | \cup           | 33   | ⊉   | \nsupseteq     |
| 12   | ⋓   | \Cup           | 34   | ⊋   | \supsetneq     |
| 13   | ⊔   | \sqcup         | 35   | ⊋   | \varsupsetneq  |
| 14   | ⋃   | \bigcup        | 36   | ⊒   | \sqsupseteq    |
| 15   | ⨆   | \bigsqcup      | 37   | ⫅   | \subseteqq     |
| 16   | ⊎   | \uplus         | 38   | ⊈   | \nsubseteqq    |
| 17   | ⨄   | \biguplus      | 39   | ⫋   | \subsetneqq    |
| 18   | ∖   | \setminus      | 40   | ⫋   | \varsubsetneqq |
| 19   | ∖   | \smallsetminus | 41   | ⫆   | \supseteqq     |
| 20   | ×   | \times         | 42   | ⊉   | \nsupseteqq    |
| 21   | ⊂   | \subset        | 43   | ⫌   | \supsetneqq    |
| 22   | ⋐   | \Subset        | 44   | ⫌   | \varsupsetneqq |

##### 箭头 Arrows

| 序号 | 图标 | LaTeX               | 序号 | 图标 | LaTeX                |
| ---- | ---- | ------------------- | ---- | ---- | -------------------- |
| 1    | ⇛   | \Rrightarrow        | 36   | ⟼   | \longmapsto          |
| 2    | ⇚   | \Lleftarrow         | 37   | ⇀   | \rightharpoonup      |
| 3    | ⇒   | \Rightarrow         | 38   | ⇁   | \rightharpoondown    |
| 4    | ⇏   | \nRightarrow        | 39   | ↼   | \leftharpoonup       |
| 5    | ⟹   | \Longrightarrow     | 40   | ↽   | \leftharpoondown     |
| 6    | ⟹   | \implies            | 41   | ↿   | \upharpoonleft       |
| 7    | ⇐   | \Leftarrow          | 42   | ↾   | \upharpoonright      |
| 8    | ⇍   | \nLeftarrow         | 43   | ⇃   | \downharpoonleft     |
| 9    | ⟸   | \Longleftarrow      | 44   | ⇂   | \downharpoonright    |
| 10   | ⇔   | \Leftrightarrow     | 45   | ⇌   | \rightleftharpoons   |
| 11   | ⇎   | \nLeftrightarrow    | 46   | ⇋   | \leftrightharpoons   |
| 12   | ⟺   | \Longleftrightarrow | 47   | ↶   | \curvearrowleft      |
| 13   | ⟺   | \iff                | 48   | ↺   | \circlearrowleft     |
| 14   | ⇑   | \Uparrow            | 49   | ↰   | \Lsh                 |
| 15   | ⇓   | \Downarrow          | 50   | ⇈   | \upuparrows          |
| 16   | ⇕   | \Updownarrow        | 51   | ⇉   | \rightrightarrows    |
| 17   | →   | \rightarrow         | 52   | ⇄   | \rightleftarrows     |
| 18   | →   | \to                 | 53   | ↣   | \rightarrowtail      |
| 19   | ↛   | \nrightarrow        | 54   | ↬   | \looparrowright      |
| 20   | ⟶   | \longrightarrow     | 55   | ↷   | \curvearrowright     |
| 21   | ←   | \leftarrow          | 56   | ↻   | \circlearrowright    |
| 22   | ←   | \gets               | 57   | ↱   | \Rsh                 |
| 23   | ↚   | \nleftarrow         | 58   | ⇊   | \downdownarrows      |
| 24   | ⟵   | \longleftarrow      | 59   | ⇇   | \leftleftarrows      |
| 25   | ↔   | \leftrightarrow     | 60   | ⇆   | \leftrightarrows     |
| 26   | ↮   | \nleftrightarrow    | 61   | ↢   | \leftarrowtail       |
| 27   | ⟷   | \longleftrightarrow | 62   | ↫   | \looparrowleft       |
| 28   | ↑   | \uparrow            | 63   | ↪   | \hookrightarrow      |
| 29   | ↓   | \downarrow          | 64   | ↩   | \hookleftarrow       |
| 30   | ↕   | \updownarrow        | 65   | ⊸   | \multimap            |
| 31   | ↗   | \nearrow            | 66   | ↭   | \leftrightsquigarrow |
| 32   | ↙   | \swarrow            | 67   | ⇝   | \rightsquigarrow     |
| 33   | ↖   | \nwarrow            | 68   | ↠   | \twoheadrightarrow   |
| 34   | ↘   | \searrow            | 69   | ↞   | \twoheadleftarrow    |
| 35   | ↦   | \mapsto             |      |      |                      |

##### 特殊 Special

| 序号 | 图标 | LaTeX          | 序号 | 图标 | LaTeX             |
| ---- | ---- | -------------- | ---- | ---- | ----------------- |
| 1    | ∞   | \infty         | 33   | ♭   | \flat             |
| 2    | ℵ   | \aleph         | 34   | ♮   | \natural          |
| 3    | ∁   | \complement    | 35   | ♯   | \sharp            |
| 4    | ∍   | \backepsilon   | 36   | ╱   | \diagup           |
| 5    | ð   | \eth           | 37   | ╲   | \diagdown         |
| 6    | Ⅎ   | \Finv          | 38   | ⋅   | \centerdot        |
| 7    | ℏ   | \hbar          | 39   | ⋉   | \ltimes           |
| 8    | Im   | \Im            | 40   | ⋊   | \rtimes           |
| 9    | 𝚤   | \imath         | 41   | ⋋   | \leftthreetimes   |
| 10   | 𝚥   | \jmath         | 42   | ⋌   | \rightthreetimes  |
| 11   | 𝕜𝑘 | \Bbbk          | 43   | ≖   | \eqcirc           |
| 12   | ℓ   | \ell           | 44   | ≗   | \circeq           |
| 13   | ℧   | \mho           | 45   | ≜   | \triangleq        |
| 14   | ℘   | \wp            | 46   | ≏   | \bumpeq           |
| 15   | Re   | \Re            | 47   | ≎   | \Bumpeq           |
| 16   | Ⓢ   | \circledS      | 48   | ≑   | \doteqdot         |
| 17   | ⨿   | \amalg         | 49   | ≓   | \risingdotseq     |
| 18   | %    | \%             | 50   | ≒   | \fallingdotseq    |
| 19   | †   | \dagger        | 51   | ⊺   | \intercal         |
| 20   | ‡   | \ddagger       | 52   | ⊼   | \barwedge         |
| 21   | …   | \ldots         | 53   | ⊻   | \veebar           |
| 22   | ⋯   | \cdots         | 54   | ⩞   | \doublebarwedge   |
| 23   | ⌣   | \smile         | 55   | ≬   | \between          |
| 24   | ⌢   | \frown         | 56   | ⋔   | \pitchfork        |
| 25   | ≀   | \wr            | 57   | ⊲   | \vartriangleleft  |
| 26   | ◃   | \triangleleft  | 58   | ⋪   | \ntriangleleft    |
| 27   | ▹   | \triangleright | 59   | ⊳   | \vartriangleright |
| 28   | ♢   | \diamondsuit   | 60   | ⋫   | \ntriangleright   |
| 29   | ♡   | \heartsuit     | 61   | ⊴   | \trianglelefteq   |
| 30   | ♣   | \clubsuit      | 62   | ⋬   | \ntrianglelefteq  |
| 31   | ♠   | \spadesuit     | 63   | ⊵   | \trianglerighteq  |
| 32   | ⅁   | \Game          | 64   | ⋭   | \ntrianglerighteq |

#### 运算与函数 Operations & Functions

##### 分数 Fractions

| 类型                                                             | 样式                                                                         | LaTeX                                                                    |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| 分数 Fractions                                                  | $\frac{2}{4}x=0.5x or {2 \over 4}x=0.5x$                                   | \frac{2}{4}x=0.5x or {2 \over 4}x=0.5x                                   |
| 小型分数 Small fractions (force \textstyle)                     | $\tfrac{2}{4}x = 0.5x$                                                     | \tfrac{2}{4}x = 0.5x                                                     |
| 大型分数（不嵌套）Large (normal) fractions (force \displaystyle) | $\dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a$ | \dfrac{2}{4} = 0.5 \qquad \dfrac{2}{c + \dfrac{2}{d + \dfrac{2}{4}}} = a |
| 大型分数（嵌套）Large (nested) fractions                         | $\cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a$                           | \cfrac{2}{c + \cfrac{2}{d + \cfrac{2}{4}}} = a                           |
| 约分线的使用 Cancellations in fractions                          | $\cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2}$             | \cfrac{x}{1 + \cfrac{\cancel{y}}{\cancel{y}}} = \cfrac{x}{2}             |

**注意：** 其中 `\cancel`命令需要**cancel扩展包**支持，**cancel扩展包**是一款自定义宏包，如需使用请在公式页面右上角【设置】页面勾选后使用。

##### 标准数值函数 Standard numerical functions

| 样式                                                                                 | LaTeX                                                                            |
| ------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------- |
| $\exp_a b = a^b, \exp b = e^b, 10^m$                                               | \exp_a b = a^b, \exp b = e^b, 10^m                                               |
| $\ln c, \lg d = \log e, \log_{10} f$                                               | \ln c, \lg d = \log e, \log_{10} f                                               |
| $\sin a,\cos b,\tan c,\cot d,\sec e,\csc f$                                        | \sin a, \cos b, \tan c, \cot d, \sec e, \csc f                                   |
| $\arcsin a, \arccos b, \arctan c$                                                  | \arcsin a, \arccos b, \arctan c                                                  |
| $\operatorname{arccot} d, \operatorname{arcsec} e, \operatorname{arccsc} f$        | \operatorname{arccot} d, \operatorname{arcsec} e, \operatorname{arccsc} f        |
| $\sinh a, \cosh b, \tanh c, \coth d$                                               | \sinh a, \cosh b, \tanh c, \coth d                                               |
| $\operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n$ | \operatorname{sh}k, \operatorname{ch}l, \operatorname{th}m, \operatorname{coth}n |
| $ \operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q$             | \operatorname{argsh}o, \operatorname{argch}p, \operatorname{argth}q              |
| $\operatorname{sgn}r, \left\vert s \right\vert$                                    | \operatorname{sgn}r, \left\vert s \right\vert                                    |
| $\min(x,y), \max(x,y)$                                                             | \min(x,y), \max(x,y)                                                             |

**注意：** LaTeX和MathJax支持的操作符有限，如有特殊操作符，可以使用 `\operatorname{}` 命令自定义，例如
`\operatorname{mydefine}x：`$\operatorname{mydefine}x$

##### 根式 Radicals

| 样式                            | LaTeX                       |
| ------------------------------- | --------------------------- |
| $\surd$                       | \surd                       |
| $\sqrt{\pi}$                  | \sqrt{\pi}                  |
| $\sqrt[n]{\pi}$               | \sqrt[n]{\pi}               |
| $\sqrt[3]{\frac{x^3+y^3}{2}}$ | \sqrt[3]{\frac{x^3+y^3}{2}} |

##### 微分与导数 Differentials and derivatives

| 样式                                                                                                                             | LaTeX                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------- |
| $dt, \mathrm{d}t, \partial t, \nabla\psi$                                                                                      | dt, \mathrm{d}t, \partial t, \nabla\psi                                                                                      |
| $dy/dx, \mathrm{d}y/\mathrm{d}x, \frac{dy}{dx}, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\partial^2}{\partial x_1\partial x_2}y$ | dy/dx, \mathrm{d}y/\mathrm{d}x, \frac{dy}{dx}, \frac{\mathrm{d}y}{\mathrm{d}x}, \frac{\partial^2}{\partial x_1\partial x_2}y |
| $\prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y$                                                              | \prime, \backprime, f^\prime, f', f'', f^{(3)}, \dot y, \ddot y                                                              |

##### 同余与模算术 Modular arithmetic

| 样式                                     | LaTeX                                |
| ---------------------------------------- | ------------------------------------ |
| $s_k \equiv 0 \pmod{m}$                | s_k \equiv 0 \pmod{m}                |
| $a \bmod b$                            | a \bmod b                            |
| $\gcd(m, n), \operatorname{lcm}(m, n)$ | \gcd(m, n), \operatorname{lcm}(m, n) |
| $\mid, \nmid, \shortmid, \nshortmid$   | \mid, \nmid, \shortmid, \nshortmid   |

##### 极限 Limits

| 样式                                  | LaTeX                             |
| ------------------------------------- | --------------------------------- |
| $\lim_{n \to \infty}x_n$            | \lim_{n \to \infty}x_n            |
| $\textstyle \lim_{n \to \infty}x_n$ | \textstyle \lim_{n \to \infty}x_n |

##### 界限与投影 Bounds and Projections

| 样式                                       | LaTeX                                  |
| ------------------------------------------ | -------------------------------------- |
| $\min x, \max y, \inf s, \sup t$         | \min x, \max y, \inf s, \sup t         |
| $\lim u, \liminf v, \limsup w$           | \lim u, \liminf v, \limsup w           |
| $\dim p, \deg q, \det m, \ker\phi$       | \dim p, \deg q, \det m, \ker\phi       |
| $\Pr j, \hom l, \lVert z \rVert, \arg z$ | \Pr j, \hom l, \lVert z \rVert, \arg z |

##### 积分 Integral

| 样式                                          | LaTeX                                     |
| --------------------------------------------- | ----------------------------------------- |
| $\int\limits_{1}^{3}\frac{e^3/x}{x^2}\, dx$ | \int\limits_{1}^{3}\frac{e^3/x}{x^2}\, dx |
| $\int_{1}^{3}\frac{e^3/x}{x^2}\, dx$        | \int_{1}^{3}\frac{e^3/x}{x^2}\, dx        |
| $\textstyle \int\limits_{-N}^{N} e^x dx$    | \textstyle \int\limits_{-N}^{N} e^x dx    |
| $\textstyle \int_{-N}^{N} e^x dx$           | \textstyle \int_{-N}^{N} e^x dx           |
| $\iint\limits_D dx\,dy$                     | \iint\limits_D dx\,dy                     |
| $\iiint \limits_E dx\,dy\,dz$               | \iiint\limits_E dx\,dy\,dz                |
| $ \int_{(x,y)\in C} x^3\, dx + 4y^2\, dy$   | \int_{(x,y)\in C} x^3\, dx + 4y^2\, dy    |
| $\oint_{(x,y)\in C} x^3\, dx + 4y^2\, dy$   | \oint_{(x,y)\in C} x^3\, dx + 4y^2\, dy   |

**注意：** 积分符号可以使用 `\int_{}^{}`命令调用，如需双重积分符号只需将 `int`替换成 `iint`即可，以此类推，最高支持四重。曲线积分可使用 `\oint`命令调用，但曲面积分符号在MathJax环境中并不支持 `\oiint`的用法，但仍可通过 `\unicode{}`命令，即Unicode代码的方式进行调用（前提是您需要在设置中打开Unicode扩展），具体使用方法如下：

##### 其他大型运算 Large operators

| 类别              | 样式                             | LaTeX                        |
| ----------------- | -------------------------------- | ---------------------------- |
| 求和 Summation    | $\sum_{a}^{b}$                 | \sum_{a}^{b}                 |
| 求和 Summation    | $\textstyle \sum_{a}^{b}$      | \textstyle \sum_{a}^{b}      |
| 连乘积 Product    | $\prod_{a}^{b}$                | \prod_{a}^{b}                |
| 连乘积 Product    | $\textstyle \prod_{a}^{b}$     | \textstyle \prod_{a}^{b}     |
| 余积 Coproduct    | $\coprod_{a}^{b}$              | \coprod_{a}^{b}              |
| 余积 Coproduct    | $\textstyle \coprod_{a}^{b}$   | \textstyle \coprod_{a}^{b}   |
| 并集 Union        | $\bigcup_{a}^{b}$              | \bigcup_{a}^{b}              |
| 并集 Union        | $\textstyle \bigcup_{a}^{b}$   | \textstyle \bigcup_{a}^{b}   |
| 交集 Intersection | $\bigcap_{a}^{b}$              | \bigcap_{a}^{b}              |
| 交集 Intersection | $\textstyle \bigcap_{a}^{b}$   | \textstyle \bigcap_{a}^{b}   |
| 析取 Disjunction  | $\bigvee_{a}^{b}$              | \bigvee_{a}^{b}              |
| 析取 Disjunction  | $\textstyle \bigvee_{a}^{b}$   | \textstyle \bigvee_{a}^{b}   |
| 合取 Conjunction  | $\bigwedge_{a}^{b}$            | \bigwedge_{a}^{b}            |
| 合取 Conjunction  | $\textstyle \bigwedge_{a}^{b}$ | \textstyle \bigwedge_{a}^{b} |

#### 上下标 Sub & Super

| 类型                                                          | 样式                                                             | 代码                                                         |
| ------------------------------------------------------------- | ---------------------------------------------------------------- | ------------------------------------------------------------ |
| 上标 Superscript                                              | $a^2, a^{x+3}$                                                 | a^2, a^{x+3}                                                 |
| 下标 Subscrip                                                 | $a_2$                                                          | a_2                                                          |
| 组合 Grouping                                                 | $10^{30} a^{2+2}$                                              | 10^{30} a^{2+2}                                              |
|                                                               | $a*{i,j} b* {f'} $                                             | a*{i,j} b* {f'}                                              |
| 上下标混合 Combining sub & super                              | $x_2^3 $                                                       | x_2^3                                                        |
|                                                               | ${x_2}^3$                                                      | {x_2}^3                                                      |
| 上标的上标 Super super                                        | $10^{10^{8}}$                                                  | 10^{10^{8}}                                                  |
| 混合标识 Preceding and/or additional sub & super              | ${}_1^2\Omega_3^4$                                             | {}_1^2!\Omega_3^4                                            |
| 顶标底标 Stacking                                             | $\overset{\alpha}{\omega}$                                     | \overset{\alpha}{\omega}                                     |
|                                                               | $\underset{\alpha}{\omega}$                                    | \underset{\alpha}{\omega}                                    |
|                                                               | $\overset{\alpha}{\underset{\gamma}{\omega}}$                  | \overset{\alpha}{\underset{\gamma}{\omega}}                  |
|                                                               | $\stackrel{\alpha}{\omega}$                                    | \stackrel{\alpha}{\omega}                                    |
| 导数 Derivatives                                              | $x', y'', f', f''$                                             | x', y'', f', f''                                             |
|                                                               | $x^\prime, y^{\prime\prime}$                                   | x^\prime, y^{\prime\prime}                                   |
| 导数 Derivative dots                                          | $\dot{x}, \ddot{x}$                                            | \dot{x}, \ddot{x}                                            |
| 下划线、上划线与向量 Underlines, overlines, vectors           | $\hat a \ \bar b \ \vec c$                                     | \hat a \ \bar b \ \vec c                                     |
|                                                               | $\overrightarrow{a b} \ \overleftarrow{c d} \ \widehat{d e f}$ | \overrightarrow{a b} \ \overleftarrow{c d} \ \widehat{d e f} |
|                                                               | $\overline{g h i} \ \underline{j k l}$                         | \overline{g h i} \ \underline{j k l}                         |
| 弧度 Arc (workaround)                                         | $\overset{\frown} {AB}$                                        | \overset{\frown} {AB}                                        |
| 箭头 Arrow                                                    | $A \xleftarrow{n+\mu-1} B \xrightarrow[T]{n\pm i-1} C$         | A \xleftarrow{n+\mu-1} B \xrightarrow[T]{n\pm i-1} C         |
| 大括号 Overbraces                                             | $\overbrace{ 1+2+\cdots+100 }^{5050}$                          | \overbrace{ 1+2+\cdots+100 }^{5050}                          |
| 底部大括号 Underbraces                                        | $\underbrace{ a+b+\cdots+z }_{26}$                             | \underbrace{ a+b+\cdots+z }_{26}                             |
| 求和运算 Sum                                                  | $\sum_{k=1}^N k^2$                                             | \sum_{k=1}^N k^2                                             |
| 文本模式下的求和运算 Sum (force \textstyle)                   | $\textstyle \sum_{k=1}^N k^2$                                  | \textstyle \sum_{k=1}^N k^2                                  |
| 分式中的求和运算 Sum in a fraction (default \textstyle)       | $\frac{\sum_{k=1}^N k^2}{a}$                                   | \frac{\sum_{k=1}^N k^2}{a}                                   |
| 分式中的求和运算 Sum in a fraction (force \displaystyle)      | $\frac{\displaystyle \sum_{k=1}^N k^2}{a}$                     | \frac{\displaystyle \sum_{k=1}^N k^2}{a}                     |
| 分式中的求和运算 Sum in a fraction (alternative limits style) | $\frac{\sum\limits^{^N}_{k=1} k^2}{a}$                         | \frac{\sum\limits^{^N}_{k=1} k^2}{a}                         |
| 乘积运算 Product                                              | $\prod_{i=1}^N x_i$                                            | \prod_{i=1}^N x_i                                            |
| 乘积运算 Product (force \textstyle)                           | $\textstyle \prod_{i=1}^N x_i$                                 | \textstyle \prod_{i=1}^N x_i                                 |
| 副乘运算 Coproduct                                            | $\coprod_{i=1}^N x_i$                                          | \coprod_{i=1}^N x_i                                          |
| 副乘运算 Coproduct (force \textstyle)                         | $\textstyle \coprod_{i=1}^N x_i$                               | \textstyle \coprod_{i=1}^N x_i                               |
| 极限 Limit                                                    | $\lim_{n \to \infty}x_n$                                       | \lim_{n \to \infty}x_n                                       |
| 极限 Limit (force \textstyle)                                 | $\textstyle \lim_{n \to \infty}x_n$                            | \textstyle \lim_{n \to \infty}x_n                            |
| 积分 Integral                                                 | $\int\limits_{1}^{3}\frac{e^3/x}{x^2}\, dx$                    | \int\limits_{1}^{3}\frac{e^3/x}{x^2}\, dx                    |
| 积分 Integral (alternative limits style)                      | $\int_{1}^{3}\frac{e^3/x}{x^2}\, dx$                           | \int_{1}^{3}\frac{e^3/x}{x^2}\, dx                           |
| 积分 Integral (force \textstyle)                              | $\textstyle \int\limits_{-N}^{N} e^x dx$                       | \textstyle \int\limits_{-N}^{N} e^x dx                       |
| 积分 Integral (force \textstyle, alternative limits style)    | $\textstyle \int_{-N}^{N} e^x dx$                              | \textstyle \int_{-N}^{N} e^x dx                              |
| 双重积分 Double integral                                      | $\iint\limits_D dx\,dy$                                        | \iint\limits_D dx\,dy                                        |
| 三重积分 Triple integral                                      | $\iiint\limits_E dx\,dy\,dz$                                   | \iiint\limits_E dx\,dy\,dz                                   |
| 路径积分 Line or path integral                                | $\int_{(x,y)\in C} x^3\, dx + 4y^2\, dy$                       | \int_{(x,y)\in C} x^3\, dx + 4y^2\, dy                       |
| 环路积分 Closed line or path integral                         | $\oint_{(x,y)\in C} x^3\, dx + 4y^2\, dy$                      | \oint_{(x,y)\in C} x^3\, dx + 4y^2\, dy                      |
| 交集 Intersections                                            | $\bigcap_{i=1}^n E_i$                                          | \bigcap_{i=1}^n E_i                                          |
| 并集 Unions                                                   | $\bigcup_{i=1}^n E_i$                                          | \bigcup_{i=1}^n E_i                                          |

#### 矩阵与多行列式 Matrices & Multilines

| 类型                                                                      | 样式                                                                                                   | LaTeX                                                                                              |
| ------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------------------------------------------- |
| 二项式系数 Binomial coefficients                                          | $\binom{n}{k}$                                                                                       | \binom{n}{k}                                                                                       |
| 小型二项式系数 Small binomial coefficients (force \textstyle)             | $\tbinom{n}{k}$                                                                                      | \tbinom{n}{k}                                                                                      |
| 大型二项式系数 Large (normal) binomial coefficients (force \displaystyle) | $\dbinom{n}{k}$                                                                                      | \dbinom{n}{k}                                                                                      |
| 矩阵 Matrices                                                             | $\begin{matrix}x & y\\z & v\end{matrix}$                                                             | \begin{matrix}x & y\\z & v\end{matrix}                                                             |
|                                                                           | $\begin{vmatrix}x & y\\z & v\end{vmatrix}$                                                           | \begin{vmatrix}x & y\\z & v\end{vmatrix}                                                           |
|                                                                           | $\begin{Vmatrix}x & y\\z & v\end{Vmatrix}$                                                           | \begin{Vmatrix}x & y\\z & v\end{Vmatrix}                                                           |
|                                                                           | $\begin{bmatrix}0 & \cdots & 0\\\vdots & \ddots & \vdots \\0 & \cdots & 0\end{bmatrix}$              | \begin{bmatrix}0 & \cdots & 0\\\vdots & \ddots & \vdots \\0 & \cdots & 0\end{bmatrix}              |
|                                                                           | $\begin{Bmatrix}x & y \\z & v\end{Bmatrix}$                                                          | \begin{Bmatrix}x & y\\z & v\end{Bmatrix}                                                           |
|                                                                           | $\begin{pmatrix}x & y\\z & v\end{pmatrix}$                                                           | \begin{pmatrix}x & y\\z & v\end{pmatrix}                                                           |
|                                                                           | $\bigl( \begin{smallmatrix}a&b\\c&d\end{smallmatrix} \bigr)$                                         | \bigl( \begin{smallmatrix}a&b\\c&d\end{smallmatrix} \bigr)                                         |
| 条件定义 Case distinctions                                                | $f(n) =\begin{cases}n/2, & \text{if }n\text{ is even}\\3n+1, & \text{if }n\text{ is odd}\end{cases}$ | f(n) =\begin{cases}n/2, & \text{if }n\text{ is even}\\3n+1, & \text{if }n\text{ is odd}\end{cases} |
| 多行等式 Multiline equations                                              | $\begin{array}{lcl} z & = & a \\ f(x,y,z) & = & x + y + z \end{array}$                               | \begin{array}{lcl}z & = & a\f(x,y,z) & = & x + y + z\end{array}                                    |
|                                                                           | $\begin{array}{lcr}z & = & a\\f(x,y,z) & = & x + y + z\end{array}$                                   | \begin{array}{lcr}z & = & a\\f(x,y,z) & = & x + y + z\end{array}                                   |
| 方程组 Simultaneous equations                                             | $\begin{cases} 3x + 5y + z\\ 7x - 2y + 4z \\ -6x + 3y + 2z \end{cases}$                              | \begin{cases} 3x + 5y + z\\ 7x - 2y + 4z \\ -6x + 3y + 2z \end{cases}                              |

#### 2.5 括号 Brackets

常用的括号符号例如 `( )[ ]{ }……`这些也可以在输入环境中直接使用：

```markdown
2(x+y)=z
```

$2(𝑥+𝑦)=𝑧$

但如果是在较大的表达式中这些符号就显得不合适了

```markdown
( \frac{\pi}{2} )^n
```

$\frac{\pi}{2} $

正确用法应配合 `\left`和 `\right`命令使用。

```markdown
\left ( \frac{\pi}{2} \right )^n
```

$\left ( \frac{\pi}{2} \right )^n$

**具体可参考下表**：

| 类型                                                                                                                                 | 样式                                                                                                                                                                                                                               | LaTeX                                                                                                                                                                       |
| ------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 圆括号、小括号 Parentheses                                                                                                          | $\left ( \frac{a}{b} \right )$                                                                                                                                                                                                   | \left ( \frac{a}{b} \right )                                                                                                                                                |
| 方括号、中括号 Brackets                                                                                                              | $\left [ \frac{a}{b} \right ] \quad\left \lbrack \frac{a}{b} \right \rbrack$                                                                                                                                                     | \left [ \frac{a}{b} \right ] \quad\left \lbrack \frac{a}{b} \right \rbrack                                                                                                  |
| 花括号、大括号 Braces                                                                                                                | $\left {\frac{a}{b} \right }$                                                                                                                                                     | \left { \frac{a}{b} \right } \quad \left \lbrace \frac{a}{b} \right \rbrace                                                                                                 |
| 角括号 Angle brackets                                                                                                                | $\left \langle \frac{a}{b} \right \rangle$                                                                                                                                                                                       | \left \langle \frac{a}{b} \right \rangle                                                                                                                                    |
| 单竖线和双竖线 Bars and double bars                                                                                                  | $\left \langle \frac{a}{b} \right \rangle$                                                                                                                                                                                       | \left \langle \frac{a}{b} \right \rangle                                                                                                                                    |
| 取整函数与取顶函数 Floor and ceiling functions:                                                                                      | $\left \| \frac{a}{b} \right \vert \quad \left \Vert \frac{c}{d} \right \|$                                                                                                                                                      | `\left \| \frac{a}{b} \right \vert \quad \left \Vert \frac{c}{d} \right \|`                                                                                                 |
| 斜线与反斜线 Slashes and backslashes                                                                                                 | $\left / \frac{a}{b} \right \backslash$                                                                                                                                                                                          | \left / \frac{a}{b} \right \backslash                                                                                                                                       |
| 上下箭头 Up, down, and up-down arrows                                                                                                | $\left \uparrow \frac{a}{b} \right \downarrow \quad \left \Uparrow \frac{a}{b} \right \Downarrow \quad \left \updownarrow \frac{a}{b} \right \Updownarrow$                                                                       | \left \uparrow \frac{a}{b} \right \downarrow \quad \left \Uparrow \frac{a}{b} \right \Downarrow \quad \left \updownarrow \frac{a}{b} \right \Updownarrow                    |
| 混合括号 Delimiters can be mixed,as long as \left and \right match                                                                   | $\left [ 0,1 \right ) \left \langle \psi \right \|`                                                                                                                        | `\left [ 0,1 \right ) \left \langle \psi \right \|$ |                                                                                                                                                                             |
| 如果您不希望某一侧括号显示，可以使用\left. 和 \right.（带有英文句号）Use \left. and \right. if you do not want a delimiter to appear | $\left . \frac{A}{B} \right } \to X$                                                                                                                                                                                             | \left . \frac{A}{B} \right } \to X                                                                                                                                          |
| 括号的大小 Size of the delimiters (add "l" or "r" to indicate the side for proper spacing)                                           | $( \bigl( \Bigl( \biggl( \Biggl( \dots \Biggr] \biggr] \Bigr] \bigr] ]$                                                                                                                                                          | ( \bigl( \Bigl( \biggl( \Biggl( \dots \Biggr] \biggr] \Bigr] \bigr] ]                                                                                                       |
|                                                                                                                                      | ${ \bigl{ \Bigl{ \biggl{ \Biggl{ \dots \Biggr\rangle \biggr\rangle \Bigr\rangle \bigr\rangle \rangle$                                                                                                                            | { \bigl{ \Bigl{ \biggl{ \Biggl{ \dots \Biggr\rangle \biggr\rangle \Bigr\rangle \bigr\rangle \rangle                                                                         |
|                                                                                                                                      | $\| \big\| \Big\| \bigg\| \Bigg\| \dots \Bigg \| \bigg \| \Big \| \big \|$                                                                                                                                                       | `\| \big\| \Big\| \bigg\| \Bigg\| \dots \Bigg \| \bigg \| \Big \| \big \|`                                                                                                         |
|                                                                                                                                      | $\lfloor \bigl\lfloor \Bigl\lfloor \biggl\lfloor \Biggl\lfloor \dots \Biggr\rceil \biggr\rceil \Bigr\rceil \bigr\rceil \rceil$                                                                                                   | \lfloor \bigl\lfloor \Bigl\lfloor \biggl\lfloor \Biggl\lfloor \dots \Biggr\rceil \biggr\rceil \Bigr\rceil \bigr\rceil \rceil                                                |
|                                                                                                                                      | $\uparrow \big\uparrow \Big\uparrow \bigg\uparrow \Bigg\uparrow \dots \Bigg\Downarrow \bigg\Downarrow \Big\Downarrow \big\Downarrow \Downarrow$                                                                                  | \uparrow \big\uparrow \Big\uparrow \bigg\uparrow \Bigg\uparrow \dots \Bigg\Downarrow \bigg\Downarrow \Big\Downarrow \big\Downarrow \Downarrow                               |
|                                                                                                                                      | $\updownarrow \big\updownarrow \Big\updownarrow \bigg\updownarrow \Bigg\updownarrow \dots \Bigg\Updownarrow \bigg\Updownarrow \Big\Updownarrow \big\Updownarrow \Updownarrow$                                                    | \updownarrow \big\updownarrow \Big\updownarrow \bigg\updownarrow \Bigg\updownarrow \dots \Bigg\Updownarrow \bigg\Updownarrow \Big\Updownarrow \big\Updownarrow \Updownarrow |
|                                                                                                                                      | $/ \big/ \Big/ \bigg/ \Bigg/ \dots \Bigg\backslash \bigg\backslash \Big\backslash \big\backslash \backslash$                                                                                                                     | / \big/ \Big/ \bigg/ \Bigg/ \dots \Bigg\backslash \bigg\backslash \Big\backslash \big\backslash \backslash                                                                  |

#### 2.6 空格与换行 Spacing & Line breaking

##### 2.6.1 空格 Spacing

MathJax能够自动处理大多数空格间距的大小，但如果您需要自己控制，可参考下表。

| 序号 | 样式  | LaTeX        | 中文说明英文说明           |
| ---- | ----- | ------------ | -------------------------- |
| 1    | 𝑎𝑏  | a \qquad b   | 双空格                     |
| 2    | 𝑎𝑏  | a \quad b    | 单空格                     |
| 3    | 𝑎 𝑏 | a\ b         | 字符空格                   |
| 4    | 𝑎 𝑏 | a \text{ } b | 文本模式中的字符空格       |
| 5    | 𝑎𝑏  | a\;b         | 大空格                     |
| 6    | 𝑎𝑏  | a\,b         | 小空格                     |
| 7    | 𝑎𝑏  | ab           | 极小空格(用于乘因子)       |
| 8    | 𝑎𝑏  | a b          | 极小空格(用于区分其它语法) |
| 9    | ab    | \mathit{ab}  | 没有空格(用于多字母变量)   |
| 10   | 𝑎𝑏  | a!b          | 负空格                     |
