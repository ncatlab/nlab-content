
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

A commutative ring in which all [[cancellative elements]] are [[invertible]]. 

"Prefield ring" is a placeholder name for a concept which may or may not have another name in the mathematics literature. The idea however is that prefield rings are to fields as [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]]. 

## Definition ##

A commutative ring $R$ is a **prefield ring** if the [[ring of fractions]] of $R$ is isomorphic to $R$. Equivalently, a commutative ring $R$ is a prefield ring if for all elements $a \in R$, $a$ is a [[cancellative element]] if and only if $a$ is a [[unit]]; the [[monoid of cancellative elements]] $\mathrm{Can}(F)$ is equivalent to the [[group of units]] $R^\times$. 

## Examples ##

* The [[rational numbers]] $\mathbb{Q}$ are a prefield ring. 

* A classical field $F$ is a prefield ring whose monoid of cancellative elements is the set of elements [[not equal to]] zero. 

* A [[Heyting field]] $F$ is a prefield ring whose monoid of cancellative elements is the multiplicative monoid of elements [[tight apartness relation|apart from]] zero.

* The [[trivial ring]] $0$ is the unique prefield ring up to unique isomorphism such that zero is in the monoid of cancellative elements. The trivial ring is also the terminal prefield. 

* Given any positive integer $n$, the [[integers modulo n]] $\mathbb{Z}/n\mathbb{Z}$ is a prefield ring whose monoid of cancellative elements consists of all integers $m$ modulo $n$ which are [[coprime]] with $n$.

* Let $F$ be a [[discrete field]] and let $\overline{F}$ be the [[algebraic closure]] of $F$. Given any non-zero [[polynomial]] $p \in \overline{F}[x]$, the [[quotient ring]] $\overline{F}[x]/p \overline{F}[x]$ is a prefield ring whose monoid of cancellative elements consists of polynomials $q \in \overline{F}[x]$ modulo $p$ such that the [[greatest common divisor]] of $p$ and $q$ is an element of the [[group of units]] $\gcd(p, q) \in \overline{F}[x]^\times$.

* Let $R$ be a [[unique factorization domain]] such that for every [[irreducible element]] $x \in R$, the [[ideal]] $x R$ is a [[maximal ideal]]. Given any non-zero element $x \in R$, the [[quotient ring]] $R/x R$ is a prefield ring whose monoid of cancellative elements consists of elements $y \in R$ modulo $x$ such that the [[greatest common divisor]] of $x$ and $y$ is an element of the [[group of units]] $\gcd(x, y) \in R^\times$.

* A prefield ring $F$ is a [[local ring]] if the set of non-cancellative elements, the [[zero divisors]], is the [[Jacobson radical]] $J(F)$. 

* Every [[zero-dimensional ring]] is a prefield ring. 

* Non-example: the [[integers]] $\mathbb{Z}$ are not a prefield ring. 

## See also ##

* [[commutative ring]]

* [[GCD ring]]

* [[Bézout ring]]

* [[unique factorization ring]]

* [[Euclidean ring]]

* [[ring of fractions]]

* [[prevector space]]

* [[field]]

[[!redirects prefield]]
[[!redirects prefields]]

[[!redirects prefield ring]]
[[!redirects prefield rings]]