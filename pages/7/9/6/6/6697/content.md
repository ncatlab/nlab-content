
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Riemannian geometry
+-- {: .hide}
[[!include Riemannian geometry - contents]]
=--
#### Gravity
+-- {: .hide}
[[!include gravity contents]]
=--
=--
=--



#Contents#
* table of contents
{: toc}

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AdSSlicingByHyperbolic.jpg" width="400">
</div>


## Definition

Up to [[isometry]], the **anti de Sitter spacetime** of [[dimension]] $d$, $AdS_d$, is the [[pseudo-Riemannian manifold]] whose underlying [[manifold]] is the [[submanifold]] of $\mathbb{R}^{d-1,2}$ that solves the equation

$$
  \textstyle{\sum_{i = 1}^{d-1}} 
  (x_i)^2 - (x_d)^ 2 - (x_0)^2 
  \;=\; 
  - R^2
  \,,
$$

for some $R \neq 0$ (the "radius" of the spacetime) and equipped with the [[metric tensor]] induced from the ambient metric, where $\{x^0, x^1, x^2, \cdots, x^d\}$ denote the canonical [[coordinates]]. $AdS_d$ is [[homeomorphic]] to $\mathbb{R}^{d-1} \times S^1$, and its isometry group is $O(d-1, 2)$.

More generally, one may define the anti de Sitter space of signature $(p,q)$ as isometrically embedded in the space $\mathbb{R}^{p,q+1}$ with coordinates $(x_1, ..., x_p, t_1, \ldots, t_{q+1})$ as the sphere $\sum_{i=1}^p x_i^2 - \sum_{j=1}^{q+1} t_j^2 = -R^2$.

