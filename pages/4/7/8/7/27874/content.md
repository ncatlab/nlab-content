
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

  A [[Hurewicz fibration]] $f \colon X \to Y$ has *sectional category $ \le n $* if there is an [[open cover]] of $Y$ by at most $n$ sets $U\subseteq Y$ equipped with [[local section|local sections]] $s\colon U\to X$ of $f$. The *sectional category* or *Schwarz genus* of $f$ is the least $n$ such that $X$ has sectional category $\le n$.

 =--

+-- {: .num_remark}
###### Remark

  As with the [[Lusternik–Schnirelmann category]], parts of the literature use an alternative definition, according to which the sectional category is one _less_ than the definition used here.

 =--

+-- {: .num_remark}
###### Remark

  There are several inequivalent definitions of sectional category for arbitrary maps: [James (1978: 342)](#James1978) simply extends the definition to any space $f \colon X \to Y$ over $Y$, whereas e.g. [Moraschini–Murillo (2016: 23)](#MoraschiniMurillo2016) replace local sections in the definition by local sections in the [[homotopy category]] (which is equivalent for Hurewicz fibrations by the [[homotopy lifting property]]).

 =--

## Properties
  * If $f \colon X \to Y$ is a fibration with $Y$ [[paracompact space|paracompact]] [[Hausdorff space|Hausdorff]] (so that every open cover of $Y$ is [[numerable cover|numerable]]), then $f$ has sectional category $\le n$ iff the $n$-fold [[join of topological spaces|fiberwise join]] $f^{\star n} \colon X \star_Y \dots \star_Y X \to Y$ (with Milnor’s topology) has a [[global section]].

  * For path-connected spaces $X$ and $x_0\in X$, the [[Lusternik–Schnirelmann category]] of $X$ is exactly the sectional category of the path fibration $ev_1 \colon \{\gamma \in X^I : \gamma(0)=x_0\}\to X$.

## References

  * {#James1978} [[Ioan James|I.M. James]], _On category, in the sense of Lusternik–Schnirelmann_, Topology **17** 4 (1978) 331–348 &lbrack;[doi:10.1016/0040-9383(78)90002-2](https://doi.org/10.1016/0040-9383(78%2990002-2)&rbrack;

  * {#MoraschiniMurillo2016} Marco Moraschini, Aniceto Murillo, _Abstract sectional category in model structures on topological spaces_, Topology and its Applications **199** (2019) 23–31 &lbrack;[doi:10.1016/j.topol.2015.12.002](https://doi.org/10.1016/j.topol.2015.12.002)&rbrack;

[[!redirects Schwarz genus]]