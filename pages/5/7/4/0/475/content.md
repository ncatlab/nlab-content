
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A **tricategory** is a particular [[algebraic definition of higher category|algebraic]] notion of _weak_ [[3-category]].  The idea is that a tricategory is a category _weakly_ [[enriched category|enriched]] over [[Bicat]]: the [[hom-object|hom-objects]] of a tricategory are [[bicategories]], and the associativity and unity laws of [[enriched category|enriched categories]] hold only up to coherent equivalence.

## Examples {#Examples}

For $R$ a commutative [[ring]], there is a [[symmetric monoidal bicategory]] $Alg(R)$ whose 

* [[object]]s are $R$-[[algebra]]s;

* [[morphism]]s are algebra [[bimodule]]s;

* [[2-morphisms|k-morphism]] are bimodule homomorphisms.

The monoidal product is given by [[tensor product]] over $R$.

By [[delooping]] this once, this gives an example of a [[tricategory]] with a single object.

The tricategory statement follows from theorem 21 of

* [[Richard Garner]], [[Nick Gurski]], _The low-dimensional structures that tricategories form_ ([arXiv:0711.1761](http://arxiv.org/abs/0711.1761))

This, and that the monoidal bicategory is even symmetric monoidal is given by the main theorem in

* [[Mike Shulman]], _Constructing symmetric monoidal bicategories_ ([arXiv:1004.0993](http://arxiv.org/abs/1004.0993))



## Related entries 

*  [[strict 3-category]]
*  [[bicategory]]
*  [[tetracategory]]

## References

The original source is

* Gordon, Power, Street, _Coherence for tricategories_, Mem. Amer. Math Soc. 117 (1995) no 558 

This was refined in the thesis

* [[Nick Gurski]], _An algebraic theory of tricategories_ ([pdf](http://www.math.yale.edu/~mg622/tricats.pdf))

which is probably the best current starting point to read about tricategories and from where to take pointers to the original work by Gordon-Power-Street.

* [[Richard Garner]], [[Nick Gurski]], _The low-dimensional structures that tricategories form_ ([arXiv](http://arxiv.org/abs/0711.1761))


[[!redirects tricategories]]