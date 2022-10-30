
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

A [[model category]] structure whose fibrant objects are [[Segal categories]]. This is a [[presentable (infinity,1)-category|presentation]] of the [[(∞,1)-category]] [[(∞,1)Cat]] from the point of view of (weakly) [[∞Grpd]]-[[enriched categories]].

## Definition

Write $PreSegalCat \hookrightarrow [\Delta^{op}, sSet]$ for the full [[subcategory]] on those bisimplicial sets $X$ for which $X_0$ is a discrete simplicial set (the "precategories").

The [[nerve]] functor 

$$
  N : Cat \to PreSegalCat
$$

has a [[left adjoint]] ("fundamental category" functor)

$$
  \tau_1 : PreSegalCat \to Cat
  \,.
$$

There is a completion functor

$$
  compl : PreSegalCat \to PreSegalCat
$$

(...)

Define

* the cofibrations are precisely the [[monomorphisms]];

* the weak equivalences are those morphisms which under $compl$ become essentially surjective (under $\tau_1$) and full and faithful (equivalence on hom simplicial sets)

(...)

## Properties

### General 

The model structure is 

* [[left proper model category|left proper]];

* [[cartesian monoidal category|cartesian]] [[monoidal model category|monoidal]];

* a [[Cisinski model structure]]

### Relation to other model structures

See _[[table - models for (infinity,1)-categories]]_.


## Related concepts

* [[model structure for Segal operads]]

## References

The model structure for Segal categories was introduced in

* [[André Hirschowitz]], [[Carlos Simpson]], _Descente pour les $n$-champs (Descent for $n$-stacks)_ ([arXiv:9807049](http://arxiv.org/abs/math/9807049))

Its cartesian closure was established in 

* Regis Pellissier. Cat&#233;gories enrichies faibles. Th&#232;se, Universit&#233; de Nice-Sophia Antipolis (2002), arXiv:math/0308246,

The fact that the fibrant Segal categories in this model structure are precisely the [[Reedy model structure|Reedy fibrant]] bisimplicial sets is due to

* [[Julie Bergner]], _A characterization of fibrant Segal categories_ ([pdf](http://www.math.ucr.edu/~jbergner/ReedyFib.pdf))

