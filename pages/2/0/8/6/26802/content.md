
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

If we view a [[matrix]] with entries in some set $X$ with rows labelled by elements in the index set $I$ and rows labelled by elements in $J$ as a function $A \colon I\times J\to X$ then a *partitioned matrix* (also called a *block matrix*) is a matrix together with partitions of the sets of row labels and column labels. 

For partitions 
$I = I_1\coprod I_2\coprod\ldots\coprod I_k$, 
$J = J_1\coprod J_2\coprod\ldots\coprod J_l$,
there are corresponding submatrices, cells or blocks
$A^{J_r}_{L_s}:J_r\times L_s\to X$ 
which are matrices defined by 
$A^{J_r}_{L_s}(i,j) = A(i,j)$ as long as 
$(i,j)\subset J_r\times L_s$.
Conversely, $A$ is determined by $A^{J_r}_{L_s}$ for all $1\leq r\leq k$ and $1\leq s\leq l$. Thus, one views a partitioned matrix as such a labelled collections of blocks. 

One often uses some ordering on $I$ and $J$ and partitions which respect the ordering. 

## Properties

[[Gauss elimination procedure]], [[row operation]]s, [[Gauss decomposition]], [[quasideterminant]]s, computation of [[inverse matrix]], make sense and are performed alike the classical case, but with the order of multiplicating blocks essential. However, the determinant does not make sense or does not behave well even when it is still accidentaly defined. 

Heredetary property of quasideterminants: quasideterminant at $(i,j)$ of block quasideterminant at $(I_r,J_s)$ where $i\in I_r$, $j\in J_s$ equals the quasideterminant of the original matrix at $(i,j)$. In particular, inverse of a block matrix has entries of entries which are entries of inverse of the original matrix. Consequently, linear equations may be solved by block version of Gaussian elimination and the result reinterpreted in terms of original matrix labels. 

## References

See also 

* Wikipedia, *[Block matrix](https://en.wikipedia.org/wiki/Block_matrix)*
* David C. Lay, Steven R. Lay, Judi J. McDonald, _Linear algebra and its applications_, 6th edition, Pearson Education Ltd. 2022 (Sec. 2.4, Partitioned matrices)
* Daniel Krob, [[Bernard Leclerc]], _Minor identities for quasi-determinants and quantum determinants_, Comm. Math. Phys. 169 (1995) 1--23 [doi](https://doi.org/10.1007/BF02101594) arXiv:[hep-th/9411194](https://arxiv.org/pdf/hep-th/9411194)

category: algebra

[[!redirects partitioned matrices]]
[[!redirects block matrix]]
[[!redirects block matrices]]


