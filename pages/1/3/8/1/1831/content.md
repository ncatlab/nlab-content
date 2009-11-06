
#Idea#

A _Cartesian fibration_ is a morphism between [[simplicial set]]s that generalizes the notion of [[Grothendieck fibration]] from [[category|categories]] to [[quasi-category|quasi-categories]].

This means that precisely if an [[∞-functor]] $p : C \to D$ if a Cartesian fibration is it possible to interpret its value over any [[morphism]] $f : d_1 \to d_2$ in $D$ as an [[∞-functor]] $p^{-1}(f) : p^{-1}(d_2) \to p^{-1}(d_1)$ between the [[fiber]]s $p^{-1}(d_2)$ and $p^{-1}(d_1)$ over its source and target [[object]]s. 

So a Cartesian fibration $p : C \to D$ determines and is determined by an [[∞-functor]] $S_p : D \to (\infty,1)Cat^{op}$ from $D$ into the [[opposite category]] of the  [[(∞,1)-category of (∞,1)-categories]].

This correspondence is mediated by the [[universal fibration of (∞,1)-categories]] which is a Cartesian fibration $p_{univ}: Z \to (\infty,1)Cat$ such that for every Cartesian fibration $p : C \to D$ there is a functor $S_p : D \to (\infty,1)Cat^{op}$ such that $p$ is the ($(\infty,1)$-categorical) [[pullback]] of $p_{univ}$

$$
  \array{
    C &\to& Z
    \\
    \downarrow^p && \downarrow^{p_{univ}}
    \\
    D &\stackrel{S_p}{\to}& (\infty,1)Cat^{op}
  }
  \,.
$$

As described at [[generalized universal bundle]], this pullback construction is the $(\infty,1)$-categorical analog of the [[Grothendieck construction]] for ordinary categories.

# Definition #

A Cartesian fibration is an [[inner fibration]] of simplicial sets $p : X \to S$ such that for every edge $f : X \to Y$ of $S$ and every lift $\tilde{y}$ of $y$ (that is, $p(\tilde{y})=y$), there is a [[cartesian morphism|Cartesian edge]] $\tilde{f} : \tilde{x} \to \tilde{y}$ in $X$ lifting $f$.

# Properties #


+-- {: .un_prop}
###### Proposition
Basic properties:

* Every [[isomorphism]] of [[simplicial set]]s is a Cartesian fibration.

* Cartesian fibrations are [[pullback stability|stable under base change]] in [[SSet]].

* The composite of two Cartesian fibrations is again a Cartesian fibration.

=--

+-- {: .proof}
###### Proof

This is proposition 2.4.2.3 in [[Higher Topos Theory|HTT]].

=--


# References #

Definition 2.4.2.1 in

* [[Jacob Lurie]], [[Higher Topos Theory]]


[[!redirects cartesian fibration]]
[[!redirects coCartesian fibration]]
[[!redirects co-cartesian fibration]]
[[!redirects cocartesian fibration]]