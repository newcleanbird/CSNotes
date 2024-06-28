# Markdown

## Markdown 简介

Markdown是一种轻量级的标记语言，由约翰·格鲁伯（John Gruber）与亚伦·斯沃茨（Aaron Swartz）于2004年共同创建。它设计的核心理念是让文本内容的编写既简单又易读，同时能够转换成结构化的HTML文档，从而实现文本的格式化和美化，而无需直接编写HTML代码。

### Markdown的定义

Markdown是一种使用纯文本格式编写的标记语言，旨在让用户以接近自然语言的方式，通过特定的符号和语法来表达文本的格式信息，如段落、标题、列表、链接、图片、代码块等。这些格式化指令在视觉上不干扰文本的阅读，使得Markdown文档即便在未经过转换的情况下也保持高度可读性。Markdown文档通常以.md或.markdown作为文件扩展名。

### 特点

1. 易读易写：Markdown语法设计得非常简单，易于学习和记忆，几乎不需要专门的培训，适合所有水平的用户快速上手。
2. 跨平台兼容：Markdown文档是纯文本格式，可以在任何文本编辑器中打开和编辑，不受操作系统限制。
3. 专注内容：Markdown鼓励作者集中精力于内容创作，而不是花费大量时间在格式调整上，提高了写作效率。
4. 转换灵活：Markdown文件可以方便地转换成多种格式，如HTML、PDF、EPUB等，满足不同场合的发布需求。
5. 广泛支持：许多网站和服务，包括GitHub、Reddit、Jekyll、GitLab等，直接支持Markdown作为内容编辑的格式，促进了其广泛应用。

### 应用领域

- 技术文档：因Markdown的简单性和对代码块的良好支持，它成为编写软件文档、API文档和技术博客的首选。
- 个人笔记：许多笔记应用（如Notion、Joplin）支持Markdown，便于组织结构化笔记。
- 项目管理：项目说明、README文件、任务列表等，Markdown使得项目信息清晰、易于维护。
- 学术写作：虽然Markdown原生支持有限，但结合扩展或工具（如Pandoc），也能用于撰写学术论文和报告。
- 在线出版：博客平台、电子书制作工具中广泛采用Markdown，便于内容创作者直接在浏览器中编写和发布内容。
- 论坛与社交媒体：部分在线论坛和社交媒体平台支持Markdown，方便用户发表格式丰富的帖子。

## Markdown语法

### 1.目录

``# 一级目录 {#top目录捏}``
``## 二级目录 {.类1 .类2}``
``### 三级目录``
``#### 四级目录``
``##### 五级目录``
``###### 六级目录``
``####### 七级没有目录 和正文一样``

