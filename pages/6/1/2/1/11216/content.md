
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In [[Type Two Theory of Effectivity]] for [[computable analysis]] (see [Weihrauch 00](#Weihrauch00)) one considers the following definition:

A _representation_ of a $T_0$-[[topological space]] $X$ is a presentation of it as a [[quotient space]] of a [[subspace]] $B$ of [[irrational number|Baire space]] (the underlying space of [[Kleene's second algebra]]). Such a representation is called _admissible_ if the quotient map $B \to X$ has the [[right lifting property]] against [[continuous functions]] out of other subspaces $B'$ of Baire space.

Given representations of $X$ and $X'$ in this way, then a [[function]] $f \colon X \to X'$ is called _continuously realizable_ if there exists a [[continuous function]] $\phi \colon B \to B'$ between the corresponding subspaces of Baire space such that the evident [[commuting diagram|diagram commutes]].

For admissible representations a function $X\to X'$ is continuously realizable precisely if it is already continuous.

Write $AdmRep$ for the [[category]] of admissible representations in this sense, and continuously realizable (and hence continuous) functions between these.

## Properties

### Relation to function realizability

The category $AdmRep$ above is a [[reflective subcategory]] of the [[function realizability topos]] $RT(\mathcal{K}_2)$ (see [vanOosten 08](#vanOosten08)).

## Related concepts

[[!include computable mathematics -- table]]


## References

Lecture notes include

* {#Bauer05} [[Andrej Bauer]], section 2 of _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

Textbooks include

* {#Weihrauch00} [[Klaus Weihrauch]], _Computable Analysis_. Berlin, Springer, 2000


* {#vanOosten08} [[Jaap van Oosten]], _Realizability: an introduction to its categorical side_, Studies in Logic and the Foundations of Mathematics, vol. 152, Elsevier, 2008 ([preface pdf](http://www.staff.science.uu.nl/~ooste110/boekbegin.pdf))