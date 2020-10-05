

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

A _simplicial homotopy equivalence_ is a [[homotopy equivalence]] between [[simplicial sets]].

## Definition

A [[morphism]] $f\colon A\to B$ of [[simplicial sets]]
is a __simplicial homotopy equivalence__ if there is a morphism $g\colon B\to A$ and [[homotopies]] $p\colon \Delta^1\times A\to A$ from $id_A$ to $g \circ f$ and $q\colon \Delta^1\times B\to B$ from $f \circ g$ to $id_B$ (where $id_X$ denotes the [[identity morphism]] on the simllicial set $X$).

## Properties

* If $A$ and $B$ are [[Kan complexes]],
then $f$ is a simplicial homotopy equivalence
if and only if $f$ has the [[right homotopy lifting property]] with respect to the [[boundary]] inclusion $\partial\Delta^n\to\Delta^n$ of [[simplices]].

* All simplicial homotopy equivalences are [[simplicial weak equivalences]]. The converse is true if $A$ and $B$ are [[Kan complexes]].


## Related notions

* [[simplicial weak equivalence]]

* [[simplicial Whitehead theorem]]

* [[classical model structure on simplicial sets]]

