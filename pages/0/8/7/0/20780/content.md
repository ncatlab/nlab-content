
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The distribution monad is a [[monad]] on [[Set]], whose [[algebra over a monad|algebras]] are [[convex spaces]]. 

It can be thought of as the [[finitary monad|finitary]] prototype of a [[probability monad]]. 

## Definition

### Finite distributions

Let $X$ be a set. Define $D X$ as the set whose elements are functions $p:X\to[0,1]$ such that 

* $p(x)\ne 0$ for only finitely many $x$, and

* $\sum_{x\in X} p(x)=1$. 

Note that the sum above is finite if one excludes all the zero addenda.

The elements of $D X$ are called **finite distributions** or **finitely-[[support|supported]] probability measures** over $X$. 

### Pushforward

Given a function $f:X\to Y$, one defines the **pushforward** $D f:D X\to D Y$ as follows. Given $p\in D X$, then $(D f)(p)\in D Y$ is the function
$$
y \;\mapsto\; \sum_{x\in f^{-1}(y)} p(x) .
$$
(Note that, up to zero addenda, the sum above is again finite.)

Compare with the [[pushforward of measures]]. 

This makes $D$ into an [[endofunctor]] on [[Set]]. 

### Monad structure

The unit map $\delta:X\to D X$ maps the element $x\in X$ to the function $\delta_x:X\to[0,1]$ given by
$$
\delta_x(y) \;=\; \begin{cases}
1 & y=x ;\\
0 & y\ne x .
\end{cases}
$$
Compare with the [[Dirac measures]] and [[continuous valuation#dirac_valuation|valuations]]. 

The multiplication map $E:D D X\to D X$ maps $\xi\in D D X$ to the function $E\xi\in D X$ given by
$$
E\xi(x) \;=\; \sum_{p\in D X} p(x) \, \xi(p).
$$
(Note that, up to zero addenda, the sum above is once again finite.)

The maps $E$ and $\delta$ satisfy the usual [[monad]] laws. The resulting monad $(D,E,\delta)$ is known as **distribution monad**, or **finitary Giry monad** (in analogy with the [[Giry monad]]), or **convex combination monad**, since the elements of $D X$ can be interpreted as formal [[convex space|convex combinations]] of elements of $X$.

This can be seen as a discrete, finitary analogue of a [[probability monad]], where one replaces [[integrals]] by [[sums]]. 


## Properties

* The [[algebra over a monad|algebras]] of $D$ are [[convex spaces]].

* The monad $D$ is [[finitary monad|finitary]], and [[commutative monad|commutative]]. 

* The [[Kleisli morphisms]] of $D$ are (finitary) [[stochastic maps]].

(...)

## See also

* [[convex space]], [[conical space]]

* [[monads of probability, measures, and valuations]]

* [[Giry monad]], [[probabilistic powerdomain]], [[extended probabilistic powerdomain]]

* [[monad]], [[monad (in computer science)]]


## References

* [[Tobias Fritz]] and [[Paolo Perrone]], _Monads, partial evaluations, and rewriting_, MFPS 34, 2020 - Section 6. ([arXiv](https://arxiv.org/abs/1810.06037))

* {#jacobs} [[Bart Jacobs]], _From probability monads to commutative effectuses_, Journal of Logical and Algebraic Methods in Programming 94, 2018. 
([doi:10.1016/j.jlamp.2016.11.006](https://doi.org/10.1016/j.jlamp.2016.11.006))

* {#fritzconvex} [[Tobias Fritz]], _Convex spaces I: definitions and examples_, 2009. ([arXiv:0903.5522](https://arxiv.org/abs/0903.5522))