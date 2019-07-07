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
