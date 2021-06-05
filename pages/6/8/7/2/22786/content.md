+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


# Contenta
* table of contents
{: toc}

## Idea

Exponential rings are [[rings]] that behave like the [[real numbers]] with its [[exponential map]]. 

## Definitions

A [[ring]] $R$ is a __exponential ring__ if it is equipped with a [[monoid]] [[homomorphism]] $e^{(-)}:R \to R$ from the additive monoid of $R$ to the multiplicative monoid of $R$: 

$$e^{0} = 1$$

$$e^{a + b} = e^a \cdot e^b$$

## Properties

The monoid homomorphism is an [[group]] homomorphism into the multiplicative subgroup of two-sided [[units]] of $R$, due to the fact that the additive monoid of $R$ is a [[group]]. 

### Trigonometric functions

If an exponential ring $R$ has elements $i$ and $\frac{1}{2}$ in $R$ such that $i \cdot i = -1$ and $\frac{1}{2} + \frac{1}{2} = 1$, then the __[[sine]]__ and __[[cosine]]__ could be defined as 

$$
\sin{x} \coloneqq \frac{1}{2}\cdot i\cdot (e^{-i\cdot x} - e^{i\cdot x}) = \frac{1}{2}\cdot (e^{-x \cdot i} - e^{x \cdot i}) \cdot i
$$

$$
\cos{x} \coloneqq \frac{1}{2}\cdot (e^{i\cdot x} + e^{-i\cdot x})
$$

It could be proven from these definitions that the sine and cosine satisfy various [[trigonometric identities]]. 

## Examples

* Every ring can be made into a exponential ring by defining $e^a \coloneqq 1$ for all $a$ in $R$. 

* Any [[cyclic group|cyclic ring]] $\mathbb{Z}/2n\mathbb{Z}$ with $e^{(-)}$ defined such that $e^{a} = 1$ for $a \equiv 0 \mod 2$ and $e^{a} = -1$ for $a \equiv 1 \mod 2$ is an exponential ring. 

* The real numbers and complex numbers with the usual [[exponential map]] $\exp$ are a exponential ring. 

* An exponential ring that is a [[field]] is a __exponential field__. 

## Related concepts

* [[exponential map]]

* [[Pythagorean ring]]

## External links

* Wikipedia, *[Exponential ring](https://en.wikipedia.org/wiki/Exponential_ring)*