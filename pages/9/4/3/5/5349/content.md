
# Rank
* table of contents
{: toc}

## Idea

The term 'rank' is used in many contexts to number levels within a hierarchy.


## Rank of a module

Let $A$ be a [[ring]] and $N$ a [[module]] over $A$. If $A$ is a [[field]], then $N$ is a [[vector space]] and we speak of the _[[dimension]]_ of $N$; in the general case, we may speak of the _rank_:

A collection of elements $(w_i)_{i \in I}$ of $N$ is called a [[basis]] of $N$ (over $A$) if for every $x \in N$ there is a unique collection $(a_i)_{i \in I}$ of elements of $A$ such that $a_i = 0$ for all but finitely many $i \in I$ and $x = \sum_{i \in I} a_i w_i$. 

If $N$ has a basis it is called a _[[nLab:free module]]_ (over $A$). For many examples of $A$ (the __invariant basis number rings__), the [[cardinality]] $# I$ only depends on $N$ and not on the choice of basis. It is called the **rank** of $N$ over $A$, notation: $rank_A(M)$. In any case, $N$ is called the __free module of rank $# I$__. If $N$ is a [[finitely generated]] free module then the rank is a [[finite number]].

All of the following are invariant basis rings (source: [Wikipedia](http://en.wikipedia.org/wiki/Invariant_basis_number)):

*  any nontrivial [[commutative ring]] $K$,

*  the [[group ring]] $K(G)$ for $K$ any [[field]] (or nontrival commutative ring?) and $G$ any [[group]],

*  any [[Noetherian ring]].

Besides the [[trivial ring]] (over which any module is free with any set as basis), an example of a ring without invariant basis number is the ring of $\aleph_0$-dimensional square [[matrix|matrices]] (over any ring) in which each column has only finitely many nonzero entries (which allows multiplication to be defined).  As a module over itself, this ring is free on any inhabited finite set, as may be shown by using the equation $\aleph_0 = n \aleph_0$ (applied to the columns).

## Rank of a linear map
 {#RankOfALinearMap}

Given a [[linear map]], hence a [[homomorphism]] of [[modules]], its rank is the rank of its [[image]]-module.

Often this is considered for the case that the linear map is represented by a [[matrix]] and one speaks of the *rank of a matrix*.

## Rank of a sheaf of modules

Let $(X,\mathcal{O})$ be a [[locally ringed space]] and $\mathcal{E}$ a $\mathcal{O}$-module. Then its _rank_ at a point $x \in X$ is the vector space dimension of the [[fiber]] $\mathcal{E}(x) \coloneqq \mathcal{E}_x \otimes_{\mathcal{O}_x} k(x)$ over the [[residue field]] $k(x)$.

If $\mathcal{E}$ is of [[coherent sheaf|finite type]], then the rank at $x$ can equivalently be defined as the minimal number of elements needed to generate the stalk $\mathcal{E}_x$ as a $\mathcal{O}_x$-module (by [[Nakayama's lemma]]). In this case, the rank is a [[semicontinuous map|upper semicontinuous]] function $X \to \mathbb{N}$.

In the [[internal logic|internal language]] of the sheaf topos $\mathrm{Sh}(X)$, the rank of $\mathcal{E}$ can internally quite simply be defined as the minimal number of elements needed to generate $\mathcal{E}$ (taken as an element of the suitably completed natural numbers, i.e. the poset of inhabited upper sets). Under the correspondence of internal inhabited upper sets in $\mathrm{Sh}(X)$ and upper semicontinuous functions $X \to \mathbb{N}$ (details at _[[one-sided real number]]_), this definition coincides with the usual one if $\mathcal{E}$ is of finite type; see [this MathOverflow question](http://mathoverflow.net/questions/34412/the-upper-semi-continuous-rank-of-a-module-sheaf).

See also _[[rank of a coherent sheaf]]_.

## Rank of a vector bundle

As a simple special case of the above, a [[vector bundle]] is said to have _rank $n$_ if each [[fiber]] is a [[vector space]] of [[dimension]] $n$. 

## Hereditary rank of a pure set

Every [[pure set]] within the [[von Neumann hierarchy]] appears first at some level given by an [[ordinal number]]; this number is its __hereditary rank__.

We may define this rank explicitly (and [[recursion|recursively]]) as follows:

$$ rank S = \bigcup_{x \in S} (rank x)^+ ,$$

where $\bigcup$ is the [[supremum]] operation on ordinals (literally the [[union]] for [[von Neumann ordinals]]) and $(-)^+$ is the [[successor]] operation (which is $a \mapsto a \cup \{a\}$ for von Neumann ordinals).

## Rank of a functor

Recall that a [[cardinal number]] $\alpha$ is said to be _regular_ if $|\bigcup_{i\in I} X_i |$&lt;$\alpha$ whenever $|I|$&lt;$\alpha$ and $|X_i|$&lt;$\alpha$ for all $i\in I$.

A functor $F:\mathcal{A}\to \mathcal{B}$  _has rank_ $\alpha$ for some regular cardinal $\alpha$ if $F$ preserves $\alpha$-[[filtered colimit|filtered colimits]]. $F$ _has rank_ when it has rank $\alpha$ for some regular cardinal $\alpha$. A monad has rank ($\alpha$) when its underlying endofunctor does.

The properties of functors with rank are discussed in section 5.5 of Borceux ([1994](#Borceux2)).

## Rank of a Lie group

* [[rank-nullity theorem]]

* [[rank of a Lie group]]

* [[rank of a coherent sheaf]], 

  [[degree of a coherent sheaf]]

  [[slope of a coherent sheaf]]

* [[stable coherent sheaf]], [[Bridgeland stability condition]]

## Related concepts

* [[rank-nullity theorem]]


## References

* {#Borceux2}[[Francis Borceux]], _[[Handbook of Categorical Algebra]] vol. 2_ , Cambridge UP 1994.

[[!redirects ranks]]

[[!redirects rank of a vector bundle]]
[[!redirects rank of vector bundles]]

[[!redirects monad rank]]
[[!redirects monad with rank]]

[[!redirects rank of a linear map]]
[[!redirects ranks of linear maps]]

[[!redirects rank of a matrix]]
[[!redirects ranks of matrices]]


