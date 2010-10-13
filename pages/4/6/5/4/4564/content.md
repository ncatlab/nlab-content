
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Hyperconnected geometric morphisms
* table of contents
{: toc}

## Definition

A [[geometric morphism]] $f\colon E\to F$ between [[topoi]] is called **hyperconnected** if the image of $f^*\colon F\to E$ is closed under [[subquotients]] in $E$.

+--{: .query}
I think I must have forgotten a clause in this definition, since the geometric morphism $* = Sh(\emptyset) \to Set = Sh(*)$ satisfies it and is also [[localic geometric morphism|localic]], but is not an equivalence.
=--


## Examples

* If $g\colon C\to D$ is a [[functor]] between [[small categories]] which is both [[essentially surjective functor|essentially surjective]] and [[full functor|full]], then the induced geometric morphism $Set^C\to Set^D$ is hyperconnected.  In fact, instead of essentially surjective it suffices for $g$ to be [[Cauchy surjective functor|Cauchy surjective]], i.e. $D$ is the closure of $g(C)$ under retracts.

* In particular, the [[global sections]] geometric morphism $Set^C\to Set$ is hyperconnected for any [[inhabited set|inhabited]] small category $C$.  This includes the case when $C=G$ is a [[group]] and $Set^C$ is the topos of [[group action|G-sets]].


## Remarks

* Any hyperconnected geometric morphism is [[connected geometric morphism|connected]], so the name is not unreasonable.

* Hyperconnected geometric morphisms are the left class of a 2-categorical [[orthogonal factorization system]] on the 2-category of topoi; the right class is the class of [[localic geometric morphisms]].  In particular, a geometric morphism can only be both hyperconnected and localic if it is an equivalence.  Therefore, if we view topoi as generalized [[topological spaces]] (or [[locales]]), the world of hyperconnected topoi and geometric morphisms lives entirely in the "generalized" part.


[[!redirects hyperconnected geometric morphism]]
[[!redirects hyperconnected geometric morphisms]]
