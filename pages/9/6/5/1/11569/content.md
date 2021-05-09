

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[forgetful functor]] $U$ from [[abelian groups]] to [[commutative monoids]] has a [[left adjoint]] $G$. This is called _group completion_.
A standard presentation of the group completion is the [[Grothendieck group of a commutative monoid]]. As such group completion plays a central role in the definition of [[K-theory]].


More generally in [[(∞,1)-category theory]] and [[higher algebra]] there is 
the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  K \;\colon\;  CMon_\infty(\infty Grpd) \longrightarrow AbGrp_\infty(\infty Grpd)
$$

to the inclusion of [[abelian ∞-groups]] ([[connective spectra]]) into [[commutative ∞-monoids]] in [[∞Grpd]] ([[E-∞ spaces]]). This may be called _$\infty$-group completion_.

This serves to define [[algebraic K-theory of symmetric monoidal (∞,1)-categories]].

In [[algebraic topology]] a key role was played by models of this process at least on [[H-spaces]] ([Quillen 71](#Quillen71), [May, def. 1.3](#May)). If $N$ is a [[topological monoid]], let $B N$ denotes its [[bar construction]] ("[[classifying space]]") and $\Omega B N$ the [[loop space]] of that. Then this 
$$
  N \longrightarrow \Omega B N
$$
represents the group completion of $N$ ([Quillen 71, section 9](#Quillen71), [May, theorem  1.6](#May)). This crucially enters the construction of the [[K-theory of a permutative category]].

According to ([Dwyer-Kan 80, prop. 3.7, prop. 9.2, remark 9.7](#DwyerKan80)) this indeed gives a model for the total [[derived functor]] of 1-categorical group completion.

## Related concepts

* [[Grothendieck group]]

* [[localization of a monoid]]

## References

Classical accounts include

* {#Quillen71} [[Daniel Quillen]], _On the group completion of a simplicial monoid_ [pdf](http://www.maths.ed.ac.uk/~aar/papers/quillencomp.pdf), MIT preprint 1971, Memoirs of the AMS vol 529, 1994, pp. 89-105

* {#May} [[Peter May]], _$E_\infty$-Spaces, group completions, and permutative categories_ ([pdf](http://www.math.uchicago.edu/~may/PAPERS/13.pdf))

* {#DwyerKan80} [[William Dwyer]], [[Daniel Kan]], _Simplicial localization of categories_, Journal of pure and applied algebra 17 (1980) 267-284


$\infty$-Group completion is discussed in

* {#BunkeTamme12} [[Ulrich Bunke]], [[Georg Tamme]], section 2.1 of _Regulators and cycle maps in higher-dimensional differential algebraic K-theory_ ([arXiv:1209.6451](http://arxiv.org/abs/1209.6451))

* {#Nikolaus13} [[Thomas Nikolaus]] _Algebraic K-Theory of $\infty$-Operads_ ([arXiv:1303.2198](http://arxiv.org/abs/1303.2198))

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], def. 6.1 in  _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

and specifically its monoidal properties in 

* {#GepnerGrothNikolaus13} [[David Gepner]], [[Moritz Groth]], [[Thomas Nikolaus]], _Universality of multiplicative infinite loop space machines_, [arXiv:1305.4550](http://arxiv.org/abs/1305.4550).


[[!redirects group completions]]

[[!redirects ∞-group completion]]
[[!redirects ∞-group completions]]