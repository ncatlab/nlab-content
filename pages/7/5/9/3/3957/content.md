#Contents#
* tic
{:toc}

##Idea

A convenient vector spaces is a [[locally convex topological vector space]] satisfying a certain [[complete locally convex topological vector space|completeness]] property.  Loosely, the completeness property is that such that "all derivatives which ought to exist actually do".

The term _convenient vector space_ was introduced by Kriegl and Michor as part of their theory of global analysis.  It is equivalent to the notion _locally complete_ which is more usual in [[functional analysis]].

## Definition

There are various equivalent definitions of a _convenient_ vector space, a long list is given in Theorem 2.14 of [KM](#KM).  We shall give the definition that is closest to its _raison d'etre_, namely the existence of derivatives.

+-- {: .num_defn #ConSp}
###### Definition
A [[locally convex topological vector space]] is said to be **convenient** or **$c^\infty$-complete** if whenever $c \colon \mathbb{R} \to E$ is a curve such that $l \circ c \colon \mathbb{R} \to \mathbb{R}$ is smooth for all $l \in E^*$ then $c$ is smooth.
=--

We shall give one other characterisation which recasts the definition in language more common in functional analysis.

+-- {: .num_defn #LocCpt}
###### Definition
A [[locally convex topological vector space]], $E$, is said to be **locally complete** if for $B \subseteq E$ a [[bounded]], [[closed]], [[absolutely convex]] subset then its norm space, $E_B$, is a Banach space.
=--

The equivalence of these two forms part of Theorem 2.14 of [KM](#KM).

## Examples

* A [[Cartesian space]] $\mathbb{R}^n$ carries a unique structure of a convenient vector space.

* For $X$ and $Y$ to convenient vector spaces, the vector space of [[smooth function]]s $C^\infty(X,Y)$ is again a convenient vector space. This is to a large degree the motivating example. It makes the category of convenient vector spaces by Cartesian closed. (See below).

## Properties

* The [[category]] of convenient vector spaces and [[smooth function]]s between them is a [[cartesian closed category]].

* The definition of a convenient vector space has a natural interpretation in terms of [[Frölicher space]]s. It may also be related to [[synthetic differential geometry]]: convenient vector spaces form a [[full subcategory]] of the [[Cahiers topos]].

##Reference

* Andreas Kriegl, Peter Michor: _the convenient setting of global analysis_ (free download [here] (http://www.ams.org/publications/online-books/surv53-index))
{#KM}

Convenient vector spaces from the point of view of [[generalized smooth space]]s are considered in 

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17, ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))



[[!redirects convenient vector spaces]]
[[!redirects locally complete topological vector space]]
[[!redirects locally complete]]
[[!redirects locally complete vector space]]