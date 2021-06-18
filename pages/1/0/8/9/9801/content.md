
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
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

The _gauged WZW model_ is a [[field (physics)|field]] [[theory (physics)]] which combines the [[WZW model]] with [[gauge theory]]:
given a ([[simple Lie group|simple]]) [[Lie group]] $G$ and a [[subgroup]] $H \hookrightarrow G \times G$, the corresponding gauged WZW model is a 2-dimensional [[prequantum field theory]] on some [[worldvolume]] $\Sigma_2$ whose [[field (physics)|fields]] are pairs consisting of a smooth function $\Sigma_2 \to G$ and a [[Lie algebra valued 1-form]] $A \in \Omega^1(\Sigma_2, \mathfrak{h})$, with values in the [[Lie algebra]] of $H$.

Where the [[Lagrangian]]/[[action functional]] of the ordinary [[WZW model]] is the sum/product of a standard [[kinetic action]] and the [[surface holonomy]] of a [[circle 2-bundle with connection]] whose [[curvature]] 3-form is the canonical 3-form $\langle \theta \wedge [\theta \wedge \theta]\rangle \in \Omega^3(G)^G$, so the action functional of the gauged WZW model is that obtained by refining this circle 2-bundle to the $H$-[[equivariant cohomology|equivariant]] [[differential cohomology]] of $G$, with [[curvature]] 3-form in [[equivariant de Rham cohomology]].

