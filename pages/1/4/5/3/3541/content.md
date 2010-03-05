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

The relevance of this concept of **(completely) positive trace-preserving maps** apparently became widely recognized due to the article

* Choi, _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

The concept was picked up in the physics literature, where (completely) positive trace-preserving maps are referred to as **quantum operations** or **quantum channels**, reflecting the physical interpretation of these maps: 

Notably in [[quantum information theory]] one thinks of each way to send a signal from one quantum system to another as being modeled by such a map.

A useful review of the notion in this context is in section 1.7 of

* Caleb J. O'Loan, _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

More generally, the definition can be extended in a more-or-less obvious way from systems with a finite number of degrees of freedom, to general systems. This requires replacing the finite dimensional complex vector space $\mathbb{C}^n$ with an arbitrary [[Hilbert space]] $\mathcal{H}$ and the space of matrices by a suitable space of linear operators on that Hilbert space.

## Quantum Operations

+--{: .query}
TO DO: Briefly summarize quantum operations since they form the basis for the definition of channels and also since they relate to environmentally assisted reversibility.
=--

## Quantum Channels

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

+--{: .query}
TO DO: Describe open systems and their relation to reversibility.
=--

### Discussion

## References

* Choi, M. (1975). _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications 10: 285&#8211;290.

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* Nielsen, Michael and Chuang, Isaac (2000) _Quantum Computation and Quantum Information_, Cambridge University Press, Cambridge.

* O'Loan, Caleb J.,  _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))



[[!redirects quantum channel]]
[[!redirects quantum channels]]
[[!redirects quantum operation]]
[[!redirects quantum operations]]