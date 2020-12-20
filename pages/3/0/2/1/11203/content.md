
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

(...)

## Properties

### Magnetic flux quantization in type II superconductors
 {#MagneticFluxQuantizationInTypeIISuperconductors}

Due to the [[Meissner-Ochsenfeld effect]], a superconductor placed in a sufficiently small external [[magnetic field]] $H_{ext} \lt H_{c_1}$ (aligned along some axis) "expels" that field , making the total  magnetic field in the bulk of the superconductor vanish. However, as the ambient magnetic field exceeds a critical value $H_{c_1}$, this behaviour changes:

* for _Type I superconductors_, the superconducting state simply breaks down as $H_{ext} \gt H_{c_1}$ and the ambient magnetic field fully penetrates the material as for any normal conductor;

* for _Type II superconductors_ the superconducting state eventually also breaks down as $H_{ext} \gt H_{c_2} \gt H_{c_1}$, but there is an intermediate parameter region $H_{c_1} \lt H_{ext} \lt H_{c_2}$ where both regimes mix:


\begin{imagefromfile}
    "file_name": "SuperconductorsPhaseDiagram.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Chapman 09](#Chapman00)"
\end{imagefromfile}


In this mixed regime, a _[[finite number]]_ of elementary units of [[magnetic flux]] enter the superconductor, carried by little _flux tubes_ inside _[[vortices]]_ of electric currents (about a [[micron]] in diameter, e.g. [Chapman 00, p. 559](#Chapman00)). Each vortex core carries one unit of magnetic flux -- also called a _fluxon_ --  while at some small finite distance away from all vortices, the bulk magnetic flux in the superconductor still vanishes (mathematically: it [[vanishes at infinity]]):

\begin{imagefromfile}
    "file_name": "SuperconductorVortexStructure.jpg",
    "width": 570,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Loudon-Midgley 09](#LoudonMidgley09)"
\end{imagefromfile}

At sufficiently large density these vortices form hexagonal patterns, first described by  [Abrikosov 57](#Abrikosov57), whence also known as _Abrikosov vortices_.

This flux quantization in type II superconductors is traditionally explained via the [[effective field theory]] provided by the [[Landau-Ginzburg model]]; the derivation may be found reviewed in [Chapman 00 (Section 2, culminating in (2.33))](#Chapman00). 

But, as indicated a little more explicitly in [Alvarez-Gaumé 98 (Section IV.B, culminating below IV.11)](#AlvarezGaume98), the flux quantization as such is mathematically a direct consequence of the global topological nature of the [[electromagnetic field]], the argument being the direct 2-dimensional analog of the quantization of [[instantons in QCD]] in 4d (see also at [SU(2)-Instantons -- From the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)) and in fact is but a slight variation of the argument for [[Dirac charge quantization]] of [[magnetic monopoles]]:

Namely, the [[electromagnetic field]] is a [[connection on a circle bundle]],  and hence the [[Brown representability theorem|cohomology classifying space]] for the topological class of the [[electromagnetic field]] is the [[classifying space]] $B \mathrm{U}(1)$ of the [[circle group]], which, being an [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$, has second [[homotopy group]] the [[integers]]:

$$
  \pi_2(B \mathrm{U}(1)) 
    \;\simeq\; 
  \big\{  S^2 \to B \mathrm{U}(1)\big\}_{\big/hmpty} 
    \;\simeq\; 
  \mathbb{Z}
  \,.
$$

This implies that on every [[spacetime]] which looks, up to [[homotopy equivalence]], like a [[2-sphere]] to the electromagnetic field, the [[magnetic flux]] is identified with an element in the group of [[integers]], hence is _quantized_ in integral multiples of some [[physical unit|unit]] flux.

For the case of a (hypothetical) [[magnetic monopole]] (e.g. a magnetically [[charged black hole]]), it is the [[spacetime]] _around_ the monopole (the [[complement]] of its [[worldline]] $\mathbb{R}^{0,1}$ in the ambient (asymtptotically) [[Minkowski spacetime]] $\mathbb{R}^{3,1}$) which has the [[homotopy type]] of a [[2-sphere]] $\mathbb{R}^{3,1} \setminus \mathbb{R}^{0,1} \,\simeq\, \mathbb{R}^{0,1} \times \mathbb{R}_{rad} \times S^2$; this implies the [[Dirac charge quantization]] of the [[magnetic monopole]]'s [[magnetic charge]]:


\begin{imagefromfile}
    "file_name": "DiracChargeQuantizationViaClassifyingMap.jpg",
    "width": 630,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}


For the case of the type II [[superconductor]] it is instead the transversal [[vanishing at infinity]] of the magnetic field (i.e. the [[Meissner-Ochsenfeld effect]] away from the vortices) which implies that the classifying map of the [[electromagnetic field]] sees not the full transversal [[Euclidean plane]] $\mathbb{R}^2$ but its [[one-point compactification]] $\big( \mathbb{R}^2 \big) \,\simeq\, S^2$, which introduces an effective [[2-sphere]] topology onto spacetime (same as the [[3-sphere]] in the discussion of [[Skyrmions]] and the [[4-sphere]] in the discussion of [[instantons]]): $\mathbb{R}^{1,1} \times \big( \mathbb{R}^2 \big) \,\simeq\, \mathbb{R}^{1,1} \times S^2$. This implies the superconductor's magnetic flux quantization:

\begin{imagefromfile}
    "file_name": "VortexFluxQuantizationViaClassifyingMap.jpg",
    "width": 630,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

The argument that is given in most references, via consideration of the [[period of a differential form|period]] of the [[vector potential]] on a large [[circle]] around the superconductor (e.g. [Timm 20, Section 5.3](#Timm20)), is secretly just the analysis of this picture through the [[clutching construction]] (the direct 2d analog of the discussion at _[SU(2)-Instantons -- From the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_).




## Related concepts

* [[Landau-Ginzburg model]]

* [[AdS/CFT in condensed matter physics]]

* [[colour superconductivity]]


## References

### General


Review

* {#Chapman00} S. J. Chapman, _A Hierarchy of Models for Type-II Superconductors_, IAM Review Vol. 42, No. 4 (2000), pp. 555-598 ([jstor:2653134](https://www.jstor.org/stable/2653134))

* {#Timm20} Carsten Timm, _Theory of Superconductivity_, 2020 ([pdf](https://tu-dresden.de/mn/physik/itp/cmt/ressourcen/dateien/skripte/Skript_Supra.pdf?lang=en))

See also:

* Wikipedia, _[Superconductivity](http://en.wikipedia.org/wiki/Superconductivity)_

* Wikipedia, _[Meissner effect](https://en.wikipedia.org/wiki/Meissner_effect)_

### Vortices and flux quantization

Original articles:

* {#Abrikosov57} A. A. Abrikosov, _The magnetic properties of superconducting alloys_, Journal of Physics and Chemistry of Solids Volume 2, Issue 3, 1957, Pages 199-208 (<a href="https://doi.org/10.1016/0022-3697(57)90083-5">doi:10.1016/0022-3697(57)90083-5</a>)

See also 

* Wikipedia, _[Abrikosov vortex](https://en.wikipedia.org/wiki/Abrikosov_vortex)_

More on the experimental detecttion magnetic flux quantization and vortices:

* {#LoudonMidgley09} J. C. Loudon, P. A. Midgley, _Imaging Flux Vortices in Type II Superconductors with a Commercial Transmission Electron Microscope_, Ultramicroscopy 109: 700-729, 2009 ([arXiv:0807.2401](https://arxiv.org/abs/0807.2401))


More theoretically flavored discussion of the flux quantization mechanism:

* H. B. Nielsen, P. Olesen, _Vortex-line models for dual strings_, Nuclear Physics B Volume 61, 24 September 1973, Pages 45-61 (<a href="https://doi.org/10.1016/0550-3213(73)90350-7">doi:10.1016/0550-3213(73)90350-7</a>)

  > (regarding vortices as [[strings]])

* {#AlvarezGaume98} [[Luis Alvarez-Gaumé]], Frederic Zamora, Section IV.B of: _Duality in Quantum Field Theory (and String Theory)_, AIP Conference Proceedings 423, 46 (1998) ([arXiv:hep-th/9709180](https://arxiv.org/abs/hep-th/9709180))



### Discussion via AdS/CFT


Discussion of [[superconductivity]] via [[AdS/CFT in condensed matter physics]]:

* [[Sean Hartnoll]], [[Christopher Herzog]], [[Gary 
 Horowitz]], _Building an AdS/CFT superconductor_, Phys. Rev. Lett. 101:031601, 2008 ([arXiv:0803.3295](https://arxiv.org/abs/0803.3295))

* Alberto Salvio, _Superconductivity, Superfluidity and Holography_ ([arXiv:1301.0201](http://arxiv.org/abs/1301.0201))

* Rong-Gen Cai, Li Li, Li-Fang Li, Run-Qiu Yang, _Introduction to Holographic Superconductor Models_, Sci China-Phys Mech Astron, 2015, 58(6):060401 ([arXiv:1502.00437](https://arxiv.org/abs/1502.00437))


* {#HartnollLucasSachdev16} [[Sean Hartnoll]], [[Andrew Lucas]], [[Subir Sachdev]], Section 6.3 of: _Holographic quantum matter_, MIT Press 2018 ([arXiv:1612.07324](https://arxiv.org/abs/1612.07324), [publisher](https://mitpress.ublish.com/book/holographic-quantum-matter))


[[!redirects superconductor]]
[[!redirects superconductors]]

[[!redirects Meissner effect]]
[[!redirects Meissner-Ochsenfeld effect]]

