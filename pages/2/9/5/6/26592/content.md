+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
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

In [[probability theory]], it is a well known fact that [[events]] are not always [[independent events|independent]], i.e. that in general
$$
P(A,B) \ne P(A)\,P(B).
$$
One says that *the probability of a product is not the product of the probabilities*.
The term on the left is called the *joint probability* (the probability that the events $A$ and $B$ happen *jointly*) and the terms on the right are called *marginal probabilities* (the probabilities that $A$ and $B$ happen *separately*.)
In general, the joint probability has more information than the marginal probabilities alone, because of the presence of [[correlation]] or other [[stochastic interactions]].

From the [[category-theoretic approaches to probability theory|category-theoretic perspective]], one can encode this idea using the following (related) concepts:

* A [[monoidal category|monoidal structure]] on a [[category of kernels]] or [[Markov category]] which is [[semicartesian monoidal category|semicartesian]], but not [[cartesian monoidal category|cartesian]], i.e. for which the tensor product is not a [[product|categorical product]];

or 

* A [[probability monad]] which is [[affine monad|affine]] but not [[strong monoidal functor|strong monoidal]], i.e. which does not preserve [[products]].

When one takes as [[Markov category]] the [[Kleisli category]] of a [[probability monad]], the two concepts coincide.



## In measure-theoretic probability

Let $(\Omega,\mathcal{F},p)$ be a [[probability space]], and let $A,B\subseteq\mathcal{F}$ be [[events]], i.e. [[measurable subsets]] of $\Omega$.
We call the **joint probability** of $A$ and $B$ the probability of their [[intersection]], $p(A\cap B)$.

More generally, let $f:(\Omega,\mathcal{F})\to(X,\mathcal{A})$ and $g:(\Omega,\mathcal{F})\to(Y,\mathcal{B})$ be [[random variables]] (or [[random elements]]) on $\Omega$.
The **joint random variable** of $f$ and $g$ is the random variable $(f,g):(\Omega,\mathcal{F})\to(X\times Y,\mathcal{A}\otimes\mathcal{B})$ given by the [[universal property]] of the [[product]]:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
& \Omega \ar{dl}[swap]{f} \ar{dr}{g} \ar[dashed]{d}[near end]{(f,g)} \\
X & X\times Y \ar{l}{\pi_1} \ar{r}[swap]{\pi_2} & Y
\end{tikzcd}

We call 

* The **joint distribution** of $f$ and $g$ (or of $X$ and $Y$, when the maps are clear from the context) the [[pushforward measure]] $p_{X,Y}=(f,g)_*p$ on $X\times Y$;
* The **marginal distributions** of $f$ and $g$ (or of $X$ and $Y$) the [[pushforward measures]] $p_X=f_*p$ and $p_Y=g_*p$ on $X$ and $Y$, respectively.

Note that $(\pi_1)_*p_{X,Y} = p_X$ and $(\pi_2)_*p_{X,Y} = p_Y$, so that the marginalization maps can be seen as the functorial images of the [[product]] projections under a [[probability monad]].

In absence of the space $\Omega$ one can call "joint distribution" any probability distribution on a product space $X\times Y$, and define its marginal distributions by pushing forward along the product projections. This is equivalent to taking $X\times Y$ as $\Omega$. The same is true for products of more spaces, including [[infinite tensor product|infinite products]].

Given two (marginal) distributions $p$ and $q$ on spaces $(X,\mathcal{A})$ and $(Y,\mathcal{B})$, in principle there could be many joint distributions on $X\times Y$ admitting $p$ and $q$ as their marginals, corresponding to different possible [[stochastic dependence and independence|stochastic interactions]].
A canonical choice of joint distribution is given by the **product distribution** $p\otimes q$, defined on product sets in the form $A\times B\subseteq X\times Y$ by
$$
(p\otimes q)\,(A\times B) = p(A)\,q(B) ,
$$
which makes $X$ and $Y$ [[stochastic dependence and independence|independent]].


### In terms of probability monads

Recall that the [[Giry monad]], as well as other [[probability monads]], encodes the idea of forming, from a space $X$, a space $P X$ of [[probability measures]] over it. 
A joint distribution is then encoded by an element of the space $P(X\times Y)$, and the marginals are elements of $P X$ and $P Y$ obtained via applying $P$ to the product projections.
Additionally, by the [[universal property]] of [[products]], there exists a unique map $\Delta:P(X\times Y)\to P X\times P Y$ making the following diagram commute.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
& P(X\times Y) \ar{dl}[swap]{P(\pi_1)} \ar{dr}{P(\pi_2)} \ar[dashed]{d}{\Delta} \\
PX & PX\times PY \ar{l}{\pi_1} \ar{r}[swap]{\pi_2} & PY
\end{tikzcd}
This can be interpreted as forming, from a joint distribution, the pair of its marginals, which in general encode less information. The same can be done for joint distributions over a larger number of factors, including [[infinite tensor product|infinite products]].

