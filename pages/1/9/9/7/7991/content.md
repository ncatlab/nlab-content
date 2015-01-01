
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

### Double cover $Mp$

For $n \in \mathbb{N}$, the _metaplectic group_ $Mp(2n, \mathbb{R})$ is the [[Lie group]] which is the unique [[double cover]] of the [[symplectic group]] $Sp(2n, \mathbb{R})$.

### Circle extension $Mp^c$
  {#CircleExtension}

There is also a nontrivial  [[circle group]]-extension of the [[symplectic group]], called $Mp^c$. This is in direct [[analogy]] to the group [[Spin^c]] and its relation to [[Spin]].

Let $(V, \omega)$ be a [[symplectic vector space]]. By the [[Stone-von Neumann theorem]] there is an essentially unique [[irreducible representation|irreducible]] [[unitary representation]] $W$ of its [[Heisenberg group]] $Heis(V,\omega)$. This being essentially unique implies that for each element $g\in Sp(V,\omega)$ of the [[symplectic group]], there is a unique [[unitary operator]] $U_g$ such that for all $v\in V$

$$
  W(g(v)) = U_g W(v) U^{-1}_g
  \,.
$$

The group $Mp^c$ is the [[subgroup]] of the [[unitary group]] of all such $U_g$ for $g\in Sp(V,\omega)$. The map $U_g \mapsto g$ exhibits this as a [[group extension]] by the [[circle group]]

$$
  U(1)\longrightarrow Mp^c(V,\omega) \longrightarrow Sp(V,\omega)
  \,.
$$

e.g. ([Robinson-Rawnsley 89, p. 19](#RobinsonRawnsley89))

## Properties

### Relation to the metalinear group

Inside the [[symplectic group]] $Sp(2n, \mathbb{R})$ sits the [[general linear group]] 

$$
  Gl(n,\mathbb{R}) \hookrightarrow Sp(2n,\mathbb{R})
$$

as the subgroup that preserves the standard [[Lagrangian submanifold]] $\mathbb{R}^n \hookrightarrow \mathbb{R}^{2n}$. Restriction of the metaplectic [[group extension]] along this inclusion defines the [[metalinear group]] $Ml(n)$

$$
  \array{
    Ml(n, \mathbb{R}) &\hookrightarrow& Mp(2n, \mathbb{R})
    \\
    \downarrow && \downarrow
    \\
    Gl(n, \mathbb{R}) &\hookrightarrow& Sp(2n, \mathbb{R})
  }
  \,.
$$

Hence a [[metaplectic structure]] on a [[symplectic manifold]] induces a [[metalinear structure]] on its [[Lagrangian submanifolds]].

## Related concepts

* [[metaplectic structure]]

* [[metaplectic correction (in geometric quantization)]]

* [[metaplectic representation]]

## References

An original reference is

* [[Andre Weil]], _Sur certains groupes d'op&#233;rateurs unitaires_, Acta Math. 111: 143&#8211;211. (1964).

Further discussion includes

* {#RobinsonRawnsley89} P. L. Robinson, [[John Rawnsley]], _The metaplectic representation, $Mp^c$-structures and geometric quantization_, 1989

* [[John Rawnsley]], _On the universal covering group of the real symplectic group_, Journal of Geometry and Physics 62 (2012) 2044&#8211;2058 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rawnsley.pdf))

* [[Michel Cahen]], [[Simone Gutt]], _$Spin^c$, $Mp^c$ and Symplectic Dirac Operators_, Geometric Methods in Physics Trends in Mathematics 2013, pp 13-28 ([pdf](http://homepages.ulb.ac.be/~sgutt/spinbiel.pdf))


[[!redirects metaplectic groups]]

[[!redirects Mp]]
[[!redirects Mp^c]]
