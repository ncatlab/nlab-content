

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Fields and quanta
+--{: .hide}
[[!include fields and quanta - table]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

\begin{imagefromfile}
    "file_name": "VacuumPairCreation.jpg",
    "float": "right",
    "width": 200,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": -20,
        "right": 0, 
        "left": 10
    },
    "caption": "from [Hebenstreit 14](#Hebenstreit14)"
\end{imagefromfile}

What came to be called the _Schwinger effect_ ([Sauter 31](#Sauter31), [Heisenberg-Euler 36](#HeisenbergEuler36), [Schwinger 51](#Schwinger51), [Affleck-Manton 82](#AffleckManton82), [Affleck-Alvarez-Manton 82](#AffleckAlvarezManton82)) is a [[non-perturbative effect]] of [[vacuum polarization]] expected in [[quantum electrodynamics]], where a strong [[electric field]] causes [[electron]]/[[positron]]-[[pairs]] to appear out of the [[vacuum]].  The analogous effect in [[quantum chromodynamics]] would lead to [[deconfinement]] of [[quarks]] in a strong [[electric field]].

While the effect is clearly predicted by established [[theory (physics)|theory]], it has not been observed in [[experiment]] yet, since the required electric field strengths are so large. But recent experiments get close to the required intensities ([Dunne 09](#Dunne09)).



## The field strengths

We consider $(\vec E, \vec B)$ a [[constant function|constant]] [[electromagnetic field]] on 4d [[Minkowski spacetime]] in a given Lorentz frame. 

Write

\[
  \label{ActualFieldStrengths}
  \begin{aligned}
    E 
    & \coloneqq
    \sqrt{
      \vec E \cdot \vec E
    }
    \\
    B 
    & \coloneqq
    \sqrt{
      \vec B \cdot \vec B
    }
  \end{aligned}
\]

for the [[norm]] of these field vectors. These, of course, depend on the choice of Lorentz frame. For the Schwinger effect the relevant [[Lorentz group|Lorentz]] [[invariants]] are

\[
  \label{LorentzInvariantFieldStrenghts}
  \begin{aligned}
    \mathcal{E}
     \;\coloneqq\;
     \sqrt{
      \sqrt{  
        \left(
          \tfrac{1}{2}
            \big(
              \vec E \cdot \vec E
              - 
              \vec B \cdot \vec B
            \big)
        \right)^2
        +
        \big(
          \vec E \cdot \vec B
        \big)^2
      }
      +
      \tfrac{1}{2}
      \big(
        \vec E \cdot \vec E
        - 
        \vec B \cdot \vec B
      \big)
    }
    \\
    \mathcal{B}
     \;\coloneqq\;
    \sqrt{
      \sqrt{  
        \left(
          \tfrac{1}{2}
            \big(
              \vec B \cdot \vec B
              - 
              \vec E \cdot \vec E
            \big)
        \right)^2
        +
        \big(
          \vec E \cdot \vec B
        \big)^2
      }
      +
      \tfrac{1}{2}
      \big(
        \vec B \cdot \vec B
        - 
        \vec E \cdot \vec E
      \big)
    }
  \end{aligned}
\]

(reviewed in [Dunne 04, (1.6)](#Dunne04))

Noticing that if $\vec E \cdot \vec B \neq 0$ then there is a [[Lorentz transformation]] to $(\vec E', \vec B')$ such that the electric field is strictly parallel to the magentic field $\vec E \parallel \vec B$, these invariants are more explicity given as follows:

$$
  \begin{aligned}
  \mathcal{E}
  \; = \;
  \left\{
    \array{
      \sqrt{
        \vec E \cdot \vec E - \vec B \cdot \vec B
      }
      &
      \vert
      &
      \mathrlap{
        \vec E \cdot \vec B = 0
      }
      \\
      E'
      &\vert&
      \mathrlap{
      \vec E \cdot \vec B \neq 0
      \;\;
      \Rightarrow
      \underset{
        {
          Lorentz   
          \atop
          transformation
        }
        \atop
        {
          (\vec E, \vec B) 
          \mapsto 
          (\vec E', \vec B')
        }
      }{\exists}
        \vec E' \parallel \vec B'
      }
    }
  \right.
  \\
  \mathcal{B}
  \; = \;
  \left\{
    \array{
      \sqrt{
        \vec B \cdot \vec B
        - 
        \vec E \cdot \vec E 
      }
      &
      \vert
      &
      \mathrlap{
        \vec E \cdot \vec B = 0
      }
      \\
      B'
      &\vert&
      \mathrlap{
      \vec E \cdot \vec B \neq 0
      \;\;
      \Rightarrow
      \underset{
        {
          Lorentz   
          \atop
          transformation
        }
        \atop
        {
          (\vec E, \vec B) 
          \mapsto 
          (\vec E', \vec B')
        }
      }{\exists}
        \vec E' \parallel \vec B'
      }
    }
  \right.
  \end{aligned}
$$

\linebreak


## The Schwinger effect

### For general field strength at small coupling

Assuming

* **parallel field components:**  $\vec E \cdot \vec B \neq 0$;

and

* **weak coupling**: $e$ small;

the rate of pair creation out of the [[vacuum]] of [[spinor]] [[particles]] of [[electric charge]] $e$ and [[mass]] $m$ is

$$
  \label{SchwingerEffectAtGeneralFieldStrengthForWeakCoupling}
  \Gamma_{
   {
     e\,small
   }
  }
  \;=\;
  \frac
  {
    e^2 \mathcal{E} \mathcal{B}
  }{
    8 \pi^2
  }
  \underoverset
    {n = 1}
    {\infty}
    {\sum}
  \frac{1}{n}
  \coth
  \left(
    \frac{\mathcal{B}}{\mathcal{E}} n \pi
  \right)  
  \exp
  \left(
    - 
    \frac{
      m^2 \pi n
    }{
      e \mathcal{E}
    }
  \right)
$$

For [[electron]]/[[positron]] pair-creation in [[electromagnetism]] this is due to [Nikishov 69](#Nikishov69), [Bunkin-Tugov 70](#BunkinTugov70), reviewed in [Dunne 04, (1.28)](#Dunne04). For [[quark]]/[[antiparticle|ani-]][[quark]] pair creation in [[quantum chromodynamics]] the analogous formula is due to [Suganuma-Tatsumin 91](#SuganumaTatsumin91), [Suganuma-Tatsumi 93](#SuganumaTatsumi93), reviewed in [Hidaka-Iritani-Suganuma 11, (2)](#HidakaIritaniSuganuma11).

In the [[limit of a sequence]] $\mathcal{B} \to 0$, using that

$$
  \underset{
    \underset{
      x \to 0
    }{
      \longrightarrow
    }
  }{\lim}
  \,
  x \coth(x) 
  \;=\;
  x
  \,,
$$

this reduces to

\[
  \label{ForVanishingBFieldAtWeakCoupling}
  \Gamma_{
   {
    {
      \mathcal{B} = 0
    }
   }
   \atop
   {
     e\,small
   }
  }
  \;\coloneqq\;
  \underset{
    \underset{
      B \to 0
    }{
      \longrightarrow
    }
  }{\lim}
  \,
  \Gamma
  \;=\;
  \frac
  {
    e^2 \mathcal{E}^2
  }{
    8 \pi^3
  }
  \underoverset
    {n = 1}
    {\infty}
    {\sum}
  \frac{1}{n^2}
  \exp
  \left(
    - 
    \frac{
      m^2 \pi n
    }{
      e \mathcal{E}
    }
  \right)
\]

This is due to [Schwinger 51](#Schwinger51) (review in [Dunne 04, (1.25)](#Dunne04))


### For small field strength at small coupling

Assuming in addition

* **weak fields:**: $\mathcal{E}$ small compared to $m$

the expression (eq:ForVanishingBFieldAtWeakCoupling) simplifies to

\[
  \label{ForWeakFieldsAndWeakCoupling}
  \Gamma_{
   {
    {
      \mathcal{B} = 0
    }
    \atop
    {
      \mathcal{E}\, small
    }
   }
   \atop
   {
     e\,small
   }
  }
  \;\coloneqq\;
  \frac
  {
    e^2 \mathcal{E}^2
  }{
    8 \pi^3
  }
  \exp
  \left(
    - 
    \frac{
      m^2 \pi
    }{
      e \mathcal{E}
    }
  \right)
\]

For [[electron]]/[[positron]] pair-creation in [[electromagnetism]] this is originally due to [Heisenberg-Euler 36](#HeisenbergEuler36), reviewed in [Dunne 04, (1.10)](#Dunne04). For [[quark]]/[[antiparticle|ani-]][[quark]] pair creation in [[quantum chromodynamics]] the analogous formula is due to [Suganuma-Tatsumin 91](#SuganumaTatsumin91), [Suganuma-Tatsumi 93](#SuganumaTatsumi93), reviewed in [Hidaka-Iritani-Suganuma 11, (3)](#HidakaIritaniSuganuma11).



### For small field strength at strong coupling

For strong coupling $e$ the expression (eq:ForWeakFieldsAndWeakCoupling) get corrected to 

$$
  \Gamma_{
   {
    {
      \mathcal{E}\, small
    }
    \atop
    {
      \mathcal{B} = 0
    }
   }
  }
  \;=\;
  \frac
  {
    e^2 \mathcal{E}^2
  }{
    8 \pi^3
  }
  \exp
  \left(
    - 
    \frac{
      m^2 \pi 
    }{
      e \mathcal{E}
    }
    + 
    \tfrac{1}{4}e^2
  \right)
$$

This was argued in [Affleck-Alvarez-Manton 82](#AffleckAlvarezManton82).





## Properties



### Schwinger limit -- Critical electric field strength 
 {#CriticalFieldStrength}

From (eq:SchwingerEffectAtGeneralFieldStrengthForWeakCoupling) 
one deduces a critical [[electric field|electric]] [[field strength]] $\mathcal{E}_{crit}$ which sets the [[scale]] beyond which the [[vacuum polarization]] due to the [[Schwinger effect]] counteracts the ambient electric field and/or leads to [[vacuum decay]]. 

As a [[Lorentz group|Lorentz]] [[invariant]] (eq:LorentzInvariantFieldStrenghts) this _[[Schwinger limit]]_ for the [[electric field|electric]] [[field strength]] is:

\[
  \label{CriticalFieldStrengthLorentzInvariant}
  \mathcal{E}_{crit}  
  \;\coloneqq\;
  \frac{
    m^2 c^3
  }{
    e \hbar
  }  
\]

([Dunne 04, (1.3)](#Dunne04), [Martin 07, (40)](#Martin07))

Here 

* $e$ is the [[charge]] of the [[charged particles]],

* $m$ is the [[mass]] of the [[charged particles]],

* $c$ is the [[speed of light]],

* $\hbar$ is [[Planck's constant]].

This is such that the corresponding [[Lorentz force]] 

$$
  F_{crit}
  \; \coloneqq \;
  e
  \, 
  \mathcal{E}_{crit}
$$

acting over the [[Compton wavelength]] $\lambda_{Comp} \;\coloneqq\; \frac{\hbar }{m c}$ equals the [[rest energy]] $m c^2$ of the given [[charged particle]]:

$$
  \begin{aligned}
    &
    F_{crit} \lambda_{Comp}
    \; = \;
    m c^2
    \\
    \Leftrightarrow
    \;\;\;
    &
    \mathcal{E}_{crit}
    \; = \;
    \frac{
      m c^2
    }{
      e \lambda_{Comp}
    }
  \end{aligned}
$$


Expressing (eq:CriticalFieldStrengthLorentzInvariant) in terms of the corresponding critical value $E_{crit}$ of the actual [[electric field|electric]] [[field strength]] (eq:ActualFieldStrengths) in the given Lorentz frame yields ([Hashimoto-Oka-Sonoda 14b, (2.17)](#HashimotoOkaSonoda14b), [check](https://www.wolframalpha.com/input/?i=solve+for+e+%3A+c++%3D+Sqrt%5B+Sqrt%5B+%281%2F4%29*%28+e%5E2+-+b%5E2+%29%5E2+%2B+%28p%5E2%29*%28e%5E2%29+%5D+%2B+%281%2F2%29*+%28e%5E2+-+b%5E2%29++%5D+)):

$$
  \mathcal{E}(E_{crit}, B)
  \;=\;
  \mathcal{E}_{crit}
  \phantom{AA}
   \Leftrightarrow
  \phantom{AA}
  E_{crit}
  \;=\;
  \mathcal{E}_{crit}
  \sqrt{
    \frac{
      \mathcal{E}_{crit}^2 + B^2
    }
    {
      \mathcal{E}_{crit}^2 + B_{\parallel}^2
    }
  }
$$

This happens to coincide with the critical field strength of the [[DBI-action]], see [there](DBI-action#CriticalFieldStrength).


### In holographic QCD
 {#InHolographicQCD}

It has been argued that in terms of [[intersecting D-brane models]] the Schwinger effect is what is reflected by the non-linearities in the [[DBI-action]] on probe branes in [[AdS/CFT]] ([Semenoff-Zarembo 11](#SemenoffZarembo11)) and on [[flavor branes]] in [[holographic QCD]] ([Hashimoto-Oka 13](#HashimotoOka13), [Hashimoto-Oka-Sonoda 14a](#HashimotoOkaSonoda14a), [Hashimoto-Oka-Sonoda 14b](#HashimotoOkaSonoda14b)). This is now referred to as the _holographic Schwinger effect_.


## References

### In quantum electrodynamics

Discussion of the [[Schwinger effect]] in [[quantum electrodynamics]]:

The original theoretical prediction:

* {#Sauter31} F. Sauter, _Über das Verhalten eines Elektrons im homogenen elektrischen Feld nach der relativistischen Theorie Diracs_, Z. Physik 69, 742–764 (1931) ([doi:10.1007/BF01339461](https://doi.org/10.1007/BF01339461)) 


* {#HeisenbergEuler36} [[Werner Heisenberg]], [[Hans Euler]],  _Folgerungen aus der Diracschen Theorie des Positrons_, Z. Physik 98, 714–732 (1936) ([doi:10.1007/BF01343663](https://doi.org/10.1007/BF01343663))

* {#Schwinger51} [[Julian Schwinger]], _On Gauge Invariance and Vacuum Polarization_, Phys. Rev. 82, 664 (1951) ([doi:10.1103/PhysRev.82.664](https://doi.org/10.1103/PhysRev.82.664))

* {#Nikishov69} A. I. Nikishov, _Pair production by a constant external field_, Zh. Eksp. Teor. Fiz. 57 (1969) 1210-1216 ([spire:59436](http://inspirehep.net/record/59436))

* {#BunkinTugov70} F. V. Bunkin, I. I. Tugov, _Possibility of creating electron-positron pairs in avacuum by the focusing of laser radiation_, Sov. Phys. Dokl.14 (1970), 678


* {#AffleckManton82} [[Ian Affleck]], [[Nicholas Manton]], _Monopole pair production in a magnetic field_, Nuclear Physics B Volume 194, Issue 1, (1982) Pages 38-64 (<a href="https://doi.org/10.1016/0550-3213(82)90511-9">doi:10.1016/0550-3213(82)90511-9</a>

* {#AffleckAlvarezManton82} [[Ian Affleck]], [[Orlando Alvarez]], [[Nicholas Manton]], _Pair production at strong coupling in weak external fields_, Nuclear Physics B Volume 197, Issue 3 (1982) Pages 509-519 (<a href="https://doi.org/10.1016/0550-3213(82)90455-2">doi:10.1016/0550-3213(82)90455-2</a>)

Discussion via [[worldline formalism]]:

* [[Gerald Dunne]], [[Christian Schubert]], _Worldline Instantons and Pair Production in Inhomogeneous Fields_, Phys. Rev. D72 (2005) 105004 ([arXiv:hep-th/0507174](https://arxiv.org/abs/hep-th/0507174))


Review:

* Walter Dittrich, Holger Gies, _Probing the Quantum Vacuum --
Perturbative Effective Action Approach in Quantum Electrodynamics and its Application_, Springer Tracts in Modern Physics, Vol. 166 ([ISBN 978-3-540-45585-1](https://www.springer.com/gp/book/9783540674283))

* {#Dunne04} [[Gerald Dunne]], _Heisenberg-Euler Effective Lagrangians: Basics and Extensions_, in:  [[Misha Shifman]], [[Arkady Vainshtein]], [[John Wheater]] (eds.), _[[From Fields to Strings -- Circumnavigating Theoretical Physics]]_, pp. 445-522, World Scientific 2005 ([arXiv:hep-th/0406216](https://arxiv.org/abs/hep-th/0406216), [doi:10.1142/9789812775344_0014](https://doi.org/10.1142/9789812775344_0014))


* [[Gerald Dunne]], _The Heisenberg-Euler Effective Action: 75 years on_, Int. J. Mod. Phys. A27 (2012) 1260004 ([arXiv:1202.1557](https://arxiv.org/abs/1202.1557))


* Francois Gelis, Naoto Tanji, _Schwinger mechanism revisited_, Progress in Particle and Nuclear Physics Volume 87, March 2016, Pages 1-49 ([arXiv:1510.05451](https://arxiv.org/abs/1510.05451))

See also

* Wikipedia, _[Schwinger effect](https://en.wikipedia.org/wiki/Schwinger_effect)_

* Wikipedia, _[Schwinger limit](https://en.wikipedia.org/wiki/Schwinger_limit)_



Discussion of [[experiments]] that could/should see the [[Schwinger effect]]:

* {#Dunne09} [[Gerald Dunne]], _New Strong-Field QED Effects at ELI: Nonperturbative Vacuum Pair Production_, Eur. Phys. J. D55:327-340, 2009 ([arXiv:0812.3163](https://arxiv.org/abs/0812.3163))

* Hidetoshi Taya, _Mutual assistance between the Schwinger mechanism and the dynamical Casimir effect_ ([arXiv:2003.12061](https://arxiv.org/abs/2003.12061))

* {#Hebenstreit14} Florian Hebenstreit, _A space-time resolved view  of the Schwinger effect_, Frontiers of intense laser physics – KITP 2014 ([[HebenstreitSchwingerEffect2014.pdf:file]])

and in relation to [[magnetic monopoles]]:

* B. Acharya et al., *First experimental search for production of magnetic monopoles via the Schwinger mechanism* ([arXiv:2106.11933](https://arxiv.org/abs/2106.11933))


Discussion in [[cosmic inflation|inflationary]] [[cosmology]]:

* {#Martin07} Jerome Martin, _Inflationary Perturbations: the Cosmological Schwinger Effect_, Lect. Notes Phys. 738:193-241, 2008 ([arXiv:0704.3540](https://arxiv.org/abs/0704.3540), [doi:10.1007/978-3-540-74353-8_6](https://doi.org/10.1007/978-3-540-74353-8_6))

See also:

* Shintaro Takayoshi, Jianda Wu, Takashi Oka, _Twisted Schwinger Effect: Pair Creation in Rotating Fields_ ([arXiv:2005.01755](https://arxiv.org/abs/2005.01755))


* Prasant Samantray, Suprit Singh, _Schwinger Effect in Compact Space_ ([arXiv:2010.13453](https://arxiv.org/abs/2010.13453))







### In quantum chromodynamics

Discussion of the [[Schwinger effect]] in [[quantum chromodynamics]]:

* Asim Yildiz, Paul H. Cox, _Vacuum Behavior in Quantum Chromodynamics_, Phys. Rev. D21 (1980) 1095 ([spire:7860](http://inspirehep.net/record/7860))

* M. Claudson, Asim Yildiz, Paul H. Cox, _Vacuum behavior in quantum chromodynamics. II_, Phys. Rev. D 22, 2022 (1980) ([doi:10.1103/PhysRevD.22.2022](https://doi.org/10.1103/PhysRevD.22.2022))


* Paul H. Cox, Asim Yildiz, _$q \bar q$ pair creation: A field-theory approach_, Phys. Rev. D 32, 819 (1985) ([doi:10.1103/PhysRevD.32.819](https://doi.org/10.1103/PhysRevD.32.819))

* {#SuganumaTatsumin91} Hideo Suganuma, Toshitaka Tatsumim, _On the behavior of symmetry and phase transitions in a strong electromagnetic field_, Annals of Physics Volume 208, Issue 2, June 1991, Pages 470-508 (<a href="https://doi.org/10.1016/0003-4916(91)90304-Q">doi:10.1016/0003-4916(91)90304-Q</a>)

* {#SuganumaTatsumi93} Hideo Suganuma, Toshitaka Tatsumi, _Chiral Symmetry and Quark-Antiquark Pair Creation in a Strong Color-Electromagnetic Field_, Progress of Theoretical Physics, Volume 90, Issue 2, August 1993, Pages 379–404 ([spire:318092](http://inspirehep.net/record/318092), [doi:10.1143/ptp/90.2.379](https://doi.org/10.1143/ptp/90.2.379))

* Naoto Tanji, _Dynamical view of pair creation in uniform electric and magnetic fields_, Annals Phys. 324:1691-1736, 2009 ([arXiv:0810.4429](https://arxiv.org/abs/0810.4429))

* {#HidakaIritaniSuganuma11} Yoshimasa Hidaka, Takumi Iritani, Hideo Suganuma, _Fast Vacuum Decay into Quark Pairs in Strong Color Electric and Magnetic Fields_, AIP Conference Proceedings 1388, 516 (2011) ([arXiv:1103.3097](https://arxiv.org/abs/1103.3097), [doi:10.1063/1.3647442]( https://doi.org/10.1063/1.3647442))


* Sho Ozaki, Takashi Arai, Koichi Hattori, Kazunori Itakura, _Euler-Heisenberg-Weiss action for QCD+QED_, Phys. Rev. D 92, 016002 (2015) ([arXiv:1504.07532](https://arxiv.org/abs/1504.07532))

* Koichi Hattori, Kazunori Itakura, Sho Ozaki, _Note on all-order Landau-level structures of the Heisenberg-Euler effective actions for QED and QCD_ ([arXiv:2001.06131](https://arxiv.org/abs/2001.06131))

* Patrick Copinger, Pablo Morales, _Schwinger Pair Production in $SL(2,\mathbb{C})$  Topologically Non-Trivial Fields via Non-Abelian Worldline Instantons_ ([arXiv:2011.12526](https://arxiv.org/abs/2011.12526))



In [[quantum hadrodynamics]]:


* William R. Tavares, Sidney S. Avancini, _Schwinger mechanism in the $SU(3)$ Nambu--Jona-Lasinio model with an electric field_, Phys. Rev. D 97, 094001 (2018) ([arXiv:1801.10566](https://arxiv.org/abs/1801.10566))





[[!include holographic Schwinger effect -- references]]



[[!redirects Schwinger effects]]

[[!redirects holographic Schwinger effect]]
[[!redirects holographic Schwinger effects]]

