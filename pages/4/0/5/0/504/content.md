
\tableofcontents

## Idea

A **bijection** is an [[isomorphism]] in [[Set]].  

Since [[Set]] is a [[balanced category]], bijections can also be characterized as functions which are both [[injection|injective]] ([[monomorphism|monic]]) and [[surjection|surjective]] ([[epimorphism|epic]]).

## Definition

Given [[sets]] $A$ and $B$, a [[function]] $f:A \to B$ is a **bijection** if it comes with an [[inverse function]] $f^{-1}:B \to A$ such that for all elements $b \in B$, $f(f^{-1}(b)) = b$ and for all elements $a \in A$, if $f(a) = b$, then $a = f^{-1}(b)$

$$\forall b \in B.(f(f^{-1}(b)) = b \wedge \forall a \in A.(f(a) = b \implies a = f^{-1}(b)))$$

The condition that $f(f^{-1}(b)) = b$ could also be made more general, by any element $a:A$ such that $a = f^{-1}(b)$. This then becomes

$$\forall a \in A.\forall b \in B.((a =_A f^{-1}(b)) \implies (f(a) =_B b)) \wedge ((f(a) =_B b) \implies (a =_A f^{-1}(b))$$

This could be simplified down to the statement that $f(a) = b$ if and only if $a = f^{-1}(b)$. 

$$\forall a \in A.\forall b \in B.((f(a) =_B b) \iff (a =_A f^{-1}(b))$$

## Terminology

In older literature, a bijection may be called a __one-to-one correspondence__, or (as a compromise) __bijective correspondence__.

## See also

* [[equivalence of types]]

[[!include types and logic - table]]

[[!redirects bijective]]
[[!redirects bijection]]
[[!redirects bijections]]
[[!redirects bijective function]]
[[!redirects bijective functions]]
[[!redirects bijective correspondence]]
[[!redirects bijective correspondences]]
[[!redirects one-to-one correspondence]]
[[!redirects one-to-one correspondences]]
[[!redirects one to one correspondence]]
[[!redirects one to one correspondences]]
[[!redirects 1-to-1 correspondence]]
[[!redirects 1-to-1 correspondences]]
[[!redirects 1 to 1 correspondence]]
[[!redirects 1 to 1 correspondences]]
[[!redirects 1-1 correspondence]]
[[!redirects 1-1 correspondences]]
[[!redirects 1–1 correspondence]]
[[!redirects 1–1 correspondences]]
