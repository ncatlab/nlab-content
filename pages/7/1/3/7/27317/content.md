
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _(weakly) stable Yang-Mills-Higgs pair_ (or _(weakly) stable YMH connection_) is a [[Yang-Mills-Higgs pair]], around which the Yang-Mills-Higgs [[action functional]] is positive or even strictly positively curved. [[Yang-Mills-Higgs pairs]] are [[critical points]] of the Yang-Mills-Higgs action functional, where the first [[variational calculus|variational]] derivative vanishes. For (weakly) stable Yang-Mills connections, the second derivative is additionally required to be positive or even strictly positive.


## Basics

Consider

* $G$ a [[Lie group]] and $\mathfrak{g}$ its [[Lie algebra]],

* $X$ an [[orientable]] [[Riemannian manifold]] with Riemannian metric $g$ and volume form $vol_g$,

* $P\twoheadrightarrow X$ a [[principal bundle|principal $G$-bundle]] and $Ad(P)\coloneqq P\times_G\mathfrak{g}\twoheadrightarrow B$ its [[adjoint bundle]],

* $\Phi\in\Omega_{Ad}^0(P,\mathfrak{g})\cong\Omega^0(X,Ad(P))\cong\Gamma^\infty(X,Ad(P))$ a smooth section,

* $A\in\Omega_{\operatorname{Ad}}^1(P,\mathfrak{g})\cong\Omega^1(X,Ad(P))$ a [[principal connection]],

* $F_A\coloneqq\mathrm{d}A+\frac{1}{2}[A\wedge A]\in\Omega_{Ad}^2(P,\mathfrak{g})\cong\Omega^2(X,Ad(P))$ its [[curvature]]. If $A$ is a Yang-Mills connection, $F_A$ is also called [[Yang-Mills field]].

## Definition

The _Yang-Mills-Higgs action functional_ (or _YMH action functional_) is given by:

$$
YMH\colon
\Omega^1(X,Ad(P))\times\Gamma^\infty(X,Ad(P))\rightarrow\mathbb{R},
YMH(A,\Phi)
\coloneqq\int_X\|F_A\|^2+\|\mathrm{d}_A\Phi\|^2\mathrm{d}vol_g.
$$

$A$ and $\Phi$ are called a _stable Yang-Mills-Higgs pair_ (or _stable YMH pair_) iff:

$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}\operatorname{YMH}(\alpha(t),\varphi(t))\vert_{t=0}
\gt 0
$$

for all smooth families $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ and $\varphi\colon(-\varepsilon,\varepsilon)\rightarrow\Gamma^\infty(X,Ad(P))$ with $\alpha(0)=A$ and $\varphi(0)=\Phi$. It is called _weakly stable_ if only $\geq 0$ holds. For comparison, the condition for a _Yang-Mills-Higgs pair_ (or _YMH pair_) is:

$$
\frac{\mathrm{d}}{\mathrm{d}t}YMH(\alpha(t),\varphi(t))\vert_{t=0}
=0.
$$

