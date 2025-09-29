

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
  (-1)^n
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

Similarly, the _Hermite functions_ are

\[
  \label{RodriguezFormulaForHermiteFunctions}
  \begin{aligned}
    h_n(x)
    & 
    \coloneqq\;
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
      -
      x^2
    \right)
    \\
    & =
    \frac{
      1
    }{
      \sqrt{
        n! \sqrt{\pi}
      }
    }
    \,
    H_n
    \big(
      \sqrt{2} x
    \big) 
    \,
    \exp
    \left( 
      -\tfrac{1}{2}x^2
    \right)
  \end{aligned}
  \,,
\]



## Properties

### Orthonormality

Regarded as [[smooth functions]] $h_n \colon \mathbb{R} \to \mathbb{R}$ on the [[real line]], the Hermite functions (eq:RodriguezFormulaForHermiteFunctions) form an [[orthonormal basis]] of [[square-integrable functions]] with respect to the [[p-norm|2-norm]], in that the [[integration]] over their product satisfies

\[
  \label{Orthonormalizty}
  \int_{\mathbb{R}^1}
    h_{n}(x)
    h_{m}(x)
    \,
    d x
  \;=\;
  \delta_{n,m}
\]

(where on the right we have the [[Kronecker delta]]).

### Recursion relations

(...)

\[
  \label{DifferentialRecursionRelationForHermiteFunctions}
  \frac{d}{d x}
  h_n(x)
  \;=\;
  \sqrt{
    \tfrac
      {n}
      {2}
  }
  h_{n-1}(x)
  -
  \sqrt{
    \tfrac
      {n-1}
      {2}
  }
  h_{n+1}(x)
\]

(...)



## Related concepts

* [[special function]]

* [[hypergeometric function]]

## References

Named after [[Charles Hermite]].

Review:

*  Zhi-yuan Huang, Jia-an Yan: *Hermite polynomials and Hermite functions*, Appendix A in: *Introduction to Infinite Dimensional Stochastic Analysis*, Mathematics and Its Applications **502**, Springer 2000  &lbrack;[doi:10.1007/978-94-011-4108-6](https://doi.org/10.1007/978-94-011-4108-6), [[HermitePolynomialsAndHermiteFunctions.pdf:file]]&rbrack;


See also:

* [[eom]]: _[Hermite polynomials](https://www.encyclopediaofmath.org/index.php/Hermite_polynomials)_

* Wikipedia: _[Hermite polynomials](https://en.wikipedia.org/wiki/Hermite_polynomials)_

* Keith Y. Patarroyo: _A digression on Hermite polynomials_ &lbrack;[arXiv:1901.01648](https://arxiv.org/abs/1901.01648)&rbrack;

[[!redirects Hermite polynomials]]

[[!redirects Hermite function]]
[[!redirects Hermite functions]]


