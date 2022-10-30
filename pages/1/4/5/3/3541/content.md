
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--

#Contents
* table of contents
{:toc}

## Idea

Any physical process is supposed to take [[physical states]] into physical states ([[Schrödinger picture]]). If  [[density matrices]] are used to describe [[quantum states]] in [[quantum mechanics]], then it must be some operation that sends density matrices to density matrices. So for finite-dimensional state spaces then an process it should be a [[linear map]] of [[vector spaces]] of [[matrices]]

$$
  U : Mat(n \times n, \mathbb{C}) \to Mat(k \times k, \mathbb{C})
$$

that preserves the subset of [[density matrices]], in that

* it preserves the [[trace]] of matrices;

* takes hermitian matrices with non-negative eigenvalues to hermitian matrices with non-negative eigenvalues.

Such a map is then called a _quantum operation_. The notion of a quantum operation is built from the [[Stinespring factorization theorem]].


## Definition

We first give the traditional definition in terms of [[linear algebra]] and [[matrices]] in 

* [In terms of matrices](#InTermsOfMatrices)

Then we consider the general abstract formulation 

* [In terms of compact closed categories](#InTermsOfCompactClosedCategories)


### In terms of matrices
 {#InTermsOfMatrices}

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

### In terms of compact closed categories
 {#InTermsOfCompactClosedCategories}

... due to ([Selinger 05](#Selinger)) ... see for instance ([Coecke-Heunen 11, section 2](#CoeckeHeunen11)) for a quick summary ...

## Properties


### Characterization of complete positivity

+-- {: .num_theorem}
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

This is originally due to ([Choi, theorem 1](#Choi)). A proof in terms of [[dagger category|†-categories]] is given in ([Selinger 05](#Selinger05)). A characterization of completely positive maps entirely in terms of $\dagger$-categories is given in ([Coecke](#Coecke)).

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

## Related concepts

* [[quantum mechanics in terms of dagger-compact categories]]
  

## References

An early influential reference on _(completely) positive trace-preserving maps (CPTP)_ is:

* M. Choi, _Completely positive linear maps on complex matrices_, Linear Algebra and its Applications Volume 10, Issue 3, (1975), Pages 285-290
 {#Choi}

Reviews and surveys include

* [[Greg Kuperberg]], section 1.5 of _A concise introduction to quantum probability, quantum mechanics, and quantum computation_, 2005 ([pdf](http://www.math.ucdavis.edu/~greg/intro-2005.pdf))
 {#Kuperberg05}

* Michael Nielsen, Isaac Chuang, section 8.2 of _Quantum Computation and Quantum Information_, Cambridge University Press, Cambridge (2000) ([[NielsenChuangQuantumComputation.pdf:file]])

See also

* Caleb J. O'Loan (2009), _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))


* Christian B. Mendl, Michael M. Wolf, _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))


* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* John Watrous, _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ (2008) ([arXiv](http://arxiv.org/abs/0807.2668))

The description of completely positive maps in terms of [[dagger-categories]] (see at _[[finite quantum mechanics in terms of dagger-compact categories]]_) goes back to

* [[Peter Selinger]], _Dagger-compact closed categories and completely positive maps_, Electronic Notes in Theoretical Computer
Science (special issue: Proceedings of the 3rd International Workshop on Quantum Programming Languages). 2005 ([[SelingerPositiveMaps.pdf:file]], [ps](http://www.mscs.dal.ca/~selinger/papers/dagger.ps))
 {#Selinger05}

* [[Bob Coecke]], _Complete positivity without compactness_ ([pdf](http://www.comlab.ox.ac.uk/files/666/RR-07-05.pdf)) 
 {#Coecke}

This is further explored in

* [[Bob Coecke]], Eric Paquette, [[Dusko Pavlovic]], _Classical and quantum structures_ ([pdf](http://www.comlab.ox.ac.uk/files/627/RR-08-02.pdf))

* [[Bob Coecke]], [[Chris Heunen]], _Pictures of complete positivity in arbitrary dimension_, EPTCS 95, 2012, pp. 27-35 ([arXiv:1110.3055](http://arxiv.org/abs/1110.3055))
 {#CoeckeHeunen11}

* [[Bob Coecke]], [[Chris Heunen]], [[Aleks Kissinger]], _Categories of Quantum and Classical Channels_ ([arXiv:1305.3821](http://arxiv.org/abs/1305.3821))

[[!redirects quantum channel]]
[[!redirects quantum channels]]
[[!redirects quantum operation]]
[[!redirects quantum operations]]
[[!redirects quantum operations and channels]]

[[!redirects completely positive map]]
[[!redirects completely positive maps]]