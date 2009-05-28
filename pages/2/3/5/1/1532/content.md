An [[algebraic cycle]] on a [[scheme]] $X$ of finite type over a [[field]] $k$ is a finite linear combination $\sum_{i=1}^r n_i Z_i$ of integral closed subschemes $Z_i\subset X$ with integral coefficients $n_i$.  The algebraic cycles form a group $\mathcal{Z}= \mathcal{Z}_*$ of algebraic cycles on $X$ which is graded by the dimensions of the cycles. Sometimes (for equidimensional $X$) one looks at the grading by codimension $\mathcal{Z}_*$. 

Let $\mathrm{SmProj}_k$ be the category of smooth projective [[algebraic variety|varieties]] over $k$.  A rule giving an [[equivalence relation]] $\mathcal{Z}^*(X)$ for every $X$ in $\mathrm{SmProj}_k$, and which is compatible with grading is an **adequate equivalence relation** such that

1. For every pair of cycles $a,b\in \mathcal{Z}^*(X)$, there exists $a'\sim a$ such that $a'$ is transversal to $b$.

2. Consider a product $X\times Y$ in $\mathrm{SmProj}_k$, denote by $p_X,p_Y$ its projections. Consider cycles $a\in \mathcal{Z}^*(X)$ and $b\in \mathcal{Z}^*(X\times Y)$ such that $b$ and $p_X^*(a)$ intersect properly. Then $a\sim 0$ implies $p_Y_*(p_X^*(a)\cdot b) \sim 0$ where $p_X^*(a)\cdot b$ denotes the intersection product. 

The [[intersection product]], which is associative but only partially defined on $\mathcal{Z}^*$, then becomes globally defined on $\mathcal{Z}^*/{\sim}$.

Typical choices are rational, algebraic and numerical adequate equivalence relations.  The rational is the finest and the numerical is the coarsest nonzero adequate equivalence relation.