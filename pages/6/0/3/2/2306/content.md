#Idea#

The _Lazard_ [[ring]] is 

* the [[cohomology ring]] that the [[complex cobordism cohomology theory]] assigns to the point;

and at the same time

* the universal coefficient ring for [[formal group law]]s.

#Details#

The _Lazard ring_ can be presented as by generators $a_{i j}$ with $i,j \in \mathbb{N}$

$$
  L = \mathbb{Z}[a_{i j}] / (relations 1-3 below)
$$

and relatins as follows

1. $a_{i j} = a_{j i}$

1. $a_{10} = a_{01} = 1$; $\forall i \neq 0: a_{i 0} = 0$

1. the obvious associativity relation

the universal [[formal group law]] is the power series

$$
  \ell(x,y) = \sum_{i,j} a_{i j} x^j y^j \in L[[x,y]]
$$

in two variables with coefficients in the Lazard ring.


For any [[ring]] $S$ with [[formal group law]] $g(x,y) \in power series in x,y with coefficients in S$ there is a unique morphism $L \to S$ that sends $\ell$ to $g$.


We now describe Quillen's theorem on how the Lazard ring is the cohomlogy ring of peridodic complex cobrdism theory over the point.

**Theorem (Quillen)** Let $M P $ denote the peridodic [[complex cobordism cohomology theory]]. Its [[cohomology ring]] $M P(*)$ over the point together with its [[formal group law]] is naturally isomorphic to the universal Lazard ring with its formal group law $(L,\ell)$

how one might make a [[formal group law]] $(R,f(x,y))$ into a cohomology theory

use the classifying map $M P({*}) \to R$
to build the [[tensor product]] 

$$
  E^n(X) := M P^n(X) \otimes_{M P({*})} R
$$ 

this construction could however break the left exactness condition. However, $E$ built this way will be left exact of the ring morphism $M P{{*}) \to R$ is a flat morphism. This is the [[Landweber exactness]] condition (or maybe slightly stronger).

#related entries#

for some context see 

* [[A Survey of Elliptic Cohomology - cohomology theories]]