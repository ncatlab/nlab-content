
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea 

The [[irrational number]] conventionally denoted $e$ (a notation credited to [[Euler]], hence also called the _[[Euler number]]_) is the base of the natural [[logarithm]]; it is approximately 2.71828182845 in decimal notation. 


## Definition 

There are numerous ways of defining $e$. One is 

$$e \coloneqq \sum_{n \geq 0} \frac1{n!} = 1 + 1 + \frac1{2!} + \frac1{3!} + \ldots.$$ 

This can be interpreted as the [[groupoid cardinality]] for $core(FinSet)$. Perhaps more important than the [[constant function|constant]] $e$ is the standard [[exponential function]] (defined for all [[complex numbers]] $x$) 

$$\exp(x) = \sum_{n \geq 0} \frac{x^n}{n!}$$ 

for which $e = \exp(1)$. This exponential function is especially convenient because it is uniquely characterized as a function $f(x)$ equal to its own [[derivative]] such that $f(0) = 1$ (necessary in order that it satisfy the exponential law $f(x + y) = f(x)f(y)$). 


## Lay geometric description 

Construct a [[polar coordinates|polar coordinate grid]] (consisting of radial lines through a point called the origin, and concentric circles centered at the origin). Draw a curve starting at any point except the origin in such a way that at each of its points $p$, the tangent at $p$ meets the radial line at $p$ in a 45 degree angle. This curve is called a _logarithmic spiral_. Then, following the trajectory of the spiral inward (towards the origin, so to speak) through one radian from $p$ to a second point $q$, the distance from $p$ to the origin differs to the distance from $q$ to the origin by a factor of $e$. 

Equivalently, imagine four ants situated at the corners of a square, and imagine that at some instant each begins crawling toward its neighbor looking clockwise from above, each at the same speed. The trajectory of each ant is a logarithmic spiral as described above, and the same description of $e$ applies. 

## Irrationality 

It is a simple matter to show that $e$ is [[irrational number|irrational]]. For if on the contrary we have $e = p/q$, then $e \cdot n!$ would be an integer for any $n \geq q$. However, 

$$e \cdot n! = integer + \frac1{n+1} + \frac1{(n+1)(n+2)} + \ldots$$ 

where the nonzero tail after the integer part is bounded above by $\sum_{k=1}^\infty 1/(n+1)^k = 1/n \lt 1$ for $n \gt 1$, giving a contradiction. 

It is harder to show that $e$ is transcendental. An online proof (written up by David Richeson) may be found [here](https://divisbyzero.com/2010/09/28/the-transcendence-of-e/). 

## Related entries

* [[Euler number]]

* [[exponential map]]

* [[pi]]

* [[golden ratio]]

## References 

* [Wikipedia](http://en.wikipedia.org/wiki/E_%28mathematical_constant%29) 

* Eli Maor, _e: The Story of a Number_, Princeton University Press (1994). ISBN 0-691-05854-7. 
