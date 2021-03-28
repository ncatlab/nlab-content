
# Contraction
* table of contents
{: toc}

## Disambiguation

In [[physics]], __contraction__ is a dilation with coefficient $\lambda\lt 1$. This notion is used in fixed point theory, theory of topological vector spaces etc. There is also a notion of contraction from [[metric space]] theory; see [[short map]].  Finally, the [[contraction rule]] is a structural rule in [[logic]] and [[type theory]].  This entry will be predominantly about another notion of a contraction.


## Contraction of tensors

This entry will be predominantly about contraction of tensors, where by [[tensor]] we mean a vector in some [[tensor power]] $V^{\otimes n}$ of a vector $k$-space $V$ (or a projective $k$-module if $k$ is only a commutative ring). Let $V^* = Hom_k(V,k)$ be the dual vector space and $(V^*)^{\otimes m}$ be some tensor of $V^*$. Then one may define $(l,s)$-contraction
$$(V^*)^{\otimes m}\otimes V^{\otimes n}\to (V^*)^{\otimes (m-1)}\otimes V^{\otimes (n-1)}$$
by pairing by the evaluation map the $l$-th tensor factor of $(V^*)^{\otimes r}$ and $s$-th tensor factor of $V^{\otimes n}$. In fact as a map written, one can contract also elements of $(V^*)^{\otimes m}\otimes V^{\otimes n}$ which did not come from a product of a pair of element (i.e. which are not [[decomposable tensor]]s).

Let the rank $r$ of $V$ be finite.
If $S\in V^{\otimes n}$ is given in some basis by components $S^{i_1,\ldots, i_n}$ and $T\in (V^*)^{\otimes r}$ is given in the dual basis by components $T_{j_1,\ldots,j_r}$, then the components of the contraction will be 
$$contr_{l,s}(T,S)^{i_1,\ldots, i_{s-1},i_{s+1},\ldots,i_n}_{j_1,\ldots, j_{l-1},j_{l+1},\ldots,j_m} = \sum_{u = 1}^r T_{j_1,\ldots, j_{l-1},u,j_{l+1},\ldots,j_m} S^{i_1,\ldots, i_{s-1},u,i_{s+1},\ldots,i_n}$$

More generally one can contract mixed tensors and do several contractions simultaneously. In fact it is better to think of a contraction as a tensor multiplication of two tensors and then doing the genuine contraction of one upper and one lower index of the same tensor:
$$
contr_{l,s}(A)^{i_1,\ldots, i_{s-1},i_{s+1},\ldots,i_n}_{j_1,\ldots,j_{l-1},j_{l+1},\ldots, j_m}) := \sum_{u = 1}^r A^{i_1,\ldots, i_{s-1},u,i_{s+1},\ldots,i_n}_{j_1,\ldots,j_{l-1},u,j_{l+1},\ldots, j_m}
$$

The simplest case is the [[trace]] of a $(1,1)$-tensor: $tr A = \sum_{i=1}^r A^i_i$.

These operations can be symmetrized or antisymmetrised appropriately to make sense on symmetric or antisymmetric powers. 

For example, there is a contraction of a vector $X\in V$ and a $n$-form $\omega\in \Lambda V^*$:
$$(X,\omega)\mapsto \iota_X(\omega)$$
and $\iota_X: \omega\mapsto \iota_X(\omega)$ is a graded derivation of the exterior algebra of degree $-1$. This is also done for the tangent bundle which is a $C^\infty(M)$-module $V = T M$, then one gets the contraction of vector fields and differential forms. It can also be done in vector spaces, fibrewise.  

## Related concepts

* [[tensor algebra]]

* [[symmetric algebra]]

* [[exterior algebra]]

* [[divided power algebra]]

* [[multilinear algebra]]

## References

* wikipedia: [tensor contraction](http://en.wikipedia.org/wiki/Tensor_contraction)

* Shlomo Sternberg, _Introduction to differential geometry_

[[!redirects contraction]]
[[!redirects contractions]]
