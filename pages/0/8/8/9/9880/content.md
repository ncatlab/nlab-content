
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

An effect in [[non-perturbative quantum field theory]] that cannot be seen in [[perturbative quantum field theory]] is called a _non-perturbative effect_.

More in detail, [[theory (physics)|theories]] with [[instantons]] [[field (physics)|field]] configurations (such as in [[Yang-Mills theory]], hence in [[QCD]] and [[QED]]) or [[branes]] (such as in [[string theory]]), etc., are expected to have [[observables]] which as [[functions]] of the [[coupling constant]] $g$ are [[transseries]] of the form

\[
  \label{TypicalTransseries}
  Z(g)
  = 
  \sum_n a_n g^n
  + 
  e^{-A/g}
  \sum_n a_n^{(1)} g^n
  +
  e^{-B/g^2}
  \sum_n b_n^{(1)} g^n
  \,,
\]

where the first sum is the [[Feynman perturbation series]] itself and where the terms with a [[analytic function|non-analytic]] dependence of the form $\exp(-A/g)$ or $\exp(-A/g^2)$ are the contributions of the [[instantons]]. Since all the [[derivatives]] of the functions $g \mapsto e^{-1/g}$ or $g \mapsto e^{-1/g^2}$ vanish at [[coupling constant]] $g = 0$, the [[Taylor series]] of this part of the observable does not appear in [[perturbative QFT]], even though it is present. Therefore this is called a _non-perturbative effect_.