> graphics grabbed from [Yan 19](holographic+entanglement+entropy#Yan19)

## Properties


### Coordinate charts
 {#CoordinateCharts}

A comprehesive account of the AdS [[metric tensor]] in various [[coordinate charts]] is given in [Blau §39.3](#Blau).

\linebreak

**Poincaré and horospheric coordinates** (e.g. [Blau §39.3.7](#Blau)).
Consider the [[Cartesian space]] $\mathbb{R}^{1+p}$ with its canonical [[coordinate functions]]
$$
  X^a 
   \;\colon\; 
  \mathbb{R}^{1+p} 
    \xrightarrow{\phantom{-}}  
  \mathbb{R}
  \,,
  \;\;\;
  a \in \{0,1,\cdots, p\}
$$
and denote its standard [[Minkowski spacetime|Minkowski]] [[metric tensor]] by
$$
  d s^2_{\mathbb{R}^{1,p}}
  \;\coloneqq\;
  \textstyle{\sum_{a = 0}^p}
  \mathrm{d}X^a \otimes \mathrm{d}X^a
  \,.
$$
Moreover consider $\mathbb{R}^{1+p} \times \mathbb{R}_{\gt 0}$ equipped with the pullback of the above coordinate function as well as with
$$
  r
  \;\colon\;
  \mathbb{R}^{1+p} \times \mathbb{R}_{\gt 0}
  \twoheadrightarrow
  \mathbb{R}_{\gt 0}
  \hookrightarrow
  \mathbb{R}
  \,.
$$


Then there is a chart of $AdS_{p+2}$ of the form
$$
  \iota
  \;\colon\;
  \mathbb{R}^{1+p} \times \mathbb{R}_{\gt 0}
  \xhookrightarrow{\phantom{--}}
  AdS_{p+2}
$$
such that the pullback of the AdS metric tensor is
\[
  \label{MetricInPoincareCoordinatesI}
  \iota^\ast \mathrm{d}s^2_{AdS}
  \;=\;
  \tfrac{r^2}{R^2}
  \mathrm{d}s^2_{\mathbb{R}^{1,d}}
  \,+\,
  \tfrac{R^2}{r^2} 
  \mathrm{d}r^2
  \,.
\]

This is the form of the AdS-metric which arises naturally as the [[near horizon geometry]] of [[black branes|black]] [[p-branes]] in [[supergravity]] (e.g. [AFFHS98 (5)](near-horizon+geometry#AFFHS98)). The black brane [[singularity]] itself would be at $r = 0$.

In slight variation, in terms of
$$
  z \,\coloneqq\, 1/r
  \,,
  \;\;\;
  \text{hence}
  \;\;\;
  r = z^{-1}
  \,,
  \;\;
  \mathrm{d}r 
    \;=\; 
  -\tfrac{1}{z^2} 
    \mathrm{dz} \;\;
$$
the metric (eq:MetricInPoincareCoordinatesI) becomes
\[
  \label{MetricInPoincareCoordinatesII}
  \iota^\ast \mathrm{d}s^2_{AdS}
  \;=\;
  \frac{R^2}{z^2}
  \big(
    \tfrac{1}{R^4}
    \mathrm{d}s^2_{\mathbb{R}^{1,d}}
    \,+\,
    \mathrm{d}z^2
  \big)
  \,.
\]

cf. e.g. [Bayona & Braga 2007 (11)](conformal+boudnary#BayonaBraga07).
(These are called *horospheric coordinates* by [Gibbons 2000 (12)](#Gibbons00).)

On the other hand, in terms of
$$
  \rho \;\coloneqq\; ln r
  \,,
  \;\; \text{hence} \;\;
  r = e^\rho
  \,,
  \;\;
  \mathrm{d}r = r \, \mathrm{d}\rho
$$
the metric (eq:MetricInPoincareCoordinatesI) becomes
\[
  \label{MetricInPoincareCoordinatesIII}
  \iota^\ast \mathrm{d}s^2_{AdS}
  \;=\;
  \tfrac{e^{2\rho}}{R^2}
  \mathrm{d}s^2_{\mathbb{R}^{1,d}}
  \,+\,
  R^2
  \mathrm{d}\rho^2
  \,.
\]
This is called *horospheric coordinates* in [arXiv:1412.2054 (37)](https://arxiv.org/abs/1412.2054).


\linebreak

### Cartan geometry
 {#CartanGeometry}

We spell out the [[curvature]] tensors of anti de Sitter spacetime, using a [[Cartan connection]] (i.e. [[first order formulation of gravity|first order formulation]]).

An evident choice of an orthonormal [[coframe field]] for the AdS metric in Poincaré coordinates (eq:MetricInPoincareCoordinatesI) is
$$
  \begin{array}{ccll}
    E^a &\coloneqq& \tfrac{r}{R} \mathrm{d}X^a  
    & a \in \{0,1, \cdots, d\}
    \\
    E^{p'} &\coloneqq& \tfrac{R}{r} \mathrm{d}r
  \end{array}
$$
in that 
$$
  \iota^\ast \mathrm{d}s^2_{AdS_{p+2}}
  \;=\;
  \eta_{a b} E^a \otimes E^b
  +
  E^{p'} \otimes E^{p'}
  \,.
$$

> (no sum over $p'$ -- this is meant to be the index *value* corresponding to the radial direction)

The [[torsion of a Cartan connection|torsion]]-free [[spin connection]] $\Omega$ for this [[coframe field]], characterized by
\[
  \label{SpinConnection}
  \begin{array}{ccl}
    \mathrm{d}E^a &=& \Omega^a{}_b \, E^b
    \\
    \mathrm{d}E^{p'} &=& \Omega^{p'}{}_b \, E^b 
    \mathrlap{\,,}
  \end{array}
\]
has non-vanishing components
$$
  \Omega^{a p'} \,=\, - \Omega^{p' a}
  \;=\;
  - \tfrac{r}{R^2} \mathrm{d}X^a
  \,.
$$

The corresponding [[curvature]] [[differential 2-form|2-form]]
$$
  \begin{array}{l}
    R^{a_1 a_2}
    \;=\;
    -
    \Omega^{a_1}{}_{p'} \Omega^{p' a_2}
    \\
    R^{a d'}
    \;\coloneqq\;
    \mathrm{d}\Omega^{a p'}
  \end{array}
$$
has non-vanishing components
$$
  \begin{array}{l}
    R^{a_1 a_2}
    \;=\;
    - \tfrac{r^2}{R^4} \mathrm{d}X^{a_1}\, \mathrm{d}X^{a_2}
    \;=\;
    - \tfrac{1}{R^2} E^{a_1} \, E^{a_2}
    \\
    R^{a p'} \,=\, - R^{p' a} 
    \;=\;
    - \tfrac{1}{R^2} \mathrm{d}X^a 
    \;=\; 
    - \tfrac{1}{R^2} E^a \, E^{p'}
    \,.
  \end{array}
$$
Hence the [[Riemann tensor]] has non-vanishing components
$$
  \begin{array}{ccl}
    R^{a_1 a_2}{}_{b_1 b_2}
    &=&
    + \tfrac{1}{R^2} \delta^{a_1 a_2}_{b_1 b_2}
    \\
    R^{a p'}{}_{b p'}
    &=&
    + \tfrac{1}{R^2} \delta^a{}_b 
    \mathrlap{\,,}
  \end{array}
$$
so that the [[Ricci tensor]] is proportional to the metric,
as befits an [[Einstein manifold]]:
$$
  \begin{array}{ccl}
    Ric_{a_1 a_2}
    &\coloneqq&
    R_{a_1}{}^{b}{}_{a_2 b}
    \,+\,
    R_{a_1}{}^{p'}{}_{a_2 p'}
    \;=\;
    \tfrac{p}{R^2} \, \eta_{a_1 a_2}
    + 
    \tfrac{1}{R^2} \, \eta_{a_1 a_2}
    \\
    &=& \tfrac{p+1}{R^2} \, \eta_{a_1 a_2}
    \\
    Ric_{p' p'} 
    &\coloneqq&
    R_{p'}{}^b{}_{p' b}
    \\
    &=&
    \tfrac{p+1}{R^2}
    \,.
  \end{array}
$$

> The above convention $\mathrm{d}E^a = + \Omega^a{}_b \, E^b$ (eq:SpinConnection) makes this come out positive, following the old convention by [Freund & Rubin 1980](Freund-Rubin+compactification#FreundRubin80), see [there](Freund-Rubin+compactification#TheGeneralFreundRubinSolution).


\linebreak


### Conformal boundary

(...) *[[conformal boundary]]* (...) &lbrack;e.g. [Frances 2011](#Frances11)&rbrack;


### Holography

Asymptotically anti-de Sitter spaces play a central role in the realization of the [[holographic principle]] by [[AdS/CFT correspondence]].

### In $p$-adic geometry

A [[p-adic geometry|2-adic]] [[arithmetic geometry]]-version of [[AdS spacetime]] is identified with the [[Bruhat-Tits tree]] for the [[projective general linear group]] $PGL(2,\mathbb{Q}_p)$:

<center>
  <img src="https://ncatlab.org/nlab/files/BruhatTitsTreeOfSL2.jpg" width="600">
</center>

> graphics from [Casselman 14](Bruhat-Tits+tree#Casselman14)

In the [[p-adic AdS/CFT correspondence]] this may be regarded (at some finite depth truncation) as a [[tensor network state]]: 

<center>
<img src="https://ncatlab.org/nlab/files/BruhatTitsTreeTensorNetworkStateFromMetricLie.jpg" width="300">
</center>

> graphics from [[schreiber:Differential Cohomotopy implies intersecting brane observables|Sati-Schreiber 19c]]

and as such validates the [[Ryu-Takayanagi formula]] for [[holographic entanglement entropy]].

## Related concepts

* [[thermal AdS3]]

* [[anti de Sitter group]]

* [[de Sitter spacetime]]

* [[super anti de Sitter spacetime]]

* [[near-horizon geometry]]

* [[singleton representation]]

* [[AdS/CFT correspondence]], [[AdS/QCD correspondence]]


## References

### Geometry

Review:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], volume 1, chapter I.3.8 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), toc: [[CDF91-TOC.pdf:file]], ch I.3: [[CastellaniDAuriaFre-ChI3.pdf:file]],&rbrack;

* [[Ingemar Bengtsson]], _Anti-de Sitter space_, lecture notes (1998) &lbrack;[[Bengtsson98.pdf:file]]&rbrack;

* {#Blau} [[Matthias Blau]], chapter 39 of: _Lecture notes on general relativity_ &lbrack;[web](http://www.blau.itp.unibe.ch/GRLecturenotes.html)&rbrack;

* {#Gibbons00} [[Gary Gibbons]], *Anti-de-Sitter spacetime and its uses*, in: *Mathematical and Quantum Aspects of Relativity and Cosmology*, Lecture Notes in Physics **537**, Springer (2000)  &lbrack;[arXiv:1110.1206](http://arxiv.org/abs/1110.1206), [doi:10.1007/3-540-46671-1_5](https://doi.org/10.1007/3-540-46671-1_5)&rbrack;

* {#Frances11} [[Charles Frances]], *The conformal boundary of anti-de Sitter space-times*, in: *AdS/CFTCorrespondence: Einstein Metrics and Their Conformal Boundaries*, IRMA Lectures in Mathematical and Theoretical Physics, EMS (2011) 205-216 &lbrack;[ems:irma/9/206](https://ems.press/books/irma/9/206), [hal:03195056](https://hal.science/hal-03195056), [pdf](https://hal.science/hal-03195056v1/document)&rbrack;

* {#Natsuume15} [[Makoto Natsuume]], section 6 of: _AdS/CFT Duality User Guide_, Lecture Notes in Physics **903** Springer (2015) &lbrack;[arXiv:1409.3575](https://arxiv.org/abs/1409.3575), [doi:10.1007/978-4-431-55441-7](https://doi.org/10.1007/978-4-431-55441-7)&rbrack;

* Leszek M. Sokolowski, _The bizarre anti-de Sitter spacetime_, International Journal of Geometric Methods in Modern Physics **13** 9 (2016) 1630016 &lbrack;[arXiv:1611.01118](https://arxiv.org/abs/1611.01118)&rbrack;

* Ricard M. Calvo, *Geometry of (Anti-)De Sitter space-time* (2018) &lbrack;[pdf](https://diposit.ub.edu/dspace/bitstream/2445/125099/1/Monge%20Calvo%20Ricard.pdf), [[Calvo-AdS.pdf:file]]&rbrack;

See also:

* Wikipedia, _[anti de Sitter space](http://en.wikipedia.org/wiki/Anti_de_Sitter_space)_

With attention to the [[conformal geometry]]:

* [[Juan A. Valiente Kroon]]: chapter 17 of: *Conformal Methods in General Relativity*, Cambridge University Press (2017, 2022) &lbrack;[doi:10.1017/9781009291309](https://doi.org/10.1017/9781009291309), [oapen:20.500.12657/59217](https://library.oapen.org/handle/20.500.12657/59217), [pdf](https://library.oapen.org/bitstream/id/548cfabe-a25b-4562-b95e-aa2894525f32/9781009291309.pdf)&rbrack;


Further discussion:

* Abdelghani Zeghib, _On closed anti de Sitter spacetimes_, Math. Ann. 310, 695&#8211;716 (1998) ([pdf](http://www.umpa.ens-lyon.fr/~zeghib/Anti.de.Sitter.pdf))


* Jiri Podolsky, Ondrej Hruska, _Yet another family of diagonal metrics for de Sitter and anti-de Sitter spacetimes_, Phys. Rev. D 95, 124052 (2017) ([arXiv:1703.01367](https://arxiv.org/abs/1703.01367))

### Quantum field theory
 {#ReferencedQuantumFieldTheory}

Discussion of ([[scalar field|scalar]]) [[quantum field theory]] [[quantum field theory on curved spacetimes|on AdS backgrounds]]:

* S. J. Avis, [[Chris J. Isham]], D. Storey: *Quantum field theory in anti-de Sitter space-time*, Phys. Rev. D **18** 3565 (1978) &lbrack;[doi:10.1103/PhysRevD.18.3565](https://doi.org/10.1103/PhysRevD.18.3565)&rbrack;

* Peter Breitenlohner, [[Daniel Z. Freedman]], *Positive energy in anti-de Sitter backgrounds and gauged extended supergravity*, Physics Letters B **115** 3 (1982) 197-201 &lbrack;<a href="https://doi.org/10.1016/0370-2693(82)90643-8">doi:10.1016/0370-2693(82)90643-8</a>&rbrack;

Discussion of thermal [[Wick rotation]] on global [[anti-de Sitter spacetime]]  (which is already periodic in _real_ time) to [[Euclidean field theory]] with periodic _imaginary_ time is in

* {#AllenFolacciGibbons87} B. Allen, A. Folacci, [[Gary Gibbons]], _Anti-de Sitter space at finite temperature_, Physics Letters B Volume 189, Issue 3, 7 May 1987, Pages 304-310 (<a href="https://doi.org/10.1016/0370-2693(87)91437-7">doi:10.1016/0370-2693(87)91437-7</a>)

Discussion of [[black holes in anti de Sitter spacetime]]:

* Hawking, Stephen W., and Don N. Page. "Thermodynamics of black holes in anti-de Sitter space." Communications in Mathematical Physics 87.4 (1983): 577-588.

* {#Socolovsky17} M. Socolovsky, _Schwarzschild Black Hole in Anti-De Sitter Space_ ([arXiv:1711.02744](https://arxiv.org/abs/1711.02744))

* Peng Zhao, _Black Holes in Anti-de Sitter Spacetime_ ([pdf](https://pdfs.semanticscholar.org/9939/335e0d282e70201d6087988bf4f5aedfc8f6.pdf))

* Jakob Gath, _The role of black holes in the AdS/CFT correspondence_ ([pdf](https://www.imperial.ac.uk/media/imperial-college/research-centres-and-groups/theoretical-physics/msc/dissertations/2009/Jakob-Gath-Dissertation-2009.pdf))

Relation to [[Teichmüller theory]]:

* Francesco Bonsante, Andrea Seppi, _Anti-de Sitter geometry and Teichmüller theory_ ([arXiv:2004.14414](https://arxiv.org/abs/2004.14414))

### Phenomenology

* {#SenAdilSen21} Anjan A. Sen, Shahnawaz A. Adil, Somasri Sen, *Do cosmological observations allow a negative $\Lambda$?* ([arXiv:2112.10641](https://arxiv.org/abs/2112.10641))



### As string vacua

On (in-)stability of non-[[supersymmetry|supersymmetric]] [[AdS spacetime|AdS]] [[string theory vacua|vacua in string theory]]:

* [[Iosif Bena]], [[Krzysztof Pilch]], [[Nicholas Warner]], _Brane-Jet Instabilities_,  J. High Energ. Phys. 2020, 91 (2020) ([arXiv:2003.02851](https://arxiv.org/abs/2003.02851))



[[!include pp-waves as Penrose limits of AdS spacetimes -- references]]

[[!redirects anti de Sitter space]]
[[!redirects anti de Sitter spaces]]
[[!redirects anti-de Sitter space]]
[[!redirects anti-de Sitter spaces]]
[[!redirects anti de Sitter spacetime]]
[[!redirects anti de Sitter spacetimes]]
[[!redirects anti-de Sitter spacetime]]
[[!redirects anti-de Sitter spacetimes]]

[[!redirects anti de-Sitter spacetime]]

[[!redirects AdS-spacetime]]
[[!redirects AdS-spacetimes]]

[[!redirects horospheric coordinates]]
[[!redirects horospheric coordinate chart]]
[[!redirects horospheric coordinate charts]]

[[!redirects AdS spacetime]]
[[!redirects AdS spacetimes]]

[[!redirects AdS]]
