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

In [[probability theory]], the *empirical distribution* is the [[probability distribution]] formed by taking empirical frequencies of a phenomenon, and dividing by the total number of cases. 

For example, if we flip a coin 5 times, the empirical frequency is the probability distribution on the space $\{heads, tails\}$ given by 
$$
p(heads) \;=\; \frac{\# heads}{5}, \qquad p(tails) \;=\; \frac{\# tails}{5} .
$$
For instance, if we have obtained "heads" 3 times and "tails" 2 times, we have 
$$
p(heads) \;=\; \frac{3}{5} \;=\; 0.6, \qquad p(tails) \;=\; \frac{2}{5} \;=\; 0.4.
$$

The name *empirical distribution* denotes both the distribution obtained by sampling a finite amount of data, as well as the limit (when it exists) resulting from an infinite sequence of observations, usually generated from a [[stochastic process]]. 

In [[statistics]] it is used as an [[estimator]] of the distribution of a [[random variable]] whenever it is possible to take [[iid samples]].


## In measure-theoretic probability

Let $X$ be a [[measurable space]]. 
For each $x\in X$, denote by $\delta_x$ the [[Dirac delta]] distribution given by 
$$
\delta_x(A) \;=\; 1_A(x) \;=\; \begin{cases}
1 & x\in A ; \\
0 & x\notin A 
\end{cases}
$$
for all [[measurable subset|measurable]] $A\subseteq X$.

Let now $N$ be a finite set. We can view the product space $X^N$ as the space of finite sequences $(x_1,\dots,x_n)$. 
The **empirical distribution** of a finite sequence $(x_1,\dots,x_n)\in X^N$ is the [[probability measure]] on $X$ given by 
$$
\frac{\delta_{x_1}+\dots+\delta_{x_n}}{n} ,
$$
meaning that it assigns to each measurable $A\subseteq X$ the value
$$
\frac{1_A(x_1)+\dots+1_A(x_n)}{n} \;=\; \frac{\#\{x_i in A\}}{n} .
$$

Similarly, we can view the countable product $X^\mathbb{N}$ as the space of infinite sequences $(x_1,x_2,x_3\dots)$ of elements of $X$. The **empirical distribution** of a sequence $(x_1,x_2,x_3,\dots)\in X^\mathbb{N}$ is the probability measure on $X$ given by the limit, if it exists,
$$
\lim_{n\to\infty} \frac{1}{n} \sum_{i=1}^n \delta_{x_i} .
$$

If the $x_i$ are [[random variables]], and so they form a [[stochastic process]] (for example, if they are coin flips), the empirical distribution, if it exists, is a random variable as well.


## In categorical probability

(...)


## Properties

* The [[Glivenko-Cantelli theorem]] says that, under some conditions, the limiting empirical distribution of an [[iid process]] equals the generating distribution of the process.
* [[De Finetti's theorem]] says equivalently that [[exchangeable]] random variables are [[conditionally independent]] given their empirical distribution.


## See also

* [[probability theory]], [[categorical probability]]
* [[random variable]], [[expectation value]]
* [[probability monad]], [[Giry monad]], [[convex space]]
* [[law of large numbers]], [[empirical mean]], [[Glivenko-Cantelli theorem]]
* [[ergodic theorem]]
* [[central limit theorem]]


category: probability


[[!redirects empirical distributions]]