
# Amnestic functors
* table of contents
{: toc}

## Definition

An **amnestic functor** is a functor $U : \mathcal{D} \to \mathcal{C}$ (between [[strict categories]]) that reflects [[identity morphism|identity morphisms]]: more precisely, for any [[isomorphism]] $f\colon a \to b$ in $\mathcal{D}$, if $U a = U b$ and $U f = id_{U a}$, then $a = b$ and $f = id_a$.

If we follow the [[principle of equivalence]] and refuse to state equations between objects, then the closest thing to this that we can say is that if $U a \cong U b$ (say via $g\colon U a \to U b$) and $U f = g \circ id_{U a}$ (which is a trivial hypothesis, since $g$ can simply be $U f$), then $a \cong b$ (say via $h\colon a \to b$) and $f = h \circ id_a$ (which is a trivial conclusion, since $h$ can simply be $f$.)  Thus, this is really a property of [[strict functors]] between [[strict categories]].  Or to put it another way, if $U\colon \mathcal{D} \to \mathcal{C}$ is any functor, then there exist [[equivalent categories]] $\mathcal{D}' \simeq \mathcal{D}$ and $\mathcal{C}' \simeq \mathcal{C}$ such that the composite $\mathcal{D}' \to \mathcal{D} \overset{F}\to \mathcal{C} \to \mathcal{C}'$ is amnestic.


## Properties

* An amnestic [[full and faithful functor]] is automatically an [[isocofibration]], i.e. injective on objects: if $U D' = U D$, then there is some _isomorphism_ $f : D' \to D$ in $\mathcal{D}$ such that $U f = id_{U D}$, but then we must have $f = id_{U D'} = id_{U D}$, so $D' = D$.

* An amnestic [[isofibration]] has the following lifting property: for any object $D$ in $\mathcal{D}$ and any isomorphism $f : C \to U D$ in $\mathcal{C}$, there is a _unique_ isomorphism $\tilde{f} : \tilde{C} \to D$ such that $U \tilde{f} = f$. Indeed, if $\tilde{f}' : \tilde{C}' \to D$ were any other isomorphism such that $U \tilde{f}' = f$, then $U (\tilde{f}^{-1} \circ \tilde{f}') = id_C$, so we must have $\tilde{f} = \tilde{f}'$.

* If the [[composite]] $U \circ K$ is an amnestic functor, then $K$ is also amnestic.


## Examples

* Any strictly [[monadic functor]] is amnestic. Conversely, any monadic functor that is also an amnestic isofibration is necessarily strictly monadic.


## Related concepts

* [[structure]], 

* [[stuff, structure, property]]


## References

* Ad&#225;mek, Herlich and Strecker, [[The Joy of Cats]], Chapter I, Definition 3.27.


[[!redirects amnestic functor]]
[[!redirects amnestic functors]]
