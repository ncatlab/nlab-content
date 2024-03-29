## Idea

Given an [[abelian category]], the _filtered derived category_ is the category of [[chain complexes]] of [[filtered objects]] up to [[quasi-isomorphism]].

## Definition

Given an [[abelian category]] $A$, one may consider the [[additive category]] $Fil(A)$ of [[filtered objects]] in $A$, whose objects are pairs $(a, F^*)$ with $a$ an object of $A$ and $F^*$ a [[filtration]] on $a$.
Let $Comp(Fil(A))$ denote the category of [[chain complexes]] in $Fil(A)$.
One defines a morphism in $Comp(Fil(A))$ to be a **quasi-isomorphism** if it induces [[quasi-isomorphisms]] on each degree of the [[associated graded objects]].
The **filtered derived category** of $A$,
  $$ D_{fil}(A) = Comp(Fil(A))[qis^{-1}] $$
is the [[localization]] of $Comp(Fil(A))$ at the class of [[quasi-isomorphisms]].

## See also

* [[derived category]]
* [[filtered chain complex]]

## References

* [[Stacks Project]], [Tag 03T9](http://stacks.math.columbia.edu/tag/03T9).

[[!redirects filtered derived categories]]
[[!redirects filtered quasi-isomorphism]]
[[!redirects filtered quasi-isomorphisms]]