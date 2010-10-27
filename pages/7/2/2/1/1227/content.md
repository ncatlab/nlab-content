
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of _ind-object_ and _ind-category_ in an [[(∞,1)-category]] is the straightforward generalization of the notion of [[ind-object]] in an ordinary category. See there for idea and motivation.

We describe $\kappa$-ind-objects for $\kappa$ a [[regular cardinal]]. 

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

Write $\kappa$ for a [[regular cardinal]] and write $ind_\kappa \text{-}C$ for the full sub-[[(∞,1)-category of (∞,1)-presheaves]] on those $(\infty,1)$-presheaves

$$
  F : C^{op} \to Top
$$

which classify [[right fibration]]s $\tilde C \to C$ such that $\tilde C$ is $\kappa$-[[filtered (infinity,1)-category|filtered]].

In the case $\kappa = \omega$ write $ind_\kappa\text{-}C = ind\text{-}C$.

### In terms of filtered colimits 

Equivalently, an [[(∞,1)-presheaf]] is in $ind_\kappa\text{-}C$ if there exists a $\kappa$-[[filtered (∞,1)-category]] $D$ and an $(\infty,1)$-functor $W: D \to C$ such that $F$ is the colimit over $Y \circ W$, where $Y$ is the [[(∞,1)-Yoneda embedding]].


## Properties

Let $C$ a small $(\infty,1)$-category and $\kappa$ a [[regular cardinal]].

+-- {: .un_prop}
###### Proposition

$Ind_\kappa(C)$ is closed in $PSh(C)$ under $\kappa$-filtered [[(∞,1)-colimits]].

=--

This is [[Higher Topos Theory|HTT, prop. 5.3.5.3]].

+-- {: .un_prop}
###### Proposition

For any $F \in PSh(C)$ the following are equivalent:

1. $F$ is a $\kappa$-filtered colimit in $PSh(C)$ of a diagram in $C$;

1. $F$ belongs to $Ind_\kappa(C)$;

1. $F : C^{op} \to \infty Grpd$ preserves $\kappa$-small limits.

=--

This is [[Higher Topos Theory|HTT, corollary 5.3.5.4]].

+-- {: .un_prop}
###### Proposition

Every object of $C$ is a $\kappa$-[[compact object]] of $Ind_\kappa(C)$.

=--

This is [[Higher Topos Theory|HTT, prop. 5.3.5.5]].

## Related concepts

* [[ind-object]] / **ind-object in an $(\infty,1)$-category**

* [[pro-object]] / [[pro-object in an (∞,1)-category]]

## References 

Section 5.3 and in particular 5.3.3 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_


[[!redirects ind-object (infinity,1)-category]]
[[!redirects ind-object (infinity,1)-categories]]
[[!redirects ind-object (∞,1)-category]]
[[!redirects ind-object (∞,1)-categories]]
[[!redirects ind-object in an (∞,1)-category]]