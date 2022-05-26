
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Contents

* table of contents
{: toc}

## Definition

A **closed bicategory** is a [[bicategory]] $B$ admitting all [[Kan extension|right extensions]] and [[Kan lift|right lifts]], equivalently a bicategory whose composition functor

$${\circ}_{x, y, z} \colon B(y,z) \times B(x,y) \to B(x,z)$$

participates in a [[two-variable adjunction]]. Closed bicategories were introduced by Lawvere in unpublished lecture notes *Closed categories and biclosed bicategories* (1971).

## Remarks

A closed bicategory is a [[horizontal categorification]] of a [[closed monoidal category]].  It is not to be confused with a closed [[monoidal bicategory]], which is a [[vertical categorification]] of the same concept.

Dually, a bicategory admitting all *left* extensions and lifts is called a **coclosed bicategory**, and is analogously the horizontal categorification of a [[coclosed monoidal category]]. A bicategory admitting all (right and left) extensions and lifts is a **biclosed bicategory**.

## Examples

- [[Prof]]
- The bicategory $Span(E)$ is closed if and only if the category $E$ is [[locally cartesian closed]]; see ([Day 1974, Proposition 4.1](#Day74)).

## Related entries

* [[symmetric bicategory]]

* An [[closed category|extension system]] is to a closed bicategory what a [[closed category]] is to a [[monoidal category]].

* [[locally internal category]]

## References

* {#Day74} [[Brian Day]], _Limit spaces and closed span categories_,  Lecture Notes in Mathematics, 420, 1974 ([doi:10.1007/BFb0063100](https://doi.org/10.1007/BFb0063100))

* {#BettiWalters1985} [[Renato Betti]], [[Robert F. C. Walters]], *Closed bicategories and variable category theory*, Universita degli Studi di Milano (1985), reprinted in: Reprints in Theory and Applications of Categories, **26** (2020) 1-27 $[$[tac:tr26](http://www.tac.mta.ca/tac/reprints/articles/26/tr26abs.html)$]$

[[!redirects closed bicategories]]
[[!redirects coclosed bicategory]]
[[!redirects coclosed bicategories]]
[[!redirects biclosed bicategory]]
[[!redirects biclosed bicategories]]
