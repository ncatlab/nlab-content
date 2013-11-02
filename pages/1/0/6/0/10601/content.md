A [[binary algebraic structure]] $(A,\cdot)$ is __medial__ if for all $a,b,c,d\in A$ $(a\cdot b)\cdot(c\cdot d) = (a\cdot c)\cdot (b\cdot d)$.
This law is quite close to commutativity: for example, if $(A,\cdot)$ has a unit element (is a unital [[magma]]), then by [[Eckmann-Hilton argument]], it is an Abelian [[monoid]]. Without two-sided unit element, the connection with Abelian groups is somewhat more intricate

__(Bruck-Toyoda theorem)__ A [[quasigroup]] $(A,\cdot)$ is medial iff there is an Abelian group structure $(A,+)$ on $A$ and mutually commuting group [[automorphism]]s $\phi,\psi:A\to A$ and an element $h\in A$ such that 
$$
a\cdot b = \phi(a)+\psi(b)+h
$$

An element $a$ in a magma $(A,\cdot)$ is left regular if the left multiplication $L_a$ by $a$ is bijective and right regular if the right multiplication $R_a$ is bijective.
The Bruck-Toyoda theorem is a direct corollary of a more general statement about (nonunital in general) magmas:

Theorem. A [[medial magma]] $(A\cdot)$ has a left regular element $f$ and a right regular element $g$ such that also $f^2$ is left regular and $g^2$ is right regular iff there exist a commutative [[semigroup]] structure $(A,+)$ on $A$, mutually commuting automorphisms $\phi,\psi:A\to A$ and a regular element $h$ in semigroup $(A,+)$ such that
$$
a\cdot b = \phi(a)+\psi(b)+h
$$

category: algebra
[[!redirects Toyoda theorem]]