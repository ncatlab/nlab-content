

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

Handling higher structures such as [[higher category theory|higher categories]] usually involves conceiving them as  conglomerates of _cells_ of certain _shape_.

Examples for possible shapes used to model higher categories are

* [[globe|globes]];

* [[simplex|simplices]];

* [[cube|cubes]]. 

* [[trees]].

* [[opetopes]], aka [[multitopes]].

There are corresponding categories whose 

* objects are the "standard cellular shapes" of the given sort: [[globe|globes]], [[simplex|simplices]], [[cube|cubes]], respectively.  For globes, simplices, and cubes, there is one object for each natural number $n \in \mathbb{N}$, so they are usually denoted $[n]$.  For other sorts of shapes, there can be multiple shapes of each dimension.

* morphisms are generated from (some of) the ways of mapping these standard cellular shapes to each other such that their cellular structure is preserved;

* and composition of such morphisms is subject to the relations which are inherited from the geometric meaning of these maps, which says for instance that the left boundary of the top boundary of a [[cube]] is the same as the top boundary of its left boundary -- these are the  _globular identities_, the _simplicial identities_ and the _cubical identities_, respectively.

The resulting categories of basic cellular shapes are

* the _[[globe category]]_ $\mathbb{G}$

* the _[[simplex category]]_ $\Delta$

* the _[[cube category]]_ $\square$

* the _[[tree category]]_ $\Omega$

* the _[[opetope category]]_ $\mathbb{O}$

In general, there are two types of morphism in such categories, called *face inclusions* (or *cofaces*) and *degeneracies*.  Face inclusions exhibit a lower-dimensional cell as a "face" of a higher-dimensional one, while degeneracies collapse a higher-dimensional cell down to a lower-dimensional one.  All such categories have face inclusions (these are the really basic "structural" maps that determine the shapes of the cells), but some (such as $\Delta$, $\square$, and $\Omega$) include degeneracies while some (such as $\mathbb{G}$ and $\mathbb{O}$) do not usually.

A general notion which includes all of these categories is that of a [[generalized Reedy category]].  If degeneracies are excluded, then we obtain the simpler notion of a (generalized) [[direct category]].

A higher structure based on these geometric sheapes is a [[presheaf]] on one of these categories. These are called

* [[globular sets]]

* [[simplicial sets]]

* [[cubical sets]]

* [[dendroidal sets]]

* [[opetopic sets]]

respectively. 

There are also other notions of geometric shape which have been found useful in higher category theory, such as the shapes encapsulated in Joyal's [[disk category]] $\Theta$ (which include both globes and simplices as special cases). 

Many definitions of [[higher category theory|higher categories]] are given by one of these presheaves

* either equipped with _extra properties_, in the [[geometric definition of higher category|geometric definition of higher categories]];

* or equipped with _extra structure_, in the [[algebraic definition of higher category|algebraic definition of higher categories]]. 

For instance, the usual definition of [[strict omega-category|strict ∞-categories]] is based on giving [[globular sets]] extra structure, as is the weak version of [[Batanin ∞-category]].  Similarly, [[n-fold category|n-fold categories]] give extra structure to [[cubical sets]].  On the other hand, the notion of [[quasi-category|quasi-categories]] is based on [[simplicial sets]], while other more "homotopical" notions of higher category are based on cubical or multisimplicial techniques.  In general, the "geometric" definitions can usually be thought of as a [[nerve]] of the "algebraic" ones.

Sometimes, two definitions that use different kinds of shapes nevertheless capture equivalent notions.  This is hoped to be true for all proposed definitions of [[n-category]], although they use many different kinds of shapes.  On the other hand, sometimes the use of different shapes indicates a fundamentally different structure being considered.  For instance, edge-symmetric $n$-fold categories with connections give the same notion as globular $n$-categories, while arbitrary $n$-fold categories are something quite different.  Moreover, even in the case where different kinds of shapes produce "equivalent" notions, it can sometimes be markedly easier to work with one kind of shape than another for some particular application.

## References ##

* [This Week's Finds in Mathematical Physics (Week 242)](http://golem.ph.utexas.edu/category/2006/12/this_weeks_finds_in_mathematic_4.html#c006655) (Discussion at the n-Cafe)


[[!redirects geometric shape for higher categories]]
[[!redirects geometric shapes for higher categories]]
[[!redirects geometric shape for higher structures]]
[[!redirects geometric shapes for higher structures]]
