#Contents#
* table of contents
{:toc}


## Idea

A *self-adjoint functor* is an [[endofunctor]] $F : C \to C$ such that $F \dashv F$, so that $F$ is both [[left adjoint]] and [[right adjoint]] to itself.

## Examples

- The [[duality involution]] $({-})^{op} : Cat \to Cat$ is self-adjoint. More generally, this is true of the underlying category of any [[2-category]] with a duality involution.
- If a category $C$ has [[biproducts]], then the composite $\oplus \circ \Delta_n$ of the (discrete $n$-ary) [[diagonal functor]] $\Delta_n$ with the ($n$-ary) biproduct functor $\oplus$ is self-adjoint.

## Functors self-adjoint on the left

There is a similar phenomenon involving a change of variance. A functor $F : C^{op} \to C$ is called **self-adjoint on the left** if $F \dashv F^{op}$. In this case, we have a natural isomorphism $C(F A, B) \cong C(F B, A)$. (Conversely, we may talk about functors **self-adjoint on the right** if $C(A, F B) \cong C(B, F A)$.)

- The contravariant powerset functor $\mathcal{P}: Set \to Set^{op}$ is left-adjoint to $\mathcal{P}^{op} : Set^{op} \to Set$, i.e. self-adjoint on the right.
- More generally, in a symmetric monoidal closed category $(C, \otimes, I, \multimap)$, for a fixed object $A$, the functor $(-) \multimap A$ is self-adjoint on the right.


[[!redirects self-adjoints]]
[[!redirects self-adjoint functor]]
[[!redirects self-adjoint functors]]

[[!redirects self-adjoint on the left]]
[[!redirects self-adjoint on the right]]