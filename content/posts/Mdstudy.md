---
title: "Mdstudy"
date: 2022-05-06T03:57:30+08:00
draft: false
author: lilisaber
cover: /img/Typora.png
image:
   - /img/Typora.png
categories:
   -Markdown and Typora
tags:
   - Markdown and Typora
---

2022/05/06 in a review

<!--more-->

<table><tr><td bgcolor=moccasin>

# Markdown快速入门（typora）

## 1、代码块

1.1通过键盘ESC键下方三个连续飘号加对应语言名称(```language)引入代码块输入模式：

```java
//代码块语法：
​```java(languageName)
    :
    :
​```C++ 
```

1.2java代码

```java
<!DOCTYPE>
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
<title>Canvas圆形时钟</title>
<script src="https://ajax.aspnetcdn.com/ajax/jquery/jquery-3.5.1.min.js"></script>
<style type="text/css">
	#myCanvas {
		opacity: 0.8;
		-webkit-animation: roll 3s;
		animation: roll 3s;
	}
	@-webkit-keyframes roll {
		from{-webkit-transform:rotate(360deg);opacity:0;}
		to{-webkit-transform:rotate(0deg);opacity:0.8;}		
	}
	@keyframes roll {
		from{transform:rotate(360deg);opacity:0;}
		to{transform:rotate(0deg);opacity:0.8;}		
	}
</style>
</head>
<body>
<div style="width:150px;margin:150px auto;">
	<canvas id="myCanvas" width="150" height="150"></canvas>
</div>

  <!-- 时钟悬浮网页游动 -->
<!-- <script> 
var x = 50,y = 60;//图片距离顶部的位置 
var xin = true, yin = true 
var step = 1  //图片移动的步速 越高越快
var delay = 10 //图片移动延时 越高越慢
var obj=document.getElementById("myCanvas") //通过Document类的get方法获得”myCanvas”的标签ID
function float() { 
var L=T=0
var R= document.documentElement.clientWidth-obj.offsetWidth //offsetHeight 则是网页内容实际高度
var B = document.documentElement.clientHeight-obj.offsetHeight // clientHeight 就是透过浏览器看内容的这个区域高度。
obj.style.left = x + document.documentElement.scrollLeft + "px";
obj.style.top = y + document.documentElement.scrollTop + "px";
x = x + step*(xin?1:-1) 
if (x < L) { xin = true; x = L} 
if (x > R){ xin = false; x = R} 
y = y + step*(yin?1:-1) 
if (y < T) { yin = true; y = T } 
if (y > B) { yin = false; y = B } 
} 
var itl= setInterval("float()", delay) 
obj.οnmοuseοver=function(){clearInterval(itl)} 
obj.οnmοuseοut=function(){itl=setInterval("float()", delay)} 
</script> -->

