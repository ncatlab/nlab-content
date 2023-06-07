
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Trigonometry
+-- {: .hide}
[[!include trigonometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[trigonometry]], the _tangent function_ is one of the basic [[trigonometric functions]]. 

## Definition

The tangent function is the [[ratio]] of the [[sine]] and the [[cosine]]:


$$
  \tan(x) = \frac{\sin(x)}{\cos(x)}
$$

## Properties 

* The tangent function $f(x) = \tan x$ is of course odd, and obeys a functional equation ('addition formula') 
$$f(x + y) = \frac{f(x) + f(y)}{1 - f(x)f(y)}.$$ 

* The [[hyperbolic functions|hyperbolic]] analog $\tanh x$, related to the tangent by 
$$\tan(i x) = i\tanh x,$$ 
arises in [[special relativity theory]] in connection with [[rapidity]]. 

* The [[MacLaurin series]] for the tangent function arises in enumerative combinatorics, especially when bundled with the [[secant function]]. Here the sum 
$$\sec x + \tan x = \sum_{n \geq 0} \frac{E_n x^n}{n!}$$ 
is the exponential generating function of a sequence of natural numbers $E_k$ that count "zigzag permutations" on the set $\{1, \ldots, k\}$, i.e., permutations $a_1 a_2 \ldots a_k$ where $a_1 \gt a_2 \lt a_3 \gt \ldots$. The *tangent numbers*, which are the coefficients $E_n$ when $n$ is odd, are related to [[Bernoulli numbers]] through the formula 
$$(-1)^{k-1} B_{2k} = \frac{2k \cdot E_{2k-1}}{2^{2k}(2^{2k} - 1)}.$$  

## Related concepts

* [[tangent]]

* [[cotangent function]]

* [[arctan]]

* [[trigonometric identity]]

* [[tangent vector]]

## References

* Wikipedia, _[Trigonometric functions -- tan](https://en.wikipedia.org/wiki/Trigonometric_functions#tan)_


[[!redirects tangent functions]]

[[!redirects tan]]