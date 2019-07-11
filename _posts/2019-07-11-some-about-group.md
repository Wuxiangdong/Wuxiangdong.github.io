---
title: 关于群的一些东西
tags: Math Algebra 群论
---

<!-- vim-markdown-toc GFM -->

* [$\bf 1$](#bf-1)

<!-- vim-markdown-toc -->

## $\bf 1$
有限 $p$-群是指阶数为 $p$ 的幂的有限群, 其中 $p$ 是一个素数.

$p$-群在集合上的置换作用可产生一个轨道分解公式, 有时在模 $p$ 的意义下这些公式可以给出一些性质.

**定理** 有限 $p$-群必有非平凡的中心.
{:.info}
<!--more-->
**证明** 设 $G$ 是有限 $p$-群, 将 $G$ 共轭作用到 $G$ 本身:

$$
    \rho: G \rightarrow S(G), \rho(a)\circ b = a{b}a^{-1}.
$$

将 $G$ 拆分为轨道的无交并 $G = \bigcup_{i=1}^{t}{\Delta_{i}}$, $\mid G \mid = \sum_{i=1}^{t}{ \mid  \Delta_i  \mid}$. 记 $a_i$ 是 $\Delta_i$ 的代表元, $G_{a_i}$ 是 $a_i$ 的稳定子群, 则 $\mid \Delta_i \mid = \frac{ \mid G \mid }{ \mid G_{a_i} \mid}$. 这说明 $\mid \Delta_i \mid$ 要么为 $1$, 要么为 $p$ 的幂. $a \in G$ 单独在一个轨道等价于 $a \in Z(G)$. 从而

$$
    |G| = |Z(G)| + \sum_{1\le i \le n, |\Delta_i| \ne 1} |\Delta_i| \equiv |Z(G)|\pmod{p}
$$

这说明 $\mid Z(G) \mid \equiv 0 \pmod{p}$, 从而 $\mid Z(G) \mid \ne 1$. $Z(G)$ 非空, 故 $G$ 有非平凡的中心.
<p align="right">$\blacksquare$</p>

**定理** (**Sylow 定理, 之一**) 设 $G$ 为有限群, 则 $G$ 的 Sylow-$p$ 子群彼此共轭.
{:.info}

**证明** 记 $p^r \mid\mid\,\,\mid G \mid$. 令 $\Sigma$ 是 $G$ 的所有 Sylow-$p$ 子群构成的集合, 将 $G$ 共轭作用于其上. 令 $\Delta$ 是一个 $G$-轨道. 取 $G$ 的一个 Sylow-$p$ 子群 $P$. 可 $P$ 作用于 $\Delta$ 上, $\Delta$ 被拆分为 $P$-轨道. 且每个 $P$-轨道的长度是 $\mid P \mid = p^r$ 的因子. 若 $P' \in \Delta$ 单独在一个 $P$-轨道, 则 $PP' = P'P$, 从而 $PP'$ 是 $G$ 的子群. $\mid PP'\mid = \mid P \mid\mid P' \mid / \mid P \cap P'\mid$, 仍然是 $p$ 的幂. 又 $P \leqslant PP' \leqslant G$, 只能是 $PP' = P = P'$. 上述说明长度为 $1$ 的 $P$-轨道只能是 $$\{P\}$$ 本身. 

现在假设 $\Delta \ne \Sigma$, 存在 $P \in \Sigma - \Delta$. 将 $P$ 共轭作用于 $\Delta$, 则 $\mid \Delta\mid \equiv 0 \pmod{p}$ (每个 $P$-轨道都是 $p$ 的幂且不为 $1$). 再取 $Q \in \Delta$, 将 $Q$ 共轭作用于 $\Delta$ 上, 可以得到 $\mid\Delta\mid \equiv 1 \pmod{p}$. 这两者矛盾! 故 $\Delta= \Sigma$, 从而 $G$ 在 $\Sigma$ 上的作用是传递的, $G$ 上的 Sylow-$p$ 子群彼此共轭.
<p align="right">$\blacksquare$</p>

**例** 令 $P_1,P_2,\cdots ,P_N$ 是有限群 $G$ 的全部 Sylow-$p$ 子群. 如果对任意 $i \ne j$, 都有 $\mid P_i : P_i \cap P_j\mid \ge p^r$, 则 $N \equiv 1\pmod{p^r}$.
{:.warning}

**证明** 记 $$\Sigma = \{P_1,P_2,\cdots , P_N\}$$, 将 $P_1$ 共轭作用在 $\Sigma$ 上. 每个 $P_j \in \Sigma$ 的稳定子群为 $P_1 \cap N_G(P_j)$. $N_G(P_j)$ 的所有 $p$的幂阶元均在 $P_j$ 中, 从而 $P_1 \cap (N_G(P_j) - P_j) = \varnothing$. 于是当 $j \ne 1$ 时

$$
    P_1\cap N_G(P_j) = P_1\cap (P_j \cup (N_G(P_j)-P_j)) = P_1\cap P_j.
$$

这说明 $P_j$ 所在轨道的长度为 $\mid P_1 : P_1 \cap P_j \mid \ge p^r$, 它一定是 $p$ 的幂, 从而是 $p^r$ 的倍数. 又 $P_1$ 单独在一个轨道, 故 $N \equiv 1\pmod{p^r}$.
<p align="right">$\blacksquare$</p>
