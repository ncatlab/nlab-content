
# Cauchy filters
* table of contents
{: toc}

## Idea

A _Cauchy filter_ on a [[space]] $X$ is a [[proper filter]] on $X$ that contains  sets (meaning [[subsets]] of $X$) of arbitrarily small [[diameter]].

The precise definition depends on what sort of space $X$ is, up to	the full generality of a [[Cauchy space]].


## Definitions

+-- {: .num_defn #reals}
###### Definition

A __Cauchy filter__ on the [[real numbers]] is a [[proper filter]] $F$ with, for each strictly [[positive number]] $\delta \in \mathbb{R}$, a set $A \in F$ with, for each $x,y \in A$, $\vert y - x\vert \leq \delta$.
=--

Sometimes, one uses Cauchy filters on the rational numbers to construct the real numbers in the first place. 

+-- {: .num_defn #rationals}
###### Definition

A __Cauchy filter__ on the [[rational numbers]] is a [[proper filter]] $F$ with, for each strictly [[positive number]] $\delta \in \mathbb{Q}$, a set $A \in F$ with, for each $x,y \in A$, $\vert y - x\vert \leq \delta$.
=--

In a [[metric space]], the [[diameter]] of a [[subset]] $A$ is the [[supremum]] of the [[distance]]s $d(x,y)$ for $x,y \in A$ (which is a [[lower real number]] in general).  However, we need not think precisely about these diameters; it is enough to characterise those sets with diameter at most $\delta$.

+-- {: .num_defn #metric}
###### Definition

A __Cauchy filter__ on a metric space is a [[proper filter]] $F$ with, for each strictly [[positive number]] $\delta$, a set $A \in F$ with, for each $x,y \in A$, $d(x,y) \leq \delta$.
=--

(It is actually sufficient to consider enough sufficiently small values of $\delta$, say [[rational number|rational]] $\delta$ or [[decimal fraction]] $\delta$.)

In a [[gauge space]], instead of a single number $\delta$ to estimate diameter, we use $\delta$ together with a gauging distance $d$.

+-- {: .num_defn #gauge}
###### Definition

A __Cauchy filter__ on a gauge space is a [[proper filter]] $F$ with, for each gauging distance $d$ and each strictly positive number $\delta$, a set $A \in F$ with, for each $x,y \in A$, $d(x,y) \leq \delta$.
=--

(It is actually sufficient to consider a base of gauging distances, as well as enough sufficiently small $\delta$.)

In a [[Booij premetric space]], we use the [[premetric]] to estimate diameter. 

+-- {: .num_defn #metric}
###### Definition

A __Cauchy filter__ on a [[Booij premetric space]] is a [[proper filter]] $F$ with, for each strictly [[positive number]] $\delta$, a set $A \in F$ with, for each $x,y \in A$, $x \sim_\epsilon y$.
=--

In a [[topological group]], we use a [[neighbourhood]] of the [[identity element]] to estimate diameter.

+-- {: .num_defn #topgroup}
###### Definition

A __Cauchy filter__ on a topological group is a [[proper filter]] $F$ with, for each neighbourhood $U$ of the identity, a set $A \in F$ with, for each $x,y \in A$, $x^{-1} y \in U$ (or equivalently, for each $x,y \in A$, for some $n \in U$, $x n = y$).
=--

(It is sufficient to consider a [[neighbourhood base]] at the identity.  There is no difference between left and right even for nonabelian groups.)

In a [[uniform space]], we use an [[entourage]] $U$ to estimate diameter.

+-- {: .num_defn #uniform}
###### Definition

A __Cauchy filter__ on a uniform space is a [[proper filter]] $F$ with, for each entourage $U$, a set $A \in F$ with, for each $x,y \in A$, $x \approx_U y$ (that is, $(x,y) \in U$).
=--

(It is sufficient to consider a base of the uniformity.)

If you want to define uniformities in terms of [[uniform covers]]:

+-- {: .num_defn #ucover}
###### Definition

A __Cauchy filter__ on a uniform space is a [[proper filter]] $F$ with, for each uniform cover $U$, a set $A \in F$ with $A \in U$.
=--

(It is sufficient to consider a base of uniform covers.)

All of the above have non-symmetric versions: [[quasimetric spaces]], [[quasigauge spaces]], [[topological monoids]], [[quasiuniform spaces]].  The definition of Cauchy filter for these is the same, with these caveats:

* for a topological monoid, there is a difference between left and right in $x n = y$ in Definition \ref{topgroup}, giving left-Cauchy and right-Cauchy filters;
* there is no notion of quasiuniform cover to generalise Definition \ref{ucover}.

The most general context is that of a [[Cauchy space]], where the notion of Cauchy filter is axiomatic.


## Properties

Cauchy filters in all cases above have these properties:

* Every Cauchy filter is [[proper filter|proper]].
* The [[principal ultrafilter]] $U_x$ at any point $x$ is Cauchy.
* If $F$ is Cauchy, $G$ is [[proper filter|proper]], and $G$ refines $F$ ($G \supseteq F$), then $G$ is Cauchy.
* If $F$ and $G$ are Cauchy and their [[join]] $F \vee G$ is proper, then their [[intersection]] $F \cap G$ is Cauchy.

These conditions form the abstract definition of a [[Cauchy space]].

Furthermore, all of these have a notion of [[convergence]] given as follows:

*  A filter $F$ __converges__ to a point $x$ if $F \cap U_x$ is Cauchy.

In this way, every Cauchy space becomes a [[convergence space]], which agrees with the usual convergence on metric spaces, uniform spaces, etc.

A [[function]] $f\colon X \to Y$ between spaces is __[[Cauchy-continuous map|Cauchy-continuous]]__ if, for every Cauchy filter $F$ on $X$, the filter (generated by) $f(F)$ is Cauchy.  (These are the [[morphisms]] in the [[category]] of Cauchy spaces.)


## In nonstandard analysis

In [[nonstandard analysis]], the hyperpoints of a (quasi)uniform space have a relation of [[adequality]].  A proper filter $F$ is Cauchy iff its nonstandard extension $F^*$ contains a hyperset (a collection of hyperpoints) $A$ whose elements are all adequal.  So compared to the other definitions, a single $A$ of infinitesimal diameter suffices.

A hyperpoint $x$ is __[[finite hyperpoint|finite]]__ (or __limited__) if there is a proper filter $F$ (necessarily Cauchy) such that $F^*$ contains a hyperset whose elements are all adequal to $x$.  In the analogy between hyperpoints and [[ultrafilters]], the finite hyperpoints correspond to the Cauchy ultrafilters.

A map $f$ between (quasi)uniform spaces is Cauchy-continuous iff its nonstandard extension $f^*$ has the property that $f^*(x)$ and $f^*(y)$ are adequal whenever $x$ and $y$ are adequal and $x$ is finite.  (Compare that $f$ is [[uniformly continuous]] iff $f^*$ has this property regardless of whether $x$ is finite.)  Presumably one can define a [[Cauchy space]] in nonstandard analysis by specifying the finite hyperpoints and the relation of adequality only with these (although perhaps not every Cauchy space arises in this way).


[[!redirects Cauchy filter]]
[[!redirects Cauchy filters]]
