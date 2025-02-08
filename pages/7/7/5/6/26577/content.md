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

In elementary [[probability theory]], [[Bayes' formula]] refers to a version of the formula 
$$
   P(A)\,P(B|A) \,=\, P(B)\,P(A|B)
   \,,
$$
and relates the [[conditional probability]] of $B$ given $A$ to the one of $A$ given $B$.

From the [[category-theoretic probability|category-theoretic point of view]], this formula expresses a duality, sometimes called **Bayesian inversion**, which often gives rise to a [[dagger category|dagger structure]].


## Intuition

In logical reasoning, implications in general cannot be reversed: $A \to B$, alone, does not imply $B\to A$. 

In [[probability theory]], instead, conditional statements exhibit a [[duality]] which is absent in pure logical reasoning.

Consider for example a city in which *all taxis are yellow*. (The implication is $taxi\to yellow$.)
If we see a yellow car, of course we can't be sure it's a taxi. However, it's *more likely* that it's a taxi compared to a randomly colored car. This increase in likelihood is larger if the fraction of yellow cars is small. Indeed, [[Bayes' rule]] says that 
$$
P(taxi|yellow) = \frac{P(yellow\,taxi)}{P(yellow)} = \frac{P(taxi)}{P(yellow)} .
$$

More generally, in a city where *most* taxis are yellow, there is a high conditional probability that a given taxi is yellow,
$$
P(yellow|taxi) .
$$
The higher this probability is, the higher is the probability that a given yellow car is a taxi, again according to [[Bayes' rule]]:
$$
P(taxi|yellow) = \frac{P(yellow\,taxi)}{P(yellow)} = \frac{P(taxi)\,P(yellow|taxi)}{P(yellow)}
$$

In [[categorical probability]], this phenomenon can be modeled by saying that to each "conditional" morphism in the form $\{taxi, not\,taxi\}\to\{colors\,of\,cars\}$ there corresponds a canonical morphism $\{colors\,of\,cars\}\to\{taxi, not\,taxi\}$, called the *Bayesian inverse*. The name, which is kept for historical reasons, is somewhat improper, since we don't actually have an [[inverse morphism]] in the sense of category theory, but simply a reversal of the arrow.

In some cases, this symmetry gives rise to a [[dagger category]].



## In traditional probability theory

In traditional [[probability theory]], Bayesian inversions are a special case of [[conditional probability]].
Some care must be taken to avoid dividing by zero or incurring into paradoxes via limiting procedures.


### Discrete case

In the discrete case, a [[probability distribution]] on a [[set]] $X$ is simply a function $p:X\to[0,1]$ such that 
$$
\sum_{x\in X} p(x) = 1 .
$$

A [[stochastic map]] $k:X\to Y$ is a function 
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
X\times Y \ar{r} & {[0,1]} \\
(x,y) \ar[mapsto]{r} & k(y|x)
\end{tikzcd}
such that for all $x\in X$,
$$
\sum_{y\in Y} k(y|x) = 1 .
$$
If we now equip $X$ and $Y$ with discrete probability distributions $p$ and $q$, obtaining discrete [[probability spaces]], we say that $k$ is a [[stochastic map#measurepreserving_stochastic_maps|measure-preserving stochastic map]] $(X,p)\to(Y,q)$ if for every $y\in Y$,
$$
\sum_{x} k(y|x) \, p(x) = q(y) .
$$

A **Bayesian inverse** of $k:(X,p)\to(Y,q)$ is then defined to be a measure-preserving stochastic map $k^\dagger:(Y,q)\to(X,p)$ such that for every $x\in X$ and $y\in Y$, the following [[Bayes formula]] holds.
$$
p(x) \,k(y|x) = q(y)\,k^\dagger(x|y) 
$$

In the discrete case, Bayesian inverses always exist, and can be obtained by taking
$$
k^\dagger(x|y) \coloneqq \frac{p(x)\,k(y|x)}{q(y)}
$$
for those $y\in Y$ with $q(y)\ne 0$, and an arbitrary number on the $y\in Y$ with $q(y)=0$.
(To ensure the normalization condition, on such $y$ one can for example take $k^\dagger(x|y)=\delta_{x_0,x}$, where $x_0$ is a fixed element of $X$. Note that $X$ is nonempty since it admits a probability measure.)

Bayesian inverses are not unique, but they are uniquely defined on the support of $q$. That is, they are unique up to [[almost surely|almost sure]] [[equality]].


### Measure-theoretic case

The situation is more delicate outside the discrete case.
Given [[probability spaces]] $(X,\mathcal{A},p)$ and $(Y,\mathcal{B},q)$, and a [[Markov kernel#measurepreserving_kernels|measure-preserving Markov kernel]] $k:(X,\mathcal{A},p)\to(Y,\mathcal{B},q)$, a **[[Markov kernel#bayesian_inversion|Bayesian inverse]]** of $k$ is a Markov kernel $k^\dagger:(Y,\mathcal{B},q)\to(X,\mathcal{A},p)$ such that for all $A\in\mathcal{A}$ and $B\in\mathcal{B}$, the following Bayes-type formula holds.
$$
\int_A k(B|x)\,p(dx) = \int_B k^\dagger(A|y)\,q(dy) 
$$
As one can see from [[Markov kernel#almost_sure_equality|Markov kernel - Almost sure equality]], this formula specifies a kernel only up to [[almost surely|almost sure]] [[equality]], just as in the discrete case.

Existence, on the other hand, is more tricky. In general, a kernel $k^\dagger$ as above may fail to exist. The problem is that in order for $k^\dagger$ to be a well-defined [[Markov kernel]] $(Y,\mathcal{B})\to(X,\mathcal{A})$, we need the following two conditions:

* the map $y\mapsto k^\dagger(A|y)$ is [[measurable function|measurable]] in $y$ for all $A\in\mathcal{A}$;
* the assignment $A\mapsto k^\dagger(A|y)$ is a [[probability measure]] in $A$ for all $y\in Y$.

The first condition can be taken care of using [[conditional expectation]]. 
That however does not assure the second condition. It can be shown, however, that if $(X,\mathcal{A})$ is [[standard Borel]] and either 

* $(Y,\mathcal{B})$ is standard Borel too

or

* the kernel $k:X\to Y$ is in the form $\delta_f$ for a measurable $f:X\to Y$,

then a Bayesian inverse always exists. 

(See also [[Markov kernel#bayesian_inversion|Markov kernel - Bayesian inversion]] and [[Markov kernel#conditionals|Markov kernel - Conditionals]].)



## In categorical probability

In [[categorical probability]], Bayesian inverses are axiomatized in a way which reflects the measure-theoretic version of the concepts.
One then can choose to work in categories where such axioms are satisfied.


### In Markov categories

In [[Markov categories]], Bayesian inverses are defined in a way that parallels the construction for Markov kernels. 

The abstraction of a [[probability space]] is given by an [[object]] $X$ in a [[Markov category]], together with a state $p:I\to X$. As usual, the abstraction of a kernel is a morphism $f:X\to Y$.  
A **Bayesian inverse** of $f$ with respect to $p$ is a morphism $f^\dagger:Y\to X$ such that the following equation holds, where $q=f\circ p$.

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=bn] (0) at (-3, -1) {};
		\node [style=bn] (1) at (3, -1) {};
		\node [style=none] (2) at (-3, -2) {};
		\node [style=none] (3) at (3, -2) {};
		\node [style=none] (4) at (-4, 0) {};
		\node [style=none] (5) at (-2, 0) {};
		\node [style=none] (6) at (2, 0) {};
		\node [style=none] (7) at (4, 0) {};
		\node [style=none] (8) at (-4, 1.5) {};
		\node [style=none] (9) at (-2, 1.5) {};
		\node [style=none] (10) at (2, 1.5) {};
		\node [style=none] (11) at (4, 1.5) {};
		\node [style=none] (16) at (-4, 2) {$X$};
		\node [style=none] (17) at (-2, 2) {$Y$};
		\node [style=none] (18) at (2, 2) {$X$};
		\node [style=none] (19) at (4, 2) {$Y$};
		\node [style=none] (20) at (0, -0.25) {$=$};

		\draw [in=165, out=-90] (4.center) to (0);
		\draw [in=15, out=-90] (5.center) to (0);
		\draw (0) to (2.center);
		\draw [in=165, out=-90] (6.center) to (1);
		\draw [in=15, out=-90] (7.center) to (1);
		\draw (1) to (3.center);
		\draw (8.center) to (4.center);
		\draw (9.center) to (5.center);
		\draw (10.center) to (6.center);
		\draw (11.center) to (7.center);

		\node [style=morphism] (12) at (-4, 0.25) {$f^\dagger_p$};
		\node [style=morphism] (13) at (4, 0.25) {$f$};
		\node [style=morphism] (14) at (-3, -2) {$q$};
		\node [style=morphism] (15) at (3, -2) {$p$};
\end{tikzpicture}

This recovers the classical probability definitions when instantiated in [[Stoch]] and its subcategories.

Just as in traditional probability, Bayesian inverses are unique only up to [[almost sure equality]].
Also, just as in traditional probability, they may fail to exist. Being an instance of [[Markov category#conditionals|conditionals]], however, they always exists when conditionals exist, such as in the category [[BorelStoch]].

(See also [[Markov category#conditionals|Markov category - conditionals]].)



### In dagger categories

In the [[category of couplings]], the idea of Bayesian inversion is made explicit from the start by means of the [[dagger category|dagger structure]]. 
Given [[probability spaces]] $(X,\mathcal{A},p)$ and $(Y,\mathcal{B},q)$, a [[coupling (probability theory)|coupling]] between them can be seen equivalently as going from $X$ to $Y$ or from $Y$ to $X$. This duality, when the couplings are expressed via [[Markov kernels]], reflects exactly Bayesian inversion. 
Therefore, at the level of joint distributions, one can consider the duality given by Bayesian inversions to be already part of the symmetry of the category.

Categorical abstractions of the category of coupling via [[dagger categories]] have therefore the concept of Bayesian inversion already built in.



## Quantum versions

(For now, see the references.)



## See also

* [[categorical probability]], [[Markov category]]

* [[transport plan]], [[category of couplings]]

* [[Markov kernel]], [[stochastic map]], [[Stoch]]

* [[conditional probability]], [[conditional expectation]]

* [[probability theory]], [[statistics]], [[Bayesian statistics]]

* [[dagger category]]



## References

For [[categorical probability]]:

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#cd_categories} Kenta Cho and [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* Dario Stein and [[Sam Staton]], _Probabilistic Programming with Exact Conditions_, JACM, 2023. ([arXiv](https://arxiv.org/abs/2312.17141))

* Noé Ensarguet and [[Paolo Perrone]], _Categorical probability spaces, ergodic decompositions_, and transitions to equilibrium, 2023. ([arXiv:2310.04267](https://arxiv.org/abs/2310.04267))


For the quantum case:

* {#coecke_spekkens12} [[Bob Coecke]], [[Robert W. Spekkens]]: *Picturing classical and quantum Bayesian inference*, Synthese, **186** 3 (2012) &lbrack;[arXiv:1102.2368](https://arxiv.org/abs/1102.2368), [doi:10.1007/s11229-011-9917-5](https://doi.org/10.1007/s11229-011-9917-5)&rbrack;

and using [[Markov categories]]:

* {#quantum_markov} [[Arthur J. Parzygnat]], _Inverses, disintegrations, and Bayesian inversion in quantum Markov categories_, 2020. ([arXiv](https://arxiv.org/abs/2001.08375))

* {#noncommutative_bayes} [[Arthur J. Parzygnat]], [[Benjamin P. Russo]]: _A noncommutative Bayes theorem_, Linear Algebra Applications **644** (2022) &lbrack;[doi:10.1016/j.laa.2022.02.030](https://doi.org/10.1016/j.laa.2022.02.030), [arXiv:2005.03886](https://arxiv.org/abs/2005.03886)&rbrack;

* {#conditional_quantum} [[Arthur J. Parzygnat]]: *Conditional distributions for quantum systems*, EPTCS **343** (2021) 1-13 &lbrack;[arXiv:2102.01529](https://arxiv.org/abs/2102.01529), [doi:10.4204/EPTCS.343.1](https://doi.org/10.4204/EPTCS.343.1)&rbrack;

* {#retrodiction} [[Arthur J. Parzygnat]], Francesco Buscemi, _Axioms for retrodiction: achieving time-reversal symmetry with a prior_, Quantum **7** (2023) 1013 &lbrack;[arXiv:2210.13531](https://arxiv.org/abs/2210.13531), [doi:10.22331/q-2023-05-23-1013](https://doi.org/10.22331/q-2023-05-23-1013)&rbrack;

* {#quantum_states_time} [[James Fullwood]], [[Arthur J. Parzygnat]]: _On quantum states over time_, Proceedings of the Royal Society A **478** (2022) &lbrack;[arXiv:2202.03607](https://arxiv.org/abs/2202.03607), [doi:10.1098/rspa.2022.0104](https://doi.org/10.1098/rspa.2022.0104)&rbrack;

* {#quantum_bayes} [[James Fullwood]], [[Arthur J. Parzygnat]]: *From time-reversal symmetry to quantum Bayes rules*, PRX Quantum **4** 020334 (2023) &lbrack;[arXiv:2212.08088](https://arxiv.org/abs/2212.08088), [doi:10.1103/PRXQuantum.4.020334](https://doi.org/10.1103/PRXQuantum.4.020334)&rbrack;

* [[James Fullwood]], [[Arthur J. Parzygnat]]: *Operator representation of spatiotemporal quantum correlations* &lbrack;[arXiv:2405.17555](https://arxiv.org/abs/2405.17555)&rbrack;

* [[Arthur J. Parzygnat]], [[James Fullwood]]: *Time-symmetric correlations for open quantum systems* &lbrack;[arXiv:2407.11123](https://arxiv.org/abs/2407.11123)&rbrack;

* {#noncomm_disintegrations} [[Arthur J. Parzygnat]], Benjamin P. Russo, _Non-commutative disintegrations: existence and uniqueness in finite dimensions_, Journal of Noncommutative Geometry 17(3), 2023. ([arXiv](https://arxiv.org/abs/1907.09689))

Review:

* [[Arthur Parzygnat]]: *A Spatiotemporal Extension of Density Matrices and Time-Reversal Symmetry for Measurements*, [talk at](Center+for+Quantum+and+Topological+Systems#ParzygnatNov2024) [[CQTS]] (Nov 2024) &lbrack;slides:[[Parzygnat-CQTS-Nov2024.pdf:file]]&rbrack;



category: probability

[[!redirects Bayesian inversions]]
[[!redirects Bayesian inverse]]
[[!redirects Bayesian inverses]]
[[!redirects bayesian inversion]]
[[!redirects bayesian inversions]]
[[!redirects bayesian inverse]]
[[!redirects bayesian inverses]]

