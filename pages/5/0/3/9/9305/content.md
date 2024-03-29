
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Small objects
+--{: .hide}
[[!include compact object - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #DeformationContext}
###### Definition

A **[[deformation context]]** is an [[(∞,1)-category]] $\mathcal{Y}$ such that

1. it is a [[presentable (∞,1)-category]];

1. it contains a [[terminal object in an (∞,1)-category|terminal object]]

together with a [[set]] of [[objects]] $\{E_\alpha \in Stab(\mathcal{Y})\}$ in the [[stabilization]] of $\mathcal{Y}$.

=--

This is ([Lurie, def. 1.1.3](#Lurie)) together with the assumption of a terminal object stated (and later implicialy used) on p.9.

+-- {: .num_remark}
###### Remark

Definition \ref{DeformationContext} is meant to be read as follows:

First, we think of $\mathcal{Y}$ as an [[opposite (∞,1)-category]] of [[pointed object|pointed]] spaces in some [[higher geometry]]. The point is the [[initial object]] in $\mathcal{Y}^{op}$ which is the terminal object in $\mathcal{Y}$. 

Then we think of the formal duals of the objects $\{E_\alpha\}_\alpha$ as a set of generating [[infinitesimally thickened points]].

=--

The following construction generates the "[[jets]]" induced by the generating infinitesimally thickened points.

+-- {: .num_defn #SmallObjects}
###### Definition

Given a [[deformation context]] $(\mathcal{Y}, \{E_\alpha\}_\alpha)$, we say

* a [[morphism]] in $\mathcal{Y}$ is an **elementary morphism** if it is the [[homotopy fiber]] to a map into $\Omega^{\infty -n}E_\alpha$ for some $n \in \mathbb{Z}$ and some $\alpha$;

* a morphism is a **small morphism** if it is the composite of [[finite set|finitely]] many elementary morphisms.

We write

$$
  \mathcal{Y}^{inf} \hookrightarrow \mathcal{Y}
$$

for the full [[sub-(∞,1)-category]] on those objects $A$ for which the essentially unique map $A \to *$ is small.

=--

([Lurie, def. 1.1.8](#Lurie))

## Related concepts

* [[deformation theory]]

* [[formal moduli problem]]

* [[Lie differentiation]]

* [[model structure for L-infinity algebras]]

## References

* [[Jacob Lurie]], _[[Formal moduli problems]]_
 {#Lurie}

[[!redirects deformation contexts]]

