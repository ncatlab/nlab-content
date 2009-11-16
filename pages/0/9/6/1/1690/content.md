Let $B$ be a [[bialgebra]], possibly noncommutative,
over a field $k$ and
$G = (g^i_j)^{i = 1,\ldots, n}_{j = 1,\ldots, n}$
an $n\times n$-matrix over $B$.
$B$ is a **matrix bialgebra** with basis $G$ if

* the set of entries of $G$ generates $B$ and

* the comultiplication $\Delta$ and counit $\epsilon$ satisfy
the matrix equations $\Delta G = G \otimes G$ (i.e. in components
$\Delta g^i_j = \sum_{k = 1}^n g^i_k \otimes g^k_j$)
and $\epsilon G = 1$ (reading in components $\epsilon (g^i_j) = \delta^i_j$).

According to a result of Redford every finite-dimensional Hopf algebra over a [[field]] is a matrix Hopf algebra with respect to some basis. 

The free (noncommutative) associative algebra $F$
on $n^2$ generators $f^i_j$
has a unique coalgebra structure making it a
matrix bialgebra with basis $(f^i_j)^{i = 1,\ldots, n}_{j = 1,\ldots, n}$.
We call it the **free matrix bialgebra of rank $n^2$**.
Every bialgebra quotient of that bialgebra is a matrix bialgebra.

A **matrix Hopf algebra** $\mathcal{H}$ with basis $T = (t^i_j)$ is a Hopf algebra which possess a matrix subbialgebra $B$ with basis $T$ such that the map $H(id_B):H(B)\rightarrow\mathcal{H}$
is onto (where $H(B)$ denotes the [[Hopf envelope]] of $B$ and $H$ is understood as a [[functor]]).  

A matrix Hopf algebra $\mathcal{H}$ with basis $T$ is often not a matrix bialgebra with basis $T$: e.g. the commutative
coordinate ring of $GL(n,k)$ is not a matrix bialgebra
with respect to the obvious basis $T$; in this example this can be repaired by enlarging the basis by one group-like element: the inverse of the determinant. On the other hand, the coordinate algebra of the special linear group $O(SL(n,k))$ is a matrix bialgebra and a matrix Hopf algebra with the same standard basis $T$.

[[!redirects matrix Hopf algebras]]