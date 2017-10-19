+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **polycategory** is like a [[category]] or a [[multicategory]], but where both the [[domain]] and the [[codomain]] of a [[morphism]] can be [[finite set|finite]] [[lists]] of [[objects]] rather than just single objects.  Like multicategories, polycategories have both symmetric and non-symmetric variants.

Just as a symmetric multicategory with one object is also called an [[operad]], and so a general symmetric multicategory is sometimes called a "colored operad", a symmetric polycategory with one object is also called a **dioperad** and a general symmetric polycategory is sometimes called a "colored dioperad".

## Properties

### Relation to PROPs

A (multicolored) [[PROP]] can also be described as a polycategory; what distinguishes a polycategory from a PROP is that in a polycategory, we can only compose along one object at once.  That is, we have a composition operation

$$\circ_D \colon Hom(A,B;C,D,E) \times Hom(F,D,G; H) \to Hom(F,A,B,G; C,H,E)$$

but not an operation such as

$$\circ_{B,C} \colon Hom(A; B,C) \times Hom(B,C; D) \to Hom(A,D).$$

### Internal logic

Polycategories provide a natural [[categorical semantics]] for [[linear logic]].

### Representability

A polycategory that is "representable on both sides", meaning informally that morphisms in $Hom(A_1,\dots,A_n;B_1,\dots,B_m)$ correspond to morphisms $A_1 \otimes \cdots\otimes A_n \to B_1 \invamp \cdots \invamp B_m$, is a [[linearly distributive category]].  A formal definition can be found in [(Cockett-Seely)](#CockettSeely97).

### Internal structures

Some categorical structures that are normally defined in a monoidal category can instead be defined in a polycategory, including [[Frobenius algebras]] and [[dual objects]].  Dual objects, in particular, are a form of "negation" that make a linearly distributive category into a [[star-autonomous category]].

## Generalizations

Just as [[multicategories]] are a special case of [[generalized multicategories]], which can be defined relative to any suitable [[monad]], polycategories are a special case of [[generalized polycategories]], which can be defined relative to any suitable [[pseudo-distributive law]].

## References

* M.E. Szabo, *Polycategories*, Comm. Algebra 3 (1975) 663-689.  [DOI](http://www.tandfonline.com/doi/abs/10.1080/00927877508822067)

* {#CockettSeely97} [[Robin Cockett]], [[Robert Seely]],  _Weakly Distributive Categories_, _Journal of Pure and Applied Algebra_, 114(1997)2, pp 133-173 ([ps.gz](http://www.math.mcgill.ca/rags/linear/wdc.ps.gz))

* [[Richard Garner]], *Polycategories via pseudo-distributive laws*, [arXiv](http://arxiv.org/abs/math/0606735)

* Wee Liang Gan, _Koszul duality for dioperads_, [arxiv](https://arxiv.org/abs/math/0201074)

[[!redirects polycategories]]
[[!redirects dioperad]]
[[!redirects dioperads]]
[[!redirects colored dioperad]]
[[!redirects colored dioperads]]
[[!redirects coloured dioperad]]
[[!redirects coloured dioperads]]
