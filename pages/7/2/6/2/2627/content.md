# $2$-rigs
* table of contents
{: toc}

## Idea

A $2$-rig is a [[categorification]] of a [[rig]].  There is more than one inequivalent notion; just as a rig is a multiplicative [[monoid]] whose underlying set also has a notion of addition, so a $2$-rig is a [[monoidal category]] whose underlying category also has a notion of addition, and we can describe this notion of addition in a few different ways.

Note that we don\'t expect a $2$-rig to have additive inverses; by the same argument as in the [[Eilenberg swindle]], they are unreasonable to expect.  However, in a monoidal [[abelian category]], we have as close to additive inverses as is reasonable and so a categorification of a [[ring]].

Compare also the notion of [[rig category]].

## Definitions

1.  A __$2$-rig__ might be an [[Ab-enriched category]] which is [[enriched monoidal category|enriched monoidal]].

2.  A __$2$-rig__ might be an [[additive category]] which is enriched monoidal.

3.  A __$2$-rig__ might be a monoidal category with finite [[coproducts]] such that the monoidal product distributes over the coproducts.

4.  A __$2$-rig__ might be a [[closed monoidal category]] with finite coproducts.

5.  Finally, a __$2$-ring__ is a monoidal [[abelian category]].

Note that (2) is a special case of both (1) and (3), which are independent.  (4) is a special case of (3), by the [[adjoint functor theorem]].  (5) is a special case of (2), of course.

## Yet another definition ##

The following paper:

* John Baez and James Dolan, Higher-dimensional algebra III: $n$-categories and the algebra of opetopes, _Adv. Math._ **135** (1998), 145-206.  [[arXiv](http://arxiv.org/abs/q-alg/9702014)]

uses the term '2-rig' in yet another way: it defines a 2-rig to be a [[monoidal category|monoidal]] [[colimit|cocomplete category]] where the monoidal product distributes over colimits.   We can define [[braided monoidal category|braided]] and [[symmetric monoidal category|symmetric]] 2-rigs in this sense (and indeed, also in the other senses listed above).  In particular, there is a 2-category $\mathbf{Symm2Rig}$ with:

* symmetric monoidal cocomplete categories where the monoidal product distributes over colimits as objects,

* symmetric monoidal cocontinuous functors as 1-morphisms,

* symmetric monoidal natural transformations as 2-morphisms.

This leads to the following:

+-- {: .un_thm}
###### Conjecture ([[John Baez]])
The initial symmetric 2-rig is $Set$, in a suitably weakened sense.  Namely, if $R$ is any object of $\mathbf{Symm2Rig}$, then there is a 1-morphism $Set \to R$ that is unique up to a 2-isomorphism.  

Furthermore, the free symmetric 2-rig on one object is the category of [[species]], $\widehat{\mathbb{P}}$ --- that is, the category of presheaves on the groupoid of finite sets and bijections, $\mathbb{P}$.  This symmetric 2-rig is free on the object $X$ which is the presheaf sending the one-element set to the one-element set, and every other set to the empty set.  

More precisely: if $R$ is any symmetric 2-rig and $x \in R$, there exists a 1-morphism $F: \widehat{\mathbb{P}} \to R$ with $F(X) = x$, and $F$ is unique up to a 2-isomorphism.
=--

[[!redirects 2-rig]]
[[!redirects 2-rigs]]
[[!redirects 2-ring]]
[[!redirects 2-rings]]
