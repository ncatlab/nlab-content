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

The notion of _enriched Lawvere theory_ is a generalization of [[Lawvere theories]] to the setting of [[enriched categories]].

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

* [[John Power]], _Enriched Lawvere theories_, [tac](http://www.tac.mta.ca/tac/volumes/6/n7/6-07abs.html)

* [[Koki Nishizawa]], [[John Power]], _Lawvere theories enriched over a general base_. Journal of Pure and Applied Algebra **213**, Issue 3, March 2009, Pages 377--386. ([pdf](https://www.sciencedirect.com/science/article/pii/S0022404908001485)), 
MR2477057, Zbl:1158.18003,
doi:[10.1016/j.jpaa.2008.07.009](http://dx.doi.org/10.1016/j.jpaa.2008.07.009).

* [[Sam Staton]], _Freyd categories are enriched Lawvere theories_, [pdf](http://www.cs.ox.ac.uk/people/samuel.staton/papers/freyd-lawvere-2014.pdf)

* Rory B. B. Lucyshyn-Wright, _Enriched algebraic theories and monads for a system of arities_, ([arXiv:1511.02920](https://arxiv.org/abs/1511.02920)).

* [[Stephen Lack]], [[John Power]], _Gabriel-Ulmer Duality and Lawvere Theories Enriched over a General Base_, [pdf](http://maths.mq.edu.au/~slack/papers/jfp.pdf)

* [[Richard Garner]], [[John Power]], _An enriched view on the extended finitary monad--Lawvere theory correspondence_, ([ arXiv:1707.08694](https://arxiv.org/abs/1707.08694))