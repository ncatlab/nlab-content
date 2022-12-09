
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
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

In the same vein that [[commutative rings]] are to [[integral domains]] and [[GCD rings]] are to [[GCD domains]], [[prefield rings]] are to [[fields]]. 

## Definition ##

A commutative ring $R$ is a **prefield ring** if the [[ring of fractions]] of $R$ isomorphic to $R$. Equivalently, a commutative ring $R$ is a prefield ring if for all elements $a \in R$, $a$ is a [[cancellative element]] if and only if $a$ is a [[unit]]; the [[monoid of cancellative elements]] $\mathrm{Can}(F)$ is equivalent to the [[group of units]] $R^\times$. 

## Examples ##

* The [[rational numbers]] $\mathbb{Q}$ are a prefield ring. 

* A classical field $F$ is a prefield ring whose monoid of cancellative elements is the set of elements [[not equal to]] zero. 

* A [[Heyting field]] $F$ is a prefield ring whose monoid of cancellative elements is the multiplicative monoid of elements [[tight apartness relation|apart from]] zero

* A [[local ring]] $F$ is a prefield ring whose monoid of cancellative elements is the multiplicative monoid of elements [[apartness relation|apart from]] the [[ideal]] of [[zero divisors]] $D$. 

* The [[trivial ring]] $0$ is the unique prefield ring up to unique isomorphism such that zero is in the monoid of cancellative elements. The trivial ring is also the terminal prefield. 

* The [[integers modulo n|integers modulo 6]] $\mathbb{Z}/6\mathbb{Z}$ is a prefield ring which is not a [[local ring]], because $2$, $3$, and $4$ are not cancellative: $2 \cdot 3 = 0$, $4 \cdot 3 = 0$ and $2 \cdot 0 = 0$, $3 \cdot 0 = 0$, $4 \cdot 0 = 0$, but $2 \neq 0$, $3 \neq 0$, $4 \neq 0$, and thus, the monoid of cancellative elements is the same as the group of units $\{1, 5\}$. 

* Non-example: the [[integers]] $\mathbb{Z}$ are not a prefield ring. 

## See also ##

* [[commutative ring]]

* [[GCD ring]]

* [[Bézout ring]]

* [[Euclidean ring]]

* [[ring of fractions]]

* [[prevector space]]

* [[field]]

[[!redirects prefield]]
[[!redirects prefields]]

[[!redirects prefield ring]]
[[!redirects prefield rings]]