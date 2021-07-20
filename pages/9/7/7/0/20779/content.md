
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

A Dirac measure is a [[measure]] whose (unit) mass is concentrated on a single [[point]] $x$ of a [[space]] $X$. 

From the point of view of [[probability theory]], a Dirac measure can be seen as the [[law of a random variable|law]] of a [[deterministic random variable]], or more generally one which is [[almost surely]] equal to a point $x$.

See also [[Dirac distribution]] for the analogous concept in the language of [[distributions]].


## Definition

### For measurable spaces

Let $X$ be a [[measurable space]]. Given $x\in X$, the **Dirac measure** $\delta_x$ at $x$ is the [[measure]] defined by
$$
\delta_x(A) \;\coloneqq\; 
\begin{cases}
1 & x\in A \\
0 & x\notin A
\end{cases}
$$
for each [[measurable set]] $A\subseteq X$. 

### For topological spaces

If $X$ is a [[topological space]], the Dirac measure at $x$ can be also defined as the unique [[Borel measure]] $\delta_x$ which satisfies 
$$
\delta_x(U) \;\coloneqq\; 
\begin{cases}
1 & x\in U \\
0 & x\notin U
\end{cases}
$$
for each [[open set]] $U\subseteq X$. 

Equivalently, it is the [[continuous valuation#extending_valuations_to_measures|extension to a measure]] of the [[continuous valuation#dirac_valuations|Dirac valuations]].

### For locales

(...)

(See also [[correspondence between measure and valuation theory]].)

## Properties

* On [[topological spaces]], Dirac measures are [[Radon measure|Radon]] and [[τ-additive]].

* Every [[continuous valuation#dirac_valuations|Dirac valuation]] on a topological space can be [[continuous valuation#extending_valuations_to_measures|extended]] to a Dirac measure.

* On a [[topological space]] $X$, the [[support]] of the Dirac measure at $x\in X$ is equal to the [[closure]] of $x$. On [[T1]] spaces, this is just the [[singleton]] $\{x\}$. 

* The [[pushforward measure]] of a Dirac measure along a [[measurable function]] is again a Dirac measure. This is related to [[natural transformation|naturality]] of the unit map of [[probability and measure monads]].

* Given a Dirac measure $\delta_x$ on a [[measurable space]] $X$ and any [[measure]] $\mu$ on any measurable space $Y$, the [[product measure]] $\delta_x\otimes \mu$ is the unique [[coupling]] of $\delta_x$ and $\mu$. 

* The coupling above defines a map $X\times P Y\to P(X\times Y)$ which gives the [[strong monad|strength]] of most [[probability and measure monads]].

## Significance

* The Dirac measures (and the [[continuous valuation#Dirac valuations|Dirac valuations]]) give the unit of all [[probability and measure monads]]. 

* The probabilistic interpretation is that the Dirac measures are exactly those of [[deterministic]] elements (or almost deterministic), i.e. which are "not truly random".

* In terms of [[random variables]], and somewhat conversely, a [[random element]] of $X$ has the Dirac measure $\delta_x$ as [[law of a random variable|law]] if and only if it is [[almost surely]] equal to $x$. 

## See also 

* [[Dirac distribution]]

* [[monads of probability, measures, and valuations]]

* [[measure]], [[Radon measure]], [[τ-additive measure]], [[continuous valuation]]


[[!redirects Dirac measures]]

[[!redirects Dirac delta measure]]
[[!redirects Dirac delta measures]]

[[!redirects delta measure]]
[[!redirects delta measures]]

[[!redirects point measure]]
[[!redirects point measures]]

[[!redirects point mass measure]]
[[!redirects point mass measures]]
