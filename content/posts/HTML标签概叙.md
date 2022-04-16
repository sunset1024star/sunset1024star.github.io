---
title: "HTML标签概叙"
date: 2022-01-16T21:42:12+08:00
draft: true
author: LiLisaber
cover: /img/CSS.jpg
images:
   - /img/CSS.jpg
categories:
   - HTML and CSS
tags:
   - JSP、HTML、CSS
---
 
2022/01/16 in a review.

<!--more-->

<table><tr><td bgcolor=moccasin>

## JSP技术(java server pages)
 
JSP作为我所学相关web制作的先导知识，是我最先接触的。JSP作为sun公司开发的动态网页技术，可以根据用户的请求，动态地生成HTML，XML等其他格式文档地web网页。

其基础的脚本语言是Java，jsp是作为网站后端开发的一种语言之一。而MVC框架是我所学的第一种软件设计模式。M即model，其由一个或多个Javabean组成，主要负责存储数据；V即view，其由一个或多个jsp页面组成，主要负责显示数据；C即control,由一个或多个servlet组成，主要负责处理数据。如下图所示：

![Alt text](/img/MVC.jpg)

<hr style="height:0.5px; border:none; border-top:1px solid rbg(234,236,239)" />

## HTML文档

**HTML全称超文本标记语言（hypertext makeup language）**,使用HTML编写的文本文档即为HTML文档，其可独立于各种操作系统，并且被各种浏览器所识别。用于确定网页的结构和内容。

<hr style="height:1px; border:none; border-top:1px solid rbg(234,236,239)" />

## CSS

**CSS全称层叠样式表（cascading style sheets）**,可用于定义页面的样式结构，并且减轻了HTML文档的负担。其用于设置网页的样式，主要包括各元素的外观，大小，位置等。通过掌握HTML和CSS，就可以制作各种静态页面。

<hr style="height:1px; border:none; border-top:1px solid rbg(234,236,239)" />

## JavaScript

**JavaScript是一种解释性脚本语言，简称JS**。它可以收集页面上的数据，并且记录用户的操作，使页面呈现出交互性。用于添加更为复杂的动画和交互效果。

<hr style="height:1px; border:none; border-top:1px solid rbg(234,236,239)" />

## HTML的常用标签

- ## <font face="华文楷体" color=red><html注释></font> ##

  普通注释：<!- -要注释的内容- -除>

    if注释：<!- -[if 条件]>注释内容<![endif]- -除>


- ## <font face="华文楷体" color=red><font元素></font> ##

  font标签用于设置html文字字体、html字体颜色（颜色可以为十六进制颜色代码，rbg码，颜色英文）、html字体大小

  <font除 color="颜色代码">文本内容<除/font>

  <font除 size="字体大小数字">文本内容<除/font>

  <font除 face="字体">文本内容<除/font> 


- ## <font face="华文楷体" color=red><html px em pt（像素 相对长度 点）></font> ##

  px（像素pixel），相对长度单位，相对显示器屏幕分辨率，国内使用居多；
  
  em（相对长度），相对于当前对象内文本的字体尺寸，国外使用居多；

  pt（点point），以前作为table标签的使用长度大小，现在基本不用；


- ### <三种长度单位在css和html上的语法> ###

- CSS代码

  .divcss5-px{font-size:   px}

  .divcss5-pt{font-size:   pt}

  .divcss5-em{font-size:   em}

- HTML代码

  <div除 class="divcss5-px">文本内容<除/div>

  <div除 class="divcss5-pt">文本内容<除/div>

  <div除 class="divcss5-em">文本内容<除/div>

- ### <em与px的换算> ###

  浏览器默认字体高为16px,因此  1em = 16px。

  为了简化font-size的换算，需要在css中的body选择器中声明font-size=62.5%，这就使em值变为 16px*62.5%=10px

  即可在对全体HTML声明一次初始值font-size=62.5%，如{除font-size=62.5%}，后续单位换算即有：
 
  1.2em=12px,1.4em=14px; 

  注意事项：

  em的值并不是固定的，em会继承父级元素的字体大小。

    我们在写CSS的时候如果要用em为单位，需要注意三点：

　- body选择器中声明Font-size=62.5%;