([Hu & Hu 15](#HuHu15), [Cheng 21, Definition 3.1](#Cheng21), [Han, Jin & Wen 23](#HanJinWen23))

\begin{theorem}
**(Formula for Yang--Mills--Higgs stability)**
Let $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(X,Ad(P))$ be a path with $A=\alpha(0)$, $B=\alpha'(0)$ and $C=\alpha''(0)$ and let $\varphi\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(X,Ad(P))$ be a path with $\Phi=\varphi(0)$, $\Psi=\varphi'(0)$ and $\Omega=\varphi''(0)$, then:
$$
\begin{aligned}
\frac{\mathrm{d}^2}{\mathrm{d}t^2}YMH(\alpha(t),\varphi(t))\vert_{t=0}
&=\int_X\|\mathrm{d}_A B\|^2
+\|\mathrm{d}_A \Psi+[B,\Phi]\|^2
+\langle\underbrace{\delta_A F_A-[\mathrm{d}_A\Phi,\Phi]}_{YMH},C\rangle \\
&+\langle\underbrace{\delta_A \mathrm{d}_A\Phi}_{YMH},\Omega\rangle
+\langle F_A,[B\wedge B]\rangle
+2\langle\mathrm{d}_A\Phi,[B,\Psi]\rangle.
\end{aligned}
$$
\end{theorem}
The [[Yang-Mills-Higgs equations]] are $\delta_A F_A-[\mathrm{d}_A \Phi,\Phi]=0$ as well as $\delta_A \mathrm{d}_A \Phi=0$ and therefore the formula simplifies for a [[Yang-Mills-Higgs pair]] $(A,\Phi)$. In this case it also becomes independent of $C$ and $\Omega$.
\begin{proof}
For the calculations for the first term see [[stable Yang-Mills connection]]. One has the following derivatives for the [[covariant derivative]]:
$$
\begin{aligned}
\frac{\mathrm{d}}{\mathrm{d}t}\mathrm{d}_{\alpha(t)}\varphi(t)
&=\frac{\mathrm{d}}{\mathrm{d}t}\left(
\mathrm{d}\varphi(t)
+[\alpha(t),\varphi(t)]
\right) \\
&=\mathrm{d}\varphi'(t)
+[\alpha(t),\varphi'(t)]
+[\alpha'(t),\varphi(t)]
=\mathrm{d}_{\alpha(t)}\varphi'(t)
+[\alpha'(t),\varphi(t)];
\end{aligned}
$$
$$
\begin{aligned}
\frac{\mathrm{d}^2}{\mathrm{d}t^2}d_{\alpha(t)}\varphi(t)
&=\mathrm{d}\varphi''(t)
+[\alpha(t),\varphi''(t)]
+2[\alpha'(t),\varphi'(t)]
+[\alpha''(t),\varphi(t)] \\
&=\mathrm{d}_{\alpha(t)}\varphi''(t)
+2[\alpha'(t),\varphi'(t)]
+[\alpha''(t),\varphi(t)],
\end{aligned}
$$
which combine together into the following second derivative for the additional part of the Yang-Mills-Higgs action functional:
$$
\begin{aligned}
\frac{\mathrm{d}^2}{\mathrm{d}t^2}(YMH-YM)(\alpha(t),\varphi(t))\vert_{t=0}
&=\int_X\left\|\frac{\mathrm{d}}{\mathrm{d}t}\mathrm{d}_{\alpha(t)}\varphi(t)\right\|^2
+\left\langle\mathrm{d}_{\alpha(t)}\varphi(t),\frac{\mathrm{d}^2}{\mathrm{d}t^2}\mathrm{d}_{\alpha(t)}\varphi(t)\right\rangle\mathrm{d}vol_g\vert_{t=0} \\
&=\int_X\|\mathrm{d}_{\alpha(t)}\varphi'(t)+[\alpha'(t),\varphi(t)]\|^2 \\ 
&+\left\langle \mathrm{d}_{\alpha(t)}\varphi(t),\mathrm{d}_{\alpha(t)}\varphi''(t)
+2[\alpha'(t),\varphi'(t)]
+[\alpha''(t),\varphi(t)]\right\rangle\mathrm{d}vol_g
\end{aligned}
$$
\end{proof}
Since the first and second term are always positive, leaving both out directly implies:
\begin{corollary}
If $A\in\Omega^1(X,Ad(P))$ and $\Phi\in\Gamma^\infty(X,Ad(P))$ are a [[Yang-Mills-Higgs pair]] with:
$$
\int_X\langle F_A,[B\wedge B]\rangle
+2\langle\mathrm{d}_A\Phi,[B,\Psi]\rangle\mathrm{d}vol_g
\gt 0\;\text{(or}\geq 0\text{)}
$$
for all $B\in\Omega^1(X,Ad(P))$ and $\Psi\in\Gamma^\infty(X,Ad(P))$, then it is stable (or weakly stable).
\end{corollary}

## Properties

\begin{theorem}
Let $(A,\Phi)$ be a weakly stable YMH pair on $S^n$.

* If $n=4$, then $\mathrm{d}_A\star F_A=0$ (meaning $A$ is a YM connection), $\mathrm{d}_A\Phi=0$ and $\|\Phi\|=1$.
* If $n\geq 5$, then $F_A=0$ (meaning $A$ is flat), $\mathrm{d}_A\Phi=0$ and $\|\Phi\|=1$.

\end{theorem}

([Han, Jin & Wen 23](#HanJinWen23))

## References

* {#HuHu15} Zhi Hu and Sen Hu, _Degenerate and Stable Yang-Mills-Higgs Pair_ (2015), [arxiv:1502.01791](https://arxiv.org/abs/1502.01791)
* {#Cheng21} Da Rong Cheng, _Stable Solutions to the Abelian Yang–Mills–Higgs Equations on $S^2$ and $T^2$_ (2021), Journal of Geometric Analysis **31**, pp. 9551–9572, [doi:10.1007/s12220-021-00619-y](https://doi.org/10.1007/s12220-021-00619-y)
* {#HanJinWen23} Xiaoli Han, Xishen Jin and Yang Wen; _Stability and energy identity for Yang-Mills-Higgs pairs_ (2023), Journal of Mathematical Physics **64**, [arxiv:2303.00270](https://arxiv.org/abs/2303.00270)

## See also

* [[stable Yang-Mills connection]]
* [[Yang-Mills-Higgs equations]]

## References

See also:

* Wikipedia, _[stable Yang-Mills-Higgs pair](https://en.wikipedia.org/wiki/Stable_Yang%E2%80%93Mills%E2%80%93Higgs_pair)_

[[!redirects stable Yang-Mills-Higgs pairs]]
[[!redirects stable YMH pair]]
[[!redirects stable YMH pairs]]

[[!redirects weakly stable Yang-Mills-Higgs pair]]
[[!redirects weakly stable Yang-Mills-Higgs pairs]]
[[!redirects weakly stable YMH pair]]
[[!redirects weakly stable YMH pairs]]