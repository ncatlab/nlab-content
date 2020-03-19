

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

In [[nuclear physics]], specifically in the [[chiral perturbation theory]] of [[quantum chromodynamics]], the _pion_ or _pi-meson_ ($\pi$-meson) is the [[isospin]]-triplet scalar-[[meson]] [[field (physics)|field]] in the first-[[generation of fermions]], i.e. a [[bound state]] of an [[up quark]] and a [[down quark]]:

[[!include flavors of fundamental particles -- table]]

\linebreak

## Details

### As the Goldstone boson of chiral symmetry breaking

From the point of view of the [[quark]]-[[model (in theoretical physics)|model]] of [[nuclear physics]], the pion is the [[Goldstone boson]] corresponding to the [[spontaneous symmetry breaking]] of the "[[chiral symmetry|chiral]]"-[[symmetry group]] $SU(2)_R \times SU(2)_L$ to the [[diagonal]] [[subgroup]] $SU(2)_V$, by the [[vacuum expectation value]] $\langle q \bar q\rangle \neq 0$ of the [[quark]]-[[condensate]].
 
(e.g. [Machleidt-Entem 11, 2.1.3](#MachleidtEntem11))

### Plain pion field

Hence, in the sense of the [[Wigner classification]], the pion field transforms in the trivial representation of the [[Lorentz group]] (is a spacetime scalar) and in the [[adjoint representation]] of the [[isospin]] [[group]] [[SU(2)]]

\begin{imagefromfile}
    "file_name": "FirstGenerationMesonFields.jpg",
    "width": 500,
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

Explicitly, the "topological"-part $B_{top}$ of the [[baryon]] [[current]] (the piece that is not generally [[conserved current|conserved]], reflecting the [[chiral anomaly]]), is the [[Wess-Zumino-Witten term]] ([Witten 83b](#Witten83a), [Witten 83b](#Witten83b)):

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

Introduction:

* {#MachleidtEntem11} R. Machleidt, D. R. Entem, _Chiral effective field theory and nuclear forces_, Phys. Rept. 503:1-75, 2011 ([arXiv:1105.2919](https://arxiv.org/abs/1105.2919))

See also

* Wikipedia, _[Pion](https://en.wikipedia.org/wiki/Pion)_

### Exponentiated pion field and Skyrmions

Discussion of the exponentiated pion field ("chiral field") and the interpretation of its [[winding number]] as [[Skyrmion]]-number / [[baryon]]

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



