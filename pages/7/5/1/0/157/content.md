
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Foundations
+--{: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A [[category]] is said to be **locally small** if each of its  [[hom-set|hom-sets]] is a [[small set]], i.e., is a [[set]] instead of a [[proper class]].  Local smallness is included by some authors in the definition of "category."

In other words, a locally small category is a $Set$-category, i.e. a category [[enriched category|enriched in]] the category [[Set]].

If [[Grothendieck universe]]s are used to handle [[size issues]], then one speaks of a **locally $U$-small** category if all [[hom-set|hom-sets]] are elements of $U$, or of a $U\Set$-category or simply of a $U$-category.

Compare with [[small category]]; a category is **small** if it is locally small and its set of objects is also a set.  (Some care must be taken if you want this definition to be non-[[evil]].)


## Remarks

Local smallness is an instance of a general scheme by which a category may be called "locally $P$" if all hom-sets satisfy property $P$.  This is more commonly used in [[enriched category theory]] where the [[hom-objects]] have more structure than a set and can support more interesting properties.

For instance, a topologically enriched category may be said to be _locally discrete_ if its [[hom-space]]s have [[discrete space|discrete]] topologies (hence it is essentially just an ordinary category).  Likewise, a [[2-category]] is said to be _locally discrete_ if its [[hom-category|hom-categories]] are [[discrete category|discrete]] (so it is essentially an ordinary category), _locally groupoidal_ if its hom-categories are [[groupoid|groupoids]], and so on.

However, this use of the word "locally" does not really have anything to do with the intuitive _geometrical_ meaning of "local," so it should not be taken too literally, especially when one is dealing with [[internal category|internal categories]] in spaces.  Furthermore, in other contexts a category is often said to be "locally $P$" if it has the completely unrelated property that all its [[over category|slice categories]] satisfy property $P$; see for instance [[locally cartesian closed category]].  Confusion is rarely created, however, because the properties $P$ that one is interesting in applying to hom-sets are usually quite different from those that one applies to slice categories.

## Related concepts

* [[small category]] , **locally small category**

* [[large category]]


[[!redirects locally small]]
[[!redirects locally small categories]]