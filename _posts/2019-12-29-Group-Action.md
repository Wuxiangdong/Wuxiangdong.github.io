---
title: 群在集合上的作用
tags: Math Algebra
---


<!-- vim-markdown-toc GFM -->

* [Preliminaries](#preliminaries)
* [Burnside's Lemma](#burnsides-lemma)
* [n-Transitivity](#n-transitivity)
* [Primitive Actions](#primitive-actions)
* [Applications](#applications)

<!-- vim-markdown-toc -->

## Preliminaries
设 $G$ 是一个群. $G$ (左)作用在集合 $X$ 上是指一个映射

$$
    G \times X \to X, (g,x) \mapsto gx,
$$

满足如下性质:

$(1)\, g(g'x) = (gg')x, \forall x \in X, g,g' \in G$.  
$(2)\, 1x = x,\forall x \in X$.

等价的, $G$ 在 $X$ 上的作用也可由群同态 $G \to \mathcal{S}_X$ 给出, 其中 $\mathcal{S}_X$ 指 $X$ 的对称群.

**Definition.** 若集合 $X$ 被 $G$ 作用, 称 $X$ 为 $G$-Set.  
设 $X,Y$ 是两个 $G$-Set, 映射 $f: X \to Y$ 被称为 $G$-Map, 如果 $f(gx) = gf(x)$ 对任意 $x \in X, g \in G$ 成立.  
设 $X,Y$ 是 $G$-Set, 若存在一一对应的 $G$-Map $X \to Y$, 称 $G$ 在 $X,Y$ 上的作用同构的. 下文简称 $X,Y$ 是 $G$-同构的.
{:.success}

**Definition.** 设 $X$ 是一个 $G$-Set, $x \in X$, 用 $G_x$ 表示 $x$ 的稳定子群(Stabilizer)
{:.success}

**Definition.** $G$ 在 $X$ 上的作用被称为$\ldots$, 若$\ldots$.  
$(1)$ 忠实的(faithful), 若 $$G \to \mathcal{S}_X$$ 是单射. 这等价于 $$\bigcap_{x \in X}G_x = 1$$.  
$(2)$ 自由的(free), 若任意 $x \in X$, 有 $G_x = 1$.  
若 $G$ 自由且传递地作用于 $X$, 则 $X$ 称为 $G$-torsor.
{:.success}

其他需要的概念和性质, 例如 $G$-轨道(Orbit), 轨道-稳定子群定理, 这里省去. $X$ 的所有轨道组成的集合记为 $X/G$.

设 $G$ 传递地作用于 $X$, 取 $x \in X$, 有 $G$-同构 $G/G_x \to X, gG_x \mapsto gx$. $G$ 传递地作用于一个集合 $X$, 等价于给定一个子群 $H \subset G$, $G$ 作用于(左)陪集 $G/H$.

设 $X$ 是 $G$-torsor, 我们有 $G$ 在 $X$ 上的作用同构于 $G$ 的(左)正则表示.

设 $G$ 自由地作用于 $X$ 上, 任取 $X$ 的一个 $G$-轨道 $\mathcal{O}$, $\mathcal{O}$ 是 $G$-torsor, 而 $X$ 是这些 $G$-torsor 的无交并.

**Example.** 设 $n \geqslant 0$, 集合 $X$, $\mid X\mid \geqslant n$. $$\mathcal{S}_X$$ 自然地作用于 $X^n$ 上. 对 $x = (x_i)_{i=1}^n \in X^n$, 按照 $i \equiv j \Longleftrightarrow x_i = x_j$ 定义 $$\{1,2,\cdots ,n\}$$ 的等价关系 $R_x$. 设 $x,y \in X^n$, 则 $R_x = R_y$ 当且仅当 $x,y$ 在相同的 $\mathcal{S}_X$-轨道中.
{:.warning}

清晰地看到, $$\mathcal{S}_X$$ 作用在 $$X^n$$ 产生的轨道和 $$\{1,2,\cdots ,n\}$$ 上的等价关系是一一对应的. 从而 $$X^n/\mathcal{S}_X$$ 的大小恰为 $B(n)$, 即第 $n$ 个 Bell 数. Bell 数满足熟知的公式 $B(n+1) = \sum_{k=0}^n\binom{n}{k}B(k)$. 当 $X$ 有限时, 由 Burnside 引理, 这个公式等价于

$$
    \sum_{g\in \mathcal{S}_X}\chi_{X}(g)^n = \sum_{g\in \mathcal{S}_X}(\chi_X(g)+1)^{n-1}, \,\,\,\,\,\,\forall n \leqslant |X|. \tag{1}\label{r1}
$$

($g \in \mathcal{S}_X$ 作用在 $X^m$ 上不动点个数为 $\chi_X(g)^m$)

下面给出 $\eqref{r1}$ 式的直接证明. (大飞机太强啦~!)

**证明** 记 $$\mid X\mid = m, G = \mathcal{S}_X$$. 我们只需证明任意 $n \leqslant m$ 有 $\sum_{g\in G} \binom{\chi_X(g)}{n} = \sum_{g\in G} \frac{1}{\chi_X(g) + 1}\binom{\chi_X(g) + 1}{n}$ (将 $$\binom{-}{n}$$ 看成 $$n$$ 次多项式), 只需证明 $\sum_{g\in G}\binom{\chi_X(g)}{n} = \frac{1}{n}\sum_{g\in G}\binom{\chi_X(g)}{n-1}$, 再考虑 $\sum_{g\in G}\binom{\chi_X(g)}{0} = m!$, 只需证明

$$\sum_{g\in \mathcal{S}_X}\binom{\chi_X(g)}{n} = \frac{|X|!}{n!}. \tag{2}\label{r2}$$

设 $k \leqslant m$, 则 $$\mathcal{S}_X$$ 中不动点个数为 $k$ 的置换的个数为 $\binom{m}{k}$ 乘 $m-k$ 全错排数, 为

$$
    \binom{m}{k}(m-k)!\sum_{i=0}^{m-k}(-1)^i\frac{1}{i!} = \frac{m!}{k!}\sum_{i=0}^{m-k}{(-1)^i\frac{1}{i!}}.
$$

从而, $\eqref{r2}$ 左边为

$$\begin{aligned}
    \sum_{k=0}^m\sum_{i=0}^{m-k}\binom{k}{n}\frac{m!}{k!i!}(-1)^i &= \sum_{k=n}^{m}\sum_{i=k}^{m}\binom{k}{n}\frac{m!}{k!(i-k)!}(-1)^{i-k} \\
    &=\frac{m!}{n!}\sum_{i=n}^{m}\sum_{k=n}^{i}\frac{(-1)^{i-k}}{(k-n)!(i-k)!} \\
    &=\frac{m!}{n!}\sum_{i=0}^{m-n}\sum_{k=0}^{i}\frac{(-1)^{i-k}}{k!(i-k)!} \\
    &= \frac{m!}{n!}\sum_{i=0}^{m-n}\frac{1}{i!}\sum_{k=0}^{i}\binom{i}{k}(-1)^{i-k}
\end{aligned}$$

当 $i \geqslant 1$ 时, $\sum_{k=0}^{i} \binom{i}{k}(-1)^{i-k} = 0$, $i = 0$ 时它为 $1$, 由此左边 $= \frac{m!}{n!} =$ 右边.

## Burnside's Lemma
**Proposition.** 设 $G$ 为有限群, 令 $X$ 是一个有限 $G$-Set. 对每一个 $g \in F$, 令 $X^g \subset X$ 为 $g$ 的不动点集, 并令 $\chi_X(g) = \mid X^g \mid$. 有:  
$$
    \mid X/G \mid = \frac{1}{\mid G\mid}\sum_{g\in G}\chi_X(g).
$$
{:.info}

**证明的概要** 令 $$S = \{(g,x) \in G \times X \mid gx = x\}$$. 用两种方法计算 $\mid S\mid$.

## n-Transitivity
令 $n$ 为大于 $1$ 的整数, 群 $G$ 作用于一集合 $X$, 且 $\mid X\mid \geqslant n$. $G$ 按照自然的方式作用于 $X^n$, 即 $g(x_1,x_2,\cdots,x_n) = (gx_1,gx_2,\cdots ,gx_n)$. 令 $$X_{\mathrm{dist}}^n = \{(x_i)_{1 \leqslant i \leqslant n} \in X^n \mid x_{i} \ne x_{j}, \forall i \ne j\}$$. 称 $G$ 在 $X$ 上的作用是 $n$ 重传递的($n$-transitive), 如果 $G$ 在 $X_{\mathrm{dist}}^n$ 上的作用是传递的. 即对两个两两不同的 $n$ 元组 $(x_1,x_2,\cdots,x_n)$, $(y_1,y_2,\cdots,y_n) \in X^n$, 存在 $g \in G$, 使 $gx_i = y_i, 1 \le i \le n$.

**Proposition.** 设 $X$ 是 $G$-Set, 整数 $$|X| \geqslant n \geqslant 2$$. 则以下条件等价:  
$(\rm{i})$ $G$ 在 $X$ 上的作用 $n$ 重传递.  
$(\rm{ii})$ $G$ 在 $X$ 上的作用传递, 并且如果 $H \subset G$ 是 $X$ 一点 $x$ 的稳定子群, 则 $H$ 在 $X-\{x\}$ 上的作用是 $n-1$ 重传递的.  
$(\rm{iii})$ $G$ 作用在 $X^n$ 上的轨道和 $$\mathcal{S}_X$$ 作用在 $X^n$ 上的相同.  
$(\rm{iv})$ $G$ 作用在 $X^n$ 上的轨道数是 $B(n)$, 其中 $B(n)$ 是第 $n$ 个 Bell 数.  
当 $X$, $G$ 皆有限时,还有  
$(\rm{v})$ $\frac{1}{\mid G\mid}\sum_{g\in G}\chi_X(g)^n \leqslant B(n)$, 其中 $\chi_X(g) = \mid X^g\mid$.  
$(\rm{vi})$ $\frac{1}{\mid G\mid}\sum_{g\in G}\chi_X(g)^n = B(n)$.
{:.info}
## Primitive Actions

## Applications
