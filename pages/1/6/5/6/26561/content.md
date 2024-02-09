
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

The [[category]] whose [[objects]] are [[measurable spaces]] and whose [[morphisms]] are [[stochastic kernels]] (or [[Markov kernels]]) is often denotes _Stoch_, or similar.

It is the motivating example of a [[Markov category]], and together with its subcategory [[Stoch#borelstoch|BorelStoch]], one of the most important categories of [[categorical probability]].

## Definition

_Stoch_ is the category whose 

* [[Objects]] are [[measurable spaces]], i.e. pairs $(X,\mathcal{A})$ where $X$ is a set and $\mathcal{A}$ is a [[sigma-algebra]] on $X$;
* [[Morphisms]] $(X,\mathcal{A})\to(Y,\mathcal{B})$ are [[Markov kernels]] of entries $k(B|x)$, for $x\in X$ and $B\in\mathcal{B}$;
* The [[identities]] $(X,\mathcal{A})\to(X,\mathcal{A})$ are given by the [[Dirac delta]] kernels
$$
\delta(A|x) = 1_A(x) = \begin{cases}
1 & x\in A ; \\
0 & x\notin A ;
\end{cases}
$$
* The [[composition]] of kernels $k:(X,\mathcal{A})\to(Y,\mathcal{B})$ and $h:(Y,\mathcal{B})\to(Z,\mathcal{C})$ is given by the [[Lebesgue integral]]
$$
(h\circ k) (C|x) = \int_Y h(C|y)\,k(dy|x)
$$
for all $x\in X$ and $C\in\mathcal{C}$.
This is sometimes called _Chapman-Kolmogorov formula_. (Compare with the composition formula for [[stochastic matrices]].)


## As a Kleisli category

_Stoch_ can be equivalently described as the [[Kleisli category]] of the [[Giry monad]] on [[Meas]]. 

(...)


## Notable subcategories

### BorelStoch

_BorelStoch_ is the [[full subcategory]] of _Stoch_ whose objects are [[standard Borel space|standard Borel]] measurable spaces. 
This is particularly important as a [[Markov category]] because it has [[Markov category#conditionals|conditionals]] and countable [[Markov category#kolmogorov_products|Kolmogorov products]].
It is the Kleisli category of the [[Giry monad]] restricted to [[standard Borel spaces]].

As proven [here](#markov_support), in _BorelStoch_ all [[idempotent splitting|idempotents split]], making it a [[Cauchy-complete category]].


### FinStoch

[[FinStoch]] is the [[full subcategory]] of _Stoch_ whose objects are discrete [[finite sets]]. Equivalently, it is the category of finite [[stochastic matrices]].
It is closely related to the Kleisli category of the [[distribution monad]].


## Related concepts

* [[Markov category]]
* [[Markov kernel]]
* [[category of couplings]]
* [[probability monad]]
* [[Giry monad]]
* [[Kleisli category]]
* [[categorical probability]]


## References

* {#Lawvere62} [[Bill Lawvere]], _The category of probabilistic mappings_, ms. 12 pages, 1962 
([[lawvereprobability1962.pdf:file]])

* {#Chentsov65} N. N. Chentsov, _The categories of mathematical statistics_, Dokl. Akad. SSSR 164, 1965.

* {#panangaden_cat_markov} [[Prakash Panangaden]], _The category of Markov kernels_, ENTCS, 1999. ([full text](https://www.sciencedirect.com/science/article/pii/S1571066105806024))

* {#cd_categories} Kenta Cho, [[Bart Jacobs]], _Disintegration and Bayesian Inversion via String Diagrams_, Mathematical Structures of Computer Science 29, 2019. ([arXiv:1709.00322](https://arxiv.org/abs/1709.00322))

* {#fritzmarkov} [[Tobias Fritz]], _A synthetic approach to Markov kernels, conditional independence and theorems on sufficient statistics_, Advances of Mathematics 370, 2020. ([arXiv:1908.07021](http://arxiv.org/abs/1908.07021))

* {#markov_support} Tobias Fritz, Tomáš Gonda, Antonio Lorenzin, Paolo Perrone, Dario Stein, _Absolute continuity, supports and idempotent splitting in categorical probability_, ([arXiv:2308.00651](https://arxiv.org/abs/2308.00651))


category: category, probability

[[!redirects BorelStoch]]
[[!redirects category of kernels]]
[[!redirects category of Markov kernels]]