
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Cardy condition_ is part of the [[sewing constraint]] consistency condition on data that gives an [[open string|open]]-[[closed string|closed]] [[2d CFT]] or [[2d TQFT]].

It is the algebraic reflection of the fact that the following two [[cobordisms]] are equivalent (as topological as well as as conformal cobordisms):

1. an [[open string]] coming in, closing to a [[closed string]] and then opening up again to an open string (the "zip-unzip cobordism");

1. an [[open string]] coming in, splitting into two open strings, these crossing each other (with the endpoints of one of them at the same time making a full rotation), then both merging again to one open string.

(e.g. [Lauda-Pfeiffer 05 (3.44)](#LaudaPfeiffer05), [Kong 06, figure 3](#Kong06))

[[cardy_condition.jpg:pic]]

For instance in the classification of open-closed [[2d TQFT]] with [[coefficients]] in [[Vect]] via [[Frobenius algebras]], this means that for $O$ the Frobenius algebra of open string states and for $C$ the commutative Frobenius algebra of closed string states, then the canonical [[linear function]]

$$
  O \longrightarrow C \longrightarrow O
$$

is equal to the canonical map

$$
  O \stackrel{\Delta}{\longrightarrow} O \otimes O
  \stackrel{\tau}{\longrightarrow}
  O \otimes O
  \stackrel{\mu}{\longrightarrow}
  O
  \,,
$$

where $\mu$ is the [[coalgebra|coproduct]], $\mu$ the product and $\tau$ the [[braided monoidal category|braiding]] (e.g. [Lauda-Pfeiffer 05 (2.14)](#LaudaPfeiffer05)).

## Related concepts

* [[modular invariance]]

## References

Discussion in [[2d TQFT]] includes

* {#LaudaPfeiffer05} [[Aaron Lauda]], [[Hendryk Pfeiffer]] (2005), Open-closed strings: two-dimensional extended TQFTs and Frobenius algebras, _Topology Appl._ **155**, 623-666. ([arXiv:0510664](http://arxiv.org/abs/math/0510664))

* {#MooreSegal06} [[Gregory W. Moore]], [[Graeme Segal]] (2006), D-branes and K-theory in 2D topological field theory. ([arXiv:hep-th/0609042](https://arxiv.org/abs/hep-th/0609042))

* {#MooreSegal02} [[Gregory W. Moore]], [[Graeme Segal]] (2002), Lectures on Branes, K-theory and RR Charges. Lecture notes from the Clay Institute School on Geometry and String Theory held at the Isaac Newton Institute, Cambridge, UK. Available [here](http://www.physics.rutgers.edu/∼gmoore/clay1/clay1.html); related notes from the ITP Miniprogram ‘The Duality Workshop’ at Santa Barbara available [here](http://online.itp.ucsb.edu/online/mp01/moore1/).

Discussion in [[2d CFT]] includes

* {#Kong06} [[Liang Kong]], _Cardy condition for open-closed field algebras_ ([arXiv:math/0612255](http://arxiv.org/abs/math/0612255))

[[!redirects Cardy conditions]]
