## Definition

If we view a [[matrix]] with entries in some set $X$ with rows labelled by elements in the index set $I$ and rows labelled by elements in $J$ as a function $A: I\times J\to X$ then a partitioned matrix (also called a block matrix) is a matrix together with partitions of the sets of row labels and column labels. 

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

category: algebra

[[!redirects partitioned matrices]]
[[!redirects block matrix]]
[[!redirects block matrices]]