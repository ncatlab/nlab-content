
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--


\tableofcontents


## Preface 
 {#Preface}

The sections to follow give a summary of the account in [Barandes 2025](#Barandes2025). As a brief preview, here is the gist of what is going on: 

For a finite (physical) system with $N \in \mathbb{N}$ states, a one-step random evolution is given by a [[stochastic matrix]] $(P_{i j})_{i, j =1}^N$ whose entry $P_{i j} \in [0,1]$ gives the [[probability]] that the system, if in state $j$, evolves to state $i$. 

Assuming there is a (temporal) [[sequence]] of such one-step random evolutions then these [[stochastic matrices]] depend on a [[pair]] of (time) parameters $t_1 \geq t_0 \in \mathbb{R}$. 

Say that the [[stochastic process]] defined thereby is *divisible* iff these matrices of transition probabilities  over some (time) interval are the [[matrix multiplication|matrix product]] $(-) \cdot (-)$ over those associated with any decomposition of the interval:

$$ 
  \text{decomposable}
  \;\;\;\;
  \Leftrightarrow
  \;\;\;\;
  \forall_{t_1 \leq t \leq t_0}
  \;\;
  P(t_1, t_0) = P(t_1, t) \cdot P(t, t_0)
  \,.
$$

Now, if these transition probabilities $P$ are given by the rules of coherent time-evolution of [[pure states|pure]] [[quantum states]] according to [[quantum mechanics]], then:

1. the *[[Born rule]]* says that the probabilities are [[norm]]-squares

   $$
     P_{i j} = \vert\Theta_{i j}\vert^2
   $$

   of [[complex numbers]] known as *[[probability amplitudes]]* and traditionally denoted as on the right here:

   $$
     \begin{aligned}
       \Theta_{i j} 
         & = \langle i \vert \Theta \vert j \rangle
       \\
       P_{i j}
         & = 
          \langle i \vert \Theta \vert j \rangle
          \,
          \langle j \vert \Theta^\dagger \vert i \rangle
     \end{aligned}
   $$

   (where traditionally one writes "$U$" for where Barandes has "$\Theta$"),

1. (what is essentially) the [[Schrödinger equation]] says that it is these [[probability amplitudes]] that compose under [[matrix multiplication]]:

   $$
     \forall_{t_0 \leq t \leq t_1}
     \;\;
     \Theta(t_1, t_0) = \Theta(t_1, t) \cdot \Theta(t, t_0) 
     \,.
   $$ 

But with the probability amplitudes $\Theta$ composing according to matrix multiplication, then in general the corresponding (doubly) stochastic matrices $P$ of transition probabilities will clearly *not* compose by the rules of matrix multiplication.

In conclusion: The stochastic processes given by quantum processes are generically *indivisible*.

That seems to be the key point highlighted by [Barandes 2025](#Barandes2025) (without maybe explicitly saying so).



## Idea

The indivisible [[stochastic process]] interpretation of [[quantum mechanics]]
proposes that quantum systems can be understood as [[stochastic processes]] that lack the "Markov property," meaning they cannot be broken down into independent, sequential steps. Instead, they evolve over finite chunks of time through a more general, non-Markovian, stochastic law. This interpretation, developed by [[Jacob Barandes]], suggests that the core features of [[quantum mechanics]], such as [[quantum interference]], [[decoherence]], and [[entanglement]] are an artifact of the indivisible dynamics of the underlying indivisible [[stochastic processes]] being approximated by Markovian dynamics in the Hilbert space formalism of [[quantum mechanics]]. 


## Definitions and the stochastic-quantum correspondence 

Let $\Omega$ be a [[measurable space]] which we interpret as the space of all possible configurations of some system, and let $T$ denote an interval of time starting at $0$.  An indivisible real-time [[stochastic process]] on $\Omega$ consists of a family of morphisms in the [[Kleisli category]] of the [[Giry monad]] $G$,
$$
\Omega_0 \xrightarrow{\Gamma_t} \Omega_t
$$
where $\Omega_t$ is a copy of $\Omega$ at time $t \in T$. These [[Markov kernels]] $\Gamma_t$ are defined as functions
$$
\begin{array}{ccc}
\Omega_0 \times \Sigma_{\Omega_t} & \xrightarrow{\Gamma_t} & [0,1] \\
(\omega, U) & \mapsto & \Gamma_t(U | \omega)
\end{array}
$$
which we read as ''the probability of $\Gamma_t$ on the measurable set $U$ given the point $\omega \in \Omega_0$''.  For each fixed $\omega \in \Omega_0$ the function $\Gamma_t(\bullet | \omega)$ defines a probability measure on $\Omega_t$ ($\Gamma_t(\bullet | \omega) \in G(\Omega_0)$), and for each fixed $U \in \Sigma_{\Omega_t}$ the function $\Omega_0 \xrightarrow{\Gamma_t(U | \bullet)} [0,1]$ is a measurable function.
 
To say that the stochastic process is indivisible means that for any $0 \lt s \lt t$ there exists no morphism $\Omega_s \xrightarrow{ \Gamma_{t,s}} \Omega_t$ in the [[Kleisli category]] of the [[Giry monad]] $G$ such that $\Gamma_t = \Gamma_{t,s} \circ \Gamma_s$ where the composition in the [[Kleisli category]] is defined by $(\Gamma_{t,s} \circ \Gamma_s)(U | \omega) = \int_{\lambda \in \Omega_s} \Gamma_{t,s}(U | \lambda) \, d\Gamma_s(\bullet | \omega)$. 

The stochastic-quantum correspondence assumes the configuration (or "state'') space $\Omega$ is a countable [[measurable space]] with the discrete $\sigma$-algebra. Here we assume $\Omega$ is finite, say $|\Omega| = N$.  It follows that every singleton set $\{i\} \subset \Omega_t$ is measurable, and hence the morphism $\Gamma_t$ is completely determined by the values $\Gamma_t(\{i\} | j)$ which represent the transition probability from the state $j$ at time $0$ to the state $i$ at time $t$. 
 Since $\Omega$ is finite the morphisms $\Gamma_t$ in the [[Kleisli category]] of $G$ can be representated as an $N \times N$ matrix, and the composition in the [[Kleisli category]] reduces to just matrix multiplication.  Let $\Gamma(t)$ denote the matrix whose component at row $i$ and column $j$ is $\Gamma_t(\{i\}|j)$, and denote that component of $\Gamma(t)$ by $\Gamma_{i,j}(t)$. 

Let us now proceed, from the indivisible [[stochastic process]] specified by the laws $\Gamma(t)$, to a [[Hilbert space]] formulation of that same process. Since $\Gamma_{i,j}(t) \in [0,1]$ we can introduce an $N \times N$ __potential matrix__ $\Theta(t)$ consisting of complex-valued matrix elements $\Theta_{i,j}(t)$ related to $\Gamma_{i,j}(t)$ by the modulus squared relation
$$
\Gamma_{i,j}(t) = |\Theta_{i,j}(t)|^2.
$$
The matrix $\Theta(t)$ is not unique.  Let  $P_i = diag(0,\ldots,1,0,\ldots,0)$ denote the $N \times N$ diagonal matrix with value one at row $i$ and column $i$.  We can represent the elements $\Gamma(t)$ as the trace of the composite of four matrices,
$$
\Gamma_{i,j}(t) = tr( \Theta^{\dagger}(t) P_j \Theta(t) P_i )
$$
where $\Theta^{\dagger}(t)$ is the [[conjugate transpose matrix]] of $\Theta(t)$. We call this equation the __dictionary formula__ as it  provides the translation between indivisible [[stochastic processes]], as represented by the left-hand side, and the formalism of quantum-theoretic [[Hilbert spaces]] as represented on the right-hand side.  This dictionary formula is the basic ingredient of the stochastic-quantum correspondence.

Given an initial probability measure $p(0)$ on $\Omega_0$ with components $p_j(0)$ we can define the __density matrix__ $\rho(0) = diag(p_1(0),p_2(0),\ldots,p_N(0))$. We then define a time-dependent density matrix by
$$
\rho(t) = \Theta(t) \rho(0) \Theta^{\dagger}(t)
$$
which is not generally diagonal, but is self-adjoint, positive semi-definite, and has trace equal to one.

Provided the density matrix is of rank one we can write the density matrix as the outer product of an $N \times 1$ column vector $\Psi(t)$ and its complex-conjugate-transpose (adjoint)
$$
\rho(t) = \Psi^{\dagger}(t) \Psi(t). 
$$
The __state vector__ or __wave function__ $\Psi(t)$ then evolves over time according to
$$
\Psi(t) = \Theta(t) \Psi(0),
$$
and $\Psi(t)$ satisfies the property $||\Psi(t)||=1$.
Thus we have derived the [[Hilbert space]] viewpoint of the [[stochastic process]].  This procedure can be reversed using the dictionary formula.

 For this brief overview of the stochastic-quantum correspondence we have ignored the measurement aspect as measurements cannot be modeled for [[stochastic processes]] within the [[Kleisli category]] of the [[Giry monad]] $G$. (They can however be modeled within the larger category of the category of algebras of the monad $G$. See Example 1 in [[stochastic processes]].)


## Interpretations

Being developed: How  [[quantum interference]], [[decoherence]], [[entanglement]] arise within the framework of indivisible [[stochastic processes]].

## History

The development of the indivisible stochastic interpretation of quantum systems is due to [[Jacob Barandes]].


## Related concepts

* [[The Interpretation of Quantum Mechanics]]
* SEP: [Copenhagen interpretation of qm](http://plato.stanford.edu/entries/qm-copenhagen)

* SEP: [qm:collapse theories](http://plato.stanford.edu/entries/qm-collapse),

* SEP: [many-world interpretation of qm](http://plato.stanford.edu/entries/qm-manyworlds), 

* SEP: [modal-interpretations of qm](http://plato.stanford.edu/entries/qm-modal)

* SEP: [Everett's relative-state formulation of qm](http://plato.stanford.edu/entries/qm-everett)

* [[hidden variable theory]]

  * [[Bohmian mechanics]] 


## References

The development of the indivisible stochastic process interpretation is based upon the following three articles:

* {#Barandes2025} [[Jacob Barandes]], *Quantum Systems as Indivisible Stochastic Processes* &lbrack;[arXiv:2507.21192](https://arxiv.org/abs/2507.21192)&rbrack;

* [[Jacob Barandes]], *The Stochastic-Quantum Theorem* &lbrack;[arXiv:2309.03085[quant-ph]](https://arxiv.org/abs/2309.03085)&rbrack;

* [[Jacob Barandes]], *The Stochastic-Quantum Correspondence* &lbrack;[arXiv:2302.10778[quant-ph]](https://arxiv.org/abs/2302.10778)&rbrack;

For a discussion of the measurement problem arising in other interpretations of quantum mechanics see

* {#Wallace07} [[David Wallace]], _The Quantum Measurement Problem: State of Play_ ([arXiv:0712.0149](http://arxiv.org/abs/0712.0149))



[[!redirects indivisible stochastic interpretation of quantum mechanics]]
[[!redirects Barandes interpretation of quantum mechanics]]