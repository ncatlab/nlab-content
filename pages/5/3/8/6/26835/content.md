
\tableofcontents

## Idea 

The [[determinant]] of a [[square matrix]] with [[commutative ring|commutative]] entries can be expanded into a [[sum]] of signed products of all maximal [[minors]] in a chosen proper subset
of the sets of rows (or columns) with the complementary minors. 

Analogous formulas hold for [[quantum determinants]].

## Laplace expansion identity

Let $A$ be a quadratic $n\times n$-matrix with entries in a commutative ring $R$ and $K,L\subset \{1,\ldots,n\}$, $\hat{K} = \{1,\ldots,n\}\backslash K$ and $card(K) =card(L) = m$. Denote by $A^J_I$ the submatrix of $A$ with rows in $I$ and columns in $J$ for $I,J\subset\{1,\ldots,n\}$. Then
\[ \begin{array}{l}
 (-1)^{l(L\star \hat{L})} \delta^L_K\, det(T) = 
\sum_{card(J) = m} (-1)^{l(J\star \hat{J})} \,
det(A^J_K) det(T^{\hat{J}}_{\hat{L}})\\
 (-1)^{l(L\star \hat{L})}\delta^K_L\, det(T) = 
\sum_{card(J) = m} (-1)^{l(J\star \hat{J})} \,
det(T^K_J) det(T^{\hat{L}}_{\hat{J}})\\
\end{array}\]
where $l$ is the length function of a sequence considered as a permutation of $\{1,\ldots,n\}$ and $\star$ denotes the concatenation and $\delta$ is the Kronecker for multiindices. 

Notice that if $m = n-1$ then $J = \{j\}$ and $l(J\star \hat{J}) = l(j,1,\ldots,j-1,j+1,\ldots n) = j-1$.

category: algebra

