A **pretopos** is a [[coherent category]] which is both [[extensive category|extensive]] and [[exact category|exact]].  (See [[familial regularity and exactness]] for why extensivity and exactness deserve to be considered together.)

Frequently one is especially interested in pretoposes having additional properties, such as:

* A _Heyting pretopos_, is a pretopos which is also a [[Heyting category]].  Likewise, a _Boolean pretopos_ is a pretopos which is also a [[Boolean category]].
* A _$\Pi$-pretopos_ is a pretopos which is also a [[locally cartesian closed category]].  A $\Pi$-pretopos is automatically Heyting.
* A _$W$-pretopos_ is a pretopos which has (locally) [[inductive object]]s (initial [[algebra of a functor|algebras]] of [[polynomial]] [[endofunctor]]s), most famously a [[natural numbers object]].
* A _$\Pi$-$W$-pretopos_ is of course a pretopos that has both $\Pi$ and $W$; these are widely studied as frameworks for [[predicative mathematics]].
* A _topos_ is a pretopos that has [[power object]]s.  A topos is automatically a $\Pi$-pretopos; conversely, a $\Pi$-pretopos is a topos iff it has a [[subobject classifier]], and a Boolean $\Pi$-pretopos is always a topos.
* A _$W$-topos_ is of course a topos that has $W$; it is sufficient that the topos have a [[natural numbers object]], so this is often called a _topos with NNO_.  These are widely studied as frameworks for (non-predicative) [[constructive mathematics]], while a [[Boolean topos|Boolean]] $W$-topos is a framework for ordinary classical mathematics.  (You still need to add the [[axiom of choice]] to get [[ETCS]].)

Like any coherent (or Heyting) category, a (Heyting) pretopos has an [[internal logic]].  Extensivity and exactness make a Heyting pretopos a very set-like category.  One can say imprecisely that it has "all the good first-order properties of a [[topos]];" that is, all the good properties except the existence of exponentials and power objects.  Therefore, pretoposes (especially Heyting, $\Pi$, and/or $W$ ones) are related to [[predicative mathematics]] in a way similar to how toposes are related to non-predicative constructive mathematics.

+--{.query}
I changed 'intuitionistic mathematics' to 'non-predicative constructive mathematics'.  While, for example, 'IZF' and 'CZF' are contrasted so that the latter is predicative while the former is not, 'intuitionistic mathematics' can also mean the mathematics practised by Brouwer\'s intellectual descendants in the Netherlands, which is predicative (and in fact does not even accept $\Pi$ in general).  &#8212;Toby

Fair enough.  Is a topos with an NNO automatically a $W$-topos? -Mike

_Toby_:  Yes, given a polynomial functor, its initial algebra is a countable direct limit of elements defined on various days, and while without replacement you can\'t take that sort of limit for just any functor (like the covariant powerset functor, which would give the unreachable ordinal $\omega + \omega$ after $\omega$ days and still not have an initial algebra yet), a polynomial functor grows slowly enough (unlike the exponential-growth powerset functor) that you can do the whole thing inside one copy of $\N$.  I should write this up on [[inductive type]], maybe even find a reference ... OK, Google gives me [_$W$-types in sheaves_ (2008-09-25) by Benno van den Berg & Ieke Moerdijk](http://www.phil.cmu.edu/projects/ast/Papers/) (the one with `Wtypes` in the filename, which I haven\'t actually read yet).

=--

A pretopos is necessarily [[balanced category|balanced]], but while it has coproducts and coequalizers of equivalence relations, it need not have all finite colimits.  However, if it has countable pullback-stable unions of subobjects, then any internal binary relation generates an equivalence relation and therefore has a quotient, so we can construct arbitrary coequalizers and thus arbitrary finite colimits.  And we can perform an "internal" version of this argument in a $\Pi$-pretopos with a [[natural numbers object|NNO]], such as a $\Pi$-$W$-pretopos.

## Infinitary pretoposes ##

An **infinitary pretopos** is an [[coherent category|infinitary coherent category]] which is both [[extensive category|infinitary extensive]] and [[exact category|exact]].  Giraud's theorem says that infinitary pretoposes with small generating sets are the same as [[Grothendieck topos|Grothendieck toposes]], and in particular are [[topos|toposes]].