
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Inspection of the [[equations of motion]] for [[classical field theory|classical]] [[electromagnetism]] ([[Maxwell's equations]]) readily reveals that --- either in [[vacuum]], in a [[dielectric medium]] or in a [[background field]] of [[gravity]] --- they may equivalently be (re)written (in fact this is close to their original historical form) as 

1. a system of purely "topological", "cohomological" or "exterior" [[partial differential equations]]

1. a linear "[[constitutive equation]]" imposing a "duality" relation on the fields,

where it is *only the second but not the first* part that involves the "[[background field|background]]" structure, namely the [[dielectric tensor]] characterizing the ambient [[dielectric medium]] and/or the [[pseudo-Riemannian metric]] characterizing the [[field (physics)|field]] of [[gravity]].

This fact itself is fairly evident (certainly in modern formulations of Maxwell's equations, see [below](#Details)), but some authors have highlighted it as possibly being of deeper relevance, starting with [Kottler (1922a)](#Kottler22a), [(1922b)](#Kottler22b), and [Dantzig (1934)](#Dantzig34) (and apparently also [[Élie Cartan]] in *Sur les variétés à connexion affine...* (1925), but I haven't found the relevant passage yet) and more recently by [Delphenich (2005a)](#Delphenich05a), [(2005b)](#Delphenich05a) (see the comprehensive account [Delphenich (202x)](#DelphenichBook)) who coined the term *pre-metric electromagnetism* for this formulation (the broad idea being that the second step above should be regarded as, indeed, secondary and subject to conceptual re-evaluation)
and has attached high hopes with it [Delphenich (2015)](#Delphenich15).

We point out [below](#RRFieldInGravitationalBackground) that, while the explicit perspective of "pre-metric electromagnetism" is maybe not widely appreciated, in fact exactly the same idea -- just with the [[electromagnetic field]] replaced by the (hypothetical) "[[RR-field]]" --  is secretly at the heart of the the widely recognized [[conjecture]] of [[K-theory classification of D-brane charge]] as well as of related conjectures, such as *[[schreiber:Hypothesis H]]*.


## Premetric electromagentism
 {#Details}

### Electromagnetism in gravitational backgrounds

The [[equations of motion]] of [[classical field theory|classical]] [[electromagnetism]] ([[Maxwell's equations]]) on any [[spacetime manifold]] $(X,g)$ read, in modern [[differential form]]-formulation:

\[
  \label{MaxwellEquationsInTraditionalDifferentialForm}
  \begin{array}{rcl}
    \mathrm{d}\,  F &=& 0 \mathrlap{\,,}
    \\
    \mathrm{d} \, \star_g F &=& j
  \end{array}
\]

where 

* the [[differential 2-form]] $F \,\in\, \Omega^2(X)$ is the [[Faraday tensor]],

* the [[differential 3-form]] $j \,\in\, \Omega^3(X)$ is the electromagnetic [[current]] density

* $\mathrm{d} \,\colon\,\Omega^p(X) \longrightarrow \Omega^{p+1}(X)$ denotes the [[de Rham differential]],


and last not least

* $\star_g \,\colon\, \Omega^p(X) \longrightarrow \Omega^{4-p}(X)$ denotes the [[Hodge star operator]] induced by the [[pseudo-Riemannian metric]] of the given [[Lorentzian manifold]] $(X,g)$.

Often this is considered for $X \simeq \mathbb{R}^{3,1}$ being [[Minkowski spacetime]], hence for $g = \eta$ the [[Minkowski metric]], in which case this describes pure "Maxwell theory", but the exact same formulas apply in the generality that $(X,g)$ is any [[Lorentzian manifold]], in which case they form the sector of the [[equations of motion]] of [[Einstein-Maxwell theory]] which involve the [[electromagnetic field]] and its coupling to [[background field|background]] [[gravity]]. (The remaining sector are the [[Einstein equations]] for the metric field $g$ sourced by the [[stress-energy tensor]] of the Maxwell field).

In order to bring out more manifestly that [[gravity]] (the [[pseudo-Riemannian metric]]) enters *only* through the [[Hodge star operator]], we may evidently re-write the above pair of equations (eq:MaxwellEquationsInTraditionalDifferentialForm) equivalently as follows:

\[
  \label{MaxwellEquationsInPreMetricDifferentialForm}
  \begin{array}{rcl}
    \mathrm{d}\,  F &=& 0 \mathrlap{\,,}
    \\
    \mathrm{d} \, G &=& j
  \end{array}
  \;\;\;\;
  \text{and}
  \;\;\;\;
  G \,=\, \star_g F
  \,.
\]

### Electromagnetism in dielectric media

In fact, this formulation (eq:MaxwellEquationsInPreMetricDifferentialForm) is closer to the (original) formulation of Maxwell's equations used in the case that spacetime $X$ is thought of as possibly filled with a *[[dielectric medium]]* where, *a priori*, one considers 2 groups of fields: 

1. the [[electric field]] $\vec E$ and [[magnetic field|magnetic]] [[flux density]] $\vec B$ 

   which constitute the [[Faraday tensor]]) given (on a local [[coordinate chart]] $(t,x^1, x^2, x^3)$) by (see [here](#InTermsOfFaradayTensor)):

  $$
    F 
      \,=\, 
    E_i \mathrm{d}x^i \wedge \mathrm{d} t 
      \,+\, 
    \epsilon_{i j k} B^i \mathrm{d} x^j \mathrm{d} x^k
  $$

as well as 

1. the actual [[magnetic field]] $\vec H$ and the *dielectric displacement cuurent* $\vec D$ with

   $$
     G 
       \,=\, 
     H_i \mathrm{d}x^i \wedge \mathrm{d} t 
       \,-\, 
     \epsilon_{i j k} D^i \mathrm{d} x^j \mathrm{d} x^k
   $$

and then imposes *constitutive equations* 
relating $(\vec E, \vec B)$ to $(\vec H, \vec D)$ and thereby expressing the [[dielectric]]-property of any electromagneric *medium* that one imagines filling the spacetime $X$.

In general, constitutive equations can be nonlinear (and even multi-valued, reflecting hysteresis effects), but for sufficiently small [[field strength]] they are of the form

$$
  G \,=\, \star_\epsilon F
$$

for a [[linear map]]

$$
  \star_\epsilon
  \,\colon\,
  \Omega^2(X)
  \longrightarrow
  \Omega^2(X)
$$

much like the [[Hodge star operator]] (whence here we use similar notation for both, which is non-standard).

## Premetric higher electromagnetism

While not usually discussed under this terminology in the literature, we may recognize [[higher gauge field|higher]] versions of "premetric" electromagnetism occuring in the ([[string theory]]-)literature:


### RR-fields in gravitational backgrounds
 {#RRFieldInGravitationalBackground}

The [[theory (physics)|theory]] of [[type II supergravity|type II]] [[D=10 supergravity]] famously contains [[higher gauge fields]] called the *[[Ramond-Ramond fields]]* or *[[RR-fields]]* for short, which may be understood as a certain higher-degree generalization of the [[electromagnetic field]]:

Where the [[electromagnetism|electromagnetic]] [[field strength]] is a single [[differential 2-form]] $F_2 \,\in\, \Omega^2(X)$ (the [[Faraday tensor]]), the [[RR-fields]] have their [[field strengths]] encoded in a [[tuple]] of [[differential forms]] in every second degree up to *half* the [[spacetime]] [[dimension of a manifold|dimension]]:

$$
  \Big\{
    F_{2p + \sigma}
    \,\in\,
    \Omega^{2p+\sigma}(X)
    \;{\Big\vert}\;
    0 \leq 2p+\kappa \leq 5
  \Big\}
  \,,
$$

where $\sigma = 0$ for [[type IIA supergravity]] and $\sigma = 1$ for [[type IIB supergravity]].

Moreover, the [[equations of motion]] of these [[RR-fields]] are of the general form of [[Maxwell's equations]], in fact when the [[Kalb-Ramond field]] and the [[spinor fields]] vanish, then the equations of motion are as before, up to form degree

$$
  \begin{array}{rcl}
    \mathrm{d} F_{2p + \sigma} &=& 0
    \\
    \mathrm{d} \star_g F_{2p + \sigma} &=& 0
  \end{array}
$$

and in more generality the right-hand sides are non-vanishing combinations of the [[Kalb-Ramond field]] (already for the first equation!) and the [[spinor fields]].

But one may famously understand [[type II supergravity]] as the low-energy limit of [[type II string theory]], in which case there are subtle [[flux quantization laws]] of the total [[flux]] of these [[RR-fields]] (in variation of the [[Dirac charge quantization]]-law imposed on the Maxwell field when regarding [[electromagnetism]] as the background field for [[quantum]] [[electrons]]). 

A widely-considered [[conjecture]] ([[K-theory classification of D-brane charge|here]]) says that this [[flux quantization]] is realized by 

1. regarding the would-be [[Hodge duality|Hodge duals]] $\star_g F_{2p + \sigma}$ of the RR-fields as independent fields $F_{10-2p-\sigma}$, so that the "pre-metric RR-field" now has about twice as many components:

   $$
     \Big\{
       F_{2p + \sigma}
       \,\in\,
       \Omega^{2p+\sigma}(X)
       \;{\Big\vert}\;
       0 \leq 2p+\kappa \leq 5
     \Big\}
     \,,
   $$

   and then regarding/constraining such a [[tuple]] as the image under the [[Chern character]] of a class in ([[differential K-theory|differentia]]) complex [[topological K-theory]] in addition to imposing the pre-metric [[equations of motion]].

1. afterwards imposing the Hodge-duality constraint, now thought of as a "self-duality" on K-theory and remaining subject to discussion in the literature: see at *[[self-dual higher gauge field]]* the section *[Examples -- RR-Fields](self-dual+higher+gauge +theory#RRFieldsin10d).

(This is stated for vanishing [[Kalb-Ramond field]], for ease of exposition here. More generally the KR-field does not vanish and the above discussion applies for [[twisted K-theory]].)

Clearly, this just the idea of "pre-metric electromagnetism" but now enacted in a variant situation.

### $C$-Field in gravitational background

Somewhat similarly, the [[equations of motion]] of the [[supergravity C-field]] in [[D=11 supergravity]] are of the form

$$
  \begin{array}{rcl}
    \mathrm{d} G_4 &=& 0
    \\
    \mathrm{d} \star_g G_4 &=& \tfrac{1}{2} G_4 \wedge G_4
  \end{array}
$$

where now $G_4 \,\in\, \Omega^4(X)$ is a [[differential 4-form]]. If we regard these equations in "pre-metric" form as in the above discussion of the [[RR-fields]], by introducing an a priori independent 7-form $G_7 \,\in\, \Omega^7(X)$, then they read

\[
  \label{PreMetricEOMsForCField}
  \begin{array}{rcl}
    \mathrm{d} G_4 &=& 0
    \\
    \mathrm{d} G_7 &=& \tfrac{1}{2} G_4 \wedge G_4
  \end{array}
  \;\;\;\;\;\;
  \text{and}
  \;\;\;\;\;\;
  G_7 \,=\, \star_g G_4
  \,.
\]

As for the [[RR-field]] and its conjectured [[K-theory classification of D-brane charge|charge quantization in K-theory]], in this "pre-metric" formulation it makes sense to ask which [[generalized cohomology theory]] yields the differential equations on the left, as those characterizing the image under its generalized [[Chern-Dold character|Chern-Dold-like charatcer]].

There is no [[Whitehead-generalized cohomology theory]] with this property, due to the non-linear [[Quadratic Functions in Geometry, Topology, and M-Theory|quadratic function]] $G_4 \mapsto \tfrac{1}{2} G_4 \wedge G_4$ appearing in (eq:PreMetricEOMsForCField), but there is a [[non-abelian cohomology]] theory with the correct [[schreiber:The Character Map in Non-Abelian Cohomology|nonabelian character map]]: namely [[Cohomotopy|4-Cohomotopy theory]]. This observation (due to [Sati (2013,2018), §2.5](https://ncatlab.org/schreiber/show/Hypothesis+H#ReferencesInRational)) suggests (this is "[[schreiber:Hypothesis H]]") that the [[charge quantization]] of the [[supergravity C-field]] in [[M-theory]] may be in some form of [[Cohomotopy]] theory.


## References

The idea (if not the terminology) of pre-metric electromagnetism is attributed to:

* {#Kottler22a} [[Friedrich Kottler]], *Newtonsches Gesetz und Metrik*, Sitzungsber. Akad. Wiss. Wien, Math.-Naturw. Klasse, Abt. IIa, **131** (1922) 1-14 &lbrack;Engl. transl. by [[David H. Delphenich|Delphenich]]: [pdf](http://www.neo-classical-physics.info/uploads/3/4/3/6/34363841/kottler_-_newtons_law_and_metrics.pdf), [[Kottler-NewtonsLawAndMetric.pdf:file]]&rbrack;

* {#Kottler22b} [[Friedrich Kottler]], *Maxwell'sche Gleichungen und Metrik*, Sitz. Akad. Wien IIa **131** (1922) 119-146 &lbrack;Engl. transl. by [[David H. Delphenich|Delphenich]]: [pdf](http://www.neo-classical-physics.info/uploads/3/4/3/6/34363841/kottler_-_maxwells_equation.pdf), [[Kottler-MaxwellEquationsAndMetric.pdf:file]]&rbrack;

also:

* {#Dantzig34} [[David van Dantzig]], *The fundamental equations of electromagnetism, independent of metrical geometry*, Mathematical Proceedings of the Cambridge Philosophical Society **30** 4  (1934) 421-427 &lbrack;[doi:10.1017/S0305004100012664](https://doi.org/10.1017/S0305004100012664)&rbrack;

Early review:

* [[Edmund T. Whittaker]]: pp. 192-196 of: *A History of the Theories of Aether and Electricity* -- Vol. 2: *The Modern Theories 1900-1926* (1953), reprinted by Humanities Press (1973) &lbrack;<a href="https://isidore.co/CalibreLibrary/Whittaker,%20Edmund%20Taylor/A%20History%20of%20the%20Theories%20of%20Aether%20and%20Electricity_%20The%20Modern%20Theories%201900-1926%20(4500)/A%20History%20of%20the%20Theories%20of%20Aether%20and%20El%20-%20Whittaker,%20Edmund%20Taylor.pdf">pdf</a>, <a href="https://en.wikipedia.org/wiki/A_History_of_the_Theories_of_Aether_and_Electricity">Wikipedia entry</a>&rbrack;

  > "&lbrack;...&rbrack; This chapter has been concerned, for the most part, with General Relativity, which is essentially a geometrisation of physics. It may be closed with some accountof a movement in the opposite direction, seeking to abolish the priviledged position of geometry in physics, and indeed inquiring how far it may be possible to construct a physics independent of geometry. Since the notion of metric is a complicated one, which requires measurements with clocks and scales, generally with *rigid* bodies, which themselves are systems of great compelxity, it seems undesirable to take metric as fundamental, particularly for phenomena which are simpler and actually independent of it."

  > "The movement was initiated by Friedrich Kottler of Vienna, who in 1922 published two papers &lbrack;[Kottler (1922a)](#Kottler22a), [(1922b)](#Kottler22b)&rbrack;"

Further amplification of the *[[constitutive equation|constitutive]] map* that relates the pre-metrically independent fields:

* [[E. Jan Post]], *The constitutive map and some of its ramifications*, Annals of Physics **71** 2 (1972) 497-518 &lbrack;<a href="https://doi.org/10.1016/0003-4916(72)90129-7">doi:10.1016/0003-4916(72)90129-7</a>&rbrack;


The terminology "pre-metric electromagnetism" seems to be due to [[David H. Delphenich]], who gives much further discussion:

* {#Delphenich05a} [[David H. Delphenich]], *On the Axioms of Topological Electromagnetism*, Annalen Phys. **14** (2005) 347-377 &lbrack;[arXiv:hep-th/0311256](https://arxiv.org/abs/hep-th/0311256), [doi:10.1002/andp.20055170601](https://doi.org/10.1002/andp.20055170601)&rbrack;

* {#Delphenich05b} [[David H. Delphenich]], *Symmetries and pre-metric electromagnetism*, Ann. Phys. **14** (2005) 663-704 &lbrack;[arXiv:gr-qc/0508035](https://arxiv.org/abs/gr-qc/0508035), [doi:10.1002/andp.200510159](https://doi.org/10.1002/andp.200510159)&rbrack;

* {#Delphenich07} [[David H. Delphenich]], *On linear electromagnetic constitutive laws that define almost-complex structures*, Annalen Phys. **16** (2007) 207-217 &lbrack;[doi:gr-qc/0610031](https://arxiv.org/abs/gr-qc/0610031), [doi:10.1002/andp.200610227](https://doi.org/10.1002/andp.200610227)&rbrack;

* {#Delphenich08} [[David H. Delphenich]], *Spinors and Pre-Metric Electromagnetism*, Advances in Applied Clifford Algebras **18** (2008) 567–578 &lbrack;[doi:10.1007/s00006-008-0115-6](https://doi.org/10.1007/s00006-008-0115-6)&rbrack;

* {#Delphenich15} [[David H. Delphenich]], *Pre-metric electromagnetism as a path to unification*, in: *Unified Field Mechanics*, World Scientific (2015) 215-220 &lbrack;[arXiv:1512.05183](https://arxiv.org/abs/1512.05183), [doi:10.1142/9789814719063_0023](https://doi.org/10.1142/9789814719063_0023)&rbrack;

Monographs:

* {#DelphenichBook} [[David H. Delphenich]], *Pre-Metric Electromagnetism* &lbrack;part I:[pdf](http://www.neo-classical-physics.info/uploads/3/4/3/6/34363841/intro-chap_vi.pdf), part II:[pdf](http://www.neo-classical-physics.info/uploads/3/4/3/6/34363841/chapter_vii-xii.pdf), full:[[Delphenich-PreMetricElectromagnetism.pdf:file]]&rbrack;

* [[Friedrich W. Hehl]], [[Yuri N. Obukhov]], *Foundations of Classical Electrodynamics -- Charge, Flux, and Metric*, Progress in Mathematical Physics **33**, Springer (2003) &lbrack;[arXiv:10.1007/978-1-4612-0051-2](https://doi.org/10.1007/978-1-4612-0051-2)&rbrack;


Further discussion:

* {#HehlItinObukhov16} [[Friedrich W. Hehl]], [[Yakov Itin]], [[Yuri N. Obukhov]], *On Kottler's path: origin and evolution of the premetric program in gravity and in electrodynamics*, International Journal of Modern Physics D **25** 11 (2016) 1640016  &lbrack;[arXiv:1607.06159](https://arxiv.org/abs/1607.06159), [doi:10.1142/S0218271816400162](https://doi.org/10.1142/S0218271816400162)&rbrack;

* [[Yakov Itin]], *Premetric representation of mechanics, electromagnetism and gravity*, International Journal of Geometric Methods in Modern Physics **15** supp01 (2018) &lbrack;[doi:10.1142/S0219887818400029](https://doi.org/10.1142/S0219887818400029)&rbrack;

* [[Yuri N. Obukhov]], *Premetric approach in gravity and electrodynamics*, in: *The Fifteenth Marcel Grossmann Meeting* (2022) 654-659 &lbrack;[doi:10.1142/9789811258251_0087](https://doi.org/10.1142/9789811258251_0087), [arXiv:1904.00180](https://arxiv.org/abs/1904.00180)&rbrack;



[[!redirects premetric electromagnetic]]

[[!redirects pre-geometric electromagnetic]]
[[!redirects pregeometric electromagnetic]]


[[!redirects pre-metric electrodynamics]]
[[!redirects premetric electrodynamics]]

[[!redirects pre-geometric electrodynamics]]
[[!redirects pregeometric electrodynamics]]




