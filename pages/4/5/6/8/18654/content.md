

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+-- {: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[nuclear physics]], specifically in the [[chiral perturbation theory]] of [[quantum chromodynamics]], the _pion_ or _pi-meson_ ($\pi$-meson) is the [[isospin]]-triplet scalar-[[meson]] [[field (physics)|field]] in the first-[[generation of fermions]], i.e. a [[bound state]] of an [[up quark]] and a [[down quark]] (a [[light meson]]):

[[!include flavors of fundamental particles -- table]]

\linebreak

## Details

### As the Goldstone boson of chiral symmetry breaking

From the point of view of the [[quark]]-[[model (in theoretical physics)|model]] of [[nuclear physics]], the pion is the [[Goldstone boson]] corresponding to the [[spontaneous symmetry breaking]] of the "[[chiral symmetry|chiral]]"-[[symmetry group]] $SU(2)_R \times SU(2)_L$ to the [[diagonal]] [[subgroup]] $SU(2)_V$, by the [[vacuum expectation value]] $\langle q \bar q\rangle \neq 0$ of the [[quark]]-[[condensate]].
 
(e.g. [Machleidt-Entem 11, 2.1.3](#MachleidtEntem11))

### Plain pion field

Hence, in the sense of the [[Wigner classification]], the pion field transforms in the [[sign representation]] of the [[Lorentz group]]/[[Pin group]] (is a spacetime [[pseudoscalar]]) and in the [[adjoint representation]] of the [[isospin]] [[group]] [[SU(2)]]

\begin{imagefromfile}
    "file_name": "LightAndChiralPartnerMesonFieldsPinIII.jpg",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": 0,
        "right": 10,
        "bottom": 0,
        "left": 20
    }
\end{imagefromfile}


As such, a pion [[field history]] is a [[smooth function]] from [[spacetime]] to the [[Lie algebra]] [[su(2)]]

\[
  \label{PlainPionField}
  i \vec \pi
  \;\colon\;
  \mathbb{R}^{3,1}
  \longrightarrow
  \mathfrak{su}(2)
  \,,
\]

where the vecotr notation on the left is to indicate that this is, at each spacetime point ([[event]]) $x \in \mathbb{R}^{3,1}$, an element in a [[real numbers|real]] 3-dimensional [[vector space]]

$$
  i \vec \pi(x) \;\in\; \mathfrak{su}(2) \;\simeq_{\mathbb{R}}\; \mathbb{R}^3
  \,.
$$

This means that for any choice of [[linear basis]] of $\mathfrak{su}(2)$, the pion field decomposes as three real-valued fields. 

In the [[nuclear physics]]-literature the common choice is that corresponding to the [[Cartan-Weyl basis]] 

$$
  \mathrm{Span}
  \big(
    \{t_+, t_-, t_0\} 
  \big)
  \;\simeq_{\mathbb{R}}\;
  \mathfrak{su}(2)
$$

in terms of which the components of the pion field are hence denoted as follows

| [[pion]] field component | [[quark]] [[bound state]] |
|--------------------------|---------------------------|
|      $\pi^0$             |         $u \bar u$ or $d \bar d$ |
|      $\pi^+$             |         $u \bar d$        |
|      $\pi^-$             |         $d \bar u$       |

\linebreak

### Exponentiated pion field

Especially in [[chiral perturbation theory]], the pion field is typically represented as the [[exponentiation]] of (eq:PlainPionField) to an [[SU(2)]]-valued [[field (physics)|field]]

\[
  \label{ExponentiatedPionField}
  e^{i \vec \pi/f_\pi}
  \;\colon\;
  \mathbb{R}^{3,1}
  \longrightarrow
  SU(2)
  \,,
\]

([Witten 83, (2)](#Witten83), [Adkins-Nappi 84, (1)-(3)](#AdkinsNappi84))
nowadays called the _exponentiated pion field_ or often just _the chiral field_, for review see [Machleidt-Entem 11, (2.29)](#MachleidtEntem11), [Rho et al. 16, around (1)](#RhoEtAl16).



Here the [[physical unit|unit]] $f_\pi$ is called the _pion decay constant_.

Assuming that the pion field [[vanishing at infinity|vanishes at spatial infinity]] hence means that the exponentiated pion field is a [[map]]

$$
  e^{i \vec \pi/f_\pi}
  \;\colon\;
  \mathbb{R}^{0,1} \times (\mathbb{R}^3)^{cpt}
  \;=\;
  \mathbb{R}^{0,1} \times S^3
  \longrightarrow
  S^3 
  \simeq
  SU(2)
$$

from (the [[time]]-axis [[product manifold|times]]) the [[3-sphere]] to [[SU(2)]]. The [[homotopy class]] of this [[continuous function]], an element of the ([[cohomotopy|co-]])[[homotopy group of spheres]] $\pi_3(S^3) \simeq \pi^3(S^3) \simeq \mathbb{Z}$, is the [[Skyrmion]]-number, or, in fact, the [[baryon]]-number, encoded in the [knotted stucture](On+Vortex+Atoms#RanadaTrueba01) of the pion field.

### Relation to baryon current

Explicitly, the [[baryon current]] is the [[Wess-Zumino-Witten term]] in the [[exponentiated pion field]] ([Witten 83a](#Witten83a), [Witten 83b](#Witten83b)):

$$
  \begin{aligned}
  B_{top}
  & \coloneqq \;
  Tr
  \big( 
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
    \wedge
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
    \wedge
    ( e^{-i \vec \pi/f_\pi} d e^{i \vec \pi/f_\pi} )
  \big)
  \\
  & =\;
  \big\langle
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
    \wedge
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
    \wedge
    (e^{i \vec \pi/f_\pi})^\ast(\theta)
  \big\rangle
  \;\;\in\;
  \Omega^3(\mathbb{R}^{3,1})
  \end{aligned}
$$

Here the expression in the first line uses the fact that [[SU(2)]] is a [[matrix group]], while the second line exporesses the same via [[pullback of differential forms|pullback]] of the [[Maurer-Cartan form]] $\theta$ from the group manifold.

### Relation to Skyrmions

The [[skyrmion]]-model (see there) realizes [[baryons]] as [[solitons]]/[[instantons]] in the exponentiated pion field.

## Related concepts

* [[omega-meson]],[[rho meson]]

* [[kaon]]

* [[B-meson]]

* [[quarkonium]]


## References

### General

Introduction and survey:

* {#MachleidtEntem11} [[Rupert Machleidt]], [[David Rodríguez Entem]], _Chiral effective field theory and nuclear forces_, Phys. Rept. 503:1-75, 2011 ([arXiv:1105.2919](https://arxiv.org/abs/1105.2919), [doi:10.1016/j.physrep.2011.02.001](https://doi.org/10.1016/j.physrep.2011.02.001))

* {#Brambilla14} Brambilla et al., Section 3.2.7 of: _[[QCD and strongly coupled gauge theories - challenges and perspectives]]_, Eur Phys J C Part Fields. 2014; 74(10): 2981  ([arXiv:1404.3723](https://arxiv.org/abs/1404.3723), [doi:10.1140/epjc/s10052-014-2981-5](https://link.springer.com/article/10.1140%2Fepjc%2Fs10052-014-2981-5))


See also

* Wikipedia, _[Pion](https://en.wikipedia.org/wiki/Pion)_

### Decays and interactions

On $\gamma \to \pi^0 + \pi^+ + \pi^-$:

* Ruvi Aviv, [[Anthony Zee]], _Low-Energy Theorem for $\gamma \to 3 \pi$_
Phys. Rev. D 5, 2372 (1972) ([doi:10.1103/PhysRevD.5.2372](https://doi.org/10.1103/PhysRevD.5.2372))

* {#Witten83a} [[Edward Witten]], _Global aspects of current algebra_, Nuclear Physics B Volume 223, Issue 2, 22 August 1983, Pages 422-432 (<a href="https://doi.org/10.1016/0550-3213(83)90063-9">doi:10.1016/0550-3213(83)90063-9</a>)

* {#BDDL09}  M. Benayoun, P. David, L. DelBuono, O. Leitner, _A Global Treatment Of VMD Physics Up To The $\phi$: I. $e^+ e^-$ Annihilations, Anomalies And Vector Meson Partial Widths_, Eur. Phys. J. C65:211-245, 2010 ([arXiv:0907.4047](https://arxiv.org/abs/0907.4047))

On [[pion]]-[[nucleon]] [[interaction]]:

* E. Ruiz Arriola, J. E. Amaro, R. Navarro Perez, _Three pion nucleon coupling constants_, Modern Physics Letters A Vol. 31, No. 28, 1630027 (2016) ([arXiv:1606.02171](https://arxiv.org/abs/1606.02171))


On the [[Dalitz decay]] of the [[pion]]:

* {#Dalitz51} [[Richard Dalitz]], _On an alternative decay process for the neutral $\pi$-meson_, Proceedings of the Physical Society. Section A 64 (7), 667, 1951 ([doi:10.1088/0370-1298/64/7/115](https://doi.org/10.1088/0370-1298/64/7/115))

* {#KKN02} Karol Kampf, Marc Knecht, Jiri Novotny, _Some aspects of Dalitz decay $\pi^0 \to e^+ e^- \gamma$_,  presented at Int. Conf. Hadron Structure '02, September 2002, Slovakia ([arXiv:hep-ph/0212243](https://arxiv.org/abs/hep-ph/0212243))

* {#KKN06} Karol Kampf, Marc Knecht, Jiri Novotny, _The Dalitz decay $\pi^0 \to e^+ e^- \gamma$ revisited_, Eur. Phys. J. C46:191-217, 2006 ([arXiv:hep-ph/0510021](https://arxiv.org/abs/hep-ph/0510021))

* {#Berghauser10} Henning Berghäuser, _Investigation of the Dalitz decays and the electromagnetic form factors of the $\eta$ and $\pi^0$-meson_, 2010 ([spire:1358057](https://inspirehep.net/literature/1358057))

* {#Kunkel12} M. Kunkel, _Dalitz Decays of Pseudo-Scalar Mesons_, talk at [Light Meson Decays Workshop August 5, 2012](https://www.jlab.org/conferences/lmd2012/) ([[KunkelDalitzDecay.pdf:file]])

* Sergi González-Solís, _Single and double Dalitz decays of $\pi^0$, $\eta$ and $\eta'$ mesons_, Nuclear and Particle Physics Proceedings Volumes 258–259, January–February 2015, Pages 94-97 ([doi:10.1016/j.nuclphysbps.2015.01.021](https://doi.org/10.1016/j.nuclphysbps.2015.01.021))

* Esther Weil, Gernot Eichmann, Christian S. Fischer, Richard Williams, section III.A of: _Electromagnetic decays of the neutral pion_, Phys. Rev. D 96, 014021 (2017) ([arXiv:1704.06046](https://arxiv.org/abs/1704.06046))



### Exponentiated pion field and Skyrmions

Discussion of the exponentiated pion field ("chiral field") in [[chiral perturbation theory]] and the interpretation of its [[winding number]] as [[Skyrmion]]-number / [[baryon]]

* {#Witten83a} [[Edward Witten]], _Global aspects of current algebra_, Nuclear Physics B Volume 223, Issue 2, 22 August 1983, Pages 422-432 (<a href="https://doi.org/10.1016/0550-3213(83)90063-9">doi:10.1016/0550-3213(83)90063-9</a>)

* {#Witten83b} [[Edward Witten]], _Current algebra, baryons, and quark confinement_, Nuclear Physics B Volume 223, Issue 2, 22 August 1983, Pages 433-444 (<a href="https://doi.org/10.1016/0550-3213(83)90064-0">doi:10.1016/0550-3213(83)90064-0</a>)

* {#AdkinsNappi84} [[Gregory Adkins]], [[Chiara Nappi]], _Stabilization of Chiral Solitons via Vector Mesons_, Phys. Lett. 137B (1984) 251-256 ([spire:194727](http://inspirehep.net/record/194727), <a href="https://doi.org/10.1016/0370-2693(84)90239-9">doi:10.1016/0370-2693(84)90239-9</a>)

  (beware that the two copies of the text at these two sources differ!)

* {#RhoEtAl16} [[Mannque Rho]] et al., _Introduction_, In: [[Mannque Rho]] et al. (eds.) _[[The Multifaceted Skyrmion]]_, World Scientific 2016 ([doi:10.1142/9710](https://doi.org/10.1142/9710))

### Via holographic QCD

Discussion via the [[AdS/QCD correspondence]]:

* Domenec Espriu, Alisa Katanaeva, _Effects of bulk symmetry breaking on AdS/QCD predictions_ ([arXiv:2001.08723](https://arxiv.org/abs/2001.08723))


[[!redirects pions]]

[[!redirects pi meson]]
[[!redirects pi mesons]]
[[!redirects pi-meson]]
[[!redirects pi-mesons]]

[[!redirects pion field]]
[[!redirects pion fields]]

[[!redirects chiral field]]
[[!redirects chiral fields]]

[[!redirects exponentiated pion field]]
[[!redirects exponentiated pion fields]]

[[!redirects π meson]]
[[!redirects π mesons]]
[[!redirects π-meson]]
[[!redirects π-mesons]]



