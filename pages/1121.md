
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

### Of a general category

Traditionally, a **wide subcategory** of a [[category]] $C$ is a [[subcategory]] containing all the [[objects]] of $C$. 

Equivalently, it is a subcategory through which the canonical [[functor]] $disc(Obj(C)) \to C$ (from the [[discrete category]] on the collection of [[objects]]) factors, or whose inclusion functor is [[bo functor|bijective on objects]].

Notice that the condition to contain all the objects is not invariant under [[equivalence of categories]] and so the definition of wide subcategory above violates the [[principle of equivalence]].  A variant of the definition which fixes this is:

an **essentially wide subcategory** contains at least one object from each [[isomorphism class]] of objects; that is, its inclusion functor is [[essentially surjective functor|essentially surjective on objects]].


A wide subcategory is also called a **lluf subcategory** ("lluf" being "[[full subcategory|full]]" spelled backwards).

### Of an abelian category

An unrelated definition of "wide subcategory" is commonly used in the study of [[derived categories]] and [[stability conditions]]. 

In this context, a [[full subcategory]] $\mathcal{W} \hookrightarrow \mathcal{A}$ of an [[abelian category]] $\mathcal{A}$ is called **wide** if it is closed under [[kernels]], [[cokernels]] and [[extensions]]. 

See, for example, [Hovey 01](#Hovey01), [Ingalls-Thomas 09](#IngallsThomas09), [Marks-Stovicek 15](#MarksStovicek15).

Given a wide subcategory $\mathcal{W}$ in this sense, one can consider the minimal [[torsion theory|torsion class]] $T(\mathcal{W})$ containing it. Conversely, if $\mathcal{T}$ is a torsion class, define $W(\mathcal{T})$ to be the [[full subcategory]] on those [[objects]] $X \in \mathrm{Ob}(\mathcal{T})$ such that, for any $Y \in \mathrm{Ob}(\mathcal{T})$ and any $g: Y \to X$, the [[kernel]] of $g$ is in $\mathcal{T}$. The [[composition]] $W \circ T$ is the [[identity functor|identity]], thus exhibiting the [[poset]] of wide subcategories as a [[retract]] of the poset of [[torsion theory|torsion classes]]. 

The [[surjection]] $W$ becomes an [[injection]] when restricted to [[functorially finite]] torsion classes, and is often a [[bijection]] between functorially finite torsion classes and functorially finite wide subcategories; see [Marks-Stovicek 15](#MarksStovicek15).

## Examples

### General

Given any category $C$, the maximal sub-groupoid of $C$ is the subcategory consisting of all objects of $C$ but with morphisms only the isomorphisms of $C$. This is the [[core]] of a category, and it is a wide subcategory.

## References

### General

...

### For abelian categories

* {#Hovey01} [[Mark Hovey]], _Classifying subcategories of modules_, Trans. Amer. Math. Soc. 353 (2001), 3181-3191  ([doi:10.1090/S0002-9947-01-02747-7](https://doi.org/10.1090/S0002-9947-01-02747-7))

* {#IngallsThomas09} Colin Ingalls, Hugh Thomas, _Noncrossing partitions and representations of quivers_,  Volume 145, Issue 6 November 2009 , pp. 1533-1562 ([doi:10.1112/S0010437X09004023](https://doi.org/10.1112/S0010437X09004023))

* {#MarksStovicek15} Frederik Marks, Jan Stovicek, _Torsion classes, wide subcategories and localisations_ [arXiv:1503.04639](https://arxiv.org/abs/1503.04639)


[[!redirects wide subcategory]]
[[!redirects wide subcategories]]
[[!redirects lluf subcategory]]
[[!redirects lluf subcategories]]
[[!redirects essentially wide subcategory]]
[[!redirects essentially wide subcategories]]
[[!redirects essentially lluf subcategory]]
[[!redirects essentially lluf subcategories]]
