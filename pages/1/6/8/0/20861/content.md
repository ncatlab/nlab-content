[[!redirects Jacobi diagrams]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A closed _Jacobi diagram_ is a suitably oriented connected trivalent [[graph]] with an embedded [[circle]]. If all the [[vertices]] sit on the circle, Jacobi diagrams specialize to [[chord diagrams]].

Half the number of vertices of a Jacobi diagram is called its _order_

$$
  order(\Gamma) \;\coloneqq\; \#Vertices(\Gamma)/2
$$

For example, these are the two closed Jacobi diagrams with 2 vertices (order 1):

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagramsOfOrder1.jpg" width="200">
</center>

and these are are the 10 closed Jacobi diagrams with 4 vertices (order 2):

<center>
<img src="https://ncatlab.org/nlab/files/JacobiDiagramsOfOrder2.jpg" width="700">
</center>

> graphics grabbed from [Chmutov-Duzhin-Mostovoy 11](#ChmutovDuzhinMostovoy11)

In applications to [[Vassiliev invariants]] in [[knot theory]], Jacobi diagrams play the role of connected [[Feynman diagrams]] for [[Chern-Simons theory]] in the presence of one [[Wilson line]] (the circle is then the knot/Wilson line).

**Terminology.** Jacobi diagrams have originally been called "chinese character diagrams" ([Bar-Natan 95, Def. 1.8](#BarNatan95)) 
or "[[Feynman diagrams]] for [[Chern-Simons theory]]" ([Kricker-Spence-Aitchison 97](#KrickerSpenceAitchison97))
or "circle diagrams" ([Kneissler 97](#Kneissler97))
or "round diagrams" ([Willerton 99](#Willerton99)).
The term "Jacobi diagram" ([Chmutov-Duzhin-Mostovoy 11, Chapter 5](#ChmutovDuzhinMostovoy11), [Jackson-Moffat 19, Section 13](#JacksonMoffat19)) alludes to the [[Jacobi identity]], via the fact that these diagrams are naturally labelled by a [[Lie algebra]] equipped with a [[Lie algebra representation]] (which is really just the [[interaction]]-aspect of their interpretation as [[Chern-Simons theory]] [[Feynman diagrams]]...).

## Properties

### Relation to chord diagrams

[[chord diagrams modulo 4T are Jacobi diagrams modulo STU]]:

<center>
<img src="https://ncatlab.org/nlab/files/ChordsMod4TIsCSModSTU.jpg" width="840">
</center>

> graphics grabbed form [Bar-Natan & Stoimenow 97](#BarNatanStoimenow97)

## Related concepts

* [[weight system]]

* [[Vassiliev invariant]]

## References

Original articles

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

* {#KrickerSpenceAitchison97} A. Kricker, B. Spence and I. Aitchison, _Cabling the Vassiliev invariants_, J. Knot Theory Ramifications 6 (1997) 327–358

* {#Kneissler97} Jan Kneissler, _The number of primitive Vassiliev invariants up to degree 12_ ([arXiv:q-alg/9706022](https://arxiv.org/abs/q-alg/9706022))

* {#Willerton99} [[Simon Willerton]], _The Kontsevich integral and algebraic structures on the space of diagrams_ in: Knots in Hellas ’98. Series on Knots and Everything, vol. 24, World Scientific, 2000, 530–546 ([arXiv:math/9909151](https://arxiv.org/abs/math/9909151))


Lecture notes

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))


Textbook accounts

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], Section 5 of:  _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))


* {#JacksonMoffat19} [[David Jackson]], [[Iain Moffat]], Section 13 of: _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))
