<div class="rightHandSide toc">
[[!include cohomology - contents]]

***

[[!include higher category theory - contents]]


***

[[!include higher geometry - contents]]

***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

and

* [[Gromov-Witten invariants]]

see there for background and context.

This entry contains a basic introduction to [[elliptic curve]]s and their [[moduli space]]s.


=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]



>the following are rough unpolished notes taken more or less verbatim from some seminar talk -- needs attention, meaning: **somebody should go through this and polish**


***

#Contents#

* toc
{:toc}


# Introduction #

The slogan is: for $A$ a [[cohomology theory]], finding [[equivariant cohomology]] $A$-theory corresponds to finding [[group scheme]] over $A({*})$.

The main example we'll be looking at here is complex [[K-theory]].

# Notions of equivariant cohomology #

## Borel equivariant cohomology ##

**Remark** if $A_G$ is an [[equivariant cohomology]] theory and if $Y \to X$ is a $G$-[[principal bundle]] then we want that $A_G(Y) \simeq A(X)$.
So whenever we have a $G$-space where the $G$-[[action]] is free enough.

Let $X$ be a $G$-space, form the [[Borel construction]] $\mathcal{E}G \times_G X$ with $\mathcal{E}G \to \mathcal{B}G$ the [[universal principal bundle]].

Then we can _define_ 

$$
  A_G^{Borel}(X) := A(\mathcal{E}G \times_G X)
  \,.
$$

> notice that $\mathcal{E}G \times_G X$ is the realization of the [[action groupoid]] $X//G$. This Borel equivariant cohomology theory is what is discussed currently at the entry [[equivariant cohomology]]. The following will actually define a refinement of the discussion currently at [[equivariant cohomology]].

**Problem** If the cohomology theory is given by a geometric model, such as [[topological K-theory]] in terms of [[vector bundle]]s or [[elliptic cohomology]] potentially in a [[geometric model for elliptic cohomology]], then the above notion of equivariant cohomology need not coincide with the cohomology theory given by the equivariant version of these geometric models. In particular, equivariant [[vector bundle]]s are geometric cocycles of equivariant [[K-theory]] $K_G$ and there is a morphism

$$
  K_G(X) \to K_G^{Borel}(X)
$$

but it is not an [[isomorphism]]. Instead, $K_G$ is a _completion_ of $K_G^{Bor}$.

Here $K_G(X)$ is the [[Grothendieck group]] of [[equivariant vector bundle]]s over the [[G-space]] $X$ (say $G$ is a compact [[Lie group]]).

## Grothendieck ring of equivariant vector bundles ##

**Definition** An [[equivariant vector bundle]] over $X$ is

* a [[G-space]] $E$ and $G$-equivariant map $p : E \to X$ such that this is a (complex, here) [[vector bundle]] of finite rank

* for each $g \in G$ the map $g : E_x \to E_{g x}$ is linear.

Morephism are the obvious $G$-equivariant morphisms of [[vector bundle]]s.

*examples**

1. $X$ a trivial $G$-space,then a $G$-equivariant vector bundle is a family of complex representations;

1. for $E \to X$ a [[vector bundle]]

1. if $G$ acts smoothly on $X$ then the complexified [[tangent bundle]] $T X \otimes \mathbb{C} \to X$ is a $G$-equivariant vector bundle.

**remark** The [[category]] of $G$-[[equivariant vector bundle]], has 

* [[direct sum]] $\oplus$ 

* [[tensor product]] $\otimes$

And we can pull back $Vect^G$ \to $Vecg^H$ along any group homomorphism $\phi : H \to G$

So we are entitled to say

**definition** the [[Grothendieck group]] of $Vect^G(X)$ is

$$
  K_G(X) := Groth(E \to X, \oplus)
  \,.
$$

With the remaining [[tensor product]] $\otimes$ this yields a commutative [[ring]].

**proposition** 

1. if $X = pt$ then $K_G(X) \simeq Rep(G)$ is the [[representation ring]] of $G$.

   1. in general, $K_G(X)$ is an algebra over $Rep(G)$.

1. if $G$ [[free axction|acts freely]] on $X$, then $K_G(X) \simeq K(X/G)$.


So in particular

$$
  K(\mathcal{E}G \times_G X)
  \simeq
  K_G(\mathcal{E}G \times X)
$$

so we get a map 

$$
  \alpha : K_G(X) \to K_G(\mathcal{E}G \times X)
  \simeq
  K(\mathcal{E}G \times_G X)
  := K_G^{Borel}(X)
$$

**theorem** (Atiyah-Segal) This $\alpha$ induces an [[isomorphism]]

$$
  \hat K_G(X) \simeq K_G^{Borel}(X)
$$

where

$$
  \hat K_G(X) := \lim_\leftarrow K_G(X)/I_G^n K_G(X)
$$

where $I_G = ker(Rep(G) \simeq K_G({*}) \to K_G(\mathcal{E}G) \simeq K(\mathcal{B}G)
  \stackrel{\epsilon}{\to} \mathbb{Z})$

**consider** $X = {*}$, $G = S^1$, $\mathbb{C}P^\infty \simeq \mathcal{B}S^1$

$$
  \alpha : Rep(G)
  \to 
  K(\mathcal{B}G)
  = K(\mathbb{C}P^\infty)
  \simeq
  \mathbb{Z}[ [ t ] ]
$$

1. since $S^1$ is an abelian group, every [[irreducible representation]] is 1-dimensional
   
   $$
     \phi : S^1 \to \mathbb{C}^\times
   $$

1. $\chi : S^1 \hookrightarrow \mathbb{C}^times$

$$
  Rep(G) \simeq \mathbb{Z}[\chi, \chi^{-1}]
  \,.