In order to form product distributions, one needs additional compatibility conditions between the [[monad]] structure (giving probability measures) and the [[products]] of the category.
These conditions are exactly captured by the idea of a [[monoidal monad]], or equivalently, a [[commutative monad]].  
This amounts in particular to a [[natural transformation|natural map]] $\nabla:P X\times P Y\to P(X\times Y)$ satisfying particular compatibility conditions. For the [[Giry monad]], it is the following map.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
row sep=0,%
]
PX\times PY \ar{r}{\nabla} & P(X\times Y) \\
(p,q) \ar[mapsto]{r} & p\otimes q 
\end{tikzcd}

Consider now the following two diagrams.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large%
]
PX \times PY \ar{dr}[swap]{\mathrm{id}} \ar{r}{\nabla} & P(X\times Y) \ar{d}{\Delta} & P(X\times Y) \ar{dr}[swap]{\mathrm{id}} \ar{r}{\Delta} & PX\times PX \ar{d}{\nabla} \\
& PX\times PY & & P(X\times Y)
\end{tikzcd}

We have that 

* The commutativity of the diagram on the left says that if one forms a product measure and then takes its marginals, one recovers the two factors. In other words, *every product probability measure is necessarily the product of its marginals*.
One can show that the diagram on the left commutes if and only if $P$ preserves the terminal object, i.e. $P(1)\cong 1$ (see at [[affine monad]]). This is the case for the [[Giry monad]] and for most [[probability monads]], since the one-point space admits a unique probability measure. (It can be considered a "normalization" condition for probability measures: if one drops normalization, the one-point space admits several measures.)


