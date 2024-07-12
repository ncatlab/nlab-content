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

One of the main purposes of [[probability theory]], and of related fields such as [[statistics]] and [[information theory]], is to *make predictions in situations of uncertainty*.

Suppose that we are interested a quantity $X$, whose value we don't know exactly (for example, a [[random variable]]), and which we cannot observe directly. 
Suppose that we have another quantity, $Y$, which we also don't know exactly, but which we can observe (for example, through an [[experiment]]). 
We might now wonder: *can observing $Y$ give us information about $X$, and reduce its uncertainty?*
Viewing the unknown quantities $X$ and $Y$ as having hidden knowledge or hidden [[information]], one might ask, *how much of this hidden information is shared between $X$ and $Y$*, so that observing $Y$ uncovers information about $X$ as well? 

This form of dependence between $X$ and $Y$ is called *stochastic dependence*, and is one of the most important concepts both in [[probability theory]], and, due to its conceptual nature, in most [[categorical approaches to probability theory]].


## Intuition

### Dependence and independence

(...)

### Conditional dependence and independence

(...)


## In measure-theoretic probability

Let $(\Omega,\mathcal{F},p)$ be a [[probability space]], and let $A,B\in\mathcal{F}$ be [[events]], i.e. measurable subsets of $\Omega$. 
We say that $A$ and $B$ are **independent** if and only if 
$$
p(A\cap B) = p(A)\,p(B) ,
$$
i.e. if *the [[joint probability]] is the product of the probabilities*.

More generally, if $f:(\Omega,\mathcal{F})\to(X,\mathcal{A})$ and $g:(\Omega,\mathcal{F})\to(Y,\mathcal{B})$ are [[random variables]] or [[random elements]], one says that $f$ and $g$ are **independent** if and only if all the events they induce are independent, i.e. for every $A\in\mathcal{A}$ and $B\in\mathcal{B}$, 
$$
p\big(f^{-1}(A)\cap g^{-1}(B)\big) = p\big(f^{-1}(A)\big)\,p\big(g^{-1}(B)\big) .
$$

Equivalently, one can form the [[joint distribution|joint random variable]] $(f,g):(\Omega,\mathcal{F})\to(X\times Y,\mathcal{A}\otimes\mathcal{B})$ and form the [[joint distribution]] $q=(f,g)_*p$ on $X\times Y$. 
We have that $f$ and $g$ are independent as random variables if and only if for every $A\in\mathcal{A}$ and $B\in\mathcal{B}$, 
$$
q\big(\pi_1^{-1}(A)\cap \pi_2^{-1}(B)\big) = q\big(\pi_1^{-1}(A)\big)\,q\big(\pi_2^{-1}(B)\big) .
$$ 
If we denote the [[marginal distributions]] of $q$ by $q_X$ and $q_Y$, the independence condition reads
$$
q(A \times B) = q_X(A)\,q_Y(B) ,
$$
meaning that the joint distribution $q$ is the product of its marginals.


(...)

### In terms of the Giry monad

(...)

### In the category of Markov kernels

(...)


## In Markov categories

(For now see [[Markov category#stochastic_independence|Markov category - Stochastic independence]])


## In dagger categories

(...)


## See also 

* [[probability theory]], [[categorical probability]]
* [[joint and marginal probability]]
* [[Kolmogorov extension theorem]]
* [[probability monad]], [[Giry monad]]
* [[Markov category]], [[Markov kernel]]


## References

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* [[Alex Simpson]], *Equivalence and Conditional Independence in Atomic Sheaf Logic* ([arXiv:2405.11073](https://arxiv.org/abs/2405.11073))

category: probability

[[!redirects stochastic dependence]]
[[!redirects stochastic independence]]
[[!redirects statistical dependence]]
[[!redirects statistical independence]]
[[!redirects conditional dependence and independence]]
[[!redirects conditional dependence]]
[[!redirects conditional independence]]
[[!redirects stochastic interaction]]
[[!redirects stochastic interactions]]
[[!redirects statistical interaction]]
[[!redirects statistical interactions]]
[[!redirects stochastically dependent]]
[[!redirects stochastically independent]]
[[!redirects statistically dependent]]
[[!redirects statistically independent]]
[[!redirects conditionally dependent]]
[[!redirects conditionally independent]]
[[!redirects independent events]]
[[!redirects independent random variables]]