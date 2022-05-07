
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Relevance monoidal categories

* table of contents
{:toc}

## Idea

A *relevance monoidal category* is a [[symmetric monoidal category]] which has [[monoidal category with diagonals|diagonal maps]] $A\to A\otimes A$, but not projection maps $A \to I$.  (If it had both, it would be a [[cartesian monoidal category]]; while if it had projection maps but not diagonals it would be a [[semicartesian monoidal category]].)  The name comes from the connection with [[relevance logic]], and seems to have been introduced in ([Petrić 2002](#Petric02)).

## Definition

Given a [[symmetric monoidal category]] $C$, let $CCSG(C)$ denote the category of commutative co-[[semigroups]] [[internalization|in]] $C$, i.e. objects $A$ equipped with a "comultiplication" $A\to A\otimes A$ that is coassociative and cocommutative.  There is an obvious forgetful functor $CCSG(C) \to C$.  Moreover, $CCSG(C)$ has a symmetric monoidal structure making the forgetful functor strict symmetric monoidal: if $A$ and $B$ are cosemigroups then $A\otimes B \to (A\otimes A)\otimes (B\otimes B) \cong (A\otimes B) \otimes (A\otimes B)$ makes $A\otimes B$ into a commutative cosemigroup as well, and the unit is the unit object $I$ of $C$ with its a canonical commutative cosemigroup structure given by the coherence isomorphism $I\cong I\otimes I$. 

We say that $C$ is a **relevance monoidal category** if this functor $CCSG(C) \to C$ is equipped with a strict section that is also a strict symmetric monoidal functor.  That is, we have a functor assigning to every object of $C$ a commutative cosemigroup structure on that object, in such a way that every morphism becomes a cosemigroup map, the structure on $A\otimes B$ is induced from those on $A$ and $B$ as above, and the structure on $I$ is the canonical one.  This amounts to a natural assignment of "diagonal maps" $A\to A\otimes A$ satisfying some straightforward axioms.

(If we replaced cosemigroups with comonoids, then the analogous property would characterize [[cartesian monoidal categories]], while if instead we used copointed objects --- that is, the slice $C/I$ --- it would characterize [[semicartesian monoidal categories]].  Interestingly, unlike in those two cases, the relevance case doesn't seem to imply any universal property for the monoidal product or the unit.)

One can of course additionally ask that a relevance monoidal category be [[closed monoidal category|closed]], or that it have finite [[products]] or [[coproducts]].  One might also ask it to be [[star-autonomous]], although in that case there might need to be some compatibility between the star-autonomy and the relevance.

## Examples

* The category of [[pointed sets]], which is equivalent to the category of sets and [[partial functions]], is a relevance monoidal category with its pointed [[smash product]] ([Došen-Petrić 2007](#DosenPetric07)).

* Any [[Church monoid]] is a relevance monoidal category whose underlying category is a [[poset]].

## Related concepts

* [[monoidal category with diagonals]]

* [[semicartesian monoidal category]]

* [[monoidal category]]

* [[relevance logic]]


## References

* {#Petric02} Z. Petrić, _Coherence in Substructural Categories_, Studia Logica volume 70, (2002) pp.271–296, doi:[10.1023/A:1015186718090](https://doi.org/10.1023/A:1015186718090), arXiv:[math/0006061](https://arxiv.org/abs/math/0006061)

* {#DosenPetric07} K. Došen and Z. Petrić, _Relevant Categories and Partial Functions_, Publications de l'Institut Mathématique, Nouvelle Série, Vol. 82(96), pp. 17–23 (2007) ([doi:10.2298/PIM0796017D](https://doi.org/10.2298/PIM0796017D), [arxiv:math/0504133](http://arxiv.org/abs/math/0504133))

[[!redirects relevance monoidal categories]]
