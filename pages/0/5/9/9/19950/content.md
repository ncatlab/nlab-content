

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The [[Bredon cohomology]]-[[equivariant cohomology|equivariant]] enhancement of [[cohomotopy]]-theory is _equivariant cohomotopy_: 

For $G$ a [[group]], $V$ a [[finite dimensional vector space|finite-dimensional]] [[real vector space|real]]  $G$-[[representation]] $G \to O(V)$ and writing $S^V$ for the corresponding [[representation sphere]], the _equivariant cohomotopy_ in [[RO(G)-degree]] $V$ of a [[G-space]] $X$ is the set of $G$-[[equivariant homotopy theory|equivariant]] [[homotopy classes]] of maps from $X$ to $S^V$:

$$
  \pi_G^V\big( X \big)
  \;\coloneqq\;
  \left[
    X, S^V
  \right]^G
  \,.
$$

For $V = \mathbb{R}^n$ the [[trivial representation]] of [[dimension]] $n$, this reduces to the definition of plain [[cohomotopy]]-sets

$$
  \pi^{\mathbb{R}^n}(X)
  \;=\;
  \pi^n(X)
  \;=\;
  \left[ X, S^n\right]
  \,.
$$


The [[stabilization]] of this construction, in the sense of [[equivariant stable homotopy theory]], yields the concept of _[[equivariant stable cohomotopy]]_.


## Properties

### Pontryagin-Thom construction
 {#PontryaginThomConstruction}

The [[Pontryagin-Thom construction]] generalizes from plain [[cohomotopy]] ([here](cohomotopy#RelationToCobordismGroup)), to equivariant cohomotopy. Here it identifies classes in $\pi^V(X)$ with [[cobordism classes]] of $d$-[[dimension|dimensional]] [[submanifolds]] $\Sigma \subset X^G$ inside the $G$-[[fixed point]]-locus $X^G \subset X$ for

$$
  d \;=\;  dim\left( X^G \right) - dim\left( V^G \right)
$$

hence with [[codimension]] relative to $X^G$ the dimension of the [[fixed point]]-locus of $V$.

([Grady 18](#Grady18))

## Related concepts

[[!include flavours of cohomotopy -- table]]

## References

### General

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))


* {#Cruickshank03} James Cruickshank, _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)

* {#Grady18} Daniel Grady, _Cobordisms of global quotient orbifolds and an equivariant Pontrjagin-Thom construction_ ([arXiv:1811.08794](https://arxiv.org/abs/1811.08794))


### Classification of M-branes

Discussion of [[M-brane]] physics in terms of equivariant cohomotopy

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

  ([[equivariant rational homotopy theory|rational equivariant]] cohomotopy)

* [Grady 18, section 4](#Grady18)
