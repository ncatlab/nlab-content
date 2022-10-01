
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebraic Quantum Field Theory
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the context of [[quantum mechanics]], the **collapse of the wave function**, also known as the **reduction of the wave packet**, is said to occur after [[observation]] or [[measurement]], when a wave function expressed as the sum of [[eigenfunctions]] of the observable is projected randomly onto one of them. Different [[interpretations of quantum mechanics]] understand this process differently.

The perspective associated with the _[[Bayesian interpretation of quantum mechanics]]_ observes (see [below](#RelationToConditionalExpectationValues)) that the apparent collapse is just the mathematical reflection of the formula for [[conditional expectation values]] in [[quantum probability theory]].

## Relation to conditional expectation values
 {#RelationToConditionalExpectationValues}

There is a close relation between wave function collapse and [[conditional expectation values]] in [[quantum probability]] (e.g. [Kuperberg 05, section 1.2](#Kuperberg05), [Yuan 12](#Yuan12)):

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

thought of as an event, then for any observable $A \in \mathcal{A}$ the [[conditional expectation value]] of $A$, conditioned on the observation of $P$, is (e.g. [Redei-Summers 06, section 7.3](#RedeiSummers06), see also [Fröhlich-Schubnel 15, (5.49)](#FroehlichSchubnel15), [Fröhlich 19 (45)](Froehlich19))

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

Now assume a [[star-representation]] $\rho \;\colon\; \mathcal{A} \to End(\mathcal{H})$ of the [[algebra of observables]] by [[linear operators]] on a [[Hilbert space]] $\mathcal{H}$ is given, and that the state $\langle -\rangle$ is a [[pure state]], hence given by a [[vector]] $\psi \in \mathcal{H}$ ("[[wave function]]") via the [[Hilbert space]] [[inner product]] $\langle (-), (-)\rangle \;\colon\; \mathcal{H} \otimes \mathcal{H} \to \mathbb{C}$ as 

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

where in the last step we used (eq:ConditionalExpectation).

This says that _assuming_ that $P$ has been observed in the [[pure state]] $\vert \psi\rangle$, then the corresponding [[conditional expectation values]] are the same as actual [[expectation values]] but for the new pure state $\vert P \psi \rangle$.

This is the statement of "wave function collapse"

$$
  \vert \psi \rangle \mapsto P \vert \psi \rangle
  \,.
$$

The original [[wave function]] is $\psi \in \mathcal{H}$, and after observing $P$ it "collapses" to $P \psi \in \mathcal{H}$ (up to normalization).
 

## Related concepts

* [[interpretation of quantum mechanics]]

* [[Bayesian interpretation of quantum mechanics]]

* [[propositions as projections]]

[[!include states and observables -- content]]



## References
 {#References}

Early explicit discussion of wavefunction collapse in [[quantum measurements]], including discussion relating to historical experiments:

* {#vonNeumann32} [[John von Neumann]], §III.3 and §VI of: 

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics* Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

But the formulation in [von Neumann 1932](#vonNeumann32) postulated  that a [[pure state]] would collapse to a [[mixed state]] when the [[quantum observable]]'s [[eigenvalues]] are degenerate. 

This problem was pointed out and the modern formulation of the collapse postulate was formulated by:

* {#Lüders51} [[Gerhart Lüders]]:

  *Über die Zustandsänderung durch den Meßprozeß*, Ann. Phys. **8** (1951) 322–328  &lbrack;[doi:10.1002/andp.19504430510](https://doi.org/10.1002/andp.19504430510)&rbrack;

  *Concerning the state-change due to the measurement process*, Ann. Phys. **15** 9 (2006) 663-670 &lbrack;[pdf](http://myweb.rz.uni-augsburg.de/~eckern/adp/history/historic-papers/2006_518_663-670.pdf), [[Lueders-StateChange.pdf:file]]&rbrack;

Textbook accounts in [[quantum information theory]]:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §2.2.3 of: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[Joseph M. Renes]], eq. (3.2) in: *Quantum Information Theory* (2015) &lbrack;[pdf](https://edu.itp.phys.ethz.ch/hs15/QIT/renes_lecture_notes14.pdf)&rbrack;, (A.2) in: De Gruyter (2022) &lbrack;[doi:10.1515/9783110570250](https://doi.org/10.1515/9783110570250)&rbrack;



Discussion from the point of view of [[quantum probability]] includes

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))

* {#RedeiSummers06} [[Miklos Redei]], [[Stephen Summers]], _Quantum Probability Theory_ ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158))

* {#Yuan12} [[Qiaochu Yuan]], _[Finite noncommutative probability, the Born rule, and wave function collapse](https://qchu.wordpress.com/2012/09/09/finite-noncommutative-probability-the-born-rule-and-wave-function-collapse/)_, 2012

* {#FroehlichSchubnel15} [[Jürg Fröhlich]],  B. Schubnel, _Quantum Probability Theory and the Foundations of Quantum Mechanics_. In: Blanchard P., Fröhlich J. (eds.) _The Message of Quantum Science_. Lecture Notes in Physics, vol 899. Springer 2015 ([arXiv:1310.1484](https://arxiv.org/abs/1310.1484), [doi:10.1007/978-3-662-46422-9_7](https://doi.org/10.1007/978-3-662-46422-9_7))

* {#Froehlich16} [[Jürg Fröhlich]], _The structure of quantum theory_, Chapter 6 in _The quest for laws and structure_, EMS 2016  ([doi](https://www.researchgate.net/publication/308595814_The_Quest_for_Laws_and_Structure), [doi:10.4171/164-1/8](https://www.ems-ph.org/books/show_abstract.php?proj_nr=207&vol=1&rank=8))

See also 

* Wikipedia, _[Wave function collapse](https://en.wikipedia.org/wiki/Wave_function_collapse)_

* Wikipedia, _[Born rule](https://en.wikipedia.org/wiki/Born_rule)_

[[!redirects wave function collapse]]
[[!redirects wavefunction collapse]]

[[!redirects collapse of the wave function]]
[[!redirects collapse of the wavefunction]]

[[!redirects Born's rule]]
