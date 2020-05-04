

#Contents#
* table of contents
{:toc}

## Idea

(...)

## Definition

For $n \in \mathbb{N}$ a  [[natural number]], the _$n$th Hermite polynomial_ is the [[polynomial]] in one [[variable]] $x$ with [[coefficients]] in the [[real numbers]] (and as such a naturally regarded as a [[smooth function]] $\mathbb{R} \to \mathbb{R}$ on the [[real line]]) which is given by the following expression:

\[
  \label{RodriguezFormulaForHermitePolynomials}
  H_n(x)
  \;\coloneqq\;
  \frac{
    (-1)^n
  }{
    \sqrt{
      n! 2^n \sqrt{\pi}
    }
  }
  \exp\left( 
    \tfrac{1}{2}
    x^2
  \right)
  \frac{d}{d x^n}
  \exp\left( 
    -\tfrac{1}{2}
    x^2
  \right)
  \,,
\]

where $\exp(-)$ denotes the [[exponential function]] and $d/d x^n$ denotes the $n$th [[derivative]] with respect to $x$. 

Sometimes one writes $H_n(x)$ for the polynomial above, times $\exp\left( 
-\tfrac{1}{2} x^2\right)$. We will follow that custom below. 


## Properties

### Orthonormality

Regarded as [[smooth functions]] $H_n \colon \mathbb{R} \to \mathbb{R}$ on the [[real line]], the Hermite polynomials (eq:RodriguezFormulaForHermitePolynomials) form an [[orthonormal basis]] of [[square-integrable functions]] with respect to the [[p-norm|2-norm]], in that the [[integration]] over their product satisfies

\[
  \label{Orthonormalizty}
  \int_{\mathbb{R}^1}
    H_{n}(x)
    H_{m}(x)
    \,
    d x
  \;=\;
  \delta_{n,m}
\]

(where on the right we have the [[Kronecker delta]]).

### Recursion relations


$$
  \frac{d}{d x}
  H_n(x)
  \;=\;
  \sqrt{
    \tfrac
      {n}
      {2}
  }
  H_{n-1}(x)
  -
  \sqrt{
    \tfrac
      {n-1}
      {2}
  }
  H_{n+1}(x)
$$


## Properties

(...)

## Related concepts

* [[special function]]

* [[hypergeometric function]]

## References

Named after [[Charles Hermite]].

See also:

* [[eom]], _[Hermite polynomials](https://www.encyclopediaofmath.org/index.php/Hermite_polynomials)_

* Wikipedia, _[Hermite polynomials](https://en.wikipedia.org/wiki/Hermite_polynomials)_

* Keith Y. Patarroyo, _A digression on Hermite polynomials_ ([arXiv:1901.01648](https://arxiv.org/abs/1901.01648))

[[!redirects Hermite polynomials]]

