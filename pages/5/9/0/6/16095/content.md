
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

## Definition

The **inverse function theorem** says that given any [[sequentially Cauchy complete]] [[Archimedean field]] $\mathbb{R}$ and a [[continuously differentiable function]] $f:I \to \mathbb{R}$ from an [[open interval]] $I \subseteq \mathbb{R}$ such that for all points $a \in I$,
$$\left| \frac{d f}{d x}(a) \right| \gt 0$$
the [[inverse function]] $f^{-1}:\mathrm{im}(f) \to \mathbb{R}$ exists and is unique and is defined by the first-order nonlinear [[ordinary differential equation]]

$$\left(\frac{d f}{d x} \circ f^{-1}\right) \frac{d f^{-1}}{d x} = 1$$

with initial condition $f^{-1}(f(a)) = a$. Classically, $\mathbb{R}$ is essentially unique, but constructively, there are multiple inequivalent [[sequentially Cauchy complete]] [[Archimedean fields]]. 

## Related concepts

* [[Banach fixed-point theorem]]

* [[Picard–Lindelöf theorem]]

* [[regular value]]

* [[Mather's stability theorem]]

* [[real quadratic function]]

* [[real square root]]

## References

* Wikipedia, _[Inverse function theorem](https://en.wikipedia.org/wiki/Inverse_function_theorem)_