　- 将你的原来的px数值除以10，然后换上em作为单位;

　- 重新计算那些被放大的字体的em数值。避免字体大小的重复声明。
 

- ## <font face="华文楷体" color=red><html声明></font> ##

  <!除DOCTYPE html>，位于html标签的上方


- ## <font face="华文楷体" color=red><html元素/html></font> ##

  作为HTML文档的根元素,标志着HTML文档的开始与结束。其中间部分则为文档的头部结构<head元素>和主体结构<body元素>


- ## <font face="华文楷体" color=red><head头元素/head></font> ##

  用于设置文档标题和其他不在网页中显示的信息,


- ### <meta元素/> ###

  <除meta name="" content="" charset=""/>


- ### <title标题元素/title> ###

  用于设置文档标题，**一个网页中只能使用一次title标签**，是标识一个网页唯一标题作用，而且根据W3C标准必须**放入**一个网页中**头部head标签内**。


- ## <font face="华文楷体" color=red><body元素/body></font> ##

  在HTML中**只能使用或出现一次**，用于放置页面显示的内容


- ### <h1标题元素/h1> ###

  其数值由1到4，标题大小逐渐减小


- ### <p段落元素/p> ###

  用于创建一个段落，**区别于br元素的单独使用**。其所造成的换行即**产生段落间距**


- ### <br/强制换行元素> ###

  我们可以在需要的地方进行手动添加，**单独使用<br/除>即可强制换行**


- ### <nobr强制不换行元素/nobr> ###

  被设置的内容将在一行显示，除非在内容中有br强制换行标签，否则不换行。格式如下：

  <nobr除>文本内容</除nobr>


- ## <font face="" color="red"><加粗元素标签></font> ##


- ### <b文字加粗元素/b> ###

  <b除>加粗的文本内容<除/b>


- ### <strong文字加粗元素/strong> ###

  <strong除>加粗的文本内容<除/strong>


- ## <font face="" color="red"><斜体强调元素标签></font> ##


- ### <em强调元素/em> ###

  em标签修饰的内容都是**用斜体字**来显示，但这些内容也具有更广泛的含义,如果你**只想使用斜体字来显示文本**的话，**请使用i标签**。除此之外，文档中还可以包括用来改变文本显示的级联样式定义。格式如下：

  <em除>被强调斜体的内容<除/em> 


- ### <i强调元素/i> ###

  <i除>被强调斜体的内容<除/i>


- ## <font face="" color="red"><线条元素标签></font> ##


- ### <u下划线元素/u> ###

  <u除>被添加下划线的内容<除/u>


- ### <s删除线元素/s> ###

  <s除>被添加删除线的元素<除/s>


- ### <hr水平线元素/> ###
 
  html Hr水平线特点是100%宽度水平分割线，并且独占一行，hr水平线将与上下内容一定距离。
并且还可以对其设置css样式，其格式如下：

  <hr除 style="height:  px;  border:none;  border-top:  px  样式(例如solid)  颜色#或rbg代码或英文颜色 /> 

  水平线样式如：dotted（虚线），dashed，solid（实线），double，ridge，groove


- ## <font face="华文楷体" color=red><html sup上标 sub下标></font> ##

  上标格式：<除sup>需要上浮的文本内容</除sup>

  下标格式：<除sub>需要下沉的文本内容</除sub>  


- ## <font face="华文楷体" color=red><style格式元素/style></font> ##

  常见的**style标签**作为放置**CSS样式**和**JavaScript代码**的标志，HTML下的CSS和JavaScript在style下生效，格式如下：

  <除style type="text/css"><除/style>

  <除style type="text/javascript"><除/style>


- ### <script元素/script> ###

  用于链接外部JS文件，区别于link的href链接css文件，script可以用于HTML网页源代码的**任何地方**。其格式为：

  <script src="js文件地址" type="text/javascript"除></script>


- ### <link元素/> ###

  link标签主要链接外部css文件，链接收藏夹图标（favicon.ico）。一般放置在网页的**头部标签head标签内**。

   **link引入css**：<link href="css文件地址" rel="stylesheet" type="text/css"/除>

  **link引入icon**：<link href="favicon.ico" rel="icon" type="image/x-icon"/除>

  **href** 值为外部资源地址

   **rel** 定义当前文档与被链接文档之间的关系,rel值不唯一

  **type** 规定被链接文档的 MIME 类


