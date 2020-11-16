
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
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

for some constants $\delta, \epsilon$. Hence for non-degenerate choices of parameters ($\delta^2 \neq \epsilon$ and $\epsilon \neq 0$) in the square root this is the expansion at 0 of an elliptic function. 

So the logarithm here is an [[elliptic integral]] and that was the original reason for the term "elliptic genus".

## Examples

### Degenerate case: Signature genus

The degenerate case with parameters $\delta = \epsilon = 1$ (as [above](#Definition)) is the [[signature genus]].

### Degenerate case: $\hat A$-genus

The degenerate case with parameters $\delta = - \frac{1}{8}$ and $\epsilon = 0$ (as [above](#Definition)) is the [[A-hat genus]].

### Universal case: Witten genus

Given an elliptic genus with non-degenerate parameters $\delta, \epsilon \in \mathbb{C}$ (as [above](#Definition), see also at _[[j-invariant]]_), the [[Jacobi quartic]] [[Riemann surface]] which is given by the [[equation]]

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

### Integrality on Spin-manifolds

On [[manifolds]] with [[spin structure]] the elliptic genus
takes values in integral series $\mathbb{Z}[ [q] ]$.

([Chudnovsky-Chudnovsky 88](#ChudnovskyChudnovsky88), [Landweber 88, section 5](#Landweber88) [Kreck-Stolz 93](#KreckStolz93), [Hovey 91](#Hovey91))

### Relation to partition functions of superstring

The [[partition function]] of a [[type II superstring]] as a function depending on the [[modulus]] of the [[worldsheet]] [[elliptic curve]] yields an elliptic genus ([Witten 87](#Witten87)). (The analog for the [[heterotic string]] is hence called the _[[Witten genus]]_ with values in the "universal elliptic cohomology" theory, [[tmf]]).

For equivariant/gauged string [[sigma-models]] the elliptic genus should take values in [[equivariant elliptic cohomology]], see at _[gauged WZW mode -- Partition function in elliptic cohomology](gauged+WZW+model#PartitionFunctionInEllipticCohomology)_.

### Rigidity theorem

See _[[rigidity theorem for elliptic genera]]_.


## Related concepts

* [[elliptic cohomology]]

* [[spin orientation of Ochanine elliptic cohomology]]

* [[Witten genus]], [[string orientation of tmf]]

* [[equivariant elliptic genus]]

[[!include genera and partition functions - table]]


## References





### As a mathematical genus

The notion of elliptic genus was introduced in

* {#Ochanine87} [[Serge Ochanine]], _Sur les genres multiplicatifs definis par des integrales elliptiques_, Topology, Vol. 26, No. 2, 1987 ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Mult-genre-Ochanine.pdf))

A quick review is in

* {#Ochanine09} [[Serge Ochanine]], _What is... an elliptic genus_?, Notices of the AMS, volume 56, number 6  (2009) ([pdf](http://www.ams.org/notices/200906/rtx090600720p.pdf))

More review (and in the context of the lift to the [[spin orientation of Tate K-theory]]) is in  

* {#KreckStolz93} [[Matthias Kreck]], [[Stefan Stolz]], section 2 of _$HP^2$-bundles and elliptic homology_, Acta Math, 171 (1993) 231-261 ([[KreckStolzElliptic.pdf:file]])

* {#Thomas02} [[Charles Thomas]], section 1 of _Elliptic cohomology_, Kluwer Academic, 2002 

The relation of this to [[elliptic cohomology]] was understood in

* {#Landweber88} [[Peter Landweber]], _Elliptic genera: An introductory overview_ In: P. Landweber (eds.) _Elliptic Curves and Modular Forms in Algebraic Topology_, Lecture Notes in Mathematics, vol 1326. Springer  (1988) ([doi:10.1007/BFb0078036](https://doi.org/10.1007/BFb0078036))

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et al (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))

The integrality of the elliptic genus and elliptic homology on Spin-manifolds is due to

* {#ChudnovskyChudnovsky88} D.V. Chudnovsky, G.V. Chudnovsky, _Elliptic modular functions and elliptic genera_, Topology, Volume 27, Issue 2, 1988, Pages 163&#8211;170

([Kreck-Stolz 93](#KreckStolz93))


* {#Hovey91} [[Mark Hovey]], _Spin Bordism and Elliptic Homology_ (1991) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.3277))

Refinement of the Ochanine genus to a homomorphism of [[ring spectra]] (in analogy to the lift of the [[Witten genus]] to the [[string orientation of tmf]]) is considered in

* [[Dylan Wilson]], _Orientations and Topological Modular Forms with Level Structure_ ([arXiv:1507.05116](http://arxiv.org/abs/1507.05116))



### As CFT partition function


The interpretation of the elliptic genus/[[Witten genus]] as the [[partition function]] of a [[2d SCFT]] or [[Landau-Ginzburg model]] and especially of the [[type II superstring]]/[[heterotic string]] [[worldsheet]] theory:

* {#Witten87} [[Edward Witten]], _Elliptic genera and quantum field theory_, Comm. Math. Phys. Volume 109, Number 4 (1987), 525-536.  ([euclid:cmp/1104117076](http://projecteuclid.org/euclid.cmp/1104117076))

* [[Edward Witten]], _On the Landau-Ginzburg Description of $N=2$ Minimal Models_, Int.J. Mod. Phys.A9:4783-4800,1994 ([arXiv:hep-th/9304026](http://arxiv.org/abs/hep-th/9304026))

* [[Toshiya Kawai]], [[Yasuhiko Yamada]], Sung-Kil Yang, _Elliptic Genera and $N=2$ Superconformal Field Theory_, Nucl. Phys. B414:191-212, 1994
([arXiv:hep-th/9306096](http://arxiv.org/abs/hep-th/9306096), <a href="https://doi.org/10.1016/0550-3213(94)90428-6">doi:10.1016/0550-3213(94)90428-6</a>)


Review in:


* [[Katrin Wendland]], Section 2.4 in: _Snapshots of Conformal Field Theory_, in:
Mathematical Aspects of Quantum Field Theories. Mathematical Physics Studies. Springer 2015 
([arXiv:1404.3108](http://de.arxiv.org/abs/1404.3108), [doi:10.1007/978-3-319-09949-1_4](https://doi.org/10.1007/978-3-319-09949-1_4))

See also:

* Sujay K. Ashok, Jan Troost, _A Twisted Non-compact Elliptic Genus_, JHEP 1103:067,2011 ([arXiv:1101.1059](http://arxiv.org/abs/1101.1059))

### As fiber integral in elliptic cohomology

The [[elliptic genus]]/[[Witten genus]] as [[fiber integration]] in [[elliptic cohomology]]:

* [[Haynes Miller]], _The elliptic character and the Witten genus_, in: [[Mark Mahowald]], [[Stewart Priddy]] (eds.), _Algebraic topology_ (Evanston, IL, 1988), Contemp. Math. 96, Amer. Math. Soc., Providence, RI (1989) 281&#8211;289 ([pdf](http://dedekind.mit.edu/~hrm/papers/ell-char.pdf), [[MillerEllipticGenus.pdf:file]], [doi:10.1090/conm/096](http://dx.doi.org/10.1090/conm/096))

* [[Ioanid Rosu]], _Equivariant Elliptic Cohomology and Rigidity_, American Journal of Mathematics 123 (2001), 647-677 ([arXiv:math/9912089](https://arxiv.org/abs/math/9912089))

* [[Matthew Ando]], Maria Basterra, _The Witten genus and equivariant elliptic cohomology_,
Math Z 240, 787–822 (2002).
([arXiv:math/0008192](https://arxiv.org/abs/math/0008192), [doi:10.1007/s002090100399](https://doi.org/10.1007/s002090100399))


### M5-brane elliptic genus

Discussion of the [[M5-brane]] [[partition function]] as an [[elliptic genus]] seen under an [[AGT correspondence]] ([[M5-brane elliptic genus]]):

A [[2d SCFT]] argued to describe the  [[KK-compactification]] of the [[M5-brane]] on a [[4-manifold]] (specifically: a [[complex surface]]) originates with

* [[Juan Maldacena]], [[Andrew Strominger]], [[Edward Witten]], _Black Hole Entropy in M-Theory_, JHEP 9712:002, 1997 ([arXiv:hep-th/9711053](https://arxiv.org/abs/hep-th/9711053))

Discussion of the resulting [[elliptic genus]] ([[2d SCFT]] [[partition function]]) originates with:

* [[Davide Gaiotto]], [[Andrew Strominger]], [[Xi Yin]], _The M5-Brane Elliptic Genus: Modularity and BPS States_, JHEP 0708:070, 2007 ([hep-th/0607010](https://arxiv.org/abs/hep-th/0607010))

* [[Davide Gaiotto]], [[Xi Yin]], _Examples of M5-Brane Elliptic Genera_, JHEP 0711:004, 2007 ([arXiv:hep-th/070](https://arxiv.org/abs/hep-th/070))

Further discussion in:

* Murad Alim, Babak Haghighat, Michael Hecht, Albrecht Klemm, Marco Rauch, Thomas Wotschke, _Wall-crossing holomorphic anomaly and mock modularity of multiple M5-branes_ ([arXiv:1012.1608](https://arxiv.org/abs/1012.1608))



* [[Sergei Gukov]], [[Du Pei]], [[Pavel Putrov]], [[Cumrun Vafa]], _4-manifolds and topological modular forms_ ([arXiv:1811.07884](https://arxiv.org/abs/1811.07884))



[[!redirects elliptic genera]]

[[!redirects Ochanine genus]]
[[!redirects Ochanine elliptic genus]]
