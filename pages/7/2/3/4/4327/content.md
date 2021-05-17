
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[field]] $k$ and a [[natural number]] $n \in \mathbb{N}$, the **special linear group** $SL(n,k)$ (or $SL_n(k)$) is the [[subgroup]] of the [[general linear group]] $SL(n,k) \subset GL(n,k)$ consisting of those linear transformations that preserve the [[volume form]] on the vector space $k^n$.  It can be canonically identified with the group of $n\times n$ [[matrix|matrices]] with entries in $k$ having [[determinant]] $1$.

This group can be considered as a sub[[variety]] of the [[affine scheme|affine space]] $M_{n\times n}(k)$ of square matrices of size $n$ carved out by the equations saying that the [[determinant]] of a matrix is 1.  This [[variety]] is an [[algebraic group]] over $k$, and if $k$ is the field of [[real number|real]] or [[complex numbers]] then it is a [[Lie group]] over $k$.

## Properties


+-- {: .num_prop #SLOverFieldIsPerfect} 
###### Proposition 

The [[special linear group]] $SL_n(\mathbb{F})$ is a [[perfect group]] for any [[field]] $\mathbb{F}$ and any $n \geq 1$, except for the cases of the [[prime fields]] $\mathbb{F}_2$ and $\mathbb{F}_3$.

=-- 

See for example [here](http://people.brandeis.edu/~igusa/Math101b/SL.pdf), or [Lang 02, theorems XIII 8.3 and 9.2](#Lang02). 


## Examples


+-- {: .num_remark} 
###### Remark

The first case admitted by Prop. \ref{SLOverFieldIsPerfect} is the [[binary icosahedral group]] ([this Prop.](icosahedral+group#IsomorphismToSL25)):

$$
  SL(2,\mathbb{F}_5)
  \;\simeq\;
   2I 
$$

=--

* [[SL(2,Z)]]

* not quite an example: [[SL(2,O)]] (over the [[octonions]])

## Related concepts

* [[general linear group]], 

* [[projective special linear group]]

* [[special unitary group]]

* [[congruence subgroup]]

* [[special linear Lie algebra]]

## References

* {#Lang02} [[Serge Lang]], _Algebra_, $3^{rd}$ edition, Springer 2002 ([pdf](https://math24.files.wordpress.com/2013/02/algebra-serge-lang.pdf))


[[!redirects special linear group]]
[[!redirects special linear groups]]

[[!redirects SL(n)]]

