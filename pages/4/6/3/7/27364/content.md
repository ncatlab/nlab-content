
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Defintion

A **zero-dimensional ring** is a [[commutative ring]] $R$ such that for all elements $x \in R$ there exists an element $a \in R$ and a natural number $n \in \mathbb{N}$ such that $x^n = a x^{n + 1}$

## Properties

Every zero-dimensional ring is a "[[prefield ring]]" in that every [[cancellative element]] is [[invertible element|invertible]]. 

## Examples

* Every [[Boolean ring]] is a zero-dimensional ring.

* Every [[discrete field]] is a zero-dimensional ring which is a [[local ring]] and a [[reduced ring]]. 

* Every commutative [[von Neumann regular ring]] is a zero-dimensional ring which is a [[reduced ring]]. 

* Every [[local Artinian ring]] is a zero-dimensional ring which is also a [[local ring]]. In [[constructive mathematics]], only the [[residually discrete local ring|residually discrete]] local Artinian rings are zero-dimensional local rings. 

* Every [[Artinian ring]] is a zero-dimensional ring which is also a [[Noetherian ring]] and a [[coherent ring]]. 

## BHK interpretation

The [[BHK interpretation]] of a zero-dimensional ring states that for all elements $x \in R$ one can construct an element $a \in R$ and a natural number $n \in \mathbb{N}$ such that $x^n = a x^{n + 1}$. This is equivalent to adding to the ring the structure of an [[endofunction]] $\alpha:R \to R$ and a function to the [[natural numbers]] $\nu:R \to \mathbb{N}$, where the equational axiom is then for all elements $x \in R$, $x^{\nu(x)} = \alpha(x) x^{\nu(x) + 1}$. 

It is unknown if it is possible to construct the above structure from the usual notion of a zero-dimensional ring. However, given a ring $R$ with an endofunction $\alpha:R \to R$, if for all elements $x \in R$ and natural numbers $n:\mathbb{N}$, the [[equality]] $x^n = \alpha(x) x^{n + 1}$ is [[decidable equality|decidable]] (such as the case in [[classical mathematics]]), then the [[existential quantifier]] 
$$\exists n \in \mathbb{N}.x^n = \alpha(x) x^{n + 1}$$
has a [[choice operator]], from which one can construct the function $\nu:R \to \mathbb{N}$ such that for all elements $x \in R$, $x^{\nu(x)} = \alpha(x) x^{\nu(x) + 1}$. 

## Related concepts

* [[Artinian ring]]

* [[von Neumann regular ring]]

## References

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) &lbrack;[doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf)&rbrack;

[[!redirects zero-dimensional ring]]
[[!redirects zero-dimensional rings]]