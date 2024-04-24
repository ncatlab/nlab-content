

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

While in [[classical mechanics]] a ([[pure state|pure]]) [[state]] is an [[generalized element|element]] of an [[object]] in a [[cartesian monoidal category]], in contrast in [[quantum mechanics]] a pure state is an element of an object in a non-cartesian [[monoidal category]] (say of [[Hilbert spaces]]). As a result, in quantum mechanics a state of a compound [[physical system]] may not come from a pair of states of the two [[subsystems]], but instead be a nontrivial [[sum]] -- a _[[superposition]]_ -- of such. These non-classical combinations of states of subsystems are called _entangled states_.

## Definition

In [[quantum mechanics]] a [[state]] of a [[physical system]] is represented by a [[vector]] in some ([[Hilbert space|Hilbert]]-)[[vector space]] $H$. If the system is the composite of two [[subsystems]] with state spaces $H_1$ and $H_2$, respectively, then the state space of the total system is the [[tensor product]] $H = H_1 \otimes H_2$. The [[universal property]] of the [[tensor product]] gives a [[bilinear map]]

$$
  p : H_1 \times H_2 \to H_1 \otimes H_2
$$

which sends a pair of states $(\psi_1, \psi_2)$ to their tensor product $\psi_1 \otimes \psi_2$. States in the [[image]] of $p$ are called **product states** or **separable states**. An **entangled state** is a state which is _not_ a product state.


## Examples

Consider two [[quantum systems]], $A$ and $B$, with state vectors $|\Psi^{(A)}\rangle$ and $|\Psi^{(B)}\rangle$ respectively.  The combined state of the system may be described by a single state vector $|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle$.


As an example, suppose that in the basis $\{|0\rangle ,|1\rangle\}$, $|\Psi^{(A)}\rangle = \frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)$.  This can be interpreted as system $A$ being in state $|0\rangle$ with probability 1/2 and state $|1\rangle$ with probability 1/2.  Suppose further that $|\Psi^{(B)}\rangle = |0\rangle$.  Then we have

$|\Psi^{(AB)}\rangle=|\Psi^{(A)}\rangle \otimes |\Psi^{(B)}\rangle=\frac{1}{\sqrt{2}}\left(|0\rangle +|1\rangle\right)\otimes|0\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|10\rangle\right)$.

Such a state is said to be a **product state** because it is "factorable" or equivalently separable, i.e. it can be formed from some combination of individual states in the basis.


Compare the above example to the state

$|\Psi^{(AB)}\rangle=\frac{1}{\sqrt{2}}\left(|00\rangle +|11\rangle\right)$.

This state is not a product state since it cannot be formed from any combination of individual states in the given basis.  Such a state is known as an **entangled state** because it is said to be _non-factorable_ or _non-separable_.  The entangled states discussed above are, in fact, [[pure states]] rather than [[mixed states]] because they cannot be broken down further.  However, there is also a notion of entanglement for mixed states.

## Properties

### LOCC and SLOCC

