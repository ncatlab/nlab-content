
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

The _elementary symmetric polynomial_ on $n$ [[variables]] $\{X_i\}$ of degree $k \leq n$ is the [[polynomial]]

$$
  \sigma_k(X_1, \cdots, X_n)
  \coloneqq
  \sum_{1 \leq i_1 \lneq \cdots \lneq i_k \leq n}
  X_{i_1} \cdots X_{i_k}
  \,.
$$

Equivalently these are the degree-$k$ summands in the polynomial

$$
  (1+X_1)(1+X_2) \cdots (1+X_n)
$$

These polynomials form a [[basis]] for the [[Lambda-ring]] of [[symmetric functions]].

## Examples

* The [[Chern classes]] are, under the [[splitting principle]], elementary symmetric polynomials of the [[first Chern classes]].

## Related concepts

* [[simple root]]

## References

* Wikipedia, _[Elementary symmetric polynomial](https://en.wikipedia.org/wiki/Elementary_symmetric_polynomial)_

[[!redirects elementary symmetric polynomials]]

[[!redirects elementary symmetric function]]
[[!redirects elementary symmetric functions]]