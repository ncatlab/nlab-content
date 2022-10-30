
# Amnestic functors
* table of contents
{: toc}

## Definition

An **amnestic functor** is a functor $U : \mathcal{D} \to \mathcal{C}$ (between [[strict categories]]) that reflects [[identity morphism|identity morphisms]]: more precisely, for any [[isomorphism]] $f\colon a \to b$ in $\mathcal{D}$, if $U a = U b$ and $U f = id_{U a}$, then $a = b$ and $f = id_a$.


## Properties

* An amnestic [[full and faithful functor]] is automatically an [[isocofibration]], i.e. injective on objects: if $U D' = U D$, then there is some _isomorphism_ $f : D' \to D$ in $\mathcal{D}$ such that $U f = id_{U D}$, but then we must have $f = id_{U D'} = id_{U D}$, so $D' = D$.

* An amnestic [[isofibration]] has the following lifting property: for any object $D$ in $\mathcal{D}$ and any isomorphism $f : C \to U D$ in $\mathcal{C}$, there is a _unique_ isomorphism $\tilde{f} : \tilde{C} \to D$ such that $U \tilde{f} = f$. Indeed, if $\tilde{f}' : \tilde{C}' \to D$ were any other isomorphism such that $U \tilde{f}' = f$, then $U (\tilde{f}^{-1} \circ \tilde{f}') = id_C$, so we must have $\tilde{f} = \tilde{f}'$.

* If the [[composite]] $U \circ K$ is an amnestic functor, then $K$ is also amnestic.


## Examples

* Any strictly [[monadic functor]] is amnestic. Conversely, any monadic functor that is also an amnestic isofibration is necessarily strictly monadic.


## References

* Ad&#225;mek, Herlich and Strecker, [[The Joy of Cats]], Chapter I, Definition 3.27.


[[!redirects amnestic functor]]
[[!redirects amnestic functors]]
