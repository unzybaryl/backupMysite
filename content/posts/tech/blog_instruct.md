+++
title = "我的Hugo+Github page搭建博客教程"
date = "2021-11-27"
description = ""
featured = false
reward = false
draft = false
categories = [
  "技术类"
]
tags = [
  "博客搭建"
]
series = [

]
images = [

]
+++

(多图警告！）给一些需要的朋友，互联网本身也有很多教程，反正有疑问的地方可以通过网站给出的链接询问~

<!--more-->

## PERFACE

### 1.教程方向

尽量简单易懂    
有问题反馈后会进行补充。

### 2.顺序结构

按照Hugo，GIthub Page和Git，域名的顺序来写。由Hugo的基本操作，选择Theme后生成博客；通过Git上传博客内容至Github仓库，在仓库中设置Github page，最后的域名购买可绑定是可选择的。最后还会介绍一些需要使用的东西，如Md文档样式，hugo theme文件格式。

## 一、Hugo

Hugo是由Go语言实现的静态网站生成器。可以快速生成静态网站。

### 1.Hugo的下载和安装

Hugo下载地址：[Hugo 0.89.2](https://github.com/gohugoio/hugo/releases/download/v0.89.2/hugo_0.89.2_Windows-64bit.zip)  
下载了好后解压把文件放在一个位置，如我放在了D:\目录下（www3不用管）：


<div align=center>
<img src="/images/blog_1.png"  width="75%" />  
</div>

&emsp;

接下来配置环境变量，win和R键一起按，调出运行窗口，在其中输入“systempropertiesadvanced”回车：

<div align=center>
<img src="/images/blog_2.png"  width="75%" />  
</div>

&emsp;

出现系统属性窗口，点击右下角的“环境变量”，双击系统变量中的“Path”：

<div align=center>
<img src="/images/blog_3.png"  width="75%" />  
</div>

&emsp;

点击右边的新建，将你下载解压的hugo地址填上去：

<div align=center>
<img src="/images/blog_4.png"  width="75%" />  
</div>

&emsp;

检查是否安装成功，win+R键打开运行窗口，输入“cmd”回车，在命令提示符中输入“hugo -help”查看是否有以下信息出现，出现则安装成功：

<div align=center>
<img src="/images/blog_5.png"  width="75%" />  
</div>

&emsp;

在命令行窗口中输入“hugo new site 路径/名字” 就可以建立一个站点，例如以我的环境，输入"hugo new site D:\hugo_0.82.1_Windows-64bit\www3"。我上面的www3文件夹也是这么来的，文件夹名字可以随便取，我取的就是“www3”啦。

<div align=center>
<img src="/images/blog_8.png"  width="75%" />  
</div>

&emsp;



### 2.Hugo Theme下载和安装

安装好了Hugo，还需要安装一个主题，主题就是你搭建博客的style样式。主题地址：https://themes.gohugo.io/ ：

<div align=center>
<img src="/images/blog_6.png"  width="75%" />  
</div>

&emsp;

这里有非常非常多的主题，你喜欢哪款就点击进去，点击左下角的“Download”按钮，跳转到对应的github仓库，在绿色的code按钮下，点击“Download zip”就可以下载啦：

<div align=center>
<img src="/images/blog_7.png"  width="75%" />  
</div>

&emsp;

之前我们用hugo new site命令创建了一个站点，现在将下载的Theme放入站点中的theme文件夹，我这里已经放了3个theme了：

<div align=center>
<img src="/images/blog_9.png"  width="75%" />  
</div>

&emsp;

接下来导入theme的配置文件，这里不同的theme表现有些不同，先去下载theme的examplesite找一下，我遇到的有两种可能：  
①存在一个config.toml，那么就把这个文件复制到站点根目录下去：

<div align=center>
<img src="/images/blog_10.png"  width="75%" />  
</div>

&emsp;

②没有config.toml而是一整个config文件夹，那么把这个文件夹复制到站点根目录下：

<div align=center>
<img src="/images/blog_11.png"  width="75%" />  
</div>

&emsp;

反正不管怎么样，这个东西或者文件夹就是配置文件了。这里面的设置都挺重要的，并且还有一些theme作者提供的额外功能，一般来说theme里面有教程，我这里附上我以前的配置，里面包含了url，网站语言，HTML title，使用的主体文件夹名等等，这个就自己探索吧。里面的配置随着主题的不同有很大的不同，一般来说作者会给出教程的，在下载主题文件夹里面找找。

<div align=center>
<img src="/images/blog_12.png"  width="75%" />  
</div>

&emsp;



### 3.Hugo创建和写作文章

首先需要在之前生成site的那个文件夹内打开cmd窗口，先打开那个文件夹，然后在文件夹上方的那个地址栏中输入”cmd“即可实现：

<div align=center>
<img src="/images/blog_13.png"  width="75%" />  
</div>

&emsp;

之后我们就可以用命令来生成空文章了，在cmd中输入：
```
hugo new xxx.md
```
就在站点目录的content中生成了一个叫"xxx.md"的文件。有些站点的文章目录结构有些不同，像我的站点content里面还有文件夹，如我想在content\posts\文件夹里面生成空文章的话，可以输入：
```
hugo new posts\new.md
```
其他的目录就依次类推了。

<div align=center>
<img src="/images/blog_14.png"  width="75%" />  
</div>

&emsp;

打开自动生成的空文章，最上面就是生成空文章的一些信息，title表示文章标题，date表示发布日期，draft代表是否是草稿，如果文章是操作，在之后的生成过程中这篇文章是不会被生成的。当然这里不同主题的表现可能也有些不同，下面是图，这个就自己探索了，如果有疑问可以通过站内给出的联系方式问我。

<div align=center>
<img src="/images/blog_15.png"  width="75%" />  
</div>

&emsp;

之后就可以用md文档写文章了，md文章还是有很多样式的，并且可以插入HTML代码，之后的附录里会给一些md文章写作技巧。

### 4.调试站点和生成站点

写好文章以后，还是在站点根目录的cmd窗口中输入`hugo server`或者`hugo server --buildDraft`来调试站点。其中第二个指的是将draft设置为true的站点也生成。
<div align=center>
<img src="/images/blog_16.png"  width="75%" />  
</div>

&emsp;
默认地在浏览器中输入`localhost:1313`就可以看到你的站点啦~之后在网站的各个地方修改并且保存后，它会检测到改动，并且快速地重构站点，你可以立刻就看到改动后的样子。我现在写这篇文章就是这样做的哦！注意如果源代码出错了hugo server也是会构建不了的，需要重新再输入一次上面的指令。
<div align=center>
<img src="/images/blog_17.png"  width="75%" />  
</div>

&emsp;
站点调试完成后，觉得差不多了想要上传，还是在站点根目录的cmd的窗口中输入：
```
hugo
```
就会生成站点啦。站点生成在站点根目录的“public”文件夹下面：
<div align=center>
<img src="/images/blog_18.png"  width="75%" />  
</div>

&emsp;

## 二、Github Page
静态站点的源代码hugo已经帮我们弄好了，现在怎么才能变成可以访问到呢？Github Page给我们提供了个非常方便的服务，可以将网站源代码上传至github仓库，设置好Github Page以后我们网站可以由github提供的域名：“username.github.io”访问到了，并且还可以绑定上自己买的域名。

### 1.Git
首先需要注册个github账号，之后嘛……给你个链接：[GIt使用](https://blog.csdn.net/mrjkzhangma/article/details/89466811)  
配置好SSH key，把站点public文件上传到Github仓库就算成功啦。下面给出我站点仓库的截图，里面的东西和之前用`hugo`指令生成在public文件夹的东西是一模一样的，所以这部就是把public的东西搬过来。
<div align=center>
<img src="/images/blog_19.png"  width="75%" />  
</div>

&emsp;
每次写完文章，用`hugo`生成了之后，都需要上传至Github仓库，这里我把我上传的过程写一下：  
首先在网站public目录中打开Git，然后4条指令就搞定：
```
git add .
git commit -m "注释"
git pull
git push origin master
```



### 2.Github Page
在网站仓库的“settings”中倒数第二个“Pages”中设置，启用了之后自动就给一个域名，可以直接访问。

## 三、域名购买和绑定Github Page
续待未完。

## 四、附录
### 1.Md文章写作
### 2.Hugo主题自定义



















