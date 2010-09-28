
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents
{:toc}

## Definition of strict case 

A **$0$-fold category** is a [[set]].  An **$n$-fold category** for $n \gt 0$ is an [[internal category]] in $(n-1)$-fold categories.  An $n$-fold category is also known as an **$n$-tuple category**.

In particular, a $1$-fold category is preciesely a [[category]], and a $2$-fold category is precisely a [[double category]] (introduced by [[Charles Ehresmann]] in 1963).

Analogously, a **$0$-fold groupoid** is again a set, and an **$n$-fold groupoid** is an [[internal groupoid]] in $(n-1)$-fold groupoids; in particular, a $1$-fold groupoid is a [[groupoid]].

More generally, an **$(n,r)$-fold groupoid** is an $r$-fold category in $(n-r)$-fold groupoids; compare $(n,r)$-[[(n,r)-category|category]].


## Remarks ##

* Notice that an $n$-fold category is a _strict_ version of an [[n-category]] in that all $n$ composition operations are strictly unital and associative and strictly commute with each other. Still, $n$-fold groupoids model all [[homotopy n-type]]s. See [[homotopy hypothesis]].

* Analogous to how a [[group]] is a groupoid with a single object, one can consider $(n+1)$-fold groupoids for which all morphisms in one of the $(n+1)$ directions are endomorphisms. These are the [[cat-n-group]]s.

* By a theorem by Brown and Higgins, [[strict omega-category|strict omega-categories]] are equivalent to those $\infty$-fold categories that satisfy a couple of restrictive properties (something like that all 1-categories of $n$-cells for all $n$ are the same and that all the "thin" identity elements exist, called "connections").

* There are some moves towards a weak notion of $n$-fold category, particularly the case of [[double bicategory]].


## References ##

* Thomas M. Fiore, Simona Paoli, _A Thomason Model Structure on the Category of Small $n$-fold Categories_ ([arXiv](http://arxiv.org/abs/0808.4108))

* [[Ronnie Brown]] and P.J. Higgins, The equivalence of $\infty$-groupoids and crossed  complexes,  Cah. Top. G\'eom. Diff.  22 (1981) 371--386.


[[!redirects n-fold categories]]
[[!redirects n-tuple category]]
[[!redirects n-tuple categories]]