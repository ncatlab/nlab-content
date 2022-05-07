+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Arithmetic
+-- {: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### For abelian groups

For $A$ an [[abelian group]] and $(a,b) \in A \times A$ a pair of [[elements]], their **difference** is the element 

$$
 b - a \coloneqq b + a^{-1} \in A
 \,.
$$

This is often considerd for the case that $A$ is the abelian group underlying a [[vector space]] $V$, which which case one typically denotes the elements instead as $(\vec x, \vec y) \in V \times V$ and their difference as

$$
  \vec y - \vec x \in V
  \,.
$$

Specifically if $V = \mathbb{R}$ is the [[real line]] or the [[rational numbers]] of just the [[integers]], one just writes $y-x$. Etc.

### For commutative semigroups and magmas

For $(A,+)$ a [[commutative]] [[semigroup]] or [[magma]] and $(a,b) \in A \times A$ a pair of [[elements]], their **difference**, if it exists, is an element $c \in A$ such that

$$
 c + a = b
 \,.
$$

$a$ is called the __subtrahend__ of $b$ and $b$ is called the __minuend__ of $a$. 

For example, in the ordered commutative semigroup of positive integers $\mathbb{N}^+$, two positive integers $m,n \in \mathbb{N}^+$ have a difference $n - m$ if $m \lt n$. 

If the magma is a multiplicative monoid $\cdot$ of a [[commutative ring]], then the difference is usually called a __quotient__ (see [[divisor (ring theory)]]. 

A commutative [[quasigroup]] is a commutative magma such that every pair of elements $(a,b) \in A \times A$ has a difference. 
 
## Related concepts

* [[subtraction]]

* [[monus]]

* A _[[derivative]]_ is a limiting ratio of differences.



[[!redirects differences]]

[[!redirects subtrahend]]
[[!redirects subtrahends]]
[[!redirects minuend]]
[[!redirects minuends]]