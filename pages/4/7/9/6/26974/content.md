+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

An *invariant measure* (a.k.a. *stationary* or *steady*) is a [[measure]] which is [[invariant]] under the [[action]] of a [[group]] or [[monoid]], often playing the role of [[time]], or a [[symmetry]] of the system.

An action with an invariant measure is sometimes called a *stationary* or *steady-state* system.

It is an important concept in [[probability theory]], [[dynamical systems]], [[statistical physics]], and [[representation theory]].
It is one of the weakest forms to mathematically formalize the idea of [[equilibrium]]. (Stronger forms of equilibrium are for example [[detailed balance]] and [[ergodicity]].)


## Definitions

Let $X$ be a [[measurable space]], and let $M$ be a [[monoid]] with an [[action]] on $X$ via [[measurable functions]]. 
For each $m\in M$, denote the action on $X$ again by $m:X\to X$. 

A [[measure]] $p$ on $X$ is called **invariant** or **stationary** under the action of $M$ if and only if for all $m\in M$, the pushforward $m_*p$ is equal to $p$. That is, for each [[measurable subset]] $A\subseteq X$,
$$
p(m^{-1}(A)) \;=\; p(A) .
$$

A space $X$ together with an action of $M$ and a stationary measure $M$ is sometimes called a **stationary system**.
In particular, a [[stochastic process]] whose underlying [[joint distribution]] is invariant is called a **stationary process**.

Note that, similarly to [[invariant sets]], if a measure is invariant, it does *not* in general mean that *each point in the support of the measure is an invariant point*.
The points may move, but their distribution overall is kept constant. 
For example, the [[Lebesgue measure]] on the [[unit circle]] (given by the [[length]]) is invariant under [[rotations]], but no point of the circle is invariant.

An interpretation in terms of [[equilibrium]] is that for each measurable set $A$, some mass may move away from $A$, but an equal amount of mass moves into $A$, so that the measure of $A$ overall stays the same. 


### Examples

* The [[Haar integral|Haar measure]] on a [[compact]] [[topological group]] $G$ is invariant for the action of $G$ on itself, given by left multiplication.

* An [[exchangeable measure]] on a [[product]] space $X^\mathbb{N}$ is invariant under the action of finite [[permutations]].

* A single measurable function $f:X\to X$ generates a monoid (the one of [[natural numbers]]). In this case, an invariant measure $p$ simply needs to satisfy $f_*p=p$.

* In [[statistical physics]], [[Liouville's theorem]] says that the distribution function of the [[phase space]] is invariant under the action of [[Hamiltonian flow]].


### Actions via Markov kernels

A monoid $(M,e,\cdot)$ can also act on a measurable space $X$ via [[Markov kernels]]. That is, to each $m\in M$ we can assign a kernel $k_m:X\to X$ such that 
$$
k_e(A|x) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A ,
\end{cases}
$$
and
$$
k_{m\cdot n}(A|x) \;=\; \int_X k_m(A|x')\,k_n(d x'|x) .
$$

In this case, a measure $p$ on $X$ is **invariant** or **stationary** if and only if for all $m\in M$, and for all measurable $A\subseteq X$,
$$
\int_X k_m(A|x) \, p(d x) \;=\; p(A) ,
$$
that is, each kernel $k_m$ [[Markov kernel#measurepreserving_kernels|preserves]] the measure $p$.

A [[probability space]] together with a measure-preserving kernel is sometimes called a **stationary [[Markov chain]]**.


## Category-theoretic description

A [[group]] or [[monoid]] $M$ can be seen (via [[delooping]]) as a one-object [[category]] $B M$, and an [[action]] of $M$ on a measurable space $X$ can be seen as a [[functor]] $B M\to Meas$ (the [[category of measurable spaces]]) or $B M\to Stoch$ (the [[category of Markov kernels]]). (Since [[Markov kernel#kernels_from_deterministic_functions|every measurable function canonically defines a Markov kernel]], without loss of generality we can take the category of kernels in both cases.)
As a [[diagram]], it has a single object, and a [[loop]] for each element of $M$:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=huge,%
]
X \ar[out=60,in=120,loop,"e",swap,distance=1.5cm] \ar[out=132,in=192,loop,"",swap,distance=1.5cm] \ar[out=204,in=264,loop,"",swap,distance=1.5cm] \ar[out=276,in=336,loop,"",swap,distance=1.5cm] \ar[out=348,in=408,loop,"",swap,distance=1.5cm]  
\end{tikzcd}

An invariant probability measure is now a [[cone]] over this diagram. Specifically, since a probability measure is equivalently a [[Markov kernel]] from the one-point space, it makes the following diagram of [[Stoch]] commute for every $m\in M$:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
column sep=large,%
]
& X \ar{dd}{k_m} \\
 1 \ar{ur}{p} \ar{dr}[swap]{p} \\
& X
\end{tikzcd}

In many situations, [[ergodic measures]] even form a [[limit]] cone.


Equivalently, a stationary measure $p$ gives an action of $M$ in the category of [[probability spaces]] and [[Markov kernel#measurepreserving_kernels|measure-preserving kernels]] (see for example at [[category of couplings]]).


## Further properties

* An invariant [[probability measure]] is called [[ergodic measure|ergodic]] if it is [[zero-one measure|zero-one]] on all [[invariant sigma-algebra|invariant sets]].

* A stationary system (for example, [[Markov kernel]]) satisfies [[detailed balance]], or is called [[reversible dynamics|reversible]] if 
$$
\int_A k(B|x) \,p(d x) \;=\; \int_B k(A|x)\,p(d x) ,
$$
i.e. if $k$ is its own [[Bayesian inverse]]. This is a stronger form of [[equilibrium]] than just stationarity.
(Not every stationary system satisfies this property.)

* The [[ergodic decomposition theorem]] says that, under some conditions, an invariant measure is a [[mixture]] of [[ergodic measure|ergodic ones]]. 


## See also

* [[group]], [[monoid]], [[action]]
* [[cone]], [[limit]], [[cocone]], [[colimit]]
* [[exchangeability]], [[invariant set]]
* [[ergodic measure]], [[ergodic decomposition theorem]]


## References

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#cornish} Rob Cornish, _Stochastic Neural Network Symmetrization in Markov Categories_, 2024. ([arXiv](https://arxiv.org/abs/2406.11814))


category: probability


[[!redirects invariant measures]]
[[!redirects invariant probability measure]]
[[!redirects invariant probability measures]]
[[!redirects invariant state]]
[[!redirects invariant states]]
[[!redirects measure-preserving Markov kernel]]
[[!redirects measure-preserving Markov kernels]]
[[!redirects measure preserving Markov kernel]]
[[!redirects measure preserving Markov kernels]]
[[!redirects measure-preserving kernel]]
[[!redirects measure-preserving kernels]]
[[!redirects measure preserving kernel]]
[[!redirects measure preserving kernels]]
[[!redirects stationary Markov process]]
[[!redirects stationary Markov processes]]
[[!redirects stationary Markov chain]]
[[!redirects stationary Markov chains]]
