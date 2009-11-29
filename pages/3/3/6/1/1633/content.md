# Localy compact spaces
* tic
{: toc}


## Definition

A locally compact space is a space such that every point has a [[compact space|compact]] neighborhood. It may be considered as an example of a [[nice topological space]]. 

Note: as observed in the discussion at [[compact space]], many authors choose to include the [[Hausdorff space|Hausdorff]] condition as a matter of course, calling locally compact not-necessarily-Hausdorff spaces 'locally quasi-compact'. We will not follow that convention here, but the reader should be warned that without the Hausdorff hypothesis, there are several inequivalent notions of local compactness in the literature; see [the English Wikipedia](https://secure.wikimedia.org/wikipedia/en/wiki/Locally_compact_space) for a survey and counterexamples. 


## Examples ## 

1. Clearly, any [[discrete space]] is locally compact. 

1. An open subspace of a compact space is locally compact. In fact, every locally compact space $X$ arises in this way, since it can be considered an open space in its one-point compactification $X \sqcup \{\infty\}$ (where the open neighborhoods of the adjoined point $\infty$ are precisely those of the form $K^c \sqcup \{\infty\}$, where $K^c$ is the complement of a compact subset $K \subseteq X$). 

1. The reals, complexes, and $\mathfrak{p}$-adic completions of [[algebraic number field]]s (with respect to a prime ideal $\mathfrak{p}$ in the ring of integers) are locally compact. In characteristic $p$, the field of Laurent series $\mathbb{F}_q((t))$ over a finite field with $q$ elements, topologized with respect to a discrete valuation, is locally compact. In fact, any non-discrete locally compact [[field]] must be of one of these types; they are called "local fields". 

1. Finite products of locally compact spaces are locally compact. Closed subspaces of locally compact spaces are locally compact. (Hence locally compact spaces form a [[finitely complete category]].) 

1. Topological [[manifold]]s (including "pathological examples" like [[long line]]s), being locally homeomorphic to $\mathbb{R}^n$, are locally compact. 

1. The only Hausdorff [[topological vector space]]s that are locally compact are finite-dimensional Euclidean spaces. More generally, a TVS is locally compact if and only if its Hausdorff quotient has finite dimension. 


## Basic category-theoretic results ## 

Perhaps the most important consequence of local compactness for categorical topology is that locally compact spaces are [[exponential object|exponentiable]], i.e., if $Y$ is locally compact, then $Y \times -: Top \to Top$ has a [[adjunction|right adjoint]] $(-)^Y: Top \to Top$. In fact, this is almost an abstract definition of local compactness: for $T_0$ spaces, local compactness is equivalent to being exponentiable. This situation generalises to [[locales]]: a result of Hyland is that locale is locally compact if and only if it is exponentiable.  (See [[exponential law for spaces]] for more details.)

As noted above, locally compact spaces form a finitely complete [[full subcategory]] of $Top$. It is not true that arbitrary products of locally compact spaces are locally compact. However, some important examples of locally compact spaces are constructed as restricted direct products, as follows. 

Let $(X_p, K_p)_{p \in P}$ be a collection of pairs of spaces where each $X_p$ is locally compact and $K_p \subseteq X_p$ is a compact _open_ subspace. The **restricted direct product** of the collection is the colimit of the [[filtered category|filtered diagram]] consisting of spaces 
$$D_F = \prod_{p \in F} X_p \times \prod_{p \notin F} K_p$$ 
where $F$ ranges over all finite subsets of $P$, together with inclusions $D_F \subseteq D_{F'}$ where $F \subseteq F'$. We observe that each of the $D_F$ is locally compact, and that a filtered colimit or union of a system of _open_ inclusions of locally compact spaces is again locally compact. Therefore, restricted direct products are locally compact, under the hypotheses stated above. 

These hypotheses are of course pretty severe; the main examples of such restricted direct products, as many readers will be aware, include topologized [[adele ring]]s and [[idele group]]s. In the case of adele rings, the collection of pairs is $(K_{\mathfrak{p}}, O_{\mathfrak{p}})$ where $K_{\mathfrak{p}}$ is the $\mathfrak{p}$-adic completion of a [[number field]] $K$ and $O_{\mathfrak{p}}$ is the $\mathfrak{p}$-adic completion of the ring of integers $O \subseteq K$. 

Locally compact spaces are closed under [[coproduct]]s in $Top$. They do not admit many types of [[colimit]]s generally; in some sense this is a _raison d\'&#234;tre_ for [[compactly generated space]]s: they are precisely the colimits in $Top$ of diagrams of locally compact spaces. 


## Further properties #

Locally compact Hausdorff spaces are [[paracompact space|paracompact]] whenever they are also [[second countable space|second countable]].


[[!redirects locally compact Hausdorff space]]