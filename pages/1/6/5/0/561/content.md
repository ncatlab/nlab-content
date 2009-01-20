It is common in category theory to consider the objects of a [[slice category]] $C/X$ as "objects of $C$ varying over $X$."  For example, an object $A\to X$ of $Set/X$ can be identified with an $X$-indexed family $\{A_x\}_{x\in X}$ of sets, where $A_x$ is the [[fiber]] of $A\to X$ over $x\in X$.  Likewise, if $X$ is a [[topological space]], can regard an object of $Top/X$ as a family of spaces (the fibers) "varying continuously" over $X$.

However, if $X$ has more structure than a set, we may want to require that this structure acts on, or can be lifted to, an object varying over $X$.  For example, if $X$ is a category, an object of $Cat/X$ can be thought of as a "category varying over $X$," but we would quite reasonably like this varying to happen _functorially_, which is not guaranteed for an arbitrary object of $Cat/X$; we would need to be able to "transport" objects in one fiber to objects in another fiber along morphisms in $X$.  Likewise, when $X$ is a space, we may consider it as an $\infty$-groupoid and ask to be able to transport points in one fiber to points in another fiber along paths and homotopies in $X$.

In general, the term **fibration** refers to a map $A\to X$ with such a "transportation" property, which can also be thought of as "lifting" morphisms in the base $X$ to morphisms in $A$.  Particular types of fibration include:

* [[Serre fibration]]s between topological spaces allow lifting of paths, homotopies, and higher homotopies in the base.  [[Hurewicz fibration]]s allow lifting of arbitrary structures.

* [[Kan fibration]]s between simplicial sets allow lifting of $n$-simplices for every $n$.

* [[isofibration]]s between categories allow lifting of isomorphisms in the base.

* [[quasifibration]]s between simplicial sets are a common generalization of Kan fibrations and isofibrations, just as [[quasicategory|quasicategories]] are a common generalization of [[Kan complex]]es and categories.

* [[Grothendieck fibration]]s between categories allow lifting of arbitrary morphisms in the base.  Because functors can be covariant or contravariant, there are two dual types of Grothendieck fibration, and because arrows are not invertible, the liftings must satisfy an extra "universality" condition.

Moreover, in [[homotopy theory]], fibrations are part of the structure commonly imposed on a [[category with weak equivalences]] to make its homotopy theory more tractable.  For example, in many cases the [[pullback]] of a fibration is already a [[homotopy pullback]].  In such cases, usually every object of $C/X$ can be replaced by a weakly equivalent one which is a fibration (and replacing a map by a fibration is one way to compute a homotopy pullback).  Formal structures that include such fibrations include [[category of fibrant objects|categories of fibrant objects]] and [[model category|model categories]].

Serre fibrations, Hurewicz fibrations, Kan fibrations, isofibrations, and quasifibrations are all the fibrations in some approriate model category.  This is not true for Grothendieck fibrations because of the non-homotopical "universality" condition on lifts, but every Grothendieck fibration is in particular an isofibration.


+--{.query}
[[Tim Porter|Tim]]: I do not quite agree with 'transport' as being the main point of fibrations. Rather 'lifting' is the main point, in particular lifting of homotopies, at least in topological situations.   For transport, one needs connections of some sort to get things working well, but in many cases  there is only a very weak notion of action, so perhaps that should be derived as a property rather than taken as a 'defining property' in some sense.

Perhaps a reference to Stasheff and Wirth 
 
James Wirth & Jim Stasheff

_Homotopy Transition Cocycles_

math.AT/0609220.

and the discussion

http://golem.ph.utexas.edu/category/2006/09/wirth_and_stasheff_on_homotopy.html

on the cafe would be a good idea to add.

_[[Urs Schreiber|Urs]]:_ In situations where one wants
to talk of transport, the fibration usually arises as the
pullback of some "universal fibration", a
[[generalized universal bundle]]. For instance 
(split op-)fibrations of categories are precisely the pullbacks of the universal $Cat$-bundle 
$Cat_* \to Cat$ along a functor $F : C \to Cat$.

If one looks at this kind of situation where we do have an established notion of _(parallel) transport_ one sees:

* it is the classifying functor $F : C \to Cat$ which should be addressed as the "(parallel) transport", while the corresponding fibration is its "action object" as in [[action groupoid]], i.e. the thing whose objects are all possible things that the parallel transport can transport and whose morphisms take these things to the image of that transport. So it's a subtle difference, but an important one.

For instance, to make this more concrete, consider the category of [[generalized smooth space|smooth]] [[groupoids]] (which is a [[category of fibrant objects]]), let for any manifold $X$ the groupoid $P_1(X)$ be the groupoid of smooth thin-homotopy classes of paths in $X$, let $G$ be any Lie group, $\mathbf{B} G$ the corresponding one-object Lie groupoid and consider the _universal fibration _ $\mathbf{E} G \to \mathbf{B}G$ -- the groupoid incarnation of the universal $G$-bundle as described at [[generalized universal bundle]]. Then

Theorem: $G$-bundles with connection on $X$ are equivalent to functors $tra : \widehat{P_1(X)} \to \mathbf{B}G$ out of acyclic fibrations $\widehat{P_1(X)} \to P_1(X)$ over $P_1(X)$ (i.e. smooth [[anafunctor]]s $P_1(X) \to \mathbf{B}G$). These functors are literally the corresponding "parallel transport": indeed, evaluated on a path $\gamma$ in $X$ there is locally a 1-form $A \in \Omega^1(X, Lie(G))$ such that the group element $tra(\gamma)$ is the traditional parallel transport of that 1-form, $tra(\gamma) = P exp(\int_\gamma A)$.

Now, we can form the fibration which is associated with this parallel transport, namely the pullback

$$
  \array{
     tra^* \mathbf{E} G &\to& \mathbf{E}G
     \\
     \downarrow && \downarrow
     \\
     \widehat{P_2(X)} &\stackrel{tra}{\to}& \mathbf{B}G
     \\
     \downarrow
     \\
     P_2(X)
  }
  \,.
$$

This fibration $tra^* \mathbf{E}G \to \widehat{P_2(X)}$ is what is properly speaking the [[action groupoid]] of $tra$ acting on the fibers of the principal $G$-bundle. 

=--