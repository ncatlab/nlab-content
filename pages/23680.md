[[!redirects tabular dagger 2-posets]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

## Contents ##
* table of contents
{:toc}

## Idea ## 

A dagger 2-poset with tabulations, such as a [[tabular allegory]]. 

## Definition ##

A **tabular dagger 2-poset** is a [[dagger 2-poset]] $C$ such that for every object $A:Ob(C)$ and $B:Ob(C)$ and morphism $R:Hom(A,B)$, there is an object $\vert R \vert:Ob(C)$ and [[map in a dagger 2-poset|maps]] $f:Hom(\vert R \vert, A)$, $g:Hom(\vert R \vert, B)$, such that $R = f^\dagger \circ g$ and for every object $E:Ob(C)$ and maps $h:Hom(E,\vert R \vert)$ and $k:Hom(E,\vert R \vert)$, $f \circ h = f \circ k$ and $g \circ h = g \circ k$ imply $h = k$. 

## Properties ##

The [[category of maps]] of a tabular dagger 2-poset has all [[pullbacks]]. 

## Examples ##

The dagger 2-poset [[Rel]] of [[sets]] and [[relations]] is a tabular dagger 2-poset. 

## See also ##

* [[dagger 2-poset]]