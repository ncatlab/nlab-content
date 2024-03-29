
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

### General

_Perturbation theory_ is a general method of finding (or even defining) the solution of equations of mathematical physics by expanding them with respect to a small parameter in the vicinity of known, defined or well-understood solution (for which the small parameter is $0$). It is used in the study of PDEs involving operators depending on small parameter, in classical and celestical mechanics, in quantum mechanics, and in the statistical and [[perturbative quantum field theory]]. 

One of the varieties of perturbation theory provides a method to make sense of and handle the [[path integral]] involved in the [[quantization]] of [[classical field theory]] to [[quantum field theory]].

It is based on the observation that the [[quantization]] of free [[classical field theory|classical field theories]], whose [[action functional]] contains only the kinetic term, is well understood; therefore, the quantization of a functional consisting of a kinetic term and polynomial interaction terms may be expanded like a [[Taylor series]] in the interaction terms, thus yielding what looks like a series of [[correlator]]s in a free field theory.  If the **coupling constant** -- the parameter in front of the interaction terms -- is small enough, one says one is in the _weakly coupled regime_ of the theory and expects this perturbation series to approximate the desired answer. Usually, even for that to work the [[action functional]] first has to be subjected to [[renormalization]].

### More details

Suppose we're working with a quantum system that's nearly a [[quantum harmonic oscillator]], but not quite; that is, the quadratic potential $V_0 = \frac{1}{2}k x^2 - \frac{1}{2}$ is only a good local approximation to the real potential $V_0 + \lambda V$.  Then we can write the [[Hamiltonian]] as $H = H_0 + \lambda V,$ where $V$ is a function of the [[position]] $x$ and the [[momentum]] $p$ (or equivalently, of $z = \frac{p+i x}{\sqrt{2}}$ and $\frac{d}{dz}$) and $\lambda$ is small.

Now we solve Schr&#246;dinger's equation perturbatively.  We know that
\[\psi(t) = e^{-itH} \psi(0),\]
and we assume that
\[e^{-itH}\psi(t) \approx e^{-itH_0} \psi(t)\]
so that it makes sense to solve it perturbatively.  Define
\[\psi_1(t) = e^{itH_0} e^{-itH}\psi(t)\]
and
\[V_1(t) = e^{itH_0} \lambda V e^{-itH_0}.\]
After a little work, we find that
\[\frac{d}{dt}\psi_1(t) = -i V_1(t) \psi_1(t),\]
and integrating, we get
\[\psi_1(t) = -i\int_0^t V_1(t_0) \psi_1(t_0) dt_0 + \psi(0).\]
We feed this equation back into itself recursively to get
\[\array{ \psi_1(t) & = & -i \int_0^t V_1(t_0) \left[-i\int_0^{t_0} V_1(t_1) \psi_1(t_1) dt_1 + \psi(0) \right] dt_0 + \psi(0) \\ & = & \left[\psi(0)\right] + \left[\int_0^t i^{-1} V_1(t_0)\psi(0) dt_0\right] + \left[\int_0^t\int_0^{t_0} i^{-2} V_1(t_0)V_1(t_1) \psi_1(t_1) dt_1 dt_0\right] \\ & = & \sum_{n=0}^{\infty} \int_{t \ge t_0 \ge \ldots \ge t_{n-1} \ge 0} i^{-n} V_1(t_0)\cdots V_1(t_{n-1}) \psi(0) dt_{n-1}\cdots dt_0 \\ & = & \sum_{n=0}^{\infty} (-\lambda i)^n \int_{t \ge t_0 \ge \ldots \ge t_{n-1} \ge 0} e^{-i(t-t_0)H_0} V e^{-i(t_0-t_1)H_0} V \cdots V e^{-i(t_{n-1}-0)H_0} \psi(0) dt_{n-1}\cdots dt_0. }\]
So here we have a sum of a bunch of terms; the $n$th term involves $n$ interactions with the potential interspersed with evolving freely between the interactions, and we integrate over all possible times at which those interactions could occur.

