---
title: "Live2D初学习"
date: 2022-03-27T00:29:52+08:00
draft: true
author: lilisaber
cover: /img/sabersan.png
images:
   - /img/sabersan.png
categories:
   -Live2D贴一
tags:
   - Live2D
---

2022/03/27 in a review

<!--more-->

<table><tr><td bgcolor=moccasin>


## Live2D基本流程间接经验学习

## 任务一：图层的分层

### Tools：SAI/SAI2/PhotoShop

### Steps：

1.简略的拆分预览

2.建模器中制作关键帧和变形器

3.Live2D动态化

4.效果预览，导出moc输出Live2D的贴图

### Notice：

如果想要制作一个比较精致的Live2D就需要拆分更多的图层


## 任务二：分层的步骤（SAI or PhotoShop）

### Steps：

1.拆分头部，身体，腿（使用SAI或者PhotoShop为图层分层并且导出PSD格式）。

2.导出为PSD格式


## 任务三：导入PSD以及修复异常的图层（Live2D Cubism modeler）

### Steps：

1.打开建模器，new --> PSD import，或者直接将PSD文件导入到建模器当中。

2.建模器为PSD自动布点，可能出现点位不准。（如果布点不准确，将出现图层融合的情况）

3.解决办法：双击修正图层
  
a.点击Eraser橡皮擦工具，将出界的布点擦除

b.点击Insert Point添加布点工具,手动添加修正布线（鼠标右键弹出来的选项可以自动补齐未连接的线）


## 任务四：基础的动态/脸部表情制作（Live2D Cubism modeler and Live2D Viewer）

### Steps:

1.圈选图层，将会显现图层所有的布点，然后鼠标点击移动图层，确认是否圈选完整。

2.按下shift键，圈选更多想要动的图层，然后绑定旋转变形器

3.选择Create Deformer，创建一个Rotation旋转变形器

4.更改Destination Part变形部位body，输入变形器Name（如果出现乱码，请按ctrl+shift+F 切换简体繁体输入）

5.将变形器按ctrl+鼠标左键，拖至变形的对应部位，在parameter框找到对应变形器名称Body Z，然后在出现的弹框里点击添加3个关键帧

6.在parameter框中找到上述变形器，移动变形器关键帧的滑条

#### A.上述为Body Z轴身体倾斜的图层关键帧制作


1.选中图层右键，将出现菜单，点击select Drawerable Object，可以快速定位附近需要的图层布点

2.创建旋转变形器，选择目标部位face

3.在parameter框中找到上述变形器Angle Z，添加3个关键帧，然后移动滑条，使其倾斜

4.如果漏选了绑定进变形器的图层，可以再次框选对应图层，然后在Edit里选择对应图层的变形器，再移动滑条确认是否绑定成功

#### B.上述为Angle Z轴脸部倾斜的图层关键帧制作


1.进行眼部的关键帧制作，这部分比较精细，在框选图层以后，再次进入布点的更改

#### A.眉毛布点（眉毛位于布点的中间，从横向切面看为两层及三层布点，尽量平行，点距对应均等）

a.三角形布点

b.贯穿中线沿眉形布点

#### B.睫毛布点（眼部精细部分）

a.贯穿中线菱形布点

#### C.嘴巴布点

a.贯穿中线向外围拓展菱形布点（向外拓展两层布点）

#### Notice：

a.布点形成正三角形

b.尽量沿着既有线条的走向布点


2.眼部开闭关键帧（EyeL or EyeR Open）

a.给睫毛闭眼添加2个关键帧，然后将睫毛图层向下平移，点击菜单栏的钢笔工具（设置三个钢笔布点，点击指针将可以同时移动多个布点），然后细调睫毛布点，使其自然化。

b.给眼白闭眼添加两个关键帧，然后移动滑条，使睫毛图层处于闭眼状态，然后圈选眼白图层，使其可以被睫毛完全遮盖，然后再移动滑条，眼白闭眼关键帧制作完成（8:19）


## Final

点击建模器上方菜单栏的Tool，选择Live2D Viewer,预览效果。

</td></tr></table>