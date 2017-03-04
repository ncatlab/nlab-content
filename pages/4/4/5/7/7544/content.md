
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of an _elementary (∞,1)-topos_ is the analog of the notion of _[[elementary topos]]_ in [[(∞,1)-category theory]].

This is in contrast to the notion of a _Grothendieck_ _[[(∞,1)-topos]] [[equivalence of (∞,1)-categories|equivalent]] to an [[(∞,1)-category of (∞,1)-sheaves]]_, the analog of a [[sheaf topos]], which is more specific (see [[geometric homotopy type theory]]). 

While every _Grothendieck_ [[(∞,1)-topos]] provides [[categorical semantics]] for [[homotopy type theory]] with a [[univalence|univalent]] Tarskian-[[type of types]] (and [[higher inductive types]]), one idea is roughly that elementary $(\infty,1)$-toposes should be defined as a larger class which precisely provides the [[categorical semantics]] for homotopy type theory in this sense.

Grothendieck $(\infty,1)$-toposes have many properties that are not reflected in type theory due to the finitary nature of type theory; the question is to find appropriate "finitary shadows" of them.  For instance, one can construct initial algebras for endofunctors using a transfinite induction argument; thus in type theory we postulate the existence of inductive types.  So the question is: what class of "infinitary constructions" that are available in Grothendieck $(\infty,1)$-toposes can be described finitarily by something that deserves the name "higher inductive type"? 

For more on this see 

* [[Michael Shulman]], [[Peter Lumsdaine]], 2016, _Semantics and syntax of
higher inductive types_, ([slides](http://home.sandiego.edu/~shulman/papers/stthits.pdf))

and at

* _[[homotopytypetheory:model of type theory in an (infinity,1)-topos]]_

* _[relation between type theory and category theory -- Univalent homotopy type theory and infinity-toposes](relation+between+type+theory+and+category+theory#HomotopyWithUnivalence)_ .


## References


A proposal for a definition, with an eye towards [[homotopy type theory]] and the [[relation between type theory and category theory]] is on the very last slide of 

* {#Shulman12} [[Mike Shulman]], _Inductive and higher inductive types_ (2012) ([pdf](https://home.sandiego.edu/~shulman/hottminicourse2012/04induction.pdf))

This proposal is [[predicative mathematics|predicative]], but could be made impredicative easily (to correspond closer to elementary 1-toposes rather than to types of 1-[[pretoposes]]) by adding a [[subobject classifier]] (i.e. a classifier for *all* subobjects, rather than merely the "classifiers for small subobjects" obtainable from object classifiers).

Related discussion is in 

* {#Joyal14} [[André Joyal]], _What is an elementary higher topos?_, talk at _[Reimagining The Foundations Of Algebraic Topology](https://www.msri.org/workshops/689)_ April 07, 2014 - April 11, 2014_ [web video](https://www.msri.org/workshops/689/schedules/18227) [PDF](https://www.msri.org/workshops/689/schedules/18227/documents/2046/assets/20468)

See maybe also the comments at

* [[Georg Hegel]], [book 2](Science+of+Logic#LehreVomWesen) of _[[Science of Logic]]_

[[!redirects elementary (∞,1)-topos]]

[[!redirects elementary (∞,1)-toposes]]
[[!redirects elementary (infinity,1)-toposes]]

[[!redirects elementary infinity-topos]]
[[!redirects elementary infinity-toposes]]
