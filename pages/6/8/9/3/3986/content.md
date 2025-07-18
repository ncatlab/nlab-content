
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A trigonometric identity is (formally) a [[commutative diagram]] in the [[category]] of [[cartesian spaces]] and [[partial functions]] whose edges are labelled by [[rational functions]] (or sometimes [[algebraic functions]]) and [[trigonometric functions]]. 

Slightly more precisely: each rational function $p(x_1, \ldots, x_n) \in \mathbb{R}(x_1, \ldots, x_n)$ is interpreted as a [[partial function]] $\mathbb{R}^n \hookleftarrow D \stackrel{f}{\to} \mathbb{R}^n$ where $D$ is the "natural domain" of $p$ (see [[rational function]] for more discussion); these are partial [[analytic functions]]. The basic trigonometric functions [[sine]] ($\sin$) and [[cosine]] ($\cos$) are (total) [[analytic functions]] $\mathbb{R} \to \mathbb{R}$. All of these may be interpreted as partial functions $\mathbb{R}^n \rightharpoonup \mathbb{R}^n$, and generate a class of functions by applying the [[monoidal category]] structure on the category of partial functions that is induced by the [[cartesian product]] on cartesian spaces. A trigonometric identity is then (formally) an [[equality]] of morphisms in the monoidal category thus generated. 

Of course, this is complete overkill; category theorists are not oblivious to the fact that this is exactly the kind of description lampooned in Linderholm's _Mathematics Made Difficult_. It's just a formal way of covering bases. So let us add that in practice, a trigonometric identity usually involves functions obtained by substituting trigonometric functions into rational functions, or substituting rational _linear_ (affine) functions into trigonometric functions: the class of functions considered is usually fairly limited in scope. 

## Examples

Virtually all trigonometric identities can be seen as arising from suitable [[exponential function]] identities on _[[complex numbers]]_ such as 

* $\exp(i t) = \cos(t) + i\sin(t)$ ([[Euler's formula]]); 

* $\exp(z + w) = \exp(z)\exp(w)$,

* $\widebar{\exp(z)} = \exp(\widebar{z})$. 

These imply the *sum of angles* formulas for the [[sine function]] and the [[cosine function]] as follows:

\[
  \label{SumOfAnglesFormulas}
  \begin{array}{rcl}
    \sin\left( \alpha + \beta \right)
    &=&
    \sin(\alpha) \cos(\beta) + \cos(\alpha) \sin(\beta)
    \\
    \cos(\alpha + \beta)
    &=&
    \cos(\alpha) \cos(\beta) - \sin(\alpha) \sin(\beta)
  \end{array}
\]

which in turn implies

\[
  \label{ProductOfSinWithCos}
  \sin(\alpha) \cos(\beta) 
  \;=\; 
  \tfrac{1}{2}
  \left(
    \sin(\alpha + \beta) + \sin(\alpha - \beta)
  \right)
\]

etc.


## Related entries

* See also [[trigonometric function]] for some discussion. 

* [[trigonometry]]

## References

See also

* Wikipedia, _[List of trigonometric identities](https://en.wikipedia.org/wiki/List_of_trigonometric_identities)_

[[!redirects trigonometric identities]]
