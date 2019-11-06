---
title: $\bf\text{收集}$
tags: Math
---

长期更新, 收集各种问题/技巧/日常/诸如此类.

$\bf 2019$

$\bf 11\,\text{月}\,2\,\text{日}$

$\bf 1.$
{:.warning}

$\bf 2.$ 求 $\int\frac{x^3}{\sqrt{-x^2+2x+1}} dx$.
{:.warning}

$\bf 3. \text{(Circulant Determinant)}$ 见 [$\bf Wolfram$](http://mathworld.wolfram.com/CirculantDeterminant.html) 和 [$\bf StackExchange$](https://math.stackexchange.com/questions/386526/circular-determinant-problem)
{:.warning}

$\bf 11.6$

$\bf 1.$ 已知群 $G$, $N$ 是 $G$ 的正规子群, $\mid N\mid = n$, $(G:N)=m$ 且 $(n,m)=1$. 求证: $N$ 是 $G$ 唯一的 $n$ 阶子群.
{:.warning}

**证明** 设 $H \leqslant G$ 是 $G$ 的 $n$ 阶子群, $N \triangleleft G$, 故 $HN \leqslant G$. 有 $\mid HN\mid\, \mid\,  \mid G \mid = nm$, 而 $\mid HN \mid = \mid H \mid  \mid N \mid / \mid H\cap N \mid$ 与 $m$ 互素, 故 $\mid HN \mid \mid n$. 又 $n\le  \mid HN \mid$ (因 $N \leqslant HN$), 故 $n =   \mid HN \mid$. 从而 $\mid H\cap N \mid =n$, 故 $H=N$.
<p align="right">$\blacksqure$</p>

$\bf 2.$ 记 $C_{[a,b]}$ 是 $[a,b]$ 上所有连续函数构成的环(加法和乘法就是函数相加和相乘),求其极大理想.
{:.warning}

(注: 设 $I$ 是 $C_{[a,b]}$ 的一个理想.设 $x_0\in [a,b]$, 考虑 $$I_0=\{f(x_0) \mid f \in I\}$$ 是 $\mathbb{R}$ 的理想,从而为 $(0)$ 或 $\mathbb{R}$. 接着考虑形如 $$\{f(x)\in C_{[a,b]} \mid f(h) = 0\}$$ 构成的集合, 其中 $h \in[a,b]$. 证明它是极大理想)

(注: 我口胡的,可能不对)

