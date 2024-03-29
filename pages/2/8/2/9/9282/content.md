
#Contents#
* table of contents
{:toc}

## Idea

What is called _Newton's method_ after [[Isaac Newton]] is an [[recursion|recursive]] procedure for computing approximations to zeros ("[[roots]]") of [[differentiable functions]] with values in the [[real numbers]].

## Definition

Let $f \colon \mathbb{R} \to \mathbb{R}$ be a [[differentiable function]] and for $x_0 \in \mathbb{R}$ a [[real number]] such that the first [[derivative]] $f' \colon \mathbb{R} \to \mathbb{R}$ is non-vanishing at $x_0$. 

Let $\{x_n \in \mathbb{R} | n \in \mathbb{N}\}$ be defined [[recursion|recursively]] by

$$
  x_{n+1}
  \coloneqq
  x_n 
  -
  \frac{f(x_n)}{f'(x_n)}
  \,.
$$

Under mild conditions, this sequence [[convergence|converges]] to a zero/[[root]] of $f$.

## Related concepts

* [[Puiseux series]]

## References

* Wikipedia, _[Newton's method](http://en.wikipedia.org/wiki/Newton%27s_method)_

[[!redirects Newton method]]