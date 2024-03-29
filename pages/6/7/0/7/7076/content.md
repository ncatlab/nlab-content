
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A __cartesian model category__ (alias __cartesian closed model category__) is a [[cartesian closed category]] that is equipped with the structure of a [[monoidal model category]] in a compatible way, which combines the axioms for a [[monoidal model category]] and an [[enriched model category]].

## Definition

\begin{definition}
A **cartesian closed model category** (following [Rezk 09, 2.2](#Rezk09) and [Simpson 12](#Simpson12)) is 

* a [[cartesian closed category]] 

* equipped with a [[model category]]-[[mathematical structure|structure]]

that satisfies

1. the following equivalent axioms:

   * **[[pushout-product axiom]]**

     For $f \colon X \to Y$ and $f' \colon X' \to Y'$ [[cofibrations]], the induced morphism 

     $$
       (Y \times X') 
         \overset{X \times X'}{\coprod} 
       (X \times Y') 
          \longrightarrow 
       Y \times Y'
     $$

     is a cofibration that is a [[weak equivalence]] if at least one of $f$ or $f'$ is;

   * **[[pullback-power axiom]]**

     For $f \colon X \to Y$ a [[cofibration]] and $f' \colon A \to B$ a [[fibration]], the induced morphism

     $$
       [Y,A] 
         \longrightarrow
       [X,A] \underset{[X,B]}{\prod} [Y,B]
     $$

     is a fibration, and a weak equivalence if at least one of $f$ or $f'$ is.


1. the **unit axiom**: 

   The [[terminal object]] is [[cofibrant object|cofibrant]].

\end{definition}

## Examples
 {#Examples}

Cartesian monoidal model categories include:

* the standard [[Quillen model structure on topological spaces]] on [[compactly generated topological space|compactly generated]] [[weakly Hausdorff topological spaces]]

  (see [there](classical+model+structure+on+topological+spaces#TopologicalEnrichment))

* the [[fine model structure on topological G-spaces]] 

  (see [there](fine+model+structure+on+topological+G-spaces#MonoidalModelCategoryStructure))

* the [[classical model structure on simplicial sets]]

* the [[canonical model structure on categories]] (and [[canonical model structure on groupoids|that on groupoids]])

  (see [there](canonical+model+structure+on+Cat#CartesianMonoidalModelStructure))

* the [[model structure for complete Segal spaces]]

  (see [there](model+structure+for+complete+Segal+spaces#CartesianMonoidalModelStructure))

* the model structure for [[Theta-spaces]]

  (see [there](Theta-space#CartesianMonoidalAndEnrichedStructure))

## Related concepts

* [[cartesian closed category]], [[locally cartesian closed category]]

* [[cartesian closed functor]], [[locally cartesian closed functor]]

* [[locally cartesian closed model category]]

* [[cartesian closed enriched category]]

* [[cartesian closed (∞,1)-category]] [[locally cartesian closed (∞,1)-category]]


## References

* {#Rezk09} [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_, Geom. Topol. 14(1): 521-571 (2010). ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602), [doi:10.2140/gt.2010.14.521](https://projecteuclid.org/journals/geometry-and-topology/volume-14/issue-1/A-cartesian-presentation-of-weak-ncategories/10.2140/gt.2010.14.521.full))

* {#Simpson12} [[Carlos Simpson]],  Chapter 10 of: _[[Homotopy Theory of Higher Categories]]_, Cambridge University Press 2011 ([hal:00449826](https://hal.archives-ouvertes.fr/hal-00449826/document), [ISBN:9780521516952](https://www.cambridge.org/in/academic/subjects/mathematics/geometry-and-topology/homotopy-theory-higher-categories-segal-categories-ini-categories-and-beyond?format=HB))


[[!redirects cartesian model categories]]

[[!redirects cartesian monoidal model category]]
[[!redirects cartesian monoidal model categories]]

[[!redirects cartesian closed model category]]
[[!redirects cartesian closed model categories]]

[[!redirects cartesian closed monoidal model category]]
[[!redirects cartesian closed monoidal model categories]]

[[!redirects cartesian model structure]]
[[!redirects cartesian model structures]]

[[!redirects cartesian closed model structure]]
[[!redirects cartesian closed model structures]]

[[!redirects cartesian closed monoidal model structure]]
[[!redirects cartesian closed monoidal model structures]]



