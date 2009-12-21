## 0-dimensional TQFT ##

0-dimensional cobordism is the symmetric monoidal category $Cob_0$ having the $-1$-dimensional manifold $\emptyset$ as the only object and isomorphism classes of compact $0$-dimensional manifolds as morphisms. Clearly $Cob_0$ is equivalent to $\mathbf{B}\mathbb{N}$

A 0-dimensional TQFT (with values in $\mathbb{Z}$-modules) is a tensor functor
$Z\colon Cob_0\to \mathbb {Z}-modules$. By definition of tensor functor, one has $Z({\emptyset})=\mathbb{Z}$ and so $Z$ is completely (and freely) determined by the assignment $Z(\{pt\}\in End_\mathbb{Z}(\mathbb{Z})=\mathbb{Z}$. In other words, the space of 0-dimensional TQFTs is $\mathbb{Z}$.

One can consider TQFTs with a target manifold $X$: all bordisms are required to have a map to $X$. In dimension $0$, morphisms in $Cob_0(X)$ are the topological monoid $\bigcup_{n\geq 1} Sym^n(X)$. In particular, continuous tensor functors from $Cob_0(X)$ to $\mathbb{Z}$-modules are naturally identified with $H^0(X;\mathbb{Z})$.

The picture becomes more interesting if one goes from topological field theory to [[extended topological quantum field theory]]. Indeed, from this point of view, to the $-1$-dimensional vacuum is assigned the symmetric monoidal $0$-category $\mathbb{Z}$, and consequently, the infinity-version of the space of all $0$-dimensional TQFTs is the [[Eilenberg-Mac Lane spectrum]]. It follows that the space of extended $0$-dimensional TQFTs with target $X$ (taking values in $\mathbb{Z}$-modules) is $H^*(X;\mathbb{Z})$.

From the differential geometry point of view, a relation between de Rham cohomology of a smooth manifold $X$ and $0$-dimensional functorial field theories arises if one moves from topological field theory to $(0|1)$-supersymmetric field theory, see [[Axiomatic field theories and their motivation from topology]].[^It would be interesting to describe a direct connection between the extended and the susy theory; it should parallel the usual Cech-de Rham argument]
