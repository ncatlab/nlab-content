# Definition

A **(finitely) filtered category** (sometimes called a **filtrant category**, as for instance in Kashiwara--Schapira\'s book [[Categories and Sheaves]]) is a [[category]] $C$ in which any finite diagram has a [[cocone]].  That is, for any finite category $D$ and any functor $F:D\to C$, there exists an object $c\in C$ and a natural transformation $F\to \Delta c$ where $\Delta c:D\to C$ is the constant diagram at $c$.

This can be rephrased in more elementary terms by saying that:

* There exists an object of $C$  (the case when $D=\emptyset$)
* For any two objects $c_1,c_2\in C$, there exists an object $c_3\in C$ and morphisms $c_1\to c_3$ and $c_2\to c_3$.
* For any two [[parallel morphisms]] $f,g:c_1\to c_2$ in $C$, there exists a morphism $h:c_2\to c_3$ such that $h f = h g$.

Just as all finite [[colimit|colimits]] can be constructed from initial objects, binary coproducts, and coequalizers, so a cocone on any finite diagram can be constructed from these three.

More generally, if $\kappa$ is a [[cardinal number]], then a **$\kappa$-filtered category** is one such that any diagram $D\to C$ has a cocone where $D$ has fewer than $\kappa$ arrows.  Note that a [[preorder]] is $\kappa$-filtered as a category just when it is $\kappa$-[[direction|directed]] as a preorder.


# Examples

* A filtered [[preorder]] is the same as a [[direction|directed]] one.

* Every category with a [[terminal object]] is filtered.

* Every category which has finite [[colimit]]s is filtered.

* A [[product]] of filtered categories is filtered.


# Filtered colimits

A colimit of a functor $F:D\to C$ where $D$ is a filtered category is called a **filtered colimit**.  A category whose opposite is filtered is called **cofiltered**, and a limit over a cofiltered category is called a **cofiltered limit** or a **filtered inverse limit**.

One of the reasons filtered colimits are important is that in [[Set]], filtered colimits commute with finite limits (and in fact, filtered colimits can be characterized as precisely those colimits that commute with all finite limits in $Set$).  Filtered colimits are also important in the theory of [[locally presentable category|locally presentable]] and [[accessible category|accessible]] categories.  See also [[pro-object]] and [[ind-object]].


[[!redirects filtrant category]]