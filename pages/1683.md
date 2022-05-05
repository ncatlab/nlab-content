
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The **K-theory spectrum** $KU$ (for complex K-theory) or $KO$ (for orthogonal K-theory) in the strict sense is the [[spectrum]] that represents the [[generalized (Eilenberg-Steenrod) cohomology]] theory [[topological K-theory]]. For complex [[topological K-theory]] this is periodic with period 2 (reflect Bott periodicity) of the form

$$
  \mathbb{Z} \times B U ,\; U ,\; \cdots
  \,.
$$


## Definition

As a [[symmetric spectrum]]: [Schwede 12, Example I.2.10](#Schwede12)

## Properties

### Periodicity

$KU$ is a 2-[[periodic ring spectrum]]. This is the original _[[Bott periodicity]]_.

### As a localization of an $\infty$-group $\infty$-ring

[[Snaith's theorem]] asserts that the [[K-theory spectrum]] for [[periodic complex K-theory]] is the [[∞-group ∞-ring]] of the [[circle 2-group]] localized away from the [[Bott element]] $\beta$:

$$
  KU \simeq \mathbb{S}[B U(1)][\beta^{-1}]
  \,.
$$

### Relation between $KU$, $KO$ and  $KR$-

#### $KO$ as homotopy-fixed points of $KU$

[[complex conjugation|Complex conjugation]] on [[complex vector bundles]] induces on the [[complex K-theory]] [[spectrum]] $KU$ an [[involution|involutive]] [[automorphism]]. [[KR-theory]] is the corresponding $\mathbb{Z}_2$-[[equivariant cohomology]] theory. 

In particular, the [[homotopy fixed point]] of [[KU]] under this automorphism is [[KO]]

$$
  KO \simeq (KU)^{\mathbb{Z}/2}
$$

and this way where in complex K-theory one has [[KU]]-[[modules]] ([[∞-modules]]), so in KR-theory one has $KO$-modules.

#### Wood's theorem

$$
  KO \wedge \Sigma^{-2}\mathbb{CP}^2 \simeq KU
$$

a proof in terms of [[moduli stacks]] is given in [Mathew 13, section 3](#Mathew13)

### Relation to Clifford algebras

There are close relations between K-theory and [[Clifford algebras]]. One conceptual statement relating them is this:

_KO-theory is the first Weiss-derivative (in [[orthogonal calculus]]) of the K-theory of Clifford algebras._ ([[Charles Rezk]], [MO comment, Sept '13](http://mathoverflow.net/a/142091/381))


## Related concepts

* [[Eilenberg-MacLane spectrum]]

* [[tmf]]

* [[cohomology theory]]

* [[KO-theory]]

* [[Tate K-theory]]

* [[splitting principle]]

* [[comparison map between algebraic and topological K-theory]]

[[!include string theory and cohomology theory -- table]]


## References

The weak homotopy eqivalence $B U \to \Omega U$ is discussed in detail in

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, appendix B.2 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

The incarnation of $KU$ and $KO$ as a [[symmetric spectrum]] is discussed in

* {#Schwede12} [[Stefan Schwede]], Example I.2.10 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

and the structure of a [[symmetric ring spectrum]] on $KO$ is discussed in

* {#Joachim01} [[Michael Joachim]], _A symmetric ring spectrum representing
$KO$-theory_, Topology 40 (2001) 299-308

The structure of a homotopy [[ring spectrum]] on $KU$ is discussed in 

* {#Switzer75} [[Robert Switzer]], section 13.90 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

The [[E-infinity ring]] structure of $KU$ is discussed in 

* [[Peter May]], section VIII &#167;2 of _$E_\infty$-Ring spaces and $E_\infty$ ring spectra_ ([pdf](http://www.math.uchicago.edu/~may/BOOKS/e_infty.pdf))

and the underlying [[H-infinity ring spectrum]] structure in 

* {#McLure86} [[James McLure]], _$H_\infty$-ring spectra via space-level homotopy theory_ ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/BMMS8.pdf)), chapter VII in R. Bruner, [[Peter May]], [[James McLure]], M. Steinberger, _$H_\infty$-Ring Spectra and their Applications_, Lecture Notes in Mathematics 1176, Springer 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/h_infty.pdf))

The uniqueness of the [[E-infinity ring]] structure on $KU$ is due to

* [[Andrew Baker]], [[Birgit Richter]], _$\Gamma$-cohomology of rings of numerical polynomials and $E_\infty$ structures on K-theory_ ([arXiv:math/0304473](https://arxiv.org/abs/math/0304473))

Discussion of $KO$ in analogy to the construction of [[tmf]] is in 

* {#Mathew13} [[Akhil Mathew]], _The homology of $tmf$_ ([arXiv:1305.6100](http://arxiv.org/abs/1305.6100))

with a summary in 

* [[Akhil Mathew]], _The homotopy groups of $TMF$_ ([pdf](http://math.mit.edu/~sglasman/tmfhomotopy.pdf))



[[!redirects KU]]
[[!redirects KO]]

[[!redirects complex K-theory spectrum]]

[[!redirects KU-theory]]
