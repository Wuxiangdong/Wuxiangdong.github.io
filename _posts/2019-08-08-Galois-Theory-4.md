---
title: 特殊方程的伽罗瓦群
tags: Math Algebra 伽罗瓦理论
---
这是伽罗瓦群的计算的第二部分. 讨论一些特殊方程的伽罗瓦群.

<!-- vim-markdown-toc GFM -->

* [纯粹方程](#纯粹方程)

<!-- vim-markdown-toc -->

## 纯粹方程
设 $F$ 是域. 将方程 $g(x) = x^n - a = 0\, (0 \ne a \in F, n \ge 2)$ 称为 **纯粹方程**. 这类方程的伽罗瓦群是研究任意方程的根式可解性的重要一步. 这里假设 $F$ 特征为零, 或这为不整除 $n$ 的素数 $p$. 这等价于 $g(x)$ 无重根. 下面计算 $G_g = \mathrm{Gal}(E/F)$, 其中 $E$ 是 $g(x)$ 在 $F$ 上的分裂域.

**引理** 设整数 $n\ge 2$, 域 $F$ 的特征为零或与 $n$ 互素, $\omega$ 是一个 $n$ 次本原根.  
$\mathrm{(i)}$ 设 $f(x)=x^n - 1 \in F[x]$. 则 $G_f$ 是 $$\mathbb{Z}_n^*$$ 的子群, 从而是 $\rm Abel$ 群. 而 $$G_f = \mathbb{Z}_n^*$$ 当且仅当分圆多项式 $\Phi_n(x)$ 是 $F$ 上的不可约多项式.  
特别的, 分圆多项式 $\Phi_n(x)$ 在 $\mathbb{Q}$ 上的伽罗瓦群同构于 $$\mathbb{Z}_n^*$$.  
$\mathrm{(ii)}$ 设 $\omega \in F$, $g(x) = x^n - a$, $0 \ne a \in F$. 则 $G_g$ 是 $m$ 阶循环群, 其中 $m \mid n$; 且 $G_g$ 是 $n$ 阶循环群当且仅当 $g(x)$ 在 $F$ 上不可约.  
$\mathrm{(iii)}$ 设 $\omega \notin F$. 用 $GL(2,\mathbb{Z}_n)$ 表示剩余类环 $\mathbb{Z}_n$ 上的所有 $2$ 阶可逆矩阵的集合对于矩阵乘法作成的群. 则 $G_g$ 是 $H$ 的子群, 其中  
$$H = \left\{\begin{pmatrix} k & l \\ 0 & 1 \end{pmatrix} \mid k \in \mathbb{Z}_n^*, l \in \mathbb{Z}_n\right\}$$  
是 $GL(2,\mathbb{Z}_n)$ 的子群.  
$\mathrm{(iv)}$ 设 $p$ 为素数, $g(x) = x^p - a$ 为有理数域 $\mathbb{Q}$ 上的不可约多项式. 则 $G_g$ 同构于子群 $$H = \left\{
\begin{pmatrix}
k & l \\
0 & 1
\end{pmatrix} \mid k \in \mathbb{Z}_p^*, l \in\mathbb{Z}_p
\right\}$$.
{:.info}
<!--more-->

**证明** 首先, $F$ 的特征为零或与 $n$ 互素, 故 $n$ 次本原根是存在的.

$\mathrm{(i)}$ 设 $E$ 是 $f(x) = x^n - 1$ 在 $F$ 上的分裂域, 有 $E = F(\omega)$. 对 $\sigma \in \mathrm{Gal}(E/F)$, $\sigma(\omega) = \omega^{k}\,(1\le k\le n-1)$ 也是 $n$ 次本原根, 故 $(k,n) = 1$. $\sigma$ 由 $k$ 唯一决定, 则 $\sigma \mapsto \overline{k}$ 给出群的单同态 $$G_f \rightarrow \mathbb{Z}_n^*$$.

这个同态是满射, 当且仅当任意 $(k,n) = 1\, (1\le k\le n-1)$, 存在 $F$-同构 $\sigma$ 使得 $\sigma(\omega) = \omega^k$, 即 $\omega$ 和 $\omega^k$ 在 $F$ 上的极小多项式相同. 这等价于多项式

$$
\Phi_n(x) = \prod_{1\le k \le n, (k,n) = 1} (x-\omega^k) \in F[x]
$$

是 $F$ 上的不可约多项式. 特别地, 分圆多项式 $\Phi_n(x)$ 是 $\mathbb{Q}$ 上的不可约多项式, 因此它在 $Q$ 上的伽罗瓦群同构于 $\mathbb{Z}_n^*$.

$\mathrm{(ii)}$ 设 $E$ 是 $g(x) = x^n - a$ 在 $F$ 上的分裂域, $b$ 是 $g(x)$ 的一根, 则 $g(x)$ 的所有根为 $b,b\omega,\cdots, b\omega^{n-1}$, 有 $E = F(b,\omega) = F(b)$ (注意 $\omega\in F$). 对 $\sigma \in \mathrm{Gal}(E/F)$, 存在 $0 \le i\le n-1$ 使得 $\sigma(b) = b\omega^i$. $\sigma$ 由 $i$ 唯一决定, 于是 $\sigma \mapsto \overline{i}$ 给出群的单同态 $G_g \rightarrow \mathbb{Z}_n$. 于是 $G_g$ 是循环群 $\mathbb{Z}_n$ 的子群, 故 $G_g$ 的阶 $m$ 整除 $n$.

$g(x)$ 无重根, 故 $E/F$ 是有限伽罗瓦扩张. $\mid G_f\mid = [E:F] = [F(b):F]$. 故 $\mid G_f\mid = n$ 当且仅当 $b$ 在 $F$ 上的极小多项式次数为 $n$, 当且仅当 $g(x)$ 在 $F$ 上不可约.

$\mathrm{(iii)}$ 设 $E$ 是 $g(x)$ 在 $F$ 上的分裂域, 有 $E=F(b,\omega)$. 任意 $\sigma \in \mathrm{Gal}(E/F)$, 有 $\sigma(b) = b\omega^l$, $\sigma(\omega) = \omega^k$ 且 $(k,n) = 1$, $0 \le i,k \le n-1$. $\sigma$. $\sigma$ 由 $l$ 和 $k$ 唯一决定, 记 $\sigma = \sigma_{k,l}$, 则对 $\sigma_{k,l},\sigma_{k',l'} \in \mathrm{Gal}(E/F)$, 有

$$
\begin{aligned}
\sigma_{k,l}\sigma_{k',l'}(b) &= \sigma_{k,l}(b\omega^{l'}) = b\omega^{kl' + l}; \\
\sigma_{k,l}\sigma_{k',l'}(\omega) &= \sigma_{k,l}(\omega^{k'}) = \omega^{kk'}.
\end{aligned}
$$

故

$$
\psi:\mathrm{Gal}(E/F) \rightarrow H, \sigma_{k,l} \mapsto
\begin{pmatrix}
k & l \\
0 & 1
\end{pmatrix}
$$

是群的单同态. 因此 $\mathrm{Gal}(E/F)$ 是 $H$ 的一个子群.

$\mathrm{(iv)}$ 由 $\mathrm{(iii)}$, 只需证明 $G_g$ 和 $H$ 的阶相同. 设 $b$ 是 $g(x)$ 的一个根, 则 $[\mathbb{Q}(b) : \mathbb{Q}] = p$. 而 $p$ 次本原根 $\omega$ 在 $\mathbb{Q}$ 上的极小多项式为 $x^{p-1} + \cdots + x + 1$, 故 $[\mathbb{Q}(\omega) :\mathbb{Q}] = p-1$. 由 $$[\mathbb{Q}(b,\omega):\mathbb{Q}] = [\mathbb{Q}(b,\omega) : \mathbb{Q}(b)]p = [\mathbb{Q}(b,\omega):\mathbb{Q}(\omega)](p-1)$$ 知道 $p \mid [\mathbb{Q}(b,\omega):\mathbb{Q}(\omega)]$, 从而 $[\mathbb{Q}(b,\omega) : \mathbb{Q}(\omega)] \ge p$. 而 $b$ 在 $\mathbb{Q}(\omega)$ 上的极小多项式的次数小于或等于 $p$. 故 $[\mathbb{Q}(b,\omega) : \mathbb{Q}(\omega)] = p$, 从而 

$$\mid G_g\mid = [\mathbb{Q}(b,\omega) : \mathbb{Q}] = [\mathbb{Q}(b,\omega) : \mathbb{Q}(\omega)][\mathbb{Q}(\omega) : \mathbb{Q}] = p(p-1) = H.$$

由 $\mathrm{(iii)}$ 知 $G_g$ 同构于 $H$.
<p align="right">$\blacksquare$</p>

**例** 设 $p$ 是素数, 用 $L$ 表示 $p$ 元域 $\mathbb{Z}_p$ 的所有形如 $$\sigma_{a,b}: x \mapsto ax+b$, $a\ne 0,b \in \mathbb{Z}_p$$ 的一一变换对于映射的合成作成的群, 用 $T$ 表示 $L$ 中所有形如 $\sigma_b: x \mapsto x_b$, $b \in \mathbb{Z}_p$ 的元作成的群. 将 $L$ 视为 $\mathbb{Z}_p$ 的置换群, 即视 $L$ 为对称群 $S_p$ 的子群. 证明  
$\mathrm{(i)}$ $$L \cong \left\{\begin{pmatrix}a & b \\ 0 & 1\end{pmatrix} \mid a \in \mathbb{Z}_p^*, b\in\mathbb{Z}_p\right\}$$, $L$ 是 $\mathbb{Z}_p$ 的可迁置换群, 且 $L$ 是可解群;  
$\mathrm{(ii)}$ $$T \cong \left\{\begin{pmatrix}1 & b \\ 0 & 1\end{pmatrix}\mid b \in \mathbb{Z}_p\right\}$$, $T$ 是 $\mathbb{Z}_p$ 的可迁置换群, 且 $T$ 是 $L$ 的唯一 $\rm{Sylow}$ -$p$ 子群 (从而 $T$ 是 $L$ 的正规子群);  
$\mathrm{(iii)}$ 设 $$\{1\} \ne H \leqslant L$$. 利用习题 $7$ 证明: $H$ 是 $L$ 的正规子群当且仅当 $T \leqslant H$;  
$\mathrm{(iv)}$ 设 $T \leqslant H \leqslant L$. 设 $T$ 恰是 $H$ 中所有没有固定点的元生成的子群;  
$\mathrm{(v)}$ 设 $T \leqslant H \leqslant L$. 则 $T$ 恰是 $H$ 中所有 $p$-轮换生成的子群.
{:.warning}

**证明** $\mathrm{(i)}$ 记 $$G= \left\{\begin{pmatrix}a & b \\ 0 & 1\end{pmatrix} \mid a \in \mathbb{Z}_p^*, b\in\mathbb{Z}_p\right\}$$ 由

$$
\sigma_{a,b}\sigma_{a',b'}(x) = \sigma_{a,b}(a'x+b') = aa'x+ab'+b
$$

知 $\pi: \sigma_{a,b} \mapsto \begin{pmatrix}a & b \\ 0 & 1\end{pmatrix}$ 给出 $L \rightarrow G$ 的群同态. 这个同态的核为 $$\{\sigma_{1,0}\}$$, 从而这个同态是单同态. 任意 $$a \in \mathbb{Z}_p^*$$, $b \in \mathbb{Z}_p$, $\sigma_{a,b}$ 给出 $\mathbb{Z}_p$ 的一一变换 (因为 $ax+b = ay+b \Leftrightarrow ax = ay \Leftrightarrow x = y$), 从而 $\pi$ 是满射, 推出 $\pi$ 给出同构 $L \cong G$.

任意 $x, y\in\mathbb{Z}_p$, 映射 $\sigma_{1,y-x} \in L$ 满足 $\sigma_{1,y-x}(x) = x + y - x = y$. 这说明 $L$ 是 $\mathbb{Z}_p$ 的可迁置换群.

最后证明 $L$ 是可解群. 这等价于 $G$ 可解. 由 $\mid G\mid = p(p-1)$.

未完待续.
