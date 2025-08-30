+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
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

The Radon monad is a [[measure monad]] on the [[category]] of [[compact Hausdorff spaces]]. 
Its functor assigns to each space $X$ the space of [[Radon measure|Radon]] [[probability measure|probability]] or subprobability [[measures]], equipped with the [[weak topology]].

There is also an [[order theory|ordered]] version of the Radon monad on the category of [[compact ordered spaces]] (see [below](#the_ordered_case)).

## Spaces of Radon measures

Let $X$ be a [[compact Hausdorff space]]. 
Denote by $R X$ the set of those [[Radon measures]] on $X$ which are _subnormalized_, i.e. those measures $\mu$ for which $\mu(X)\le 1$. 
Denote by $P X$ its subset of Radon [[probability measures]].

Equip both sets with the [[weak topology|topology of weak convergence]] with respect to [[continuous functions]]. It is well known that the resulting spaces $R X$ and $P X$ are themselves [[compact Hausdorff spaces]]. 


### In terms of τ-additive measures

Since [[tau-additive measure#relationship_with_other_measuretheoretical_notions|on compact Hausdorff spaces Radon and τ-additive measures coincide]], we can equivalently define $R X$ and $P X$ as the sets of subnormalized and normalized [[τ-additive measures]].

For probability measures, the [[weak topology]] and the [[extended probabilistic powerdomain#the_measure_monad_on_top|A-topology]] coincide, so that $P$ an be extended to the [[extended probabilistic powerdomain#the_probability_monad_on_top|probability monad on Top]].

The same cannot be said for $R$, since the weak topology and the A-topology do not coincide for _subnormalized_ measures: given $\mu\in R X$, the measure $r \mu$ for $0 \le r \le 1$ is in the [[closure]] of $\mu$ for the $A$-topology, while the weak topology is [[Hausdorff]].


### In terms of valuations

Note that, since every [[continuous valuation]] on a [[compact Hausdorff space]] can be [[continuous valuation#extending_valuations_to_measures|extended to a τ-additive measure]], we could equivalently defined the Radon monad as a monad of [[continuous valuations]].

Just as above, for probability measures, the [[weak topology]] and the [[extended probabilistic powerdomain#spaces_of_valuations|pointwise topology of valuations]] coincide, so that $P$ an be extended to a submonad of the [[extended probabilistic powerdomain]] on [[Top]]. Again, the same cannot be said for $R$.

## Functoriality, unit and multiplication

Let $f:X\to Y$ be a [[continuous map]] between [[compact Hausdorff spaces]]. The [[pushforward of measures]] (or equivalently of [[continuous valuation#pushforward|valuations]]) gives a well-defined, continuous map $R X\to R Y$ which restricts to the map $P X \to P Y$. 
This makes $R$ and $P$ [[endofunctors]] of [[Top]].

As it is usual for [[measure monads]], the unit is given by the [[Dirac measures]] and the multiplication is given by [[integration]]. 

More in detail, given a [[compact Hausdorff space]] $X$, we can assign to each $x\in X$ its [[Dirac measure]] (equivalently, [[continuous valuation#dirac_valuations|Dirac valuation]] $\delta_x$. The assignment $\delta:X\to P X$, or $X\to R X$ is continuous, and [[natural transformation|natural]] in $X$.

Just as well, given a measure $\mu\in P P X$, we can define the measure $E\mu\in P X$ as the one assigning to a measurable $A\subseteq X$ the number
$$
E\mu(A) \coloneqq \int_{P X} p(A) \,d\mu(p).
$$
(In terms of valuations, the same is given for [[open sets]] instead of [[measurable sets]].)
Again, the assignment $E: P P X \to P X$ is continuous and [[natural transformation|natural]] in $X$.
The multiplication for $R$ is defined analogously.

The unit and multiplication thus defined satisfy the usual [[axioms]] of a [[monad]].
The monads $R$ and $P$ are both known in the literature as the **Radon monad**. 

The monad $P$ is the restriction to [[compact Hausdorff spaces]] of the [[extended probabilistic powerdomain#the_probability_monad_on_top|probability monad on Top]], which is itself a submonad of the [[extended probabilistic powerdomain]]. (See also [[monads of probability, measures, and valuations]].)


## Algebras 

The [[algebra over a monad|algebras]] of the Radon monad $P$ are [[compact]] [[convex subsets]] of [[locally convex topological vector spaces]]. 

More in detail, a compact convex subset $C$ of a locally convex topological vector space is a [[compact Hausdorff space]], and it admits a canonical $P$-algebra structure $e:P C\to C$ via (vector-valued) [[integration]]:
$$
p \mapsto \int_{C} c \,dp(c) .
$$
Since the space is [[compact]], the integral above is well-defined, and it returns an element of $C$ which we can view as the "center of mass" of $p$. 

Conversely, it can be proven that every $P$-algebra is of this form.

The [[Eilenberg-Moore category|morphisms of algebras]] are the continuous maps between algebras which commute with the operation of taking integrals. 
It can be shown that these coincide with the _affine_ maps, i.e. those maps $f:A\to B$ which satisfy
$$
f\big( \lambda\, a + \mu\, b  \big) \;=\; \lambda\,f(a) + \mu\,f(b)
$$
for all $a,b\in A$ and $0\le\lambda,\mu\le 1$ (with $\lambda+\mu=1$ for the normalized case).

For more information, see [Swirszcz '74](#swirszcz) and the later [Keimel '08](#radonkeimel).

The expectation map on $[0, \infty]$ is *not* a Radon monad algebra, although it is a [[Giry monad]] algebra. This is because $[0, \infty]$ is not a convex subset of any topological vector space, which causes the expectation map to not be continuous. To see this, consider the sequence of Radon measures $$r_n := (1 -\frac{1}{n})\delta_0 + \frac{1}{n} \delta_{n^2}$$. Note that the expectation of the limit, and limit of the expectations are not equal.
$$\mathbb{E}(\lim_{n \to \infty} r_n) = \mathbb{E}(\delta_0) = 0$$
$$\lim_{n \to \infty}\mathbb{E}(r_n) = \lim_{n \to \infty} n = \infty $$
Therefore the map $\mathbb{E}$ is not continuous, although it is measurable.


## The ordered case

The Radon monad can be lifted to the [[CompOrd#categories_of_compact_ordered_spaces|category of compact ordered spaces]] (and [[continuous map|continuous]] [[monotone maps]]).
This is done by means of the [[stochastic order]].

Here we sketch the construction. For more details, see [Keimel '08](#radonkeimel).

### Construction of the spaces

Given a [[compact ordered space]] $X$, we can form the spaces $R X$ and $P X$ as for the unordered case, and then equip them with the [[stochastic order]]. Over compact ordered spaces, the stochastic order is antisymmetric (i.e. it is a partial order), and it has [[closed graph]], so that $R X$ and $P X$ are again compact ordered spaces. 

Given a monotone map $f:X\to Y$, the maps $R f$ and $P f$ are monotone for the stochastic order, and so are the monad structure maps. This way, $P$ and $R$ lift to a monad on [[CompOrd#categories_of_compact_ordered_spaces|CompOrd]].

For the canonical [[locally posetal 2-category]] structure of [[CompOrd#categories_of_compact_ordered_spaces|CompOrd]] given by the [[pointwise order]], $P$ and $R$ are even [[2-monads]], since whenever $f\le g:X\to Y$, we have $R f\le R g$ $P f\le P g$.

Both the resulting monads are known in the literature as **ordered Radon monad**.

### Algebras

The algebras of the ordered Radon monad $P$ are known to be [[compact]] [[convex space|convex]] subsets of [[locally convex topological vector space|locally convex]] [[ordered topological vector spaces]]. This can be seen as the ordered equivalent of the characterization [above](#algebras).

The algebras of $R$, similarly, can be seen as the ordered equivalent of [[Kegelspitze]]. 

See [Keimel '08](#radonkeimel) for more.

Just as for the unordered case, the [[Eilenberg-Moore category|algebra morphisms]] are the continuous affine maps, which here are also required to be monotone.

### Lax morphisms are concave maps

Differently from the unordered case, in the ordered setting we have a [[2-category]], and so it makes sense to talk about [[lax morphisms]] of algebras. 
By definition, these amount to maps between algebras $f:A\to B$ with the [[stuff, structure, property|property]] that 
$$
f \left( \int a \, dp(a) \right) \;\le\; \int f(a) \, dp(a)
$$
for all $p\in P A$ (resp. $R A$).

By the generalized [[Jensen's inequality]], these are precisely the (continuous, monotone) [[concave maps]], i.e. the maps that satisfy
$$
f\big( \lambda\, a + \mu\, b  \big) \;\le\; \lambda\,f(a) + \mu\,f(b) .
$$
(Compare with the strict case by replacing the order with equalities.)

Just as well, the oplax morphisms are the (continuous, monotone) [[convex maps]].

(For more information see the analogous discussion for the [[Kantorovich monad]] in [F-P '18](#orderedkantorovich).)


## See also

* [[monads of probability, measures, and valuations]]

* [[Giry monad]], [[extended probabilistic powerdomain]], [[Kantorovich monad]]

* [[locally convex topological vector space]], [[ordered vector space]], [[convex space]]

* [[compact Hausdorff space]], [[compact ordered space]], [[stably compact space]]

* [[Borel measure]], [[Radon measure]], [[τ-additive measure]], [[continuous valuation]]


## References

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonais des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

* {#orderedkantorovich} [[Tobias Fritz]] and [[Paolo Perrone]], _Stochastic order on metric spaces and the ordered Kantorovich monad_, Advances in Mathematics 366, 2020. ([arXiv:1808.09898](https://arxiv.org/abs/1808.09898))


[[!redirects ordered Radon monad]]
[[!redirects radon monad]]
[[!redirects ordered radon monad]]