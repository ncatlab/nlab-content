
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Cosmic monopoles


In a [[gauge theory]] with a degenerate [[vacuum]] (such as when a [[Higgs mechanism]] applies), the [[moduli space]] of [[vacua]] is the [[quotient]] $G/H$ (the [[coset]]) of the [[gauge group]] $G$ by the [[stabilizer subgroup]] $H \hookrightarrow G$ of any of these vacua ([[spontaneous symmetry breaking]]).

This means that gauge equivalence classes of vaccum configurations on a [[spacetime]] $X$ are given by [[homotopy]] classes of maps $X \to \Pi(G/H)$ (where the notation on the right denotes the underlying [[homotopy type]] of the [[coset]] space, $\Pi$ is the [[shape modality]]).

If [[spacetime]] is locally to be taken of the form $\mathbb{R} \times (\mathbb{R}^3 - D^3 \times \mathbb{R}^0)$, hence with a 3-dimensional ball-like piece taken out, them homotopy classes of maps $X \to \Pi(G/H)$ are classified by the second [[homotopy group]] $\pi_2(G/H)$. For a given nontrivial element here the correponding [[vacuum]] is said to contain a **cosmic monopole defect**. ("Cosmic" just because this effect is thought to be most relevant on scales of [[cosmology]].)

In other words this means that the vacuum strcture changes continuously as one moves around the string, but has a [[singularity]] on the locus of the string itself.

For more see at _[[QFT with defects]]_ the section _[Topological defects from spontaneously broken symmetry](http://ncatlab.org/nlab/show/QFT+with+defects#DefectsFromBrokenSymmetry)_.

## Examples

### Magnetic monopoles 
 {#MagneticMonopoles}

#### Dirac monopole
 {#DiracMonopole}

In the original [[Dirac charge quantization]] argument an [[electromagnetic field]] is considerd _outside_ a given point in space (line in [[spacetime]]). Mathematically this just corresponds to considering electromagfnetism on the maifold $(\mathbb{R}^3-D^0) \times \mathbb{R}$, but physically this may be taken to model a situation where there is a magnetic monopole defect in the vavuum structure. The _[[Dirac monopole]]_.

This is the classical example of monopoles and often taken to be the default meaning. (In the context of the [[standard model of particle physics]], however, the default meaning is that of electroweak vacuum defect monopoles, discussed [below](#ElectroweakMonopoles).)

Technically, in the sense of the discussion at [[QFT with defects]] in the section _[Topological defects from spontaneous symmetry breaking](QFT%20with%20defects#DefectsFromBrokenSymmetry)_ what happens here is that the [[moduli space]] of the [[instanton sector]] of electromagnetism (= the [[classifying space]] of [[circle group]]-[[principal bundles]]) $BU(1)$ has the [[homotopy type]] of an [[Eilenberg-MacLane space]] $B U(1) \simeq K(\mathbb{Z},2)$. This is by definition a space such that [[homotopy classes]] of [[continuous functions]] from a [[sphere]] into it are classified by the [[integers]]: $\pi_2(B U(1)) \simeq \mathbb{Z}$.

But since there is a [[homotopy equivalence]]

$$
  (\mathbb{R}^3 - D^0)\times \mathbb{R} \simeq S^2
$$

of [[Minkowski spacetime]] with the [[worldline]] of a point removes, this means precisely that the possible [[instanton]] field configurations of the [[electromagnetic field]] on such a spacetime is given by an [[integer]]. This integer is called the _[[magnetic charge]]_ of the monopole defect. (Mathematically it is the [[first Chern class]] of the $U(1)$-[[principal bundle]] which underlies the electromagnetic field).

#### Kaluza-Klein monopole

The gravitational incarnation of the [[Dirac monopole]] under [[Kaluza-Klein compactification]] is the _[[Kaluza-Klein monopole]]_. See there for more.

#### Yang monopole and 't Hooft monopole

The generalization of the [[Dirac monopole]] from $U(1)$-[[Yang-Mills theory]] in 3+1 dimensional [[spacetime]] to $SU(2)$-[[Yang-Mills theory]] in 5+1 dimensional spacetime is the _[[Yang monopole]]_.

With the [[Higgs field]] included, there is the _[['t Hooft-Polyakov monopole]]_.


### Electroweak monopoles
 {#ElectroweakMonopoles}

For a $G$-[[gauge theory]] with [[spontaneous symmetry breaking]] of the [[vacuum]] from [[gauge group]] $G$ down to some [[subgroup]] $H \hookrightarrow G$, monopole [[topological defects]] in the vacuum structure are classified by the second [[homotopy group]] $\pi_2(G/H)$ of the [[coset space]] (as explained at _[[QFT with defects]]_).

For the gauge theory of the [[electroweak force]] with its [[Higgs mechanism]] that is of relevance in the [[standard model of particle physics]]. This would mean that monopoles are classified by 

$$
  \pi_2( (SU(2) \times U(1))_{ew} / U(1)_{em} )
  \,.
$$

However, in ([Cho-Maison](#ChoMaison)) it is claimed that the true topology of the moduli space of vacua in electroweak symmetry breaking is topologically more interesting. The corresponding phenomenology of vacuum defect monopoles of this kind is discussed in ([Cho-Kim-Yoon13](#ChoKimYoon13)).


## Related concepts

* [[fiber bundles in physics]]

* [[domain wall]], [[cosmic string]]

* [[vortex]]

* [[caloron correspondence]]

* [[dyon]]

* [[Nahm transform]], [[Bogomolny equation]]

[[!include fields and quanta - table]]


## References

Textbook account:

* [[Mikio Nakahara]], Section 10.5.2 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)

Experimental search for magnetic monopoles via the [[Schwinger effect]]:

* B. Acharya et al., *First experimental search for production of magnetic monopoles via the Schwinger mechanism* ([arXiv:2106.11933](https://arxiv.org/abs/2106.11933))


A general account of [[vacuum]] [[QFT with defects|defects]] such as [[domain walls]] and monopoles is in 

* [[Alexander Vilenkin]], E.P.S. Shellard, _Cosmic strings and other topological defects_, Cambridge University Press (1994)
 {#VilenkinShellard94}

Detailed discussion of the [[phenomenology]] of [[electroweak force|electroweak]] monopoles is in 

* {#ChoMaison} Y.M. Cho and D. Maison, Phys. Lett. B391, 360 (1997)
 

* {#ChoKimYoon13} Y. M. Cho, Kyoungtae Kim, J. H. Yoon, _Finite Energy Electroweak Dyon_ ([arXiv:1305.1699](http://arxiv.org/abs/1305.1699))
 
Discussion of monopole [[correlators]]:

* {#Iqbal14} [[Nabil Iqbal]], _Monopole correlations in holographically flavored liquids_, Phys. Rev. D 91, 106001 (2015) ([arXiv:1409.5467](https://arxiv.org/abs/1409.5467))


[[!redirects monopoles]]

[[!redirects cosmic monopole]]
[[!redirects cosmic monopoles]]

[[!redirects magnetic monopole]]
[[!redirects magnetic monopoles]]
