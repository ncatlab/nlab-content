
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

For $n \in \mathbb{N}$, the _metaplectic group_ $Mp(2n, \mathbb{R})$ is the [[Lie group]] which is the unique [[double cover]] of the [[symplectic group]] $Sp(2n, \mathbb{R})$.

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

* P. L. Robinson, [[John Rawnsley]], _The metaplectic representation, $Mp^c$-structures and geometric quantization_, 1989

* [[John Rawnsley]], _On the universal covering group of the real symplectic group_, Journal of Geometry and Physics 62 (2012) 2044&#8211;2058 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rawnsley.pdf))

* [[Michel Cahen]], [[Simone Gutt]], _$Spin^c$, $Mp^c$ and Symplectic Dirac Operators_, Geometric Methods in Physics Trends in Mathematics 2013, pp 13-28 ([pdf](http://homepages.ulb.ac.be/~sgutt/spinbiel.pdf))


[[!redirects metaplectic groups]]