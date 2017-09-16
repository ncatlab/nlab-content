#Idea#

To some extent, a group "is" a [[groupoid]] with a single object.

More precisely and more along the lines of [the definition you're used to](http://en.wikipedia.org/wiki/Group_%28mathematics%29#Definition).
a **group** is a [[monoid]] in which every element has an [[inverse]].

But the [[delooping]] of a group $G$ is a [[groupoid]] $\mathbf{B} G$ with 

* $Obj(\mathbf{B}G) = \{\bullet\}$ 

* $Hom_{\mathbf{B}G}(\bullet, \bullet) = G$.

Since for $G, H$ two groups, [[functor]]s $\mathbf{B}G \to \mathbf{B}H$ are canonically in bijection with group homomorphisms $G \to H$, this gives rise to the following statement:

Let [[Grpd]] be the 1-[[category]] whose objects are [[groupoid]]s and whose [[morphism]]s are [[functor]]s (discarding the [[natural transformation]]s). Let [[Grp]] be the category of groups. Then the [[delooping]] functor

$$
  \mathbf{B} : Grp \to Grpd
$$

is a [[full and faithful functor]]. In terms of this functor we may regard groups as the full [[subcategory]] of groupoids on groupoids with a single object.

It is in this sense that a group really is a groupoid with a single object.

But notice that it is unnatural to think of [[Grpd]] as a 1-category. It is really a [[2-category]], namely the sub-2-category of [[Cat]] on groupoids.

And the category of groups is _not_ equivalent to the full sub-2-category of the 2-category of groupoids on one-object groupoids. 

The reason is that two functors:

$$
  \mathbf{B}f_1, \mathbf{B}f_2 : \mathbf{B}G \to \mathbf{B}H
$$ 

coming from two group homomorphisms $f_1, f_2 : G \to H$ are related by a [[natural transformation]] $\eta_h : f_1 \to f_2$ with single component $\eta_h : \bullet \mapsto h \in Mor(\mathbf{B} H)$ for each element $h \in H$ such that the homomorphisms $f_1$ and $f_2$ differ by the inner automorphism $Ad_h : H \to H$

$$
  (\eta_h : \mathbf{B}f_1 \to \mathbf{B}f_2)
  \Leftrightarrow 
  (f_2 = Ad_h \circ f_1)
  \,.
$$


# Internalization #

A **[[group object]]** [[internalization|internal to]] a [[category]] $C$ with finite [[product|products]] is an object $G$ together with maps $mult:G\times G\to G$, $id:1\to G$, and $inv:G\to G$ such that various diagrams expressing associativity, unitality, and inverses commute.

Equivalently, it is a functor $C^{op}\to Grp$ whose underlying functor $C^{op} \to Set$ is [[representable functor|representable]].

For example, a group object in [[Diff]] is a [[Lie group]].  A group object in [[Top]] is a [[topological group]].  And a group object in $CAlg^{op}$, where $CAlg$ is the category of commutative algebras, is a (commutative) [[Hopf algebra]].

A group object in [[Grp]] is the same thing as an abelian group (see [[Eckmann-Hilton argument]]), and a group object in [[Cat]] is the same thing as an [[internal category]] in [[Grp]], both being equivalent to the notion of [[crossed module]]. 
