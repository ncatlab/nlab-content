<div class="rightHandSide toc">
[[!include physicscontents]]
</div>

#Contents
* automatic table of contents goes here
{:toc}

## Idea

Any physical process is supposed to take [[physical state]]s into physical states. If we use [[density matrices]] to describe states in [[quantum mechanics]], then it must be some operation that sends density matrices to density matrices: it should be a [[linear map]] of [[vector space]]s

$$
  U : Mat(n \times n, \mathbb{C}) \to Mat(k \times k, \mathbb{C})
$$

that preserves the subset of density matrices, in that it 

* preserves the trace of matrices;

* takes hermitian matrices with non-negative eigenvalues to hermitian matrices with non-negative eigenvalues.

The notion of a quantum operation is built from the [[Stinespring factorization theorem]].


## Definition

Let $k,n \in \mathbb{N}$.

A matrix $A \in Mat(n \times n, \mathbb{C})$ is called _positive_ if it is hermitian -- if $A^\dagger = A$ -- and if all its eigenvalues (which then are necessarily real) are non-negative.

A linear map (morphism of [[vector space]]s of matrices)

$$
  \Phi : Mat(n \times n, \mathbb{C}) \to 
   Mat(k \times k, \mathbb{C})
$$

is called _positive_ if it takes positive matrices to positive matrices.

The map $\Phi$ is called _completely positive_ if for all $p \in \mathbb{N}$ the [[tensor product]]

$$
  \Phi \otimes Id_{Mat(p\times p),\mathbb{C}} :
  Mat(n \times n , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
  \to
  Mat(k \times k , \mathbb{C})\otimes
  Mat(p \times p , \mathbb{C})
$$

is positive.

Note that [[Bob Coecke|Coecke]] has shown that FdHilb, the category of finite dimensional Hilbert spaces and linear maps, has the completely positive maps as morphisms.  See _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)).


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

* Choi, _Completely positive linear maps on complex matrices_, Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

=--

Note that a proof of the above theorem in terms of [[dagger category|†-categories]] can be found in [[Peter Selinger]], _Dagger-compact closed categories and completely positive maps_ ([ps](http://www.mscs.dal.ca/~selinger/papers/dagger.ps)).

The matrices $\{E_i\}$ that are associated to a completely positive and trace-preserving map by the above theorem are called **Kraus operators**.

In the physics literature the above theorem is then phrased as: _Every quantum channel can be represented using Kraus operators_  .

Notice that the identity map is clearly completely positive and trace preserving, and that the composite of two maps that preserve positivity and trace clearly still preserves positivity and trace. Therefore we obtain a [[category]] $QChan \subset Vect$ -- a [[subcategory]] of [[Vect]]${}_{\mathbb{C}}$ -- whose

* objects are the vector spaces $Mat(n \times n, \mathbb{C})$ for all $n \in \mathbb{N}$;

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.

See also [[extremal quantum channels]] and [[graphical quantum channels]].


## Example

A very common example of this formalism comes from its use in [[open quantum systems]], that is systems that are coupled to an environment.  Let $\rho$ be the state of some quantum system and $\rho_{env}$ be the state of the environment.  The action of a unitary transformation, $U$, on the system is

$$
  T(\rho) = Tr_{env}U(\rho \otimes \rho_{env})U^{\dagger}.
$$

## References

An early influential reference on _(completely) positive trace-preserving maps (CPTP)_ is:

* Choi, M. (1975). _Completely positive linear maps on complex matrices_, Linear Algebra and its Applications Volume 10, Issue 3, June 1975, Pages 285-290

A useful review of the notion is provided by 

* Caleb J. O'Loan (2009), _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* Nielsen, Michael and Chuang, Isaac (2000) _Quantum Computation and Quantum Information_, Cambridge University Press, Cambridge.

* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))

The description of completely positive maps in terms of [[dagger-categories]] goes back to

* [[Peter Selinger]], _Dagger-compact closed categories and completely positive maps_ ([ps](http://www.mscs.dal.ca/~selinger/papers/dagger.ps))

* [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 

This was further developed in

* [[Bob Coecke]], [[Eric Paquette]], [[Dusko Pavlovic]], _Classical and quantum structures_ ([pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf))

A recently revised presentation that could use some work, but hopefully serves to encourage further development from the [[nPOV]] is:

* [[Ian Durham]], Categorical quantum channels: Attacking the quantum version of Birkhoff's theorem with category theory ([[apstalk2.pdf:file]])

+-- {: .query}
I guess that this is all right as an introduction to quantum channels, but the connection to category theory really isn\'t made; it\'s almost two disjoint talks interwoven.  (The category theory in there is also very vaguely defined, but maybe it was good enough in context.)  ---[[Toby Bartels]]

I'm not completely opposed to removing it.  The talk was limited to 10 minutes with 2 minutes for questions so I was trying to squeeze a lot in.  But the general approach to quantum channels was ripped straight from the nLab and was a bit different than most attendees were used to.

Anyway, the big reason I put it here is that I thought it might inspire someone to assist with further development of the idea.  --[[Ian Durham]]
=--


[[!redirects quantum channel]]
[[!redirects quantum channels]]
[[!redirects quantum operation]]
[[!redirects quantum operations]]
[[!redirects quantum operations and channels]]
