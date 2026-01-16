

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

Volume preserving diffeomorphisms form a [[subgroup]] of the general [[diffeomorphism group]] of the [[underlying]] [[smooth manifold]] of $X$. For $X$ [[compact topological space|compact]], this is a [[Fréchet Lie group]]. Its [[Lie algebra]] is the algebra of incompressible (i.e. zero-[[divergence]]) [[vector fields]] on $X$.

In [[physics]] ([[field theory]]), volume-preserving diffeomorphisms appear: 

* as the [[gauge symmetries]] of *[[unimodular gravity]]*, 

* as residual [[gauge symmetries]] of relativistic [[brane]] [[sigma models]] after [[light cone gauge]]-[[gauge fixing|fixing]] (cf. [below](#ReferencesAsSymmetriesOfBraneDynamics)),

* as ([[gauge symmetry|gauge]]) [[symmetries]] of [[effective field theory|effective]] descriptions of [[fractional quantum Hall systems]] (cf. [below](#ReferencesAsSymmetriesOfFQHSystems)).



## References

### General

Proof that the volume-preserving [[diffeomorphism group]] of [[Cartesian space]] $\mathbb{R}^n$ is a [[perfect group]] when $n \geq 3$:

* [[Dusa McDuff]]: *On the Group of Volume-Preserving Diffeomorphisms of $\mathbf{R}^n$*, Transactions of the AMS **261** 1 (1980) &lbrack;[doi:10.1090/S0002-9947-1980-0576866-3](https://doi.org/10.1090/S0002-9947-1980-0576866-3)&rbrack;

Discussion in relation to $w_\infty$-algebras:

* [[Ergin Sezgin]]: *Area-Preserving Diffeomorphisms, $w_\infty$ Algebras and $w_\infty$ Gravity* &lbrack;[arXiv:hep-th/9202086](https://arxiv.org/abs/hep-th/9202086)&rbrack;

* Ian I. Kogan: *Area Preserving Diffeomorphisms and  Symmetry in a  Chern-Simons Theory* &lbrack;[arXiv:hep-th/9208028](https://arxiv.org/abs/hep-th/9208028)&rbrack;




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






### As symmetries of unimodular gravity
  {#ReferencesAsSymmetriesOfUnimodularGravity}

(...)

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

[[!redirects area-preserving diffeomorphism]]
[[!redirects area-preserving diffeomorphisms]]
[[!redirects area preserving diffeomorphism]]
[[!redirects area preserving diffeomorphisms]]

[[!redirects VPD]]
[[!redirects APD]]
