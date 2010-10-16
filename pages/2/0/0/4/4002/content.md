
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Connected topos
* table of contents
{: toc}

## Idea

If we view a (Grothendieck) [[topos]] as a generalized [[topological space]], then a *connected topos* is a generalization of a [[connected topological space]].

More generally, a *connected geometric morphism* $p\colon E\to F$ is a "relativized" notion of this, saying that $E$ is "connected as a topos over $F$."

## Definition

A [[geometric morphism]] $p\colon E\to F$ is **connected** if its inverse image part $p^*$ is [[fully faithful functor|full and faithful]].

A [[Grothendieck topos]] $E$ is **connected** if the unique geometric morphism $E \to Set = Sh(*)$ is connected.  If $E$ is the [[topos of sheaves]] on a [[topological space]] $X$ (or more generally a [[locale]]), then this is equivalent to the usual definition of connectedness for $X$ (see C1.5.7 in the [[Elephant]]).

## Connected locally connected morphisms

For geometric morphisms which are also [[locally connected geometric morphism|locally connected]], connectedness can be phrased in an especially nice form.

+-- {: .un_prop}
###### Proposition
If $p\colon E\to F$ is locally connected, then it is connected if and only if the left adjoint $p_!$ of the inverse image functor (which exists, since $p$ is locally connected) preserves the terminal object.
=--
+-- {: .proof}
###### Proof
This is C3.3.3 in the [[Elephant]].
=--

Strengthenings of this condition include
* a [[strongly connected geometric morphism]], which is locally connected such that $p_!$ preserves all finite products, and
* a [[totally connected geometric morphism]], which is locally connected such that $p_!$ preserves all finite limits.


## Examples


The [[gros topos|gros]] [[sheaf topos]] $Sh(CartSp)$ on the [[nLab:site]] [[CartSp]] -- which contains the [[quasi-topos]] of [[diffeological space]] -- is a connected topos:

crucially the site [[CartSp]] with its standard [[nLab:Grothendieck topology]] has the special property that a _constant presheaf_ is already a [[sheaf]]: since all the [[Cartesian space]]s are connected. So the [[constant sheaf]] functor

$$
  LConst := L \circ Const : Set \stackrel{Const}{\to} PSh(CartSp) 
  \stackrel{L}{\to} Sh(CartSp)
$$

does not actually involve any [[sheafification]] and is really just the constant presheaf functor that happens to factor through sheaves.

This implies that the [[left adjoint]] $\Pi_0 : Sh(CartSp) \to Set$ of $LConst = Const$, which always exists at the level of presheaves, where it is given by the [[colimit]] operation

$$
  \Pi_0 = \lim_\to
$$

is already also the left adjoint at the level of sheaves. By the [[co-Yoneda lemma]] the [[colimit]] over any [[representable presheaf]] is the singleton set

$$
  \lim_\to y(V) = \int^{U \in C} C(U,V) = \int^{U \in C} C(U,V) \cdot * = *
  \,.
$$ 

For here $\Pi_0$ takes every [[Cartesian space]] $\mathbb{R}^n$ to the singleton, reflecting the fact that every Cartesian space is, indeed, conncected. So in particular the terminal object, which is represented by $\mathbb{R}^0$ is sent ot the singleton set. By the above proposition therefore $Sh(CartSp)$ is connected.


## Related concepts

* [[essential geometric morphism]]

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* **connected topos** / [[∞-connected (∞,1)-topos]]

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]



[[!redirects connected topoi]]
[[!redirects connected toposes]]
[[!redirects connected locally connected topos]]
[[!redirects connected locally connected topoi]]
[[!redirects connected locally connected toposes]]
[[!redirects connected geometric morphism]]
[[!redirects connected geometric morphisms]]
[[!redirects connected locally connected geometric morphism]]
[[!redirects connected locally connected geometric morphisms]]
