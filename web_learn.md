[TOC]
# web开发学习
---
## HTML
是一种描述网页的超文本标记语言。标记语言即用**标记标签**和文本内容共同组成文档。即学习如何用特定的标记标签使文本呈现特定的形式。文件的保存格式为.htm或.html，两者无区别，建议统一用.html。

---
### HTML页面的组成
@import "HTML页面组成.jpg"
- \<!DOCTYPE html> 声明为HTML5文档（不区分大小写）
- \<html> 元素是 HTML 页面的根元素
- \<head> 元素包含了文档的元（meta）数据，如 \<meta charset="utf-8"> 定义网页编码格式为 utf-8。注：对于中文网页需要使用 <meta charset="utf-8"> 声明编码，否则会出现乱码。有些浏览器(如 360 浏览器)会设置 GBK 为默认编码，则你需要设置为 <meta charset="gbk">。
- \<title> 元素描述了文档的标题
- \<body> 元素包含了可见的页面内容
- \<h1> 元素定义一个大标题
- \<p> 元素定义一个段落

---

### HTML标签（HTML tag）的特点
- 由尖括号包围成的关键词，比如<HTML>
- 通常成对出现，如<body>和</body>。标签对中第一个为开始标签，第二个为结束标签。
- 开始和结束标签也被称为开放标签和闭合标签。
- 形式一般为<标签>内容</标签>

