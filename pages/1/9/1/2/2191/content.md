+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea
 {#Idea}

As the notion of [[monoidal categories]] is a [[vertical categorification]] of [[monoids]], the notion of *actegories* is a [[vertical categorification]] of that of *[[actions]]* of monoids: [[action objects]]  [[coherence|coherently]] [[internalization|internal]] to the [[2-category]] [[Cat]].


So given a monoidal category $(C,\otimes,I,l,r,a)$ an actegory is another [[category]] $D$ with a notion of "tensor by object of $C$", i.e., a [[functor]]:

$$\oslash \colon C \times D \to D$$

that is [[associativity|associative]] (satisfies the [action property](action#eq:ActionProperty)) and [[unitality|unital]] up to [[natural isomorphism]] with respect to $\otimes$ in ways that generalize actions of a monoid, and satisfy [[coherence laws]] similar to those of a [[monoidal category]].

At least in situations where the monoidal category $C$  is (regarded as) a [[categorification|categorified]] [[ring]] (a [[2-ring]]), then if $D$ carries compatible linear structure one would alternatively call it a categorified [[module]] over $C$: a *[[2-module]]* (see also at *[[n-module|$n$-module]]*).


## Definition

For any [[category]] $A$, the category of [[endofunctors]] $End(A)$ is [[monoidal category|monoidal]] with respect to the (horizontal) composition (the composition of functors and the [[Godement product]] for natural transformations).

Given a [[monoidal category]] $(C,\otimes,I,l,r,a)$ a (left or right) __$C$-actegory__ is a category $A$ together with a (left or right) coherent action of $C$ on $A$. Depending on author and context, the left coherent action of $C$ on $A$ is a morphism of monoidal categories $C\to End(A)$ in the lax, colax, pseudo or strict sense (most often in pseudo-sense) or, in another terminology, a monoidal, comonoidal, strong monoidal or strict [[monoidal functor]]. Right coherent actions correspond to the monoidal functors into the category $End(A)$ with the opposite tensor product. 

$C$-actegories, colax $C$-equivariant functors and natural transformations of colax $C$-equivariant functors form a [[strict 2-category]] $_C Act^c$. A [[monad]] in $_C Act^c$ amounts to a pair of a monad in $Cat$ and a [[distributive law]] between the monad and an action of $C$. 

The notion of $C$-action (hence a $C$-actegory) is easily extendable to [[bicategories]] (see Bakovi&#263;'s thesis).

+-- {: .num_defn #Actegory}
###### Definition
A **(left) $\mathcal{C}$-actegory** is

1. a category $\mathcal{A}$;
1. a functor $\oslash : \mathcal{C} \times \mathcal{A} \to \mathcal{A}$ called the *action*;
1. a natural isomorphism $\lambda_a : a \to I \oslash a$ called the *unitor*;
1. a natural isomorphism $\alpha_{c,d,a} : c \oslash (d \oslash a) \to (c \otimes d) \oslash a$ called the *actor*;

satisfying a pentagonal and two triangular laws (see [KJ01](#KJ01), diagg. (1.1)-(1.3)) that witness the coherence of $\lambda$ and $\alpha$ with the unitors and associators of $\mathcal{C}$.
=--

## Connection with enrichment 
If a category $D$ is [[enriched category|enriched]] in $C$ with [[copowers]], then the copower structure forms an actegory on the ordinary category underlying $D$. 

Conversely, if an actegory is such that the functor $(-)\oslash d:C\to D$ has a [[right adjoint]] for all objects $d$ of $D$, then the right adjoints $D(d,-):D\to C$ provide an enrichment of $D$ in $C$ for which the action is a copower. See [KJ01](#KJ01).

## Origins

The original use of the term is explained in [Cockett & Pastro](#CockettPastro07): 

> The term *actegory* is used to describe the situation of a monoidal category “acting” on a category.  They first appeared (under a different name) in the work of B&eacute;nabou as a simple example of a bicategory. B. Pareigis developed the theory of actegories (again under a different name) and showed there usefulness in the representation theory of monoids and comonoids. The word “actegory” was first suggested at the Australian Category Seminar and first appeared in print in the thesis of P. McCrudden where they were used to study categories of representations of coalgebroids.



## Related Concepts

* If an actegory is like a [[module]], then a _[[biactegory]]_ is like a [[bimodule]].

## References

* [[Bodo Pareigis]], _Non-additive ring and module theory I. General theory of monoids_, Publ. Math. Debrecen 24 (1977), 189--204. MR 56:8656; _Non-additive ring and module theory II. C-categories, C-functors, and C-morphisms_, Publ. Math. Debrecen 24 (351--361) 1977. 

* {#KJ01} [[Max Kelly]], [[George Janelidze]], _A note on actions of a monoidal category_, Theory and Applications of Categories, Vol. 9, 2001, No. 4, pp 61--91 [link](http://www.tac.mta.ca/tac/volumes/9/n4/9-04abs.html)

* P. Schauenburg, _Actions of monoidal categories and generalized Hopf smash products_, J. Algebra __270__ (2003) 521&#8211;563 (remark: actegories with action in the strong monoidal sense)

* [[Zoran Škoda]], _Distributive laws for actions of monoidal categories_, [arxiv:0406310](http://arxiv.org/abs/math/0406310), _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_, [arxiv:0707.1609](http://arxiv.org/abs/0707.1609)

* [[J. R. B. Cockett]], Craig Pastro, _The logic of message-passing_ [arXiv:math/0703713](https://arxiv.org/abs/math/0703713).

A recent survey of many basic definitions and operations on actegories is

* Matteo Capucci, Bruno Gavranovic, _Actegories for the working amthematician_, [arxiv](https://arxiv.org/abs/2203.16351), 2022

[[!redirects actegories]]