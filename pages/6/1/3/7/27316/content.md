
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

A _(weakly) stable Yang-Mills connection_ (or _(weakly) stable YMH connection_) is a [[Yang-Mills connection]], around which the Yang-Mills [[action functional]] is positive or even strictly positively curved. [[Yang-Mills connections]] are [[critical points]] of the Yang-Mills action functional, where the first [[variational calculus|variational]] derivative vanishes. For (weakly) stable Yang-Mills connections, the second derivative is additionally required to be positive or even strictly positive.

## Basics

Consider

* $G$ a [[Lie group]] and $\mathfrak{g}$ its [[Lie algebra]],

* $X$ an [[orientable]] [[Riemannian manifold]] with Riemannian metric $g$ and volume form $vol_g$,

* $P\twoheadrightarrow X$ a [[principal bundle|principal $G$-bundle]] and $Ad(P)\coloneqq P\times_G\mathfrak{g}\twoheadrightarrow X$ its [[adjoint bundle]],

* $A\in\Omega_{Ad}^1(P,\mathfrak{g})\cong\Omega^1(X,Ad(P))$ a [[principal connection]],

* $F_A\coloneqq\mathrm{d}A+\frac{1}{2}[A\wedge A]\in\Omega_{Ad}^2(P,\mathfrak{g})\cong\Omega^2(X,Ad(P))$ its [[curvature]]. If $A$ is a Yang-Mills connection, $F_A$ is also called [[Yang-Mills field]].

## Definition

The _Yang-Mills action functional_ (or _YM action functional_) is given by:

$$
\operatorname{YM}\colon\Omega^1(X,\operatorname{Ad}(P))\rightarrow\mathbb{R},
\operatorname{YM}(A)
\coloneqq\int_X\|F_A\|^2\mathrm{d}\operatorname{vol}_g.
$$

$A$ is called a _stable Yang-Mills connection_ (or _stable YM connection_) iff:

$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}\operatorname{YM}(\alpha(t))\vert_{t=0}
\gt 0
$$

for all smooth families $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(X,\operatorname{Ad}(P))$ with $\alpha(0)=A$. It is called _weakly stable_ if only $\geq 0$ holds. If it is not weakly stable, it is called _unstable_.

