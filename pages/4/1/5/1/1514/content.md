

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--


> under construction

#Contents#
* table of contents 
{:toc}


## Idea

The notion of **path integral** originates in and is mainly used in the context of [[quantum mechanics]] and [[quantum field theory]], where it is a certain operation supposed to model the notion of [[quantization]].

The idea is that the quantum propagator -- in [[FQFT]] the value of the functor $U : Cob \to Vect$ on a certain [[cobordism]] -- is given by an [[integral kernel]] $U : \psi \mapsto \int K(-,y) \psi(y) d\mu$ where $K(x,y)$ is something like the integral of the exponentiated [[action functional]] $S$ over all field configurations $\phi$ with prescribed boundary data $x$ and $y$. Formally one writes

$$
  K(x,y) = \int \exp(i S(\phi))\; D\phi 
$$

and calls this the **path integral**. Here the expression $D \phi$ is supposed to allude to a [[measure space|measure integral]] on the space of all $\phi$. The main problem with the path integral idea is that it is typically unclear what this measure should be, or, worse, it is typically clear that no suitable such measure does exist. 

The name _path integral_ originates from the special case where the system is the [[sigma model]] describing a particle on a target space manifold $X$. In this case a field configuration $\phi$ is a path $\phi : [0,1] \to X$ in $X$, hence the integral over all field configurations is an integral over all paths.

The idea of the path integral famously goes back to [[Richard Feynman]], who motivated the idea in [[quantum mechanics]]. In that context the notion can typically be made precise and shown to be equivalent to various other [[quantization]] prescriptions. 

The central impact of the idea of the path integral however is in its application to [[quantum field theory]], where it is often taken in the physics literature as the _definition_ of what the quantum field theory encoded by an [[action functional]] should be, disregarding the fact that in these contexts it is typically quite unclear what the path integral actually means, precisely. 

Notably the [[Feynman perturbation series]] summing over [[Feynman graphs]] is motivated as one way to make sense of the path integral in quantum field theory and in practice usually serves as a _definition_ of the perturbative path integral.

## Realizations

We start with stating the elementary description of the [[Feynman-Kac formula]] as traditional in physics textbooks in 

