
# Measurable subsets
* table of contents
{: toc}

## Idea

The measurable subsets of a [[measure space]] $(X,\mu)$ are those [[subsets]] $A$ of the [[underlying set]] $X$ for which the measure $\mu(A)$ is defined (at all, even possibly as infinite).  Intuitively, one might expect every subset of $X$ to be measurable, and this is the case in some examples, but in the standard example of [[Lebesgue measure]] on the [[real line]], this is incompatible with the [[axiom of choice]].  (On the other hand, in [[dream mathematics]], where the full axiom of choice fails, every subset of the real line *is* Lebesgue measurable.)

Regardless, every subset $A$ of $X$ has both an [[outer measure]] $\mu^*(A)$ and an [[inner measure]] $\mu_*(A)$.


## Definitions

Typically, the notion of measurable subset of $X$ is given axiomatically by a [[structure]] on the [[set]] $X$, usually a $\sigma$-[[sigma-algebra|algebra]] $\mathcal{M}$.  The a subset of $X$ is __measurable__ if it belongs to $\mathcal{M}$.

Sometimes $\mathcal{M}$ is a weaker structure, such as a $\delta$-ring; see other variants at [[sigma-algebra]].  Then we require some subsidiary notions: $S$ is __relatively measurable__ if $S \cap T$ belongs to $\mathcal{M}$ whenever $T$ does, and $S$ is __$\sigma$-measurable__ if it is a [[union]] of a [[countable set|countable]] [[family of subsets|family]] of elements of $\mathcal{M}$.

(The terms 'relatively measurable' and '$\sigma$-measurable' are [[Toby Bartels|my own]]; I cannot find them in the literature.  In the case of $\sigma$-measurable sets, the terminology follows a standard pattern.  Halmos uses relatively measurable sets, but he doesn\'t seem to give them a name.)


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
