
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

An (even) _2-periodic cohomology theory_ or just _periodic cohomology theory_ for short is an ([[even cohomology theory|even]]) [[multiplicative cohomology theory|multiplicative]] [[cohomology theory]] $E$ with a [[Bott element]] $\beta \in E^2({*})$ which is invertible (under multiplication in the [[cohomology ring]] of the point) so that multiplication by it induces an [[isomorphism]] 

$$
  (-)\cdot \beta : E^*({*}) \simeq E^{*+2}({*})
  \,.
$$

Via the [[Brown representability theorem]] this corresponds to a [[periodic ring spectrum]].

Compare with the notion of [[weakly periodic cohomology theory]].

More generally one considers $2n$-periodic cohomology theories

## Properties

### Periodicity of the $\infty$-category of $\infty$-modules
 {#PeriodicityOnModules}

For $E$ an [[E-∞ ring]] representing a periodic cohomology (a [[periodic ring spectrum]]) double [[suspension]]/[[looping]] on any $E$-[[∞-module]] $N$ is equivalent to the identity

$$
  \Omega^2 N \simeq N \simeq \Sigma^2 N
  \,.
$$

This equivalence ought to be [[coherence|coherent]] to yield a $\mathbb{Z}/2\mathbb{Z}$ [[∞-action]] on the [[(∞,1)-category of (∞,1)-modules]] $E Mod$ ([MO discussion](http://mathoverflow.net/q/46399/381)).

### Landweber exact functor theorem

There is an analogue of the [[Landweber exact functor theorem]] for [[even cohomology theory|even]] 2-[[periodic cohomology theories]], with [[MU]] replaced by [[MP]] ([Hovey-Strickland 99, theorem 2.8](#HoveyStrickland99), [Lurie lecture 18, prop. 11](#LurieLect18)).


## Examples

* [[KU]]

* [[MP]]

* [[elliptic cohomology]]

* [[Morava E-theory]]


## Related entries

* [[Bott periodicity]]

* [[periodic ring spectrum]]

* [[A Survey of Elliptic Cohomology - cohomology theories]]

## References

The concept of even 2-periodic multiplicative cohomology theories originates with

* {#AndoHopkinsStrickland} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], _Elliptic spectra, the Witten genus, and the theorem of the cube_, Inventiones Mathematicae, 146:595&#8211;687, 2001, DOI 10.1007/s002220100175

The analogue of the [[Landweber exact functor theorem]] for even 2-periodic cohomology is discussed in

* {#HoveyStrickland99} [[Mark Hovey]], [[Neil Strickland]], theorem 2.8 of _Morava K-theories and localisation_ Mem. Amer. Math. Soc., 139(666):viii+100, 1999.

* [[Jacob Lurie]], _[[Chromatic Homotopy Theory]]_, Lecture series 2010 , Lecture 18 _Even periodic cohomology theories_ ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture18.pdf))

Review includes

* section 5.1 by [[Markus Land]] in these "TMF seminar" notes: [pdf](https://math.berkeley.edu/~aaron/livetex/TMF.pdf)

* [[Akhil Mathew]], Lennart Meier, section 2.1 of _Affineness and chromatic homotopy theory_, J. Topol. 8 (2015), no. 2, 476--528 ([arXiv:1311.0514](https://arxiv.org/abs/1311.0514))

[[!redirects periodic cohomology theories]]

[[!redirects even periodic cohomology theory]]
[[!redirects even periodic cohomology theories]]