- ## <font face="华文楷体" color=red><超链接元素></font> ##

- ### <a 超链接htmla /a> ###

  html a超链接可以将页面由a页面转向b页面，**超链接的锚文本可以为，文字或图片url**
若为图片，则可为<除img src="图片url"/>
  
  <除a href="具体网址或相对文件url"  target="可省"  title="超链接的页面标题">超链接内容</a>

  **target：为打开目标的方式**
  
    **省略**：则为默认是在浏览网页中重新载入对应链接地址的网页

  **_blank**: 将在新建的标签窗口打开对应超链接地址

   **_parent**：父级打开网页，此属性可以理解为本页网页从新载入锚文本的网页，针对html框架iframe网页中，整个网页将重新载入打开目标网址地址


- ## <font face="华文楷体" color=red><div分割布局元素/div></font>

  作为一种代码布局标签，其代替了之前的table标签布局成为最常用的布局标签。div可以起到**分割页面**，从而进行**独立设置对应样式**的作用。我们常说的网页重构便是DIV+CSS切图布局重构技术。


- ## <font face="华文楷体" color=red><span布局元素/span></font>
  
  span在html中常用的布局标签,**与div标签区别在于**，span**随内容而占用**高宽空间（紧贴内容），而**一对div标签却占用一行**。


- ## <font face="华文楷体" color=red><img图片元素/></font> ##

  格式如下：

  <img除 src="图片地址路径或图片网址" width=" " height=" " alt="图片描述"/>

  width：图片宽度，值为具体数字，默认以像素为单位（不用跟单位）
  
  height：图片高度，值为具体数字，默认以像素为单位（不用跟单位）


- ## <font face="华文楷体" color=red><表单布局></font> ##


- ## <font face="华文楷体" color=red><form表单/form></font> ##

  html的form表单区域标签，其提交数据的方式method有两种，get或post。

  - get：限制提交数据为1024字节，安全性较低，其提交的数据将会在url网址之后显示，一般适用于不需要安全保密的简短字符。

  - post：没有限制提交数据，安全性比get高，其可隐藏传递数据，一般用于用户登录和大数据传输。

  html的form表单区域标签，其action值可填写为将表单提交内容送往的页面地址。

  通常此标签的表单控件有，input控件{(input[text输入框])、(input[sumbit提交按钮])、(input[radio单选框])、(input[checkbox多选框])}、多行文本框(textarea)、下拉列表(select)等表单内容。

  <form除 action=" " method="get">表单内容</form>，是**通过URL** 传内容与参数,这个时候我们通过 **网址URL能看见** 自己填写 **内容提交处理** 。
  
  <form除 action=" " method="post">表单内容</form>，是**通过类似缓存**传填写内容与参数，而URL是**不能看到** form表单填写内容**提交内容** 。 


- ### <label标签元素/label> ###

  通过label标签实现对其加入文字的触发，使其可以实现对应表单控件功能，从而达到点击按钮或选项框前的文字，就可实现选中选项的目的。格式如下：

  <label除 for="自定义属性值">作为连结表单控件的文字，在控件外围</label>    

  label标签内**for属性的值**为自定义，一般**与对应的表单控件的id值一致**。


- ### <input标签/> ###

  格式如下例：<input  name=" "  type="text/submit/radio/checkbox"  (size=""text有文本大小)  value="提交"/>

  name为此表单控件识别命名，一般使用英文字母，且在一个页面里具有唯一性。

  type为表单控件样式。
  
  value为控件的显示名称或叫默认值，位于控件上；区别于label标签的文字声明在控件外。

- #### <font face="" color=red><input text输入框></font> ####

  - type="text"输入框控件，用于输入用户名、密码等等

- #### <font face="" color=red><input submit按钮></font> ####

  - type="submit"按钮控件，用于提交、重置动作

- #### <font face="" color=red><input radio单选框></font> ####

  - type="radio"单选框，用于单选，唯一选择功能


