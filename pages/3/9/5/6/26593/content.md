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

(...)


## Intuition

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
[[!redirects independent events]]