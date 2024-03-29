
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


#Contents#
* table of contents
{:toc}

## Definition

The term **simplicial category** has at least three common meanings.  Thus, to avoid ambiguity, it is perhaps better to avoid it entirely and use an equivalent, unambiguous term for the particular meaning one has in mind.

First of all

* The **simplicial category** $\Delta$ is the domain category for the presheaf category of [[simplicial set|simplicial sets]].  This is the [[full subcategory]] of [[Cat]] on categories which are linear [[quiver]]s, or equivalently the category of finite, non-empty totally ordered sets and order-preserving functions between them.  To avoid ambiguity, $\Delta$ may also be called the **[[simplex category]]** or the **simplicial indexing category**.

More importantly, there are these two uses of the word:

1. A **simplicial category** is a [[simplicial object]] in [[Cat]] (that is, a functor from $\Delta^{op}$ to $Cat$), just like a simplicial set is a simplicial object in [[Set]], a simplicial space is a simplicial object in [[Top]], a simplicial abelian group is a simplicial object in [[Ab]], and so on.  To avoid ambiguity, **[[simplicial objects in Cat]]** may be called exactly that.  They may equivalently be regarded as [[internal categories]] in simplicial sets.

1. A **simplicial category** also frequently means a category [[enriched category|enriched]] over the category of [[simplicial sets]] ([Quillen 67, II.1](#Quillen67)), i.e. an [[sSet]]-[[enriched category]].  Such categories can be identified with simplicial objects in [[Cat]] all of whose face and degeneracy morphisms are [[bo functor|bijective on objects]].  To avoid ambiguity, categories enriched over simplicial sets may be called **[[simplicially enriched category|simplicially enriched categories]]**.

The analogous issue arises for "[[simplicial groupoids]]" etc., see also there.

Of course there are close relations between these three meanings. In particular [[simplicially enriched categories]] may be identified with those [[simplicial objects in Cat]] whose face and degeneracy maps are constant on [[objects]] and only affect the [[morphisms]]. 

An example of a text that speaks about what elsewhere are mostly regarded as [[simplicially enriched categories]] as [[simplicial objects in Cat]] which are constant on objects is ([Lydakis 98, around def. 3.2, remark 3.6](#Lydakis98)).

## Related concepts

* **simplicial category**

  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[simplicial groupoid]]

* [[relation between quasi-categories and simplicial categories]]

## References

* {#Quillen67} [[Dan Quillen]], chapter II, section 1 of _Homotopical algebra_, Lecture Notes in Mathematics __43__, Springer-Verlag 1967, iv+156 pp.


* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))


[[!redirects simplicial categories]]