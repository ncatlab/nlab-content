A **pretopos** is a [[coherent category]] which is both [[extensive category|extensive]] and [[exact category|exact]].  (See [[familial regularity and exactness]] for why extensivity and exactness deserve to be considered together.)


Frequently one is especially interested in pretoposes having additional properties, such as:

* A _Heyting pretopos_, is a pretopos which is also a [[Heyting category]]; a _Boolean pretopos_ is a pretopos which is also a [[Boolean category]].  These are suitable as frameworks for [[predicative mathematics]], respectively with [[intuitionistic logic|intuitionistic]] or [[classical logic|classical]] logic.
* A _$\Pi$-pretopos_ is a pretopos which is also a [[locally cartesian closed category]].  A $\Pi$-pretopos is automatically a Heyting pretopos.
* A _$W$-pretopos_ is a pretopos which has (locally) [[inductive object]]s (initial [[algebra for an endofunctor|algebras]] for [[polynomial]] [[endofunctor]]s), most famously a [[natural numbers object]].
* A _$\Pi$-$W$-pretopos_ is of course a pretopos that has both $\Pi$ and $W$; these are widely studied as frameworks for [[predicative mathematics]] in the weaker constructive sense.
* A _topos_ is a pretopos that has [[power object]]s.  A topos is automatically a $\Pi$-pretopos; conversely, a $\Pi$-pretopos is a topos iff it has a [[subobject classifier]], and a Boolean $\Pi$-pretopos is always a topos.
* A _$W$-topos_ is of course a topos that has $W$; it is sufficient that the topos have a [[natural numbers object]] (see van den Berg & Moerdijk), so this is often called a _topos with NNO_.  These are widely studied as frameworks for (non-predicative) [[constructive mathematics]], while a [[Boolean topos|Boolean]] $W$-topos is a framework for ordinary classical mathematics (without the [[axiom of choice]], of course, unless you additionally assume the topos satisfies choice.)


Like any coherent (or Heyting) category, a (Heyting) pretopos has an [[internal logic]].  Extensivity and exactness make a Heyting pretopos a very set-like category.  One can say imprecisely that it has "all the good first-order properties of a [[topos]]", meaning not that it has those properties that can be expressed in elementary terms (which is false) but that it has those properties that (unlike exponential and power objects) correspond to first-order reasoning in ordinary mathematics.  Therefore, pretoposes (especially Heyting, $\Pi$, and/or $W$ ones) are related to predicative constructive mathematics in a way similar to how toposes are related to non-predicative constructive mathematics.


A pretopos is necessarily [[balanced category|balanced]], but while it has coproducts and coequalizers of equivalence relations, it need not have all finite colimits.  However, if it has countable pullback-stable unions of subobjects, then any internal binary relation generates an equivalence relation and therefore has a quotient, so we can construct arbitrary coequalizers and thus arbitrary finite colimits.  And we can perform an "internal" version of this argument in a $\Pi$-pretopos with a [[natural numbers object|NNO]], such as a $\Pi$-$W$-pretopos.


## Infinitary pretoposes ##

An **infinitary pretopos** is an [[coherent category|infinitary coherent category]] which is both [[extensive category|infinitary extensive]] and [[exact category|exact]].  Giraud's theorem says that infinitary pretoposes with small generating sets are the same as [[Grothendieck topos|Grothendieck toposes]], and in particular are [[topos|toposes]].


## References

*  Benno van den Berg & Ieke Moerdijk (2008-09-25); _$W$-types in sheaves_; [vdBM_Wtypes.ps/pdf](http://www.phil.cmu.edu/projects/ast/Papers/)


[[!redirects Heyting pretopos]]
[[!redirects Boolean pretopos]]
[[!redirects Pi-pretopos]]
[[!redirects Π-pretopos]]
[[!redirects W-pretopos]]
[[!redirects Pi-W-pretopos]]
[[!redirects ∞-W-pretopos]]
[[!redirects infinitary pretopos]]
