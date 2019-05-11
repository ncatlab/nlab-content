
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

### Series expansion

The cotangent is the [[logarithmic derivative]] of the [[sine function]]: 

$$\cot x = (\log (\sin x))'.$$ 

Applying this observation to the Euler-Weierstrass product formula for the sine: 

$$\sin (\pi x) = \pi x \prod_{n=1}^\infty \left(1 - \frac{x^2}{n^2}\right)$$ 

one obtains the following summation formula for the cotangent: 

$$\pi\, \cot (\pi x) = \frac1{x} + \sum_{n=1}^\infty \left(\frac1{x + n} + \frac1{x - n}\right)$$ 

This expansion was used by Eisenstein as a starting point for developing the theory of trigonometric functions; Eisenstein's account of elliptic functions, developed further by Weierstrass, Kronecker, and others, runs parallel to his trigonometric theory, as explained later by Weil. For some more details, see these [notes](#vsv) by Varadarajan. 

## Related concepts

* [[tangent function]]

* [[trigonometric identity]]

## References

* Wikipedia, _[Trigonometric functions -- tan](https://en.wikipedia.org/wiki/Trigonometric_functions#tan)_ 

* {#vsv} [[Veeravalli Varadarajan]], *Circular Functions* ([pdf](http://www.math.ucla.edu/~vsv/fullnotes.pdf)). 


[[!redirects cotangent functions]]
[[!redirects cotan]] 
[[!redirects cot]]
[[!redirects cotangent]]