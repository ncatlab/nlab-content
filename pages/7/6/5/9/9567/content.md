
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Infinite series
* table of contents
{: toc}

## Motivation

A series is a formal precursor to a various notions of a sum of an infinite sequence. 


## Definition

An (ordinary) __series__ $\sum_{n=0}^\infty a_n$ whose members are the elements $a_n$ in a given additive [[group]] or [[semigroup]] is an ordered pair of a [[sequence]] $(a_n)_{n=0}^\infty$ and a sequence $(b_k)_k$ of its partial [[sums]] $b_k = \sum_{n=0}^k a_k$.

### As an operator

For any group or semigroup $G$, we can [[inductive definition|inductively define]] the finite sum $\mathbb{N}$-[[action]] 

$$\sum_{n=0}^{(-)} (-)(n) : (\mathbb{N} \to G) \times \mathbb{N} \to G$$

as 

$$\sum_{n=0}^{0} a(n) = a(0)$$

$$\sum_{n=0}^{k+1} a(n) = a(k+1) + \sum_{n=0}^{k} a(n)$$

for all $k:\mathbb{N}$ and $a:\mathbb{N} \to G$, such that [[currying]] the action results in the infinite series [[operator]]

$$\sum_{n=0}^\infty (-)(n) : (\mathbb{N} \to G) \to (\mathbb{N} \to G)$$

over the [[function algebra|function $G$-module]] $\mathbb{N} \to G$. 

## Internalisation

In a [[cartesian closed category]] $C$, let $(G,+)$ be an additive [[magma object]], let $(N,0,s)$ be a [[natural numbers object]] in $C$, and let $a:N\to G$ be an __infinite sequence object__ of elements in $G$. Then there exists an infinite sequence object $b:N\to G$ called the __left partial sum infinite sequence object__ of $a$ inductively defined by $b(0) = a(0)$ and $b(s(n)) = b(n) + a(s(n))$, and an infinite sequence object $c:N\to G$ called the __right partial sum infinite sequence object__ of $a$ inductively defined by $c(0) = a(0)$ and $c(s(n)) = a(s(n)) + c(n)$. The element $b(n)$ is called the __left $n$-th partial sum__ of the infinite sequence $a$, and the element $c(n)$ is called the __right $n$-th partial sum__ of the infinite sequence $a$. A __left series object__ is an infinite sequence object with its left partial sum infinite sequence object, and a __right series object__ is an infinite sequence object with its right partial sum infinite sequence object. If the magma object is [[commutative]] and [[associative]], then the left and right partial sum infinite sequence objects of $a$ are equal and just called a __partial sum infinite sequence object__ $d = \sum_{n:N} a(n)$ of $a$, where the element $d(n)$ is the __$n$-th partial sum__. Then s __series object__ is an infinite sequence object with its partial sum infinite sequence object,

## Sum of a series

The most straightforward notion of the **sum** of a series is the [[limit of a sequence|limit]] of its sequence of partial sums, if this sequence converges, relative to some [[topological space|topology]] on the space where the members of the sequence belong to.  A series that does not converge in this sense is called [[divergent series|divergent]]; sometimes these can also be "summed" by fancier techniques.

## Examples

* [[geometric series]]

* [[power series]]

* [[Taylor series]]

* The formal [[e]], $e = \sum_{n=0}^\infty \frac{1}{n!}$, where $\frac{1}{(-)!}:\mathbb{N}\to \mathbb{Q}$

## Related concepts

* [[asymptotic series]]

* [[infinite product]]

* [[divergent series]]

[[!redirects series]]
[[!redirects infinite series]]

[[!redirects infinite sum]]
[[!redirects infinite sums]]
