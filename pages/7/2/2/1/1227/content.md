
#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of _ind-object_ and _ind-category_ in an [[(∞,1)-category]] is the straightforward generalization of the notion of [[ind-object]] in an ordinary category. See there for idea and motivation.


## Definition

The different equivalent definitions of ordinary [[ind-object]]s have their analog for [[(∞,1)-categories]].

Let in the following $C$ be a small [[(∞,1)-category]]. 

### In terms of formal colimits 

The definition in terms of formal colimits is precisely analogous to the one for ordinary [[ind-object]]s, with colimits and limits replaced by the corresponding $\infty$-notion (compare [[homotopy limit]] and [[limit in quasi-categories]])

So the objects of $Ind C$ are small filtered diagrams $X : D_X \to C$ in $C$, and the morphisms are given by

$$
  Hom_{Ind C}(X,Y) := lim_{d\in D_X} colim_{d' \in D_Y} Hom_C(X(d), Y(d'))
  \,.
$$

(... should be made more precise...)

### In terms of filtered fibrations 

Write $\kappa$ for a [[cardinal number|regular cardinal]] and write $ind_\kappa \text{-}C$ for the full sub-[[(∞,1)-category of (∞,1)-presheaves]] on those $(\infty,1)$-presheaves

$$
  F : C^{op} \to Top
$$

which classify [[right fibration]]s $\tilde C \to C$ such that $\tilde C$ is $\kappa$-[[filtered (infinity,1)-category|filtered]].

In the case $\kappa = \omega$ write $ind_\kappa\text{-}C = ind\text{-}C$.

### In terms of filtered colimits 

Equivalently, an [[(∞,1)-presheaf]] is in $ind_\kappa\text{-}C$ if there exists a $\kappa$-[[filtered (∞,1)-category]] $D$ and an $(\infty,1)$-functor $W: D \to C$ such that $F$ is the colimit over $Y \circ W$, where $Y$ is the [[(∞,1)-Yoneda embedding]].



## References 

Section 5.3 and in particular 5.3.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects ind-object (infinity,1)-category]]
[[!redirects ind-object (infinity,1)-categories]]
[[!redirects ind-object (∞,1)-category]]
[[!redirects ind-object (∞,1)-categories]]
[[!redirects ind-object in an (∞,1)-category]]