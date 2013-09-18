
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

_Laurent series_ generalize [[power series]] by allowing both positive and negative powers. In particular, _Laurent series_ with complex coefficients generalize [[Taylor series]] of analytic functions to meromorphic functions. A Laurent series for a meromorphic function $f(z)$ at finite $z\in\mathbb{C}$ has the form
$$ f(z) = \sum_{n=k}^{\infty}f_n z^n, $$
where $k$ is merely constrained to be finite and is often negative.

## Definition

A Laurent series in one variable $z$ over a commutative unital ring $k$ is a [[doubly infinite series]] 
$$ f(z) = \sum_{n=-\infty}^{\infty} f_n z^n ,$$
where $f_n\in k$.

The questions of convergence are a separate issue. 
In complex analysis, the Laurent series describes a meromorphic function in a neighborhood 
around some point $z$ (possibly with a pole in $z$)
if all but finitely many negatively indexed terms are zero. 

## Properties

### Algebraic closure

+-- {: .num_theorem #Puiseux} 
###### Theorem 
If $K$ is [[algebraically closed field|algebraically closed]] and has [[characteristic]] 0, then the [[algebraic closure]] of the field of Laurent series over $K$ is the field of [[Puiseux series]] over $K$.

=-- 

See at _[[Puiseux series]]_ for more details.


* [Doubly Infinite Laurent Series](http://math.rutgers.edu/~sdurst/DILS.html), lectures for formal Laurent series in [[vertex operator algebra]] context