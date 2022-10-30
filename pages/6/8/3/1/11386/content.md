
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
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

For $p$ a [[prime number]], givem $n \in \mathbb{N}$ write $K(n)$ for the coresponding [[Morava K-theory]] [[spectrum]] and write $L_{K(n)}(-)$ for [[K(n)-local spectrum|K(n)-localization]] of spectra.

The _Bousfield-Kuhn functor_ $\Phi$ is a [[functor]] from [[pointed object|pointed]] [[homotopy types]] to [[spectra]]

$$
  \Phi \;\colon\; \in \infty Grpd_\ast \longrightarrow Spectra
$$

such that there is a [[natural equivalence]]

$$
  \Phi(\Omega^\infty Y ) \simeq L_{K(n)}(Y)
$$

and

$$
  \pi_\bullet \Phi(X) \simeq v_n^{-1} \pi_\bullet(X)
  \,.
$$

(...)

## Related concepts

* [[power operation]]

* [[logarithmic cohomology operation]]

## References

The original articles are


* [[Aldridge Bousfield]], _Uniqueness of infinite deloopings for K-theoretic spaces_, Pacific J. Math. 129 (1987), no. 1, 1&#8211;31. MR 89g:55017

* [[Nicholas Kuhn]], _Morava K-theories and infinite loop spaces, Algebraic topology (Arcata, CA, 1986) (Berlin), Lecture Notes in Math., vol. 1370, Springer, 1989, pp. 243&#8211;257. MR
MR1000381 (90d:55014)

See also 

* [[Nat Stapleton]], _Power operations and the Bousfield-Kuhn functro_, in _Report of $E$-theory conjectures seminar_ (2013) ([pdf](http://math.berkeley.edu/~ericp/latex/misc/mit-ethy.pdf))

The relation to [[topological André-Quillen cohomology]] is discussed in

* [[Mark Behrens]], [[Charles Rezk]], _The Bousfield-Kuhn functor and topological Andr&#233;-Quillen cohomology_ ([pdf](http://math.mit.edu/~mbehrens/papers/BKTAQ4.pdf))

Review and further discussion of [[logarithmic cohomology operations]] is in 

* {#Rezk06} [[Charles Rezk]], _The units of a ring spectrum and a logarithmic cohomology operation_, J. Amer. Math. Soc. 19 (2006), 969-1014 ([arXiv:math/0407022](http://arxiv.org/abs/math/0407022))

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], section 4.2 of  _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

[[!redirects Bousfield-Kuhn functors]]

[[!redirects Bousfield-Kuhn construction]]
[[!redirects Bousfield-Kuhn constructions]]

