
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Simons theory
+--{: .hide}
[[!include infinity-Chern-Simons theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

Witten introduced two topological twists of a supersymmetric nonlinear [[sigma model]], which is a certain N=2 superconformal field theory attached to a compact [[Calabi-Yau variety]] $X$. One of them is the _B-model_ [[topological string]]; it is a 2-dimensional [[topological conformal field theory|topological N=1 superconformal field theory]]. In Kontsevich's version, instead of SCFT with Hilbert space, one assembles all the needed data in terms of [[Calabi-Yau category|Calabi-Yau A-infinity-category]] which is the A-infinity-category of coherent sheaves on the underlying variety. In fact only the structure of a derived category is sufficient (and usually quoted): it is now known (by the results of [[Dmitri Orlov]] and [[Valery Lunts]]) that under mild assumptions on the variety, a derived category of coherent sheaves has a unique [[enhanced triangulated category|enhancement]].

The B-model arose in considerations of [[string theory|superstring]]-propagation on Calabi--Yau varieties: it may be motivated by considering the [[vertex operator algebra]] of the 2d[[CFT|SCFT]] given by the N=2 supersymmetric nonlinear [[sigma-model]] with target $X$ and then changing the fields so that one of the super-[[Virasoro algebra|Virasoro]] generators squares to 0. The resulting "topologically twisted" algebra may then be read as being the [[BRST complex]] of a [[TCFT]].

One can also define a B-model for [[Landau-Ginzburg model|Landau?Ginzburg models]]. The category of [[D-brane|D-branes]] for the string --  the [[B-branes]] -- is given by the category of [[matrix factorization|matrix factorizations]] (this was proposed by Kontsevich and elaborated by Kapustin-Li; see also papers of Orlov). For the genus 0 closed string theory, see the work of Saito.

By [[homological mirror symmetry]], the B-model is dual to the  [[A-model]].

## Properties

### Second quantization / effective background field theory


The [[second quantization]] [[effective field theory]] defined by the [[perturbation series]] of the B-model is supposed to be "Kodaira-Spencer gravity" / "BVOC theory" in 6d ([BCOV 93](#BCOV93), [Costello-Li 12](#CostelloLi12), [Costello-Li 15](#CostelloLi15)).

For more on this see at _[TCFT -- Worldsheet and effective background theories](http://ncatlab.org/nlab/show/TCFT#ActionFunctionals)_.


## Related concepts

* [[schreiber:∞-Chern-Simons theory]]

* [[sigma-model]]

  * [[AKSZ sigma-model]]

    * [[Poisson sigma-model]]

      * [[A-model]], **B-model**
     
      * [[half-twisted model]]

      * [[twistor string theory]]

    * [[Courant sigma-model]]

      * [[Chern-Simons theory]]

  * [[topological membrane]]

* [[topologically twisted D=4 super Yang-Mills theory]]

* [[Landau-Ginzburg model]]

[[!include gauge theory from AdS-CFT -- table]]


## References
 {#References}

### General

The B-model was first conceived in

* [[Edward Witten]], _Topological sigma models_, Commun. Math. Phys. __118__ (1988) 411--449, [euclid](http://projecteuclid.org/euclid.cmp/1104162092), [MR90b:81080](http://www.ams.org/mathscinet-getitem?mr=0958805)

An early review is in 

* [[Edward Witten]]. _Mirror manifolds and topological field theory_, in: Essays on mirror manifolds, pp. 120&#8211;-158. Int. Press, Hong Kong, 1992. ([arXiv:hep-th/9112056](http://arxiv.org/abs/hep-th/9112056)).

The motivation from the point of view of [[string theory]] with an eye towards the appearance of the Calabi-Yau categories is reviewed for instance in

* [[Paul Aspinwall]], _D-Branes on Calabi-Yau Manifolds_ ([arXiv:hep-th/0403166](http://arxiv.org/abs/hep-th/0403166))

A summary of these two reviews is in 

* H. Lee, _Review of topological field theory and homological mirror symmetry_ ([pdf](http://people.maths.ox.ac.uk/leeh/files/CYMSmini.pdf))

That the B-model [[Lagrangian]] arises in [[AKSZ theory]] by [[gauge fixing]] the [[Poisson sigma-model]] was observed in

* {#AKSZ} M. Alexandrov, [[Maxim Kontsevich|M. Kontsevich]], [[Albert Schwarz|A. Schwarz]], O. Zaboronsky, around page 28 in _The geometry of the master equation and topological quantum field theory_, Int. J. Modern Phys. A 12(7):1405--1429, 1997


For survey of the literature see also 

* [[Kevin H. Lin]], MO comment on _[Matrix factorization and physics](http://mathoverflow.net/a/9748/381), 2009

The B-model on [[genus]]-0 [[cobordism]]s had been constructed in

* S. Barannikov, [[Maxim Kontsevich]], _Frobenius manifolds and formality of Lie algebras of polyvector fields_ ,  Internat. Math. Res. Notices  1998,  no. 4, 201--215; [math.QA/9710032](http://arxiv.org/abs/alg-geom/9710032) [doi](http://dx.doi.org/10.1155/S1073792898000166)

The construction of the B-model as a [[TCFT]] on [[cobordisms]] of arbitrary [[genus]] was given in 

* [[Kevin Costello]], _The Gromov-Witten potential associated to a TCFT_ ([math.QA/0509264](http://arxiv.org/abs/math/0509264))

See also the MathOverflow discussion: [higher-genus-closed-string-b-model](http://mathoverflow.net/questions/8692/higher-genus-closed-string-b-model)

### Second quantization to Kodeira-Spencer gravity
 {#ReferencesBCOV}

The [[second quantization]] [[effective field theory|effective]] field theory defined by the B-model [[perturbation series]] ("Kodeira-Spencer gravity"/"BCOV theory") is discussed in 

Discussion of how the [[second quantization]] of the [[B-model]] yields [[Kodeira-Spencer gravity]]/[[BCOV theory]] is in 

* {#BCOV93} M. Bershadsky, S. Cecotti, [[Hirosi Ooguri]], [[Cumrun Vafa]], _Kodaira-Spencer Theory of Gravity and Exact Results for Quantum String Amplitudes_, Commun.Math.Phys.165:311-428,1994 ([arXiv:hep-th/9309140](http://arxiv.org/abs/hep-th/9309140))
 

* {#CostelloLi12} [[Kevin Costello]], [[Si Li]], _Quantum BCOV theory on Calabi-Yau manifolds and the higher genus B-model_ ([arXiv:1201.4501](http://arxiv.org/abs/1201.4501))
 

* [[Si Li]], _BCOV theory on the elliptic curve and higher genus mirror symmetry_ ([arXiv:1112.4063](http://arxiv.org/abs/1112.4063))

* [[Si Li]], _Variation of Hodge structures, Frobenius manifolds and Gauge theory_ ([arXiv:1303.2782](http://arxiv.org/abs/1303.2782))

* {#CostelloLi15} [[Kevin Costello]], Si Li, _Quantization of open-closed BCOV theory, I_ ([arXiv:1505.06703](http://arxiv.org/abs/1505.06703))

### Computation via topological recursion

Computation via [[topological recursion]] in [[matrix models]] and all-[[genus of  a surface|genus]] proofs of [[mirror symmetry]] is due to

* {#BouchardKlemmMarinoPasquetti09} [[Vincent Bouchard]], [[Albrecht Klemm]], [[Marcos Marino]], [[Sara Pasquetti]], _Remodeling the B-model_, Commun.Math.Phys.287:117-178, 2009 ([arXiv:0709.1453](https://arxiv.org/abs/0709.1453))

* [[Bertrand Eynard]], [[Amir-Kian Kashani-Poor]], Olivier Marchal, _A matrix model for the topological string I: Deriving the matrix model_ ([arXiv:1003.1737](https://arxiv.org/abs/1003.1737))

* [[Bertrand Eynard]], [[Amir-Kian Kashani-Poor]], Olivier Marchal, _A matrix model for the topological string II: The spectral curve and mirror geometry_ ([arXiv:1007.2194](https://arxiv.org/abs/1007.2194))

* {#EynardOrantin12} [[Bertrand Eynard]], [[Nicolas Orantin]], _Computation of open Gromov-Witten invariants for toric Calabi-Yau 3-folds by topological recursion, a proof of the BKMP conjecture_ ([arXiv:1205.1103](https://arxiv.org/abs/1205.1103))

* {#FangLiuZong13} Bohan Fang, Chiu-Chu Melissa Liu, Zhengyu Zong, _All Genus Open-Closed Mirror Symmetry for Affine Toric Calabi-Yau 3-Orbifolds_ ([arXiv:1310.4818](https://arxiv.org/abs/1310.4818))


[[!redirects Kodeira-Spencer gravity]]
[[!redirects BCOV theory]]

[[!redirects B-models]]