- #### <font face="" color=red><input checkbox多选框></font> ####

  - type="checkbox"多选复选控件，用于多选题、多选功能一选择功能


- ### <select下拉表单标签/select> ###

  select下拉列表格式如下：

  <select除 name="">

  <option除 value="传值1">选项声明，将在控件位置默认显示</除option>

  <option除 value="传值2">选项声明，将在控件位置默认显示</除option>

  </除select>
  
  select为下拉列表菜单标签，option为下拉列表数据标签，Value**为option的**数据值（用于数据的**传值**）
 
  **下拉列表主要有以下三种**

  - **普通下拉列表菜单**
 
  <select除 name="">

  <option除 value="传值1">选项声明，将在控件位置默认显示</除option>

  <option除 value="传值2">选项声明，将在控件位置默认显示</除option>

  </除select>


  - **跳转下拉列表菜单**（实现跳转还需要在head标签内加入js脚本动作代码）

  <select除 name="jumpMenu" id="jumpMenu" **onchange="MM_jumpMenu('parent',this,0)**"> 
  
  <option除 value="将要跳转的网址">选项声明，将在控件位置默认显示</除option> 
  
  <option除 value="将要跳转的网址">选项声明，将在控件位置默认显示</除option> 

  </除select> 

  **js脚本**例如
 
  <script除  type="text/javascript"> 

  function **MM_jumpMenu(targ,selObj,restore)**{

  eval(targ+".location='"+selObj.options[selObj.selectedIndex].value+"'"); 

  if (restore) selObj.selectedIndex=0; } 

  </除script> 

  
  - **更简洁的新建浏览器（选项卡）窗口跳转菜单**

  该跳转菜单只需要在普通的基础上，在select标签里加入以下代码，即可：
  
  onchange="javascript:if (this.options[this.selectedIndex].value != '') window.open(this.options[this.selectedIndex].value);this.options[0].selected;"


- ### <textarea文本框标签/textarea> ###

  <textarea除 name="" cols="每行文字的宽度数值" rows="默认输入框的高度行数">文本区域内容文字</除textarea>


- ## <font face="" color="red"><iframe内嵌网页标签元素-html iframe内嵌网页框架/></font> ##

  <iframe除 src="被嵌入网页地址" width="宽度数值/百分比" height="高度数值/百分比" scrolling="yes/no/auto 是否有滚动条、根据被显示html自动显示或隐藏"/>

  特点：不利于当前页面的搜索引擎优化，如果要在某一页面中**局域显示另外网页**，即可使用iframe标签


- ## <font color="red"><HTML Table td/th表格 tr td th表格标签></font> ##

  格式如下：

  <font color="red"><table除 </font>

  width="表格宽度数值或百分比，100%与浏览器等宽" 

  border="边框线厚度" 

  bordercolor="边框颜色" 

  cellpadding="单元格内容与单元格边框线的距离" 

  cellspacing="单元格间距" 

  align="对齐方式left、right、top 、middle 和 bottom或center"<font color="red"> > </font>

  <font color="red"><tr除> </font>

  <td或tr>

  <font color="red"><th或td>内容标题</th或/td> </font>

  <td或tr> 

  <font color="red"></除tr> </font>

  <font color="red"></除table> </font>


- ## <font color="red"><html dl表格 dl dt dd 列表标签></font> ##

  格式如下：

  <dl除>

      <dt除>列表标题</dt>

      <dd除>列表内容</dd>

      <dd除>列表内容</dd>

  ...

  </除dl>

  dd内可以放置ul标签


- ## <font color="red"><html ol li 有序列表标签></font> ##

  <ol除> 

      <li除>内容一</除li> 

      <li除>内容二</除li> 

      <li除>内容三</除li> 

  </除ol> 

  使用该标签，将自动生成序号，常用于文章标题排版、图片列表排版布局

- ## <font color="red"><html ul li 列表标签></font> ##

  <ul除> 

      <li除>内容</除li> 

      <li除>内容</除li> 

      <li除>内容</除li> 

  </除ul> 

  使用该标签，将生成点，相对于有序标签使用较多，常用于文章标题排版、图片列表排版布局，以上均可以再使用css进行美化。

</td></tr></table>










