# Idea #

In the general sense of [[space and quantity]]
an $(\infty,1)$-[[(infinity,1)-topos|topos]] is a collection of generalized
_spaces_, namely of [[presheaf|presheaves]] 
(precisely: of $(\infty,1)$-[[(infinity,1)-sheaf|sheaves]])
on some [[site]] $S$.

A [[structured (infinity,1)-topos]] $T \simeq Sh_\infty(S)$ is 
an $(\infty,1)$-[[(infinity,1)-topos|topos]] equipped
with a generalized _quantity_: a $C$-valued co-presheaf

$$
  C(-) : G \to T
$$

on some $(\infty,1)$-[[(infinity,1)-category|category]] $G$. 

This is to be interpreted as

* assigning to each object $V \in G$ -- which we think of a _co-test space_

* the $(\infty,1)$-[[(infinity,1)-sheaf|sheaf]] of _structure preserving maps_ from $S$ to $V$,

  * i.e. the sheaf that assigns to each test space $U \in S$ the collection
    of _structure preserving maps_ from $U$ to $V$

Here the structure that is "preserved" is 
to be thought of as _defined_ (implicitly) by the choice of $C(-)$, following the
general idea of [[space and quantity]]. 

In standard motivating example (in the context of [[petit topos]]es), that
of [[derived smooth manifold]]s, we have

* $S = Op(X)$ is the [[category of open subsets]] of a [[topological space]] $X$

* $G = CartSp$ is the full [[subcategory]] of [[Diff]] 
  on Cartesian [[manifold]]s (manifolds of the form
  $\mathbb{R}^n$)
  
* the choice $C(-) : G \to Sh_\infty(Op(X))$ is to be thought of as specifying
  a [[differential geometry]] on $X$ in that it amounts to specifying for each
  open (topological!) subset $U \subset X$ the collection of maps $U \to \mathbb{R}^n$
  that are to count as _smooth_ .
  
It is in this sense that one thinks of $G$ as encoding **geometry** over
topology: $G$ is to be thought of as a category of co-test spaces that are
topological spaces equipped with extra geometrical structure.


# Definitions #

+-- {: .un_defn}
###### Definition

A **homotopical topology** on an $(\infty,1)$-[[(infinity,1)-category|category]] $C$ is
a [[Grothendieck topology]] on $C$ that is generated from its intersection
with a subcategory $G^{ad} \subset G$ whose morphisms -- called the 
**admissable morphisms** have the following properties

* admissable morphisms are stable under [[pullback]];

* admissable morphism satisfy [[category with weak equivalences|2-out-of-3]].
=--

+-- {: .un_defn}
###### Definition

A **geometry (for $(\infty,1)$-toposes)** is 

* An $(\infty,1)$-[[(infinity,1)-category|category]] $G$ that

  * is [[essentially small category|essentially small]];
  
  * has all finite [[limit]]s
  
  * is [[idempotent complete category|idempotent complete]].

* equipped with a _homotopical coverage_ .
=--

+-- {: .un_defn}
###### Definition

For $G$ a geometry, and $T \simeq Sh_\infty(S)$ an $(\infty,1)$-[[(infinity,1)-topos|topos]],
a **$G$-structure on the $(\infty,1)$-topos $T$** making it a 
[[structured (infinity,1)-topos]] is a $(\infty,1)$-[[(infinity,1)-functor|functor]]

$$
  C(-) : G \to T
$$ 

such that

* $C(-)$ is left [[exact functor|exact]] (preseerves finite [[limit]]]s);

* $C(-)$ satisfies [[codescent]] (the dual notion of [[descent]]): 
  for $\pi : (V = \coprod_i V_i) \to W$ any 
  [[cover]] by admissable morphisms in $G$, the induced morphism
  $$
    C(\pi) : C(V) \to C(W)
  $$
  is an [[effective epimorphism]] in $T$, i.e. its [[Cech nerve]]
  is a [[simplicial resolution]] of $C(W)$:
  $$
    Cech(C(\pi)) \stackrel{\simeq}{\to} C(W)
    \,.
  $$
=--


# References #

The general theory is developed in

* **StrSh** [[Jacob Lurie]], _Structured spaces_ ([arXiv](http://arxiv.org/abs/0905.0459))

The special case of "smoothly structured spaces" called [[derived smooth manifold]] is 
discussed in 

* David Spivak, _Derived smooth manifolds_ PhD thesis ([pdf](http://www.uoregon.edu/~dspivak/files/thesis1.pdf))

Apart from looking at the special case this article also contains useful introduction
and details on the general case.

In the version of this that is available on the arXiv ([arXiv](http://arxiv.org/abs/0810.5174))
the point of view is more on bi-presheaves, a useful discussion to the relation
to structured morphisms here is in section 10.1. there.