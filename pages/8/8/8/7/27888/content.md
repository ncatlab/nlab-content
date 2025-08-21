+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Yang-Mills moduli space_ (short _YM moduli space_, also _instanton moduli space_) is the [[moduli space]] of the [[Yang-Mills equations]], hence the space of its solutions up to [[gauge]]. It is used in the proof of [[Donaldson's theorem]], which was listed as [[Simon Donaldson]]'s contributions for einning the [[Fields medal]], and to defined the [[Donaldson invariants]] used to study [[4-manifolds]]. A difficulity is, that the Yang-Mills moduli space is usually not compact and has to be compactified around singularities through laborious techniques. An improvement later appeared with the always compact [[Seiberg-Witten moduli space]]. The Yang-Mills moduli space is named after [[Chen Ning Yang]] and [[Robert Mills]], who introduced the underlying [[Yang-Mills equations]] in 1954.

In four dimensions, important subspaces of the Yang-Mills moduli space are the _self-dual Yang-Mills moduli space_ (short _SDYM moduli space_, also _self-dual instanton moduli space_) of solutions of the [[self-dual Yang-Mills equations]] up to gauge and the _anti self-dual Yang-Mills moduli space_ (short _ASDYM moduli space_, also _anti self-dual instanton moduli space_) of solutions of the [[anti self-dual Yang-Mills equations]] up to gauge. See also [[D=4 Yang-Mills theory]] and [[self-dual Yang-Mills theory]].

## Definition

Let $G$ be a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$ and $\pi\colon P\twoheadrightarrow X$ be a [[principal bundle|principal $G$-bundle]] over a [[smooth manifold]] $X$, which automatically makes $P$ a [[smooth manifold]] as well. Let $Ad(P)\coloneqq P\times_G\mathfrak{g}$ be the [[adjoint bundle]], then the [[Yang-Mills equations]] as well as the (anti) self-dual Yang-Mills equations are formulated on the _configuration space_:
$$
\mathcal{A}
=\Omega^1(X,Ad(P))
\cong\Omega_{Ad}^1(P,\mathfrak{g})
$$
where the isomorphism requires a choice of local sections $s_i\colon U_i\hookrightarrow P$ for an open cover $(U_i)_{i\in I}\subset X$ (or alternatively a connection since the latter space is an affine vector space, which makes the isomorphism non-canonical) and is then given by:
$$
\Omega_{Ad}^1(P,\mathfrak{g})\xrightarrow\cong\Omega^1(X,Ad(P)),
A\mapsto(s_i^*A)_{i\in I}.
$$
Since the configuration space is an infinite-dimensional [[vector space]], it is more difficult to handle. But also due to the group action on the [[principal bundle]], it is plausible to consider a [[group action]] on the configuration space with the following _gauge group_:
$$
\mathcal{G}
\coloneqq C^\infty(P,G)^G
\cong C^\infty(X,G)
\cong Aut(P)
$$
where the isomorphisms are given using the free and transitive action of $G$ on the fibers of $P$ (with $G$ as a superscript meaning the $G$-equivariant maps and which are canonical):
$$
C^\infty(X,G)\xrightarrow\cong Aut(P),
f\mapsto(p\mapsto p\cdot f(\pi(p)));
$$
$$
C^\infty(P,G)^G\xrightarrow\cong Aut(P),
f\mapsto(p\mapsto p\cdot f(p)).
$$
A principal bundle automorphism $P\rightarrow P$ induces a vector bundle automorphism $Ad(P)\rightarrow Ad(P)$, causing the gauge group $\mathcal{G}$ to act free on the configuration space $\mathcal{A}$ and resulting in the [[orbit space]]:
$$
\mathcal{B}
\coloneqq\mathcal{A}/\mathcal{G}.
$$
It can be shown that the [[Yang-Mills equations]] are gauge invariant and hence are formulated over just this orbit space. Its solution form the _Yang-Mills moduli space_:
$$
\mathcal{M}_P\colon
\coloneqq\{[A]\in\mathcal{A}|d_A\star F_A=0\}.
$$
If $X$ is a [[4-manifold]], then [[D=4 Yang-Mills theory]] furthermore allows the definition of the _(anti) self-dual Yang-Mills moduli space_:
$$
\mathcal{M}_P^-
=\mathcal{M}_P^\mathrm{ASD}\colon
\coloneqq\{[A]\in\mathcal{A}|d_AF_A=-F_A\};
$$
$$
\mathcal{M}_P^+
=\mathcal{M}_P^\mathrm{SD}\colon
\coloneqq\{[A]\in\mathcal{A}|\star F_A=+F_A\}.
$$
There are canonical inclusions $\mathcal{M}_P^-,\mathcal{M}_P^+\hookrightarrow\mathcal{M}_P^+$. The intersection $\mathcal{M}_P^-\cap\mathcal{M}_P^+$ includes exactly the flat connections, the critical points of the [[Chern-Simons action functional]], and could therefore be refered to as _Chern-Simons moduli space_.

## Properties

If $X$ is a [[4-manifold]], then: ([Donaldson 1983, p. 290](#Donaldson83), [Donaldson 1987, Eq. (2.1)](#Donaldson87), [Freed & Uhlenbeck 1991, Eq. (2.28) ](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=2p_1(Ad(P))[X]
-\dim G(1-b_1+b_2^-).
$$
In particular for $G=\operatorname{SU}(2)$ the second [[special unitary group]]: ([Freed & Uhlenbeck 1991, between eq. (2.28) and (2.29) on p. 42](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=-8c_2(P)[X]
-3(1-b_1+b_2^-).
$$
In particular for $G=\operatorname{SO}(3)$ the third [[special orthogonal group]]: ([Freed & Uhlenbeck 1991, Eq. (2.29) on p. 42 & eq. (10.3) on p. 155](#FreedUhlenbeck91))
$$
dim\mathcal{M}_P^+
=2p_1(P)[X]
-3(1-b_1+b_2^-).
$$

## Related entries

* [[Seiberg-Witten moduli space]] (monopole moduli space)

## References

* {#Donaldson83} [[Simon Donaldson]]. _An application of gauge theory to four-dimensional topology_. In: Journal of Differential Geometry. 18. Jahrgang, Nr. 2, 1. Januar 1983, [doi:10.4310/jdg/1214437665](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-18/issue-2/An-application-of-gauge-theory-to-four-dimensional-topology/10.4310/jdg/1214437665.full)
* {#Donaldson87} [[Simon Donaldson]]. _The orientation of Yang-Mills moduli spaces and 4-manifold topology_. In: Journal of Differential Geometry. 26. Jahrgang, Nr. 3, 1. Januar 1987, [doi:10.4310/jdg/1214441485](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-26/issue-3/The-orientation-of-Yang-Mills-moduli-spaces-and-4-manifold/10.4310/jdg/1214441485.full)
* {#FreedUhlenbeck91}  [[Daniel Freed]], [[Karen Uhlenbeck]], _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

See also:

* Wikipedia, _[Yang–Mills moduli space](https://en.wikipedia.org/wiki/Yang–Mills_moduli_space)_

[[!redirects YM moduli space]]
[[!redirects instanton moduli space]]

[[!redirects self-dual Yang-Mills moduli space]]
[[!redirects SDYM moduli space]]
[[!redirects self-dual instanton moduli space]]

[[!redirects anti self-dual Yang-Mills moduli space]]
[[!redirects ASDYM moduli space]]
[[!redirects anti self-dual instanton moduli space]]