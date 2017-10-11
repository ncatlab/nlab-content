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

Monoidal bicategories provide a fruitful context for examples of the [[microcosm principle]]; various kinds of [[monoidal category]] can naturally be generalized to corresponding kinds of [[pseudomonoids]] internal to corresponding kinds of monoidal bicategories.  In some cases this is very immediate:

* Inside a monoidal bicategory one can define a [[pseudomonoid]], which when specialized to $Cat$ yields a [[monoidal category]].
* Inside a braided monoidal bicategory one can define a [[braided pseudomonoid]], which when specialized to $Cat$ yields a [[braided monoidal category]].
* Inside a sylleptic monoidal bicategory one can define a [[symmetric pseudomonoid]], which when specialized to $Cat$ yields a [[symmetric monoidal category]].
* Inside a balanced monoidal bicategory one can define a [[balanced pseudomonoid]], which  when specialized to $Cat$ yields a [[balanced monoidal category]].

Of course, these also specialize to the appropriate kinds of monoidal categories when specialized to monoidal 2-categories of [[enriched categories]], [[internal categories]], etc.

But for fancier kinds of monoidal structure, we need instead to consider monoidal bicategories like [[Prof]] instead.  An ordinary pseudomonoid in $Prof$ specializes to a [[promonoidal category]], but ordinary monoidal categories can be regarded as particular "representable" promonoidal ones.  In terms of the bicategory $Prof$, a [[Cauchy-complete]] monoidal category can be identified with a [[map pseudomonoid]], i.e. a pseudomonoid whose structure 1-morphisms are [[bicategory of maps|maps]] (left adjoints).  The non-Cauchy-complete case can be dealt with using a monoidal [[proarrow equipment]] instead.  Of course, this also generalizes to bicategories of enriched profunctors, internal profunctors, etc.

Having passed from $Cat$ to $Prof$, we can now define more kinds of pseudomonoids.  Note that $Prof$ has more structure than being merely (symmetric) monoidal: it is a [[compact closed bicategory]], i.e. all objects have duals.

* Inside any compact closed bicategory one can define a [[closed pseudomonoid]].  A representable closed pseudomonoid in $Prof$ specializes to a [[closed monoidal category]].
* Inside any compact closed bicategory one can define a [[star-autonomous pseudomonoid]] (a.k.a. a "Frobenius pseudomonoid", since it also categorifies a [[Frobenius algebra]]).  A representable star-autonomous pseudomonoid in $Prof$ specializes to a [[star-autonomous category]].
* Inside any compact closed bicategory one can define a [[compact closed pseudomonoid]].  A representable compact closed pseudomonoid in $Prof$ specializes to a [[compact closed category]].

In fact compact closedness of the whole monoidal bicategory is not necessary to assume; it suffices to assume only that the pseudomonoid itself has a dual.  (And in the star-autonomous case, this is actually a *consequence* of the definition.)

All the above definitions can be found in [Day-Street 97](#DS97), except for the star-autonomous case which is in [Day-Street 03](#DS03) and [Street 04](#Street04).

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

### Definitions

Slightly different definitions of these various structures can be found in the following sequence of papers:

* Kapranov and Voevodsky, in "2-categories and Zamolodchikov tetrahedra equations" and "Braided monoidal 2-categories and Manin-Schechtman higher braid groups", defined *braided Gray monoids*, i.e. Gray-monoids with a braiding.

* [[John Baez|Baez]] and Neuchl, in "Higher-Dimensional Algebra I. Braided monoidal 2-categories" corrected the KV definition by adding one axiom.

* [[Brian Day|Day]] and [[Ross Street|Street]], in "Monoidal bicategories and Hopf algebroids," (1997) gave a definition of braided Gray-monoid equivalent to Baez-Neuchl, and also defined sylleptic and symmetric Gray-monoids and functors between them.
 {#DS97}

* [[Sjoerd Crans|Crans]], in "Generalized centers of braided and sylleptic monoidal 2-categories," further modified the definition by adding an axiom relating to the tensor unit.

* [[Paddy McCrudden|McCrudden]], in "Balanced coalgebroids," defined braided and sylleptic monoidal *bicategories* (not Gray monoids).

* [[Chris Schommer-Pries]], in his [Ph. D. thesis](http://sites.google.com/site/chrisschommerpriesmath/Home/Schommer-Pries-Thesis.pdf), gave the full definition of braided, sylleptic, and symmetric monoidal bicategories and also assembled them into a [[tricategory]].

* [[Nick Gurski]], in "Loop spaces, and coherence for monoidal and braided monoidal bicategories" [arXiv](http://arxiv.org/abs/1102.0981), proved a strictification theorem relating all these definitions, along with a coherence theorem for the braided case.

* [[Nick Gurski]] and [[Angelica Osorno]], in "Infinite loop spaces, and coherence for symmetric monoidal bicategories" [arXiv](http://arxiv.org/abs/1210.1174), proved a coherence and strictification theorem for the symmetric case (but the sylleptic case is perhaps still open).

### Other

Other references referred to above include:

* [[Brian Day|Day]] and [[Ross Street|Street]], "Quantum categories, star autonomy, and quantum groupoids", 2003
 {#DS03}

* [[Ross Street]], "Frobenius monads and pseudomonoids", 2004
 {#Street04}

[[!redirects Gray monoid]]
[[!redirects Gray-monoid]]
[[!redirects monoidal bicategories]]
[[!redirects Gray monoids]]
[[!redirects Gray-monoids]]

[[!redirects monoidal 2-category]]
[[!redirects monoidal 2-categories]]