Here's an example [[Feynman diagram]] for this simple system, representing the fourth term in the sum above:
<p style="text-align:center;"><img src="http://reperiendi.wordpress.com/files/2009/10/3.gif" alt="Three interactions with the perturbation." title="3" width="10" height="200" class="size-full wp-image-798" /></p>
The lines represent evolving under the free Hamiltonian $H_0$, while the dots are interactions with the potential $V$.

As an example, let's consider $V = (z + \frac{d}{dz})$ and choose $\lambda = \frac{1}{\sqrt{2}}$ so that $\lambda V = p.$  When $V$ acts on a state $\psi = z^n,$ we get $V \psi = z^{n+1} + nz^{n-1}.$  So at each interaction, the system either gains a photon or changes phase and loses a photon.

## Properties

### Divergence/Convergence
 {#DivergenceConvergence}

Despite what one might naively expect, the [[perturbation series]] of natural [[quantum field theories]] have a vanishing [[radius of convergence]], they are [[asymptotic series]]. 

Roughly this can be understood as follows: since the pertrubation is in the [[coupling constant]] about vanishing coupling, a non-zero [[radius of convergence]] would imply that the theory is finite also for _negative_ coupling (where "things fly apart"), which will not happen in realistic theories. 

More in detail, [[theory (physics)|theories]] with [[non-perturbative effects]] such as [[instantons]] [[field (physics)|field]] configurations (such as [[Yang-Mills theory]], hence [[QCD]], [[QED]]), [[branes]] (such as [[string theory]]), etc., are expected to have a  [[path integral]] which as a [[function]] of the [[coupling constant]] $g$ schematically looks like

$$
  Z(g)
  = 
  \sum_n a_n g^n
  + 
  e^{-A/g}
  \sum_n a_n^{(1)} g^n
  + 
  \mathcal{O}(e^{-2A/g})
  \,,
$$

where the first sum is the [[perturbation series]] itself and where the terms with a prefactor of the form $\exp(-A/g)$ are the contributions of the [[instantons]] ($A$ is the contribution of the [[instanton]] [[action functional]]). Since all the [[derivatives]] of the function $g \mapsto e^{-1/g}$ vanish at [[coupling constant]] $g = 0$, the [[Taylor series]] of this part of the path integral does not appear in [[perturbation series]], even though it is present. Therefore this is called a _[[non-perturbative effect]]_.

See the [references below](#ReferencesDivergenceConvergence) for details. The mathematics behind this is called _[[resurgence theory]]_.

(See also at _[string theory FAQ -- Isn't it fatal that the string perturbation series does not converge?](string+theory+FAQ#NonConvergenceOfPerturbationSeries)_.)


## Related concepts

* [[perturbative quantum field theory]]

  * [[causal perturbation theory]], [[perturbative algebraic quantum field theory]]

  * [[renormalization]]

  * [[Feynman diagram]]

  * [[scattering amplitude]], [[string scattering amplitude]]

  * [[vacuum]], [[tachyon]]

* [[non-perturbative quantum field theory]]

  * [[non-perturbative effect]]

  * [[soliton]], [[instanton]]

  * [[Borel resummation]], [[resurgence theory]]

* [string theory FAQ -- Isn't it fatal that the string perturbation series does not converge?](string%20theory%20FAQ#NonConvergenceOfPerturbationSeries)

## References

### General

A solid mathematical formulation of perturbation theory has been given in

* K. Hepp.: _Th&eacute;orie de la Renormalisation_ Lect. Notes in Phys. Springer (1969)

* O. Steinmann, _Perturbation expansion in axiomatic field theory_ Lect. Notes in Phys. 11, Springer (1971)

### On Divergence/Convergence and Non-perturbative effects
 {#ReferencesDivergenceConvergence}

The argument that the perturbation series of realistic [[quantum field theories]] such as [[QED]] necessarily diverges goes back to 

* {#Dyson52} [[Freeman Dyson]], _Divergence of perturbation theory in quantum electrodynamics_, Phys. Rev. 85, 631, 1952 ([spire](http://inspirehep.net/record/29799?ln=en))

  **Abstract**: _An argument is presented which leads tentatively to the conclusion that all the power-series expansions currently in use in quantum electrodynamics are divergent after the renormalization of mass and charge. The divergence in no way restricts the accuracy of practical calculations that can be made with the theory, but raises important questions of principle concerning the nature of the physical concepts upon which the theory is built._

and is made more precise in

* {#Lipatov77} [[Lev Lipatov]], _Divergence of the Perturbation Theory Series and the Quasiclassical Theory_, Sov.Phys.JETP 45 (1977) 216&#8211;223 ([pdf](http://jetp.ac.ru/cgi-bin/dn/e_045_02_0216.pdf))

recalled for instance in 

* {#Suslov05} [[Igor Suslov]], section 1 of _Divergent perturbation series_, Zh.Eksp.Teor.Fiz. 127 (2005) 1350; J.Exp.Theor.Phys. 100 (2005) 1188 ([arXiv:hep-ph/0510142](https://arxiv.org/abs/hep-ph/0510142))

* Justin Bond, last section of _Perturbative QFT is Asymptotic; is Divergent; is Problematic in Principle_ ([pdf](https://mcgreevy.physics.ucsd.edu/s13/final-papers/2013S-215C-Bond-Justin.pdf))

* {#BakulevShirkov10} Alexander P. Bakulev, [[Dmitry Shirkov]], section 1.1 of _Inevitability and Importance of Non-Perturbative Elements in Quantum Field Theory_, Proceedings of the 6th Mathematical Physics Meeting, Sept. 14--23, 2010, Belgrade, Serbia (ISBN 978-86-82441-30-4), pp. 27--54 ([arXiv:1102.2380](https://arxiv.org/abs/1102.2380)) 

* {#HollandsWald14} [[Stefan Hollands]], [[Robert Wald]], section 4.1 of _Quantum fields in curved spacetime_, Physics Reports Volume 574, 16 April 2015, Pages 1-35 ([arXiv:1401.2026](https://arxiv.org/abs/1401.2026))

* Marco Serone, from 2:46 on in _A look at $\phi^4_2$ using perturbation theory_ ([recording](https://www.youtube.com/watch?v=J4nxvY1rOhI))

Exposition also in:

* [[Jakob Schwichtenberg]], *[divergence-perturbation-series-qft](http://jakobschwichtenberg.com/divergence-perturbation-series-qft)*

For the example of [[phi^4 theory]] this non-convergence of the perturbation series is discussed in

* {#Helling} Robert Helling, p. 4 of _Solving classical field equations_ ([pdf](http://homepages.physik.uni-muenchen.de/~helling/classical_fields.pdf))

For the example of [[phi^4 theory]] this non-convergence of the perturbation series is discussed in

* {#Helling} Robert Helling, p. 4 of _Solving classical field equations_ ([pdf](http://homepages.physik.uni-muenchen.de/~helling/classical_fields.pdf))


A general introduction on divergence of perturbation theory, asymptotic series and [[non-perturbative effects]] is for instance on the first pages of

* [[Marcos Marino]], _Lectures on non-perturbative effects in large N gauge theories, matrix models and strings_ ([arXiv:1206.6272](http://arxiv.org/abs/1206.6272))

See also

* Carl M. Bender, Carlo Heissenberg, _Convergent and Divergent Series in Physics_ ([arXiv:1703.05164](https://arxiv.org/abs/1703.05164))

Further discussion is for instance in

* Physics.Stack exchange discussion, _[Is QCD free from all divergences?](http://physics.stackexchange.com/questions/30105/is-qcd-free-from-all-divergences)_


### In AQFT
 {#ReferencesInAQFT}

Perturbation theory in the spirit of [[AQFT]], namely in [[locally covariant perturbative quantum field theory]] is discussed in the following articles.

The observation that in [[perturbation theory]] the [[renormalization|Stückelberg-Bogoliubov-Epstein-Glaser]] local [[S-matrix|S-matrices]] yield a [[local net of observables]] was first made in 

* V. Il'in, D. Slavnov, _Observable algebras in the S-matrix approach_ Theor. Math. Phys. **36** , 32 (1978) 578-585

which was however mostly ignored and forgotten. It is taken up again in

* [[Romeo Brunetti]], [[Klaus Fredenhagen]], _Microlocal Analysis and Interacting Quantum Field Theories: Renormalization on Physical Backgrounds_  Commun. Math. Phys. 208:623-661 (2000) ([arXiv:math-ph/9903028](http://arxiv.org/abs/math-ph/9903028))

(a quick survey is in section 8, details are in section 2).

Further developments along these lines are then

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _Algebraic quantum field theory, perturbation theory, and the loop expansion_,
Commun. Math. Phys. 219:5-30 (2001) ([arXiv:hep-th/0001129](http://xxx.uni-augsburg.de/abs/hep-th/0001129))

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative algebraic quantum field theory and deformation quantization_,
Proceedings of the Conference on Mathematical Physics in Mathematics and Physics, Siena June 20-25 (2000) ([arXiv:hep-th/0101079](http://xxx.uni-augsburg.de/abs/hep-th/0101079)) 

(relation to [[deformation quantization]])

* [[Romeo Brunetti]], [[Michael Dütsch]], [[Klaus Fredenhagen]], _Perturbative Algebraic Quantum Field Theory and the Renormalization Groups_, Adv. Theor. Math. Physics 13 (2009), 1541-1599 ([arXiv:0901.2038](http://arxiv.org/abs/0901.2038))

(relation to [[renormalization]])

* [[Michael Dütsch]], [[Klaus Fredenhagen]], _A local (perturbative) construction of observables in gauge theories: the example of qed_, Commun. Math. Phys. 203 (1999), no.1, 71-105,  ([arXiv:hep-th/9807078](http://xxx.uni-augsburg.de/abs/hep-th/9807078)). 

(relation to [[gauge theory]] and [[QED]])

Reviews includes

* [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative algebraic quantum field theory_ ([arXiv:1208.1428](http://arxiv.org/abs/1208.1428))

* [[Klaus Fredenhagen]], [[Katarzyna Rejzner]], _Perturbative Construction of Models of Algebraic Quantum Field Theory_ ([arXiv:1503.07814](http://arxiv.org/abs/1503.07814))

and a textbook acount is in 

* [[Katarzyna Rejzner]], _Perturbative Algebraic Quantum Field Theory_, Mathematical Physics Studies, Springer 2016 ([pdf](https://link.springer.com/book/10.1007%2F978-3-319-25901-7))


Further developments in perturbation theory in [[AQFT on curved spacetimes]] icludes

* {#KhavkineMoretti16} [[Igor Khavkine]], [[Valter Moretti]], _Analytic Dependence is an Unnecessary Requirement in Renormalization of Locally Covariant QFT_, Communications in Mathematical Physics, March 2016 ([arXiv:1411.1302](http://arxiv.org/abs/1411.1302), [publisher](http://link.springer.com/article/10.1007%2Fs00220-016-2618-7))

### In BV-BRST formalism

Perturbative quantization in [[BV-BRST formalism]] is nicely systematically discussed in section 5 of 

* [[Kevin Costello]], [[Owen Gwilliam]], _Factorization algebras in quantum field theory_ ([pdf](http://www.math.northwestern.edu/~costello/factorization.pdf))

in the broad context of _[[factorization algebras]]_ (see there for further references). In particular the relation to Feynman diagrams is discussed in 

* [[Owen Gwilliam]], [[Theo Johnson-Freyd]], _How to derive Feynman diagrams for finite-dimensional integrals directly from the BV formalism_ (2011) ([arXiv:1202.1554](http://arxiv.org/abs/1202.1554))

[[!redirects perturbation theories]]

[[!redirects perturbation series]]

[[!redirects perturbation]]
[[!redirects perturbations]]
