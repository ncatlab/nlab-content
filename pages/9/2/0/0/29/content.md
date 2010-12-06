
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An _isomorphism_ is an invertible [[morphism]].

Two [[objects]] of a [[category]] are **isomorphic** if they are _essentially equal_ without necessarily actually being equal.  An **isomorphism** is a specific way of translating one object to an isomorphic one.  Note that it\'s often not enough to know *that* two objects are isomorphic; you may need to know *how* they are isomorphic, that is to know the specific isomorphism in question.


##Definitions

An __isomorphism__, or __iso__ for short, is an invertible [[morphism]], i.e. a [[morphism]] with a 2-sided [[inverse]].  

A morphism could be called __isic__ (following the more common 'monic' and 'epic') if it is an isomorphism, but it\'s more common to simply call it _invertible_.  Two [[objects]] $x$ and $y$ are __isomorphic__ if there exists an isomorphism from $x$ to $y$ (or equivalently, from $y$ to $x$).  An __[[automorphism]]__ is an isomorphism from one object to itself.


## Properties

Note that the inverse of an isomorphism is an isomorphism, as is any [[identity morphism]] or [[composite]] of isomorphisms.  Thus, being isomorphic is an [[equivalence relation]] on objects.  The equivalence classes form the [[fundamental 0-groupoid]] of the category in question.

Every isomorphism is both a [[split monomorphism]] (and thus about any other kind of [[monomorphism]]) and a [[split epimorphism]] (and thus about any other kind of [[epimorphism]]).  In a [[balanced category]], every morphism that is both monic and epic (called a [[bimorphism]]) is invertible, but this does not hold in general.  However, any monic [[regular epimorphism]] (or dually, any epic [[regular monomorphism]]) must be an isomorphism.

A [[groupoid]] is precisely a [[category]] in which every morphism is an isomorphism.  More generally, the [[core]] of any category $C$ is the [[subcategory]] consisting of all objects but only the isomorphisms; it is a kind of underlying groupoid of $C$.  In a similar way, the automorphisms of any given object $x$ form a [[group]], the [[automorphism group]] of $x$.

In [[n-category|higher categories]], isomorphisms generalise to [[equivalence]]s, which we expect to have only [[weak inverse]]s.


## Examples


*  A __[[bijection]]__ is an isomorphism in [[Set]].

*  A __[[homeomorphism]]__ is an isomorphism in [[Top]].

*  A __[[diffeomorphism]]__ is an isomorphism in [[Diff]].

* Every morphism in a [[groupoid]] is an isomorphism. 
  By definition of groupoid.


[[!redirects isomorphic]]
[[!redirects isomorphisms]]
[[!redirects iso]]
[[!redirects isic]]

[[!redirects isomorphic]]