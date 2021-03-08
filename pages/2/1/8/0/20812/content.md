
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

In [[string theory]]/[[M-theory]], the _shifted C-field flux quantization condition_ is a [[charge quantization]]-condition on the [[supergravity C-field]] expected in [[M-theory]]. 

## For the magnetic $G_4$-flux

For the magnetic $G_4$-flux, the shifted flux quantization says that the [[real cohomology]] class of the [[flux density]] ([[field strength]]) [[differential 4-form]] $G_4 \in \Omega^4(X)$ on [[spacetime]] $X$ becomes integral after shifted by one quarter of the [[first Pontryagin class]], hence the condition that with the shifted 4-flux density defined as

\[
  \label{Shiftwed}
  \widetilde G_4 
  \;\coloneqq\;
  G_4 + \tfrac{1}{4}p_1(\nabla_{T X})
  \;\in\;
  \Omega^4(X)
\]

(for $\nabla_{T X}$ any [[affine connection]] on [[spacetime]], in particular the [[Levi-Civita connection]]) we have (using the [[de Rham theorem]] to translate from [[de Rham cohomology]] to [[real cohomology]]) that $\widetilde G_4$ represents an [[integral cohomology]]-class:

$$
  [\widetilde G_4]
  \;\in\;
  H^4(X, \mathbb{Z})
  \overset{H^4(X, \mathbb{Z}\hookrightarrow \mathbb{R})}{\longrightarrow}  
  H^4(X, \mathbb{R})
  \,.
$$


