
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In traditional mathematics and [[set theory]], the [[category]] [[Set]] of all [[sets]] is the archetypical [[topos]]. However, in [[predicative mathematics]] with its notion of sets, these do not form a topos since they do not satisfy the [[powerset axiom]]. In [[constructive mathematics]], we may be *weakly* predicative and *almost* form a topos; the resulting weaker structure which [[Bishop sets]] (for example) form is a  _predicative topos_ ([van den Berg](#vdBerg)).  

## Definition

There are various notions of predicative topos in the literature (see references below); here we discuss the notion advocated by [[Benno van den Berg]]. 

+-- {: .num_defn }
###### Definition

A **predicative topos** is a [[ΠW-pretopos]] satisfying [[WISC]].

=--

This is ([van den Berg, def. 6.1](#vdBerg)), who however calls what we call WISC the "axiom of multiple choice", and the usual [[axiom of multiple choice]] the "strong axiom of multiple choice".


+-- {: .num_remark }
###### Remark

In other words, the [[axiom of multiple choice]] appears in different strengths in the literature; see at _[[WISC]]_. Accordingly there is the notion of strong/weak predicative topos if it satisfies the strong/weak version of this axiom; van den Berg's notion of predicative topos is the weak version.

=--

Note that an impredicative [[elementary topos]] is *not* necessarily a predicative topos in this sense.  A topos is always a $\Pi$-pretopos, and if it has an [[NNO]] then it is a $\Pi W$-pretopos, but it need not satisfy WISC.

A different approach to a notion of predicative topos is to assert, rather than a weak choice principle, the existence of some categorical version of [[higher inductive types]].  But this would also exclude some elementary toposes.


## Properties

+-- {: .num_theorem }
###### Theorem

A [[category]] of [[internal sheaves]] over an [[internal site]] in a predicative topos is again a predicative topos.

=--

This is ([van den Berg, theorem 7.5](#vdBerg)), using [vdBerg-Moerdijk, theorem 4.21](#vdBergMoerdijk)


## Examples

+-- {: .num_theorem }
###### Theorem

The [[category]] of [[Bishop sets]] in [[Martin-Löf dependent type theory]] is a [strong predicative topos.

=--

This is ([van den Berg, theorem 6.2](#vdBerg)), based on ([Moerdijk-Palmgren 99, section 7](#MoerdijkPalmgren99)) and ([Moerdijk-Palmgren 00, section 10](#MoerdijkPalmgren00)).

Not every [[topos]] is a predicative topos, or even every $Set$-topos (i.e. a topos with a [[geometric morphism]] to the category $Set$, see ([Roberts 2015](#Roberts15))), but every _[[Grothendieck topos]]_ -- a [[bounded geometric morphism|bounded]] $Set$-topos -- is.



## References

The goal of formulating a notion of _predicative topos_ was stated and pursued in a series of articles containing

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Wellfounded trees in categories_ (1999) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.44.6700))
 {#MoerdijkPalmgren99}

* [[Ieke Moerdijk]], [[Erik Palmgren]], _Type Theories, Toposes and Constructive Set Theory: Predicative Aspects of AST_ (2000) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.34.8934))
 {#MoerdijkPalmgren00}
 
* [[Benno van den Berg]], [[Ieke Moerdijk]], _Aspects of predicative algebraic set theory III: Sheaves. Proceedings of the London Mathematical Society., (2012) ([arXiv:arXiv:0912.1242]())
 {#vdBergMoerdijk}

The definition then appears in

* [[Benno van den Berg]], _Predicative toposes_ ([arXiv:1207.0959](http://arxiv.org/abs/1207.0959))
 {#vdBerg}

Discussion of the [[category of sets]] as a $\Pi$-W-topos when formalized via [[h-sets]] in [[homotopy type theory]] is in 

* [[Egbert Rijke]], [[Bas Spitters]], _Sets in homotopy type theory_ ([arXiv:1305.3835](http://arxiv.org/abs/1305.3835))

A non-example constructed via the internal logic of an unbounded $Set$-topos is given in

* {#Roberts15} [[David Roberts]], _The weak choice principle WISC may fail in the category of sets_, [Studia Logica](http://link.springer.com/journal/11225) Volume 103 (2015) Issue 5, pp 1005-1017, doi:[10.1007/s11225-015-9603-6](http://dx.doi.org/10.1007/s11225-015-9603-6) [arXiv:1311.3074](http://arxiv.org/abs/1311.3074)



[[!redirects predicative topos]]
[[!redirects predicative topoi]]
[[!redirects predicative toposes]]

[[!redirects strong predicative topos]]
[[!redirects strong predicative topoi]]
[[!redirects strong predicative toposes]]

[[!redirects predicativity]]

