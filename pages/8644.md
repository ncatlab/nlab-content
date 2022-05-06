
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
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

In [[QCD]] [[instanton]] configurations of the [[gauge field]] control the experimentally observed [[vacuum]] structure of the theory.

One considers QCD on a [[Minkowski spacetime]] [[Wick rotation|Wick rotated]] to a Euclidean $\mathbb{R}^4$ and assumes the [[field strength]] to [[vanish at infinity]]. This makes the gauge field configurations be equivalently $SU(3)$-[[principal connections]] on the 4-[[sphere]] $S^4$. The [[second Chern class]] of the underlying $SU(3)$-[[principal bundle]] is called the [[Yang-Mills instanton]]-number of the gauge field configuration. The theoretical/experimentally observed [[vacuum]] of [[QCD]] is some [[superposition]] of gauge fields in various instanton number sectors.

In particular the **instanton liquid model** in QCD assumes that the [[vacuum]] (ground state of QCD) is populated by instanton field configurations of average radius $1/3 fm$ ([[femtometres]]) with a density of 1 such instanton per $fm^4$. Some details of this model remain subtle, see notably ([Schaefer-Shuryak](#SchaeferShuryak)) for a survey.

This instanton sea model suffers however from infrared divergencies that either require a finite-volume cutoff or appeal to other effects (e.g. [Witten 98](#Witten98)). 

But [[lattice gauge field theory]] simulations demonstrate numerically that the QCD vacuum is filled with instantons (e.g. [Gruber 13, esp. sections 5 and 7](#Gruber13)). Whether or not their density and distribution may be or has been theoretically derived from first principles is still being discussed (e.g. [Schaefer 02](#Schaefer02))

The _Witten-Veneziano formula_ ([Witten 79](#Witten79), [Veneziano 79](#Veneziano79)) relates topological instanton charge to the mass of the $\eta'$-[[particle]] in the limiting case that the gauge group is $SU(N)$ for $N \to \infty$. Discussion of this relation for the experimentally observed finite case of $N = 3$ includes ([Creutz 11](#Creutz11)).

## Experimental evidence

An instanton vacuum is argued to account for

* formation of the gluon condensate ([[Mikhail Shifman]], [[Arkady Vainshtein]] and [[Vladimir Zakharov]], Nucl. Phys. B 147 (1979) 385).

* spontaneous [[chiral symmetry breaking]] ([Diakonov 96](#Diakonov96))

* [[baryogenesis]] in the early universe by inducing baryon number non-conservation

## Critical discussion of the literature
 {#CriticalDiscussionOfTheLiterature}

In the physics literature a style of discussion of instantons is wide-spread where the motivation of the formulas considered is dubious. In these references (for instance [Schaefer-Shuryak 96](#SchaeferShuryak) and [Forkel 00](#Forkel) and many more) it is said that 

1. a YM field of minimal energy, hence of vanishing [[field strength]] is one that is pure gauge;

1. that therefore on a [[Minkowski spacetime]] $\mathbb{R}^4$ in [[temporal gauge]] and assuming fields are [[vanishing at infinity]], these are given by [[connection on a bundle|connection]] 1-forms on $S^3$ of the form $U^{-1} d U$ for $U \colon S^3 \to G$ a smooth function, and 

1. that therefore equivalence classes of such fields are given by [[homotopy]] classes of maps $S^3 \to G$, hence by the third [[homotopy group]] $\pi_3(G)$.

These points are not really correct, even though the conclusion about the classification of instanton sectors turns out to be right. 

The correct statement is that winding-number sectors/instanton sectors are equivalence classes of $G$-[[principal bundles]] on the [[one-point compactification]] $S^4$ of [[Minkowski spacetime]] $\mathbb{R}^4$, and these happen to indeed be given by homotopy classes of maps $S^3 \to G$, with $S^3$ regarded as the "equator" of $S^4$. This is for instance stated explicitly in ([Nakahara](#Nakahara)) and used in many references, such as ([Witten 85](#Witten85)).

Before we come to this, first notice the problems with the above items from the standard physics reviews:

1. [[gauge field|Gauge fields]] with vanishing [[field strength]] are [[flat connections]]. These are classified by [[group]] [[homomorphisms]] from the [[fundamental group]] of the given [[space]] or [[spacetime]] to the [[gauge group]]. Hence not every such field configuration is "pure gauge", this is only the case if the [[fundamental group]] is trivial. Of course this is the case on $\mathbb{R}^n$ and $S^n$, so the first item above is correct in these cases. But beware that these authors usually justify the third item above by referring to gauge transformations between gauge fields, which is then again wrong, see the next point.

1. Flat connection on $S^3$ are not classified by homotopy classes of maps $S^3 \to G$. Instead, since $\pi_1(S^3)$ is the trivial group, there is only the trivial such flat connection. This is actually manifest in the formula for such connections which is preferred in these references, which is "$U^{-1} d U$" with $U \colon S^3 \to G$ a gauge transformation. That formula exhibits precisely the trivial gauge connection $d$ as gauge equivalent to $U^{-1} d U$.

What would give the intended classification is if one considered connections of the form $U^{-1} d U$ only modulo those gauge transformations $h \colon S^3 \to G$ which can be smoothly extended to maps $D^4 \to G$. This is what these references seem to be implicitly assuming. But this is not the gauge transformation law for connections... this is instead the gauge transformation law for transition functions of $G$-principal bundles. 

And this brings us to the correct mathematical interpretation of instantons, as in ([Nakahara](#Nakahara)) and similar:

We are looking for gauge field configurations on $\mathbb{R}^4$ that have [[field strength]] [[vanishing at infinity]]. This means we are looking for $G$-[[principal connections]] on the [[one-point compactification]] $S^4$ of $\mathbb{R}^4$ such that the [[curvature]] 2-form vanishes at one "pole".

Now by the discussion at [[principal bundle]], $G$-principal bundles can be constructed for instance by [[cocycles]] in [[Cech cohomology]] of $S^4$ with [[coefficients]] in $G$. In general this means to specify $G$-valued transitions functions on overlaps of a [[good open cover]] of $S^4$. But a standard argument shows that for spheres the following [[covering]] is already sufficient: we cover the $n$-sphere $S^n$ by two hemi-$n$-spheres that overlap a bit at the equator, which is hence of the form $S^{n-1} \times [-\epsilon, \epsilon]$. A Cech cocycle on such a cover is then simply given by one single $G$-valed transition function $S^{n-1} \to G$. This is known as the _[[clutching construction]]_.

Moreover, a [[gauge transformation]] of such a Cech cocycle is given by multiplying with the restriction of $G$-valued functions on the two hemi-$n$-spheres $\simeq D^n$ to the equator. This just means that those transition functions $S^3 \to G$ are gauge-trivial which may be extended smoothly to funtions $D^4 \to G$.

In conclusion, the desired classification of instanton solutions by homotopy classes of maps $U \colon S^3 \to G$ is precisely the [[clutching construction]] of $G$-principal bundles.

Finally, in order to add the [[principal connections]] to the picture, we think of one of the two semi-$n$-spheres to be the neighbourhood of infinity and hence, since the [[field strength]] is demanded to be [[vanishing at infinity]], take the local gauge field to be the vanishing [[groupoid of Lie algebra valued 1-forms|Lie algebra valued differential 1-form]] there. But then the rules for [[Cech cohomology]] with coefficients in the [[groupoid of Lie algebra valued 1-forms]], and using the above [[clutching construction]], it follows that on the equator overlap the gauge field has to be $U^{-1} d U \in \Omega^1( S^3 \times (-\epsilon, \epsilon) )$. This we may then extend in any desired way to a (non-flat) gauge connection over the remaining semi-$n$-sphere $D^4$, hence over the actual spacetime. 

Notice that this is precisely the argument which for $G = U(1)$ the [[circle group]] and for $n = 2$ is known as the argument of _[[Dirac charge quantization]]_ (which is also often misrepresented in the physics literature...)

For more see at _[Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_.

## Related concepts

* [[interacting vacuum]]

* [[fiber bundles in physics]]

* [[non-perturbative effect]]

* [[Yang-Mills instanton]]

  * [[theta vacuum]]

  * [[BPST-instanton]]

* [[quantum tunneling]]

* at [[thermal field theory|finite temperature]]: [[caloron]]

  * [[caloron correspondence]]


* [[CP violation]]

* [[baryogenesis]]

* [vortex atoms -- Similarity to concepts in modern particle physics](http://ncatlab.org/nlab/show/On+Vortex+Atoms#SimilarityToParticlePhysics)


## References
 {#References}

### General

(See also the general references at _[[instanton]]_.)

Physics-style  surveys include the introductory lecture notes

* [[Marcos Marino]], _Instantons and Large $N$ -- An introduction to non-perturbative methods in QFT_ ([pdf](http://laces.web.cern.ch/laces/LACES10/notes/instlargen.pdf))


* {#Forkel} Hilmar Forkel, _A Primer on Instantons in QCD_ ([arXiv:hep-ph/0009136](http://arxiv.org/abs/hep-ph/0009136))
 
* [[Edward Shuryak]], _Physics of QCD Instantons_, Proceedings of the International School of Subnuclear Physics Erice, Sicily, Italy, August &#8211; September 2002 ([web](http://www.worldscientific.com/doi/abs/10.1142/9789812796653_0003))

and the fairly detailed account (with lots of pointers to the literature)

* {#SchaeferShuryak98} [[Thomas Schaefer]], [[Edward Shuryak]], _Instantons in QCD_, Rev. Mod. Phys.70:323-426,1998 ([arXiv:hep-ph/9610451](http://arxiv.org/abs/hep-ph/9610451)) 
  
  {#SchaeferShuryak} section III D: relation to [[confinement]]
  

* Dmitri Diakonov, _Instantons at work_ ([arXiv:hep-ph/0212026](http://arxiv.org/abs/hep-ph/0212026))

See also the survey in 

* Marcus Hutter, _Instantons in QCD: Theory and Application of the Instanton Liquid Model_ ([arXiv:hep-ph/0107098](http://arxiv.org/abs/hep-ph/0107098))

On possible experimental signatures at the [[LHC]]:

* Simone Amoroso, Deepak Kar, Matthias Schott, _How to discover QCD Instantons at the LHC_ ([arXiv:2012.09120](https://arxiv.org/abs/2012.09120))


Detailed argument for the [[theta-vacuum]] structure from [[chiral symmetry breaking]] is offered in 

* [[Curtis Callan]], R.F. Dashen, [[David Gross]], _The Structure of the Gauge Theory Vacuum_, Phys.Lett. 63B (1976) 334-340 ([spire](http://inspirehep.net/record/3673?ln=en))

* G. Morchio, [[Franco Strocchi]], _Chiral symmetry breaking and theta vacuum structure in QCD_, Annals Phys.324:2236-2254, 2009 ([arXiv:0907.2522](https://arxiv.org/abs/0907.2522))



A review in view of the [[asymptotic series]] nature of the [[Feynman perturbation series]] is in

* {#Suslov05} [[Igor Suslov]], section 4.5 of _Divergent perturbation series_, Zh.Eksp.Teor.Fiz. 127 (2005) 1350; J. Exp. Theor. Phys. 100 (2005) 1188 ([arXiv:hep-ph/0510142](https://arxiv.org/abs/hep-ph/0510142))


A survey with emphasis on the [[strong CP problem]] is in

* [[Roberto Peccei]], _The Strong CP Problem and Axions_, Lect.Notes Phys.741:3-17,2008 ([arXiv:hep-ph/0607268](http://arxiv.org/abs/hep-ph/0607268))


A more mathematically precise account which identifies instanton solutions explicitly equivalence classes of $G$-principal bundles is around Example 9.12 (p.320) and Section 10.5.5 (p.360) of

* {#Nakahara} Nakahara, _Geometry Topology and Physics_
 

This perspective is for instance also the one used in 

* [[Edward Witten]], _Global gravitational anomalies_,  Comm. Math. Phys. Volume 100, Number 2 (1985), 197-229. ([Euclid](http://projecteuclid.org/euclid.cmp/1103943444)) 
 {#Witten85}

Discussion in the context of [[chiral symmetry breaking]] includes

* {#Diakonov96} Dmitri Diakonov, _Chiral Symmetry Breaking by Instantons_ ([arXiv:hep-ph/9602375](http://arxiv.org/abs/hep-ph/9602375))

Discussion in the context of [[confinement]] includes

* Y. M. Cho, _Dimensional Transmutation by Monopole Condensation in QCD_ ([arXiv:1206.6936](http://arxiv.org/abs/1206.6936))

Discussion in the context of the [[quark-gluon plasma]] includes

* {#Shuryak01} [[Edward Shuryak]], _Nonperturbative QCD and Quark-Gluon Plasma_, lectures at Trieste, 2001 ([pdf](http://users.ictp.it/~pub_off/lectures/lns010/Shuryak/Shuryak.pdf))

* Nikolai Kochelev, _Ultra-light Glueballs in Quark-Gluon Plasma_ ([arXiv:1501.07002](http://arxiv.org/abs/1501.07002))

Discussion of the infrared problem of the QCD instanton vacuum model includes

* {#Witten98} [[Edward Witten]], _Theta Dependence In The Large N Limit Of Four-Dimensional Gauge Theories_, Phys.Rev.Lett.81:2862-2865,1998 ([arXiv:hep-th/9807109](http://arxiv.org/abs/hep-th/9807109))

Discussion of instantons in [[lattice gauge theory]] includes

* {#Moore03} Guy Moore, section 7 of _Informal lectures on lattice gauge theory_, 2003 ([pdf](http://www.physics.mcgill.ca/~guymoore/latt_lectures.pdf))

* {#Creutz11} Michael Creutz, _Anomalies, gauge field topology, and the lattice_, Annals of Physics 326 (2011) 911&#8211;925 ([pdf](http://thy.phy.bnl.gov/~creutz/mypubs/pub192.pdf))

* {#Gruber13} Florian Gruber, _Topology in dynamical Lattice QCD simulations_, 2013 ([web](http://epub.uni-regensburg.de/27631/), [pdf](http://epub.uni-regensburg.de/27631/1/dissertation.pdf))


Discussion of the $\eta'$-mass from instantons includes

* {#Witten79} [[Edward Witten]], Nucl. Phys. B 156 (1979) 269.

* {#Veneziano79} [[Gabriele Veneziano]], Nucl. Phys. B 159 (1979) 213

* {#Schaefer02} [[Thomas Schaefer]], _QCD and the eta prime Mass: Instantons or Confinement?_, Phys.Rev. D67 (2003) 074502 ([arXiv:hep-lat/0211035](http://arxiv.org/abs/hep-lat/0211035))

* _A renewed look at $\eta'$ in medium, ([arXiv:1203.6740](http://arxiv.org/abs/1203.6740))

Relation to the [[scanning map]] and [[configuration spaces of points]] in:

* {#AtiyahJones78} [[Michael Atiyah]], [[John David Stuart Jones]], _Topological aspects of Yang-Mills theory_, Comm. Math. Phys. Volume 61, Number 2 (1978), 97-118 ([arXiv:1103904210](https://projecteuclid.org/euclid.cmp/1103904210))


### Relation to skyrmions, calorons, monopoles


The construction of [[Skyrmions]] from [[instantons]] is due to 

* {#AtiyahManton89} [[Michael Atiyah]], N S Manton, _Skyrmions from instantons_, Phys.  Lett.  B, 222(3):438–442, 1989 (<a href="https://doi.org/10.1016/0370-2693(89)90340-7">doi:10.1016/0370-2693(89)90340-7</a>)

The relation between [[skyrmions]], [[instantons]], [[calorons]], [[solitons]] and [[monopoles]] is usefully reviewed and further developed in 

* {#Cork18a} [[Josh Cork]], _Calorons, symmetry, and the soliton trinity_, PhD thesis, University of Leeds 2018 ([web](http://etheses.whiterose.ac.uk/22097/))

* {#Cork18b} [[Josh Cork]], _Skyrmions from calorons_, J. High Energ. Phys. (2018) 2018: 137 ([arXiv:1810.04143](https://arxiv.org/abs/1810.04143))


[[!redirects instantons in QCD]]
[[!redirects instanton in quantum chromodynamics]]
[[!redirects instantons in quantum chromodynamics]]
[[!redirects instanton liquid]]
[[!redirects QCD instanton liquid]]
[[!redirects instanton liquid in quantum chromodynamics]]

[[!redirects QCD vacuum]]
[[!redirects QCD vacua]]

[[!redirects QCD instanton]]
[[!redirects QCD instantons]]

[[!redirects instanton sea]]