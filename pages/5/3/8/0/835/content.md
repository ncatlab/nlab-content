
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[groupoid]]

* **$2$-groupoid**

* [[3-groupoid]]

* [[∞-groupoid]]

***

# Contents
* table of contents
{:toc}

## Idea

A **$2$-groupoid** is 

* a [[(n,r)-category|(2,0)-category]]

* a [[2-category]] in which all morphisms are [[equivalence]]s

* an [[n-groupoid]] for $n = 2$

* a $2$-[[truncated]] [[∞-groupoid]].


## Definition

Fix a meaning/model of [[∞-groupoid]], however weak or strict you wish. Then a __$2$-groupoid__ is an $\infty$-groupoid such that all [[parallel pair]]s of $j$-morphisms are [[equivalence|equivalent]] for $j \geq 3$. Thus, up to [[equivalence of categories|equivalence]], there is no point in mentioning anything beyond $2$-morphisms, except whether two given parallel $2$-morphisms are equivalent. This definition may give a concept more general than your preferred definition of $2$-groupoid, but it will be equivalent; basically, you may have to rephrase equivalence of $2$-morphisms as [[equality]].


## Specific models

There are various objects that model the abstract notion of $2$-groupoid.

* A **[[bigroupoid]]** is a [[bicategory]] in which all morphisms are [[equivalences]].

* A $3$-[[coskeleton|coskeletal]] [[Kan complex]] is precisely the [[Duskin nerve]] of a bigroupoid. 

  More generally one may consider a [[Kan complex]] that is just [[homotopy equivalent]] to a $3$-coskeletal one as a $2$-groupoid -- precisely: as representing the same [[homotopy type]], namely a [[homotopy 2-type]].


## Strict $2$-groupoids

The general notion of $2$-groupoid above is also called __weak $2$-groupoid__ to distinguish from the special case of **[[strict 2-groupoids]]**. A strict $2$-groupoid is a [[strict 2-category]] in which all morphisms are strictly invertible. This is equivalently a [[Grpd]]-[[enriched category]].


[[!redirects 2-groupoid]]
[[!redirects 2-groupoids]]

[[!redirects weak 2-groupoid]]
[[!redirects weak 2-groupoids]]
