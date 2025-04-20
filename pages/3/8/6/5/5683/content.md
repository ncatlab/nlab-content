A [[functor]] $C \to Set$ is **corepresentable** if it is ([[isomorphism|isomorphic]] to) a functor of the form $Hom_C(c,-)$ for some [[object]] $c\in C$.

This is equivalently a [[representable functor]] defined on the [[opposite category]] $C^{op}$.  Often no terminological distinction is made between representable and corepresentable ones (both being called simply "representable"), since a functor $C\to Set$ can only be "corepresentable" while a functor $C^{op}\to Set$ can only be "representable".

Particularly in the study of moduli problems, there is also the notion of corepresentable contravariant functors. A functor $F : C^op \to Set$ is **corepresentable** if and only if there exists an object $X$ in $C$ and a morphism $F \to h_X$ such that for any object $T$ in $C$, the canonical map $Hom_C(X,T) \to Hom_{\PSh(C)}(h_X, h_T) \to Hom_{PSh(C)}(F, h_T)$ is bijective.

## Related concepts

* [[corepresentable functor theorem]]

* [[representable functor]]

[[!redirects corepresentable functors]]
[[!redirects corepresenting object]]
[[!redirects corepresenting objects]]
[[!redirects corepresentable]]
