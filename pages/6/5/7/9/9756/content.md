
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Ideas

In ([[homotopy type theory|homotopy]]) [[type theory]] with [[type universes]], by the *typical universe ambiguity* or just *typical ambiguity*, for short, one refers to the universe level remaining implicit, as long as a [[proof assistant]] is or would be able to deduce it from context.

Both Russell and Tarski style universes can be typically ambiguous or not.

## Examples

* [[Coq]] uses Russell style universes with typical ambiguity. 

* [[Agda]] uses Russell style universes without typical ambiguity: you always have to explicitly indicate the universe level.

* The [[HoTT Book]] (first edition) uses Russell style universes with (except for a few places) typical ambiguity.

## Related concepts

* [[universe polymorphism]]

## References

* Solomon Feferman, _Typical ambiguity: Trying to have your cake and eat it too_

* [Blog Post](http://golem.ph.utexas.edu/category/2012/12/universe_polymorphism_and_typi.html)