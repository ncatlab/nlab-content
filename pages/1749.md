* for disambiguation see [[homotopy]]

#Idea#


+-- {: .standout}
 The following abstract nonsense is a bit tentative.
 See warning below.
=--

 Ordinary _homotopy_ is a way to probe objects in an [[(infinity,1)-topos]] $\mathbf{H}$ by mapping [[sphere]]s into them:

the ordinary [[homotopy group]] $\pi_n(X,x)$ of an object $X \in \mathbf{H}$ is the fiber ober $x \in X$ of the morphism

$$
  H(S^n, X) \to H({*},X) \simeq \pi_0(X)
$$

induced on $H$, the [[homotopy category of an (infinity,1)-category]] associated to $\mathbf{H}$.

$$
  H(S^n ,X) := \pi_0(\mathbf{H}(S^n,X))
  \,.
$$

In this sense _homotopy_ is the notion that is [[Eckmann-Hilton duality|Eckmann-Hilton dual]] to [[cohomology]].

For a more precise statement of homotopy in $(\infty,1)$-toposes see section 6.5.1 of

* [[Jacob Lurie]], [[Higher Topos Theory]] .

+-- {: .standout}
  Warning: notice that in that section 6.5.1 
  homotopy groups in an $(\infty,1)$-topos are at least not _manifestly_ defined in this way, though it should come close. Somebody should have a close look and sort this out.
=--


**Remark** This duality suggests that more generally we may be entitled to speak for $B$ and $X$ objects in $\mathbf{H}$ of

$$
  H(B,X) := \pi_0 \mathbf{H}(B,X)
$$

as the **homotopy of $X$ with co-coefficients $B$**.

Examples of such constructions exist, but are rarely thought of (or even recognized as) generalizations of the notion of homotopy. Rather, by the above dulity, the same situation is usually regarded in the context of [[cohomology]], which, still by the above duality, is just as well.
