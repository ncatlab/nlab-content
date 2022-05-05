

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Combinatorics
+--{: .hide}
[[!include combinatorics - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $n$ a [[natural number]], the double factorial $(2n+1)!!$ is defined to be the product $(2n+1)(2n-1)\ldots 1$. Alternatively, in terms of the ordinary [[factorial]],

\[(2n-1)!! = \frac1{2^n} \frac{(2n)!}{n!}\]

so that in particular, $(-1)!!$ is defined to be $1$. 

Double-factorials have a number of applications in [[enumerative combinatorics]]. They are particularly prone to appear whenever dealing with [[binomial coefficients]] 

\[\binom{x}{n} = \frac{x(x-1)\ldots (x-n+1)}{n!}\]

in the case $x = 1/2$ or $x = -1/2$, or when dealing with middle binomial coefficients $\binom{2n}{n}$, or when dealing with the values of the [[Gamma function]] at half-integers. 

According to the combinatorial interpretation below, the exponential generating function of the sequence $a_n$ defined by $a_{2n} = (2n-1)!!$ and $a_{2n+1} = 0$ is 

\[\sum_{n \geq 0} \frac{a_n x^n}{n!} = \exp(x^2/2).\]

This is related to the fact that the double-factorials also crop up in calculations dealing with [[Gaussian integrals]] such as 

\[\int_0^\infty p(x) e^{-x^2/2}\; d x\]

for even polynomials $p$, with consequent applications in [[quantum mechanics]], for example calculations surrounding the [[quantum harmonic oscillator]]. See the section below on moments of Gaussian distributions. 

## Combinatorial interpretation 

The double-factorials $(2n-1)!!$ count the number of [[involutions]] without [[fixed points]] on a set with $2n$ elements, or the number of [[partitions]] of a $(2n)$-element set into $2$-element sets, or the number of isomorphism classes of [[rooted chord diagrams]] with $n$ chords. This follows readily from the exponential generating function expression above, and is related to the [[species]] composition of the exponential species $\exp$ (the terminal object in the category of species) with the species $x^2/2$, defined to be terminal at $2$-element sets and empty at others.

## Moments of the standard Gaussian distribution 

The computation begins with a famous observation 

\[\frac1{\sqrt{2\pi}} \int_{-\infty}^\infty e^{-x^2/2}\; d x = 1\]

which says that $x \mapsto \frac1{\sqrt{2\pi}} e^{-x^2/2}$ is a probability distribution on $\mathbb{R}$ with Lebesgue measure. 

+-- {: .num_prop} 
###### Proposition 
For each $n \geq 0$, 

\[\frac1{\sqrt{2\pi}} \int_{-\infty}^\infty x^n e^{-x^2/2}\; d x = a_n\] 

where $a_n$ are the MacLaurin coefficients in $e^{y^2/2} = \sum_{n \geq 0} \frac{a_n y^n}{n!}$, namely, $a_n = 0$ if $n$ is odd, and $a_{2n} = (2n-1)!!$. 
=-- 

+-- {: .proof} 
###### Proof 
By matching MacLaurin coefficients, it is enough to show 

\[\sum_{n \geq 0} \left(\frac1{\sqrt{2\pi}} \int_{-\infty}^\infty x^n e^{-x^2/2} \; d x\right) \frac{y^n}{n!} = e^{y^2/2}\] 

However, the left side equals 

\[\array{
\frac1{\sqrt{2\pi}} \displaystyle\int_{-\infty}^\infty \sum_{n \geq 0} \frac{(x y)^n}{n!} e^{-x^2/2}\; d x & = & \frac1{\sqrt{2\pi}} \displaystyle\int_{-\infty}^\infty e^{x y} e^{-x^2/2} \;d x \\ 
 & = & e^{y^2/2} \cdot \frac1{\sqrt{2\pi}} \displaystyle\int_{-\infty}^\infty e^{-(x-y)^2/2} \;d x \\ 
 & = & e^{y^2/2}
}\] 

where the last line results from the famous observation by substituting $x-y$ for $x$. 
=-- 


## References

See also 

* Wikipedia, _[Double factorial](https://en.wikipedia.org/wiki/Double_factorial)_

[[!redirects double factorials]]

[[!redirects double-factorial]]
[[!redirects double-factorials]]