</body>
<script>
$(function(){
	var iNow = 0;
	var arr = ["#ffae00","black"];
	myClock();
	myday();
    setInterval(myClock,1000);//每一秒钟重绘一次	
		setInterval(myday,1000);
 function myday(){
 	var a = new Array("星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六");
 	var week = new Date().getDay();
 	var dateDom=new Date();
	 	var year=dateDom.getFullYear();
	 	var month=dateDom.getMonth()+1;
	 	var day=dateDom.getDate();
	 	var mm=year+"-"+month+"-"+day;
	 	var myCanvas = document.getElementById("myCanvas");//通过Document类的get方法获取”myCanvas”标签的ID
		 	var cxt=myCanvas.getContext("2d");//然后获取画布的上下文（即拿到2D画笔）
	 	cxt.font="14px 黑体";
		//绘制实心字
		cxt.fillStyle="red";//填充红色
		cxt.fillText(mm,50,105);
 	for(var ind=0;ind<6;ind++){
 		if(week==ind){
 			var myCanvas = document.getElementById("myCanvas");
		 	var cxt=myCanvas.getContext("2d");
			cxt.font="14px 黑体";
			//绘制实心字
			cxt.strokeStyle="red";//填充红色
			cxt.strokeText(a[ind],55,55);
 		}
 }
}

    function myClock(){	
    	//得到年月日
    	
		var myCanvas = document.getElementById("myCanvas");		
		var oC = myCanvas.getContext("2d");
		//得到时分秒
		var now = new Date(),
		sec = now.getSeconds(),
		min = now.getMinutes(),
		hour = now.getHours();
		hour = hour>=12 ? hour-12 : hour;

		iNow++;
		iNow = iNow%2;		

		oC.save();//save():保存当前环境的状态
			//初始化画布
			oC.clearRect(0,0,myCanvas.width,myCanvas.height);//clearRect:在给定的矩形内清除指定的像素 
			oC.translate(75,75);//translate:重新映射画布上的 (0,0) 位置
			oC.scale(0.5,0.5);//scale:缩放当前绘图至更大或更小
			oC.rotate(-Math.PI/2);//rotate:旋转当前绘图
			 //  Math.PI: PI 属性就是 π，即圆的周长和它的直径之比
			//白色背景
			oC.save();
				oC.fillStyle = "#ccc";
				oC.beginPath();//beginPath:起始一条路径，或重置当前路径
				oC.arc(0,0,14+0,0,Math.PI*2,true);//arc:创建弧/曲线（用于创建圆形或部分圆）
				oC.fill();//fill:填充当前绘图（路径）
			oC.restore();//restore:返回之前保存过的路径状态和属性

			oC.strokeStyle = "#548B54";//strokeStyle:设置或返回用于笔触的颜色、渐变或模式
			oC.fillStyle = "black";//fillStyle:设置或返回用于填充绘画的颜色、渐变或模式
			oC.lineWidth = 4;//设置或返回当前的线条宽度
			oC.lineCap = "round";	//设置或返回线条的结束端点样式		

			//时针刻度
			oC.save();
				oC.beginPath();
				for(var i=0; i<12; i++){	
					oC.moveTo(110,0);//把路径移动到画布中的指定点，不创建线条
					oC.lineTo(120,0);//添加一个新点，然后在画布中创建从该点到最后指定点的线条
					oC.rotate(Math.PI/6);//旋转当前绘图
				}
				oC.stroke();//绘制已定义的路径
			oC.restore();

			//分针刻度
			oC.save();
				oC.fillStyle = "black";
				oC.lineWidth = 2;
				oC.beginPath();
				for(var i=0; i<60; i++){
					if(i%5 != 0){
						oC.moveTo(116,0);
						oC.lineTo(120,0);
					}
					oC.rotate(Math.PI/30);
				}
				oC.stroke();
			oC.restore();			
			
			oC.save();
				oC.rotate(Math.PI/2);
				oC.font = "30px impact";
				//12点
				oC.fillText("12",-15,-80);	
				oC.fillText("1",40,-75);	//文本的 x 坐标位置,文本的 y 坐标位置		
				oC.fillText("2",80,-35);		
				//3点
				oC.fillText("3",88,13);					
				//6点
				oC.fillText("6",-8,104);				
				//9点
				oC.fillText("9",-103,11);					
			oC.restore();
			
			//画时针
			oC.save();
				oC.strokeStyle = "#ff3300";
				oC.rotate((Math.PI/6)*hour+(Math.PI/360)*min+(Math.PI/21600)*sec);	
				oC.lineWidth = 8;
				oC.beginPath();
				oC.moveTo(-20,0);
				oC.lineTo(60,0);
				oC.stroke();
			oC.restore();
			
			//画分针
			oC.save();
				oC.rotate((Math.PI/30)*min+(Math.PI/1800)*sec);
				oC.strokeStyle = "#27A9E3";
				oC.lineWidth = 6;
				oC.beginPath();
				oC.moveTo(-28,0);
				oC.lineTo(90,0);
				oC.stroke();
			oC.restore();

			//画秒针
			/*oC.save();
				oC.rotate(sec*Math.PI/30);
				oC.strokeStyle = "#D40000";
				oC.lineWidth = 3;
				oC.beginPath();
				oC.moveTo(-30,0);
				oC.lineTo(105,0);
				oC.stroke();
			oC.restore();*/
	
			//风车秒针
			oC.save();
				oC.rotate(sec*Math.PI/30);				

				oC.save();					
					oC.fillStyle = "#f23";
					oC.beginPath();
					oC.arc(94,0,10,0,Math.PI,true);
					oC.fill();
				oC.restore();

				oC.save();
					oC.rotate(Math.PI/2);
					oC.fillStyle = "#ffae00";
					oC.beginPath();
					oC.arc(10,-84,10,0,Math.PI,true);				
					oC.fill();
				oC.restore();

				oC.save();
					oC.fillStyle = "#27A9E3";
					oC.beginPath();
					oC.arc(74,0,10,Math.PI,Math.PI*2,true);
					oC.fill();
				oC.restore();

				oC.save();
					oC.rotate(Math.PI/2);
					oC.fillStyle = "#0eaf52";
					oC.beginPath();
					oC.arc(-10,-84,10,Math.PI,Math.PI*2,true);
					oC.fill();
				oC.restore();
			oC.restore()
			//风车秒针


			//表框
			oC.save();
				oC.lineCap = "butt";
				oC.lineWidth = 16;
				//调整边框样式
				oC.save();				
					oC.strokeStyle = "#BBFFFF";
					oC.beginPath();
					oC.arc(0,0,142,0,Math.PI*2,true);
					oC.stroke();
				oC.restore();

				oC.save();
					oC.strokeStyle = "#C0FF3E";
					oC.beginPath();
					oC.arc(0,0,142,0,Math.PI/iNow*5/3,true);
					oC.stroke();
				oC.restore();
			oC.restore();

			//中心点
			oC.save();
				oC.fillStyle = "#fff";
				oC.beginPath();
				oC.arc(0,0,4,0,Math.PI*2,true);
				oC.fill();
			oC.restore();
		oC.restore();
	};
});
</script>
</html>
```

2.shell脚本

```shell
//linux下spring项目的启动命令
# java -jar blog start
```

## 2、标题

```java
//标题语法
# 一级标题
## 二级标题
### 三级标题
#### 四级标题
##### 五级标题
###### 六级标题
```

### 2.1标题效果展示

# Title Rank 1

## Title Rank 2

### Title Rank 3

#### Title Rank 4

##### Title Rank 5

###### Title Rank 6

## 3、字体

```java
//加粗
**天生我材必有用**
//代码高亮显示
==超级大boss==
//删除线
~~被删除的文字~~
//斜体
*斜体内容*
//斜体加粗
***斜体加粗***
//上标和小标
^上标内容^与~下表内容~
```

### 3.1字体效果展示

**天生我材必有用**

==超级大boss==

~~被删除的文字~~

*斜体内容*

***斜体加粗***

我是^上标^与我是~下表~

## 4、引用

```java
//引用语法
>一级引用
>>二级引用
>>>三级引用
```

###4.1引用效果展示

>一级引用
>>二级引用
>>>三级引用

## 5、分割线

```java
//分割线
---
//分割线2
***
```

###5.1分割线效果展示

---

***

## 6、图片插入

```java
//在线图片/本地图片
![picture name](/image/me.png)---图片路径
```

### 6.1图片插入效果展示

#### 6.1.1本地图片

![不被大风吹倒](D:\Desktop\屏幕截图 2022-05-04 001736.png)

####6.1.2网络图片

![天野阳菜](http://localhost:1313/me/8.jpg)

## 7、超链接

```java
//超链接语法
[href name](http://localhost:1313)
```

### 7.1超链接效果展示

[Myblog](http://localhost:1313)

## 8、列表

```java
//无序列表（'+','-','*'后接一个空格）
- 目录1
- 目录2
- 目录3
- 依次类推形成表格等级，列表有三个级别（实心圆，空心圆，实心正方形）
//有序列表（段落格式下选择有序列表）
数字键+.+名称（1.有序列表）
```

### 8.1无序列表效果展示

- 目录1
- 目录2
- 目录3
- - - 
- 一级目录
  - 二级目录
    - 三级目录

### 8.2有序列表效果展示

1. 有序列表
2. 有序列表1
3. 有序列表3

##9、表格

```java
//点击鼠标右键，选择茶人点击表格，即可设置行和列
//ctrl+'/',即可看到markdown所写的源码
//当然也可以用html语言进行表格以及样式设计
```

### 9.1表格效果展示

|  5   |  7   |  9   |
| :--: | :--: | :--: |
|  6   |  8   |  4   |
|  1   |  5   |  7   |

### 9.2源代码格式下表格使用方法

```java
//源代码格式下（第三行为分割，必打）
|第一格内容|第二格内容|....|第n格内容|
|-----|-----|-----|-----|
|第一格内容|第二格内容|....|第n格内容|
    ：
    ：
|第一格内容|第二格内容|....|第n格内容|
```

### 9.3非源代码格式下表格使用方法

```java
//非源代码格式下，也可直接竖线生成表格然后更改
|第一格内容|第二格内容|....|第n格内容|
 --->回车即可生成表格，然后再调整
```

eg.效果展示

| MON  | TUE  | WEN  | TRU  | FRI  | SAT  |
| ---- | ---- | ---- | ---- | ---- | ---- |
|      |      |      |      |      |      |
|      |      |      |      |      |      |
|      |      |      |      |      |      |

## 10、画图

### 10.1Markdown画图介绍

```java
//Markdown作为一款轻量级文本编辑器，其画图功能并不全面
//其中的Mermaid是一个用于画流程图、状态图、时序图、甘特图的库
//使用JS进行本地渲染，
//Mermaid作为一个使用JS渲染的库，生成的不是一个“图片”
//而是一段HTML代码
//在使用之前确保文件的偏好设置已经打开
```

### 10.2流程图（graph）

```java
//graph 方向描述
//    图表中的其他语句---
```



### 10.3序列图

### 10.4饼图

### 10.5甘特图


</td></tr></table>







