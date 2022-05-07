
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The concept of _isomorphism_ generalizes the concept of [[bijection]] from the category [[Set]] of [[sets]] to general [[categories]].

An _isomorphism_ is an invertible [[morphism]], hence a morphism with an [[inverse morphism]].

Two [[objects]] of a [[category]] are said to be _isomorphic_ if there exists an isomorphism between them. This means that they "are the same for all practical purposes" as long as one does not violate the [[principle of equivalence]].

But beware that two objects may be isomorphic by more than one isomorphism. In particular a single object may be isomorphic to itself by nontrivial isomorphisms other than the [[identity morphism]]. Frequently the particular choice of isomorphism matters.

Every isomorphism is in particular an [[epimorphism]] and a [[monomorphism]], but the converse need not hold.

Common jargon includes "is a mono" or "is monic" for "is a monomorphism", and "is an epi" or "is epic" for "is an epimorphism", and "is an iso" for "is an isomorphism".




##Definitions

An __isomorphism__, or __iso__ for short, is an invertible [[morphism]], i.e. a [[morphism]] with a 2-sided [[inverse]].  

A morphism could be called __isic__ (following the more common 'monic' and 'epic') if it is an isomorphism, but it\'s more common to simply call it _invertible_.  Two [[objects]] $x$ and $y$ are __isomorphic__ if there exists an isomorphism from $x$ to $y$ (or equivalently, from $y$ to $x$).  An __[[automorphism]]__ is an isomorphism from one object to itself.


## Properties

It is immediate that isomorphisms satisfy the [[two-out-of-three]] property. But they also satisfy [[two-out-of-six property]] satisfied by the [[weak equivalences]] in any [[homotopical category]].

Note that the [[inverse morphism]] of an isomorphism is an isomorphism, as is any [[identity morphism]] or [[composite]] of isomorphisms.  Thus, being isomorphic is an [[equivalence relation]] on objects.  The equivalence classes form the [[fundamental 0-groupoid]] of the category in question.

Every isomorphism is both a [[split monomorphism]] (and thus about any other kind of [[monomorphism]]) and a [[split epimorphism]] (and thus about any other kind of [[epimorphism]]).  In a [[balanced category]], every morphism that is both monic and epic (called a [[bimorphism]]) is invertible, but this does not hold in general.  However, any monic [[regular epimorphism]] (or dually, any epic [[regular monomorphism]]) must be an isomorphism.

A [[groupoid]] is precisely a [[category]] in which every morphism is an isomorphism.  More generally, the [[core]] of any category $C$ is the [[subcategory]] consisting of all objects but only the isomorphisms; it is a kind of underlying groupoid of $C$.  In a similar way, the automorphisms of any given object $x$ form a [[group]], the [[automorphism group]] of $x$.

In [[n-category|higher categories]], isomorphisms generalise to [[equivalence]]s, which we expect to have only [[weak inverse]]s.


## Examples


*  A __[[bijection]]__ is an isomorphism in [[Set]].

*  A __[[homeomorphism]]__ is an isomorphism in [[Top]].

*  A __[[diffeomorphism]]__ is an isomorphism in [[Diff]].

* Every morphism in a [[groupoid]] is an isomorphism. 
  By definition of groupoid.


## Related concepts

* [[equality]]

* **isomorphism**

  * [[exceptional isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], [[weak homotopy equivalence]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of (∞,1)-categories]]

* [[EI-category]]


[[!redirects isomorphic]]
[[!redirects isomorphisms]]
[[!redirects iso]]
[[!redirects isic]]

[[!redirects isomorphic]]