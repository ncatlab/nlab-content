
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
* automatic table of contents goes here
{:toc}

## Idea 

A _monoidal model category_ is a [[model category]] which is also a [[closed monoidal category]] in a compatible way.  In particular, its [[homotopy category]] inherits a closed monoidal structure.


## Definition 

A (symmetric) **monoidal model category** is a category equipped with 

* the structure of a  [[closed monoidal category|closed]] [[symmetric monoidal category|symmetric monoidal category]] 

* the structure of a [[model category]];

such that

* the [[pushout-product axiom]] is satisfied, and

* For any cofibrant object $X$, the map $Q e \otimes X \to e\otimes X \cong X$ is a weak equivalence, where $e$ is the unit object of the monoidal structure and $Q e\to e$ is a cofibrant replacement for it.  This is automatically satisfied if $e$ is cofibrant, as it is in most (but not all) cases.

## Properties 

The central fact about a monoidal model category is that its homotopy category inherits a closed monoidal structure.

## Examples 

* A [[nice category of spaces|nice category of topological spaces]] with cartesian product and the usual (Quillen) [[model structure on topological spaces|model structure]].

* The category of [[simplicial set]]s with cartesian product and the usual (Quillen) [[model structure on simplicial sets|model structure]].

* The category [[Cat]] with cartesian product and the [[folk model structure]].

* The category [[Gray]] of [[strict 2-category|strict 2-categories]] with the [[Gray tensor product]] and the [[model structure on 2-categories|Lack model structure]].

* The category of [[chain complex]]es with the usual [[tensor product]] of chain complexes and the [[model structure on chain complexes|projective model structure]].

* The category of [[pointed object|pointed]] compactly generated topological spaces or simplicial sets with the [[smash product]].

* Any of many modern model categories of [[spectrum|spectra]].  The standard example of a monoidal model category whose unit is not cofibrant is the category of EKMM S-modules.

## Related concepts

* [[monoidal Quillen adjunction]]

## References 

* [[Mark Hovey]], _Model Categories_

[[!redirects monoidal model categories]]
