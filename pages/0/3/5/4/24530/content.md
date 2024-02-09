+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context

#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

Recall that for a [[monoidal monad]] (or equivalently [[commutative monad]]) on a [[monoidal category]], both the [[Kleisli category]] and the [[Eilenberg-Moore category]] inherit a [[monoidal category|monoidal structure]]. 

An *affine* monoidal monad, on a [[cartesian monoidal category]], preserves the monoidal unit (the [[terminal object]]), and so it makes the [[Kleisli category|Kleisli]] and [[Eilenberg-Moore category|Eilenberg-Moore categories]] [[semicartesian monoidal category|semicartesian]].


## Definition

Let $(C,\times,1)$ be a [[cartesian monoidal category]].
A [[commutative monad]] $(T,\mu,\eta)$ with [[monoidal monad|monoidal structure map]] $\nabla$ is called **affine** if any of the following equivalent conditions hold:

1. The unit map $\eta_1:1\to T1$ is an [[isomorphism]];
2. The following diagram commutes for all objects $A$ and $B$,
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
TA \times TB \ar{dr}[swap]{\mathrm{id}} \ar{r}{\nabla} & T(A\times B) \ar{d}{(T\pi_1,T\pi_2)} \\
& TA\times TB
\end{tikzcd}
where $\pi_1:A\times B\to A$ and $\pi_2:A\times B\to B$ are the [[product|product projection maps]].


(Note: This should be generalizable to monads on [[cartesian multicategories]].)



## Strongly and weakly affine monads

A strong monad on a cartesian monoidal category is called **strongly affine** ([Jacobs'16](#strongly_affine)) if and only if for all objects $A$ and $B$, the following diagram is a [[pullback]],
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
A\times TB \ar{r}{\sigma} \ar{d}{\pi_1} & T(A\times B) \ar{d}{T\pi_1} \\
A \ar{r}{\eta} & TA
\end{tikzcd}
where $\sigma$ denotes the [[strong monad|strength]] of the monad, and $\pi_1$ the product projection.


A commutative monad on a cartesian monoidal category is called **weakly affine** ([FGPT'23](#weaklymarkov)) if and only if any of the following equivalent conditions hold:

1. The [[internal monoid]] $T1$ (with its canonical monoid structure) is a [[group]];
2. For all objects $A$, $B$ and $C$, the [[monoidal functor|associativity diagram]] is a [[pullback]].
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
TA\times TB\times TC \ar{r}{\mathrm{id}\times\nabla} \ar{d}{\nabla\times\mathrm{id}} & TA\times T(B\times C) \ar{d}{\nabla} \\
T(A\times B)\times TC \ar{r}{\nabla} & T(A\times B\times C)
\end{tikzcd}

Every (commutative) strongly affine monad is affine, and every affine monad is weakly affine.


## Properties

* The [[Eilenberg-Moore category]] of an affine commutative monad is a [[semicartesian monoidal category]]. In particular, it is a model of [[affine logic]]. 

* The [[Kleisli category]] of an affine commutative monad is a [[Markov category]] ([Fritz'20](#fritzmarkov)). This makes affine commutative monads suitable as [[probability monads]], modelling [[joint and marginal distributions]].

Similarly:

* The [[Kleisli category]] of a strongly affine commutative monad is a [[Markov category#positivity_and_causality|positive Markov category]] ([FGGPS'23](#dilations)).

* The [[Kleisli category]] of a weakly affine commutative monad is a *weakly Markov category*, see [FGPT'23](#weaklymarkov).


## See also 

* [[monoidal monad]], [[strong monad]], [[commutative monad]]
* [[Markov category]]
* [[joint and marginal distributions]]


## References

* [[Anders Kock]], _Bilinearity and cartesian closed monads_, Mathematica Scandinavica 29(2), 1971. 

* [[Bart Jacobs]], _Semantics of weakening and contraction_, Annals of Pure and Applied Logic 69(1), 1994. ([full text](https://www.sciencedirect.com/science/article/pii/0168007294900205))

* {#strongly_affine} [[Bart Jacobs]], _Affine Monads and Side-Effect-Freeness_, Proceedings of CMCS, 2016. ([pdf](http://www.cs.ru.nl/B.Jacobs/PAPERS/side-effects.pdf))

* {#bimonoidal_monads} [[Tobias Fritz]], [[Paolo Perrone]], _Bimonoidal Structure of Probability Monads_, Proceedings of MFPS, 2018, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#dilations} [[Tobias Fritz]], Tomáš Gonda, Nicholas Gauguin Houghton-Larsen, [[Paolo Perrone]] and Dario Stein, _Dilations and information flow axioms in categorical probability_. Mathematical Structures in Computer Science, 2023. ([arXiv:2211.02507](https://arxiv.org/abs/2211.02507)).

* {#weaklymarkov} [[Tobias Fritz]], [[Fabio Gadducci]], [[Paolo Perrone]] and Davide Trotta, _Weakly Markov categories and weakly affine monads_, Proceedings of CALCO, LIPIcs 10, 2023. ([arXiv](https://arxiv.org/abs/2303.14049))


[[!redirects affine monads]]
[[!redirects strongly affine monad]]
[[!redirects strongly affine monads]]
[[!redirects weakly affine monad]]
[[!redirects weakly affine monads]]
