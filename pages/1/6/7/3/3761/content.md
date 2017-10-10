
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A **monoidal bicategory** is a [[bicategory]] with a [[monoidal category|monoidal structure]], which is up-to-equivalence in a suitable bicategorical sense.  A concise definition is that a monoidal bicategory is a [[tricategory]] with one object.  Just as every tricategory is equivalent to a [[Gray-category]], every monoidal bicategory is equivalent to a **Gray-monoid**, i.e. a monoid in the monoidal category [[Gray]].

Just as monoidal categories also come in [[braided monoidal category|braided]] and [[symmetric monoidal category|symmetric]] versions, monoidal bicategories have *three* extra levels of commutativity (see the [[periodic table]] and the [[stabilization hypothesis]]):

* [[braided monoidal 2-categories]]
* [[sylleptic monoidal 2-categories]]
* [[symmetric monoidal 2-categories]]

There are also 2-categorical variants of other structures on monoidal 1-categories, such as:

* [[closed monoidal 2-category]]
* [[balanced monoidal 2-category]]
* [[compact closed 2-category]]

## Examples {#Examples}

+-- {: .un_example}
###### Example
For $R$ a commutative [[ring]], there is a [[symmetric monoidal bicategory]] $Alg(R)$ whose 

* [[object]]s are $R$-[[algebra]]s;
* [[morphism]]s are algebra [[bimodule]]s;
* [[2-morphisms|k-morphism]] are bimodule homomorphisms.

The monoidal product is given by [[tensor product]] over $R$.
=--

By [[delooping]] this once, this gives an example of a [[tricategory]] with a single object.  The tricategory statement follows from theorem 21 of

* [[Richard Garner]], [[Nick Gurski]], _The low-dimensional structures that tricategories form_ ([arXiv:0711.1761](http://arxiv.org/abs/0711.1761))

This, and that the monoidal bicategory is even symmetric monoidal is given by the main theorem in

* [[Mike Shulman]], _Constructing symmetric monoidal bicategories_ ([arXiv:1004.0993](http://arxiv.org/abs/1004.0993))


+-- {: .un_example}
###### Example

For $V$ a cocomplete [[closed monoidal category|closed]] [[symmetric monoidal category]], there is a symmetric (indeed compact closed) monoidal bicategory $V Prof$ whose objects are small $V$-[[enriched categories]] and whose morphisms are $V$-enriched [[profunctors]].

=--

## Internalization

Monoidal bicategories provide a fruitful context for examples of the [[microcosm principle]]:

* Inside a monoidal bicategory one can define a [[pseudomonoid]], which generalizes a [[monoidal category]].
* Inside a braided monoidal bicategory one can define a [[braided pseudomonoid]], which generalizes a [[braided monoidal category]].
* Inside a sylleptic monoidal bicategory one can define a [[symmetric pseudomonoid]], which generalizes a [[symmetric monoidal category]].
* Inside a closed monoidal bicategory one can define a [[closed pseudomonoid]], which generalizes a [[closed monoidal category]].
* Inside a balanced monoidal bicategory one can define a [[balanced pseudomonoid]], which generalizes a [[balanced monoidal category]].
* Inside a compact closed monoidal bicategory one can define a [[compact closed pseudomonoid]], which generalizes a [[compact closed category]].

See [Day-Street](#DayStreet).

## Related concepts

* [[monoidal (2,1)-category]]

* [[monoidal category]]

* [[module 2-category]]

* [[braided monoidal 2-category]]

* [[sylleptic monoidal 2-category]]

* [[symmetric monoidal 2-category]]

* [[compact closed 2-category]]

* [[monoidal (infinity,1)-category]]

* [[monoidal (infinity,n)-category]]

* [[monoidal (∞,1)-category]]

## Coherence theorems

* [[coherence theorem for monoidal bicategories]]
* [[coherence theorem for braided monoidal bicategories]]
* [[coherence theorem for symmetric monoidal bicategories]]


## Related concepts

* [[Picard 3-group]]

* [[braided monoidal 2-category]]

* [[sylleptic monoidal 2-category]]

* [[symmetric monoidal 2-category]]

* [[monoidal (infinity,1)-category]]

* [[monoidal (infinity,n)-category]]

## References

Slightly different definitions of these various structures can be found in the following sequence of papers:

* Kapranov and Voevodsky, in "2-categories and Zamolodchikov tetrahedra equations" and "Braided monoidal 2-categories and Manin-Schechtman higher braid groups", defined *braided Gray monoids*, i.e. Gray-monoids with a braiding.

* [[John Baez|Baez]] and Neuchl, in "Higher-Dimensional Algebra I. Braided monoidal 2-categories" corrected the KV definition by adding one axiom.

* [[Brian Day|Day]] and [[Ross Street|Street]], in "Monoidal bicategories and Hopf algebroids," gave a definition of braided Gray-monoid equivalent to Baez-Neuchl, and also defined sylleptic and symmetric Gray-monoids and functors between them.
 {#DayStreet}

* [[Sjoerd Crans|Crans]], in "Generalized centers of braided and sylleptic monoidal 2-categories," further modified the definition by adding an axiom relating to the tensor unit.

* [[Paddy McCrudden|McCrudden]], in "Balanced coalgebroids," defined braided and sylleptic monoidal *bicategories* (not Gray monoids).

* [[Chris Schommer-Pries]], in his [Ph. D. thesis](http://sites.google.com/site/chrisschommerpriesmath/Home/Schommer-Pries-Thesis.pdf), gave the full definition of braided, sylleptic, and symmetric monoidal bicategories and also assembled them into a [[tricategory]].

* [[Nick Gurski]], in "Loop spaces, and coherence for monoidal and braided monoidal bicategories" [arXiv](http://arxiv.org/abs/1102.0981), proved a strictification theorem relating all these definitions, along with a coherence theorem for the braided case.

* [[Nick Gurski]] and [[Angelica Osorno]], in "Infinite loop spaces, and coherence for symmetric monoidal bicategories" [arXiv](http://arxiv.org/abs/1210.1174), proved a coherence and strictification theorem for the symmetric case (but the sylleptic case is perhaps still open).

[[!redirects Gray monoid]]
[[!redirects Gray-monoid]]
[[!redirects monoidal bicategories]]
[[!redirects Gray monoids]]
[[!redirects Gray-monoids]]

[[!redirects monoidal 2-category]]
[[!redirects monoidal 2-categories]]
