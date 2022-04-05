+++
title = "一些无穷级数"
date = "2021-12-11"
description = ""
math = true
reward = false
featured = false
draft = true
categories = [
  "数学类"
]
tags = [
  "thougts",
  "infinite series"
]
series = [
  "数学随便想"
]
images = [

]

+++



随便写写最近所看到的数学。

<!--more-->

最近在读数学史，终于发现了喜欢的东西了，就是无穷级数。之前一直对分析不是很感兴趣（但是也不讨厌），所以有了点兴趣让我也很开心。今天（其实结果写了几天）随便写一点无穷级数（就是写写书上的东西），就突出一个词：“随便”。毕竟我今后是想做数学事业的，所以我还是想多花点时间在数学上……

背景在17，18世纪……人物挺多，最耀眼的当然是Euler。

顺序就不谈了，我随便写写，没有什么提纲顺序的。生成的文章右边小栏上有目录可以看看。

## 开始&一般


### 1360 Oresme

$$
级数:\frac{1} {2} + \frac{1}{2} +  ( \frac{1}{4} + \frac{1}{4}) + ( \frac{1}{8} + \frac{1}{8} + \frac{1}{8} + \frac{1}{8}  )+\cdots 发散 
$$
于是比以上大的调和级数:
$$
1+\frac{1}{2}+\frac{1}{3}+\frac{1}{4}+\frac{1}{5}+\cdots发散
$$
<br>


### Mercator, Newton

$$
log(1+x) = x - \frac{1}{2}x^{2} + \frac{1}{3}x^{3}+\cdots
$$
在$x=2$时右边的级数为无穷，而它应该为$log(3)$。
$$
2 +(-2+\frac{8}{3}) + (-4 + \frac{32}{5})+\cdots 
$$
<br>

### 1671 Collins
$$
\begin{aligned} &\tan x = x+\frac{x^3}{3}+\frac{2}{15}x^{5}+\frac{17}{315}x^7+\cdots \\\\ &\sec x = 1+\frac{x^2}{2}+\frac{5}{24}x^4 + \frac{61}{720}x^6+\cdots \end{aligned}
$$
<br>


### 1675 Leibniz
$$
\frac{\pi}{4} = 1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots
$$
<br>

### 1668 James Gregory
收敛得较快的级数，在计算中更有用。
$$
\frac{1}{2}log\frac{(1+z)}{(1-z)} = z+\frac{1}{3}z^3+\frac{1}{5}z^5+\cdots
$$
<br>

## 推理&计算

### James Bernoulli&John Bernoulli
#### ①
从级数
$$
N = \frac{a}{c}+\frac{a}{2c}+\frac{a}{3c}+\cdots 
$$
得到（注意级数是发散的）。
$$
N - \frac{a}{c}= +\frac{a}{2c}+\frac{a}{3c}+\cdots
$$
将以上两式相减得：
$$
\frac{a}{c} = \frac{a}{1\cdot 2c}+\frac{a}{2\cdot 3c}+\frac{a}{3\cdot 4c}+\cdots
$$
James说这样的做法是有问题的，如果不慎重是不能用的（级数发散的原因）。

#### ②











