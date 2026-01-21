

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[probability theory]],
the concept of _noncommutative probability space_ or _quantum probability space_ is the generalization of that of _[[probability space]]_ as the concept of "space" is generalized to [[non-commutative geometry]].

The basic idea is to encode a would-be [[probability space]] [[Isbell duality|dually]] in its [[algebra of functions]] $\mathcal{A}$, typically regarded as a [[star algebra]], and encode the [[probability measure]] as a [[state on a star-algebra|state on this star algebra]] 

$$
  \langle
    -
  \rangle
  \;\colon\;
  \mathcal{A}
    \longrightarrow
  \mathbb{C}
  \,.
$$

Hence this primarily [[axiom|axiomatizes]] the concept of _[[expectation values]]_ $\langle A\rangle$ ([Segal 65](#Segal65), [Whittle 92](#Whittle92)) while leaving the nature of the underlying [[probability measure]] implicit (in contrast to the classical formalization of [[probability theory]] by [[Andrey Kolmogorov]]).

Often $\mathcal{A}$ is assumed/required to be a [[von Neumann algebra]] (e.g. [Kuperberg 05, section 1.8](#Kuperberg05)). Often $\mathcal{A}$ is taken to be the full algebra of [[bounded operators]] on some [[Hilbert space]] (e.g. [Attal, def. 7.1](#Attal)).

In [[quantum physics]], $\mathcal{A}$ is an [[algebra of observables]] (or a [[local net of observables|local net]] thereof) and $\langle (-)\rangle$ is a particular [[quantum state]], for instance a [[vacuum state]].

The formulation of [[non-perturbative quantum field theory]] from the algebraic perspective of quantum probability is known as _[[algebraic quantum field theory]]_ ([[AQFT]]).

The formulation of [[perturbative quantum field theory]] from the algebraic perspective of quantum probability is known as _[[perturbative algebraic quantum field theory]]_ ([[pAQFT]]).

The sentiment that [[quantum physics]] _is_ quantum probability theory is also referred to as the _[[Bayesian interpretation of quantum mechanics]]_ ("QBism").

## Properties

### As classical probability theory internal to a Bohr topos
 {#AsClassicalProbabilityInBohrTopos}

The idea that 

> [[quantum probability]] is "just as" classical [[probability theory]] but generalized to [[non-commutative geometry|non-commutative]] [[probability spaces]], hence, for [[quantum physics]], to quantized [[phase spaces]]

may be made precise and fully manifest by understanding quantum probability theory as being classical [[probability theory]] _[[internalization|internal]]_ to the _[[Bohr topos]]_ of the given [[quantum mechanical system]].

For details see at _[[Bohr topos]]_ the section _[Kinematics in a Bohr topos](Bohr+topos#KinematicsOnBohrTopos)_.

For going deeper, see at _[[order-theoretic structure in quantum mechanics]]_.

### Conditional expectation and Wave function collapse
 {#ConditionalExpectationAndWaveFunctionCollapse}

Quantum probability theory shows that "[[wave function collapse]]" is just part of the formula for [[conditional expectation values]] in [[quantum probability theory]] (e.g. [Kuperberg 05, section 1.2](#Kuperberg05), [Yuan 12](#Yuan12)):

Let $(\mathcal{A},\langle -\rangle)$ be a [[quantum probability space]], hence a [[complex numbers|complex]] [[star algebra]] $\mathcal{A}$ of [[quantum observables]], and a [[state on a star-algebra]] $\langle -\rangle \;\colon\; \mathcal{A} \to \mathbb{C}$.

This means that for $A \in \mathcal{A}$ any [[observable]], its _[[expectation value]]_ in the given [[state on a star-algebra|state]] is 

$$
  \mathbb{E}(A) \;\coloneqq\;  \langle A \rangle \in \mathbb{C}
  \,.
$$

More generally, if $P \in \mathcal{A}$ is a [[real part|real]] [[idempotent]]/[[projector]]

$$
  \label{RealIdempotent}
  P^\ast = P
  \,,
  \phantom{AAA}
  P P = P
$$

thought of as an event, then for any observable $A \in \mathcal{A}$ the [[conditional expectation value]] of $A$, conditioned on the observation of $P$, is (e.g. [Redei-Summers 06, section 7.3](#RedeiSummers06), see also [Fröhlich-Schubnel 15, (5.49)](#FroehlichSchubnel15), [Fröhlich 19 (45)](#Froehlich16))


$$
  \label{ConditionalExpectation}
  \mathbb{E}(A \vert P)
  \;\coloneqq\;
  \frac{
    \left \langle P A P \right\rangle
  }{
    \left\langle P \right\rangle
  }
  \,.
$$

Now assume a [[star-representation]] $\rho \;\colon\; \mathcal{A} \to End(\mathcal{H})$ of the [[algebra of observables]] by [[linear operators]] on a [[Hilbert space]] $\mathcal{H}$ is given, and that the state $\langle -\rangle$ is a [[pure state]], hence given by an [[vector]] $\psi \in \mathcal{H}$ ("[[wave function]]") via the [[Hilbert space]] [[inner product]] $\langle (-), (-)\rangle \;\colon\; \mathcal{H} \otimes \mathcal{H} \to \mathbb{C}$ as 

$$
  \begin{aligned}
    \langle A \rangle
    & \coloneqq
    \left\langle\psi
      \vert A \vert \psi
    \right\rangle
    \\
    & \coloneqq
    \left\langle\psi,
      A \psi
    \right\rangle
  \end{aligned}
  \,.
$$

In this case the expression for the [[conditional expectation value]] (eq:ConditionalExpectation) of an observable $A$ conditioned on an idempotent observable $P$ becomes (notationally suppressing the [[representation]] $\rho$)

$$
  \begin{aligned}
    \mathbb{E}(A\vert P)
    & =
    \frac{
      \left\langle
        \psi \vert P A P\vert \psi
      \right\rangle
    }{
      \left\langle 
        \psi \vert P \vert \psi
      \right\rangle
    }
    \\
    & = 
    \frac{
      \left\langle 
        P \psi \vert A \vert P \psi
      \right\rangle
    }{
     \left\langle 
        P \psi \vert P \psi 
     \right\rangle
    }  
    \,,
  \end{aligned}
$$

where in the last step we used (eq:RealIdempotent).

This says that _assuming_ that $P$ has been observed in the [[pure state]] $\vert \psi\rangle$, then the corresponding [[conditional expectation values]] are the same as actual [[expectation values]] but for the new pure state $\vert P \psi \rangle$.

This is the statement of "[[wave function collapse]]": 

$$
  \vert \psi \rangle \mapsto P \vert \psi \rangle
  \,.
$$


The original [[wave function]] is $\psi \in \mathcal{H}$, and after observing $P$ it "collapses" to $P \psi \in \mathcal{H}$ (up to normalization).



## Related concepts

* [[noncommutative measure theory]]

* [[probability amplitude]]

* [[quantum statistical mechanics]]

* [[quantum information theory]], [[quantum mechanics]]

* [[Bell's inequalities]]

* [[Bayesian interpretation of quantum mechanics]]

* [[quantum logic]]

* [[Bohr topos]]

[[!include states and observables -- content]]


## References

The understanding of [[quantum physics]] as a [[probability theory|probabilistic]] [[theory (physics)|theory]] originates with the formulation of the [[Born rule]] and was made fully explicit in:

* [[Pascual Jordan]], *Über eine neue Begründung der Quantenmechanik*, Zeitschrift für Physik **40** (1927) 809–838 &lbrack;[doi:10.1007/BF01390903](https://doi.org/10.1007/BF01390903)&rbrack;

* {#vonNeumann32} [[John von Neumann]], *Die quantenmechanische Statistik*, Part III in:

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

see also:

* [[Jagdish Mehra]], Helmut Rechenberg, *The Probability Interpretation and the Statistical Transformation Theory, the Physical Interpretation, and the Empirical and Mathematical Foundations of Quantum Mechanics 1926-1932*, Part 1 in:  *The Historical Development of Quantum Theory. Volume 6: The Completion of Quantum Mechanics, 1926-1941*, Springer (2001)   &lbrack;[ISBN:978-0-387-98971-6](https://link.springer.com/book/9780387989716)&rbrack;

with emphasis on [[POVMs]]:

* [[Paul Busch]], Marian Grabowski, [[Pekka J. Lahti]], *Operational Quantum Physics*, Lecture Notes in Physics Monographs **31**, Springer (1995) &lbrack;[doi:10.1007/978-3-540-49239-9](https://doi.org/10.1007/978-3-540-49239-9)&rbrack;

* [[Paul Busch]], [[Pekka J. Lahti]], Juha-Pekka Pellonpää, Kari Ylinen, *Quantum Measurement*, Springer (2016) &lbrack;[doi:10.1007/978-3-319-43389-9](https://doi.org/10.1007/978-3-319-43389-9)&rbrack;

The axiomatization of [[probability theory]] in terms of the concept of [[expectation values]] (instead of [[probability measures]]) is amplified in:

* [vonNeumann 1932, §IV.1](#vonNeumann32)

* {#Segal65} [[Irving Segal]]: _Algebraic integration theory_ Part 1, Bull. Amer. Math. Soc. **71** 3 (1965) 419-489 &lbrack;[euclid:1183526903](https://projecteuclid.org/euclid.bams/1183526903)&rbrack;

* {#Whittle92} [[Peter Whittle]], _Probability via expectation_, Springer 1992 ([doi:10.1007/978-1-4612-0509-8](https://link.springer.com/book/10.1007/978-1-4612-0509-8))

* [[Rolando Rebolledo]], *An algebraic view on Probability*, Section 1.2 in: *Complete Positivity and the Markov structure of Open Quantum Systems*, chapter in: [[Stéphane Attal]], [[Alain Joye]], [[Claude-Alain Pillet]] (eds.), *Open Quantum Systems II -- The Markovian approach*,  Lecture Notes in Mathematics **1881**, Springer (2006) 149-182 &lbrack;[doi:10.1007/b128451](https://doi.org/10.1007/b128451)&rbrack;


Dedicated discussion of quantum probability theory:

* [[Itamar Pitowsky]], *Quantum Probability -- Quantum Logic*, Lecture Notes in Physics **321**, Springer (1989) &lbrack;[doi:10.1007/BFb0021186](https://doi.org/10.1007/BFb0021186)&rbrack;

  > (emphasis on the [[Bell's inequalities]] and [[quantum logic]])

* {#Meyer95} [[Paul-André Meyer]], *Quantum Probability for Probabilists*,  Lecture Notes in Mathematics **1538**, Springer 1995 ([doi:10.1007/BFb0084701](https://link.springer.com/book/10.1007/BFb0084701))

* [[Hans Maassen]], _Quantum Probability Theory_, Lecture notes 1998 ([pdf](https://www.math.ru.nl/~maassen/lectures/qp.pdf), [[MaassenQuantumProbability.pdf:file]])

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_ (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf), [[Kuperberg-ConciseQuantum.pdf:file]]&rbrack;

* {#RedeiSummers06} [[Miklos Redei]], [[Stephen Summers]], _Quantum Probability Theory_, Studies in History and Philosophy of Science Part B: Studies in History and Philosophy of Modern Physics Volume 38, Issue 2, June 2007, Pages 390-417 ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158), [doi:10.1016/j.shpsb.2006.05.006](https://doi.org/10.1016/j.shpsb.2006.05.006))

* {#Attal} [[Stéphane Attal]], *Quantum Probability*, Lecture 7 in:  *Lectures on Quantum Noises* &lbrack;[pdf](http://math.univ-lyon1.fr/~attal/Quantum_Probability.pdf), [webpage](http://math.univ-lyon1.fr/~attal/chapters.html)&rbrack;

* [[Franco Strocchi]], Section 2.4 in: *An introduction to the mathematical structure of quantum mechanics*, Advanced Series in Mathematical Physics **28**, World Scientific (2008) &lbrack;[doi:10.1142/7038](https://doi.org/10.1142/7038)&rbrack;


* {#Gleason09} [[Jonathan Gleason]], *The $C^*$-algebraic formalism of quantum mechanics* (2009) &lbrack;[[Gleason09.pdf:file]], [[GleasonAlgebraic.pdf:file]]&rbrack;

* {#Gleason11} [[Jonathan Gleason]], *From Classical to Quantum: The $F^\ast$-Algebraic Approach*, contribution to *[VIGRE REU 2011](http://www.math.uchicago.edu/~may/VIGRE/VIGREREU2011.html)*, Chicago (2011) &lbrack;[pdf](https://www.math.uchicago.edu/~may/VIGRE/VIGRE2011/REUPapers/Gleason.pdf), [[GleasonFAlgebraic.pdf:file]]&rbrack;


* [[Qiaochu Yuan]], _[Noncommutative probability](https://qchu.wordpress.com/2012/08/18/noncommutative-probability/)_, 2012

* {#Yuan12} [[Qiaochu Yuan]], _[Finite noncommutative probability, the Born rule, and wave function collapse](https://qchu.wordpress.com/2012/09/09/finite-noncommutative-probability-the-born-rule-and-wave-function-collapse/)_, 2012

* A. Ibort, V.I. Manko, G. Marmo, A. Simoni, F. Ventriglia, _A pedagogical presentation of a $C^\ast$-algebraic approach to quantum tomography_, Phys. Scr., 84 (2011) 065006 ([arXiv:1204.5231](https://arxiv.org/abs/1204.5231))

* {#FroehlichSchubnel15} [[Jürg Fröhlich]],  B. Schubnel, _Quantum Probability Theory and the Foundations of Quantum Mechanics_. In: Blanchard P., Fröhlich J. (eds.) _The Message of Quantum Science_. Lecture Notes in Physics, vol 899. Springer 2015 ([arXiv:1310.1484](https://arxiv.org/abs/1310.1484), [doi:10.1007/978-3-662-46422-9_7](https://doi.org/10.1007/978-3-662-46422-9_7))

* {#Froehlich16} [[Jürg Fröhlich]], _The structure of quantum theory_, Chapter 6 in _The quest for laws and structure_, EMS 2016  ([doi](https://www.researchgate.net/publication/308595814_The_Quest_for_Laws_and_Structure), [doi:10.4171/164-1/8](https://www.ems-ph.org/books/show_abstract.php?proj_nr=207&vol=1&rank=8))

* [[Jan Swart]], _Introduction to Quantum Probability_, 2017 ([pdf](http://staff.utia.cas.cz/swart/dict.pdf), [[SwartQuantumProbability.pdf:file]])

* {#Landsman17} [[Klaas Landsman]], _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([doi:10.1007/978-3-319-51777-3](https://link.springer.com/book/10.1007/978-3-319-51777-3), [pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))

Further discussion of quantum probability:

* [[Dror Bar-Natan]], *Two examples in noncommutative probability*, Foundations of Physics, **19** (1989) 97–104  ([doi:10.1007/BF00737769](https://doi.org/10.1007/BF00737769))
    

* Nicolò Drago, [[Valter Moretti]], _The notion of observable and the moment problem for $\ast$-algebras and their GNS representations_ ([doi:1903.07496](https://arxiv.org/abs/1903.07496), [spire:1725528](http://inspirehep.net/record/1725528))

Discussion of [[density matrices]], [[quantum entanglement]] and [[entropy]] in quantum probability/[[algebraic quantum field theory|algebraic quantum theory]], via the [[GNS construction]]:

* [[A. P. Balachandran]], T. R. Govindarajan, Amilcar R. de Queiroz, A. F. Reyes-Lega, Section II of: *Algebraic approach to entanglement and entropy*, Phys. Rev. A **88** (2013) 022301  &lbrack;[arXiv:1301.1300](http://arxiv.org/abs/1301.1300), [doi:10.1103/PhysRevA.88.022301](https://doi.org/10.1103/PhysRevA.88.022301)&rbrack;

* [[A. P. Balachandran]], A. R. de Queiroz, S. Vaidya, *Entropy of Quantum States: Ambiguities*, Eur. Phys. J. Plus **128** (2013) 112 &lbrack;[arXiv:1212.1239](https://arxiv.org/abs/1212.1239), [doi:10.1140/epjp/i2013-13112-3](https://doi.org/10.1140/epjp/i2013-13112-3)&rbrack;


* Paolo Facchi, Giovanni Gramegna, Arturo Konderak, *Entropy of quantum states* ([arXiv:2104.12611](https://arxiv.org/abs/2104.12611))


[[!redirects quantum probability theories]]

[[!redirects quantum probability]]
[[!redirects quantum probabilities]]


[[!redirects quantum probability space]]
[[!redirects quantum probability spaces]]

[[!redirects noncommutative probability]]
[[!redirects noncommutative probabilities]]
[[!redirects non-commutative probability]]
[[!redirects non-commutative probabilities]]

[[!redirects noncommutative probability space]]
[[!redirects noncommutative probability spaces]]
[[!redirects non-commutative probability space]]
[[!redirects non-commutative probability spaces]]

[[!redirects noncommutative probability theory]]
[[!redirects noncommutative probability theories]]
[[!redirects non-commutative probability theory]]
[[!redirects non-commutative probability theories]]
