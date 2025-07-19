
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



\tableofcontents

## Definition 

+-- {: .num_defn}
###### Definition

  A [[topological space]] $X$ has *Lusternik–Schnirelmann category $ \le n $* if there is an [[open cover]] of $X$ by at most $n$ sets for which the inclusion maps $ U \hookrightarrow X $ are [[nullhomotopy|nullhomotopic]]. The *Lusternik–Schnirelmann category* or *LS-category* of $X$ is the least $n$ such that $X$ has LS-category $\le n$.

 =--

+-- {: .num_remark}
###### Remark

  Parts of the literature use an alternative definition, according to which the LS-category is one _less_ than the definition used here.

 =--

## Properties
  * The LS-category is a [[homotopy invariance|homotopy invariant]]: if $ f\colon X \to Y $ is a [[homotopy equivalence]] and $ \{ U_\alpha \}_{0 \le \alpha \lt n} $ an open cover of $Y$ such that the inclusions $i_\alpha \colon U\hookrightarrow Y$ are nullhomotopic, then $\{f^{-1}(U_\alpha)\}_{0\le\alpha \lt n}$ is an open cover for which the each inclusion $f^{-1}(U_\alpha) \hookrightarrow X$ is nullhomotopic, since its composition with $f$ factors through the nullhomotopic map $i_\alpha$.

  * A space has LS-category $0$ iff it is [[empty space|empty]], and LS-category $1$ iff it is [[contractible space|contractible]]. For [[discrete space|discrete spaces]] the LS-category is equal to the [[cardinality]]. Any [[suspension]] has LS-category $2$; in particular the [[sphere]] $S^n$ has LS-category $2$ if $n \ge 0$.


  * For path-connected spaces $X$ and $x_0\in X$, the LS-category of $X$ is exactly the [[sectional category]] of the path fibration $ev_1 \colon \{\gamma \in X^I : \gamma(0)=x_0\}\to X$.

## References

  * Wikipedia, *[Lusternik-Schnirelman category](https://en.wikipedia.org/wiki/Lusternik%E2%80%93Schnirelmann_category)*

  * {#James1978} [[Ioan James|I.M. James]], _On category, in the sense of Lusternik–Schnirelmann_, Topology **17** 4 (1978) 331–348 &lbrack;[doi:10.1016/0040-9383(78)90002-2](https://doi.org/10.1016/0040-9383(78%2990002-2)&rbrack;

  * {#Fox1941} [[Ralph Fox|Ralph H. Fox]], _On the Lusternik-Schnirelmann category_, Annals of Mathematics **42** 2 (1941) 333–370 &lbrack;[doi:10.2307/1968905](http://doi.org/10.2307/1968905)&rbrack;

[[!redirects Lusternik–Schnirelmann category]]
[[!redirects Lusternik–Schnirelmann categories]]
[[!redirects Lusternik–Schnirelmann categories]]

[[!redirects Lyusternik–Schnirelmann category]]
[[!redirects Lyusternik–Schnirelmann category]]
[[!redirects Lyusternik–Schnirelmann categories]]
[[!redirects Lyusternik–Schnirelmann categories]]



