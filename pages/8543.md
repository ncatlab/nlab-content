
> This article is under construction.


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Idea

In [[probability theory]] a _conditional expectation value_ or _conditional expectation_, for short, is like an _[[expectation value]]_ of some [[random variable]]/[[observable]], but _conditioned_ on the assumption that a certain [[event (in probability theory)|event]] is assumed to have occured. 


More technically: If $(\Omega,\mathfrak{A},P)$ is a [[probability space]], the *conditional expectation* $E[X|\Sigma]$ of a (measurable) random variable $X$ with respect to some sub-$\sigma$-algebra $\Sigma\subseteq \mathfrak{A}$ is some measurable random variable which is a ''coarsened'' version of $X$. We can think of $E[X|\Sigma]$ as a random variable with the same [[domain]] but which is measured with a sigma algebra containing only restricted information on the original [[event (in probability theory)|event]] since to some events in $\mathfrak{A}$ has been assigned probability $1$ or $0$ in a consistent way.

## Conditional expectation relative to a random variable

Let $(\Omega,\mathfrak{A},P)$ be a [[probability space]], let $Y$ be a measurable function into a [[measure space]] $(U,\Sigma,P^Y)$ equipped with the [[pushforward measure]] induced by $Y$, let $X:(\Omega,\mathfrak{A},P)\to(\mathbb{R},\mathcal{B}(\mathbb{R}), \lambda)$ be a real-valued [[random variable]].

Then for $X$ and $Y$ there exists a essentially unique (two sets are defined to be equivalent if their difference is a set of measure $0$) [[integrable function]] $g=:E[X|Y]$ such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
   (\Omega,\mathfrak{A},P)&
    \stackrel{Y}{\to}&
    (\U, \Sigma, P^Y)
    \\
    \downarrow^{\mathrlap{X}}
    &&
   \swarrow_{\mathrlap{g=:E[X|Y]}}
  \\
   (\mathbb{R},\mathcal{B}(\mathbb{R}),\lambda)
 }
$$

where $g:y\mapsto E[X|Y=y]$. Here ''commutes'' shall mean that

(1) $g$ is $\Sigma$-measurable.

(2) the [[integrals]] over $X$ and $g\circ Y$ are equal.

In this case $g=E[X|Y]$ is called a version of the **conditional expectation of $X$ provided $Y$**.

In more detail (2) is equivalent to that for all $B\in \Sigma$ we have

$$\int_{Y^{-1}(B)}X(\omega)d P(\omega)=\int_B g(u)d P^Y (u)$$

and to

$$\int_{Y^{-1}(B)}X(\omega)d P(\omega)=\int_{Y^{-1}(B)}(g\circ Y)(\omega)d P (\omega)$$

(The equivalence of the last two formulas is given since we always have $\int_B g(u)d P^Y (u)=\int_{Y^{-1}(B)} (g\circ Y)(\omega)d P (\omega)$ by the substitution rule.)

Note that it does *not* follow from the preceding definition that the conditional expectation exists. This is a consequence of the [[Radon-Nikodym theorem]] as will be shown in the following section. (Note that the argument of the theorem applies to the definition of the conditional expectation by random variables if we consider the [[pushforward measure]] as given by a sub-$\sigma$-algebra of the original one. In this sense $E[X|Y]$ is a ''coarsened version'' of $X$ factored by the information (i.e. the $\sigma$-algebra) given by $Y$.)

## Conditional expectation relative to a sub-$\sigma$-algebra

Note that by construction of the pushforward-measure it suffices to define the conditional expectation only for the case where $\Sigma:=\mathfrak{S}\subseteq \mathfrak{A}$ is a sub-$\sigma$-algebra.

(Note that we loose information with the notation $P^Y$; e.g $P^{id}_\mathfrak{A}$ is different from $P^{id}_\mathfrak{S}$)

The diagram

$$\array{
(\Omega,\mathfrak{A},P)&
\stackrel{id}{\to}&
(\Omega, \mathfrak{S}, P^{id})
\\
\downarrow^X&&
\swarrow^{Z=:E[X|\mathfrak{S}]}
\\
(\mathbb{R},\mathcal{B}(\mathbb{R}),\lambda)
}$$


is commutative (in our sense) iff

(a) $Z$ is $\mathfrak{S}$-measurable

(b) $\int_A Z d P=\int_A X d P$, $\forall A\in \mathfrak{S}$

We hence can write the conditional expectation as the equivalence class

