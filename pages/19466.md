[[!redirects presheaves of groupoids]]


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### $(\infty,1)$-Category theory
+-- {: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
=--
=--





#Contents#
* table of contents
{:toc}

## Idea

The idea of _presheaf of groupoids_ may refer to one of the following distinct but closely related concepts:

1. a [[functor]] from some [[opposite category]] to the [[1-category]] [[Grpd]] of all [[small groupoids]];

1. a [[Grpd]]-[[enriched functor]] from the opposite of a [[Grpd]]-[[enriched category]] to [[Grpd]] canonically regarded as enriched over itself, all with respect to its [[cartesian closed category]]-structure;

1. a [[pseudofunctor]] from the opposite of a plain category to the [[2-category]] (in fact: [[(2,1)-category]]) [[Grpd]] of all small groupoids;

1. a [[2-functor]] from the [[opposite 2-category]] of some [[2-category]] to the [[2-category]] [[Grpd]] of all small groupoids.

In the last two cases one also speaks of _[[pre-stacks]] of groupoids_ or _[[(2,1)-presheaves]]_.

The first two of these carry [[structures]] of [[homotopical categories]], even of  [[model categories]], that make them [[presentable (infinity,1)-category]]-presentations of the latter two.

Under the [[simplicial nerve]]-constructions, presheaves of groupoids in the sense of the first two items form a [[full subcategory]] of [[simplicial presheaves]], and their [[model category]]-structures enhance to the corresponding [[model structures on simplicial presheaves]], which [[presentable (infinity,1)-category|present]] _[[(∞,1)-presheaves]] of [[∞-groupoids]]_, hence _pre-[[∞-stacks]]_.

## Examples
 {#Examples}

* For $\mathcal{C}$ an ordinary [[site]], each [[covering]] family $\{U_i \overset{\iota_i}{\to} X\}$ induces a _[[Cech groupoid|&#268;ech groupoid]]_, which is really a presheaf of groupoids

$$
  C(\{U_i\}) \in [\mathcal{C}^{op}, Grpd]
  \,.
$$

## Related concepts

* [[model structure on simplicial groupoids]]

## References

A [[model category]]-[[structure]] on categories of presheaves of groupoids, modeling [[(2,1)-categories]] of [[stacks]] the way that the [[model structure on simplicial presheaves]] model [[(∞,1)-categories]] of [[∞-stacks]] is discussed in 

* {#Hollander01} [[Sharon Hollander]], _A homotopy theory for stacks_, Israel Journal of Mathematics, 163(1), 93-124 ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247))


[[!redirects presheaf of groupoids]]