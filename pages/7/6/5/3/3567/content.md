
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

The "classical homotopy category" $Ho(Top)$ typically refers to the [[category]] of [[topological spaces]] with morphisms between them the [[homotopy classes]] of [[continuous functions]], or (slightly less classically but more commonly these days) to its [[full subcategory]] on those topological spaces [[homeomorphism|homeomorphic]] to a [[CW-complex]]. The latter is technically the [[homotopy category]] obtained by [[localization|localizing]] the category of topological spaces at those [[continuous functions]] that are  [[weak homotopy equivalences]], hence it is also the [[homotopy category of a model category]] of the [[classical model structure on topological spaces]].


## Definition

By $Ho(Top)$ one denotes the [[category]] which is the [[homotopy category]] of [[Top]] with respect to [[category with weak equivalences|weak equivalences]] given 

* either by [[homotopy equivalence]]s -- $Ho(Top)_{he}$.

* or by [[weak homotopy equivalence]]s -- $Ho(Top)_{whe}$.

Depending on context here [[Top]] contains all topological spaces or is some subcategory of [[nice topological space]]s.

The study of $Ho(Top)$ was the motivating example of [[homotopy theory]]. Often $Ho(Top)$ is called _the_ homotopy category.

The [[simplicial localization]] of [[Top]] at the [[weak homotopy equivalences]] yields the [[(∞,1)-category]] of [[∞-groupoids]]/[[homotopy types]].

## Compactly generated spaces

Let now $Top$ denote concretely the category of [[compactly generated space|compactly generated]] [[weakly Hausdorff space]]s. And Let $CW$ be the subcategory on [[CW-complex]]es. We have $Ho(CW)_{whe} = Ho(CW)_{he} = Ho(CW)$.

There is a functor

$$
  Top \to Ho(CW)
$$

that sends each topological space to a weakly homotopy equivalent CW-complex.

By the [[homotopy hypothesis]]-theorem $Ho(CW)$ is equivalent for instance to the [[homotopy category of a model category]] $Ho(sSet_{Quillen})$ of the [[classical model structure on simplicial sets]] as well as $Ho(Top_{Quillen})$of the [[classical model structure on topological spaces]].

## Shape theory

The category $Ho(Top)_{he}$ can be studied by testing its objects with objects from $Ho(CW)$. This is the topic of [[shape theory]].

## Related concepts
 {#RelatedConcepts}

* [[hypothèse inspiratrice]]

* [[Top]], [[Ho(Top)]]

* [[sSet]], [[Ho(sSet)]]

* [[∞Grpd]], [[Ho(∞Grpd)]]

* [[stable homotopy category]]

## References

> For more see the references at *[[homotopy theory]]*.

On the non-[[concrete category|concreteness]] of the classical homotopy category:

* {#Freyd70} [[Peter Freyd]]: *Homotopy is not concrete*, in: _The Steenrod Algebra and its Applications_, Lecture Notes in Mathematics **168**, Springer (1970) &lbrack;[doi:10.1007/BFb0058516](https://doi.org/10.1007/BFb0058516)&rbrack; 

  reprinted in: Reprints in Theory and Applications of Categories **6** (2004) 1-10 &lbrack;[tac:tr6](http://www.tac.mta.ca/tac/reprints/articles/6/tr6abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/6/tr6.pdf)&rbrack;


On the [[exact completion]] of $Ho(Top)$ being a [[pretopos]]:

* [[Marino Gran]], [[Enrico Vitale]], *On the exact completion of the homotopy category*, Cahiers de Topologie et Géométrie Différentielle Catégoriques **39** 4 (1998)  287-297 &lbrack;[numdam:CTGDC_1998__39_4_287_0](http://www.numdam.org/item/CTGDC_1998__39_4_287_0)&rbrack;

category: category

[[!redirects HoTop]]
[[!redirects homotopy category of spaces]]
[[!redirects homotopy category of topological spaces]]

[[!redirects classical homotopy category]]
[[!redirects classical homotopy categories]]

[[!redirects classical homotopy category of topological spaces]]
[[!redirects classical homotopy categories of topological spaces]]

[[!redirects classical pointed homotopy category]]
[[!redirects classical pointed homotopy categories]]


