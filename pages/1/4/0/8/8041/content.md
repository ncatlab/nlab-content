
\tableofcontents 

## Definition

### In set theory

Given [[sets]] $A$ and $B$ and a [[function]] $f\colon A \to B$, the __inverse function__ of $f$ (if it exists) is the function $f^{-1}\colon B \to A$ such that both [[composition|composite functions]] $f \circ f^{-1}$ and $f^{-1} \circ f$ are [[identity functions]].  Note that $f$ has an inverse function if and only if $f$ is a [[bijection]], in which case this inverse function is unique.

Inverse functions are [[inverse morphisms]] in the [[category]] [[Set]] of sets.

More generally, in any [[concrete category]], the inverse of any [[isomorphism]] is given by the inverse of the corresponding function between [[underlying sets]].

### In type theory

In type theory, given [[types]] $A$ and $B$ and a [[function]] $f:A \to B$,  the __inverse function__ of $f$ (if it exists) is the function $f^{-1}:B \to A$ such that $f^{-1}$ is a [[retraction]] of $f$, and for each element $b:B$, $f^{-1}(b)$ is the [[center of contraction]] of the fiber of $f$ at $b$. 

$$\prod_{b:B} (f(f^{-1}(b)) =_B b) \times \prod_{q:\sum_{a:A} f(a) =_A b} (\pi_1(q) =_A f^{-1}(b))$$

Equivalently, the inverse function of $f$ (if it exists) is the function $f^{-1}:B \to A$ such that $f^{-1}$ is a [[retraction]] of $f$ and for each element $a:A$ and $b:B$, there is a function $r(a, b):(f(a) = b) \to (a = f^{-1}(b))$. 

$$\left(\prod_{b:B} f(f^{-1}(b)) =_B b\right) \times \left(\prod_{a:A} \prod_{b:B} (f(a) =_B b) \to (a =_A f^{-1}(b))\right)$$

## Related concepts

* [[inverse]], [[inverse morphisms]]

* [[inverse functor]]

* [[isomorphism]]

Not really related

* [[inverse image]]

[[!redirects inverse function]]
[[!redirects inverse functions]]
[[!redirects inverse map]]
[[!redirects inverse maps]]
