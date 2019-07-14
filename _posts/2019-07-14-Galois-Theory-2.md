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
\begin{split}
|G/H| &= |G|/|H| = [E:F]/[E:\mathrm{Inv(H)}] \\
&= [\mathrm{Inv}(H):F] = |\mathrm{Gal(\mathrm{Inv}(H)/F)}|.
\end{split}
$$ 

故上述单同态是同构, 从而 $\mathrm{Gal(\mathrm{Inv(H)}/F)} \cong G/H$.
<p align="right">$\blacksquare$</p>

下面以 $\mathbb{Q}\left(\sqrt[3]{3}, \omega\right)/\mathbb{Q}$ 为例, 展示伽罗瓦理论基本定理. 其中 $\omega = e^{\frac{2\pi i}{3}}$.

记 $E = \mathbb{Q}\left(\sqrt[3]{3}, \omega\right)$. $E$ 是 $x^3-3$ 在 $\mathbb{Q}$ 上的分裂域, 且 $[E :\mathbb{Q}] = 6$. 于是 $G = \mathrm{Gal}(E /\mathbb{Q})$ 是 $6$ 阶群, 它的元素必将 $x^3 - 3$ 的根变到 $x^3 - 3$ 的根, 也必将 $x^2 + x + 1$ 的根变到 $x^2+x+1$ 的根. 因此 $G$ 的 $6$ 个元为:


$$
\begin{split}
\sigma_1 &= \mathrm{Id};\\ 
\sigma_{2}&: \sqrt[3]{3} \mapsto \sqrt[3]{3}\omega, \omega \mapsto \omega; \\
\sigma_3&: \sqrt[3]{3} \mapsto \sqrt[3]{3}\omega^2, \omega \mapsto \omega;\\
\sigma_4&: \sqrt[3]{3} \mapsto \sqrt[3]{3}, \omega \mapsto \omega^2; \\
\sigma_5&: \sqrt[3]{3} \mapsto \sqrt[3]{3}\omega, \omega \mapsto \omega^2;\\
\sigma_6&: \sqrt[3]{3} \mapsto \sqrt[3]{3}\omega^2, \omega \mapsto \omega^2.
\end{split}
$$

则 $\sigma_2$ 是 $3$ 阶元, $\sigma_4$ 是 $2$ 阶元, 且 $\sigma_4\sigma_2\sigma_4^{-1} = \sigma_2^{-1}$, $\sigma_4,\sigma_2$ 生成 $G$. 故 $G \cong D_3 \cong S_3$.

将 $x^3 - 3$ 的 $3$ 个根记为 $r_1 = \sqrt[3]{3}$, $r_2 = \sqrt[3]{3}\omega$, $r_3 = \sqrt[3]{3}\omega^2$. 则将 $G$ 作用于 $$\{r_1,r_2 ,r_3\}$$, 得到一个同态 $G \rightarrow S_3$. 这个群同态是单射, 可知这个同态是同构. 在这个意义下, $G$ 等同于

$$\begin{split}
S_3 = \{
    &\sigma_1 = (1),\sigma_2 = (123),\sigma_3 = (132),\\
    &\sigma_4 = (23),\sigma_5 = (12),\sigma_6 = (13)
\}.
\end{split}$$

其中 $(13)$ 表示 $(r_1r_3)$, 诸如此类. $S_3$ 的全部子群为

$$\begin{split}
A_3 &= \{(1),(123),(132)\}, \\
H_1 &= \{(1),(12)\},\\
H_2 &= \{(1),(13)\},\\
H_3 &= \{(1),(23)\}.
\end{split}$$

其中 $A_3 \triangleleft S_3$, 而 $H_1,H_2,H_3$ 是一个共轭类. 我们首先计算 $\mathrm{Inv}(H_1)$. $E$ 的一组 $F$-基为 $1,\sqrt[3]{3},\sqrt[3]{6},\omega,\sqrt[3]{3}\omega,\sqrt[3]{6}\omega$. 记 $\alpha \in \mathrm{Inv}(H_1)$, 设

$$
\alpha = a_1+ a_2\sqrt[3]{3}+ a_3\sqrt[3]{6}+ a_4\omega+ a_5\sqrt[3]{3}\omega+ a_6\sqrt[3]{6}\omega, \\
$$

其中 $a_1,a_2,a_3,a_4,a_6,a_6 \in \mathbb{Q}$. 则

$$
\sigma_5(\alpha) = a_1-a_4 + a_5\sqrt[3]{3} - a_3\sqrt[3]{6} -a_4\omega + a_2\sqrt[3]{3}\omega + (a_6-a_3)\sqrt[3]{6}\omega.
$$

比较系数, 得 $a_3 = a_4 = 0,a_2 = a_5$. 故 $\alpha = a_1 + a_2\sqrt[3]{3} + a_2\sqrt[3]{3}\omega + a_6\sqrt[3]{6}\omega = a_1 - a_2\sqrt[3]{3}\omega^2 + a_6\sqrt[3]{6}\omega$. 这说明 $\alpha \in \mathrm{Inv}(H_1)$ 当且仅当 $\alpha \in \mathbb{Q}(\sqrt[3]{3}\omega^2)$. 故 $\mathrm{Inv}(H_1) = \mathbb{Q}(\sqrt[3]{3}\omega^2)$. 由 $\sigma_6 = \sigma_4\sigma_5\sigma_4^{-1}$, 知 $H_2 = \sigma_4 H_1 \sigma_4^{-1}$. 故 $\mathrm{Inv}(H_2) = \sigma_4(\mathrm{Inv}(H_1)) = \mathbb{Q}(\sqrt[3]{3}\omega)$. 同理, 由 $H_3 = \sigma_6H_1 \sigma_6^{-1}$ 知 $\mathrm{Inv}(H_3) = \sigma_6(\mathrm{Inv}(H_1)) = \mathbb{Q}(\sqrt[3]{3})$.

下面决定 $\mathrm{Inv}(A_3)$. $S_3$ 的 $3$ 阶子群只有 $A_3$. 故满足 $M/\mathbb{Q}$ 是 $2$ 次扩张的中间域 $M$ 一定是 $\mathrm{Inv}(A_3)$. 考虑 $\mathbb{Q}(\omega)/\mathbb{Q}$, $\omega$ 在 $\mathbb{Q}$ 上的极小多项式是 $2$ 次的, 故 $[\mathbb{Q}(\omega) : \mathbb{Q}] = 2$, 从而 $\mathrm{Inv}(A_3) = \mathbb{Q}(\omega)$.

我们得到
<p align="center">
![](https://raw.githubusercontent.com/Wuxiangdong/Wuxiangdong.github.io/master/_posts/pictures/Galois-Theory-2.svg?sanitize=true)
</p>
