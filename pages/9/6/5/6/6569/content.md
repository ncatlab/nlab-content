
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Algebra and Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea



Where a [[vector]] specifies a _direction_ and a _magnitude_, a _bivector_ specifies a _plane_ and a magnitude.

A _bivector_ is a [[multivector]] of degree 2.

## Definition

For $V$ a $k$-[[vector space]], a _bivector_ in $V$ is a decomposable element $b = b_1\wedge b_2 \in \wedge^2 V$ of the second [[exterior power]]  of $V$. If the dimension of $V$ is $3$ or less every element in $\Lambda^2 V$ is decomposable, hence bivectors form the vector space, namely $\Lambda^2 V$ itself. The plane associated to a nonzero bivector $b_1\wedge b_2$ is $Span\{b_1,b_2\}$.

Alternatively, a bivector is a 
class of equivalence of pairs $(b_1,b_2)\in V\times V$
by the smallest equivalence relation for which $(b_1,b_2)\sim (b_1+\lambda b_2,b_2)$ for any $\lambda\in k$, $(b_1,b_2)\sim (b_1,\lambda b_1+b_2)$ for any $\lambda\in k$, and $(b_1,b_2)\sim(\frac{b_1}\mu,\mu b_2)$ for any
$\mu\in k\backslash \{0\}$. This axiomatics is parallel (and related) to the axiomatic definition of a $2\times 2$ determinant. 

Some authors (including English wikipedia) by a bivector mean any element 
$\Sigma_i b_{1 i}\wedge b_{2 i}\in\Lambda^2 V$, regardless the decomposability property (and in particular, regardless the dimension of $V$ which guarantees decomposability it $dim V\leq 3$), while they call the decomposable 
elements "simple bivectors".
This terminology may be inconvenient in analytic geometry 
as only the nonzero _simple_ bivectors define a 2-plane 
and most standard constructions which are used in the Euclidean geometry with  bivectors need the restriction, for example the notion of a vector being parallel 
to a bivector (vector $v$ is parallel to
a (simple) bivector $b$ iff $b = v\wedge w$ for some vector $w$, or equivalently
when $v$ is in the span of some pair $b_1,b_2\in V$ 
such that we can write $b = b_1\wedge b_2$).

A bivector is canonically identified with an element of degree 2 in the [[Grassmann algebra]] $\wedge^\bullet V$.

## Properties


If $V$ is equipped with a non-degenerate [[inner product]] then the space $\Lambda^2 V$ is also canonically identified with a subspace of the [[Clifford algebra]] $Cl(V)$.

If we write $\gamma_v \in Cl(V)$ for the Clifford algebra element corresponding to a vector $v \in V$, then this identification is given by the map

$$
  v \wedge w \mapsto 
  \frac{1}{2}\left(\gamma_{v} \cdot \gamma_w - \gamma_w \cdot \gamma_v\right)
  \,.
$$

(The [[inverse]] of this map is called the [[symbol map]].)

Under the [[commutator]] in the Clifford algebra bivectors go to bivectors and hence form a [[Lie algebra]]. This Lie algebra is the [[special orthogonal Lie algebra]] $\mathfrak{so}(V)$ of $V$.



## References

Discussion of [[Clifford algebra]] and [[exterior algebra]] that amplifies the role of bivectors is notably in the references at _[[Geometric Algebra]]_ . 

See also

* Wikipedia, _[Bivector](http://en.wikipedia.org/wiki/Bivector)_

[[!redirects bivectors]]