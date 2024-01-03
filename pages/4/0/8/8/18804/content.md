
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

In [[trigonometry]], the _tangent function_ "$tan$" is one of the basic [[trigonometric functions]]. 

\begin{imagefromfile}
    "file_name": "Mathnet-TangentFunction.jpg",
    "float": "left",
    "width": 220,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 10,
        "right": 15, 
        "left": 0
    },
    "caption": "From [Mathnet](#Mathnet)"
\end{imagefromfile}

The tangent function may be understood as computing the [[length]] of the segment (shown in blue) of a [[tangent]]  (whence the name) to a unit [[circle]]  inside the [[Euclidean plane]], between its point of tangency and its intersection with any radial line, as a [[function]] of the [[angle]] ${\color{red}\theta}$ between that radial line and the one [[orthogonal]] to the [[tangent]].

Since, by definition of the [[sine function]] "$sin$" and the [[cosine function]] "$cos$", that radial line has [[distance]] $sin(\theta)$ from the perpendicular line where it crosses the unit circle at $cos(\theta)$ along that perpendicular line, the length of that tangential line segment [[equality|equals]] the [[ratio]] $sin(\theta)/cos(\theta)$, and this is how the tangent function is often defined.

\linebreak

## Definition

The tangent function is the [[ratio]] of the [[sine]] and the [[cosine]], where this is defined:


$$
  \theta 
    \,\in\, 
  \mathbb{R} 
    \setminus 
  \big\{
    (k+1/2)\pi
    \,\big\vert\,
    k \in \mathbb{Z}
  \big\}
  \;\;\;\;\;\;\;\;\;\;\;\;\;
    \vdash
  \;\;\;\;\;\;\;\;\;\;\;\;\;
  \tan(\theta) 
  \,\coloneqq\, 
  \frac{\sin(\theta)}{\cos(\theta)}
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
They are related to values of the [[zeta function]] by the formula 
$$2(2^{2k}-1)\zeta(2k) = \frac{E_{2k-1}\pi^{2k}}{(2k-1)!}.$$ 
Both of these facts may be verified by putting together corresponding facts for the [[cotangent function]] (see there) with the double angle formula 
$$\tan x = \cot x - 2\cot(2x).$$

## Related concepts

* [[tangent]], [[tangent vector]]

* [[cotangent function]]

* [[arctan]]

* [[trigonometric identity]]

## References

* Wikipedia, _[Trigonometric functions -- tan](https://en.wikipedia.org/wiki/Trigonometric_functions#tan)_

* {#Mathnet} Mathnet, *[tangent](https://www.math.net/tangent)*


[[!redirects tangent functions]]

[[!redirects tan]]