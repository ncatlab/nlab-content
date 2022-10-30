
# Measurable subsets
* table of contents
{: toc}

## Idea

The measurable subsets of a [[measure space]] $(X,\mu)$ are those [[subsets]] $A$ of the [[underlying set]] $X$ for which the measure $\mu(A)$ is defined (at all, even possibly as infinite).  Intuitively, one might expect every subset of $X$ to be measurable, and this is the case in some examples, but in the standard example of [[Lebesgue measure]] on the [[real line]], this is incompatible with the [[axiom of choice]].  (On the other hand, in [[dream mathematics]], where the full axiom of choice fails, every subset of the real line *is* Lebesgue measurable.)  Regardless, every subset $A$ of $X$ has both an [[outer measure]] $\mu^*(A)$ and an [[inner measure]] $\mu_*(A)$.

The concept actually makes sense in any [[measurable space]] as well as in related contexts such as [[Cheng spaces]] and [[measurable locales]].


## Definitions

Typically, the notion of measurable subset of $X$ is given axiomatically by a [[structure]] on the [[set]] $X$, usually a $\sigma$-[[sigma-algebra|algebra]] $\mathcal{M}$.  The a subset of $X$ is __measurable__ if it belongs to $\mathcal{M}$.

Sometimes $\mathcal{M}$ is a weaker structure, such as a $\delta$-ring; see other variants at [[sigma-algebra]].  Then we require some subsidiary notions: $S$ is __relatively measurable__ if $S \cap T$ belongs to $\mathcal{M}$ whenever $T$ does, and $S$ is __$\sigma$-measurable__ if it is a [[union]] of a [[countable set|countable]] [[family of subsets|family]] of elements of $\mathcal{M}$.

(The terms 'relatively measurable' and '$\sigma$-measurable' are [[Toby Bartels|my own]]; I cannot find them in the literature.  In the case of $\sigma$-measurable sets, the terminology follows a standard pattern.  Halmos uses relatively measurable sets, but he doesn\'t seem to give them a name.)


## Modulo null sets

Besides the $\sigma$-algebra of measurable subsets, we may place another structure on $X$, a $\sigma$-[[sigma-ideal|ideal]] $\mathcal{N}$ in $\mathcal{M}$.  (This structure also exists, for example, for any [[measure space]], and already for a [[Cheng space]] or a [[localisable measurable space]].)  Then a __[[null set]]__ is any subset of $X$ (measurable or not) contained in an element of $\mathcal{N}$.  The null sets form a $\sigma$-ideal $\bar{\mathcal{N}}$ of the [[power set]] $\mathcal{P}X$, and we may equivalently begin with the $\sigma$-ideal of null sets as long as every null set is contained in a measurable null set.

This allows two complementary modifications to the notion of measurable set:

1. We may accept the [[union]] of any measurable set and any null set as measurable.  Since this changes the meaning of 'measurable', we may speak of $\mathcal{M}$-measurable and $(\mathcal{M},\mathcal{N})$-measurable sets.  The collection of such sets may be denoted $\mathcal{M} \cup \bar{\mathcal{N}}$ (applying $\cup$ pointwise).

2. We may regard two measurable sets as equivalent if their [[symmetric difference]] is a null set (and hence an element of $\mathcal{N}$).  This defines an [[equivalence relation]] on $\mathcal{M}$; the collection of [[equivalence classes]] is denoted $\mathcal{M}/\mathcal{N}$.

Note that $(\mathcal{M} \cup \bar{\mathcal{N}})/\mathcal{N} \cong \mathcal{M}/\mathcal{N}$; indeed, this diagram commutes:
$$ \array {
   \mathcal{M}             & \hookrightarrow & \mathcal{M} \cup \bar{\mathcal{N}} \\
   \downarrow              &                 & \downarrow \\
   \mathcal{M}/\mathcal{N} & \cong           & (\mathcal{M} \cup \bar{\mathcal{N}})/\mathcal{N}
} $$
Accordingly, one may skip the former modification if one intends to also perform the latter.  Nevertheless, even when using $\mathcal{M}/\mathcal{N}$ as the lattice of measurable 'sets', if one considers a subset $A$ of $X$ and asks whether $A$ is 'measurable', one usually means whether $A \in \mathcal{M} \cup \bar{\mathcal{N}}$.

One could equally well begin with a $\delta$-[[delta-filter|filter]] $\mathcal{F}$, although a $\sigma$-ideal is more traditional.  Then a __[[full set]]__ is any subset of $X$ that contains in an element of $\mathcal{F}$.  (If we start with the $\delta$-filter $\bar{\mathcal{F}}$ in $\mathcal{P}X$, then every full set must contain a measurable full set.)  In [[constructive mathematics]], full sets are more fundamental for such examples as [[Lebesgue measure]].  In any case, the modifications are as follows:

1. We may accept the [[intersection]] of any measurable set and any full set as measurable; the collection of such sets may be denoted $\mathcal{M} \cap \bar{\mathcal{F}}$.

2. We may regard two measurable sets as equivalent if their [[biconditional]] is a full set; the collection of equivalence classes is denoted $\mathcal{M}/\mathcal{F}$.

Then we have this commuting diagram:
$$ \array {
   \mathcal{M}             & \hookrightarrow & \mathcal{M} \cap \bar{\mathcal{F}} \\
   \downarrow              &                 & \downarrow \\
   \mathcal{M}/\mathcal{F} & \cong           & (\mathcal{M} \cap \bar{\mathcal{F}})/\mathcal{F}
} $$


## Abstract measurable sets

Already we have seen that we may be more interested in [[equivalence classes]] of measurable sets than in the sets themselves.  We may well start with any appropriate algebra in the place of $\mathcal{M}/\mathcal{F}$ above and regard its elements are 'measurable sets'.  This may be done in the theory of [[measurable locales]] and other 'pointless' approaches to measure theory.


[[!redirects measurable set]]
[[!redirects measurable sets]]
[[!redirects measurable subset]]
[[!redirects measurable subsets]]
[[!redirects measurable subspace]]
[[!redirects measurable subspaces]]

[[!redirects relatively measurable subset]]
[[!redirects relatively measurable subsets]]
[[!redirects relatively measurable set]]
[[!redirects relatively measurable sets]]

[[!redirects sigma-measurable subset]]
[[!redirects sigma-measurable subsets]]
[[!redirects ∞-measurable subset]]
[[!redirects ∞-measurable subsets]]
[[!redirects sigma-measurable set]]
[[!redirects sigma-measurable sets]]
[[!redirects ∞-measurable set]]
[[!redirects ∞-measurable sets]]
