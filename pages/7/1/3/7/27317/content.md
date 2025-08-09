
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

* $B$ an [[orientable]] [[Riemannian manifold]] with Riemannian metric $g$ and volume form $\operatorname{vol}_g$,

* $E\twoheadrightarrow B$ a [[principal bundle|principal $G$-bundle]] and $\operatorname{Ad}(E)\coloneqq E\times_G\mathfrak{g}\twoheadrightarrow B$ its [[adjoint bundle]],

* $\Phi\in\Omega_{\operatorname{Ad}}^0(E,\mathfrak{g})\cong\Omega^0(B,\operatorname{Ad}(E))\cong\Gamma^\infty(B,\Ad(E))$ a smooth section,

* $A\in\Omega_{\operatorname{Ad}}^1(E,\mathfrak{g})\cong\Omega^1(B,\operatorname{Ad}(E))$ a [[principal connection]],

* $F_A\coloneqq\mathrm{d}A+\frac{1}{2}[A\wedge A]\in\Omega_{\operatorname{Ad}}^2(E,\mathfrak{g})\cong\Omega^2(B,\operatorname{Ad}(E))$ its [[curvature]]. If $A$ is a Yang-Mills connection, $F_A$ is also called [[Yang-Mills field]].

## Definition

The _Yang-Mills-Higgs action functional_ (or _YMH action functional_) is given by:

$$
\operatorname{YMH}\colon
\Omega^1(B,\operatorname{Ad}(E))\times\Gamma^\infty(B,\operatorname{Ad}(E))\rightarrow\mathbb{R},
\operatorname{YMH}(A,\Phi)
\coloneqq\int_B\|F_A\|^2+\|\mathrm{d}_A\Phi\|^2\mathrm{d}\operatorname{vol}_g.
$$

$A$ and $\Phi$ are called a _stable Yang-Mills-Higgs pair_ (or _stable YMH pair_) iff:

$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}\operatorname{YMH}(\alpha(t),\varphi(t))\vert_{t=0}
\gt 0
$$

for all smooth families $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(B,\operatorname{Ad}(E))$ and $\varphi\colon(-\varepsilon,\varepsilon)\rightarrow\Gamma^\infty(B,\operatorname{Ad}(E))$ with $\alpha(0)=A$ and $\varphi(0)=\Phi$. It is called _weakly stable_ if only $\geq 0$ holds. For comparison, the condition for a _Yang-Mills-Higgs pair_ (or _YMH pair_) is:

$$
\frac{\mathrm{d}}{\mathrm{d}t}\operatorname{YMH}(\alpha(t),\varphi(t))\vert_{t=0}
=0.
$$

([Hu & Hu 15](#HuHu15), [Cheng 21, Definition 3.1](#Cheng21), [Han, Jin & Wen 23](#HanJinWen23))

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