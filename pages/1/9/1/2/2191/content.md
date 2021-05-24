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

As [[monoidal categories]] are a [[vertical categorification]] of [[monoids]], *actegories* are a [[vertical categorification]] of *[[actions]]* of a monoid.
So given a monoidal category $(C,\otimes,I,l,r,a)$ an actegory is another category $D$ with a notion of "tensor by object of $C$", i.e., a functor:

$$\oslash : C \times D \to D$$

that is associative and unital up to natural isomorphism with respect to $\otimes$ in ways that generalize actions of a monoid, and satisfy coherence laws similar to those of a monoidal category.

## Definition

For any [[category]] $A$, the category of [[endofunctors]] $End(A)$ is [[monoidal category|monoidal]] with respect to the (horizontal) composition (the composition of functors and the [[Godement product]] for natural transformations).

Given a [[monoidal category]] $(C,\otimes,1,l,r,a)$ a (left or right) __$C$-actegory__ is a category $A$ together with a (left or right) coherent action of $C$ on $A$. Depending on an author and context, the left coherent action of $C$ on $A$ is a morphism of monoidal categories $C\to End(A)$ in the lax, colax, pseudo or strict sense (most often in pseudo-sense) or, in another terminology, a monoidal, comonoidal, strong monoidal or strict [[monoidal functor]]. Right coherent actions correspond to the monoidal functors into the category $End(A)$ with the opposite tensor product. 

$C$-actegories, colax $C$-equivariant functors and natural transformations of colax $C$-equivariant functors form a [[strict 2-category]] $_C Act^c$. A [[monad]] in $_C Act^c$ amounts to a pair of a monad in $Cat$ and a [[distributive law]] between the monad and an action of $C$. 

The notion of $C$-action (hence a $C$-actegory) is easily extendable to [[bicategories]] (see Bakovi&#263;'s thesis).

## Connection with enrichment 
If a category $D$ is [[enriched category|enriched]] in $C$ with [[copowers]], then the copower structure forms an actegory on the ordinary category underlying $D$. 

Conversely, if an actegory is such that the functor $(-)\oslash d:C\to D$ has a [[right adjoint]] for all objects $d$ of $D$, then the right adjoints $D(d,-):D\to C$ provide an enrichment of $D$ in $C$ for which the action is a copower. See [KJ01](#KJ01).

## Related Concepts

* If an actegory is like a [[module]], then a _[[biactegory]]_ is like a [[bimodule]].

## References

* [[Bodo Pareigis]], _Non-additive ring and module theory I. General theory of monoids_, Publ. Math. Debrecen 24 (1977), 189--204. MR 56:8656; _Non-additive ring and module theory II. C-categories, C-functors, and C-morphisms_, Publ. Math. Debrecen 24 (351--361) 1977. 

* {#KJ01} [[Max Kelly]], [[George Janelidze]], _A note on actions of a monoidal category_, Theory and Applications of Categories, Vol. 9, 2001, No. 4, pp 61--91 [link](http://www.tac.mta.ca/tac/volumes/9/n4/9-04abs.html)

* P. Schauenburg, _Actions of monoidal categories and generalized Hopf smash products_, J. Algebra __270__ (2003) 521&#8211;563 (remark: actegories with action in the strong monoidal sense)

* [[Zoran Škoda]], _Distributive laws for actions of monoidal categories_, [arxiv:0406310](http://arxiv.org/abs/math/0406310), _Equivariant monads and equivariant lifts versus a 2-category of distributive laws_, [arxiv:0707.1609](http://arxiv.org/abs/0707.1609)

[[!redirects actegories]]