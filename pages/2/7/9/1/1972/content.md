Any [[group]] $G$ has a [[category]] of finite-dimensional [[complex number|complex]]-linear [[representations]], often denoted $Rep(G)$.  This is a [[symmetric monoidal category|symmetric monoidal]] [[abelian category]] and thus has a [[Grothendieck ring]], which is called the **representation ring** of $G$ and denoted $R(G)$.

More concretely, we get $R(G)$ as follows.  It has a basis $(e_i)_i$ given by the **irreps** of $G$: that is, $i$ is an index for an irreducible finite-dimensional complex representation of $G$.  It has a product given by 

$$ e_i e_j = \sum_k m_{i j}^k e_k ,$$

where $m_{i j}^k$ is the multiplicity of the $k$th irrep in the tensor product of the $i$th and $j$th irreps.  Note that $R(G)$ is commutative thanks to the symmetry of the tensor product.

If $G$ is a [[finite group]] and we tensor $R(G)$ with the complex numbers, it becomes isomorphic to the **[[character ring]]** of $G$: that is, the ring of complex-valued functions on $G$ that are constant on each conjugacy class.  Such functions are called **[[class function]]s**.