+++
title = "Stolz定理和一道例题"
date = "2022-06-17"
description = ""
math = true
reward = false
featured = false
categories = [
  "数学类"
]
tags = [
  "数学分析",
  "笔记"
]
series = [
  "数学随想"
]
images = [

]

+++



<!--more-->

## 一、Stolz定理<sup>[1]</sup>

### 1.$\frac{0}{0}$型Stolz定理

设{$a_n$}和{$b_n$}都是无穷小量，其中{$a_n$}还是严格单调减少数列，又存在
$$
\lim_{n\rightarrow \infty }\frac{b_{n+1}-b_{n}}{a_{n+1}-a{n}}=l
$$
（其中$l$为有限或$\pm \infty$），则有
$$
\lim_{n\rightarrow \infty } \frac{b_{n}}{a_{n}}=l
$$

---

证：只对有限的$l$作证明.根据条件对$\varepsilon > 0$存在$N$，使得当$n>N$时成立
$$
\left | \frac{b_{n}-b_{n+1}}{a_{n}-a_{n+1}}-l \right | <\varepsilon
$$
由于对每个$n$都有$a_{n}>a_{n+1}$，这样就有
$$
(l-\varepsilon)(a_{n}-a_{n+1})<b_{n}-b_{n+1}<(l+\varepsilon)(a_{n}-a_{n+1})
$$
任取$m>n$，并且将上述不等式中的$n$换成$n+1$，$n+2$，$\cdots $，直到$m-1$，然后将左右这些不等式相加，就得到
$$
(l-\varepsilon)(a_{n}-a_{m})<b_{n}-b_{m}<(l+\varepsilon)(a_{n}-a_{n+1})
$$
即
$$
\left| \frac{b_{n}-b_{m}}{a_{n}-a_{m}}-l \right|<\varepsilon
$$
令$m\rightarrow \infty$，并利用条件$\lim \limits_{n \rightarrow \infty } a_{m}=\lim \limits_{n \rightarrow \infty } b_{m}=0$，就知道当$n>N$时成立
$$
\left| \frac{b_n}{a_n}-l\right| \leq \varepsilon
$$


### 2.$\frac{*}{\infty}$型Stolz定理

设数列{$a_n$}是严格单调增加的无穷大量，又存在
$$
\lim_{n\rightarrow \infty }\frac{b_{n+1}-b_{n}}{a_{n+1}-a{n}}=l
$$
（其中$l$为有限或$\pm \infty$），则有
$$
\lim_{n\rightarrow \infty } \frac{b_{n}}{a_{n}}=l
$$

---

证：只对$l$为有限的情况写出证明。对$\varepsilon>0$存在$N$，使得当$n>N$时成立
$$
\left | \frac{b_{n+1}-b_{n}}{a_{n+1}-a_{n}}-l \right | <\varepsilon
$$
由于对每个$n$有$a_{n+1}>a_{n}$，这样就有
$$
(l-\varepsilon)(a_{n+1}-a_{n})<b_{n+1}-b_{n}<(l+\varepsilon)(a_{n+1}-a_{n})
$$
取定$N$，并且将上述不等式中的$n$换成$N$,$N+1$,$\cdots$,直到$n-1$，然后将所有这些不等式相加，就得到
$$
(l-\varepsilon)(a_{n}-a_{N})<b_{n}-b_{N}<(l+\varepsilon)(a_{n}-a_{N})
$$
即
$$
\left| \frac{b_{n}-b_{N}}{a_{n}-a_{N}}-l \right|<\varepsilon
$$
为了进一步得到关于$\left| \frac{b_n}{a_n}-l \right|$的估计，可以利用恒等式
$$
\frac{b_n}{a_n}-l=(1-\frac{a_N}{a_n})\cdot(\frac{b_n-b_N}{a_n-a_N}-l)+\frac{b_N-la_N}{a_n}
$$
由于$\lim \limits_{n \rightarrow \infty } a_{n}=+\infty$，存在$N_1$，使得当$n>N_1$时成立
$$
0<1-\frac{a_N}{a_n}<2\quad和\quad\left|\frac{b_N-la_N}{a_n} \right|<\varepsilon
$$
则在$n > max \left \\{N,N_1\right \\}$时就得到
$$
\left|\frac{b_n}{a_n}-l \right|<3\varepsilon
$$
**两类Stolz定理对$l$为有限或者$\pm \infty$的情况成立，但是对不带符号的无穷大量$\infty$不成立。且定理的逆命题不成立。**

<br><br>

## 二、一道例题



