

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--


# The $\Gamma$ function
* table of contents
{: toc}

## Idea and Definition 

[[Leonhard Euler]] solved the problem of finding a [[function]] of a continuous [[variable]] $x$ which for [[integer]] values of $x=n$ agrees with the [[factorial]] function $n\mapsto n!$. The _gamma function_ is a shift by one of the solution to this problem.

For a complex variable $x\neq -1,-2,\ldots$, we define $\Gamma(x)$ by the formula 

$$
  \Gamma(x) = \lim_{k\to \infty} \frac{k! \cdot k^{x-1}}{(x)_k}
$$

where $(x)_0 =1$ and for positive integer $k = 1,2,\ldots$,

$$
(x)_k = x (x+1) (x+2)\cdots (x+ k-1)
$$

is the "Pochhammer symbol" (or rising factorial). It easily follows that $\Gamma(n+1) = n!$ for natural numbers $n = 0, 1, 2, \ldots$. 

## Properties 

As a function of a complex variable, the Gamma function $\Gamma(x)$ is a [[meromorphic function]] with simple poles at $x = 0, -1, -2, \ldots$. 

Extending the recursive definition of the ordinary factorial function, the Gamma function satisfies the following translation formula: 

\[
  \label{TranslationFormula}
  \Gamma(x+1) 
  \;=\; 
  x\,\Gamma(x)
\]

away from $x = 0, -1, -2, \ldots$. 

It also satisfies a reflection formula, due to Euler: 

$$\Gamma(x)\Gamma(1-x) = \frac{\pi}{\sin(\pi x)}.$$ 

\begin{prop}\label{GaussMultiplicationFormula}
**([[Gauss multiplication formula]])**

For

* any [[positive number|positive]] [[integer]] $N \in \mathbb{N}_+$,

* any $z \in \mathbb{R} \setminus  \{0, -1/N, -2/N, \cdots\} $,

the [[Gamma function]] $\Gamma(-)$ satisfies 

$$
  \underoverset
    {j = 0}
    {N-1}
    {\prod}
  \Gamma
  \left(
    z + \tfrac{j}{N}
  \right)
  \;=\;
  (2 \pi)^{ \tfrac{1}{2}(N-1) } 
  \cdot
  N^{ \tfrac{1}{2} - N z }
  \cdot
  \Gamma( N z )
  \,.
$$

\end{prop}

Quite remarkably, the Gamma function (this time as a function of a real variable) is uniquely characterized in the following theorem: 


\begin{theorem}
**(Bohr-Mollerup)** \linebreak

The restriction of the Gamma function to the interval $(0, \infty)$ is the unique function $f$ such that $f(x+1) = x f(x)$, $f(1) = 1$, and $\log f$ is convex. 
\end{theorem}

A number of other representations of the Gamma function are known and frequently utilized, e.g., 

* Product representation: 
$$\frac1{\Gamma(x)} = x e^{\gamma x} \prod_{n=1}^{\infty} (1 + \frac{x}{n})e^{-x/n}$$ 
where $\gamma$ is [[Euler's constant]]. 

* Integral representation: 
$$\Gamma(x) = \int_{0}^{\infty} t^x e^{-t} \frac{d t}{t}.$$ 



## Related concepts

* [[factorial]]

* [[Euler beta function]]

* [[Riemann zeta function]]

* [[Barnes G-function]]

## References 

* George Andrews, Richard Askey, Ranjan Roy, _Special Functions_. Encyclopedia of Mathematics and Its Applications 71, Cambridge University Press, 1999. 

See also: 

* Wikipedia, *[Gamma function](https://en.wikipedia.org/wiki/Gamma_function)*

[[!redirects gamma function]]
[[!redirects Gamma function]]

[[!redirects Gamma-function]]
[[!redirects Gamma-functions]]
