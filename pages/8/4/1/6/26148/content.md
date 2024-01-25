
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

In [[probability theory]], a *stochastic map* between sets $X$ and $Y$ is a way of assigning numbers to elements $(x,y)$ of $X\times Y$ to model a probabilistic transition from $X$ to $Y$. The entries of a stochastic map form a matrix often called a *stochastic matrix* or *transition matrix*, which has nonnegative entries whose columns (or rows, depending on the convention) sum to one.

A generalization to arbitrary measurable spaces is called a [[stochastic kernel]] (or *Markov kernel*).
(Sometimes the term *stochastic map* is used to denote a stochastic kernel.)

If a stochastic map also preserves the uniform distribution, then it is called a *doubly stochastic map*.
This means that the stochastic matrix has not just columns but also rows which sum to unity, then called a *doubly stochastic matrix*.

## Definitions

Let $X$ and $Y$ be sets. A **stochastic map** or **stochastic matrix** from $X$ to $Y$ is a function $f:X\times Y\to[0,1]$, whose entries we denote by $f(y|x)$, such that 

* For all $x\in X$ and $y\in Y$, the number $f(y|x)$ is non-negative;
* For all $x\in X$, the numbers $f(y|x)$ are nonzero for only finitely many $y\in Y$;
* For all $x\in X$, $\sum_Y f(y|x) = 1$.

The quantity $f(y|x)$ can be thought of as a transition [[probability]] or [[conditional probability]] of moving to $y$ if the current state or current knowledge is $x$.

### Composition

The product of stochastic matrices is again a stochastic matrix (and so they form a category, see below).
Given stochastic matrices $f$ from $X$ to $Y$ and $g$ from $Y$ to $Z$, the entries of the product are 
$$
(g\circ f) (z|x) = \sum_X g(z|y)\,f(y|x) .
$$
Its probabilistic interpretation is that the random transition from $x$ to $y$ and from $y$ to $z$ are independent, as in a Markov process (hence their product is taken), and all intermediate states $y$ are mutually exclusive, so that the probabilities are summed over all $y$. This formula is sometimes called the *Chapman-Kolmogorov formula*. (See also the generalization to [[Markov kernels]].)

As identity matrices are stochastic, stochastic matrices form a [[category]], see below.

### Measure-preserving stochastic maps

Let $(X,p)$ and $(Y,q)$ be discrete [[probability spaces]], i.e. sets equipped with a functions $p:X\to[0,1]$ and $q:Y\to[0,1]$ which sum to one.
A stochastic map $f$ from $X$ to $Y$ is called **measure-preserving** if for every $y\in Y$, 
$$
\sum_{x\in f^{-1}(y)} p(x) = q(y) .
$$
(Compare this with the [[Markov kernel#measurepreserving_kernels|analogous notion for stochastic kernels]].)


### Stochastic maps from deterministic functions

The [[identity]] function on a set $X$ defines a stochastic map as follows,
$$
\delta(x'|x) = \delta_{x,x'} \begin{cases}
1 & x'=x ; \\
0 & x'\neq x
\end{cases}
$$
for every $x,x'\in X$. This gives the identity morphisms in the categories of stochastic maps [[stochastic map#categories_of_stochastic_maps|below]].

More generally, let $f:X\to Y$ be a function. We can define the stochastic map $\delta_f:X\to Y$ as follows,
$$
\delta_f(y|x) = \delta_{f(x),y} = \begin{cases}
1 & f(x) = y ; \\
0 & f(x) \ne y
\end{cases}
$$
for every $x\in X$ and $y\in Y$. 
Intuitively, this kernel represents the deterministic transition, from $x$ to $f(x)$ with probability one.
This construction induces a [[functor]] from the category [[Set]] to the categories of stochstic maps [[stochastic map#categories_of_stochastic_maps|below]].
(Compare with the [[Markov kernel#kernels_from_deterministic_functions|analogous construction for stochastic kernels]].)



## As Kleisli morphisms

A stochastic map can be equivalently written as a function 
\begin{tikzcd}
X \ar{r}{f^\sharp} & DY
\end{tikzcd}
where $D$ denotes the [[distribution monad]]. 
Therefore, stochastic maps can be seen as the [[Kleisli morphisms]] of the distribution monad on [[Set]]. 

(Compare with the [[Markov kernel#as_kleisli_morphisms|analogous statement for stochastic kernels]].)


## Categories of stochastic maps 

* The category of [[finite sets]] and stochastic matrices between them is often called [[Stoch#finstoch|FinStoch]], and is an example of a [[Markov category]].

* The category of finite [[probability spaces]] and measure-preserving stochastic matrices between them form a category as well.


## Related entries

* [[Markov kernel]]
* [[Markov category]]
* [[Stoch#finstoch|FinStoch]]
* [[Stoch]]
* [[quantum channel]]

## References

See also: 

* Wikipedia, *[Stochastic matrix](https://en.wikipedia.org/wiki/Stochastic_matrix)*

* James Fullwood, [[Arthur Parzygnat]], Section 4 of: *The information loss of a stochastic map*, Entropy **2021** 23(8) 1021 &lbrack;[arXiv:2107.01975](https://arxiv.org/abs/2107.01975), [doi:10.3390/e23081021](https://doi.org/10.3390/e23081021)&rbrack;

[[!redirects stochastic maps]]

[[!redirects stochastic matrix]]
[[!redirects stochastic matrices]]

[[!redirects doubly stochastic map]]
[[!redirects doubly stochastic maps]]

[[!redirects doubly stochastic matrix]]
[[!redirects doubly stochastic matrices]]



