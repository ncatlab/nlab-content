
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

In [[trigonometry]] the _cotangent function_ is one of the basic [[trigonometric functions]].

## Definition


The contangent is the [[ratio]] of the [[cosine]] and the [[sine]]:


$$
  \cot(x) = \frac{\cos(x)}{\sin(x)}
$$

## Properties

### Relations with tangent function 

* The cotangent and tangent are reciprocal to each other: $\cot x = \frac1{\tan x}$.  

* The cotangent and tangent are complementary to each other: $\cot x = \tan (\frac{\pi}{2} - x)$. 

* Double angle formula: $\tan x = \cot x - 2\cot 2x$. 

### Relation to Bernoulli numbers 

The [[hyperbolic functions|hyperbolic]] analog $\coth x = \frac{e^x + e^{-x}}{e^x - e^{-x}}$ is related to $\cot x$ via the formula 

$$\cot x = i\coth i x.$$

Meanwhile $\coth x$ is related to the [[Bernoulli numbers]] $B_n$, defined by the exponential generating function 

$$\frac{x}{e^x - 1} = \sum_{n \geq 0} \frac{B_n x^n}{n!},$$ 

through a series of equations 

$$\frac{x}{e^x - 1} + \frac{x}{2} = \frac{x(2 + e^x - 1)}{2(e^x - 1)} = \frac{x}{2} \frac{e^x + 1}{e^x - 1} = \frac{x}{2} \frac{e^{x/2} + e^{-x/2}}{e^{x/2} - e^{-x/2}} = \frac{x}{2}\coth \frac{x}{2}.$$ 

Notice the right side defines an even function. Therefore 

$$\frac{x}{2}\coth \frac{x}{2} = \sum_{n \geq 0} \frac{B_{2n} x^{2n}}{(2n)!}$$ 

and so 

$$x \cot x = i x \coth i x = \sum_{n \geq 0} \frac{B_{2n} (2i x)^{2n}}{(2n)!} = \sum_{n \geq 0} (-1)^n \frac{B_{2n} 2^{2n} x^{2n}}{(2n)!}.$$

### "Eisenstein" series expansion

The cotangent is the [[logarithmic derivative]] of the [[sine function]]: 

$$\cot x = (\log (\sin x))'.$$ 

Applying this observation to the Euler-Weierstrass [[product formula for the sine function]] (see there for a proof): 

$$\sin (\pi x) = \pi x \prod_{n=1}^\infty \left(1 - \frac{x^2}{n^2}\right)$$ 

one obtains the following summation formula for the cotangent: 

$$\pi\, \cot (\pi x) = \frac1{x} + \sum_{n=1}^\infty \left(\frac1{x + n} + \frac1{x - n}\right)$$ 

This expansion was used by Eisenstein as a starting point for developing the theory of trigonometric functions; Eisenstein's account of elliptic functions (cf. the eponymous [[Eisenstein series]]), developed further by Weierstrass, Kronecker, and others, runs parallel to his trigonometric theory, as explained later by Weil. For some more details, see these [notes](#vsv) by Varadarajan. 

### Relation to zeta function values 

\begin{proposition} 
The power series identity 

$$\pi x \cot \pi x = 1 - 2\sum_{k \geq 0} \zeta(2k) x^{2k}$$ 
holds over an open domain where the series converges, ${|x|} \lt 1$. 
\end{proposition} 

\begin{proof} 
From the Eisenstein expansion, we have  
$$\pi\, \cot (\pi x) = \frac1{x} + \sum_{n=1}^\infty \left(\frac1{x + n} + \frac1{x - n}\right) = 1 + \sum_{n \geq 0} \frac{2x^2}{x^2 - n^2} = 1 - 2\sum_{n \geq 1} \frac{x^2/n^2}{1 - x^2/n^2}.$$
By a geometric series expansion, the last expression is 

$$1 - 2\sum_{n \geq 1} \sum_{k \geq 1} \left(\frac{x^2}{n^2}\right)^k = 1 - 2\sum_{k \geq 1} x^{2k} \sum_{n \geq 1} \frac1{n^{2k}}$$ 
which is the same as $1 - 2\sum_{k \geq 1} \zeta(2k)x^{2k}$. 
\end{proof} 

## Related concepts

* [[tangent function]]

* [[trigonometric identity]]

* [[Eisenstein series]] 

* [[product formula for the sine function]]

## References

* Wikipedia, _[Trigonometric functions -- tan](https://en.wikipedia.org/wiki/Trigonometric_functions#tan)_ 

* {#vsv} [[Veeravalli Varadarajan]], *Circular Functions* ([pdf](http://www.math.ucla.edu/~vsv/fullnotes.pdf)). 


[[!redirects cotangent functions]]
[[!redirects cotan]] 
[[!redirects cot]]
[[!redirects cotangent]]