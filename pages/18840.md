
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
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

### Conditional expectation and Wave function collapse
 {#ConditionalExpectationAndWaveFunctionCollapse}

There is a close relation between [[wave function collapse]] and [[conditional expectation values]] in [[quantum probability]] (e.g. [Kuperberg 05, section 1.2](#Kuperberg05), [Yuan 12](#Yuan12)):

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

where in the last step we used (eq:ConditionalExpectation).

This says that _assuming_ that $P$ has been observed in the [[pure state]] $\vert \psi\rangle$, then the corresponding [[conditional expectation values]] are the same as actual [[expectation values]] but for the new pure state $\vert P \psi \rangle$.

This is the statement of "[[wave function collapse]]": The original [[wave function]] is $\psi \in \mathcal{H}$, and after observing $P$ it "collapses" to $P \psi \in \mathcal{H}$ (up to normalization).


## Related concepts

* [[probability amplitude]]

* [[quantum statistical mechanics]]

* [[Bayesian interpretation of quantum mechanics]]

* [[quantum logic]]


## References

The axiomatization of [[probability theory]] in terms of the concept of [[expectation values]] (instead of [[probability measures]]) is amplified in

*  {#Segal65} [[Irving Segal]], _Algebraic integration theory_, Bull. Amer. Math. Soc. Volume 71, Number 3, Part 1 (1965), 419-489 ([Euclid](https://projecteuclid.org/euclid.bams/1183526903))

* {#Whittle92} [[Peter Whittle]], _Probability via expectation_, Springer 1992

A good exposition of quantum physics from this perspective is in

* {#Gleason09} Jonathan Gleason, _The $C^*$-algebraic formalism of quantum mechanics_, 2009 ([[Gleason09.pdf:file]], [[GleasonAlgebraic.pdf:file]])

Further introduction to quantum probability theory includes

* {#Kuperberg05} [[Greg Kuperberg]], _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))

* [[Miklos Redei]], [[Stephen Summers]], _Quantum Probability Theory_ ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158))

* {#Attal} S. Attal, _Quantum probability_ ([pdf](http://math.univ-lyon1.fr/~attal/Quantum_Probability.pdf))

* [[Qiaochu Yuan]], _[Noncommutative probability](https://qchu.wordpress.com/2012/08/18/noncommutative-probability/)_, 2012

* {#Yuan12} [[Qiaochu Yuan]], _[Finite noncommutative probability, the Born rule, and wave function collapse](https://qchu.wordpress.com/2012/09/09/finite-noncommutative-probability-the-born-rule-and-wave-function-collapse/)_, 2012

A textbook account is 

* {#Landsman17} [[Klaas Landsman]], _Foundations of quantum theory -- From classical concepts to Operator algebras_, Springer Open 2017 ([pdf](https://link.springer.com/content/pdf/10.1007%2F978-3-319-51777-3.pdf))


[[!redirects quantum probability]]
[[!redirects quantum probabilities]]

[[!redirects quantum probability theory]]
[[!redirects quantum probability theories]]

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
