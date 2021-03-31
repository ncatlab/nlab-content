
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

The _twistor fibration_ $\mathbb{C}P^3 \to S^4$ ([Atyiah-Hitchin-Singer 78, Ex. 2 on p. 438](#AtyiahHitchinSinger78), [Atiyah 79, Sec. III.1](#Atiyah79), see also [Bryant 82](#Bryant82), [ArmstrongSalamon14](#ArmstrongSalamon14), [ABS 19](#ABS19)), also called, in its [[coset space]]-version $SO(5)/U(2) \to SO(5)/SO(4)$, the _Calabi-Penrose fibration_ (apparently starting with [Lawson 85, Sec. 3](#Lawson85), see also, e.g., [Loo 89](#Loo89), [Seade-Verjovsky 03, 3](#SeadeVerjovsky03) for this usage, see [Nordstrom 08, Lemma 2.31](#Nordstrom08) for review of Calabi's construction [Calabi 67](#Calabi67), [Calabi 68](#Calabi68)) is a [[fiber bundle]]-structure on [[complex projective 3-space]] over the [[4-sphere]] with [[2-sphere]] ([[Riemann sphere]]) [[fibers]]:

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

If one identifies the 4-sphere as the [[quaternions|quaternionic]] [[projective space|projective line]]  $S^4 \simeq \mathbb{H}P^1$, then the fibration $p$ here is given by sending [[complex number|complex]] lines to the [[quaternions|quaternionic]] lines which they span ([Atiyah 79, III (1.1)](#Atiyah79), see also [Seade-Verjovsky 03, p. 198](https://www.e-periodica.ch/digbib/view?pid=ens-001:2003:49::488#513)):

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

## Generalizations

It is possible to define a twistor fibration over each $S^{2n}$, where the resulting manifold is a [[complex manifold]] endowed with a [[holomorphic]] $n$-plane field transverse to the fibers of the mapping. Namely, writing $S^{2n}=SO(2n+1)/SO(2n)$, then, using the inclusion $U(n) \subset SO(2n)$, one has the coset fibration 
$$Z_n=SO(2n+1)/U(n) \to SO(2n+1)/SO(2n).$$
The manifold $Z_n$ canonically has the structure of a complex manifold and is known as the _twistor space_ of $S^{2n}$. 

There are generalizations of this picture for each of the so-called 'inner' [[symmetric spaces]] $G/K$ where $K$ is the fixed subgroup of an [[involution]] that is an [[inner automorphism]] of $G$. The twistor fibration is of the form $G/U \to G/K$ where $U \subset K$ is a subgroup such that $K/U$ (the typical fiber of the fibration) is an Hermitian symmetric space. There are also other kinds of twistor spaces over $G/K$ that are [[flag manifolds]] of the form $G/T$ where $T \subset K$ is a [[maximal torus]]. (For these generalizations see [Bryant 85](#Bryant85).)

## Related concepts

* [[quaternionic Hopf fibration]]

* [[twistor space]], [[complex projective 3-space]]

* [[metric cone over complex projective 3-space]]


## References

* {#Calabi67} [[Eugenio Calabi]], _Minimal immersions of surfaces in euclidean spheres_, J. Differential Geometry (1967), 111-125 ([euclid:jdg/1214427884](https://projecteuclid.org/euclid.jdg/1214427884))

* {#Calabi68} [[Eugenio Calabi]], _Quelques applications de l’analyse complexe aux surfaces d’aire minima_, Topics in Complex Manifolds (Ed. H. Rossi), Les Presses de l’Universit ́e de Montr ́eal (1968), 59-81 ([naid:10006413960](https://ci.nii.ac.jp/naid/10006413960))

* {#AtyiahHitchinSinger78} [[Michael Atiyah]], [[Nigel Hitchin]], [[Isadore Singer]], Example 2 on p. 438 in: _Self-Duality in Four-Dimensional Riemannian Geometry_, Proceedings of the Royal Society of London. Series A, Mathematical and Physical Sciences Vol. 362, No. 1711 (Sep. 12, 1978), pp. 425-461 (37 pages) ([jstor:79638](https://www.jstor.org/stable/79638), [doi:10.1098/rspa.1978.0143](https://doi.org/10.1098/rspa.1978.0143))

* {#Atiyah79} [[Michael Atiyah]], Section III.1 of: _Geometry of Yang-Mills fields_, Pisa, Italy: Sc. Norm. Sup. (1979) 98 ([spire:150867](https://inspirehep.net/literature/150867), [pdf](https://pdfs.semanticscholar.org/b523/d376f11a531fa5a4692401902a17ee18861f.pdf))

* {#Bryant82} [[Robert Bryant]], Section 1 of: _Conformal and minimal immersions of compact surfaces into the 4-sphere_, J. Differential Geom. Volume 17, Number 3 (1982), 455-473 ([euclid:jdg/1214437137](https://projecteuclid.org/euclid.jdg/1214437137))


* {#Bryant85} [[Robert Bryant]], _Lie groups and twistor spaces_, Duke Mathematical Journal 52 (1985), pp. 223–261, ([euclid:dmj/1077304286](https://projecteuclid.org/euclid.dmj/1077304286))

* {#Lawson85} [[H. Blaine Lawson]], _Surfaces minimales et la construction de Calabi-Penrose_,  Séminaire Bourbaki : volume 1983/84, exposés 615-632, Astérisque no. 121-122  (1985), Talk no. 624, p. 197-211 ([numdam:SB_1983-1984__26__197_0](http://www.numdam.org/item/SB_1983-1984__26__197_0))

* [[Simon Salamon]], p. 218-220 of: _Harmonic and holomorphic maps_,  In: E. Vesentini  (eds.) _Geometry Seminar "Luigi Bianchi" II - 1984_, Lecture Notes in Mathematics, vol 1164. Springer 1985 ([doi:10.1007/BFb0081912](https://doi.org/10.1007/BFb0081912))

* [[James Eells]], [[Simon Salamon]], Section 8 of: _Twistorial construction of harmonic maps of surfaces into four-manifolds_,  Annali della Scuola Normale Superiore di Pisa - Classe di Scienze, Serie 4, Volume 12 (1985) no. 4, p. 589-640 ([numdam:ASNSP_1985_4_12_4_589_0](http://www.numdam.org/item/ASNSP_1985_4_12_4_589_0))

* {#Loo89} [[Bonaventure Loo]], _The space of harmonic maps of $S^2$ into $S^4$_, Transactions of the American Mathematical Society Vol. 313, No. 1 (1989) ([jstor:2001066](https://www.jstor.org/stable/2001066))

* {#SeadeVerjovsky02} [[José Seade]], [[Alberto Verjovsky]], Section 2 of: _Higher dimensional complex Kleinian groups_,  Math Ann 322, 279–300 (2002) ([doi:10.1007/s002080100247](https://doi.org/10.1007/s002080100247))

* {#SeadeVerjovsky03} Le, [[José Seade]], [[Alberto Verjovsky]], Section 4 of: _Quadrics, orthogonal actions and involutions in complex projective space_, L'Enseignement Math&eacute;matique, t.  49 (2003) ([e-periodica:001:2003:49::488](https://www.e-periodica.ch/digbib/view?pid=ens-001:2003:49::488#488))

* {#Nordstrom08} Jonas Nordstrom, _Calabi's construction of Harmonic maps from $S^2$ to $S^n$_, Lund University 2008 ([pdf](http://www.matematik.lu.se/matematiklu/personal/sigma/students/Jonas-Nordstrom-BSc.pdf), [[NordstromCalabiConstruction.pdf:file]])

* Angel Cano, Juan Pablo Navarrete, [[José Seade]], Section 10.1 in: _Kleinian Groups and Twistor Theory_, In: _Complex Kleinian Groups_, Progress in Mathematics, vol 303. Birkhäuser 2013 ([doi:10.1007/978-3-0348-0481-3_10](https://doi.org/10.1007/978-3-0348-0481-3_10))

* {#ArmstrongSalamon14} John Armstrong, [[Simon Salamon]], _Twistor Topology of the Fermat Cubic_, SIGMA 10 (2014), 061, 12 pages ([arXiv:1310.7150](https://arxiv.org/abs/1310.7150))

* [[Bobby Acharya]], [[Robert Bryant]], [[Simon Salamon]], _A circle quotient of a $G_2$ cone_, Differential Geometry and its Applications Volume 73, December 2020, 101681  ([arXiv:1910.09518](https://arxiv.org/abs/1910.09518), [doi:10.1016/j.difgeo.2020.101681](https://doi.org/10.1016/j.difgeo.2020.101681))




In [[noncommutative geometry]]:

* Simon Brain, Giovanni Landi, _Differential and Twistor Geometry of the Quantum Hopf Fibration_, Commun. Math. Phys. 315 (2012):489-530 ([arXiv:1103.0419](https://arxiv.org/abs/1103.0419))


In higher dimensions:

Over $\mathbb{H}P^3$:

* {#LooVerjovsky94} [[Bonaventure Loo]], [[Alberto Verjovsky]], _On quotients of Hopf fibrations_, in: Rendiconti dell’Istituto di Matematica dell’Università di Trieste. An International Journal of Mathematics, 26 (1994), pp. 103-108 ([hdl:10077/4637](	http://hdl.handle.net/10077/4637), [pdf](https://www.openstarts.units.it/bitstream/10077/4637/1/LooVerjovskyRendMat26.pdf))

[[!redirects twistor fibrations]]


[[!redirects Calabi-Penrose fibration]]
[[!redirects Calabi-Penrose fibrations]]

