# 第 1 章第 3 讲（下）　尾集与上下极限

### e.g.　从一个振荡数列开始

取 $x_n=(-1)^n+1/n$，$n\ge1$。从第 $n$ 项起，所有项都落在哪个最小闭区间里？记 $T_n=\{x_k:k\ge n\}$，这个区间就是 $[\inf T_n,\sup T_n]$。

奇数项从上方逼近 $-1$，所以每个尾集的下确界都是 $-1$。偶数项递减且大于所有奇数项，所以尾集的上确界是其中第一个偶数项。随着 $n$ 增大，区间的左端点恒为 $-1$，右端点趋于 $1$。

### Def　尾集、下极限与上极限

设 $(x_\alpha)_{\alpha\in I}$ 是实数网。记 $T_\alpha=\{x_\beta:\beta\ge\alpha\}$ 为尾集，记 $\ell_\alpha=\inf T_\alpha$，$u_\alpha=\sup T_\alpha$。所有确界均在扩充实数系中取。定义

$$
\liminf_\alpha x_\alpha=\sup_\alpha\ell_\alpha,\qquad
\limsup_\alpha x_\alpha=\inf_\alpha u_\alpha.
$$

### Prop　尾部的两个端点各自单调收敛

$\ell_\alpha$ 递增趋于下极限，$u_\alpha$ 递减趋于上极限。

**Pf.** 若 $\alpha\le\gamma$，则 $T_\gamma\subseteq T_\alpha$，所以 $\ell_\alpha\le\ell_\gamma\le u_\gamma\le u_\alpha$。分别应用上一节的单调网定理及其对偶即可。

### Th　收敛判据

对 $L\in\mathbb R$，有 $x_\alpha\to L$ 当且仅当 $\liminf_\alpha x_\alpha=\limsup_\alpha x_\alpha=L$。

**Pf.** 若 $x_\alpha\to L$，对每个 $\varepsilon>0$，充分靠后的尾集都含于 $(L-\varepsilon,L+\varepsilon)$。其两个端点因而都落在 $[L-\varepsilon,L+\varepsilon]$ 中，故都趋于 $L$。

反过来，若两个端点网都趋于 $L$，由 $\ell_\alpha\le x_\alpha\le u_\alpha$，夹逼即得 $x_\alpha\to L$。

**Remark.** 夹逼时用到了指标集的有向性。下端点高于 $L-\varepsilon$ 与上端点低于 $L+\varepsilon$ 可以从不同指标开始成立。取这两个指标的共同上界，两项估计就在同一条尾网上同时成立。

### Def　从尾集到滤子

网的尾滤子是 $\mathcal F_x=\{A\subseteq\mathbb R:\exists\alpha,\ T_\alpha\subseteq A\}$。它记录哪些条件最终成立。对 $\mathbb R$ 上任意真滤子 $\mathcal F$，在扩充实数系中定义

$$
\liminf\mathcal F=\sup_{A\in\mathcal F}\inf A,\qquad
\limsup\mathcal F=\inf_{A\in\mathcal F}\sup A.
$$

**Prop.** 两式都可以只在任一滤子基上取确界。

**Pf.** 每个滤子成员 $A$ 都包含某个基成员 $B$，故 $\inf A\le\inf B$ 且 $\sup B\le\sup A$。又因基成员本身属于滤子，两式均保持原值。对尾滤子取尾集为基，就还原网的公式。

**e.g.** 对本节的振荡数列，其尾滤子用尾集作基，给出下极限 $-1$ 和上极限 $1$。只保留偶数项得到的子列，其尾滤子更细，上下极限都等于 $1$。

**Th.** 对有限实数 $L$，$\mathcal F\to L$ 当且仅当 $\liminf\mathcal F=\limsup\mathcal F=L$。

**Pf.** 若两者都等于 $L$，任取 $a<L<b$，可找 $A,B\in\mathcal F$ 满足 $\inf A>a$、$\sup B<b$。则 $A\cap B\in\mathcal F$ 且 $A\cap B\subseteq(a,b)$，故 $(a,b)\in\mathcal F$。反向若 $\mathcal F\to L$，则每个 $L$ 的邻域属于滤子，每个滤子成员都与每个这样的邻域相交。因此对所有 $A\in\mathcal F$ 有 $\inf A\le L\le\sup A$。再取滤子成员 $(L-\varepsilon,L+\varepsilon)$ 并令 $\varepsilon\downarrow0$，即得两式均等于 $L$。
