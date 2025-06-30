
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

##Idea

A _convenient_ vector space is a [[locally convex topological vector space]] satisfying a certain [[completeness]] property.  Loosely, the completeness property is that "all derivatives which ought to exist actually do".

The term _convenient vector space_ was introduced by Kriegl and Michor as part of their theory of [[global analysis]].  It is equivalent to the notion _locally complete_ which is more usual in [[functional analysis]].


## Definition

There are various equivalent definitions of a __convenient vector space__; a long list is given in Theorem 2.14 of [KM](#KM).  We shall give the definition that is closest to its _raison d'&#234;tre_, namely the existence of derivatives.

+-- {: .num_defn #ConSp}
###### Definition 
A [[locally convex topological vector space]] $E$ is said to be **convenient** or **$c^\infty$-complete** if whenever $c \colon \mathbb{R} \to E$ is a [[curve]] such that $l \circ c \colon \mathbb{R} \to \mathbb{R}$ is [[smooth map|smooth]] for all $l \in E^*$ then $c$ is smooth.
=--

We shall give one other characterisation which recasts the definition in language more common in functional analysis.

+-- {: .num_defn #LocCpt}
###### Definition
A [[locally convex topological vector space]], $E$, is said to be **locally complete** if for $B \subseteq E$ a [[bounded subset|bounded]], [[closed subset|closed]], [[absolutely convex subset]], its [[norm space]], $E_B$, is a [[Banach space]].
=--

The equivalence of these two forms part of Theorem 2.14 of [KM](#KM).

Other equivalent characterizations of convenient vector spaces $E$ are:

* $E$ is a [[locally convex vector space]] and every [[Mackey-Cauchy sequence]] in $E$ converges.

* $E$ is a [[locally convex vector space]] and for every [[smooth map|smooth]] [[curve]] $c : \mathbb{R} \to E$ there is a curve $\int c$ (an [[antiderivative]] of $c$) such that $c$ is the [[derivative]] of $\int c$.

See for instance ([Blute](#Blute)).


## Examples

* A [[Cartesian space]] $\mathbb{R}^n$ carries a unique structure of a convenient vector space. This also holds for [[Fréchet spaces]] in general and countable strict locally convex [[inductive limits]] thereof. (See [[LF-space]]).

* For $X$ and $Y$ two convenient vector spaces, the vector space of [[smooth functions]] $C^\infty(X,Y)$ is again a convenient vector space. This is to a large degree the motivating example. It makes the category of convenient vector spaces be [[cartesian-closed category|Cartesian closed]]. (See below).


## Properties

* The [[category]] of convenient vector spaces and [[smooth functions]] between them is a [[cartesian closed category]].

* The definition of a convenient vector space has a natural interpretation in terms of [[Frölicher spaces]]. It may also be related to [[synthetic differential geometry]]: convenient vector spaces form a [[full subcategory]] of the [[Cahiers topos]] ([Kock 86](#Kock86), [Kock-Reyes 86](#KockReyes86)) and in fact already of the topos of [[smooth sets]], hence (being [[concrete object|concrete]]) of the category of [[diffeological spaces]] ([Kock-Reyes 04, p. 5](#KockReyes04)).


## Related concepts

* [[convenient manifold]]


## References

A standard textbook reference is

* {#KM} [[Andreas Kriegl]], [[Peter Michor]]: _The convenient setting of global analysis_, AMS (1997) ([pdf](http://www.mat.univie.ac.at/~michor/apbookh.pdf))
 

A survey is for instance in the slides

* {#Blute} [[Richard Blute]], _Convenient Vector Spaces, Convenient Manifolds and Differential Linear Logic_ (2011) ([pdf](https://web.archive.org/web/20211027014629/http://aix1.uottawa.ca/~rblute/FMCS.pdf))
 

Results on equivalent characterizations are for instance in

* Thomas E. Gilsdorf, _Strictly Webbed Convenient Locally Convex Spaces_, Int. Journal of Math. Analysis, Vol. 1, 2007, no. 16, 775 - 782 ([pdf](http://www.m-hikari.com/ijma/ijma-password-2007/ijma-password13-16-2007/gilsdorfIJMA13-16-2007.pdf))

The embedding of convenient vector spaces into the [[Cahiers topos]] and hence the treatment of their differential geometry by [[synthetic differential geometry]] is due to

* {#Kock86} [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))
  

and with a corrected definition of the site of definition in

* {#KockReyes86} [[Anders Kock]], [[Gonzalo Reyes]], _Corrigendum and addenda to: Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17 ([numdam](http://www.numdam.org/item?id=CTGDC_1987__28_2_99_0))
 
The stronger statement of embedding into [[diffeological spaces]] appears in

* {#KockReyes04} [[Anders Kock]], [[Gonzalo Reyes]], _Categorical distribution theory; heat equation_ ([arXiv:math/0407242](https://arxiv.org/abs/math/0407242))


[[!redirects convenient vector space]]
[[!redirects convenient vector spaces]]
[[!redirects convenient topological vector space]]
[[!redirects convenient topological vector spaces]]
[[!redirects convenient TVS]]
[[!redirects convenient TVSs]]
[[!redirects convenient TVSes]]
[[!redirects convenient TVS's]]
[[!redirects convenient TVS’s]]
[[!redirects convenient TVS\'s]]

[[!redirects locally complete]]
[[!redirects locally complete vector space]]
[[!redirects locally complete vector spaces]]
[[!redirects locally complete topological vector space]]
[[!redirects locally complete topological vector spaces]]
[[!redirects locally complete TVS]]
[[!redirects locally complete TVSs]]
[[!redirects locally complete TVSes]]
[[!redirects locally complete TVS's]]
[[!redirects locally complete TVS’s]]
[[!redirects locally complete TVS\'s]]
