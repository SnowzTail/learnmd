# Markdown 教程

作为一种轻量级标记语言, Markdown使用易读写的纯文本格式帮助文档排版, 并且转换成HTML格式. 熟悉基本语法之后, 用户可以轻松地读写文本.

---

## 目录

- [标题](#标题)
- [引用](#引用)
- [字体](#字体)
- [分割](#分割)
- [列表](#列表)
- [链接](#链接)
- [图片](#图片)
- [代码](#代码)
- [表格](#表格)
- [HTML](#html)
- [CSS](#css)
- [参考](#参考)

---

## 标题

用 '#' 表示标题, '#' 的个数 (1-6) 对应H1 - H6. 在 '#' 与标题内容之间需要有空格.

```
Eg. Headers

    # H1 Header
    ## H2 Header
```

# H1 Header
## H2 Header

---

## 引用

用 '>' 表示文本引用. 记得加上空格!

```
Eg. Quotes

    > Markdown is a lightweight markup language with plain text formatting syntax.
```

> Markdown is a lightweight markup language with plain text formatting syntax.

多级引用就用多个'>'.

```
Eg. Quotes within quotes

    > Markdown is a lightweight markup language with plain text formatting syntax. 
    >
    >> It is designed so that it can be converted to HTML and many other formats using a tool by the same name.
```

> Markdown is a lightweight markup language with plain text formatting syntax. 
    >
    >> It is designed so that it can be converted to HTML and many other formats using a tool by the same name.

引用和标题也可以结合~

```
Eg. Quotes + Headers

    > ### H3 Quote
```

> ### H3 Quote

---

## 字体

### 斜体

在内容前后都加上 '*' 或 '_' 表示斜体强调 (不需要空格).

```
Eg. Italics

    *Italics* = _Italics_
```

*Italics*

### 粗体

在内容前后都加上两个 '*' 或 '_' 表示粗体强调 (不需要空格).

```
Eg. Bold

    **Bold** = __Bold__
```

**Bold**

粗斜体用三个'*' 或 '_' 表示 (不需要空格).

```
Eg. Bold italic
    ***Bold italic*** = ___Bold italic___
```

***Bold italic***

> 相比使用 '_' 我更喜欢 '*', 因为前者被认为是词的一部分, 与内容同时被选中.

### 删除

在内容前后都加上两个 '~' 表示删除线 (不需要空格).

```
Eg. Strikethrough
    ~~Strikethrough~~
```

~~Strikethrough~~

---

## 分割

用连续的三个或更多的 '-', '_' 或者 '*' 添加一条分割线.

```
Eg. Horizontal Rules

    ---
```

---

## 列表

### 无序列表

无序列表以 '-', '*', '+' 开头. 空格后加内容.

```
Eg. Unordered lists

    - item
    * item
    + item
```

- item
* item
+ item

子项目用额外缩进表示.

```
Eg. Indenting

    - item
        - subitem
    - item
```

- item 
    - subitem
- item

### 有序列表

有序列表以数字前缀开头. 空格后加内容.

```
Eg. Ordered lists

    1. item 1
        1. item 1.1
        2. item 1.2
    2. item 2
    3. item 3
```

1. item 1
    1. item 1.1
    2. item 1.2
2. item 2
3. item 3

---

## 链接

### 原始链接

原始链接用 '<' '>' 包括.

```
Eg. Links

    <https://snowztail.com/>
```

<https://snowztail.com/>

### 文字链接

文字链接用 '[' ']' 包括文字, 紧接着用 '(' ')' 包括链接.

```
Eg. Links with text

    [SnowzTail's Blog](https://snowztail.com/)
```

[SnowzTail's Blog](https://snowztail.com/)

### 重用链接

需要多次使用同一链接时, 用 '[' ']' ':' 和序号给链接分配一个key:

```
Eg. Defining the reference

    [link_1]: https://snowztail.com/
```

[link_1]: https://snowztail.com/

这个key就对应了相应链接. 调用时使用如下格式:

```
Eg. Calling the reference

    [SnowzTail's Blog][link_1]
```

[SnowzTail's Blog][link_1]

这样就可以避免因为修改链接而更改多处内容.

### 锚点

锚点是一种页面内的超级链接. 理论上通过确切的ID能够指向文章内任何元素所在的位置. 常用锚点链接到同一篇Markdown文章内的不同章节. 

当创建标题时, Markdown同时通过标题名称生成对应ID. 

``
Eg. # Header -> `<h1 id="header">Header</h1>`
``

根据命名规则, 空格将会被连字符替代, 大写会被小写替代 (与CSS命名规则类似).

``
Eg. 'Header Info' -> header-info
``

本文目录索引是通过锚点实现的.

```
Eg. Contents

    - [标题](#标题)
    - [引用](#引用)
    - [字体](#字体)
    - [分割](#分割)
    - [列表](#列表)
    - [链接](#链接)
    - [图片](#图片)
    - [代码](#代码)
    - [表格](#表格)
    - [HTML](#html)
    - [CSS](#css)
    - [参考](#参考)
```

---

## 图片

定义图片与定义链接的用法相似, 只是以 '!' 开头.

```
Eg. Pic (via [Pixiv - Bison倉鼠](https://www.pixiv.net/member.php?id=333556))

    ![☆](https://snowztail.com/wp-content/uploads/2018/06/68748564_p0.jpg)
```

![☆](https://snowztail.com/wp-content/uploads/2018/06/68748564_p0.jpg)

也可以通过key调用:

```
Eg. Defining the reference

    [pic_1]: https://snowztail.com/wp-content/uploads/2018/06/68748564_p0.jpg
```

[pic_1]: https://snowztail.com/wp-content/uploads/2018/06/68748564_p0.jpg

```
Eg. Calling the reference

    ![☆][pic_1]
```
![☆][pic_1]

---

## 代码

使用 反引号 '`' 表示代码.

### 单个对象

一组反引号表示单个对象.

```
Eg. Object

    `Object`
```

`Object`

### 单行代码

两组反引号表示单行代码.

```
Eg. Inline code 

    ``
    Inline code
    ``
```

``
Inline code
``

### 代码块

三组反引号表示代码块.

```
Eg. Code block

    ```
    Code
    block
    ```
```

```
Code
block
```

> 在 ``` 后添加语言名称实现语法高亮.

#### Go

```go
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}
```
#### Java

```java
public class HelloWorld {

    public static void main(String[] args) {
        System.out.println("Hello World!");
    }

}
```

---

## 表格

列间用 '|' 分隔, 行间用 '-' 分隔. 注意, 要分隔行, 表头和元素间至少需要三个 '-'.

为了增加可读性, 建议将表格列对齐. 下面两个例子的效果相同.

```
Eg. Not aligned table

    | Header 1 | Header 2 |
    | ----| ---|
    |Loooooooooooooong item 1 | looooooooooong item 2 |


    Aligned table

    | Header 1                | Header 2              |
    | ----------------------- | --------------------- |
    |Loooooooooooooong item 1 | looooooooooong item 2 |
```

| Header 1                | Header 2              |
| ----------------------- | --------------------- |
|Loooooooooooooong item 1 | looooooooooong item 2 |

在单元格中可以控制内容居左 / 中 / 右, 通过在分隔行内添加 ':' 实现:

 - 居左: 默认, 无需添加 ':'
 - 居中: 在 '-' 分隔块左右各加上一个 ':'
 - 居右: 在 '-' 分隔块右边加上一个 ':'

```
Eg. Align scheme
    | Header | Header 1 | Header 2  |
    | ------ | :------: | --------: |
    | Aligned Left | Aligned Center | Aligned Right | 
```

| Header | Header 1 | Header 2  |
| ------ | :------: | --------: |
| Aligned Left | Aligned Center | Aligned Right |

---

## HTML

通过以下格式添加自定义 HTML.

```html 
<p>Sample HTML Div</p>
```

<p>Sample HTML Div</p>

---

## CSS

通过以下格式添加自定义 CSS.

```html
    <style>
        body {
            color:red;
        }
    </style>
```

---

## 参考

- [James Q Quick - Markdown Worksheet](https://github.com/jamesqquick/markdown-worksheet)

- [Coding.net - Markdown 语法介绍](https://coding.net/help/doc/project/markdown.html)

- [Hacpai - Markdown 教程](https://blog.csdn.net/chenriyang0306/article/details/77259017)
