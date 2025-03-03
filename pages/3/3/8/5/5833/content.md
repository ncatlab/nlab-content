
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


# The Riesz representation theorems
* table of contents
{: toc}

## Summary

There are various related theorems in [[functional analysis]] and [[measure theory]] stating, under appropriate conditions, that the [[dual vector space|topological linear duals]] of various familiar [[Banach spaces]] (or something similar) are other familiar Banach spaces.  Most of these are due in part to [[Frigyes Riesz]], and many of them are named after him.  Here we will consider them all together.

Throughout, we use notation for [[integrals]] in which unnecessary '$\mathrm{d}$'s are dropped; see the discussion on notation at _[[measure space]]_.


## $C_c^{{*}{+}} = \overline{RM}^+$

Let $X$ be a [[locally compact Hausdorff space]].  Let $C_c(X)$ be the space of [[continuous functions]] on $X$ (valued in the [[complex numbers]]) with [[compact subset|compact]] [[support]]; make $C_c(X)$ into a [[locally convex space]] with the topology of [[uniform convergence topology|uniform convergence on compact subsets]]; the [[dual vector space]] $C_c(X)*$ of this is (of course) the space of [[continuous map|continuous]] [[linear functional]]s on $C_c(X)$; and the [[positive cone]] $C_c(X)^{{*}{+}}$ of this is the space of [[positive linear functional]]s on $C_c(X)$.  Let $RM(X)$ be the space of [[finite measure|finite]] [[Radon measure]]s on $X$; make $RM(X)$ into a [[Banach space]] with the [[total variation]] norm; the [[extended positive cone]] $\overline{RM(X)}^+$ of this is the space of [[positive measure|positive]] Radon measures on $X$.  [[integral|Integration]] gives a map from $\overline{RM(X)}^+$ to $C_c(X)^{{*}{+}}$:
$$ \mu \mapsto (f \mapsto \int_X f \mu) .$$

+-- {: .num_theorem #Cc}
###### Theorem (Riesz)
This map is a [[homeomorphism]]:
$$ C_c(X)^{{*}{+}} \cong \overline{RM(X)}^+ .$$
=--


## $C_0^* = RM$

Let $X$ be a [[locally compact Hausdorff space]].  Let $C_0(X)$ be the space of [[continuous functions]] on $X$ (valued in the [[complex numbers]]) on the [[one-point compactification]] of $X$ (so vanishing 'at infinity'); make $C_0(X)$ into a [[Banach space]] with the [[supremum norm]].  Let $RM(X)$ be the space of [[finite measure|finite]] [[Radon measure]]s on $X$; make $RM(X)$ into a [[Banach space]] with the [[total variation]] norm.  [[integral|Integration]] gives a map from $RM(X)$ to the [[dual vector space]] $C_0(X)^*$ of $C_0(X)$:
$$ \mu \mapsto (f \mapsto \int_X f d\mu) .$$

+-- {: .num_theorem #C0}
###### Theorem (Riesz--Markov)
This map is an [[isometric isomorphism]]:
$$ C_0(X)^* \cong RM(X) .$$
=--


## $L_1^* = L_0$


## $L_p^* = L_{1 - p}$


## $H^* = \bar{H}$


## $L_0^* = BA$

## Related concepts

* [[GNS construction]]


## References

A proof of Theorem \ref{Cc} in [[constructive mathematics]] (in the case where $X$ is a [[compactum]]) is given in

* [[Thierry Coquand]], [[Bas Spitters]], _Integrals and Valuations_ ([arXiv:0808.1522](http://arxiv.org/abs/0808.1522))


[[!redirects Riesz representation theorem]]
[[!redirects Riesz representation theorems]]
