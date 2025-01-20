

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

A _$\sigma$-locale_ is, intuitively, like a [[sigma-topological space|$\sigma$-topological space]] that may or may not have enough [[points]] (or even any points at all). It contains things we call [[open subspaces]] but there may or may not be enough points to distinguish between open subspaces. An open subspace in a $\sigma$-locale can be regarded as conveying a bounded amount of information about the (hypothetical) points that it contains.

Similar to [[topological spaces]] and [[locales]], every $\sigma$-topological space can be regarded as a $\sigma$-locale (with some lost information if the space is not [[sober sigma-topological space|sober]]). The $\sigma$-locales arising this way are the _[[topological sigma-locale|topological]]_ or _spatial_ $\sigma$-locales. Conversely, every $\sigma$-locale induces a $\sigma$-topology on its set of points, but sometimes a great deal of information is lost; in particular, there are many different $\sigma$-locales whose set of points is [[empty set|empty]].

## Definition

A **$\sigma$-locale** $X$ is a [[sigma-frame]], commonly labelled as $\mathcal{O}(X)$. 

A **[[continuous function]]** $f:X \to Y$ between $\sigma$-locales $X$ and $Y$ is a sigma-frame [[homomorphism]] $f^*:\mathcal{O}(Y) \to \mathcal{O}(X)$, a [[monotonic function]] which preserves [[finite set|finite]] [[meets]] and [[countable set|countable]] [[joins]]. 

## Subsidiary notions

### Points

As a $\sigma$-locale, the __abstract [[point]]__ is the locale $1$ whose $\sigma$-frame of opens is the initial sigma-frame $\Sigma$, which is a $\sigma$-subframe of [[truth values]] $\Sigma \subseteq \Omega$. in [[classical mathematics]] and in [[constructive mathematics]] that assumes the [[limited principle of omniscience]], the initial $\sigma$-frame is the [[boolean domain]] $\{\bot \lt \top\}$. This is the [[terminal object]] in $\sigma \mathrm{Locale}$, since we must have (for $f\colon X \to 1$) $f^*(\top) = \top_X$ and $f^*(\bot) = \bot_X$.

Given a $\sigma$-locale $X$, a __concrete [[point]]__ of $X$ may be defined in any of the following equivalent ways:

1.  A point of $X$ is a [[continuous map]] $f\colon 1 \to X$;
2.  Unravelling this in terms of $f^*\colon O(X) \to O(1)$ and viewing this as a [[characteristic function]], a point of $X$ is a [[countably prime filter]] in $O(X)$;

## Properties

### Relation to $\sigma$-topological spaces

Every [[sigma-topological space|$\sigma$-topological space]] $X$ has a $\sigma$-frame of opens $O(X)$, and therefore gives rise to a $\sigma$-locale $X_L$.  For every [[continuous function]] $f\colon X \to Y$ between $\sigma$-topological spaces, the [[preimage|inverse image]] map $f^{-1}\colon O(Y) \to O(X)$ is a $\sigma$-frame homomorphism, so $f$ induces a continuous map $f_L\colon X_L \to Y_L$ of locales.  Thus we have a [[functor]] 

$(-)_L\colon$ $\sigma\mathrm{Top}$ $\to$ $\sigma\mathrm{Locale}$.

Conversely, if $X$ is any $\sigma$-locale, we define a **[[point]]** of $X$ to be a [[continuous map]] $1 \to X$.  Here $1$ is the [[terminal object|terminal]] $\sigma$-locale, which can be defined as the $\sigma$-locale $1_L$ corresponding to the terminal space.  Explicitly, we have $O(1) = 1^\Sigma$, the [[function set]] from $1$ to the [[initial object|initial]] $\sigma$-frame $\Sigma$, which is a $\sigma$-subframe of the [[frame of truth values]] $\Sigma \subseteq \Omega$ and which is the [[boolean domain]] in classical mathematics or in constructive mathematics when assuming the [[limited principle of omniscience]]. Since a $\sigma$-frame homomorphism $O(X) \to 1^\Sigma$ is determined by the preimage of $1$ (the [[true]] truth value), a point can also be described more explicitly as a _[[countably prime filter]]_: an upwards-closed subset $F$ of $O(X)$ such that $X \in F$ ($X$ denotes the [[top element]] of $O(X)$), if $U,V \in F$ then $U \cap V \in F$, and given a [[countable set|countable]] index set $I$, if $\bigcup_i U_i \in F$ then $U_i \in F$ for some $i \in I$.

The elements of $O(X)$ induce a [[sigma-topology|$\sigma$-topology]] on the set of points of $X$ in an obvious way, thereby giving rise to a $\sigma$-topological space $X_\Sigma$.  Any continuous map $f\colon X \to Y$ of locales induces a continuous map $f_\Sigma\colon X_\Sigma \to Y_\Sigma$ of spaces, so we have another functor 

$(-)_\Sigma\colon \sigma\mathrm{Locale} \to \sigma\mathrm{Top}$.

One finds that $(-)_L$ is [[left adjoint]] to $(-)_\Sigma$.

\begin{definition}
A [[sigma-topological space|$\sigma$-topological]] $X$ with $X \cong X_{L \Sigma}$ is called **[[sober sigma-topological space|sober]]**.

A $\sigma$-locale with $X \cong X_{\Sigma L}$ is called **[[spatial sigma-locale|spatial]]** or **topological**; one also says that it has **enough points**.
\end{definition}

## Related concepts 

* [[sigma-frame]]

* [[sigma-topological space]]

* [[locale]]

## References

* Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* [[Alex Simpson]], *Measure, randomness and sublocales*, Annals of Pure and Applied Logic, Volume 163, Issue 11, November 2012, Pages 1642-1659. ([doi:10.1016/j.apal.2011.12.014](https://doi.org/10.1016/j.apal.2011.12.014))

* [[Raquel Bernardes]], *Lebesgue integration on $\sigma$-locales: simple functions*, ([arXiv:2408.13911](https://arxiv.org/abs/2408.13911))

[[!redirects sigma-locale]]
[[!redirects sigma-locales]]

[[!redirects σ-locale]]
[[!redirects σ-locales]]