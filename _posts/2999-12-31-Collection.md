---
title: $\bf\text{收集}$
tags: Math
---

长期更新, 收集各种问题/技巧/日常/诸如此类.

<!--more-->

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
<p align="right">$\blacksquare$</p>

$\bf 2.$ 记 $C_{[a,b]}$ 是 $[a,b]$ 上所有连续函数构成的环(加法和乘法就是函数相加和相乘),求其极大理想.
{:.warning}

**解** 首先, 记

$$\mathfrak{m}_{x_0} := \{f \in C_{[a,b]}: f(x_0) = 0\}\,\,\, x_0 \in [a,b].$$

任$$f,g\in \mathfrak{m}_{x_0}$$,任意$$h \in C_{[a,b]}$$, 有$$(f+g)(x_0) = 0$$, $$(hf)(x_0) = 0$$. 这说明  $$\mathfrak{m}_{x_0}$$ 是 $C_{[a,b]}$ 的极大理想. 下面说明其所有极大理想都有形式 $\mathfrak{m}_{x_0}$.

设 $\mathfrak{m}$ 是 $C_{[a,b]}$ 的极大理想. 记

$$
	V = \{x : f(x) = 0, \forall f \in \mathfrak{m}\}.
$$

先说明 $V$ 非空. 若不然, 任意 $x \in [a,b]$, 存在 $f \in \mathfrak{m}$ 使 $f(x) \ne 0$. $f$ 连续, 故存在开集 $U_x$ 使 $f$ 在 $U_x$ 上不变号. $$\{U_x\}$$ 覆盖 $[a,b]$, 从而存在有限覆盖. 记 $U_{x_1},\cdots , U_{x_n}$ 覆盖 $[a,b]$, $f_i 在 U_{x_i} (1 \le i \le n)$ 上不变号(不为 $0$). 则

$$
	f = f_1^2 + f_2^2 + \cdots + f_n^2 \in \mathfrak{m}, \,\,\,\,\,\,\, f(x) > 0, \forall x \in [a,b].
$$

这导致 $C_{[a,b]}$ 的单位 $f$ 属于 $$\mathfrak{m}$$, 矛盾.

现在取 $x_0 \in V$, 有 $$\mathfrak{m} \subset \mathfrak{m}_{x_0}$$, 而 $$\mathfrak{m}$$ 是极大理想, 这导致 $$\mathfrak{m} = \mathfrak{m}_{x_0}$$.
<p align="right">$\blacksquare$</p>

$\bf 11.28$

$\bf 1.$ 设群 $G$, $N$ 是其正规子群, 且 $(G:N)$ 和 $\mid N \mid$ 互素. 证明: 任意 $g \in \mathrm{Aut}(G)$, 有 $g(N) = N$.
{:.warning}

**证明** 任意 $g \in \mathrm{Aut}(G)$, $n \in N$, 有 $o(g(n)) = o(n) \mid\,\,\mid N \mid$. 于是 $o(g(n))$ 和 $(G:N)$ 互素. 考虑 $g(n)$ 在商群 $G/N$ 中的像, 由 $\mid G/N\mid = (G:N)$ 和 $o(g(n))$ 互素, 导致 $g(n)$ 在 $G/N$ 中为 $1$. 说明 $g(n) \in N$. 因此 $g(N) \subset N$. 同理, $g^{-1}\in \mathrm{Aut}(G)$, 故 $g^{-1}(N) \subset N$, 从而 $N\subset g(N)$, 故 $g(N) = N$.
<p align="right">$\blacksquare$</p>

$\bf 2.$ 已知实反对称矩阵 $A_{m\times m}$ 和 $C_{n \times n}$. 已知矩阵 $B_{m \times n}$. 证明: $A+I_m$ 可逆,且 $C-I_n-B^T(A+I_m)^{-1}B$ 可逆.
{:.warning}

**证明** 设 $X \in \mathbb{R}^{n \times 1}$, 有

$$
(A+I_m)X = 0 \Longrightarrow X^T(A+I_m)X = 0.
$$

记 $X=(x_1,x_2,\cdots x_m)^T$, 得到 $X^T(A+I_m)X = x_1^2 + x_2^2 + \cdots + x_m^2$. 这说明 $(A+I_m)X = 0 \Rightarrow X = O$. 因此 $A+I_m$ 可逆.

同理, $C-I_n$ 可逆.

设

$\bf 12.4$

$\bf 1.$ 设正整数 $a,b$. $a\mathbb{Z}/ab\mathbb{Z} \cong \mathbb{Z}/b\mathbb{Z}$(环同构) $\Leftrightarrow (a,b)=1$.
{:.warning}

由 $a\mathbb{Z} + b\mathbb{Z} = (a,b)\mathbb{Z}$ 和 $a\mathbb{Z} \cap b\mathbb{Z} = [a,b]\mathbb{Z}$.

注: 若有上述同构, 则 $a\mathbb{Z}/ab\mathbb{Z}$ 含幺元. 试着找到这个幺元:

$$
a^2xy \equiv ay \pmod{ab}, \forall y \in \mathbb{Z} \Longleftrightarrow (ax-1)y \equiv 0 \pmod {b}, \forall y \in \mathbb{Z}.
$$

