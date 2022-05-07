
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

Given an [[integral domain]] $R$, the commutative _ring of **rational functions**_ $R(z)$ with coefficients in $R$ is the [[field of fractions]] of the [[polynomial ring]] $R[z]$.  

Let $X$ be an [[affine variety]] over a field $k$ with the ring of [[regular function]]s $\mathcal{O}(X)$. A __rational function__ is any element of the [[field of fractions]] of $\mathcal{O}(X)$, that is the [[function field]] of the variety.

### As "functions" 

In either case, rational functions are [[equivalence classes]] of fractions; they need not be [[functions]] defined everywhere. If $k$ is a field, then to each fraction $\frac{p(x)}{q(x)} \in k(x)$ with $p, q \in k[x]$ relatively prime, we may associate a [[partial function]] $k \rightharpoonup k$ whose [[domain]] consists of $a \in k$ such that $q(a) \neq 0$ (defining $q(a)$ as usual as the value of $q$ under the unique $k$-algebra map $k[x] \to k$ sending $x$ to $a$), and sending each $a$ in the domain to $\frac{p(a)}{q(a)}$. For the purposes of most elementary mathematics, the domain given here may be described as the "natural domain" of the rational function. 

It is perhaps more illuminating to think of this partial function (with domain $D$) as coming from a (total) function $[p/q]: \mathbb{P}^1(k) \to \mathbb{P}^1(k)$ on the [[projective line]], where we have inclusion functions $i: k \to \mathbb{P}^1(k)$ and the partial function is given by the pair of projection maps in the [[pullback]] 

$$\array{
D & \to & k \\
\downarrow & & \downarrow_\mathrlap{i} \\ 
k & \underset{[p/q] \circ i}{\to} & \mathbb{P}^1(k) 
}$$ 

It should also be noticed that such endofunctions $[p/q]$ on $\mathbb{P}^1(k)$ are closed under composition (except that special provision must be made for the constant function valued at $\infty$, which corresponds to the "fraction" $1/0$).  

## Properties

### As continuous functions

[[rational functions are continuous]] on their domain of definition

### Function field analogy

[[!include function field analogy -- table]]


## Related concepts

* [[polynomial]]

* [[power series]]

* [[rational map]]

* [[homotopy of rational maps]]


## References

On the [[homotopy type of spaces of rational maps]] from the [[Riemann sphere]] to itself (related to the [[moduli space of monopoles]] in $\mathbb{R}^3$ and to the [[configuration space of points]] in $\mathbb{R}^2$):

* [[Graeme Segal]], _The topology of spaces of rational functions_, Acta Math. Volume 143 (1979), 39-72 ([euclid:1485890033](https://projecteuclid.org/euclid.acta/1485890033))


[[!redirects rational functions]]

[[!redirects ring of rational functions]]
[[!redirects rings of rational functions]]