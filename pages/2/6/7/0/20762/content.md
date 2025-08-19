[[!redirects Extended probabilistic powerdomain]]

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

The extended probabilistic powerdomain is a [[monad of valuations]] on [[topological spaces]]. Its functor part assigns to a given [[topological space]] the space of [[continuous valuations]] over it.

The idea of this monad was first given by Kirch for the case of [[domains]] (see [Kirch '93](#kirch), in German, or [AJK '06](#Jung), in English). It was extended to all of [[Top]] and given its current form by Heckmann (see [Heckmann '96](#Heckmann96)). 


## Definitions

### Spaces of valuations

Given a [[topological space]] $X$, denote by $V X$ the space whose points are [[continuous valuations]] on $X$ with values in $[0,\infty]$. Equip $V X$ with the [[topology]] [[topological basis|generated]] by the sets in the form
$$
\theta(U,r) \coloneqq \{ \nu \in V X \,|\, \nu(U) \gt r \},
$$
for $r\ge 0$ and $U\subseteq X$ [[open]], or equivalently by the sets in the form
$$
\Theta(g,r) \coloneqq \left\{ \nu \in V X \,\Big|\, \int g \,d\nu \gt r \right\}
$$
for $r\ge 0$ and $g:X\to[0,\infty]$ [[lower semicontinuous]].

This topology can be seen as the [[pointwise topology]] if we view valuations either as functions on the [[open sets]] or as [[functionals]] on lower semicontinuous functions (via [[continuous valuation#integration|integration]]).
It is also the [[initial topology]] of either evaluation of open sets or integration of functions, meaning that it is the coarsest topology for which either the assignments
$$
\nu \mapsto \nu(U)
$$
for every open $U\subseteq X$, or 
$$
\nu \mapsto \int g \, d\nu 
$$
for every lower semicontinuous $g:X\to[0,\infty]$, are lower semicontinuous.
Lower semicontinuity, in some sense, plays the role that [[measurable function|measurability]] plays for the [[Giry monad]] (see also [[correspondence between measure and valuation theory]]).

The [[specialization preorder]] of this topology is known as the [[stochastic order]], and can be seen as the [[pointwise order]] of valuations as functions on the open sets. 

It is known (see [Jung '04](#jung2)) that if $X$ is [[stably compact]], then $V X$ is stably compact too, so that the monad $V$ restrict to the subcategory of [[stably compact spaces]]. 


### Functoriality

Given a [[continuous map]] $f:X\to Y$, define the map $ f:V X\to V Y$ as the one assigning to a continuous valuation $\nu\in V X$ its [[continuous valuation#pushforward|pushforward]] along $f$.

It can be proven that the map $V f$ is continuous too, so that $V$ is an [[endofunctor]] of [[Top]]. 

### Unit and multiplication

We can define the unit of the [[monad]] as follows. Given a space $X$, define the map $\delta:X\to V X$ as the one assigning to the point $x\in X$ the [[valuation (measure theory)#dirac_valuation|Dirac valuation]] at $x$. 
This map $\delta$ is [[continuous map|continuous]], and [[natural transformation|natural]] in $X$. 

The multiplication map makes use of the concept of [[valuation (measure theory)#integration|integration over a valuation]]. Given a valuation $\xi\in V V X$, we can define the valuation $E \xi\in V X$ as the one mapping an [[open]] set $U\subseteq X$ to 
$$
E \xi (U) \coloneqq \int_X \nu(U) \, d\xi(\nu).
$$
This integral is well defined, since the assignment $U\mapsto \nu(U)$ is [[lower semicontinuous]]. The assignment $U\mapsto E \xi (U)$ gives a [[continuous valuation]] on $X$, and the resulting map $E: V V X \to V X$ is [[continuous map|continuous]] and [[natural transformation|natural]] in $X$. 

The maps $\delta$ and $E$ satisfy the usual [[axioms]] of a [[monad]]. The monad $(V,\delta,E)$ is usually called the **extended probabilistic powerdomain**.

This construction, especially the way the unit and multiplications are defined, can be thought of as a topological analogue of the [[Giry monad]]. 


## Monoidal structure

(...)


## Algebras

(...)


## Notable submonads

There are a number of monads that can be constructed as submonads of $V$. The [[monoidal functor|monoidal structure]] of $V$ is inherited by these submonads too, allowing the formation of joints and marginals.

See also [[monads of probability, measures, and valuations#detailed_list|monads of probability, measures, and valuations - detailed list]].

### Normalized valuations

If one restricts to _normalized_ valuations, i.e.~those $\nu\in V X$ with $\nu(X)=1$, one obtains a submonad of $V$ which can be thought of as the one of [[probability]] valuations. 


### The measure monad on Top

One can restrict $V$ only to those valuations which are [[valuation (measure theory)#extending_valuations_to_measures|extendable to measures]]. The resulting subspace $M X\subseteq V X$ (for every topological space $X$) is the space of [[tau-additive measures]] on $X$, with the subspace topology inherited by $V X$. For probability measures, this topology is sometimes known as the **A-topology**, after Alexandrov (not to be confused with the [[Alexandrov topology]], which is a different concept), for example in [Bogachev, section 8.10.iv](#bogachev2). The [[specialization preorder]] is again the [[stochastic order]]. 
Since extendable valuations are stable with respect to pushforwards and integrations, $M$ forms a submonad of $V$, the **measure monad on [[Top]]**.

More details can be found in [Fritz-Perrone-Rezagholi '19](#support), worked out explicitly for the normalized case (see below). 

See also [[correspondence between measure and valuation theory]].

### The probability monad on Top

If one restricts the measure monad above to the $\tau$-smooth _probability_ measures (i.e. normalized), one obtains again a submonad, which seems to be the most general [[probability monad]] on [[Top]]. 

If a topological space is [[Tychonoff space|Tychonoff]] (for example a [[metric space]] or a [[compact Hausdorff space]]), the A-topology for probability measures coincides with the usual [[weak topology]] of measures with respect to continuous functions. 
In particular, on the [[subcategory]] of [[compact Hausdorff spaces]], this monad restricts to the [[Radon monad]]. 

### The monad of topological cones

If one restrict to [[valuation (measure theory)#simple_valuations|simple valuations]], i.e. those that are linear combinations of deltas, one obtains again a submonad of $V$, which can be thought of as the free [[topological cone]] monad (or free internal $[0,\infty]$-[[module object]] monad). 

### The monad of topological convex spaces

If one further restricts to _normalized_ simple valuations, one obtains as submonad the free [[topological convex space]] monad.


## Related concepts

* [[monads of probability, measures, and valuations]]
* [[monads in computer science]]

* [[valuation (measure theory)]]
* [[correspondence between measure and valuation theory]]

* [[Giry monad]], [[Radon monad]], [[probabilistic powerdomain]], [[valuation monad on locales]], [[distribution monad]]

* [[convex space]], [[conical space]]



## References

* {#kirch} Olaf Kirch, _Bereiche und Bewertungen_ (in German), Master Thesis, Technische Hochschule Darmstadt, 1993 ([ps.gz](http://fb04286.mathematik.tu-darmstadt.de/fbereiche/logik/research/Domains/papers/kirch/diplom.ps.gz))

* {#Heckmann96} Reinhold Heckmann, _Spaces of valuations_, Papers on General Topology and Ap-plications, 1996 ([doi:10.1111/j.1749-6632.1996.tb49168.x](https://doi.org/10.1111/j.1749-6632.1996.tb49168.x),[pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.45.5845&rep=rep1&type=pdf))

* {#jung2} Achim Jung, _Stably compact spaces and the probabilistic powerspace construction_, ENTCS 87, 2004 ([doi:10.1016/j.entcs.2004.10.001](https://doi.org/10.1016/j.entcs.2004.10.001)).

* {#Jung}Mauricio Alvarez-Manilla, Achim Jung, [[Klaus Keimel]], _The probabilistic powerdomain for stably compact spaces_, Theoretical Computer Science 328, 2004 ([doi:10.1016/j.tcs.2004.06.021](https://doi.org/10.1016/j.tcs.2004.06.021))

* {#algebras} [[Jean Goubault-Larrecq]] and Xiaodong Jia, _Algebras of the extended probabilistic powerdomain monad_, ENTCS 345, 2019
([doi:10.1016/j.entcs.2019.07.015](https://doi.org/10.1016/j.entcs.2019.07.015))

* {#support} [[Tobias Fritz]], [[Paolo Perrone]] and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019 ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))


* {#bogachev2} V. Bogachev, _Measure Theory_, vol. 2 (2007).


[[!redirects extended probabilistic powerdomain]]
[[!redirects valuation monad on top]]
[[!redirects valuation monad on topological spaces]]