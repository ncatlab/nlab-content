
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
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

## Idea

The idea of _realizability_ is a way of making the [[Brouwer-Heyting-Kolmogorov interpretation]] of [[constructivism]] and [[intuitionistic mathematics]] precise. It is related to the [[propositions as types]] paradigm. For instance, constructively a [[proof]] of an [[existential quantification]] $\underset{x\in X}{\exists} \phi(x)$ consists of constructing a specific $x \in X$ and a proof of $\phi(x)$, which "realizes" the [[truth]] of the statement, whence the name (see e.g. [Streicher 07, section 1](#Streicher07), [Vermeeren 09, section 1](#Vermeeren09) for introductions to the rough idea, or [Bauer 05, page 12 and def. 4.7](#Bauer05) for an actual definition).

## Realizability of univalence in homotopy type theory

One possible way to find a computational interpretation for [[univalence]] in [[homotopy type theory]] is to interpret it in using realizability. Stekelburg provides a univalent universe of modest Kan complexes.

Simplicial homotopy theory can be developed in an [[extensive]] [[locally cartesian closed]] category $A$. Such categories are also called [[Heyting bialgebras]]. The category $A$ has 
a class of [[nlab:small maps]] which has a bundle of small
[[assemblies]]. This provides an internal 
[[Heyting bialgebra]] $S$ which we can use as a target for simplicial `sets'. There is a (Kan-) model structure on these simplicial sets. 

Within $S$ we can define a universe $M$ and show that it is fibrant. This universe is even univalent.

Now, the category of assemblies in number realizability provides such a Heyting bialgebra. The modest sets, a small internally complete full subcategory, provide the univalent universe. Note that modest sets are an [[impredicative]] universe. It models the [[calculus of constructions]].

## Related entries

* [[realizability topos]]

* [[realizability model]]

* [[realizability interpretation]]

* [[effective topos]], [[Kleene-Vesley topos]]

* [[propositional axiom of choice]]

* [[Lifschitz realizability]]

[[!include computable mathematics -- table]]


## References

Realizability originates with the interpretation of [[intuitionistic mathematics|intuitionistic]] [[number theory]], later developed as _[[Heyting arithmetic]]_, in

* {#Kleene45} [[Stephen Kleene]], _On the interpretation of intuitionistic number theory_ Journal of Symbolic Logic, 10:109&#8211;124, 1945. [link](http://www.jstor.org/stable/2269016)

A historical survey of realizability (including [[realizability topos|categorical realizability]]) is in

* {#vanOosten00} [[Jaap van Oosten]], _Realizability: An Historical Essay_, 2000 ([link](http://www.staff.science.uu.nl/~ooste110/realizability/history.ps.gz), [pdf](https://pdfs.semanticscholar.org/0eb4/60525d1580fb9f184b43b974499bce2a2ea7.pdf))

A quick survey is in

* {#Vermeeren09} [[Stijn Vermeeren]], _Realizability Toposes_, 2009 ([pdf](http://stijnvermeeren.be/download/mathematics/essay.pdf))

being a summary of

* [[Martin Hyland]], _The effective topos_, in The L.E.J. Brouwer Centenary
Symposium (A. S. Toelstra and D. van Dalen, eds.), North-Holland Publishing
Company, 1982, pp. 165&#8211;216

A modern textbook account is

* {#vanOosten08} [[Jaap van Oosten]], _Realizability: an introduction to its categorical side_, Studies in Logic and the Foundations of Mathematics, vol. 152, Elsevier, 2008 ([preface pdf](http://www.staff.science.uu.nl/~ooste110/boekbegin.pdf))

Lecture notes include

* {#Streicher07} [[Thomas Streicher]], _Realizability_ (2007/08) ([pdf](http://www.mathematik.tu-darmstadt.de/~streicher/REAL/REAL.pdf))

and

* {#Bauer05} [[Andrej Bauer]], _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

based on

* {#Bauer00} [[Andrej Bauer]], _The Realizability Approach to
Computable Analysis and Topology_, PhD thesis CMU (2000) ([pdf](http://andrej.com/thesis/thesis.pdf))

* Peter Lietz, _From Constructive Mathematics to Computable Analysis via the Realizability Interpretation_ ([pdf.gz](http://www.mathematik.tu-darmstadt.de/~streicher/THESES/lietz.pdf.gz))

For realizability of univalent universes:

* Wouter Stekelenburg, _Realizability of Univalence: Modest Kan complexes_, [arXiv](http://arxiv.org/abs/1406.6579)


See also


* [[Steven Awodey]], [[Andrej Bauer]], _Sheaf toposes for realizability_ ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/stfr.pdf))

* Wouter Pieter Stekelenburg, _Realizability Categories_, PhD thesis, Utrecht 2013 ([arXiv:1301.2134](http://arxiv.org/abs/1301.2134))

* [[Martin Hyland]], _Variations on realizability: realizing the propositional axiom of choice_,  Mathematical Structures in Computer Science, Volume 12, Issue 3, June 2002, pp. 295 - 317  ([doi:10.1017/S0960129502003651](https://doi.org/10.1017/S0960129502003651), [pdf](https://www.dpmms.cam.ac.uk/~jmeh1/Research/Publications/2002/vor02.pdf))

[[!redirects realizer]]
[[!redirects realizers]]
