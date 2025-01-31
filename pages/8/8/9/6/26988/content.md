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

In [[probability theory]], the *empirical mean* or *empirical average* is the [[average]] value of a quantity, with weights given by empirical frequencies.

For example, if we roll a die 3 times, and we obtain first $2$, then $3$, then $5$, the empirical mean is
$$
\frac{2+3+5}{3} \;=\; \frac{10}{3} \;\approx\; 3.33 .
$$

The name *empirical mean* denotes both the quantity obtained by sampling a finite amount of data, as well as the limit (when it exists) resulting from an infinite sequence of observations, usually generated from a [[stochastic process]]. 

In [[statistics]] it is used as an [[estimator]] of the [[expectation value]] of a [[random variable]] whenever it is possible to take [[iid samples]].


## In measure-theoretic probability

Let $N$ be a finite set. We can view the product space $\mathbb{R}^N$ as the space of finite sequences $(x_1,\dots,x_n)$ of real numbers. 
The **empirical mean** of a finite sequence $(x_1,\dots,x_n)\in \mathbb{R}^N$ is the average
$$
\frac{x_1+\dots+x_n}{n} .
$$

Similarly, we can view the countable product $\mathbb{R}^\mathbb{N}$ as the space of infinite sequences $(x_1,x_2,x_3\dots)$ of real numbers. The **empirical mean** of a sequence $(x_1,x_2,x_3,\dots)\in \mathbb{R}^\mathbb{N}$ is the limit, if it exists,
$$
\lim_{n\to\infty} \frac{1}{n} \sum_{i=1}^n x_i .
$$

If the $x_i$ are [[random variables]], and so they form a [[stochastic process]] (for example, if they are coin flips), the empirical distribution, if it exists, is a random variable as well.


## In categorical probability

(...)


## Properties

* The [[law of large numbers]] says that, under some conditions, the limiting empirical mean of an [[iid process]] equals the [[expectation value]] of the process.

* More generally, the [[ergodic theorem]] says that, under some conditions, the limiting empirical mean of a [[random variable]] on a [[stationary process]] (for example an [[ergodic process]]) equals its [[conditional expectation]] with respect to the [[invariant sigma-algebra]].


## See also 

* [[probability theory]], [[categorical probability]]
* [[random variable]], [[expectation value]]
* [[empirical distribution]], [[law of large numbers]]


## References

(...)


category: probability


[[!redirects empirical means]]
[[!redirects empirical average]]
[[!redirects empirical averages]]