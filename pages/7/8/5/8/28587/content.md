
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

The analogue of polynomial factorization of [[polynomial functions]] over the [[complex numbers]], but for [[entire function|entire]] [[complex numbers|complex]] [[analytic functions]], which come with a [[countable set]] of [[roots]] instead of a [[finite set]] of roots for polynomials.

## Definition

The Weierstrass primary factors are a [[sequence]] of functions on the complex functions inductively defined as 

$$E_0(z) = (1 - z)$$

$$E_{n + 1}(z) = E_{n}(z) e^{\frac{z^{n + 1}}{n + 1}}$$

Given a [[complex numbers|complex]] [[analytic function]] $f$ which is [[entire function|entire]] in the sense that the [[Taylor series]] expansion of $f$ [[convergence of a sequence|converges]] on all of the [[complex numbers]], and which has a zero of multiplicity $n$ at $z = 0$, the **Weierstrass factorization theorem** states that there exists a [[countable set]] of [[roots]] $z_i$ with index set $I$ such that 

$$
  f(z) = z^n e^{g(z)} \prod_{i \in I} E_{p_i}\left(\frac{z}{z_i}\right)
  \mathrlap{\,.}
$$

where $n$ is a natural number, $g(z)$ is an entire function and $E_{p_i}$ are Weierstrass primary factors and $p_i$ are natural numbers chosen to ensure the infinite product converges. 

## Examples

### Polynomial functions

For a [[polynomial function]] $f$ of degree $n$ with $m \leq n$ zeros at $z = 0$, which is always an [[entire function]], the [[countable set]] $I$ for [[roots]] $z_i$ is a [[finite set]] of cardinality $n - m$, the entire function $g(z)$ is equal to a constant $c$, and the Weierstrass primary functions used in the product is $E_{0}(z)$. Thus, Weierstrass factorization can be expressed as 

$$
  f(z) = z^m e^c \prod_{i = 1}^{n - m} E_{0}\left(\frac{z}{z_i}\right) = c^\prime z^n \prod_{i = 1}^{n - m} (z - z_i) \quad \mathrm{where} \quad c^\prime = e^c \prod_{i = 1}^{n - m} \frac{(-1)^{i}}{z_i}
  \mathrlap{\,.}
$$

which is precisely the [[fundamental theorem of algebra]] for complex polynomial functions. 

## In constructive mathematics

In constructive mathematics, the usual Weierstrass factorization theorem fails for the same reason that the [[fundamental theorem of algebra]] fails: the complex numbers are not a [[discrete field]]. As a result, there are a few alternatives for the Weierstrass factorization theorem a constructive mathematics. 

### Approximate Weierstrass factorization theorem

The approximate version of the Weierstrass factorization theorem states that given an [[entire function|entire]] [[complex numbers|complex]] [[analytic function]] $f$ with a zero of multiplicity $n$ at $z = 0$, for all [[positive number|positive]] [[rational numbers]] $\epsilon$ one can construct a countable set $I$ of complex numbers $z_i$ such that 

$$
  \vert f(z) - z^n e^{g(z)} \prod_{i \in I} E_{p_i}\left(\frac{z}{z_i}\right) \vert \lt \epsilon
  \mathrlap{\,.}
$$

where $n$ is a [[natural number]], $g(z)$ is an entire function and $E_{p_i}$ are Weierstrass primary factors and $p_i$ are natural numbers chosen to ensure the infinite product converges. 

### Using multisets of roots

Similarly to complex polynomials, instead of considering individual complex roots, one can instead consider [[multisets]] of complex roots for entire functions. 

## Related concepts

* [[algebraic closure]]

* [[fundamental theorem of algebra]]

## References

See also:

* Wikipedia: *[Weierstrass factorization theorem](https://en.wikipedia.org/wiki/Weierstrass_factorization_theorem)* 

[[!redirects Weierstrass factorisation theorem]]
