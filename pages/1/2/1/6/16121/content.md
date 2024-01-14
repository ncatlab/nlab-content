
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Statement

Consider an *[[inner product space]]* in the sense of a [[vector space]] $\mathscr{V}$ equipped with a [[Hermitian form]] $\langle -,- \rangle$ which is positive *semi*-definite:

$$
  v \in \mathscr{V}
  \;\;\;
  \vdash
  \;\;\;
  \langle
    v , v
  \rangle
  \;\geq 0\;
  \,.
$$

(we do *not* need to assume positive definiteness, cf. [MO:a/2548691](https://math.stackexchange.com/a/2548691/58526), [Ćurgus](#Ćurgus))

then for all [[pairs]] of [[vectors]] $v,w \,\in\, V$ the following Cauchy-Schwarz [[inequality]] holds:

$$
  \left\vert\langle u,v\rangle\right\vert^2 
  \;\leq\; 
  \langle u,u \rangle
  \cdot
  \langle v,v \rangle
  \,.
$$

In terms of the [[norm]] $\Vert-\Vert \,\coloneqq\, \sqrt{\langle -,-\rangle}$ and the [[absolute value]] this means equivalently:

$$
  {\big\vert \langle u,v\rangle \big\vert}
  \;\leq\; 
  \left\Vert u \right\Vert
  \cdot
  \left\Vert v \right\Vert
  \,.
$$

 

## Related concepts

* [[GNS-construction]]

## References

Original proofs are due to [[Cauchy]] in 1821, [[Bouniakowsky]] in 1859, [[Hermann Schwarz]] in 1888.

Review:

* {#Ćurgus} Branko Ćurgus, *[Cauchy-Bunyakovsky-Schwarz inequality](https://faculty.curgus.wwu.edu/Courses/Math_pages/Math_504/Cauchy-Schwarz-Bunyakovsky.html)*

* Wikipedia, _[Cauchy-Schwarz inequality](https://en.wikipedia.org/wiki/Cauchy-Schwarz_inequality)_

[[!redirects Cauchy-Schwarz inequality]]
[[!redirects Cauchy inequality]]
