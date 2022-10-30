
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _axion_ is a hypothetical type of [[field (physics)|field]]/[[fundamental particle]] originally hypothesized ([Weinberg 77](#Weinberg77), [Wilcek 78](#Wilcek78))  as a solution to the [[strong CP problem]] in the [[standard model of particle physics]]. 
After the initial model for the axion was quickly ruled out by [[experiment]] (see [Wilcek 78](#Wilcek78) for the early history) a variant model was found ([Dine-Fischler-Srednicki 81](#DineFischlerSrednicki81)), called the "invisible axion", which does not violate experimental bounds. 

The "invisible axion" turns out to also be a natural candidate for [[dark matter]] [Preskill-Wise-Wilcek 83](#PreskillWiseWilcek83), hence potentially also solves one of the problems with the [[standard model of cosmology]]. More recently it is argued in [Hui-Ostriker-Tremaine-Witten 16](#HOTW16) that indeed axionic dark matter ([[fuzzy dark matter]]) potentially solves the remaining problems of standard WIMP dark matter models: WIMP dark matter models work exceedingly well on [[cosmology|cosmological]] scales but has serious experimental problems on the scale of [[galaxies]]. Due to the extreme lightness of axion particles, their [[de Broglie wavelength]] may be of the scale of galaxies and hence their quantum properties may become relevant at this scale to deviate in the right way from the WIMP models.

The Pecchei-Quinn shift symmetry of the axion and the peculiar nature of the axion [[interaction term]] which are needed to make the axion model work this way have been argued to naturally arise in [[string theory]], if the axion is identified with the [[KK-reduction]] of the [[higher gauge fields]] in [[string theory]].



## As a solution to the strong CP problem
 {#AsASolutionToTheStrongCPProblem}

The problem here is that the [[action functional]] for [[QCD]] ([[Yang-Mills theory]]) a priori contains an arbitrary [[theta angle]] $\theta$

$$
  S
  \;\colon\;
  \nabla \mapsto
  \frac{1}{g^2 }\int_X tr(F_\nabla \wedge \star F_\nabla)  \;+\; 
  \theta \int_X tr(F_\nabla \wedge F_\nabla)
$$

but that -- since the term $tr(F_\nabla \wedge F_\nabla)$ causes parity violation, which is strongly constrained by [[experiment]] -- there must be some reason why $\theta$ vanishes or else is extremely small.

(Here the term $tr(F_\nabla \wedge F_\nabla)$ is the [[invariant polynomial]] for the [[second Chern class]], measuring the [[instanton number]] of the [[gauge field]] $\nabla$.)

The solution to this problem via axions is to assume that $\theta$ is not really a fundamental parameter, but instead is the [[vacuum expectation value]] of a dynamical [[field (physics)|field]] $a$ (the axion). 

The idea is that a standard [[kinetic action]] 

$$
  S_{kin} (a) \propto \int_X a \wedge \ast a
$$

together with the axion [[interaction]] term

$$
  S_{int} (a,\nabla) \propto  \int_X a \, tr(F_\nabla \wedge F_\nabla)
$$ 

makes $a$ have vanishing [[expectation value]] $\langle a\rangle$. This would give a dynamical explanation why under the identification of the [[theta angle]] with this expectation value

$$
  \theta \coloneqq \langle a\rangle
$$

the theta angle vanishes.


## The Vafa-Witten mechanism
 {#VafaWittenMechanism}

That this is indeed the case is due to [Vafa-Witten 84, around (2)](#VafaWitten84). These authors argue via the [[Wick rotation|Wick rotated]] [[path integral]] as follows:

Under [[Wick rotation]], parity-violating terms in the [[Lagrangian density]] pick up an imaginary factor $i$. Therefore the [[path integral]] expression for the Wick rotated [[vacuum energy]] is

$$
  \begin{aligned}
    E_{vac}(a)
    &= 
    - log \left( \underset{\nabla,a}{\int}  \exp(- S(\nabla,a)) \, D \nabla \, D a \right)
    \\
    &= 
    - log 
      \left(
       \underset{\nabla}{\int} \exp\left(
        \frac{1}{g^2 }\int_X tr(F_\nabla \wedge \star F_\nabla)  
     \right)
      \, D \nabla
      \;
     \underset{a}{\int}
     \exp\left(
        i a \int_X tr(F_\nabla \wedge F_\nabla)
     \right)
     \, D a
    \right)
  \end{aligned}
  \,.
$$

Now due to the factor of $i$ in front of $\theta$ in this expression, the real part of the argument of the logarithm necessarily becomes _smaller_ with $a$. Therefore the negative logarithm becomes _larger_ with $a$. Accordingly $E_{vac}(a)$ must have a minimum at $\theta = 0$ (according to [Vafa-Witten 84, p.2](#VafaWitten84)).
 


## In string theory -- Axions as KK-reduction of higher gauge fields
 {#AsArisingFromStringTheory}

In [[string theory]] axion fields naturally arise, as amplified in particular in [Svrcek-Witten 06](#SvrcekWitten06):

> An obvious question about the axion hypothesis is how natural it really is. Why introduce a global PQ "symmetry" if it is not actually a symmetry? What is the sense in constraining a theory so that the classical Lagrangian possesses a certain symmetry if the symmetry is actually anomalous? It could be argued that the best evidence that PQ "symmetries" are natural comes from string theory, which produces them without any contrivance. ... the string compactifications always generate PQ symmetries, often spontaneously broken at the string scale and producing axions, but sometimes unbroken. ([Svrcek-Witten 06, pages 3-4](#SvrcekWitten06))

Similarly from [ADDKM 09](#ADDKM09):

> However, at the [[effective field theory]] level  it  is  hard  to  judge  how natural it is to have such a "fake" global PQ symmetry which is explicitly broken exclusively by QCD. Note, that in order not to spoil the solution to the strong CP problem all other sources of explicit PQ symmetry breaking should be at least 10 orders of magnitude down with respect to the potential  generated  by the QCD anomaly, and one may be especially cautious about the viability of such a proposal, given the common lore that global symmetries always get broken by quantum gravitational effects [12, 13, 14]. This makes it natural to inquire whether axions arise naturally in the most developed quantum theory of gravity—string theory. ([ADDKM 09, p. 3](#ADDKM09))

The mechanism discussed in [Svrcek-Witten 06](#SvrcekWitten06), in all its incarnations in the various perspectives on string theory ([[heterotic string theory|heterotic strings]], [[type II string theory|type II strings]], [[11-dimensional supergravity]] with [[M-theory]] effects included, etc.) share the following properties:

1. the axion field itself is the [[double dimensional reduction]] of one of the [[higher gauge fields]] in string theory, the (twisted) [[Kalb-Ramond field]] for heterotic string, the [[RR-field]] for the type II string, or the [[supergravity C-field]] in 11-dimensional supergravity with [[M-brane]] effects;

1. accordingly the Peccei-Quinn periodic shift symmetry of the axion results arises as the $U(1)$-[[gauge symmetry]] that is the dimensional reduction of the $B^2 U(1)$ (heterotic [[B-field]]) or $B^3 U(1)$ (11d [[C-field]]) [[higher gauge symmetry]], where the $U(1)$-periodicity is ultimately due to the higher [[Dirac charge quantization]] for these fields;

1. the axion [[interaction term]] of the form $\propto a \langle F \wedge F\rangle $ arises as the [[double dimensional reduction]] of the self-interaction terms of these higher gauge fields: 

   * in type II string theory it is a component of the [[higher WZW term]] on coincident [[D6-branes]] with a component $\propto A_{3}^{RR} \wedge \langle F \wedge F\rangle$, 

   * for 11d C-fields it is the term $\propto C_{3} \wedge \langle F \wedge F\rangle$ induced by [[anomaly cancellation]] for M-theory at conical singularities (as discussed at _[[M-theory on G2-manifolds]]_)

   * for heterotic string theory it arises from integrating out the [[Lagrange multiplier]] that enforces the [[Green-Schwarz anomaly cancellation]] in 4d.

below we describe these various perspecrtives on the string theoretic axions in more detail.




### In type IIA string theory

Consider [[string phenomenology]] in [[type IIA string theory]] in the guise of [[intersecting D-brane models]] with the [[standard model of particle physics]] supported in intersecting [[D6-branes]] whose [[worldvolume]] fills all of 4d [[spacetime]].

The [[higher WZW term]] in the [[Green-Schwarz action functional]] for the [[D6-brane]] is of the form

$$ 
  \propto \int_{X_7} A^RR \wedge \langle \exp(F_\nabla) \rangle
$$

where $A^RR$ denotes the collective inhomogenous [[background field|backgound]] [[RR-field]] and $F_\nabla$ is the [[curvature]] 2-form of the [[Chan-Paton gauge field]] on the D-brane. The $\langle -\rangle$ denotes the [[Killing form]] [[invariant polynomial]], hence the [[trace]] for the [[special unitary Lie algebra]] regarded as a [[matrix Lie algebra]]. $X_7$ denotes the [[worldvolume]] of the [[D6-brane]]

Hence one of the three non-vanishing summands in this expression is

$$
  \propto \int_{X_7} A_3^{RR} \wedge \langle F_\nabla \wedge F_\nabla\rangle 
  \,.
$$

Now assuming a Kaluza-Klein ansatz $X_7 = X_4 \times Y_3$ with 

$$
  a \coloneqq \int_{Y_3} A_3^{RR}
$$

the effective axion field in 4d, then this term becomes the 
axion [[interaction]] term

$$
  \propto \int_{X_4} a \langle F_{\nabla} \wedge F_{\nabla}\rangle
$$

([Svrcek-Witten 06, around (6.9)](#SvrcekWitten06))


### In heterotic string theory

In [[heterotic string theory]] [[KK-compactification|KK-compactified]] to 4d, the 4d [[B-field]], dualized, serves as the axion field, called the "model independent axion" ([Svrcek-Witten 06, starting p. 15](#SvrcekWitten06)).

This works as follows: By the [[Green-Schwarz anomaly cancellation]] mechanism, then [[B-field]] in [[heterotic string theory]] is a twisted 2-form field, whose [[field strength]] $H$ locally has in addition to the exact differential $d B$ also a fundamental 3-form contribution, so that

$$
  H = d B + C
$$

(locally). Moreover, the differential $d H$ is constrained to be the Pontryagin 4-form of the gauge potential $\nabla$ (minus that of the  [[Riemann curvature]], but let's suppress this notationally for the present purpose):

$$
  d H = tr \left(F_\nabla \wedge F_\nabla\right)
  \,.
$$

Now suppose [[KK-compactification]] to 4d has been taken care of, then this constraint may be implemented in the [[equations of motion]] by adding it to the [[action functional]], multiplied with a [[Lagrange multiplier]] :

$$
  S 
    =  
  \underset{
      \text{kinetic action} \atop \text{for B-field}
   }{
        \underbrace{\int_X H \wedge \star H}
   }
    +  
   \underset{
      \text{Green-Schwarz constraint}
   }{
    \underbrace{
      \int_X a \left( d H - tr(F_\nabla \wedge F_\nabla) \right)
    }
   }
  \,.
$$

Now by the usual argument, one says that instead of varying by $a$ and thus implementing the [[Green-Schwarz anomaly cancellation]] constraint, it is equivalent to fist vary with respect to the other fields, and then insert the resulting equations in terms of $a$ into the action functional.

Now since we are dealing with a twisted [[B-field]], with free 3-form component $C$, we actually vary with respect to $C$. This yields the [[Euler-Lagrange equation]] [[equation of motion|of motion]]

$$
  d a = \star H
  \,,
$$

hence the usual relation or [[electro-magnetic duality]], expressing what used to be the [[Lagrange multiplier]] now as the magentic dual [[field (physics)|field]] to the twisted [[B-field]].

Plugging this algebraic [[equation of motion]] back into the above [[action functional]] for $H$ gives

$$
  \tilde S
    =
  \underset{\text{kinetic action} \atop \text{for axion field}}{\underbrace{\int_X d a \wedge \star d a}}
  + 
  \underset{\text{axionic} \atop \text{interaction}}{\underbrace{\int_X a \, tr(F_\nabla \wedge F_\nabla)}}
  \,.
$$

This now is an action functional for an axion field $a$ of just the form required [above](#AsASolutionToTheStrongCPProblem) for the solution of the [[strong CP-problem]].




## Related concepts

* [[axion inflation]]

[[!include fields and quanta - table]]


## References

### General

The axion as such was originally proposed in 

* {#Weinberg77} [[Steven Weinberg]], _New light boson_, Phys. Rev. Lett. 40:223-6 (1977)

* {#Wilcek78} [[Frank Wilcek]], _Problem of strong P and T invariance in the presence of instantons_, Phys. Rev. Lett. 40:279-82 (1978)

The experimentally viable variant as the "invisible axion" is due to 

* {#DineFischlerSrednicki81} [[Michael Dine]], [[Willy Fischler]], [[Mark Srednicki]], _A simple solution to the strong CP problem with a harmless axion_, Phys. Lett. B 104:199-202 (1981)

The observation that the "invisible axion" is a candidate for [[dark matter]] is due to three groups:

* {#PreskillWiseWilcek83} [[John Preskill]], M. Wise, [[Frank Wilcek]], _Cosmology of the invisible axion_, Phys. Lett. B 120:127-32 (1983)

* {#AbbottSikivie83} L.F. Abbott, P. Sikivie, _A Cosmological Bound on the Invisible Axion_, Phys.Lett. B120:133-36 (1983)

* {#DineFischler83} [[Michael Dine]], [[Willy Fischler]], _The Not So Harmless Axion_, Phys.Lett. B120:137-141 (1983)

A historical recollection of the development until here is in

* [[Frank Wilcek]], _Birth of axions_ in _This Week's Citation Classic_ (1991) ([pdf](http://www.garfield.library.upenn.edu/classics1991/A1991FE76900001.pdf))

The argument that the [[topological Yang-Mills theory|topological]] [[interaction]] term $\propto a \langle F \wedge F\rangle$ gives the axion field $a$ a vanishing [[vacuum expectation value]] is due to

* {#VafaWitten84} [[Cumrun Vafa]], [[Edward Witten]], _Parity Conservation in Quantum Chromodynamics_, Phys. Rev. Lett. 53, 535 (1984) ([publisher](http://journals.aps.org/prl/abstract/10.1103/PhysRevLett.53.535))

A reformulation of this effect in terms of [[Chern-Simons forms]] is discussed in

* [[Gia Dvali]], _Three-Form Gauging of axion Symmetries and Gravity_ ([arXiv:hep-th/0507215](https://arxiv.org/abs/hep-th/0507215))

Review includes:

* Jihn E. Kim, Gianpaolo Carosi, _Axions and the Strong CP Problem_, Rev.Mod.Phys.82:557-602,2010 ([arXiv:0807.3125](https://arxiv.org/abs/0807.3125))

* Masahiro Kawasaki, Kazunori Nakayama, _Axions : Theory and Cosmological Role_, Annual Review of Nuclear and Particle Science Vol.63:1-552   ([arXiv:1301.1123](https://arxiv.org/abs/1301.1123))

* Wikipedia _[Axion](http://en.wikipedia.org/wiki/Axion)_


### In string theory
  {#ReferencesInStringTheory}

Discussion of the various ways that axions naturally appear in [[string theory]] is in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))

and discussion specifically for the [[F-theory]] sector of string theory is in

* {#Grimm14} Thomas Grimm, _Axion Inflation in F-theory_ ([arXiv:1404.4268](http://arxiv.org/abs/1404.4268))

A textbook account of axion [[string phenomenology]] is in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 16.2 of _String Theory and Particle Physics: An Introduction to String Phenomenology_, Cambridge University Press 2012


Discussion of stringy axion [[cosmology]] (such as [[fuzzy dark matter]]) is in 

* {#ADDKM09} Asimina Arvanitaki, Savas Dimopoulos, Sergei Dubovsky, Nemanja Kaloper, John March-Russell, _String Axiverse_, Phys.Rev.D81:123530,2010 ([arXiv:0905.4720](https://arxiv.org/abs/0905.4720))

* {#AcharyaBobkovKumar10} [[Bobby Acharya]], Konstantin Bobkov, [[Piyush Kumar]], _An M Theory Solution to the Strong CP Problem and Constraints on the Axiverse_, JHEP 1011:105, 2010 ([arXiv:1004.5138](https://arxiv.org/abs/1004.5138))

* {#AcharyaKaneKumar12} [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_, Int. J. Mod. Phys. A, Volume 27 (2012) 1230012 ([arXiv:1204.2795](https://arxiv.org/abs/1204.2795))

From [Acharya-Kane-Kumar 12, p. 3](#AcharyaKaneKumar12):

> Now consider the axions.  Due to the shift symmetries mentioned above, there are no [[perturbative QFT|perturbative]] contributions to their potential.  [[non-perturbative effect|Non-perturbative effects]] though, such as strong gauge dynamics, gauge [[instantons]], gaugino condensation and stringy instantons will generate a potential for the axions. Because any such contribution is exponentially suppressed by couplings and/or extra-dimensional volumes, in our world with perturbative gauge couplings (at high scales), the axion masses will be exponentially small.  

> Furthermore, since there are large numbers of axions in general, their masses will essentially be uniformly distributed on a logarithmic scale ([5](#ADDKM09)).  See ([6](#AcharyaBobkovKumar10)) for a detailed calculation of axion masses in string/M effective theories. 

> Like the moduli, the axions are also very weakly coupled to matter and therefore do not thermalize in general.  Moreover, since their masses are tiny - ranging from $m_{3/2}$ to  even  below  the  Hubble  scale  today  -  many  of them,  including  the  QCD  axion,  start  coherent  oscillations  during  the  time  that  the  moduli  are  dominating the energy density, but before BBN. 

### Experimental signature


* Joseph P. Conlon, M.C. David Marsh, _Searching for a 0.1-1 keV Cosmic Axion Background_ ([arXiv:1305.3603](http://arxiv.org/abs/1305.3603))

  > Primordial decays of [[string theory]] [[moduli stabilization|moduli]] at $z \sim 10^{12}$ naturally generate a [[dark radiation]] Cosmic Axion Background (CAB) with $0.1 - 1 keV$ energies. This CAB can be detected through axion-[[photon]] conversion in astrophysical [[magnetic fields]] to give quasi-thermal excesses in the extreme ultraviolet and soft X-ray bands. Substantial and observable luminosities may be generated even for axion-photon couplings $\ll 10^{-11} GeV^{-1}$. We propose that axion-photon conversion may explain the observed excess emission of soft X-rays from galaxy clusters, and may also contribute to the diffuse unresolved cosmic X-ray background. We list a number of correlated predictions of the scenario. 


Discussion of the axion as a candidate for [[dark matter]] ([[fuzzy dark matter]]) is

* {#HOTW16} [[Lam Hui]], [[Jeremiah Ostriker]], [[Scott Tremaine]], [[Edward Witten]], _On the hypothesis that cosmological dark matter is composed of ultra-light bosons_, Phys. Rev. D 95, 043541 (2017) ([arXiv:1610.08297](https://arxiv.org/abs/1610.08297))

with its experimental bounds

* Nilanjan Banik, Adam J. Christopherson, Pierre Sikivie, Elisa Maria Todarello, _New astrophysical bounds on ultralight axionlike particles_, Phys. Rev. D 95, 043542 (2017) ([arXiv:1701.04573](https://arxiv.org/abs/1701.04573))

and as a candidate for [[dark energy]]:

* [[Stephon Alexander]], [[Robert Brandenberger]], [[Juerg Froehlich]], _Tracking Dark Energy from Axion-Gauge Field Couplings_ ([arXiv:1601.00057](https://arxiv.org/abs/1601.00057))

See also

* [[Frank Wilczek]], _New Ideas in Axion Searches_, talk 2017 ([pdf](http://frankwilczek.com/2017/axion_searches_01.pdf))

[[!redirects axions]]

[[!redirects invisible axion]]
[[!redirects invisible axions]]
