
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

## Idea

Let $k$ be a [[field]] and $G \in M_n(k)$ am $n \times n$ [[square matrix]] with entries in $k$. 

Then a *Gauss decompositions* of $G$ is a [[matrix decomposition|decomposition]] as $G = U D L$ where:

1. $L$ is a [[lower triangular matrix|lower triangular]] unidiagonal matrix, 

1. $U$ is [[upper triangular matrix|upper triangular]] unidiagonal 

1. $D$ is [[diagonal matrix|diagonal]]. 

Here *unidiagonal* means with only [[unit]] entries on the diagonal. 

(If $D$ is the [[identity matrix]] then this is a special case of an [[LU decomposition]].)

The notion of Gauss decomposition may be generalized to matrices entries in a [[noncommutative ring]], in which case there are explicit formulas involving [[quasideterminants]] and, in the case of [[quantum linear groups]], in terms of quantum minors. See at *[[quantum Gauss decomposition]]* for more.


## Properties

### Existence

Not every matrix has a Gauss decomposition: one may try to find a solution via the [[Gauss elimination procedure]], and the conditions for the solution involve non-vanishing of certain "principal" [[minors]] of the matrix. Then the solution for entries of $U$ or $L$ involves ratios of ([[determinants]] of) [[minors]] of the same size.

### For invertible matrices

If $G$ is an [[invertible matrix]], $G \in$ [[general linear group|$GL_n(k)$]], then there always exist an $n \times n$ [[permutation matrix]] matrix $w$ such that a [[matrix decomposition|decomposition]] of the form $G = w U D L$ exists. 

The subset of matrices $G \in GL_n(k)$ for which such a decomposition exists (and then it is automatically unique and given by universal formulas) is a [[Zariski topology|Zariski]] [[open subset]] in $GL_n(k)$, called a "Gauss cell".

The decomposition of matrices for any $w$ is also at times  called a Gauss decomposition, in which case for $w=1$ one speaks of the *main cell*. 

The group $GL_n(k)$ is *[[open cover|covered]]* by [[factorial|$n!$]] such open subsets, this is the *Gauss of global decomposition* of $GL_n$. 

In a similar manner one may discuss [[subgroups]] of $GL_n$ by inducing the decomposition from $GL_n$. 

In the case of [[special linear group|$SL_n(\mathbb{C})$]], and some other cases, the matrices corresponding to $U$ in the decomposition for $w=1$ are forming the corresponding (lower) [[Borel subgroup]].

This should be distinguished from the [[Bruhat decomposition]] where one wants $G = U w A$ instead of $G = w U A$. Except for the case when $w=1$ when the two decompositions coincide, the matrices which decompose for given $w$ make a subset of higher [[codimension]], hence nonprincipal (that is $w\neq 1$) Bruhat cells are not open. Furthermore, while in Gauss case  the cells make a cover of $GL_n$, in Bruhat case they make a partition of $GL_n$ into disjoint subsets of elements. 

If $B$ is a subgroup of lower triangular matrices, then for the fixed $w$, the entries of $U$ as a function of $G$ in the decomposition $g=wUA$ are the coordinates on the patch in $GL_n/B$ evaluated at the coset of $g$. The decomposition therefore for fixed $w$ corresponds to the trivialization of the principal $B$-bundle $GL_n\to GL_n/B$ over the open Gauss cell corresponding to $w$.



## Related concepts

* [[matrix decomposition]]

  * [[QR decomposition]]

  * [[LU decomposition]]

  * [[polar decomposition]]

* [[quantum Gauss decomposition]].


## Literature

Named after [[Carl Friedrich Gauß]].

See also:

* [[eom]], _[Gauss decomposition](https://www.encyclopediaofmath.org/index.php/Gauss_decomposition)_

[[!redirects Gauss decompositions]]

