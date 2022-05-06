
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

In [[string theory]]/[[M-theory]], the _shifted C-field flux quantization condition_ is a [[charge quantization]]-condition on the [[supergravity C-field]] expected in [[M-theory]]. It says that the [[real cohomology]] class of the [[flux density]] ([[field strength]]) [[differential 4-form]] $G_4 \in \Omega^4(X)$ on [[spacetime]] $X$ becomes integral after shifted by one quarter of the [[first Pontryagin class]], hence the condition that with the shifted 4-flux density defined as

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

## Related concepts

* [[C-field tadpole cancellation]]

## References

The suggestion originates in

* {#Witten96a} [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J. Geom. Phys. 22:1-13, 1997 ([arXiv:hep-th/9609122](https://arxiv.org/abs/hep-th/9609122))

* {#Witten96b} [[Edward Witten]], _Five-Brane Effective Action In M-Theory_, J. Geom. Phys. 22:103-133, 1997 ([arXiv:hep-th/9610234](https://arxiv.org/abs/hep-th/9610234))

Proposals to model the condition by a [[Wu class]]-shifted variant of [[ordinary differential cohomology]] include

* {#HopkinsSinger02} [[Michael Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_  J. Differential Geom. Volume 70, Number 3 (2005), 329-452.  ([arXiv:math.AT/0211216](http://arxiv.org/abs/math.AT/0211216), [euclid:1143642908](https://projecteuclid.org/euclid.jdg/1143642908))

* {#DiaconescuFreedMoore03} E. Diaconescu, [[Dan Freed]], [[Greg Moore]],  _The $M$-theory 3-form and $E_8$-gauge theory_, chapter in [[Haynes Miller]], [[Douglas Ravenel]] (eds.) _Elliptic Cohomology Geometry, Applications, and Higher Chromatic Analogues_, Cambridge University Press 2007 ([arXiv:hep-th/0312069](http://arxiv.org/abs/hep-th/0312069), [doi:10.1017/CBO9780511721489](https:
//doi.org/10.1017/CBO9780511721489))

* {#FreedMoore04} [[Dan Freed]], [[Greg Moore]], _Setting the [[quantum integrand]] of M-theory_, Communications in Mathematical Physics, Volume 263, Number 1, 89-132, ([arXiv:hep-th/0409135](http://arxiv.org/abs/hep-th/0409135), [doi:10.1007/s00220-005-1482-7](https://doi.org/10.1007/s00220-005-1482-7))

* {#Moore04} [[Greg Moore]], _Anomalies, Gauss laws, and Page charges in M-theory_ ([arXiv:hep-th/0409158](http://arxiv.org/abs/hep-th/0409158))

* {#FSS12} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_, Communications in Mathematical Physics,  Volume 333, Issue 1 (2015), Page 117-151 ([arXiv:1202.2455](http://arxiv.org/abs/1202.2455), [doi:10.1007/s00220-014-2228-1](http://link.springer.com/article/10.1007%2Fs00220-014-2228-1))



The observation that the condition is implied by [[supergravity C-field|C-field]] [[charge quantization]] in [[J-homomorphism|J-]][[twisted Cohomotopy]] ([[schreiber:Hypothesis H]]) is due to

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))


[[!redirects shifted C-field flux quantization condition]]

