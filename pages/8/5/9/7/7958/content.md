
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Complex geometry
+-- {: .hide}
[[!include complex geometry - contents]]
=--
=--
=--

# The Cauchy integral theorem
* table of contents
{: toc}

## Idea

Cauchy's integral theorem states that [[contour integrals]] of [[holomorphic functions]] in the [[complex plane]] $\mathbb{C}$ are invariant under [[homotopy]] of paths.  In particular, if a function is holomorphic on a [[simply connected space|simply connected]] [[subspace]] of $\mathbb{C}$, then its contour integral on a path depends only on the beginning and ending points of the path, and indeed can be given by subtracting the values there of an [[antiderivative]] (in accordance with the second [[Fundamental Theorem of Calculus]]).


## Statement

Let $D$ be an [[open subset]] of the [[complex plane]] $\mathbb{C}$, let $a$ and $b$ be two points in $D$, let $\gamma_1$ and $\gamma_2$ be two [[curves]] in $D$ from $a$ to $b$, let the region between them also lie entirely within $D$, and let $f$ be a [[holomorphic function]] on $D$. Then we have

$$ \int_{\gamma_1} f(z) \,\mathrm{d}z = \int_{\gamma_2} f(z) \,\mathrm{d}z .$$

In particular we have 

$$ \int_{\gamma_1} f(z) \,\mathrm{d}z = 0 $$

if $a = b$ (because then $\gamma_2$ may be taken to be a constant); in other words, the contour integral of a holomorphic function is zero around any [[loop]] whose inside lies entirely within the function\'s domain.


## Related concepts


* [[Cauchy's integral formula]]

* [[Cauchy's theorems]]

* [[Goursat theorem]]

* [[Stokes theorem]]


## References

* Wikipedia, _[Cauchy integral theorem](https://en.wikipedia.org/wiki/Cauchy's_integral_theorem)_


category: analysis

[[!redirects Cauchy integral theorem]]
[[!redirects Cauchy's integral theorem]]
[[!redirects Cauchy’s integral theorem]]
[[!redirects Cauchy\'s integral theorem]]
