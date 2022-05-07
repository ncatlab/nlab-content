

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

## Idea

Much like the [[Gamma function]] generalizes the functional equation

$$
  \Gamma(z + 1) \;=\; z \, \Gamma(z)
$$

to non-integer values of $z$, so the *Barnes $G$-function* $G(-)$ corresponds to the functional equation

$$
  G(z + 1) \;=\; \Gamma(z) \, G(z)
  \,.
$$

Just as for $z =n \in \mathbb{N}$, $\Gamma(n+1) = n!$, so $G(n+2) = n!(n-1)! \cdots 1!$.

## Definition

(...)

## Properties

### Special values

$$
  G(1/2)
  \;=\;
  2^{1/24} 
    \cdot 
  e^{ \tfrac{3}{2} \zeta^'(-1) }
    \cdot
  \pi^{ - 1/4 }
  \,.
$$

([WP here](https://en.wikipedia.org/wiki/Barnes_G-function#Value_at_1/2))

### Stirling-like asymptotics

$$
  ln G(1 + z)
  \;=\;
  z^2 
  \left( 
    \tfrac{1}{2} ln(z)
    -
    \tfrac{3}{4}
  \right)
  +
  \tfrac{1}{2}
  ln(2 \pi)
  z
  -
  \tfrac{1}{12} ln(z)
  + 
  \zeta^'(-1)
  +
  \mathcal{O}(z^{-1})
  \,,
$$

where $\zeta$ denotes the [[Riemann zeta function]]. 

(e.g. [WP here](https://en.wikipedia.org/wiki/Barnes_G-function#Asymptotic_expansion), [WMW (14)](#WMW))

### Relations to the Gamma-function

A version of the [[Gauss multiplication formula]] for the [[Gamma function]]:

$$
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \Gamma(j/2)
  \;=\;
  \frac
    {
      G(N/2+ 1)
      \cdot
      G(N/2 + 1/2)
    }
    { G(1/2) }
  \,.
$$

([Kotěšovec 13, p. 2](#Kotesovec))

To see this, consider two cases:

$N = 2M$:

$$
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \Gamma(j/2)
  \;=\;
\underoverset
    {j = 1}
    {M}
    {\prod}
  \Gamma(j)
\cdot 
\underoverset
    {j = 1}
    {M}
    {\prod}
  \Gamma(j - \frac{1}{2})
 \;=\;
G(M+1) \cdot G(M +1/2) /G(1/2)
 \;=\;
G(N/2 + 1) \cdot G(N/2 + 1/2)/G(1/2).
$$

$N = 2M+1$:

$$
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \Gamma(j/2)
  \;=\;
\underoverset
    {j = 1}
    {M}
    {\prod}
  \Gamma(j)
\cdot 
\underoverset
    {j = 1}
    {M+1}
    {\prod}
  \Gamma(j - \frac{1}{2})
 \;=\;
G(M+1) \cdot G(M +3/2) /G(1/2)
 \;=\;
G(N/2 + 1/2) \cdot G(N/2 + 1)/G(1/2).
$$

## References

See also:

* Wikipedia, *[Barnes G-function](https://en.wikipedia.org/wiki/Barnes_G-function)*

* {#WMW} WolframMathWorld, *[Barnes G-Function](https://mathworld.wolfram.com/BarnesG-Function.html)*

In the context of [counting](semistandard+Young+tableau#NumberOfSYTWithBoundedNumberOfRows) of [[standard Young tableaux]] of bounded height:

* {#Kotesovec13} Václav Kotěšovec, *Asymptotic of Young tableaux of bounded height*, 2013 ([pdf](http://www.kotesovec.cz/math_articles/kotesovec_young_tableaux_conjecture.pdf), [[KotesovecAsymptoticsOfBoundedYoungTableaux.pdf:file]])


[[!redirects Barnes G-functions]]

