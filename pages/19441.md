
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Monoidal categories
+-- {: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

* table of contents
{: toc}


## Idea

In [[functional analysis]], the _inductive tensor product_ is a kind of [[tensor product]] suitable for [[topological vector spaces]].

Specifically, the **inductive tensor product** $E\otimes_i F$ of a pair of [[topological vector spaces]] $E$, and $F$ is the target of the [[universal construction|universal]] separately [[continuous function|continuous]] [[bilinear map]] $E\times F \to E\otimes_i F$.

## Definition

Given a pair of [[locally convex topological vector spaces]] (lctvs) $E$ and $F$, the inductive tensor product is the locally convex [[topological vector space|tvs]] $E\otimes_i F$ with underlying plain [[vector space]] the algebraic [[tensor product of vector spaces]], and equipped with the finest locally convex linear [[topological space|topology]] such that $E\times F \to E\otimes_i F$ is separately [[continuous function|continuous]], where $E\times F$ has the [[product topology]].

Compare this to the (pre-completed) projective tensor product $\otimes_p$, which is equipped with the finest locally convex linear topology such that the canonical map from $E\times F$ is _jointly_ continuous.

Sometimes one will wish to consider this tensor product in the category of _complete_ lctvs, and so the result is the topological completion $E\overline{\otimes} F$ of $E\otimes_i F$ (eg by adding in the limits of Cauchy [[nets]]), which is the analogue of the (complete) projective tensor product $\widehat{\otimes}$.

## Properties

+-- {: .num_prop #whenSeparatelyCtsBilinearMapsAreCts}
###### Proposition

Let $E$ and $F$ be metrizable tvs, and $T\colon E\times F \to G$ a separately continuous bilinear function. If one of the following conditions is true

1. $E$ is a Baire space (for example, _completely_ metrizable)
1. $E$ is a [[barreled topological vector space]] (eg is a [[Frechet space]]) and $G$ is locally convex.

then $T$ is jointly continuous.

=--

For a proof see ([Schaefer-Wolff 1999](#Schaeffer-Wolff), corollary to Theorem 5.1)

Notice that there are canonical comparison maps $E\otimes_i F \to E\otimes_p F$ and $E\overline{\otimes} F \to E \widehat{\otimes} F$.

+-- {: .un_theorem}
###### Theorem

Let $E$ and $F$ be metrizable lctvs, and assume one of the conditions in Proposition \ref{whenSeparatelyCtsBilinearMapsAreCts} holds. Then the comparison maps from the inductive tensor products to the projective tensor products are isomorphisms.

=--

+-- {: .un_prop}
###### Corollary

If $E$ and $F$ are [[Fréchet spaces]], then $E\overline{\otimes} F \stackrel{\sim}{\to} E \widehat{\otimes} F$.

=--

Hence for Banach spaces and Hilbert spaces the inductive tensor product also agrees with the projective tensor product. It is for this reason that one can define [[locally convex algebra]]s with the inductive tensor product, as this reduces the the usual jointly-continuous multiplication for Banach algebras, $C^*$-algebras etc.



## Related pages

* [[spatial tensor product]]
* [[tensor product of Banach spaces]]

## References

* {#Schaeffer-Wolff} Schaeffer, Wolff, _Topological Vector Spaces_, Graduate Texts in Mathematics **3** (1999) Springer.
