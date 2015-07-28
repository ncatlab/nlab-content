+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

The concept of **dominance** is a weakening of the concept of [[surjective geometric morphism|surjectivity]] for [[geometric morphism|geometric morphisms]]. It generalizes the concept of a continuous function whose image is a [[dense subspace]] of its codomain in topology.

## Definition

A geometric morphism $f:\mathcal{E}\to\mathcal{F}$ is called _dominant_ if the following equivalent conditions hold:

* The [[direct image]] satisfies: $f_\ast(\emptyset_\mathcal{E})\cong\emptyset_\mathcal{F}$.

* The [[inverse image]] satisfies: from $f^\ast(Z)\cong\emptyset_\mathcal{E}$ follows $Z\cong\emptyset_\mathcal{F}$.

* The [[inverse image]] satisfies: from $f^\ast(Z)\cong\emptyset_\mathcal{E}$ follows $Z\cong\emptyset_\mathcal{F}$ for $Z$ a [[subterminal object]].

## Properties

* A geometric morphism $f:Sh(X)\to Sh(Y)$  between the toposes of sheaves on two topological spaces $X, Y$  is dominant iff the corresponding continuous map $f:X\to Y$  has a [[dense subspace|dense]] image $f(X)$ in $Y$.

* If $f:\mathcal{E}\to\mathcal{F}$ is a surjection (i.e. $f^\ast$ is [[faithful]]) then $f$  is dominant.

* A geometric embedding $i:\mathcal{E}\hookrightarrow\mathcal{F}$ is dominant precisely when it exhibits $\mathcal{E}$ as a [[dense subtopos]].

## Remark

The concept can be generalized to morphisms _in_ a topos $\mathcal{E}$ by calling $f:X\to Y$ dominant iff the induced functor $(\mathcal{E}/Y)/f\to\mathcal{E}/Y$ is dominant, here $f$ is viewed as an object in $\mathcal{E}/Y$.

## Related entries

* [[dense subtopos]]

## References

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, LNM **269** Springer Heidelberg 1972. (pp.429-430, 462)