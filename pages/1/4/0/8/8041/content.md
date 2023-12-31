
\tableofcontents 

## Definition

### In set theory

Given [[sets]] $A$ and $B$ and a [[function]] $f\colon A \to B$, the __inverse function__ of $f$ (if it exists) is the function $f^{-1}\colon B \to A$ such that both [[composition|composite functions]] $f \circ f^{-1}$ and $f^{-1} \circ f$ are [[identity functions]].  Note that $f$ has an inverse function if and only if $f$ is a [[bijection]], in which case this inverse function is unique.

Inverse functions are [[inverse morphisms]] in the [[category]] [[Set]] of sets.

More generally, in any [[concrete category]], the inverse of any [[isomorphism]] is given by the inverse of the corresponding function between [[underlying sets]].

### In type theory

In [[type theory]], there are two different kinds of inverse functions, quasi-inverse functions, various kinds of more or less coherent quasi-inverse functions, and inverse functions. 

For more on this see at *[[equivalence in type theory]]*.

#### Quasi-inverse functions

Given [[types]] $A$ and $B$ and a [[function]] $f:A \to B$, a __quasi-inverse function__ of $f$ is a function $g:B \to A$ such that $g$ is a [[retraction]] and a [[section]] of $f$. 

$$\prod_{b:B} (f(g(b)) =_B b) \times \prod_{a:A} (a =_A g(f(a)))$$

Equivalently, there are functions $\epsilon_0(a, b):(a =_A g(b)) \to (f(a) =_B b)$ and $\eta_0(a, b):(f(a) =_B b) \to (a =_A g(b))$ for all $a:A$ and $b:B$. 

$$\prod_{a:A} \prod_{b:B} ((a =_A g(b)) \to (f(a) =_B b)) \times ((f(a) =_B b) \to (a =_A g(b)))$$

A function $f:A \to B$ might have multiple quasi-inverse functions. The type of quasi-inverses of $f$ is given by 

$$\mathrm{QuasiInv}(f) \coloneqq \sum_{g:B \to A} \prod_{b:B} (f(g(b)) =_B b) \times \prod_{a:A} (a =_A g(f(a)))$$

#### $n$-quasi inverse functions

There are also variants of quasi-inverse functions where they are the inverse functions for $n$-truncated types. 

For example, every function $g:B \to A$ is a (-1)-quasi inverse function, because it is an inverse function for [[h-propositions]] $A$ and $B$. 

A quasi-inverse function is a 0-quasi inverse function, because it is an inverse function for [[h-sets]] $A$ and $B$. 

A 1-quasi-inverse function is a quasi-inverse function with functions $\epsilon_0(a, b):(a =_A g(b)) \to (f(a) =_B b)$ and $\eta_0(a, b):(f(a) =_B b) \to (a =_A g(b))$ for all $a:A$ and $b:B$ such that for all $c:a =_A g(b)$ and $d:f(a) =_B b$, 
there are functions
$$\epsilon_1(a, b, c, d):(\epsilon_0(a, b, c) =_{f(a) =_B b} d) \to (c =_{a =_A g(b)} \eta_0(a, b, d))$$
$$\eta_1(a, b, c, d):(c =_{a =_A g(b)} \eta_0(a, b, d)) \to (\epsilon_0(a, b, c) =_{f(a) =_B b} d)$$
This is an inverse function for [[h-groupoids]] $A$ and $B$. 

So on and so forth. 

#### Inverse functions

Given [[types]] $A$ and $B$ and a [[function]] $f:A \to B$, an __inverse function__ of $f$ is a function $g:B \to A$ with a function $\epsilon(a, b):(f(a) =_B b) \to (a =_A g(b))$ for all $a:A$ and $b:B$, such that for all identities $p:a =_A g(b)$, the fiber of $\epsilon(a, b)$ at $p$ is contractible. 

$$\mathrm{isInv}(f, g) \coloneqq \prod_{a:A} \prod_{b:B} \sum_{\epsilon(a, b):(f(a) =_B b) \to (a =_A g(b))} \prod_{p:a =_A g(b)} \mathrm{isContr}(\mathrm{fiber}(\epsilon(a, b), p))$$

#### Coherent inverse functions

Given [[types]] $A$ and $B$ and a [[function]] $f:A \to B$, a __coherent inverse function__ of $f$ is a quasi-inverse function $g:B \to A$ with [[homotopies]] 

$$G:\prod_{x:B} f(g(x)) =_B x \qquad H:\prod_{x:A} g(f(x)) =_A x$$

which additionally has one of the two [[homotopies]]
$$K:\prod_{x:A} \mathrm{ap}_{B}(f, g(f(x)), x, H(x)) =_{g(f(x)) =_A x} G(f(x)) \qquad L:\prod_{x:B} H(g(x)) =_{f(g(x)) =_B x} \mathrm{ap}_{A}(g, f(g(x)), x, G(x)) $$

