#Idea#

The notion of _weighted limit_ is naturally understood from the point of view on [[limit]]s described at [[representable functor]].

Weighted limits make sense and are considered in the general context of $V$-[[enriched category theory]], but restrict attention to $V=$ [[Set]] for the moment, in order to motivate the concept.

Let $K$ denote the small category which indexes [[diagram]]s over which we want to consider limits and eventually weighted limits. Notice that for 

$$
  F : K \to Set
$$

a [[Set]]-valued functor on $K$, the limit of $F$ is canonically identified simply with the set of [[cone]]s with tip the singleton set $pt = \{\bullet\}$:

$$
  lim F = [K,Set](\Delta pt, F)
  \,.
$$

This means, more generally, that for 

$$
  F : K \to C
$$

a functor with values in an arbitrary category $C$, the object-wise limit of the functor $F$ under the [[Yoneda embedding]]

$$
  C(-,F(-)) : K \stackrel{F}{\to} C \stackrel{Y}{\to} Set^{C^{op}}
$$

which appears in the discussion in example 1 at [[representable functor]] can be expressed by the right side of

$$
  lim C(-,F(-)) = [K,Set](\Delta pt, C(-,F(-)))
  \,.
$$

(Recall that this is the limit over the diagram $C(-,F(-)) : K \to Set^{C^{op}}$ which, if [[representable functor|representable]] defines the desired limit of $F$.)

The **idea** of weighted limits is to 

1. allow in the formular above the particular functor $\Delta pt$ to be replaced by any other functor $W : K \to Set$;

2. to generalize everything straightforwardly from the [[Set]]-[[enriched category|enriched]] context to arbitrary $V$-enriched contexts.

#Definition#


#References#

In 

* E. Riehl, _Weighted limits and colimits_ (2008) ([pdf](http://www.math.uchicago.edu/~eriehl/cat/weighted.pdf))

[[Emily Riehl]] gives an account of lectures by [[Mike Shulman]] on the subject.