This condition was originally argued for in ([Witten 96a](#Witten96a), [Witten 96b](#Witten96b)) as a sufficient condition for ensuring that the [[prequantum line bundle]] for the [[7d Chern-Simons theory]] on an [[M5-brane]] [[worldvolume]] is divisible by 2.

Proposals for encoding this condition by a [[Wu class]]-shifted variant of [[generalized (Eilenberg-Steenrod) cohomology theory|stable]] [[ordinary differential cohomology]] were considered in [Hopkins-Singer 02](#HopkinsSinger02), [Diaconescu-Freed-Moore 03](#DiaconescuFreedMoore03), [FSS 12](#FSS12).

It turns out that the shifted flux quantization condition on the C-field is naturally implied ([FSS1 19b, Prop. 4.12](#FSS19b)) by the requirement that $G_4$ is the differential form datum underlying, via [[Sullivan model|Sullivan's theorem]], a [[cocycle]] in unstable [[J-homomorphism|J-]] [[twisted Cohomotopy]] in degree 4 ([[schreiber:Hypothesis H]]).


## For the electric $G_7$-flux
 {#ForElectricG7Flux}

In the presence of non-vanishing [[C-field]] [[flux]] $G_4$, the electric [[flux density]] of [[M2-branes]] is not $G_7 \coloneqq \star G_4$ alone, but receives corrections, first due to the quadratic [[C-field]] self-interaction in [[D=11 supergravity]], but then also due to the [[shifted C-field flux quantization]] expected in [[M-theory]]:

\linebreak

**The [[11d supergravity]] literature** states the corrected 7-flux to be the following combination, also known as the _[[Page charge]]_ (due to [Page 83 (8)](M2-brane#Page83), [Duff-Stelle 91 (43)](M2-brane#DuffStelle91), reviewed e.g. in [BLMP 13, p. 21](M2-brane#BaggerLambertMukhiPapageorgakis13)):



\[
  \label{FirstCorrectionToG7}
  \widetilde G'_7 
  \;\coloneqq\;
  G_7 + \tfrac{1}{2} C_3 \wedge G_4
  \,,
\]

where the second term subtracts the electric flux induced by the self-intersection of the [[field]], and also ensures that the full expression is a [[closed differential form]] if the naive [[11d supergravity]] [[equations of motion]] hold:

$$
  d \widetilde G_7
  \;=\;
  0
  \,.
$$

But in fact (eq:FirstCorrectionToG7) does not quite make general sense, for two reasons:

1. In general $G_4 = 0$ is not an admissible condition and is not the actual vanshing of the [[C-field]], due to the [[shifted C-field flux quantization]].

1. Even if $G_4$ happens to be intregrally quantizaed (if $\tfrac{1}{4}p_1$ is integral) the appearance of a globally defined [[C-field]] potential $C_3$ in (eq:FirstCorrectionToG7),means that the total [[flux]] actually does vanish after all.

\linebreak

**Charge-quantized $\widetilde G_7$-flux with [[shifted C-field flux quantization]]** ([FSS 19b, Prop. 4.3](#FSS19b), [FSS 19c, Section 4](#FSS19c))

Both of these issues are solved if the [[C-field]] is taken to be [[charge quantization|charge quantized]] in [[J-homomorphism|J-]][[twisted Cohomotopy]] ([[schreiber:Hypothesis H]]). This gives the corrected formula 

\[
  \label{FullCorrectionToG7}
  \widetilde G_7 
  \;\coloneqq\;
  h^\ast G_7 + \tfrac{1}{2} H_3 \wedge h^\ast \widetilde G_4
\]

where

<div style="float:right;margin:0 10px 10px 0;">
<a href="">
<img src="https://ncatlab.org/schreiber/files/6dWZFromHomotopyLifting.jpg" width="440" />
</a></div>

1. the expression lives on the [[homotopy pullback]] of the [[Sp(2)]]-[[parametrized homotopy theory|parametrized]] [[quaternionic Hopf fibration]] 

   $$
     h \coloneqq h_{\mathbb{H}}\sslash Sp(2)
   $$ 

   to [[spacetime]], along the [[twisted Cohomotopy]]-[[cocycle]] that represents the [[C-field]] under [[schreiber:Hypothesis H]];

1. $\widetilde G_4 \coloneqq h^\ast G_4 + \tfrac{1}{4}h^\ast p_1(\nabla)$ is the integral [[shifted C-field flux quantization|shifted C-field]] pulled back to that 3-[[spherical fibration]] over spacetime;

1. $d H_3 = h^\ast G_4 - \tfrac{1}{4}h^\ast p_1(\nabla)$ trivializes not the C-field itself, but its pullback, and not absolutely but relative to the background charge implied by [[shifted C-field flux quantization]].

With the corrected 7-flux in [[twisted Cohomotopy]] it becomes true that 

1. the integral of $G_7$ around the [[7-sphere]] linking a [[black brane|black]] [[M2-brane]] is always [[integer]] ([FSS 19c, Theorem 4.6](#FSS19c));

1. this integer satisfies the [[C-field tadpole cancellation condition]] ([FSS 19b, Section 4.6](#FSS19b)).



## Related concepts

* [[C-field tadpole cancellation]]

## References

### General

The suggestion originates in

* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. 22:1-13, 1997 ([arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122))

* {#Witten96b} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J. Geom. Phys. 22:103-133, 1997 ([arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234))

Proposals to model the condition by a [[Wu class]]-shifted variant of [[ordinary differential cohomology]] include

* {#HopkinsSinger02} [[Michael Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_  J. Differential Geom. Volume 70, Number 3 (2005), 329-452.  ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908))

* {#DiaconescuFreedMoore03} E. Diaconescu, [[Dan Freed]], [[Greg Moore]],  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in [[Haynes Miller]], [[Douglas Ravenel]] (eds.) _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))

* {#FreedMoore04} [[Dan Freed]], [[Greg Moore]], _Setting the [[quantum integrand]] of M-theory_, Communications in Mathematical Physics, Volume 263, Number 1, 89-132, ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135), [doi:10.1007/s00220-005-1482-7](https://doi.org/10.1007/s00220-005-1482-7))

* {#Moore04} [[Greg Moore]], _Anomalies, Gauss laws, and Page charges in M-theory_, Comptes Rendus Physique 6 (2005) 251-259 ([arXiv:hep-th/0409158](http://arxiv.org/abs/hep-th/0409158))

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics,  Volume 333, Issue 1 (2015), Page 117-151 ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455), [doi:10.1007/s00220-014-2228-1](http://link.springer.com/article/10.1007%2Fs00220-014-2228-1))

Suggestion that an actual [[E8]]-[[principal bundle]] on 11d spacetime plays a role here:

* D. Diaconescu, [[Gregory Moore]], [[Edward Witten]], _$E_8$ Gauge Theory, and a Derivation of K-Theory from M-Theory_, Adv. Theor. Math. Phys. 6:1031-1134, 2003 ([arXiv:hep-th/0005090](https://arxiv.org/abs/hep-th/0005090))

* [Diaconescu-Freed-Moore 03, Section 3](#DiaconescuFreedMoore03)

* Allan Adams, [[Jarah Evslin]], _The loop group of $E_8$ and K-theory from 11d_, JHEP 02 (2003) ([arXiv:hep-th/0203218](https://arxiv.org/abs/hep-th/0203218))

* [[Hisham Sati]], _$E_8$ Gauge Theory and Gerbes in String Theory_, Adv. Theor. Math. Phys. 14:1-39, 2010 ([arXiv:hep-th/0608190](https://arxiv.org/abs/hep-th/0608190))



The observation that the condition is implied by [[supergravity C-field|C-field]] [[charge quantization]] in [[J-homomorphism|J-]][[twisted Cohomotopy]] ([[schreiber:Hypothesis H]]) is due to

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* {#FSS19c} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

Discussion of the [[Page charge]] in relation to the [[Myers effect]] in [[M-theory]] for [[M2-branes]] polarizing into [[M5-branes]] of [[fuzzy 3-sphere|fuzzy]] [[3-sphere]]-shape:

* [[Krzysztof Pilch]], Alexander Tyukov, [[Nicholas Warner]], _Flowing to Higher Dimensions: A New Strongly-Coupled Phase on M2 Branes_, JHEP11 (2015) 170 ([arXiv:1506.01045](https://arxiv.org/abs/1506.01045))

### Relation to Freed-Witten anomaly


On relating the [[Freed-Witten anomaly]] to the [[shifted C-field flux quantization]]:

On [[D4-branes]]:

* [[Edward Witten]], Section 2 of: _Duality Relations Among Topological Effects In String Theory_, JHEP 0005:031, 2000 ([arXiv:hep-th/9912086](https://arxiv.org/abs/hep-th/9912086))

On [[D6-branes]]:

* [[Sergei Gukov]], [[James Sparks]], p. 21 of: _M-Theory on $Spin(7)$ Manifolds_, Nucl. Phys. B625 (2002) 3-69 ([arXiv:hep-th/0109025](https://arxiv.org/abs/hep-th/0109025))

* [[James Sparks]], _Global Worldsheet Anomalies from M-Theory_, JHEP 0408:037, 2004 ([arXiv:hep-th/0310147](https://arxiv.org/abs/hep-th/0310147))




[[!redirects shifted C-field flux quantization condition]]

[[!redirects Page charge]]
[[!redirects Page charges]]

[[!redirects C-field flux quantization]]

