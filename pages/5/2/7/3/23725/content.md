
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

Mathematically, the [[discrete space]] underlying a [[crystal]] is a [[subset]] of a [[Euclidean space]] $S \;\subset\;E^n \simeq \mathbb{R}^n$ (the set of *atomic sites*) which is preserved (as a subset) by the [[group action|action]] of a [[crystallographic group]] $\Lambda \rtimes G \,\subset\, Iso(E)$, where $\Lambda$ is a full [[lattice in a vector space|lattice]] (and $G$ the corresponding [[point group]]). Then its Brillouin torus is the [[Pontrjagin dual group]] of this lattice (cf. [Freed & Moore 2013](#FreedMoore13)):

$$
  \mathbb{T}^n_{Br} \,=\, Hom_{Grp}\big(\Lambda, \, S^1 \big)
  \,.
$$



## Related concepts

* [[Brillouin zone]]

* [[Bravais lattice]]

* [[Bloch-Floquet theory]]

* [[valence bundle]], [[conduction bundle]]

## References
 {#References}

The concept is named after:

* {#Brillouin30} [[Léon Brillouin]], *Les électrons libres dans les métaux et le role des réflexions de Bragg*, J. Phys. Radium **1** (1930) 377-400 &lbrack;[doi:10.1051/jphysrad:01930001011037700](https://doi.org/10.1051/jphysrad:01930001011037700), [hal:jpa-00233038](https://hal.archives-ouvertes.fr/jpa-00233038), [pdf](https://hal.archives-ouvertes.fr/jpa-00233038/document)&rbrack;

Textbooks on [[solid state physics]] traditionally speak of the "reciprocal lattice" (e.g. [Kittel 1953](solid+state+physics#Kittel53), [p. 27](http://metal.elte.hu/~groma/Anyagtudomany/kittel.pdf#page=47)) which is the dual lattice $Hom_{Grp}\big(\Lambda, \, \mathbb{Z} \big)$, e.g.:

* [[Michael Reed]], [[Barry Simon]], p. 311 of: Sec. XIII.16 *Schrödinger operators with periodic potentials*, of:  *[[Methods of Modern Mathematical Physics]] -- IV: Analysis of Operators*, Academic Press (1978) 
([ISBN:9780080570457](https://www.elsevier.com/books/iv-analysis-of-operators/reed/978-0-08-057045-7))


* {#Tong2017} [[David Tong]], [§2.2.2](http://www.damtp.cam.ac.uk/user/tong/aqm/solidstate.pdf#page=57) in: *Lectures on solid state physics* (2017) $[$[pdf](http://www.damtp.cam.ac.uk/user/tong/aqm/solidstate.pdf), [webpage](http://www.damtp.cam.ac.uk/user/tong/solidstate.html)$]$

The resulting Brillouin torus $Hom_{Grp}\big(\Lambda, \, \mathbb{R} \big)/Hom_{Grp}\big(\Lambda, \, \mathbb{Z} \big)$ is often left implicit. It is made explicit for instance in:

* {#FreedMoore13} [[Daniel Freed]], [[Gregory Moore]], [p. 52](https://arxiv.org/pdf/1208.5055.pdf#page=52) of: _Twisted equivariant matter_, Ann. Henri Poincaré (2013) 14: 1927 &lbrack;[arXiv:1208.5055](https://arxiv.org/abs/1208.5055), [doi:10.1007/s00023-013-0236-x](https://doi.org/10.1007/s00023-013-0236-x)&rbrack;

* [[Guo Chuan Thiang]], §2.1 in: *Topological Semimetals*, [[Encyclopedia of Mathematical Physics 2nd ed]] **1** (2025) 66-77 &lbrack;[doi:10.1016/B978-0-323-95703-8.00046-X](https://doi.org/10.1016/B978-0-323-95703-8.00046-X), [arXiv:2407.12692](https://arxiv.org/abs/2407.12692)&rbrack;

* [[Kiyonori Gomi]], [[Guo Chuan Thiang]], p. 9 in: *Crystallographic T-duality*, J. Geom. Phys **139** (2019) 50-77 \[<a href="https://doi.org/10.1016/j.geomphys.2019.01.002">doi:10.1016/j.geomphys.2019.01.002</a>, [arXiv:1806.11385](https://arxiv.org/abs/1806.11385)\]

The [[crystallographic group|crystallographic symmetry]] of Brillouin tori:

* Chen Zhang, Z. Y. Chen, Zheng Zhang, Y. X. Zhao: *General Theory of Momentum-Space Nonsymmorphic Symmetry*, Phys. Rev. Lett. **130** (2023) 256601 &lbrack;[doi:10.1103/PhysRevLett.130.256601](https://doi.org/10.1103/PhysRevLett.130.256601), [arXiv:2306.14410](https://arxiv.org/abs/2306.14410)&rbrack;



Texts that make explicit the choice of [[spin structure]] on Brillouin tori:

* Ümit Ertem: *Weyl semimetals and $spin^c$ cobordism* &lbrack;[arXiv:2003.04082](https://arxiv.org/abs/2003.04082)&rbrack;

* Andy Knoll, [[Carsten Timm]]: *Irreducible momentum-space spin structure of Weyl semimetals and its signatures in Friedel oscillations*, Phys. Rev. B **109** (2024) 035145 &lbrack;[doi:10.1103/PhysRevB.109.035145](https://doi.org/10.1103/PhysRevB.109.035145)&rbrack;




[[!redirects Brillouin tori]]

[[!redirects Brillouin zone]]
[[!redirects Brillouin zones]]