([Chiang 2013, Definition 3.1.7](#Chiang13))

For comparison, the condition for a _Yang-Mills connection_ (or _YM connection_) is:

$$
\frac{\mathrm{d}}{\mathrm{d}t}\operatorname{YM}(\alpha(t))\vert_{t=0}
=0.
$$

If $A$ is a (weakly) stable or unstable Yang-Mills connection, $F_A$ is also called _(weakly) stable_ or _unstable Yang-Mills field_.

\begin{theorem}
**(Formula for Yang--Mills stability)**
Let $\alpha\colon(-\varepsilon,\varepsilon)\rightarrow\Omega^1(X,Ad(P))$ be a path with $A=\alpha(0)$, $B=\alpha'(0)$ and $C=\alpha''(0)$, then:
$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}YM(\alpha(t))\vert_{t=0}
=\int_X\|\mathrm{d}_A B\|^2
+\langle F_A,[B\wedge B]\rangle
+\langle\underbrace{\delta_A F_A}_{YM},C\rangle\mathrm{d}vol_g.
$$
\end{theorem}
The [[Yang-Mills equations]] are $\delta_A F_A=0$ and therefore the formula simplifies for a [[Yang-Mills connection]] $A$. In this case it also becomes independent of $C$.
\begin{proof}
One has the following derivatives for the [[curvature]]:
$$
\frac{\mathrm{d}}{\mathrm{d}t}F_{\alpha(t)}
=\frac{\mathrm{d}}{\mathrm{d}t}\left(\mathrm{d}\alpha(t)+\frac{1}{2}[\alpha(t)\wedge\alpha(t)]\right)
=\mathrm{d}\alpha'(t)+[\alpha(t)\wedge\alpha'(t)]
=\mathrm{d}_{\alpha(t)}\alpha'(t);
$$
$$
\frac{\mathrm{d}^2}{\mathrm{d}t^2}F_{\alpha(t)}
=\mathrm{d}_{\alpha(t)}\alpha''(t)
+[\alpha'(t)\wedge\alpha'(t)],
$$
which combine together into the following second derivative for the [[Yang-Mills action functional]]:
$$
\begin{aligned}
\frac{\mathrm{d}^2}{\mathrm{d}t^2}YM(\alpha(t))\vert_{t=0}
&=\int_X\left\|\frac{\mathrm{d}}{\mathrm{d}t}F_{\alpha(t)}\right\|^2
+\left\langle F_{\alpha(t)},\frac{\mathrm{d}^2}{\mathrm{d}t^2}F_{\alpha(t)}\right\rangle\mathrm{d}vol_g\vert_{t=0} \\
&=\int_X\left\|\mathrm{d}_{\alpha(t)}\alpha'(t)\right\|^2
+\left\langle F_{\alpha(t)},\mathrm{d}_{\alpha(t)}\alpha''(t)
+[\alpha'(t)\wedge\alpha'(t)]\right\rangle\mathrm{d}vol_g\vert_{t=0} \\
&=\int_X\|\mathrm{d}_A B\|^2
+\langle F_A,\mathrm{d}_A C+[B\wedge B]\rangle.
\end{aligned}
$$
\end{proof}
Since the first term is always positive, leaving it out directly implies:
\begin{corollary}
If $A\in\Omega^1(X,Ad(P))$ is a [[Yang-Mills connection]] with:
$$
\int_X\langle F_A,[B\wedge B]\rangle\mathrm{d}\vol_g
\gt 0\;\text{(or}\geq 0\text{)}
$$
for all $B\in\Omega^1(X,Ad(P))$, then it is stable (or weakly stable).
\end{corollary}

## Properties

\begin{theorem}
Every weakly stable Yang-Mills connection on $S^n$ for $n\geq 5$ is flat.
\end{theorem}

