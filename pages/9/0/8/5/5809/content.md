
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

Equivalently, if the [[cohomology theory]] has a [[classifying space]] (as it does for all usual notions of [[cohomology]], in particular for all [[Whitehead-generalized cohomology theories]]) then, by the [[Yoneda lemma]], (non-abelian/unstable) cohomology operations are in natural bijection with [[homotopy classes]] of maps between classifying spaces.

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

(This statement is made fully explicit for instance below def. 12.3.22 in ([Aguilar-Gitler-Prieto](#AguilarGitlerPrieto)).


If here $E_\bullet$ and $F_\bullet$ are the component spaces of [[spectra]] and if such cohomology operations are compatible with the [[suspension isomorphism]], then one speaks of a _stable cohomology operation_.

## Examples

### List of examples

* every [[universal characteristic class]] is a cohomology operation.

* [[Bockstein homomorphism]]

* [[cup product]]

* [[Massey product]]

* [[power operation]]

  * [[Steenrod squares]] are the stable cohomology endo-operations on [[ordinary cohomology]] (mod 2)

  * [[Adams operations]] are the endo-cohomology operations on [[K-theory]]

* [[logarithmic cohomology operation]]



### Cup powers in multiplicative cohomology
 {#CupPowersInMultiplicativeCohomology}


\begin{example}
  \label{CupSquareCohomologyOperation}
  [**Cup-square cohomology operation**]

Let $E$ be a [[multiplicative cohomology theory|multiplicative]] [[Whitehead-generalized cohomology theory]] [[Brown representability theorem|represented]] by a [[ring spectrum]]

$$
  \big(
    E, 1^E, m^E
  \big)
  \;\in\;
  CommutativeMonoids
  \Big(
    Ho\big( Spectra\big),
    \mathbb{S},
    \wedge
  \Big)
  \,.
$$

Then for all $n \in \mathbb{N}$ there is an unstable $E$-cohomology operation

\[
  \label{CupSquareAsUnstableCohomologyOperation}
  \big[
    \Omega^\infty \Sigma^n E
    \overset{
      (-)^{2_\cup}
    }{\longrightarrow}
    \Omega^\infty \Sigma^{2 n} E
  \big]
  \;\;\in\;\;
  \widetilde E^{ 2 n }
  \big(
    \Omega^{\infty - n} E
  \big)
\]

defined -- via the [[Yoneda lemma]] on the [[opposite category|opposite]] of the [[classical homotopy category]] of [[pointed topological spaces]] -- by acting over any $X \,\in\, Ho\big(PointedTopologicalSpaces\big)$ as the [cup square on E-cohomology](cup+product#CupProductInWhiteheadGeneralizedCohomologyTheory) on cohomology in degree $n$:

\[
  \label{CupSquareInMultiplicativeCohomologyNaturalTransformation}
  X
  \;\;\mapsto\;\;
  \Big(
  [X, \Omega^\infty \Sigma^n E]
  \,=\,
  {\widetilde E}{}^n(X)
  \overset{
    \;\;
    \Delta_{{\widetilde E}{}^n(X)}
    \;\;
  }{\longrightarrow}
  {\widetilde E}{}^n(X)
  \times  
  {\widetilde E}{}^n(X)
  \overset{ \;\;  
    \cup^E_X 
  \;\; }{\longrightarrow}
  {\widetilde E}{}^n(X)
  \,=\,
  [X, \Omega^\infty \Sigma^{2n} E]
  \Big)
\]

Here the first [[function]] $\Delta_{{\widetilde E}{}^n(X)}$ is the [[diagonal morphism|diagonal]] on the _set_ underlying the degree=$n$ $E$-[[cohomology group]] of $X$, while the second function $\cup^E_X$ is the operation of forming the [E-cup product](cup+product#CupProductInWhiteheadGeneralizedCohomologyTheory) of [[pairs]] of its elements.

Both of these operations are clearly [[natural transformations]] (for the first this is evident, for the second this comes down to the fact that the [smash-monoidal diagonals of suspension spectra](suspension+spectrum#SmashMonoidalDiagonals) are natural, hence are indeed [[monoidal category with diagonals|monoidal diagonals]]). Therefore the [[full subcategory|fully-faithfulness]] of the [[Yoneda embedding]] 

$$ 
  Ho
  \big(
    PointedTopologicalSpaces
  \big)^{op}
  \;\overset{ \;\; \;\; }{\hookrightarrow}\;
  Functors
  \Big(
    Ho
    \big(
      PointedTopologicalSpaces
    \big)^{op}
    ,
    Set
  \Big)
$$

implies that this natural transformation (eq:CupSquareInMultiplicativeCohomologyNaturalTransformation) between the [[representable functors]] $[-,\Omega^\infty \Sigma^n E]$ and $[-,\Omega^\infty \Sigma^{2n} E]$ is itself represented by a [[morphism]] (eq:CupSquareAsUnstableCohomologyOperation) between the representing classifying spaces, hence by an unstable cohomology operation.

\end{example}

The analogous construction of course exists for the $k$th cup power 
$(-)^{k_\cup}$ for any $k \in \mathbb{N}$. Brief mentioning of this is in [Wirthmüller 12, Example (1) on p. 44 (46 of 67) ](#Wirthmuller12).

## References

### General

Steenrod's original colloquium lectures:

* [[Norman Steenrod]], _Cohomology operations, and obstructions to extending continuous functions_,  Advances in Math. 8, 371&#8211;416. (1972)  (<a href="https://doi.org/10.1016/0001-8708(72)90004-7">doi:10.1016/0001-8708(72)90004-7</a>, [pdf](http://www.maths.ed.ac.uk/%7Eaar/papers/steen6.pdf))

Background and review:

* [[John Michael Boardman]], _Stable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman/stabop.pdf)) in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

* {#May} [[Peter May]], chapter 22, section 5 of: _A concise course in algebraic topology_, University of Chicago Press 1999 (ISBN:978-0226511832, [pdf](https://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

On the structure on the collection of all unstable cohomology operations:

* [[John Michael Boardman]], [[David Copeland Johnson]], [[W. Stephen Wilson]], _Unstable Operations in Generalized Cohomology_ ([pdf](https://hopf.math.purdue.edu/Boardman-Johnson-Wilson/bjw.pdf)), in: [[Ioan Mackenzie James]] (ed.) _[[Handbook of Algebraic Topology]]_ Oxford 1995 ([doi:10.1016/B978-0-444-81779-2.X5000-7](https://doi.org/10.1016/B978-0-444-81779-2.X5000-7))

* [[Andrew Stacey]], [[Sarah Whitehouse]], _The Hunting of the Hopf Ring_,     Homology Homotopy Appl. Volume 11, Number 2 (2009), 75-132. ([arXiv:0711.3722](https://arxiv.org/abs/0711.3722), [euclid:hha/1251832594](https://projecteuclid.org/euclid.hha/1251832594))

* [[Tilman Bauer]], _Formal plethories_, Advances in Mathematics Volume 254, 20 March 2014, Pages 497-569 ([arXiv:1107.5745](https://arxiv.org/abs/1107.5745), [doi:10.1016/j.aim.2013.12.023](https://doi.org/10.1016/j.aim.2013.12.023))

* [[William Mycroft]], _Unstable Cohomology Operations: Computational Aspects of Plethories_, 2017 ([pdf](https://etheses.whiterose.ac.uk/20524/1/wm-thesis-final.pdf), [[MycroftUnstableCohomologyOperations.pdf:file]])

### On ordinary cohomology

Operations on [[ordinary cohomology]]:

* [[Robert Mosher]], [[Martin Tangora]], _Cohomology Operations and Application in Homotopy Theory_, Harper and Row (1968), Dover (2008) ([ISBN10:0486466647](https://store.doverpublications.com/0486466647.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/moshtang.pdf))


* [[Andrew Stacey]], [[Sarah Whitehouse]], _Stable and unstable operations in mod $p$ cohomology theories_, Algebr. Geom. Topol. Volume 8, Number 2 (2008), 1059-1091 ([arXiv:math/0605471](https://arxiv.org/abs/math/0605471), [euclid:agt/1513796856](https://projecteuclid.org/euclid.agt/1513796856))


### On topological K-theory

Operations on [[topological K-theory]]:

* {#Wirthmuller12} [[Klaus Wirthmüller]], Sections 11 and 13 of: _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])

For [[Adams operations]]:

* {#AguilarGitlerPrieto} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, Section 10 of: _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([doi:10.1007/b97586](https://link.springer.com/book/10.1007/b97586))

More:

* [[William Mycroft]], [[Sarah Whitehouse]], _The plethory of operations in complex topological K-theory_ ([arXiv:2001.01608](https://arxiv.org/abs/2001.01608))


### On complex-oriented cohomology theories

For [[Steenrod operations]] on [[complex oriented cohomology|complex-oriented]] [[Whitehead-generalized cohomology|generalized cohomology]] (such as [[MU]] and [[BP]]):

* {#Kochmann96} [[Stanley Kochmann]], section 2.5 and 3.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

### On differential cohomology

Refinement to [[differential cohomology]]:

* Daniel Grady, [[Hisham Sati]], _Primary operations in differential cohomology_, Adv. Math. 335 (2018), 519-562 ([arXiv:1604.05988](https://arxiv.org/abs/1604.05988), [doi:10.1016/j.aim.2018.07.019](https://www.sciencedirect.com/science/article/pii/S0001870818302676?via%3Dihub))


[[!redirects cohomology operations]]