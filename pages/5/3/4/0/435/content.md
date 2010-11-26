
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

## Idea

A _simplicially enriched category_ is a [[category]] with a [[simplicial set]] of [[morphism]]s between any two objects. 

One may think of the 1-cells in a hom-simplicial set as a [[2-morphism]], the 2-cells as a [[3-morphism]] and generally a $(k-1)$-cell as a [[k-morphism]]. Therefore simplicially enriched categories may serves as models for [[∞-categories]]. Precisely which notion of $\infty$-category depends on which extra [[stuff, structure, property|structure and property]] one imposes.

For instance

* requiring the hom-simplicial sets to be [[Kan complex]]es makes simplicially enriched categories a model for [[(∞,1)-categories]];

* similary, equipping the $sSet$-enriched category with the structure of a $sSet_{Quillen}$-[[enriched model category]] -- a [[simplicial model category]] -- makes it a model for an $(\infty,2)$-category.

  This is discussed in more detail at [[relation between quasi-categories and simplicial categories]].

* on the other hand, eqipping the $sSet$-enriched category with the structure of an $sSet_{Joyal}$-enriched model category over the Joyal-[[model structure for quasi-categories]] makes it a model for an [[(∞,2)-category]].
 

## Definition

+-- {: .un_defn}
###### Definition

A _simplicially enriched category_ is a [[enriched category|category enriched over]] the [[cartesian monoidal category]] [[sSet]] of [[simplicial sets]].

=--

+-- {: .un_remark}
###### Remark

These $sSet$-enriched categories are sometimes, somewhat imprecisely, called just _[[simplicial categories]]_.

=--

There is a related notion of [[simplicial groupoid]] with the added requirement that all arrows in the categories concerned are [[isomorphisms]].


## As models for $(\infty,1)$-categories 

Since simplicial sets that are [[Kan complex]]es are an incarnation of [[∞-groupoid]]s, an $sSet$-category all whose [[hom-object]]s happen to be [[Kan complex]]es may be regarded as a category enriched in [[∞-groupoid]]s. By the logic of [[(n,r)-category]] theory this should be a model for an [[(∞,1)-category]].

Treating simplicial categories tis way as models for $(\infty,1)$-categories is one of the central tools in [[homotopy coherent category theory]].

Indeed, there is a [[model structure on simplicial categories]] whose fibrant objects are Kan-complex enriched categories, and which is one model for the [[(∞,1)-category of (∞,1)-categories]].

By a web of [[Quillen equivalence]]s this is related to the other incarnations of $(\infty,1)$-categories. Notably to [[quasi-categories]] and [[complete Segal space]]s. For more on this see

* [[relation between quasi-categories and simplicial categories]].


### Properties

#### Homotopy Kan extension

See [[homotopy Kan extension]] for the moment.


#### Model structure

See [[model structure on sSet-categories]] for the moment.


## As models for $(\infty,2)$-categories

See [[(∞,2)-category]] for the moment.


## References

Simplicially enriched categories as models for $(\infty,1)$-categories are discussed in some detail in section A.3 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Homotopy coherent category theory on $sSet$-categories is discussed in 

* [[Jean-Marc Cordier]] [[Timothy Porter]], _Homotopy coherent category theory_  ([pdf](http://www.ams.org/journals/tran/1997-349-01/S0002-9947-97-01752-2/S0002-9947-97-01752-2.pdf))

which describes resolutions of the simplicial functor categories between two simplicial categories and

* [[Michael Batanin]], _Homotopy coherent category theory and $A_\infty$-structures in monoidal categories_ ([pdf](http://dodo.pdmi.ras.ru/~topology/books/batanin.pdf))

which shows that these resolved functor categories are in fact $sSet$-[[A-∞ categories]].


[[!redirects simplicially enriched category]]
[[!redirects simplicially enriched categories]]
[[!redirects sSet-enriched category]]
[[!redirects sSet-enriched categories]]
[[!redirects SSet-enriched category]]
[[!redirects SSet-enriched categories]]
[[!redirects SimpSet-enriched category]]
[[!redirects SimpSet-enriched categories]]
[[!redirects sSet-category]]
[[!redirects sSet-categories]]
[[!redirects SSet-category]]
[[!redirects SSet-categories]]
[[!redirects SimpSet-category]]
[[!redirects SimpSet-categories]]
