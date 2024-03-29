+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Multilinear maps between [[locally convex topological vector spaces]] are important in many respects not least because of their use in infinite dimensional calculus as the homes of higher derivatives.  However, outside the realm of [[normed vector spaces]], there is no natural choice of topology on the spaces of multilinear maps.

## Definition

The definition of an $n$-linear map is straightforward and is an application of the definition at [[bilinear map]].

+-- {: .num_defn #mult}
###### Definition
Let $V$ and $W$ be [[vector spaces]] and $n \in \mathbb{N}$.  The space of $n$-linear mappings $V \to W$, written $L^n(V,W)$, is the space of set maps $V^n \to W$ with the property that they are linear in each variable.

For $n = 1$ we write $L(V,W)$ and we extend the notation to $n = 0$ where by $L^0(V,W)$ we mean just $W$.
=--

When $V$ and $W$ are [[LCTVS]] we can restrict to continuous maps.

+-- {: .num_defn #cmult}
###### Definition
Let $V$ and $W$ be [[locally convex topological vector spaces]] and $n \in \mathbb{N}$.  The space of continuous $n$-linear mappings $V \to W$, written $\mathcal{L}^n(V,W)$, is the space of continuous maps $V^n \to W$ with the property that they are linear in each variable.

For $n = 1$ we write $\mathcal{L}(V,W)$ and we extend the notation to $n = 0$ where by $\mathcal{L}^0(V,W)$ we mean just $W$.
=--

There are a variety of topologies that one can put on the spaces $\mathcal{L}^n(V,W)$.  The most common are the topologies of uniform convergence on some family of [[bounded sets]] of the source.

+-- {: .num_defn #cmtop}
###### Definition
Let $V$ and $W$ be [[LCTVS]] and $n \in \mathbb{N}$.  Let $\mathcal{S}$ be a collection of [[bounded subsets]] of $V$ which covers $V$.  Define $\Lambda_{\mathcal{S}}$ to be the topology on $\mathcal{L}^n(V,W)$ given by uniform convergence on $\mathcal{S}$.  That is, it is the [[LCTVS]] structure on $\mathcal{L}^n(V,W)$ defined by the family of [[semi-norms]]:
$$
\rho(u)_{\sigma,S} \coloneqq \sup \{\sigma(u(h_1,\dots,h_n)) : h_i \in S\}
$$
where $S \in \mathcal{S}$ and $\sigma \colon W \to \mathbb{R}$ is a continuous semi-norm on $W$.

We write $\mathcal{L}^n_{\mathcal{S}}(V,W)$ for the [[LCTVS]] with underlying vector space $\mathcal{L}^n(V,W)$ and topology $\Lambda_{\mathcal{S}}$.
=--

The commonest families in use are:

1. The finite subsets.  This resulting topology is known as the **simple** topology and the usual notations are $\Lambda_s$ and $\mathcal{L}_s(V,W)$.
1. The compact subsets, with notations $\Lambda_k$ and $\mathcal{L}_k(V,W)$.
1. The [[precompact subsets]], with notations $\Lambda_{p k}$ and $\mathcal{L}_{p k}(V,W)$.
1. The [[bounded subsets]], with notations $\Lambda_b$ and $\mathcal{L}_b(V,W)$.

Of all the topologies definable using Definition \ref{cmtop}, the topology $\Lambda_s$ is the coarsest and $\Lambda_b$ the finest.

The topology of simple convergence ($\Lambda_s$) also makes sense on the spaces $L^n(V,W)$ and we write $L_s^n(V,W)$ for the resulting LCTVS.  We have that $\mathcal{L}_s^n(V,W) \subseteq L^n_s(V,W) \subset W^{V^n}$ (with the product topology) are topological embeddings.

## Properties

1. For any suitable family of [[bounded sets]], $\mathcal{S}$, the natural map $\mathcal{L}_{\mathcal{S}}^{n+m}(V,W) \to \mathcal{L}_{\mathcal{S}}^n(V,\mathcal{L}_{\mathcal{S}}^m(V,W))$ is a topological embedding.

1. If $V$ is [[metrisable]], $W$ arbitrary, and $\mathcal{S}$ contains all [[compact]] sets then $\mathcal{L}_{\mathcal{S}}^{n+m}(V,W) \to \mathcal{L}_{\mathcal{S}}^n(V,\mathcal{L}_{\mathcal{S}}^m(V,W))$ is an isomorphism.

1. If $V$ is [[metrisable]] and [[barrelled]], $W$ arbitrary, and $\mathcal{S}$ arbitrary then $\mathcal{L}_{\mathcal{S}}^{n+m}(V,W) \to \mathcal{L}_{\mathcal{S}}^n(V,\mathcal{L}_{\mathcal{S}}^m(V,W))$ is an isomorphism.

## Separate Continuity

The definition of $\mathcal{L}^n(V,W)$ requires the maps $V^n \to W$ to be continuous in the product topology.  On the other hand, the linearity is required only on a per-factor basis.  It is possible to make the continuity requirement also work on a per-factor basis using the notion of [[hypocontinuity]].  For this we need to fix the type of continuity first.

+-- {: .num_defn #smult}
Let $V$ and $W$ be [[LCTVS]] and $n \in \mathbb{N}$.  Let $\mathcal{S}$ be a family of [[bounded subsets]] of $V$ which cover $V$.  We define $\mathcal{H}^n_{\mathcal{S}}(V,W)$ inductively by:

1. $\mathcal{H}^0(V,W) \coloneqq W$
2. $\mathcal{H}^n_{\mathcal{S}}(V,W) \coloneqq \mathcal{L}_{\mathcal{S}}(V, \mathcal{H}^{n-1}_{\mathcal{S}}(V,W))$.
=--

## Properties

1. $\mathcal{L}^n_{\mathcal{S}}(V,W) \to \mathcal{H}^n_{\mathcal{S}}(V,W)$ is a topological embedding.
1. If $\mathcal{S} \subseteq \mathcal{S}'$ then $\mathcal{H}^n_{\mathcal{S}'}(V,W)$ injects continuously into $\mathcal{H}^n_{\mathcal{S}}(V,W)$.
2. $\mathcal{H}^n_s(V,W)$ consists of the [[separately continuous]] multilinear maps $V^n \to W$.
3. If $V$ is [[metrisable]] and $\mathcal{S}$ contains all compact sets, or if $V$ is [[metrisable]] and [[barrelled]], then for any $W$ and $n$, $\mathcal{L}^n_{\mathcal{S}}(V,W) = \mathcal{H}^n_{\mathcal{S}}(V,W)$.

## Convergence Structures

A [[topological vector space]] defines a [[convergence vector space]] with the same underlying vector space and the same continuous mappings (that is to say, the functor from topological vector spaces to convergence vector spaces is full and faithful and respects the vector space functor).
The construction of the spaces of continuous multilinear operators makes sense for convergence vector spaces as well as for topological ones.
The resulting spaces of multilinear operators has several useful structures as a [[convergence vector space]] which are not topological.

+-- {: .num_defn #cvs}
###### Definition
Let $V$ and $W$ be [[convergence vector spaces]].  The **continuous convergence** structure on $\mathcal{L}^n(V,W)$ is the coarsest convergence structure which makes the evaluation map $\mathcal{L}^n(V,W) \times V^n \to W$ continuous.  The resulting convergence space (which is a convergence vector space) is written $\mathcal{L}^n_c(V,W)$.

The structure of **bounded convergence** (resp. **quasi-bounded convergence**) on $\mathcal{L}^n(V,W)$ is defined by the following requirement: for every filter $\mathcal{F}$ on $\mathcal{L}^n(V,W)$ and every $u \in \mathcal{L}^n(V,W)$ then $\mathcal{F} \to u$ if and only if $(\mathcal{F} - u)(\mathcal{B}^n) \to 0$ in $W$ for every bounded (resp. quasi-bounded) filter $\mathcal{B}$ on $V$.
The resulting convergence vector space is written $\mathcal{L}_b^n(V,W)$ (resp. $\mathcal{L}_{q b}^n(V,W)$.
=--

Recall that a filter is *bounded* if it contains a bounded set and is *quasi-bounded* if the filter $\mathcal{V} \cdot \mathcal{F} \to 0$ where $\mathcal{V}$ is the filter of $0$-neighbourhoods in $\mathbb{R}$.

If both $V$ and $W$ are LCTVS then the two notions of bounded convergence agree.