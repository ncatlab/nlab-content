
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[Kaluza-Klein reduction]] of [[11-dimensional supergravity]] on [[G2 manifolds]] (notably [[Freund-Rubin compactifications]] and variants) yields an [[effective field theory|effective]] $N=1$ [[4-dimensional supergravity]] with [[gauge fields]] (arising from the KK-modes of the [[graviton]]) and charged [[fermions]] (arising from the KK-models of the [[gravitino]]). This construction is thought to lift to [[M-theory]] as the analog of the KK-compactification of [[heterotic string theory]] on [[Calabi-Yau manifolds]] (see at _[[string phenomenology]]_), and of [[F-theory on CY4-manifolds]].

[[!include N=1 susy compactifications -- table]]

In order for this to yield [[phenomenology|phenomenologically]] interesting effective physics the compactification space must be a [[G2-orbifold]] (hence a [[Riemannian orbifold]] of [[special holonomy]]), its [[stabilizer groups]] will encode the [[nonabelian group|nonabelian]] [[gauge group]] of the effective theory by "[[geometric engineering of quantum field theory]]" ([Acharya 98](#Acharya98), [Atiyah-Witten 01, section 6](#AtiyahWitten01)), see [below](#EnhancedGaugeGroups). Specifically for discussion of [[string phenomenology]] obtaining or approximating the [[standard model of particle physics]] by this procedure see at _[[G2-MSSM]]_.


## Details
 {#G2Manifolds}

### Vacuum solutions
 {#VacuumSolutionsAndTorsion}

Genuine [[G2-manifold]]/[[orbifold]] fibers, these having vanishing [[Ricci curvature]], correspond to [[vacuum]] solutions of the [[Einstein equations]] of [[11d supergravity]], i.e. with vanishing [[field strength]] of the [[gravitino]] and the [[supergravity C-field]] (see e.g. [Acharya 02, p. 9](#Acharya02)).
(If one includes non-vanishing $C$-field strength one finds "weak $G_2$-holonomy" instead, see [below](#TheCField)).

Notice that vanishing [[gravitino]] [[field strength]] (i.e. [[covariant derivative]]) means that the [[torsion of a Cartan connection|torsion]] of the super-[[vielbein]] is in each [[tangent space]] the canonical torsion of the [[super Minkowski spacetime]]. This [[supergravity torsion constraint|torsion constraint]] already just for the bosonic part $(E^a)$ of the super-vielbein $(E^a, E^\alpha)$ implies (together with the [[Bianchi identities]]) the [[equations of motion]] of supergravity, hence here the vacuum [[Einstein equations]] in the 11d [[spacetime]]. 

### Complexified moduli space
{#ComplexifiedModuli} 

For vanishing [[field strength]] of the [[supergravity C-field]], the formal linear combination 

$$
  \tau \coloneqq C_3 + i \phi_3
$$

of the (flat) supergravity $C$-field $C_3$ and the the 3-form $\phi_3$ of the $G_2$-structure is the natural [[holomorphic function|holomorphic coordinate]] on the [[moduli space]] of the [[KK-compactification]] of a $G_2$-manifold, in M-theoretic higher analogy of the complexified K&#228;hler classes of CY compactifications of 10d string theory ([Harvey-Moore 99, (2.7)](#HarveyMoore99), [Acharya 02, (32) (59) (74)](#Acharya02), [Grigorian-Yau 08, (4.57)](#GrigorianYau08), [Acharya-Bobkov 08, (4)](#AcharyaBobkov08)).

Notice that restricted to [[associative submanifolds]] this combination becomes $C_3 + i vol$, which also governs the [[membrane instanton]]-contributions ("[[complex volume]]").


### Nonabelian gauge groups and chiral fermions at orbifold singularities
 {#EnhancedGaugeGroups}

The [[KK-compactification]] of vacuum [[11-dimensional supergravity]] on a _[[smooth manifold|smooth]]_ [[G2-manifold]] $Y$ results in a [[effective field theory|effective]] [[N=1 D=4 super Yang-Mills theory]] with [[abelian group|abelian]] [[gauge group]] $U(1)^{b_2(Y)}$ and with $b_3(Y)$ [[complex scalar fields]] which are neutral (not charged) under this gauge group (with $b_\bullet(Y)$ the [[Betti numbers]] of $Y$) (e.g. [Acharya 02, section 2.3](#Acharya02)). This is of course unsuitable for [[phenomenology]].


But when $Y$ is a $G_2$-[[orbifold]] then: 

1. at an [[ADE singularity]] there is _[[enhanced gauge symmetry]] in that the [[gauge group]] (which a priori is copies of the [[abelian group]] $U(1)$ of the [[supergravity C-field]]) becomes [[nonabelian group|nonabelian]] ([Acharya 98](#Acharya98), [Acharya 00](#Acharya00), review includes [Acharya 02, section 3](#Acharya02), [BBS 07, p. 422, 436](#BBS07), [Ib&#225;&#241;ez-Uranga 12, section 6.3.3](string+phenomenology#IbanezUranga12), [Wijnholt 14, part III](string+phenomenology#Wijnholt14) (from which the graphics below is grabbed));

1. at a (non-orbifold) [[conical singularity]] [[chiral fermions]] appear ([Witten 01, p. 3](#Witten01), [Atiyah-Witten 01](#AtiyahWitten01), [Acharya-Witten 01](#AcharyaWitten01), [Berglund-Brandhuber 02](#BerglundBrandhuber02),  [Bourjaily-Espahbodi 08](#BourjailyEspahbodi08)).

| [[ADE-singularity]] |  [[conical singularity]] |
|---------------------|--------------------------|
|  [[gauge enhancement]] | [[chiral fermions]]   |

The [[conical singularities]] are supposed/assumed to be isolated ([Witten 01, section 2](#Witten01)), while the [[ADE singularities]] are supposed/assumed to be of [[codimension]]-4 in the 7-dimensional fibers ([Witten 01, section 3](#Witten01), [Barrett 06](#Barrett06)).

In the absence of a proper microscopic definition of M-theory, the first point is argued for indirectly in at least these ways: 

1. The fact that under [[KK-compactification]] to [[type IIA string theory]] the singularity becomes special points of intersecting [[D6-branes]] for which the gauge enhancement is known ([Sen 97](#Sen97), [Witten 01, p. 1](#Witten01), based on [Cvetic-Shiu-Uranga 01](#CveticShiuUranga01)).

1. The [[duality in string theory|duality]] between M-theory compactified on [[K3]] and [[heterotic string theory]] on a 3-torus ([Acharya-Witten 01](#AcharyaWitten01)). Here it is fairly well understood that at the degeneration points of the K3-[[moduli space]] enhanced nonabelian gauge symmetry appears (e.g. [Acharya-Gukov 04, section 5.1](#AcharyaGukov04)). This comes down ([Intriligator-Seiberg 96](ALE+space#IntriligatorSeiberg96)) to the fact that an [[ADE singularity]] $\mathbb{C}^2/\Gamma$ generically constitutes a point in the [[moduli space]] of [[vacua]] in the [Higgs branch](N%3D2+D%3D4+super+Yang-Mills+theory#ModuliSpacesOfVacua) of a super Yang-Mills theory.

1. {#Blowup} <div style="float:left;margin:0 10px 10px 0;"><img src="http://ncatlab.org/nlab/files/ADESingularity.jpg" width="600" alt="ADE 2Cycle" /></div> The [[blow-up]] of an [[ADE-singularity]] happens to be a union of [[2-spheres]] touching pairwise in one point, such as to form the [[Dynkin diagram]] of the [[simple Lie group]] which under the [[ADE classification]] corresponds to the given [[orbifold]] isotropy group. 

   (graphics grabbed from [HSS18](http://ncatlab.org/schreiber/show/Equivariant+homotopy+and+super+M-branes))

   [[M2-branes]] may [[wrapped brane|wrap]] these 2-cycles and since before blow-up they are of vanishing size, this corresponds to [[double dimensional reduction]] under which the M2-branes become [[strings]] stretching between coincident [[D-branes]]. These are well-understood to be the quanta of nonabelian gauge [[Chan-Paton gauge fields]] located on the D-branes, and hence these same nonabelian degrees of freedom have had to be present already at the level of the M2-branes. This is due to ([Sen 97](#Sen97)), for more see at _[[M-theory lift of gauge enhancement on D6-branes]]_.

1. In the [[F-theory]] description the ADE singularity maps to the locus where the F-theory [[elliptic fibration]] degenerates with 2-cycles in the elliptic fibers shrinking to 0. Via [[double dimensional reduction]] this manifestly takes the [[M2-brane]] [[wrapped brane|wrapping]] these elliptic fibers to an [[open string]] stretching between [[D7-branes]]. This yields at least $SU(N)$ gauge symmetry by the usual string theory argument about [[Chan-Paton gauge fields]].

Also notice that at least the $SU(N)$-enhancement of the [[effective field theory]] at $\mathbb{Z}_k$-singularities matches the $SU(N)$-enhancement of the [[worldvolume]] theory of $N$-coincident [[M2-branes]] sitting at the orbifold singularity: this is the statement of the [[ABJM model]].



### Solutions with non-vanishing $C$-field strength
 {#TheCField}

{#FluxBreaksSuSy} **Claim:** _There is no warped [[KK-compactification]] of M-theory on $X_4 \times F_7$ which retains at least $N = 1$ [[supersymmetry]] in 4d while at the same time having non-vanishing $G_4$-[[flux]] ([[field strength]] of the [[supergravity C-field]]). In other words, non-vanishing flux always breaks the supersymmetry._

e.g. ([Acharya-Spence 00](#AcharyaSpence00)) see the Introduction of ([Beasley-Witten 02](#BeasleyWitten02))

$\,$


In compactifications with [[weak G2 holonomy]] it is the defining 4-form $\phi_4$ (the one which for strict [[G2 manifolds]] is the [[Hodge star operator|Hodge dual]] of the [[associative 3-form]]) which is the [[flux]]/[[field strength]] of the [[supergravity C-field]]. See for instance ([Bilal-Serendinger-Sfetos 02, section 6](#BilalDerendingerSfetos)):

Consider a [[KK-compactification]]-Ansatz $X_{11} = (X_4,g_4) \times (X_7,g_7)$ and

* $F_4 = f vol_{X_4}$;

* $F_7 = \tilde g e_7^\ast \phi_4$

where $e_4$, $e_7$ are given [[vielbein]] fields on $X_4$ and $X_7$ and $\phi_4$ is the [[Hodge star operator|Hodge dual]] of the [[associative 3-form]]. Then the [[Einstein equations]] of [[11-dimensional supergravity]] give

$$
  R_4 = - \frac{1}{3}\left(f^2 + \frac{7}{2} \tilde g^2\right) g_4
$$

$$
  R_7 = \frac{1}{6}\left(f^2 + 5 \tilde g^2\right) g_7
$$

(where $g_4$, $g_7$ is the [[pseudo-Riemannian metric|metric tensor]]) saying that both spaces are [[Einstein manifolds]] ([BSS 02, (5.4)](#BilalDerendingerSfetos)). The [[equations of motion]] for the [[supergravity C-field]] is

$$
  \tilde g\left(
     d \phi - f \star\phi
  \right)
  = 0
$$

for $\phi = e_7^\ast \phi_3$ the pullback of the [[associative 3-form]] ([BSS 02, (5.5)](#BilalDerendingerSfetos)), saying that $\phi \propto \star F_7$ exhibits [weak G2-holonomy](G2+manifold#WeakG2Holonomy) with weakness parameter given by the component of the  [[C-field]] on $X_4$.

### Confinement?
 {#Confinement}

An idea for a strategy towards a proof of [[confinement]] in [[N=1 D=4 super Yang-Mills theory]] via two different but conjecturally equivalent realizations as [[M-theory on G2-manifolds]] has been given in [Atiyah-Witten 01, section 6](#AtiyahWitten01), review is in [Acharya-Gukov 04, section 5.3](#AcharyaGukov04).

The idea here is to consider a [[KK-compactification]] of [[M-theory]] on [[fibers]] which are [[G2-manifolds]] that locally around a special point 
are of the form

$$
  X_{1,\Gamma} 
  \;\coloneqq\;
  \big( S^3 / \Gamma \big) \times Cone\big(S^3\big)
  \phantom{AA}
  \text{or}
  \phantom{AA}
  X_{2,\Gamma} 
  \;\coloneqq\;
  S^3 \times Cone\big(S^3/\Gamma\big)
$$

where 

* $\Gamma$ is a [[finite subgroup of SU(2)]] that [[action|acts]] canonically by left-multiplication on $S^3 \simeq $ [[SU(2)]];

* $Cone(\cdots)$ denotes the [[metric cone]] construction.

This means that $X_{1,\Gamma}$ is a [[smooth manifold]], but $X_{2,\Gamma}$, as soon as $\Gamma$ is not the [[trivial group]], $\Gamma \neq 1$, is an [[orbifold]] with an [[ADE singularity]].

Now the lore of [[M-theory on G2-manifolds]] predicts that [[KK-compactification]]

1.  on $X_{1,\Gamma}$ yields a 4d theory without massless fields (since there are no massless modes on the [[covering space]] $S^3$ of $X_{1,\Gamma}$)

1. on the [[ADE-singularity]] $X_{2,\Gamma}$ yields [[non-abelian group|non-abelian]] [[Yang-Mills theory]] in 4d coupled to [[chiral fermions]].

both of these [[duality in string theory|dual]] by thinking of them in two different ways as [[M-theory on 8-manifolds|M-theory on the 8-manifold]] [[HP^2]] ([Atiyah-Witten 01, p. 75 onwards](#AtiyahWitten01)).

So in the first case a [[mass gap]] is manifest, while non-abelian gauge theory is not visible, while in the second case it is the other way around.

But if there were an argument that [[M-theory on G2-manifolds]] is in fact equivalent for compactification both on $X_{1,\Gamma}$ and on $X_{2,\Gamma}$. To the extent that this is true, it looks like an argument that could demonstrate confinement in non-abelian 4d gauge theory.

This approach is suggested in [Atiyah-Witten 01, pages 84-85](#AtiyahWitten01). An argument that this equivalence is indeed the case is then provided in sections 6.1-6.4, based on an argument in [Atiyah-Maldacena-Vafa 00](#AtiyahMaldacenaVafa00).



### Relation to intersecting D-brane models

relation to [[intersecting D-brane models]]: see [there](intersecting+D-brane+model#ReferencesLiftToMTheory)

## Related concepts

* [[G2]]

* [[G2 manifold]], [[generalized G2-manifold]]

* [[G2-MSSM]]

* [[Freund-Rubin compactification]]

* [[exceptional generalized geometry]]

* [[topological M-theory]], [[Hitchin functional]]

* [[7d Chern-Simons theory]]

[[!include KK-compactifications of M-theory -- table]]

## References
 {#References}

### General

The first discussion of [[KK-compactification]] of [[11d supergravity]] on  [[fibers]] with [[G2-holonomy]] is due to:

* {#AwadaDuffPope83} M. A. Awada, [[Mike Duff]], [[Christopher Pope]], _$N=8$ Supergravity Breaks Down to $N=1$_, Phys. Rev. Lett. 50, 294 (1983) ([doi:10.1103/PhysRevLett.50.294](https://doi.org/10.1103/PhysRevLett.50.294))

* [[Mike Duff]], [[Bengt Nilsson]], [[Christopher Pope]], _Spontaneous Supersymmetry Breaking by the Squashed Seven-Sphere_, Phys. Rev. Lett. 50, 2043 (1983) ([doi:10.1103/PhysRevLett.50.2043](https://doi.org/10.1103/PhysRevLett.50.2043), [erratum](https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.51.846))

  > (compactification on a [[squashed sphere|squashed]] [[7-sphere]] with $G_2$-holonomy)

More generally, the [[KK-compactification]] of [[11d supergravity]] of [[fibers]] of [[special holonomy]] was originally considered in

* [[Edward Witten]], _Search for a realistic Kaluza-Klein theory_, Nuclear Physics B Volume 186, Issue 3, 10 August 1981, Pages 412-428 (<a href="https://doi.org/10.1016/0550-3213(81)90021-3">doi:10.1016/0550-3213(81)90021-3</a>)

* {#DauriaFreCastellani91} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], chapter V.6 of _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991)

* [[George Papadopoulos]], [[Paul Townsend]], _Compactification of D=11 supergravity on spaces of exceptional holonomy_, Phys. Lett. B357:300-306,1995 ([arXiv:hep-th/9506150](http://arxiv.org/abs/hep-th/9506150))

Dedicated [[string phenomenology]] for the case of compactification on [[G2-manifolds]] (or rather [[orbifolds]]) goes back to:

* {#Acharya98} [[Bobby Acharya]], _M theory, Joyce Orbifolds and Super Yang-Mills_, Adv. Theor. Math. Phys. 3 (1999) 227-248 ([arXiv:hep-th/9812205](http://arxiv.org/abs/hep-th/9812205))

* {#Acharya00} [[Bobby Acharya]], _On Realising $N=1$ Super Yang-Mills in M theory_ ([arXiv:hep-th/0011089](http://arxiv.org/abs/hep-th/0011089))

* {#AcharyaSpence00} [[Bobby Acharya]], B. Spence, _Flux, Supersymmetry and M theory on 7-manifolds_ ([arXiv:hep-th/0007213](http://arxiv.org/abs/hep-th/0007213))

* {#Acharya02} [[Bobby Acharya]], _M Theory, $G_2$-manifolds and four-dimensional physics_,  Classical and Quantum Gravity Volume 19 Number 22, 2002  ([doi:10.1088/0264-9381/19/22/301](https://iopscience.iop.org/article/10.1088/0264-9381/19/22/301/meta), [pdf](http://users.ictp.it/~pub_off/lectures/lns013/Acharya/Acharya_Final.pdf))

* {#AtijayMaldacenaVafa00} [[Michael Atiyah]], [[Juan Maldacena]], [[Cumrun Vafa]], _An M-theory Flop as a Large N Duality_, J. Math. Phys.42:3209-3220, 2001 ([arXiv:hep-th/0011256](https://arxiv.org/abs/hep-th/0011256))

* {#BeasleyWitten02} [[Chris Beasley]], [[Edward Witten]], _A Note on Fluxes and Superpotentials in M-theory Compactifications on Manifolds of $G_2$ Holonomy_, JHEP 0207:046,2002 ([arXiv:hep-th/0203061](http://arxiv.org/abs/hep-th/0203061))

* {#AtiyahWitten01} [[Michael Atiyah]], [[Edward Witten]] _$M$-Theory dynamics on a manifold of $G_2$-holonomy_, Adv. Theor. Math. Phys. 6 (2001) ([arXiv:hep-th/0107177](http://arxiv.org/abs/hep-th/0107177), [doi:10.4310/ATMP.2002.v6.n1.a1]( https://dx.doi.org/10.4310/ATMP.2002.v6.n1.a1))

* {#Witten01} [[Edward Witten]], _Anomaly Cancellation On Manifolds Of $G_2$ Holonomy_ ([arXiv:hep-th/0108165](http://arxiv.org/abs/hep-th/0108165))

* {#AcharyaWitten01} [[Bobby Acharya]], [[Edward Witten]], _Chiral Fermions from Manifolds of $G_2$ Holonomy_ ([arXiv:hep-th/0109152](http://arxiv.org/abs/hep-th/0109152), [spire:563029](https://inspirehep.net/literature/563029))

* {#BerglundBrandhuber02} Per Berglund, Andreas Brandhuber, _Matter from $G_2$-manifolds_, Nucl. Phys. B641 (2002) 351-375 ([arXiv:hep-th/0205184](https://arxiv.org/abs/hep-th/0205184))

* {#Barrett06} Adam B. Barrett, _M-Theory on Manifolds with $G_2$ Holonomy_, 2006 ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))

* {#BourjailyEspahbodi08} Jacob L. Bourjaily, Sam Espahbodi, _Geometrically Engineerable Chiral Matter in M-Theory_ ([arXiv:0804.1132](https://arxiv.org/abs/0804.1132))

Expanding on [Atiyah-Witten 01](#AtiyahWitten01):

* [[Bobby Acharya]], Lorenzo Foscolo, Marwan Najjar, Eirik Eik Svanes, _New $G_2$-conifolds in M-theory and their Field Theory Interpretation_ ([arXiv:2011.06998](https://arxiv.org/abs/2011.06998))


See also:

* {#Sen97} [[Ashoke Sen]], _A Note on Enhanced Gauge Symmetries in M- and String Theory_, JHEP 9709:001,1997 ([arXiv:hep-th/9707123](http://arxiv.org/abs/hep-th/9707123))

* [[Mirjam Cvetic]], [[Gary Gibbons]], H. L&#252;  and [[Christopher Pope]], _Supersymmetric M3-branes and G2 Manifolds_ ([pdf](http://cdsweb.cern.ch/record/503160/files/0106026.pdf))

* {#AcharyaDenefHofmanLambert03} [[Bobby Acharya]], F. Denef, C. Hofman, [[Neil Lambert]], _Freund-Rubin Revisited_ ([arXiv:hep-th/0308046](http://arxiv.org/abs/hep-th/0308046))

More discussion of the non-abelian gauge group enhancement at [[orbifold]] singularities includes

* {#CveticShiuUranga01} [[Mirjam Cvetic]], [[Gary Shiu]], [[Angel Uranga]], _Chiral Four-Dimensional $N=1$ Supersymmetric Type IIA Orientifolds from Intersecting D6-Branes_, Nucl. Phys. B615:3-32,2001 ([arXiv:hep-th/0107166](http://arxiv.org/abs/hep-th/0107166))

* {#HalversonMorrison15} [[James Halverson]], [[David Morrison]], _On Gauge Enhancement and Singular Limits in $G_2$ Compactifications of M-theory_ ([arXiv:1507.05965](http://arxiv.org/abs/1507.05965))

* [[Antonella Grassi]], [[James Halverson]], Julius L. Shaneson, _Matter From Geometry Without Resolution_, Journal of High Energy Physics October 2013, 2013:205 ([arXiv:1306.1832](http://arxiv.org/abs/1306.1832))

* [[Neil Lambert]], Miles Owen, _Charged Chiral Fermions from M5-Branes_ ([arXiv:1802.07766](https://arxiv.org/abs/1802.07766))

* {#BCHS19} [[Andreas Braun]], Sebastjan Cizel, Max Hubner, [[Sakura Schafer-Nameki]], _Higgs Bundles for M-theory on G2-Manifolds_ ([arXiv:1812.06072](https://arxiv.org/abs/1812.06072))

* Max Hubner, _Local $G_2$-Manifolds, Higgs Bundles and a Colored Quantum Mechanics_ ([arXiv:2009.07136](https://arxiv.org/abs/2009.07136))

Discussion in relation to the [[duality between M-theory and heterotic string theory]]:

* [[Bobby Acharya]], Alex Kinsella, [[David Morrison]], *Non-Perturbative Heterotic Duals of M-Theory on $G_2$ Orbifolds* ([arXiv:2106.03886](https://arxiv.org/abs/2106.03886))



Discussion of [[Freund-Rubin compactification]] on $\mathbb{R}^4 \times X_7$ "with flux", hence non-vanishing [[supergravity C-field]] and how they preserve one supersymmetry if $X_7$ is of [[weak G2 holonomy]] with $\lambda$ = [[cosmological constant]] = C-[[field strength]] on $\mathbb{R}^4$ is in:

* {#BilalDerendingerSfetos} [[Adel Bilal]], J.-P. Derendinger, K. Sfetsos, _(Weak) $G_2$ Holonomy from Self-duality, Flux and Supersymmetry_, Nucl.Phys. B628 (2002) 112-132 ([arXiv:hep-th/0111274](http://arxiv.org/abs/hep-th/0111274))
 
* {#HouseMicu04} Thomas House, Andrei Micu, _M-theory Compactifications on Manifolds with $G_2$ Structure_ ([arXiv:hep-th/0412006](http://arxiv.org/abs/hep-th/0412006))

Further discussion of [[membrane instantons]] in this context includes

* [[Gottfried Curio]], _Superpotentials for M-theory on a G_2 holonomy manifold and Triality symmetry_, JHEP 0303:024,2003 ([arXiv:hep-th/0212211](http://arxiv.org/abs/hep-th/0212211))


Survey and further discussion includes

* [[Michael Duff]], _M-theory on manifolds of G2 holonomy: the first twenty years_ ([arXiv:hep-th/0201062](http://arxiv.org/abs/hep-th/0201062))


* [[Sergei Gukov]], _M-theory on manifolds with exceptional holonomy_, Fortschr. Phys. 51 (2003), 719&#8211;731 ([pdf](http://research.physics.unc.edu/string/gukov.pdf))




* {#AcharyaGukov04} [[Bobby Acharya]], [[Sergei Gukov]], _M theory and Singularities of Exceptional Holonomy Manifolds_, Phys.Rept.392:121-189,2004 ([arXiv:hep-th/0409191](http://arxiv.org/abs/hep-th/0409191))

* Adil Belhaj, _M-theory on G2 manifolds and the method of (p, q) brane webs_ (2004) ([web](http://iopscience.iop.org/0305-4470/37/18/011))

* Adam B. Barrett, _M-Theory on Manifolds with $G_2$ Holonomy_ ([arXiv:hep-th/0612096](http://arxiv.org/abs/hep-th/0612096))
 
* [[James Halverson]], [[David Morrison]], _The Landscape of M-theory Compactifications on Seven-Manifolds with $G_2$ Holonomy_ ([arXiv:1412.4123](http://arxiv.org/abs/1412.4123))

* Aaron Kennon, _$G_2$-Manifolds and M-Theory Compactifications_ ([arXiv:1810.12659](https://arxiv.org/abs/1810.12659))

The corresponding [[membrane]] [[instanton]] corrections to the [[superpotential]] are discussed in 

* {#HarveyMoore99} [[Jeffrey Harvey]], [[Greg Moore]], _Superpotentials and Membrane Instantons_ ([arXiv:hep-th/9907026](http://arxiv.org/abs/hep-th/9907026))

* {#BBS07} [[Katrin Becker]], [[Melanie Becker]], [[John Schwarz]], p. 333 of _String Theory and M-Theory: A Modern Introduction_, 2007

Discussion of [[duality in string theory|duality]] with [[F-theory on CY4-manifolds]] includes

* {#GukovYauZaslow02} [[Sergei Gukov]], [[Shing-Tung Yau]], [[Eric Zaslow]], _Duality and Fibrations on $G_2$ Manifolds_ ([arXiv:hep-th/0203217](http://arxiv.org/abs/hep-th/0203217))

* {#Belhaj02} Adil Belhaj, _F-theory Duals of M-theory on $G_2$ Manifolds from Mirror Symmetry_ ([arXiv:hep-th/0207208](http://arxiv.org/abs/hep-th/0207208))

* [[Mariana Graña]], C. S. Shahbazi, [[Marco Zambon]], _$Spin(7)$-manifolds in compactifications to four dimensions_, JHEP11(2014)046 ([arXiv:1405.3698](http://arxiv.org/abs/1405.3698))

Discussion of [[duality in string theory|duality]] with [[heterotic string theory on CY3-manifolds]]:

* {#BraunSchaeferNameki17} [[Andreas Braun]], Sakura Schaefer-Nameki, _Compact, Singular G2-Holonomy Manifolds and M/Heterotic/F-Theory Duality_, JHEP04(2018)126 ([arXiv:1708.07215](https://arxiv.org/abs/1708.07215))

The [[moduli space]] is discussed in

* {#GrigorianYau08} [[Sergey Grigorian]], [[Shing-Tung Yau]], _Local geometry of the $G_2$ moduli space_, Commun.Math.Phys.287:459-488,2009 ([arXiv:0802.0723](http://arxiv.org/abs/0802.0723))

* {#AcharyaBobkov08} [[Bobby Acharya]], Konstantin Bobkov, _K&#228;hler Independence of the G2-MSSM_, HEP 1009:001,2010 ([arXiv:0810.3285](http://arxiv.org/abs/0810.3285))

* [[Spiro Karigiannis]], [[Naichung Conan Leung]]_, _Hodge Theory for $G_2$-manifolds: Intermediate Jacobians and Abel-Jacobi maps_, Proceedings of the London Mathematical Society (3) 99, 297-325 (2009) ([arXiv:0709.2987](http://arxiv.org/abs/0709.2987) [talk slides pdf](http://www.math.uwaterloo.ca/~karigian/talks/g2modulispace.pdf)


### Phenomenology
 {#ReferencesPhenomenology}

Popular exposition of the [[G2-MSSM]] [[phenomenology]] is in

* {#Kane17} [[Gordon Kane]], _String theory and the real world_, Morgan & Claypool, 2017 (<a href="http://iopscience.iop.org/book/978-1-6817-4489-6">doi:0.1088/978-1-6817-4489-6</a>)

Further discussion of [[string phenomenology]] in terms of $M$-theory on $G_2$-manifolds, beyond the original ([Acharya 98](#Acharya98), [Atiyah-Witten 01](#AtiyahWitten01), [Acharya-Witten 01](#AcharyaWitten01)), includes

* {#AcharyaKaneKumar12} [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_, Int. J. Mod. Phys. A, Volume 27 (2012) 1230012 ([arXiv:1204.2795](http://arxiv.org/abs/1204.2795))

* {#Acharya12} [[Bobby Acharya]], _$G_2$-manifolds at the CERN Large Hadron collider and in the Galaxy_, talk at _$G_2$-days_ (2012) ([pdf](http://www.mth.kcl.ac.uk/~tbmadsen/acharya.pdf))

* {#Kane16} [[Gordon Kane]], _String/M-theories About Our World Are Testable in the traditional Physics Way_ ([arXiv:1601.07511](http://arxiv.org/abs/1601.07511), [video recording](https://videoonline.edu.lmu.de/en/node/7485))




Discussion of [[moduli stabilization]] for stabilization via "[[flux]]" (non-vanishing bosonic  [[field strength]] of the [[supergravity C-field]]) is in

* {#Acharya02} [[Bobby Acharya]], _A Moduli Fixing Mechanism in M theory_ ([arXiv:hep-th/0212294](http://arxiv.org/abs/hep-th/0212294))

and [[moduli stabilization]] for fluxless compactifications via [[nonperturbative effects]], claimed to be sufficient and necessary to solve the [[hierarchy problem]], is discussed in

* {#AcharyaBobkovKaneKumarVaman06} [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Diana Vaman, _An M theory Solution to the Hierarchy Problem_, Phys.Rev.Lett.97:191601,2006 ([arXiv:hep-th/0606262](http://arxiv.org/abs/hep-th/0606262))

* {#AcharyaBobkovKaneKumarShao07} [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _Explaining the Electroweak Scale and Stabilizing Moduli in M Theory_, Phys.Rev.D76:126010,2007 ([arXiv:hep-th/0701034](http://arxiv.org/abs/hep-th/0701034))

* {#AcharyaKumarBobbkovKaneShaoWatson08} [[Bobby Acharya]], [[Piyush Kumar]], Konstantin Bobkov, [[Gordon Kane]], Jing Shao, Scott Watson, _Non-thermal Dark Matter and the Moduli Problem in String Frameworks_,JHEP 0806:064,2008 ([arXiv:0804.0863](http://arxiv.org/abs/0804.0863))

and specifically for the [[G2-MSSM]] in

* [[Bobby Acharya]], Konstantin Bobkov, [[Gordon Kane]], [[Piyush Kumar]], Jing Shao, _The $G_2$-MSSM - An $M$ Theory motivated model of Particle Physics_ ([arXiv:0801.0478](http://arxiv.org/abs/0801.0478))


the [[strong CP problem]] is discussed in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], section 6 of _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))


* [[Bobby Acharya]], Konstantin Bobkov, [[Piyush Kumar]], _An M Theory Solution to the Strong CP Problem and Constraints on the Axiverse_, JHEP 1011:105,2010 ([arXiv:1004.5138](http://arxiv.org/abs/1004.5138))

and realization of [[GUTs]] in

* {#Witten02} [[Edward Witten]], _Deconstruction, $G_2$ Holonomy, and Doublet-Triplet Splitting_, ([arXiv:hep-ph/0201018](http://arxiv.org/abs/hep-ph/0201018))

* [[Bobby Acharya]], Krzysztof Bozek, Miguel Crispim Romao, Stephen F. King, Chakrit Pongkitivanichkul, _$SO(10)$ Grand Unification in M theory on a $G_2$ manifold_ ([arXiv:1502.01727](http://arxiv.org/abs/1502.01727))

The phenomenology of compactifications on [[compact twisted connected sum G2-manifolds]] ([Kovalev 00](G2+manifold#Kovalev00)) is in

* {#GHKY17} Thaisa C. da C. Guio, [[Hans Jockers]], [[Albrecht Klemm]], Hung-Yu Yeh, _Effective action from M-theory on twisted connected sum $G_2$-manifolds_ ([arXiv:1702.05435](https://arxiv.org/abs/1702.05435), [talk video](https://lecture2go.uni-hamburg.de/l2go/-/get/v/21906)) 

Discussion of the [[cosmological constant]] in these models includes

* Beatriz de Carlos, Andre Lukas, Stephen Morris, _Non-perturbative vacua for M-theory on G2 manifolds_, JHEP 0412:018, 2004 ([arxiv:hep-th/0409255](https://arxiv.org/abs/hep-th/0409255))

which concludes that with taking [[non-perturbative effects]] from [[membrane instantons]] into account one gets 4d vacua with vanishing and negative [[cosmological constant]] ([[Minkowski spacetime]] and [[anti-de Sitter spacetime]]) but not with positive [[cosmological constant]] ([[de Sitter spacetime]]). They close by speculating that [[M5-brane]] 
instantons might yield [[de Sitter spacetime]].

Suggestion that [[higher curvature corrections]] allow [[de Sitter spacetime]] vacua:

* Johan Blåbäck, [[Ulf Danielsson]], Giuseppe Dibitetto, Suvendu Giri, _Constructing stable de Sitter in M-theory from higher curvature corrections_ ([arXiv:1902.04053](https://arxiv.org/abs/1902.04053))


See also

* {#BCHS18} [[Andreas Braun]], Sebastjan Cizel, Max Hubner, Sakura Schafer-Nameki, _Higgs Bundles for M-theory on $G_2$-Manifolds_ ([arXiv:1812.06072](https://arxiv.org/abs/1812.06072))

Discussion of [[Yukawa couplings]] among 3 [[generations of fundamental fermions]]:

* Eric Gonzalez, [[Gordon Kane]], Khoa Dang Nguyen, [[Malcolm Perry]], _Quark and lepton mass matrices from localization in M-theory on $G_2$ orbifold_ ([arXiv:2002.11820](https://arxiv.org/abs/2002.11820))




 
[[!redirects G2 compactifications of M-theory]]