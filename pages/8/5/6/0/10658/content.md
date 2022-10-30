
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea

[[motive|Motivic]] structures enters [[quantum physics]] in two dual guises, related to on the one hand [[algebraic deformation quantization]] and on the other hand to [[geometric quantization]]

### Via perturbative algebraic deformation quantization

In the first case one observes that [[formal deformation quantization]] of $n$-dimensional [[prequantum field theory]] amounts to choosing an inverse [[equivalence]] to the [[formality]] map from [[En-algebras]] to [[Pn-algebras]], this is explained at _[Motivic Galois group action on the space of quantizations](deformation+quantization#MotivicGaloisGroup)_. 

The [[automorphism infinity-group]] of either side therefore naturally [[infinity-action|acts]] on the space of formal deformation quantization choices obtained this way and one shows (conjectured by [[Maxim Kontsevich]] ([Kontsevich 99](#Kontsevich99)), recently proven by Dolgushev) that the connected component group of this is the 
[[Grothendieck-Teichmüller group]], a [[quotient]] of the [[motivic Galois group]]. 
Related to this in some way is [[Alain Connes]]' "[[cosmic Galois group]]" [[action|acting]] on the space of [[renormalization|renormalizations]] of [[perturbative quantum field theory]]. 

According to Kontsevich, this explains the role of motivc [[periods]] in [[correlation functions]] and hence in [[scattering amplitudes]] in [[perturbative field theory]], see the references at _[[motivic multiple zeta values]] _[[motivic L-function]]_.


### Via non-perturbative geometric quantization

On the other hand, in full [[non-perturbative quantum field theory|non-perturbative]] [[geometric quantization]] in its modern cohomological form as [geometric quantization by push-forward](http://ncatlab.org/nlab/show/geometric+quantization+by+push-forward) one finds a "[[cohesion|cohesive]]" form of actual [[motivic cohomology]]exhibited by "[[cohesive]] [[pure motives]]". In effect, a [[local action functional]] on a [[moduli space]] of [[field (physics)|field]] [[trajectories]] is exhibited by a [[correspondence]]
with the [[local action functional]] itself exhibited by a [[twisted bivariant cohomology|twisted bivariant cocycle]] on the correspondence space, and the [[motivic quantization|motivic path integral quantization]] of this corresponds to the induced pull-push index transform. See the [references below](#ReferencesNonPerturbativeGeometric).
  

## References

We list references

1. [on motives in pertrubative algebraic quantization](#ReferencesPerturbativeAlgebraic)

1. [on motives in non-perturbative geometric quantization](#ReferencesNonPerturbativeGeometric)

### On motivic structures in perturbative quantum field theory
 {#ReferencesPerturbativeAlgebraic}

The action of a [[motivic Galois group]] ("[[cosmic Galois group]]") on the space of choices in [[deformation quantization]] was first observed/conjectured in 

* [[Maxim Kontsevich]], _Operads and Motives in Deformation Quantization_, Lett. Math. Phys.48:35-72,1999 ([arXiv:math/9904055](http://arxiv.org/abs/math/9904055))
 {#Kontsevich99}

A survey of this and similar motivic phenomena in physics is in the appendix of

* A. Rej, [[Matilde Marcolli]], _Motives, an introductory survey for physicists_ ([pdf](http://www.its.caltech.edu/~matilde/ObiMotivesSurveyFinal.pdf))

and more is in

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_


See also the lecture

* [[Spencer Bloch]], _Dilogarithm motives appearing in physics_ ([video](http://blip.tv/pifagorov/spencer-bloch-dilogarithm-motives-arising-in-physics-3854827)); S. Bloch, H. Esnault, D. Kreimer, _On motives associated to graph polynomials_ [pdf](http://www.math.uchicago.edu/~bloch/graphpoly050928b.pdf); Spencer Bloch, Pierre Vanhove, _The elliptic dilogarithm for the sunset graph_, IHES preprint P-13-24, [pdf](http://preprints.ihes.fr/2013/P/P-13-24.pdf)
* Conference _Amplitudes and Periods_, Dec 3-7, 2012, IH&#201;S, &lt;http://pagesperso.ihes.fr/~vanhove/QFT2012> (has online videos of talks) 

### On motivic structures in non-perturbative local quantum field theory
 {#ReferencesNonPerturbativeGeometric}

The formulation of [[quantization]] of [[local prequantum field theory]] as a passage to [[cohesive]] generalized [[pure motives]], hence "[[motivic quantization]]" is formulated as such in the last section of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

based on 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_


The following is a list of "precursors" of aspects of the idea [[motivic quantization]] as laid out there

$\,$

The formulation of [[geometric quantization]] as an [[index]] map in [[K-theory]] is attributed to [[Raoul Bott]].

The proposal that the natural [[domain]] for geometric quantization are [[Lagrangian correspondences]] is due to 

* [[Lars Hörmander]], _Fourier Integral Operators I._, Acta Math. __127__ (1971)
 {#Hoermander71}

* [[Alan Weinstein]], _Symplectic manifolds and their lagrangian submanifolds_, Advances in Math. __6__ (1971) {#Weinstein71}

In [[semiclassical quantization]] the precursor to this are works of Maslov in 1960s (which are quite related to Hoermander's and Sato's work).

With the recognition of [[supersymmetric quantum mechanics]] in the 1980s, [[index theory]] (hence [[push-forward in generalized cohomology]] to the point) was understood to be about [[partition functions]] of systems of [[supersymmetric quantum mechanics]] in 

* [[Luis Alvarez-Gaumé]], _Supersymmetry and the Atiyah-Singer index theorem_, Comm. Math. Phys. __90__:2 (1983) 161-173, [euclid](http://projecteuclid.org/euclid.cmp/1103940278) {#AlvarezGaume83}

* [[Ezra Getzler]], _Pseudodifferential operators on supermanifolds and the Atiyah-Singer index theorem_, Comm. Math. Phys. 92 (1983), 163-178. ([pdf](http://math.northwestern.edu/~getzler/Papers/1103940796.pdf))
 {#Getzler83}

*  [[Ezra Getzler]], _A short proof of the Atiyah-Singer index theorem_, Topology 25 (1986), 111-117 ([pdf](http://math.northwestern.edu/~getzler/Papers/local.pdf))

In higher analogy to this but much more subtly, the [[partition function]] of the [[heterotic string]], hence the [[Witten genus]], was understood to be the [[push-forward in generalized cohomology|push-forward]] to the point in [[tmf]]:

* [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))
  {#AndoHopkinsRezk}

The general perspective of the [[path integral as a pull-push transform]] was originally laid out, somewhat implicitly, in

* [[Daniel Freed]], _Quantum groups from path integrals_, [arXiv:q-alg/9501025](http://xxx.lanl.gov/abs/q-alg/9501025); _Higher algebraic structures and quantization_, [arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115)

and then fully explicitly in

* [[Daniel Freed]], _Twisted K-theory and the Verlinde ring_, Andrejewski lecture ([pdf slides](http://www.ma.utexas.edu/users/dafr/Andrejewski%20Lectures.html))

Discussion along these lines of a pull-push quantization over [[KU]] of a 2-dimensional [[Chern-Simons theory]]-like [[gauge theory]] is in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Consistent orientation of moduli spaces_, [arXiv:0711.1909](http://arxiv.org/abs/0711.1909) {#FreedHopkinsTeleman07}

More in detail a functorial quantization of suitable correspondences of smooth manifolds to [[KK-theory]] by pull-push has been given in ([Connes-Skandalis 84](#ConnesSkandalis84)) and the generalization of that to [[equivariant K-theory]] (hence to [[groupoid K-theory]] of [[action groupoids]]) is in

* [[Heath Emerson]], [[Ralf Meyer]], _Bivariant K-theory via correspondences_, Adv. Math. 225 (2010), 2883-2919 ([arXiv:0812.4949](http://arxiv.org/abs/0812.4949))
 {#EmersonMeyer08}



The point of view that the [[path integral as a pull-push transform|pull-push quantization]] of [[Gromov-Witten theory]] should be thought of as a theory of [[Chow motives]] of [[Deligne-Mumford stacks]] is expressed in 

* [[Kai Behrend]], [[Yuri Manin]], _Stacks of Stable Maps and Gromov-Witten Invariants_ ([arXiv:alg-geom/9506023](http://arxiv.org/abs/alg-geom/9506023))
 {#BehrendManin95}

* [[Bertrand Toën]], _On motives for Deligne-Mumford stacks_, International Mathematics Research Notices 2000, 17 (2000) 909-928 ([arXiv:math/0006160](http://arxiv.org/abs/math/0006160), [web](http://hal.archives-ouvertes.fr/hal-00773027), [pdf](http://hal.archives-ouvertes.fr/docs/00/77/30/27/PDF/motdm.pdf))
 {#Toen00}


The proposal that the natural [[codomain]] for geometric quantization is [[KK-theory]] is due to 

* [[Klaas Landsman]], _Functorial quantization and the Guillemin-Sternberg conjecture_ Proc. Bialowieza 2002 ([arXiv:math-ph/0307059](http://arxiv.org/abs/math-ph/0307059))

* [[Klaas Landsman]], _Functoriality of quantization: a KK-theoretic approach_, talk at ECOAS, ECOAS, Dartmouth College, October 2010 ([web](http://www.academia.edu/1992202/Functoriality_of_quantization_a_KK-theoretic_approach))


The point of view that pull-push along [[correspondences]] equipped with [[operator K-theory]] [[cycles]] in [[KK-theory]] is a [[K-theory]]-analog of [[motives]] was amplified in 

* [[Alain Connes]], [[Georges Skandalis]], _The longitudinal index theorem for foliations_. Publ. Res. Inst. Math. Sci. 20,
no. 6, 1139&#8211;1183 (1984) ([pdf](http://www.alainconnes.org/docs/longitudinal.pdf))
 {#ConnesSkandalis84}

* [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

The proof that the [[universal property]] that characterizes [[noncommutative motives]] is the analog in [[noncommutative algebraic geometry]] of the [[universal property]] that characterizes [[KK-theory]] in [[noncommutative topology]] is due to

* [[Gonçalo Tabuada]], _K-theory via universal invariants_, Duke Math. J. 145 (2008), no.1, 121&#8211;206.
 {#Tabuada08}

* [[Denis-Charles Cisinski]], [[Gonçalo Tabuada]], _Non connective K-theory via universal invariants_. Compositio
Mathematica 147 (2011), 1281&#8211;1320 ([arXiv:0903.3717](http://arxiv.org/abs/0903.3717))
 {#CisinskiTabuada11}

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_,  Geometry and Topology ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282))
 {#BlumbergGepnerTabuada10}

The description of [[string topology]] operations as an [[HQFT]] defined by pull-push transforms in [[ordinary homology]]/[[ordinary cohomology]] was originally realized in 

* [[Ralph Cohen]], [[Veronique Godin]],  _[[A Polarized View of String Topology]]_ ([arXiv:math/0303003](http://arxiv.org/abs/math/0303003))

* Hirotaka Tamanoi, _Loop coproducts in string topology and triviality of higher genus TQFT operations_ (2007) ([arXiv:0706.1276](http://arxiv.org/abs/0706.1276))
 {#Tamanoi07}

A detailed discussion and generalization to [[open strings]] and an open-closed [[HQFT]] in the presence of a single space-filling [[brane]] is in

* [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 {#Godin}


and for arbitrary [[branes]] in 

* [[Alexander Kupers]], _String topology operations_ MS thesis (2011) ([pdf](http://math.stanford.edu/~kupers/thesis7thjune2011.pdf))

That [[D-brane charge]] and [[T-duality]] is naturally understood in terms of pull-push/[[indices]] along [[correspondences]] in [[noncommutative topology]]/[[KK-theory]] was amplified in 

* [[Jacek Brodzki]], [[Varghese Mathai]], [[Jonathan Rosenberg]], [[Richard Szabo]],  _Noncommutative correspondences, duality and D-branes in bivariant K-theory_, Adv. Theor. Math. Phys.13:497-552,2009 ([arXiv:0708.2648](http://arxiv.org/abs/0708.2648))
 {#BMRS2}


The general analogy between such [[KK-theory]] cocycles and [[pure motives]] is noted explicitly in 

* [[Alain Connes]], Caterina Consani, [[Matilde Marcolli]], _Noncommutative geometry and motives: the thermodynamics of endomotives_ ([arXiv:math/0512138](http://arxiv.org/abs/math/0512138))
 {#ConnesConsaniMarcolli05}

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_

This analogy is given a precise form in

*  [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities, and applications to topological T-duality_, ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf), [talk notes](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KKTD.pdf))
 {#Mahanta13}

where it is shown that there is a universal functor $KK \longrightarrow NCC_{dg}$ from [[KK-theory]] to the category of [[noncommutative motives]], which is the category of [[dg-categories]] and dg-[[profunctors]] up to homotopy between them. This is given by sending a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] of (the unitalization of) its underlying [[associative algebra]].


Linearization of correspondences of [[discrete groupoid|geometrically discrete groupoids]] was considered in 

* [[John Baez]], [[Jim Dolan]], _Groupoidification_, November 2009 ([web](http://math.ucr.edu/home/baez/groupoidification/))

and applied to a pull-push quantization of [[Dijkgraaf-Witten theory]] in 

* [[Jeffrey Morton]], _2-Vector Spaces and Groupoids_ ([arXiv:0810.2361](http://arxiv.org/abs/0810.2361))

* [[Jeffrey Morton]], _Cohomological Twisting of 2-Linearization and Extended TQFT_ ([arXiv:1003.5603v4](http://arxiv.org/abs/1003.5603v4))
 {#Morton10}

following previous work by [[Daniel Freed]] and [[Frank Quinn]].

An unpublished predecessor note on quantization of correspondences of moduli stacks of fields is 

* [[Urs Schreiber]], _[[schreiber:Nonabelian cocycles and their quantum symmetries]]_ (2008)
 {#Schreiber08}

Quantization of [[correspondences]] of [[perfect ∞-stacks]] by pull-push of [[stable (∞,1)-categories]] of [[quasicoherent sheaves]] is discussed in

* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]],
_[[geometric function theory|Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry]]_, J. Amer. Math. Soc. __23__ (2010), no. 4, 909-966,
([arXiv:0805.0157](http://arxiv.org/abs/0805.0157))

Linearization of [[higher correspondences]] of [[discrete ∞-groupoids]] as the quantizaton of [[∞-Dijkgraaf-Witten theories]] is indicated in section 3 and 8 of 

* [[Daniel Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]], in P. Kotiuga (ed.), _A Celebration of the Mathematical Legacy of Raoul Bott,  AMS, (2010) ([arXiv:0905.0731](http://arxiv.org/abs/0905.0731))
 {#FreedHopkinsLurieTeleman09}

and in 

* [[Jacob Lurie]], _Finiteness and ambidexterity in $K(n)$-local stable homotopy theory_, talk at Notre Dame Graduate Summer School on Topology and Field Theories and Harvard lecture 2012

A clear picture of [[fiber integration]] in [[twisted cohomology]] is developed in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG}

A proposal to axiomatize [[perturbative field theory|perturbative]] [[prequantum field theory]] by functors from [[cobordisms]] to a [[symplectic category]] of [[symplectic manifolds]] and [[Lagrangian correspondences]] is in 

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical and quantum Lagrangian field theories with boundary_ ([arXiv:1207.0239](http://arxiv.org/abs/1207.0239), [pdf slides](http://users.uoa.gr/~iandroul/GAP%202012%20WEBPAGE/GAP2012_Cattaneo.pdf))
 {#CattaneoMnevReshetikhin12}


## Related entries

* [[geometry of physics]]

* [[fiber bundles in physics]]

* [[twisted smooth cohomology in string theory]]

* [[motivation for higher differential geometry]]

* [[higher category theory and physics]]

* [[string theory FAQ]]

[[!redirects motives and physics]]
[[!redirects motivic cohomology in physics]]