$$E[X|\mathfrak{S}]=\{Z\in L^1 (\Omega, F,P)|\int_A ZdP=\int_A XdP\;\forall A\in \mathfrak{S}\}$$

An element of this class is also called a *version*.

+-- {: .num_theorem}
###### Theorem

$E[X|\mathfrak{S}]$ exists and is unique almost surely.

=--

+-- {: .proof}
###### Proof

Existence: By

$$Q(A):=\int_A X(\omega)P(d\omega)$$

$A\in \mathfrak{A}$ is defined a measure $Q$ on $(\Omega,\mathfrak{A},P)$ (if $X\ge 0$; if not consider the positive part $X^+$ and the negative part $X^-$ of $X=X^+ -X^-$ separate and use linearity of the integral). Let $P|_{\mathfrak{S}}$ be the restriction of $P$ to $\mathfrak{S}$. Then

$$Q\lt\lt P|_{\mathfrak{S}}$$

meaning: $P|_{\mathfrak{S}}(M)=0\Rightarrow Q(M)=0$ for all $M\in\mathfrak{S}$. This is the condition of the [[Radon-Nikodym derivative|theorem of Radon-Nikodym]] (the other condition of the theorem that $P|_{\mathfrak{S}}$ is $\sigma$-finite is satisfied since $P$ is a probability measure). The theorem implies that $Q$ has a density w.r.t $P|_{\mathfrak{S}}$ which is $E[X|\mathfrak{S}]$.

Uniqueness: If $g$ and $g^\prime$ are candidates, by linearity the integral over their difference is zero.
=--

## Conditional probability

From elementary probability theory we know that $P(A)=E[1_A]$.

For $A\in \mathfrak{S}$ we call $P(A|\mathfrak{S}):=E[1_A|\mathfrak{S}]$ the *conditional probability of $A$ provided $B$*.



## Conditional distribution, Conditional density

## Integral kernel, Stochastic kernel

In probability theory and statistics, a stochastic kernel is the transition function of a stochastic process. In a discrete time process with continuous probability distributions, it is the same thing as the kernel of the integral operator that advances the probability density function.

### Integral kernel

An *integral transform* $T$ is an assignation of the form

$$(Tf)(u)=\int K(t,u)f(t)dt$$

where the function of two variables $K( \dots ,\cdots)$ is called *integral kernel of the transform $T$*.

### Stochastic kernel

Let $(\Omega_1,\mathfrak{A}_1)$ be a measure space, let $(\Omega_2,\mathfrak{A}_2)$ be a measurable space.

A map $Q: \Omega_1\times \mathfrak{A}_2$ satisfying

(1) $Q(-, A):\Omega_1\to [0,1]$ is $\mathfrak{A}_1$ measurable $\forall A_2\in \mathfrak{A}_2$

(2) $Q(\omega,-):\mathfrak{A}_2\to [0,1]$ is a probability measure on $(\Omega_2,\mathfrak{A}_2)$, $\forall \omega_1\in \Omega_1$

is called a *stochastic kernel* or *transition kernel* (or *Markov kernel* - which we avoid since it is confusing) *from $(\Omega_1,\mathfrak{A}_1)$ to $(\Omega_2,\mathfrak{A}_2)$.

Then $Q$ induces a function between the classes of measures on $(\Omega_1, \mathfrak{A}_1)$ and on $(\Omega_2, \mathfrak{A}_2)$

$$\overline{Q}:
\begin{cases}
M(\Omega_1, \mathfrak{A}_1)&
\to&
M(\Omega_2, \mathfrak{A}_2)
\\
\mu&
\mapsto&
(A\mapsto \int_{\Omega_1} Q(-, A) d\mu)
\end{cases}$$

If $\mu$ is a probability measure, then so is $\overline{Q}(\mu)$. The symbol $Q(\omega, A)$ is sometimes written as $Q(A|\omega)$ in optical proximity to a conditional probability.

The stochastic kernel is hence in particular an integral kernel.

In a discrete stochastic process (see below) the transition function is a stochastic kernel (more precisely it is the function $\overline{Q}$ induced by a kernel $Q$).

#### Coupling (Koppelung)

Let $(\Omega_1,\mathfrak{A}_1, P_1)$ be a probability space, let $(\Omega_2,\mathfrak{A}_2)$ be a measure space, let $Q:\Omega_1\times \mathfrak{A}_2\to [0,1]$ be a stochastic kernel from $(\Omega_1,\mathfrak{A}_1, P_1)$ to $(\Omega_2,\mathfrak{A}_2)$.

