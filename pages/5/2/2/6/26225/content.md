Expression __Euler form__ may mean either a [[differential form]] ("Chern-Euler form") representing the [[Euler characteristic class]], but also a $\mathbf{Z}$-bilinear form on a Grothendieck group of a $k$-linear abelian or triangulated category, related to an alternative sum of dimensions of Ext-groups. This entry is about the latter.
The terminology is allegedly due [[Claus Michael Ringel]]. 

## Definition 

If $C$ a $k$-linear [[abelian category]] such that $dim(Ext^i(M,N))\lt \infty$ for all $i$ and all objects $M,N$ in $C$, then the Euler form is a $\mathbf{Z}$-bilinear form $\langle -,-\rangle : K_0(C)\times K_0(C)\to\mathbf{Z}$ defined by
$$
\langle [M],[N]\rangle = \sum_{i\geq 0} (-1)^i dim_k(Ext^i(M,N)).
$$
Similarly, for suitable $k$-linear [[triangulated category]] $D$ one sets
$$
\langle [M],[N]\rangle = \sum_{i\geq 0} (-1)^i dim_k(Hom_D(M,\Sigma^i N))
$$

## Literature

* C. Geiß, _Derived tame algebras and Euler-forms_, Math Z. __239__ (2002) 829--862 [doi](https://doi.org/10.1007/s002090100349)
* Helmut Lenzing, _On the K-theory of weighted projective curves_, [arXiv:1702.03445](https://arxiv.org/abs/1702.03445)
* Helmut Lenzing, _A K-theoretic study of canonical algebras_, in: Representation theory of algebras (Cocoyoc, 1994), CMS Conf. Proc, 1996 [RG](https://www.researchgate.net/profile/Helmut-Lenzing/publication/265548116_A_K-theoretic_study_of_canonical_algebras/links/55ba4d0008aec0e5f43e995b/A-K-theoretic-study-of-canonical-algebras.pdf)
* [[Sefi Ladkani]], _Refined Coxeter polynomials_, [arXiv:2110.15329](https://arxiv.org/pdf/2110.15329)