---
title:  伽罗瓦理论基本定理
tags: Math Algebra 伽罗瓦理论
---

# 伽罗瓦理论基本定理

伽罗瓦理论基本定理是说: 对于有限伽罗瓦扩张, 伽罗瓦对应是反序的一一对应, 且保持共轭性.
<!--more-->
设 $E/F$ 是有限伽罗瓦扩张, $G  =\mathrm{Gal}(E/F)$. 令 

$$\Omega = \{E/F 的中间域\}, \Gamma = \{G 的子群\}.
$$

有伽罗瓦对应:

$$
\mathrm{Gal}(E/-): \Omega \rightarrow \Gamma, \mathrm{Gal}(E/-)M = \mathrm{Gal}(E/M),\\
\mathrm{Inv}: \Gamma \rightarrow \Omega, \mathrm{Inv}(H) = \{a \in E \mid \sigma(a) = a,\forall \sigma \in H\}.
$$

由定义, 对任意中间域 $M \in \Omega$, $E/M$ 也是有限伽罗瓦扩张. 于是

$$
[E:M] = \mid \mathrm{Gal}(E/M)\mid, [M:F] = [E :  F]/[E:M] = \frac{\mid G\mid}{\mid\mathrm{Gal}(E/M)\mid}.
$$

对 $M,M' \in \Omega$, 如果存在 $\sigma \in G$ 使得 $M' = \sigma(M)$, 则称 $M,M'$ 是 **共轭** 的. 由 $G$ 是群, 知共轭是 $\Omega$ 上的等价关系.

**定理** (**伽罗瓦理论基本定理**) 设 $E/F$ 是有限伽罗瓦扩张, $\mathrm{Gal}(E/-)$,$\mathrm{Inv}$,$\Omega$ 和 $\Gamma$ 的定义同上, 则  
$\mathrm{(i)}$: $\mathrm{Gal}(E/-)$ 和 $\mathrm{Inv}$ 是互逆反序的映射, 既:  
$\mathrm{Inv}(\mathrm{Gal}(E/M)) = M$, $\mathrm{Gal}(E/\mathrm{Inv}(H)) = H$, $\forall M\in \Omega,H \in \Gamma$.  
$\mathrm{(ii)}$: $G$ 的子群 $H$ 和 $H'$ 共轭, 当且仅当 $\mathrm{Inv}(H)$ 和 $\mathrm{Inv}(H')$ 是共轭的. $G$ 的子群 $H$ 是正规子群当且仅当 $\mathrm{Inv}(H)/F$ 是正规扩张. 在这种情况下, 有 $\mathrm{Gal}(\mathrm{Inv}(H)/F) \cong G/H$.
{:.info}

利用 $\mathrm{(i)}$ 将 $\mathrm{(ii)}$ 的话倒过来说, 就得到:

$\mathrm{(ii')}$: $E/F$ 的中间域 $M$ 和 $M'$ 共轭当且仅当 $\mathrm{Gal}(E/M)$ 和 $\mathrm{Gal}(E/M')$ 是共轭的.  
设 $M \in \Omega$. 则 $M/F$ 是正规扩张当且仅当 $\mathrm{Gal}(E/M)$ 是 $G$ 的正规子群. 在这种情况下, 有 $\mathrm{Gal}(M/F) \cong \mathrm{Gal}(E/F) /\mathrm{Gal}(E/M)$.
{:.info}

**证明** $\mathrm{(i)}$ $\forall M \in \Omega$, $E/M$ 是有限伽罗瓦扩张, 从而 $\mathrm{Inv}(\mathrm{Gal}(E/M)) = M$. 任意 $H \in \Gamma$,  由阿廷定理, $E/\mathrm{Inv}(H)$ 是有限伽罗瓦扩张, 且 $\mathrm{Gal}(E/\mathrm{Inv}(H)) = H$.

由 $\mathrm{(i)}$, $\sigma \in G$ 使 $H' = \sigma H\sigma^{-1}$  当且仅当 $\mathrm{Inv}(\sigma H\sigma^{-1}) = \mathrm{Inv}(H')$, 其中

$$
\begin{split}
\mathrm{Inv}(\sigma H\sigma^{-1}) &= \{a \in E\mid \sigma\pi\sigma^{-1}(a) = a ,\forall \pi \in H\} \\
&= \{a \in E \mid \pi\sigma^{-1}(a) = \sigma^{-1}(a),\forall \pi \in H\} \\
&= \{a \in E \mid \sigma^{-1}(a) \in \mathrm{Inv}(H)\} = \sigma(\mathrm{Inv}(H)).
\end{split}
$$

这说明 $\mathrm{Inv}(\sigma H\sigma^{-1}) = \mathrm{Inv}(H')$ 当且仅当 $\sigma(\mathrm{Inv}(H)) = \mathrm{Inv}(H')$. 故 $H$ 和 $H'$ 共轭当且仅当 $\mathrm{Inv}(H)$ 和 $\mathrm{Inv}(H')$ 共轭.

这也说明 $H$ 是 $G$ 的正规子群当且仅当 $\mathrm{Inv(H)}/F$ 是正规扩张 (见[正规扩张](https://wuxiangdong.github.io/2019/07/06/normal-extension.html#%E6%9C%89%E9%99%90%E6%AD%A3%E8%A7%84%E6%89%A9%E5%BC%A0%E7%9A%84%E5%88%BB%E7%94%BB)的例). 这个情况下有 $\sigma(\mathrm{Inv}(H)) = \mathrm{Inv(H)},\forall \sigma \in G$, 于是可以记

$$
\pi: G \rightarrow \mathrm{Gal}(\mathrm{Inv}(H)/F), \sigma \mapsto \sigma\mid_{\mathrm{Inv}(H)}.
$$

则 $\pi$ 是同态, 且

$$\ker \pi = \{\sigma\in G \mid \sigma(a) = a,\forall a \in \mathrm{Inv}(H)\} = \mathrm{Gal}(E/\mathrm{Inv}(H)) = H.$$

故 $\pi$ 诱导出单同态 $G/H \rightarrow \mathrm{Gal}(\mathrm{Inv}(H)/F)$.  又

$$
|G/H| = |G|/|H| = [E:F]/[E:\mathrm{Inv(H)}] = [\mathrm{Inv}(H):F] = |\mathrm{Gal(\mathrm{Inv}(H)/F)}|.
$$ 

故上述单同态是同构, 从而 $\mathrm{Gal(\mathrm{Inv(H)}/F)} \cong G/H$.
<p align="right">$\blacksquare$</p>
