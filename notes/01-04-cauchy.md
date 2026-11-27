# 第 1 章第 4 讲　Cauchy 判别法与闭集套

**e.g.** 取 $\sqrt2$ 的十进制截断 $q_n=10^{-n}\lfloor10^n\sqrt2\rfloor$。当 $m\ge n$ 时，$q_n\le q_m<q_n+10^{-n}$，故尾集 $T_n=\{q_m:m\ge n\}$ 的直径至多为 $10^{-n}$。这在 $\mathbb Q$ 和 $\mathbb R$ 中是同一个估计。

**Def.** 度量空间 $X$ 上的真滤子 $\mathcal F$ 称为 Cauchy 滤子，若对每个 $\varepsilon>0$，存在 $A\in\mathcal F$ 使 $\operatorname{diam}A<\varepsilon$。对数列的尾滤子，这等价于 $\operatorname{diam}T_n\to0$。

**Th.** 完备度量空间中的每个 Cauchy 滤子都收敛到唯一一点。

**Pf.** 取 $A_n\in\mathcal F$ 使 $\operatorname{diam}A_n<2^{-n}$，令 $B_n=A_1\cap\cdots\cap A_n$，$K_n=\overline{B_n}$。有限交仍属于真滤子，故各 $B_n$ 非空。各 $K_n$ 闭且嵌套，直径等于 $B_n$ 的直径，至多为 $2^{-n}$。由完备度量空间中的 Cantor 闭集套定理，存在唯一 $x\in\bigcap_n K_n$。

给定 $r>0$，取 $2^{-n}<r$。由于 $x\in K_n$，有 $B_n\subseteq K_n\subseteq B(x,r)$。由滤子的向上封闭性，$B(x,r)\in\mathcal F$，故 $\mathcal F\to x$。极限唯一性也直接来自度量拓扑的 Hausdorff 性。

**Remark.** 收敛滤子总是 Cauchy 滤子，因为半径 $r$ 的球直径至多为 $2r$。例中的尾滤子在 $\mathbb R$ 中收敛到 $\sqrt2$，在 $\mathbb Q$ 中仍是 Cauchy 滤子，却没有极限。
