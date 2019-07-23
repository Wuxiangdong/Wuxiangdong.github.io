---
title: 伽罗瓦群的计算
tags: Math Algebra 伽罗瓦理论
---
~~认真抄书(逃~~

## 伽罗瓦的原始思想

设 $E$ 是域 $F$ 上多项式 $f(x)$ 在域 $F$ 上的分裂域. 将伽罗瓦群 $\mathrm{Gal}(E/F)$ 称为多项式 $f(x)$ 或方程 $f(x)=0$ 在 $F$ 上的伽罗瓦群, 记为 $\mathrm{Gal}(f(x), F)$. 或简记为 $G_f$. 具体方程的伽罗瓦群的计算是伽罗瓦理论的重要课题. 这里主要讨论无重根多项式的伽罗瓦群, 这里 "无重根" 保证了 $E/F$ 是有限伽罗瓦扩张, 从而 $\mid G_f \mid = [E:F]$.
<!--more-->
<!-- vim-markdown-toc GFM -->

* [判别式](#判别式)

<!-- vim-markdown-toc -->

对称群 $S_n$ 的子群 $G$ 称为 $S_n$ 的可迁子群, 或称为集合 $$\Lambda = \{1,2,\cdots ,n\} $$ 上的可迁置换群, 如果任意 $i, j\in\Lambda$, 存在 $\sigma \in G$ 使得 $\sigma(i) = j$. 我们将 $S_n$ 视为 $f(x)$ 的根集 $$\{r_1,\cdots ,r_n\} $$ 上的对称群. 例如, $(12)$ 指的是 $(r_1r_2)$.

**定理** 设 $r_1,\cdots ,r_n$ 是域 $F$ 上 $n$ 次无重根多项式 $f(x)$ 的全部根. 则  
$\mathrm{(i)}$ 伽罗瓦群 $G_f$ 是 $S_n$ 的阶为 $[E:F]$ 的子群;  
$\mathrm{(ii)}$ 设 $\sigma \in S_n$, 则 $\sigma\in G_f$ 当且仅当 $\sigma$ 保持 $f(x)$ 的根之间的所有代数关系, 即若 $g(r_1,\cdots ,r_n) = 0$, 其中 $g \in F[x_1,\cdots ,x_n]$. 则 $g(\sigma(r_1),\cdots ,\sigma(r_n)) = 0$;  
$\mathrm{(iii)}$ $f(x)$ 在 $F$ 上不可约当且仅当 $G_f$ 是可迁子群.
{:.info}


**证明** 设 $E$ 是 $f(x)$ 在 $F$ 上的分裂域.

$\mathrm{(i)}$: 设 $\sigma \in G_f$.由 $0 = f(r_i)$ 知 $0 = \sigma(0) = f(\sigma(r_i))$, 因而 $\sigma(r_1),\sigma(r_2),\cdots ,\sigma(r_n)$ 也是 $f(x)$ 的两两不同的根, 从而是 $r_1,\cdots ,r_n$ 的一个置换. 于是

$$
\sigma\mapsto \begin{pmatrix} 
r_1 & r_2 & \cdots & r_n \\
\sigma(r_1) & \sigma(r_2) & \cdots & \sigma(r_n)
\end{pmatrix}
$$

是 $G_f$ 到 $S_n$ 的同态. 因 $E = F(r_1,\cdots ,r_n)$, 故 $\sigma$ 由值 $\sigma(r_1),\cdots ,\sigma(r_n)$ 唯一确定, 因此这个同态是单射, 从而 $G_f$ 可以视为 $S_n$ 的子群. 由 $f(x)$ 无重根知 $\mid G_f \mid = \mid \mathrm{Gal}(E/F) \mid = [E:F]$.

$\mathrm{(ii)}:$ 设 $\sigma \in G_f$. 若 $g(r_1,\cdots ,r_n) = 0$, 则

$$
0 = \sigma(0) = \sigma(g(r_1,\cdots,r_n)) = g(\sigma(r_1),\cdots,\sigma(r_n)).
$$

即 $\sigma$ 保持 $f(x)$ 根之间的所有代数关系. 反之, 设 $\sigma \in S_n$ 且保持 $f(x)$ 根之间的所有代数关系. 任意 $a \in E$, 存在 $\psi \in F[x_1,\cdots ,x_n]$ 使 $a = \psi(r_1,\cdots ,r_n)$. 定义 $E$ 的一个 $F$-自同构为

$$
\pi: E\rightarrow E, a = \psi(r_1,\cdots ,r_n) \mapsto \psi(\sigma(r_1),\cdots ,\sigma(r_n)).
$$

首先说明这个映射的定义是合理的, 即映射的值 $\pi(a)$ 与 $\psi$ 的选取无关. 若 $a = \psi(r_1,\cdots ,r_n) = \phi(r_1,\cdots ,r_n)$, 则 $\psi(r_1,\cdots ,r_n) - \phi(r_1,\cdots ,r_n) = 0$, 其中 $\psi,\phi \in F[x_1,\cdots ,x_n]$. $\sigma$ 保持 $r_1,\cdots ,r_n$ 的代数关系, 故 $\psi(\sigma(r_1), \cdots , \sigma(r_n)) - \phi(\sigma(r_1),\cdots ,\sigma(r_n)) = 0$, 从而 $\psi(\sigma(r_1), \cdots , \sigma(r_n)) = \phi(\sigma(r_1),\cdots ,\sigma(r_n))$. 于是 $\pi$ 确实是 $E$ 到自身的映射. 可以看出 $\pi$ 保持 $E$ 的加法和乘法, 从而 $\pi \in \mathrm{Gal}(E/F) = G_f$. 因为 $\pi(r_i) = \sigma(r_i)$, 故 $\pi$ 作为 $S_n$ 的元就是 $\sigma$.

$\mathrm{(iii)}$: 设 $f(x)$ 在 $F[x]$ 中不可约. 对于 $f(x)$ 的任意根 $r_i$, $r_j$ 来说, $r_i$, $r_j$ 在 $F$ 上的极小多项式均为 $f(x)$, 因此存在 $F$-同构 $\sigma: F(r_i) \rightarrow F(r_j)$ 使得 $\sigma(r_i) = r_j$. $E$ 可以看成 $f(x)$ 在 $F(r_i)$ 和 $F(r_j)$ 上的分裂域, 由同构延拓定理, $\sigma$ 可以延拓为 $\pi: E\rightarrow E$, 从而 $\pi \in G_f$ 且 $\pi(r_i) = r_j$, 即 $G_f$ 是 $S_n$ 的可迁子群. 反之, 设 $G_f$ 是 $S_n$ 的可迁子群. 对于 $f(x)$ 的任意根, 存在 $\sigma \in G_f$ 使 $\sigma(r_1) = r_j$. 令 $f_1(x)$ 是 $r_1$ 在 $F$ 上的极小多项式. 将 $\sigma$ 作用在等式 $0 = f_1(r_1)$ 的两边, 我们得到

$$
0 = \sigma(0) = \sigma(f_1(r_1)) = f_1(r_j).
$$

这说明 $f(x)$ 的任意根均为 $f_1(x)$ 的根, 于是 $f(x) \mid f_1(x)$, 由 $f_1(x)$ 不可约知 $f(x) = f_1(x)$, 从而 $f(x)$ 在 $F$ 上不可约.
<p align="right">$\blacksquare$</p>

伽罗瓦本人就是将 $G_f$ 定义为保持 $f(x)$ 的根 $r_1,\cdots ,r_n$ 之间全部代数关系的根集 $$\{r_1,\cdots ,r_n\}$$ 上的所有置换构成的群. 于是 $G_f$ 反映了 $f(x)$ 根之间的对称. $G_f$ 需保持 $f(x)$ 对称, 因此 $G_f$ 一般不是 $S_n$, 而是 $S_n$ 的某个子群.

将 $G_f$ 定义为 $\mathrm{Gal}(E/F)$ 是戴德金的贡献: 这不仅使得伽罗瓦理论取得了现代的形式, 而且使伽罗瓦群的计算更具可操作性: 因为从计算的观点来看, 确定 $f(x)$ 的根之间的所有代数关系是困难的. 当然, 将伽罗瓦原始思想理解清楚了也恰好就是我们今天使用的戴德金的定义.

**例** 求有理数域 $\mathbb{Q}$ 上可约多项式 $x^4 + 4$ 的伽罗瓦群.
{:.warning}

**解** 设 $f(x) = x^4 + 4$, $E$ 是 $f(x)$ 在 $\mathbb{Q}$ 上的分裂域. $f(x)$ 的四个根分别为 $1+i, -1 + i, -1 -i, 1 - i$. 于是 $E =\mathbb{Q}(i)$. 从而 $[E:F] = 2$. $\mathrm{Gal}(E/F)$ 有两个元 $\sigma_1 = \mathrm{Id}$, $\sigma_2: i \mapsto -i$. 记 $r_1 = 1+i, r_2 = -1+i, r_3 = -1-i, r_4 = 1-i$, 将 $G_f$ 看成 $$\{r_1,r_2,r_3,r_4 \}$$ 的对称群. 则 $\sigma_1 = (1),\sigma_2 = (14)(23)$. 这说明 $$G_f = \{(1), (14)(23)\}$$.

注: $r_1$ 和 $r_4$ 有相同的代数关系, 它们在 $\mathbb{Q}$ 上的极小多项式为 $x^2 -2x + 2$. $r_2$ 和 $r_3$ 有相同的代数关系, 它们在 $\mathbb{Q}$ 上的极小多项式为 $x^2 + 2x + 2$. 而 $x^4 + 4 = (x^2 - 2x+ 2)(x^2 + 2x + 2)$.

**例** 设 $G$ 是 $S_n$ 的可迁子群, $H$ 是 $G$ 的正规子群. 则 $$\{1,2,\cdots ,n\}$$ 每个 $H$-轨道有相同的长度. 由此证明: 若 $n=p$ 是素数且 $$H \ne \{1\}$$, 则 $H$ 也是 $S_n$ 的可迁子群, 从而 $p \mid \,\mid H\mid$, 进而 $H$ 含有 $p$-轮换.
{:.warning}

**证明** 对 $1 \le a\le n$, 记 $a$ 所在的 $H$-轨道为 $\Delta_a$. 由轨道公式, 有 $\mid \Delta_a \mid = [H : G_a]$, 其中 $$G_{a} = \{\sigma \in H \mid \sigma(a) = a\}$$. 只需证明 $\mid G_{a}\mid = \mid G_{b} \mid$, $\forall 1\le a,b \le n$. $G$ 是可迁子群, 存在 $\pi \in G$ 使得 $\pi(a) = b$.  $H$ 是 $G$ 的正规子群, 故 $\forall \sigma \in H$, $\pi\sigma\pi^{-1} \in H$. 记

$$
	\eta_1: G_a \rightarrow G_b, \sigma \mapsto \pi\sigma\pi^{-1}. \\
	\eta_2: G_b \rightarrow G_a, \sigma \mapsto \pi^{-1}\sigma\pi.
$$

对任意 $\sigma \in G_a$, $\pi\sigma\pi^{-1}(b) = \pi\sigma(a) = \pi(a) = b$, 因此 $\eta_1$ 确实是 $G_a \rightarrow G_b$ 的映射. 同理 $\eta_2$ 是 $G_b \rightarrow G_a$ 的映射. 可以验证 $\eta_1\eta_2 = \eta_2\eta_1 = \mathrm{Id}$, 这说明 $\eta_1$, $\eta_2$ 是双射, 从而 $\mid G_a\mid = \mid G_b\mid$.

下设 $n=p$ 是素数且 $$H \ne {1}$$. 则 $$\{1,2,\cdots ,p\}$$ 的每一个 $H$-轨道有相同的长度. 记每一个轨道的长度为 $l$, 则 $l \mid p$. $$H \ne \{1\}$$ 故 $l \ne 1$, 从而只能是 $l = p$. 这说明 $H$ 在 $$\{1,2,\cdots ,p\}$$ 上的作用是传递的, 从而 $H$ 也是可迁子群. $p$ 是 $H$ 某个子群的阶数, 故 $p \mid \, \mid{H}\mid$. 从而 $H$ 有 $p$ 阶元. $H$ 的每个元素写为不相交轮换之积, 有 $H$ 的每个元素的阶为其每个轮换长度的最小公倍数. $p$ 是素数, 从而 $H$ 的 $p$ 阶元素必然是 $p$-轮换. 这说明 $H$ 有 $p$-轮换.
<p align="right">$\blacksquare$</p>

**例** 证明对称群 $S_4$ 的全部可迁子群是  
$\mathrm{(i)} S_4,$  
$\mathrm{(ii)} A_4,$  
$$\mathrm{(iii)} V = \{(1), (12)(34), (13)(24), (14)(23)\},$$  
$\mathrm{(iv)} C_4 = \langle(1234)\rangle$ 及其共轭子群 $\langle(1243)\rangle$ 和 $\langle(1324)\rangle.$  
$\mathrm{(v)}$ 3 个 Sylow-$2$ 子群: $$D_4 = V \cup \{(1234),(1432),(24),(13)\}$$ 及其共轭子群 $$V \cup \{(1423), (1324), (12), (34)\}$$ 和 $$V \cup \{(1243),(1342),(14),(23)\}.$$
{:.warning}

**证明**  设 $H$ 是 $S_4$ 的可迁子群,  $H$ 在 $$\{1,2,3,4\}$$ 上的作用只有一个轨道, 长度为 $4$. 从而 $4 \mid\,\mid H\mid\,\mid 24$. 于是 $H$ 的阶只能是 $4, 8, 12$ 或 $24$. 其中 $S_4$ 阶为 $24$ 或 $12$ 的子群分别只有 $S_4$ 和 $A_4$. 而 $S_4$ 阶为 $8$ 的子群是 $S_4$ 的 Sylow-$2$ 子群. 可以验证它们是可迁子群. 接下来考虑 $S_4$ 阶为 $4$ 的可迁子群. 阶为 $4$ 的群要么为循环群, 要么同构于 $\mathbb{Z}_2 \oplus \mathbb{Z}_2$. $S_4$ 的 $4$ 阶循环子群为 $\langle(1234)\rangle$ 和共轭, 它们都是可迁子群. $S_4$ 的二阶元为 $(12)$ 和它的共轭, $(12)(34)$ 和它的共轭. 从而 $S_4$ 同构于 $\mathbb{Z}_2\oplus \mathbb{Z}_2$ 的子群为 $$\{(1),(12),(34),(12)(34)\}$$ 和它的共轭以及正规子群 $$\{(1),(12)(34),(13)(24),(14)(23)\}$$. 前者不是可迁子群而后者是可迁子群. 故 $S_4$ 的全部可迁子群就是题中所列.
<p align="right">$\blacksquare$</p>

## 判别式

设 $f(x)$ 是 $F$ 上无重根多项式, $r_1,\cdots, r_n$ 是其全部根. $E$ 是 $f(x)$ 在 $F$ 上的分裂域. 并且视伽罗瓦群 $G_f$ 为对称群 $S_n$ 的子群. 记 $A_n$ 为 $n$ 次交错群. 那么在 $E/F$ 的对应下 $G_f \cap A_n$ 对应的中间域是什么?

令 $\Delta = \Delta(f) = \prod_{1 \le i < j \le n} (r_i-r_j) \in E$. 对每个 $\sigma \in G_f$, 有 $\sigma(\Delta^2) = \sigma(\Delta)^2 = (\pm \Delta)^2 = \Delta^2$ (因为 $\sigma$ 置换 $r_1,\cdots ,r_n$, 从而只改变 $\Delta$ 的符号). 这说明 $\Delta^2 \in F$. 称 $d(f) = \Delta^2 \in F$ 为 $f(x)$ 在 $F$ 上的 **判别式**. 对任意多项式(不一定无重根) $f(x)$, 其判别式同样定义, 则 $f(x)$ 无重根当且仅当 $d(f) \ne 0$. 令 $$F^2 = \{a^2 \mid a \in F\}$$. 则 $\Delta \in F$ 当且仅当 $d(f) = \Delta^2 \in F^2$. 若 $\mathrm{Char} F \ne 2$, 一个置换 $\sigma$ 是偶置换当且仅当 $\sigma(\Delta) = \Delta$ (一次对换改变一次 $\Delta$ 的符号). 于是 $G_f \cap A_n = \mathrm{Gal}(E/F(\Delta))$, 从而 $G_f \cap A_n$ 对应的中间域就是 $F(\Delta)$. 这证明了下面的 $\mathrm{(i)}$.

**引理** 设域 $F$ 特征不为 $2$, $E$ 是 $n$ 次无重根多项式 $f(X) \in F[x]$ 在 $F$ 上的分裂域. 则  
$\mathrm{(i)}$ $\mathrm{Gal}(E/F(\Delta)) = G_f \cap A_n$, $\mathrm{Inv}(G_f\cap A_n) = F(\Delta)$.  
$\mathrm{(ii)}$ $G_f \in A_n$ 当且仅当 $\Delta \in F$, 这等价于 $d(f) \in F^2$.  
$\mathrm{(iii)}$ 若 $f(x)$ 是 $F$ 上的 $3$ 次不可约多项式, 则  
$$
	G_f = 
		\begin{cases}
			A_3 &, \text{若 $d(f) \in F^2$},\\
			S_3  &, \text{若 $d(f) \notin F^2$}.
		\end{cases}
$$
{:.info}

**证明** $\mathrm{(ii)}$ $G_f \subseteq A_n$ 当且仅当 $G_f \cap A_n = G_f$, 使用伽罗瓦理论基本定理, 这等价于 $F(\Delta) = F$, 等价于 $\Delta \in F$.

$\mathrm{(iii)}$ $G_f$ 是 $S_3$ 的可迁子群, 从而只是 $S_3$ 或 $A_3$. 再由 $\mathrm{(ii)}$ 可知结论成立.
<p align="right">$\blacksquare$</p>

$\Delta$ 是 $r_1,r_2,\cdots ,r_n$ 的范德蒙行列式, 记 $r_1,\cdots ,r_n$ 的初等对称多项式 

$$p_i  = \sum_{1 \le k_1 < \cdots < k_i \le n}{r_{k_1}r_{k_2}\cdots r_{k_i}}, i=1,2,\cdots ,n.$$

则 $d(f) = \Delta^2$ 是关于 $r_1,\cdots ,r_n$ 的对称多项式, 从而是 $p_1,\cdots ,p_n$ 的多项式. 例如

$2$ 次多项式 $f(x) = x^2 - a_1x + a_2$ 的判别式为

$$
d(f) = a_1^2 - 4a_2.
$$ 

$3$ 次多项式 $f(x) = x^3 - a_1x^2 + a_2x - a_3$ 的判别式为

$$
d(f) = -4a_1^3a_3 + a_1^2a_2^2 + 18a_1a_2a_3 - 4a_2^3 - 27a_3^2.
$$
