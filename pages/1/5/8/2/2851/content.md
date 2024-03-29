
#Contents#
* table of contents
{:toc}

## Idea

Let $k$ be a [[field]] and $g\in M_n(k)$ $n\times n$ square matrix whose entries are in $k$. One would like to decompose this matrix as $g = UDL$ where $L$ is the lower triangular unidiagonal matrix, $U$ upper triangular unidiagonal and $D$ a diagonal matrix. Unidiagonal means with only units on a diagonal. One can also try to decompose $g = UA$ where $A$ is lower triangular and $U$ upper triangular unidiagonal. Not every matrix however has such a decomposition: one tries to find the solution via [[Gauss elimination procedure]], and the conditions for the solution involve non-vanishing of certain "principal" minors of the matrix. Then the solution for entries of $U$ or $L$ involves ratios of (determinants of) minors of the same size, while the solution for $A$ the ratio of (determinants of) minors of sizes different by one. These  decompositions of a matrix $G$ are called the Gauss decompositions.

If $g\in GL_n(k)$ then there exist a permutation $n\times n$ matrix $w$ such that the problem $G = wUDL$ has a solution. The subset of matrices $G\in GL_n(k)$ for which such a decomposition exists (and then it is automatically unique and given by universal formulas) is a Zariski open subset in $GL_n(k)$, one of the "Gauss cells"; the decomposition of matrices is for each $w$ also called Gauss decomposition. Then $w=1$ is said to be the main cell. The group $GL_n(k)$ is __covered__ by $n!$ open subsets, this is the Gauss of global decomposition of $GL_n$; similarly one can do for various subgroups of $GL_n$ by inducing the decomposition from $GL_n$. In the case of $SL_n(\mathbb{C})$, and some other cases, the matrices corresponding to $A$ in the decomposition for $w=1$ are forming the corresponding (lower) Borel subgroup.

This should be distinguished from Bruhat decomposition where one wants $g=UwA$ instead of $g=wUA$. Except for the case when $w=1$ when the two decompositions coincide, the matrices which decompose for given $w$ make a subset of higher codimension, hence nonprincipal (that is $w\neq 1$) Bruhat cells are not open. Furthermore, while in Gauss case  the cells make a cover of $GL_n$, in Bruhat case they make a partition of $GL_n$ into disjoint subsets of elements. 

If $B$ is a subgroup of lower triangular matrices, then for the fixed $w$, the entries of $U$ as a function of $G$ in the decomposition $g=wUA$ are the coordinates on the patch in $GL_n/B$ evaluated at the coset of $g$. The decomposition therefore for fixed $w$ corresponds to the trivialization of the principal $B$-bundle $GL_n\to GL_n/B$ over the open Gauss cell corresponding to $w$.

Gauss decomposition can be generalized to the matrices with noncommutative entries and there are explicit formulas involving [[quasideterminants]], and in the case of quantum linear groups in terms of quantum minors. 

Remark. The upper conventions are more from mathematical physics literature. The lowest weight representations have often positive energy, what is normal requirement there and the lower triangular matrices are used to act on the lowest weight vector. In mathematical community, one prefers to talk about upper triangular matrices forming Borel subgroup and about the decomposition $LDU$ and $LA$ where $A$ is upper triangular and act on heighest weight representations instead.

## Related concepts

See also [[quantum Gauss decomposition]].


## References

Named after [[Carl Friedrich Gauß]].

See also 

* [[eom]], _[Gauss decomposition](https://www.encyclopediaofmath.org/index.php/Gauss_decomposition)_