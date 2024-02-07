
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
(Sometimes the term *transition kernel* denotes a more general, non-normalized mapping.)

It can be thought of as a generalization of a [[stochastic map]] outside the finite discrete case.
(Sometimes the term "stochastic map" is itself used to denote a Markov kernel.)

Markov kernels, in the form of regular conditional distributions (see [below](#regular_conditional_distributions)) are also the standard setting for talking about [[conditional probability]] outside of the discrete setting.

Markov kernels and their categories are among the basic building blocks of [[categorical probability]].


## Definition

Let $(X,\mathcal{A})$ and $(Y,\mathcal{B})$ be [[measurable spaces]], i.e. sets equipped each with a [[sigma-algebra]]. 
A **Markov kernel** $(X,\mathcal{A})\to(Y,\mathcal{B})$ is an assignment 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
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
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
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
\int_X k(B|x)\,p(d x) = q(B) .
$$

### Kernels from deterministic functions

The [[identity]] function on a measurable set $(X,\mathcal{A})$ defines a kernel as follows,
$$
\delta(A|x) = \delta_x(A) = 1_A(x) = \begin{cases}
1 & x\in A ; \\
0 & x\notin A
\end{cases}
$$
for every $x\in X$ and $A\in\mathcal{A}$. This gives the identity morphisms in the categories of kernels [[Markov kernel#categories_of_markov_kernels|below]].

More generally, let $f:(X,\mathcal{A})\to (Y,\mathcal{B})$ be a [[measurable function]]. We can define the kernel $\delta_f:(X,\mathcal{A})\to (Y,\mathcal{B})$ as follows,
$$
\delta_f(B|x) = \delta_f(x)(B) = 1_{f^{-1}(B)}(x) = \begin{cases}
1 & f(x)\in B ; \\
0 & f(x)\notin B
\end{cases}
$$
for every $x\in X$ and $B\in\mathcal{B}$. 
Intuitively, this kernel represents the deterministic transition, from $x$ to $f(x)$ with probability one.
This construction induces a [[functor]] from the category [[Meas]] to the categories of kernels [[Markov kernel#categories_of_markov_kernels|below]].
(Compare with the [[stochastic map#stochastic_maps_from_deterministic_functions|analogous construction for stochastic maps]].)

Note that if $f:(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$ is a [[measure-preserving function]], then $\delta_f$ is a measure-preserving kernel in the sense defined above.

### Bayesian inversion

Given a measure-preserving Markov kernel $k:(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$, a **[[Bayesian inverse]]** of $k$ is a Markov kernel $k^\dagger:(Y,\mathcal{B},q)\to(X,\mathcal{A},p)$ such that for all $A\in\mathcal{A}$ and $B\in\mathcal{B}$,
$$
\int_A k(B|x)\,p(d x) = \int_B k^\dagger(A|y)\,q(d y) .
$$
The last formula can be seen as an instance of [[Bayes' formula]], as it generalize the usual discrete formula
$$
P(b|a)\,P(a) = P(a|b)\,P(b) .
$$
We have that 

* Every kernel between [[standard Borel]] spaces admits a Bayesian inverse;

* If a kernel $k:(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$ admits a Bayesian inverse $k^\dagger:(Y,\mathcal{B},q)\to(X,\mathcal{A},p)$, then any kernel $h:(Y,\mathcal{B},q)\to(X,\mathcal{A},p)$ is a Bayesian inverse of $k$ if and only if it is $q$-almost surely equal to $k^\dagger$. 

* Bayesian inverses, when they exist, depend crucially on the measure $p$.

* Bayesian inversion makes the category [[Krn]] (see [[Markov kernel#categories_of_markov_kernels|below]]) a [[dagger category]].


## Regular conditional distributions

A Markov kernel can be seen as a [[probability measure]] which depends [[measurable function|measurably]] on a parameter. 
Therefore, together with the idea of [[conditional expectation]], they a very useful tool to talk about [[conditional probability]] without incurring into paradoxes. Let's see how.

Let $(X,\mathcal{A},p)$ be a [[probability space]], and consider a sub-[[sigma-algebra]] $\mathcal{B}\subseteq\mathcal{A}$. 
Recall that 

* the [[conditional expectation]] of an integrable function $f:(X,\mathcal{A},p)\to\mathbb{R}$ given $\mathcal{B}$ is a function $\mathbb{E}[f|\mathcal{B}]:X\to\mathbb{R}$ which is $\mathcal{B}$-measurable ("coarser" than $f$), and such that for every $B\in\mathcal{B}$,
$$
\int_B f \, d p = \int_B \mathbb{E}[f|\mathcal{B}] \, d p .
$$
(Such a function always exists by the [[Radon-Nikodym theorem]].)

* the [[conditional probability]] of an event (measurable subset) $A\in\mathcal{A}$ is the conditional expectation of its indicator function:
$$
\mathbb{P}[A|\mathcal{B}] = \mathbb{E}[1_A|\mathcal{B}] .
$$

Note that $\mathbb{P}[A|\mathcal{B}]$ is a function, 
$$
x\mapsto \mathbb{P}[A|\mathcal{B}](x) 
$$
which is $\mathcal{B}$-measurable for every $A\in\mathcal{A}$. Therefore, in order for the assignment 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X \times \mathcal{A} \ar{r} & {[0,1]} \\
(x,A) \ar[mapsto]{r} & \mathbb{P}{[A|\mathcal{B}]}(x)
\end{tikzcd} 
to be a Markov kernel $(X,\mathcal{B})\to(X,\mathcal{A})$ (see the definition [above](#definition)), we moreover need that for every $x\in X$ the assignment 
$$
A \mapsto \mathbb{P}[A|\mathcal{B}](x) 
$$
be a probability measure on $(X,\mathcal{A})$. 
This is not always the case. When this happens, we call the resulting kernel $(X,\mathcal{B})\to(X,\mathcal{A})$ a **regular conditional distribution** given $\mathcal{B}$.
We can view a regular conditional distribution as a probability measure on $(X,\mathcal{A})$ which is parametrized in a measurable way by $(X,\mathcal{B})$. 

The **disintegration theorem** says that when $(X,\mathcal{A})$ is standard Borel, regular conditional distributions in the form above always exist. 

### Regular conditionals from a joint distribution

Using the disintegration theorem we can obtain conditional probability distributions in a way that generalizes the discrete formula
$$
p(b|a) = \frac{p(a,b)}{p(a)}
$$
to the non-discrete setting.

Given standard Borel spaces $(X,\mathcal{A})$ and $(Y,\mathcal{B})$, their product $(X\times Y,\mathcal{A}\otimes\mathcal{B})$ is again standard Borel. The projection map $\pi_1:(X\times Y,\mathcal{A}\otimes\mathcal{B})\to (X,\mathcal{A})$ induces a sub-sigma-algebra $\pi_1^{-1}(\mathcal{A})$ on $X\times Y$ (which makes it isomorphic to $(X,\mathcal{A})$ in both [[Stoch]] and [[Krn]], see [Section 2.1 of this paper](#ergodic_dagger)).

Given a joint distribution $r$ on $(X\times Y,\mathcal{A}\otimes\mathcal{B})$, we can then form the regular conditional $(X\times Y,\pi_1^{-1}(\mathcal{A}))\to(X\times Y,\mathcal{A}\otimes\mathcal{B})$ (or equivalently, up to isomorphism, $(X,\mathcal{A})\to(X\times Y,\mathcal{A}\otimes\mathcal{B})$).
Further composing with the projection $\pi_2:(X\times Y,\mathcal{A}\otimes\mathcal{B})\to(Y,\mathcal{B})$ (or equivalently restricting the kernel to the sub-sigma-algebra $\pi_2^{-1}(\mathcal{B})$) we then get a kernel
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X\times\mathcal{B} \ar{r} & {[0,1]} \\
(x,B) \ar[mapsto]{r} & \mathbb{P}{[\pi_2^{-1}(B)|\pi_1^{-1}(\mathcal{A})]}(x) ,
\end{tikzcd}
sometimes denoted simply $r(B|x)$ or $r'(B|x)$.

This kernel satisfies the property that for every $A\in\mathcal{A}$ and $B\in\mathcal{B}$,
$$
\int_A r'(B|x) \, p(d x) = r(A\times B) ,
$$
and is therefore a generalization of conditional probability to the non-discrete setting: compare it to the formula 
$$
P(b|a)\,P(a) = P(a,b) .
$$


## Categories of Markov kernels

* [[Stoch]] is the category of [[measurable spaces]] and Markov kernels between them.

* One can also form the category of [[probability spaces]] and equivalence classes of Markov kernels between them (under [[Markov kernel#almost_sure_equality|almost sure equality]]). 

* One can restrict the category above to [[standard Borel]] probability spaces, obtaining a [[dagger category]] sometimes denoted by [[Krn]], which is equivalent to the [[category of couplings]].




## Related concepts

* [[Markov category]]

* [[Stoch]]

* [[category of couplings]]

* [[stochastic map]]

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

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions, and transitions to equilibrium_.  [arXiv](https://arxiv.org/abs/2310.04267).


category: probability

[[!redirects Markov kernels]]
[[!redirects stochastic kernel]]
[[!redirects stochastic kernels]]
[[!redirects transition kernel]]
[[!redirects transition kernels]]
[[!redirects probability kernel]]
[[!redirects probability kernels]]