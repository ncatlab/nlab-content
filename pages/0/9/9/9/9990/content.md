
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _elliptic genus_  is a [[genus]] in [[elliptic cohomology]] ([Landweber-Ravenel-Stong 93](#LandweberRavenelStong93)). In analogy to how there is a "universal elliptic cohomology", namely [[tmf]], there is a universal elliptic genus -- the [[Witten genus]]. This arises as the [[large volume limit]] of the [[partition function]] of the [[superstring]] whose [[target space]] is the given [[manifold]].

## Definition
 {#Definition}

The original definition of elliptic genus is due to ([Ochanine 87](#Ochanine87)) (see the review ([Ochanine 09](#Ochanine09))) and says that an _[[genus]]_ of [[orientation|oriented]] manifolds is called an elliptic genus if it vanishes on manifolds which are [[projective spaces]] of the form $\mathbb{C}P(\xi)$ for $\xi$ an even-dimensional [[complex vector bundle]] over an [[orientation|oriented]] [[closed manifold]].

The terminomology _elliptic_ for this was motivated by the central theorem of ([Ochanine 87](#Ochanine87)) which says that every genus $\phi$ satisfying this condition has a [logarithm](genus#LogarithmAndCharacteristicSeries) $log_\phi$ of the form

$$
  log_\phi(u) = \int_{0^u} (1- 2 \delta t^2+  \epsilon t^4)^{-1/2}
$$

for some constants $\delta, \epsilon$. Hence in for non-degenrate choices of parameters ($\delta^2 \neq \epsilon$ and $\epsilon \neq 0$) in the square root this is the expansion at 0 of an elliptic function.

## Examples

### Degenerate case: Signature genus

The degenerate case with parameters $\delta = \epsilon = 1$ (as [above](#Definition)) is the [[signature genus]].

### Degenerate case: $\hat A$-genus

The degenerate case with parameters $\delta = - \frac{1}{8}$ and $\epsilon = 0$ (as [above](#Definition)) is the [[A-hat genus]].

### Universal case: Witten genus

Given an elliptic genus with non-degenerate parameters $\delta, \epsilon \in \mathbb{C}$ (as [above](#Definition)), the [[Jacobi quartic]] [[Riemann surface]] which is given by the [[equation]]

$$
  Y^2 = X^4 - 2 \delta X^2 + \epsilon
$$

is naturally parameterized by the [[upper half plane]]. Under this identification obe may think of $\epsilon$ and $\delta$ as functions of moduli of [[elliptic curves]] and concretely as [[modular forms]] for the [[subgroup]] $\Gamma_0(2)$ of that of M&#246;bius transformations.

Viewed this way the collection of all elliptic genera provides a single [[genus]] with [[coefficients]] in this ring $MF_\bullet(\Gamma_0(2))$ of [[modular forms]] 

$$
  w \colon \Omega^{SO}_\bullet \longrightarrow MF_\bullet(\Gamma_0(2))
$$

(such that postcomposition with evaluation on any elliptic curve parameterized by the given value of $\delta$ and $\epsilon$ produces the corrponding elliptic genus).

This "universal" elliptic genus is the _[[Witten genus]]_.

## Properties

### Relation to partition functions of superstring

The [[partition function]] of a [[type II superstring]] as a function depending on the [[modulus]] of the [[worldsheet]] [[elliptic curve]] yields an elliptic genus ([Witten 87](#Witten87)). (The analog for the [[heterotic string]] is hence called the _[[Witten genus]]_ with values in the "universal elliptic cohomology" theory, [[tmf]]).

For equivariant/gauged string [[sigma-models]] the elliptic genus should take values in [[equivariant elliptic cohomology]], see at _[gauged WZW mode -- Partition function in elliptic cohomology](gauged+WZW+model#PartitionFunctionInEllipticCohomology)_.


## Related concepts

* [[elliptic cohomology]]

* [[Witten genus]]

* [[equivariant elliptic genus]]

[[!include genera and partition functions - table]]


## References

The notion of elliptic genus was introduced in

* {#Ochanine87} [[Serge Ochanine]], _Sur les genres multiplicatifs definis par des integrales elliptiques_, Topology, Vol. 26, No. 2, 1987 ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Mult-genre-Ochanine.pdf))

The relation of this to [[elliptic cohomology]] was understood in

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et al (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))

The interpretation of the elliptic genus/[[Witten genus]] as the [[partition function]] of the [[type II superstring]]/[[heterotic string]] is due to 

* [[Edward Witten]], _Elliptic genera and quantum field theory_, Comm. Math. Phys. Volume 109, Number 4 (1987), 525-536.  ([EUCLID](http://projecteuclid.org/euclid.cmp/1104117076))
  {#Witten87}

A quick review is in

* {#Ochanine09} [[Serge Ochanine]], _What is... an elliptic genus_?, Notices of the AMS, volume 56, number 6  (2009) ([pdf](http://www.ams.org/notices/200906/rtx090600720p.pdf))

Similar elliptic genera of $N=2$ $d = 2$ field theories and [[Landau-Ginzburg models]] are discussed in 

* [[Edward Witten]], _On the Landau-Ginzburg Description of $N=2$ Minimal Models_, Int.J.Mod.Phys.A9:4783-4800,1994 ([arXiv:hep-th/9304026](http://arxiv.org/abs/hep-th/9304026))

* Toshiya Kawai, Yasuhiko Yamada, Sung-Kil Yang, _Elliptic Genera and $N=2$ Superconformal Field Theory_ ([arXiv:hep-th/9306096](http://arxiv.org/abs/hep-th/9306096))

More on this is in 

* Sujay K. Ashok, Jan Troost, _A Twisted Non-compact Elliptic Genus_, JHEP 1103:067,2011 ([arXiv:1101.1059](http://arxiv.org/abs/1101.1059))

[[!redirects elliptic genera]]