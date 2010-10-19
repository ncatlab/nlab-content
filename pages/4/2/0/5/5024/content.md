+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos theory
+--{: .hide}
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

If we think of an [[(∞,1)-topos]] as a generalized [[topological space]], then its being **∞-connected** is the analogue of a topological space being (weakly) [[contractible]], i.e. weak-homotopy equivalent to a [[point]].

It is an (∞,1)-categorification of the notion of a [[topos]] being [[connected topos|connected]].

## Definition

Let $\mathbf{H}$ be a (Grothendieck) $(\infty,1)$-topos.  It therefore admits a unique [[geometric morphism]] $(\Gamma,LConst)\colon \mathbf{H}\to \infty Grpd$.  We say that $\mathbf{H}$ is **$\infty$-connected** if $LConst$ is [[fully faithful (∞,1)-functor]|fully faithful]].

More generally, we call a [[geometric morphism]] between $(\infty,1)$-toposes **connected** if its [[inverse image functor]] is fully faithful.

## Properties

+-- {: .un_lemma}
###### Observation

An $\infty$-connected $(\infty,1)$-topos has the _shape_ of the point, in the sense of [[shape of an (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

By a basic property of [[adjoint (∞,1)-functor]]s, $LConst$ being a [[full and faithful (∞,1)-functor]]  is equivalent to the unit of $(LConst \dashv \Gamma)$ being an [[equivalence in a quasi-category|equivalence]]

$$
 Id_{\infty Grpd} \stackrel{\simeq}{\to} \Gamma Lconst
 \,.
$$

By definition of [[shape of an (∞,1)-topos]] this means that $\mathbf{H}$ has the same shape as [[∞Grpd]], which is to say that it shape is [[representable functor|represented]], as a functor $\infty Grpd \to \infty Grpd$, by the terminal object $*$.  Hence it has the "shape of the point".

=--


## Locally ∞-connected and ∞-connected

As in the case of [[connected topos|connected 1-topoi]], we have the following.

+--{: .un_prop}
###### Proposition
If an $(\infty,1)$-topos $\mathbf{H}$ is [[locally ∞-connected (∞,1)-topos|locally ∞-connected]] (i.e. $LConst$ has a left adjoint $\Pi$), then $\mathbf{H}$ is connected if and only if $\Pi$ preserves the terminal object.
=--
+--{: .proof}
###### Proof
This is just like the 1-categorical proof.  On the one hand, if $\mathbf{H}$ is ∞-connected, so that $LConst$ is fully faithful, then by properties of [[adjoint (∞,1)-functors]] this implies that the counit $\Pi \circ LConst \to \Id$ is an equivalence.  But $LConst$ preserves the terminal object, since it is left exact, so $\Pi(*) \simeq \Pi(LConst(*)) \simeq *$.

Conversely, suppose $\Pi(*)\simeq *$.  Then any $\infty$-groupoid $A$ can be written as $A = \colim^A *$, the colimit over $A$ itself of the constant diagram at the terminal object.  Since $LConst$ and $\Pi$ are both left adjoints, both preserve colimits, so we have 
$$
\Pi(LConst(A)) \simeq \Pi(LConst(\colim^A *)) \simeq \colim^A \Pi(LConst(*)) \simeq \colim^A * \simeq A.
$$
Therefore, the counit $\Pi \circ LConst \to \Id$ is an equivalence, so $LConst$ is fully faithful, and $\mathbf{H}$ is ∞-connected.
=--

## Related concepts

* [[locally connected topos]] / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / **∞-connected (∞,1)-topos**

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

[[!redirects ∞-connected (∞,1)-topos]]
[[!redirects ∞-connected (∞,1)-toposes]]
[[!redirects ∞-connected (∞,1)-topoi]]
[[!redirects ∞-connected (∞,1)-geometric morphism]]
[[!redirects ∞-connected (∞,1)-geometric morphisms]]
