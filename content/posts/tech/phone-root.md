+++
title = "记一次简单的救砖经历"
date = "2022-05-01"
description = ""
featured = false
reward = false
draft = false
categories = [
  "技术类"
]
tags = [
  "magisk",
  "root"
]
series = [

]
images = [

]
+++



<!--more-->

## 0x00 前情

在4月中旬的时候，我看我一个op5二手机一直没人用，想送给别人，最终决定送给一个刚刚高中上完的亲戚使用。本着传教的目的，想着给手机root了再送出去，于是就了这么个简短的救砖的经历。我玩机的时间也不是太多，很多知识不懂，这次救砖也是我第一次经历。



## 0x01 变成砖

在昨年5月份，我人生的第一次root是通过别人提供的工具箱一键root的，虽然在这之前通过magisk的官方教程尝试过root，但是因为手机是vivo，bl锁解不了，所以没有root成功，这也是二手机的由来。

于是这次，我为了图方便还是使用了那个工具箱，全然忘机了我为什么丢掉了root（直接升级了系统到安卓10），而工具箱root只支持安卓8和9，结果就是手机就变成了砖，具体表现是手机开机后进入不了系统，黑屏状态，但是可以进入fastboot。recovery也是进入不了。

## 0x02 救砖

由于已经过了半个月了记忆模糊了，我只是把整个流程叙述一遍，至于过程，反反复复搞了4个多小时吧，都是一步一步边搜索边操作的。

recovery方面，我分别尝试了官方rec和twrp。官方rec每次利用usb修复的时候中途都会失败，原因不明，因而使用了twrp。twrp刷入时使用了'fastboot flash recovery'，但是每次重启时却又没安装成功，于是只能使用低版本的twrp，recovery到这里就解决了，可以顺利进入twrp。

接下来就是使用sideload线刷第三方rom了，这一部分比较顺利，但是sideload总会出错，查了一下发现是好像传的东西超过2gb的话就会有问题，于是只能委曲求全找比较小的第三方rom，最终成功刷入miui。

## 0x03 官方方法root

成功救砖后我就安装官方教程进行root了，这一部分我之前做过，所以很顺利。安装magisk，去除rom的boot.img用magisk修补，利用adb pull这个img取到电脑上，fastboot flash boot。顺利的话很快的。root成功后就进行一些常用软件的安装，先弄zygisk，然后shamiko，lsposed，scene安上，再弄点什么模块什么的给他玩玩……其余的就等他自己探索，如果他有兴趣的话……没兴趣也无所谓，反正手机已经给他了……

## 0x04 尾

回看其实发现过程不怎么难，但我觉得还是有点意思。希望后面会越来越好玩~

<div align=center>
<img src="/images/phone-root_1.jpg"  width="50%" />  
</div>