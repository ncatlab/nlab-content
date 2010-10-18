
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea ##

The condition that a [[presheaf]] be a [[sheaf]] may be seen as a condition of unique existence.  A presheaf is separated if it satisfies the uniqueness part.

## Definition ##

A [[presheaf]] $A \in PSh(S)$ with respect to some [[site]] $S$ is **separated** (or a **monopresheaf**) if for all [[local isomorphism]]s $Y \to X$ the induced morphism $Hom(X,A) \to Hom(Y,A)$ is a [[monomorphism]].

This definition generalizes to any system of [[local isomorphisms]] on any topos, such as that obtained from any [[Lawvere-Tierney topology]], or equivalently any [[subtopos]].

More generally, for a class $V$ of arrows in a category $C$, an object $A\in C$ is $V$-**separated** if for all morphisms $Y\to X$ in $V$, the induced morphism $Hom(X,A)\to Hom(Y,A)$ is a monomorphism.

## Basic results ## 

* The full subcategory of separated presheaves in a presheaf category is a [[quasitopos]]. 

* There are [[adjoint functor|left adjoints]] to the forgetful functors from sheaves of sets to separated presheaves of sets (called **sheafification**) and from separated presheaves of sets to presheaves of sets (called **monosheafification**); both of these can be described by the same operation on presheaves of sets: the Grothendieck [[plus construction]].  Thus, [[sheafification]] in the usual sense (the left adjoint to the forgetful functor from sheaves of sets all the way down to presheaves of sets) may be obtained by applying the plus construction twice.  This is all for presheaves of sets; some generalizations to other categories exist.

Both of these generalize to systems of local isomorphisms on any topos.

## Remarks ##

Recall that a [[sheaf]] on $S$ is a presheaf $A$ such that for all local isomorphisms $Y \to X$ the induced morphism is an *[[isomorphism]]*.  (For an arbitrary class of morphisms $V$, the corresponding condition is called being a [[local object]].)  So a separated presheaf is close to being a sheaf, but not necessarily quite there.

As with sheaves, it is sufficient to check only the [[dense monomorphism]]s instead of all local isomorphisms.  This is equivalent to checking [[cover]]ing [[sieve]]s.

[[!redirects monopresheaf]]
[[!redirects separated presheaves]]
[[!redirects separated object]]
[[!redirects separated objects]]
