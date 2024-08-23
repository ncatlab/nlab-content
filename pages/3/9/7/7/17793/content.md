+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The term "mean" or "average" usually refers to a value (for example a [[number]]) that lies *between* some given values. 
For example, the number $3$ is the average of $2$ and $4$.

The idea admits several generalizations in different fields such as [[geometry]], [[analysis]], and [[probability theory]].

As algebraic operations, several notions of "mean" give rise to [[probability monads]].


## Definitions

Given two [[numbers]] or [[vectors]] $x,y$, their **arithmetic mean** or **average** is the number or vector
$$
\frac{x+y}{2} .
$$
More generally, given $x_1,\dots,x_n$, their arithmetic mean or average is given by 
$$
\frac{x_1+\dots+x_n}{n} .
$$

### Weighted averages

Given numbers or vectors $x_1,\dots,x_n$ and nonnegative real numbers $p_1,\dots,p_n$ such that $p_1+\dots+p_n=1$ (equivalently, a [[distribution monad|discrete probability distribution]]), the **weighted average** of the $x_i$ with weights $p_i$ is given by
$$
\sum_i p_i\cdot x_i \;=\; p_1\cdot x_1 + \dots + p_n\cdot x_n .
$$
In other words, a weighted average is the same as a [[convex combination]], or as the [[expectation value]] of a [[discrete random variable]].

### Continuous generalization

One can replace the [[sum]] with an [[integral]] and obtain a continuous analogue of weighted averages as follows. First of all, fix a [[Banach space]] $V$ (for example the real line).

* Instead of values $x_1,\dots,x_n\in V$ one can take a [[measurable space]] $X$ and a [[measurable function]] $f:X\to V$, which one can interpret as a selection of possibly infinitely many values $f(x)$ of $V$;
* Instead of weights $p_1,\dots,p_n$ one can take a [[probability measure]] on $X$;
* Instead of a sum one can now form the [[convex mixture]]
$$
\int f(x)\, p(d x) 
$$
given by [[integration]] (for example, [[Bochner integration]]).

In the language of [[probability theory]], this is the [[expectation value]] of the [[random variable]] $f$ on the [[probability space]] $(X,p)$. 


### Nonlinear generalizations

Given numbers $x$ and $y$,

* Their **geometric mean** is given by
$$
\sqrt{xy} .
$$ 
In other words, one is taking the arithmetic mean of their logarithms.

* Their **quadratic mean** is given by 
$$
\sqrt{\frac{x^2+y^2}{2}}
$$
In other words, one is taking the mean of the squares. This is used, for example, to compute the [[variance]] in [[probability theory]].

* Their **harmonic mean** is given by 
$$
\frac{1}{\;\frac{1/x+1/y}{2}\;}
$$
In other words, one is taking the mean of the inverses. 

One has the inequality
$$
harmonic \le geometric \le arithmetic \le quadratic ,
$$
and equality holds if and only if $x=y$.

The same can be extended to any tuple of numbers.

Similarly, in the continuous case, given a [[probability space]] $(X,\mu)$ and a [[random variable]] $f:X\to\mathbb{R}$, one can take the mean 
$$
\left( \int |f|^p d\mu \right)^{1/p}
$$
for any $p$, which is equivalently the [[L^p space|L^p norm]] of $f$.


## Related concepts

* [[probability monad]]
* [[expectation value]]
* [[convex combination]]
* [[convex mixture]]
* [[L^p space]]
* [[mean value theorem]]


## References

* Wikipedia, _[Mean](https://en.wikipedia.org/wiki/Mean)_

[[!redirects means]]
[[!redirects average]]
[[!redirects averages]]
[[!redirects weighted average]]
[[!redirects weighted averages]]