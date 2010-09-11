
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* **geometric definition of higher categories**

* [[algebraic definition of higher categories]]

***

#Contents#
* table of contents
{:toc}

## Idea

In a **geometric definition** of [[(n,r)-categories]] [[composition]] of [[higher morphism]]s is not an _operation_ with a specified outcome but a _relation_ : the $(n,r)$-category is presented much like a [[directed space]] and [[k-morphism]]s are $k$-dimensional subspaces in there. When some of these $k$-morphsims are suitably adjacent, there is a guarantee that there exists a $k$-morphism that serves as their composite. But there may be several such. Instead of a rule for picking a specific one, subject to [[associativity]] constraints, there is a _contractible space of choices_ of possible composites.

From a geometric presentation of an $(n,r)$-category one can typically obtain an algebraic presentation by choosing composites. The contractibility of the space of choices becomes a [[coherence law]] satisfied by the collection of choices. 

Conversely, one may typically think of the geometric presentation of an $(n,r)$-category as being the [[nerve]] of a corresponding algebraic presentation.

## Examples

* a geometric model for [[(∞,0)-categories]] = [[∞-groupoids]] are [[Kan complex]]es;

  An [[algebraic Kan complex]] is an algebraic model that is obtained from  a Kan complex by making choices for [[composition]], [[associator]] etc.


  * a geometric model for an [[n-groupoid]] is a $(n+1)$-[[coskeletal]] Kan complex.

* a geometric model for [[(∞,1)-categories]] are [[quasi-categories]]

  An [[algebraic quasicategory]] is an algebraic model that is obtained from  a quasi-category by making choices for [[composition]], [[associator]] etc.
  

  * a geometric model for a [[(1,1)-category]] = [[category]] is a 2-[[coskeletal]] [[quasi-category]]

* a geometric model for an [[(n,r)-category]] is an $(n,r)$-[[Theta space]]

* a geometric model for an [[(∞,n)-category]] is

  * an [[n-fold complete Segal space]]

* a geoemtric model for a general [[omega-category]] is supposed to be a [[weak complicial set]]

## Properties

When the [[(∞,1)-category]] of all [[(n,r)-categories]] is presented by a [[model category]], then typically geometric models are _cofibrant_ objects while algebraic models are typically _fibrant_ objects.

For instance all in the standard [[model structure on simplicial sets]], or the standard [[model structure for quasi-categories]] all objects are cofibrant. 



[[!redirects geometric definition of higher categories]]
[[!redirects geometric definition of higher category]]
[[!redirects geometric model of higher categories]]
[[!redirects geometric model of higher category]]