## Definition
 {#Definition}

The [[Chevalley-Eilenberg algebra]] of the [[Lie algebra]] $\mathfrak{g}$ is naturally identified with the sub-algebra of [[left invariant differential forms]] on $G$:

$$
  CE(\mathfrak{g}) \simeq \Omega^\bullet(G)^G
  \,.
$$

The ordinary [[WZW model]] is given by the basic [[circle 2-bundle with connection]] on $G$ whose [[curvature]] 3-form is 

$$
  H = \langle \theta \wedge [\theta \wedge \theta]\rangle 
  \in \Omega^3(G)^G
  \,.
$$

Now for $H \hookrightarrow G$ a [[subgroup]], write 

$$
  CE(\mathfrak{g}//\mathfrak{h})
 \coloneqq 
  \Omega^\bullet(G, \mathfrak{h}^\ast[1])^G
$$

for the corresponding dg-algebra of (say) the [[Cartan model]] for [[equivariant de Rham cohomology]] on $G$. There is a canonical projection

$$
  CE(\mathfrak{g}//\mathfrak{h})
  \to 
  CE(\mathfrak{g})
  \,.
$$

A curvature 3-form for the **gauged WZW model** is a 3-cocycle 

$$
  \tilde H \in CE^3(\mathfrak{g}//\mathfrak{h})
$$

in this [[equivariant de Rham cohomology]] which lifts $H \coloneqq \langle \theta \wedge [\theta \wedge \theta]\rangle$ through this projection.

 One finds ([Witten 92, appendix](#Witten92)) that in terms of the degree-2 generators $\{F^a\}$ of the [[Cartan model]] (see there) with respect to some [[basis]] $\{t_a\}$ of $\mathfrak{g}$, these lifts are of the form ([Witten 92, (A.14)](#Witten92))

{#WZWCurvatureInCartanModel}
$$
  \tilde H = H + \lambda_a \wedge F^a
$$

where $\lambda_a \in \Omega^1(G)$ is given by (in [[matrix Lie algebra]] notation)

$$
  \lambda_a
  = 
  \left\langle 
    t_a^l \cdot (d g)g^{-1} 
    +
    t_a^r \cdot g^{-1} d g
  \right\rangle
$$

and exist precisely if ([Witten 92, (A.16)](#Witten92)) for all pairs of basis elements

$$
  \langle 
    t_a^l \cdot t_b^l
    -
    t_a^r \cdot t_b^r
  \rangle
  = 0
  \,.
$$

This condition had originally been seen as a [[anomaly cancellation]]-condition of the gauged WZW model. A systematic discussion of these obstructions in [[equivariant de Rham cohomology]] is in ([Figueroa-O'Farrill-Stanciu 94](#FigueroaOFarrillStanciu94)).

Now by [[schreiber:∞-Wess-Zumino-Witten theory]], the corresponding WZW model has as target the [[smooth groupoid]] $\tilde G//H$ such that maps into it are locally a map $g$ into $G$ together with 1-form potentials $A^a$ for the $F^a$, and the WZW term is locally a 2-form built from $d g$ and $A^a$ such that its curvature 3-form is $\tilde H$. This is the **gauged WZW model** ([Witten 92, (A.16)](#Witten92)).


## Properties

### Partition function in (equivariant) elliptic cohomology
 {#PartitionFunctionInEllipticCohomology}

The [[partition function]] of the gauged WZW model as an [[elliptic genus]] is considered in ([Henningsonn 94, (8)](#Henningson94)). When done properly this should give elements in [[equivariant elliptic cohomology]], hence an [[equivariant elliptic genus]].

## Related concepts

* [[coset WZW model]]

* [[gauged linear sigma model]]

## References


[[!include WZW term of QCD chiral perturbation theory -- references]]


### General gauged WZW models

The original articles are


* [[Edward Witten]], _Nonabelian bosonization in two dimensions_, Commun. Math. Phys. 92 (1984) 455 ([euclid:cmp/1103940923](https://projecteuclid.org/euclid.cmp/1103940923))

* [[Krzysztof Gawedzki]], A. Kupiainen, _G/H conformal field theory from gauged WZW model_ Phys. Lett. 215B, 119 (1988); 


* [[Krzysztof Gawedzki]], A. Kupiainen, _Coset construction from functional integrals_, Nucl. Phys. B 320 (FS), 649 (1989)

* [[Krzysztof Gawedzki]], in _From Functional Integration, Geometry and Strings_, ed. by Z. Haba and J. Sobczyk (Birkhaeuser, 1989).

The (curvature of the)gauged WZW term was recognized/described as a  [[cocycle]] in [[equivariant de Rham cohomology]] is in the appendix of 

* {#Witten92} [[Edward Witten]], _On holomorphic factorization of WZW and coset models_,  Comm. Math. Phys. Volume 144, Number 1 (1992), 189-212. ([EUCLID](http://projecteuclid.org/euclid.cmp/1104249222))
 

This is expanded on in 

* {#FigueroaOFarrillStanciu94} [[José Figueroa-O'Farrill]], S Stanciu, _Gauged Wess-Zumino terms and Equivariant Cohomology_, Phys.Lett. B341 (1994) 153-159 ([arXiv:hep-th/9407196](http://arxiv.org/abs/hep-th/9407196))

* [[José de Azcárraga]],  J. C. Perez Bueno, _On the general structure of gauged Wess-Zumino-Witten terms_ ([arXiv:hep-th/9802192](http://arxiv.org/abs/hep-th/9802192))
  

A quick review of this class of 3-cocycles in equivariant de Rham cohomology is also in section 4.1 of 

* Hugo Garcia-Compean, Pablo Paniagua, [[Bernardo Uribe]], _Equivariant extensions of differential forms for non-compact Lie groups_ ([arXiv:1304.3226](http://arxiv.org/abs/1304.3226))

which further generalizes the discussion to non-compact Lie groups.

See also

* [[Edward Witten]], _The $N$ matrix model and gauged WZW models_, Nuclear Physics B Volume 371, Issues 1&#8211;2, 2 March 1992, Pages 191&#8211;245

* Stephen-wei Chung, S.-H. Henry Tye, _Chiral Gauged WZW Theories and Coset Models in Conformal Field Theory_, Phys. Rev. D47:4546-4566,1993 ([arXiv:hep-th/9202002](http://arxiv.org/abs/hep-th/9202002))

* Konstadinos Sfetsos, _Gauged WZW models and Non-abelian duality_,  	Phys.Rev. D50 (1994) 2784-2798 ([arXiv:hep-th/9402031](http://arxiv.org/abs/hep-th/9402031))

* [[Elias Kiritsis]], _Duality in gauged WZW models_ ([pdf](http://hep.physics.uoc.gr/~kiritsis/papers2/dual.pdf))

The [[partition function]]/[[elliptic genus]] of the SU(2)/U(1) gauged WZW model is considered in 

* {#Henningson94} [[Måns Henningson]], _N=2 gauged WZW models and the elliptic genus_, Nucl.Phys. B413 (1994) 73-83 ([arXiv:hep-th/9307040](http://arxiv.org/abs/hep-th/9307040))

Emphasis of the special case of abelian gauging in Section 2 of

* {#Forste04} [[Stefan Förste]],  _Deformations of WZW models_, Class. Quant. Grav. 21 (2004) S1517-1522 ([arXiv:hep-th/0312202](https://arxiv.org/abs/hep-th/0312202))

[[!redirects gauged WZW models]]


[[!redirects gauged Wess-Zumino-Witten model]]
[[!redirects gauged Wess-Zumino-Witten models]]

[[!redirects gauged WZW-model]]
[[!redirects gauged WZW-models]]

