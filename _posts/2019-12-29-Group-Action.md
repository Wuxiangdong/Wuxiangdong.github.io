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

**Definition** 若集合 $X$ 被 $G$ 作用, 称 $X$ 为 $G$-Set.  
设 $X,Y$ 是两个 $G$-Set, 映射 $f: X \to Y$ 被称为 $G$-Map, 如果 $f(gx) = gf(x)$ 对任意 $x \in X, g \in G$ 成立.  
设 $X,Y$ 是 $G$-Set, 若存在一一对应的 $G$-Map $X \to Y$, 称 $G$ 在 $X,Y$ 上的作用同构的. 下文简称 $X,Y$ 是 $G$-同构的.
{:.success}

**Definition** 设 $X$ 是一个 $G$-Set, $x \in X$, 用 $G_x$ 表示 $x$ 的稳定子群(Stabilizer)
{:.success}

**Definition** $G$ 在 $X$ 上的作用被称为$\ldots$, 若$\ldots$.  
$(1)$ 忠实的(faithful), 若 $$G \to \mathcal{S}_X$$ 是单射. 这等价于 $$\bigcap_{x \in X}G_x = 1$$.  
$(2)$ 自由的(free), 若任意 $x \in X$, 有 $G_x = 1$.  
若 $G$ 自由且传递地作用于 $X$, 则 $X$ 称为 $G$-torsor.
{:.success}

其他需要的概念和性质, 例如 $G$-轨道(Orbit), 轨道-稳定子群定理, 这里省去.

设 $G$ 传递地作用于 $X$, 取 $x \in X$, 有 $G$-同构 $G/G_x \to X, gG_x \mapsto gx$. $G$ 传递地作用于一个集合 $X$, 等价于给定一个子群 $H \subset G$, $G$ 作用于(左)陪集 $G/H$.

设 $X$ 是 $G$-torsor, 我们有 $G$ 在 $X$ 上的作用同构于 $G$ 的(左)正则表示.

设 $G$ 自由地作用于 $X$ 上, 任取 $X$ 的一个 $G$-轨道 $\mathcal{O}$, $\mathcal{O}$ 是 $G$-torsor, 而 $X$ 是这些 $G$-torsor 的无交并.

## Burnside's Lemma

## n-Transitivity

## Primitive Actions

## Applications
