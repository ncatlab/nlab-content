
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Solid state physics
+-- {: .hide}
[[!include solid state physics -- contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[crystal|crystalline]] material, its *Brillouin torus* is the [[space]] of distinguishable [[momenta]]/[[wave vectors]] of its [[electron|electronic]] excitations. Due to the periodicity of the crystal, also these momenta/wave vectors are (dually) periodically identified, which makes this space an [[n-torus]].

Mathematically, the [[discrete space]] underlying a [[crystal]] is a [[subset]] of a [[Euclidean space]] $S \;\subset\;E^n \simeq \mathbb{R}^n$ (the set of *atomic sites*) which is preserved (as a subset) by the [[group action|action]] of a [[crystallographic group]] $\Lambda \rtimes G \,\subset\, Iso(E)$, where $\Lambda$ is a full [[lattice in a vector space|lattice]] (and $G$ the corresponding [[point group]]). Then its Brillouin torus is the [[Pontrjagin dual group]] of this lattice (eg. [Freed-Moore 13](#FreedMoore13)):

$$
  \mathbb{T}^n_{Br} \,=\, Hom_{Grp}\big(\Lambda, \, S^1 \big)
  \,.
$$



## Related concepts

* [[Bravais lattice]]

* [[Bloch-Floquet theory]]

* [[valence bundle]], [[conduction bundle]]

## References
 {#References}

Textbooks on [[solid state physics]] traditionally speak of the "reciprocal lattice" (e.g. [Kittel 1953](solid+state+physics#Kittel53), [p. 27](http://metal.elte.hu/~groma/Anyagtudomany/kittel.pdf#page=47)) which is the dual lattice $Hom_{Grp}\big(\Lambda, \, \mathbb{Z} \big)$, e.g.:

* [[Michael Reed]], [[Barry Simon]], p. 311 of: Sec. XIII.16 *Schrödinger operators with periodic potentials*, of:  *[[Methods of Modern Mathematical Physics]] -- IV: Analysis of Operators*, Academic Press (1978) 
([ISBN:9780080570457](https://www.elsevier.com/books/iv-analysis-of-operators/reed/978-0-08-057045-7))


* {#Tong2017} [[David Tong]], [§2.2.2](http://www.damtp.cam.ac.uk/user/tong/aqm/solidstate.pdf#page=57) in: *Lectures on solid state physics* (2017) $[$[pdf](http://www.damtp.cam.ac.uk/user/tong/aqm/solidstate.pdf), [webpage](http://www.damtp.cam.ac.uk/user/tong/solidstate.html)$]$

The resulting Brillouin torus $Hom_{Grp}\big(\Lambda, \, \mathbb{R} \big)/Hom_{Grp}\big(\Lambda, \, \mathbb{Z} \big)$ is often left implicit. It is made explicit in:

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]], [p. 52](https://arxiv.org/pdf/1208.5055.pdf#page=52) of: _Twisted equivariant matter_, Ann. Henri Poincaré (2013) 14: 1927 $[$[arXiv:1208.5055](https://arxiv.org/abs/1208.5055), [doi:10.1007/s00023-013-0236-x](https://doi.org/10.1007/s00023-013-0236-x)$]$

[[!redirects Brillouin tori]]

