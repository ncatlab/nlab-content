
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The ordinary [[Chern character]] for [[K-theory]] sends K-classes to [[ordinary cohomology]] with real coefficients. Over a [[smooth manifold]] the [[de Rham theorem]] makes this equivalently take values in [[de Rham cohomology]]. 

The **twisted Chern character** analogously goes from [[twisted K-theory]] to [[twisted de Rham cohomology]].

## Details

### In terms of twisted curvature characteristic forms
 {#InTermsOfTwistedCurvatureCharacteristicForms}

For a degree-3 [[ordinary cohomology]]-class $\tau_3 \in \,H^3(X;, \mathbb{Z})\,$ (e.g. modeled as a [[bundle gerbe]]) on a [[compact topological space|compact]] [[smooth manifold]] $X$, a class in the $\tau_3$-[[twisted K-theory]] $KU^{\tau_3}(X)$ may be represented as a suitable [[Grothendieck group]]-[[equivalence class]] $[V_1,V_2]$ of a [[pair]] $V_1, V_2 \in TwVectBund^{\tau_3}(X)$ of [[complex vector bundles|complex]] [[twisted vector bundles]] (e.g. modeled as [[bundle gerbe modules]], possibly of infinite [[rank of a vector bundle|rank]]). 

Then for any lift of the twist $\tau_3$ [to](ordinary+differential+cohomology#CurvatureAndCharClass) a [[Deligne cohomology|Deligne cocycle]] $[h_0, A_1, B_2, H_3]_U$ (a [[connection on a bundle gerbe]]) with respect to some [[surjective submersion]] $p \colon U \twoheadrightarrow X$, hence in particular with a [[differential 2-form]] (the local [[B-field]])

\[
  \label{BFieldForTheTwist}
  B_2 
    \,\in\,
  \Omega^2(U)
  \,,
\]

one may make a choice of [[connections on twisted vector bundles]] $(\nabla_1, \nabla_2)$ on $(V_1, V_2)$, and this induces [[endomorphism ring]]-valued [[curvature 2-forms]] 

\[
  \label{TwistedCurvatureForms}
  F_i 
    \,\in\, 
  \Omega^2
  \big(
    U, 
    \,
    End(V_i)
  \big)
\]

on the cover. 

Now the twisted [[characteristic form]] (eq:TwistedCharacteristicFormOnCover) obtained as the [[trace]] (in the [[square matrix]]-[[coefficients]]) of the difference of the [[wedge product]]-[[exponential series]] of these two twisted [[curvature forms]] (eq:TwistedCurvatureForms), [[wedge product|wedged]] with the wedge-[[exponential series]] of the [[B-field]] (eq:BFieldForTheTwist)

\[
  \label{TwistedCharacteristicFormOnCover}
  \exp(B_2)
  \wedge
  tr
  \big(
    \exp(F_1) - \exp(F_2)
  \big)
  \;\;
  =
  p^\ast ch^{B_2}(\nabla_1, \nabla_2)
  \;\;
  \;\;\;
  \in
  \;
  \Omega^\bullet(U)
\]

turns out to

1. be well-defined, in that the [[traces]] all exist;

1. be the [[pullback of differential forms|pullback]] of an even-degree [[differential form]] on $X$

   $$
     ch^{B_2}(\nabla_1,\nabla_2)
     \;\;\;
     \in
     \;
     \Omega^{2\bullet}(X)
     \,,
   $$

1. which is closed in the $H_3$-[[twisted de Rham cohomology|twisted de Rham complex]] on $X$, in that 

   $$
     \big( d - H_3 \wedge \big) ch^{B_2}(\nabla_1, \nabla_2)
     \;=\; 
     0
     \,,
   $$

1. and whose [[twisted de Rham cohomology|twisted de Rham]] class

   \[
     \label{TwistedChernCharacterAsTwistedDeRhamClassOfTwistedCharClass}
     ch^{\tau_3}[V_1, V_2]
     \;\coloneqq\;
     \big[
       ch^{B_2}(\nabla_1, \nabla_2)
     \big]
     \;\;\;
     \in
     \;
     H^{3 + H_3}_{dR}(X)
   \]

   is independent of the choices ($B_2$, $\nabla_1$, $\nabla_2$) made.

([BCMMS 2002, Prop. 9.1](#BCMMS02))

This class (eq:TwistedChernCharacterAsTwistedDeRhamClassOfTwistedCharClass) is the *twisted Chern character* of the twisted K-theory class $[V_1, V_2]$ ([BCMMS 2002, p. 26](#BCMMS02)).

## Related concepts

* [[Chern character]]

* [[equivariant Chern character]]

* [[twisted equivariant Chern character]]

## References

* {#BCMMS02}  [[Peter Bouwknegt]], [[Alan Carey]], [[Varghese Mathai]], [[Michael Murray]], [[Danny Stevenson]], Section 6.3 in: _Twisted K-theory and K-theory of bundle gerbes_ ,  Commun Math Phys, 228 (2002) 17-49 ([arXiv:hep-th/0106194](http://arxiv.org/abs/hep-th/0106194), [doi:10.1007/s002200200646](https://doi.org/10.1007/s002200200646))
  

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], Section 2 of: _Twisted equivariant K-theory with complex coefficients_, Journal of Topology, Volume 1, Issue 1, 2007 ([arXiv:math/0206257](https://arxiv.org/abs/math/0206257), [doi:10.1112/jtopol/jtm001](https://doi.org/10.1112/jtopol/jtm001))


* [[Varghese Mathai]], [[Danny Stevenson]], _Chern character in twisted K-theory: equivariant and holomorphic cases_, Commun. Math. Phys. 236:161-186, 2003 ([arXiv:hep-th/0201010](https://arxiv.org/abs/hep-th/0201010))

* {#AtiyahSegal04} [[Michael Atiyah]], [[Graeme Segal]], Section 7 of: _Twisted K-theory_, Ukrainian Math. Bull. 1 (2004) ([arXiv:math/0407054](http://arxiv.org/abs/math/0407054), [journal page](http://iamm.su/en/journals/j879/?VID=10), [published pdf](http://iamm.su/upload/iblock/45e/t1-n3-287-330.pdf))

* [[Varghese Mathai]], [[Danny Stevenson]], Section 6 of: _On a generalized Connes-Hochschild-Kostant-Rosenberg theorem_, Advances in Mathematics, vol. 200 no. 2 (2006) 303-335 ([arXiv:math/0404329](https://arxiv.org/abs/math/0404329))

* [[Paul Bressler]], A. Gorokhovsky, R. Nest, [[Boris Tsygan]], _Chern Character for Twisted Complexes_. In: Kapranov M., Manin Y.I., Moree P., Kolyada S., Potyagailo L. (eds.) Geometry and Dynamics of Groups and Spaces. Progress in Mathematics, vol 265. Birkhäuser Basel (2007) ([doi:10.1007/978-3-7643-8608-5_5](https://doi.org/10.1007/978-3-7643-8608-5_5))

* [[Kiyonori Gomi]], [[Yuji Terashima]], Section 4 of: _Chern-Weil Construction for Twisted K-Theory_,  Commun. Math. Phys. 299, 225–254 (2010) ([doi:10.1007/s00220-010-1080-1](https://doi.org/10.1007/s00220-010-1080-1)) 

  (in terms of [[vectorial bundles]])

* [[Max Karoubi]], Section 8.3 of: _Twisted bundles and twisted K-theory_, in:  Guillermo Cortiñas (ed.) _Topics in Noncommutative Geometry_ ([arXiv:1012.2512](https://arxiv.org/abs/1012.2512), [ISBN:978-0-8218-6864-5](https://bookstore.ams.org/cmip-16))

In twisted [[orbifold K-theory]]:

* [[Jean-Louis Tu]], [[Ping Xu]], _Chern character for twisted K-theory of orbifolds_, Advances in Mathematics Volume 207, Issue 2, 20 December 2006, Pages 455-483 ([arXiv:math/0505267](https://arxiv.org/abs/math/0505267), [doi:10.1016/j.aim.2005.12.001](https://doi.org/10.1016/j.aim.2005.12.001))
