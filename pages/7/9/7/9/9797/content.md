
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

## Idea

A **nuclear vector space** is a [[locally convex topological vector space]] that is as far from being a [[normed vector space]] as possible.  Any map from a nuclear space into a [[normed vector space]] is compact, whence the only normed nuclear spaces are finite dimensional.

Nuclear spaces have very good properties with regard to [[topological tensor product]]s and [[dual vector space|duality]].


## Definition

To define a nuclear space we need to start with the concept of a nuclear map, first between [[Banach spaces]].

Let $E$ and $F$ be [[Banach spaces]].  Let $\mathcal{L}(E,F)$ be the Banach space of continuous linear maps $E \to F$.  Let $E^*$ denote the dual Banach space of $E$.  Let $E^* \widetilde{\otimes} F$ denote the completion of the [[projective tensor product]] of $E^*$ and $F$.  The bilinear map $E^* \times F \to \mathcal{L}(E,F)$ extends to a continuous linear map $E^* \widetilde{\otimes} F \to \mathcal{L}(E,F)$ (which might not be injective).

+-- {: .num_defn #nnmap}
###### Definition
Let $E$ and $F$ be Banach spaces.  A linear map $f \colon E \to F$ is **nuclear** if it lies in the image in $\mathcal{L}(E,F)$ of the completion of the projective tensor product $E^* \widetilde{\otimes} F$.
=--

From the notion of nuclear maps between Banach spaces we can define nuclear maps between arbitrary [[LCTVS]].  In essence, a linear map between arbitrary LCTVS is nuclear if it factors through a nuclear map of Banach spaces.

To make this precise, we need to recall how to associate Banach spaces to certain subsets of an LCTVS.  Let $E$ be an LCTVS and $U \subseteq E$ a [[convex set|convex]] [[circled set|circled]] $0$-neighbourhood.  Then we can define a Banach space $\widetilde{E}_U$ as follows: as $U$ is convex and circled, its [[Minkowski functional]] is a [[semi-norm]] on $E$.  The quotient $E_U \coloneqq E/\ker U$ is therefore a [[normed vector space]].  As $U$ is a $0$-neighbourhood, the quotient mapping defines a continuous linear function $E \to E_U$.  We define $\tilde{E}_U$ to be the Banach completion of $E_U$.

There is a dual notion.  Let $F$ be an LCTVS and $B \subseteq F$ a convex, circled, and [[bounded subset]] of $F$.  Let $F_B$ be the span of $B$ in $F$.  Then $B$ is [[absorbing]] in $F_B$ and so its Minkowski functional is defined.  If $F$ is [[Hausdorff]] then $B$ cannot contain a linear subspace and thus $F_B$ is a normed vector space.  We cannot complete $F_B$ to a Banach space but it might so happen that it is one.  As $B$ is bounded, the inclusion $F_B \to F$ is continuous.

(There is no danger of confusing the two notations since if $E$ admits a bounded $0$-neighbourhood then it is a normed vector space.)

Now we say that a continuous linear map $f \colon E \to F$ is **bounded** if for some $0$-neighbourhood $U$ of $E$ (which we may take to be [[circled set|circled]] and [[convex set|convex]]), $f(U)$ is bounded in $F$.  In which case, $f$ factors through a continuous map $f_{U,B} \colon E_U \to F_B$ where $B \subseteq F$ is bounded and contains $f(U)$.

+-- {: .num_defn #nmap}
###### Definition
Let $E$ and $F$ be LCTVS.  A linear map $f \colon E \to F$ is **nuclear** if there exists a [[convex set|convex]] [[circled set|circled]] $0$-neighbourhood, say $U$, in $E$ and a [[convex set|convex]] [[circled set|circled]] [[bounded set|bounded]], say $B$, in $F$ with $F_B$ complete such that $f(U) \subseteq B$ and the associated map $f_{U,B} \colon \tilde{E}_U \to F_B$ is nuclear.
=--

The following characterisation of nuclear maps is often helpful.

+-- {: .num_lemma #nchar}
###### Lemma
A linear map $f \colon E \to F$ is nuclear if and only if it is of the form:
$$
u(x) = \sum_{n=1}^\infty \lambda_n f_n(x) y_n
$$
where $\sum_{n=1}^\infty {|\lambda_n|} \lt \infty$, $\{f_n\}$ is an [[equicontinuous]] sequence in $E^*$, and $\{y_n\}$ is a sequence in $F$ contained in a convex, circled, bounded subset $B$ such that $F_B$ is complete.
=--

Now that we have the notion of a nuclear map, we can define a nuclear space.

+-- {: .num_defn #nsp}
###### Definition
A [[LCTVS]] $E$ is nuclear if it has a base $\mathcal{B}$ of convex circled $0$-neighbourhoods such that for $V \in \mathcal{B}$ the canonical mapping $E \to \tilde{E}_V$ is nuclear.
=--


## Properties

1. The following are equivalent:
    1. $E$ is nuclear,
    1. Every continuous linear map of $E$ into any Banach space is nuclear,
    1. Every convex, circled $0$-neighbourhood $U$ contains another, say $V$, such that the canonical map $\tilde{E}_V \to \tilde{E}_U$ is nuclear.
1. Every bounded subset of a nuclear space is precompact.
1. The completion of a nuclear space is a nuclear space.
1. A nuclear space is a projective limit of $\ell^p$ spaces (in particular, of [[Hilbert spaces]]).
1. Nuclearity is inherited by the following constructions: subspaces, separated quotients, arbitrary products, locally convex direct sum of a countable family, projective limits, countable inductive limits.
1. The [[projective tensor product]] (and its completion) of two nuclear spaces is nuclear.


## Examples

1. Any finite dimensional vector space is nuclear,
1. For a finite dimensional smooth manifold $M$, $C^\infty(M)$ is nuclear,
1. The space of rapidly decreasing functions on $\mathbb{R}^n$ is nuclear,
1. The product an arbitrary number of copies of $\mathbb{R}$ is nuclear,
1. The direct sum of a countable number of copies of $\mathbb{R}$ is nuclear,
1. The direct sum of $\mathbb{R}$-copies of $\mathbb{R}$ is *not* nuclear.


## References
* A. Grothendieck,  _Produits tensoriels topologiques et espaces nucl&#233;aires_, Memoirs of the Amer. Math. Soc. __16__, 190 pp. and 140 pp. (1955).
* [[Alexander Grothendieck]], _R&#233;sum&#233; des r&#233;sultats essentiels dans la th&#233;orie des produits tensoriels topologiques et des espaces nucl&#233;aires_, Annales de l'institut Fourier __4__ (1952), p. 73-112, [numdam](http://www.numdam.org/item?id=AIF_1952__4__73_0)


category: functional analysis

[[!redirects Nuclear space]]
[[!redirects nuclear space]]
[[!redirects nuclear spaces]]
[[!redirects nuclear vector space]]
[[!redirects nuclear vector spaces]]
[[!redirects nuclear topological vector space]]
[[!redirects nuclear topological vector spaces]]
