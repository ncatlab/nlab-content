

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

In [[quantum electrodynamics]] and [[quantum chromodynamics]] the _Schwinger limit_ is a maximal [[scale]] 

$$
  \;\approx\;
  \frac{
    m^2 c^3
  }{
    e \hbar
  }  
$$

of the [[field strength]] of an [[electric field|electric]] [[background field]] beyond which the [[vacuum polarization]] caused by pair creation [[electrons]]/[[positrons]] or [[quarks]]/[[antiparticle|anti]]-[[quarks]] (of [[charge]] $e$ and [[mass]] $m$)  out of the [[vacuum]], via the [[Schwinger effect]], becomes sizeable, leading to non-linearities and/or [[vacuum decay]].

From the perspective of [[geometric engineering of QFT|geometric engineering]] of [[QCD]] in [[intersecting D-brane models]] ([[holographic QCD]]) the Schwinger limit corresponds to the limiting field strength in the [[DBI-action]] of the [[Chan-Paton gauge field]] on [[D-branes]] ("[[holographic Schwinger effect]]").

The [[Schwinger effect]] and its resulting [[Schwinger limit]] are securely prediuted by established [[quantum field theory]], but have not been observed in [[experiment]] yet. However, recent experiments are getting very close and upcoming experiments might see the effect.

## Details

From the rate 

$$
  \label{SchwingerEffectAtGeneralFieldStrengthForWeakCoupling}
  \Gamma 
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


([here](Schwinger+effect#eq:SchwingerEffectAtGeneralFieldStrengthForWeakCoupling)) of particle pair creation via the [[Schwinger effect]]  one deduces a critical [[electric field|electric]] [[field strength]] $\mathcal{E}_{crit}$ which sets the [[scale]] beyond which the [[vacuum polarization]] due to the [[Schwinger effect]] counteracts the ambient electric field and/or leads to [[vacuum decay]]. 

As a [[Lorentz group|Lorentz]] [[invariant]] ([here](Schwinger+effect#eq:LorentzInvariantFieldStrenghts))
 this _[[Schwinger limit]]_ for the [[electric field|electric]] [[field strength]] is:

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

## Properties

### Relation to DBI-limit

Expressing (eq:CriticalFieldStrengthLorentzInvariant) in terms of the corresponding critical value $E_{crit}$ of the actual [[electric field|electric]] [[field strength]] ([here](Schwinger+effect#eq:ActualFieldStrengths)) in the given Lorentz frame yields ([Hashimoto-Oka-Sonoda 14b, (2.17)](#HashimotoOkaSonoda14b), [check](https://www.wolframalpha.com/input/?i=solve+for+e+%3A+c++%3D+Sqrt%5B+Sqrt%5B+%281%2F4%29*%28+e%5E2+-+b%5E2+%29%5E2+%2B+%28p%5E2%29*%28e%5E2%29+%5D+%2B+%281%2F2%29*+%28e%5E2+-+b%5E2%29++%5D+)):

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

## Related concepts

[[!include fundamental scales -- contents]]


## References

### General

Review:

* {#Dunne04} [[Gerald Dunne]], _Heisenberg-Euler Effective Lagrangians: Basics and Extensions_, in:  [[Misha Shifman]], [[Arkady Vainshtein]], [[John Wheater]] (eds.), _[[From Fields to Strings -- Circumnavigating Theoretical Physics]]_, pp. 445-522, World Scientific 2005 ([arXiv:hep-th/0406216](https://arxiv.org/abs/hep-th/0406216), [doi:10.1142/9789812775344_0014](https://doi.org/10.1142/9789812775344_0014))

* {#Martin07} Jerome Martin, around (40) in: _Inflationary Perturbations: the Cosmological Schwinger Effect_, Lect. Notes Phys. 738:193-241, 2008 ([arXiv:0704.3540](https://arxiv.org/abs/0704.3540), [doi:10.1007/978-3-540-74353-8_6](https://doi.org/10.1007/978-3-540-74353-8_6))

For more see the references at _[[Schwinger effect]]_.

See also

* Wikipedia, _[Schwinger limit](https://en.wikipedia.org/wiki/Schwinger_limit)_

### Experimental realization

Discussion of [[experiments]] that could/should see physics at the [[Schwinger limit]]:

* {#Dunne09} [[Gerald Dunne]], _New Strong-Field QED Effects at ELI: Nonperturbative Vacuum Pair Production_, Eur. Phys. J. D55:327-340, 2009 ([arXiv:0812.3163](https://arxiv.org/abs/0812.3163))

* Hidetoshi Taya, _Mutual assistance between the Schwinger mechanism and the dynamical Casimir effect_ ([arXiv:2003.12061](https://arxiv.org/abs/2003.12061))

* Florian Hebenstreit, _A space-time resolved view  of the Schwinger effect_, Frontiers of intense laser physics – KITP 2014 ([[HebenstreitSchwingerEffect2014.pdf:file]])


[[!include holographic Schwinger effect -- references]]


