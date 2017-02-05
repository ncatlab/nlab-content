
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _axion_ is hypothetical type of [[field (physics)|field]]/[[fundamental particle]] related to the [[strong CP problem]].

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

but that -- since the term $tr(F_\nabla \wedge F_\nabla)$ causes parity violation, which is strongly bounded by [[experiment]] -- there must be some reason why $\theta$ is extremely small.

The solution to this problem via axions is to assume that $\theta$ is not really a fundamental constant, but instead the [[vacuum expectation value]] of a dynamical field $a$ (the axion). The argument then is that the presence of the coupling term $\theta \int_X tr(F_\nabla \wedge F_\nabla)$ necessarily gives $a$ vanishing expectation value (that's due to [Vafa-Witten 84, around (2)](#VafaWitten84)). They argue, via the [[Wick rotation|Wick rotated]] [[path integral]] as follows:

Under [[Wick rotation]]. parity-violating terms in the [[Lagrangian density]] pick up an imaginary factor $i$. Therefore the [[path integral]] expression for the Wick rotated [[vacuum energy]] is

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
 


## As arising from string theory
 {#AsArisingFromStringTheory}

In [[string theory]] axion fields naturally arise in various ways [Svrcek-Witten 06](#SvrcekWitten06):

> An obvious question about the axion hypothesis is how natural it really is. Why introduce a global PQ "symmetry" if it is not actually a symmetry? What is the sense in constraining a theory so that the classical Lagrangian possesses a certain symmetry if the symmetry is actually anomalous? It could be argued that the best evidence that PQ "symmetries" are natural comes from string theory, which produces them without any contrivance. ... the string compactifications always generate PQ symmetries, often spontaneously broken at the string scale and producing axions, but sometimes unbroken.([Svrcek-Witten 06, pages 3-4](#SvrcekWitten06))


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

* M. Dine, [[Willy Fischler]], [[Mark Srednicki]], _A simple solution to the strong CP problem with a harmless axion_, Phys. Lett. B 104:199-202 (1981)

The observation that this "invisible axion" is a cadidate for [[dark matter]] is due to

* [[John Preskill]], M. Wise, [[Frank Wilcek]], _Comology of the invisible axion_, Phys. Lett. B 120:127-32 (1983)

A historical recollection of the development until here is in

* [[Frank Wilcek]], _Birth of axions_ in _This Week's Citation Classic_ (1991) ([pdf](http://www.garfield.library.upenn.edu/classics1991/A1991FE76900001.pdf))

The argument that the [[topological Yang-Mills theory|topological]] [[interaction]] term $\propto a \langle F \wedge F\rangle$ gives the axion field $a$ a vanishing [[vacuum expectation value]] is due to

* {#VafaWitten84} [[Cumrun Vafa]], [[Edward Witten]], _Parity Conservation in Quantum Chromodynamics_ Phys. Rev. Lett. 53, 535 (1984) ([publisher](http://journals.aps.org/prl/abstract/10.1103/PhysRevLett.53.535))

A reformulation of this effect in terms of [[Chern-Simons forms]] is discussed in

* [[Gia Dvali]], _Three-Form Gauging of axion Symmetries and Gravity_ ([arXiv:hep-th/0507215](https://arxiv.org/abs/hep-th/0507215))

See also

* Wikipedia _[Axion](http://en.wikipedia.org/wiki/Axion)_


### In string theory

Discssion of the various ways that axions naturally appea in [[string theory]]  is in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))

and discuss specifically for the [[F-theory]] sector of string theory is in

* {#Grimm14} Thomas Grimm, _Axion Inflation in F-theory_ ([arXiv:1404.4268](http://arxiv.org/abs/1404.4268))


### Experimental signature

* Joseph P. Conlon, M.C. David Marsh, _Searching for a 0.1-1 keV Cosmic Axion Background_ ([arXiv:1305.3603](http://arxiv.org/abs/1305.3603))

  > Primordial decays of [[string theory]] [[moduli stabilization|moduli]] at $z \sim 10^{12}$ naturally generate a [[dark radiation]] Cosmic Axion Background (CAB) with $0.1 - 1 keV$ energies. This CAB can be detected through axion-[[photon]] conversion in astrophysical [[magnetic fields]] to give quasi-thermal excesses in the extreme ultraviolet and soft X-ray bands. Substantial and observable luminosities may be generated even for axion-photon couplings $\ll 10^{-11} GeV^{-1}$. We propose that axion-photon conversion may explain the observed excess emission of soft X-rays from galaxy clusters, and may also contribute to the diffuse unresolved cosmic X-ray background. We list a number of correlated predictions of the scenario. 


Discussion of the axion as a candidate for [[dark matter]] is

* {#HOTW16} Lam Hui, Jeremiah P. Ostriker, Scott Tremaine, [[Edward Witten]], _On the hypothesis that cosmological dark matter is composed of ultra-light bosons_ ([arXiv:1610.08297](https://arxiv.org/abs/1610.08297))

and as a candidate for [[dark energy]]:

* [[Stephon Alexander]], [[Robert Brandenberger]], [[Juerg Froehlich]], _Tracking Dark Energy from Axion-Gauge Field Couplings_ ([arXiv:1601.00057](https://arxiv.org/abs/1601.00057))

[[!redirects axions]]

[[!redirects invisible axion]]
[[!redirects invisible axions]]