Related is _[[resurgence theory]]_. See also at _[perturbation theory -- Divergence/convergence](perturbation+theory#DivergenceConvergence)_ for more.

## Examples


### Schwinger effect

* [[Schwinger effect]]

### Confinement and the mass gap

A central example of a non-perturbative effect is [[confinement]] (hence the "[[mass gap problem]]") in [[Yang-Mills theory]] at low [[temperature]]. Perturbation theory is not suited to explain this (e.g [Espiru 94, section 7](http://arxiv.org/abs/hep-ph/9410287)).

### Quark-gluon plasma

At the other extreme of high [[temperature]] QCD, also the [[quark-gluon plasma]], while now [[confinement|deconfined]] is thought to be strongly coupled.

### Hadronic physics in flavour and $g-2$ anomalies
 {#HadronicPhysics}

Non-perturbative effects in [[hadron]]-physics affects the
discussion of possible beyond-[[standard model of particle physics|standard model]] physics as seen in 

1. [[flavour anomalies]] ([Nierste 18, 26/59](#Nierste18))

1. [[muon anomalous magnetic moment]] ([Jegerlehner 18b, section 2](#Jegerlehner18b))



### Worldsheet and brane instantons in string/M-theory
 {#WorldsheetAndBraneInstantons}


Consider the [[M-theory]] [[scales]]

* $\ell_P$, the [[Planck length]] in 11-dimensions;

* $R_{10}$ the [[length]] (circumference) of the $S^1_{10}$ [[circle]] [[fiber]] for [[KK-compactification]] to 10 dimensions

and the [[string theory]] [[scales]]

* $\ell_s$, the [[string length scale]];

* $g_{s}$, the [[string coupling constant]] of [[perturbative string theory]].


Then under the [[duality between M-theory and type IIA string theory]] these scales are related as follows:

$$
  \ell_P \;=\; g_{st}^{1/3} \ell_s
  \,,
  \phantom{AAA}
  R_{10} \;=\; g_{st} \ell_s
$$

equivalently

$$
  \ell_s \;=\; R_{10}/ g_{st}
  \,,
  \phantom{AAA}
  \ell_P \;=\; g_{st}^{-2/3} R_{10}
$$

equivalently

$$
  g_{st} \;=\; (R_{10}/\ell_P)^{3/2}
  \,,
  \phantom{AAA}
  \ell_s \;=\; \ell_P (R_{10}/\ell_P)^{-1/2}
  \,.
$$

Hence a [[membrane instanton]], which on a 3-[[cycle]] $C_3$ gives a contribution

$$
  \exp\left(
    - \frac{ vol(C_3) }{ \ell^3_P }
  \right)
$$

becomes 

1. if the cycle [[wrapped brane|wraps]], $C_3 = C_2 \cup S^1_{10}$, a [[worldsheet instanton]]

   $$
     \exp\left( - \frac{ vol(C_3) }{ \ell_P^3 }  \right) 
     \;=\; 
     \exp\left( - \frac{ R_{10} vol(C_2) }{ g_{st} \ell_s^3 }  \right)
     \;=\;
     \exp\left( - \frac{ vol(C_2) }{ \ell_s^2 }  \right)
   $$

1. the cycle does not [[wrapped brane|wrap]], a spacetime instanton contribution, specifically a [[D2-brane instanton]]

   $$
     \exp\left( - \frac{ vol(C_3) }{ \ell_P^3 }  \right)
     \;=\;
     \exp\left( - \frac{ vol(C_3)/\ell_s^3 }{ g_{st} }  \right)
   $$
   
   
(This unification of the two different [[non-perturbative effects]] in [[perturbative string theory]]
([[worldsheet instantons]] and spacetime [[instantons]]), to a single type of effect ([[membrane instanton]])
 in [[M-theory]] was maybe first made explicit in [Becker-Becker-Strominger 95](#BeckerBeckerStrominger95). Brief review includes [Marino 15, sections 1.2 and 1.3](#Marino15)).


## Related concepts

* [[transseries]], [[resurgence theory]]

* [[fiber bundles in physics]]

* [[instanton]], [[brane]], [[renormalon]]

  * [[membrane instanton]]

* [[lattice gauge theory]]

* [perturbation theory -- convergence/divergence](perturbation+theory#DivergenceConvergence)

* [[higher curvature correction]]

* [[interacting vacuum]]

* [[proton spin crisis]]

* [[AdS/CFT correspondence]], [[AdS/QCD correspondence]]

* [string theory FAQ -- Isn't it fatal that the string perturbation series does not converge?](string+theory+FAQ#NonConvergenceOfPerturbationSeries)


## References

### In field theory

* {#BakulevShirkov10} Alexander P. Bakulev, [[Dmitry Shirkov]], _Inevitability and Importance of Non-Perturbative Elements in Quantum Field Theory_, Proceedings of the 6th Mathematical Physics Meeting, Sept. 14--23, 2010, Belgrade, Serbia, pp. 27--54 ([arXiv:1102.2380](https://arxiv.org/abs/1102.2380), [ISBN 978-86-82441-30-4](http://www.proceedings.com/22646.html), [book webpage](http://www.mphys6.ipb.ac.rs/proceedings6.htm), [book TOC pdf](http://toc.proceedings.com/22646webtoc.pdf)) 


Genral introduction and toy examples (e.g. the anharmonic oscillator) are given in 

* [Mariño 12, section 2, section 3.1](#Marino12)

Discussion for [[phi^4 theory]] is in

* {#Serone18} Marco Serone, from 2:46 on in _A look at $\phi^4_2$ using perturbation theory_, January 2018 ([recording](https://www.youtube.com/watch?v=J4nxvY1rOhI))

Discussion for [[QCD]] includes

* [[Marcos Mariño]], _Instantons and Large $N$ -- An introduction to non-perturbative methods in QFT_ ([pdf](http://laces.web.cern.ch/laces/LACES10/notes/instlargen.pdf))

and in ([[super Yang-Mills theory|super]]-)[[Yang-Mills theory]] and [[string theory]] is in

* {#Marino12} [[Marcos Mariño]], _Lectures on non-perturbative effects in large N gauge theories, matrix models and strings_, Fortschritte der Physik 62.5‐6 (2014): 455-540 ([arXiv:1206.6272](http://arxiv.org/abs/1206.6272))

* {#Marino15} [[Marcos Mariño]], _Non-perturbative effects in string theory and AdS/CFT_, [Spring School on Superstring Theory and Related Topics 2015](http://indico.ictp.it/event/a14251/)  ([[MarinoNonPerturbative.pdf:file]], [pdf](http://indico.ictp.it/event/a14251/session/89/contribution/401/material/0/0.pdf), [recording](https://youtu.be/5hw6l-JSpc4?list=PLzYFBWfshN8eqXZFYg2jBZSii7lHaeyXJ))

### In phenomeloogy:

In [[flavour anomalies]]:

* {#Nierste18} Ulrich Nierste, _Flavour Anomalies: Phenomenology and BSM Interpretations_, 2018 ([pdf](https://indico.desy.de/indico/event/18498/session/5/contribution/52/material/slides/0.pdf))

* {#Jegerlehner18b} [[Fred Jegerlehner]], _The Role of Mesons in Muon $g-2$_ ([arXiv:1809.07413](https://arxiv.org/abs/1809.07413))

### In cosmology

In [[cosmology]]:


* Anna Ijjas, Frans Pretorius, [[Paul Steinhardt]], _Stability and the gauge problem in non-perturbative cosmology_,  Journal of Cosmology and Astroparticle Physics, Volume 2019, January 2019 ([arXiv:1809.07010](https://arxiv.org/abs/1809.07010), [doi:10.1088/1475-7516/2019/01/015](https://iopscience.iop.org/article/10.1088/1475-7516/2019/01/015))



### In string theory

The form of the contribution of non-perturbative effects in [[string theory]] was originally observed in 

* [[Stephen Shenker]], _The Strength of nonperturbative effects in string theory_, presented at the Cargese Workshop on Random Surfaces, Quantum Gravity and Strings, Cargese, France, May 1990 ([spire](http://inspirehep.net/record/298523?ln=en))

The interpretation via [[D-branes]] of non-perturbative effects in the string [[coupling constant]] is due to

* {#Polchinski94} [[Joseph Polchinski]], _Combinatorics of boundaries in string theory_, Phys. Rev. D 50, 6041 (1994) ([arXiv:hep-th/9407031](https://arxiv.org/abs/hep-th/9407031))


The identification of non-perturbative contributions in [[string theory]] with brane contributions is due to

* {#BeckerBeckerStrominger95} [[Katrin Becker]], [[Melanie Becker]], [[Andrew Strominger]], _Five-branes, membranes and nonperturbative string theory_, Nucl. Phys. B 456, 130 (1995) ([hep-th/9507158](http://arxiv.org/abs/hep-th/9507158))

Review includes

* [Marino 15](#Marino15)

Reviews specifically in [[type II string theory]] include

* Hugo Looyestijn, _Non-perturbative effects in type IIA string theory_, Master Thesis 2006 ([pdf](http://testweb.science.uu.nl/ITF/teaching/2006/Looyestijn.pdf))

* [[Angel Uranga]], _Non-perturbative effects and D-brane instanton resummation in string theory_ ([[UrangaNonPerturbativeBrane.pdf:file]], [pdf](https://indico.cern.ch/event/75810/contributions/1250733/attachments/1050849/1498253/uranga.pdf))

### In M-Theory

The relation of non-perturbative effects in string theory to [[M-theory]] goes back to

* {#Witten95} [[Edward Witten]], section 2.2 of _[[String Theory Dynamics In Various Dimensions]]_, Nucl.Phys.B443:85-126,1995 ([arXiv:hep-th/9503124](http://arxiv.org/abs/hep-th/9503124))

In [Becker-Becker-Strominger 95](#BeckerBeckerStrominger95) it was realized that the [[worldsheet instantons]] and [[D-brane instantons]] of string theory unify to [[membrane instantons]] (see [Marino 15, section 1.3](#Marino15))


[[!redirects non-perturbative effects]]
[[!redirects non-perturvative effects]]


[[!redirects nonperturbative effect]]
[[!redirects nonperturbative effects]]
