---
title: 有限伽罗瓦扩张
tags: Math Algebra 伽罗瓦理论
---

# 有限伽罗瓦扩张
**伽罗瓦扩张** 是指可分正规扩张, **有限伽罗瓦扩张** 是指有限可分正规扩张.
{:.success}

设 $E/F$ 是任意域扩张, 令  
$$G = \mathrm{Gal}(E/F) = \{\sigma: E \rightarrow F 是域同构 \mid \sigma(a) = a, \forall a \in F\}.$$
则 $\mathrm{Gal}(E/F)$ 对于映射的合成作成群. 记 $$\Omega = \{E/F 的中间域\}$$, $$\Gamma = \{G 的子群\}$$. 考虑如下两个映射, 通常称之为 **伽罗瓦对应**:

$$
    \mathrm{Gal}(E/-): \Omega \rightarrow \Gamma, \mathrm{Gal}(E/-)(M) = \mathrm{Gal}(E/M), \forall M \in \Omega, \\
    \mathrm{Inv}: \Gamma \rightarrow \Omega, \mathrm{Inv}(H) = \{a \in E \mid \sigma(a) = a,\forall \sigma \in H\},\forall H \in \Gamma.
$$

这里 $\mathrm{Gal}(E/M)$ 称作 $E$ 在 $M$ 上的 **伽罗瓦群**; $\mathrm{Inv}(H)$ 称为 $H$ 的不动点域.
<!--more-->

**引理** 设 $E/F$ 是域扩张, $G$,$\Omega$,$\Gamma$ 的定义同上, 则  
$(\mathrm i)$ 若 $M_1 \subseteq M_2$ 是 $E/F$ 的中间域, 则 $\mathrm{Gal}(E/M_1) \supseteq \mathrm{Gal}(E/M_2)$;  
若 $H_1\subseteq H_2$ 都是 $G$ 的子群, 则 $\mathrm{Inv}(H_1) \supseteq \mathrm{Inv}(H_2)$.  
$(\mathrm{ii})$ (作用 $2$ 次变大) 对于 $M \in \Omega$, 有 $M \subseteq \mathrm{Inv}(\mathrm{Gal}(E/M))$; 对于 $H \in \Gamma$ 有 $H \subseteq \mathrm{Gal}(E/\mathrm{Inv(H)})$.  
$(\mathrm {iii})$ (作用 $3$ 次等于作用 $1$ 次) 对于 $M \in \Omega$, $H \in \Gamma$, 有  
$\mathrm{Gal}(E/\mathrm{Inv}(\mathrm{Gal}(E/M))) = \mathrm{Gal}(E/M)$;$\mathrm{Inv}(\mathrm{Gal}(E/\mathrm{Inv}(H))) = \mathrm{Inv}(H)$.
{:.info}
## 阿廷引理和戴德金无关性引理
**引理** (**阿廷引理**) 设 $Q$ 是 $\mathrm{Aut}(K)$ 的有限子群. 则有 $$[K :\mathrm{Inv}(Q)] \le \mid Q \mid$$, 其中 $$\mathrm{Inv}(Q) = \{a \in K \mid \sigma(a) = a, \forall \sigma \in Q\}$$.
{:.info}

**证明** 记 $\mid Q \mid = n\ge 1$, 欲证 $[K: \mathrm{Inv}(Q)] \le n$, 只需证明 $K$ 上任意 $n+1$ 个元必然 $\mathrm{Inv}(Q)$-线性相关. 记 $$Q = \{f_1 = \mathrm{Id}_K,f_2,\cdots ,f_n\}$$, 对任意 $a_1,a_2,\cdots ,a_{n+1} \in K$, 考虑方程组

