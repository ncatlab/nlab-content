
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

## Quantum doubles

Given a pure state on the tensor product of Hilbert spaces 
$V\otimes W$, the partial trace $\tr_W$ specifies a mixed state on $V$. Moreover, every mixed state comes from the partial trace of a pure state. Hence, this gives an alternate characterization of what a density matrix is: The image of the "pure state" outer products $|\psi\rangle\langle\psi|$ under partial trace.

Even better, given a density matrix $\rho\in V$ one can explicitly construct a pure state which traces to it. Expand $\rho$ as 

$$\rho=\sum_{\alpha}\rho_\alpha |\psi_\alpha \rangle \langle \psi_\alpha |.$$

The states $| \psi_{\alpha}\rangle$ serve as a basis for $V$, and the states $\langle\psi_\alpha |$ serve as a basis for $V^*$. Hence, we can consider the state

$$\tilde{\rho}=\sum_{\alpha}\sqrt{\rho_\alpha}|\psi_\alpha \rangle\otimes \langle \psi_\alpha |\in V\otimes V^*.$$

Tracing $V^*$ out of $\tilde{\rho}$ allows us to recover $\rho$. This can be seen in the following computation:

$$
\begin{aligned}
\tr_{V^*}(\tilde{\rho} \tilde{\rho}^{\dagger})&=\left(\sum_{\alpha}\sqrt{\rho_\alpha}|\psi_\alpha \rangle\otimes \langle \psi_\alpha |\right)
\otimes \left(\sum_{\alpha}\sqrt{\rho_\alpha}|\psi_\alpha \rangle\otimes \langle \psi_\alpha |\right)^{\dagger}\\
&=\left(\sum_{\alpha}\sqrt{\rho_\alpha}|\psi_\alpha \rangle\otimes \langle \psi_\alpha |\right)
\otimes \left(\sum_{\alpha}\sqrt{\rho_\alpha}\langle\psi_\alpha |\otimes |\psi_\alpha \rangle\right)\\
&=\sum_{\alpha,\beta}\sqrt{\rho_{\alpha}}\sqrt{\rho_{\beta}}|\psi_\alpha \rangle \langle \psi_\beta | \otimes \langle \psi_\alpha | \psi_\beta \rangle\\
&=\sum_{\alpha}\rho_\alpha |\psi_\alpha \rangle \langle \psi_\alpha |=\rho.
\end{aligned}
$$

## Limitations

Note that a density operator, as the representation of the state of a quantum system, is less restrictive than a state vector which specifies the wavefunction.  On the other hand, two different state vectors can give rise to the same density operator. However, in that case, the two vectors are the same up to a phase, so arguably the density operator still describes the [[physical state]] unambiguously.

More controversially, two entirely different probabilisitic combinations of state vectors can give rise to the same density operator. [[Roger Penrose]], for one, has argued that this means that that the density operator does not describe mixed states unambiguously. But one can also argue the reverse: that mixed states with the same operator really are the same physical state, since they are observationally indistinguishable.

## Related concepts

* [[maximally mixed quantum state]]

* [[quantum channel]]

* [[quantum computation]]


[[!include states and observables -- content]]



## References

The notion of density matrices originates with

* {#vonNeumann32} [[John von Neumann]], §IV, §V in:

  *Mathematische Grundlagen der Quantenmechanik*, Springer (1932, 1971) &lbrack;[doi:10.1007/978-3-642-96048-2](https://link.springer.com/book/10.1007/978-3-642-96048-2)&rbrack;

  *Mathematical Foundations of Quantum Mechanics*, Princeton University Press (1955) &lbrack;[doi:10.1515/9781400889921](https://doi.org/10.1515/9781400889921), [Wikipedia entry](https://en.wikipedia.org/wiki/Mathematical_Foundations_of_Quantum_Mechanics)&rbrack;

(in precursor discussion of what later came to be called *[[quantum measurement channels]]*).

Most accounts of [[quantum physics]] discuss density matrices in some form. See for instance:

* [[Jun John Sakurai]], Jim Napolitano, §3.4 in: *Modern Quantum Mechanics*, Cambridge University Press (1985, 1994, 2020) &lbrack;[doi:10.1017/9781108587280](https://doi.org/10.1017/9781108587280), [Wikipedia](https://en.wikipedia.org/wiki/Modern_Quantum_Mechanics)&rbrack;

* [[Chris Isham]], §6.1 in: *Lectures on Quantum Theory -- Mathematical and Structural Foundations*, World Scientific (1995) &lbrack;[doi:10.1142/p001](https://doi.org/10.1142/p001), [ark:/13960/t4xh7cs99](https://archive.org/details/lecturesonquantu0000isha)&rbrack;

In the context of [[quantum computation]]:

* [[Michael A. Nielsen]], [[Isaac L. Chuang]], §2.4 in: *Quantum computation and quantum information*, Cambridge University Press (2000) &lbrack;[doi:10.1017/CBO9780511976667](https://doi.org/10.1017/CBO9780511976667), [pdf](http://csis.pace.edu/~ctappert/cs837-19spring/QC-textbook.pdf), [[NielsenChuangQuantumComputation.pdf:file]]&rbrack;

* [[John Preskill]], §2.3 in: *States and Ensembles*, chapter 2 of: *Quantum Computation*, lecture notes, since 2004 &lbrack;[pdf](http://www.theory.caltech.edu/~preskill/ph219/chap2_15.pdf), [web](http://theory.caltech.edu/~preskill/ph229/)&rbrack;

* {#Kuperberg05} [[Greg Kuperberg]], §1.4 of: *A concise introduction to quantum probability, quantum mechanics, and quantum computation* (2005) &lbrack;[pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf)&rbrack;

In the context of [[entanglement]]:

* [[Ingemar Bengtsson]], [[Karol Życzkowski]], Chapters 8 and 12 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048)&rbrack;


In the context of [[decoherence]]:

* [[Maximilian Schlosshauer]], §2.4 in: *Decoherence and the Quantum-To-Classical Transition*, The Frontiers Collection, Springer (2007) &lbrack;[doi:10.1007/978-3-540-35775-9](https://doi.org/10.1007/978-3-540-35775-9)&rbrack;

In the context of [[open quantum systems]]:

* [[Heinz-Peter Breuer]], [[Francesco Petruccione]], §2.1.3 and Part II of: *The Theory of Open Quantum Systems*, Oxford University Press (2007) &lbrack;[doi:10.1093/acprof:oso/9780199213900.001.0001](https://doi.org/10.1093/acprof:oso/9780199213900.001.0001)&rbrack;


Further:


* [[Franco Strocchi]], pp. 46 in: *An introduction to the mathematical structure of quantum mechanics*, Advanced Series in Mathematical Physics **28**, World Scientific (2008) &lbrack;[doi:10.1142/7038](https://doi.org/10.1142/7038)&rbrack;


* [[Benjamin Schumacher]], [[Michael Westmoreland]], §8 of:  *Quantum Processes, Systems, and Information*, Cambridge University Press (2010) &lbrack;[doi:10.1017/CBO9780511814006](https://doi.org/10.1017/CBO9780511814006)&rbrack;


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

[[!redirects quantum mixed state]]
[[!redirects quantum mixed states]]


