

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **compact closed category**, or simply a **compact category**, is a [[symmetric monoidal category]] in which every object is [[dualizable object|dualizable]], hence a [[rigid monoidal category|rigid]] symmetric monoidal category.

In particular, a compact closed category is a [[closed monoidal category]], with the [[internal hom]] given by $[A,B] = A^* \otimes B$ (where $A^*$ is the [[dual object]] of $A$).

More generally, if we drop the symmetry requirement, we obtain a [[rigid monoidal category]], a.k.a. an *autonomous category*.  Thus a compact category may also be called a **rigid symmetric monoidal category** or a **symmetric autonomous category**.  A maximally clear, but rather verbose, term would be a **symmetric monoidal category with duals for objects**.

## Propertues

### Relation to traced monoidal categories
 {#RelationToTracedMonoidalCategories}

Given a [[traced monoidal category]] $\mathcal{C}$, there is a [[free construction]] completion of it to a compact closed category $Int(\mathcal{C})$ ([Joyal-Street-Verity 96](#JoyalStreetVerity96)):

the objects of $Int(\mathcal{C})$ are pairs $(A^+, A^-)$ of objects of $\mathcal{C}$, a morphism $(A^+ , A^-) \to (B^+ , B^-)$ in $Int(\mathcal{C})$ is given by a morphism of the form $A^+\otimes B^- \longrightarrow A^- \otimes B^+$ in $\mathcal{C}$, and [[composition]] of two such morphisms $(A^+ , A^-) \to (B^+ , B^-)$ and $(B^+ , B^-) \to (C^+ , C^-)$ is given by [[trace|tracing out]] $B^+$ and $B^-$ in the evident way.


### Relation to star-autnomous categories

A compact closed category is a [[star-autonomous category]] with the [[tensor unit]] as [[dualizing object]].

## Related concepts

* [[compact closed 2-category]]

## References

Discussion of [[coherence]] in compact closed catories is due to

* [[Max Kelly]], M.L. Laplaza, _Coherence for compact closed categories_,  Journal of Pure and Applied Algebra 19: 193&#8211;213 (1980)

The relation to [[quantum operations]] and [[completely positive maps]] is discussed in

* Peter Selinger, _Dagger compact closed categories and
completely positive maps. [pdf](http://www.mscs.dal.ca/~selinger/papers/dagger.pdf)_

The relation to [[traced monoidal categories]] is discussed in

* [[André Joyal]], [[Ross Street]], [[Dominic Verity]], _Traced monoidal categories_, Math. Proc. Camb. Phil. Soc. (1996), 119, 447 ([pdf](http://sci-prew.inf.ua/v119/3/S0305004100074338.pdf))
 {#JoyalStreetVerity96}


* Wikipedia, _[Compact closed category](http://en.wikipedia.org/wiki/Compact_closed_category)_ .

[[!redirects compact closed categories]]
[[!redirects compact category]]
[[!redirects compact categories]]
[[!redirects symmetric monoidal category with duals for objects]]
[[!redirects symmetric monoidal categories with duals for objects]]
[[!redirects symmetric monoidal category with duals]]
[[!redirects symmetric monoidal categories with duals]]