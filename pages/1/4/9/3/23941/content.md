
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
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

A *Bravais lattice* (terminology originating in the study of [[crystals]] in [[solid state physics]]) is the *equivalence class* of a [[crystal]] [[lattice (discrete subgroup)|lattice]] with *maximal* [[point symmetry]].

Mathematically, this the [[equivalence class]] of the corresponding [[crystallographic group]] $\Lambda \rtimes G_{pt} \;\subset\; \mathbb{R}^d \rtimes \mathrm{O}(d)$ (for $G_{pt} \coloneqq Stab_{O(d)}(\Lambda)$ the full [[stabilizer group]]) under [[conjugation]] by ambient [[linear transformations]] $\phi \,\in\,$ [[GL(n)|$GL(d)$]]:

$$
  \Lambda \rtimes G_{pt}
  \;\;\sim\;\;
  \phi(\Lambda) \rtimes \big( \phi \circ G_{pt} \circ \phi^{-1} \big)
  \,.
$$

(eg. [Schwarzenberger 1972, p. 325](#Schwarzenberger72))

Variant definitions exist, for instance it is of interest to retain handedness and divide out only by [[SL(n)|$SL(d)$]].

All crystal lattices with non-maximal point symmetry may be understood as unions of affine transformations of Bravais lattices.


## Related concepts

* [[crystal]], [[lattice (discrete subgroup)]]

* [[crystallographic group]]

* [[Brillouin torus]]

## References

The concept goes back to:

* {#Bravais1850}  [[Auguste Bravais]], *Mémoire sur les Systèmes Formés par les Points Distribués Régulièrement sur un Plan ou dans L'espace*, J. Ecole Polytech. 19 (1850) 1 $[$[ark:12148/bpt6k96124j](https://gallica.bnf.fr/ark:/12148/bpt6k96124j)$]$

A good review is in:

* [[Helmut G. F. Winkler]], *Hundert ]ahre Bravais Gitter*, Die Naturwissenschaften **37** 17 (1950) $[$[doi:10.1007/BF00738360](https://doi.org/10.1007/BF00738360), [pdf](https://link.springer.com/content/pdf/10.1007/BF00738360.pdf)$]$

Further discussion:

* {#Schwarzenberger72} [[Rolph Ludwig Edward Schwarzenberger]], *Classification of crystal lattices*, Mathematical Proceedings of the Cambridge Philosophical Society, **72** 3 (1972) 325-349 $[$[doi:10.1017/S0305004100047162](https://doi.org/10.1017/S0305004100047162)$]$


* M. Pitteri, G. Zanzotto, *On the Definition and Classification of Bravais Lattices*, Acta Cryst. A **52** (1996) 830-838 $[$[doi:10.1107/S0108767396005971](https://doi.org/10.1107/S0108767396005971)$]$


Lecture notes and textbook accounts:

* {#Engel86} [[Peter Engel]], Section 7 of: *Geometric Crystallography -- An Axiomatic Introduction to Crystallography*, D. Reidel Publishing (1986) $[$[doi:10.1007/978-94-009-4760-3](https://doi.org/10.1007/978-94-009-4760-3)$]$


* [[Peter Engel]], [[Louis Michel]], [[Marjorie Senechal]], Chapter 1 of: *Lattice Geometry*, IHES/P/04/45 (2004) $[$[pdf](https://cds.cern.ch/record/859509/files/cer-002542451.pdf), [cds:859509](https://cds.cern.ch/record/859509)$]$ 


* [[Sheng San Li]], Section 1.2 in: *Semiconductor Physical Electronics*, Springer (2006)   $[$[doi:10.1007/0-387-37766-2_4](https://doi.org/10.1007/0-387-37766-2_4)$]$

* {#Souvignier08} Bernd Souvignier, around Def. 54 in: *Group theory applied to crystallography*, Summer School on Mathematical and Theoretical Crystallography (2008) $[$[pdf](https://www.math.ru.nl/~souvi/krist_09/cryst.pdf)$]$

* {#Muller13} Ulrich Müller, Def. 6.15 in: *Symmetry Relationships between Crystal Structures*, Oxford University Press (2013) $[$[pdf](https://www.xray.cz/kryst/grupy-struktury.pdf)$]$


See also:

* Wikipedia, *[Bravais lattice](https://en.wikipedia.org/wiki/Bravais_lattice)*

[[!redirects Bravais lattices]]

[[!redirects Bravais class]]
[[!redirects Bravais classes]]


[[!redirects hexagonal lattice]]
[[!redirects hexagonal lattices]]

[[!redirects honeycomb lattice]]
[[!redirects honeycomb lattices]]

[[!redirects crystal lattice]]
[[!redirects crystal lattices]]
