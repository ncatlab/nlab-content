In a category $C$, for any objects $c\in C$ and $I\in C$, the [[hom-set]]
$$
  Hom_C(I,c)
$$
can be referred to as the set of **generalized elements** of $c$ with domain (or "stage of definition") $I$.

Common choices for $I$ are a [[terminal object]] (in which case generalized elements are called [[global element]]s) or a [[monoidal category|tensor unit]] (in which case the generalized elements are important in [[enriched category|enriched category theory]]).  In a [[concrete category]] represented by $I$, the $I$-elements of an object are the same as the elements of its underlying set.

However, one of the important insights of category theory is that in arbitrary categories, generalized elements of all possible stages of definition must often be used to replace global elements.  For instance, a set is determined by its global elements, while an object of an arbitrary category is determined by all of its generalized elements (this is one way to state the [[Yoneda lemma]]).


#Examples#

* For $C =$ [[Set]] and $I = \{\bullet\}$ the singleton set, the [[global element]]s of a set $C$ are precisely the ordinary elements of $C$.

* For $C = [D^{op}, Set]$  a [[presheaf]] category and for $I = \Delta_{pt} = (d \mapsto \{\bullet\})$ the presheaf constant on the singleton set, the generalized elements of a presheaf $F$ are the _global sections_ of this presheaf, equivalently these are the elements in the [[limit]] set over $F$.

* Again for $C = [D^{op}, Set]$ and $I=D(-,d)$ a [[representable functor|representable]] presheaf, the generalized elements of $F$ at stage $d$ are precisely the elements of the set $F(d)$, by the [[Yoneda lemma]].

* An [[element in an abelian category]] is an equiavalence class of generalised elements.

+-- {: .query}
How do global elements allow to reconstruct the element-wise thinking from set theory?

_Answer_:  In general, by themselves, they don\'t.  In general, you need to use *all* of the generalized elements.  On the other hand, if the [[terminal object]] (or whatever object is used to define the [[global element]]s) is a [[generator]], then global elements are enough.  In particular, this is true in a [[concrete category]].

_Rafael_:  Can you be more specific in the case of a concrete category?
In particular, how can elements of an abstract set be morphisms (with domain the terminal object) in a concrete category?
Compare with the definition of an abstract set from set theory where elements are featureless dots.
=--