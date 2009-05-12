#Idea#

The notion of _ind-object_ and _ind-category_ in an [[(infinity,1)-category]] is the straightforward generalization of the notion of [[ind-object]] in an ordinary category. See there for idea and motivation.

#Definition#

The different equivalent definitions of ordinary [[ind-object]]s have their analog for [[(infinity,1)-category|(infinity,1)-categories]].

Let in the following $C$ be a small [[(infinity,1)-category]]. 

## in terms of formal colimits ##

the definition in terms of formal colimits is precisely analogous to the one for ordinary [[ind-object]]s, with colimits and limits replaced by the corresponding $\infty$-notion (compare [[homotopy limit]] and [[limit in quasi-categories]])

So the objects of $Ind C$ are small filtered diagrams $X : D_X \to C$ in $C$, and the morphisms are given by

$$
  Hom_{Ind C}(X,Y) := lim_{d\in D_X} colim_{d' \in D_Y} Hom_C(X(d), Y(d'))
  \,.
$$

(... should be made more precise...)

## in terms of filtered fibrations ##

Write $\kappa$ for a [[cardinal number|regular cardinal]] and write $ind_\kappa \text{-}C$ for the full sub-[[(infinity,1)-category]] of [[(infinity,1)-presheaf|(infinity,1)-presheaves]] on those $(\infty,1)$-presheaves

$$
  F : C^{op} \to Top
$$

which classify [[fibration in simplicial sets|right fibrations]] $\tilde C \to C$ such that $\tilde C$ is $\kappa$-[[filtered (infinity,1)-category|filtered]].

In the case $\kappa = \omega$ write $ind_\kappa\text{-}C = ind\text{-}C$.

## in terms of filtered colimits ##

Equivalently, an [[(infinity,1)-presheaf]] is in $ind_\kappa\text{-}C$ if there exists a $\kappa$-[[filtered (infinity,1)-category]] $D$ and an $(\infty,1)$-functor $W: D \to C$ such that $F$ is the colimit over $Y \circ W$, where $Y$ is the [[Yoneda (infinity,1)-embedding]].



# References #

Section 5.3 and in particular 5.3.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]