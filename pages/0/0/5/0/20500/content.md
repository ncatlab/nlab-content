
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An expression for [[Hopf invariants]] in terms of [[secondary characteristic classes]] induced from the [[intersection pairing]], also known as _[[functional cup products]]_ ([Steenrod 49](#Steenrod49)) or _[[homotopy periods]]_ ([Sinha-Walter 13](#SinhaWalter13)).

The original expression due to [Whitehead 47](#Whitehead47) (see [Bott-Tu 82, Prop. 17.22](#BottTu82)) is in terms of [[smooth functions]] to an [[n-sphere]] (in which case the [[wedge product]]/[[cup product]] of the [[pullback of differential forms|pullback]] of the [[volume form]] with itself vanishes identically).

More generally the homotopy Whitehead formula applies to general [[cocycles]] in [[cohomotopy]]. Its existence was suggested in [Haefliger 78, p. 17](#Haefliger78), worked out for the case of maps from the [[3-sphere]] to the [[2-sphere]] in [Griffiths & Morgan 81, Section 14.5](#GriffithsMorgan13) and stated generally but without proof in [Sinha-Walter 13, Example 1.9](#SinhaWalter13). A transparent proof of the general expression via lifts in [[cohomotopy]] through [[Hopf fibrations]] is in [FSS 19](#FSS19), relating the expression to the [[Hopf-Wess-Zumino term]] of the [[M5-brane]].

## Statement

### The base case
 {#TheBaseCase}

Consider a [[smooth function]] $f \,\colon\, S^3 \xrightarrow{\;} S^2$. Write $n \in \mathbb{N}$ for its [[Hopf invariant]], hence for the element in the [[homotopy group of spheres]] $\pi_3(S^2) \,\simeq\, \mathbb{Z}$ that is represented by (the [[underlying]] [[continuous function]] of) $f$.

Write $F_2 \coloneqq dvol_{S^2} \in \Omega^2_{dR}(S^2)$ for the unit [[volume form]] of the [[2-sphere]], or any other [[differential 2-form|2-form]] with unit [[integration of differential forms|integral]]:

$$
  \textstyle{\int_{S^2}} \, F_2 \;=\; 1
  \,.
$$

Observe that the [[pullback of differential forms|pullback]] of $F_2$ along $f$ admits a [[de Rham cohomology|de Rham]] [[coboundary]] $A_1 \in \Omega^1_{\mathrm{dR}}(S^3)$, since the [[de Rham cohomology]] of the [[3-sphere]] vanishes in degree 2, $H^2_{dR}(S^3) \,\simeq\, 0$:
$$
  \mathrm{d}\, A_1 \;=\; f^\ast F_2
  \,.
$$


\begin{proposition}

For any such choice of $A_1$, the [[integration of differential forms|integral]]

$$
  \textstyle{\int_{S^3}} \, A_1 \wedge f^\ast F_2
  \;=\;
  n
$$

computes the [[Hopf invariant]].

\end{proposition}

This is the original statement of [Whitehead 1947](#Whitehead47). In the above modernized form it is stated, e.g., in [Bott & Tu 1982, p 228](#BottTu82) and in [Griffiths & Morgan 2013 p 134](#GriffithsMorgan13).




## Related concepts

* [[functional cup product]]

## References


* {#Whitehead47} [[J. H. C. Whitehead]], _An expression of Hopf's invariant as an integral_, Proc. Nat. Acad. Sci. USA **33** (1947) 117–123 &lbrack;[jstor:87688](https://www.jstor.org/stable/87688)&rbrack;

* {#Steenrod49} [[Norman Steenrod]]: _Cohomology Invariants of Mappings_, Annals of Mathematics Second Series, **50** 4 (1949) 954-988 &lbrack;[jstor:1969589 ](https://www.jstor.org/stable/1969589)&rbrack;

* [[Hassler Whitney]], Section 31 in: *Geometric Integration Theory* (1957) &lbrack;[pup:3151](https://press.princeton.edu/titles/3151.html)&rbrack;

* {#Haefliger78} [[André Haefliger]], p. 3 of: _Whitehead products and differential forms_, in: P. A. Schweitzer (ed.), *Differential Topology, Foliations and Gelfand-Fuks Cohomology*, Lecture Notes in Mathematics **652**, Springer (1978) &lbrack;[doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500)&rbrack;

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Prop. 17.22 in _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics **82**, Springer (1982) &lbrack;[doi:10.1007/978-1-4757-3951-0](https://link.springer.com/book/10.1007/978-1-4757-3951-0)&rbrack;

* Lee Rudolph: _Whitehead's Integral Formula, Isolated Critical Points, and the Enhancement of the Milnor Number_, Pure and Applied Mathematics Quarterly **6** 2 (2010) &lbrack;[arXiv:0912.4974](https://arxiv.org/abs/0912.4974)&rbrack;

* {#GriffithsMorgan13} [[Phillip Griffiths]], [[John Morgan]], Section 14.5 of: _Rational Homotopy Theory and Differential Forms_,  Progress in Mathematics **16**, Birkhauser (1981, 2013) &lbrack;[doi:10.1007/978-1-4614-8468-4](https://doi.org/10.1007/978-1-4614-8468-4)&rbrack;

* {#SinhaWalter13} [[Dev Sinha]], [[Ben Walter]]: _Lie coalgebras and rational homotopy theory II: Hopf invariants_, Trans. Amer. Math. Soc. **365** (2013) 861-883  &lbrack;[arXiv:0809.5084](https://arxiv.org/abs/0809.5084), [doi:10.1090/S0002-9947-2012-05654-6](https://doi.org/10.1090/S0002-9947-2012-05654-6)&rbrack;

* [[Felix Wierstra]], *Hopf Invariants in Real and Rational Homotopy Theory* (2017) &lbrack;[diva:146246](http://urn.kb.se/resolve?urn=urn:nbn:se:su:diva-146246), [pdf](https://www.diva-portal.org/smash/get/diva2:1136442/FULLTEXT02.pdf)&rbrack;

* {#FSS19} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], pp. 18 of: _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_, Comm. Math. Phys. **384** (2021) 403-432 &lbrack;[arXiv:1906.07417](https://arxiv.org/abs/1906.07417), [doi:10.1007/s00220-021-03951-0](https://doi.org/10.1007/s00220-021-03951-0)&rbrack;


[[!redirects Whitehead integral formulas]]

[[!redirects Whitehead's integral formula]]
[[!redirects Whitehead's integral formulas]]

[[!redirects homotopy Whitehead integral formula]]
[[!redirects homotopy Whitehead integral formulas]]

[[!redirects homotopy Whitehead's integral formula]]
[[!redirects homotopy Whitehead's integral formulas]]




[[!redirects Whitehead integral]
[[!redirects Whitehead integrals]]

[[!redirects Whitehead's integral]]
[[!redirects Whitehead's integrals]]

[[!redirects homotopy Whitehead integral]]
[[!redirects homotopy Whitehead integrals]]

[[!redirects homotopy Whitehead's integral]]
[[!redirects homotopy Whitehead's integrals]]



