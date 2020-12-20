

### Magnetic flux quantization in type II superconductors
 {#MagneticFluxQuantizationInTypeIISuperconductors}

Due to the [[Meissner-Ochsenfeld effect]], a [[superconductor]] placed in a sufficiently small external [[magnetic field]] $H_{ext} \lt H_{c_1}$ (aligned along some axis) "expels" that field , making the total  magnetic field in the [[bulk]] of the superconductor vanish. However, as the ambient magnetic field exceeds a critical value $H_{c_1}$, this behaviour changes:

* for _[[type I superconductors]]_, the superconducting state simply breaks down as $H_{ext} \gt H_{c_1}$ and the ambient magnetic field fully penetrates the material as for any normal conductor;

* for _[[type II superconductors]]_ the superconducting state eventually also breaks down as $H_{ext} \gt H_{c_2} \gt H_{c_1}$, but there is an intermediate parameter region $H_{c_1} \lt H_{ext} \lt H_{c_2}$ where both regimes mix:


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
    "caption": "From [Chapman 09](superconductivity#Chapman00)"
\end{imagefromfile}


In this mixed regime, a _[[finite number]]_ of elementary units of [[magnetic flux]] enter the superconductor, carried by little _flux tubes_ inside _[[vortices]]_ of electric currents: _[[vortex strings]]_ (about a [[micron]] in diameter, e.g. [Chapman 00, p. 559](superconductivity#Chapman00)). Each vortex core carries one unit of magnetic flux -- also called a _fluxon_ --  while at some small finite distance away from all vortices, the bulk magnetic flux in the superconductor still vanishes (mathematically: it [[vanishes at infinity]]):

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
    "caption": "From [Loudon-Midgley 09](superconductivity#LoudonMidgley09)"
\end{imagefromfile}

At sufficiently large density these vortices form hexagonal patterns, first described by  [Abrikosov 57](superconductivity#Abrikosov57), whence also known as _Abrikosov vortices_.

This flux quantization in type II superconductors is traditionally explained via the [[effective field theory]] provided by the [[Landau-Ginzburg model]]; the derivation may be found reviewed in [Chapman 00 (Section 2, culminating in (2.33))](superconductivity#Chapman00). 

But, as indicated a little more explicitly in [Alvarez-Gaumé 98 (Section IV.B, culminating below IV.11)](superconductivity#AlvarezGaume98), the flux quantization as such is mathematically a direct consequence of the global topological nature of the [[electromagnetic field]], the argument being the direct 2-dimensional analog of the quantization of [[instantons in QCD]] in 4d (see also at [SU(2)-Instantons -- From the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)) and in fact is but a slight variation of the argument for [[Dirac charge quantization]] of [[magnetic monopoles]]:

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


For the case of the type II [[superconductor]] it is instead the transversal [[vanishing at infinity]] of the magnetic field (i.e. the [[Meissner-Ochsenfeld effect]] away from the vortices) which implies that the classifying map of the [[electromagnetic field]] sees not the full transversal [[Euclidean plane]] $\mathbb{R}^2$ but its [[one-point compactification]] $\big( \mathbb{R}^2 \big)^{cpt} \,\simeq\, S^2$, which introduces an effective [[2-sphere]] topology onto spacetime (same as the [[3-sphere]] in the discussion of [[Skyrmions]] and the [[4-sphere]] in the discussion of [[instantons]]): $\mathbb{R}^{1,1} \times \big( \mathbb{R}^2 \big)^{cpt} \,\simeq\, \mathbb{R}^{1,1} \times S^2$. This implies the superconductor's magnetic flux quantization:

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

The argument that is given in most references, via consideration of the [[period of a differential form|period]] of the [[vector potential]] on a large [[circle]] around the superconductor (e.g. [Timm 20, Section 5.3](superconductivity#Timm20)), is secretly just the analysis of this picture through the [[clutching construction]] (the direct 2d analog of the discussion at _[SU(2)-Instantons -- From the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_).