如果你想要给你的标题添加 id 或者 class，请在标题最后添加 {#id .class1 .class2}。例如：

```markdown
# 这个标题拥有 1 个 id {#my_id}
# 这个标题有 2 个 classes {.class1 .class2}
```

### 2.正文

不带任何#直接输入

### 3.代码代码块

代码块通过两行 ``` 符号框出，如果你写的代码是某种语言，那么可以在第一行末尾加上这个语言的名字，代码块内的代码就会执行对应的高亮语法，例如python

``` c++ {.line-numbers}
#include <bits/stdc++.h>
using namespace std;
int main(int argc, char)
{
    cout << "hello,world!" << endl;
}
```

### 4.行内代码：``Enter``

正文中的代码，则通过输入`` 框出

### 5.列表

有序列表，输入数字，加一个句点，然后空格即可；可以缩进空置多级列表；

1. 早上吃什么
   1. 吃个鸡蛋
       1. 是哪种蛋呢
          1. 可以吃温泉蛋
             1. 水刚开放入鸡蛋，然后关火自然加热即可

2. 中午吃什么
3. 晚上吃什么
4. 夜宵就不吃了吧

无序列表，输入 - ,然后空格

- 减肥餐
- 绿色蔬菜
- 不吃米饭
- 也不能吃面条捏
  
### 6.强调--加粗和倾斜

```markdown
**加粗**
*倾斜*
*斜体*
***倾斜和加粗***
*你也 **组合** 这些符号*
~~这个文字将会被横线删除~~
``<del>``<del>这个文字也会被删除，但内部显示不会</del></del>再添加就好了
==marked== ``==marked==``被标记的
```

### 7.代码行数

如果你想要你的代码块显示代码行数，只要添加 line-numbers class 就可以了。

```javascript {.line-numbers}
function add(x, y) {
  return x + y
}
```

### 8.添加图片

Markdown插图片有三种方法，各种Markdown编辑器的插图方式也都包含在这三种方法之内。
插图最基础的格式就是：
``![Alt text](图片链接 "optional title")``

- Alt text:图片的Alt标签，用来描述图片的关键词，可以不写，最初的本意是当图片因为某种原因不能显示时而出现而代替文字，后又被用于SEO，可以方便搜索引擎Alt text 里的关键词搜索到图片。
- 图片链接:可以是图片的本地地址或者是网址。
- "optional title" 鼠标悬停于图片上会出现的标题文字，可以不写。
  
#### 插入本地图片

只需要在基础语法的括号中填入图片的位置路径即可，支持绝对路径和相对路径。
例如：
![QQ Logo](头像.jpg "好看的头像")

#### 插入网络图片

- 格式一样地址换成网络图片的地址即可。
![avatar](https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fc-ssl.duitang.com%2Fuploads%2Fblog%2F202107%2F19%2F20210719150601_4401e.thumb.1000_0.jpg&refer=http%3A%2F%2Fc-ssl.duitang.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=auto?sec=1682471023&t=55cbf63aa3df6c5f53391dc11f636168)

#### 把图片存入markdown文件

用base64转码工具把图片转成一段字符串，然后把字符串填到基础格式中链接的那个位置。
基础用法：
``![avatar](data:image/png;base64,iVBORw0......)``
这个时候会发现插入的这一长串字符串会把整个文章分割开，非常影响编写文章时的体验。如果能够把大段的base64字符串放在文章末尾，然后在文章中通过一个id来调用，文章就不会被分割的这么乱了。
比如：

```markdown
![avatar][doge] 
[doge]:data:image/png;base64,iVBORw0...... 
```

具体base 64 格式需要自己去转换，感觉很麻烦，先空着以后写。

### 9.链接

格式：
``[GitHub](https://github.com)``
[GitHub](https://github.com)

### 10.引用

正如 Kanye West 所说：
> We're living the future so
> the present is our past.

### 11.分割线

```markdown
如下，三个或者更多的
---
连字符
---
星号
---
下划线
```

### 12.任务列表

```markdown
- [x] @mentions, #refs, [links](https://google.com), **formatting**, and <del>tags</del> supported
- [x] list syntax required (any unordered or ordered list supported)
- [x] this is a complete item
- [ ] this is an incomplete item
```

### 13.表格

| 左对齐 | 居中对齐 | 右对齐 |
| :----- | :------: | -----: |
| 1      |   张三   |   17岁 |
| 2      |   李四   |   18岁 |
| 3      |   五王   |   19岁 |

### 公式

1. 行内公式
    对于行内公式，你需要使用一对 `\( 和 \)` 包围你的 `LaTeX` 公式代码。例如，要在文本中插入平方根公式，可以这样写：

    ```markdown
    这是一个行内公式: \( \sqrt{x} = y \)。
    ```

    这是一个行内公式: \( \sqrt{x} = y \)。

2. 块级公式

块级公式则使用一对 `$$` 或者 `\[\]` 包围。例如：

```markdown
$$
\begin{align}
y &= mx + b \\
E &= mc^2
\end{align}
$$
```

或者

```markdown
\[
\begin{align}
y &= mx + b \\
E &= mc^2
\end{align}
\]
```

## 扩展的语法

### 1.表格
>
> 需要在插件设置中打开 enableExtendedTableSyntax 选项来使其工作。

### 2.Emoji & Font-Awesome
>
>只适用于 markdown-it parser 而不适用于 pandoc parser。
缺省下是启用的。你可以在插件设置里禁用此功能。
:smile:``:smile:``
:fa-car:``:fa-car:``

### 3.上标

30^th^

### 4.下标

H~2~O

### 5.脚注

Content [^1]

[^1]: Hi! This is a footnote

### 6.缩略(鼠标悬停显示)

*[HTML]: Hyper Text Markup Language
*[W3C]: World Wide Web Consortium
The HTML specification is maintained by the W3C.

### 7.标记

==marked==

### 8.CriticMarkup

CriticMarkup 缺省是禁用的，你可以通过插件设置来启动它。
有关 CriticMarkup 的更多信息，请查看[CriticMarkup 用户指南](https://criticmarkup.com/users-guide.php)
这里有 5 种基本语法：
添加 ``{++ ++}``
删除 ``{-- --}``
替换 ``{~~ ~> ~~}``
注释 ``{>> <<}``
高亮 ``{== ==}{>> <<}``
>CriticMarkup 仅可用于 markdown-it parser，不与 pandoc parser 兼容。

### 9.Admonition(告诫、警告、提示)

!!! note This is the admonition title
    This is the admonition body

```markdown
格式：
!!! note This is the admonition title
    This is the admonition body
```

>请在 [https://squidfunk.github.io/mkdocs-material/reference/admonitions](https://squidfunk.github.io/mkdocs-material/reference/admonitions/) 查看更多信息

## 支持数学公式

Markdown Preview Enhanced 使用 [KaTeX](https://github.com/KaTeX/KaTeX) 或者 [MathJax](https://github.com/mathjax/MathJax) 来渲染数学表达式。

KaTeX 拥有比 MathJax 更快的性能，但是它却少了很多 MathJax 拥有的特性。你可以查看 [KaTeX supported functions/symbols](https://khan.github.io/KaTeX/function-support.html) 来了解 KaTeX 支持那些符号和函数。

默认下的分隔符：

- `$...$` 或者 `\(...\)` 中的数学表达式将会在行内显示。
- `$$...$$`或者 `\[...\]` 或者 ````math` 中的数学表达式将会在块内显示。