* [Elementary description in quantum mechanics](#ElementaryDescription).

Then we indicate the more abstract formulation of this in terms of [[integration]] against the [[Wiener measure]] on the space of paths (for the Euclidean path integral) in 

* _[As an integral against the Wiener measure](#AsAnIntegralAgainstTheWienerMeasure)_.

Then we indicate a formulation in [[perturbation theory]] and [[BV-formalism]] in 

* _[Perturbatively in the BV-formalism](#PerturbativelyInBVFormalism)_

### Elementary description in quantum mechanics
 {#ElementaryDescription}

A simple form of the path integral is realized in [[quantum mechanics]], where it was originally dreamed up by [[Richard Feynman]] and then made precise using the [[Feynman-Kac formula]].  (Most calculations in practice are still done using [[perturbation theory]], see the section _[Perturbatively in BV-formalism](#PerturbativelyInBVFormalism)_ below).

The [[Schrödinger equation]] says that the rate at which the phase of an energy eigenvector rotates is proportional to its energy:
\[ i \hbar \frac{d}{dt} \psi = H \psi. \]
Therefore, the probability that the system evolves to the final state $\psi_F$ after evolving for time $t$ from the initial state $\psi_I$ is
\[ \langle \psi_F|e^{-iHt}|\psi_I\rangle.\]
Chop this up into time steps $\Delta t = t/N$ and use the fact that 
\[\int_{-\infty}^{\infty}|q\rangle\langle q| = 1\]
to get
\[ \langle \psi_F| e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_{N-1} \rangle \langle q_{N-1}| dq_{N-1}\right) e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_{N-2} \rangle \langle q_{N-2}| dq_{N-2}\right) e^{-iH\Delta t} \cdots e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} |q_1 \rangle \langle q_1| dq_1\right) e^{-iH\Delta t} |\psi_I\rangle \]
\[ = \int_{q_1} \cdots \int_{q_{N-2}} \int_{q_{N-1}} \langle \psi_F| e^{-iH\Delta t} |q_{N-1} \rangle \langle q_{N-1}| e^{-iH\Delta t} |q_{N-2} \rangle \langle q_{N-2}|  e^{-iH\Delta t} \cdots e^{-iH\Delta t} |q_1 \rangle \langle q_1| e^{-iH\Delta t} |\psi_I\rangle dq_{N-1} dq_{N-2} \cdots dq_1 \]
Assume we have the free Hamiltonian $H=p^2/2m.$  Looking at an individual term $\langle q_{n+1}| e^{-iH\Delta t} |q_{n} \rangle,$ we can insert a factor of 1 and solve to get
\[ \array{\langle q_{n+1}| e^{-iH\Delta t} \left(\int_{-\infty}^{\infty} \frac{dp}{2\pi}|p\rangle \langle p|\right)|q_{n} \rangle &=& \int_{-\infty}^{\infty} \frac{dp}{2\pi} e^{-ip^2\Delta t/2m} \langle q_{n+1}|p\rangle \langle p|q_{n} \rangle \\ &=& \int_{-\infty}^{\infty} \frac{dp}{2\pi} e^{-ip^2\Delta t/2m} e^{ip(q_{n+1}-q_n)} \\ &=& \left(\frac{-i 2\pi m}{\Delta t}\right)^{\frac{1}{2}} e^{i \Delta t (m/2)[(q_{n+1}-q_n)/\Delta t]^2}.} \]
Defining
\[\int Dq = \lim_{N \to \infty} \left(\frac{-i 2\pi m}{\Delta t}\right)^{\frac{N}{2}} \prod_{n=0}^{N-1} \int dq_n,\]
and letting $\Delta t \to 0, N \to \infty,$ we get
\[ \langle \psi_F|e^{-iHt}|\psi_I\rangle = \int Dq e^{i \int_0^t dt \frac{1}{2}m \dot{q}^2}. \]

For arbitrary Hamiltonians $H = \frac{p^2}{2m} + V(x),$ we get
\[ \array{\langle \psi_F|e^{-iHt}|\psi_I\rangle &=& \int Dq e^{i \int_0^t dt \frac{1}{2}m \dot{q}^2 - V(x)} \\ &=& \int Dq e^{i\int_0^t\mathcal{L}(\dot{q},q) dt} \\ &=& \int Dq e^{iS(q)}, } \]
where $S(q)$ is the [[action]] functional.

\begin{remark}\label{OperatorOrderAndTimeOrder}
**(operator product order and time-order)**
\linebreak
  Under the path integral, the order of the product of [[linear operators]] (such as $x \cdot \frac{d}{d x}$ as opposed to $\frac{d}{d x} x \cdot$) corresponds to *temporal ordering* of their [[observable]] values ([Feynman 1942 p. 35](#Feynman42), [1948 p. 381](#Feynman48),  reviewed in [Nagaosa 1999, pp. 33](#Nagaosa99); [Ong](#Ong)).

Conversely the product of [[observable]] values in the path integral corresponds to the [[time-ordered product]] of the corresponding [[linear operators]], eg. [Polchinski 1998 (A.1.17)](#Polchinski98); [Rischke 2021 (5.63)](#Rischke21).
\end{remark}


### As an integral against the Wiener measure
 {#AsAnIntegralAgainstTheWienerMeasure}

More abstractly, the Euclidean path integral for the [[quantum mechanics]] of a [[charged particle]] may be defined by [[integration]] the gauge-coupling action again the [[Wiener measure]] on the space of paths.


Consider a [[Riemannian manifold]] $(X,g)$ -- hence a [[background field]] of [[gravity]] -- and a [[connection on a bundle|connection]] $\nabla : X \to \mathbf{B}U(1)_{conn}$  -- hence an [[electromagnetic field|electromagnetic]] [[background gauge field]].

The gauge-coupling [[interaction]] term is given by the [[parallel transport]] of this connection

$$  
  \exp(i S)
  \coloneqq
  \exp(2\pi i \int_{(-)} [(-),\nabla] ) 
  \colon 
  [I, X]_{x_0,x_1} \to Hom(E_{x_0}, E_{x_1})
  \,,
$$

where $E \to X$ is the [[complex line bundle]] which is [[associated bundle|associated]] to $\nabla$. 

The [[Wiener measure]] $d\mu_W$ on the space of stochastic paths in $X$,we may write suggestively write as

$$
  d\mu_W = [\exp(-S_{kin})D\gamma]
$$

for it combines what in the physics literature is the [[kinetic action]] and a canonical measure on paths.

(This is a general phenomenon in formalizations of the process of [[quantization]]: the [[kinetic action]] (the [[free field theory]]-part of the [[action functional]]) is absorbed as part of the integration [[measure]] against with the remaining [[interaction]] terms are integrated.  )

Then one has
(e.g. [Norris92, theorem (34)](#Norris), [Charles 99, theorem 6.1](#Charles99)):

the [[integral kernel]] for the time evolution propagator is

$$
  U(x_0,x_1) = \int_{\gamma} tra(\nabla)(\gamma) \, [\exp(-S_{kin}(\gamma)) D\gamma]
  \,,
$$

hence the [[integration]] of the [[parallel transport]]/[[holonomy]] against the [[Wiener measure]].

(To make sense of this one first needs to extend the [[parallel transport]] from smooth paths to stochastic paths, see the references [below](#ReferencesForChargedParticle).)

+-- {: .num_remark #WorldlineFormalism}
###### Remark

This "holonomy integrated against the Wiener measure" is the path integral in the form in which it notably appears in the _[[worldline formalism]]_ for computing [[scattering amplitudes]] in [[quantum field theory]]. See ([Strassler 92, (2.9), (2.10)](#Strassler92)). Notice in particular that by the discussion there this is the correct [[Wick rotation|Wick rotated]] form: the [[kinetic action]] is not a [[complex phase]] but a real exponential $\exp(- S_{kin})$ while the [[gauge field|gauge]] [[interaction]] term (the [[holonomy]]) is a complex phase (locally $\exp(i \int_\gamma A)$).

=--

+-- {: .num_remark}
###### Remark

From the point of view of [[higher prequantum field theory]] this means that the path integral sends a [[correspondence]] in the [[slice (infinity,1)-topos]] of [[smooth infinity-groupoids]] over the [[delooping]] groupoid $\mathbf{B}U(1)$ 

$$
  \array{
    && [I,X]
    \\
    & {}^{(-)|_0}\swarrow && \searrow^{(-)|_1}
    \\
    X && \swArrow_{\exp(i S)} && X
    \\
    & {}_{\mathllap{\chi(\nabla)}}\searrow && \swarrow_{\mathrlap{\chi(\nabla)}}
    \\
    && \mathbf{B}U(1)
  }
$$

(essentially a [[prequantized Lagrangian correspondence]]) to another [[correspondence]], now in the slice over the [[stack]] (now an actual [[2-sheaf]]) $\mathbb{C}\mathbf{Mod}$ of [[modules]] over the [[complex numbers]], hence of [[complex vector bundles]]:

$$
  \array{
    && X \times X
    \\
    & {}^{p_1}\swarrow && \searrow^{p_2}
    \\
    X && \swArrow_{\int_{\gamma}\exp(i S(\gamma)) [\exp(-S_{kin}(\gamma))D\gamma]} && X
    \\
    & {}_{\mathllap{\rho(\chi(\nabla))}}\searrow && \swarrow_{\mathrlap{\rho(\chi(\nabla))}}
    \\
    && \mathbb{C}\mathbf{Mod}
   \,.
  }
$$

=--

For more discussion along these lines see at _[[motivic quantization]]_.



### Perturbatively for free field theory in BV-formalism
 {#PerturbativelyInBVFormalism}

[[BV-BRST formalism]] is a means to formalize the path integral in [[perturbation theory]] as the passage to [[cochain cohomology]] in a _[[quantum BV-complex]]_. See at _[The BV-complex and homological integration](BV-BRST+formalism#HomologicalIntegration)_ for more details.

[[!include action (physics) - table]]

## The path integral in the bigger picture

Ours is the age whose central fundamental theoretical physics question is: 

>_What is [[quantum field theory]]_? 

A closely related question is:

> _What is the path integral_ ? 

After its conception by [[Richard Feynman]] in the middle of the 20th century It was notably [[Edward Witten]]'s achievement in the late 20th century to make clear the vast potential for fundamental physics and pure math underlying the concept of the quantum field theoretic path integral.

And yet, among all the aspects of QFT, the notion of the path integral is the one that has resisted attempts at formalization the most.

While [[FQFT|functorial quantum field theory]] is the formalization of the properties that the _locality_ and the _sewing law_ of the path integral is demanded to have -- whatever the path integral is, it is a process that in the end yields a [[functor]] on a [[(infinity,n)-category of cobordisms]] -- by itself, this sheds no light on what that procedure called "path integration" or "path integral quantization" is.

The single major insight into the right [[higher category theory|higher categorical]] formalization of the path integral is probably the idea indicated in

* [[Dan Freed]]

  * _Quantum groups from path integrals_ ([arXiv:q-alg/9501025](https://arxiv.org/abs/q-alg/9501025))

  * _[[Higher Algebraic Structures and Quantization]]_ ([arXiv:hep-th/9212115](http://arxiv.org/abs/hep-th/9212115))

which says that

* it is wrong to think of the _action functional_ that the path integral integrates over as just a _function_: it is a higher categorical object;

* accordingly, the path integral is not something that just controls the numbers or linear maps assigned by a $d$-dimensional [[quantum field theory]] in dimension $d$: also the assignment to higher codimensions is to be regarded as part of the path integral;

  * notably: the fact that quantum mechanics assigns a (Hilbert) space of sections of a vector bundle to codimension 1 is to be regarded as due to a _summing operation_ in the sense of the path integral, too: the space of sections of a vector bundle is the continuum equivalent of the direct sum of its fibers


More recently, one sees attempts to formalize this observation of Freed's, notably in the context of the [[cobordism hypothesis]]:

* [[geometric infinity-function theory]] is used to compute at least something like a path integral in codimension 1 and 2 in the context of [[sigma-model]] QFT;

* see [[path integral as a pull-push transform]]

* and something similar or is indicated in section 3 and section 6 of

  * [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ ([arXiv:0905.0731](http://arxiv.org/abs/0905.0731))



based on material (on categories of "families") in _[[On the Classification of Topological Field Theories]]_ . 

## Related concepts

* [[Feynman-Kac formula]]

* [[S-matrix]]

* [[Dyson formula]]

* [[fermionic path integral]]

* [[principle of extremal action]]

* [[integration over infinite-dimensional manifolds]]

* [[cohomological integration]], [[BV-BRST quantization]]

* [[Schwinger-Dyson equation]]




## References 
 {#References}

### General


The original articles:

* {#Dirac33} [[Paul A. M. Dirac]], *The Lagrangian in Quantum Mechanics*, Physikalische Zeitschrift der Sowjetunion, Band **3**, Heft 1 (1933) 64–72 &lbrack;[pdf](https://www.informationphilosopher.com/solutions/scientists/dirac/Lagrangian_1933.pdf)&rbrack;, reprinted in [Brown 2005](#Brown05) &lbrack;[doi:10.1142/9789812567635_0003](https://doi.org/10.1142/9789812567635_0003)&rbrack;

* {#Feynman42} [[Richard P. Feynman]], *The Principles of Least Action in Quantum Mechanics*, PhD thesis (1942), reprinted in [Brown 2005](#Brown05) &lbrack;[doi:10.1142/9789812567635_0001](https://doi.org/10.1142/9789812567635_0001)&rbrack;

* {#Feynman48} [[Richard P. Feynman]], *Space-Time Approach to Non-Relativistic Quantum Mechanics*, Rev. Mod. Phys. **20** (1948) 367 &lbrack;[doi:10.1103/RevModPhys.20.367](https://doi.org/10.1103/RevModPhys.20.367), [pdf](http://www-f1.ijs.si/~ramsak/km1/feynman.pdf)&rbrack;

reprinted in:

* {#Brown05} [[Laurie M. Brown]], *Feynman's Thesis — A New Approach to Quantum Theory*, World Scientific (2005) &lbrack;[doi:10.1142/5852](https://doi.org/10.1142/5852)&rbrack;

and then the original monograph:

* [[Richard P. Feynman]], [[Albert R. Hibbs]], _Quantum Mechanics and Path Integrals_, New York: McGraw-Hill (1965)

* [[Daniel F. Styer]], *The Errors of Feynman and Hibbs* &lbrack;[pdf](https://www2.oberlin.edu/physics/dstyer/FeynmanHibbs/ErrorsOfFeynmanHibbsX.pdf)&rbrack;

* [[Daniel F. Styer]], [[Richard P. Feynman]], [[Albert R. Hibbs]], *Quantum Mechanics and Path Integrals: Emended Edition*, Dover (2010) &lbrack;[ISBN:0486477223](https://store.doverpublications.com/0486477223.html), [pdf](http://www-f1.ijs.si/~ramsak/km1/FeynmanHibbs.pdf)&rbrack; 

Textbook accounts:

* [[John W. Negele]], [[Henri Orland]], *Functional Integral Formulation*, §2.2 in: *Quantum Many-Particle Systems*, Westview Press (1988, 1998) &lbrack;[doi:10.1201/9780429497926](https://doi.org/10.1201/9780429497926)&rbrack;

* {#Kleinert90} [[Hagen Kleinert]], *Path Integrals in Quantum Mechanics, Statistics, Polymer Physics, and Financial Markets*, World Scientific (1990, 1994, 2003, 2006, 2009) &lbrack;[doi:10.1142/7305](https://doi.org/10.1142/7305), [pdf](https://hagenkleinert.de/documents/pi/HagenKleinert_PathIntegrals.pdf)&rbrack;

* {#Polchinski98} [[Joseph Polchinski]], *A short course on path integrals*,  Appendix A in: _[[String theory]]_ part I: *An Introduction to the Bosonic String*, Cambridge University Press (1998) &lbrack;[doi:10.1017/CBO9780511816079](https://doi.org/10.1017/CBO9780511816079), [pdf](http://www.nucleares.unam.mx/~alberto/apuntes/polchinski1.pdf)&rbrack;

* {#Nagaosa99} [[Naoto Nagaosa]], *Quantization with Path Integral Methods*, Section 2 of: *Quantum Field Theory in Condensed Matter Physics*, Texts and Monographs in Physics, Springer (1999) &lbrack;[doi:10.1007/978-3-662-03774-4_2](https://doi.org/10.1007/978-3-662-03774-4_2)&rbrack;

* G. Johnson, M. Lapidus, _The Feynman integral and Feynman's operational calculus_, Oxford University Press (2000)

* [[Barry Simon]], _Functional integration and quantum physics_ AMS Chelsea Publ. (2005)

* [[Pierre Cartier]], [[Cécile DeWitt-Morette]], _Functional integration: action and symmetries_, Cambridge Monographs on Mathematical Physics (2006) &lbrack;[ISBN:9780521143578](https://www.cambridge.org/ae/academic/subjects/physics/theoretical-physics-and-mathematical-physics/functional-integration-action-and-symmetries?format=PB#contentsTabAnchor)&rbrack;

* Daisuke Fujiwara, _Rigorous Time Slicing Approach to Feynman Path Integrals_ (2017) Springer &lbrack;[doi:/10.1007/978-4-431-56553-6](https://dx.doi.org/10.1007/978-4-431-56553-6)&rbrack;

See also:

* {#Ong} Yen Chin Ong, *Where is the Commutation Relation Hiding in the Path Integral Formulation?* &lbrack;[pdf](https://physicstravelguide.com/_media/quantum_theory/path-integral.pdf), [[Ong-CommutationRelationInPathIntegral.pdf:file]]&rbrack;

Further lecture notes:

* R. Rosenfelder, _Path Integrals in Quantum Physics_ &lbrack;[arXiv:1209.1315](http://arxiv.org/abs/1209.1315)&rbrack;

* {#Rischke21} [[Dirk Rischke]], *Path Integrals in Quantum Mechanics*, lecture notes (2021) &lbrack;[pdf](https://itp.uni-frankfurt.de/~drischke/Script_Path_Integrals_GU2021.pdf)&rbrack;


Discussion in [[constructive quantum field theory]]:

* [[James Glimm]], [[Arthur Jaffe]], *[[Glimm-Jaffe|Quantum physics: a functional integral point of view]]*, Springer (1981, 1987) &lbrack;[doi:10.1007/978-1-4612-4728-9](https://doi.org/10.1007/978-1-4612-4728-9)&rbrack;

* Simon, _Functional Integration in Quantum Physics_ (AMS, 2005)

* [[Sergio Albeverio]], Raphael H&#248;egh-Krohn, Sonia Mazzucchi. _Mathematical theory of Feynman path integrals - An Introduction_, 2 nd corrected and enlarged edition,
Lecture Notes in Mathematics, Vol. 523. Springer, Berlin, 2008 ([ZMATH](href="http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:pre05233292&format=complete))

* Sonia Mazzucchi, _Mathematical Feynman Path Integrals and Their Applications_,
World Scientific, Singapore, 2009.


The [[worldline]] path integral as a way to compute [[scattering amplitudes]] in [[QFT]] was understood in 

* {#Strassler92} [[Matthew Strassler]], _Field Theory Without Feynman Diagrams: One-Loop Effective Actions_, Nucl. Phys. B385:145-184,1992 ([arXiv:hep-ph/9205205](http://arxiv.org/abs/hep-ph/9205205))

On dicretization of path integrals for [[AKSZ sigma-models]]:

* {#Lackman24} [[Joshua Lackman]], *A Groupoid Construction of Functional Integrals: Brownian Motion and Some TQFTs* &lbrack;[arXiv:2402.05866](https://arxiv.org/abs/2402.05866)&rbrack;
  
* [[Joshua Lackman]], *A Groupoid Construction of Functional Integrals*, [talk at](CQTS#Lackman24) [[CQTS]] (Feb 2024) &lbrack;video:[kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_57ywhlbg?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_57ywhlbg)&rbrack;

* [[Joshua Lackman]], *A Mathematical Definition of Path Integrals on Symplectic Manifolds* &lbrack;[arXiv:2406.14547](https://arxiv.org/abs/2406.14547)&rbrack;

* [[Joshua Lackman]]: *On an Axiomatization of Path Integral Quantization and its Equivalence to Berezin's Quantization* &lbrack;[arXiv:2410.02739](https://arxiv.org/abs/2410.02739)&rbrack;


### Stochastic integration theory

The following articles use the integration over [[Wiener measures]] on [[stochastic processes]] for formalizing the path ingegral.

* {#Norris92} [[James Norris]], _A complete differential formalism for stochastic calculus in manifolds_, S&#233;minaire de probabilit&#233;s de Strasbourg,  26 (1992), p. 189-209 ([NUMDAM]( http://www.numdam.org/item?id=SPS_1992__26__189_0))
 

* Vassili Kolokoltsov, _Path integration: connecting pure jump and Wiener processes_ ([pdf](http://www2.warwick.ac.uk/fac/sci/statistics/staff/academic-research/kolokoltsov/minnesota.pdf))

* Bruce Driver, Anton Thalmaier, _Heat equation derivative formulas for vector bundles_, Journal of Functional Analysis 183, 42-108 (2001) ([pdf](http://www.math.ucsd.edu/~bdriver/DRIVER/Papers/Drivers_Papers/A26-Heat-Derivative-Formula.pdf))




### For charged particle/path integral of holonomy functional
 {#ReferencesForChargedParticle}

The following articles discuss (aspects of) the path integral for the [[charged particle]] coupled to a [[background gauge field]], in which case the path integral is essentially the integration of the [[holonomy]]/[[parallel transport]] functional against the [[Wiener measure]].


* Marc Arnaudon and Anton Thalmaier, _Yang--Mills fields and random holonomy along Brownian bridges_, Ann. Probab. Volume 31, Number 2 (2003), 769-790. ([Euclid](http://projecteuclid.org/euclid.aop/1048516535))

* [[Mikhail Kapranov]], _Noncommutative geometry and path integrals_, in _Algebra, Arithmetic and Geometry_, Birkh&#228;user Progress in Mathematics 27 (2009) ([arXiv:math/0612411](http://arxiv.org/abs/math/0612411))


* [[Christian Bär]], [[Frank Pfäffle]], _Path integrals on manifolds by finite dimensional approximation_,  J. reine angew. Math., (2008), 625: 29-57. ([arXiv:math.AP/0703272](http://arxiv.org/abs/math.AP/0703272))

* Dana Fine, [[Stephen F. Sawin]]: _A Rigorous Path Integral for Supersymmetric Quantum Mechanics and the Heat Kernel_, Commun. Math. Phys. **284** (2008) 79–91 &lbrack;[arXiv:0705.0638](http://arxiv.org/abs/0705.0638), [doi:10.1007/s00220-008-0606-2](https://doi.org/10.1007/s00220-008-0606-2)&rbrack;
 > (for [[supersymmetric quantum mechanics]])

* Florian Hanisch, [[Matthias Ludewig]]: _A Rigorous Construction of the Supersymmetric Path Integral Associated to a Compact Spin Manifold_, ([arXiv:1709.10027](https://arxiv.org/abs/1709.10027))


A discussion for [[phase spaces]] equipped with a [[Kähler polarization]] and a [[prequantum line bundle]] is in 

* {#Charles99} Laurent Charles, _Feynman path integral and Toeplitz Quantization_, Helv. Phys. Acta **72** (1999) 341., ([pdf](http://ipht.cea.fr/DocsphtV2/articles/t98/093/public/publi.pdf))
 

following [Norris 92, theorem (34)](#Norris92).



### More


Other references on mathematical aspects of path integrals include

* [[Pierre Cartier]], [[Cécile DeWitt-Morette]], _Functional integration: action and symmetries_, Cambridge Monographs on Mathematical Physics, 2006.  ISBN: 9780521866965.  [doi](https://doi.org/10.1017/CBO9780511535062).

* {#HenneauxTeitelboim} [[Marc Henneaux]], [[Claudio Teitelboim]], _[[Quantization of Gauge Systems]]_, Princeton University Press 1992

* [[Nikolai Reshetikhin]], _Lectures on quantization of gauge systems_, [arxiv/1008.1411](http://arxiv.org/abs/1008.1411)

* [[Edward Witten]], _A new look at the path integral of quantum mechanics_, ([arxiv/1009.6032](http://arxiv.org/abs/1009.6032))

Detailed rigorous discussion for [[quadratic Hamiltonians]] and for [[phase space]] paths in in 

* {#RobbinSalamon93} [[Joel Robbin]],  [[Dietmar Salamon]], _Feynman path integrals on phase space and the metaplectic representation_ in [[Dietmar Salamon]] (ed.), _Symplectic Geometry_, LMS Lecture Note series 192 (1993) ([[RobbinSalamonMetaplectic.pdf:file]])

Discussion of quantization of [[Chern-Simons theory]] via a [[Wiener measure]] is in

* Adrian P. C. Lim, _Chern-Simons Path Integral on $\mathbb{R}^3$ using Abstract Wiener Measure_ ([pdf](http://www.math.cornell.edu/~pclim/Docs/papers/CSabe01.pdf))

Lecture notes on [[quantum field theory]], emphasizing mathematics of the Euclidean path integrals and the relation to statistical physics are at

* [[AJ Tolland]], _[Wilsonian QFT for Mathematicians](http://www.math.sunysb.edu/~ajt/Teaching/560spring2011/)_ 

MathOverflow questions: [mathematics-of-path-integral-state-of-the-art](http://mathoverflow.net/questions/19495/mathematics-of-path-integral-state-of-the-art),[path-integrals-outside-qft](http://mathoverflow.net/questions/20393/path-integrals-outside-qft), [doing-geometry-using-feynman-path-integral](http://mathoverflow.net/questions/19490/doing-geometry-using-feynman-path-integral), [path-integrals-localisation](http://mathoverflow.net/questions/17577/path-integrals-localisation), [finite-dimensional-feynman-integrals](http://mathoverflow.net/questions/31966/finite-dimensional-feynman-integrals), [the-mathematical-theory-of-feynman-integrals](http://mathoverflow.net/questions/24823/the-mathematical-theory-of-feynman-integrals)

* [[Theo Johnson-Freyd]], _The formal path integral and quantum mechanics_, J. Math. Phys. __51__, 122103 (2010) [arxiv/1004.4305](http://arxiv.org/abs/1004.4305),  [doi](http://dx.doi.org/10.1063/1.3503472); _On the coordinate (in)dependence of the formal path integral_, [arxiv/1003.5730](http://arxiv.org/abs/1003.5730)

[[!redirects path integrals]]

[[!redirects Feynman path integral]]
[[!redirects Feynman path integrals]]

[[!redirects path-integral]]
[[!redirects path-integrals]]

[[!redirects Feynman path-integral]]
[[!redirects Feynman path-integrals]]
