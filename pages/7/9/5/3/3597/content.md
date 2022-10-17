
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

In [[quantum mechanics]] a _density matrix_ is a linear endomorphism of a [[Hilbert space]] of pure [[quantum states]] that represents a [[statistical ensemble]] of [[quantum states]], hence [[state on a star-algebra|states]] which are not necessarily [[pure states]] but [[mixed states]].

The space of density matrices inside all suitable endomorphisms is called the _[[Bloch region]]_.


## Notation

In the following definition, we use Dirac's "bra-ket" notation for vectors where a state vector, describing a [[pure state]] of a quantum system, is represented by a "ket" which is a column vector,

$$ {|\psi_{\alpha}\rangle} = \left(
\begin{aligned}
\vdots \\
x_{n-1} \\
x_{n} \\
x_{n+1} \\
\vdots
\end{aligned}
\right) .$$

The [[Hermitian adjoint]], ${\langle\psi_{\alpha}|} = ({|\psi_{\alpha}\rangle})^{\dagger}$, is called a "bra" (hence "bra(c)ket") and is a row vector.


## The density operator of an ensemble

Suppose we have a [[quantum state]] $Q$ that arises from some random process such that the state ${|\psi_{\alpha}\rangle}$ has a probability $p_{\alpha} \in [0,1]$ (we often speak of having 'prepared' the state with the associated probability).  The possible states ${|\psi_{\alpha}\rangle}$ need not be orthogonal and we thus call such a collection of states a *[[mixed state]]*.  More specifically, a mixed state is often described as an *[[ensemble]]* of quantum systems.

Suppose we now measure some observable $\mathbf{A}$ on the system as a whole, i.e. on the ensemble.  The expectation value of $\mathbf{A}$ over the state ${|\psi_{\alpha}\rangle}$ is $\langle{A}\rangle_{\alpha} = \langle\psi_{\alpha} | \mathbf{A} |\psi_{\alpha}\rangle$.  Over the entire ensemble, this becomes

$$ \langle{A}\rangle = \sum_{\alpha} p_{\alpha} \langle{A}\rangle_{\alpha} = \sum_{\alpha} p_{\alpha} tr {|\psi_{\alpha}\rangle} {\langle\psi_{\alpha}|} \mathbf{A} .$$

Given the above, we define the __density operator__ to be

$$ \mathbf{\rho} = \sum_{\alpha} \rho_\alpha {|\psi_{\alpha}\rangle}{\langle\psi_{\alpha}|} .$$

We call the [[matrix]] representation of the density operator, relative to a given [[basis]], the __density matrix__.

## Characterisation

An operator $\rho$ is the density operator associated to some ensemble if and only if it is a positive operator with trace 1.  (Nielsen and Chuang Theorem 2.5, p. 101)

## Coherence

Diagonal density matrices with at least two non-zero terms on the diagonal represent *[[mixed state]]s*.  Density matrices that possess non-zero off-diagonal terms represent *[[superposition state]]s*.  Such states are referred to as *coherent* and the off-diagonal entries are called the *coherences*.  Any physical process that has the effect of suppressing the coherences is known as *[[decoherence]]*.


## Limitations

Note that a density operator, as the representation of the state of a quantum system, is less restrictive than a state vector which specifies the wavefunction.  On the other hand, two different state vectors can give rise to the same density operator. However, in that case, the two vectors are the same up to a phase, so arguably the density operator still describes the [[physical state]] unambiguously.

More controversially, two entirely different probabilisitic combinations of state vectors can give rise to the same density operator. [[Roger Penrose]], for one, has argued that this means that that the density operator does not describe mixed states unambiguously. But one can also argue the reverse: that mixed states with the same operator really are the same physical state, since they are observationally indistinguishable.

## Related concepts

* [[quantum operation]]

* [[quantum computation]]

[[!include states and observables -- content]]



## References

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §2.4 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;



* [[Benjamin Schumacher]], [[Michael Westmoreland]], §8 of:  *Quantum Processes, Systems, and Information*, Cambridge University Press (2010) &lbrack;[doi:10.1017/CBO9780511814006](https://doi.org/10.1017/CBO9780511814006)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], § 1.4 of: *A concise introduction to quantum probability, quantum mechanics, and quantum computation* (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf)&rbrack;

On [[quantum circuits]] with density matrices:

* [[Dorit Aharonov]], [[Alexei Kitaev]], [[Noam Nisan]], *Quantum Circuits with Mixed States*, *Proceedings of the Thirtieth Annual ACM Symposium on Theory of Computation (STOC)* (1998) 20-30 &lbrack;[arXiv:quant-ph/9806029](https://arxiv.org/abs/quant-ph/9806029), [doi:10.1145/276698.276708](https://doi.org/10.1145/276698.276708)&rbrack;


[[!redirects density matrix]]
[[!redirects density matrixes]]
[[!redirects density matrices]]

[[!redirects density operator]]
[[!redirects density operators]]

[[!redirects mixed state]]
[[!redirects mixed states]]

[[!redirects mixed quantum state]]
[[!redirects mixed quantum states]]


