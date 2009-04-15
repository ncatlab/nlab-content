#Idea#

The notion of _ind-object_ and _ind-category_ in an [[(infinity,1)-category]] is the straightforward generalization of the notion of [[ind-object]] in an ordinary category. See there for idea and motivation.

#Definition#

The different equivalent defintions of ordinary [[ind-object]]s have their analog for [[(infinity,1)-category|(infinity,1)-categories]].

Let $C$ be a small [[(infinity,1)-category]]. Write for $\kappa$ a [[cardinal number|regular cardinal]] write $ind_\kappa \text{-}C$ for the full sub-[[(infinity,1)-category]] of $[[(infinity,1)-presheaf|(infinity,1)-presheaves]]$ on those $(\infty,1)$-presheaves

$$
  F : C^{op} \to TOp
$$

which classify [[fibrations in simplicial sets|right fibrations]] $\tilde C \to C$ such that $\tilde C$ is $\kappa$-[[filtered (infinity,1)-category|filtered]].

In the case $\kappa = \omega$ write $ind_\kappa\text{-}C = ind\text{-}C$.

Equivalently, an [[(infinity,1)-presheaf]] is in $ind_\kappa\text{-}C$ if there exists a $\kappa$-[[filtered (infinity,1)-category]] $D$ and an $(\infty,1)$-functor $W: D \to C$ such that $F$ is the colimit over $Y \circ W$, where $Y$ is the [[(infinity,1)-Yoneda embedding]].



# References #

Section 5.3 and in particular 5.3.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]