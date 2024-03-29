
# Contents
* table of contents
{: toc}

## Idea

A _bornological set_ is a notion of [[space]], where instead of considering [[open sets]] and [[continuous functions]] whose [[inverse images]] preserve open sets as one does for [[topological space]]s, one considers [[bounded sets]] (which constitute a _bornology_) and [[bounded maps]] whose [[direct images]] preserve bounded sets. Bornological [[topological vector spaces]], called [[bornological spaces]], are important in [[functional analysis]].


## Definitions

Let $X$ be a [[set]]. A **bornology** on $X$ is a collection $\mathcal{B} \subseteq P X$ of [[subsets]] of $X$ such that 

* $\mathcal{B}$ covers $X$: $\bigcup_{B \in \mathcal{B}} B = X$, 

* $\mathcal{B}$ is downward-closed: if $B \in \mathcal{B}$ and $A \subseteq B$, then $A \in \mathcal{B}$, 

* $\mathcal{B}$ is closed under finite unions: if $B_1 \ldots, B_n \in \mathcal{B}$, then $\bigcup_{1 \leq \i \leq n} B_i \in \mathcal{B}$. 

A **bornological set** is a set $X$ equipped with a bornology. The elements of $\mathcal{B}$ are called the **[[bounded sets]]** of a bornological set. 

If $X$, $Y$ are bornological sets, a [[function]] $f\colon X \to Y$ is said to be **[[bounded function|bounded]]** if $f(B)$ is bounded in $Y$ for every bounded $B$ in $X$. One obtains a category of bornological sets and bounded maps. 


## Examples

* If $X$ is any [[topological space]] such that every point is closed, then there is a bornology consisting of all [[precompact subsets]] of $X$ (subsets whose closure is [[compact set|compact]]).  Any [[continuous map]] is bounded with respect to this choice of bornology. 

* If $X$ is any [[metric space]], there is a bornology where a set is bounded if it is contained in some open [[ball]]. Any [[Lipschitz map]] is bounded with respect to this choice of bornology.  A metric space is __bounded__ if it\'s a bounded subspace of itself.

* If $X$ is a [[measure space]], then the subsets of the sets of finite measure form a bornology .

* For [[linear operators]] between [[bornological spaces]], a map is continuous if and only if it is bounded. 


## Properties

+-- {: .num_theorem}
###### Theorem 
The category of bornological sets is a [[quasitopos]], in fact a topological universe. 
=-- 

For a proof, see this [article](#AdamHerr) by Adamek and Herrlich. 

+-- {: .num_theorem} 
###### Theorem 
Let $Alg_{\mathbb{C}}$ be the category of (noncommutative) finite-dimensional algebras over $\mathbb{C}$, the field of complex numbers. Let 

$$U \colon Alg_{\mathbb{C}} \to Born$$ 

be the functor that takes an algebra $A$ to the set ${|A|}$ equipped with the bornology of precompact sets. Then there is a canonical identification of the monoid $Born^{Alg_\mathbb{C}}(U, U)$ with the monoid of entire holomorphic functions. 
=-- 

This was proved by [Schanuel](#Schanuel). 

## Related concepts

* [[bornological group]]

* [[bornological vector space]]

* [[bornological topos]]


## References 

* {#AdamHerr} [[Jiří Adámek]] and [[Horst Herrlich]], _Cartesian closed categories, quasitopoi, and topological universes_, Comm. Math. Univ. Carol., Vol. 27, No. 2 (1986), 235-257. ([web](http://dml.cz/handle/10338.dmlcz/106447))

* {#Hogbe-Nlend70}H. Hogbe-Nlend, _Les racines historiques de la bornologie moderne_ , pp.1-6 in _S&#233;minaire Choquet: Initiation &#224; l'analyse_ 10.1 (1970-1971).  ([numdam](http://www.numdam.org/item?id=SC_1970-1971__10_1_A5_0))

* {#ProsmansSchneiders} [[Fabienne Prosmans]], [[Jean-Pierre Schneiders]], _A homological study of bornological spaces_, December 2000, Prepublications Mathematiques de l'Universite Paris 13, 46. ([pdf](http://www.analg.ulg.ac.be/jps/rec/hsbs.pdf))

* {#Schanuel} [[Stephen Schanuel]], _Continuous extrapolation to triangular matrices characterizes smooth functions_, J. Pure App. Alg. 24, Issue 1 (1982), 59&#8211;71. ([web](http://www.sciencedirect.com/science/journal/00224049/24/1)) 

Review includes

* {#Bambozzi14} [[Federico Bambozzi]], section 1 of _On a generalization of affinoid varieties_ ([arXiv:1401.5702](http://arxiv.org/abs/1401.5702))


[[!redirects bornology]]
[[!redirects bornologies]]
[[!redirects bornological]]
[[!redirects bornological set]]
[[!redirects bornological sets]]

[[!redirects bounded space]]
[[!redirects bounded spaces]]

