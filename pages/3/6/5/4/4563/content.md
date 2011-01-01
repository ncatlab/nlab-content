
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Localic geometric morphisms
* table of contents
{: toc}

## Definition

A [[geometric morphism]] $f\colon E\to F$ between [[topoi]] is **localic** if every [[object]] of $E$ is a [[subquotient]] of an object in the [[inverse image]] of $f$: of the form $f^*(x)$.


## Examples

* Any geometric morphism between [[localic topoi]] is localic.

* Any [[geometric embedding]] is localic.

* If $g:C\to D$ is a [[faithful functor]] between [[small categories]], then the induced geometric morphism $Set^C \to Set^D$ is localic.


## Remarks

* A [[Grothendieck topos]] is a [[localic topos]] if and only if its unique [[global section]] geometric morphism to [[Set]] is a localic geometric morphism.  Thus, in general we regard a localic geometric morphism $E\to S$ as exhibiting $E$ as a "localic $S$-topos".

* This is supported by the fact that for any base $S$, the [[2-category]] of localic $S$-toposes (i.e. the full sub-2-category 

  $$
    (Topos/S)_{loc} \subset Topos/S
  $$

  of the [[over-category]] [[Topos]] over $S$ spanned by the localic morphisms into $S$) is equivalent to the 2-category of [[internalization|internal]] [[locales]] in $S$

  $$
    Loc(S) \simeq (Topos/S)_{loc}
  $$


* Localic geometric morphisms are the right class of a 2-categorical [[orthogonal factorization system]] on the 2-category of topoi. The corresponding left class is the class of [[hyperconnected geometric morphism]]s.


[[!redirects localic geometric morphism]]
[[!redirects localic geometric morphisms]]
