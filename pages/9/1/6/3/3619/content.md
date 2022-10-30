
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
* automatic table of contents goes here
{:toc}

## Product States

Consider two [[quantum systems]], $A$ and $B$, with state vectors $|\Psi^{(A)}\rangle$ and $|\Psi^{(B)}\rangle$ respectively.  The combined state of the system may be described by a single state vector $|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle$.

## Example

As an example, suppose that in the basis $\{|0\rangle ,|1\rangle\}$, $|\Psi^{(A)}\rangle = \frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)$.  This can be interpreted as system $A$ being in state $|0\rangle$ with probability 1/2 and state $|1\rangle$ with probability 1/2.  Suppose further that $|\Psi^{(B)}\rangle = |0\rangle$.  Then we have

$|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle=\frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)\otimes|0\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|10\rangle\right)$.

Such a state is said to be a **product state** because it is "factorable" or equivalently separable, i.e. it can be formed from some combination of individual states in the basis.

## Entangled States

Compare the above example to the state

$|\Psi^{(AB)}\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|11\rangle\right)$.

This state is not a product state since it cannot be formed from any combination of individual states in the given basis.  Such a state is known as an **entangled state** because it is said to be _non-factorable_ or _non-separable_.  Entangled states are, in fact, [[pure states]] rather than [[mixed states]] because they cannot be broken down further.

The formation of entangled states requires an external action that, mathematically, takes the form of some type of unitary operator acting on a product state.  Physically this usually entails interacting systems $A$ and $B$ in some way, e.g. one method for entangling photons is producing them from the same source.

## LOCC and SLOCC

Often if [[multi-party state]]s can be inter-converted via local operations, they are considered to be the same. This can be made formal by the following definition.

+-- {: .num_defn}
###### Definition
Two states $|\Psi\rangle,|\Phi\rangle \in \bigotimes H_i$ are said to be equivalent up to local operations with classical communication (LOCC) if they can be inter-converted by a protocol involving any number of steps where (i) one party applies a local unitary operation $U : H_i \rightarrow H_i$ or (ii) one party sends some classical information to another.
=--

Such a protocol is reversible, so since protocols compose, this generates an equivalence relation. While this removes a good deal of redundancy from the study of entanglement, it is often useful to use an even more course-grained relation.

+-- {: .num_defn}
###### Definition
Two states $|\Psi\rangle,|\Phi\rangle \in \bigotimes H_i$ are said to be equivalent up to stochastic LOCC (SLOCC) if they can be inter-converted _with some non-zero probability_ a protocol involving any number of steps where (i) one party applies a an _arbitrary_ local operation $L : H_i \rightarrow H_i$ or (ii) one party sends some classical information to another.
=--

An example of a local stochastic operation is as follows. Suppose Alice and Bob share a state $|\Psi\rangle \in H_A \otimes H_B$ and Alice wishes to perform some operation $L$. Alice prepares an ancilla qubit $|0\rangle \in \mathbb{C}^2$ and performs a unitary operation 

\[ U : \mathbb{C}^2 \otimes H_1 \rightarrow \mathbb{C}^2 \otimes H_1 \]

on her qubit as well as her part of the state $|\Psi\rangle$. She then measures the ancilla qubit. If she gets an outcome of $|0\rangle$, she has performed some operation $L : H_A \rightarrow H_A$ and if she gets outcome $|1\rangle$ she has performed $L' : H_A \rightarrow H_A$. The probability of Alice successfully performing $L$ is then the probability of getting the outcome of $|0\rangle$ when she performed her measurement.

+-- {: .num_theorem}
###### Theorem
Two states are SLOCC-equivalent iff they can be inter-converted by applying arbitrary invertible local operations (ILOs).
=--

Its easy to show using the Schur decomposition that there are only two SLOCC-equivalence classes in $\mathbb{C}^2 \otimes \mathbb{C}^2$, namely the product state class and the Bell state class. Perhaps more surprising is the following result to to Dur, Vidal, and Cirac. [2]

+-- {: .num_theorem}
###### Theorem
Any genuine tripartite state |$\Psi$> $\in \mathbb{C}^2 \otimes \mathbb{C}^2 \otimes \mathbb{C}^2$ is SLOCC-equivalent to either |W> or |GHZ>;.
=--

By genuine, they mean a state that is not a product of smaller states. The two states are defined as:
\[ |W\rangle = |100\rangle + |010\rangle + |001\rangle
\qquad\qquad
|GHZ\rangle = |000\rangle + |111\rangle
\]

Each of these states yields the structure of a commutative [[Frobenius algebra]]. $|GHZ\rangle$ yields a special CFA and $|W\rangle$ yields an "anti-special" CFA. This structure serves to uniquely identity these states (up to SLOCC) in $\mathbb{C}^2$. [1]


## References

1. Bob Coecke, Aleks Kissinger. The compositional structure of multipartite quantum entanglement. arXiv:1002.2540v1 [quant-ph]
2. W. D&#252;r, G. Vidal, and J. I. Cirac. Three qubits can be entangled in two inequivalent ways. PRA. Vol 62, 062314


[[!redirects entangled state]]
[[!redirects entangled]]
[[!redirects separable]]