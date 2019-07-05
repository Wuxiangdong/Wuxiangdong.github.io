---
title: 正规扩张
tags: Math Algebra 伽罗瓦理论
---

# 正规扩张
设代数扩张 $E/F$. 如果 $E$ 中任一元 $u$ 在 $F$ 上的极小多项式在 $E[x]$ 中分解为一次因子的乘积, 则称 $E/F$ 为 **正规扩张**.即在 $E$ 中有根的 $F$ 上的不可约多项式的根均在 $E$ 中.
{:.success}

如果 $E/F$ 既是可分扩张也是正规扩张, 则称 $E/F$ 是 **伽罗瓦扩张**.  
如果 $E/F$ 即使有限扩张又是伽罗瓦扩张, 则称 $E/F$ 是 **有限伽罗瓦扩张**.
{:.success}
<!--more-->

## 有限正规扩张的刻画
**引理** 设域扩张 $K/E$, $E/F$, $E$ 是 $F$ 上某一多项式在 $F$ 上的分裂域, 则任意 $F$-嵌入 $\sigma: E \rightarrow K$ 都有 $\sigma(E) = E$.
{:.info}

**证明** 设 $E$ 是首一不可约多项式 $f(x) \in F[x]$ 在 $F$ 上的分裂域, $f(x)$ 的根为 $$\Sigma = \{ u_1,u_2,\cdots ,u_n \}$$. 则 $E = F(\Sigma)$. 由于 $f(x) \in F[x]$, 有

$$f(x) = \sigma(f(x)) = \prod_{i=1}^{n}{(x-\sigma(u_i))}.$$

$\sigma$ 是单射, 说明 $\sigma$ 可以看成 $\Sigma$ 的置换. 于是

$$\sigma(E) = \sigma(F(\Sigma)) = F(\sigma(\Sigma)) = F(\Sigma) = E.$$

( $\sigma(F(\Sigma)) = F(\sigma(\Sigma))$ 的理由是: $\sigma(F(\Sigma))$ 包含 $\sigma(\Sigma)$ 和 $F$, 故 $F(\sigma{(\Sigma)}) \subseteq \sigma(F(\Sigma))$. 同理 $\sigma^{-1}(F(\sigma(\Sigma))) \supseteq F(\Sigma)$, 从而 $F(\sigma(\Sigma)) \supseteq \sigma(F(\Sigma))$. 故 $F(\sigma(\Sigma)) = \sigma(F(\Sigma))$.)
<p align="right">$\blacksquare$</p>

**定理** 设域扩张 $E/F$, 则 $E/F$ 是有限正规扩张当且仅当 $E$ 是 $F$ 上某一多项式在 $F$ 上的分裂域.
{:.info}

**证明** 设 $E/F$ 是有限正规扩张, 则 $[E:F]$ 有限, 存在 $F$ 上的代数元 $u_1,u_2,\cdots,u_n$ 使 $E = F(u_1,u_2,\cdots,u_n)$. 记 $u_i$ 在 $F$ 上的极小多项式为 $f_i(x)$, $i = 1,2,\cdots,n$. 记 $f(x) = f_1(x)f_2(x)\cdots f_n(x)$. 设 $f(x)$ 在 $F$ 上的分裂域为 $F'$. 一方面, $u_1,u_2,\cdots ,u_n$ 只是 $f(x)$ 的一部分根, 从而 $E \subseteq F'$. 另一方面, 由 $E/F$ 是正规扩张, $f_i(x)$ 的所有根均在 $E$ 上, 从而 $E \supseteq F'$. 这说明 $E = F'$, 是 $F$ 上某一多项式在 $F$ 上的分裂域.  

反之, 设 $E$ 是 $F$ 上某一多项式 $f(x)$ 在 $F$ 上的分裂域. 设 $g(x) \in F[x]$ 是不可约多项式且 $g(x)$ 在 $E$ 中有根 $\alpha$. 下证 $g(x)$ 的任意根都在 $E$ 中. 记 $E$ 的一个代数闭包 $\Omega$. $\beta \in \Omega$ 是 $g(x)$ 的任一个根. $\alpha,\beta$ 在 $F$ 上的极小多项式相同, 故存在$F$-同构 $\sigma: F(\alpha) \rightarrow F(\beta)$, 使 $\sigma(\alpha) = \beta$. $E$ 也可以看成 $f(x)$ 在 $F(\alpha)$ 上的分裂域, 故 $\sigma$ 可以延拓为 $F$-嵌入 $\sigma: E \rightarrow \Omega$. 由引理知 $\sigma(E) = E$, 从而 $\beta = \sigma(\alpha) \in E$. 也即 $g(x)$ 的任意根都在 $E$ 中.
<p align="right"> $\blacksquare$ </p>

**推论** 设域扩张 $E/F$, 则 $E/F$ 是有限伽罗瓦扩张当且仅当 $E$ 是 $F$ 上某一可分多项式在 $F$ 上的分裂域.
{:.info}

**证明** 设 $E/F$ 是有限伽罗瓦扩张, 则 $E$ 是 $F$ 上某一多项式 $f(x)$ 在 $F$ 上的分裂域. 由 $E/F$ 是可分扩张知 $f(x)$ 是可分多项式.

反之, 若 $E$ 是 $F$ 上某一可分多项式在 $F$ 上的分裂域, 则 $E/F$ 是可分扩张和有限正规扩张, 从而是有限伽罗瓦扩张.
<p align="right">$\blacksquare$</p>
