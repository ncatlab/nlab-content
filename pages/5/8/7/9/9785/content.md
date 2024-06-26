[[!redirects M-theory super Lie algebra]]

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

A [[super Lie algebra]] which is a [polyvector](super+Poincare+Lie+algebra#PolyvectorExtensions) [[Lie algebra extension|extension]] of the [[super Poincaré Lie algebra]] ([[supersymmetry]]) in $D = 10+1$ for  $N=1$ [[supersymmetry]] by [[charges]] corresponding to the [[M2-brane]] and the [[M5-brane]] ("[[extended supersymmetry]]"). 


## Properties

### As the algebra of conserved currents of the M-branes

In ([AGIT 89](#AGIT89)) it is shows that the M-algebra-like polyvector extensions arise as the algebras of [[conserved currents]] of the [[Green-Schwarz super p-brane sigma-models]].

By the discussion at [conserved current -- In higher prequantum geometry](conserved+current#InHigherPrequantumGeometry) this means that this is the degree-0 piece in the [[Heisenberg Lie n-algebra]] which is induced by regarding the WZW-curvature terms as super [[n-plectic forms]] on $\mathbb{R}^{10,1|32}$.

### As the Lie algebra of derivations of the SuGra Lie 3-algebra

In ([Castellani 05](#Castellani05)) it is 
implicitly shown ([FSS 13](#FSS13)) that the M-extension arises  as the [[derivations]]/automorphisms of the [[supergravity Lie 3-algebra]]/[[supergravity Lie 6-algebra]] (see there for the details).

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

They find, see also ([Bandos-Azcarraga-Izquierdo-PiconVarela 04](#BandosAzcarragaIzquierdoPiconVarela04)) that a solution for $\mathfrak{g}$ includes a fermionic extension of the M-theory super Lie algebra.




## Related concepts

* [[type II super Lie algebra]]

* [[BPS state]]

* [[supergravity Lie 3-algebra]]

* [[supergravity Lie 6-algebra]]

* [[M2-brane]], [[M5-brane]]

* [[M-theory]]

## References

### From the M2-Cocyle
 {#ReferencesFromTheM2Cocycle}

Two versions of a fermionic extension of the Polyvector extensions of $\mathfrak{Iso}(\mathbb{R}^{10,1|32})$ on which the [[M2-brane]] [[Lie algebra cohomology|4-cocycle]] trivializes were first found in

* {#DAuriaFre82}  [[Riccardo D'Auria]], [[Pietro Fré]], last pages of _[[GeometricSupergravity.pdf:file]]_, Nuclear Physics B201 (1982) 101-140 

and then a 1-parameter family of such was discovered in

* {#BandosAzcarragaIzquierdoPiconVarela04} [[Igor Bandos]], [[José de Azcárraga]], J.M. Izquierdo, M. Picon, O. Varela, _On the underlying gauge group structure of D=11 supergravity_, Phys.Lett.B596:145-155,2004 ([arXiv:hep-th/0406020](http://arxiv.org/abs/hep-th/0406020))

* [[Igor Bandos]], [[José de Azcárraga]], Moises Picon, Oscar Varela, _On the formulation of $D=11$ supergravity and the composite nature of its three-from field_, Annals Phys. 317 (2005) 238-279 ([arXiv:hep-th/0409100](https://arxiv.org/abs/hep-th/0409100))

That a limiting case of this is given by the [[orthosymplectic super Lie algebra]] $\mathfrak{osp}(1\vert 32)$:

* {#FernandezIzquierdoOlmo15} J.J. Fernandez, [[José M. Izquierdo]], M.A. del Olmo, _Contractions from $osp(1|32) \oplus osp(1|32)$ to the M-theory superalgebra extended by additional fermionic generators_, Nuclear Physics B **897** (2015) 87-97 &lbrack;[arXiv:1504.05946](http://arxiv.org/abs/1504.05946)&rbrack;

Further discussion:

* {#AndrianopoliDAuriaRavera16} [[Laura Andrianopoli]], [[Riccardo D'Auria]], [[Lucrezia Ravera]], *Hidden Gauge Structure of Supersymmetric Free Differential Algebras*, JHEP 1608 (2016) 095 &lbrack;[arXiv:1606.07328](https://arxiv.org/abs/1606.07328), <a href=" https://doi.org/10.1007/JHEP08(2016)095">doi:10.1007/JHEP08(2016)095</a>&rbrack;

* [[Laura Andrianopoli]], [[Riccardo D'Auria]], [[Lucrezia Ravera]], _More on the Hidden Symmetries of 11D Supergravity_ ([arXiv:1705.06251](https://arxiv.org/abs/1705.06251))

where the algebra is referred to as the _DF-algebra_, in honor of [D'Auria-Fré 82](#DAuriaFre82).

All this is reviewed in 

* {#Azcarraga05} [[José de Azcárraga]], section 5 of _Superbranes, D=11 CJS supergravity and enlarged superspace coordinates/fields correspondence_, AIP Conf. Proc. 767:243-267, 2005 ([arXiv:hep-th/0501198](https://arxiv.org/abs/hep-th/0501198))

also

* [[Lucrezia Ravera]], *On the hidden symmetries of $D=11$ supergravity* ([arXiv:2112.00445](https://arxiv.org/abs/2112.00445))

* [[Laura Andrianopoli]], [[Riccardo D'Auria]], *Supergravity in the Geometric Approach and its Hidden Graded Lie Algebra* &lbrack;[arXiv:2404.13987](https://arxiv.org/abs/2404.13987)&rbrack;



Another, alternative "weak [[decomposable differential form|decomposition]]" of the M2-brane [[extended super-Minkowski spacetime]] was found in 

* {#Ravera18a} [[Lucrezia Ravera]], section 3 of _Hidden Role of Maxwell Superalgebras in the Free Differential Algebras of D=4 and D=11 Supergravity_ ([arXiv:1801.08860](https://arxiv.org/abs/1801.08860))

with the interesting difference that for this splitting [[super Lie algebra]]  is non-abelian, in fact an extension of the Lie algebra of the [[Spin group]] $Spin(10,1)$ ([Ravera 18, (3.5)-(3-6)](#Ravera18)). 

See also:
 
* {#Ravera18b} [[Lucrezia Ravera]], _Group Theoretical Hidden Structure of Supergravity Theories in Higher Dimensions_ ([arXiv:1802.06602](https://arxiv.org/abs/1802.06602))

That the underlying bosonic [[body]] of this super Lie algebra happens to be the [[typical fiber]] of what would be the 11-d [[exceptional generalized tangent bundle]], namely the [level-2 truncation of the l1-representation](E11#FundamentalRepresentationAndBraneCharges) of [[E11]] according to ([West 04](E11#West04)) was highlighted in the review 

* [[Silvia Vaula]], _On the underlying $E_{11}$ symmetry of the $D= 11$ Free Differential Algebra_, JHEP 0703:010, 2007 ([arXiv:hep-th/0612130](http://arxiv.org/abs/hep-th/0612130))

For analogous discussion in [[7d supergravity]] and [[4d supergravity]], see the references there.


### Alternative

From a different perspective the M-theory algebra extensions were (apparently independently) introduced in

 * [[Jan-Willem van Holten]], [[Antoine Van Proeyen]], _$N=1$ supersymmetry algebras in $d=2,3,4 \,mod\, 8$_ J.Phys. A15, 3763 (1982).

 * [[Paul Townsend]], _p-Brane Democracy_ ([arXiv:hep-th/9507048](http://arxiv.org/abs/hep-th/9507048))

with further amplification including

* {#Townsend97a} [[Paul Townsend]], _M(embrane) theory on $T^0$_, Nucl.Phys.Proc.Suppl.68:11-16,1998 ([arXiv:hep-th/9708034](http://arxiv.org/abs/hep-th/9708034))

* {#Townsend97b} [[Paul Townsend]], _M-theory from its superalgebra_, Cargese lectures 1997 ([arXiv:hep-th/9712004](http://arxiv.org/abs/hep-th/9712004))

In their global form, where differential forms are replaced by their de Rham cohomology classes on curved superspacetimes, these algebras were identified (for the case including the 2-form piece but not the 5-form piece) as the algebras of [[conserved currents]] of the [[Green-Schwarz super p-brane sigma-models]] in

* {#AGIT89} [[José de Azcárraga]], [[Jerome Gauntlett]], J.M. Izquierdo, [[Paul Townsend]], _Topological Extensions of the Supersymmetry Algebra for Extended Objects_, Phys.Rev.Lett. 63 (1989) 2443 ([spire](https://inspirehep.net/record/26393?ln=en))

reviewed in 

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.8 of _[[Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics]]_, Cambridge monographs of mathematical physics, (1995)


The generalization of this including also the contribution of the [[M5-brane]] was considered in

* {#SorokinTownsend97} [[Dmitri Sorokin]], [[Paul Townsend]], _M-theory superalgebra from the M-5-brane_, Phys.Lett. B412 (1997) 265-273 ([arXiv:hep-th/9708003](http://arxiv.org/abs/hep-th/9708003))

Further detailed discussion along these lines producing also the [[type II supersymmetry algebras]] is in

* Hanno Hammer, _Topological Extensions of Noether Charge Algebras carried by D-p-branes_, Nucl.Phys. B521 (1998) 503-546 ([arXiv:hep-th/9711009](http://arxiv.org/abs/hep-th/9711009))


The full extension was named "M-algebra" in

* [[Ergin Sezgin]], _The M-Algebra_, Phys.Lett. B392 (1997) 323-331 ([arXiv:hep-th/9609086](http://arxiv.org/abs/hep-th/9609086))

In ([D'Auria-Fr&#233; 82](#DAuriaFre82)) the motivation is from the formulation of the fields of [[11-dimensional supergravity]] as connections with values in the [[supergravity Lie 3-algebra]], see at _[[D'Auria-Fré formulation of supergravity]]_. Realization of the M-theory super Lie algebra as the algebra of [[derivations]] of the [[supergravity Lie 3-algebra]] is in 

* {#Castellani05} [[Leonardo Castellani]], _Lie derivatives along antisymmetric tensors, and the M-theory superalgebra_, J. Phys. Math. Volume 3 (2011), 1-7. ([arXiv:hep-th/0508213](http://arxiv.org/abs/hep-th/0508213), [Euclid](http://projecteuclid.org/euclid.jpm/1359468398))

with amplification in

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_ (2013)

* [[nLab:Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Lie n-algebras of BPS charges]]_

  
Discussion of a formulation in terms of [[octonions]] (see also at _[[division algebra and supersymmetry]]_) includes

* A. Anastasiou, [[Leron Borsten]], [[Michael Duff]], L. J. Hughes, S. Nagy, _An octonionic formulation of the M-theory algebra_ ([arXiv:1402.4649](http://arxiv.org/abs/1402.4649))

Arguments that the charges of the M-theory super Lie algebra may be identified inside [[E11]] are given in 

* [[Peter West]], _$E_{11}$, $SL(32)$ and Central Charges_, Phys.Lett.B575:333-342,2003 ([arXiv:hep-th/0307098v2](http://arxiv.org/abs/hep-th/0307098v2))

* [[Paul Cook]], around p. 75 of _Connections between Kac-Moody algebras and M-theory_ ([arXiv:0711.3498](http://arxiv.org/abs/0711.3498))


[[!redirects M-theory Lie algebra]]

[[!redirects M-Lie algebra]]
[[!redirects M-theory algebra]]

[[!redirects M-theory supersymmetry Lie algebra]]
[[!redirects M-theory supersymmetry super Lie algebra]]

[[!redirects M-theory super Lie algebra extension]]
[[!redirects M-theory super Lie algebra extensions]]

[[!redirects DF-algebra]]
[[!redirects DF-algebras]]

[[!redirects D'Auiria-Fré algebra]]
[[!redirects D'Auiria-Fré algebras]]

[[!redirects D'Auiria-Fre algebra]]
[[!redirects D'Auiria-Fre algebras]]

