

## Idea ##

A _cellular model category_ is a particularly convenient form of a [[model category]].

It is similar to a [[cofibrantly generated model category]].

> (How exactly?)

## Definition ##

A **cellular model category** is a [[cofibrantly generated model category]] such that there is a [[set]] of generating cofibrations $I$ and a set of generating acyclic cofibrations $J$, such that

* all domain and codomain objects of elements of $I$ are [[compact object]]s;

* the domain objects of the elements of $J$ are [[small object]]s relative to $I$;

* the cofibrations are [[effective monomorphism]]s.


## Examples ##

* [[Top]] with the standard [[model structure on topological spaces]] (same for pointed topological spaces)

* [[SSet]] with the standard [[model structure on simplicial sets]] (same for pointed simplicial sets).

For $C$ a cellular model category we have that

* the [[functor category]] $[D,C]$ for any [[small category]] $C$ with its projective [[global model structure on functors]] is again a cellular model category;

* for $c \in C$ any object, the [[over category]] $C/c$ is again a cellular model category.


## Applications ##

For cellular model categories $C$ that are [[proper model category|left proper model categories]] all left [[Bousfield localization]]s $L_S C$ at any set $S$ of morphisms are guaranteed to exist.




## References ##

Section 12 of

* Hirschhorn, _Model categories and their localizations_