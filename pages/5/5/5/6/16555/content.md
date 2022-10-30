+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contents
* automatic table of contents goes here
{:toc}

## Idea

The notion of _enriched Lawvere theory_ is a generalization of Lawvere theories to the setting of [[enriched categories]].

## Definitions and elementary properties

+-- {: .un_defn}
###### Definition

An **enriched [[Lawvere theory]]** over a [[locally finitely presentable]] $V$-[[enriched category]]&#160;$A$ is a small $V$-[[enriched category]]&#160;$L$ together with a $V$-[[enriched functor]] $J\colon A_f^{op}\to L$
that induces an identity map on the set of objects.
Here $A_f$ denotes the [[full subcategory]] of [[finitely presentable objects]] in&#160;$A$.
The category&#160;$V$ is a locally finitely presentable [[closed symmetric monoidal category]].

=--

+-- {: .un_defn}
###### Definition

An **algebra** over an enriched Lawvere theory is
an object&#160;$X$ in&#160;$A$ equipped with a functor $M\colon L\to V$ whose precomposition with&#160;$J$ is isomorphic to the representable functor of&#160;$X$.

=--

+-- {: .un_defn}
###### Proposition

For the case $A=Set$ the above definition recovers
the usual notion of a [[Lawvere theory]]
and an [[algebra]] over a Lawvere theory.

=--

+-- {: .un_defn}
###### Proposition

The forgetful functor from algebras to&#160;$A$
is a [[finitary enriched monadic functor]] (over&#160;$V$).

=--

+-- {: .un_defn}
###### Proposition

The category of enriched Lawvere theories over&#160;$A$
is equivalent to the category of [[finitary enriched
monads]] over&#160;$A$.
The corresponding $V$-enriched categories of
algebras are also equivalent.

=--

## References

[[Koki Nishizawa]], [[John Power]].
_Lawvere theories enriched over a general base_. Journal of Pure and Applied Algebra **213**, Issue 3, March 2009, Pages 377--386.
MR2477057, Zbl:1158.18003,
doi:[10.1016/j.jpaa.2008.07.009](http://dx.doi.org/10.1016/j.jpaa.2008.07.009).