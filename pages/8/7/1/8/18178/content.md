
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

thought of as an event, then for any observable $A \in \mathcal{A}$ the [[conditional expectation value]] of $A$, conditioned on the observation of $P$, is (e.g. [Redei-Summers 06, section 7.3](#RedeiSummers06))

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

This is the statement of "wave function collapse". The original [[wave function]] is $\psi \in \mathcal{H}$, and after observing $P$ it "collapses" to $P \psi \in \mathcal{H}$ (up to normalization).
 

## Related concepts

* [[interpretation of quantum mechanics]]

* [[propositions as projections]]


## References

Discussion from the point of view of [[quantum probability]] includes

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))

* {#RedeiSummers06} [[Miklos Redei]], [[Stephen Summers]], _Quantum Probability Theory_ ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158))

* {#Yuan12} [[Qiaochu Yuan]], _[Finite noncommutative probability, the Born rule, and wave function collapse](https://qchu.wordpress.com/2012/09/09/finite-noncommutative-probability-the-born-rule-and-wave-function-collapse/)_, 2012


See also 

* Wikipedia, _[Wave function collapse](https://en.wikipedia.org/wiki/Wave_function_collapse)_


[[!redirects wave function collapse]]
[[!redirects wavefunction collapse]]

[[!redirects collapse of the wave function]]
[[!redirects collapse of the wavefunction]]
