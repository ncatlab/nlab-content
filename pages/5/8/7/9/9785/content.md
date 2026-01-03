
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
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

A [[super Lie algebra]] which is a [polyvector](super+Poincare+Lie+algebra#PolyvectorExtensions) [[Lie algebra extension|extension]] of the [[super Poincaré Lie algebra]] ([[supersymmetry]]) in $D = 10+1$ for  $\mathcal{N}=1$ [[supersymmetry]] by [[charges]] corresponding to the [[M2-brane]] and the [[M5-brane]] ("[[extended supersymmetry]]"). 

Concretely, where the non-trivial [[super Lie bracket]] of the [[super-Minkowski Lie algebra]] is 

$$
  \big[
    Q_\alpha
    ,\,
    Q_\beta
  \big]
  \;=\;
  -2 \, \Gamma^a_{\alpha \beta} \, P_a
$$

in the M-theory super-Lie algebra this equation is extended to 

$$
  \big[
    Q_\alpha
    ,\,
    Q_\beta
  \big]
  \;=\;
  -2 \, \Gamma^a_{\alpha \beta} \, P_a
  \,-\,2 \Gamma^{a_1 a_2}_{\alpha \beta} \, Z_{a_1 a_2}
  \,-\,2 \Gamma^{a_1 \cdots a_5}_{\alpha \beta} \, Z_{a_1 \cdots a_5}
$$

([D'Auria & Fré 1982, Table 4](#DAuriaFre82), [Townsend 1995 (13)](#Townsend95) [1997a (1)](#Townsend97a) [1997b (24)](#Townsend97b), [BdAPV 2005 (1.2-4)](#BdAPV05); the term "M-algebra" for a further extension is due to [Sezgin 1997](#Sezgin97).)


## Properties

### As the algebra of conserved currents of the M-branes

In ([AGIT 89](#AGIT89)) it is shows that the M-algebra-like polyvector extensions arise as the algebras of [[conserved currents]] of the [[Green-Schwarz super p-brane sigma-models]].

By the discussion at [conserved current -- In higher prequantum geometry](conserved+current#InHigherPrequantumGeometry) this means that this is the degree-0 piece in the [[Heisenberg Lie n-algebra]] which is induced by regarding the WZW-curvature terms as super [[n-plectic forms]] on $\mathbb{R}^{10,1|32}$.

### As the Lie algebra of derivations of the SuGra Lie 3-algebra

[Castellani 2005](#Castellani05) 
implicitly shows (cf. [FSS 13](#FSS13)) that the M-extension arises  as the [[derivations]]/automorphisms of the [[supergravity Lie 3-algebra]]/[[supergravity Lie 6-algebra]] (see there for the details).

### As an 11-dimensional boundary condition for the M2-brane
 {#AsAn11DimensionalBoundaryCondition}

The original construction in ([D'Auria-Fré 82](#DAuriaFre82)) asks for a [[super Lie algebra]] [[Lie algebra extension|extension]] $\mathbb{R}^{10,1\vert 32} \rtimes \mathfrak{g}$ of [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert 32}$ such that the 4-[[cocycle]] $\mu_4 = \overline{\psi} \wedge \Gamma^{a b} \psi \wedge e_a \wedge e_b$ for the M2-brane trivializes when pulled back to this:

$$
  \array{
    & & \mathbb{R}^{10,1\vert 32} \rtimes \mathfrak{g}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\simeq} && \mathbb{R}^{10,1\vert 32}
    \\
    & \searrow && \swarrow_{\mathrlap{\mu_4}}
    \\
    && B^{3}\mathbb{R}
  }
  \,.
$$

(In the language of [[local prequantum field theory]] this identifies a [[boundary condition]] for the WZW term of the M2-brane.)

They find (see also [Bandos, Azcarraga, Izquierdo, Picon & Varela 2004](#BandosAzcarragaIzquierdoPiconVarela04)) that a solution for $\mathfrak{g}$ includes a fermionic extension of the M-theory super Lie algebra.




## Related concepts

* [[type II super Lie algebra]]

* [[BPS state]]

* [[supergravity Lie 3-algebra]]

* [[supergravity Lie 6-algebra]]

* [[M2-brane]], [[M5-brane]]

* [[M-theory]]

## References

### From the M2-Cocycle
 {#ReferencesFromTheM2Cocycle}

Two versions of a fermionic extension of the Polyvector extensions of $\mathfrak{Iso}(\mathbb{R}^{10,1|32})$ on which the [[M2-brane]] [[Lie algebra cohomology|4-cocycle]] trivializes were first found in

* {#DAuriaFre82} [[Riccardo D'Auria]], [[Pietro Fré]]: _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B **201** (1982) 101-140 &lbrack;<a href="https://doi.org/10.1016/0550-3213(82)90376-5">doi:10.1016/0550-3213(82)90376-5</a>,  [[GeometricSupergravityErrata.pdf:file]]&rbrack;


and then a 1-parameter family of such was discovered in

* {#BandosAzcarragaIzquierdoPiconVarela04} [[Igor Bandos]], [[José de Azcárraga]], [[José M. Izquierdo]], Moises Picon, [[Oscar Varela]]: _On the underlying gauge group structure of D=11 supergravity_, Phys. Lett.B **596** (2004) 145-155 \[<a href="https://doi.org/10.1016/j.physletb.2004.06.079">doi:10.1016/j.physletb.2004.06.079</a>, [arXiv:hep-th/0406020](http://arxiv.org/abs/hep-th/0406020)\]

* {#BdAPV05} [[Igor Bandos]], [[José de Azcárraga]], Moises Picon, [[Oscar Varela]]: _On the formulation of $D=11$ supergravity and the composite nature of its three-from field_, Annals Phys. **317** (2005) 238-279 \[<a href="https://doi.org/10.1016/j.aop.2004.11.016">doi:10.1016/j.aop.2004.11.016</a>, [arXiv:hep-th/0409100](https://arxiv.org/abs/hep-th/0409100)\]

That a limiting case of this is given by the [[orthosymplectic super Lie algebra]] $\mathfrak{osp}(1\vert 32)$:

* {#FernandezIzquierdoOlmo15} J. J. Fernandez, [[José M. Izquierdo]], M. A. del Olmo, *Contractions from $osp(1|32) \oplus osp(1|32)$ to the M-theory superalgebra extended by additional fermionic generators*, Nuclear Physics B **897** (2015) 87-97 &lbrack;[arXiv:1504.05946](http://arxiv.org/abs/1504.05946), [doi:10.1016/j.nuclphysb.2015.05.018](https://doi.org/10.1016/j.nuclphysb.2015.05.018)&rbrack;

Review and further discussion:

* {#Azcarraga05} [[José de Azcárraga]], section 5 of: _Superbranes, $D=11$ CJS supergravity and enlarged superspace coordinates/fields correspondence_, AIP Conf. Proc. **767** (2005) 243-267 \[<a href="https://doi.org/10.1063/1.1923338">doi:10.1063/1.1923338</a>, [arXiv:hep-th/0501198](https://arxiv.org/abs/hep-th/0501198)\]

* [[Oscar Varela]]: *Symmetry and holonomy in M Theory*, PhD thesis, Valencia (2006) &lbrack;[arXiv:hep-th/0607088](https://arxiv.org/abs/hep-th/0607088), [hdl:10550/15484](https://hdl.handle.net/10550/15484),  [spire:1397691](https://inspirehep.net/literature/1397691)&rbrack;


* {#AndrianopoliDAuriaRavera16} [[Laura Andrianopoli]], [[Riccardo D'Auria]], [[Lucrezia Ravera]], *Hidden Gauge Structure of Supersymmetric Free Differential Algebras*, JHEP 1608 (2016) 095 &lbrack;[arXiv:1606.07328](https://arxiv.org/abs/1606.07328), <a href=" https://doi.org/10.1007/JHEP08(2016)095">doi:10.1007/JHEP08(2016)095</a>&rbrack;

* [[Laura Andrianopoli]], [[Riccardo D'Auria]], [[Lucrezia Ravera]]: _More on the Hidden Symmetries of 11D Supergravity_, Phys. Lett. B **772** (2017) 578 \[<a href="https://doi.org/10.1016/j.physletb.2017.07.016">doi:10.1016/j.physletb.2017.07.016</a>, [arXiv:1705.06251](https://arxiv.org/abs/1705.06251)\]
  > where the algebra is referred to as the _DF-algebra_, in honor of [D'Auria & Fré 1982](#DAuriaFre82).

* [[Lucrezia Ravera]], *On the hidden symmetries of $D=11$ supergravity*, Springer Proceedings in Mathematics & Statistics **396** Springer (2021) \[<a href="https://doi.org/10.1007/978-981-19-4751-3_15">doi:10.1007/978-981-19-4751-3_15</a>, [arXiv:2112.00445](https://arxiv.org/abs/2112.00445)\]

* [[Laura Andrianopoli]], [[Riccardo D'Auria]], *Supergravity in the Geometric Approach and its Hidden Graded Lie Algebra*, Expositiones Mathematicae, &lbrack;[arXiv:2404.13987](https://arxiv.org/abs/2404.13987) [10.1016/j.exmath.2024.125631](https://doi.org/10.1016/j.exmath.2024.125631)&rbrack;

* [[Grigorios Giotopoulos]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:The Hidden M-Group]]*, Journal of Geometry and Physics (2025) &lbrack;[doi:10.1016/j.geomphys.2025.105743](https://doi.org/10.1016/j.geomphys.2025.105743), [arXiv:2411.11963](https://arxiv.org/abs/2411.11963)&rbrack;




Another, alternative "weak [[decomposable differential form|decomposition]]" of the M2-brane [[extended super-Minkowski spacetime]] was claimed in 

* {#Ravera18a} [[Lucrezia Ravera]], section 3: of _Hidden Role of Maxwell Superalgebras in the Free Differential Algebras of D=4 and D=11 Supergravity_, Eur. Phys. J. C **78** 3 (2018) 211 \[<a href="https://doi.org/10.1140/epjc/s10052-018-5673-8">doi:10.1140/epjc/s10052-018-5673-8</a>, [arXiv:1801.08860](https://arxiv.org/abs/1801.08860)\]

with the interesting difference that for this splitting [[super Lie algebra]]  is non-abelian, in fact an extension of the Lie algebra of the [[Spin group]] $Spin(10,1)$ ([Ravera 18, (3.5)-(3-6)](#Ravera18)). 

See also:
 
* {#Ravera18b} [[Lucrezia Ravera]]: _Group Theoretical Hidden Structure of Supergravity Theories in Higher Dimensions_, PhD thesis, Torino (2018) &lbrack;[arXiv:1802.06602](https://arxiv.org/abs/1802.06602), [doi:10.6092/polito/porto/2700157](https://doi.org/10.6092/polito/porto/2700157)&rbrack;

That the underlying bosonic [[body]] of this super Lie algebra happens to be the [[typical fiber]] of what would be the 11-d [[exceptional generalized tangent bundle]], namely the [level-2 truncation of the l1-representation](E11#FundamentalRepresentationAndBraneCharges) of [[E11]] according to ([West 04](E11#West04)) was highlighted in:

* [[Silvia Vaula]], *On the underlying $E_{11}$ symmetry of the $D = 11$ Free Differential Algebra*, JHEP 0703:010 (2007) &lbrack;[arXiv:hep-th/0612130](http://arxiv.org/abs/hep-th/0612130), [doi:10.1088/1126-6708/2007/03/010](https://doi.org/10.1088/1126-6708/2007/03/010)&rbrack;

For analogous discussion in [[7d supergravity]] and [[4d supergravity]], see the references there.


### Alternative

Alternatively, from considerations of brane charges, the M-theory algebra extensions were (apparently independently) introduced in

 * {#vHvP82} [[Jan-Willem van Holten]], [[Antoine Van Proeyen]], _$N=1$ supersymmetry algebras in $d = 2, 3, 4 \,mod\, 8$_ J. Phys. A **15** (1982) 3763 &lbrack;[doi:10.1088/0305-4470/15/12/028](https://iopscience.iop.org/article/10.1088/0305-4470/15/12/028), [spire:177060](https://inspirehep.net/literature/177060)&rbrack;

 * {#Townsend95} [[Paul Townsend]], _$p$-Brane Democracy_, in: *[Particles, strings and cosmology](https://inspirehep.net/literature/431132)* Proceedings, 19th Johns Hopkins Workshop and 5th PASCOS Interdisciplinary Symposium, Baltimore, USA, March 22-25 (1995) &lbrack;[arXiv:hep-th/9507048](http://arxiv.org/abs/hep-th/9507048), [spire:397058](https://inspirehep.net/literature/397058)&rbrack;

   reprinted in: [[Michael Duff]] (ed.), *[[The World in Eleven Dimensions]]*, IoP (1999) 375-389

with further amplification including

* {#Townsend97a} [[Paul Townsend]], _M(embrane) theory on $T^9$_, Nucl. Phys. Proc. Suppl. **68** (1998) 11-16 \[<a href="https://doi.org/10.1016/S0920-5632(98)00136-4">doi:10.1016/S0920-5632(98)00136-4</a>, [arXiv:hep-th/9708034](http://arxiv.org/abs/hep-th/9708034)\]

* {#Townsend97b} [[Paul Townsend]]: *M-theory from its superalgebra*, in *Strings, Branes and Dualities*, NATO ASI Series **520**, Springer (1999) &lbrack;[arXiv:hep-th/9712004](http://arxiv.org/abs/hep-th/9712004), [doi:10.1007/978-94-011-4730-9_5](https://doi.org/10.1007/978-94-011-4730-9_5)&rbrack;

* [[Chris Hull]]: pp 5 in: *Gravitational Duality, Branes and Charges*, Nucl. Phys. B **509** (1998) 216-251 &lbrack;[arXiv:hep-th/9705162](https://arxiv.org/abs/hep-th/9705162), <a href="https://doi.org/10.1016/S0550-3213(97)00501-4">doi:10.1016/S0550-3213(97)00501-4</a>&rbrack;


In their global form, where differential forms are replaced by their de Rham cohomology classes on curved superspacetimes, these algebras were identified (for the case including the 2-form piece but not the 5-form piece) as the algebras of [[conserved currents]] of the [[Green-Schwarz super p-brane sigma-models]] in

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], [[José M. Izquierdo]], [[Paul Townsend]]: *Topological Extensions of the Supersymmetry Algebra for Extended Objects*, Phys. Rev. Lett. **63** (1989) 2443 &lbrack;[doi:10.1103/PhysRevLett.63.2443](https://doi.org/10.1103/PhysRevLett.63.2443), [spire:26393](https://inspirehep.net/record/26393?ln=en)&rbrack;

reviewed in 

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.8 of: _[[Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics]]_, Cambridge monographs of mathematical physics, (1995)


The generalization of this including also the contribution of the [[M5-brane]] was considered in

* {#SorokinTownsend97} [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys.Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

Further detailed discussion along these lines producing also the [[type II supersymmetry algebras]] is in

* Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))


The full extension was named "M-algebra" in

* {#Sezgin97} [[Ergin Sezgin]], _The M-Algebra_, Phys. Lett. B **392** (1997) 323-331 \[<a href="https://doi.org/10.1016/S0370-2693(96)01576-6">doi:10.1016/S0370-2693(96)01576-6</a>, [arXiv:hep-th/9609086](http://arxiv.org/abs/hep-th/9609086)\]

In ([D'Auria-Fr&#233; 82](#DAuriaFre82)) the motivation is from the formulation of the fields of [[11-dimensional supergravity]] as connections with values in the [[supergravity Lie 3-algebra]], see at _[[D'Auria-Fré formulation of supergravity]]_. Realization of the M-theory super Lie algebra as the algebra of [[derivations]] of the [[supergravity Lie 3-algebra]] is in 

* {#Castellani05} [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors, and the M-theory superalgebra_, J. Phys. Math. **3** (2011)  1-7 &lbrack;[arXiv:hep-th/0508213](http://arxiv.org/abs/hep-th/0508213), [euclid:jpm/1359468398](http://projecteuclid.org/euclid.jpm/1359468398)&rbrack;

with amplification in

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ (2013)

* [[nLab:Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lie n-algebras of BPS charges]]_

  
Discussion of a formulation in terms of [[octonions]] (see also at _[[division algebra and supersymmetry]]_) includes

* A. Anastasiou, [[Leron Borsten]], [[Michael Duff]], L. J. Hughes, S. Nagy, _An octonionic formulation of the M-theory algebra_ ([arXiv:1402.4649](http://arxiv.org/abs/1402.4649))

Arguments that the charges of the M-theory super Lie algebra may be identified inside [[E11]] are given in 

* [[Peter West]], _$E_{11}$, $SL(32)$ and Central Charges_, Phys.Lett.B575:333-342,2003 ([arXiv:hep-th/0307098v2](http://arxiv.org/abs/hep-th/0307098v2))

* [[Paul Cook]], around p. 75 of _Connections between Kac-Moody algebras and M-theory_ ([arXiv:0711.3498](http://arxiv.org/abs/0711.3498))

Relation to [[exceptional field theory]]:

* [[Igor Bandos]]: *Exceptional field theories, superparticles in an enlarged 11D superspace and higher spin theories*, Nucl. Phys. B **925** (2017) 28-62 &lbrack;[arXiv:1612.01321](https://arxiv.org/abs/1612.01321), [doi:10.1016/j.nuclphysb.2017.10.001](https://doi.org/10.1016/j.nuclphysb.2017.10.001)&rbrack;



[[!redirects M-theory Lie algebra]]

[[!redirects M-Lie algebra]]
[[!redirects M-theory algebra]]

[[!redirects M-theory supersymmetry Lie algebra]]
[[!redirects M-theory supersymmetry super Lie algebra]]

[[!redirects M-theory super Lie algebra]]


[[!redirects M-theory super Lie algebra extension]]
[[!redirects M-theory super Lie algebra extensions]]

[[!redirects DF-algebra]]
[[!redirects DF-algebras]]

[[!redirects D'Auria-Fré algebra]]
[[!redirects D'Auria-Fré algebras]]

[[!redirects D'Auria-Fre algebra]]
[[!redirects D'Auria-Fre algebras]]

[[!redirects M-algebra]]
[[!redirects M-algebras]]
