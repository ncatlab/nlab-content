+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Homotopy type theory
+-- {: .hide}
[[!include homotopy type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

[[Homotopy type theory]] provides a [[synthetic mathematics|synthetic]]  formalization of [[homotopy theory]] in its modern and most powerful incarnation in the guise of [[(∞,1)-toposes]].

Just like plain [[dependent type theory]] is the [[internal logic]] of
[[locally cartesian closed categories]], so homotopy type theory is the
internal logic of [[locally cartesian closed (∞,1)-categories]], and
homotopy type theory with [[univalence|univalent]] type [[universes]] is the internal
logic of [[elementary (∞,1)-toposes]]. This means that homotopy type
theory provides a "structural" foundation of the kind that William
Lawvere had found in [[topos theory]], but refined to homotopy theory
in the refined guise of (∞,1)-topos theory.

Homotopy type theory natively knows about the formalization of simplicial homotopy theory and higher topos theory without the need to first formalize several textbooks worth of material starting from bare set theory. For instance, the formal proof of the [[Blakers-Massey theorem]] ([FFLL](#FFLL)) does not need to begin by first formalizing what a simplicial set is,
what a Kan fibrancy condition is, what the infinite tower of homotopy
groups is, what weak homotopy equivalences are, what homotopy pushouts
are, how they reflect in long exact sequences of homotopy groups;
because all this is native to homotopy type theory. Accordingly, the
proof, on top of being a formal proof, is elegantly transparent
and of actual practical interest. Moreover, since the formal HoTT
proof generalizes the traditional statement to more general
(∞,1)-toposes, it is actually a genuine new mathematical result of
genuine interest in modern homotopy theory, to practicing
mathematicians not concerned about foundations. 


## Cubical synthetic homotopy theory

In ([Mörtberg-Pujet](#Mortberg-Pujet)) the authors make the case for the use of [[cubical type theory]] over [[HoTT]] in synthetic homotopy theory since [[univalence]] and [[HITs]] are natively supported there, rather than axiomatically added as in HoTT. The path algebra in HoTT is made complicated by the fact that many equalities do not hold definitionally, even in the proof of simple results such as that the torus is equivalent to the product of two circles. The proof of this result is trivial in cubical type theory.


## References

The above text follows [Schreiber 14](https://cs.nyu.edu/pipermail/fom/2014-October/018251.html).

* [[Mike Shulman]], slides 37 onwards in _Homotopical trinitarianism:A perspective on homotopy type theory_, 2018 ([pdf](https://home.sandiego.edu/~shulman/papers/trinity.pdf))

* {#Rijke19} [[Egbert Rijke]], _Classifying Types_ ([arXiv:1906.09435](https://arxiv.org/abs/1906.09435))

* {#FFLL} [[Favonia|Kuen-Bang Hou (Favonia)]], [[Eric Finster]], [[Dan Licata]], [[Peter LeFanu Lumsdaine]], _A mechanization of the Blakers-Massey connectivity theorem in Homotopy Type Theory_, ([arXiv:1605.03227](https://arxiv.org/abs/1605.03227)) 

Many of the articles listed at [[mathematics presented in homotopy type theory]] count as synthetic homotopy theory.

The use of [[cubical type theory]] for synthetic homotopy theory is discussed in:

* {#Mortberg-Pujet} [[Anders Mörtberg]], Loïc Pujet, _Cubical synthetic homotopy theory_,  CPP 2020: Proceedings of the 9th ACM SIGPLAN International Conference on Certified Programs and Proofs January 2020, pp. 158–171, [doi:10.1145/3372885.3373825](https://doi.org/10.1145/3372885.3373825), ([pdf](https://staff.math.su.se/anders.mortberg/papers/cubicalsynthetic.pdf))
