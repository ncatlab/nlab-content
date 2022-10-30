

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Ordinary homology_ is [[generalized homology]] with respect to an [[Eilenberg-MacLane spectrum]] $H A$, and often understood over $H \mathbb{Z}$. 

Equivalently this is computed by _[[singular homology]]_ with [[coefficients]] in $A$.


## Properties

### Relation to homotopy groups

Ordinary homology with [[coefficients]] in $\mathbb{Z}$ of a [[topological space]] $X$  serves to approximate the [[homotopy groups]] of $X$.

See for instance at _[[Hurewicz theorem]]_

### Description in terms of higher linear algebra

We discuss ([[twisted cohomology|twisted]]) ordinary homology and [[ordinary cohomology]] in terms of sections of [[(∞,1)-module bundles]] over the [[Eilenberg-MacLane spectrum]].

Let $k$ be a [[commutative ring]]. Write 

$$
  H k \in CRing_\infty
$$

for the [[Eilenberg-MacLane spectrum]] of $k$, canonically regarded as an [[E-∞ ring]]. Write

$$
  (H k) Mod \in (\infty,1)Cat
$$

for the [[(∞,1)-category of (∞,1)-modules]] over $H k$.

+-- {: .num_prop #DoldKan}
###### Proposition

There is an [[equivalence of (∞,1)-categories]]

$$
 (H k)Mod \simeq L_{qi} Ch_\bullet(k Mod)
$$

between the [[(∞,1)-category of (∞,1)-modules]] over the [[Eilenberg-MacLane spectrum]] $H k$ and the [[simplicial localization]] of the [[category of unbounded chain complexes]] of ordinary (1-categorical) $k$-[[modules]].

=--

This is the statement of the _[[stable Dold-Kan correspondence]]_, see at _[(∞,1)-category of (∞,1)-modules -- Properties -- Stable Dold-Kan correspondence](%28infinity%2C1%29-module#StableDoldKanCorrespondence)_.
  
+-- {: .num_defn}
###### Definition

Let $X$ be a [[topological space]] and write $\Pi(X) \in $ [[∞Grpd]] for its underlying [[homotopy type]] (its [[fundamental ∞-groupoid]]). Then we say that an [[(∞,1)-functor]]

$$
  \Pi(X) \to (H k) Mod
$$

is (the [[higher parallel transport]]) a _[[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundle]]_ over $X$, or a _[[local system]]_ of $H k$-[[(∞,1)-modules]] over $X$.

=--


+-- {: .num_prop}
###### Proposition
**([[Riemann-Hilbert correspondence]])**

If $X$ is an [[orientation|oriented]] [[closed manifold]], then there is an [[equivalence of (∞,1)-categories]]

$$
  [\Pi(X), (H k)Mod]
  \simeq
  (T X)Mod
$$

between [[flat (∞,1)-bundle|flat]] [[(∞,1)-module bundles]]/[[local systems]] and [[L-∞ algebroid representations]] of the [[tangent Lie algebroid]] of $X$. From right to left the equivalece is established by sending an [[L-∞ algebroid representation]] given (as discussed there) by a flat $\mathbb{Z}$-graded connection on bundles of chain complexes (via prop. \ref{DoldKan}), to its [[higher holonomy]] defined in terms of [[iterated integrals]].

=--

This is the main theorem in ([Block-Smith 09](#BlockSmith09)).


## Related concepts

* [[ordinary cohomology]]

## References

The [[Riemann-Hilbert correspondence]]/[[de Rham theorem]] for $K k$-modules is established in 

* [[Jonathan Block]], Aaron Smith, _A Riemann--Hilbert correspondence for infinity local systems_ ([arXiv:0908.2843](http://arxiv.org/abs/0908.2843))
 {#BlockSmith09}