Then by

$$P(A):=\int_{\Omega_1}(\int_{\Omega_2} 1_A (\omega_1,\omega_2 Q(\omega_1,\omega_2))P_1(d \omega_1)$$

is defined a probability measure on $\mathfrak{A}_1\otimes\mathfrak{A}_2$ which is called *coupling*. $P=:P\otimes Q$ is unique with the property

$$P(A_1\times A_2)=\int_{A_1} Q(\omega_1, A_2) P_1(d\omega_1)$$

+-- {: .num_theorem}
###### Theorem

Let (with the above settings) $Y:\Omega_1\to \Omega_2$ be $(\mathfrak{A}_1,\mathfrak{A}_2)$-measurable, let $X$ be a $d$-dimensional random vector.

Then there exists a stochastic kernel from $(\Omega_1, \mathfrak{A}_1)$ to $(\mathbb{R}^d,\mathcal{B}(\mathbb{R})^d)$ such that

$$P^{X,Y}=P^Y\otimes Q$$

and $Q$ is (a version of) the conditional distribution of $X$ provided $Y$, i.e.

$$Q(y,-)=P^X(-|Y=y)$$
=-- 

This theorem says that that $Q$ (more precisely $y\mapsto Q(y,-)$) fits in the diagram

$$\array{
(\Omega_1,\mathfrak{A}_1,P)&
\stackrel{Y}{\to}&
(\Omega_2,\mathfrak{A}_2, P^Y)
\\
\downarrow^X&&
\swarrow^{Q}
\\
(\mathbb{R},\mathcal{B}(\mathbb{R}),\lambda)
}$$

and $E[X|Y]=Q$.

#### Discrete case

In the discrete case, i.e. if $\Omega_1$ and $\Omega_2$ are finite- or enumerable sets, it is possible to reconstruct $Q$ by just considering one-element sets in $\mathfrak{A}_2$ and the related probabilities

$$p_{ij}:= Q(i,\{j\})$$

called *transition probabilities* encoding $Q$ assemble to a (perhaps countably infinite) matrix $M$ called *transition matrix of $Q$ resp. of $\overline{Q}$*. Note that $p_{ij}$ is the probability of the transition of the *state* (aka. *elementary event* or *one-element event*) $i$ to the *event* $\{j\}$ (which in this case happens to have only one element, too). We have $\sum_i p_{ij}=1$ forall $i\in \Omega_1$.

If $\rho:=(p_i)_{i\in \Omega_1}$ is a counting density on $\Omega_1$, then

$$pM=(\sum_{i\in \Omega} p_i p_{ij})_{j\in \Omega_2}$$

is a counting density on $\Omega_2$.

The conditional expectation plays a defining role in the theory of *martingales* which are *stochastic processes* such that the conditional expectation of the next value (provided the previous values) equals the present realized value.

### Stochastic processes

The terminology of *stochastic processes* is a special interpretation of some aspects of [[infinitary combinatorics]] in terms of [[probability theory]].

Let $I$ be a [[total order]] (i.e. transitive, antisymmetric, and total).

A *stochastic process* is a diagram $X_I: I\to \mathcal{R}$ where $\mathcal{R}$ is the class of random variables such that $X_I(i)=:X_i:(\Omega_i, \mathfrak{F}_i, P_i)\to (S_i, \mathfrak{S}_i)$ is a random variable. Often one considers the case where all $(S_i, \mathfrak{S}_i)=(S, \mathfrak{S})$ are equal; in this case $S$ is called *state space of the process $X_I$*.

If all $\Omega_i=\Omega$ are equal and the class of $\sigma$-algebras $(\mathfrak{A}_i)_{i\in I}$ is *filtered* i.e.

$$\mathfrak{F}_i\subseteq \mathfrak{F}_j\;;iff\;; i\le j$$

and all $X_l$ are $\mathfrak{F}_l$ measurable, the process is called *adapted process*. 

For example the *natural filtration* where $\mathfrak{F}_i=\sigma(\{X^{-1}_l(A), l\le i, A\in \mathfrak{S}\})$ gives an adapted process.

In terms of a diagram we have for $i\le j$

$$\array{
(\Omega_j,\mathfrak{A}_j,P_j)&
\stackrel{f}{\to}&
(\Omega_i,\mathfrak{A}_i,P_i)
\\
\downarrow^{X_j}&&
\swarrow^{\omega_i\mapsto Q(\omega_i,-)}
\\
(\mathbb{R},\mathcal{B}(\mathbb{R}),\lambda)
}$$

and $\overline{Q}:(\Omega_i,\mathfrak{A}_i,P_i)\to(\Omega_j,\mathfrak{A}_j,P_j)$ where $Q:\Omega_i\times\mathfrak{A}_j\to [0,1]$ is the transition probability for the passage from state $i$ to state $j$.

### Martingale

An adapted stochastic process with the natural filtration in discrete time is called a *martingale* if all $E[X_i]\lt \infty$ and $\forall i\le j, E[X_j|\mathfrak{A}_i]=X_i$.

$$\array{
(\Omega_j,\mathfrak{A}_j,P_j)&
\stackrel{f}{\to}&
(\Omega_i,\mathfrak{A}_i,P_i)
\\
\downarrow^{X_j}&&
\swarrow^{E[X_j|\mathfrak{A}_i]=X_i}
\\
(\mathbb{R},\mathcal{B}(\mathbb{R}),\lambda)
}$$
[[martingale]]

(...)

### Markow Process

An adapted stochastic process satisfying

$$P(X_t|\mathfrak{A}_s)=P(X_t|X_s)\;;\forall s\le t$$

is called a *Markow process*.

## Chapman-Kolmogorow Equation

For a Markow process the Chapman-Kolmogorow equation encodes the statement that the transition probabilities of the process form a [[semigroup]].

If in the notation from above $(P_t:\Omega\times\mathfrak{A}\to [0,1])_t$ is a family of stochastic kernels $(\Omega,\mathfrak{A})\to(\Omega,\mathfrak{A})$ such that all $P_t(\omega,-):\mathfrak{A}\to [0,1]$ are probabilities, then $(P_t)_t$ is called *transition semigroup* if

$$\overline P_t (P_s(\omega,A))=P_{s+t} (\omega, A)$$

where

$$\overline P_t: P_s(\omega,-)\mapsto (A\mapsto\int_\Omega P_t (y,A) P_s(\omega,-)(d_y))$$


## In quantum probability theory
 {#InQuantumProbability}

In the dual algebraic formulation of [[probability theory]] known as _[[noncommutative probability theory]]_ or _[[quantum probability theory]]_, where the concept of _[[expectation value]]_ is primitive (while that of the corresponding [[probability space]] (if it exists) is a derived concept), the concept of conditional expection appears as follows (e.g. [Redei-Summers 06, section 7.3](#RedeiSummers06)):


Let $(\mathcal{A},\langle -\rangle)$ be a [[quantum probability space]], hence a [[complex numbers|complex]] [[star algebra]] $\mathcal{A}$ of [[quantum observables]], and a [[state on a star-algebra]] $\langle -\rangle \;\colon\; \mathcal{A} \to \mathbb{C}$.

This means that for $A \in \mathcal{A}$ any [[observable]], its _[[expectation value]]_ in the given [[state on a star-algebra|state]] is 

$$
  \mathbb{E}(A) \;\coloneqq\;  \langle A \rangle \in \mathbb{C}
  \,.
$$

More generally, if $P \in \mathcal{A}$ is a [[real part|real]] [[idempotent]]/[[projector]]

$$
  \label{RealIdempotent}
  P^\ast = P
  \,,
  \phantom{AAA}
  P P = P
$$

thought of as an event, then for any observable $A \in \mathcal{A}$ the [[conditional expectation value]] of $A$, conditioned on the observation of $P$, is 

$$
  \label{ConditionalExpectation}
  \mathbb{E}(A \vert P)
  \;\coloneqq\;
  \frac{
    \left \langle P A P \right\rangle
  }{
    \left\langle P \right\rangle
  }
  \,.
$$


## Related concepts

* [[Bayesian reasoning]]

* [[wavefunction collapse]]

## References

See also

* Wikipedia, _[Conditional expectation](https://en.wikipedia.org
/wiki/Conditional_expectation)_

Discussion form the point of view of [[quantum probability]] is in

* {#RedeiSummers06} [[Miklos Redei]], [[Stephen Summers]], section 7.3 of _Quantum Probability Theory_ ([arXiv:quant-ph/0601158](https://arxiv.org/abs/quant-ph/0601158))


[[!redirects conditional probability]]
[[!redirects conditional probabilities]]

[[!redirects conditional expectation value]]
[[!redirects conditional expectation values]]