The following refers to ([Coecke-Kissinger](#CoeckeKissinger)).

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

Its easy to show using the Schur decomposition that there are only two SLOCC-equivalence classes in $\mathbb{C}^2 \otimes \mathbb{C}^2$, namely the product state class and the [[Bell state]] class. Perhaps more surprising is the following result to to Dur, Vidal, and Cirac. [2]

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

## Related concepts

* [[entanglement entropy]]

* [[holographic entanglement entropy]]

* [[short-range entanglement]]

* [[quantum embezzlement]]

* [[tensor network]]

* [[quantum teleportation]]

* [[quantum error correction]]



[[!include states and observables -- content]]


## References

Early discussion of [[composite quantum systems]] and their [[quantum entanglement]]:

* [[Erwin Schrödinger]], *Discussion of Probability Relations between Separated Systems*, Mathematical Proceedings of the Cambridge Philosophical Society, **31** 4 (1935) 555-563 &lbrack;[doi:10.1017/S0305004100013554](https://doi.org/10.1017/S0305004100013554)&rbrack;

Introduction and review:

* [[Teiko Heinosaari]], [[Mário Ziman]], Section 6 of: *The Mathematical Language of Quantum Theory -- From Uncertainty to Entanglement*, Cambridge University Press  (2011) &lbrack;[doi:10.1017/CBO9781139031103]( https://doi.org/10.1017/CBO9781139031103)&rbrack;

* Dagmar Bruss, _Characterizing entanglement_, J. Math. Phys. 43, 4237 (2002) [arXiv:quant-ph/0110078](http://arxiv.org/abs/quant-ph/0110078) [doi](http://dx.doi.org/10.1063/1.1494474)

* [[Ingemar Bengtsson]], [[Karol Życzkowski]], Chapter 15 of: *Geometry of Quantum States --- An Introduction to Quantum Entanglement*, Cambridge University Press (2006) &lbrack;[doi:10.1017/CBO9780511535048](https://doi.org/10.1017/CBO9780511535048)&rbrack;

Extensive survey of the field:

* Ryszard Horodecki, Paweł Horodecki, Michał Horodecki, and Karol Horodecki: *Quantum entanglement*, Rev. Mod. Phys. **81** (2009) 865 &lbrack;[arXiv:quant-ph/0702225](https://arxiv.org/abs/quant-ph/0702225), [doi:10.1103/RevModPhys.81.865](https://doi.org/10.1103/RevModPhys.81.865)&rbrack;

As a notion in [[quantum information theory]]:

* [[John Watrous]], Chapter 6 of: *The Theory of Quantum Information*, Cambridge University Press (2018) &lbrack;[doi:10.1017/9781316848142](https://doi.org/10.1017/9781316848142), [webpage](https://cs.uwaterloo.ca/~watrous/TQI/), [pdf](https://cs.uwaterloo.ca/~watrous/TQI/TQI.pdf)&rbrack;



In relation to *[[correlation]]*:

* {#LuoLuo03} Shun-long Luo, You-feng Luo, *Correlation and Entanglement*, Acta Mathematicae Applicatae Sinica **19** (2003) 581–598 $[$[doi:10.1007/s10255-003-0133-z](https://doi.org/10.1007/s10255-003-0133-z)$]$

and in relation to [[quantum computation]]/[[quantum supremacy]]:

* [[John Preskill]]: *Quantum computing and the entanglement frontier*: pp. 63-80 in: *The Theory of the Quantum World -- Proceedings of the 25th Solvay Conference on Physics*, World Scientific (2013) &lbrack;[arXiv:1203.5813](https://arxiv.org/abs/1203.5813), [doi:10.1142/8674](https://doi.org/10.1142/8674), slides: [pdf](https://simons.berkeley.edu/sites/default/files/docs/394/preskilljohn.pdf)&rbrack;


and in the context of [[entanglement entropy]] of [[topological phases of matter]]:

* [[Bei Zeng]], [[Xie Chen]], [[Duan-Lu Zhou]], [[Xiao-Gang Wen]]: 

  Sec. 1 of of: *[[Quantum Information Meets Quantum Matter]] -- From Quantum Entanglement to Topological Phases of Many-Body Systems*, Quantum Science and Technology (QST), Springer (2019) $[$[arXiv:1508.02595](https://arxiv.org/abs/1508.02595), [doi:10.1007/978-1-4939-9084-9](https://doi.org/10.1007/978-1-4939-9084-9)$]$

Exposition of entanglement as a phenomenon of non-[[Cartesian monoidal category|Cartesian]] [[monoidal categories]]:

* {#Baez04} [[John Baez]], *Quantum Quandaries: a Category-Theoretic Perspective*, in D. Rickles et al. (ed.) *The structural foundations of quantum gravity*, Clarendon Press (2006) 240-265 &lbrack;[arXiv:quant-ph/0404040](https://arxiv.org/abs/quant-ph/0404040), [ISBN:9780199269693](https://global.oup.com/academic/product/the-structural-foundations-of-quantum-gravity-9780199269693)&rbrack;

A discussion in [[quantum mechanics in terms of dagger-compact categories]] is in

* {#CoeckeKissinger} [[Bob Coecke]], [[Aleks Kissinger]], _The compositional structure of multipartite quantum entanglement_ ([arXiv:1002.2540](http://arxiv.org/abs/1002.2540))
 

See also

* W. D&#252;r, G. Vidal, J. I. Cirac, _Three qubits can be entangled in two inequivalent ways_, Phys. Rev. A. __62__, 062314

Discussion in [[quantum optics]]:

* [[Tim Byrnes]], [[Ebubechukwu Ilo-Okeke]], Section 10 of: *Quantum Atom Optics: Theory and Applications to Quantum Technology*, Cambridge University Press 2021 ([arXiv:2007.14601](https://arxiv.org/abs/2007.14601), [CUP](https://www.cambridge.org/core/books/quantum-atom-optics/2D867888B5C666D3A936F1C942C99568))

A connection to algebraic geometry is proposed in 

* Fr&#233;d&#233;ric Holweck, Jean-Gabriel Luque, Jean-Yves Thibon, _Geometric descriptions of entangled states by auxiliary varieties_, J. Math. Phys. __53__, 102203 (2012); [doi](http://dx.doi.org/10.1063/1.4753989)

The following work included the consideration of identical particles into the study of quantum entanglement. In this case, the usage of partial trace may not be suitable and instead subsystems are described in terms of subalgebras. The work is in operator algebraic framework, based on usage of [[GNS construction]] and related to the consideration of von Neumann entropy.

* [[A. P. Balachandran]], [[T. R. Govindarajan]], Amilcar R. de Queiroz, A. F. Reyes-Lega, _Entanglement and particle identity: a unifying approach_, Phys. Rev. Lett. 110, 080503 (2013) [arxiv/1303.0688](http://arxiv.org/abs/1303.0688); _Algebraic approach to entanglement and entropy_, [arxiv/1301.1300](http://arxiv.org/abs/1301.1300); _Entanglement, particle identity and the GNS construction: a unifying approach_ [arxiv/1205.2882](http://arxiv.org/pdf/1205.2882) (earlier, longer version, overlapping with 1303.0688)  

Use of [[homological algebra]] for quantifying entanglement:

* {#Mainiero2019} [[Tom Mainiero]], *Homological Tools for the Quantum Mechanic* (2019) &lbrack;[arXiv:1901.02011](https://arxiv.org/abs/1901.02011), [10.10.11.6/handle/1/1339](http://10.10.11.6/handle/1/1339)&rbrack;


category: physics

[[!redirects entangled state]]
[[!redirects entangled states]]

[[!redirects entangled]]
[[!redirects separable]]

[[!redirects quantum entanglement]]

[[!redirects entangled particles]]