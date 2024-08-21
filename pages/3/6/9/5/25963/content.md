
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **constant polynomial** is a [[polynomial]] where not having [[degree of a polynomial|degree]] $0$ implies that it is the zero polynomial. (In [[classical mathematics]] this is equivalent to saying that a constant polynomial is a polynomial which either has [[degree of a polynomial|degree]] $0$ or is the zero polynomial.) 

Equivalently, given a [[commutative ring]] $R$, [[polynomial rings]] $R[S]$ are [[free object|free]] [[commutative algebra|commutative $R$-algebras]] on an [[inhabited set|inhabited]] [[finite set]] of [[generators]] $S$; and are characterized by the universal property that it is the [[initial object]] with a [[ring homomorphism]] $h:R \to R[S]$ and a [[function]] $i:S \to R[S]$. A **constant polynomial** of $R[S]$ is a polynomial which is in the [[image]] of the canonical [[ring homomorphism]] $h:R \to R[S]$. As a result, the subring of constant polynomials is in [[isomorphism]] with the [[ground ring]]. 

A related point of view, falling under the rubric "structure-semantics duality" in the old terminology of Lawvere, emanates from the recognition that if $F: Set \to CommRing$ is the left adjoint of the forgetful functor $U: CommRing \to Set$, so that $F$ takes a set $S$ to the polynomial ring $R[S]$, then a polynomial in (say) $n$ variables can be naturally identified with any of the following: 

* An element $1 \to U F(n)$; 

* A ring map $F(1) \to F(n)$; 

* A natural transformation between representable functors $CommRing(F(n), -) \to CommRing(F(1), -)$; 

* A natural transformation $U^n \to U$. 

From that point of view, a polynomial in $n$ variables is constant if the corresponding transformation $U^n \to U$ is constant in the sense of [[constant morphism]], i.e., factors through the terminal functor $U^0$. 



## Related concepts

* [[polynomial]]

* [[degree of a polynomial]] 

* [[constant morphism]] 

* [[constant of a theory]] 

## References

* Wikipedia, [Constant polynomial](https://en.wikipedia.org/wiki/Constant_polynomial)

[[!redirects constant polynomial]]
[[!redirects constant polynomials]]