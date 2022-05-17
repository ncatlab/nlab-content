

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


# Orthogonal and orthonormal subsets
* table of contents
{: toc}

## Definition

For $V$ an [[inner product space]], a collection of vectors $\{v_i\}$ of $V$ is **orthogonal** with respect to the inner $\langle{-, -}\rangle\colon V \times V \to k$ if for all $i \neq j$ we have $\langle{v_i, v_j}\rangle = 0$. It is __orthonormal__ if additionally we have $\langle{v_i, v_i}\rangle = 1$; that is, $\langle{v_i, v_j}\rangle = \delta_{i,j}$ (the [[Kronecker delta]]) for all $i, j$.  Note that an orthogonal set is necessarily [[linearly independent subset|linearly independent]], assuming (as one often does) that the inner product is nondegenerate.


## Bases

In speaking of the notion of orthonormal or orthogonal _[[basis]]_ of $V$, due attention must be paid to the meaning of 'basis'. When $V$ has finite [[dimension]], one can just use the [[Hamel basis|purely algebraic sense of basis]]: a linearly independent set whose span is all of $V$, or equivalently a [[maximal element|maximal]] linearly independent set. In this case, there is no restriction on the ground field $k$. 

Often, however, 'basis' is supposed to mean the [[basis in functional analysis|sense of basis]] used for a [[topological vector space]] $V$, i.e., a linearly independent set whose span is [[dense subspace|dense]] in $V$. In the TVS case, it is usually understood that the ground field $k$ is a [[local field]], and the inner product is separately continuous with respect to the topology on $V$. A typical situation is where $k$ is $\mathbb{R}$ or $\mathbb{C}$ and the inner product is a positive definite inner product on $V$ which naturally induces a [[metric space|metric]] and from there a TVS structure on $V$. 

We have this interesting pair of results:

* On one hand, no infinite-dimensional positive-definite inner-product space has an orthogonal (much less orthonormal) basis in the purely algebraic sense.
* On the other hand, any maximal orthogonal set (which must exist by an application of [[Zorn's lemma]]) is necessarily a basis in the topological sense.


## Gram&#8211;Schmidt process

For a finite-dimensional vector space equipped with a nondegenerate inner product, one may replace any [[well-ordered set|well-ordered basis]] by an well-ordered orthogonal basis using the [[Gram–Schmidt process]]. Assuming that we have $\langle v, v \rangle \neq 0$ for $v \neq 0$ (as for example in the case of a positive definite inner product space), and assuming square roots $\langle v, v \rangle^{1/2}$ exist in the ground field $k$, we can further produce a well-ordered orthonormal basis from a well-ordered basis. 

In the TVS case, with the appropriate meaning of basis understood, the Gram-Schmidt process extends without difficulty to any well-ordered basis, because the process yields a linearly independent orthogonal set with the same span as the original basis. 

## Examples

* [[Schur's lemma]] says that [[irreducible representations]] form an orthogonal basis of the [[representation ring]]. See [there](Schur's+lemma#InterpretationInCategoricalAlgebra) for more.


## Related concepts

* [[frame field]]

* [[orthogonality]]

* [[orthogonal structure]]

* [[normal vector]]

## References

See also

* Wikipedia, _[Orthogonal basis](https://en.wikipedia.org/wiki/Orthogonal_basis)_


[[!redirects orthogonal set]]
[[!redirects orthogonal sets]]
[[!redirects orthogonal subset]]
[[!redirects orthogonal subsets]]

[[!redirects orthonormal set]]
[[!redirects orthonormal sets]]
[[!redirects orthonormal subset]]
[[!redirects orthonormal subsets]]

[[!redirects orthogonal basis]]
[[!redirects orthogonal bases]]
[[!redirects orthogonal basises]]

[[!redirects orthonormal basis]]
[[!redirects orthonormal bases]]
[[!redirects orthonormal basises]]

[[!redirects orthonormal]]
[[!redirects orthonormal vector]]
[[!redirects orthonormal vectors]]