$\bf 12.5$

$\bf 1.$ 现有 $1000$ 名员工与一个老板. 老板将员工排成一排, 自己站在排尾. 老板给员工与自己标以序号 $1,2,\cdots, 1000,1001$, 不同的人标号不同. 每个人都只能看到站在自己前面的所有人的标号. 老板令员工从后至前报出一个 $1 \sim 1001$ 的整数, 报出过的整数不能再报. 结束后报出整数等于标号的员工将会留下, 否则将会被开除.  
员工十分团结, 事前他们约定令尽可能多的人留下. 请你设计一种方法实现.
{:.warning}

**答案** 将他们(包括老板)与标号看成一个$1,2,\cdots ,1001$的置换, 第 $1000$ 号员工只有两个数的位置不知道, 他报出使整个置换成为偶置换时他的标号(交换两个数奇偶性改变). 第 $999$ 名员工有三个数的位置不知道. 他将 $1000$ 号员工报出的数赋予 $1000$ 号员工后就只剩两个数字的位置不明确. 为了使整个置换成为偶置换, 他报出相应的那个数字. 递归可知 $1$ 到 $999$ 号的每个人都可以知道自己的标号.

# 2020-3-27

https://math.stackexchange.com/questions/2634576/localization-of-maximal-ideal-is-again-a-maximal-ideal-and-the-residue-fields-ar?r=SearchResults

我裂开来,分式环保证正合列.


3-29

https://math.stackexchange.com/questions/74198/question-on-a-result-of-artin-and-tate?r=SearchResults

https://math.stackexchange.com/questions/1674183/integral-and-prime-ideal-in-dedekind-domain?r=SearchResults&newreg=f1891a0988704aa487759eb4ca802b0c

4-14

Problem. 求

$$\sum_{k=0}^{n}\frac{k}{k+2}\binom{n}{k}(-1)^k$$

解1. 看到$\frac{k}{k+2} = 1 - \int_{0}^1 2x^{k+1} \mathrm{d}x$,有

$$\begin{aligned}
    \mathrm{Left}&= \sum_{k=0}^{n} \binom{n}{k}(-1)^k + 2\sum_{k=0}^{n}\int_{0}^1 x^{k+1}\binom{n}{k}(-1)^{k+1} \mathrm{d}x\\
    &= -2\int_{0}^1 x(1-x)^n \mathrm{d}x = -\frac{2}{n^{2}+3n+2}.
\end{aligned}$$

解2.

$$
    \frac{2}{k+2}\binom{n}{k} = 2\frac{n!(k+1)}{(k+2)!(n-k)!} = \frac{2}{n+1}\binom{n+1}{k+1} - \frac{2}{(n+1)(n+2)}\binom{n+2}{k+2}.
$$

Problem. 求$d= \mathrm{gcd}\left(\binom{n}{1},\cdots,\binom{n}{n-1}\right)$.

解1. 设素数$p$,有$p \mid d \Longleftrightarrow (t+1)^n = t^n+1 \in \mathbb{F}_p[t]$.后者导致$t^n+1$只有一个根.设$n = p^rs$,$\mathrm{gcd}(s,p) = 1$,有$t^n+1=(t^s+1)^{p^r}$,从而$t^s+1$只有一根,而$(st^{s-1},t^s+1) \overset{\underset{\mathrm{s \ne 0}}{}}{=} (t^{s-1},t^s+1)=1$,有$t^s+1$无重根,从而$s=1$,$n = p^r$.

也就是说,当$n$包含两个或以上个素因子时,$d=1$.

我们有$p \mid\mid \binom{p^r}{p^{r-1}}$.故当$n = p^r$时,$d=p$.

2020.4.29

$(1+6\mathbb{Z})^{-1}\mathbb{Z}[\frac{1}{6}] =\mathbb{Q}$.
{:.warning}

设$k \in \mathbb{Z}$,设$k = k_0k_1$,其中$k_1$与$6$互素,$k_0$只有素因子$2,3$.存在$u \in \mathbb{Z}$,使得$uk_1 \equiv 1 \pmod{6}$.存在$v \in \mathbb{Z}$使得$k_0v$是$6$的幂,记为$6^n$.于是

$$
\frac{1}{k} = \frac{1}{k_0k_1} = \frac{uv}{k_0k_1uv} = \frac{uv}{6^nk_1u} \in (1+6\mathbb{Z})^{-1}\mathbb{Z}[\frac{1}{6}].
$$

注, $(1+6\mathbb{Z})^{-1}\mathbb{Z}$是主理想整环,也就是.设$R$是PID,设$u$是$R$的不可约元.即使$R$有超过两个极大理想,$R[\frac{1}{u}]$也可能是域.

请对域上一元多项式环$F[x]$考虑以上命题.


2020.6.16

设$$\mathbb{F}$$是域,设$V$是有限维$F$线性空间.设$A,B$是$V$的线性变化.若$B$和任何和$A$交换的线性变化交换,证明$B$可以表示为$A$的多项式.

https://math.stackexchange.com/questions/497806/matrices-b-that-commute-with-every-matrix-commuting-with-a

https://math.stackexchange.com/questions/767975/textv-is-semisimple-as-a-kx-module-if-and-only-if-a-in-operatornameen
