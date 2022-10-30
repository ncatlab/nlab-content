
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Type-theoretic model categories

> under construction

* table of contents
{: toc}

## Idea

[[homotopy type theory|Homotopy type theory]] has [[categorical semantics]] in suitable [[homotopical categories]] which in turn present certain [[(infinity,1)-categories]].

The concept of _type-theoretic model category_ ([Shulman 12a](#Shulman12a)) or _type-theoretic fibration category_ ([Shulman 12b, def. 2.1](#Shulman12b)) is one particular way of making this precise. Specifically every [[locally presentable (∞,1)-category|locally presentable]] [[locally cartesian closed (∞,1)-category]] has a presentation by a type-theoretic model category, hence provides higher [[categorical semantics]] for [[homotopy type theory]] (without possibly [[univalence]]). For more on this see also the respective sections at _[[relation between type theory and category theory]]_.

## Definition

> under construction

By decomposing the structure in homotopy type theory in layers as

1. [[dependent type theory]]

2. with [[identity types]]

3. and [[univalence|univalent]] [[universe]] types.

A 1-[[category]] whose [[internal logic]] can interpret this needs to 

1. be a [[locally cartesian closed category]]

2. equipped with a [[weak factorization system]] with [[stable path objects]], such that [[acyclic cofibrations]] are preserved by [[pullback]] along [[fibrations]] between [[fibrant objects]]. 

3. (needs to be finished)


## References

The definition originates in and a discussion of [[categorical semantics]] of [[homotopy type theory]] in a type-theoretic model category appears in 

* {#Shulman12b} [[Michael Shulman]], _Univalence for inverse diagrams and homotopy canonicity_ ([arXiv:1203.3253](http://arxiv.org/abs/1203.3253))

An exposition is in 

* {#Shulman12a} [[Mike Shulman]], _[Minicourse on Homotopy Type Theory](http://www.math.ias.edu/~mshulman/hottminicourse2012/)_ part 3, _Categorical models of homotopy type theory_, April 2012 ([pdf](http://www.math.ias.edu/~mshulman/hottminicourse2012/03models.pdf))


Similar conisderations (using the term "typos" for something similar to a type-theoretic model category) are presented in

* [[André Joyal]], _What is categorical type theory_, various talks in 2013, ([pdf](http://www.math.uwaterloo.ca/~asl2013/Slides/Joyal.pdf))

[[!redirects presentation of homotopy type theory]]
[[!redirects categorical semantics of homotopy type theory]]
[[!redirects type-theoretic model category]]
[[!redirects type-theoretic model categories]]

[[!redirects type-theoretic fibration category]]
[[!redirects type-theoretic fibration categories]]
