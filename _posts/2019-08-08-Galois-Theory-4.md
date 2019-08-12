---
title: 特殊方程的伽罗瓦群
tags: Math Algebra 伽罗瓦理论
---
这是伽罗瓦群的计算的第二部分. 讨论一些特殊方程的伽罗瓦群.

<!-- vim-markdown-toc GFM -->

* [纯粹方程](#纯粹方程)
* [分圆域](#分圆域)
* [素数次对称群](#素数次对称群)
* [一些习题](#一些习题)

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

## 分圆域

**引理** 设 $L_i\, (i = 1,2,\cdots ,s)$ 是域扩张 $E/F$ 的中间域且 $L_i/F$ 均为有限伽罗瓦扩张. 则 $L_1\cdots L_s/F$ 也是有限伽罗瓦扩张, 映射  
$$\begin{aligned}
\pi: \mathrm{Gal}(L_1\cdots L_s/F) &\rightarrow \mathrm{Gal}(L_1/F) \times \cdots \times \mathrm{Gal}(L_s/F), \\ \sigma &\mapsto (\sigma\mid_{L_1},\cdots,\sigma\mid_{L_s})
\end{aligned}$$  
是群的单同态; 且这一同态是同构当且仅当 $[L_1L_2\cdots L_s : F] = [L_1:F]\cdots [L_s:F]$
{:.info}

**证明** 设 $L_i$ 是 $f_i(x) \in F$ 在 $F$ 上的分裂域 $(i = 1,2,\cdots ,s)$, 则 $L_1\cdots L_s$ 是 $f_1(x)\cdots f_s(x)$ 在 $F$ 上的分裂域, 从而 $L_1\cdots L_s/F$ 是有限伽罗瓦扩张. 易见 $\pi$ 保持乘法, 从而是群同态. $\sigma \in \mathrm{Gal}(L_1\cdots L_s/F)$ 可以由 $\sigma$ 在 $f_1(x),f_2(x),\cdots f_s(x)$ 的根上的取值确定, 即可以由 $\sigma\mid_{L_1},\cdots ,\sigma\mid_{L_s}$ 确定. 从而 $\pi$ 是单同态. $\pi$ 给出群同构当且仅当 $\mid  \mathrm{Gal}(L_1\cdots L_s/F)\mid = \mid \mathrm{Gal}(L_1/F) \times \cdots \times \mathrm{Gal}(L_s/F)\mid$, 即 $[L_1\cdots L_s : F] = [L_1:F]\cdots [L_s:F]$.
<p align="right">$\blacksquare$</p>

接下来, 设 $n = n_1n_2\cdots n_s$, 其中 $n_1,\cdots ,n_s$ 是两两互素的大于 $1$ 的正整数. 记 $\omega_k = e^{\frac{2\pi i}{k}}$. 则 $\omega_{n_1}\omega_{n_2}\cdots\omega_{n_s}$ 是一个 $n$ 次本原单位根. 从而 $\mathbb{Q}(\omega_n) = \mathbb{Q}(\omega_{n_1}\cdots\omega_{n_s}) = \mathbb{Q}(\omega_{n_1})\mathbb{Q}(\omega_{n_2})\cdots\mathbb{Q}(\omega_{n_s})$. 又有

$$
\mid\mathbb{Q}(\omega_n)\mid = \varphi(n) = \varphi(n_1)\cdots\varphi(n_s) = \mid\mathbb{Q}(\omega_{n_1})\mathbb{Q}(\omega_{n_2})\cdots\mathbb{Q}(\omega_{n_s})\mid,
$$

这说明 

$$
\mathrm{Gal}(\mathbb{Q}(\omega_n)/\mathbb{Q}) \cong \mathrm{Gal}(\mathbb{Q}(\omega_{n_1})/\mathbb{Q}) \times\cdots\times \mathrm{Gal}(\mathbb{Q}(n_s))
$$

这即是 $$\mathbb{Z}_n^* \cong \mathbb{Z}_{n_1}^* \times\cdots\times \mathbb{Z}_{n_s}^*$$.

当 $k$ 是某一素数 $p$ 的幂时, $$\mathbb{Z}_k^*$$ 的结构已被探明. 于是对任意 $\omega_n$, $\mathrm{Gal}(\mathbb{Q}(\omega_n)/\mathbb{Q})$ 的结构也就已经明确了.

## 素数次对称群

**定理** 设 $f(x) \in \mathbb{Q}[x]$ 是有理数域 $\mathbb{Q}$ 上的 $p$ 次不可约多项式, $p$ 为素数. 若 $f(x)$ 恰好有两个非实的复根 (其余的根均为实数), 则 $f(x)$ 的伽罗瓦群 $G_f$ 同构于对称群 $S_p$.

**证明** 设 $E$ 是 $f(x)$ 在 $\mathbb{Q}$ 上的分裂域, $r_1,r_2,\cdots, r_p$ 是 $f(x)$ 的所有根, 且 $r_1,r_2 \notin \mathbb{R}$, $r_3,\cdots, r_p \in \mathbb{R}$. 则 $p = [\mathbb{Q}(r_1) : \mathbb{Q}]\mid [\mathbb{Q}(r_1,\cdots ,r_n) : \mathbb{Q}] = \mid G_f\mid$. 由 $\mathrm{Sylow}$ 定理, $G_f$ 存在 $p$ 阶元 $\sigma$. 又 $p$ 是素数, 知 $\sigma$ 一定是 $p$-轮换, 这说明 $(1\,2\,3\,\cdots\, p) \in G_f$. $r_1,r_2$ 是 $f(x)$ 唯二的非实根, 从而 $r_1,r_2$ 是共轭的. 令 $\pi: \mathbb{C}\rightarrow\mathbb{C}, a+bi \mapsto a-bi$ 是复数域的复共轭自同构, 则 $\pi\mid_{E} \in G_f$ 且 $\pi$ 交换 $r_1,r_2$, 固定 $r_3,\cdots, r_p$. 这说明 $(1\, 2) \in G_f$. $(1\, 2)$ 和 $(1\,2\,\cdots\, p)$ 生成 $S_p$, 从而 $G_f = S_p$.
<p align="right">$\blacksquare$</p>

**定理(布饶尔)** 设 $p$ 是奇素数, $n_1 \le \cdots \le n_{p-2}$ 均为偶数, $m$ 是满足 $2m > \sum_{1 \le i \le p-2}n_i^2$ 的正偶数. 则 $f(x) = (x^2+m)(x-n_1)\cdots (x-n_{p-2}) - 2$ 
是 $\mathbb{Q}$ 上的不可约多项式且恰好有两个非实的复根. 即 $f(x)$ 在 $\mathbb{Q}$ 上的伽罗瓦群 $G_f \cong S_p$.

## 一些习题

**例** 设 $p$ 是素数, 用 $L$ 表示 $p$ 元域 $$\mathbb{Z}_p$$ 的所有形如 $\sigma_{a,b}: x \mapsto ax+b$, $a\ne 0,b \in \mathbb{Z}_p$ 的一一变换对于映射的合成作成的群, 用 $T$ 表示 $L$ 中所有形如 $\sigma_b: x \mapsto x+b$, $b \in \mathbb{Z}_p$ 的元作成的群. 将 $L$ 视为 $\mathbb{Z}_p$ 的置换群, 即视 $L$ 为对称群 $S_p$ 的子群. 证明  
$\mathrm{(i)}$ $$L \cong \left\{\begin{pmatrix}a & b \\ 0 & 1\end{pmatrix} \mid a \in \mathbb{Z}_p^*, b\in\mathbb{Z}_p\right\}$$, $L$ 是 $\mathbb{Z}_p$ 的可迁置换群, 且 $L$ 是可解群;  
$\mathrm{(ii)}$ $$T \cong \left\{\begin{pmatrix}1 & b \\ 0 & 1\end{pmatrix}\mid b \in \mathbb{Z}_p\right\}$$, $T$ 是 $\mathbb{Z}_p$ 的可迁置换群, 且 $T$ 是 $L$ 的唯一 $\rm{Sylow}$ -$p$ 子群 (从而 $T$ 是 $L$ 的正规子群);  
$\mathrm{(iii)}$ 设 $$\{1\} \ne H \leqslant L$$. 利用[习题 $7$](https://wuxiangdong.github.io/2019/07/17/Galois-Theory-3.html#伽罗瓦的原始思想)证明: $H$ 是 $L$ 的正规子群当且仅当 $T \leqslant H$;  
$\mathrm{(iv)}$ 设 $T \leqslant H \leqslant L$. 则 $T$ 恰是 $H$ 中所有没有固定点的元生成的子群;  
$\mathrm{(v)}$ 设 $T \leqslant H \leqslant L$. 则 $T$ 恰是 $H$ 中所有 $p$-轮换生成的子群.
{:.warning}

**证明** $\mathrm{(i)}$ 记 $$G= \left\{\begin{pmatrix}a & b \\ 0 & 1\end{pmatrix} \mid a \in \mathbb{Z}_p^*, b\in\mathbb{Z}_p\right\}$$ 由

$$
\sigma_{a,b}\sigma_{a',b'}(x) = \sigma_{a,b}(a'x+b') = aa'x+ab'+b
$$

知 $$\pi: \sigma_{a,b} \mapsto \begin{pmatrix}a & b \\ 0 & 1\end{pmatrix}$$ 给出 $L \rightarrow G$ 的群同态. 这个同态的核为 $$\{\sigma_{1,0}\}$$, 从而这个同态是单同态. 任意 $$a \in \mathbb{Z}_p^*$$, $$b \in \mathbb{Z}_p$, $\sigma_{a,b}$$ 给出 $\mathbb{Z}_p$ 的一一变换 (因为 $ax+b = ay+b \Leftrightarrow ax = ay \Leftrightarrow x = y$), 从而 $\pi$ 是满射, 推出 $\pi$ 给出同构 $L \cong G$.

任意 $$x, y\in\mathbb{Z}_p$$, 映射 $\sigma_{1,y-x} \in L$ 满足 $\sigma_{1,y-x}(x) = x + y - x = y$. 这说明 $L$ 是 $\mathbb{Z}_p$ 的可迁置换群.

最后证明 $L$ 是可解群. 这等价于 $G$ 可解. 由 $\mid G\mid = p(p-1)$, 知道 $G$ 有唯一的 $\mathrm{Sylow}$-$p$ 子群. 即题中所指 $T$. 记 $$M = \left\{\begin{pmatrix}a & 0 \\ 0 & 1\end{pmatrix}\mid a \in \mathbb{Z}_p^*\right\}$$, 则 $MT = G$ 且 $$M\cap T = \left\{\begin{pmatrix} 1 & 0 \\ 0 & 1\end{pmatrix}\right\}$$. 从而 $G/T = MT/T \cong M/T\cap M = M$. $T$ 和 $G/T$ 皆是可解群, 从而 $G$ 是可解群.

$\mathrm{(ii)}$ $$\pi(T) = \left\{\begin{pmatrix}1&b \\ 0 & 1\end{pmatrix}\mid b \in \mathbb{Z}_p\right\}$$. 由 $\mathrm{(i)}$ 中的证明也可知 $T$ 是 $\mathrm{Z}_p$ 的可迁置换群. 由 $\mid L\mid=p(p-1)$ 知 $L$ 只有唯一的 $\mathrm{Sylow}$-$p$ 子群.

$\mathrm{(iii)}$ 设 $H \triangleleft L$. $L$ 是 $\mathbb{Z}_p$ 的可迁置换群, 从而 $H$ 含有 $p$-轮换. $T$ 是 $L$ 唯一的 $\mathrm{Sylow}$-$p$ 子群且 $\mid T\mid = p$. 故 $H$ 包含 $T$.

反之, 设 $T \leqslant H$, 任意 $\sigma_{a,b} \in L$ 和 $\sigma_{a',b'} \in H$, 有

$$
\begin{aligned}
\sigma_{a,b}^{-1}\sigma_{a',b'}\sigma_{a,b}(x) &= \sigma_{a^{-1},-a^{-1}b}\sigma_{a',b'}(ax+b) \\
&= \sigma_{a^{-1},-a^{-1}b}(a'ax+a'b+b') \\
&= a'x+a^{-1}a'b+a^{-1}b' - a^{-1}b.
\end{aligned}
$$

于是

$$
\begin{aligned}
\sigma_{a,b}^{-1}\sigma_{a',b'}\sigma_{a,b} &= \sigma_{a',a^{-1}a'b+a^{-1}b'-a^{-1}b} = \sigma_{1,a^{-1}a'b+a^{-1}b'-a^{-1}b-b'}\sigma_{a',b'} \\
&\in T\sigma_{a',b'} \subseteq H.
\end{aligned}
$$

这说明 $H$ 是 $L$ 的正规子群.

$\mathrm{(iv)}$ 对于 $\sigma_{a,b} \in H$, $\sigma_{a,b}$ 没有固定点当且仅当 $a \ne 1$ 且 $b \ne 0$, 当且仅当 $\sigma_{a,b} \in T$ 且 $b \ne 0$, 即 $\sigma_{a,b}$ 是 $T$ 中的元且 $\sigma_{a,b}$ 不是幺元.

$\mathrm{(v)}$ $T$ 是 $L$ 唯一的 $\mathrm{Sylow}$-$p$ 子群, 从而 $H$ 中的 $p$-轮换属于 $T$. 又 $T \leqslant H$, 且 $T$ 是 $p$ 阶群, 从而 $H$ 中的 $p$-轮换生成 $T$.
<p align="right">$\blacksquare$</p>

**例** 设 $L$ 和 $T$ 同上题, $T \leqslant H \leqslant L$, $G$ 是 $S_p$ 的子群且 $H$ 是 $G$ 的正规子群. 证明  
$\mathrm{(i)}$ 设 $1 \ne \sigma \in G$. 利用上题 $\mathrm{(iv)}$ 证明: 存在 $0 \ne a \in \mathbb{Z}_p$ 使得 $\sigma(x+1) = \sigma(x) + a$, $\forall x \in \mathbb{Z}_p$.  
$\mathrm{(ii)}\, G \leqslant L$.
{:.warning}

**证明** $\mathrm{(i)}$ 首先说明 $T \triangleleft G$. $T$ 恰是 $H$ 中所有没有固定点的元生成的子群. 现设 $\sigma \in H$ 且 $\sigma$ 没有固定点. 由 $H \triangleleft G$, 知任意 $\pi \in G$, $\pi\sigma\pi^{-1} \in H$. 且 $\pi\sigma\pi^{-1}$ 也没有固定点 (否则, 若 $x$ 是其固定点, 则 $\pi^{-1}(x)$ 是 $\sigma$ 的固定点). 设 $S$ 是 $H$ 中所有没有固定点的元组成的集合, 则 $\pi S\pi^{-1}$ 是 $S$ 的一个置换, 故 $\pi T\pi^{-1} = T$.

设 $1 \ne \sigma \in G$, 记 $\sigma_1 \in T$, 且 $\sigma_1(x) = x+1$. 则 $\sigma\sigma_1\sigma^{-1} \in T$. 记 $\sigma\sigma_1\sigma^{-1}(x) = x + a$, $a \in \mathbb{Z}_p$. 则 $\sigma(x+1) = \sigma\sigma_1(x) = \sigma\sigma_1\sigma^{-1}\sigma(x) = \sigma(x) + a$.

$\mathrm{(ii)}$ 任意 $$x \in \mathbb{Z}_p$$, 设 $$x = \underbrace{1+1+\cdots +1}_{i\,\text{个}}$$, $$0 \le i \le p-1$$. 则 

$$\begin{aligned}
\sigma(x) = \sigma(\underbrace{1+\cdots + 1}_{i\, \text{个}}) &= \sigma(\underbrace{1+\cdots + 1}_{(i-1)\,\text{个}}) + a \\
&\cdots \\
& = \sigma(1) + (i-1)a = ax + \sigma(1) - a.
\end{aligned}$$ 

这说明 $G \leqslant L$.
<p align="right">$\blacksquare$</p>
