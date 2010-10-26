
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
* automatic table of contents goes here
{:toc}

## Definition

By $Ho(Top)$ one denotes the [[category]] which is the [[homotopy category]] of [[Top]] with respect to [[category with weak equivalences|weak equivalences]] given 

* either by [[homotopy equivalence]]s -- $Ho(Top)_{he}$.

* or by [[weak homotopy equivalence]]s -- $Ho(Top)_{whe}$.

Depending on context here [[Top]] contains all topological spaces or is some subcategory of [[nice topological space]]s.

The study of $Ho(Top)$ was the motivating example of [[homotopy theory]]. Often $Ho(Top)$ is called _the_ homotopy category.

## Compactly generated spaces

Let now $Top$ denote concretely the category of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s. And Let $CW$ be the subcategory on [[CW-complex]]es. We have $Ho(CW)_{whe} = Ho(CW)_{he} = Ho(CW)$.

There is a functor

$$
  Top \to Ho(CW)
$$

that sends each topological space to a weakly homotopy equivalent CW-complex.

By the [[homotopy hypothesis]]-theorem $Ho(CW)$ is equivalent for instance to the [[homotopy category]] $Ho(sSet_{Quillen})$ of the standard [[model structure on simplicial sets]]. 

## Shape theory

The category $Ho(Top)_{he}$ of can be studied by testing its objects with objcts from $Ho(CW)$. This is the topic of [[shape theory]].

category: category

[[!redirects HoTop]]
[[!redirects homtopy category of spaces]]
[[!redirects homtopy category of topological spaces]]