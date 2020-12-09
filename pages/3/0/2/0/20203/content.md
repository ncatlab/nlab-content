

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[8-manifolds]]. In the low-energy limiting  [[11-dimensional supergravity]] this is KK-compactification to [[3d supergravity]].

Typically this is considered with a [[reduction of the structure group]] on the compactification fiber from [[Spin(8)]] to [[Spin(7)]], in which case one speaks of _M-theory on [[Spin(7)-manifolds]]_ (see the references [below](#ReferencesWithSpin7Structure)). Further reduction to [[G2-structure]] yields [[M-theory on G2-manifolds]].


## Properties

### C-field tadpole cancellation condition

In [[M-theory]] [[KK-compactification|compactified]]  [[compact topological space|compact]] [[8-manifold]] [[fibers]],  [[tadpole cancellation]] for the [[supergravity C-field]] (see also at _[[C-field tadpole cancellation]]_) is equivalently the condition

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \underset{
    I_8(X^8)
  }{
    \underbrace{
      \tfrac{1}{48}\big( p_2 - \tfrac{1}{2}p_1^2  \big)[X^{8}]
    }
  }
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
$$

where

1. $N_{M2}$ is the net number of [[M2-branes]] in the spacetime (whose [[worldvolume]] appears as points in $X^{(8)}$);

1. $G_4$ is the [[field strength]]/flux of the [[supergravity C-field]]

1. $p_1$ is the [[first Pontryagin class]] and $p_2$ the [[second Pontryagin class]] combining to [[I8]], all regarded here in [[rational homotopy theory]].

If $X^{8}$ has 

* [[Spin(7)-structure]] (hence in particular if it is a [[Calabi-Yau manifold]], which has $SU(4) = $ [[Spin(6)]]-structure) 

or 

* [[Sp(2).Sp(1)-structure]] 

then

$$
  \tfrac{1}{2}\big( p_2 - \tfrac{1}{4}(p_1)^2  \big)
  \;=\;
  \chi
$$

is the [[Euler class]] (see [this Prop.](Spin7-manifold#CharacteristicClassesForSpinStructure) and [this Prop.](quaternion-Kähler+manifold#CharacteristicClassesForSpin5Spin3Structure), respectively), hence in these cases the condition is equivalently

$$
  N_{M2}
  \;+\;
  \tfrac{1}{2} \big( G_4[X^{(8)}]\big)^2
  \;=\;
  \tfrac{1}{24}\chi[X^8]
  \;\;\;\;
  \in
  \mathbb{Z}
  \,,
$$

where $\chi[X]$ is the [[Euler characteristic]] of $X$.

For references see [there](C-field+tadpole+cancellation#References).

\linebreak

### Relation to F-theory 
 {#RelationToFTheory}

If the 8-dimensional [[fibers]] themselves are [[elliptic fibrations]], then [[M-theory]] on these 8-manifolds is supposedly [[T-duality|T-dual]] to [[F-theory]] [[KK-compactification|KK-compactified]] to $3+1$ [[spacetime]]-[[dimensions]]. 

In particular, if there is an [[M2-brane]] [[wrapped brane|filling]] the base 2+1-dimensional spacetime, this is supposedly [[T-duality|T-dual]] to a 3+1-dimensional spacetime filling [[D3-brane]] in [[F-theory]] (e.g. [Condeescu-Micu-Palti 14, p. 2](#CondeescuMicuPalti14))

For more on this see at _[[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]_ and at _[[F-theory on Spin(7)-manifolds]]_ and at _[[Witten's Dark Fantasy]]_.

([Bonetti-Grimm-Pugh 13a](#BonettiGrimmPugh13a), [Bonetti-Grimm-Pugh 13b](#BonettiGrimmPugh13b), reviewed in [Pugh](#Pugh))

\linebreak

### Black M2-branes and Exotic 7-spheres
 {#BlackM2BranesAndExotic7Spheres}

The discovery of [[exotic 7-spheres]] proceeded via [[8-manifolds]] $X$ [[manifold with boundary|with boundary]] [[homeomorphism|homeomorphic]] to the [[7-sphere]] $\partial X \simeq_{homeo} S^7$, but not necessarily [[diffeomorphism|diffeomorphic]] to $S^7$ with its canonical [[smooth structure]] (for more see [there](8-manifold#ExoticBoundary7Spheres)).

Hence when regarded from the point of view of [[M-theory on 8-manifolds]], exotic 7-spheres arise as [[near horizon limits]] of peculiar [[black brane|black]] [[M2-brane]] [[spacetimes]] $\mathbb{R}^{2,1} \times X$.

See also [Morrison-Plesser 99, section 3.2](#MorrisonRPlesser99).

### Relation to J-twisted Cohomotopy
 {#RelationToJTwistedCohomotopy}

On a [[spin-manifold]] [[8-manifold|of dimension 8]] a choice of topological [[Spin(7)]]-[[G-structure|structure]] is equivalently a choice of [[cocycle]] in [[J-homomorphism|J-]][[twisted Cohomotopy cohomology theory]]. This follows ([[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation|FSS 19, 3.4]]) from 

1. the standard [[coset space]]-[[structures]] on the [[7-sphere]] (see [here](7-sphere#CosetSpaceRealization)) 

1. the fact that [[coset spaces]] $G/H$ are the [[homotopy fibers]] of the maps $B H \to B G$ of the corresponding [[classifying spaces]] (see [here](coset#ForInfinityGroups))

\begin{imagefromfile}
  "file_name": "ExceptionalSpheres.jpg",
  "width": 730
\end{imagefromfile}




## Related concepts

[[!include KK-compactifications of M-theory -- table]]



* [[M2-M5 brane bound state]]

## References

### General

* {#Witten95} [[Edward Witten]], _Strong Coupling and the Cosmological Constant_, Mod. Phys. Lett.A10:2153-2156, 1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

  (on possible relation to the [[cosmological constant]]: [[Witten's Dark Fantasy]])

* [[Katrin Becker]], [[Melanie Becker]], _M-Theory on Eight-Manifolds_, Nucl. Phys. B477 (1996) 155-167 ([arXiv:hep-th/9605053](https://arxiv.org/abs/hep-th/9605053))

* [[Savdeep Sethi]], [[Cumrun Vafa]], [[Edward Witten]], _Constraints on Low-Dimensional String Compactifications_, Nucl. Phys. B480: 213-224, 1996 ([arXiv:hep-th/9606122](https://arxiv.org/abs/hep-th/9606122))

### In terms of $G$-structure

Discussion in terms of [[G-structures]]:

* {#IshamPope88} [[Chris Isham]], [[Christopher Pope]], _Nowhere Vanishing Spinors and Topological Obstructions to the Equivalence of the NSR and GS Superstrings_, Class. Quant. Grav. 5 (1988) 257 ([spire:251240](http://inspirehep.net/record/251240), [doi:10.1088/0264-9381/5/2/006](https://doi.org/10.1088/0264-9381/5/2/006))

  (focus on [[Spin(7)-structure]])

* {#IshamPopeWarner88} [[Chris Isham]], [[Christopher Pope]], [[Nicholas Warner]], _Nowhere-vanishing spinors and triality rotations in 8-manifolds_,  Classical and Quantum Gravity, Volume 5, Number 10, 1988 ([cds:185144](http://cds.cern.ch/record/185144), [doi:10.1088/0264-9381/5/10/009](https://iopscience.iop.org/article/10.1088/0264-9381/5/10/009))

  (focus on [[Spin(7)-structure]])


* {#CondeescuMicuPalti14} Cezar Condeescu, [[Andrei Micu]], [[Eran Palti]], _M-theory Compactifications to Three Dimensions with M2-brane Potentials_, JHEP 04 (2014) 026 ([arXiv:1311.5901](https://arxiv.org/abs/1311.5901))

* Daniël Prins, [[Dimitrios Tsimpis]], _IIA supergravity and M-theory on manifolds with $SU(4)$ structure_, Phys. Rev. D 89.064030 ([arXiv:1312.1692](https://arxiv.org/abs/1312.1692))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Foliated eight-manifolds for M-theory compactification_, JHEP 01 (2015) 140 ([arXiv:1411.3148](https://arxiv.org/abs/1411.3148))

* C. S. Shahbazi, _M-theory on non-Kähler manifolds_, JHEP 09 (2015) 178 ([arXiv:1503.00733](https://arxiv.org/abs/1503.00733))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Singular foliations for M-theory compactification_, JHEP 03 (2015) 116 ([arXiv:1411.3497](https://arxiv.org/abs/1411.3497))

* [[Elena Babalic]], [[Calin Lazaroiu]], _The landscape of $G$-structures in eight-manifold compactifications of M-theory_, JHEP 11 (2015) 007 ([arXiv:1505.02270](https://arxiv.org/abs/1505.02270))

* [[Elena Babalic]], [[Calin Lazaroiu]], _Internal circle uplifts, transversality and stratified $G$-structures_, JHEP 11 (2015) 174 ([arXiv:1505.05238](https://arxiv.org/abs/1505.05238))



### With $Spin(7)$-structure
  {#ReferencesWithSpin7Structure}

Discussion of [[KK-compactification]] on 8-dimensional [[Spin(7)-manifolds]] (see also at _[[M-theory on G2-manifolds]]_ and at _[[F-theory on Spin(7)-manifolds]]_):

* [[Mirjam Cvetic]], [[Gary Gibbons]], H. Lu, [[Christopher Pope]], _New Complete Non-compact Spin(7) Manifolds_, Nucl. Phys. B620: 29-54, 2002 ([arXiv:hep-th/0103155](https://arxiv.org/abs/hep-th/0103155))

* Jaydeep Majumder, _Type IIA Orientifold Limit of M-Theory on Compact Joyce 8-Manifold of Spin(7)-Holonomy_, JHEP 0201 (2002) 048 ([arXiv:hep-th/0109076](https://arxiv.org/abs/hep-th/0109076))

* [[Ralph Blumenhagen]], [[Volker Braun]], _Superconformal Field Theories for Compact Manifolds with Spin(7) Holonomy_, JHEP 0112:013, 2001 ([arXiv:hep-th/0111048](https://arxiv.org/abs/hep-th/0111048))


* {#GukovSparks02} [[Sergei Gukov]], [[James Sparks]], _M-Theory on $Spin(7)$ Manifolds_, Nucl. Phys. B625 (2002) 3-69 ([arXiv:hep-th/0109025](https://arxiv.org/abs/hep-th/0109025))

* [[Sergei Gukov]], James Sparks, [[David Tong]], _Conifold Transitions and Five-Brane Condensation in M-Theory on $Spin(7)$ Manifolds_, Class. Quant. Grav.20: 665-706, 2003 ([arXiv:hep-th/0207244](https://arxiv.org/abs/hep-th/0207244))

* [[Melanie Becker]], Dragos Constantin, [[Sylvester James Gates Jr.]], William D. Linch III, Willie Merrell, J. Phillips, _M-theory on $Spin(7)$ Manifolds, Fluxes and 3D, $\mathcal{N}=1\,$ Supergravity_, Nucl. Phys. B683 (2004) 67-104 ([arXiv:hep-th/0312040](https://arxiv.org/abs/hep-th/0312040))

* Dragos Constantin, _M-Theory Vacua from Warped Compactifications on $Spin(7)$ Manifolds_, Nucl. Phys. B706: 221-244, 2005 ([arXiv:hep-th/0410157](https://arxiv.org/abs/hep-th/0410157))

* Dragos Constantin, _Flux Compactification of M-theory on Compact Manifolds with $Spin(7)$ Holonomy_, Fortsch. Phys. 53 (2005) 1272-1329 ([arXiv:hep-th/0507104](https://arxiv.org/abs/hep-th/0507104))

* [[Dimitrios Tsimpis]], _M-theory on eight-manifolds revisited: $N=1$ supersymmetry and generalized $Spin(7)$ structures_, JHEP 0604 (2006) 027 ([arXiv:hep-th/0511047](https://arxiv.org/abs/hep-th/0511047))

* S. Salur, O. Santillan, _New $Spin(7)$ holonomy metrics admiting $G_2$ holonomy reductions and M-theory/IIA dualities_, Phys. Rev. D79: 086009, 2009 ([arXiv:0811.4422](https://arxiv.org/abs/0811.4422))

* Adil Belhaj, Luis J. Boya, Antonio Segui, _Holonomy Groups Coming From F-Theory Compactification_, Int J Theor Phys (2010) 49: 681.  ([arXiv:0911.2125](https://arxiv.org/abs/0911.2125))

* Thomas Bruun Madsen, _$Spin(7)$-manifolds with three-torus symmetry_, J. Geom. Phys. 61: 2285-2292, 2011 ([arXiv:1104.3089](https://arxiv.org/abs/1104.3089))

* [[Federico Bonetti]], [[Thomas Grimm]], [[Tom Pugh]], _Non-Supersymmetric F-Theory Compactifications on $Spin(7)$ Manifolds_, JHEP 01 (2014) 112 ([arXiv:1307.5858](https://arxiv.org/abs/1307.5858))

* [[Federico Bonetti]], [[Thomas Grimm]], [[Eran Palti]], [[Tom Pugh]], _F-Theory on $Spin(7)$ Manifolds: Weak-Coupling Limit_, JHEP02(2014)076 ([arXiv:1309.2287](https://arxiv.org/abs/1309.2287))


* {#Pugh} [[Tom Pugh]], _M-theory on $Spin(7)$-manifolds and their F-theory duals_ ([[PughMTheoryOnSpin7.pdf:file]])


* [[Andreas Braun]], [[Sakura Schaefer-Nameki]], _$Spin(7)$-Manifolds as Generalized Connected Sums and 3d $N=1$ Theories_, JHEP 06 (2018) 103 ([arXiv:1803.10755](https://arxiv.org/abs/1803.10755))

  (generalization of [[compact twisted connected sum G2-manifolds]])

See also 

* [[Mariana Graña]], C. S. Shahbazi, [[Marco Zambon]], _$Spin(7)$-manifolds in compactifications to four dimensions_, JHEP 11 (2014) 046 ([arXiv:1405.3698](http://arxiv.org/abs/1405.3698))

Relating [[M-theory on Spin(7)-manifolds]] with [[F-theory on Spin(7)-manifolds]] via [[Higgs bundles]]:

* {#CHRTZ20} [[Mirjam Cvetic]], [[Jonathan Heckman]], Thomas B. Rochais, Ethan Torres, [[Gianluca Zoccarato]], _Geometric Unification of Higgs Bundle Vacua_ ([arXiv:2003.13682](https://arxiv.org/abs/2003.13682))



### With $Sp(2)\cdot Sp(1)$-structure

M-theory on [[HP^2]], hence on a [[quaternion-Kähler manifold]] of dimension 8 with [[holonomy]] [[Sp(2).Sp(1)]], is considered in

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]], p. 75 onwards in  _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177))

and argued to be [[duality in string theory|dual]] to [[M-theory on G2-manifolds]] in three different ways, which in turn is argued to lead to a possible [[proof]] of [[confinement]] in the resulting 4d [[effective field theory]] (see [there](M-theory+on+G2-manifolds#Confinement) for more).

See also

* {#FSS19b} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 4 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

### Witten's Dark Fantasy

For more on the following see at _[[Witten's Dark Fantasy]]_:

An argument for [[non-perturbative effect|non-perturbative]] non-[[supersymmetry|supersymmetric]] 4d [[string phenomenology]] with fundamentally vanishing [[cosmological constant]], based on 3d [[M-theory on 8-manifolds]] decompactified at strong coupling to 4d via [[duality between M-theory and type IIA string theory]] (recall the [[super 2-brane in 4d]]):


* {#Witten00} [[Edward Witten]], p. 7 of: _The Cosmological Constant From The Viewpoint Of String Theory_, lecture at [DM2000](http://inspirehep.net/record/972507), in: David Kline (ed.) _Sources and detection of dark matter and dark energy in the universe 2000_, Springer 2001. 27-36. ([arXiv:hep-ph/0002297](https://arxiv.org/abs/hep-ph/0002297), [doi:10.1007/978-3-662-04587-9](https://link.springer.com/book/10.1007/978-3-662-04587-9))


  (see p. 7)

* [[Edward Witten]], _Strong coupling and the cosmological constant_, Mod. Phys. Lett. A 10:2153-2156, 1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

* [[Edward Witten]], Section 3 of _Some Comments On String Dynamics_, talk at [Strings95](https://cds.cern.ch/record/305869) ([arXiv:hep-th/9507121](http://arxiv.org/abs/hep-th/9507121))

The realization of this scenario in [[F-theory on Spin(7)-manifolds]]:

* [[Cumrun Vafa]], Section 4.3 of: _Evidence for F-Theory_, Nucl. Phys. B469:403-418, 1996 ([arxiv:hep-th/9602022](https://arxiv.org/abs/hep-th/9602022))


* {#BonettiGrimmPugh13a} [[Federico Bonetti]], [[Thomas Grimm]], [[Tom Pugh]], _Non-Supersymmetric F-Theory Compactifications on $Spin(7)$ Manifolds_, JHEP 01 (2014) 112 ([arXiv:1307.5858](https://arxiv.org/abs/1307.5858))

* {#BonettiGrimmPugh13b} [[Federico Bonetti]], [[Thomas Grimm]], [[Eran Palti]], [[Tom Pugh]], _F-Theory on $Spin(7)$ Manifolds: Weak-Coupling Limit_, JHEP 02 (2014) 076 ([arXiv:1309.2287](https://arxiv.org/abs/1309.2287))

* [[Jonathan Heckman]], Craig Lawrie, Ling Lin, [[Gianluca Zoccarato]], _F-theory and Dark Energy_, Fortschritte der Physik  ([arXiv:1811.01959](https://arxiv.org/abs/1811.01959), [doi:10.1002/prop.201900057]( https://doi.org/10.1002/prop.201900057))

* [[Jonathan Heckman]], Craig Lawrie, Ling Lin, Jeremy Sakstein, [[Gianluca Zoccarato]], _Pixelated Dark Energy_ ([arXiv:1901.10489](https://arxiv.org/abs/1901.10489))


### M2-brane spacetimes

* {#MorrisonPlesser99} [[David Morrison]], [[M. Ronen Plesser]], section 3.2 of _Non-Spherical Horizons, I_, Adv. Theor. Math. Phys.3:1-81, 1999 ([arXiv:hep-th/9810201](https://arxiv.org/abs/hep-th/9810201))

### M-theory on $K3 \times K3$

Discussion of M-theory on the [[product manifold]] of two [[K3]]s

* [[Paul Aspinwall]], _An Analysis of Fluxes by Duality_,([arXiv:hep-th/0504036](https://arxiv.org/abs/hep-th/0504036), [spire:679724](https://inspirehep.net/literature/679724))

* [[Paul Aspinwall]], [[Renata Kallosh]], _Fixing All Moduli for M-Theory on $K3 \times K3$_, JHEP 0510:001, 2005 ([arXiv:hep-th/0506014](https://arxiv.org/abs/hep-th/0506014))

  > ([[moduli stabilization]])

* [[Andreas Braun]], Arthur Hebecker, Christoph Ludeling, Roberto Valandro, _Fixing D7 Brane Positions by F-Theory Fluxes_, Nucl. Phys. B815:256-287, 2009 ([arXiv:0811.2416](https://arxiv.org/abs/0811.2416))



[[!redirects M-theory on Spin(8)-manifolds]]
[[!redirects M-theory on Spin(7)-manifolds]]
