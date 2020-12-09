

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

_F-theory_ is a toolbox for describing [[type IIB string theory]] backgrounds -- _including_ [[non-perturbative effects]] induced from the presence of [[D7-branes]] and [[(p,q)-strings]] -- in terms of [[complex numbers|complex]] [[elliptic fibrations]] whose fiber modulus $\tau$ encodes the [[axio-dilaton]] (the [[string coupling constant]] and the degree-0 [[RR-field]]) tranforming under the $SL(2, \mathbb{Z})$ [[S-duality]]/[[U-duality]] [[group]]. See also at _[[duality in string theory]]_.

More technically, F-theory is what results when [[KK-compactification|KK-compactifying]] [[M-theory]] on an [[elliptic fibration]] (which yields [[type IIA superstring theory]] compactified on a [[circle]]-[[fiber bundle]]) followed by [[T-duality]] with respect to one of the two cycles of the elliptic fiber. The result is (uncompactified) [[type IIB superstring theory]] with [[axio-dilaton]] given by the moduli of the original elliptic fibration, see [below](#From11dSupergravity). 

Or rather, this is [[type IIB string theory]] with some [[non-perturbative effects]] included, reducing to [[perturbative string theory]] in the [[Sen limit]]. With a full description of [[M-theory]] available also F-theory should be a full non-perturbative description of type IIB string theory, but absent that it is some kind of approximation. For instance while the [[modular group|modular]] [[structure group]] of the [[elliptic fibration]] in principle encodes (necessarily non-perturbative) [[S-duality]] effects, it is presently not actually known in full detail how this affects the full theory, notably the proper charge quantization law of the 3-form fluxes, see at _[S-duality -- Cohomological nature of the fields under S-duality](S-duality#CohomologicalNatureOfTypeIIFieldsUnderSDuality)_  for more on that.




## Properties

### Relation to M-theory
 {#From11dSupergravity}

The [[duality between M-theory and F-theory]]:

The following line of argument shows why first compactifying M-theory on a torus $S_1^A \times S_1^B$ to get type IIA on a circle and then T-dualizing that circle to get type IIB indeed only depends on the shape $\frac{R_A}{R_B}$ of the torus, but not on its other geometry.

By the [[dualities in string theory]], 10-dimensional [[type II string theory]] is supposed to be obtained from the [[UV-completion]] of [[11-dimensional supergravity]] by first [[Kaluza-Klein mechanism|dimensionally reducing]] over a circle $S^1_A$ -- to obtain [[type IIA supergravity]] -- and then applying [[T-duality]] along another circle $S^1_B$ to obtain [[type IIB supergravity]].

To obtain type IIB sugra in noncompact 10 dimensions this way, also $S^1_B$ is to be compactified (since [[T-duality]] sends the radius $r_A$ of $S^1_A$ to the inverse radius $r_B = \ell_s^2 / R_A$ of $S^1_B$).
Therefore type IIB sugra in $d = 10$ is obtained from 11d sugra compactified on the [[torus]] $S^1_A \times S^1_B$. More generally, this torus may be taken to be an [[elliptic curve]] and this may vary over the 9d base space as an [[elliptic fibration]]. 

Applying T-duality to one of the compact direction yields a 10-dimensional theory which may now be thought of as encoded by a 12-dimensional elliptic fibration. This 12d elliptic fibration encoding a 10d type II supergravity [[vacuum]] is the input data that F-theory is concerned with.

A schematic depiction of this story is the following:

|  |  |  |
|--|--|--|
| [[11d supergravity|M-theory]] in $d = 11$ | | F-theory in $d = 12$ |
| $\downarrow$ [[Kaluza-Klein mechanism|KK-reduction]] along [[elliptic fibration]] | | $\downarrow$ [[axio-dilaton]] is modulus of [[elliptic fibration]] |
| [[type IIA string theory|IIA string theory]] in $d = 9$ | $\leftarrow$[[T-duality]]$\rightarrow$ | [[type IIB string theory|IIB string theory]] in $d = 10$ |

In the simple case where the elliptic fiber is indeed just $S^1_A \times S^1_B$, the [[imaginary part]] of its complex modulus is

$$
  Im(\tau) = \frac{R_A}{R_B}
  \,.
$$

By following through the above diagram, one finds how this determines the [[coupling constant]] in the [[type II string theory]]:

First, the [[KK-compactification]] of [[M-theory]] on $S^1_A$ yields a type IIA [[string coupling]]

$$
  g_{IIA} = \frac{R_A}{\ell_s}
  \,.
$$

Then the T-duality operation along $S^1_B$ divides this by $R_B$:

$$
  \begin{aligned}
    g_{IIB} & = g_{IIA} \frac{\ell_s}{R_B} 
    \\
    & = \frac{R_A}{R_B}
    \\
    & = Im(\tau)
   \end{aligned}
   \,.
$$


#### Relation to M-theory on $G_2$-manifolds

In order to get minimal [[N=1 d=4 supergravity]] after [[KK-compactification]], one needs [[M-theory on G2-manifolds]] and [[F-theory on CY4-manifolds]].

Discussion of the relation between then [[G2-manifold]] fibers for [[M-theory on G2-manifolds]] and the corresponding [[Calabi-Yau manifold|Calabi-Yau 4-manifold]] fibers in F-theory includes ([Gukov-Yau-Zaslow 02](#GukovYauZaslow02), [Belhaj 02](#Belhaj02)). 


#### Relation to heterotic M-theory on ADE-singularities 

Relation to [[heterotic M-theory on ADE-singularities]]:

* [[Monika Marquart]], [[Daniel Waldram]], _F-theory duals of M-theory on $S^1/\mathbb{Z}_2 \times T^4 / \mathbb{Z}_N$_ ([arXiv:hep-th/0204228](https://arxiv.org/abs/hep-th/0204228))

* Christoph Lüdeling, [[Fabian Ruehle]], _F-theory duals of singular heterotic K3 models_, Phys. Rev. D 91, 026010 (2015) ([arXiv:1405.2928](https://arxiv.org/abs/1405.2928))


### Relation to orientifold type II backgrounds
 {#RelationToOrientifolds}

The general [[vacuum]] of [[type II superstring theory]] (including [[type I superstring theory]]) is an [[orientifold]]. 

The [[target space]] data of an [[orientifold]] is a $\mathbb{Z}_2$-[[principal bundle]]/[[local system]], possibly singular (hence possibly on a [[smooth stack]]). On the other hand, the non-singular part of the [[elliptic fibration]] that defines the F-theory is a $SL_2(\mathbb{Z})$-[[local system]] (being the "homological invariant" of the [[elliptic fibration]]). 

An argument due to ([Sen 96](#Sen96), [Sen 97a](#Sen97a)) says that the F-theory data does induce the [[orientifold]] data along the [[subgroup]] inclusion $\mathbb{Z}_2 \hookrightarrow SL_2(\mathbb{Z})$. See at _[[Sen limit]]_. 

The degeneration locus of the elliptic fibration -- where the [[discriminant]] $\Delta$ vanishes and its fibers are the [[nodal curve]] -- is interpreted as that of [[D7-branes]] and [[O-planes|O7-planes]] ([Sen 97a, (3)](#Sen97a), [Blumenhagen 10, (11)](#Blumenhagen10)), exhibiting [[gauge enhancement]] [Sen 97b](#Sen97b) see [below](#SingularLocusAndD7Branes).


Reasoning like this might suggest that in generalization to how type II [[orientifolds]] involve $\mathbb{Z}_2$-[[equivariant]] [[K-theory]] (namely [[KR-theory]]), so F-theory should involve $SL_2(\mathbb{Z})$-equivariant [[elliptic cohomology]]. This was conjectured in ([Kriz-Sati 05, p. 3, p.17, 18](#KrizSati05)). For more on this see at _[[modular equivariant elliptic cohomology]]_. 


### Relation to heterotic string theory

The [[duality between F-theory and heterotic string theory]]:A subclass of K3 manifolds elliptically fibered.

F-theory on an [[elliptic fibration|elliptically fibered]] [[K3]] is supposed to be equivalent to [[heterotic string theory]] [[KK-compactification|compactified]] on a 2-[[torus]]. An early argument for this is due to ([Sen 96](#Sen96)). 

More generally, heterotic string theory on an elliptically fibered Calabi-Yau $Z \to B$ of complex dimension $(n-1)$ is supposed to be equivalent $F$-theory on an $n$-dimensional $X\to B$ with elliptic K3-fibers.

A detailed discussion of the [[equivalence]] of the respective [[moduli spaces]] is originally due to ([Friedman-Morgan-Witten 97](#FriedmanMorganWitten97)). A review of this is in ([Donagi 98](#Donagi98)).


### Singular locus of the elliptic fibration and D7-branes
 {#SingularLocusAndD7Branes}

In passing from [[M-theory]] to [[type IIA string theory]], the locus of any [[Kaluza-Klein monopole]] in 11d becomes the locus of [[D6-branes]] in 10d. The locus of the [[Kaluza-Klein monopole]] in turn (as discussed there) is the locus where the $S^1_A$-circle fibration degenerates. Hence in F-theory this is the locus where the fiber of the $S^1_A \times S^1_B$-[[elliptic fibration]] degenerates to the [[nodal curve]]. Since the [[T-duality|T-dual]] of [[D6-branes]] are [[D7-branes]], it follows that [[D7-branes]] in F-theory "are" the singular locus of the elliptic fibration.

Now an [[elliptically fibered complex K3-surface]] 

$$
  \array{
    T &\longrightarrow& K3
    \\
    && \downarrow
    \\
    && \mathbb{C}\mathbb{P}^1
  }
$$

may be parameterized via the [[Weierstrass elliptic function]] as the solution locus of the equation

$$
  y^2 = x^3 + f(z) x + g(z)
$$

for $x,y,z \in \mathbb{C}\mathbb{P}^1$, with $f$ a [[polynomial]] of degree 8 and $g$ of degree twelve. The [[j-invariant]] of the complex [[elliptic curve]] which this parameterizes for given $z$ is

$$
  j(\tau(z)) = \frac{4 (24 f)^3}{27 g^2 + 4 f^3} 
  \,.
$$

The [[poles]] $j\to \infty$ of the [[j-invariant]] correspond to the [[nodal curve]], and hence it is at these poles that the [[D7-branes]] are located. 

\begin{imagefromfile}
        "file_name": "K3CobordismBetween24ThreeSpheres.jpg",
        "web": "nlab",
        "width": 260,
        "unit": "px",
        "float": "right",
        "margin": {
            "top": -40,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "homotopy pasting diagram exhibiting the homotopy Whitehead integral",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Since the order of the poles is 24 (the polynomial degree of the [[discriminant]] $\Delta = 27 g^2 + 4 f^3$, see at _[[elliptically fibered K3-surface]]  -- [singular points](elliptic+fibration+of+a+K3-surface#SingularPoints)_) there are necessarily _24 D7-branes_ ([Sen 96, page 5](#Sen96), [Sen 97b](#Sen97b), see also [Morrison 04, sections 8 and 17](#Morrison04), [Denef 08, around (3.41)](#Denef08), [Douglas-Park-Schnell 14](duality+between+M%2FF-theory+and+heterotic+string+theory#DouglasParkSchnell14)).

Under [[T-duality]] this translates to 24 [[D6-branes]] in [[type IIA string theory]] on [[K3]] ([Vafa 96, Footnote 2 on p. 6](#Vafa96)).

Notice that the _net charge_ of these 24 D7-branes is supposed to vanish, due to [[S-duality]] effects (e.g. [Denef 08, below (3.41)](#Denef08)).

(This reminds one of the situation for the [[third stable homotopy group of spheres]]...)

For analogous discussion of 24 NS5-branes in [[heterotic string theory]] on [[K3]] see [Schwarz 97, around p. 50](duality+in+string+theory#Schwarz97).



### F-brane scan
 {#Fbranescan}

[[!include F-branes -- table]]

### S-duality operation on $(p,q)$-branes

The F-theory picture gives a geometric interpretation of the [[S-duality]] expected in [[type II string theory]], by which all branes carry _two_ integer charges $(p,q)$ acted on by $SL(2,\mathbb{Z})$. For instance the fundamental string ([[F1-brane]]) and the [[D1-brane]] combine to the $(p,q)$-string, and similarly the [[NS5-brane]] and the [[D5-brane]] combine to a $(p,q)$-5-brane.

Namely in the F-theory picture this comes from [[wrapped brane|wrapping]] the [[M2-brane]] and the [[M5-brane]], respectively, on either of the two cycles of the elliptic fibration (and the [[T-duality|T-dualizing]]).

(e.g. [Johnson 97, p. 4](#Johnson97))


### Model building and phenomenology
 {#ModelBuildingAndPhenomenology}

For F-theory a fairly advanced [[model (physics)|model]] building and [[string phenomenology]] has been developed. A detailed review is in ([Denef 08](#Denef08)).

Via the relation between [[supersymmetry and Calabi-Yau manifolds]] there is particular interest in F-theory compactified on [[Calabi-Yau variety|Calabi-Yau spaces]] of ([[complex manifold|complex]]) [[dimension]] 4. For more on this see at _[[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]_.

A large number of realizations of the exact field content of the [[standard model of particle physics]] (or rather the [[MSSM]]) is claimed to be realized in in F-theory in [Cvetic-Halverson-Lin-Liu-Tian 19](#CveticHalversonLinLiuTian19).


## Related concepts

* [[F'-theory]]

* [[D=12 supergravity]], [[D=14 supersymmetry]], [[bosonic M-theory]]

[[!include F-theory compactifications -- table]]

* [[F-theory on Spin(7)-manifolds]]

## References
 {#References}

### General

Discussion of [[T-duality]] in the strong coupling limit is due to

* {#Schwarz96} [[John Schwarz]], _M Theory Extensions of T Duality_ ([arXiv:hep-th/9601077](https://arxiv.org/abs/hep-th/9601077))

* {#Russo97} [[Jorge Russo]], _T-duality in M-theory and supermembranes_, Phys.Lett. B400 (1997) 37-42 ([arXiv:hep-th/9701188](https://arxiv.org/abs/hep-th/9701188))

That [[S-duality]] of [[type II string theory]] may be interpreted in terms of [[conformal transformations]] on the [[fiber]] for [[M-theory]] compactified on a [[torus]] was originally observed in 

* [[John Schwarz]], _An $SL(2,\mathbb{Z})$-Multiplet of Type IIB Superstrings_, Phys.Lett.B 360:13-18, 1995; ERRATUM-ibid.B364:252, 1995 ([arXiv:hep-th/9508143](https://arxiv.org/abs/hep-th/9508143))

* [[Paul Aspinwall]], _Some Relationships Between Dualities in String Theory_, Nucl.Phys.Proc.Suppl. 46 (1996) 30-38 ([arXiv:hep-th/9508154](https://arxiv.org/abs/hep-th/9508154))

The original article on F-theory as such is

* {#Vafa96} [[Cumrun Vafa]], _Evidence for F-theory_, Nucl. Phys. B469:403-418, 1996, ([arXiv:hep-th/9602022](http://arxiv.org/abs/hep-th/9602022))

An early survey of its relation to [[M-theory]] with [[M5-branes]] is in 

* {#Johnson97} [[Clifford Johnson]], _From M-theory to F-theory, with Branes_, Nucl.Phys. B507 (1997) 227-244 ([arXiv:hep-th/9706155](http://arxiv.org/abs/hep-th/9706155))

A more recent survey is

* {#Blumenhagen10} [[Ralph Blumenhagen]], _Basics of F-theory from the Type IIB Perspective_ ([arXiv:1002.2836](http://arxiv.org/abs/1002.2836))

Lecture notes include

* {#Morrison04} [[David Morrison]], _TASI Lectures on Compactification and Duality_ ([arXiv:hep-th/0411120](http://arxiv.org/abs/hep-th/0411120))

* [[Timo Weigand]], _Lectures on F-theory compactifications and model building_ Class. Quantum Grav. 27 214004 ([arXiv:1009.3497](http://arxiv.org/abs/1009.3497))

* {#Weigand18} [[Timo Weigand]], _TASI Lectures on F-theory_ ([arXiv:1806.01854](https://arxiv.org/abs/1806.01854))




Textbook accounts include

* [[Katrin Becker]], [[Melanie Becker]], [[John Schwarz]], section 8.4 of _String Theory and M-Theory: A Modern Introduction_, 2007

Further survey includes

* [[Timo Weigand]], _F-theory: Progress and Prospects_, 2014 ([pdf](https://www.theorie.physik.uni-muenchen.de/activities/workshops/archive_workshops_conferences/string_pheno_ringberg/slides_frontiers/weigand.pdf))

* {#Vafa15} [[Cumrun Vafa]], _Reflections on F-theory_, 2015 ([pdf](http://wwwth.mpp.mpg.de/conf/f-theory15/talks/Vafa.pdf))


Related conferences include

* _[Physics and Geometry of F-theory 2014](http://www.match.uni-heidelberg.de/GPF/)_

* _[Physics and Geometry of F&#8209;theory 2015](http://f-theory15.mpp.mpg.de)_


### Relation to orientifolds

F-theory lifts of [[orientifold]] backgrounds were first identified in

* {#Sen96} [[Ashoke Sen]], _F-theory and Orientifolds_, Nucl.Phys.B475:562-578,1996 ([arXiv:hep-th/9605150](http://arxiv.org/abs/hep-th/9605150))

* {#Sen97a} [[Ashoke Sen]], _Orientifold Limit of F-theory Vacua_, Nucl. Phys. Proc. Suppl. 68 (1998) 92 (Nucl. Phys. Proc. Suppl. 67 (1998) 81) ([arXiv:hep-th/9702165](http://arxiv.org/abs/hep-th/9702165))

and the corresponding [[gauge enhancement]] in

* {#Sen97b} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

with more details including

* Zurab Kakushadze, [[Gary Shiu]], S.-H. Henry Tye, _Type IIB Orientifolds, F-theory, Type I Strings on Orbifolds and Type I - Heterotic Duality_, Nucl.Phys. B533 (1998) 25-87 ([arXiv:hep-th/9804092](http://arxiv.org/abs/hep-th/9804092))

This is further expanded on in

* [[Hisham Sati]], _The Elliptic curves in gauge theory, string theory, and cohomology_, JHEP 0603 (2006) 096 ([arXiv:hep-th/0511087](http://arxiv.org/abs/hep-th/0511087))


### Relation to elliptic cohomology

A series of articles arguing for a relation between the [[elliptic fibration]] of F-theory and [[elliptic cohomology]] (see also at [[modular equivariant elliptic cohomology]])

* {#KrizSati05} [[Igor Kriz]], [[Hisham Sati]], _Type II string theory and modularity_, 	JHEP 0508 (2005) 038 ([arXiv:hep-th/0501060](http://arxiv.org/abs/hep-th/0501060))

### Relation to heterotic string string theory

* {#FriedmanMorganWitten97} Robert Friedman, [[John Morgan]], [[Edward Witten]], _Vector Bundles And F Theory_ ([arXiv:hep-th/9701162](http://arxiv.org/abs/hep-th/9701162))

* {#Donagi98} [[Ron Donagi]], _ICMP lecture on heterotic/F-theory duality_ ([arXiv:hep-th/9802093](http://arxiv.org/abs/hep-th/9802093))

### Relation to M-theory on $G_2$-manifolds

* {#GukovYauZaslow02} [[Sergei Gukov]], [[Shing-Tung Yau]], [[Eric Zaslow]], _Duality and Fibrations on $G_2$ Manifolds_ ([arXiv:hep-th/0203217](http://arxiv.org/abs/hep-th/0203217))

* {#Belhaj02} Adil Belhaj, _F-theory Duals of M-theory on $G_2$ Manifolds from Mirror Symmetry_ ([arXiv:hep-th/0207208](http://arxiv.org/abs/hep-th/0207208))

* [[Mariana Graña]], C. S. Shahbazi, [[Marco Zambon]], _$Spin(7)$-manifolds in compactifications to four dimensions_, JHEP11(2014)046 ([arXiv:1405.3698](http://arxiv.org/abs/1405.3698))


### Relation to the 6d superconformal theory

Realization to the [[6d (2,0)-supersymmetric QFT]] is discussed in

* {#HeckmannMorrisonVafa13} Jonathan Heckman, [[David Morrison]], [[Cumrun Vafa]], _On the Classification of 6D SCFTs and Generalized ADE Orbifolds_ ([arXiv:1312.5746](http://arxiv.org/abs/1312.5746))

### Phenomenology and model building
 {#ReferencesPhenomnenology}

A large body of literature is concerned with particle physics [[string phenomenology]] modeled in the context of F-theory, in particular [[GUTs]]:

* {#Denef08} [[Frederik Denef]], _Les Houches Lectures on Constructing String Vacua_, in _[[String theory and the real world]]_ ([arXiv:0803.1194](http://arxiv.org/abs/0803.1194), [spire:780946](https://inspirehep.net/literature/780946))

* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_, JHEP 0901:058,2009 ([arXiv:0802.3391](http://arxiv.org/abs/0802.3391))


* [[Chris Beasley]], [[Jonathan Heckman]], [[Cumrun Vafa]], _GUTs and Exceptional Branes in F-theory - I_ ([arxiv:0802.3391](http://arxiv.org/abs/0802.3391)), _II: Experimental Predictions_ ([arxiv:0806.0102](http://arxiv.org/abs/0806.0102))

* {#Wijhnholt14} [[Martin Wijnholt]], _String compactification_, [PITP 2014](https://pitp2014.ias.edu) lecture notes ([[WijnholtCompactification14.pdf:file]], [slides for lecture 1](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P1_wijnholt.pdf), [slides for lecture 2](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P2_wijnholt.pdf), [slides for lecture 3](https://static.ias.edu/pitp/2014/sites/pitp2014.ias.edu/files/PITP2014_P3_wijnholt.pdf))

* {#Zoccarato14} Gianluca Zoccarato, _Yukawa couplings at the point
of $E_8$ in F-theory_, 2014 ([pdf](http://stringpheno2014.ictp.it/parallels/tuesday/F-theory(B)/zoccarato.pdf))

Discussion of the _exact_ [[gauge group]] of the [[standard model of particle physics]], $G = \big( SU(3) \times SU(2) \times U(1)\big)/\mathbb{Z}_6 $ including its $\mathbb{Z}_6$-[[quotient group|quotient]] (see [there](standard+model+of+particle+physics#GaugeGroup)) and the exact [[fermion]] field content, realized in F-theory is in

* Denis Klevers, Damian Kaloni Mayorga Pena, Paul-Konstantin Oehlmann, Hernan Piragua, Jonas Reuter, _F-Theory on all Toric Hypersurface Fibrations and its Higgs Branches_, JHEP01(2015)142 ([arXiv:1408.4808](https://arxiv.org/abs/1408.4808))

* {#CveticLin17} [[Mirjam Cvetic]], Ling Lin, section 3.3 of _The global gauge group structure of F-theory compactifications with $U(1)$s_ ([arXiv:1706.08521](https://arxiv.org/abs/1706.08521))


Based on this large number of realizations of the exact field content of the [[standard model of particle physics]] (or rather [[MSSM]]) in [[F-theory]] is claimed to be realized in

* {#CveticHalversonLinLiuTian19} [[Mirjam Cvetic]], [[James Halverson]], Ling Lin, Muyang Liu, Jiahua Tian, _A Quadrillion Standard Models from F-theory_ ([arXiv:1903.00009](https://arxiv.org/abs/1903.00009))

* {#TaylorTurner19} [[Washington Taylor]], Andrew P. Turner, _Generic construction of the Standard Model gauge group and matter representations in F-theory_ ([arXiv:1906.11092](https://arxiv.org/abs/1906.11092))

#### Cosmological constant


An argument for [[non-perturbative effect|non-perturbative]] non-[[supersymmetry|supersymmetric]] 4d [[string phenomenology]] with fundamentally vanishing [[cosmological constant]], based on 3d [[M-theory on 8-manifolds]]
decompactified at strong coupling to 4d via [[duality between M-theory and type IIA string theory]] (recall the [[super 2-brane in 4d]]):

* {#Witten00} [[Edward Witten]], _The Cosmological Constant From The Viewpoint Of String Theory_, lecture at [DM2000](http://inspirehep.net/record/972507) ([arXiv:hep-ph/0002297](https://arxiv.org/abs/hep-ph/0002297))

  (see p. 7)

* [[Edward Witten]], _Strong coupling and the cosmological constant_, Mod. Phys. Lett. A 10:2153-2156, 1995 ([arXiv:hep-th/9506101](https://arxiv.org/abs/hep-th/9506101))

* [[Edward Witten]], Section 3 of _Some Comments On String Dynamics_, talk at [Strings95](https://cds.cern.ch/record/305869) ([arXiv:hep-th/9507121](http://arxiv.org/abs/hep-th/9507121))

The realization of this scenario in [[F-theory]]:

* [[Cumrun Vafa]], Section 4.3 of: _Evidence for F-Theory_, Nucl. Phys. B469:403-418, 1996 ([arxiv:hep-th/9602022](https://arxiv.org/abs/hep-th/9602022))

* [[Jonathan Heckman]], Craig Lawrie, Ling Lin, Gianluca Zoccarato, _F-theory and Dark Energy_, Fortschritte der Physik  ([arXiv:1811.01959](https://arxiv.org/abs/1811.01959), [doi:10.1002/prop.201900057]( https://doi.org/10.1002/prop.201900057))

* [[Jonathan Heckman]], Craig Lawrie, Ling Lin, Jeremy Sakstein, Gianluca Zoccarato, _Pixelated Dark Energy_ ([arXiv:1901.10489](https://arxiv.org/abs/1901.10489))

#### Flavour anomalies

Realization in [[F-theory]] of [[GUT]]-models with [[Z'-bosons]] and/or [leptoquarks]] addressing the [[flavour anomalies]] and the [(g-2) anomalies](anomalous+magnetic+moment#Anomalies):

* Miguel Crispim Romao, Stephen F. King, George K. Leontaris, _Non-universal $Z'$ from Fluxed GUTs_, Physics Letters B Volume 782, 10 July 2018, Pages 353-361 ([arXiv:1710.02349](https://arxiv.org/abs/1710.02349))

* A. Karozas, G. K. Leontaris, I. Tavellaris, N. D. Vlachos, _On the LHC signatures of $SU(5) \times U(1)'$ F-theory motivated models_ ([arXiv:2007.05936](https://arxiv.org/abs/2007.05936))



### 4-Form flux and instantons
 {#FluxAndInstantons}

The image of the [[supergravity C-field]] from [[11-dimensional supergravity]] to F-theory yields the _$G_4$-[[flux compactification|flux]]_.

* Andres Collinucci, Raffaele Savelli, _On Flux Quantization in F-Theory_ (2010) ([arXiv:1011.6388](http://arxiv.org/abs/1011.6388))

* Sven Krause, Christoph Mayrhofer, [[Timo Weigand]], _$G_4$ flux, chiral matter and singularity resolution in F-theory compactifications_ ([arXiv:1109.3454](http://arxiv.org/abs/1109.3454))

* {#GKP12} [[Thomas Grimm]], Denis Klevers, Maximilian Poretschkin, _Fluxes and Warping for Gauge Couplings in F-theory_ ([arXiv:1202.0285](http://arxiv.org/abs/1202.0285))

* {#KMW12} Sven Krause, Christoph Mayrhofer, [[Timo Weigand]], _Gauge Fluxes in F-theory and Type IIB Orientifolds_ (2012) ([arXiv:1202.3138](http://arxiv.org/abs/1202.3138))

and with [[M5-brane]] [[instanton]] contributions:

* Max Kerstan, [[Timo Weigand]], _Fluxed M5-instantons in F-theory_ ([arXiv:1205.4720](http://arxiv.org/abs/1205.4720))

Reviewed in

* {#Weigand12} [[Timo Weigand]], _Fluxes and M5-instantons in F-theory_, 2012 ([pdf slides](http://people.physik.hu-berlin.de/~ahoop/weigand.pdf))

For more on this see also at _[[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]_.