* In general, the diagram on the right does not commute: if one starts with a joint distribution and then forms its marginals, the original distribution may be different from the product of the marginals. Therefore marginalization is a destructive operation, forgetting possible [[stochastic interaction]]. 
Indeed, if the diagram on the left commutes, then the diagram on the right commutes if and only if the monad $P$ preserves [[products]], i.e. it is [[strong monoidal functor|strong monoidal]]. The "random" behavior of the [[Giry monad]] and of other [[probability monads]] can be explained, to a large degree, by their failure to preserve products. (More on this below, and at [[Markov category#eqdet|Markov category]]).


### In the category of Markov kernels

As we have seen above, a joint distribution, in general, encodes more information than the pair of its marginals, and cannot always be recovered by forming the product distribution. 

We can express this equivalently by looking at the category [[Stoch]] of [[Markov kernels]], as well as at other [[Kleisli categories]] of similar [[probability monads]].

First of all, recall that the category [[Stoch]] inherits the [[monoidal category|monoidal structure]] from the [[product]] in [[Meas]], the [[cartesian product]] of [[measurable spaces]]. 

This product in [[Stoch]], however, is not a categorical product: the [[universal property]] of a [[product]] requires that given [[objects]] $\Omega$, $X$ and $Y$ in a [[category]], for every pair of morphisms $f:\Omega\to X$ and $g:\Omega\to Y$ there exists a unique morphism $\Omega\to X\otimes Y$ making the following diagram commute.
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
sep=large,%
]
& \Omega \ar{dl}[swap]{f} \ar{dr}{g} \ar[dashed]{d}[near end]{(f,g)} \\
X & X\otimes Y \ar{l}{\pi_1} \ar{r}[swap]{\pi_2} & Y
\end{tikzcd}
For Markov kernels, this property does not hold: setting $\Omega=1$, the one-point space, the property would require in particular that there is a unique joint distribution on $X\times Y$ for every pair of marginals $X$ and $Y$. As we have seen above, this is not the case. 
What fails is not the *existence* part of the universal property: a joint distribution always exists, the product distribution. What fails is the *uniqueness* part. In other words, the monoidal structure in [[Stoch]] is a [[weak limit|weak product]] but not a categorical [[product]]. 

More generally, given a [[monoidal monad]] on a [[cartesian monoidal category]], the induced monoidal structure on the [[Kleisli category]] is monoidal only when the monad is [[strong monoidal functor|strong monoidal]], and we saw that this is not the case for most probability monads.
(As mentioned at [[Markov category#eqdet|Markov category]], a cartesian monoidal Kleisli category can be seen as having "no randomness".)


## In Markov categories

In [[Markov categories]], one can define joint and marginal states similarly to what happens in the category [[Stoch]]. Recall that a state on $X$

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, double}},%
]

		\node [style=none] (0) at (0, -0.5) {};
		\node [style=none] (1) at (0, 1) {};
                \node [style=none] (2) at (0, 1.5) {$X$};

		\draw (0.center) to (1.center);

        \node [style=morphism] (4) at (0, -0.5) {$p$};
\end{tikzpicture}

has the interpretation of a [[probability measure]] on $X$, and in [[Stoch]] it is exactly a [[Markov kernel]] $1\to X$, i.e. a probability measure.

A *joint state* is a state in the form $I\to X\otimes Y$:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (10) at (-3, 0) {};
		\node [style=none] (11) at (-2, 0) {};
		\node [style=none] (12) at (-2, 1.25) {};
		\node [style=none] (13) at (-3, 1.25) {};
		\node [style=none] (14) at (-3, 1.75) {$X$};
		\node [style=none] (15) at (-2, 1.75) {$Y$};
		\node [style=none] (20) at (-2.5, 0) {};

		\draw (10.center) to (13.center);
		\draw (11.center) to (12.center);
        
                \node [style=morphism] (27) at (-2.5, 0) {$\;\, p \;\,$};
\end{tikzpicture}

In *Stoch*, this is exactly a probability measure on $X\times Y$.

Given a joint state $p$ on $X\otimes Y$, its *marginals* are the states $p_X$ and $p_Y$ on $X$ and $Y$ respectively given by discarding the unobserved variable:

\begin{tikzpicture}[%
thick,%
scale=0.8,%
every node/.style={scale=1.25},%
none/.style={fill=none,draw=none},%
morphism/.style={fill=white, draw=black, shape=rectangle},%
bn/.style={fill=black, draw=black, shape=circle, inner sep=1.8pt},%
over arrow/.style={-, black, preaction={draw=white, line width=2mm}},%
]
	
		\node [style=none] (0) at (-3.5, -0.75) {};
		\node [style=none] (2) at (-4, 1) {};
		\node [style=none] (3) at (-4, 1.5) {$X$};
		\node [style=none] (4) at (-4, -0.5) {};
		\node [style=none] (5) at (-3, -0.5) {};
		\node [style=bn] (6) at (-3, 0.5) {};
		\node [style=none] (9) at (-8.25, 1) {};
		\node [style=none] (10) at (-8.25, 1.5) {$X$};
		\node [style=none] (11) at (-8.25, -0.5) {};
		\node [style=none] (12) at (-6, 0) {$=$};
		\node [style=none] (13) at (7.75, -0.75) {};
		\node [style=none] (15) at (8.25, 1) {};
		\node [style=none] (16) at (8.25, 1.5) {$Y$};
		\node [style=none] (17) at (8.25, -0.5) {};
		\node [style=none] (18) at (7.25, -0.5) {};
		\node [style=bn] (19) at (7.25, 0.5) {};
		\node [style=none] (21) at (3, 1) {};
		\node [style=none] (22) at (3, 1.5) {$Y$};
		\node [style=none] (23) at (3, -0.5) {};
		\node [style=none] (24) at (5.25, 0) {$=$};

		\draw (2.center) to (4.center);
		\draw (5.center) to (6);
		\draw (9.center) to (11.center);
		\draw (15.center) to (17.center);
		\draw (18.center) to (19);
		\draw (21.center) to (23.center);

		\node [style=morphism] (1) at (-3.5, -0.75) {$\;\, p \;\,$};
		\node [style=morphism] (8) at (-8.25, -0.75) {$p_X$};
		\node [style=morphism] (14) at (7.75, -0.75) {$\;\, p \;\,$};
		\node [style=morphism] (20) at (3, -0.75) {$p_Y$};
\end{tikzpicture}

In *Stoch*, these correspond exactly to marginal distributions.

More on this (and examples in other Markov categories) can be found at [[Markov category#states_channels_joints_marginals|Markov category - States, channels, joints, marginals]].


## See also 

* [[stochastic dependence and independence]]
* [[affine monad]]
* [[probability theory]], [[categorical probability]]
* [[probability monad]], [[Giry monad]]
* [[Markov category]], [[Markov kernel]]
* [[infinitary tensor product]], [[Kolmogorov extension theorem]]


## References

* {#bimonoidal_monads} [[Tobias Fritz]], [[Paolo Perrone]], _Bimonoidal Structure of Probability Monads_, Proceedings of MFPS, 2018, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* {#Perrone_thesis} [[Paolo Perrone]], _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* [[Anders Kock]], _Bilinearity and cartesian closed monads_, Mathematica Scandinavica 29(2), 1971. 


category: probability


[[!redirects joint and marginal probabilities]]
[[!redirects joint and marginal distribution]]
[[!redirects joint and marginal distributions]]
[[!redirects joint and marginal measure]]
[[!redirects joint and marginal measures]]
[[!redirects joint and marginal probability distribution]]
[[!redirects joint and marginal probability distributions]]
[[!redirects joint and marginal probability measure]]
[[!redirects joint and marginal probability measures]]
[[!redirects joints and marginals]]
[[!redirects joint distribution]]
[[!redirects joint distributions]]
[[!redirects joint probability]]
[[!redirects joint probabilities]]
[[!redirects joint measure]]
[[!redirects joint measures]]
[[!redirects joint probability distribution]]
[[!redirects joint probability distributions]]
[[!redirects joint probability measure]]
[[!redirects joint probability measures]]
[[!redirects marginal distribution]]
[[!redirects marginal distributions]]
[[!redirects marginal probability]]
[[!redirects marginal probabilities]]
[[!redirects marginal measure]]
[[!redirects marginal measures]]
[[!redirects marginal probability distribution]]
[[!redirects marginal probability distributions]]
[[!redirects marginal probability measure]]
[[!redirects marginal probability measures]]
[[!redirects product probability]]
[[!redirects product probabilities]]
[[!redirects product distribution]]
[[!redirects product distributions]]
[[!redirects product probability distribution]]
[[!redirects product probability distributions]]
[[!redirects product probability measure]]
[[!redirects product probability measures]]