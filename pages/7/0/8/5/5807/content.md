
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


\tableofcontents

## Idea ##

In [[knot theory]],
*writhe* is a measure of how much a [[knot]] or [[link]] _writhes_ around itself.  As a 1-dimensional line cannot actually twist, this is not a [[knot invariant]] but is an invariant of [[framed knots]] (and [[framed links]]).  Since a [[link diagram]] can be given a natural framing (the _blackboard framing_), it is possible to compute the writhe of a specific diagram.  One place where this is used very neatly is to convert the [[Kauffman bracket]], which is an invariant of framed links, into the [[Jones polynomial]], being an invariant of ordinary links.

## Definition ##

Recall that a [[framed link]] can be thought of as a link together with a normal direction along each component, which we call the _framing direction_.

+-- {: .num_definition #writhe}
###### Definition
The **writhe** of a framed link is the [[linking number]] of the link with its infinitesimal displacement in the framing direction.
=--

For an oriented link diagram, the writhe is defined using the orientation of the crossings.

+-- {: .num_definition #writediag}
###### Definition
The **writhe** of an oriented [[link diagram]] is defined to be the sum of the orientations of its crossings.
=--

## Related concepts

* [[crossing number]]

* [[linking number]]

* [[framing number]]

## References

* Colin C. Adams p. 152 of: *The Knot Book -- An elementary Introduction to the Mathematical Theory of Knots*,  W. H. Freedman and Co. (1994) &lbrack;[ISBN:978-0-8218-3678-1](https://bookstore.ams.org/KNOT)&rbrack;

* {#Ohtsuki01} [[Tomotada Ohtsuki]], p. 523 in: *Quantum Invariants -- A Study of Knots, 3-Manifolds, and Their Sets*, World Scientific (2001) &lbrack;[doi:10.1142/4746](https://doi.org/10.1142/4746)&rbrack;

* David Cimasoni: *Computing the writhe of a knot*, J. Knot Theory Ramifications **10** 3 (2001) 387-395 &lbrack;[arXiv:math/0406148](https://arxiv.org/abs/math/0406148), [doi:10.1142/S0218216501000913](https://doi.org/10.1142/S0218216501000913), [pdf](https://www.unige.ch/math/folks/cimasoni/writhe.pdf)&rbrack;

See also:

* Wikipedia: *[Writhe](https://en.wikipedia.org/wiki/Writhe)*

