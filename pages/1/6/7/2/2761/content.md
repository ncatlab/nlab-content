
# Idea #

The statement of the [[Yoneda lemma]] has a straightforward generalization from [[category|categories]] to [[(∞,1)-category|(∞,1)-categories]].

It is not clear if it is known if the full $(\infty,1)$-statement obtained this way does hold.

But one aspect of the generalization of the standard [[Yoneda lemma]], the fact that the [[Yoneda embedding]] is a [[full and faithful functor]], is known to generalize.


#Details#

+-- {: .un_theorem }
###### Theorem
**$(\infty,1)$-Yoneda embedding**

Let $C$ be an [[(∞,1)-category]] and $PSh(C) := Func(C^\op, \infty Grpd)$ be the corresponding [[(∞,1)-category of (∞,1)-presheaves]]. Then the canonical [[(∞,1)-functor]]

$$
  Y : C \to PSh(C) 
$$

is a [[full and faithful (∞,1)-functor]].

=--


+-- {: .proof}
###### Proof

This is proposition 5.1.3.1 in

* [[Jacob Lurie]], [[Higher Topos Theory]]

=--


[[!redirects Yoneda lemma for (∞,1)-categories]]