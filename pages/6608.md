

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

A [[tensor]] -- an element in a [[tensor product]] of $k$ [[vector spaces]] $V_1\otimes V_2\otimes\ldots\otimes V_k$ -- is said to be __decomposable__ if it can be written in the form $v_1\otimes v_2\otimes\ldots\otimes v_k$ where $v_i \in V_i$ for $i = 1,\ldots, k$. 

If all $V_i$ are copies of $V$ or $V^*$ for the same $V$ then we often talk of vectors in the tensor product as tensors and the tensor product the space of tensors. If $V_i$ has a basis $\{e^s_i\}_{s= 1}^{n_i}$ then $V_1\otimes V_2\otimes\ldots\otimes V_k$ has a basis consisting of all decomposable vectors of the form $e_1^{s_1}\otimes\ldots\otimes e_k^{s_k}$ for all $(s_1,\ldots,s_k)$ such that $1\leq s_i\leq n_i$. 

Let $V$ be finite-dimensional vector space. Then for a tensor 
$A\in V^{\otimes k}$ we say that $A$ has __decomposability rank__ $r$ if 

$$
r = min\{ h | \exists A_1,\ldots, A_h decomposable, A = A_1+\ldots+A_h \}
$$

Distinguish this invariant from the covariance rank of a tensor. 

While the decomposability rank of a covariance rank 2 tensor $A$ is the same as the rank of the corresponding matrix, for higher covariance rank tensors we do not have general algorithms how to determine the decomposability rank. 

## Related concepts

* [[decomposable differential form]]

[[!redirects decomposable tensors]]

[[!redirects indecomposable tensor]]
[[!redirects indecomposable tensors]]

