
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

What is called _$p$-adic string theory_ is the study of a variant of [[scattering amplitudes]] in [[string theory]] (hence [[string scattering amplitudes]]) where the [[worldsheet]] of the [[string]] is regarded not as a [[Riemann surface]] but as an object in [[p-adic geometry]].

### Open string amplitudes

The original observation is that of ([Volovich 87](#Volovich87), reviewed in [VVZ 95, section XIV](#VVZ95)) that the [[integral]] expression for the [[Veneziano amplitude]] of the [[open string|open]] [[bosonic string]] naturally generalizes from an integral over the [[real numbers]] (which in this case parameterize the [[boundary]] of the [[open string]] [[worldsheet]]) to the [[p-adic numbers]] by _[[adelic integration]]_.

The standard [[Veneziano amplitude]] has the expression

$$
  \int_{\mathbb{R}}
  {\vert x\vert}^{a-1}
  \cdot
  {\vert 1-x\vert}^{b-1}
  d x
$$

where the [[norm]] involved is the usual [[absolute value]], and the proposed $p$-adic version is hence

$$
  \int_{\mathbb{Q}_p}
  {\vert x\vert}_p^{a-1}
  \cdot
  {\vert 1-x\vert}_p^{b-1}
  d x
$$

with the [[p-adic norm]] instead.


The main result here is ([Freund-Witten 87](#FreundWitten87)) that the ordinary [[Veneziano amplitude]] equals the inverse of the product of its $p$-adic versions, for all primes $p$, apparently a version of the [idelic product formula](group%20of%20ideles#ProductFormula).

With due regularization this result carries over to other [[string scattering amplitudes]], too. When forming these products one also speaks of _[[ring of adeles|adelic]] string theory_.

Since the [[Veneziano amplitude]] concerns the [[bosonic string]] [[tachyon]] [[state]], [[p-adic string theory]] has been discussed a lot in the context of [[tachyon condensation]] and [[Sen's conjecture]] ([Cottrell 02](#Cottrell02)).

Traditionally literature on $p$-adic string theory asserts that the generalization of this from the [[open string]] to the [[closed string]] remains unclear (e.g [CMZ 89, section 4](#CMZ89), [Cottrell 02, section 5](#Cottrell02)), since it is unclear which adic version of the [[complex numbers]] to use. However, in other parts of the literature adic versions of closed strings are common, this we discuss [below](#TopologicalWittenGenus).

### Closed string 1-loop vacuum amplitudes (topological Witten genus)
 {#TopologicalWittenGenus}

Generally, the development of string theory has shown that its [[worldsheet]] is usefully regarded as an object in [[algebraic geometry]] (see also at _[[number theory and physics]]_) and mathematically the generalization from [[algebraic varieties]] over the [[complex numbers]] to more general algebraic varieties (or [[schemes]]) is often natural, if not compelling. 

For instance when the [[Witten genus]] (essentially the [[partition function]] of the [[superstring]]) is refined to the [[string orientation of tmf]] then the [[elliptic curves]] over the [[complex numbers]] which serve as the [[torus|toroidal]] [[worldsheets]] over the [[complex numbers]] are generalized to [[elliptic curves]] over general [[rings]] and by the [[fracture theorems]] the computations in [[tmf]] in fact typically proceed (see [here](tmf#DecomopositionViaArithmeticSquares)) by decomposing the general problem into that of ellitpic curves over the [[rational numbers]] and over the [[p-adic integers]]. The result refines the [[Witten genus]]

$$
  \Omega^String_{\bullet} \longrightarrow MF_\bullet
$$

(being a [[ring]] [[homomorphism]]) from the [[String structure]] [[cobordism ring]] to that of [[modular forms]] to one of [[E-∞ rings]]

$$
  M String \longrightarrow tmf
$$

from the [[String structure]] [[Thom spectrum]] to [[tmf]]. Notice that $M String$ here classifies String-[[cobordism cohomology theory|cobordism]] and hence parameterizes ordinary (not $p$-adic) [[target space|target]] [[spacetime]] [[manifolds]], while $tmf$ on the right does regard the [[genus of a surface|genus]]-1 [[worldsheet]] as a general [[elliptic curve]], hence in particular possibly as an [elliptic curve over the p-adic integers](elliptic%20curve#OverpAdics).

## Related concepts

* The interesting aspects of $p$-adic string theory have led people to consider _[[p-adic physics]]_ more generally. But it remains noteworthy that in $p$-adic string theory it is exactly only the [[worldsheet]] which is regarded in [[p-adic geometry]], while for instance the [[complex numbers]] as they appear as [[coefficients]] of [[quantum physics]] are not replaced by $p$-adics.

* [[p-adic AdS-CFT]]

* [[number theory and physics]]

* [[p-adic geometry]]

* [[p-adic homotopy]]

* [[p-adic cohomology]]

## References

The original articles include

* [[Peter Freund]], Mark Olson, _Non-archimedean strings_, Physics Letters B 199,2 (1987) (<a href="https://doi.org/10.1016/0370-2693(87)91356-6">arXiv:10.1016/0370-2693(87)91356-6</a>)

* {#Volovich87} I. V. Volovich, _p-&#1040;&#1076;&#1080;&#1095;&#1077;&#1089;&#1082;&#1086;&#1077; &#1087;&#1088;&#1086;&#1089;&#1090;&#1088;&#1072;&#1085;&#1089;&#1090;&#1074;&#1086;-&#1074;&#1088;&#1077;&#1084;&#1103; &#1080; &#1090;&#1077;&#1086;&#1088;&#1080;&#1103; &#1089;&#1090;&#1088;&#1091;&#1085;_, &#1058;&#1052;&#1060;, 71:3 (1987)[free Rus. pdf](http://www.mathnet.ru/links/704079ec1d28d91ba6eb6d492359b387/tmf4962.pdf); transl. _$p$-adic space-time and string theory_, Theor. Math. Phys. __71__, 574&#8211;576 (1987), [eng doi](http://dx.doi.org/10.1007/BF01017088), [nonfree Eng. pdf](http://www.springerlink.com/content/k514t553607324n0/fulltext.pdf)

The early history of the subject is recalled in

* Paul H. Frampton, _Particle Theory at Chicago in Late Sixties and p-Adic Strings_ ([arXiv:2001.10915](https://arxiv.org/abs/2001.10915))


That the ordinary [[Veneziano amplitude]] is the inverse product of all its $p$-adic versions is due to

* {#FreundWitten87} [[Peter Freund]], [[Edward Witten]], _Adelic string amplitudes_, Phys. Lett. B 199, 191 (1987). ([web record](http://adsabs.harvard.edu/abs/1987PhLB..199..191F))

also

* Lee Brekke,  [[Peter Freund]],  Mark Olson, [[Edward Witten]], _Non archimedean  string dynamics_, Nucl. Phys. B302, 3 (1988) (<a href="https://doi.org/10.1016/0550-3213(88)90207-6">arXiv:10.1016/0550-3213(88)90207-6</a>)

A detailed discussion of $p$-adic open [[string scattering amplitudes]] is in 

* {#CMZ89} L. Chekhov, A. Mironov, A. Zabrodin, _Multiloop calculations in $p$-adic String theory and Bruhat-Tits Trees_, Comm. Math. Phys. 125, 675-711 (1989) ([Euclid](http://projecteuclid.org/euclid.cmp/1104179635))

A review of this is in 

* Lee Brekke and [[Peter Freund]], _$p$-Adic numbers in physics_, Phys. Rep. 233, 1 (1993) ([web record](http://adsabs.harvard.edu/abs/1993PhR...233....1B))

and with an eye towards [[AdS-CFT duality]] in 

* [[Peter Freund]], _$p$-adic Strings Then and Now_ ([arXiv:1711.00523](https://arxiv.org/abs/1711.00523))

Suggestion that the [[disk]] [[worldsheet]] of the [[open string|open]] [[p-adic string]] is to be identified with the [[Bruhat-Tits tree]] $T_p$:

* [[Anton Zabrodin]], _Non-Archimedean strings and Bruhat-Tits trees_, Comm. Math. Phys.
Volume 123, Number 3 (1989), 463-483 ([euclid.cmp/1104178891](https://projecteuclid.org/euclid.cmp/1104178891))


Discussion of [[tachyon condensation]] in $p$-adic string theory includes

* {#Cottrell02} William Cottrell, _$p$-adic Strings and Tachyon Condensation_, 2002 ([pdf](http://jfi.uchicago.edu/~tten/teaching/Phys.291/Cottrell_Freund_2002.pdf))

See also

* {#BGZ16} Miriam Bocardo-Gaspar, H. García-Compeán, W. A. Zúñiga-Galindo, _Regularization of p-adic String Amplitudes, and Multivariate Local Zeta Functions_ ([arXiv:1611.03807](https://arxiv.org/abs/1611.03807))


Relation to [[gravity]] and the zeros of the [[Riemann zeta function]] (hence the [[Riemann hypothesis]]):

* {#HuangStoicaYau19} [[An Huang]], [[Bogdan Stoica]], [[Shing-Tung Yau]], _General relativity from $p$-adic strings_ ([arXiv:1901.02013](https://arxiv.org/abs/1901.02013), [spire:1712659](http://inspirehep.net/record/1712659/))

Discussion of [[BTZ black holes]]:

* [[Ingmar Saberi]], around Figure 4.3 of: _Knots, Trees, and Fields: Common Ground Between Physics and Mathematics_, 2016 ([doi:10.7907/Z9VX0DHZ](https://thesis.library.caltech.edu/9896), [pdf](https://thesis.library.caltech.edu/9896/1/Saberi_Ingmar_2016.pdf))


[[!redirects p-adic string theories]]

[[!redirects adelic string theory]]
[[!redirects adelic string theories]]

[[!redirects p-adic string]]
[[!redirects p-adic strings]]
