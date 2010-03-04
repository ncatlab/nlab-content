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

The concept was picked up in the physics literature, where (completely) positive trace-preserving maps were synonymously renamed to **quantum channels**, reflecting the physical interpretation of these maps: 

Notably in [[quantum information theory]] one thinks of each way to send a signal from one quantum system to another as being modeled by such a map.

A useful review of the notion in this context is in section 1.7 of

* Caleb J. O'Loan, _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))



More generally, the definition can be extended in a more-or-less obvious way from systems with a finite number of degrees of freedom, to general systems. This requires replacing the finite dimensional complex vector space $\mathbb{C}^n$ with an arbitrary [[Hilbert space]] $\mathcal{H}$ and the space of matrices by a suitable space of linear operators on that Hilbert space.

## Details

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

+--{: .query}
[[Ian Durham]]: If the objects are the set of linear operators on the Hilbert space in question, is $QChan$ small?  Or, if we could make sub-categories of QChan for sets of linear operators of different dimension, could we then use these to make a commutative square?

[[David Roberts]]: Let me be the first to say that I'm not sure what you're asking with regard to the commutative square. But there are certainly subcategories $QChan_n$ with the only object $Mat(n \times n, \mathbb{C})$. More natural would be to allow arbitrary $End(V)$ where $V$ is an $n$-dimensional $\mathbb{C}$-vector space, as then different $V$ could correspond to different representations, say. But in respect of the next comment box, I don't think that this was the category you were after, so this may be a moot point. Unfortunately I don't know enough relevant physics to make that call.

[[Urs Schreiber]]: there is one object of $QChan$ per element $n$ of the set of natural numbers, namely the vector space $Mat(n \times n, \mathbb{C})$. So $QChan$ has a _set_ of objects, namely $Obj(QChan) \simeq \mathbb{N}$ and hence is certainly a [[small category]]. (I don't know which commuting squares are meant.)

[[Ian Durham]]: Yeah, the question on commutative squares was vague so let's not worry about it right now.  I would agree that, as defined, $QChan$ is small, though I'm not so sure about it necessarily being an endomorphism (unless I'm mis-interpreting Urs' comment).  For instance, a quantum channel can take as the input $L(\mathcal{H}_{A})\otimes C(X)$ (where $L(\mathcal{H}_{A})$ is the set of linear operators on the Hilbert space $\mathcal{H}_{A}$ and $C(X)$ is the set of continuous functions on some vector space $X$) and can spit out $L(\mathcal{H}_{B})$.  Physically this means it can take a quantum + classical input and give a quantum-only output.  This doesn't seem endomorphic to me (since we traditionally don't define the classical piece as being on a Hilbert space), at least on some level, but I could be wrong.

[[David Roberts]]: Ok then - if I have two quantum channels, $L(\mathcal{H}_1)\otimes C(X) \to L(\mathcal{H}_2)$ and $L(\mathcal{H}_2)\otimes C(Y) \to L(\mathcal{H}_3)$ (where we may need to have $X = Y$), then what is the composite? I presume this is something of the form
$$
L(\mathcal{H}_1)\otimes C(X)\otimes C(Y) \to L(\mathcal{H}_3)?
$$
I would be more comfortable if instead of $C(X)\otimes C(Y)$ we had $C(somthing)$, but this should become clear once we write down what the map above is, some expression in terms of Kraus operators I presume.

Personally I think that instead of identifying the objects of the category with the algebras $Mat(m \times m, \mathbb{C})$ (or better, $End(H)$), we should consider the isomorphic category with objects $H$, but with the arrows as before. This allows us to generalise the inputs of the channel to a mix of classical and quantum, as you indicate. The real substance is to show that composites (as I consider in the previous paragraph) exist and behave as they should.

[[Ian Durham]]: There's one sticky wicket there: not all quantum channels are reversible so they're not necessarily isomorphisms (unless I'm mis-interpreting you).  From an information theoretic perspective, there are some quantum channels for which perfect recovery of the initial information, even with environmental assistance, is not possible.  So I would certainly say that _some_ quantum channels are isomorphic categories, but not all.

Regarding composites, normally it is just a composite of Kraus operators (see my first revision of the [quantum channel](http://ncatlab.org/nlab/revision/quantum+channel/1) page).  Regarding the categories, though, I think I may have actually been able to show that it behaves as expected using a commutative square.
=--

* morphism are completely positive and trace-preserving linear maps $\Phi : Mat(n\times n , \mathbb{C}) \to Mat(m \times m, \mathbb{C})$;

* composition of morphisms is, of course, the composition in [[Vect]], i.e. the ordinary composition of linear maps.

+--{: .query}
[[David Roberts]]: I was thinking that perhaps the objects of the category were the vector/Hilbert spaces, and the arrows were the completely positive and trace-preserving maps between the matrix algebras. In this instance, the category theoretical content seems that it would be more detailed than \'it\'s just a subcategory of Vect\'.

[[Ian Durham]]: Yes!  That was what my original plan was.  The idea was that it would be possible to create a monoid if the input and output Hilbert space was the same which would give it possibly interesting group theoretic properties (namely Cayley's theorem which would potentially allow me to find some morphism to unitaries which we like in quantum mechanics because they describe system evolution).

[[Urs Schreiber]]: certainly the quantum channels that go $Mat(n \times n , \mathbb{C}) \to Mat(n \times n, \mathbb{C})$ form a monoid. This is the endomorphism monoid $End_{QChan}(n)$ in $QChan$ on the object $n$, i.e. on the object $Mat(n \times n , \mathbb{C})$.

=--

## References


* Choi, M. (1975). _Completely positive linear maps on complex matrices_ , Linear Algebra and its Applications 10: 285&#8211;290.


* Smolin, John A., Verstraete, Frank, and Winter, Andreas _Entanglement of assistance and multipartite state distillation_ , Phys. Rev. A, vol. 72, 052317, 2005 ([arXiv:quant-ph/0505038](http://arxiv.org/abs/quant-ph/0505038))

* Mendl, Christian B. and Wolf, Michael M. (2009) _Unital Quantum Channels - Convex Structure and Revivals of Birkhoff's Theorem_ , Commun. Math. Phys. 289, 1057-1096 (2009) ([arXiv:0806.2820](http://arxiv.org/abs/0806.2820))

* O'Loan, Caleb J.,  _Topics in Estimation of Quantum Channels_ , PhD thesis, University of St. Andrews, ([arXiv](http://arxiv.org/abs/1001.3971))

* Watrous, John (2008). _Mixing doubly stochastic quantum channels with the completely depolarizing channel_ ([arXiv](http://arxiv.org/abs/0807.2668))


[[!redirects quantum channel]]
[[!redirects quantum channels]]
