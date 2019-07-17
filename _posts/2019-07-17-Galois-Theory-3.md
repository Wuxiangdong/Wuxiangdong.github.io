---
title: 伽罗瓦群的计算
tags: Math Algebra 伽罗瓦理论
---
~~认真抄书(逃~~

## 伽罗瓦的原始思想

设 $E$ 是域 $F$ 上多项式 $f(x)$ 在域 $F$ 上的分裂域. 将伽罗瓦群 $\mathrm{Gal}(E/F)$ 称为多项式 $f(x)$ 或方程 $f(x)=0$ 在 $F$ 上的伽罗瓦群, 记为 $\mathrm{Gal}(f(x), F)$. 或简记为 $G_f$. 具体方程的伽罗瓦群的计算是伽罗瓦理论的重要课题. 这里主要讨论无重根多项式的伽罗瓦群, 这里 "无重根" 保证了 $E/F$ 是有限伽罗瓦扩张, 从而 $\mid G_f \mid = [E:F]$.

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
\end{pmatrix}.
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

将 $G_f$ 定义为 $\mathrm{Gal}(E/F)$ 是戴德金的共线: 这不仅使得伽罗瓦理论取得了现代的形式, 而且使伽罗瓦群的计算更具可操作性: 因为从计算的观点来看, 确定 $f(x)$ 的根之间的所有代数关系是困难的. 当然, 将伽罗瓦原始思想理解清楚了也恰好就是我们今天使用的戴德金的定义.

**例** 求有理数域 $\mathbb{Q}$ 上可约多项式 $x^4 + 4$ 的伽罗瓦群.
{:.warning}

**解** 设 $f(x) = x^4 + 4$, $E$ 是 $f(x)$ 在 $\mathbb{Q}$ 上的分裂域. $f(x)$ 的四个根分别为 $1+i, -1 + i, -1 -i, 1 - i$. 于是 $E =\mathbb{Q}(i)$. 从而 $[E:F] = 2$. $\mathrm{Gal}(E/F)$ 有两个元 $\sigma_1 = \mathrm{Id}$, $\sigma_2: i \mapsto -i$. 记 $r_1 = 1+i, r_2 = -1+i, r_3 = -1-i, r_4 = 1-i$, 将 $G_f$ 看成 $$\{r_1,r_2,r_3,r_4 \}$$ 的对称群. 则 $\sigma_1 = (1),\sigma_2 = (14)(23)$. 这说明 $$G_f = \{(1), (14)(23)\}$$.

注: $r_1$ 和 $r_4$ 有相同的代数关系, 它们在 $\mathbb{Q}$ 上的极小多项式为 $x^2 -2x + 2$. $r_2$ 和 $r_3$ 有相同的代数关系, 它们在 $\mathbb{Q}$ 上的极小多项式为 $x^2 + 2x + 2$. 而 $x^4 + 4 = (x^2 - 2x+ 2)(x^2 + 2x + 2)$.
