
# Absolutely continuous measures
* table of contents
{: toc}

## Idea

A [[measure]] $\mu$ is absolutely continuous with respect to $\nu$ if we can think of $\mu$ as a weighted variation on $\nu$.


## Definition

Fix a [[measurable space]] $X$ and let $\mu$ and $\nu$ be two [[measures]] on $X$.

+-- {: .num_defn}
###### Definition

The measure $\mu$ is __absolutely continuous__ with respect to $\nu$ if every $\nu$-[[full set]] is also $\mu$-full.
=--

Because [[null sets]] are more familiar than [[full sets]], we may equivalently express things as follows (but this is not correct in [[constructive mathematics]]):

+-- {: .num_defn}
###### Definition (classical)

The measure $\mu$ is __absolutely continuous__ with respect to $\nu$ if every $\nu$-[[null set]] is also $\mu$-null.
=--

If $\mu$ and $\nu$ are [[positive measures]], then we may also express this as follows:

+-- {: .num_defn}
###### Definition (positive, classical)

The positive measure $\mu$ is __absolutely continuous__ with respect to $\nu$ if, for every [[measurable set]] $A$, $\mu(A) = 0$ if $\nu(A) = 0$.
=--

Since the [[absolute value]] of a measure is a positive measure, we can also express the general definition as follows:

+-- {: .num_defn}
###### Definition (classical)

The measure $\mu$ is __absolutely continuous__ with respect to $\nu$ if, for every [[measurable set]] $A$, ${|\mu|}(A) = 0$ if ${|\nu|}(A) = 0$.
=--


## Generalisation

Since only the [[full sets]] (or, classically, the [[null sets]]) matter, we do not need to have the full structure of a [[measure]].  Sometimes we equip a [[measurable space]] with a $\delta$-[[delta-filter|filter]] $\mathcal{F}$ of full sets (or a $\sigma$-[[sigma-ideal|ideal]] $\mathcal{N}$ of null sets) without specifying a measure that produces these.  (For example, a [[smooth manifold]] is so equipped, effectively the full/null sets under [[Lebesgue measure]], even though there is no canonical such measure, since these sets are the same regardless of [[coordinate chart]].)  Then we say:

+-- {: .num_defn}
###### Definition

The measure $\mu$ is __absolutely continuous__ with respect to $\mathcal{F}$ (or $\mathcal{N}$) if every element of $\mathcal{F}$ is $\mu$-[[full set|full]] (or every element of $\mathcal{N}$ is $\mu$-[[null set|null]]).
=--

In fact, only the full/null sets of $\mu$ matter either, but until somebody has use for the notion of one $\delta$-filter (or $\sigma$-ideal) being absolutely continuous with respect to another, I will refrain from writing it down.  (See [[centipede mathematics]].)


## Defaults

If one calls a measure on the [[real line]] 'absolutely continuous', this means with respect to [[Lebesgue measure]].

This generalises to any [[cartesian space]] (with Lebesgue measure) or indeed to any [[smooth manifold]] of [[finite dimension]] (where there is no canonical Lebesgue measure but a family of local ones and so still a notion of Lebesgue-full and Lebesgue-null sets).

Or, this generalises to any [[compact group]] (with [[Haar measure]]) or indeed to any [[locally compact group]] (where there is no canonical Haar measure but a proportional family of them and so still a canonical notion of Haar-full and Haar-null sets).


## Properties

Let $\nu$ be a measure, and let $f \in L^1(\nu)$ be an [[absolutely integrable function]] with respect to $\nu$; then [[integration]] defines a measure $f \nu$:
$$ (f \nu)(E) = \int_E f \nu = \int_E f(x) \nu(\mathrm{d}x) .$$
This measure $f \nu$ is absolutely continuous with respect to $\nu$.  Conversely, given any absolutely continuous measure $\mu$, there is (at most) a unique (up to [[almost equality]]) absolutely integrable function $f$ such that $\mu = f \nu$; and this function must exist if $\mu$ and $\nu$ are [[localizable measure|localizable]].  This converse is the subject of the [[Radon–Nikodym theorem]].

A function $f\colon \mathbb{R} \to \mathbb{R}$ is [[absolutely continuous function|absolutely continuous]] iff the [[Stieltjes integral|Lebesgue–Stieltjes measure]] $\mathrm{d}f$ is absolutely continuous with respect to [[Lebesgue measure]].  (All such functions are [[continuous function|continuous]], and this example is actually the origin of the term.)


[[!redirects absolutely continuous measure]]
[[!redirects absolutely continuous measures]]
