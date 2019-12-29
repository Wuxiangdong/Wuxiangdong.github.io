---
title: 群在集合上的作用
tags: Math Algebra
---


<!-- vim-markdown-toc GFM -->

* [Preliminaries](#preliminaries)
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

**Definition** 若集合 $X$ 被 $G$ 作用, 称 $X$ 为 $G$-Set. 若 $X,Y$ 是两个 $G$-Set, 映射 $f: X \to Y$ 被称为 $G$-Map, 如果 $f(gx) = gf(x)$ 对任意 $x \in X, g \in G$ 成立.
{:.success}

**Definition** 设 $X$ 是一个 $G$-Set, $x \in X$, 用 $G_x$ 表示 $x$ 的稳定子群(Stabilizer)
{:.success}

**Definition** $G$ 在 $X$ 上的作用被称为$\ldots$, 若$\ldots$.  
$(1)$ 忠实的(faithful), 若 $G \to \mathcal{S}_X$ 是单射. 这等价于 $\bigcap_{x \in X}G_x = 1$.  
$(2)$ 自由的(free), 若任意 $x \in X$, 有 $G_x = 1$.  
若 $G$ 自由且传递地作用于 $X$, 则 $X$ 称为 $G$-torsor.
{:.success}

设 $G$ 传递地作用于 $X$, 取 $x \in X$, 有 $G$-Set 的同构 $G/G_x \to X, gG_x \mapsto gx$. $G$ 传递地作用于一个集合 $X$, 等价于给定一个子群 $H \subset G$.
## n-Transitivity

## Primitive Actions

## Applications
