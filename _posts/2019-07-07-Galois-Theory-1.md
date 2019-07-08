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

其必然有非零解, 取其中的一个非零解 $(u_1,u_2,\cdots ,u_n)$ 使其中非零元素最少, 不妨设 $u_1,u_2,\cdots ,u_t \ne 0$, $u_{t+1},\cdots , u_{n} = 0$. 不妨设 $u_1 = 1$. 下面证明 $u_1,u_2,\cdots ,u_n \in \mathrm{Inv}(Q)$, 从而由第一个方程知 $a_1,a_2,\cdots ,a_n$ 是 $\mathrm{Inv}(Q)$-线性相关的.

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

**引理** (**戴德金无关性原理 **) 设 $\chi_1,\cdots , \chi_n$ 是群 $H$ 的 $K$-线性特征标, 则 $\chi_1,\cdots ,\chi_n$ 在 $K$ 上线性无关.
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
    \sum_{i=1}^{m}c_i\sigma_i(x) = \sum_{i=1}^{m}\sum_{j=1}^{n}c_i\sigma_i(k_ja_j) = \sum_{j=1}^{n}\sigma(k_j)\sum_{i=1}^{m}c_i\sigma_i(a_j) = 0
$$

这说明 $\sigma_1,\sigma_2,\cdots ,\sigma_m$ $E$-线性相关. 但是 $\sigma_1,\cdots ,\sigma_m$ 是 $E*$ 两两不同的 $E$-线性特征标, 这与戴德金无关性引理矛盾!
<p align="right">$\blacksquare$</p>
