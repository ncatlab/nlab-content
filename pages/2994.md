
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### As partial functions on a field

If $k$ is a [[field]], given the [[polynomial ring]] $k[x]$, there is a canonical [[ring homomorphism]] $j:k[x] \to (k \to k)$ which sends [[constant function|constant]] [[polynomials]] in $k[x]$ to [[constant functions]] in $k \to k$, and the [[generator]] $x \in k[x]$ to the [[identity function]] $id_k$, where $k \to k$ is the [[function algebra]] on $k$. 

There is a function 
$$i:k(x) \to \{A \in Ob(Part(k)) \vert Hom(A, k)\}$$
from the field of [[rational expression]] to the set of all [[partial functions]] in the [[category of partial functions]] $Part(k)$, where the [[function algebra]] $k \to k$ is the [[endomorphism]] $k$-algebra on the [[improper subset]] $k$. The function $i$ is defined as follows: given two polynomials $p, q \in k[x]$, for all $x \in \{a \in k | q(a) \neq 0\}$
$$i\left(\frac{p}{q}\right)(x) \coloneqq \frac{j(p)(x)}{j(q)(x)}$$
where 
$$\frac{x}{y}$$
is the [[division]] of $x$ by $y$ in $k$. A **rational function** $f$ is an [[element]] of the [[image]] of $i$, $f \in \im(i)$. 

### As functions on the projective line

It is perhaps more illuminating to think of this partial function (with domain $D$) as coming from a (total) function $[p/q]: \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ on the [[projective line]], where we have inclusion functions $i: k \to \mathbb{P}^1(k)$ and the partial function is given by the pair of projection maps in the [[pullback]] 

$$\array{
D & \to & k \\
\downarrow & & \downarrow_\mathrlap{i} \\ 
k & \underset{[p/q] \circ i}{\to} & \mathbb{P}^1(k) 
}$$ 

It should also be noticed that such endofunctions $[p/q]$ on $\mathbb{P}^1(k)$ are closed under composition (except that special provision must be made for the constant function valued at $\infty$, which corresponds to the "fraction" $1/0$). 

## Properties

### Rational functions on a field do not form a field

This comes from the fact that the reciprocal function is not a multiplicative inverse of the identity function $f(x) = \frac{x}{x} \neq 1$, due to the fact that $f(x)$ is undefined at $0$, and thus has a different domain than the constant function $1$, which is the multiplicative unit. 

### As continuous functions

[[rational functions are continuous]] on their domain of definition

## Related concepts

* [[polynomial]]

* [[power series]]

* [[rational map]]

* [[homotopy of rational maps]]

* [[category of partial functions]]

* [[rational fraction]]

* [[rational function on an affine variety]] 

## References

* Wikipedia, [Rational function](https://en.wikipedia.org/wiki/Rational_function)

On the [[homotopy type of spaces of rational maps]] from the [[Riemann sphere]] to itself (related to the [[moduli space of monopoles]] in $\mathbb{R}^3$ and to the [[configuration space of points]] in $\mathbb{R}^2$):

* [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))

[[!redirects rational functions]]

[[!redirects ring of rational functions]]
[[!redirects rings of rational functions]]