

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--



\tableofcontents


## Idea

A [[diffeomorphism]] $\phi \colon X \longrightarrow X$ of a ([[pseudo-Riemannian manifold|pseudo]]-) [[Riemannian manifold]] $X$ is *volume preserving* (VPD) if its [[pullback of differential forms]] fixes the [[volume form]]: $\phi^\ast vol = vol$.

If the [[dimension of a manifold|dimension]] is $dim(X) = 2$, then one also speaks of *area-preserving diffeomorphisms* (APD).

Volume preserving diffeomorphisms form a [[subgroup]] 
$$
  SDiff(X) \subset Diff(X)
$$
of the general [[diffeomorphism group]] of the [[underlying]] [[smooth manifold]] of $X$. For $X$ [[compact topological space|compact]], this is an [[infinite-dimensional Lie group|infinite-dimensional]] [[Fréchet Lie group]]. 

Its [[Lie algebra]] then is the algebra of incompressible (i.e. zero-[[divergence]]) [[vector fields]] on $X$. For the case $dim(X) = 2$, these Lie algebras (or their [[central extensions]]) are known as *[[w-infinity algebra|$w_\infty$-algebras]]* (with lower case "w") and certain [[deformation quantizations]] of these as *[[W-infinity algebra|$W_\infty$-algebras]]* (with capital "W").


## In physics

In [[physics]] ([[field theory]]), volume-preserving diffeomorphisms appear:

