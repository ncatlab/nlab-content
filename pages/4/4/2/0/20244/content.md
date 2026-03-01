
> This entry is about the concept in [[group theory]]. For the concept in [[quantum field theory|quantum]][[field theory]] see at _[[effective action functional]]_; for disambiguation see *[[effective action]]*.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A [[group action]] is _effective_ if no group element other than the [[neutral element]] acts [[trivial action|trivially]] on _all_ elements of the space, hence if no other element acts the way the neutral element does.

## Definition

A [[group action]] of a [[group]] ([[group object]]) $G$ on a  [[set]] ([[object]]) $X$ is _effective_ if $\underset{x \in X}{\forall} g x = x$ implies that $g = e$ is the [[neutral element]].

Beware the similarity to and difference with [[free action]]: a free action is effective, but an effective action need not be free.

## Properties

\begin{proposition}\label{NewmanTheorem}
**(Newman's theorem)** Given an effective action of a [[finite group]] $G$ on a [[connected topological space|connected]] [[manifold]] $X$ by [[homeomorphisms]], then the [[subset]] $X_{reg} \subset X$ of points with [[trivial group|trivial]] [[stabilizer group]] is [[open subset|open]] and everywhere [[dense subset|dense]].
\end{proposition}
(cf. [Dress 1969 Thm. 1](#Dress1969))


## Related concepts

* [[transitive action]], [[free action]], [[semi-free action]], [[regular action]],

* [[proper action]], [[properly discontinuous action]]

* [[effective orbifold]]

## References

Original reference for Newman's theorem:

* [[M. H. A. Newman]], _A theorem on periodic transformations of spaces_, The Quarterly Journal of Mathematics os-2:1 (1931), 1-8.  [DOI](https://doi.org/10.1093/qmath/os-2.1.1-a).


See also

* {#Dress1969} [[Andreas Dress]]: *Newman's theorems on transformation groups*, Topology **8** 2 (1969) 203-207 \[<a href="https://doi.org/10.1016/0040-9383(69)90010-X">doi:10.1016/0040-9383(69)90010-X</a>\]

[[!redirects effective group actions]]

[[!redirects Newman's theorem]]
[[!redirects Newman theorem]]
