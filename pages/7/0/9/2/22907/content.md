
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[homotopy theory]] of [[L-infinity algebra|$L_\infty$-algebras]] happens to be equivalent to that of [[dg-Lie algebras]] (over any [[ground field]] of [[characteristic zero]]). In fact, [[dg-Lie algebras]], being [[chain complexes]] equipped with a binary bracket, manifestly form the [[full subcategory]] of the [[1-category]] of [[L-infinity algebra|$L_\infty$-algebras]] on those whose $k$-ary brackets vanish for all $k \geq 3$,

\[
  \label{InclusionOfdgLieAlgebrasIntoLInfinityAlgebras}
  dgLieAlgebras
  \xhookrightarrow{\;\;i\;\;}
  L_\infty Algebras
  \,,
  {\phantom{AAAA}}
  L_{\mathrm{W}} 
  \big(
    dgLieAlgebras
  \big)
  \underoverset
    {\simeq}
    {\;\;L_{\mathrm{W}}(i)\;\;}
    {\longrightarrow}
  L_{\mathrm{W}} 
  \big(
    L_\infty Algebras
  \big)
  \,
\]

and under [[simplicial localization]] $L_{\mathrm{W}}$ this inclusion 
is an [[equivalence of (∞,1)-categories]]. 

Conversely, this means that [[dg-Lie algebras]] are *[[strict ∞-category|strict]]* [[L-infinity algebra|$L_\infty$-algebras]] -- namely those whose [[Jacobi identity]] is satisfied strictly, not just up to [[coherence|coherent]] [[higher homotopies]] -- and that every [[L-infinity algebra|$L_\infty$-algebra]] may be *[[rectification|rectified]]* to a strict one.

When formulated in terms of [[operads]] this means that the canonical [[functor]] from the category of [[algebras over an operad|algebras over]] the [[Lie operad]] in [[chain complexes]] (which are the [[dg-Lie algebras]]) to that of [[algebras over an operad|algebras over]] any of its [[cofibrant resolutions]] (which are the [[L-infinity algebra|$L_\infty$-algebras]]) is, at least, a surjection on [[quasi-isomorphism]] [[equivalence classes|classes]]. In this form the statement appears in [Kriz and May 1995, p. 28](#KrizMay95).

This refines to an [[equivalence of (∞,1)-categories|equivalence of homotopy theories]] as follows:

* [[L-infinity algebra|$L_\infty$-algebras]] are the [[fibrant objects]] in the [[model structure on dg cocommutative coalgebras]] ([Pridham 10](#Pridham10), [this Prop. ](model+structure+for+L-infinity+algebras#LInfinityAlgebraIsFibrantObjectIndgFormalSpace));

* [[dg-Lie algebras]] are [[fibrant objects]] in the [[model structure on dg-Lie algebras]] (trivially so)

and the inclusion (eq:InclusionOfdgLieAlgebrasIntoLInfinityAlgebras) of the latter [[category of fibrant objects]] into the former extends to a [[right Quillen functor]] with [[left adjoint]] being [[rectification]] ([this Prop.](model+structure+for+L-infinity+algebras#LeftAdjointFromDgCoAlgToDgAlg)) and which constitutes a [[Quillen equivalence]] ([Hinich 97](#Hinich97), [this Prop.](model+structure+for+L-infinity+algebras#QuillenEquivalenceBetweendgLieAnddgCoCAlg)).

## Related entries

* [[model structure for L-infinity algebras|model structure for $L_\infty$-algebras]]

* [[rectification]]

* [[rational homotopy theory]]

## References

* {#Quillen69} [[Dan Quillen]], _Rational homotopy theory_, The Annals of Mathematics, Second Series, Vol. 90, No. 2 (Sep., 1969), pp. 205-295 ([jstor:1970725](http://www.jstor.org/stable/1970725), [pdf](http://www.math.northwestern.edu/~konter/gtrs/rational.pdf))

* {#KrizMay95} [[Igor Kriz]], [[Peter May]], p. 28 of: _Operads, algebras, modules and motives_, Ast&#233;risque __233__, Soci&#233;t&#233; Math&#233;matique de France (1995) ([pdf](http://www.math.uchicago.edu/~may/PAPERS/kmbooklatex.pdf), [numdam:AST_1995__233__1_0](http://www.numdam.org/item/?id=AST_1995__233__1_0))

* {#Pridham10} [[Jonathan Pridham]], _Unifying derived deformation theories_, Adv. Math. 224 (2010), no.3, 772-826 ([arXiv:0705.0344](http://arxiv.org/abs/0705.0344))

* {#Hinich97} [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_, Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), Erratum: [arXiv:math/0309453](http://arxiv.org/abs/math/0309453))


[[!redirects relation between L-∞ algebras and dg-Lie algebras]]

[[!redirects relation between dg-Lie algebras and L-infinity algebras]]
[[!redirects relation between dg-Lie algebras and L-∞ algebras]]
