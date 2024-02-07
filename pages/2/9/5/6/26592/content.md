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
One says that [[stochastic dependence and independence|the probability of a product is not the product of the probabilities]].
The term on the left is called the *joint probability* (the probability that the events $A$ and $B$ happen *jointly*) and the terms on the right are called *marginal probabilities* (the probabilities that $A$ and $B$ happen *separately*.)
In general, the joint probability has more information than the marginal probabilities alone, because of the presence of [[correlation]] or other [[stochastic interactions]].

From the [[category-theoretic approaches to probability theory|category-theoretic perspective]], one can encode this idea using the following (related) concepts:

* A [[monoidal category|monoidal structure]] on a [[category of kernels]] or [[Markov category]] which is [[semicartesian monoidal category|semicartesian]], but not [[cartesian monoidal category|cartesian]], i.e. for which the tensor product is not a [[product|categorical product]];

or 

* A [[probability monad]] which is [[affine]] but not [[strong monoidal functor|strong monoidal]], i.e. which does not preserve [[products]].

When one takes as [[Markov category]] the [[Kleisli category]] of a [[probability monad]], the two concepts coincide.



## In measure-theoretic probability

(...)

### In terms of the Giry monad

(...)

### In the category of Markov kernels

(...)


## In Markov categories

(...)

## See also 

* [[stochastic dependence and independence]]
* [[probability theory]], [[categorical probability]]
* [[probability monad]], [[Giry monad]]
* [[Markov category]], [[Markov kernel]]
* [[infinitary tensor product]], [[Kolmogorov extension theorem]]


## References

* {#bimonoidal_monads} [[Tobias Fritz]], [[Paolo Perrone]], _Bimonoidal Structure of Probability Monads_, Proceedings of MFPS, 2018, ([arXiv:1804.03527](https://arxiv.org/abs/1804.03527))

* {#Perrone_thesis} [[Paolo Perrone]], _Categorical Probability and Stochastic Dominance in Metric Spaces_, ([thesis](http://www.paoloperrone.org/phdthesis.pdf))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))


category: probability

[[!redirects joints and marginal distribution]]
[[!redirects joints and marginals]]
[[!redirects joint distribution]]
[[!redirects marginal distribution]]
[[!redirects product probability]]
[[!redirects product probability distribution]]
[[!redirects product distribution]]