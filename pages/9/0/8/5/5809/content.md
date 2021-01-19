
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _cohomology operation_ is a family of [[morphism]] between [[cohomology groups]], which is [[natural transformation|natural]] with respect to the base space. 

Equivalently, if the [[cohomology theory]] has a [[classifying space]] (as it does for all usual notions of [[cohomology]], in particular for all [[generalized (Eilenberg-Steenrod) cohomology theories]]) then, by the [[Yoneda lemma]], cohomology operations are in natural bijection with [[homotopy]]-classes of morphisms between classifying spaces.

(This statement is made fully explicit for instance below def. 12.3.22 in ([Aguilar-Gitler-Prieto](#AguilarGitlerPrieto)).

$$
  \{
    H^k(-, E)
    \to
    H^l(-, F)
  \}
  \simeq
  Ho(E_k, F_l)
  \,.
$$

## Examples

* every [[universal characteristic class]] is a cohomology operation.

* [[Bockstein homomorphism]]

* [[cup product]]

* [[Massey product]]

* [[power operation]]

  * [[Steenrod squares]] are the stable cohomology endo-operations on [[ordinary cohomology]] (mod 2)

  * [[Adams operations]] are the endo-cohomology operations on [[K-theory]]

* [[logarithmic cohomology operation]]

## References

Steenrod's original colloquium lectures were published as:

* [[Norman Steenrod]], _Cohomology operations, and obstructions to extending continuous functions_,  Advances in Math. 8, 371&#8211;416. (1972)  (<a href="https://doi.org/10.1016/0001-8708(72)90004-7">doi:10.1016/0001-8708(72)90004-7</a>, [pdf](http://www.maths.ed.ac.uk/%7Eaar/papers/steen6.pdf))


Review in:

* {#May} [[Peter May]], chapter 22, section 5 of: _A concise course in algebraic topology_, University of Chicago Press 1999 (ISBN:978-0226511832, [pdf](https://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

In the generality of unstable cohomology operations (operations in [[non-abelian cohomology]]):

* [[John Michael Boardman]], [[David Copeland Johnson]], [[W. Stephen Wilson]], _Unstable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman-Johnson-Wilson/bjw.pdf)), in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))


Textbook accounts:

For [[ordinary cohomology]]:

* [[Robert Mosher]], [[Martin Tangora]], _Cohomology Operations and Application in Homotopy Theory_, Harper and Row (1968), Dover (2008) ([ISBN10:0486466647](https://store.doverpublications.com/0486466647.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/moshtang.pdf))

For [[Adams operations]]:

* {#AguilarGitlerPrieto} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, Section 10 of: _Algebraic topology from a homotopical viewpoint_, Springer (2002)

For [[Steenrod operations]] and operations in [[generalized (Eilenberg-Steenrod) cohomology|generalized cohomology]] ([[MU]] and [[BP]]):

* {#Kochmann96} [[Stanley Kochmann]], section 2.5 and 3.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


Discussion of refinement of cohomology operations to [[differential cohomology]] is in

* Daniel Grady, [[Hisham Sati]], _Primary operations in differential cohomology_, Adv. Math. 335 (2018), 519-562 ([arXiv:1604.05988](https://arxiv.org/abs/1604.05988), [doi:10.1016/j.aim.2018.07.019](https://www.sciencedirect.com/science/article/pii/S0001870818302676?via%3Dihub))


[[!redirects cohomology operations]]