
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $G$ be a [[compact Lie group]] and let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] $G$-[[linear representation]] on a [[real vector space]] $V$. Then the underlying [[Euclidean space]] $\mathbb{R}^V$ inherits the [[mathematical structure|structure]] of a [[topological G-space]]

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
   & 
   \in G TopSpaces
\end{xymatrix}

We may call this the _[[Euclidean G-space]]_ associated with the linear representation $V$.

## Properties

### Relation to representation spheres

The [[one-point compactification]] of a Euclidean $G$-space is the corresponding [[representation sphere]]:

$$
  \big( \mathbb{R}^V \big)^{cpt}
  \;\simeq\;
  S^V
  \,.
$$

### Relation to representation tori

Let $V \in RO(G)$ be an [[orthogonal group|orthogonal]] [[linear representation]] of a [[finite group]] $G$ on a [[real vector space]] $V$.

If $G$ is the [[point group]] of a [[crystallographic group]] inside the [[Euclidean group]] 

$$
  N \rtimes G
  \hookrightarrow
  Iso(\mathbb{R}^V)
$$

then the $G$-[[action]] on the Euclidean $G$-space $\mathbb{R}^V$ descends to the [[quotient]] by the [[action]] of the translational [[normal subgroup]] [[lattice in a vector space|lattice]] $N$ ([this Prop.](crystallographic+group#InducedPointGroupActionOnTorus)). The resulting $G$-space is an [[n-torus]] with $G$-action, which might be called the _[[representation torus]]_ of $V$

\begin{xymatrix}
   \mathbb{R}^V\ar@(ul,ur)^G
   \ar@{}[r]|-{:=}
   &
   \big( \mathbb{R}^V\ar@(ul,ur)^G\big)/N
\end{xymatrix}

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=13">
<img src="https://ncatlab.org/schreiber/files/ExamplesOfLinearRepsAndInducedGSpaces.jpg" width="690">
</a>
</center>

> graphics grabbed from [SS 19](equivariant+Hopf+degree+theorem#SatiSchreiber19)

### Equivariant configurations in Euclidean $G$-spaces

(...)

## Related concepts

* [[Euclidean space]]

* [[super-Euclidean space]]


## References

Discussion of equivariant [[configuration spaces of points]] in Euclidean $G$-spaces:

* {#RourkeSanderson00} [[Colin Rourke]], [[Brian Sanderson]], _Equivariant Configuration Spaces_, J. London Math. Soc. 62 (2000) 544-552 ([arXiv:math/9712216](https://arxiv.org/abs/math/9712216))




[[!redirects Euclidean G-spaces]]
