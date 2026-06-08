\tableofcontents

## Definition

Given a commutative ring $k$ and a field $L\supset k$, an element $x\in L$ is said to be __integral__ over $k$ if it satisfies a [[monic polynomial]] equation with coefficients in $k$, or equivalently, there exist a finitely-generated nonzero $k$-submodule $M\subset L$ such that $x M \subset M$. 

A commutative ring $K\supset k$ is said to be __integral__ over $k$ if every element of $K$ is integral over $k$. The relation of integrality of overrings is transitive. If $f:K\to K'$ is a surjective homomorphism of rings and $K$ integral over $k\subset K$, then $K' = f(K)$ is integral over $f(k)$.

The set of all elements of $L$ integral over $k$ is a subring of $L$ called the __integral closure__ of $k$ in $L$. We say that $k$ is __integrally closed in__ $L$ if it equals its own integral closure in $L$.

An [[integral domain]] $k$ is __integrally closed__ if it is integrally closed in the quotient field of $k$. 

## Properties

If $k$ is an integrally closed [[Noetherian ring|Noetherian domain]] and $L$ a finite separable field extension of its quotient field $Q(k)$ then the integral closure of $k$ in $L$ is finitely generated over $k$. 

If $k$ is a principal ideal ring and $L$ a finite separable extension of degree $n$ of its quotient field $Q(k)$, then the integral closure of $k$ in $L$ is a free rank $n$-module over $k$. 

If $K$ is integral over a subring $k$ then for any multiplicative set $S\subset k$, the localization $S^{-1} K$ is integral over $S^{-1} k$.  

Every [[unique factorization domain]] is integrally closed. 

## In constructive mathematics

In [[constructive mathematics]], algebraic closure for [[Heyting fields]] is stronger than [[integral closure]] for Heyting fields, since every monic polynomial has a well-defined degree, while not every nonconstant polynomial function, in the sense of being [[tight apartness relation|apart from]] every constant polynomial function, has a well-defined degree and thus might not be able to be made monic. This difference is reflected in the two versions of the [[fundamental theorem of algebra]], one for monic polynomials and one for non-constant polynomials (see [Geuvers, Wiedijk, & Zwanenburg 2000](#GWZ00)). 

## See also

* [[fundamental theorem of algebra]]

## References

* Serge Lang, _Algebraic number theory_, GTM 110, Springer 1970, 2000
* O. Zariski, Samuel, _Commutative algebra_
* N. Bourbaki, _Commutative algebra_
* Z. Borevich, I. Shafarevich, _Number theory_
* E. Artin, J. Tate, _Class field theory_, 1967
* A. Weil, _Basic number theory_

* {#GWZ00} Herman Geuvers, Freek Wiedijk, Jan Zwanenburg, *A Constructive Proof of the Fundamental Theorem of Algebra without using the Rationals*, TYPES '00: Selected papers from the International Workshop on Types for Proofs and Programs, Pages 96 - 111, 08 December 2000 &lbrack;[web](https://dl.acm.org/doi/10.5555/646540.696038), [pdf](https://www.cs.ru.nl/F.Wiedijk/pubs/kneser.pdf)&rbrack;

[[!redirects integrally closed]]

[[!redirects integrally closed ring]] 
[[!redirects integrally closed rings]]

[[!redirects integrally closed field]]
[[!redirects integrally closed fields]] 