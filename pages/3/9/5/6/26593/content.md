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

Very roughly, two unknown quantities are **stochastically independent** when learning the value of one of them does not change what one should expect about the other.

For instance, suppose that $X$ and $Y$ are random variables. If observing $Y$ changes the distribution one assigns to $X$, then $X$ and $Y$ are stochastically dependent. If observing $Y$ does not change the distribution of $X$, then $X$ and $Y$ are stochastically independent.

For a concrete example, let $X$ be the result of throwing one die, and let $Y$ be the result of throwing another die. If the dice are thrown separately and do not influence each other, then learning the value of $Y$ does not change the probabilities assigned to $X$. If we learn that $Y=6$, the probability that $X=6$ is still $1/6$. Thus $X$ and $Y$ are independent.

By contrast, let $X$ be the result of throwing a die, and let $Y$ be the event that the result is even. Then $X$ and $Y$ are dependent: learning that $Y$ has occurred changes the possible values of $X$ from
$$
\{1,2,3,4,5,6\}
$$
to
$$
\{2,4,6\}.
$$
Thus observing $Y$ gives information about $X$.

A more geometric example is given by choosing a point uniformly at random in the unit disk, and letting $X$ and $Y$ be its two coordinates. Each coordinate separately has a symmetric distribution, but the two coordinates are not independent: if $X$ is close to $1$, then $Y$ must be close to $0$. The dependence is not caused by either coordinate determining the other exactly, but by the joint constraint
$$
X^2+Y^2\leq 1.
$$


### Conditional dependence and independence

Often one is interested not in whether two quantities are independent absolutely, but whether they are independent **relative to some background information**.

A standard example is the following. Let $Z$ say whether it is raining, let $X$ say whether the grass in Alice's garden is wet, and let $Y$ say whether the grass in Bob's garden is wet. Marginally, $X$ and $Y$ are dependent: if Alice's grass is wet, this is evidence that it is raining, and hence evidence that Bob's grass is wet. But after conditioning on whether it is raining, the remaining dependence may disappear. In that case $X$ and $Y$ are conditionally independent given $Z$.

Thus conditional independence does not mean that $X$ and $Y$ are independent in the usual sense. Rather, it means that their dependence is *completely mediated* by the conditioning variable $Z$.

Conversely, conditioning can also create dependence. For example, suppose that two independent causes $X$ and $Y$ may each lead to a common effect $Z$. If one conditions on the effect $Z$ having occurred, then learning that $X$ occurred can make $Y$ less likely, since the effect has already been explained by $X$. This phenomenon is sometimes called [[explaining away]]. Thus conditional independence and ordinary independence are logically distinct notions.


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
meaning that the joint distribution $q$ is the product of its marginals:
$$
q = q_X \otimes q_Y .
$$


In this form, stochastic dependence is the obstruction to reconstructing the joint law from its two marginals. The marginal laws $q_X$ and $q_Y$ describe the two random quantities separately, while the joint law $q$ contains in addition their possible dependence structure.

For a finite family of random variables
$$
f_i:(\Omega,\mathcal{F})\to(X_i,\mathcal{A}_i),
\qquad i=1,\ldots,n,
$$
mutual independence means that the joint distribution factors as the product of its marginals:
$$
(f_1,\ldots,f_n)_*p
=
(f_1)_*p\otimes\cdots\otimes(f_n)_*p .
$$

Equivalently, for all measurable subsets $A_i\in\mathcal{A}_i$,
$$
p\big(f_1^{-1}(A_1)\cap\cdots\cap f_n^{-1}(A_n)\big)
=
\prod_{i=1}^n p\big(f_i^{-1}(A_i)\big).
$$

The infinitary equivalent can be obtained by means of the [[Kolmogorov extension theorem]].


### Conditional independence

Let $\mathcal{G}\subseteq\mathcal{F}$ be a sub-$\sigma$-algebra, thought of as encoding some background information. Events $A,B\in\mathcal{F}$ are **conditionally independent given $\mathcal{G}$** if
$$
p(A\cap B\mid\mathcal{G})
=
p(A\mid\mathcal{G})\,p(B\mid\mathcal{G})
$$
[[almost surely]].

More generally, random elements $f:(\Omega,\mathcal{F})\to(X,\mathcal{A})$ and $g:(\Omega,\mathcal{F})\to(Y,\mathcal{B})$ are **conditionally independent given $\mathcal{G}$** if, for all $A\in\mathcal{A}$ and $B\in\mathcal{B}$,
$$
p\big(f^{-1}(A)\cap g^{-1}(B)\mid\mathcal{G}\big)
=
p\big(f^{-1}(A)\mid\mathcal{G}\big)\,
p\big(g^{-1}(B)\mid\mathcal{G}\big)
$$
almost surely.

