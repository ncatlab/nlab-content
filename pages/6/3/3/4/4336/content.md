

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

For [[natural numbers]] $n$ and $m$ and a set $X$, an $n\times m$ __matrix__ of elements of $X$ is a function $M:[n]\times[m]\rightarrow X$ from the Cartesian product $[n]\times[m]$ to $X$.

Often one uses the term in a context where one can add and multiply matrices using [[matrix calculus]].  Addition of matrices of the same dimension requires $X$ to have an "addition" operation; multiplication of matrices requires $X$ to also have a "multiplication" operation.  Usually $X$ is at least a [[rig]] and often a [[ring]] or a [[field]].

More generally, for arbitrary sets $A$ and $B$ we can define an $A\times B$-matrix to be a function $A\times B\to X$.  If $X$ has some kind of "infinitary sums" as well as finite "products", then we can also multiply matrices of this sort: e.g. if $X$ is the set of objects of a [[monoidal category]] with arbitrary [[coproducts]].

Note that if the structure on X is such that matrix multiplication is associative and there exist identity matrices, then matrices over X may be taken as the morphisms of a category $Mat_X$ whose composition is matrix multiplication. This is in particular the case if X is a field, and so many basic theorems of linear algebra may be understood as concerning functors from $Vect_X$ into $Mat_X$ and natural transformations between such functors.

## Related concepts

* [[matrix multiplication]], [[matrix calculus]]

* [[matrix decomposition]]

* [[square matrix]]

* [[diagonal matrix]]

* [[elementary matrix]]

* [[block matrix]] ([[partitioned matrix]])

* [[row echelon matrix]]

* [[rank of a matrix]]

* [[inverse matrix]]

* [[matrix equivalence]]

* [[monomial matrix]], [[permutation matrix]]

* [[principal submatrix]]

* [[matrix group]], [[matrix Lie group]]

* [[unitary matrix]]. [[unitary group]]

* [[triangular matrix]]

* [[Smith normal form]]

* [[stochastic matrix]]

* [[adjacency matrix]]

* [[linear algebra]], [[general linear group]], [[special linear group]], [[matrix mechanics]], [[matrix theory]], [[matrix Hopf algebra]], [[matrix Lie algebra]], [[matrix Lie group]], [[classical Lie group]], [[universal localization]], [[tensor calculus]], [[moment of inertia]], [[eigenvalue]], [[characteristic polynomial]] (Cayley-Hamilton theorem), [[spectral curve]]

Special cases: [[S-matrix]], [[classical r-matrix]], [[density matrix]], [[hermitian matrix]], [[skew-symmetric matrix]], [[quantum Yang-Baxter matrix]], [[random matrix]], [[skew-symmetric matrix]]

Operations on/with matrices: [[transpose matrix]], [[adjoint matrix]]  [[trace]], [[matrix factorization]], [[Gauss decomposition]], [[Gram-Schmidt process]]

Determinants and [[determinant]] like notions, and special cases: [[quasideterminant]], [[Berezinian]],[[Jacobian]], [[Pfaffian]], [[hafnian]],  [[Wronskian]], [[resultant]], [[discriminant]]

## References

Historical origins:

* [[Arthur Cayley]]: *A Memoir on the Theory of Matrices*, Philosophical Transactions of the Royal Society of London, **148** (1858) 17-37 &lbrack;[jstor:108649](https://www.jstor.org/stable/108649)&rbrack;

Textbook accounts:

* [[Igor R. Shafarevich]], [[Alexey O. Remizov]]: §2 in: *Linear Algebra and Geometry* (2012) &lbrack;[doi:10.1007/978-3-642-30994-6](https://doi.org/10.1007/978-3-642-30994-6), [MAA-review](https://maa.org/press/maa-reviews/linear-algebra-and-geometry)&rbrack; 

See also: 

* Wikipedia: <a href="https://en.wikipedia.org/wiki/Matrix_(mathematics)">Matrix (mathematics)</a>



[[!redirects matrix]]
[[!redirects matrices]]
