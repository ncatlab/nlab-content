
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


\tableofcontents

## Idea

A *tabulator* is a kind of [[double limit]], i.e. a [[limit]] in a [[double category]], generalizing the notion of the *[[graph of a profunctor]]* (also called the _cocollage_). Dually, the notion of a *cotabulator* generalizes that of the *[[cograph of a profunctor]]* (also called the _collage_).

## Definition

The _tabulator_ of a [[loose morphism]] $u \colon A \nrightarrow B$ in a [[double category]] $\mathbb{D}$ consists of an object $T u$ and a [[2-morphism]]
\begin{tikzcd}
Tu
\arrow[r, "p"]
\arrow[d, "\bullet"{anchor=center}, "id"']
\arrow[rd, phantom, "\tau_{u}"]
& A
\arrow[d, "\bullet"{anchor=center}, "u"]
\\
Tu
\arrow[r, "q"']
& B
\end{tikzcd}
with the universal properties:

  1. For every [[2-morphism]] 
\begin{tikzcd}
   X
   \arrow[r, "f"]
   \arrow[d, "\bullet"{anchor=center}, "id"']
   \arrow[rd, phantom, "\xi"]
   & A
   \arrow[d, "\bullet"{anchor=center}, "u"]
   \\
   X
   \arrow[r, "g"']
   & B
\end{tikzcd}
  there is a unique tight morphism $x \colon X \rightarrow T u$ such that 
    $\tau_{u} x = \xi$. 

  2. The tetrahedron condition holds (see [Paré, page 478](#Pare2011)). 

If only the first universal property holds, we say that the loose morphism has a _$1$-tabulator_. 

## Properties

* A double category $\mathbb{D} = (D_{0}, D_{1})$ has all $1$-tabulators (resp. $1$-cotabulators) if and only if the [[identity morphisms|identity]]-assigning map $id \colon D_{0} \rightarrow D_{1}$ has a [[right adjoint]] (resp. [[left adjoint]]). 

* A double category has all small [[double limits]] if and only if it has small double products, double equalisers, and tabulators.

* A tabulator in a [[2-category]], viewed as a [[double category]], is a [[power]] by the [[interval category]].

## References

An early reference for what is essentially the universal property of an (effective) tabulator is the definition of a **tabulation**, based on a similar definition in an [[allegory]]:

* [[Aurelio Carboni]], [[Stefano Kasangian]] and [[Ross Street]], _Bicategories of spans and relations_, Journal of Pure and Applied Algebra, Vol. 33, No. 3, 1984, pp. 259-267. &lbrack;<a href="https://doi.org/10.1016/0022-4049(84)90061-6">doi:10.1016/0022-4049(84)90061-6</a>&rbrack;

The definition of a (co)tabulator was first introduced in Section 5.3 of: 

* [[Marco Grandis]], [[Robert Pare]], _Limits in double categories_, Cahiers de Topologie et Géométrie Différentielle Catégoriques, **40**, 1999. ([url](http://www.numdam.org/item/CTGDC_1999__40_3_162_0/))

The $2$-dimensional universal property of a tabulator is stated in Section 3 of:

* {#Pare2011} [[Robert Pare]], _Yoneda theory for double categories_, Theory and Applications of Categories_, **25**, 2011. ([url](http://www.tac.mta.ca/tac/volumes/25/17/25-17abs.html))

Other references on (co)tabulators include:

* [[Susan Niefield]], _Span, cospan, and other double categories_ Theory and Applications of Categories_, **26**, 2012. ([url](http://www.tac.mta.ca/tac/volumes/26/26/26-26abs.html))

* [[Marco Grandis]] and [[Bob Paré]], _Span and cospan representations of weak double categories_, Categories and General Algebraic Structures with Applications 6.Speical Issue on the Occasion of Banaschewski's 90th Birthday (I) (2017): 85-105. ([url](https://www.mscs.dal.ca/~pare/DblRpr.pdf))

* [[Marco Grandis]], _Higher Dimensional Categories. From Double to Multiple Categories_, 2019. ([doi:10.1142/11406](https://doi.org/10.1142/11406))

[[!redirects tabulators]]
[[!redirects cotabulator]]
[[!redirects cotabulators]]