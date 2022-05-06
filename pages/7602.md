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

### Relation to properads and PROPs

(Coloured) [[properads]] and [[PROPs]] are both similar to polycategories: what distinguishes polycategories from both properad and PROPs is that in a polycategory, we can only compose along one object at once.  That is, we have a composition operation

$$\circ_D \colon Hom(A,B;C,D,E) \times Hom(F,D,G; H) \to Hom(F,A,B,G; C,H,E)$$

but not an operation such as

$$\circ_{B,C} \colon Hom(A; B,C) \times Hom(B,C; D) \to Hom(A,D).$$

In properads and PROPs, we allow composition along multiple objects at once. This is analogous to the definition of (coloured) [[operads]] in terms of partial composition or simultaneous composition. However, though both kinds of operads are equivalent, there exist coloured properads that are not equivalent to polycategories. For instance, if we have polymorphisms $f : A \to B, B$ and $g : B, B \to C$, we can form the composite $g \circ f : A \to C$ in a properad, but not a polycategory.

PROPs generalise properads further by, in addition to having the multiple composition operator of properads, also having a tensoring operator (given by the action of $\otimes$ on morphisms) that allows for composition along _zero_ objects.

### Internal logic

Polycategories provide a natural [[categorical semantics]] for [[linear logic]].

### Representability

A polycategory that is "representable on both sides", meaning informally that morphisms in $Hom(A_1,\dots,A_n;B_1,\dots,B_m)$ correspond to morphisms $A_1 \otimes \cdots\otimes A_n \to B_1 \invamp \cdots \invamp B_m$, is a [[linearly distributive category]].  A formal definition can be found in [(Cockett-Seely)](#CockettSeely97).

### Internal structures

Some categorical structures that are normally defined in a monoidal category can instead be defined in a polycategory, including [[Frobenius algebras]] and [[dual objects]].  Dual objects, in particular, are one approach to [[star-polycategories]]; they are the form of "negation" that makes a linearly distributive category into a [[star-autonomous category]].

## Generalizations

Just as [[multicategories]] are a special case of [[generalized multicategories]], which can be defined relative to any suitable [[monad]], polycategories are a special case of [[generalized polycategories]], which can be defined relative to any suitable [[pseudo-distributive law]].

## Related concepts

* [[dioperad]]
* [[PROP]]
* [[properad]]
* [[multicategory]]
* [[operad]]

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
