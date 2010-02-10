* for disambiguation see [[homotopy]]

#Idea#


+-- {: .standout}
 The following abstract nonsense is a bit tentative.
 See warning below.
=--

+-- {: .query}

[[Urs Schreiber]]: the more coherent picture seems to be that developing at 

* [[homotopy groups in an (∞,1)-topos]] .

I think we should eventually make that the main page on _homotopy_ and merge into it from the material here only what deserves being kept.

=--

 Ordinary _homotopy_ is a way to probe objects in an [[(∞,1)-topos]] $\mathbf{H}$ by mapping [[sphere]]s into them:

the ordinary [[homotopy group]] $\pi_n(X,x)$ of an object $X \in \mathbf{H}$ is the fiber over $x \in X$ of the morphism

$$
  H(S^n, X) \to H({*},X) \simeq \pi_0(X)
$$

induced on $H$, the [[homotopy category of an (infinity,1)-category]] associated to $\mathbf{H}$.

$$
  H(S^n ,X) := \pi_0(\mathbf{H}(S^n,X))_*
  \,.
$$

In this sense _homotopy_ is the notion that is [[Eckmann-Hilton duality|Eckmann-Hilton dual]] to [[cohomology]].

For a detailed discussion see 

* [[homotopy groups in an (∞,1)-topos]]

+-- {: .un_remark}
###### Remark

This duality suggests that more generally we may be entitled to speak for $B$ and $X$ objects in $\mathbf{H}$ of
$$
  H(B,X) := \pi_0 \mathbf{H}(B,X)_*
$$
as the **homotopy of $X$ with co-coefficients in $B$** (or efficients in $B$ if you want to be funny).

Examples of such constructions exist, but are rarely thought of (or even recognized as) generalizations of the notion of homotopy. Rather, by the above duality, the same situation is usually regarded in the context of [[cohomology]], which, still by the above duality, is just as well.
=--

##An experimental attempt to dualize the [[cohomology]] page##

###Examples###

*  classes of special cases of homotopies with their own entries include (create page if you think it might work)
   * [[group homotopy]]
   * [[generalized (Eilenberg-Steenrod) homotopy]]
   * abelian cosheaf homotopy
   * nonabelian homotopy
   * [[?ech homotopy]]
   * differential homotopy
   * twisted homotopy