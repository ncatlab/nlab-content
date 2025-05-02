
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Geometric type theory_ is a conjectural extension of [[geometric logic]] to  an [[extensional type theory|extensional]] [[dependent type theory|dependent]] [[type theory]].  That is, it is supposed to be a dependent type theory which under the [[relation between category theory and type theory]] corresponds to [[sheaf toposes]], and is preserved by [[geometric morphisms]].

At present it is not clear exactly how such a type theory should be defined.

A *motivating example* is a [[geometric theory]] as follows. Its signature has one sort, $N$, and two function symbols $0\colon 1 \to N$ and $s \colon N \to N$. Its axioms are -

  * $0 = s(n) \vdash_{n} \bot$
  * $s(n) = s(n') \vdash_{n n'} n=n'$
  * $\top \vdash_{n} \bigvee_{i} n=s^{i}(0)$

("$s^{i}(0)$" is not a term in the formal language, but $i$ indexes an inductively defined sequence of formulae "$n=s^{i}(0)$".)

In any model (in a Grothendieck topos) the interpretation of $N$ is uniquely isomorphic to an [[natural numbers object|nno]], so the nno can be characterized uniquely up to isomorphism by geometry theory - something that would be impossible in finitary first-order logic. There is essentially only one model, and this theory is equivalent to the empty theory. What this illustrates is that a sort for the nno can be added "for free" to any theory - and this is consistent with the fact that nno's are preserved by inverse image functors.

List objects ($List X$ is the set of finite sequences of elements from $X$) can similarly be added "for free", and in fact the same goes for free constructions for [[cartesian theory|cartesian theories]]. Thus such constructors can be added as a type theoretic adjunct to geometric logic without altering its expressive power. Since geometric type theory also includes [[quotient types]], the constructions are similar to quotient inductive types.

As an example, the [[geometric theory]] of a real number can be rewritten in a form that more directly describes Dedekind sections of rationals, with sort $Q$ that is geometrically constrained to be the rationals. For further details, see [Vickers 2007](#Vickers07).

All this leads to a conjecture of a "geometric type theory", geometric logic enhanced with the geometrically definable types.

An "arithmetic type theory" has now been formalized [Vickers 2018](#Vickers18) by adjoining such type constructors to coherent logic.
Categorically, it corresponds to replacing [[Grothendieck topos|Grothendieck toposes]] with [[arithmetic universe|arithmetic universes]].
Although it lacks the infinitary disjunctions of geometric logic, they can in many cases be provided by existential quantification over infinite sorts.
[Vickers 2017](#Vickers17) shows how it can be used to prove base-free results for (relative) Grothendieck toposes.





## Related concepts

* [[modal type theory]]

* [[geometric homotopy type theory]]

* [[synthetic geometry]]

* [[geometric mathematics]]

* [[strongly predicative dependent type theory]]

## References

* {#Vickers07}[[Steve Vickers]], _Locales and toposes as spaces_, Handbook of Spatial Logics, Springer 2007 ([pdf](http://www.cs.bham.ac.uk/~sjv/LocTopSpaces.pdf))

* {#Vickers17}[[Steve Vickers]], _Arithmetic universes and classifying toposes_, Cahiers de topologie et g&eacute;om&eacute;trie diff&eacute;rentielle cat&eacute;gorique **58 (4)** (2017), pp. 213-248 ([pdf](http://arxiv.org/abs/1701.04611))

* {#Vickers18}[[Steve Vickers]], _Sketches for arithmetic universes_, accepted 2018 for Journal of Logic and Analysis ([pdf](http://arxiv.org/abs/1608.01559))

* {#vBB25} [[Johannes Schipp von Branitz]] and [[Ulrik Buchholtz]]. *Propositional Geometric Type Theory*, Workshop on Homotopy Type Theory / Univalent Foundations 2025, Genoa, Italy, 16 April 2025. ([slides](https://hott-uf.github.io/2025/slides/Schipp_von_Branitz.pdf), [video](https://www.youtube.com/watch?v=URr93_DWDNg))

[[!redirects geometric type theories]]