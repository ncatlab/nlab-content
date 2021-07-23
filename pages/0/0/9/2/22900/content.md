
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
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

There are two notions of [[homomorphism]] of [[L-∞ algebras|$L_\infty$-algebras]], one a special case of the other, depending on the [[homotopy theory|homotopy theoretic]] perspective:

If an [[L-∞ algebra|$L_\infty$]]-algebra $\mathfrak{g} = (V_\bullet, [\cdots])$ is regarded as a [[chain complex]]  $V_\bullet$ equipped with higher-[[arity|ary]]-bracket operations $[\cdots]$, then a homomorphism $\mathfrak{g} \xrightarrow{\;\;} \mathfrak{g}'$ is a [[chain map]] $V_\bullet \xrightarrow{\;\;} V'_\bullet$ which is compatible with the bracket operations.

However, even when so regarded, [[L-∞ algebras]] are [[objects]] of a [[homotopical category]], in fact of the [[category of fibrant objects]] of a [[model structure for L-∞ algebras|model structure for $L_\infty$-algebras]], so that the homotopy-correct morphisms out of $\mathfrak{g}$ are those out of a [[cofibrant resolution]] $\varnothing \xhookrightarrow{\;} \widehat {\mathfrak{g}} \xrightarrow{ \in \mathrm{W} } \mathfrak{g}$, hence are [[zig-zags]] of naive morphisms, as above, of the form $\mathfrak{g} \xleftarrow{\in \mathrm{W}} \widehat {\mathfrak{g}} \xrightarrow{\;\;\;} \mathfrak{g}'$.

But such poperly resolved morphisms are equivalently just the evident homomorphism of the associated [[Chevalley-Eilenberg algebra|Chevalley-Eilenberg]] [[dg-coalgebras]] $CE_\bullet(-)$ ([here](L-infinity-algebra#ReformulationInSemifreeDgCoalgebra)), 
[[formal duality|dually]] of the [[Chevalley-Eilenberg algebra|CE]]-[[dg-algebras]] $CE^\bullet(-)$ ([here](L-infinity-algebra#ReformulationInTermsOfSemifreeDGAlgebra)):

$$
  CE_\bullet(\mathfrak{g}) \xrightarrow{\;\;\;\;} CE_\bullet(\mathfrak{g}')
  \,,
  \;\;\;\;\;\;\;\;
  CE^\bullet(\mathfrak{g}) \xleftarrow{\;\;\;\;} CE^\bullet(\mathfrak{g}')
  \,.
$$

These homotopy-correct homomorphisms of $L_\infty$-algebras are known under a variety of different names, including:

* "strong homotopy maps", abbreviated: "sh maps" 

  (Stasheff following [Sugawara 60, Sec. 2](#Sugawara60), see also [Merkulov 02, 2.11](#Merkulov02)),

* "weak maps" 

  ([Lada & Markl 1994, Rem. 5.3](#LadaMarkl94)),

* "$L_\infty$-morphisms" 
   
  ([Kontsevich 1997, p. 12](#Kontsevich97))


## References

* {#LadaMarkl94} [[Tom Lada]], [[Martin Markl]], Rem. 5.3 of: _Strongly homotopy Lie algebras_, Communications in Algebra Volume 23, Issue 6, (1995) ([arXiv:hep-th/9406095](http://arxiv.org/abs/hep-th/9406095))

* {#Kontsevich97} [[Maxim Kontsevich]], *Deformation quantization of Poisson manifolds, I*,  Lett. Math. Phys. **66** (2003) 157-216 ([arXiv:q-alg/9709040](https://arxiv.org/abs/q-alg/9709040), [doi:10.1023/B:MATH.0000027508.00421.bf](https://doi.org/10.1023/B:MATH.0000027508.00421.bf))

* {#Merkulov02} [[Sergei A. Merkulov]], *Operads, deformation theory and $F$-manifolds* ([arXiv:math/0210478](https://arxiv.org/abs/math/0210478))

The terminology "strong homotopy" for the homotopy-coherent morphisms was originally borrowed from:

* {#Sugawara60} [[Masahiro Sugawara]], *On the homotopy-commutativity of groups and loop spaces*, Mem. College Sci. Univ. Kyoto Ser. A Math. 33(2): 257-269 (1960) ([DOI:10.1215/kjm/1250775911](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-33/issue-2/On-the-homotopy-commutativity-of-groups-and-loop-spaces/10.1215/kjm/1250775911.full))



[[!redirects homomorphisms of L-∞ algebras]]

[[!redirects homomorphism of L-infinity algebras]]
[[!redirects homomorphisms of L-infinity algebras]]

[[!redirects morphism of L-∞ algebras]]
[[!redirects morphisms of L-∞ algebras]]

[[!redirects morphism of L-infinity algebras]]
[[!redirects morphisms of L-infinity algebras]]

[[!redirects sh map]]
[[!redirects sh maps]]
[[!redirects sh-map]]
[[!redirects sh-maps]]

[[!redirects strong homotopy map]]
[[!redirects strong homotopy maps]]

[[!redirects weak map]]
[[!redirects weak maps]]
