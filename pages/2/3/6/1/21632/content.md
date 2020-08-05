
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _twistor fibration_ ([Atiyah 79, Sec. III.1](#Atiyah79)) or _Calabi-Penrose fibration_ 
([Seade-Verjovsky 03, 3](#SeadeVerjovsky03)) is a [[fiber bundle]]-structure on [[complex projective 3-space]] over the [[4-sphere]] with [[2-sphere]] ([[Riemann sphere]]) [[fibers]]:

$$
  \array{
    \mathbb{C}P^1 
      &\longrightarrow&
    \mathbb{C}P^3
    \\
    && 
    \big\downarrow^{\mathrlap{p}}
    \\
    && S^4
  }
$$

If one identifies the 4-sphere as the [[quaternions|quaternionic]] [[projective space|projective line]]  $S^4 \simeq \mathbb{H}P^1$, then the fibration $p$ here is given by sending complex lines to quaternionic lines ([Atiyah 79, III (1.1)](#Atiyah79), [Seade-Verjovsky 03, p. 198](https://www.e-periodica.ch/digbib/view?pid=ens-001:2003:49::488#513)):

$$
  \array{
    \mathbb{C}P^3 
    &\overset{p}{\longrightarrow}&
    \mathbb{H}P^1
    \\
    \{x \cdot z \vert z \in \mathbb{C}\}
    &\mapsto&
    \{x \cdot q \vert q \in \mathbb{H}\}
  }
  \,,
$$

for any $x \in \mathbb{C}^4 \simeq_{\mathbb{R}} \mathbb{H}^2$.

## Related concepts

* [[quaternionic Hopf fibration]]

* [[twistor space]]

## References

* {#Atiyah79} [[Michael Atiyah]], Section III.1 of: _Geometry of Yang-Mills fields_, Pisa, Italy: Sc. Norm. Sup. (1979) 98 ([spire:150867](https://inspirehep.net/literature/150867), [pdf](https://pdfs.semanticscholar.org/b523/d376f11a531fa5a4692401902a17ee18861f.pdf))

* [[Robert Bryant]], Section 1 of: _Conformal and minimal immersions of compact surfaces into the 4-sphere_, J. Differential Geom. Volume 17, Number 3 (1982), 455-473 ([euclid:jdg/1214437137](https://projecteuclid.org/euclid.jdg/1214437137))

* [[Simon Salamon]], p. 218-220 of: _Harmonic and holomorphic maps_,  In: E. Vesentini  (eds.) _Geometry Seminar "Luigi Bianchi" II - 1984_, Lecture Notes in Mathematics, vol 1164. Springer 1985 ([doi:10.1007/BFb0081912](https://doi.org/10.1007/BFb0081912))

* [[James Eells]], [[Simon Salamon]], Section 8 of: _Twistorial construction of harmonic maps of surfaces into four-manifolds_,  Annali della Scuola Normale Superiore di Pisa - Classe di Scienze, Serie 4, Volume 12 (1985) no. 4, p. 589-640 ([numdam:ASNSP_1985_4_12_4_589_0](http://www.numdam.org/item/ASNSP_1985_4_12_4_589_0))

* {#SeadeVerjovsky02} [[José Seade]], [[Alberto Verjovsky]], Section 2 of: _Higher dimensional complex Kleinian groups_,  Math Ann 322, 279–300 (2002) ([doi:10.1007/s002080100247](https://doi.org/10.1007/s002080100247))

* {#SeadeVerjovsky03} Le, [[José Seade]], [[Alberto Verjovsky]], Section 4 of: _Quadrics, orthogonal actions and involutions in complex projective space_, L'Enseignement Math&eacute;matique, t.  49 (2003) ([e-periodica:001:2003:49::488](https://www.e-periodica.ch/digbib/view?pid=ens-001:2003:49::488#488))


[[!redirects Calabi-Penrose fibrations]]

[[!redirects twistor fibration]]
[[!redirects twistor fibrations]]
