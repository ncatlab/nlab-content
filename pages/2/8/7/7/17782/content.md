
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Gravity
+--{: .hide}
[[!include gravity contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _pp-wave spacetime_ (for *parallel [[plane waves]]*) is a [[spacetime]], i.e. an exact solution to [[Einstein's equations]] for [[gravity]], containing nothing but [[radiation]] ([[gravitational waves]] and/or [[electromagnetic waves]]) with one fixed [[wave vector]].

The [[Ricci flat]] pp-wave spacetimes are examples of [[universal spacetimes]].

## Properties

### As Penrose limits
 {#AsPenroseLimits}

Every [[spacetime]] looks like a pp-wave near a [[lightlike]] [[geodesic]]. This is due to [Penrose 1976](#Penrose76) and hence came to be called the _Penrose limit_ (review includes [Blau 11](#Blau11)).

Notice that Penrose limits of [[Einstein manifolds]] are [[Ricci flat]] ([Philip 2005, Prop. 3.4.1](#Philip05), [Philip 2006, Prop. 3](#Philip06), review in [Blau 2011](#Blau11), [p. 41](https://ncatlab.org/nlab/files/BlauPlaneWavesAndPenroseLimit.pdf#page=41)).

{#MaximallySupersymmetric11dExample} For example, the Penrose limits of both the [[black brane|black]] [[M2-brane]] solution $AdS_4 \times S^7$ as well as the [[black brane|black]] [[M5-brane]] solution $AdS_7 \times S^4$ of [[D=11 supergravity]] are &lbrack;[BFHP 2002](#BlauFigueroaHullPapadopoulos02), [BMN 2002, §2](#BerensteinMaldacenaNastase02)&rbrack; the (same) pp-maximally supersymmetric pp-wave spacetime originally found by [Kowalski-Glikman 1984 (0)](#Kowalski-Glikman84), [Figueroa & Papadopoulos 2001 (12,14)](#FigueroaPapadopoulos01):

### Examples

\begin{example}\label{MaximallySuSyWaveIn11D}
**(maximally supersymmetric pp-wave in 11d SuGra)**
\linebreak
The maximally supersymmetric pp-wave solution of [[D=11 supergravity]] &lbrack;[Kowalski-Glikman 1984 (0)](#Kowalski-Glikman84), [Figueroa & Papadopoulos 2001 (12,14)](#FigueroaPapadopoulos01)&rbrack; has [[metric tensor]] of the form
\[
  \label{MetricTensorOfMaximalSuSyWaveIn11d}
  \begin{array}{lcl}
  \mathrm{d}s^2
  &\equiv&
  2
  \, 
  \mathrm{d}x^- \otimes \mathrm{d}x^+ 
  \,-\,
  \big(
    (\mu/3)^2 x^i x_i
    +
    (\mu/6)^2 x^j x_j
  \big)
  \,
  \mathrm{d}x^- \otimes \mathrm{d}x^-
  \\
  &&
  \,+\,
  \mathrm{d}x^i \otimes \mathrm{d}x_i
  \,+\,
  \mathrm{d}x^j \otimes \mathrm{d}x_j
  \,,
  \end{array}
  \;\;
  \text{where}
  \;\;
  \begin{array}{l}
    i \,\in\, \{1,2,3\}
    \\
    j \,\in\, \{4,5,6,7,8,9\}
    \mathrlap{\,,}
  \end{array}
\]
supported by a [[supergravity C-field|C-field]] [[flux density]] of the form
\[
  \label{CFieldFLuxDensityForMaximalSuSyWaveIn11d}
  F
  \;=\;
  \mu 
  \;
  \mathrm{d}x^- 
  \, \mathrm{d}x^1 \, \mathrm{d}x^2 \, \mathrm{d}x^3
  \,,
\]
for given parameter $\mu \in \mathbb{R}$.

Consider on the [[vector space]] $\mathbb{R}^{1,10}$ with its canonical [[linear basis]] $(x^a)_{a=0}^{10}$ the [[light cone gauge]] basis

$$
  \begin{array}{lcl}
    x^- 
      &\coloneqq& 
    (-x^0 + x^1)/\sqrt{2}
    \\
    x^+ 
      &\coloneqq& 
    \phantom{+}(x^0 + x^1)/\sqrt{2}
    \\
    x^i 
      &\coloneqq& 
    \phantom{+}x^a \;\text{for}\; a = i \in \{1,2,3\}
    \\
    x^j 
      &\coloneqq& 
    \phantom{+}x^a \;\text{for}\; a = j \in \{4,5,6,7,8,9\}
  \end{array}
$$

in terms of which the [[Minkowski metric]] $\eta_{a b} \coloneqq \mathrm{diag}\big(-1,+1, +1, \cdots, +1\big)_{a b}$ has components

$$
  \begin{array}{lcl}
    \eta_{+ +} \,=\, \eta_{- -}
    &=&
    0
    \\
    \eta_{- +} \,=\, \eta_{+ -}
    &\coloneqq&
    1
    \\  
    \eta_{i_1 i_2} &\coloneqq& diag(1,1,1)_{i_1 i_2}
    \\
    \eta_{j_1 j_2} &\coloneqq& diag(1,1,1,1,1,1)_{j_1 j_2}
    \,.
  \end{array}
$$

Then a choice of orthonormal [[coframe field]] for (eq:MetricTensorOfMaximalSuSyWaveIn11d) is (cf. [Bandos 2012 (3.4)](#Bandos12))

$$
  \begin{array}{lcl}
    e^+ 
    &\coloneqq&
    \mathrm{d}x^+ 
    \,-\,
    \tfrac{1}{2}
    \big(
      (\mu/3)^2 \, x^i x_i
      \,+\,
      (\mu/6)^2 \, x^j x_j
    \big)
    \,
    \mathrm{d}x^-
    \\
    e^-
    &\coloneqq&
    \mathrm{d}x^-
    \\
    e^i &\coloneqq& \mathrm{d}x^i
    \\
    e^j &\coloneqq& \mathrm{d}x^j
  \end{array}
$$
in that
$$
  \mathrm{d}s^2
  \;=\;
  2 \, e^- \otimes e^+
  \,+\,
  e^1 \otimes e^1 
  \,+\,
  e^2 \otimes e^2
  \,+\,
  \cdots
  \,+\,
  e^{9} \otimes e^9
  \,.
$$

From this one finds that the [[torsion of a Cartan connection|torsion]]-free [[spin connection]] $\omega$ for this co-frame field, characterized by
$$
  \mathrm{d} e^a - \omega^a{}_b \cdot e^b 
  \;=\;
  0
  \,,
$$
has as only non-vanishing components (cf. [Bandos 2012 (3.5)](#Bandos12)):
$$
  \begin{array}{l}
    \omega^{+ i} \;=\; - \omega^{i +}
    \;=\;
    (\mu/3)^2 \, x^i \, e^+
    \\
    \omega^{+ j} \;=\; - \omega^{j +}
    \;=\;
    (\mu/6)^2 \, x^j \, e^+
    \,,
  \end{array}
$$
with which
$$
  \begin{array}{ccl}
  \mathrm{d}e^+
  &=&
  \,-\,
  (\mu/3)^2 x_i \, \mathrm{d}x^i \otimes e^-
  \,-\,
  (\mu/6)^2 x_j \, \mathrm{d}x^j \otimes e^-
  \\
  &=&
  \;\;\;\;\;\;\;\;\;\;\;\;
  \omega^+{}_{i} \, \mathrm{e}^i 
  \;\;\;\;\;\;\;\;\;\;\;\;\;\;\;
  \,+\,
  \omega^+{}_{j} \, \mathrm{e}^j
  \,.
  \end{array}
$$
From this, the only non-vanishing contribution in  

* the [[curvature 2-form]] $R^{a b} \,\equiv\, \mathrm{d}\omega^{a b} - \omega^a{}_c \omega^{c b}$ is (cf. [Bandos 2012 (3.6)](#Bandos12)):
  $$
    \begin{array}{l}
      R^{+ i}
      \,=\,
      - R^{i +}
      \;=\;
      \mathrm{d} \omega^{+ i}
      \;=\;
      (\mu/3)^2 \, e^i \, e^-
      \\
      R^{+ j}
      \,=\,
      -
      R^{j +}
      \;=\;
      \mathrm{d} \omega^{+ j}
      \;=\;
      (\mu/6)^2 \, e^j \, e^-
      \,.
    \end{array}
  $$

* the [[Riemann tensor]] ($R^{a b} = \tfrac{1}{2}R^{a b}{}_{c_1 c_2} e^{c_1} e^{c_2}$) is (cf. [Bandos 2012 (3.7)](#Bandos12)):
  $$
    \begin{array}{l}
      R^{+ i_1}\,{}_{i_2 -}
      \;=\;
      \delta^{i_1}_{i_2} (\mu/3)^2 
      \\
      R^{+ j_1}\,{}_{j_2 -}
      \;=\;
      \delta^{j_1}_{j_2} (\mu/6)^2 
      \,.
    \end{array}
  $$

* the [[Ricci tensor]] $R_{a b} \coloneqq \eta_{a a'} R^{a' c}{}_{b c}$ is

  \[
    \label{RicciTensorOfMaximalSuSyWaveIn11d}
    Ric_{- -}
    \;=\;
    -\mu^2/3
    -\mu^2/6
    \,=\,
    -\tfrac{1}{2}\mu^2
    \,.
  \]

* the [[scalar curvature]] $\mathrm{R} \equiv \eta^{a b}Ric_{a b}$ is

  $$
    \mathrm{R} \;=\; 0
    \,,
  $$

* the [[Einstein tensor]] $G_{a b} = Ric_{a b} - \tfrac{1}{2} \mathrm{R} \eta_{a b}$ is again

  \[
    \label{EinsteinTensorOfMaximalSuSyWaveIn11d}
    G_{- -}
    \;=\;
    -\mu^2/3
    -\mu^2/6
    \,=\,
    -\tfrac{1}{2}\mu^2
    \,.
  \]


On the other hand, the non-vanishing contribution in the [[energy momentum tensor]] 
$$
  T_{\mu \nu}
  \;=\;
  \big(
    \tfrac{1}{8}
    F_{\mu_1 \cdots \mu_s}
    F^{\mu_1 \cdots \mu_s}
    \,
    g_{\mu \nu}
    -
    F_{\mu \, \mu_1 \cdots \mu_{s-1}}
    F_{\nu}{}^{ \mu_1 \cdots \mu_{s-1} }
  \big)
$$
of the [[supergravity C-field|C-field]] (eq:CFieldFLuxDensityForMaximalSuSyWaveIn11d) is
\[
  \begin{array}{lcl}
    T_{- -}
    &=&
    -
    \mu^2
    \epsilon_{i_1 i_2 i_3}
    \,
    \epsilon^{i_1 i_2 i_3}
    \\
    &=&
    -
    6
    \mu^2
    \,.
  \end{array}
\]

This shows that the [[Einstein equation]] $G_{a b} = T_{a b}$ is satisfied 

> (up to a conventional rescaling of $F$...)

\end{example}

\linebreak

### Relation to BMN matrix model

The _[[BMN matrix model]]_ ([BMN 02, Section 5 and Appendix B](#BerensteinMaldacenaNastase02)) is a deformation of the [[BFSS matrix model]] by [[mass]]-terms which correspond to a deformation of the [[Minkowski spacetime]] background to a [[pp-wave spacetime]]. 


## Examples

* [[M-wave]]

## Related concepts

* [[flat space holography]]


## References

### General

Introducing what came to be known as the *Penrose limit* for producing pp-wave spacetimes:

* {#Penrose76} [[Roger Penrose]], *Any Space-Time has a Plane Wave as a Limit*, in *Differential Geometry and Relativity*, Mathematical Physics and Applied Mathematics **3**, Springer (1976) 271–275 &lbrack;[doi:10.1007/978-94-010-1508-0_23](https://doi.org/10.1007/978-94-010-1508-0_23), [pdf](https://link.springer.com/content/pdf/10.1007/978-94-010-1508-0_23.pdf)&rbrack;

Lecture notes

* {#Blau11} [[Matthias Blau]], _Plane waves and Penrose limits_ (2011) &lbrack;[pdf](http://www.blau.itp.unibe.ch/lecturesPP.pdf), [[BlauPlaneWavesAndPenroseLimit.pdf:file]]&rbrack;

See also:

* Wikipedia, _[pp-wave spacetime](https://en.wikipedia.org/wiki/Pp-wave_spacetime)_

Detailed mathematical discussion:

* [[José Figueroa-O'Farrill]], [[Patrick Meessen]], [[Simon Philip]], *Homogeneity and plane-wave limits*,  Journal of High Energy Physics **2005** JHEP05 (2005) &lbrack;[arXiv:hep-th/0504069](https://arxiv.org/abs/hep-th/0504069), [doi:10.1088/1126-6708/2005/05/050](https://doi.org/10.1088/1126-6708/2005/05/050)&rbrack;

* {#Philip05} [[Simon Philip]], *Plane-wave limits and homogeneous M-theory backgrounds*, PhD thesis, Edinburgh (2005) &lbrack;[pdf](https://www.era.lib.ed.ac.uk/bitstream/handle/1842/15645/Philip2005.Pdf?sequence=1), [[PhilipPlaneWave05.pdf:file]]&rbrack;

* {#Philip06} [[Simon Philip]], *Penrose limits of homogeneous spaces*, Journal of Geometry and Physics **56** 9 (2006) 1516-1533 &lbrack;[doi:10.1016/j.geomphys.2005.08.002](https://doi.org/10.1016/j.geomphys.2005.08.002), [doi:math/0405506](https://arxiv.org/abs/math/0405506)&rbrack;

### Examples
 {#ReferencesExamples}

The maximally supersymmetric pp-wave solution of [[D=11 supergravity]] is due to:

* {#Kowalski-Glikman84} Jerzy Kowalski-Glikman, *Vacuum states in supersymmetric Kaluza-Klein theory*, Physics Letters B **134** 3–4 (1984) 194-196 &lbrack;<a href="https://doi.org/10.1016/0370-2693(84)90669-5">doi:10.1016/0370-2693(84)90669-5</a>, [InSpire:202143](https://inspirehep.net/literature/202143)&rbrack;

* {#FigueroaPapadopoulos01} [[José Figueroa-O’Farrill]], [[George Papadopoulos]], *Homogeneous fluxes, branes and a maximally supersymmetric solution of M-theory*, JHEP 0108:036 (2001) &lbrack;[arXiv:hep-th/0105308](https://arxiv.org/abs/hep-th/0105308), [doi:10.1088/1126-6708/2001/08/036](https://doi.org/10.1088/1126-6708/2001/08/036)&rbrack;

Its realization as a [[Penrose limit]] of both the [[black brane|black]] [[M2-brane]] solution $AdS_4 \times S^7$ as well as the [[black brane|black]] [[M5-brane]] solution $AdS_7 \times S^4$ is due to 

* {#BlauFigueroaHullPapadopoulos02} [[Matthias Blau]], [[José Figueroa-O’Farrill]], [[Christopher Hull]], [[George Papadopoulos]], *Penrose limits and maximal supersymmetry*, Class. Quant. Grav. **19** (2002) L87-L95 &lbrack;[arXiv:hep-th/0201081](https://arxiv.org/abs/hep-th/0201081), [doi:10.1088/0264-9381/19/10/101](https://doi.org/10.1088/0264-9381/19/10/101)&rbrack;

* [BMN 2002, §2](#BerensteinMaldacenaNastase02)



### pp-Wave Super spacetimes
{#EnhancementToSuperSpacetime} 

On the enhancement of pp-wave spacetimes to [[super spacetimes]]:

* [[Keshav Dasgupta]], [[Mohammad M. Sheikh-Jabbari]], [[Mark Van Raamsdonk]], §2.2 in: *Matrix Perturbation Theory For M-theory On a PP-Wave*,  J. High Energy Physics **2002** JHEP05 (2002) &lbrack;[arXiv:hep-th/0205185](https://arxiv.org/abs/hep-th/0205185), [doi:10.1088/1126-6708/2002/05/056](https://iopscience.iop.org/article/10.1088/1126-6708/2002/05/056)&rbrack;

* {#Bandos12} [[Igor A. Bandos]], p. 7 of: *Multiple M0-brane equations in eleven dimensional pp-wave superspace and BMN matrix model*, Phys. Rev. D **85** 126005 (2012) &lbrack;[arXiv:1202.5501](https://arxiv.org/abs/1202.5501), [doi:10.1103/PhysRevD.85.126005](https://doi.org/10.1103/PhysRevD.85.126005)&rbrack;


[[!include pp-waves as Penrose limits of AdS spacetimes -- references]]


### BMN limit: AdS/CFT in the pp-wave limit
 {#ReferencesBMNLimit}

The [[AdS-CFT|AdS/CFT dual]] to the pp-wave [[Penrose limit]] of [$AdS_5 \times S^5$](AdS-CFT+correspondence#AdS5CFT4)-spacetimes is the *BMN limit* of [[super Yang-Mills theory]] (governed by [[spin chain]]-dynamics), due to:

* {#BerensteinMaldacenaNastase02} [[David Berenstein]], [[Juan Maldacena]], [[Horatiu Nastase]], *Strings in flat space and pp waves from $\mathcal{N}=4$ Super Yang Mills*, JHEP 0204 (2002) 013 &lbrack;[arXiv:hep-th/0202021](https://arxiv.org/abs/hep-th/0202021), [doi:10.1088/1126-6708/2002/04/013](https://doi.org/10.1088/1126-6708/2002/04/013)&rbrack;

Review:

* [[Rodolfo Russo]], Alessandro Tanzini, *The Duality between IIB String Theory on PP-wave and $\mathcal{N}=4$ SYM: a Status Report*, Class. Quant. Grav. **21** (2004) S1265-2196 &lbrack;[arXiv:hep-th/0401155](https://arxiv.org/abs/hep-th/0401155), [doi:10.1088/0264-9381/21/10/001](https://doi.org/10.1088/0264-9381/21/10/001)&rbrack;

* [[Jan Plefka]], *Lectures on the Plane-Wave String/Gauge Theory Duality*, Fortsch. Phys. **52** (2004) 264-301 &lbrack;[arXiv:hep-th/0307101](https://arxiv.org/abs/hep-th/0307101), [doi:10.1002/prop.200310121](https://doi.org/10.1002/prop.200310121)&rbrack;

Further references as of 2010 are listed at:

* [String Theory Wiki](https://www.stringwiki.org/wiki/String_Theory_Wiki), *[The BMN limit](https://www.stringwiki.org/wiki/The_BMN_limit)* (2010)

Review in the context of the [[AdS/CMT correspondence]]:

* [[Horatiu Nastase]], Chapter 28 of: *String Theory Methods for Condensed Matter Physics*, Cambridge University Press (2017) &lbrack;[doi:10.1017/9781316847978](https://doi.org/10.1017/9781316847978), toc: [pdf](https://assets.cambridge.org/97811071/80383/frontmatter/9781107180383_frontmatter.pdf)&rbrack;

Analogous phenomena claimed for pp-wave limits of [$AdS_7 \times S^4/\Gamma_{ADE}$](AdS-CFT+correspondence#AdS7CFT6) and [[spin chains]] in the dual [[D=6 N=(2,0) SCFT]]:

* Florent Baume, [[Jonathan J. Heckman]], Craig Lawrie, *6D SCFTs, 4D SCFTs, Conformal Matter, and Spin Chains*, Nuclear Physics B **967** (2021) 115401 &lbrack;[doi:10.1016/j.nuclphysb.2021.115401](https://doi.org/10.1016/j.nuclphysb.2021.115401), [arXiv:2007.07262](https://arxiv.org/abs/2007.07262)&rbrack;

* [[Jonathan J. Heckman]], *Qubit construction in 6D SCFTs*, Physics Letters B **811** (2020) 135891 &lbrack;[doi:10.1016/j.physletb.2020.135891](https://doi.org/10.1016/j.physletb.2020.135891), [arXiv:2007.08545](https://arxiv.org/abs/2007.08545)&rbrack;



[[!redirects pp-wave spacetimes]]

[[!redirects pp-wave]]
[[!redirects pp-waves]]

[[!redirects PP-wave spacetime]]
[[!redirects PP-wave spacetimes]]

[[!redirects PP-wave]]
[[!redirects PP-waves]]

[[!redirects Penrose limit]]
[[!redirects Penrose limits]]

[[!redirects BMN limit]]
[[!redirects BMN limits]]

