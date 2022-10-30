
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An the notion of _$n$-fold category_ is what is obtained by iterating the process of forming [[internal categories]] $n$-times: an $0$-fold category is just an object of the ambient category (say a [[set]]) and then inductively an $n+1$-fold category is a [[internal category]] in the category of $n$-fold categories.

If the ambient category is instead an [[(∞,1)-category]] such as [[∞Grpd]], then an $n$-fold category is an _[[n-fold complete Segal space]]_, see there for more details.

## Definition

### $n$-Fold categories

A **$0$-fold category** is a [[set]].  A (strict) **$n$-fold category** for $n \gt 0$ is an [[internal category]] in the category of $(n-1)$-fold categories.  An $n$-fold category is also known as an **$n$-tuple category**.

In particular, a $1$-fold category is preciesely a [[category]], and a $2$-fold category is precisely a [[double category]] (introduced by [[Charles Ehresmann]] in 1963).

### $n$-Fold groupoids

Analogously, a **$0$-fold groupoid** is again a set, and an **$n$-fold groupoid** is an [[internal groupoid]] in $(n-1)$-fold groupoids; in particular, a $1$-fold groupoid is a [[groupoid]].

Analogous to how a [[group]] is a groupoid with a single object, one can consider $(n+1)$-fold groupoids for which all morphisms in one of the $(n+1)$ directions are endomorphisms. These are the _[[cat-n-groups]]_.

More generally, an **$(n,r)$-fold groupoid** is an $r$-fold category in $(n-r)$-fold groupoids; compare $(n,r)$-[[(n,r)-category|category]].




## Properties
 {#Properties}

### Cartesian closure
 {#CartesianClosure}

The category of $n$-fold categories is a [[cartesian closed category]]. By [[induction]] from the statement at _[Internal category - Cartesian closure](internal+category#CartesianClosure)_.

### Homotopy types

Even though an $n$-fold category is a _strict_ version of an [[n-category]] in that all $n$ composition operations are strictly unital and associative and strictly commute with each other,  still $n$-fold _groupoids_ model all [[homotopy n-types]]. See [[homotopy hypothesis]].

### Relation to strict $\omega$-categories

By a theorem by Brown and Higgins, [[strict omega-category|strict omega-categories]] are equivalent to those $\infty$-fold categories that satisfy a couple of restrictive properties (something like that all 1-categories of $n$-cells for all $n$ are the same and that all the "thin" identity elements exist, called "connections").

## Related concepts

* [[double bicategory]]

* [[n-fold complete Segal space]]


## References ##

* Thomas M. Fiore, Simona Paoli, _A Thomason Model Structure on the Category of Small $n$-fold Categories_ ([arXiv](http://arxiv.org/abs/0808.4108))

* [[Ronnie Brown]] and P.J. Higgins, The equivalence of $\infty$-groupoids and crossed  complexes,  Cah. Top. G\'eom. Diff.  22 (1981) 371--386.


[[!redirects n-fold categories]]
[[!redirects n-tuple category]]
[[!redirects n-tuple categories]]

[[!redirects n-fold groupoid]]
[[!redirects n-fold groupoids]]
