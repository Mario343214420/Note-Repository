## 1. 基本选择器

### 1.1 子元素选择器

1)定义：只能选择某元素的子元素

2)语法：父元素>子元素

### 1.2 相邻兄弟选择器

1)定义：可以选择紧接着在另外一个元素后的元素，而且他们具有一个相同的父元素

2)语法：元素 + 相邻兄弟元素

### 1.3 通用兄弟选择器

1)定义：选择某元素后边的所有兄弟元素，而且他们具有一个共同的父亲

2)语法：元素 ~ 后面所有兄弟元素

### 1.4 群组选择器 

1)定义：将具有相同样式的元素分组在一起，每个选择器之间用逗号 ， 隔开

2) 语法：元素1，元素2，元素3，.......


## 2. 属性选择器 

### 2.1 element[attribute] 

1)定义： 为带有attribute属性的元素设置样式  

2)语法：element[attribute]

### 2.2 element[attribute='value'] 

1) 定义：为attribute='value'属性的元素设置样式

2)语法：element[attribute='value']

### 2.3 element[attribute~='value'] 

1) 定义：选择attribute属性包含单词value的元素,并设置样式

2) 语法：element[attribute~='value']

### 2.4 element[attribute^='value'] 

1) 定义：设置attribute属性值，以value开头的所有元素样式

2)语法：element[attribute^='value']

### 2.5 element[attribute$='value'] 

1) 定义：设置attribute属性值，以value结尾的所有元素样式

2) 语法：element[attribute$='value']

### 2.6 element[attribute\*='value'] 

1)定义：设置attribute属性值，包含value的所有元素，并为其设置样式

2)语法：element[attribute*='value']


## 3. 动态伪类 

### 3.1 锚点伪类 

1):link  

2):visited

### 3.2 用户行为伪类 

1) :hover 

2)  :active

3)  :focus

### 3.3 目标伪类 

:target 当我们点击锚链接时，对应ID的元素会显示在视口


### 3.4 checked状态伪类 

1) checkbox:只能设置宽度和高度，不能设置背景颜色和边框

2) 清除input的默认样式 appearance: none;

### 3.5 CSS3结构类 

1)  first-child：选择属于其父元素的首个子元素的每个element元素，并为其设置样式（element:first-child）

2) last-child：.为其设置样式（element:last-child）

3) nth-child(n)：选择某元素下第number个element元素（n是一个简单的表达式，不能用其他字母代替，n从0开始计算）

1.nth-child(odd) : 可用于匹配下标是奇数的元素的关键字

2.nth-child(even):可用于匹配下标是偶数的元素的关键字

4)  nth-last-child()：匹配属于其元素的第n个元素的每个元素，从最后一个子元素开始计数(element:nth-last-child(n))

5)  nth-of-type()：匹配属于父元素的特定类型的第n个子元素（element:nth-of-type()）

6)  nth-last-of-type()：选匹配属于父元素的特定类型的第n个子元素，从最后一个开始计数(element:nth-last-of-type()）

7)  first-of-type()：匹配属于其父元素的特定类型的首个子元素的每个元素（element：first-of-type()）

8)  last-of-type()：匹配属于其父元素的特定类型的最后一个子元素的每个元素（element：last-of-type()）

9)  :only-child：匹配属于其父元素的唯一子元素的每个元素（element:only-child）

10)  :only-of-type：匹配属于其父元素特定类型的唯一子元素的每个元素（element :only-of-type）

11)  :empty：匹配没有子元素（包括文本节点）的每个元素（element :empty ---- div:empty）


## 4. 否定选择器 

### 4.1 定义 

匹配非 元素或者选择器 的每个元素

### 4.2 语法 

父元素：not(子元素或者选择器)

ul  :not(span)


## 5. 伪元素 

### 5.1 element::first-line 

对元素的第一行文本进行设置，只能用于块级元素

### 5.2 element::first-letter 

用于向文本的首字母设置特殊样式，只能用于块级元素

### 5.3 element::before 

在元素的内容前面插入新内容，常与content配合使用

### 5.4 element::after 

在元素的内容后面插入新内容，常与content配合使用

### 5.5 element::selection 

用于设置浏览器中选中文本后的背景色与前景色

### 5.6 伪元素与元素的区别 

无法通过JS获取其DOM，无法通过浏览器直接查看

伪元素默认是 inline

### 5.7 使用伪元素注意事项 

1)使用伪元素before,after必须设置content

2)使用伪元素before,after显示背景图，一定要使用display设置为块元素

3)使用伪元素before,after设置为display:inline-block,需要再次设置vertcal-align:middle