[TOC]
# web开发学习

---
---
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
- \<ul> 定义无序列表，\<ol>则定义有序列表
    \<ul>
    \<li>Coffee\</li>
    \<li>Tea\</li>
    \<li>Milk\</li>
    \</ul>
- \<footer> 定义文档的页脚

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
---
## CSS

---
---
## Javascript

---
---
## flask
flask 是使用 Python 编写的 Web 微框架。Web 框架可以让我们不用关心底层的请求响应处理，更方便高效地编写 Web 程序。因为 Flask 核心简单且易于扩展，所以被称作微框架。Flask 有两个主要依赖，一个是 WSGI (Web Server Gateway Interface, Web 服务器网关接口）工具集 Werkzeug (http: //werkzeug.pocoo.org ），另一个是 Jinja2 模板引擎 http: //jinja.pocoo.org 。Flask 只保留了 Web 开发的核心功能，其他的功能都由外部扩展来实现。以下内容主要学习自《Flask Web 开发实战：入门、进阶与原理解析 (李辉) 》和《flask入门教程（李辉）》。

---
### flask基础
#### 一、搭建安装环境
- Pipenv工作流
  - 安装Pipenv包
  Pipenv 是基于pip的Python包管理工具，是pip、pipfile、Virtualenv的结合体，它让包安装、包依赖管理和虚拟环境管理更加方便，使用它可以实现高效的Python项目开发工作流。
  - 创建虚拟环境
  通过创建虚拟环境，可以拥有一个独立的 Python 解释器环境，这样做的好处是可以为每个项目创建独立的 Python 解释器环境，因为不同的项目常常会依赖不同版本的库或 Python 版本 使用虚拟环境可以保待全局 Python 解释器环境的干净，避免包和版本的混乱，并且可以方便地区分和记录每个项目的依赖，以便在新环镜复现依赖环境。
  - Pipfile管理依赖包
- 安装flask
  - 在虚拟环境下运行pip install flask安装flask，同时被安装的还有五个依赖包。如下：
    | 包名称       |                              说明                              | 资源                                                                                                                |
    | ------------ | :------------------------------------------------------------: | ------------------------------------------------------------------------------------------------------------------- |
    | Jinja2       |                          模板渲染引擎                          | 主页:http://jinja.pocoo.org/<br>源码:https://github.com/pallets/jinja<br>文档:http://jinja.pocoo.org/docs/          |
    | MarkupSafe   |                    HTML字符转义(escape)工具                    | 主页:https://github.com/pallets/markupsafe                                                                          |
    | Werkzeug     | WSGI工具集，处理请求与响应，内置WSGI开发服务器、调试器和重载器 | 主页:http://werkzeug.pocoo.org/<br>源码:https://github.com/pallets/werkzeug<br>文档:http://werkzeug.pocoo.org/docs/ |
    | click        |                           命令行工具                           | 主页:https://github.com/pallets/click<br>文档:http://click.pocoo.org/docs/6/                                        |
    | itsdangerous |                      提供各种加密签名功能                      | 主页:https://github.com/pallets/itsdangerous<br>文档:http://pythonhosted.org/itsdangerous/                          |
 - 将编辑器中该项目的python解释器设置为虚拟环境中的python解释器。Windows系统的路径类似"C:\Users\zzy\.virtualenvs\helloflask-QZ2E7io1\Scripts\python.exe"
#### 二、初识flask
- 创建程序实例
  - 用程序名创建flask类的实例：
  from flask import Flask
  app = Flask (\_\_name__)，之后便可直接用app实例来调用Flask类的属性和方法，如app.route()
- 注册路由
  - 在一个 Web 应用里，客户端和服务器上的 Flask 程序的交互可以简单概括为以下几步：
   l、用户在浏览器输入 URL 访问某个资源
   2、Flask 接收用户请求并分析请求的 URL
   3、为这个 URL 找到对应的处理函数
   4、执行函数并生成响应，返回给浏览器
   5、浏览器接收并解析响应，将信息显示在页面
  - 我们要做的只是建立处理请求的函数，并为其定义对应的 URL 规则，只需为函数附加 app.route() 装饰器，并传入 URL 则作为参数，我们就可以让 URL 与函数建立关联。这个过程我们称为注册路由 (ro ute) ，路由负责管理 URL 和函数之间的映射， 而这个函数则被称为视图函数 (view function)。
  - @app.route('/')
def index():
    return '\<h1>Hello, World!\</h1>'
  - 在这个程序里，app.route()装饰器把根地址/（为相对URL，即省略了域名）和index()函数绑定起来，当用户访问这个URL时就会触发index()函数。响应的主体就是呈现在浏览器窗口的 HTML 页面。
  - URL(Uniform Resource Lacator，统一资源定位符）正是我们使用浏览器访问网页时输入的网址，比如 http://helloflask.com，简单来说，URL 就是指向网络中某个资源的地址。
    - 可为一个视图函数绑定多个URL
    - 可设置动态URL，使用<'变量名'> 。如：
  @app.route('/greet', defaults={'name': 'Programmer'})
  @app.route('/greet/\<name>')
  def greet(name):
      return '\<h1>Hello, %s!<\/h1>' % name
  其中defaults={'name': 'Programmer'}设置name变量的默认值
    - url_for()函数生成视图函数对应的url，第一个参数为视图函数名
  #### 三、启动开发服务器
  - Flask 内置了一个简单的开发服务器（由依赖包 Werkzeug 提供），足够在开发和测试阶段使用。flask run命令用来启动内置的开发服务器。如果程序的主模块是其它名称，比如 hello.py，那么需要设置**环境变量**FLASK_APP, 将包含程序实例的模块名赋值给这个变量，windows系统中使用命令**set FLASK_APP=hello**
    - .flaskenv用来存储和 Flask 相关的公开环境变量 ，比如 FLASK_APP，.env 用来存储包含敏感信息的环境变量。在虚拟环境中安装python-dotenv来管理环境变量。.env包含敏感信息，不能上传到公开的git，可加入到.gitignore文件中。
    - 使用pycharm运行服务器，需设置一个运行配置
    - 更多启动服务器设置：flask run --host=o.o.o.o使服务器外部可见。flask run --port=8000 命令改变默认窗口。
 - 自定义flask命令。如：
   @app.cli.command()
def hello():
    """Just say hello."""
    click.echo('Hello, Human!')
 - 模板和静态文件。模板（template）和静态文件(static file）用来生成更加丰富的网页。模板即包含程序页面的 HTML 文件，静态文件是需要在 HTML 文件中加载的 CSS 和JavaScript 文件，以及图片、字体文件等资源文件。默认情况下，模板文件存放在项目根目录中的 templates 文件夹中，静态文件存放在 static 文件夹下。

---
### flask与http

---
### 模板
#### jinja2——模板渲染引擎
包含变量和运算逻辑的 HTML 或其他格式的文本叫做模板，执行这些变量替换和逻辑计算工作的过程被称为渲染。
在模板里，需要添加特定的定界符将 Jinja2 语句和变量标记出来。
- jinja2定界符
  - {{...}} 用来标记变量
  - {%...%} 用来标记语句，比如if语句
  - {#...#} 用来写注释
  - {% endif %}用来声明关闭if语句，大多数jinja2语句都需要声明关闭
- jinja2过滤器
  - Jinja2模板中的过滤器起到一个简单的渲染作用，它可以把接收到的数据经过简单的处理重新显示。
  - 用法：{{ 变量名|过滤器名 }}，如:{{ movies|length }}
  - 过滤器介绍
    - capitalize ,将字符串的首字母大写，其余字母转换成小写。如果字符串的首字母是非英文字母，则不进行首字母大小写转换，仅仅将字符串中其他英文字母转换成小写。
    - lower，将字符串中的英文字母转换成小写。
    - upper，将字符串中的英文字母转换成大写。
    - title，将字符串中的每个单词的首字母大写，并将单词的其他字母变成小写。
    - trim，去掉字符串的前后空格。
    - striptags，去掉字符串中所有的HTML标签。
    - abs，转化成绝对值
    - default(value,default_value,boolean=false)，如果当前变量没有值，则会使用参数中的值来代替。name|default(‘xiaoli’)——如果 name 不存在，则会使用 xiaoli 来替代。boolean=False 默认是在只有这个变量为 undefined 的时候才会使用default 中的值，如果想使用 python 的形式判断是否为 false，则可以传递 boolean=true。也可以使用 or 来替换。
    - escape或e，转义字符，会将<、>等符号转义成HTML中的符号。例如：content|escape 或 content|e。
    - first(value)	返回一个序列的第一个元素。
    - format(value,*arags,**kwargs)，格式化字符串。例如以下代码：{{ “%s” - “%s”|format(‘Hello?’,“Foo!”) }} 将输出：Hello? - Foo!
    - last(value)	返回一个序列的最后一个元素。示例：names|last。
    - length(value)	返回一个序列或者字典的长度。示例：names|length。
    - join(value,d=’+’)	将一个序列用d这个参数的值拼接成字符串。
    - int，将值转换为 int 类型。
    - float，将值转换为 float 类型。
    - string(value)	将变量转换成字符串。
    - wordcount(s)	计算一个长字符串中单词的个数。
    - replace(value,old,new)	替换将 old 替换为 new 的字符串。
    - truncate(value,length=255,killwords=False)	截取 length 长度的字符串。

- jinja2用法：
  将模板文件（即html文件）存入根目录下的templates文件夹中（模板文件可使用app.py即主文件中的变量），使用flask中的render_templates函数调用模板文件并传入模板文件中所需的参数。
  如：
  ~~~python
  @app.route('/')
  def index():
    return render_template('index.html', name=name, movies=movies)
  ~~~
- 在传入 render_template() 函数的关键字参数中，左边的 movies 是模板中使用的变量名称，右边的 movies 则是该变量指向的实际对象。这里传入模板的name 是字符串， movies 是列表，但能够在模板里使用的不只这两种 Python
数据结构，也可以传入元组、字典、函数等。
- render_template() 函数在调用时会识别并执行 index.html 里所有的 Jinja2 语句，返回渲染好的模板内容。在返回的页面中，变量会被替换为实际的值（包括定界符），语句（及定界符）则会在执行后被移除（注释也会一并移除）。即渲染后页面的源码html是不包含jinja2语句和注释的。
- 使用faker可实现自动生成虚拟数据，详见https://github.com/joke2k/faker。
  
---
### 静态文件
静态文件（static files）和模板概念相反，指的是内容不需要动态生成的文件。比如图片、CSS 文件和 JavaScript 脚本等。
- 生成静态文件url
  在 **HTML 文件**里，引入这些静态文件需要给出资源所在的 URL。为了更加灵活，这些文件的 URL 可以通过 Flask 提供的 url_for() 函数来生成。
  例如：在 static 文件夹的根目录下面放了一个 foo.jpg 文件，下面的调用可以获取它的 URL：
  ~~~
   <img src="{{ url_for('static', filename='foo.jpg') }}">
  ~~~
- 添加favicon
  Favicon（favourite icon）是显示在标签页和书签栏的网站头像。需要准备一个ICO、PNG 或 GIF 格式的图片，大小一般为16×16、32×32、48×48 或 64×64 像素。把这个图片放到static 目录下，在html模板的头部引用它。
- 添加图片
  在 static 目录下面创建一个子文件夹 images，把图片都放到这个文件夹里。
  ~~~
  <img alt="Avatar" src="{{ url_for('static', filename='images/avatar.png') }}">
  ~~~
  如上在index.html文件中合适的位置上加入图片或gif动图。
- 添加css
  在static 目录下创建一个 CSS 文件 style.css定义页面样式。
  接着在页面的 <head> 标签内引入这个 CSS 文件：
  ~~~
  <head>
  ...
  <link rel="stylesheet" href="{{ url_for('static', filename='style.css') }}" type="text/css">
  </head>
  ~~~
  最后要为对应的元素设置 **class** 属性值，以便和对应的 CSS 定义关联起来。
  ~~~
  <img alt="foot_image" class='foot_image' src="{{ url_for('static', filename='images/微信图片_20220706112817.gif') }}"/>
  ~~~

- 可以借助前端框架来完善页面样式，比如[Bootstrap](https://getbootstrap.com/)、[Semantic-UI](https://semantic-ui.com/)、[Foundation](https://get.foundation/) 等。它们提供了大量的 CSS 定义和动态效果，使用起来非常简单。
- 扩展 [Bootstrap-Flask](https://github.com/helloflask/bootstrap-flask) 可以简化在 Flask 项目里使用 Bootstrap 4 的步骤。

### 数据库
