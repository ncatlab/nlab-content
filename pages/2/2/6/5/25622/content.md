
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Algebra 
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The term *graded derivation* would a priori refer in general to suitably compatible [[derivations]] of [[graded algebras]], but is in practice used mostly for those operations $d \,\colon\, A \to A$ on [[superalgebras]] $A$ that satisfy the condition that for $a_1, a_2 \,\in\, A$ a [[pair]] of [[elements]] each of homogeneous degree $deg(a_i) \in \mathbb{Z} \,mod\, 2$ the derivation of their product is

$$
  d(a_1 \cdot a_2)
  \;=\;
  (d a_1) \cdot a_2
  +
  (-1)^{deg(a_1) \cdot deg(d)}
  a_1 \cdot d a_2
  \,,
$$

where $deg(d) \,\in\, \mathbb{Z} \,mod\,2$ is the degree of the graded derivation.

For $d = 0$ this is the law satisfied by an ordinary (un-graded) [[derivation]], also known as the *[[Leibniz rule]]* satisfied by ordinary [[differentiation]]. The archetypical example of a non-trivially graded derivation is the [[de Rham differential]] acting on the [[de Rham algebra]].

[[!redirects graded derivations]]



