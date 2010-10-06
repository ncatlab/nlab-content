#Definition#

A [[functor]] $F :  C \to D$ is **continuous** if it preserves all small ([[weighted limit|weighted]]) [[limit]]s that exist in $C$, i.e. if for 
every [[small category]] [[diagram]] $A : E \to C$ in $C$ there is an isomorphism

$$
  F(\lim A) \simeq \lim (F\circ A)
  \,.
$$

Since all limits can be obtained from (small) [[product]]s and binary [[equalizer]]s, it follows that a functor is continuous if and only if it preserves all products and all binary equalizers.

#Relation to other concepts#


##Relation to adjoint functors##

The [[adjoint functor theorem]] states that any continuous functor between [[complete category|complete]] categories has a [[adjoint functor|left adjoint]] if it satisfies a certain 'small solution set' criterion.

##Relation to exact functors ##

If $C$ has finite [[limit]]s, then functors commuting 
with these _finite_ limits are precisely what are
called left [[exact functor]]s.


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

2. H. Bass in his treatment of [[K-theory]] uses the older term 'right continuous functor' for the dual notion of [[cocontinuous functor]] in a version which is [[additive functor|additive]]. If the domain of an additive functor which commutes with direct sums is a [[cocomplete category]], then the functor automatically has [[adjoint functor|right adjoint]]. Following this fact, some people in ring theory and noncommutative geometry use the simple term 'continuous functor' for a functor with a right adjoint (even if the domain [[abelian category]] is not cocomplete). In general, of course, this is just a bit more than *co*continuous in the standard sense.

+--{.query}
Left I could understand, but right?  ---Toby

The way I rewrote it explains it. It is unfortunate that the Eilenberg-Watts theorem treated in Bass was using only right adjoint functors so later they dropped word right. -- Zoran

Thanks.  ---Toby
=--