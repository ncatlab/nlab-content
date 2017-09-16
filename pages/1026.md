A [[functor]] $F :  C \to D$ is **continuous** if it preserves all small ([[weighted limit|weighted]]) [[limit]]s that exist in $C$, i.e. if for 
every [[small category]] [[diagram]] $A : E \to C$ in $C$ there is an isomorphism

$$
  F(\lim A) \simeq \lim (F\circ A)
  \,.
$$


(... say more ...)

The [[adjoint functor theorem]] states that any continuous functor between [[complete category|complete]] categories has a [[adjoint functor|left adjoint]] if it satisfies a certain 'small solution set' criterion.

#Examples#

* The archetypical example is the [[Set]]-valued [[hom-functor]]: its continuity in both arguments is indeed equivalent to the very definition of [[limit]]: for 
$F : D^{op} \to C$ a diagram and $c \in C$, the covariant [[hom-functor]] $Hom_C(c,-) : C \to Set$ satisfies by definition of [[limit]]
$$
  Hom_C(c, \lim F)
  \simeq
  \lim Hom(c,F(-))
  \,.
$$

# Warnings #

1. Topologists sometimes use "continuous functor" to mean a functor [[enriched category|enriched]] over [[Top]], since a functor between topologically enriched categories is enriched iff its actions on hom-spaces are continuous functions.

2. H. Bass in his treatment of K-theory (and more recently A. Rosenberg and some others) use "continuous functor" in the sense "[[additive category|additive]] functor having right adjoint". 

+--{.query}
Left I could understand, but right?  ---Toby
=--