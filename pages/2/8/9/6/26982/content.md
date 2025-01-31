+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
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

*Zero-one measures* are [[measures]] whose only values are [[zero]] and [[one]]. 

In [[probability theory]], they model situations which "are not really random", where we are almost surely certain of which events take place and which do not. 
They are used to express [[zero-one laws]] and more generally to model situations of [[ergodicity]].

Zero-one measures form a [[monad]], which is analogous to [[sober topological space#Reflection|sobrification of topological spaces]].

The analogous concept for [[Markov kernels]] is a [[zero-one kernel]].


## Definition

A [[probability measure]] $p$ on a [[measurable space]] $X$ is said to be **zero-one**, **irreducible** or **extremal** if and only if any of the following equivalent conditions hold:

* For every event (measurable subset) $A$ of $X$, 
$$
p(A) \;=\; 0 \qquad or \qquad p(A) \;=\; 1 .
$$
* Every real-valued [[random variable]] $f$ on the [[probability space]] $(X,p)$ is [[almost surely]] constant (i.e. it is a [[determinstic random variable]]).
* Every event (measurable subset) $A$ of $X$ is [[conditional independence|independent]] of itself:
$$
p(A) \;=\; p(A\cap A) \;=\; p(A)\,p(A) .
$$
* Every two events $A,B$ of $X$ are [[conditional independence|independent]]:
$$
 p(A\cap B) \;=\; p(A)\,p(B) .
$$
* $p$ cannot be expressed as a nontrivial [[convex combination]] of other probability measures: if
$$
p \;=\; \lambda\,q_1 + (1-\lambda)\,q_2
$$
for $\lambda\in(0,1)$ and $q_1,q_2\in P X$, then $q_1=q_2=q$.
(This can be seen as analogous to [[irreducible closed sets]].)
* $p$ cannot be expressed as a nontrivial [[convex mixture]]: if $p=\mu(\pi)$ for some $\pi\in P P X$ (where $P$ is the [[Giry monad]] and $\mu$ is its multiplication), then necessarily $\pi=\delta_p$.
* For every $f,g:X\to\mathbb{R}$ for which the integrals below exist, integration with $p$ preserves multiplication:
$$
\int_X (f\cdot g)\,dp \;=\; \left( \int_X f\,dp \right) \cdot \left( \int_X g\,dp \right) .
$$
* The parallel pair of maps
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX ,
\end{tikzcd}
agree on $p$. ($P$ denotes the [[Giry monad]], and $\delta$ is its [[unit]], given by [[Dirac measures]].) 


## Examples

* Every [[Dirac measure|Dirac delta]] measure is zero-one: 
$$
\delta_x(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A .
\end{cases}
$$
If $X$ is [[standard Borel]], or more more generally [[sober measurable space|if it has enough points]], every zero-one measure on $X$ is a Dirac delta.

* Every [[ergodic measure]] is zero-one when restricted to the [[invariant sigma-algebra]]. 


## Further properties

* Zero-one measures are exactly the [[law of a random variable|laws]] of those [[random variables]] which satisfy a [[zero-one law]].

* Zero-one kernels are exactly the [[Markov category#deterministic_morphisms|deterministic states]] of [[Stoch]], in the sense of [[Markov categories]].


## The monad of zero-one measures

Zero-one measures form a [[monad]], which we denote by $(S,\eta_S,\mu_S)$, a submonad of the [[Giry monad]]. 
It can be seen as an analogue of the monad of [[completely prime filters]] ([[sober topological space#Reflection|sobrification]]) on $Top$, and because of that we also call it the **sobrification monad of measurable spaces** (see also at [[sober measurable space]]).
This monad is defined abstractly in [MP'22](#det_submonad) (based on previous work, see the references), here we give a more explicit description.

In what follows, let $X$ be a [[measurable space]], and denote its [[sigma-algebra]] by $\Sigma_X$.


### Functor and unit

The space of zero-one measures $S X$ on $X$ can be equivalently described as follows:

* It is the [[equalizer]] of the following pair:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX ,
\end{tikzcd}
* It is the subset of $P X$ (the [[Giry monad]]) of those measures which are zero-one, with the [[sigma-algebra]] induced from the one of $P X$;
* It is the set of all zero-one measures on $X$, together with the [[sigma-algebra]] $\Sigma_{S X}$ given by the following sets,
$$
A^* \;\coloneqq\; \{p\in S X \;:\; p(A) = 1 \}
$$
for all measurable $A\subseteq X$. 


The unit of the monad can be characterized equivalently as follows:

* Since every [[Dirac measure]] is zero-one, the map $\delta:X\to P X$ lands in $S X$. 
* Notice that by naturality of $\delta$ (the unit of the Giry monad), the map $\delta:X\to P X$ factors uniquely through the [[equalizer]] $S X$:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
X \ar{dr}{\delta} \ar[dashed]{d} \\
SX \ar[hookrightarrow]{r}{\iota} & PX \ar[shift left]{r}{\delta} \ar[shift right]{r}[swap]{P\delta} & PPX ,
\end{tikzcd}
We take as unit $\eta_S$ the resulting map $X\to S X$. 
Explicitly,
$$
\eta_S(x)(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A .
\end{cases}
$$

\begin{proposition}
 The assignment $A\mapsto A^*$ is an [[isomorphism]] of [[sigma-algebras]] $\Sigma_X\to \Sigma_{S X}$. Its [[inverse]] is given by the preimage map 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
column sep=large,%
row sep=0,%
]
\Sigma_{S X} \ar{r} & \Sigma_X \\
B \ar[mapsto]{r} & (\eta_S)^{-1}(B) .
\end{tikzcd}
\end{proposition}

(Compare to how a [[topological space]] and its [[sober topological space#Reflection|sobrification]] have the same [[frame]].) 


### Multiplication and idempotency


We can define the multiplication of the monad, explicitly, as follows. Given a *zero-one measure over zero-one measures* $\pi\in S S X$, we take $\mu_S(\pi)\in S X$ to be defined by
$$
\mu_S(\pi)(A) \;\coloneqq\; \pi(A^*) .
$$
Notice that for every $p\in S X$ and $\pi in S S X$, 
$$
\mu_S(\delta_S(p))(A) \;=\; \delta_S(p)(A^*) \;=\; 1_{A^*}(p) \;=\; p(A)
$$
and 
$$
\delta_S(\mu_S(\pi))(A^*) \;=\; 1_{A*}(\mu_S(\pi)) \;=\; \mu_S(\pi)(A) \;=\; \pi(A^*) .
$$
Therefore (using the fact that $A\mapsto A^*$ is a bijection), $\delta_S: S X\to S S X$ and $\mu_S: S S X\to S X$ are mutually inverse. 
This makes $S$ an [[idempotent monad|idempotent]] submonad of the [[Giry monad]]. 


### Kleisli category

The [[Kleisli category]] of the monad $S$ is the category of [[measurable spaces]] and [[zero-one kernels]], sometimes denoted by $Stoch_det$.

Since the monad is [[idempotent monad|idempotent]], its Kleisli category is [[equivalence of categories|equivalent]] to its [[Eilenberg-Moore category]], which is the category $SoberMeas$ of [[sober measurable spaces]]. 

Let's now write this equivalence explicitly.
One one side, define the functor $F:SoberMeas\to Stoch_det$ as follows:

* On [[objects]], it is the identity (or better said, it is forgetful from [[sober measurable spaces]] to all measurable spaces).
* On [[morphisms]], it maps a [[measurable function]] $f:X\to Y$ to the [[zero-one kernel]] $\delta_f:X\to Y$ [[Markov kernel#kernels_from_deterministic_functions|induced by]] $f$. 

Similarly we can define a functor $G:Stoch_det\to SoberMeas$ as follows:

* On [[objects]], it maps a (not necessarily sober) measurable space $X$ to $S X$.
* On [[morphisms]], it maps a [[zero-one kernel]] $k:X\to Y$ to the map $S X \to S Y$ which takes a zero-one measure $p\in S X$ and gives the zero-one measure on $Y$ defined by
$$
B \mapsto p(k^*B) ,
$$
for all $B\in\Sigma_Y$, where
$$
k^*B \;\coloneqq\; \{x\in X \,:\, k(B|x) = 1 \} .
$$

The unit $\eta_S:X\to S X$ induces a natural transformation with components $X\to GFX$. When $X$ is [[sober measurable space|sober]], this component is an isomorphism. 

Conversely, for a generic measurable space $Y$ (not necessarily sober), we have a [[natural transformation|natural]] [[zero-one kernel]] $\epsilon_S: S Y \to Y$ defined by
$$
\epsilon_S(A|p) \;=\; p(A) 
$$
for all $p\in S Y$ and all measurable subsets $A\subseteq Y$. 
(This can be seen as the restriction of the [[sampling map]] to zero-one measures.)

\begin{proposition}\label{Siso}
 The kernel $\epsilon: S Y \to Y$ is an isomorphism of $Stoch_det$, 
 where its inverse [[Markov kernel#kernels_from_deterministic_functions|is induced by]] the function $\eta_S:X\to S X$.
\end{proposition}

This way we have natural isomorphisms $\eta_S:id\Rightarrow G\circ F$ and $\epsilon_S:F\circ G\Rightarrow id$, which give an [[equivalence of categories]]. 


## Related entries

* [[zero-one kernel]]
* [[Markov kernel]], [[Markov category]], [[Stoch]], [[Krn]]
* [[zero-one law]], [[ergodicity]], [[deterministic random variable]]
* [[thunk-force category]]
* [[sober measurable space]]
* [[point-free topology]], [[point of a locale]]


## References

* [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_. Adv. Math., 370:107239, 2020. [arXiv:1908.07021](https://arxiv.org/abs/1908.07021).

* {#det_submonad} Sean Moss, [[Paolo Perrone]], _Probability monads with submonads of deterministic states_, LICS 2022. ([arXiv:2204.07003](https://arxiv.org/abs/2204.07003))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)

* {#br} Anna Bucalo and [[Giuseppe Rosolini]], _Sobriety for equilogical spaces_. Theorerical Computer Science 546, 2014. ([doi](https://doi.org/10.1016/j.tcs.2014.03.002))

* {#taylor} [[Paul Taylor]], _Sober spaces and continuations_. Theory and Applications of Categories 10(12), 2002. ([link](http://paultaylor.eu/asd/sobsc))

* {#moggi} [[Eugenio Moggi]], _Notions of computations and monads_, Information and Computation 93(1), 1991 (LICS 1989).

### Introductory material

* [[Paolo Perrone]], _When measurable spaces don't have enough points_, introductory talk. ([YouTube](https://www.youtube.com/watch?v=V4WzTgjbP3c))


category: probability


[[!redirects zero-one measure]]
[[!redirects zero-one measures]]
[[!redirects deterministic measure]]
[[!redirects deterministic measures]]
[[!redirects irreducible measure]]
[[!redirects irreducible measures]]