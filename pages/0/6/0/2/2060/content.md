
# Idea #
 
The _universal fibration of [[(infinity,1)-category|(∞,1)-categories]] is the [[generalized universal bundle]] of $(\infty,1)$-categories in that it is [[Cartesian fibration]]

$$
  p : Z \to (\infty,1)Cat^{op}
$$

over the [[opposite category]] of the [[(∞,1)-category of (∞,1)-categories]] such that

* its fiber  $p^{-1}(C)$ over $C \in (\infty,1)Cat$ is just the $(\infty,1)$-category $C$ itself;

* every [[Cartesian fibration]] $p : C \to D$ arises as the [[pullback]] of the universal fibration along an [[(∞,1)-functor]] $S_p : D \to (\infty,1)Cat^{op}$.


Recall from the discussion at [[generalized universal bundle]] and at [[stuff, structure, property]] that for [[n-category|n-categories]] at least for low $n$ the corresponding universal object was the $n$-category $n Cat_*$ of [[pointed object|pointed]] $n$-categories. $Z$ should at least morally be $(\infty,1)Cat_*$.


## Restriction of $\infty$-Groupoids ##

The universal fibration of $(\infty,1)$-categories restricts to a [[Cartesian fibration]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ over [[∞-Grpd]] by [[pullback]] along the inclusion morphism $\infty Grpd \hookrightarrow (\infty,1)Cat$

$$
  \array{
    Z|_{\infty Grpd} &\to& Z
    \\
    \downarrow && \downarrow
    \\
    \infty Grpd^{op} &\hookrightarrow& (\infty,1)Cat^{op}
  }
  \,.
$$

The [[∞-functor]] $Z|_{\infty Grpd} \to \infty Grpd^{op}$ is even a [[right fibration]] and it is the universal right fibration. 

+-- {: .un_prop }
###### Proposition

The following are equivalent:

* An [[∞-functor]] $p : C \to D$ is a [[right fibration]].

* Every functor $S_p : D \to (\infty,1)Cat$ that classifies $p$ as a [[Cartesian fibration]] factors through [[? Grpd]].

* There is a functor $G_p : D \to \infty Grpd$ that classifies $p$ as a [[right fibration]].

=--

+-- {: .proof}
###### Proof

This is proposition 3.3.2.5 in [[Higher Topos Theory|HTT]].

=--





# Definition #

see section 3.3.2 of [[Higher Topos Theory|HTT]].

#References#

section 3.3.2 of

* [[Jacob Lurie]], [[Higher Topos Theory]]

[[!redirects universal fibration of (∞,1)-categories]]