+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
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

An *invariant set* is a subset which is [[invariant]] under the [[action]] of a [[group]] or a [[monoid]]. 

## Definition

Let $X$ be a [[set]], let $M$ be a [[monoid]] (or a [[group]]), and consider an [[action]] of $M$ on $X$. (For each $m\in M$, denote the resulting action on $X$ again by $m:X\to X$.)

A subset $S$ of $X$ is called **invariant** if and only if for each $m\in M$, $m^{-1}(S)=S$.
Equivalently, if for every $x\in X$ we have that $x\in S$ if and only if $f(x)\in S$. 

Note that the *points* of an invariant set are not themselves invariant: they might move under the action (but they remain in the set $S$). For example, for rotations in the plane, any circle centered at the origin is an invariant set, but each point in each nontrivial circle is not a fixed point.

### Variations of the definition

Since the original definition was given for the case of [[group actions]], which are invertible, there are a number of variants of the same definition which differ for the case of arbitrary monoids. 
In particular, sometimes one calls a subset $S\subseteq X$ *invariant* if and only if $m^{-1}(S)\subseteq S$, i.e. if for every $x\in S$, $f(x)\in S$ as well. (Without requiring that if $f(x)\in S$, then $x\in S$.) 
In other words, it is a set "which we cannot leave" under the specified action. 
Sometimes such a set is called an *absorbing set* instead. (But that term may itself be used for other concepts, to make matters even worse.)

Also, in different categories than [[Set]], similar variation of the notion of invariant set are given:

* In [[topology]], given a [[continuous]] action, one is often interested in invariant [[closed]] sets;
* In [[probability theory]], one is often interested in invariant [[measurable]] sets;
* In [[differential geometry]], one is often interested in invariant [[submanifolds]],
...and so on.


## Examples

* Each [[orbit]] of a [[group action]] is an invariant set. Moreover, a set is invariant if and only if it is a (possibly empty) union of orbits.

* In [[probability theory]], an [[exchangeable event]] is a [[measurable subset]] which is invariant under finite [[permutations]], and a [[tail event]] is invariant under [[shifts]].


## Invariant sigma-algebras

Let $X$ be a [[measurable set]]. Let $M$ be a [[monoid]] (or [[group]]), and consider an action of $M$ on $X$ via measurable functions $m:X\to X$.

A [[measurable subset]] $A\subseteq X$ is called **invariant** if and only if for every $m\in M$, $m^{-1}(A)=A$. 

Invariant sets form naturally a [[sigma-algebra]], often called the **invariant sigma-algebra**. 

The [[exchangeable sigma-algebra]] and the [[tail sigma-algebra]] are examples of this. (Sometimes one uses the almost sure versions, see [below](#almost_surely_invariant_sets).)

The invariant sigma-algebra gives a [[colimit]] of the [[action]] of $M$ in the [[Stoch|category of Markov kernels]] ([MP'23](#markov_ergodic)). More precisely, denote by $X_inv$ the set $X$ together with the invariant sigma-algebra, and denote by $q:X\to X_inv$ the kernel [[Markov kernel#kernels_from_deterministic_functions|induced by]] the set-theoretic identity. 
Then the $(X_inv,q)$ forms a universal [[cocone]] (i.e. [[colimit]]), meaning that for every kernel $k:X\to Y$ satisfying $k\circ m=k$, (i.e. right-invariant under the action of $m$), there exists a unique kernel $\tilde{k}:X_inv\to Y$ making the following diagram commute:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
column sep=large,%
]
X \ar{dd}[swap]{k_m} \ar{dr}[swap]{q} \ar{drr}{k} \\
 & X_\mathrm{inv} \ar[dashed]{r}{\tilde{k}} & Y \\
X \ar{ur}[swap]{q} \ar{urr}{k}
\end{tikzcd}
The kernel $\tilde{k}$ has the same entries as $k$: by invariance, $k$ is indeed [[measurable]] for the sigma-algebra of invariant sets.


### For stochastic actions

(...)

### Almost surely invariant sets

(...)

### Further properties

(..)



## See also

* [[group]], [[monoid]], [[action]]
* [[cone]], [[limit]], [[cocone]], [[colimit]]
* [[exchangeability]], [[invariant measure]], [[tail event]]
* [[ergodic measure]], [[ergodic decomposition theorem]]

* Wikipedia, [Invariant sigma-algebra](https://en.wikipedia.org/wiki/Invariant_sigma-algebra)


## References

* {#fritz_definetti} [[Tobias Fritz]], Tomáš Gonda, [[Paolo Perrone]], _De Finetti's theorem in categorical probability_. Journal of Stochastic Analysis, 2021. ([arXiv:2105.02639](https://arxiv.org/abs/2105.02639))

* {#markov_ergodic} Sean Moss, [[Paolo Perrone]], _A category-theoretic proof of the ergodic decomposition theorem_, Ergodic Theory and Dynamical Systems, 2023. ([arXiv:2207.07353](https://arxiv.org/abs/2207.07353))

* {#ergodic_dagger} Noé Ensarguet, [[Paolo Perrone]], Categorical probability spaces, ergodic decompositions, and transitions to equilibrium, [arXiv:2310.04267](https://arxiv.org/abs/2310.04267)


category: probability


[[!redirects invariant sets]]
[[!redirects invariant subset]]
[[!redirects invariant subsets]]
[[!redirects invariant sigma-algebra]]
[[!redirects invariant sigma-algebras]]
[[!redirects invariant sigma algebra]]
[[!redirects invariant sigma algebras]]
[[!redirects invariant σ-algebra]]
[[!redirects invariant σ-algebras]]