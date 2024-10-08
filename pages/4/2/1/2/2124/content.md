
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
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

### General
 {#General}

In [[supersymmetry|supersymmetric]] [[quantum field theory]] with [[extended supersymmetry]], certain extremal [[supermultiplets]] have some of the [[supersymmetry|supersymmetries]] retained (have 0-[[eigenvalue]] under some of the [[supersymmetry]] generators). These are called __Bogomol'nyi--Prasad--Sommerfield saturated solutions__. 

More in detail, where in a plain [[supersymmetry]] [[super Lie algebra]] a suitable [[basis]] $\{Q_A\}$ of supersymmetry generators has odd bracket proportional to the spacetime translation and hence to an [[energy]]/[[mass]] operator $E$ (with terminology as at [[unitary representation of the Poincaré group]])

$$
 \{Q_A, Q_B\} = E \delta_{A B}
$$

for [[extended supersymmetry]] there are further bosonic super Lie algebra generators $K_{A B}$ (charges) such that

$$
 \{Q_A, Q_B\} = E \delta_{A B} -  K_{A B}
 \,.
$$

It follows from the supersymmetry algebra that $(E \delta_{A B} -  K_{A B})$ is a positive definite [[bilinear form]], which puts a lower bound on the [[energy]] given the values of these extra charges. This is called the _BPS bound_. See also at _[[Bridgeland stability condition]]_.

In particular when this bound is satisfied in that some of the [[eigenvalues]] of the [[matrix]] $(K_{A B})$ are actually equal to the energy/mass, then the corresponding component of the right hand side in the above equation vanishes and hence then the corresponding supersymmetry generators may annihilate the given state, then called a _BPS state_. This way enhanced supersymmetry of states goes along with certain charges taken extremal values.


States with similar behaviour are also considered also in some models of [[soliton]] theory
(English Wikipedia: [Bogomol'nyi&#8211;Prasad&#8211;Sommerfield bound](http://en.wikipedia.org/wiki/Bogomol'nyi%E2%80%93Prasad%E2%80%93Sommerfield_bound)). 

BPS states play a central role in the investigation of [[moduli spaces]] of classical [[vacua]] as they form part of the moduli problem which is often the most tractable.

Several mathematical theories in [[geometry]] are interpreted as counting BPS-states in the sense of integration on appropriate compactification of the [[moduli space]] of BPS-states in a related physical model attached to the underlying geometry: most notably the [[Gromov-Witten invariants]], [[Donaldson-Thomas invariants]] and the [[Thomas-Pandharipande invariants]]; all the three seem to be deeply interrelated though they are defined in rather very different terms. The compactification of the moduli space involves various [[stability conditions]]. 


### In supergravity

In the context of [[supergravity]] BPS states correspond to [[super spacetimes]] admitting [[Killing vectors]]. These notably include extremal [[black brane]] solutions.

### In superstring theory

Specifically in [[superstring theory]] BPS states in [[target space]] correspond to string states on the worldsheet which are annihilated by the left-moving (say) half of the [[Dirac-Ramond operator]]. These are counted by the [[Witten genus]], see at _[Witten genus -- Relation to BPS states](Witten+genus#RelationToBPSStateCounting)_.

The degeneracy of BPS states in string theory has been used to provide a microscopic interpretation of [[Bekenstein-Hawking entropy]] of [[black holes]], see at _[[black holes in string theory]]_.

## Formalization in higher differential geometry
 {#InTermsOfHigherDifferentialGeometry}

> The following are some observations on the formalization of BPS states from the [[nPOV]], in [[higher differential geometry]], following ([Sati & Schreiber 2015](#SatiSchreiber15)).

Let $\mathbb{R}^{d-1,1|N}$ be a [[super-Minkowski spacetime]], let $(d,N,p)$ be in the [[brane scan]] and write

$$
  \phi \coloneqq \bar{\psi} \wedge E^{\wedge p} \wedge \psi \in \Omega^{p+2}(\mathbb{R}^{d-1,1|N})
$$

for the correspoding [[super Lie algebra]] [[Lie algebra cohomology|cocycle]], as discussed at _[[Green-Schwarz action functional]]_, see ([FSS 13](#FSS13)) for the perspective invoked here.

Consider then $X$ a [[super-spacetime]] locally modeled on $\mathbb{R}^{d-1,1|N}$ as a [[Cartan geometry]], solving the relevant [[supergravity]] [[equations of motion]] (e.g. [[11-dimensional supergravity]] for $d= 11$, [[heterotic supergravity]] for $d = 10$ and $N = (1,0)$, [[type IIA supergravity]] for $d = 10$ and $N= (1,1)$ or [[type IIB supergravity]] for $d = 10$ $N= (2,0)$).

This means in particular that $X$ carries a [[super differential form]]

$$
  \omega \in \Omega^{p+2}(X)
$$

which is [[definite form|definite]] on $\phi$. This is the [[curvature]] of the [[WZW-term]] which defines the relevant [[super p-brane sigma-model]] with [[target space]] $X$.

By ([AGIT 89](#AGIT89)) $X$ is a BPS state to the extent that it carries [[Killing spinors]] which form a central [[Lie algebra extension]] of a sub-algebra of the [[supersymmetry]] algebra (i.e. of the [[super translation Lie algebra]]) by $H^p_{dR}(X)$ which is classified by the [[Lie algebra cohomology|cocycle]] given by

$$
  (\epsilon_1, \epsilon_2) \mapsto
  \omega(\epsilon_1,\epsilon_2)
  \in 
  \Omega^p(X)_{cl}/im(\mathbf{d}_{dR})
  \,.
$$

Now we observe that by ([hgpII, theorem 3.3.1](#hgpII)) this is precisely the [[0-truncation]] of the [[super L-infinity algebra|super]]-[[Poisson bracket Lie n-algebra]] $\mathfrak{Pois}(X,\omega)$ induced by regarding $(X,\omega)$ as an [[pre-n-plectic manifold|pre-n-plectic]] [[supermanifold]] and restricting along the inclusion of the [[Killing vectors]]/[[Killing spinors]] into all the [[Hamiltonian vector fields]].

$$
  H^p_{dR}(X) \to \tau_0 \mathfrak{Pois}(X,\omega) \to Vect_{Ham}(X)
$$

(Here we are using that if an [[n-type]] is an extension of a [[0-type]], then its 0-truncation is still an extension by the 0-truncation of the original homotopy fiber.)

The elements in $H^p_{dR}(X)$ here are precisely the $p$-brane charges, as discussed in ([AGIT 89, p. 8](#AGIT89)).

Hence $X$ is the more BPS the more odd-graded elements there are in $\tau_0 \mathfrak{Pois}(X,\omega)$ (or its restriction to super-isometries). Hence $X$ is a 1/2 BPS state of supergravity if the odd dimension of this is half that of $\mathbb{R}^{d-1,d|N}$, it is 1/4 BPS if the odd dimension is one fourth of that of $\mathbb{R}^{d-1,d|N}$, etc.

Notice that if 

$$
  \array{
    &&     
     \mathbf{B}^{p+1} (\mathbb{R}/\Gamma)_{conn}
    \\
    &  {}^{\mathllap{\mathbf{L}_{WZW}}}\nearrow & \downarrow^{\mathrlap{F_{(-)}}}   
    \\
    X 
    &\stackrel{\omega}{\longrightarrow}&
    \mathbf{\Omega}^{p+2}_{cl}
  } 
$$

is a [[prequantum line n-bundle|prequantization]] of $\omega$, i.e. an actual [[WZW term]] with [[curvature]] $\omega$, then $\mathfrak{Pois}(X,\omega)$ is supposed to be the [[Lie differentiation]] of the [[stabilizer group]] of $\mathbf{L}_{WZW}$, which is the [[quantomorphism n-group]] $QuantMorph(\mathbf{L}_{WZW})$. (This Lie differentiation statement is strictly shown only for $p = 0$ and $p = 1$ in [[schreiber:differential cohomology in a cohesive topos|dcct]] but clearly should hold generally.)

Hence we may regard $\mathbf{QuantMorph}(\mathbf{L}_{WZW})$ (or its restriction to super-[[isometries]]) as the [[Lie integration]] of the brane-charge extended supersymmetry algebra. By the discussion at _[conserved current -- In higher differential geometry](conserved+current#InHigherPrequantumGeometry)_ this is indeed the [[n-group]] of conserved currents of $\mathbf{L}_{WZW}$ regraded as a [[local Lagrangian]], and so this conceptually connects back to the considerations in ([AGIT 89](#AGIT89)).



## Examples

### In 11d Supergravity 

In [[11-dimensional supergravity]] ([[M-theory]]) there are four kinds of 1/2 BPS states (the [[black brane|black]] [[M-branes]]) (e.g. [Stelle 98, section 3](#Stelle98) [EHKNT 07](#EHKNT07)):

* the [[M2-brane]];

* the [[M5-brane]];

* the [[M-wave]];

* the [[Kaluza-Klein monopole]].

## Related concepts

* [[Bridgeland stability condition]]

* [[Killing spinor]]

* [[supermultiplet]]

* [[wall crossing]]

* [[protection from quantum corrections]]

* [[positive energy theorem]]

* [[enhanced gauge symmetry]]

* [[geometry of physics -- BPS charges]]

* [[intersecting branes]]

  [[membrane triple junction]]

## References

### General

The BPS bound derives its name from the discussion of [[magnetic monopoles]] in 4-dimensional [[Yang-Mills theory]] in 

* [[Е. Б. Богомольный]], _&#1059;&#1089;&#1090;&#1086;&#1081;&#1095;&#1080;&#1074;&#1086;&#1089;&#1090;&#1100; &#1082;&#1083;&#1072;&#1089;&#1089;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1093; &#1088;&#1077;&#1096;&#1077;&#1085;&#1080;&#1081;_, &#1071;&#1076;. &#1060;&#1080;&#1079; __24__ (1976) 449-454

  Engl. tanslation:

  [[Evgeny B. Bogomolnyj]], *Stability of classical solutions*, Sov. J. Nucl. Phys. **24** (1976) 449  and Yad. Fiz. 24 (1976) 861-870 &lbrack;[spire:101280](https://inspirehep.net/literature/101280)&rbrack;

  reprinted in:

  *Solitons and Particles*, World Scientific (1984) 389-394 &lbrack;[doi:10.1142/0046](https://doi.org/10.1142/0046)&rbrack;

* [[Manoj K. Prasad]], [[Charles Sommerfield]], *Exact classical solution for 't Hooft monopole and the Julia-Zee dyon*, Phys. Rev. Lett. __35__ (1975) 760-762 &lbrack;[doi:10.1103/PhysRevLett.35.760](https://doi.org/10.1103/PhysRevLett.35.760)&rbrack;


The extension of the term "BPS-saturated state" from this case to situations in [[string theory]] seems to have happened in 

* {#Witten95} [[Edward Witten]], around (2.5) of _[[String Theory Dynamics In Various Dimensions]]_, Nucl. Phys. B **443** (1995) 85-126 &lbrack;[arXiv:hep-th/9503124](https://arxiv.org/abs/hep-th/9503124)&rbrack;

The original article identifying the role of BPS states in [[supersymmetry|supersymmetric]] [[field theory]]:

* [[Edward Witten]], [[David Olive]], _Supersymmetry algebras that include topological charges_ (2002) ([journal](http://www.sciencedirect.com/science/article/pii/037026937890357X))

Exposition and review includes

* [[Andrew Neitzke]], _What is a BPS state?_, 2012 ([pdf](http://www.ma.utexas.edu/users/neitzke/expos/bps-expos.pdf))

* {#Dimofte10} [[Tudor Dimofte]], _Refined BPS invariants, Chern-Simons theory, and the quantum dilogarithm_, 2010 ([pdf](http://thesis.library.caltech.edu/5808/1/DimofteTDofficial.pdf), [web](http://thesis.library.caltech.edu/5808/))


Further developments:

*  [[Jeffrey Harvey]], [[Greg Moore]], _Algebras, BPS states, and strings_, Nucl.Phys. B **463** (1996) 315-368 &lbrack;[doi:10.1016/0550-3213%2895%2900605-2](http://doi.org/10.1016/0550-3213%2895%2900605-2), [hep-th/9510182](https://arxiv.org/abs/hep-th/9510182)&rbrack; 

*  [[Jeffrey Harvey]], [[Greg Moore]], _On the algebras of BPS states_, Comm. Math. Phys. __197__ (1998), 489&#8211;-519, [doi](https://doi.org/10.1007/s002200050461), [hep-th/9609017](https://arxiv.org/abs/hep-th/9609017).

* [[Ali Chamseddine]], M. S. Volkov, *Non-abelian BPS monopoles in $\mathcal{N}=4$ gauged supergravity*, Physical Review Letters **79** 3343&-3346 (1997) &lbrack;[hep-th/9707176](http://arxiv.org/abs/hep-th/9707176)&rbrack;

* [[Steven Weinberg]], _The quantum theory of fields_, vol. II

* [[Tudor Dimofte]], [[Sergei Gukov]], _Refined, Motivic, and Quantum_, [arXiv:0904.1420](http://arXiv.org/abs/0904.1420) 

* [[Davide Gaiotto]], [[Gregory Moore]], [[Andrew Neitzke]], _Wall-crossing, Hitchin systems, and the WKB approximation_, [arxiv:0907.3987](https://arxiv.org/abs/0907.3987)

* R. Pandharipande, R. P. Thomas, _Stable pairs and BPS invariants_, [arXiv:0711.3899](https://arxiv.org/abs/0711.3899)

* [[Markus Reineke]], _Cohomology of quiver moduli, functional equations, and integrality of Donaldson-Thomas type invariants_, Compositio Mathematica __147__:3 (2011) 943--964 [doi](https://doi.org/10.1112/S0010437X1000521X) [arXiv:0903.0261](https://arXiv.org/abs/0903.0261)

* Duiliu-Emanuel Diaconescu, _Moduli of ADHM sheaves and local Donaldson-Thomas theory_, J. Geom. & Physics __62__:4 (2012) 763--799 [arXiv:0801.0820](https://arXiv.org/abs/0801.0820) f[doi](https://doi.org/10.1016/j.geomphys.2011.12.018)

* [[Tom Bridgeland]], _Stability conditions on triangulated categories_, Ann. of Math. 166 (2007) 317&#8211;345,[math.AG/0212237](https://arxiv.org/abs/math/0212237)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Stability structures, motivic Donaldson-Thomas invariants and cluster transformations_, [arXiv:0811.2435](https://arxiv.org/abs/0811.2435)

* [[Maxim Kontsevich]], [[Yan Soibelman]], _Motivic Donaldson-Thomas invariants: summary of results_, in: Mirror Symmetry and Tropical Geometry, Contemp. Math. __527__ (2010) [doi](https://doi.org/10.1090/conm/527/10400) [arxiv/0910.4315](https://arxiv.org/abs/0910.4315)

* [[Dominic Joyce]], Y. Song, _A theory of generalized Donaldson-Thomas invariants_,  [arxiv/0810.5645](https://arxiv.org/abs/0810.5645)


### Introductions, surveys and lectures
 {#IntroductoryReferences}

An introduction that starts at the beginning and then covers much of the ground in some detail is

* [[Greg Moore]], _PiTP Lectures on BPS states and wall-crossing in $d = 4$, $\mathcal{N} = 2$ theories_ ([pdf](http://www.physics.rutgers.edu/~gmoore/PiTP_July26_2010.pdf))


A survey of progress on the most general picture is in 

* Katzutoshi Ohta, _BPS state counting and related physics_ (2005) ([pdf](http://www2.yukawa.kyoto-u.ac.jp/~qft/2005/slides/ohta.pdf))



### In supergravity

Discussion of extremal/BPS [[black branes]] in [[supergravity]] (especially in [[11-dimensional supergravity]] and 10d [[type II supergravity]]) includes

* {#Stelle98} [[Kellogg Stelle]], _BPS Branes in Supergravity_, in: *Quantum Field Theory: Perspective and Prospective*, NATO Science Series **530**, Springer (1999) &lbrack;[arXiv:hep-th/9803116](http://arxiv.org/abs/hep-th/9803116), [doi:10.1007/978-94-011-4542-8_12](https://doi.org/10.1007/978-94-011-4542-8_12)&rbrack;

* {#GauntlettHull99} [[Jerome Gauntlett]], [[Chris Hull]], _BPS states with extra supersymmetry_, JHEP 0001 (2000) 004 &lbrack;[arXiv:hep-th/9909098](https://arxiv.org/abs/hep-th/9909098) [doi:10.1088/1126-6708/2000/01/004](https://doi.org/10.1088/1126-6708/2000/01/004)&rbrack;

* {#EHKNT07} [[Francois Englert]], [[Laurent Houart]], [[Axel Kleinschmidt]], [[Hermann Nicolai]], Nassiba Tabti, _An $E_9$ multiplet of BPS states_, JHEP 0705:065 (2007) &lbrack;[arXiv:hep-th/0703285](https://arxiv.org/abs/hep-th/0703285)&rbrack;

* Andrew Callister, [[Douglas Smith]], _Topological BPS charges in 10 and 11-dimensional supergravity_, Phys. Rev. D **78** 065042 (2008) &lbrack;[arXiv:0712.3235](https://arxiv.org/abs/0712.3235)&rbrack;

* Andrew Callister, [[Douglas Smith]], _Topological charges in $SL(2,\mathbb{R})$ covariant massive 11-dimensional and Type IIB SUGRA_, Phys.Rev.D80:125035,2009 ([arXiv:0907.3614](http://arxiv.org/abs/0907.3614))

* Andrew Callister, _Topological BPS charges in 10- and 11-dimensional supergravity_, thesis 2010 ([spire](http://inspirehep.net/record/1221591?ln=en))


* Cristine N. Ferreira, _BPS solution for eleven-dimensional supergravity with a conical defect configuration_ ([arXiv:1312.0578](https://arxiv.org/abs/1312.0578))


Specifically for $1/2^n$-BPS states of intersecting [[M-branes]] in 11d there is discussion in 

* {#Tseytlin96} [[Arkady Tseytlin]], _Harmonic superpositions of M-branes_, Nucl.Phys.B475:149-163,1996 ([arXiv:hep-th/9604035](https://arxiv.org/abs/hep-th/9604035)) also in [[Mike Duff]] (ed.) chapter 5 of _[[The World in Eleven Dimensions]]_

see also 

* [[Jerome Gauntlett]], _Intersecting Branes_ ([hep-th/9705011](https://arxiv.org/abs/hep-th/9705011))

* [[Igor Bandos]], [[José de Azcárraga]], [[José Izquierdo]], [[Jerzy Lukierski]], _BPS states in M-theory and twistorial constituents_, Phys. Rev. Lett. __86__ (2001) 4451-4454 &lbrack;[arXiv:hep-th/0101113](https://arxiv.org/abs/hep-th/0101113)&rbrack;

* [[Ulf Gran]], [[Jan Gutowski]], [[George Papadopoulos]], _Classification, geometry and applications of supersymmetric backgrounds_ &lbrack;[arXiv:1808.07879](https://arxiv.org/abs/1808.07879)&rbrack;

Semiclassical approach:

* T. Daniel Brennan, [[Gregory W. Moore]], _A note on the semiclassical formulation of BPS states in four-dimensional N = 2 theories_, Prog. Theor. Exp. Phys. 2016, 12C110 (19 pages) [doi](https://doi.org/10.1093/ptep/ptw159)

Discussion in the context of multiple [[M2-branes]] in the  [[BLG model]] is in

* {#BaggerLambert12} [[Jonathan Bagger]], [[Neil Lambert]], Sunil Mukhi, Constantinos Papageorgakis, section 1.6 of _Multiple Membranes in M-theory_ ([arXiv:1203.3546](https://arxiv.org/abs/1203.3546))

Discussion for [[4d supergravity]], hence in [[KK-compactification]] of [[type II supergravity]] on a [[Calabi-Yau manifold]] is due to

* {#Denef00} [[Frederik Denef]], _Supergravity flows and D-brane stability_, JHEP 0008:050, 2000 ([arXiv:hep-th/0005049](http://arxiv.org/abs/hep-th/0005049))

* [[Frederik Denef]], _Quantum Quivers and Hall/Hole Halos_, JHEP 0210:023, 2002 ([arXiv:hep-th/0206072](http://arxiv.org/abs/hep-th/0206072))


Discussion of more general classification of solutions to [[supergravity]] preserving some [[supersymmetry]], i.e. admitting some [[Killing spinors]] includes
 
* [[Jerome Gauntlett]], Stathis Pakis, _The Geometry of $D=11$ Killing Spinors_, JHEP 0304 (2003) 039 ([arXiv:hep-th/0212008](http://arxiv.org/abs/hep-th/0212008))

* {#HEGKS08} [[Eric D'Hoker]], John Estes, Michael Gutperle, Darya Krym, Paul Sorba, _Half-BPS supergravity solutions and superalgebras_, JHEP 0812:047 (2008) &lbrack;[arXiv:0810.1484](http://arxiv.org/abs/0810.1484), [doi:10.1088/1126-6708/2008/12/047](https://iopscience.iop.org/article/10.1088/1126-6708/2008/12/047)&rbrack;

The conceptual identification of the relevant brane-charge extension of the [[supersymmetry]] algebra as that of the [[conserved currents]] of the [[Green-Schwarz super p-brane sigma models]] for branes is due to

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], [[José Izquierdo|J. M. Izquierdo]], [[Paul Townsend]], _Topological extensions of the supersymmetry algebra for extended objects_, Phys. Rev. Lett. __63__ (1989) 2443 &lbrack;[spire](https://inspirehep.net/record/26393?ln=en)&rbrack;

reviewed in  

* [[José de Azcárraga]], [[José Izquierdo|Jos&#233; M. Izquierdo]], section 8.8. of _Lie groups, Lie algebras, cohomology and some applications in physics_ , Cambridge monographs of mathematical physics (1995)

This is for branes in the old [[brane scan]] ([[strings]], [[membranes]], [[NS5-branes]]), excluding [[D-branes]] and [[M5-brane]].

The generalization oft this perspective to the [[M5-brane]] is discussed in 

* {#SorokinTownsend97} [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys.Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

and the generalization to [[D-branes]] is discussed in

* {#Hammer97} Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))

Detailed discussion of examples for various backgrounds is in 

* Takeshi Sato, _Superalgebras in Many Types of M-Brane Backgrounds and Various Supersymmetric Brane Configurations_, Nucl.Phys. B548 (1999) 231-257 ([arXiv:hep-th/9812014](https://arxiv.org/abs/hep-th/9812014))

Discussion of this in [[higher differential geometry]] via the [[Poisson bracket Lie n-algebra]] is in 

* {#SatiSchreiber15} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lie n-algebras of BPS charges]]_,  J. High Energ. Phys. **2017** 87 (2017) &lbrack;[arXiv:1507.08692](http://arxiv.org/abs/1507.08692), <a href="http://link.springer.com/article/10.1007/JHEP03(2017)087">doi:10.1007/JHEP03(2017)087</a>&rbrack;

Discussion of relation of [[M5-brane]] BPS states to [[knot invariants]] includes

* [[Edward Witten]], _Fivebranes and Knots_ ([arXiv:1101.3216](http://arxiv.org/abs/1101.3216))

* [[Sergei Gukov]], Marko Sto&#353;i&#263;, _Homological algebra of knots and BPS states_, GTM __18__ (2012) 309--367 ([arXiv:1112.0030](https://arxiv.org/abs/1112.0030) [doi](https://doi.org/10.2140/gtm.2012.18.309))

* Ross Elliot, [[Sergei Gukov]], _Exceptional knot homology_ ([arXiv:1505.01635](https://arxiv.org/abs/1505.01635))


### Spectral networks
 {#SpectralNetworksReferences}

* [[Davide Gaiotto]], [[Greg Moore]], [[Andrew Neitzke]], _Spectral networks_ ([arXiv:1204.4824](http://arxiv.org/abs/1204.4824), 
[illustrating animations](http://www.ma.utexas.edu/users/neitzke/spectral-network-movies/))


[[!redirects BPS state]]
[[!redirects BPS states]]
[[!redirects BPS-states]]
[[!redirects BPS-state]]

[[!redirects BPS invariant]]
[[!redirects BPS invariants]]

[[!redirects BPS charge]]
[[!redirects BPS charges]]

[[!redirects BPS brane]]
[[!redirects BPS branes]]

[[!redirects BPS solution]]
[[!redirects BPS solutions]]

[[!redirects half-BPS solution]]
[[!redirects half-BPS solutions]]

