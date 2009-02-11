# Definition in ordinary category theory #

A **limit** of some [[diagram]] $F$ is a [[universal construction|universal]] [[cone]] to $F$. In more detail, it is a cone $\theta$ from an object denoted $lim F$ to $F$, such that given any cone $\gamma: \Delta c \to F$, there exists a unique morphism $f: c \to lim F$ such that 
$$\gamma = (\Delta c \stackrel{\Delta f}{\to} \Delta lim F \stackrel{\theta}{\to} F$$ 
(Given $f: c \to d$, $\Delta f: \Delta c \to \Delta d$ is the evident natural transformation whose component at each object $j$ of $J$ is $f: c \to d$.) 

[To be continued...]

Here are some important examples of limits, classified by the shape of the diagram:

* A limit of the [[empty set|empty diagram]] is a [[terminal object]].
* A limit of a diagram consisting of two (or more) objects is their [[product]].
* A limit of a [[cospan]] is a [[pullback]].
* A limit of a pair (or more) of [[parallel morphisms]] is an [[equalizer]].

#Relation to adjoints of the constant diagram functor#

For $D$ a [[small category]] and $C$ a category the [[functor category]] $[D,C]$ is the category of $D$-[[diagram]]s in $C$.  Pullback along the functor $D \to pt$ to the [[terminal object|terminal]] category $pt = \{\bullet\}$ induces a functor
$$
  const :  C \to [D,C]
$$
which sends every object of $C$ to the diagram functor constant on this object.

The [[left adjoint]]
$$
  colim_D : [D,C] \to C
$$
of this functor is, if it exists, the functor
which sends every diagram to its [[colimit]] and the [[right adjoint]] is, if it exists, the functor
$$
  lim_D : [D,C] \to C
$$
which sends every diagram to its [[limit]]. The Hom-isomorphisms of these [[adjunction]]s state precisely the universal property of [[limit]] and [[colimit]] given above.



#Remarks#

* The meaning of the notion of limit is possibly best appreciated by regarding them in the context of [[representable functor]]s (as explained there).