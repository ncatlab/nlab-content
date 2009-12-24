#Contents#
* automatic table of contents goes here
{:toc}


## Idea

A _0-dimensional TQFT_ is a [[TQFT]] regarded in the sense of [[FQFT]] as a [[representation]] of the [[category]] of 0-dimensional [[cobordism]]s.

This degenerate case turns out to exhibit a nontrivial amount of interesting information, in particular if regarded in the context of _super_ QFT.

## Definition 

### 0-Dimensional Cobordisms

The [[category]] $Cob_0$ of 0-dimensional [[cobordism]]s is the [[symmetric monoidal category]] $Cob_0$ having the $-1$-dimensional [[manifold]] $\emptyset$ as the only [[object]] and [[isomorphism]] classes of compact $0$-dimensional manifolds as morphisms. Clearly $Cob_0$ is equivalent to $\mathbf{B}\mathbb{N}$

### 0-Dimensional TQFT

A **0-dimensional [[TQFT]]** (with values in $\mathbb{Z}$-[[module]]s) is a [[monoidal functor]]

$$
  Z\colon Cob_0\to \mathbb {Z} Mod
  \,.
$$

By definition of [[monoidal functor]], one has $Z({\emptyset})=\mathbb{Z}$ and so $Z$ is completely (and freely) determined by the assignment $Z(\{pt\}\in End_\mathbb{Z}(\mathbb{Z})=\mathbb{Z}$. In other words, the space of 0-dimensional TQFTs is $\mathbb{Z}$.

### Over a manifold 

One can consider TQFTs with a target manifold $X$: all bordisms are required to have a map to $X$. 

In dimension $0$, morphisms in $Cob_0(X)$ are the topological [[monoid]] $\bigcup_{n\geq 1} Sym^n(X)$. In particular, continuous tensor functors from $Cob_0(X)$ to $\mathbb{Z}$-modules are naturally identified with degree 0 [[integral cohomology]] $H^0(X;\mathbb{Z})$.

### Extended version

The picture becomes more interesting if one goes from topological field theory to [[extended topological quantum field theory]]. Indeed, from this point of view, to the $-1$-dimensional vacuum is assigned the symmetric monoidal [[0-category]] $\mathbb{Z}$, and consequently, the infinity-version of the space of all $0$-dimensional TQFTs is the [[Eilenberg-Mac Lane spectrum]]. It follows that the space of extended $0$-dimensional TQFTs with target $X$ (taking values in $\mathbb{Z}$-modules) is the graded [[integral cohomology]] ring $H^*(X;\mathbb{Z})$.

### Super version

From the [[differential geometry]] point of view, a relation between de Rham cohomology of a smooth manifold $X$ and $0$-dimensional functorial field theories arises if one moves from topological field theory to $(0|1)$-supersymmetric field theory, see [[Axiomatic field theories and their motivation from topology]].

> It would be interesting to describe a direct connection between the extended and the susy theory; it should parallel the usual Cech-de Rham argument
