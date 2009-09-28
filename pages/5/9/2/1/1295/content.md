# Idea #

The concept of [[cartesian product]] makes sense for any family of sets, while the category-theoretic [[product]] makes sense for any family of objects.  In each case, however, the family is indexed by a [[set]]; how can we get a purely category-theoretic product indexed by an object?

First we need to describe a family of objects indexed by an object; it\'s common to interpret this as a [[bundle]], that is an arbitrary morphism $g: B \to A$.  (In [[Set]], $A$ would be the index set of the family, and the [[fiber]] of the bundle over an element $x$ of $A$ would be the set indexed by $x$.  Conversely, given a family of sets, $B$ can be constructed as its [[disjoint union]].)

In these terms, the cartesian product of the family of sets is the set $S$ of (global) [[section]]s of the bundle.  This set comes equipped with an evaluation map $ev: S \times A \to B$ such that
$$ S \times A \stackrel{ev}\to B \stackrel{g}\to A $$
equals the usual product projection; in other words, $ev$ is a morphism in the [[over category]] $Set/A$.  The [[universal property]] of $S$ is that, given any set $T$ and morphism $T \times A \to B$ in $Set/A$, there\'s a unique map $T \to S$ that makes everything commute.

In other words, $S$ and $ev$ define an [[adjoint functor|adjunction]] from $Set$ to $Set/A$ in which taking the product with $A$ is the left adjoint and applying this universal property is the right adjoint.  This is the basis for the definition below, but we add one further level of generality: we move everything from $Set$ to an arbitrary over category $Set/I$.

#Definition#

For $C$ a [[category]], the **dependent product** of the morphism $g: B \to A$ indexed by the morphism $f: A \to I$ is an object $\prod_f g$ in the [[over category]] $C/I$, where the operation $\prod_f: C/A \to C/I$ is [[generalized the|the]] [[adjoint functor|right adjoint]] to the [[base change]] functor $f^*: C/I \to C/A$.

For this to make sense, $f^*$ must exist; that is, all [[pullback]]s along $f$ must exist.  So a category with all dependent products is necessarily a category with all [[pullback]]s.

#Remarks#

Note that the *left* adjoint to the base-change functor, the _dependent coproduct_ or _dependent sum_ $\sum_f: C/A \to C/I$, is much simpler.  It is simply given by [[composition]] with $f$, so it always exists when it makes sense (that is when $f$ has all pullbacks).

+-- {: .un_prop }
###### Proposition

For $C$ a [[topos]] and $f : A \to I$ any morphism in $C$, both the left adjoint $\sum_f : C/A \to C/I$ as well as the right adjoint $\prod_f: C/A \to C/I$ to $f^*: C/I \to C/A$ exist. 

Moreover, $f^*$ preserves the  [[subobject classifier]] and [[internal hom]]s.

=--

This is theorem 2 in section IV, 7 of

* MacLane, Moerdijk, [[Sheaves in Geometry and Logic]]

#Examples#

* the dependent product plays a role in the definition of [[universe in a topos]].

[[!redirects dependent products]]
