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

For probability measures, the [[weak topology]] and the [[extended probabilistic powerdomain#the_measure_monad_on_top|A-topology]] coincide, so that $P$ an be extended to a submonad of the [[extended probabilistic powerdomain#the_probability_monad_on_top|probability monad on Top]].

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

Conversely, it can be proven that every $P$-algebra is of this form (see [Swirszcz '74](#swirszcz) and the later [Keimel '08](#radonkeimel)).


## The ordered case

(Work in progress. For now see [Keimel '08](#radonkeimel).)

(...)


## See also

* [[monads of probability, measures, and valuations]]

* [[Giry monad]], [[extended probabilistic powerdomain]]

* [[locally convex topological vector space]], [[ordered vector space]], [[convex space]]

* [[compact Hausdorff space]], [[compact ordered space]], [[stably compact space]]

* [[Borel measure]], [[Radon measure]], [[τ-additive measure]], [[continuous valuation]]


## References

* {#swirszcz} T. Swirszcz, _Monadic functors and convexity_, Bulletin de l'Academie Polonais des Sciences 22, 1974 ([pdf](https://www.fuw.edu.pl/~kostecki/scans/swirszcz1974.pdf))

* {#radonkeimel} [[Klaus Keimel]], _The monad of probability measures over compact ordered spaces and its Eilenberg-Moore algebras_, Topology and its Applications, 2008 ([doi:10.1016/j.topol.2008.07.002](https://doi.org/10.1016/j.topol.2008.07.002))

[[!redirects ordered Radon monad]]
[[!redirects radon monad]]
[[!redirects ordered radon monad]]