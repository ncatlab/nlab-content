\tableofcontents

## Idea

A unique factorization ring is like a [[unique factorization domain]] but where we do not require the [[commutative ring]] to be an [[integral domain]]: instead of talking about the non-zero elements, we simply talk about the [[regular elements]] of the commutative ring, since the non-regular elements of a commutative ring are precisely the [[zero divisors]] of a commutative ring. 

This becomes important in [[constructive mathematics]] when we have multiple different notions of [[integral domain]], where one could talk about 

* the non-regular elements being zero, 

* or in rings with a [[tight apartness relation]], the elements apart from zero being regular, 

* or in rings with [[decidable relation|decidable]] tight apartness, where both notions coincide

Instead of having to constantly distinguish between different notions of unique factorization domains, we could simply generalize to unique factorization rings. 

## Definition

Let $R$ be a [[commutative ring]]. We say that an element  $r\in R$ is _regular_ if left multiplication by $r$ is an [[injection]] and right multiplication by $r$ is an injection. We say that an element $r\in R$ is a _unit_ if it is [[invertible element|invertible]]. A non-unit is called _irreducible_ if it can not be represented as a product of two non-units. 

A commutative ring $R$ is a __unique factorization ring__ if every regular non-unit has a factorization $u = r_1 \cdots r_n$ (where $n \ge 1$) as product of irreducibles and this decomposition is unique up to renumbering and rescaling the irreducibles by units. 

Put differently: $R$ is a unique factorization ring precisely when the multiplicative monoid of regular [[principal ideals]] of $R$ (which is isomorphic to the quotient monoid $Reg(R)/R^\times$, where $Reg(R)$ denotes the [[multiplicative subset of regular elements]] in $R$ and $R^\times$ denotes the [[group of units]] in $R$) is a [[commutative monoid]] [[free object|freely generated]] by irreducible principal ideals. 

## Examples

* A [[unique factorization domain]] is precisely a unique factorization ring which is an integral domain; i.e. a commutative ring whose [[multiplicative subset of regular elements]] are precisely the non-zero elements. 

* A [[prefield ring]] is a unique factorization ring where every regular element is invertible. 

## See also

* [[commutative ring]]

* [[GCD ring]]

* [[Euclidean ring]]

* [[prefield ring]]

* [[unique factorization domain]]