
# Contents
* table of contents
{: toc}

## Idea

Borel measures are [[measures]] on the [[Borel σ-algebra]] of a [[topological space]].  They play an important role in [[measure theory]].


## Definition

A __Borel measure__ on $X$ is a (countably additive) measure on the [[Borel σ-algebra]] of the topological space $X$.

A __Baire measure__ on $X$ is a (countably additive) measure on the [[Baire σ-algebra]] of the topological space $X$.

A [[Radon measure]] on $X$ is a Borel measure $\mu$ on $X$
such that for any [[Borel subset]] $B\subset X$ and any $\epsilon\gt0$ there is a [[compact subset]] $K\subset B$
such that $|\mu|(B\setminus K)\lt\epsilon$,
where $|\mu|$ denotes the total [[variation]] of the measure $\mu$.

Borel measures are uniquely determined by their values on open subsets,
and are closely related to [[continuous valuations]] on the underlying [[locale]].

A measure $\mu$ on a topological space $X$
is __tight__ if for any $\epsilon\gt0$
there is a [[compact subset]] $K\subset X$
such that $|\mu|(A)\lt\epsilon$ for any $A\subset X\setminus K$.

A measure $\mu$ on a topological space $X$
is __regular__ if for any measurable subset $A\subset X$
and $\epsilon\gt0$
there is a closed subset $F\subset A$ such that
$A\setminus F$ is measurable and $\mu(A\setminus F)\lt\epsilon$.

Radon measures on [[Hausdorff spaces]] are regular and tight.
Regular tight Borel measures are automatically Radon.
A regular Borel measure need not be tight.

A Borel measure $\mu$ on a topological space $X$
is __[[τ-additive]]__ (alias τ-regular, τ-smooth)
if $|\mu|(\bigcup_i U_i)=\lim_i |\mu|(U_i)$
for any directed system of open subsets $U_i\subset X$.
In other words, the underlying valuation of $\mu$ is a [[continuous valuation]].

If the above condition only holds in the case $\bigcup_i U_i=X$,
we talk about __$\tau_0$-additive__ (or weakly τ-additive) measures.

Any regular $\tau_0$-additive Borel measure is [[τ-additive]].
There are $\tau_0$-additive Borel measures that are not [[τ-additive]].


## Properties

On a [[metric space]] every Borel measure is regular.
More generally, every Borel measure on a [[perfectly normal]] space is regular.

On a complete separable [[metric space]] every Borel measure is Radon.

Every Baire measure is regular.

Every [[Radon measure]] is [[τ-additive]].

Every [[τ-additive]] measure on a regular space is regular.
In particular, every [[τ-additive measure]] on a compact space is Radon.

Every tight [[τ-additive]] measure is Radon.

Every Borel measure on a separable metric space X is τ-additive.
Moreover, this is true if X is [[hereditary Lindelöf]].

Every [[τ-additive]] measure has a [[support]], which is a closed subset.

## Extension properties

Every tight Baire measure on a [[completely regular]] space admits a unique extension to a Radon measure.
More generally, any tight Baire measure on a Hausdorff space has a Radon extension.

Every Baire measure on a σ-compact [[completely regular space]] has a unique extension to a Radon measure.

## Relation to linear functionals

Given a topological space $X$, the integration map
sends Borel measures on $X$ to linear functionals
on the space of continuous bounded functions on $X$.

For many types of topological spaces and measures
this map is bijective, as indicated below.

There is a bijection between Baire measures on a topological space
and continuous linear functionals $L$ on continuous bounded functions
such that $L(f_n)\to 0$ whenever $f_n \to 0$ pointwise and monotonic.

There is a bijection between Radon measures on a completely
regular topological space and continuous linear functionals $L$
on continuous bounded functions such that for any $\epsilon\gt0$
there is a compact subset $K$ such that for any continuous bounded
function $f$ that vanishes on $K$ we have $|L(f)|\le\epsilon\sup|f|$.

There is a bijection between τ-additive Borel measures
on a completely regular topological space and continuous linear functionals $L$ on continuous bounded functions such that
$L(f_a)\to0$ for any net $f$ of bounded continuous functions
that decreases to zero pointwise.

There is a bijection between positive Borel measures on a [[locally compact]]
topological space that are inner regular on all Borel subsets
with respect to compact subsets
and positive linear functionals on continuous functions vanishing at infinity.

## Related concepts

* [[Borel set]]

* [[Radon measure]]

* [[continuous valuation]]

* [[measure]]

[[!redirects Borel measures]]
[[!redirects Baire measures]]
