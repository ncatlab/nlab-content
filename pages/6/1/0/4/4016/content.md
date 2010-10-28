
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Definition

A [[cardinal number]] $\kappa$ is **measurable** if some (hence any) set of cardinality $\kappa$ admits a two-valued [[measure]] which is $\kappa$-additive, or equivalently an [[ultrafilter]] which is $\kappa$-complete.

## Properties

Any measurable cardinal is necessarily [[inaccessible cardinal|inaccessible]], and in fact much larger than the smallest inaccessible.  In fact, if $\kappa$ is measurable, then there is a $\kappa$-complete ultrafilter $\mathcal{U}$ on $\{\lambda | \lambda \lt \kappa\}$ which contains the set $\{\lambda | \lambda \lt \kappa$ and $\lambda$ is inaccessible $\}$.  In particular, there are $\kappa$ inaccessible cardinals smaller than $\kappa$.

It follows from this that the existence of any measurable cardinals cannot be proven in [[ZFC]], since the existence of inaccessible cardinals cannot be so proven.  Thus measurable cardinals are a kind of [[large cardinal]].  They play an especially important role in large cardinal theory, since any measurable cardinal gives rise to an [[elementary embedding]] of the universe $V$ into some submodel $M$ (such as an [[ultrapower]] by a countably-complete ultrafilter), while the "critical point" of any such embedding is necessarily measurable.

Measurable cardinals are sometimes said to mark the boundary between "small" large cardinals (such as inaccessibles, [[Mahlo cardinal]]s, and [[weakly compact cardinal]]s) and "large" large cardinals (such as [[strongly compact cardinal]]s, [[supercompact cardinal]]s, and so on).

## In category theory

The existence or nonexistence of measurable cardinals can have noticeable impacts on [[category theory]], notably in terms of the properties of the category [[Set]].

For instance, the category $Set^{op}$ has a [[small category|small]] [[dense subcategory]] if and only if there does *not* exist a [[proper class]] of measurable cardinals.  Specifically, the subcategory of all sets of cardinality $\lt\lambda$ is dense in $Set^{op}$ precisely when there are no measurable cardinals larger than $\lambda$.  In particular, the full subcategory on $\mathbb{N}$ is dense in $Set^{op}$ precisely when there are no measurable cardinals at all.

This is theorem A.5 of Adamek & Rosicky, "Locally presentable and accessible categories."

[[!redirects measurable cardinals]]
