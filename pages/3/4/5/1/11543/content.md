

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


\tableofcontents



## Statement 

For $k$ a [[natural number]] and $r$ a [[complex number]], define the [[falling factorial]] by 

$$r^{\underline{k}} = r(r-1)\ldots (r-k+1),$$ 

a polynomial of degree $k$ evaluated at $r$. If $r$ is a natural number, this expression vanishes for $k \gt r$. 

The binomial theorem may be stated thus: if $r$ is any complex number and ${|x|} \lt 1$, then 

$$(1 + x)^r = \sum_{k \geq 0} \frac{r^{\underline{k}} x^k}{k!}$$ 

where the left side may be formally defined as $\exp(r \cdot \log (1+x))$, taking the principal branch of the [[logarithm]] as defined by the power series 

$$\log(1 + x) = x - \frac{x^2}{2} + \frac{x^3}{3} - \ldots $$ 

with radius of convergence equal to $1$. (A formal verification of the binomial theorem may be found at [[coinduction]].) 

Thus, if we define the **[[binomial coefficient]]** $\binom{r}{k}$ by the formula 

$$\binom{r}{k} \coloneqq \frac{r^{\underline{k}}}{k!},$$ 

then we have 

$$
  (y + x)^r 
   \;=\; 
  \sum_{k \geq 0} 
   \binom{r}{k} \cdot y^{r-k} \cdot x^k
$$ 

whenever ${|\frac{x}{y}|} \lt 1$, i.e., whenever ${|y|} \gt {|x|}$. More precisely: for any fixed $y \neq 0$, this equation holds for any branch of the logarithm that we use to define $(y+x)^r$ as $\exp(r\log(y+x))$ over the domain $\{x: {|x|} \lt {|y|}\}$. 

## Combinatorial interpretation 

The special finitary case in which $i, j, n$ are positive integers, 

$$(i + j)^n = \sum_{0 \leq k \leq n} \binom{n}{k} i^k j^{n-k}$$ 

may be established combinatorially (or in "bijective fashion") as follows. Start by interpreting $(i + j)^n$ as the number of functions $f: N \to I \sqcup J$ from an $n$-element set, where $I, J$ have cardinalities $i, j$ respectively. By pulling back $f$ along each of the inclusions of $I, J$ into $I \sqcup J$, we get functions $f_I: f^{-1}(I) \to I$, $f_J: f^{-1}(J) \to J$. Here $f^{-1}(I)$ and $f^{-1}(J)$ are complementary subsets of $N$, say of cardinalities $k$ and $n-k$ respectively. (In effect, we are using the fact that the category of finite sets is an [[extensive category]].) Thus, $f$ determines and is uniquely determined by the following data 

* A subset $K (= f^{-1}(I))$ of $N$, 
* A function $g (= f_I)$ of the form $K \to I$, 
* A function $h (= f_J)$ of the form $N-K \to J$ 

and by counting the number of such triplets $(K, g, h)$, we are led to the right-hand side of the previous displayed equation. 

Notice this gives a rigorous proof for the polynomial identity 

$$(x+y)^n = \sum_{0 \leq k \leq n} \binom{n}{k} x^k y^{n-k}$$ 

since a polynomial in $\mathbb{Z}[x, y]$ is the zero polynomial if it vanishes for all positive integer values substituted for $x$ and $y$. 

## Pascal's triangle

The binomial coefficient polynomials $\binom{x}{k}$ (here $x$ is an indeterminate) satisfy the recurrence 

$$\Delta \binom{x}{k} \coloneqq \binom{x+1}{k} - \binom{x}{k} = \binom{x}{k-1}, \qquad \binom{x}{0} \coloneqq 1, \binom{0}{k} = 0\; (k \neq 0)$$ 

where the first two equations may also be written as 

$$\Delta \frac{x^\underline{k}}{k!} = \frac{x^\underline{k-1}}{(k-1)!}, \qquad \frac{x^\underline{0}}{0!} = 1.$$ 

The first equation may be viewed as the discrete analogue of the continuous [[derivative]] formula 

$$\frac{d}{d x} \frac{x^k}{k!} = \frac{x^{k-1}}{(k-1)!}.$$ 

The more familiar form of this recurrence, 

$$\binom{x+1}{k} = \binom{x}{k} + \binom{x}{k-1},$$ 

may be interpreted combinatorially: a $k$-element subset $K$ of $X + 1$ is either entirely contained in $X$, or is determined by the $(k-1)$-element subset of $X$ that is $K \cap X$. 

## Related concepts

* [[binomial coefficient]]

* [[multinomial coefficient]]

* [[factorial]], [[double factorial]]

* [[Catalan number]]

* [[binomial type]]

## References

See also 

* Wikipedia, _[Binomial theorem](https://en.wikipedia.org/wiki/Binomial_theorem)_


