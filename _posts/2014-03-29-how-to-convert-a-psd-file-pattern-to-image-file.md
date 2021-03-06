---
layout: post
title:  "将PSD文件中的图案叠加背景转换为图片文件"
date:   2014-03-29 08:08:42 +0800
categories: 前端学习
tags: CSS Photoshop
---
花了四天把《Head First HTML and CSS》看了一遍，确实是本入门好书。
接下来搞了点网页的psd模版打算练练手，哪知一上来就遇到个难题：文件的背景图层用的是PS的图案叠加效果做成的，无法直接导出为图像文件（jpg、png、gif之类）供css调用。虽然有个方法是直接在原图上切割，但一来这背景边缘很不明显，二来不够优雅。怎么办？

<!-- more -->

#解决
放狗搜了一圈，发现一个曲线救国的好办法，步骤如下：

1. 双击背景图层，出现图层样式对话框，选择图案叠加，可以看到所使用的图案。
    ![步骤1](http://i1266.photobucket.com/albums/jj540/wxt2005/01.png)

2. 鼠标在图案上放一会，就会出现一个提示显示图案的像素尺寸，记下来，待会用得着。
    ![步骤2](http://i1266.photobucket.com/albums/jj540/wxt2005/02.png)

3. 点击图案右边的“从当前图案创建新的预设”按钮。
    ![步骤3](http://i1266.photobucket.com/albums/jj540/wxt2005/03.png)

4. 新建一个文件，画布大小就是刚才记下的像素尺寸。然后用同样的方法新建图层，使用图案叠加，这时候再点向下箭头，刚才的图案就可以使用啦。接下来点击“贴紧原点”，然后确定。
    ![步骤4](http://i1266.photobucket.com/albums/jj540/wxt2005/04.png)

5. 搞定！这时候你就可以另存为gif，或者任意你想要的文件格式了。