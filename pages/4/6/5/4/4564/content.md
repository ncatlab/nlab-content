
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

+-- {: .un_def}
###### Definition

A [[geometric morphism]] $f\colon E\to F$ between [[toposes]] is called **hyperconnected** if the [[inverse image]] [[functor]] $f^*\colon F\to E$

1. is a [[full and faithful functor]] 

1. its [[image]] is closed under [[subquotients]] in $E$.

=--

This appears ([Johnstone, p. 225](#Johnstone)).

## Examples

* If $g\colon C\to D$ is a [[functor]] between [[small categories]] which is both [[essentially surjective functor|essentially surjective]] and [[full functor|full]], then the induced geometric morphism $Set^C\to Set^D$ is hyperconnected.  In fact, instead of essentially surjective it suffices for $g$ to be [[Cauchy surjective functor|Cauchy surjective]], i.e. $D$ is the closure of $g(C)$ under retracts.

* In particular, the [[global sections]] geometric morphism $Set^C\to Set$ is hyperconnected 
iff $C$ is strongly connected (see Elephant, A4.6.9), i.e., inhabitated and for any two objects $A,B$ there exist morphisms $f:A\to B$ and $g:B\to A$. This includes the case when $C=M$ is a [[monoid]], and the topos of [[simplicial set|simplicial sets]].


## Remarks

* Any hyperconnected geometric morphism is [[connected geometric morphism|connected]], so the name is not unreasonable.

* Hyperconnected geometric morphisms are the left class of a 2-categorical [[orthogonal factorization system]] on the 2-category of topoi; the right class is the class of [[localic geometric morphisms]].  In particular, a geometric morphism can only be both hyperconnected and localic if it is an equivalence.  Therefore, if we view topoi as generalized [[topological spaces]] (or [[locales]]), the world of hyperconnected topoi and geometric morphisms lives entirely in the "generalized" part.

## References

* [[Peter Johnstone]], _Factorization theorems for geometric morphisms_ Cahiers, 22, no1 (1981) ([numdam](http://www.numdam.org/item?id=CTGDC_1981__22_1_3_0))
{#Johnstone}



[[!redirects hyperconnected geometric morphism]]
[[!redirects hyperconnected geometric morphisms]]

[[!redirects hyperconnected topos]]
[[!redirects hyperconnected toposes]]