* as enhanced [[symmetries]] of [[2D Yang-Mills theory]] (cf. [Witten 1991](2D+Yang-Mills+theory#Witten1991), [Kogan 1992](#Kogan1992), [Pickrell 1996](#Pickrell1996)), 

* as the [[gauge symmetries]] of *[[unimodular gravity]]*, 

* as residual [[gauge symmetries]] of relativistic [[brane]] [[sigma models]] after [[light cone gauge]]-[[gauge fixing|fixing]] (cf. [below](#ReferencesAsSymmetriesOfBraneDynamics)),

* as ([[gauge symmetry|gauge]]) [[symmetries]] of [[effective field theory|effective]] descriptions of [[fractional quantum Hall systems]] (cf. [below](#ReferencesAsSymmetriesOfFQHSystems)).

But **beware** that most of the physics literature considers this at the level of [[Lie algebras]], which can be misleading as the relation of [[infinite-dimensional Lie groups]] to their [[Lie algebras]] is more loose. For instance:

* the relation between $Lie(SDiff(\Sigma^2))$ and [[special unitary Lie algebra|$\mathfrak{su}(\infty)$]]  (cf. references [below](#ReferencesRelationBetweenSUInfinityAndLieAPD)) fails drastically at the level of groups (already for basic [[algebraic topology|topological]] reasons, as highlighted by [Swain 2004](#Swain2004a));

* the canonical [[group action]] of $SDiff(\Sigma^2)$ on [[quantum states]] of [[3D Maxwell-Chern-Simons theory]] is ([[continuous map|continuous]] but) not [[differentiable map|differentiable]], hence has no reflection on the level of Lie algebras ([Pickrell 2000](#Pickrell2000)).



## References

### General

Original discussion of the [[w-infinity algebra|$w_\infty$-algebra]] of the [[torus]]:

* [[Vladimir Arnold]]; equation (109) in: *Sur la géométrie différentielle des groupes de Lie de dimension infinie et ses applications à l'hydrodynamique des fluides parfaits*, Annales de l'Institut Fourier **16** 1 (1966) 319--361 \[<a href="https://www.numdam.org/item/AIF_1966__16_1_319_0/">numdam:AIF_1966__16_1_319_0/</a>\]

Proof that the volume-preserving [[diffeomorphism group]] of [[Cartesian space]] $\mathbb{R}^n$ is a [[perfect group]] when $n \geq 3$:

* [[Dusa McDuff]]: *On the Group of Volume-Preserving Diffeomorphisms of $\mathbf{R}^n$*, Transactions of the AMS **261** 1 (1980) &lbrack;[doi:10.1090/S0002-9947-1980-0576866-3](https://doi.org/10.1090/S0002-9947-1980-0576866-3)&rbrack;

Discussion in relation to [[w-infinity algebra|$w_\infty$-algebras]]:

* [[Eric Bergshoeff]], [[Miles P. Blencowe]], [[Kellogg S. Stelle]]: *Area-preserving diffeomorphisms and higher-spin algebras*,  Commun. Math. Phys. **128** (1990) 213–230 &lbrack;[doi:10.1007/BF02108779](https://doi.org/10.1007/BF02108779)&rbrack;

* [[Ergin Sezgin]]: *Area-Preserving Diffeomorphisms, $w_\infty$ Algebras and $w_\infty$ Gravity* &lbrack;[arXiv:hep-th/9202086](https://arxiv.org/abs/hep-th/9202086)&rbrack;

* {#Kogan1992} Ian I. Kogan: *Area Preserving Diffeomorphisms and  Symmetry in a  Chern-Simons Theory* &lbrack;[arXiv:hep-th/9208028](https://arxiv.org/abs/hep-th/9208028)&rbrack;
  > (in [[3D Maxwell-Chern-Simons theory]])


### Linear representations
 {#ReferencesRepresentationTheory}

There is no general [[representation theory]] of VPDs, but (cf. [Pickrell 2000 p. 179](#Pickrell2000)) the following examples of [[linear representations]] of $SDiff$ have been constructed.


#### Reps of $SDiff(\mathbb{R}^3)$

In the context of discussion of [[vortices]]:

* [[Mario Rasetti]], [[Tullio Regge]]: *Vortices in He II, current algebras and quantum knots*, Physica A: Statistical Mechanics and its Applications **80** 3 (1975) 217-233 \[<a href="https://doi.org/10.1016/0378-4371(75)90105-3">doi:10.1016/0378-4371(75)90105-3</a>\]

* [[Mario Rasetti]], [[Tullio Regge]]: *Quantum Vortices*, preprint TH.3643-CERN (1983) &lbrack;[pdf](https://cds.cern.ch/record/146513/files/198308324.pdf)&rbrack;

* [[Mario Rasetti]], [[Tullio Regge]]: *Quantization of Extended Vortices and $SDiff(\mathbb{R}^3)$*, in: *Algebraic Analysis*, 
**2**, Academic Press (1988) 727-734 \[<a href="https://doi.org/10.1016/B978-0-12-400466-5.50022-6">doi:10.1016/B978-0-12-400466-5.50022-6</a>\]

* Mauro Spera: *Moment map and gauge geometric aspects of the Schrödinger and Pauli equations*,  International Journal of Geometric Methods in Modern Physics **13** 04 (2016) 1630004 \[<a href="https://doi.org/10.1142/S021988781630004X">doi:10.1142/S021988781630004X</a>\]


#### Reps of $SDiff(S^2)$

Representation on [[sections]] of [[determinant line bundles]] of (tacitly) [[3D Maxwell-Chern-Simons theory]]:

* {#Pickrell2000} [[Doug Pickrell]]: *On the Action of the Group of Diffeomorphisms of a Surface on Sections of the Determinant Line Bundle*, Pacific Journal of Mathematics **193** 1 (2000) 177-199 &lbrack;[doi:10.2140/pjm.2000.193.177](http://dx.doi.org/10.2140/pjm.2000.193.177), [pdf](https://msp.org/pjm/2000/193-1/pjm-v193-n1-p10-s.pdf)&rbrack;
  > (via methods of [[constructive field theory]], also discusses $SDiff(T^2)$)

using a rigorous APD-[[invariant]] [[path integral]] [[measure]] for [[2D Yang-Mills theory]], due to:

* {#Pickrell1996} [[Doug Pickrell]]: *On $YM_2$ measures and area-preserving diffeomorphisms*, Journal of Geometry and Physics **19** 4 (1996) 315-367 \[<a href="https://doi.org/10.1016/0393-0440(95)00034-8">doi:10.1016/0393-0440(95)00034-8</a>\]

In the context of the [[Plebański formulation of gravity]]:

* [[Boris Kruglikov]], Oleg Morozov: *$SDiff(2)$ and uniqueness of the Plebański equation*, J. Math. Phys. **53** 083506 (2012) &lbrack;[doi:10.1063/1.4739749](https://doi.org/10.1063/1.4739749), [arXiv:1204.3577](https://arxiv.org/abs/1204.3577)&rbrack;

Via the [[orbit method]]:

* Robert F. Penna: *$SDiff(S^2)$ and the orbit method*, J. Math. Phys. **61** 012301 (2020) &lbrack;[arXiv:1806.05235](https://arxiv.org/abs/1806.05235), [doi:10.1063/1.5140475](https://doi.org/10.1063/1.5140475)&rbrack;
  > (though no real results obtained here)






[[!include relating su(infinity) to Lie(APD) -- references]]






### As symmetries of brane dynamics
 {#ReferencesAsSymmetriesOfBraneDynamics}

On volume-preserving diffeomorphisms as residual [[gauge symmetries]] of [[brane]] [[sigma-models]] in [[light cone gauge]]:


On APD symmetry of the [[M2-brane]] [[sigma-model]] (cf. *[M2-brane -- Light-cone quantization to the BFSS matrix model](M2-brane#LightConeQuantizationOfM2BranesToBFSSMatrixModel)*):

* {#FloratosIliopoulos1988} [[Emmanuel G. Floratos]], [[John Iliopoulos]]: *A note on the classical symmetries of the closed bosonic membranes*, Physics Letters B **201** 2 (1988) 237-240 \[<a href="https://doi.org/10.1016/0370-2693(88)90220-1">doi:10.1016/0370-2693(88)90220-1</a>\]

* {#deWitHoppeNicolai88} [[Bernard de Wit]], [[Jens Hoppe]], [[Hermann Nicolai]], *On the Quantum Mechanics of Supermembranes*, Nucl. Phys. B **305** (1988) 545-581 \[<a href="https://doi.org/10.1016/0550-3213(88)90116-2">doi:10.1016/0550-3213(88)90116-2</a>, [spire:261702](http://inspirehep.net/record/261702), [pdf](http://pubman.mpdl.mpg.de/pubman/item/escidoc:153408:1/component/escidoc:153407/353961.pdf), [[deWitHoppeNicolai88.pdf:file]]\]
  > (gauging of APD symmetry on p. 553)

* [[Bernard de Wit]], U. Marquard, [[Hermann Nicolai]]: *Area-preserving diffeomorphisms and supermembrane Lorentz invariance*,  Commun. Math. Phys. **128** (1990) 39–62 \[<a href="https://doi.org/10.1007/BF02097044">doi:10.1007/BF02097044</a>, [inSpire:277216](https://inspirehep.net/literature/277216)\]

Generalization to VPD symmetry of the higher-dimensional [[super p-branes]] without gauge fields on their [[worldvolume]]:

* [[Eric Bergshoeff]], [[Ergin Sezgin]], Y. Tanii, [[Paul K. Townsend]]: *Super $p$-branes as gauge theories of volume preserving diffeomorphisms*, Annals of Physics **199** 2 (1990) 340-365 \[<a href="https://doi.org/10.1016/0003-4916(90)90381-W">doi:10.1016/0003-4916(90)90381-W</a>, [[BSTT-BraneVPD.pdf:file]]\]

See also:

* Y. Matsuo, Y. Shibusa: *Volume Preserving Diffeomorphism and Noncommutative Branes*, JHEP 0102:006 (2001) &lbrack;[arXiv:hep-th/0010040](https://arxiv.org/abs/hep-th/0010040)&rbrack;


On VPD symmetry in the [[Nambu-Poisson M5-brane model]]:

* [[Pei-Ming Ho]], Yosuke Imamura, Yutaka Matsuo, Shotaro Shiba; section 4 of: *M5-brane in three-form flux and multiple M2-branes*, JHEP 0808:014 (2008) &lbrack;[arXiv:0805.2898](https://arxiv.org/abs/0805.2898), [doi:10.1088/1126-6708/2008/08/014](https://doi.org/10.1088/1126-6708/2008/08/014)&rbrack;

* [[Pei-Ming Ho]], Chi-Hsien Yeh; section 2 of: *D-brane in R-R Field Background*, JHEP 1103:143 (2011) &lbrack;[arXiv:1101.4054](https://arxiv.org/abs/1101.4054), <a href=" https://doi.org/10.1007/JHEP03(2011)143">doi:10.1007/JHEP03(2011)143</a>&rbrack;

* [[Pei-Ming Ho]], Chen-Te Ma, Chi-Hsien Yeh; section 2.2.1 of: *BPS States on M5-brane in Large $C$-field Background*, J. High Energ. Phys. **2012** 76 (2012) &lbrack;[arXiv:1206.1467](https://arxiv.org/abs/1206.1467), <a href=" https://doi.org/10.1007/JHEP08(2012)076">doi:10.1007/JHEP08(2012)076</a>&rbrack;

Review:

* [[Pei-Ming Ho]]; section 3.2.1 of: *A Concise Review on M5-brane in Large $C$-Field Background*, Chin. J. Phys. **48** 1 (2010) &lbrack;[arXiv:0912.0445](https://arxiv.org/abs/0912.0445)&rbrack;

* [[Pei-Ming Ho]], Yutaka Matsuo; section 4.3 of: *Nambu bracket and M-theory*, Progress of Theoretical and Experimental Physics **2016** 6 (2016) 06A104 &lbrack;[arXiv:1603.09534](https://arxiv.org/abs/1603.09534), [doi:10.1093/ptep/ptw075](https://doi.org/10.1093/ptep/ptw075)&rbrack;

On VPD symmetry of the actual [[M5-brane]] [[sigma-model]]:

* [[Igor A. Bandos]], [[Paul K. Townsend]]: *Light-cone M5 and multiple M2-branes*, Class. Quant. Grav. **25** 245003 (2008) \[<a href="https://doi.org/10.1088/0264-9381/25/24/245003">doi:10.1088/0264-9381/25/24/245003</a>, [arXiv:0806.4777](https://arxiv.org/abs/0806.4777)\]



### As symmetries of fractional quantum Hall systems
 {#ReferencesAsSymmetriesOfFQHSystems}

As ([[gauge symmetry|gauge]]) [[symmetries]] of [[fractional quantum Hall systems]] (cf. *[supersymmetry in FQH systems](quantum+Hall+effect#ReferencesSupersymmetryInFractionalQuantumHall)* and for more see at *[[W-infinity algebra|$W_\infty$-algebra]]*):


* A. Cappelli, [[Carlo A. Trugenberger]], G. R. Zemba:
*Infinite Symmetry in the Quantum Hall Effect*, Nucl. Phys. B **396** (1993) 465-490 \[<a href="https://doi.org/10.1016/0550-3213(93)90660-H">doi:10.1016/0550-3213(93)90660-H</a>, [arXiv:hep-th/9206027](https://arxiv.org/abs/hep-th/9206027)\]

* [[Yi-Hsien Du]], [[Umang Mehta]], Dung Xuan Nguyen, [[Dam Thanh Son]]: *Volume-preserving diffeomorphism as nonabelian higher-rank gauge symmetry*, SciPost Phys. **12** 050 (2022) &lbrack;[arXiv:2103.09826](https://arxiv.org/abs/2103.09826), [doi:10.21468/SciPostPhys.12.2.050](https://doi.org/10.21468/SciPostPhys.12.2.050)&rbrack;

* [[Yi-Hsien Du]], [[Umang Mehta]], [[Dam Thanh Son]]: *Noncommutative gauge symmetry in the fractional quantum Hall effect*, J. High Energ. Phys. **2024** 125 (2024) &lbrack;<a href="https://doi.org/10.1007/JHEP08(2024)125">doi:10.1007/JHEP08(2024)125</a>, [arXiv:2110.13875](https://arxiv.org/abs/2110.13875)&rbrack;

* {#Du2025} [[Yi-Hsien Du]]: *Chiral Graviton Theory of Fractional Quantum Hall States* \[<a href="https://arxiv.org/abs/2509.04408">arXiv:2509.04408</a>\]



[[!redirects volume preserving diffeomorphisms]]

[[!redirects volume-preserving diffeomorphism]]
[[!redirects volume-preserving diffeomorphisms]]

[[!redirects volume-preserving diffeomorphism group]]
[[!redirects volume-preserving diffeomorphism groups]]
[[!redirects volume preserving diffeomorphism group]]
[[!redirects volume preserving diffeomorphism groups]]

[[!redirects area-preserving diffeomorphism]]
[[!redirects area-preserving diffeomorphisms]]
[[!redirects area preserving diffeomorphism]]
[[!redirects area preserving diffeomorphisms]]

[[!redirects VPD]]
[[!redirects APD]]
