<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In [[quantum mechanics]] a _state_ of a physical system with $n \in \mathbb{N}$ degrees of freedom may be thought of as being encoded by a complex [[hermitian matrix|hermitian]] $n \times n$ [[matrix]] $\rho \in Mat(n\times n, \mathbb{C})$ with non-negative [[eigenvalue]]s and unit [[trace]]. This is called a **[[density matrix]]** .

Any physical process is supposed to take physical states into physical states. Hence it must be some operation that sends density matrices to density matrices: it should be a linear map of [[vector space]]s

$$
  U : Mat(n \times n, \mathbb{C}) \to Mat(k \times k, \mathbb{C})
$$

that preserves the subset of density matrices, in that it 

* preserves the trace of matrices;

* takes hermitian matrices with non-negative eigenvalues to hermitian matrices with non-negative eigenvalues.

The relevance of this concept of **(completely) positive trace-preserving maps (CPTP)** apparently became widely recognized due to the article

* Choi, _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

The concept was picked up in the physics literature, where (completely) positive trace-preserving maps are referred to as **quantum operations** or **quantum channels**, reflecting the physical interpretation of these maps: 

Notably in [[quantum information theory]] one thinks of each way to send a signal from one quantum system to another as being modeled by such a map.

A useful review of the notion in this context is in section 1.7 of

* Caleb J. O'Loan, _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

More generally, the definition can be extended in a more-or-less obvious way from systems with a finite number of degrees of freedom, to general systems. This requires replacing the finite dimensional complex vector space $\mathbb{C}^n$ with an arbitrary [[Hilbert space]] $\mathcal{H}$ and the space of matrices by a suitable space of linear operators on that Hilbert space.

## Formalisms
### Quantum Operations

A **quantum operation** is a mathematical formalism that is used to describe a broad class of quantum mechanical transformations.  It differs slightly from the formalism of quantum channels which are described in the next section.  Mathematically, it is a CPTP map $\Phi$ between spaces of trace class operators that, in addition to its CPTP properties, has the property that, for some density operator $\rho$, Tr$(\Phi (\rho))\le 1$.

The notion of a quantum operation is built from **Stinespring's dilation (factorization) theorem** (presented below in the notation most commonly used in quantum mechanics in which $U^{\dagger}$ is the conjugate transpose of $U$).

+-- {: .un_theorem}
###### Stinespring's dilation theorem

Let $T: S_{1}(\mathcal{H}) \to S_{2}(\mathcal{H})$ be a CPTP map between states on a finite-dimensional Hilbert space, $\mathcal{H}$.  Then there exists a Hilbert space $\mathcal{A}$ and a unitary operation $U$ on $\mathcal{H}\otimes\mathcal{A}$ such that

$$
   T(\rho) = Tr_{\mathcal{A}}U(\rho \otimes \rho_{\mathcal{A}})U^{\dagger}
$$

for all $\rho \in S_{n}(\mathcal{H})$, where $Tr_{\mathcal{A}}$ is the [[partial trace]] on the $\mathcal{A}$-system.  We refer to $\mathcal{A}$ as an _ancilla_ system and it is chosen such that dim$\mathcal{A}\le$dim$^{2}\mathcal{H}$.  This representation is unique up to unitary equivalence.

=--

+-- {: .query}
TO DO: Write down the proof (or a sketch of it - it's somewhat long, at least the version I'm familiar with.
=--

This dilation construction of channels and states is commonly termed the "Church of the Larger Hilbert Space" (coined by John Smolin) since it incorporates the Hilbert space of both the state under consideration as well the environment, even though the operation is on the system only in most cases (for an exception, see the discussion of open quantum systems below).  Note that Stinespring's theorem can also be used to show that every [[mixed state]] can be thought of as arising from some [[mixed state|pure state]] on a larger Hilbert space.

#### Example

A very common example of this formalism comes from its use in **open quantum systems** (see below), that is systems that are coupled to an environment.  Let $\rho$ be the state of some quantum system and $\rho_{env}$ be the state of the environment.  The action of a unitary transformation, $U$, on the system is

$$
  T(\rho) = Tr_{env}U(\rho \otimes \rho_{env})U^{\dagger}.
$$

### Quantum Channels

Sometimes it is advantageous (or simply not necessary) to consider the larger Hilbert space.  In such a case we are only interested in the input and output Hilbert spaces of the operation or channel itself.

+-- {: .un_defn}
###### Definition

Let $k,n \in \mathbb{N}$.

A matrix $A \in Mat(n \times n, \mathbb{C})$ is called **positive** if it is hermitian -- if $A^\dagger = A$ -- and if all its eigenvalues (which then are necessarily real) are non-negative.

A linear map (morphism of [[vector space]]s of matrices)

$$
  \Phi : Mat(n \times n, \mathbb{C}) \to 
   Mat(k \times k, \mathbb{C})
$$

is called **positive** if it takes positive matrices to positive matrices.

The map $\Phi$ is called **completely positive** if for all $p \in \mathbb{N}$ the [[tensor product]]

$$
  \Phi \otimes Id_{Mat(p\times p),\mathbb{C}} :
  Mat(n \times n , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
  \to
  Mat(k \times k , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
$$

is positive.

=--

+-- {: .un_theorem}
###### Theorem

A map $\Phi$ as above is _completely positive_ precisely if there exists a [[set]] $I$ and an $I$-family $\{E_i \in Mat(k \times n, \mathbb{C}| i \in I)\}$ of matrices, such that for all $A \in Mat(n \times n, \mathbb{C})$ we have

$$
  \Phi(A) = \sum_{i \in I} E_i A E_i^\dagger
  \,.
$$

Moreover, such $\Phi$ preserves the trace of matrices precisely if 

$$
  \sum_{i \in I} E_i^\dagger E_i = Id_{Mat(n \times n, \mathbb{C})}
  \,.
$$

=--

+-- {: .proof}
###### Proof

This is theorem 1 in 

* Choi, _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

=--

The matrices $\{E_i\}$ that are associated to a completely positive and trace-preserving map by the above theorem are called **Kraus operators**.

In the physics literature the above theorem is then phrased as: _Every quantum channel can be represented using Kraus operators_  .

Notice that the identity map is clearly completely positive and trace preserving, and that the composite of two maps that preserve positivity and trace clearly still preserves positivity and trace. Therefore we obtain a [[category]] $QChan \subset Vect$ -- a [[subcategory]] of [[Vect]]${}_{\mathbb{C}}$ -- whose

* objects are the vector spaces $Mat(n \times n, \mathbb{C})$ for all $n \in \mathbb{N}$;

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.

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

### Discussion

## References

* Choi, M. (1975). _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications 10: 285&#8211;290.

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* Nielsen, Michael and Chuang, Isaac (2000) _Quantum Computation and Quantum Information_, Cambridge University Press, Cambridge.

* O'Loan, Caleb J.,  _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))

The description of completely positive maps in terms of [[dagger-categories]] goes back to

* [[Peter Selinger]], _Dagger-compact closed categories and completely positive maps_ ([ps](http://www.mscs.dal.ca/~selinger/papers/dagger.ps))

* [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 

This was further developed in

* [[Bob Coecke]], [[Eric Paquette]], [[Dusko Pavlovic]], _Classical and quantum structures_ ([pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf))

A recent presentation on this:

* [[Ian Durham]], _Categorical quantum channels: Attacking the quantum version of Birkhoff's theorem with category theory_ ([pdf](http://ncatlab.org/nlab/files/apstalk.pdf))

[[!redirects quantum channel]]
[[!redirects quantum channels]]
[[!redirects quantum operation]]
[[!redirects quantum operations]]