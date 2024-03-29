

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry reviews basics of [[periodic cohomology theory|periodic]] [[multiplicative cohomology theory|multiplicative]] [[cohomology theory|cohomology theories]] and their relation to formal group laws.

=--

Next:

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]


## rough notes from a talk##

>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention

A complex oriented [[cohomology]] theory (meant is here and in all of the following a [[generalized (Eilenberg-Steenrod) cohomology]]) is one with a _good notion of [[Thom class]]es, equivalently first [[Chern class]] for complex [[vector bundle]]_

>(this "good notion" will boil down to certain extra assumptions such as multiplicativity and periodicity etc. What one needs is that the [[cohomology ring]] assigned by the cohomology theory to $\mathbb{C}P^\infty \simeq \mathcal{B}U(1)$ is a power series ring. The formal variable of that is then identified with the universal first Chern class as seen by that theory).

ordinary [[Chern class]] lives in [[integral cohomology]]
$
  H^*(-,\mathbb{Z})
$

or in [[K-theory]] $K^*(-)$ where for a [[vector bundle]] $V$ we would set $c_1(V) := ([V]-1)\beta$ where $\beta$ is the [[Bott generator]].

In the first case we have that under [[tensor product]] of [[vector bundle]]s the class behaves as 

$$
  c_1(V\otimes W) = c_1(V) + c_1(W)
$$

whereas in the second case we get

$$
  c_1(V \otimes W) = c_1(V)c_1(W)\beta^{-1} + c_1(V) + c_1(W)
  \,.
$$

In general we will get that the [[Chern class]] of a tensor product is given by a certain [[power series]] $E^*(pt)$


not all [[formal group law]]s arises this way. the [[Landweber criterion]] gives a condition under which there is a cohomology theory

**definition** of complex-orientation

there is an

$$
  x \in \tilde E^2(\mathbb{C}P^\infty)
$$

such that under the map

$$
  \tilde E^2(\mathbb{C}P^\infty)
  \to 
  \tilde E^2(\mathbb{C}P^1)
  \simeq
  \tilde E^2(S^1)
  \simeq E^0({*})
$$

induced by

$\mathbb{C}P^1 \to \mathbb{C}P^\infty$

we have $x \mapsto 1$

**remark** this also gives [[Thom class]]es since
$\mathbb{C}P^\infty \to (\mathbb{C}P^\infty)^\gamma$ is a [[homotopy equivalence]]  

$$
  \tilde E^2((\mathbb{C}P^\infty)^\gamma)
  \simeq
  \tilde E^2((\mathbb{C}P^\infty))
  \ni X
$$

Thom iso $\tilde H^{*+2}(X^\gamma) \simeq H^*(X)$

...


(here and everywhere the tilde sign is for [[reduced cohomology]])

**definition (Bott element and even periodic cohomology theory)**

* An [[even cohomology theory]] is one whose odd cohomology rings vanish: $E^{2k+1}({*}) = 0$.

* A [[periodic cohomology theory]] is one with a [[Bott element]] $\beta \in E^2({*})$ which is invertible (under multiplication in the [[cohomology ring]] of the point) 

  so that gives an isomorphism $(-)\cdot \beta : E^*({*}) \simeq E^{*+2}({*})$


Periodic cohomology theories are complex-orientable. $E^*(\mathbb{C}P^\infty)$ can be calculated using the [[Atiyah-Hirzebruch spectral sequence]]

$$
  H^p(X, E^q({*})) \Rightarrow E^{p+q}(X)
$$




notice that since $\mathbb{C}P^\infty $ is [[homotopy equivalence|homotopy equivalent]] to the [[classifying space]] $\mathcal{B}U(1)$ (which is a topological group) it has a product on it

$$
  \mathbb{C}P^\infty \times  \mathbb{C}P^\infty
  \to 
  \mathbb{C}P^\infty
$$

which is the one that induces the [[tensor product]] of [[line bundle]]s classified by maps into $\mathbb{C}P^\infty$.

on (at least on even periodic cohomology theories) this induces a map of the form

$$
  \array{
    \mathbb{C}P^\infty \times  \mathbb{C}P^\infty
    &\to& 
    \mathbb{C}P^\infty
    \\
    E({*})[[x,y]]  &\leftarrow& E(*)[[t]]
   \\
   f(x,y) &\leftarrow |& t
  }
$$

this $f$ is called a [[formal group law]] if the following conditions are satisfied

1. **commutativity** $f(x,y) = f(y,x)$

1. **identity** $f(x,0) = x$

1. **associtivity** f(x,f(y,z)) = f(f(x,y),z)

**remark** the second condition implies that the constant term in the power series $f$ is 0, so therefore all these power series are automatically invertible and hence there is no further need to state the existence of inverses in the formal group. So these $f$ always start as 

$$
  f(x,y) = x + y + \cdots
$$


The [[Lazard ring]] is the "universal formal group law". it can be presented as by generators $a_{i j}$ with $i,j \in \mathbb{N}$

$$
  L = \mathbb{Z}[a_{i j}] / (relations 1-3 below)
$$

and relatins as follows

1. $a_{i j} = a_{j i}$

1. $a_{10} = a_{01} = 1$; $\forall i \neq 0: a_{i 0} = 0$

1. the obvious associativity relation

the universal formal group law we get from this is the power series in $x,y$ with coefficients in the [[Lazard ring]] 

$$
  \ell(x,y) = \sum_{i,j} a_{i j} x^j y^j \in L[[x,y]]
  \,.
$$

**remark** the formal group law is not canonically associated to the cohomology theory, only up to a choice of rescaling of the elements $x$. But the underlying [[formal group]] is independent of this choice and well defined.

For any ring $S$ with formal group law $g(x,y) \in power series in x,y with coefficients in S$ there is a unique morphism $L \to S$ that sends $\ell$ to $g$.

**remark** Quillen's theorem says that the Lazard ring is the ring of complex cobordisms


**some universal cohomology theories** $M U$ is the [[spectrum]] for [[complex cobordism cohomology theory]]. The corresponding [[spectrum]] is in degree $2 n$ given by

$$
  M U(2n) = Thom
  \left(
    standard associated bundle to universal bundle
    \array{
      E U(n) \\ \downarrow \\ B U(n)
    }
  \right)
$$

periodic [[complex cobordism cohomology theory]] is given by

$$
  M P = \vee_{n \in \mathbb{Z}} \Sigma^{2 n} M U
$$

we get a canonical [[oriented cohomology theory|orientation]] from

$$
  \omega : \mathbb{C}P^\infty \stackrel{\simeq}{\to}
  M U(1)
  \;\;\;\;
  M U(\mathbb{C}P^\infty)
$$

this is the universal even periodic cohomology theory with orientation

**Theorem (Quillen)** the [[cohomology ring]] $M P(*)$ of periodic [[complex cobordism cohomology theory]] over the point together with its [[formal group law]] is naturally isomorphic to the universal  [[Lazard ring]] with its [[formal group law]] $(L,\ell)$

how one might make a [[formal group law]] $(R,f(x,y))$ into a cohomology theory

use the classifying map $M P({*}) \to R$
to build the [[tensor product]] 

$$
  E^n(X) := M P^n(X) \otimes_{M P({*})} R
$$ 

this construction could however break the left exactness condition. However, $E$ built this way will be left exact of the ring morphism $M P({*}) \to R$ is a flat morphism. This is the [[Landweber exactness]] condition (or maybe slightly stronger).

[[!redirects A Survey of Eilliptic Cohomology - cohomology theories]]