([Bourguignon & Lawson 81, Theorem A](#BourguignonLawson81), [Kobayashi, Ohnita & Takeuchi 86, Theorem 1.3.](#KobayashiOhnitaTakeuchi86), [Kawai 86](#Kawai86), [Chiang 13, Theorem 3.1.9](#Chiang13))

[[James Simons]] presented this result without written publication during a symposium on _Minimal Submanifolds and Geodesics_ in Tokyo in September 1977.

\begin{theorem}
If for a [[compact]] $n$-dimensional smooth submanifold of $\mathbb{R}^{n+1}$ a $\varepsilon\gt 0$ exists, so that:
$$
\frac{2}{n-2}\varepsilon
\lt\lambda_i
\leq\varepsilon
$$
at every point for all principal curvatures $\lambda_i$, then all weakly stable Yang-Mills connections on it are flat.
\end{theorem}

([Kawai 86](#Kawai86))

This includes the previous theorem as a special case.

\begin{theorem}
Every weakly stable $\operatorname{SU}(2)$- or $\operatorname{SU}(3)$-Yang-Mills field on $S^4$ is either [[D=4 Yang-Mills theory|selfdual]] or [[D=4 Yang-Mills theory|anti-selfdual]].
\end{theorem}

([Bourguignon & Lawson 81, Theorem B](#BourguignonLawson81), [Chiang 213, Theorem 3.1.10](#Chiang13))

\begin{theorem}
All weakly stable Yang-Mills connections on a [[compact]] [[orientable]] [[homogeneous space|homogeneous]] Riemannian $4$-manifold with [[structure group]] $\operatorname{SU}(2)$ are either [[D=4 Yang-Mills theory|selfdual]], [[D=4 Yang-Mills theory|antiselfdual]] or reduce to an abelian field.
\end{theorem}

([Bourguignon & Lawson 81, Theorem B'](#BourguignonLawson81), [Chiang 213, Theorem 3.1.11](#Chiang13))

## Yang-Mills-unstable manifolds

A [[compact]] [[Riemannian manifold]], for which no [[principal bundle]] over it (with a [[compact]] [[Lie group]] as [[structure group]]) has a stable Yang-Mills connection is called _Yang-Mills-unstable_ (or _YM-unstable_). For example, the spheres $S^n$ are Yang–Mills-unstable for $n\geq 5$ because of the above result from [[James Simons]]. A Yang–Mills-unstable manifold always has a vanishing second [[Betti number]].

([Kobayashi, Ohnita & Takeuchi 86, Theorem 2.17.](#KobayashiOhnitaTakeuchi86))

Central for the proof is that the infinite [[complex projective space]] $\mathbb{C}P^\infty$ is the classifying space $\operatorname{BU}(1)$ as well as the [[Eilenberg-MacLane space]] $K(\mathbb {Z} ,2)$. Hence principal $\operatorname{U}(1)$-bundles over a Yang–Mills-unstable manifold $X$ (but even more generally every [[CW complex]]) are classified by its second [[cohomology]] (with integer coefficients):

$$
\operatorname{Prin}_{\operatorname{U}(1)}(X)
\cong[X,\operatorname{BU}(1)]
=[X,K(\mathbb{Z},2)]
=H^2(X,\mathbb{Z}).
$$

On a non-trivial principal $\operatorname{U}(1)$-bundles over $X$, which exists for a non-trivial second cohomology, one could construct a stable Yang–Mills connection.

Open problems about Yang-Mills-unstable manifolds include:

* Is a [[simply connected]] compact simple [[Lie group]] always Yang-Mills-unstable?

* Is a Yang-Mills-instable simply connected compact Riemannian manifold always harmonically instable? Since $S^n\times S^1$ for $n\geq 5$ is Yang-Mills-unstable, but not harmonically instable, the condition to be simply connected cannot be dropped.

## See also

* [[stable Yang-Mills-Higgs pair]]

## References

* {#BourguignonLawson81} Jean-Pierre Bourguignon and H. Blaine Lawson Jr., _Stability and Isolation Phenomena for Yang-Mills Fields_ (March 1981), Communications in Mathematical Physics **79**, pp. 189–230, [doi:10.1007/BF01942061](https://doi.org/10.1007/BF01942061)
* {#KobayashiOhnitaTakeuchi86} S. Kobayashi, Y. Ohnita and M. Takeuchi, _On instability of Yang-Mills connections_ (1986), Mathematische Zeitschrift **193**, pp. 165–189, [doi:10.1007/BF01174329](https://link.springer.com/article/10.1007/BF01174329)
* {#Kawai86} Shigeo Kawai, _A remark on the stability of Yang-Mills connections_, Kodai Mathematical Journal **9**, pp. 117–122, [doi:10.2996/kmj/1138037154](https://doi.org/10.2996/kmj/1138037154)
* {#Chiang13} Yuan-Jen Chiang, _Developments of Harmonic Maps, Wave Maps and Yang-Mills Fields into Biharmonic Maps, Biwave Maps and Bi-Yang-Mills Fields_, [ISBN 978-3034805339](https://link.springer.com/book/10.1007/978-3-0348-0534-6)

See also:

* Wikipedia, _[stable Yang-Mills connection](https://en.wikipedia.org/wiki/Stable_Yang%E2%80%93Mills_connection)_

[[!redirects stable Yang-Mills connections]]
[[!redirects stable YM connection]]
[[!redirects stable YM connections]]

[[!redirects weakly stable Yang-Mills connection]]
[[!redirects weakly stable Yang-Mills connections]]
[[!redirects weakly stable YM connection]]
[[!redirects weakly stable YM connections]]

[[!redirects Yang-Mills-unstable manifold]]
[[!redirects YM-unstable manifold]]