---
### HTML基本语法
- 标题（heading）：通过\<h1>~\<h6>标签定义（级别和字体大小依次递减）。\<h1>标题\</h1>。（确保将 HTML 标题 标签只用于标题。不要仅仅是为了生成粗体或大号的文本而使用标题。因为搜索引擎使用标题为网页的结构和内容编制索引。）
- 段落：通过\<p>标签定义。\<p>段落内容\</p>。（注意段落中的连续多个空格和换行都只能呈现出一个空格，若要表现多个空格和换行，可用\<pre>标签。
- 链接：通过\<a>标签定义。\<a href="https://www.runoob.com"> 对链接的描述(不一定是文本，也可以是图片或其它html元素)\</a>。 在href属性中定义链接的地址。
  - target属性：可以定义被链接的文档在何处显示。下面的这行会在新窗口打开文档：
  \<a href="https://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!\</a> 。将 target 属性设置为 "_blank", 链接将在新窗口打开。
  - id属性：可用于创建一个 **HTML 文档书签**，即跳转到当前页面指定的部位或其他页面指定的部位，常用于创建跳转到页面最顶端的书签。在要跳转到的部分前插入“\<a id="tips">要跳转的部分\</a>”，在需要启动跳转的地方插入“\<a href="#tips">跳转到\</a>”，或者从另一个页面创建一个链接到"要跳转的部分(id="tips"）"：\<a href="https://www.runoob.com/html/html-links.html#tips">跳转到\</a>。实例参见[此处](https://www.runoob.com/try/try.php?filename=tryhtml_link_locations&basepath=0)。
- 图片：通过\<img>标签定义。如\<img src="H:\learn_code_note\HTML页面组成.jpg" width="256" height="66"/>
- 换行：\<br/>，"/"表示关闭
- 分隔水平线：\<hr> 标签在 HTML 页面中创建水平线。\<hr/>
- 注释：\<!-- 这是一个注释 -->，提高其可读性，使代码更易被人理解。浏览器会忽略注释，也不会显示它们。
- 文本格式化标签：
  | 标签      | 描述                       |
  | --------- | -------------------------- |
  | \<b>      | 定义粗体文本               |
  | \<em>     | 定义着重文字，效果等同斜体 |
  | \<i>      | 定义斜体文本               |
  | \<small>  | 定义小号字                 |
  | \<strong> | 定义加重语气，等同粗体     |
  | \<sub>    | 定义下标字                 |
  | \<sup>    | 定义上标字                 |
  | \<ins>    | 定义插入字                 |
  | \<del>    | 定义删除字                 |
- 计算机输出标签
  | 标签    | 描述               |
  | ------- | ------------------ |
  | \<code> | 定义计算机代码     |
  | \<kbd>  | 定义键盘码         |
  | \<samp> | 定义计算机代码样本 |
  | \<var>  | 定义变量           |
  | \<pre>  | 定义预格式文本     |
- HTML 引文, 引用, 及标签定义
  | 标签          | 描述               |
  | ------------- | ------------------ |
  | \<abbr>       | 定义缩写           |
  | \<address>    | 定义地址           |
  | \<bdo>        | 定义文字方向       |
  | \<blockquote> | 定义长的引用       |
  | \<q>          | 定义短的引用语     |
  | \<cite>       | 定义引用、引证     |
  | \<dfn>        | 定义一个定义项目。 |
- \<head>元素：包含了所有的头部标签元素。在 <head>元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。可以添加在头部区域的元素标签为: \<title>, \<style>, \<meta>, \<link>, \<script>, \<noscript> 和 \<base>。
- \<base> 元素：描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接。如：\<base href="http://www.runoob.com/images/" target="_blank">,指定了页面上所有链接的默认 URL,链接会在新窗口打开.
- \<style> 元素：定义了HTML文档的样式文件引用地址。在\<style> 元素中也可以直接添加样式来渲染 HTML 文档。\<style type="text/css">body {background-color:yellow}p {color:blue}\</style>。
- \<meta> 元素:描述了一些基本的元数据。元数据也不显示在页面上，但会被浏览器解析。META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。\<meta> 一般放置于 \<head> 区域
- 使用 \<span> 元素对文本中的一部分进行着色：\<p>我的母亲有 \<span style="color:blue">蓝色\</span> 的眼睛。\</p>
---
### HTML元素
HTML 文档由 HTML 元素定义。
- HTML 元素以开始标签起始
- HTML 元素以结束标签终止
- 元素的内容是开始标签与结束标签之间的内容
- 某些 HTML 元素具有空内容（empty content）
- 空元素在开始标签中进行关闭（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有属性
- 大多数 HTML 元素可以嵌套（HTML 元素可以包含其他 HTML 元素）。HTML 文档由相互嵌套的 HTML 元素构成。
- 所有元素都必须被关闭，不管是单体标签还是成对标签。虽然有些浏览器能兼容无关闭的元素，但严格意义上不可行。
- html对大小写不敏感，但建议使用小写标签。
  
---
### HTML属性
属性是 HTML 元素提供的附加信息。
- HTML 元素可以设置属性
- 属性可以在元素中添加附加信息
- 属性一般描述于开始标签
- 属性总是以名称/值对的形式出现，比如：name="value"。
- 属性实例：链接通过\<a>标签定义，在href属性中定义链接的地址。如：\<a href="https://www.runoob.com"> 对链接的描述\</a>
- 属性值应该始终被包括在引号内。双引号是最常用的，不过使用单引号也没有问题。提示: 在某些个别的情况下，比如属性值本身就含有双引号，那么必须使用单引号，例如：name='John "ShotGun" Nelson'
- 属性和属性值对大小写不敏感。推荐使用小写。
- 适用于大多数 HTML 元素的属性：
  | 属性  |                             描述                              |
  | ----- | :-----------------------------------------------------------: |
  | class | 为html元素定义一个或多个类名（classname）(类名从样式文件引入) |
  | id    |                       定义元素的唯一id                        |
  | style |              规定元素的行内样式（inline style）               |
  | title |             描述了元素的额外信息 (作为工具条使用)             |

- 查看完整的HTML属性列表:  [HTML 标签参考手册](https://www.runoob.com/tags/html-reference.html)。
- 更多标准属性说明： [HTML 标准属性参考手册](https://www.runoob.com/tags/ref-standardattributes.html)。

### HTML表格
表格由 \<table> 标签来定义。每个表格均有若干行（由 \<tr> 标签定义），每行被分割为若干单元格（由 \<td> 标签定义）。字母 td 指表格数据（table data），即数据单元格的内容。数据单元格可以包含文本、图片、列表、段落、表单、水平线、表格等等。表格的表头使用 \<th> 标签进行定义。大多数浏览器会把表头显示为粗体居中的文本。border为边框属性，若不设置则默认无边框。
- \<table border="1">
  \<tr>
        \<th>Header 1\</th>
        \<th>Header 2\</th>
  \</tr>
   \<tr>
        \<td>row 1, cell 1\</td>
        \<td>row 1, cell 2\</td>
    \</tr>
    \<tr>
        \<td>row 2, cell 1\</td>
        \<td>row 2, cell 2\</td>
    \</tr>
\</table>
- 更多细节参见[菜鸟教程](https://www.runoob.com/html/html-tables.html)
  
### HTML列表
无序列表和有序列表，参见[菜鸟教程](https://www.runoob.com/html/html-lists.html)

### HTML布局
大多数网站会把内容安排到多个列中（就像杂志或报纸那样）。
大多数网站可以使用\<div> 或者 \<table> 元素来创建多列。CSS 用于对元素进行定位，或者为页面创建背景以及色彩丰富的外观。
- 更多细节参见[菜鸟教程](https://www.runoob.com/html/html-layouts.html)
  
### HTML表单
HTML 表单用于收集用户的输入信息。比如：文本域（textarea）、下拉列表（select）、单选框（radio-buttons）、复选框（checkbox） 等。
HTML 表单表示文档中的一个区域，此区域包含交互控件，将用户收集到的信息发送到 Web 服务器。
- 实例-一个普通输入框和一个秘密输入框：\<form action="">
Username: \<input type="text" name="user">\<br>
Password: \<input type="password" name="password">
\</form>
- 多数情况下被用到的表单标签是输入标签 \<input>。输入类型是由 type 属性定义。
- \<input type="radio"> 标签定义了表单的单选框选项:\<form action="">
\<input type="radio" name="sex" value="male">男\<br>
\<input type="radio" name="sex" value="female">女
\</form>
- \<input type="checkbox"> 定义了复选框。
- \<input type="submit"> 定义了提交按钮。当用户单击确认按钮时，表单的内容会被传送到服务器。表单的动作属性 action 定义了服务端的文件名。action 属性会对接收到的用户输入数据进行相关的处理:\<form name="input" action="html_form_action.php" method="get">
Username: \<input type="text" name="user">
\<input type="submit" value="Submit">
\</form>
- 更多细节参见[菜鸟教程](https://www.runoob.com/html/html-forms.html)
  
### HTML框架
通过使用框架，可以在同一个浏览器窗口中显示不止一个页面。

### HTML颜色
HTML 颜色由红色、绿色、蓝色混合而成。由一个十六进制符号来定义，这个符号由红色、绿色和蓝色的值组成（RGB）。
每种颜色的最小值是0（十六进制：#00）。最大值是255（十六进制：#FF）。#FF0000对应	rgb(255,0,0)
- 141个颜色名称是在HTML和CSS颜色规范定义的（17标准颜色，再加124）。17标准颜色：黑色，蓝色，水，紫红色，灰色，绿色，石灰，栗色，海军，橄榄，橙，紫，红，白，银，蓝绿色，黄色。详见[菜鸟教程](https://www.runoob.com/html/html-colornames.html)。

### HTML脚本
JavaScript 使 HTML 页面具有更强的动态和交互性。
- 使用 \<noscript> 标签应对不支持脚本或禁用脚本的浏览器。

### HTML速查笔记
常用标签用法，见[菜鸟教程](https://www.runoob.com/html/html-quicklist.html)
标签缩写及全称，见[菜鸟教程](https://www.runoob.com/html/html-tag-name.html)

### HTML媒体
  音频视频播放，见[菜鸟教程](https://www.runoob.com/html/html-media.html)

### 简单css
CSS (Cascading Style Sheets) 是用于渲染HTML元素标签的样式。
CSS 可以通过以下方式添加到HTML中:
- 内联样式- 在HTML元素中使用"style" 属性
  -  当特殊的样式需要应用到个别元素时，就可以使用内联样式。 使用内联样式的方法是在相关的标签中使用样式属性。样式属性可以包含任何 CSS 属性。
  - 举例：
  1、改变段落的颜色和左外边距。\<p style="color:blue;margin-left:20px;">这是一个段落。\</p>
  2、背景色属性（background-color）:\<body style="background-color:yellow;">\<h2 style="background-color:red;">这是一个标题\</h2>\</body>
  3、使用font-family（字体），color（颜色），和font-size（字体大小）属性来定义字体的样式:\<p style="font-family:arial;color:red;font-size:20px;">一个段落。\</p>
  4、使用 text-align（文字对齐）属性指定文本的水平与垂直对齐方式：\<h1 style="text-align:center;">居中对齐的标题\</h1>

- 内部样式表 -在HTML文档头部 \<head> 区域使用\<style> 元素 来包含CSS
  - 当单个文件需要特别样式时，就可以使用内部样式表。可以在\<head> 部分通过 \<style>标签定义内部样式表。
  - 举例：\<head>
\<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
\</style>
\</head>
- 外部引用 - 使用外部 CSS 文件
  - 当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，就可以通过更改一个文件来改变整个站点的外观。
  - 举例：\<head>
\<link rel="stylesheet" type="text/css" href="mystyle.css">
\</head>

---
## CSS

---
## Javascript
