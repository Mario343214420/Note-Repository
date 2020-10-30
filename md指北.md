# md 指北攻略

## Markdown

> Markdown 是一种轻量级标记语言，创始人为约翰·格鲁伯（John Gruber）。它允许人们「使用易读易写的纯文本格式编写文档，然后转换成有效的XHTML(或者HTML)文档 」—— 维基百科>Markdown具有一系列衍生版本，用于扩展Markdown的功能（如表格、脚注、内嵌HTML等等），这些功能原初的Markdown尚不具备，它们能让Markdown转换成更多的格式，例如LaTeX，Docbook。Markdown增强版中比较有名的有Markdown Extra、MultiMarkdown、 Maruku等。这些衍生版本要么基于工具，如Pandoc；要么基于网站，如GitHub和Wikipedia，在语法上基本兼容，但在一些语法和渲染效果上有改动。如果你看不懂以上对 Markdown 的定义，那也无所谓。约翰·格鲁伯自己对Markdown的描述的重点也在于

## 标题

### 第一类（常规）

```md
# 一级标题
## 二级标题
### 三级标题
...
```

### 第二类（添加结束符）

```md
# 一级标题 #
## 二级标题 ##
### 三级标题 ###
...
```

### 第三类（--或==多于一个即可）

```md
一级标题           >     <h1>一级标题</h1>
=========
一级标题
---------
```

优点：代码结构划分直观

## 列表

### 第一类（无序）

```md
### 无序列表
* 1                             · 1       
+ 1            > 预览            · 1
- 1                             · 1 
```

```md
<ul>
  <li>1</li>
  <li>1</li>
  <li>1</li>
</ul>
```

### 第二类（有序）

```md
### 有序列表
1. 列表                            1. 列表     
2. 列表            > 预览          2. 列表
3. 列表                            3. 列表

！数字后面的点只能是英文点
！！有序列表的序号是根据第一行列表的数字顺序来的
```

```md
<ol>
  <li>列表</li>
  <li>列表</li>
  <li>列表</li>
</ol>
```

## 引用

```md
> 这是一段引用代码
```

引用会自动生成左侧标记和背景色区分

## 分割线

```md
***
---
```

两种分割线皆可

## 链接

### 第一类（行内链接）

```md
[Windows/Mac/Linux 全平台客户端](https://www.zybuluo.com/cmd/)
```

```md
<p><a href="https://www.zybuluo.com/cmd/">Windows/Mac/Linux 全平台客户端</a></p>
```

另一种 行外添加前缀文字或其他内容即可，不赘述。

### 第二类（参数链接）

```md
[Windows/Mac/Linux 全平台客户端](https://www.zybuluo.com/cmd/ 'title属性')
```

```md
<p><a href="https://www.zybuluo.com/cmd/" title="title属性">Windows/Mac/Linux 全平台客户端</a></p>
```

## 图片

```md
![cmd-markdown-logo](https://www.zybuluo.com/static/img/logo.png)
```

```md
<p><img src="https://www.zybuluo.com/static/img/logo.png" alt="cmd-markdown-logo" title="" /></p>
```

## 代码

### 第一类（单行）

```md
`代码内容`
```

### 第二类（段落）

```md
​```md(this is type)
代码内容
​```
```

## 文本样式

```md
  *字体倾斜*                >        <em>字体倾斜</em>
  _字体倾斜_
  **字体加粗**              >        <strong>字体加粗</strong>
  __字体加粗__
  ~~字体删除~~              >        <del>字体删除</del>

  ! 符号与字体之间不要有空格
```

## 加强的代码块（存疑，暂认为代码类型加强）

```md
非代码示例：
    ` ` `
      $ sudo apt-get install vim-gnome
    ` ` `
```

```md
$ sudo apt-get install vim-gnome
```

## 表格

```md
| 项目        | 价格    |  数量   |
| --------    | -----: | :----:  |
| 计算机      | \$1600  |   5    |
| 手机        |   \$12  |   12   |
| 管线        |    \$1  |   234  |

: 是对齐方向
```
---
* Done is better than perfect——Facebook Office
* 完成比完美更好
* Go big or go home——Facebook Office
* 要么牛逼，要么滚蛋
* Talk is cheap. Show me the code.——Linus Torvalds
* 能说算不上什么，有本事就把你的代码给我看看
* You build it, You run it. ——Werner Vogels 

* Stay hungry Stay foolish. ——Jobs
* 求知若饥，虚心若愚
* Eat our own dog food. ——Term
* dog food: 内部测试版本

## 脚注
生成一个脚注1[^1].
脚注1 [^1]:这里是 **脚注** 的 *内容*.
生成一个脚注2[^2].
脚注2 [^2]: 这里是**脚注2**的*内容*.

## 占位符
```
&ensp; or &#8194;  表示一个半角的空格
&emsp; or &#8195;  表示一个全角的空格
&emsp;&emsp;  两个全角的空格（用的比较多）
&nbsp; or &#160;  不断行的空白格
```

## 强调标记
```
*斜体*或_斜体_

**粗体**

***加粗斜体***

~~删除线~~

<u>下划线</u>

用数学公式：
下划线 $\underline{X}$
上划线 $\overline{X}$
```