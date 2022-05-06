009638231
-- {: sarah ann alvarez rightHandSide}
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

The _axion_ is a hypothetical type of [[field (physics)|field]]/[[fundamental particle]] originally hypothesized ([Weinberg 77](#Weinberg77), [Wilczek 78](#Wilczek78))  as a solution to the [[strong CP problem]] in the [[standard model of particle physics]]. 
After the initial model for the axion was quickly ruled out by [[experiment]] (see [Wilczek 78](#Wilczek78) for the early history) a variant model was found ([Dine-Fischler-Srednicki 81](#DineFischlerSrednicki81)), called the "invisible axion", which does not violate experimental bounds. 

The "invisible axion" turns out to also be a natural candidate for [[dark matter]] [Preskill-Wise-Wilczek 83](#PreskillWiseWilczek83), hence potentially also solves one of the problems with the [[standard model of cosmology]]. More recently it is argued in [Hui-Ostriker-Tremaine-Witten 16](#HOTW16) that indeed axionic dark matter ([[fuzzy dark matter]]) potentially solves the remaining problems of standard WIMP dark matter models: WIMP dark matter models work exceedingly well on [[cosmology|cosmological]] scales but has serious experimental problems on the scale of [[galaxies]]. Due to the extreme lightness of axion particles, their [[de Broglie wavelength]] may be of the scale of galaxies and hence their quantum properties may become relevant at this scale to deviate in the right way from the WIMP models.

The Pecchei-Quinn shift symmetry of the axion and the peculiar nature of the axion [[interaction term]] which are needed to make the axion model work this way have been argued to naturally arise in [[string theory]], if the axion is identified with the [[KK-reduction]] of the [[higher gauge fields]] in [[string theory]]. This we discuss [below](#AsArisingFromStringTheory).



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


### The Vafa-Witten mechanism
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
 



## In string theory 
 {#AsArisingFromStringTheory}

In [[string theory]] axion fields 

1. are naturally present as the [[KK-reduction]] of the [[higher gauge fields]] (e.g. [Svrcek-Witten 06](#SvrcekWitten06));

   reviewed below in:

   _[As KK-Reduction of higher gauge fields](#AxionsAsKKReductionOfHigherGaugeFields)_

1. are generically of positive but tiny mass ([ADDKM 09](#ADDKM09), [Acharya-Bobkov-Kumar 10](#AcharyaBobkovKumar10)) as they need to be to be a solution to the [[strong CP problem]] and be candidates for [[fuzzy dark matter|BEC/superfluid/fuzzy dark matter]];

   reviewed below in:

   _[Stringy axion phenomenology](#StringyAxionPhenomenology)_

This makes axion fields in string theory form a curious confluence point relating  

* abstract concepts related to [[higher gauge theory]] 

with

* fundamental question in [[standard model of particle physics|particle physics]]/[[standard model of cosmology|cosmology]] [[phenomenology]]:

$$
  \array{
    \mathbf{\text{higher gauge theory}}
    &&
    &&
    \mathbf{\text{particle physics/cosmology phenomenology}}
    \\
    \\
    \left.
      \array{
        \text{higher gauge fields}
        \\
        \text{higher characteristic classes} 
        \\
        \updownarrow
        \\
        \text{non-perturbative QFT/string effects}
        \\
        \text{in HET: Green-Schwarz anomaly cancellation}
        \\
        \text{in IIA/B: higher WZW term for Green-Scharz D-branes}
      }
    \right\}
    &\longrightarrow&
    \array{
      \text{axion fields}
      \\
      \text{in the string spectrum}
    }
    &\longrightarrow&
    \left\{
      \array{
        \text{solve strong CP-problem as with P-Q robustly}
        \\
        \text{solve dark matter problem by FDM}
      }
    \right.
  }
$$



### Axions as KK-reduction of higher gauge fields
 {#AxionsAsKKReductionOfHigherGaugeFields}

In [[string theory]] axion fields _naturally_ arise as the [[KK compactification]] of the [[higher gauge fields]] ([[B-field]], [[C-field]], [[RR-fields]]). Here we review how this comes about.

Notice that this means that axions in string theory are as in the output of the original Peccei–Quinn proposal, but do not actually make use of the Peccei–Quinn mechanism. 

As amplified in particular in [Svrcek-Witten 06](#SvrcekWitten06):

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

We now discuss this in more detail:

* _[In type IIA string theory](#IntypeIIA)_

* _[In heterotic string theory](#InHeteroticStringTheory)_

#### In type IIA string theory
  {#IntypeIIA}

Consider [[string phenomenology]] in [[type IIA string theory]] in the guise of [[intersecting D-brane models]] with the [[standard model of particle physics]] supported in intersecting [[D6-branes]] whose [[worldvolume]] fills all of 4d [[spacetime]].

The [[higher WZW term]] in the [[Green-Schwarz action functional]] for the [[D6-brane]] is of the form

$$ 
  \propto \int_{X_7} A^RR \wedge \langle \exp(F_\nabla) \rangle
$$

where $A^RR$ denotes the collective inhomogenous [[background field|background]] [[RR-field]] and $F_\nabla$ is the [[curvature]] 2-form of the [[Chan-Paton gauge field]] on the D-brane. The $\langle -\rangle$ denotes the [[Killing form]] [[invariant polynomial]], hence the [[trace]] for the [[special unitary Lie algebra]] regarded as a [[matrix Lie algebra]]. $X_7$ denotes the [[worldvolume]] of the [[D6-brane]]

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


#### In heterotic string theory
  {#InHeteroticStringTheory}

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

Now by the usual argument, one says that instead of varying by $a$ and thus implementing the [[Green-Schwarz anomaly cancellation]] constraint, it is equivalent to first vary with respect to the other fields, and then insert the resulting equations in terms of $a$ into the action functional.

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


### Stringy axion phenomenology
 {#StringyAxionPhenomenology}

From [Acharya-Kane-Kumar 12, p. 3](#AcharyaKaneKumar12):

> Now consider the axions.  Due to the shift symmetries mentioned above, there are no [[perturbative QFT|perturbative]] contributions to their potential.  [[non-perturbative effect|Non-perturbative effects]] though, such as strong gauge dynamics, gauge [[instantons]], gaugino condensation and stringy instantons will generate a potential for the axions. Because any such contribution is exponentially suppressed by couplings and/or extra-dimensional volumes, in our world with perturbative gauge couplings (at high scales), the axion masses will be exponentially small.  

> Furthermore, since there are large numbers of axions in general, their masses will essentially be uniformly distributed on a logarithmic scale ([5](#ADDKM09)).  See ([6](#AcharyaBobkovKumar10)) for a detailed calculation of axion masses in string/M effective theories. 

> Like the moduli, the axions are also very weakly coupled to matter and therefore do not thermalize in general.  Moreover, since their masses are tiny - ranging from $m_{3/2}$ to  even  below  the  Hubble  scale  today  -  many  of them,  including  the  QCD  axion,  start  coherent  oscillations  during  the  time  that  the  moduli  are  dominating the energy density, but before BBN. 

Observe that ultralight axion fields is precisely what is required in HEP [[phenomenology]] for

1. the solution to the [[strong CP-problem]];

1. the solution of the [[dark matter]] problem via [[fuzzy dark matter|BEC/superfluid/wave/fuzzy dark matter]] (e.g. [Hui-Ostriker-Tremaine-Witten 16](#HOTW16)).



## Related concepts

* [[axion inflation]]

* [[fuzzy dark matter]]

* [[strong CP problem]]

* [[G2-MSSM]]

## References

### General

The axion as such was originally proposed in 

* {#Weinberg77} [[Steven Weinberg]], _New light boson_, Phys. Rev. Lett. 40:223-6 (1977)

* {#Wilczek78} [[Frank Wilczek]], _Problem of strong P and T invariance in the presence of instantons_, Phys. Rev. Lett. 40:279-82 (1978)

The experimentally viable variant as the "invisible axion" is due to 

* {#DineFischlerSrednicki81} [[Michael Dine]], [[Willy Fischler]], [[Mark Srednicki]], _A simple solution to the strong CP problem with a harmless axion_, Phys. Lett. B 104:199-202 (1981)

The observation that the "invisible axion" is a candidate for [[dark matter]] is due to three groups:

* {#PreskillWiseWilczek83} [[John Preskill]], M. Wise, [[Frank Wilczek]], _Cosmology of the invisible axion_, Phys. Lett. B 120:127-32 (1983)

* {#AbbottSikivie83} L.F. Abbott, P. Sikivie, _A Cosmological Bound on the Invisible Axion_, Phys.Lett. B120:133-36 (1983)

* {#DineFischler83} [[Michael Dine]], [[Willy Fischler]], _The Not So Harmless Axion_, Phys. Lett. B120 :137-141 (1983)

A historical recollection of the development until here is in

* [[Frank Wilczek]], _Birth of axions_ in _This Week's Citation Classic_ (1991) ([pdf](http://www.garfield.library.upenn.edu/classics1991/A1991FE76900001.pdf))

The argument that the [[topological Yang-Mills theory|topological]] [[interaction]] term $\propto a \langle F \wedge F\rangle$ gives the axion field $a$ a vanishing [[vacuum expectation value]] is due to

* {#VafaWitten84} [[Cumrun Vafa]], [[Edward Witten]], _Parity Conservation in Quantum Chromodynamics_, Phys. Rev. Lett. 53, 535 (1984) ([publisher](http://journals.aps.org/prl/abstract/10.1103/PhysRevLett.53.535))

A reformulation of this effect in terms of [[Chern-Simons forms]] is discussed in

* [[Gia Dvali]], _Three-Form Gauging of axion Symmetries and Gravity_ ([arXiv:hep-th/0507215](https://arxiv.org/abs/hep-th/0507215))

Review:

* {#KusterRaffeltBeltran08} Markus Kuster, Georg Raffelt, Berta Beltrán (eds.), _Axions: Theory, cosmology, and Experimental Searches_, Lect.
Notes Phys. 741 (Springer, Berlin Heidelberg 2008) (<a href="https://doi.org/10.1007/978-3-540-73518-2_2">doi:10.1007/978-3-540-73518-2_2</a>)

* Jihn E. Kim, Gianpaolo Carosi, _Axions and the Strong CP Problem_, Rev.Mod.Phys.82:557-602,2010 ([arXiv:0807.3125](https://arxiv.org/abs/0807.3125))

* Masahiro Kawasaki, Kazunori Nakayama, _Axions : Theory and Cosmological Role_, Annual Review of Nuclear and Particle Science Vol.63:1-552   ([arXiv:1301.1123](https://arxiv.org/abs/1301.1123))

* Luca Di Luzio, Maurizio Giannotti, Enrico Nardi, Luca Visinelli, _The landscape of QCD axion models_ ([arXiv:2003.01100](https://arxiv.org/abs/2003.01100))


See also:


* Wikipedia,  _[Axion](http://en.wikipedia.org/wiki/Axion)_


### In string theory
  {#ReferencesInStringTheory}

Discussion of the various ways that axions naturally appear in [[string theory]] is in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))


Specifically for the [[F-theory]] sector of string theory:

* {#Grimm14} Thomas Grimm, _Axion Inflation in F-theory_ ([arXiv:1404.4268](http://arxiv.org/abs/1404.4268))

Specifically open string axions

* [[Gabriele Honecker]], section 4 of _From Type II string theory towards BSM/dark sector physics_, International Journal of Modern Physics A Vol. 31 (2016) 1630050 ([arXiv:1610.00007](https://arxiv.org/abs/1610.00007))


A textbook account of axion [[string phenomenology]] is in

* {#IbanezUranga12} [[Luis Ibáñez]], [[Angel Uranga]], section 16.2 of _[[String Theory and Particle Physics -- An Introduction to String Phenomenology]]_, Cambridge University Press 2012


Discussion of stringy axion [[cosmology]] (such as [[fuzzy dark matter]]) is in 

* {#ADDKM09} Asimina Arvanitaki, Savas Dimopoulos, Sergei Dubovsky, Nemanja Kaloper, John March-Russell, _String Axiverse_, Phys.Rev.D81:123530,2010 ([arXiv:0905.4720](https://arxiv.org/abs/0905.4720))

* {#AcharyaBobkovKumar10} [[Bobby Acharya]], Konstantin Bobkov, [[Piyush Kumar]], _An M Theory Solution to the Strong CP Problem and Constraints on the Axiverse_, JHEP 1011:105, 2010 ([arXiv:1004.5138](https://arxiv.org/abs/1004.5138))

* {#AcharyaKaneKumar12} [[Bobby Acharya]], [[Gordon Kane]], [[Piyush Kumar]], _Compactified String Theories -- Generic Predictions for Particle Physics_, Int. J. Mod. Phys. A, Volume 27 (2012) 1230012 ([arXiv:1204.2795](https://arxiv.org/abs/1204.2795))

### In holographic QCD

Realization in the [[Witten-Sakai-SUgimoto model]] for [[holographic QCD]]:

* Francesco Bigazzi, Alessio Caddeo, Aldo L. Cotrone, Paolo Di Vecchia, Andrea Marzolla, _The Holographic QCD Axion_ ([arXiv:1906.12117](https://arxiv.org/abs/1906.12117))



### Experimental signature

Discussion of [[experiment|experimental]] signatures of and constraints on axion physics:

#### In particle physics
 {#ReferencesExperimentalSignatureInParticlePhysics}

Discussion of [[experiment|experimental]] signatures of and constraints on axion physics from [[particle physics]]:

Specifically contribution of axions to the [[anomalous magnetic moment]] of the [[electron]] and [[muon]] in [[QED]]:

* Yannis Semertzidis, _Magnetic and Electric Dipole Moments in Storage Rings_, chapter 6 of Markus Kuster, Georg Raffelt, Berta Beltrán (eds.), _Axions: Theory, cosmology, and Experimental Searches_, Lect.
Notes Phys. 741 (Springer, Berlin Heidelberg 2008) ([Kuster-Raffelt-Beltran 08](#KusterRaffeltBeltran08), <a href="https://doi.org/10.1007/978-3-540-73518-2_2">doi:10.1007/978-3-540-73518-2_2</a>) 

* Roberta Armillis, Claudio Coriano', Marco Guzzi, Simone Morelli, _Axions and Anomaly-Mediated Interactions: The Green-Schwarz and Wess-Zumino Vertices at Higher Orders and g-2 of the muon_, JHEP 0810:034,2008 ([arXiv:0808.1882](https://arxiv.org/abs/0808.1882))

* W.J. Marciano, A. Masiero, P. Paradisi, M. Passera, _Contributions of axion-like particles to lepton dipole moments_, Phys. Rev. D 94, 115033 (2016) ([arXiv:1607.01022](https://arxiv.org/abs/1607.01022))

* Martin Bauer, Matthias Neubert, Andrea Thamm, _Collider Probes of Axion-Like Particles_, J. High Energ. Phys. (2017) 2017: 44. ([arXiv:1708.00443](https://arxiv.org/abs/1708.00443), <a href="https://doi.org/10.1007/JHEP12(2017)044">doi:10.1007/JHEP12(2017)044</a>)

The basic relevant [[Feynman diagrams]] are worked out here:

* [pdf](http://www-personal.umich.edu/~jbourj/peskin/6-3.pdf)

See also

* [[Frank Wilczek]], _New Ideas in Axion Searches_, talk 2017 ([pdf](http://frankwilczek.com/2017/axion_searches_01.pdf))

For the [ABRACADABRA](http://abracadabra.mit.edu/) (A Broadband/Resonant Approach to Cosmic Axion Detection with an Amplifying B-field Ring Apparatus) approach to axion detection, see

* Jonathan Ouellet, _ABRACADABRA: A Broadband Search for Axion Dark Matter_, talk 2017 ([pdf](https://indico.fnal.gov/event/13702/session/3/contribution/45/material/slides/0.pdf))

For the ADMX experiment:

* {#Avignone18} Frank T. Avignone III, _[Homing in on Axions?](https://physics.aps.org/articles/v11/34)_, APS Physics 11, 34, 2018


#### In astrophysics

Axion signatures in [[gravitational waves]] potentially visible by [[LIGO]]-type [[experiments]] are discussed in 

* {#HJSSZ18} Junwu Huang, Matthew C. Johnson, Laura Sagunski, Mairi Sakellariadou, Jun Zhang, _Prospects for axion searches with Advanced LIGO through binary mergers_ ([arXiv:1807.02133](https://arxiv.org/abs/1807.02133))



#### In cosmology

Discussion of [[experiment|experimental]] signatures of and constraints on axion physics in [[cosmology]], where the axion is a ([[fuzzy dark matter|fuzzy]]) [[dark matter]]-candidate:

* Joseph P. Conlon, M.C. David Marsh, _Searching for a 0.1-1 keV Cosmic Axion Background_ ([arXiv:1305.3603](http://arxiv.org/abs/1305.3603))

  > Primordial decays of [[string theory]] [[moduli stabilization|moduli]] at $z \sim 10^{12}$ naturally generate a [[dark radiation]] Cosmic Axion Background (CAB) with $0.1 - 1 keV$ energies. This CAB can be detected through axion-[[photon]] conversion in astrophysical [[magnetic fields]] to give quasi-thermal excesses in the extreme ultraviolet and soft X-ray bands. Substantial and observable luminosities may be generated even for axion-photon couplings $\ll 10^{-11} GeV^{-1}$. We propose that axion-photon conversion may explain the observed excess emission of soft X-rays from galaxy clusters, and may also contribute to the diffuse unresolved cosmic X-ray background. We list a number of correlated predictions of the scenario. 


Discussion of the axion as a candidate for [[dark matter]] ([[fuzzy dark matter]]) is in

* {#HOTW16} [[Lam Hui]], [[Jeremiah Ostriker]], [[Scott Tremaine]], [[Edward Witten]], _On the hypothesis that cosmological dark matter is composed of ultra-light bosons_, Phys. Rev. D 95, 043541 (2017) ([arXiv:1610.08297](https://arxiv.org/abs/1610.08297))

with its experimental bounds

* Nilanjan Banik, Adam J. Christopherson, Pierre Sikivie, Elisa Maria Todarello, _New astrophysical bounds on ultralight axionlike particles_, Phys. Rev. D 95, 043542 (2017) ([arXiv:1701.04573](https://arxiv.org/abs/1701.04573))

and as a candidate for [[dark energy]]:

* [[Stephon Alexander]], [[Robert Brandenberger]], [[Juerg Froehlich]], _Tracking Dark Energy from Axion-Gauge Field Couplings_ ([arXiv:1601.00057](https://arxiv.org/abs/1601.00057))




[[!redirects axions]]

[[!redirects invisible axion]]
[[!redirects invisible axions]]