<center>设已知$\lim \limits_{n \rightarrow \infty } a_{n}=a$，证明：$\lim \limits_{n \rightarrow \infty } \frac{1}{2^n} \sum \limits_{k=0}^{n} \binom{n}{k}a_k=a$</center>

证明方法直接利用极限定义分步法即可。

证明过程中注意
$$
\frac{1}{2^n} \sum \limits_{k=0}^{N} \binom{n}{k}\left| a_k-a \right|<\frac{M(1+n+\cdots+n^N)}{2^n}<\varepsilon
$$
中利用了$\binom{n}{k}<n^k$。可以这样观察这个式子：
$$
\binom{n}{k} = \frac{n!}{k!(n-k)!}=\frac{(n-k+1)(n-k+2)\cdots(n)}{k!}=\frac{(n+1-k)(n+1-k-1)\cdots n}{k\cdot(k-1)\cdots1}<n^k
$$
对于每个单项可以发现$n>\frac{n+1-k-i}{k-i}$。

这个部分其余的证明方法想不出来，反正必须要$ \sum \limits_{k=0}^{N}\binom{n}{k}$部分放缩到是$2^n$的无穷小量即可，当然我们知道这是肯定的。

---

### 1.尝试Stolz

注意到
$$
\begin{aligned}\frac{1}{2^n} \sum \limits_{k=0}^{n} \binom{n}{k}a_k &= \frac{\sum \limits_{k=0}^{n}\binom{n}{k}a_k}{\sum \limits_{k=0}^{n}\binom{n}{k}} \\\\ &=\frac{\binom{n}{0}a_0+\binom{n}{1}+a_1+\cdots+\binom{n}{n}a_n}{\binom{n}{0}+\binom{n}{1}+\cdots+\binom{n}{n}}=\frac{p_n}{q_n} \end{aligned}
$$
但这是如果应用Stolz定理会发现不能简化问题：
$$
\frac{p_{n+1}-p_{n}}{q_{n+1}-q_{n}}=\frac{\binom{n}{1}a_0+\binom{n}{1}a_1+\cdots+\binom{n}{n}a_{n-1}+a_n+a_{n+1}}{\binom{n}{0}+\binom{n}{1}+\cdots+\binom{n}{n}}
$$
<br>

### 2.一些联想

根据这个例题可以立刻联想到一种简单形式：  
设{$x_n$}收敛于$l$，如果$a_n\in R$，则有：
$$
\lim_{n\rightarrow \infty }\frac{a_1x_1+a_2x_2+\cdots+a_nx_n}{a_1+a_2+\cdots+a_n}=l
$$
可以通过极限定义证明是成立的。

那能不能有一个更一般的定理解决上面的例题呢？比如：    
设{$x_n$}收敛于$l$，如果$a_k=f(n,k)$，则有：
$$
\lim_{n\rightarrow \infty }\frac{a_1x_1+a_2x_2+\cdots+a_nx_n}{a_1+a_2+\cdots+a_n}=l
$$
这个问题我思考不了，暂且留在这里，或者用一个更具体的$a_n$可能可以解决问题，这里的题目是组合数，比如：
$$
\lim_{n\rightarrow \infty }\frac{\sum\binom{n}{k}A^{k}B^{n-k}a_k}{\sum\binom{n}{k}A^{k}B^{n-k}}=l
$$
但是这样就已经是正确的结论了。



## 三、Cauchy命题和一些变形

利用Stolz定理可以推出Cauchy命题，当然极限定义也可以证明之：  
(**Cauchy命题**)设{$x_n$}收敛于$l$，则它的前$n$项的算术平均值所成的数列也收敛于$l$，既有
$$
\lim_{n\rightarrow \infty }\frac{x_1+x_2+\cdots+x_n}{n}=l
$$
<br>

其他形式：

1. 若$\lim \limits_{n\rightarrow \infty }(a_n-a_{n-1})=d$，则$\lim \limits_{n\rightarrow \infty }\frac{a_n}{n}=d$
2. 设${a_n}$为正数列，且收敛于$A$，则$\lim \limits_{n\rightarrow \infty }(a_1a_2\cdots a_n)^{\frac{1}{n}}=A$
3. 设${a_n}$为正数列，且存在极限$\lim \limits_{n\rightarrow \infty }\frac{a_{n+1}}{a_n}=l$，则$\lim \limits_{n\rightarrow \infty }\sqrt[n]{a_n}=l$

第一个是等价命题，2和3是推论。后面如果发现有有价值相关联的Cauchy命题的东西的话会补充到这里。





<br>

<br>

<br>

<br>

[1]谢惠民,恽自求. 数学分析习题课讲义. 北京: 高等教育出版社, 2018.