# Idea #

A _proper class_ is a [[set]] that is too big to be a set.  Exactly what this means depends on the [[foundations]] of mathematics, but something must be said about it to study [[large category|large categories]].

# Definitions #

There are several ways to deal with this and define a proper class.

A __proper class__ is a [[large category|large]] [[discrete category]].  But since a large category is usually defined as having a proper class of objects, this just moves the bubble under the wallpaper to 'large category' and something must be applied there.

A __proper class__ is a class that is not a [[set]].  But now we have to define 'class'.

A __class__ is a collection of [[set]]s.  Here the bubble is moved to 'collection', but we will be able to pop that bubble below.  Also we might want to allow the members of a proper class to be other than sets; certainly it is true, however, that a __pure class__ is a collection of [[pure set]]s.

A __class__ is a formula in the language of [[set theory]] for a [[truth value]], equipped with a specified free variable for a set.  This is a formalisation of the previous definition, but it must be interpreted metamathematically (since after all, there are only countably many such formulas): a formula in the language of set theory for a class is defined to be a formula for a truth value with one more free variable for a set.

A __class__ may even be an undefined concept; the real definition is to define a __[[set]]__ as a class that is itself a member of some class.  With appropriate axioms, this is equivalent to the previous definition (and conservative over set theory without classes), but it\'s also possible to apply stronger axioms here; this is the difference between $\mathbf{BNG}$ and $\mathbf{MK}$ as extensions of <b>[[ZFC]]</b>.

A __class__ is a [[subset]] of a [[Grothendieck universe]] $U$, while a ([[small category|small]]) set is merely an element of $U$.  This gives a relative notion, depending on $U$.  As such, we get a concept of class like that of the strong theory $\mathbf{MK}$; to be more like $\mathbf{BNG}$ (and therefore conservative over set theory without an axiom of universes) we should define a __class__ to be a definable subset of $U$.

# Usage

A __[[large category]]__ is a [[category]] whose class of [[morphism]]s is a proper class.  It is sufficient that the class of [[object]]s be a proper class, which is also necessary if the category is [[locally small category|locally small]].

Category theorists care about proper classes because many examples of categories in practice (such as [[Set]], to begin with!) are large.