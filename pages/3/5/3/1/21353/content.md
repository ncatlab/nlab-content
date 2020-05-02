
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

In [[quantum hadrodynamics]] a _Dalitz decay_ is the [[decay]] of an electrically neutral [[pseudoscalar meson]] into a [[dilepton]] pair and a either a [[photon]] (this is the original sense of [Dalitz 51](#Dalitz51), a [[radiative leptonic decay]]) or a [[vector meson]] (a [[semileptonic decay]]).

### Radiative leptonic Dalitz decay
 {#RadiativeLeptonicDalitzDecay}

In [[quantum hadrodynamics]] a _Dalitz decay_ in the original sense ([Dalitz 51](#Dalitz51)) is the [[radiative leptonic decay]] of an [[electromagnetism|electromagnetically]] neutral [[pseudoscalar meson]] $P$ into a [[photon]] and a [[dilepton]]:

$$
  P \,\to\, \gamma \,+\, l^+ \,+\, l^- 
  \,.
$$

The dominant contribution to this decay is by a purely radiative decay $P \to \gamma+ \gamma$ followed by an [[electron-photon interaction]] $\gamma + e^+ + e^-$ ("Dalitz pair") of one of the two resulting photons (which thus participates as a [[virtual particle|virtual]] [[photon]] $\gamma^\ast$ with [[spacelike]] [[wave vector]] $q^2 = m^2_{e^+ e^-}$):


\begin{imagefromfile}
  "file_name": "DalitzDecayPseudoscalarMesonToPhoton.jpg",
  "width": 320,
  "caption": "from [Kunkel 12, p. 9](#Kunkel12)",
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  } 
\end{imagefromfile}

The original and archetypical example is the [[decay]] of the neutral [[pion]] into an [[electron]]/[[positron]]-[[pair]] and a [[photon]]:

$$
  \pi^0 \,\to\, e^+ \,+\, e^- \,+\, \gamma
  \,.
$$


The [[Feynman amplitude]] of the process is proportional to

$$
  \epsilon^{\mu_1 \mu_2 \nu \kappa}
  \underset{ 
    photon 
  }{
    \underbrace{
      q_{\mu_1} 
      \epsilon_{\mu_2}
    }
  }
  \underset{ 
    {scalar} 
    \atop 
    {meson} 
  }{
    \underbrace{
      p_\nu
    }
  }
  \underset{
    dilepton
  }{
    \underbrace{
      \overline{L} \!\cdot\! \gamma_\kappa  \!\cdot\! L
    }
  }
  \underset{
    {virtual} 
    \atop
    {photon}
  }{
    \underbrace{
      \tfrac{1}{(p_1 + p_2)^2}
    }
  }
$$

where 

* $\epsilon^{\mu_1 \mu_2 \nu \kappa}$ is the [[Levi-Civita symbol]],

* $q_{\mu_1}$ is the [[wave vector]] and $\epsilon_{\mu_2}$ the [[polarization]] of the [[photon]],

* $p_\mu$ is the [[momentum]] of the (pseudo-)[[scalar meson]],

* $\overline{L} \!\cdot\! \gamma_\kappa  \!\cdot\! L$ is the [[lepton current]]

* $p_1, p_2$ are the momenta of the two [[leptons]], hence $(p_1 + p_2)$ is that of the [[virtual particle|virtual]] [[photon]] mediating the decay.

(see [Yia-Sang 09, (9)](#YiaSang09) (symbol definition on p. 12), also e.g. [KKN 02, p. 2](#KKN02), [KKN06, p. 6](#KKN06) ).


### Semileptonic Dalitz decay

More generally, one speaks of (generalized) Dalitz decays for the analogous process as [above](#RadiativeLeptonicDalitzDecay) with the [[photon]] replaced by some [[vector meson]], hence for [[semileptonic decays]] $A \to B + l^+ + l^-$ for $A$ and $B$ a [[pseudoscalar meson]] and [[vector meson]], respectively, with dominant decay mode given by this [[Feynman diagram]]:

\begin{imagefromfile}
  "file_name": "DalitzDecayPseudoscalarMesonToVectorMeson.jpg",
  "width": 320,
  "caption": "from [Kunkel 12, p. 9](#Kunkel12)",
  "margin": {
    "top": 0,
    "right": 10,
    "bottom": 10,
    "left": 0,
    "unit": "px"
  } 
\end{imagefromfile}

The [[Feynman amplitude]] of the process is, analogous to before, proportional to

$$
  \epsilon^{\mu_1 \mu_2 \nu \kappa}
  \underset{ 
    {vector}
    \atop
    {meson}
  }{
    \underbrace{
      q_{\mu_1} 
      \epsilon_{\mu_2}
    }
  }
  \underset{ 
    {scalar} 
    \atop 
    {meson} 
  }{
    \underbrace{
      p_\nu
    }
  }
  \underset{
    dilepton
  }{
    \underbrace{
      \overline{L} \!\cdot\! \gamma_\kappa  \!\cdot\! L
    }
  }
  \underset{
    {virtual} 
    \atop
    {photon}
  }{
    \underbrace{
      \tfrac{1}{(p_1 + p_2)^2}
    }
  }
$$

where 

* $\epsilon^{\mu_1 \mu_2 \nu \kappa}$ is the [[Levi-Civita symbol]],

* $q_{\mu_1}$ is the [[wave vector]] and $\epsilon_{\mu_2}$ the [[polarization]] of the [[vector meson]],

* $p_\mu$ is the [[momentum]] of the (pseudo-)[[scalar meson]],

* $\overline{L} \!\cdot\! \gamma_\kappa  \!\cdot\! L$ is the [[lepton current]]

* $p_1, p_2$ are the momenta of the two [[leptons]], hence $(p_1 + p_2)$ is that of the [[virtual particle|virtual]] [[photon]] mediating the decay.

(e.g. [Wachs 00, (2.60)](#Wachs00),  [GLMY 19, (2)](#GLMY19))


## References

The original article:

* {#Dalitz51} [[Richard Dalitz]], _On an alternative decay process for the neutral $\pi$-meson_, Proceedings of the Physical Society. Section A 64 (7), 667, 1951 ([doi:10.1088/0370-1298/64/7/115](https://doi.org/10.1088/0370-1298/64/7/115))

Survey:

* {#Kunkel12} M. Kunkel, _Dalitz Decays of Pseudo-Scalar Mesons_, talk at [Light Meson Decays Workshop August 5, 2012](https://www.jlab.org/conferences/lmd2012/) ([[KunkelDalitzDecay.pdf:file]])

Further discussion of the Dalitz decay of [[pions]]:

* {#KKN02} Karol Kampf, Marc Knecht, Jiri Novotny, _Some aspects of Dalitz decay $\pi^0 \to e^+ e^- \gamma$_,  presented at Int. Conf. Hadron Structure '02, September 2002, Slovakia ([arXiv:hep-ph/0212243](https://arxiv.org/abs/hep-ph/0212243))

* {#KKN06} Karol Kampf, Marc Knecht, Jiri Novotny, _The Dalitz decay $\pi^0 \to e^+ e^- \gamma$ revisited_, Eur. Phys. J. C46:191-217, 2006 ([arXiv:hep-ph/0510021](https://arxiv.org/abs/hep-ph/0510021))

* Esther Weil, Gernot Eichmann, Christian S. Fischer, Richard Williams, section III.A of: _Electromagnetic decays of the neutral pion_, Phys. Rev. D 96, 014021 (2017) ([arXiv:1704.06046](https://arxiv.org/abs/1704.06046))

Dalitz decay of/into [[omega-mesons]]:

* {#Wachs00} Mirko Wachs, _Die Selbstenergie des Omega-Mesons_, 2000 ([epda:000050](http://elib.tu-darmstadt.de/diss/000050))

Of [[pions]] and [[eta-mesons]]:

* Sergi González-Solís, _Single and double Dalitz decays of $\pi^0$, $\eta$ and $\eta'$ mesons_, Nuclear and Particle Physics Proceedings Volumes 258–259, January–February 2015, Pages 94-97 ([doi:10.1016/j.nuclphysbps.2015.01.021](https://doi.org/10.1016/j.nuclphysbps.2015.01.021))



Discussion of Dalitz decay of [[quarkonium]]:

* {#YiaSang09} Yu Jia, Wen-Long Sang, _Observation prospects of leptonic and Dalitz decays of pseudoscalar quarkonia_, JHEP 0910:090, 2009 ([arXiv:0906.4782](https://arxiv.org/abs/0906.4782))

Of [[charmonium]]:

* _Study of the Dalitz decay $J/\psi \to e^+e^- \eta$_, Phys. Rev. D 99, 012006 (2019) ([arXiv:1810.03091](https://arxiv.org/abs/1810.03091))

Of [[upsilon-mesons]]:

* {#GLMY19} Li-Min Gu, Hai-Bo Li, Xin-Xin Ma, Mao-Zhi Yang, _Study of the electromagnetic Dalitz decays $\psi(\Upsilon) \to \eta_c(\eta_b) l^+ l^-$_, Phys. Rev. D 100, 016018 (2019) ([arXiv:1904.06085](https://arxiv.org/abs/1904.06085))




[[!redirects Dalitz decays]]




  

