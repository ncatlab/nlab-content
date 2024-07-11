+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

*Convex mixtures* are to  [[convex combinations]] as [[integrals]] are to an [[sums]]. 

In other words, convex mixtures are given by [[integration|integrating]] a [[function]] with respect to a [[measure]] whose total normalization is one (hence, a [[probability measure]]).

The concept is used in [[analysis]] and [[geometry]] as a generalization of 
as well as in [[probability theory]] to take [[expectation values]] of [[random variables]].

In terms of [[category theory]], it is tightly related to the [[Giry monad]] and other [[probability monads]]. 
 

## Constructions

### For real numbers

Let $X$ be a [[measurable space]]. 
We can view a function $f \colon X\to\mathbb{R}$ as an [[indexed set|indexed collection]] of [[real numbers]]. 
If $X$ is [[finite set|finite]], one can take the \emph{average}, or \emph{midpoint}:
$$
\dfrac{f(x_1)+\dots+f(x_n)}{n}
$$
More generally, given a [[probability distribution]] $p$ on $X$, one can take the *weighted average*, or convex combination,
$$
\sum_{x\in X} f(x)\,p(x) .
$$
The resulting number is a convex combination of the numbers $f(x)$.

Convex mixtures generalize this to the infinite case: if the function $f$ is [[measurable function|measurable]], given a [[probability measure]] $p$ on $X$, one can take, if it exist, the [[integral]]
$$
\int_X f(x) \,p(dx) \,.
$$
One can view the resulting value as a mixture, analogous to a convex combination, of the points $f(x)$. (More precisely, of the points in the support of the [[pushforward measure]] $f_p$ on $\mathbb{R}$.)

In the language of [[probability theory]], we are taking the [[expectation value]] of the [[random variable]] $f$ on the [[probability space]] $(X,p)$.

The very similar construction can be given by replacing $\mathbb{R}$ with a generic Banach space, using [[Bochner integrals]]. 


### In terms of the Giry monad

The [[Giry monad]] is the most general [[monad of probability measures]] on the category of measurable spaces. 
[[algebra over a monad|Algebras]] of the Giry monad, therefore, can be interpreted exactly as spaces where one can form arbitrary convex mixtures. This is analogous to how [[convex spaces]], where one can form arbitrary convex combinations, are the algebras of the [[distribution monad]].

Similar notions can be given using other [[probability monads]]. Note that, in order to have a *convex* mixture, one needs a form of normalization.


## Examples

* In [[probability theory]], the expected value of an integrable [[random variable]] is a convex mixture.
* In [[physics]], convex mixtures give the [[center of mass]] of non-discrete bodies.
* The multiplication of the [[Giry monad]], and of most [[probability monads]], consists of taking a convex mixture of probability measure.
* The [[ergodic decomposition theorem]] says that every [[invariant measure]] is a convex mixture of [[ergodic measure|ergodic ones]].


## See also

* [[Lebesgue integral]], [[Bochner integral]], [[expectation value]]
* [[convex space]], [[convex combination]]
* [[probability monad]], [[Giry monad]], [[distribution monad]]
* [[ergodic decomposition theorem]], [[de Finetti theorem]]


category: probability, analysis, functional analysis


[[!redirects mixture]]