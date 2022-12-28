
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$, the [[group of units]] of the [[ring]] of [[integers modulo n]]

$$
  \left(
    \mathbb{Z}/n
  \right)^\times
$$

is typically called the _multiplicative group of integers modulo $n$_. 

This consists of all those elements $k \in \mathbb{Z}/n$ which are represented by [[coprime integers]] to $n$. It is typically denoted $\mathbb{Z}/n ^\ast$. 

## Euler totient function 

The cardinality ${|(\mathbb{Z}/n)^\times|}$ is often denoted $\phi(n)$ (after Euler), and $\phi$ is known as the Euler totient function. 

The function $\phi$ is *multiplicative* in the standard number theory sense: $\phi(m n) = \phi(m)\phi(n)$ is $m$ and $n$ are coprime. This is a corollary of the [[Chinese remainder theorem]], which asserts that the canonical ring map 

$$\mathbb{Z}/m n \to \mathbb{Z}/m \times \mathbb{Z}/n$$ 

is an isomorphism if $m, n$ are coprime. Thus, if $n = p_1^{r_1} \ldots p_k^{r_k}$ is the prime factorization of $n$, we have 

$$\phi(n) = \phi(p_1^{r_1}) \ldots \phi(p_k^{r_k}).$$ 

Furthermore, as $\mathbb{Z}/p^r$ is a [[local ring]] with maximal ideal $p(\mathbb{Z}/p^r)$, the cardinality of the group of units is 

$$\phi(p^r) = p^r - p^{r-1} = p^{r-1}(p-1).$$  

## Related concepts

* [[integers modulo n]]

* [[cyclic group]]

* [[Q/Z]]

## External links

* Wikipedia, _[Multiplicative group of integers modulo n](https://en.wikipedia.org/wiki/Multiplicative_group_of_integers_modulo_n)_

[[!redirects multiplicative groups of integers modulo n]]

[[!redirects modulo]]
