
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


# The indivisible stochastic process interpretation of quantum physics
* table of contents
{: toc}



## Idea

Indivisible [[stochastic processes]] generically exhibit all the hallmark empirical features of quantum systems, including [[quantum interference]], [[decoherence]], [[entanglement]], and noncommutative observables.  Moreover an indivisible [[stochastic process]] can replicate all the empirical predictions made by the [[Hilbert space]] formalism for [[quantum mechanics]], while avoiding the famous measurement problem.  Consequently one can view any quantum system as an indivisible stochastic process yielding the indivisible stochastic process interpretation of [[quantum mechanics]].  Going in the other logical direction, one can also represent indivisible stochastic processes in the usual [[Hilbert space]] formalism yielding a bijective correspondence between indivisible stochastic process systems and quantum systems. 


## Formalism 

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
 
To say that the stochastic process is indivisible means that for any $0 \lt s \lt t$ there exists no morphism $\Omega_s \xrightarrow{ \Gamma_{t,s}} \Omega_t$ in the [[Kleisli category]] of the [[Giry monad]] $G$ such that $\Gamma_t = \Gamma_{t,s} \circ \Gamma_s$ where the composition in the [[Kleisli category]] is defined by $(\Gamma_{t,s} \circ \Gamma_s)(U | \omega) = \int_{\lambda \in \Omega_s} \Gamma_{t,s}(U | \lambda) \, d\Gamma_s(\bullet | \omega)$. An indivisible [[stochastic process]] is a very general type of [[stochastic process]] which can exhibit wild behavior because, for any $\epsilon \gt 0$, the two dynamics laws $\Gamma_t$ and $\Gamma_{t+\epsilon}$ need not have any relationship between them.  For example, even if $\Omega$ was a [[standard Borel space]] and for every $U \in \Sigma_{\Omega}$ all the measurable functions $\Omega_0 \xrightarrow{\Gamma_t(U | \bullet)} [0,1]$ and $\Omega_0 \xrightarrow{\Gamma_{t+\epsilon}(U | \bullet)} [0,1]$ were  continuous functions the two probability measures obtained by composition with an initial probability measure on $\Omega_0$, $\mathbf{1} \xrightarrow{P_0} \Omega_0 \xrightarrow{\Gamma_t} \Omega_t$ and $\mathbf{1} \xrightarrow{P_0} \Omega_0 \xrightarrow{\Gamma_{t+\epsilon}} \Omega_{t+\epsilon}$, can vary significantly.  Such a process is in stark contrast to a [[Markov process]] on a [[standard Borel space]] where continuous [[Markov kernels]] yield a continuously varying probability measure on the [[measurable space]] $\Omega$. 

The stochastic-quantum correspondence results [[Jacob Barandes]] presents assumes the configuration space $\Omega$ is a finite [[measurable space]] with the discrete $\sigma$-algebra. Since $\Omega$ is finite, say $|\Omega| = N$, it follows that every singleton set $\{i\} \subset \Omega_t$ is measurable, and hence the morphism $\Gamma_t$ is completely determined by the values $\Gamma_t(\{i\} | j)$ which represent the transition probability from the state $j$ at time $0$ to the state $i$ at time $t$. 
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

 For this brief overview we have ignored the measurement aspect as measurements cannot be modeled for [[stochastic processes]] within the [[Kleisli category]] of the [[Giry monad]] $G$. (They can however be modeled within the larger category of the category of algebras of the monad $G$. See Example 1 in [[stochastic processes]].)

## Remarks
The stochastic-quantum correspondence, derived for the case of a finite configuration space, provide an impetus for searching for a more general characterization which does not depend upon the countability of the configuration space $\Omega$.  This is not an insignificant issue as there are some interesting analogies with finite [[probability spaces]] and other systems which fail to hold for uncountable  [[probability spaces]] with non-atomic probability measure. 
This issue arises because the path required to generalize the results to uncountable spaces is not elementary and needs to be addressed. 


## Interpretations

To be added: interpretations for [[quantum interference]], [[decoherence]], [[entanglement]] within the framework of indivisible [[stochastic processes]].

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

* [[Jacob Barandes]], *Quantum Systems as Indivisible Stochastic Processes* &lbrack;[arXiv:2507.21192](https://arxiv.org/abs/2507.21192)&rbrack;

* [[Jacob Barandes]], *The Stochastic-Quantum Theorem* &lbrack;[arXiv:2309.03085[quant-ph]](https://arxiv.org/abs/2309.03085)&rbrack;

* [[Jacob Barandes]], *The Stochastic-Quantum Correspondence* &lbrack;[arXiv:2302.10778[quant-ph]](https://arxiv.org/abs/2302.10778)&rbrack;

For a discussion of the measurement problem arising in other interpretations of quantum mechanics see

* {#Wallace07} [[David Wallace]], _The Quantum Measurement Problem: State of Play_ ([arXiv:0712.0149](http://arxiv.org/abs/0712.0149))



[[!redirects indivisible stochastic interpretation of quantum mechanics]]
[[!redirects Barandes interpretation of quantum mechanics]]