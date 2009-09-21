#Idea#

A _modular form_ is a [[holomorphic function]] on the [[upper half plane]] that satisfies certain transformation properties.

Modular forms appear as

* as the [[cohomology ring]] over the point in the [[cohomology theory]] called [[tmf]] -- "tmf" stands for "topological modular forms";
 
* as the [[partition function]]s of certain 2-dimensional [[quantum field theor|quantum field theories]].


**definition** An **(integral) [[modular form]]** of weight $w$ is a [[holomorphic function]] on the [[upper half plane]]

$$
  f : (\mathbb{R}^2)_+ \hookrightarrow \mathbb{C}
$$

(complex numbers with strictly positive imaginary part) 

such that

1. if $A = \left( \array{a & b \\ c& d}\right) \in SL_2(\mathbb{Z})$ acting by $A : \tau \mapsto = \frac{a \tau + b }{c \tau + d}$ we have
 
   $$
     f(A(\tau)) = (c \tau + d)^w f(\tau)
   $$

   **note** take $A = \left( \array{1 & 1 \\ 0& 1}\right)$ then we get that $f(\tau + 1) = f(\tau)$

1. $f$ has at worst a pole at $\{0\}$ (for _weak_ modular forms this condition is relaxed)

   it follows that $f = f(q)$ with $q = e^{2 \pi i \tau}$ is a meromorphic funtion on the open disk.


1. **integrality** $\tilde f(q) = \sum_{k = -N}^\infty a_k \cdot q^k$ then $a_k \in \mathbb{Z}$

by this definition, modular forms are not relly functions on the upper half plane, but function on a [[moduli space]] of [[torus|tori]]. 



[[!redirects integral modular form]]
[[!redirects topological modular form]]
[[!redirects weak modular form]]
[[!redirects modular function]]
[[!redirects integral modular function]]
[[!redirects weak integral modular form]]

[[!redirects integral modular forms]]
[[!redirects topological modular forms]]
[[!redirects weak modular forms]]
[[!redirects modular functions]]
[[!redirects integral modular functions]]
[[!redirects weak integral modular forms]]