$$

## algebraic interpretation ##

**goal now** find an algebraic interpretation of $\alpha$ such that

$$
  Rep(S^1) = \mathcal{O}_{G_m}
$$

and

$$
  Rep(\mathbb{C}P^\infty) = \mathcal{O}_{\hat G_m}
$$

adopt the [[functor of points]] perspective

$$
  X : CRings \to Set
$$

a [[functor]].

For $A \in $ [[CRing]] get a spectrum

$$
  Spec A : R \mapsto CRing(A,R)
$$

for $X$ a functor, it is an [[affine scheme]] if it is a [[representable functor]] in that there is $A$ with $X \simeq Spec A$.

**examples**  

1. $\mathbb{A}^n(R) := R^n$

1. $\hat \mathbb{A}^n(R) := Nil(R)^n$

1. $G_m(R) := R^\times \hookrightarrow \mathbb{A}^1(R)$

1. $\mathbb{P}^n(R) := R^{n+1}/\sim$, where $\sim$ is multiplication by $R^\times$

**proposition**

$G_m$ is affine.

**proof** $A = \mathbb{Z}[x,x^{-1}]$, let $u \in Spec(\mathbb{A}(R))$ a map $u A \to R$, then define 

$$
  \phi : Spec A \to G_m
$$

by

$$
  u \mapsto u(x)
$$

Conversely, given $v \in G_m(R) = R^\times$, define

$$
  \Psi : G_m \to Spec A
$$

by

$$
  v \mapsto \Psi(v)
$$

with

$$
 \Psi(v)(\sum_k a_k x^k) := \sum_k a_k v^k
$$

**endofproof**

similarly, $\mathbb{A}^n \simeq Spec \mathbb{Z}[x_1, \cdots, x_n]$

# group schemes #

Given a functor $X : CRing \to Set$ define the ring of cuntions $\mathcal{O}_X$ as

$$
  \mathcal{O}_X := Hom_{Func(CRing,Set)}(X, \mathbb{A}^1)
$$

in the [[functor category]].

> notice notation: this is global sectins of the [[structure sheaf]], not the structure sheaf itself, properly speaking

we have

$$
  \mathcal{O}_{Spec A}
  \simeq
  A
$$

so that in particular 

$$
  \mathcal{O}_{G_m} \simeq \mathbb{Z}[x,x^{-1}]
  \,.
$$

**definition**

Let $X$ be an [[affine scheme]] and $Y : CRing \to Set$ a [[functor]] with a [[natural transformation]] $p : Y \to X$. A **system of formal coordinates** is a sequence of maps

$$
  X_i : Y \to \hat \mathbb{A}^1
$$

such that

$$
  a \mapsto (x_1(a), \cdots, x_n(a), p(a))
  \in 
  \hat \mathbb{A}^n \times X
$$

is an [[isomorphism]]. A $Y$ that admits a system of formal coorrdinates is a **[[formal scheme]]** over $X$.

> **warning** very restrictive definition. See [[formal scheme]]

A **[[formal group]]** $G$ over a [[scheme]] $X$ is a one-dimensional [[formal scheme]] with specified abelian [[group]] structure on each [[fiber]] $p^{-1}\{x\}$.

This means that there is a natural map

$$
  \sigma : G \times_X G \to G
$$

and a natural map $\zeta : X \to G$ which maps $x \mapsto 0 \in p^{-1}\{x\}$.

**definition (formal multiplicative group)**

define $\hat G_m$ on each $R \in CRing$ by

$$
  \hat G_m(R)
  = 
  \left\{
    1+n | n \in Nil(R)
  \right\}
$$

which is a group under multiplication. 

there is an [[isomorphism]] of underlying [[formal scheme]]s

$$
  \hat G_m  \simeq \hat \mathbb{A}^1
$$


> darn, omitting some material because my browser window crashed... this was about the derivation of the statement that...

$$
  \mathcal{O}_{\hat G_m} \simeq \mathbb{Z}[ [ t] ]
  \,.
$$



**recall** we have a morphism $\alpha : Rep(S^1) \to K(\mathbb{C}P^\infty)$

such that 

$$
  \mathcal{O}_{G_m}
  \simeq
   \mathbb{Z}[x,x^{-1}]
   \simeq
   Rep(S^1)
  \to 
  K(\mathbb{C}P^\infty) \simeq
  \mathbb{Z}[ [ t ] ]
  \simeq
  \mathcal{O}_{\hat G_m}
$$

is the canonical inclusion


$$
  \mathcal{O}_{G_m} \to \mathcal{O}_{\hat G_m}
$$
  
**exercise**

$$
  x \in \mathbb{Z}[x,x^{-1}] \simeq \mathcal{O}_{G_m}
$$

is the natural transformation $R^\times \to R$

and

$$
  t \in \mathbb{Z}[ [t] ] \simeq
  \mathcal{O}_{\hat G_m}
$$

is the natural transformation

$$
  \{1 + Nil(R)\}
  \to
  Nil(R)
  \to 
  R
$$

so that we get a map

$$
  \mathcal{O}_{G_m} \to \mathcal{O}_{\hat G_m}
$$

by sending $x$ to $1 + t$, and this corresponds to taking the [[germ]] of functons at $1 \in G_m$

#lesson #

given $G$ an algebraic group sich that the [[formal spectrum]] $Spf A(\mathcal{C}P^\infty)$ is the completion $\hat G$, define $A_{S^1}({*}) =: \mathcal{O}_{G}$ then passing to germs gives a completion map

$$
  A_{S^1}({*}) \to A(\mathbb{C}P^\infty) = 
  A^{Bor}_{S^1}({*})
$$