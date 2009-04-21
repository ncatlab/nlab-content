# Idea #

The concept of [[cartesian product]] makes sense for any family of sets, while the category-theoretic [[product]] makes sense for any family of objects.  In each case, however, the family is indexed by a [[set]]; how can we get a purely category-theoretic product indexed by an object?

First we need to describe a family of objects indexed by an object; it\'s common to interpret this as a [[bundle]], that is an arbitrary morphism $f: A \to I$.  (In [[Set]], $I$ would be the index set of the family, and the [[fiber]] of the bundle over an element $x$ of $I$ would be the set indexed by $x$.  Conversely, given a family of sets, $A$ can be constructed as its [[disjoint union]].)

In these terms, the cartesian product of the family of sets is the set $S$ of [[section]]s of the bundle.  This set satisfies the [[universal property]] that ...

#Definition#

For $C$ a [[category]] with the required [[limit]]s needed below, the **dependent product** of the [[morphism]] $g : B \to A$ indexed by the morphism $f : A \to I$ is the [[object]] $\Pi_f g \in C/I$ in the [[over category]] $C/I$ which is the image under the [[right adjoint]] $\Pi_f : C/A \to C/I$ of the [[base change]] functor $f^* : C/I \to C/A$.

#Examples#

* this plays a role in the definition of [[universe in a topos]].