If $h:(\Omega,\mathcal{F})\to(Z,\mathcal{C})$ is another random element, one says that $f$ and $g$ are conditionally independent given $h$ if they are conditionally independent given the sub-$\sigma$-algebra generated by $h$:
$$
\sigma(h)\subseteq\mathcal{F}.
$$
This is often written
$$
f \perp g \mid h .
$$

When [[regular conditional probabilities]] exist, conditional independence can be expressed by saying that the conditional joint law of $(f,g)$ over $h=z$ factors as the product of the corresponding conditional marginal laws:
$$
p_{f,g\mid h=z}
=
p_{f\mid h=z}\otimes p_{g\mid h=z}
$$
for $p_h$-almost every $z$.

Equivalently, the joint law of $(f,g,h)$ admits the factorization
$$
p_{f,g,h}(dx,dy,dz)
=
p_h(dz)\,p_{f\mid h=z}(dx)\,p_{g\mid h=z}(dy).
$$


### In terms of the Giry monad

Denote by $G$ the [[Giry monad]] on [[Meas]], sending a measurable space $X$ to the measurable space $G(X)$ of probability measures on $X$.

The coordinate projections
$$
\pi_X:X\times Y\to X,
\qquad
\pi_Y:X\times Y\to Y
$$
induce maps
$$
G(\pi_X):G(X\times Y)\to G(X),
\qquad
G(\pi_Y):G(X\times Y)\to G(Y),
$$
and hence the marginals
$$
q_X = G(\pi_X)\circ q,
\qquad
q_Y = G(\pi_Y)\circ q .
$$

The Giry monad is compatible with products by the usual product-measure construction: there is a natural map
$$
G(X)\times G(Y)\longrightarrow G(X\times Y),
\qquad
(\mu,\nu)\to \mu\otimes\nu .
$$

In these terms, a joint distribution $q:1\to G(X\times Y)$ is independent precisely if it is obtained from its marginals by this product-measure map: $q = q_X\otimes q_Y$.

Equivalently, if random elements $f:\Omega\to X$, $g:\Omega\to Y$ are defined on a probability space $(\Omega,\mathcal{F},p)$, then $f$ and $g$ are independent precisely when
$$
(f,g)_*p = f_*p\otimes g_*p .
$$

Thus, from the point of view of the Giry monad, stochastic dependence is exactly the failure of a state of the product object $X\times Y$ to be the product of its marginal states.

#### Higher arities

More generally, for a finite family of measurable spaces $X_1,\ldots,X_n$, there is a product-measure map
$$
G(X_1)\times\cdots\times G(X_n)
\longrightarrow
G(X_1\times\cdots\times X_n),
\qquad
(\mu_1,\ldots,\mu_n)\to
\mu_1\otimes\cdots\otimes\mu_n .
$$
A joint distribution
$$
q:1\to G(X_1\times\cdots\times X_n)
$$
is independent precisely if it is obtained from its marginals by this map:
$$
q=q_1\otimes\cdots\otimes q_n .
$$

#### Infinite families

For an infinite family $(X_i)_{i\in I}$, the corresponding statement is subtler. One would like to say that an independent joint distribution on
$$
\prod_{i\in I}X_i
$$
is determined by its finite-dimensional marginals
$$
q_J\in G\left(\prod_{j\in J}X_j\right),
\qquad
J\subseteq I \text{ finite},
$$
and that these finite-dimensional marginals factor as
$$
q_J=\bigotimes_{j\in J}q_j .
$$

The existence of a measure on the infinite product with these prescribed finite-dimensional marginals is the content of the [[Kolmogorov extension theorem]], under suitable hypotheses on the measurable spaces. Thus, for infinite families, independence is naturally formulated in terms of compatible finite-dimensional product distributions.

In particular, a family of random elements
$$
f_i:\Omega\to X_i,
\qquad i\in I,
$$
is independent if every finite subfamily is independent, equivalently if for every finite subset $J\subseteq I$ the joint law of $(f_j)_{j\in J}$ factors as the product of its marginals:
$$
((f_j)_{j\in J})_*p
=
\bigotimes_{j\in J}(f_j)_*p .
$$


### In the category of Markov kernels

(See the analogous section in [[joint and marginal probability#in_the_category_of_markov_kernels|Joint and marginal probability]].)

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