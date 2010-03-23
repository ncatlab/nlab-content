
## Open systems and reversibility

Consider two quantum systems, Q and E where Q is some system of interest and E is some system that is external to Q and that is in some fixed [[pure state]] $|e\rangle$.  Now let us suppose that the two systems interact and evolve via some [[unitary operator]] on the combined [[Hilbert space]] of each, $\mathcal{H}^{(QE)}$.  In this situation Q is known as an _open system_ and E is the _environment_.

The dilation construction of quantum states (see Stinespring's dilation theorem above), i.e. in the quantum operation formalism, the evolution of a system is often written in a more condensed manner as

$\rho^{\prime}=\varepsilon (\rho)$.

Here we refer to $\varepsilon (\rho)$ as a _superoperator_.

+-- {: .un_theorem}
###### Lemma
Suppose $\varepsilon$ is a linear map on Q-operators.  Then the following three conditions are equivalent:

* $\varepsilon$ represents a "physically reasonable" evolution for density operators on Q.
* $\varepsilon$ is given by unitary evolution on an extended system as in the quantum operation formalism.
* $\varepsilon$ has a Kraus decomposition with normalized Kraus operators as in the quantum channel formalism.

=--

+-- {: .proof}
###### Proof
This is proven in Appendix D of

* Schumacher, Benjamin and Westmoreland, Michael, _Q-PSI: Quantum Processes, Systems, and Information_, Cambridge University Press, Cambridge, 2010

where there is also an explanation of "physically reasonable."

=--

+-- {: .query}
[[Ian Durham]]: Is there a convenient category theoretic way to prove the above lemma?
=--

[[!redirects open quantum systems]]