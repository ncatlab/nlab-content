
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

A **local integral domain** is a [[commutative ring]] which is both a [[local ring]] and a [[integral domain]], hence a commutative ring such that:

* The ring is nontrivial $0 \neq 1$;

* if the sum of two elements $x + y$ is equal to $1$, then $x$ is [[invertible]] or $y$ is invertible;

* If the product of two elements $x \cdot y$ is equal to $0$, then $x = 0$ or $y = 0$. 

## Examples

* Every [[field]] is a local integral domain which is also a [[Artinian ring]]. 

* Given a [[field]] $K$, the ring of [[power series]] $K[[x]]$ is a local integral domain which is not a [[field]]. 

* In general, given a local integral domain $R$, the ring of [[power series]] $R[[x]]$ is a local integral domain. 

* Every [[discrete valuation ring]] is a local integral domain with a [[Dedekind-Hasse norm]]. 

* Every [[finite set|finite]] local integral domain is a [[finite field]]. 

## Properties

Unlike the [[theory]] of [[Heyting fields]], the theory of local integral domains is a [[coherent theory]]. It is the condition that a local integral domain is an [[Artinian ring]] that fails in [[coherent logic]], since it relies on either negation to refer to non-invertible elements (see [[Artinian local ring]]), proper ideals/maximal ideals, or the [[natural numbers]] to refer to the [[descending chain condition]]. Even if one has the natural numbers around to define a [[dependent sequence]] of [[monomorphisms]] for the [[descending chain condition]], such as working internally in an [[arithmetic pretopos]], it is not necessarily the case that every such [[Artinian local ring]] has a maximal ideal or that [[Nakayama's lemma]] holds in [[coherent logic]]. 

While every [[ring homomorphism]] between fields is an [[injection]], it is not the case that every ring homomorphism between local integral domains is an injection. The ring homomorphism which takes a local integral domain to its [[residue field]] is an injection if and only if the local integral domain is already a field. 

## See also

* [[ordered local integral domain]]

* [[discrete valuation ring]]

| [[commutative ring]] | [[reduced ring]] | [[integral domain]] |
---------------------|-----------------|-----------------|
| [[local ring]] | [[reduced local ring]] | [[local integral domain]] |
| [[Artinian ring]] | [[semisimple ring]] | [[field]] |
| [[Weil ring]] | [[field]] | [[field]] |

[[!redirects local integral domain]]
[[!redirects local integral domains]]

[[!redirects local ring without zero divisors]]
[[!redirects local rings without zero divisors]]

[[!redirects local ring without zero-divisors]]
[[!redirects local rings without zero-divisors]]