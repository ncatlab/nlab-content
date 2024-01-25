
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

A **Markov kernel** (also called **transition kernel**, **stochastic kernel**, or **probability kernel**) is a mathematical formalization of a "function with random outcomes", or "random transition".

It can be thought of as a generalization of a [[stochastic map]] outside the finite discrete case.
(Sometimes the term "stochastic map" is itself used to denote a Markov kernel.)

Markov kernels and their categories are among the basic building blocks of [[categorical probability]].


## Definition

Let $(X,\mathcal{A})$ and $(Y,\mathcal{B})$ be [[measurable spaces]], i.e. sets equipped each with a [[sigma-algebra]]. 
A _Markov kernel_ $(X,\mathcal{A})\to(Y,\mathcal{B})$ is an assignment 
\begin{tikzcd}[row sep=0]
X \times \mathcal{B} \ar{r}{k} & {[0,1]} \\
(x,B) \ar[mapsto]{r} & k(B|x)
\end{tikzcd}
which is 

* [[measurable function|measurable]] as a function of $x$, for all $B\in\mathcal{B}$;
* a [[probability measure]] as a function of $B$, for all $x\in X$.

The quantity $k(B|x)$ can be thought of as the probability of transitioning to $B$ if we are in $x$, or of the [[conditional probability]] of the event $B$ given $x$.
 

## Basic structures and properties

### As Kleisli morphisms

A Markov kernel $k:(X,\mathcal{A})\to(Y,\mathcal{B})$ can be equivalently expressed as a measurable map 
\begin{tikzcd}
X \ar{r}{k^\sharp} & PY
\end{tikzcd}
where $P$ denotes the [[Giry monad]] on [[Meas]], with the Giry sigma-algebra. 
In other words, a Markov kernel is exactly a [[Kleisli morphism]] for the Giry monad. 
Particular Markov kernels are also Kleisli morphisms for other [[probability monads]].

### Almost sure equality

Consider two $k,h:(X,\mathcal{A})\to(Y,\mathcal{B})$ and a measure $p$ on $(X,\mathcal{A})$. 
The kernels $k$ and $h$ are said to be **$p$-almost surely equal** or **$p$-almost everywhere equal** if for every $B\in\mathcal{B}$, the quantities $k(B|x)$ and $h(B|x)$ only differ on a set of measure zero. 
Note that in general this set depends on the choice of $B$, but in some cases, such as when $(Y,\mathcal{B})$ is [[standard Borel]], it can be taken independently of $B$.

### Measure-preserving kernels 

Let $(X,\mathcal{A},p)$ and $(Y,\mathcal{B},q)$ be [[probability spaces]], i.e. [[measurable spaces]] equipped each with a [[probability measure]].
A **measure-preserving kernel** $(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$ is a kernel between the underlying measurable spaces $k:(X,\mathcal{A})\to(Y,\mathcal{B})$
such that for every $B\in\mathcal{B}$, 
$$
\int_X k(B|x)\,p(dx) = q(B) .
$$

### Disintegration theorem

[...]

## Categories of Markov kernels

* [[Stoch]] is the category of [[measurable spaces]] and Markov kernels between them.

[...]




## Related concepts

* [[Markov category]]

* [[Stoch]]

* [[category of couplings]]

* [[kernel method]]

* [[Mallows kernel]] 

* [[Kendall kernel]]

* [[Cayley distance kernel]]

## References

See also:

* Wikipedia, *[Markov kernel](https://en.m.wikipedia.org/wiki/Markov_kernel)*

Discussion via [[category theory]]:

* [[F. W. Lawvere]], _The Category of Probabilistic Mappings_, 1962, [PDF](https://ncatlab.org/nlab/files/lawvereprobability1962.pdf).

* Fredrik Dahlqvist, Vincent Danos, Ilias Garnier, and Alexandra Silva, _Borel kernels and
their approximation, categorically_. In MFPS 34: Proceedings of the Thirty-Fourth Conference on the Mathematical Foundations of Programming Semantics, volume 341, 91–119, 2018.  [arXiv](https://arxiv.org/abs/1803.02651).

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* Noé Ensarguet, [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions, and transitions to equilibrium_.  [arXiv](https://arxiv.org/abs/2310.04267).

[[!redirects Markov kernels]]
[[!redirects stochastic kernel]]
[[!redirects stochastic kernels]]
[[!redirects transition kernel]]
[[!redirects transition kernels]]
[[!redirects probability kernel]]
[[!redirects probability kernels]]