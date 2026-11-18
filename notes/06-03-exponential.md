# 第 6 章第 1–3 讲　从指数函数的三阶导数到嵌套线性算子

设 $f:\mathbb R\to\mathbb R$，$f(x)=e^x$。经典计算给出 $f'(x)=f''(x)=f'''(x)=e^x$。用 Fréchet 微分重算时，每次求导都会多出一个可以代入的方向。

记 $I:\mathbb R\to\mathbb R$ 为恒等映射。一阶微分是 $Df(x)=e^x I$，即 $Df(x)(h)=e^xh$。第二次求导时变化的是基点 $x$。因为 $\|aI\|_{\mathrm{op}}=|a|$，有

$$
\left\|Df(x+t)-Df(x)-te^x I\right\|_{\mathrm{op}}
=\left|e^{x+t}-e^x-te^x\right|=o(|t|).
$$

所以 $D^2f(x)(u)=e^xuI$。它仍是线性算子，给它输入 $h$ 才得到 $D^2f(x)(u)(h)=e^xuh$。

再记 $J(u)=uI$。映射 $J$ 是固定的有界线性算子，且 $\|J\|=1$。将 $D^2f(x)=e^xJ$ 代入同样的算子范数估计，得到 $D^3f(x)(v)=e^xvJ$，于是

$$
D^3f(x)(v)(u)(h)=e^xvuh.
$$

三个方向都取 $1$ 时就读回 $f'''(x)=e^x$。接下来的第 4 讲要证明，对一般赋范空间 $X,Y$，对应 $A\mapsto[(u,h)\mapsto A(u)(h)]$ 给出从嵌套算子空间到连续双线性映射空间的等距同构。
