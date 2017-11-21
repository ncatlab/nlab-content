
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $(X, \mu)$ a [[measure space]] of finite total measure $\int_X \mu$ and for $f$ an [[measurable function]] on $X$, a _[[random variable]]_, then its **expectation value** is 

$$
  \langle f\rangle
  \coloneqq
  \frac{\int_X f \cdot \mu}{\int_X \mu}
 \,.
$$

In terms of the [[probability measure]] $\mu_P \coloneqq \frac{1}{\int_X \mu} \mu$ this is simply the [[integral]]

$$
  \langle f\rangle
  = 
 \int_X f \cdot \mu_P
  \,.
$$

## Related concepts

* [[moment]]

* [[vacuum expectation value]]

* [[Feynman diagram]]

[[!redirects expectation values]]
