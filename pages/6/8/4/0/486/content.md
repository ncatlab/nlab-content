A **pretopos** is a [[coherent category]] which is both [[extensive category|extensive]] and [[exact category|exact]].  (See [[familial regularity and exactness]] for why extensivity and exactness deserve to be considered together.)

Frequently one is especially interested in pretoposes having additional properties, such as:

* A _Heyting pretopos_, is a pretopos which is also a [[Heyting category]].
* A _$\Pi$-pretopos_ is a pretopos which is also a [[locally cartesian closed category]].  A $\Pi$-pretopos is automatically Heyting.
* A _$W$-pretopos_ is a pretopos which has [[inductive object]]s (initial [[algebra of a functor|algebras]] of [[polynomial]] [[endofunctor]]s), most famously a [[natural numbers object]].
* A _$\Pi$-$W$-pretopos_ is of course a pretopos that has both $\Pi$ and $W$; these are widely studied as frameworks for [[predicativism]].
* A _topos_ is a pretopos that has a [[subobject classifier]].  A topos is automatically a $\Pi$-pretopos.
* A _$W$-topos_ is of course a topos that has $W$; these are widely studied as frameworks for [[constructivism]].

Like any coherent (or Heyting) category, a (Heyting) pretopos has an [[internal logic]].  Extensivity and exactness make a Heyting pretopos a very set-like category.  One can say imprecisely that it has "all the good first-order properties of a [[topos]];" that is, all the good properties except the existence of exponentials and power objects.  Therefore, pretoposes (especially Heyting, $\Pi$, and/or $W$ ones) are related to [[predicativism|predicative mathematics]] in a way similar to how toposes are related to non-predicative [[constructivism|constructive mathematics]].

+--{.query}
I changed 'intuitionistic mathematics' to 'non-predicative constructive mathematics'.  While, for example, 'IZF' and 'CZF' are contrasted so that the latter is predicative while the former is not, 'intuitionistic mathematics' can also mean the mathematics practised by Brouwer\'s intellectual descendants in the Netherlands, which is predicative (and in fact does not even accept $\Pi$ in general).  &#8212;Toby
=--

A pretopos is necessarily [[balanced category|balanced]], but while it has coproducts and coequalizers of equivalence relations, it need not have all finite colimits.  However, if it has countable pullback-stable unions of subobjects, then any internal binary relation generates an equivalence relation and therefore has a quotient, so we can construct arbitrary coequalizers and thus arbitrary finite colimits.  And we can perform an "internal" version of this argument in a $\Pi$-pretopos with a [[natural numbers object|NNO]], such as a $\Pi$-$W$-pretopos.

## Infinitary pretoposes ##

An **infinitary pretopos** is an [[coherent category|infinitary coherent category]] which is both [[extensive category|infinitary extensive]] and [[exact category|exact]].  Giraud's theorem says that infinitary pretoposes with small generating sets are the same as [[Grothendieck topos|Grothendieck toposes]], and in particular are [[topos|toposes]].