In a category $C$, for any objects $c\in C$ and $I\in C$, the [[hom-set]]
$$
  Hom_C(I,c)
$$
can be referred to as the set of **generalized elements** of $c$ with domain (or "stage of definition") $I$.

# Motivation #

The primordial example is when $C$ is the category [[Set]] of sets and $I$ is a [[terminal object]] in $Set$ --- that is, a set with one element.  Then elements of any set $c$ are in one-to-one correspondence with functions $f: I \to c$.  This correspondence works as follows: given any element of $c$ there is a unique function $f: I \to c$ with this element in its image, and conversely each function $f: I \to c$ has a unique element of $c$ in its image. 

In the same way, in a [[concrete category]] represented by $I$, the $I$-elements of an object are the same as the elements of its underlying set.  (The category of sets is actually a special case of this, since it is concrete and represented by a terminal object.)

Generalizing from $Set$ in another way, in any category with a terminal object $I$, we call a morphism $f : I \to c$ a [[global element]] of the object $c$.  Generalizing further, it is common to take $I$ to be the unit object whenever $C$ is a [[monoidal category]]; in this case the generalized elements are important in [[enriched category|enriched category theory]]).  Note that any [[closed monoidal category]] is again a concrete category represented by this $I$.

The most general case where a single object $I$ may be used to define global elements is where $I$ is a [[generator]] of the category.  However, not every category has a single object as a generator!  Instead, in arbitrary categories, generalized elements of *all* possible stages of definition must often be used to replace global elements.  Thus while a set is determined by its global elements, an object of an arbitrary category is determined by all of its generalized elements (this is one way to state the [[Yoneda lemma]]).

# Examples #

* For $C =$ [[Set]] and $I = \{\bullet\}$ the singleton set, the [[global elements]] of a set $C$ are precisely the ordinary elements of $C$.

* For $C = [D^{op}, Set]$  a [[presheaf]] category and for $I = \Delta_{pt} = (d \mapsto \{\bullet\})$ the presheaf constant on the singleton set, the generalized elements of a presheaf $F$ are the _global sections_ of this presheaf, equivalently these are the elements in the [[limit]] set over $F$.

* Again for $C = [D^{op}, Set]$ and $I=D(-,d)$ a [[representable functor|representable]] presheaf, the generalized elements of $F$ at stage $d$ are precisely the elements of the set $F(d)$, by the [[Yoneda lemma]].

* An [[element in an abelian category]] is an equivalence class of generalised elements.

[[!redirects generalised element]]
[[!redirects generalised elements]]
[[!redirects generalized elements]]
