+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
#### $(0,1)$-Category theory
+-- {: .hide}
[[!include (0,1)-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The Kantorovich monad is a [[probability monad]] on the category of [[complete metric spaces]] and 1-Lipschitz (or [[Lipschitz map|Lipschitz]]) maps. 
Its functor part assigns to each complete metric space $X$ the space of [[Radon measure|Radon]] [[probability measures]] with finite first moment, equipped with the [[Kantorovich-Wasserstein distance]]. 

Its [[algebra over a monad|algebras]] are [[closed set|closed]] [[convex set|convex]] subsets of [[Banach spaces]].

The construction was first given by van Breugel for the compact case (see [vB '05](#vanbreugel)). 

There is an [[order theory|ordered]] version of the Kantorovich monad, making use of the [[stochastic order]]. Its [[algebra over a monad|algebras]] are [[closed set|closed]] [[convex set|convex]] subsets of [[ordered Banach spaces]].


## Wasserstein spaces

Let $X$ be a [[metric space]]. A [[probability measure]] on $X$ has **finite first moment** if 
$$
\int_{X\times X} d(x,y) \, dp(x)\,dp(y) \;\lt\; +\infty,
$$
where $d(-,-)$ denotes the [[distance]]. 

Let $p$ and $q$ be  [[Radon measure|Radon]] [[probability measures]] on $X$ of finite first moment. The **[[Kantorovich-Wasserstein distance]]** is given by
$$
d(p,q) \;\coloneqq\; \inf_{r\in\Gamma(p,q)} \int_{X\times X} d(x,y) \,dr(x,y) ,
$$
where the infimum (which is attained if $X$ is complete) is taken over the set $\Gamma(p,q)$ of [[joint measure|couplings]] of $p$ and $q$, i.e. the measures on $X\times X$ which admit $p$ and $q$ as their [[marginal measure|marginals]]. 

Equivalently, the distance can be written as
$$
d(p,q) \;=\; \sup_{f\in[X,\mathbb{R}]} \int f\, dp - \int f\, dq,
$$
where the supremum (which is usually not attained) is taken over the set of 1-[[Lipschitz map|Lipschitz]] functions $X\to \mathbb{R}$.
(This equivalence is an instance of the celebrated [[Kantorovich duality]].)

The **1-Wasserstein space** over $X$ is the space $P X$ of Radon probability measures on $X$ with finite first moment, equipped with the Wasserstein metric.

### Properties

* If $X$ is [[complete metric space|complete]], so is $P X$.

* If $X$ is [[separable space|separable]], so if $P X$.

* If $X$ is [[compact]], so is $P X$.

More information on Wasserstein spaces can be found in [Villani '08](#villani).

## Functor, unit and multiplication

As it is customary for [[probability monads]], the functor assigns to a [[morphism]] $f:X\to Y$ (in this case, a [[Lipschitz map|Lipschitz]] or 1-Lipschitz map) the map $P f: P X \to P Y$ induced by the [[pushforward of measures]]. 
The pushforward of a Radon probability measure of finite first moment along a Lipschitz map is again Radon and of finite first moment. Moreover, the resulting map $P f$ is again Lipschitz, with the same Lipschitz constant as $f$. Therefore we have an endofunctor $P$ on the category of [[complete metric spaces]] and [[Lipschitz maps]] (or 1-Lipschitz). 

Again, as it happens in general with [[probability monads]], the unit $\delta:X\to P X$ is given by forming the [[Dirac measures]] and the multiplication $E:P P X\to P X$ is given by [[integration]]. More formally, given $\xi\in P P X$, the measure $E \xi\in PX$ is defined as the one which assigns to a [[Borel set]] $A\subseteq X$ the number
$$
E \xi(A) \;\coloneqq\; \int p(A) \,d\xi(p) .
$$

The maps $\delta$ and $E$ satisfy the usual [[axioms]] of a [[monad]] (see [F-P '19](#kantorovich19)), which is known as the **Kantorovich monad**.

## Algebras

As it is the case for most [[probability monad]], the algebras are [[convex spaces]] of a particular kind. For the Kantorovich monad, the objects of the underlying category are complete metric spaces, and so the [[closed set|closed]] [[convex set|convex]] subsets of [[Banach spaces]] are an ideal candidate: they are [[metric spaces]], they are [[complete metric space|complete]], and they have a well-defined [[convex space|convex combination operation]]. 
It turns out that this is exactly the case. 

More in detail, every closed convex subset $A$ of a Banach space comes equipped with a map $e:P A\to A$ given by vector-valued [[integration]],
$$
p\;\mapsto\; \int a \,dp(a) .
$$
The integral exists since $p$ has finite first moment.
Conversely, it can be proven that every $P$-algebra is of this form. 

The [[Eilenberg-Moore category|morphisms of algebras]] are maps between algebras $f:A\to B$ which commute with the integration map. It can be shown that equivalently these are exactly the **affine** maps, i.e.~those maps which satisfy
$$
f\big(\lambda\,x + (1-\lambda)\,y\big) \;=\; \lambda\,f(x) + (1-\lambda)\,f(y).
$$

For more details, see [F-P '19](#kantorovich19).

## Duality

(...)

## The ordered case

(Work in progress. For now see [F-P '18](#orderedkantorovich).) 

## For Lawvere metric spaces

(...)

## See also

* [[monads of probability, measures, and valuations]]

* [[Giry monad]], [[Radon monad]], [[extended probabilistic powerdomain]]

* [[Kantorovich-Wasserstein distance]], [[optimal transport]]

* [[metric space]], [[complete metric space]]

* [[Banach space]], [[ordered Banach space]], [[convex space]]


## References

* {#vanbreugel} Franck van Breugel, _The metric monad for probabilistic nondeterminism_, unpublished, 2005. ([pdf](http://www.cse.yorku.ca/~franck/research/drafts/monad.pdf))

* {#kantorovich19} [[Tobias Fritz]] and [[Paolo Perrone]], _A probability monad as the colimit of spaces of finite samples_, Theory and Applications of Categories 34, 2019. ([pdf](http://www.tac.mta.ca/tac/volumes/34/7/34-07.pdf))

* {#orderedkantorovich} [[Tobias Fritz]] and [[Paolo Perrone]], _Stochastic order on metric spaces and the ordered Kantorovich monad_, Advances in Mathematics 366, 2020. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))

* {#villani} [[Cedric Villani]], _Optimal transport: old and new_, Springer, 2008.

* {#behavioral} Paolo Baldan, Filippo Bonchi, Henning Kerstan and Barbara König, _Coalgebraic behavioral metrics_, Logical Methods in Computer Science 14(3), 2018. ([doi: 10.23638/LMCS-14(3:20)2018](https:doi.org/10.23638/LMCS-14%283:20%292018)) 