$$
\left\{
    \begin{array}{l}
        a_1x_1 + a_2x_2 + \cdots + a_{n+1}x_{n+1} = 0 \\
        f_1(a_1)x_1 + f_1(a_2)x_2 + \cdots + f_{1}(a_{n+1})x_{n+1}  = 0 \\
        \vdots \\
        f_n(a_1)x_1 + f_n(a_2)x_2 + \cdots + f_n(a_{n+1})x_{n+1} = 0
    \end{array}
\right.
$$

其必然有非零解, 取其中的一个非零解 $(u_1,u_2,\cdots ,u_{n+1})$ 使其中非零元素最少, 不妨设 $u_1,u_2,\cdots ,u_t \ne 0$, $u_{t+1},\cdots , u_{n+1} = 0$. 不妨设 $u_1 = 1$. 下面证明 $u_1,u_2,\cdots ,u_{n+1} \in \mathrm{Inv}(Q)$, 从而由第一个方程知 $a_1,a_2,\cdots ,a_{n+1}$ 是 $\mathrm{Inv}(Q)$-线性相关的.

否则, 若不然, 存在 $u_i$ 使得 $u_i \notin \mathrm{Inv}(Q)$. 不妨设 $u_2 \notin \mathrm{Inv}(Q)$, 存在 $ 2 \ge t \ge n$ 使 $f_t(u_2) \ne u_2$. 将上面的方程组两边用 $f_t$ 作用, 得

$$
    \sum_{i=1}^{n+1}f_tf_j(a_i)f_t(u_i) = 0, j = 1,2,\cdots ,n.
$$

由 $Q$ 是群, 知 $f_tf_1,f_tf_2,\cdots,f_tf_n$ 是 $f_1,f_2,\cdots ,f_n$ 的一个置换, 故 $(f_t(u_1),f_t(u_2),\cdots , f_t(u_{n+1}))$ 也是原方程组的一个解, 与 $(1,u_2,\cdots ,u_{n+1})$ 相减得

$$
    (0,f_t(u_2) - u_2,\cdots , f_t(u_{n+1}) - u_{n+1}).
$$

它也是原方程的一个解. 且 $f_t(u_2) - u_2 \ne 0$, 从而是它非零解. 它的非零元个数比 $t$ 小, 矛盾!
<p align="right">$\blacksquare$</p>

群 $H$ 到域 $K$ 非零元组成的乘法群 $$K^*$$ 的同态称为群 $H$ 的 $K$-**线性特征标**.

**引理** (**戴德金无关性引理**) 设 $\chi_1,\cdots , \chi_n$ 是群 $H$ 两两不同的 $K$-线性特征标, 则 $\chi_1,\cdots ,\chi_n$ 在 $K$ 上线性无关.
{:.info}

**证明** (反证) 若不然, 存在不全为零的元素 $c_1,c_2,\cdots ,c_n \in K$ 使得 $\sum_{1 \le i \le n}c_i\chi_i(g) = 0,\forall g \in H$. 取其中非零元个数最少的 $c_1,\cdots ,c_n$. 不妨设 $c_1,c_2, \cdots ,c_t \ne 0$ 而 $c_{t+1},\cdots ,c_n = 0$. ($t$ 必然大于 $1$). $\chi_1 \ne \chi_2$, 故存在 $h \in H$ 使 $\chi_1(h) \ne \chi_2(h)$. 将

$$
    \sum_{i=1}^{n}c_i\chi_1(h)x_i(g) = 0, \forall g \in H,
$$

与

$$
    \sum_{i=1}^{n}c_i\chi_i(hg) = \sum_{i=1}^{n}c_i\chi_i(h)\chi_i(g) = 0, \forall g \in H,
$$

相减得到 $\sum_{1\le i \le n}c_i(\chi_1(h) - \chi_i(h))\chi_i(g) = 0,\forall g \in H$. 其中 $c_2(\chi_1(h) - \chi_2(h)) \ne 0$, 而 $c_1(\chi_1(h) - \chi_1(h)) = 0$. 这与 $t$ 的最小性矛盾!
<p align="right">$\blacksquare$</p>

用戴德金无关性引理, 我们可以给出伽罗瓦群的上界.

**推论** 设 $E/F$ 是域的有限扩张, 则 $\mid \mathrm{Gal}(E/F)\mid \le [E:F]$.
{:.info }

**证明** 首先证明 $G = \mathrm{Gal}(E/F)$ 是有限群. $E/F$ 是有限扩张,从而是代数扩张. 记 $E = F(u_1,u_2,\cdots ,u_t)$, 则 $\sigma \in G$ 由 $\sigma(u_1),\cdots ,\sigma(u_t)$ 决定. 记 $u_i$ 在 $F$ 上的极小多项式为 $f_i(x)$, 则 $0 = \sigma(f_i(u_i)) = f_i(\sigma(u_i))$, 从而 $\sigma(u_i)$ 也是 $f_i(x)$ 的根, 只有有限种可能. 综上, $\mid G \mid < \infty$.

用反证法, 若结论不正确, 记 $$G = \{\sigma_1,\sigma_2,\cdots ,\sigma_m\}$$, $[E:F] = n < m$, 取 $E$ 的一组 $F$-基 $a_1,a_2,\cdots ,a_n$. 因 $n < m$, 所以矩阵

$$
\begin{pmatrix}
    \sigma_1(a_1) & \sigma_1(a_2) & \cdots & \sigma_2(a_n) \\
    \sigma_2(a_1) & \sigma_2(a_2) & \cdots & \sigma_2(a_n) \\
    \vdots & \vdots & \ddots & \vdots \\
    \sigma_m(a_1) & \sigma_m(a_2) & \cdots & \sigma_m(a_n)
\end{pmatrix}
$$

的行向量必然 $E$-线性相关, 即存在不全为零的元素 $c_1,c_2,\cdots,c_m \in E$ 使 $\sum_{1 \le i\le m}c_i\sigma_i(a_j) = 0,\forall 1 \le j \le n$. 任意 $x \in E$, 设 $x = k_1a_1 + \cdots + k_na_n$, $k_1,\cdots,k_n \in F$. 则

$$
    \sum_{i=1}^{m}c_i\sigma_i(x) = \sum_{i=1}^{m}\sum_{j=1}^{n}c_i\sigma_i(k_ja_j) = \sum_{j=1}^{n}k_j\sum_{i=1}^{m}c_i\sigma_i(a_j) = 0
$$

这说明 $\sigma_1,\sigma_2,\cdots ,\sigma_m$ $E$-线性相关. 但是 $\sigma_1,\cdots ,\sigma_m$ 是 $$E^*$$ 两两不同的 $E$-线性特征标, 这与戴德金无关性引理矛盾!
<p align="right">$\blacksquare$</p>

**定理** 设 $E/F$ 是域扩张, 则下述命题等价:  
($\rm i$) $E/F$ 是有限伽罗瓦扩张;  
($\rm ii$) $E$ 是 $F$ 上可分多项式在 $F$ 上的分裂域;  
($\rm iii$) $E/F$ 是有限扩张且 $\mid \mathrm{Gal}(E/F)\mid = [E:F]$;  
($\rm iv$) $G = \mathrm{Gal}(E/F)$ 是有限群且 $\mathrm{Inv}(\mathrm{Gal}(E/F)) = F$.
{:.info}

上述定理的四个等价条件可以认为分别是从“内部”, “外部”, “数量关系” 和 “内外部联系” 四个方面对有限伽罗瓦扩张的等价描述.

**证明** 只证 $(\rm iii) \Rightarrow (\rm iv)$, $(\rm iv) \Rightarrow (\rm i)$.

$(\rm iii) \Rightarrow (\rm iv)$: 由 $(\rm iii)$ 知 $ G =\mathrm{Gal}(E/F)$ 是有限群. 由定义有 $F \subseteq \mathrm{Inv}(\mathrm{Gal}(E/F))$. 我们有

$$
\begin{split}
    [E : \mathrm{Inv}(\mathrm{Gal}(E/F))] &\le [E : F] = |\mathrm{Gal}(E/F)| \\
    & = |\mathrm{Gal}(E/\mathrm{Inv}(\mathrm{Gal}(E/F)))| \\
    &\le [E: \mathrm{Inv}(\mathrm{Gal}(E/F))].
\end{split}    
$$

于是 $[E: \mathrm{Inv}(\mathrm{Gal}(E/F))] = [E : F]$. 因此 $F = \mathrm{Inv}(\mathrm{Gal}(E/F))$.

$(\rm iv) \Rightarrow (\rm i)$: 有

$$
    [E:F] = [E: \mathrm{Inv}(\mathrm{Gal}(E/F))] \le | \mathrm{Gal}(E/F) | < \infty,
$$

于是 $E/F$ 是有限扩张. 任意 $u \in E$, 记 $u$ 在 $F$ 上的极小多项式为 $f(x)$, 令

$$Gu = \{\sigma(u) \mid \sigma \in \mathrm{Gal}(E/F)\} = \{u_1 = u,u_2,\cdots ,u_t\}.$$

令 $g(x) = \prod_{1 \le i\le t}(x-u_i)$, 任意 $\sigma \in G$, $\sigma(g(x)) = \prod_{1 \le i \le t}(x - \sigma(u_i))$. 其中 $\sigma(u_1),\cdots ,\sigma(u_t)$ 是 $u_1,\cdots ,u_t$ 的一个置换, 故 $\sigma(g(x)) = g(x)$, $\forall \sigma \in G$. 这导致 $g(x) \in \mathrm{Inv}(\mathrm{Gal}(E/F))[x] = F[x]$. $u_1,\cdots ,u_t$ 也是 $f(x)$ 的根, 从而 $g(x) \mid f(x)$. 于是 $g(x) = f(x)$. 这说明 $u$ 在 $F$ 上的极小多项式可分且在 $E$ 上分裂, 从而 $E/F$ 是有限伽罗瓦扩张.
<p align="right">$\blacksquare$</p>

## 正规基
**引理** $E/F$ 是有限伽罗瓦扩张, $[E:F] = n$, $$\mathrm{Gal}(E/F) = \{\sigma_1,\sigma_2,\cdots ,\sigma_n\}$$, 则 $p_1,p_2,\cdots p_n$ 是 $E$ 的一组 $F$-基当且仅当行列式 $\det{(\sigma_j(p_i))_{1 \le j,i \le n}} \ne 0$.
{:.info}

**证明** $\Rightarrow$ 假若 $\det(\sigma_j(p_i)) = 0$, 则矩阵

$$
\begin{pmatrix}
\sigma_1(p_1) & \cdots & \sigma_1(p_n) \\
\vdots & \ddots & \vdots \\
\sigma_n(p_1) & \cdots & \sigma_n(p_n)
\end{pmatrix}
$$

的行向量 $E$-线性相关, 存在 $c_1, c_2,\cdots ,c_n \in E$ 使 $\sum_{1 \le i \le n} {c_i\sigma_i(p_j)} = 0$, $j = 1,2,\cdots, n$. 任意 $x \in E$, 记 $x = \sum_{1 \le j \le n}{k_jp_j}$, 其中 $k_1,\cdots,k_n \in F$, 则

$$
\sum_{i=1}^{n}{c_i\sigma_i(x)} = \sum_{i=1}^{n}\sum_{j=1}^{n}{c_i\sigma_i(k_jp_j)} = \sum_{j=1}^{n}k_j\sum_{i=1}^{n}c_i\sigma_i(p_j) = 0
$$

这说明 $\sigma_1,\cdots ,\sigma_n$ $E$-线性相关. 然而 $\sigma_1,\cdots ,\sigma_n$ 是 $$E^*$$ 的 $E$-线性特征标, 这与戴德金无关性引理矛盾.

$\Leftarrow$ 假若 $p_1,\cdots ,p_n$ 不是 $E$ 的一组 $F$-基, 则它们 $F$-线性相关. 存在 $c_1,\cdots ,c_n \in F$ 使得 $\sum_{1 \le i \le n}{c_ip_i} = 0$. 两边用 $\sigma_j$ 作用得 $\sum_{1 \le i \le n}{c_i\sigma_j(p_i)} = 0$ ($j = 1,2,\cdots, n$). 这说明矩阵 $(\sigma_j(p_i))_{j,i}$ 的列向量线性相关, 这导致其行列式为零.

**定理** (**正规基**) 若 $E/F$ 是有限伽罗瓦扩张, 则存在 $a \in E$ 使 $$\{\sigma{(a)} \mid \sigma \in \mathrm{Gal}(E/F)\}$$ 是 $E$ 的一组 $F$-基.
{:.info}

**证明** 先证明 $F$ 是无限域的情况. $E/F$ 是有限伽罗瓦扩张, 从而是单扩张. 记 $E = F(u)$, $u$ 在 $F$ 上的极小多项式为 $f(x)$, 有 $f(x)$ 无重根. 记 $[E:F] = n$, $$G = \mathrm{Gal}(E/F) = \{\sigma_1,\cdots ,\sigma_n\}$$. 可知 $f(x)$  的根恰是 $$Gu = \{\sigma(u) \mid \sigma \in G\}$$, 且

$$
    f(x) = \prod_{t \in Gu}(x-t).
$$

记 $\sigma_{i_j} = \sigma_i\sigma_j$,$1 \le i,j \le n$. 并令 $u_{i_j} = \sigma_{i_j}(u)$. 则 $u_{1_j}, u_{2_j} \cdots ,u_{n_j}$ 和 $u_{i_1}, u_{i_2},\cdots ,u_{i_n}$ 均是 $Gu$ 的一个置换.

令 $g(x) = \frac{f(x)}{(x-u)f'(u)} \in E[x]$, $g_{i_j}(x) = \frac{f(x)}{(x-u_{i_j})f'(u_{i_j})} \in E[x]$. 则当 $\alpha \in F$ 时, $g_{i_j}(\alpha) = \sigma_{i_j}(g(\alpha))$. 且 $g_{i_j}(u_{i_j}) = 1$, $g_{i_j}(u_{k_t}) = 0$, $\forall u_{i_j} \ne u_{k_t}$.

考虑行列式

$$
d(x) =
\left|
\begin{matrix}
g_{1_1}(x) & g_{1_2}(x) & \cdots & g_{1_n}(x) \\
g_{2_1}(x) & g_{2_2}(x) & \cdots & g_{2_n}(x) \\
\vdots & \vdots & \ddots & \vdots \\
g_{n_1}(x) & g_{n_2}(x) & \cdots & g_{n_n}(x)
\end{matrix}
\right|
$$

有 $d(x) \in E[x]$. 且 $1 \le i,j \le n$ 时, $d(u_{i_j})$ 的每行, 每列有且仅有一个元素为 $1$, 其余元素为 $0$. 这说明 $d(u_{i_j}) = \pm 1 \ne 0$, 从而 $d(x)$ 不是零多项式. $F$ 无限, 故存在 $a \in F$ 使 $d(a) \ne 0$. 带入行列式得到

$$
d(a) =
\left|
\begin{matrix}
    \sigma_{1_1}(g(a)) & \cdots & \sigma_{1_n}(g(a)) \\
    \vdots & \ddots & \vdots \\
    \sigma_{n_1}(g(a)) & \cdots & \sigma_{n_n}(g(a))
\end{matrix}
\right|
\ne 0;
$$

由引理知 $\sigma_1(g(a)),\sigma_2(g(a)),\cdots ,\sigma_n(g(a))$ 是 $E$ 在 $F$ 上的一组基.
<!--
接下来考虑 $F$ 为有限域的情况. 设 $\mathrm{char} F = p$. 记 $F = F_q$ 是 $q$ 元域. $E/F$ 是 $n$ 次扩张, 则 $E$ 是 $q^n$ 元域. 由有限域的性质, $$E^*$$ 对乘法构成循环群. 记其一生成元为 $\alpha$. $\mathrm{Gal}(E/F)$ 是循环群, 其生成元为 $\sigma: a \mapsto a^{q}$. 我们有

$$
\begin{pmatrix}
    \alpha & \alpha^q & \cdots & \alpha^{q^{n-2}} & \alpha^{q^{n-1}} \\
    \alpha^q & \alpha^{q^2} & \cdots & \alpha^{q^{n-1}} & \alpha \\
    \vdots & \vdots & \ddots & \vdots & \vdots \\
    \alpha^{q^{n-1}} & \alpha & \cdots & \alpha^{q^{n-3}} & \alpha^{q^{n-2}}
\end{pmatrix}
$$

-->