The type of coherent inverse functions of $f$ is given by one of the following types

$$\mathrm{CohInv}_1(f) \coloneqq \sum_{g:B \to A} \sum_{G:\prod_{x:B} f(g(x)) =_B x} \sum_{H:\prod_{x:A} g(f(x)) =_A x} \left(\prod_{x:A} \mathrm{ap}_{B}(f, g(f(x)), x, H(x)) =_{g(f(x)) =_A x} G(f(x))\right)$$

$$\mathrm{CohInv}_2(f) \coloneqq \sum_{g:B \to A} \sum_{G:\prod_{x:B} f(g(x)) =_B x} \sum_{H:\prod_{x:A} g(f(x)) =_A x} \left(\prod_{x:B} H(g(x)) =_{f(g(x)) =_B x} \mathrm{ap}_{A}(g, f(g(x)), x, G(x))\right)$$

$f$ is called a **half adjoint equivalence** if it has a coherent inverse function. 

## Properties

Given functions $f:A \to B$ and $g:B \to A$ and homotopies $G:\prod_{x:B} f(g(x)) =_B x$ and $H:\prod_{x:A} g(f(x)) =_A x$, there are elements 
$$\mathrm{QInvToCohInv}_1(f, g, G, H):\prod_{x:A} \mathrm{ap}_{B}(f, g(f(x)), x, H(x)) =_{g(f(x)) =_A x} G(f(x))$$
$$\mathrm{QInvToCohInv}_2(f, g, G, H):\prod_{x:B} H(g(x)) =_{f(g(x)) =_B x} \mathrm{ap}_{A}(g, f(g(x)), x, G(x))$$

which satisfies the [[commutative squares]] for all elements $a:A$ and $b:B$

$$
  \array{& f(g(f(g(b)))) & \overset{G(f(g(b))}= & f(g(b)) & \\
          \mathrm{ap}_{B}(f, g(f(b)), b, H(b)) & \Vert & =_{f(g(f(g(b)))) =_B b} & \Vert & \mathrm{QInvToCohInv}_2(f, g, G, H)(b) \\
          & f(g(b)) & \underset{G(b)}= & b & \\
}$$

$$
  \array{& g(f(g(f(a)))) & \overset{H(g(f(a))}= & g(f(a)) & \\
          \mathrm{ap}_{A}(g, f(g(a)), a, G(a)) & \Vert & =_{g(f(g(f(a)))) =_A a} & \Vert & \mathrm{QInvToCohInv}_1(f, g, G, H)(a) \\
          & g(f(a)) & \underset{H(a)}= & a & \\
}$$

Thus, there are functions 
$$\lambda g:B \to A.\lambda G:\prod_{x:B} f(g(x)) =_B x.\lambda H:\prod_{x:A} g(f(x)) =_A x.\mathrm{QInvToCohInv}_1(f, g, G, H):\mathrm{QInv}(f) \to \mathrm{CohInv}_1(f)$$ 
and 
$$\lambda g:B \to A.\lambda G:\prod_{x:B} f(g(x)) =_B x.\lambda H:\prod_{x:A} g(f(x)) =_A x.\mathrm{QInvToCohInv}_2(f, g, G, H):\mathrm{QInv}(f) \to \mathrm{CohInv}_2(f)$$

Every coherent inverse function is a quasi-inverse function by forgetting the additional coherence condition. 

\begin{theorem}
If a function $f:A \to B$ has a coherent inverse function, then for all elements $b:B$ the fiber of $f$ at $b$ is contractible.
\end{theorem}

\begin{proof}
...
\end{proof}

## Related concepts

* [[inverse]], [[inverse morphisms]]

* [[inverse functor]]

* [[isomorphism]]

* [[equivalence in homotopy type theory]]

Not really related

* [[inverse image]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))

* [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

[[!redirects inverse function]]
[[!redirects inverse functions]]
[[!redirects inverse map]]
[[!redirects inverse maps]]

[[!redirects quasi-inverse]]
[[!redirects quasi-inverse function]]
[[!redirects quasi-inverse functions]]
[[!redirects quasi-inverse map]]
[[!redirects quasi-inverse maps]]

[[!redirects quasi-invertible]]
[[!redirects quasi-invertible function]]
[[!redirects quasi-invertible functions]]
[[!redirects quasi-invertible map]]
[[!redirects quasi-invertible maps]]

[[!redirects coherent inverse]]
[[!redirects coherent inverse function]]
[[!redirects coherent inverse functions]]
[[!redirects coherent inverse map]]
[[!redirects coherent inverse maps]]

[[!redirects coherently invertible]]
[[!redirects coherently invertible function]]
[[!redirects coherently invertible functions]]
[[!redirects coherently invertible map]]
[[!redirects coherently invertible maps]]

[[!redirects half adjoint equivalence]]
[[!redirects half adjoint equivalences]]
[[!redirects half-adjoint equivalence]]
[[!redirects half-adjoint equivalences]]