+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Statement

+-- {: .num_prop #MapsFromCompactSpacesToHausdorffSpacesAreClosed}
###### Proposition
**(maps from compact spaces to Hausdorff spaces are closed and proper)**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that 

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

Then $f$ is 

1. a [[closed map]];

1. a [[proper map]].

=--

+-- {: .proof}
###### Proof

For the first statement, we need to show that if $C \subset X$ is a [[closed subset]] of $X$, then also $f(C) \subset Y$ is a closed subset of $Y$.

Now 

1. since [[closed subsets of compact spaces are compact]] it follows that $C \subset X$ is also compact;

1. since [[continuous images of compact spaces are compact]] it then follows that $f(C) \subset Y$ is compact;

1. since [[compact subspaces of Hausdorff spaces are closed]] it finally follow that $f(C)$ is also closed in $Y$.

For the second statement we need to show that if $C \subset Y$ is a [[compact topological space|compact subset]], then also its [[pre-image]] $f^{-1}(C)$ is compact.

Now 

1. since [[compact subspaces of Hausdorff spaces are closed]] it follows that $C \subset Y$ is closed;

1. since [[pre-images]] under continuous of closed subsets are closed, also $f^{-1}(C) \subset X$ is closed;

1. since [[closed subsets of compact spaces are compact]], it follows that $f^{-1}(C)$ is compact.

=--

## Consequences

+-- {: .num_cor #ContinuousBijectionsFromCompactSpacesToHausdorffSpacesAreHomeomorphisms}
###### Corollary ######
**(continuous bijections from compact spaces to Hausdorff spaces are homeomorphisms)**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that 

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

1. $f \;\colon\; X \longrightarrow Y$ is a [[bijection]] of [[sets]].

Then $f$ is a [[homeomorphism]], i. e. its [[inverse function]] $Y \to X$ is also a [[continuous function]].

In particular then both $(X,\tau_X)$ and $(Y, \tau_Y)$ are [[compact Hausdorff spaces]].

=--

+-- {: .proof}
###### Proof

Write $g \colon Y \to X$ for the [[inverse function]] of $f$. 

We need to show that $g$ is continuous, hence that for $U \subset X$ an [[open subset]], then also its [[pre-image]] $g^{-1}(U) \subset Y$ is open in $Y$.
By passage to [[complements]], this is equivalent to the statement that for $C \subset X$ a [[closed subset]] then the [[pre-image]] $g^{-1}(C) \subset Y$ is also closed in $Y$. 

But since $g$ is the [[inverse function]] to $f$, its [[pre-images]] are the [[images]] of $f$. Hence the last statement above equivalently says that $f$ sends closed subsets to closed subsets. This is true by prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed}.

=--


+-- {: .num_remark}
###### Remark

The idea captured by corollary \ref{ContinuousBijectionsFromCompactSpacesToHausdorffSpacesAreHomeomorphisms} is that [[Hausdorff topological space|Hausdorffness]] is about having "enough" [[open sets]] whilst [[compact topological space|compactness]] is about having "not too many". Thus a [[compact Hausdorff space]] has both "enough" and "not too many". This theorem says that both conditions are at their limit: if we try to have more open sets, we lose compactness. If we try to have fewer open sets, we lose Hausdorffness.

=--

## Applications

### In Cohomotopy and Cobordism theory
  {#InCohomotopyAndCobordism}

[[Pontryagin's theorem]] establishes a [[bijection]]

$$
  \pi^n
  \big(
    X^d
  \big)
  \,=\,
  \pi_0 Maps
  \big(
    X^d, S^n
  \big)
  \overset
  {\simeq}{
    \;\;
    \longrightarrow
    \;\;
  }
  Cob^n_{Fr}
  \big(
    X^d
  \big)
$$

between 

1. the $n$-[[Cohomotopy]] set of a _[[closed manifold|closed]]_ (hence: [[compact topological space|compact]]) [[smooth manifold]] $X^d$;

1. the [[cobordism classes]] of its [[normally framed submanifolds]] of [[codimension]] $n$;

by taking the [[homotopy class]] of any [[map]] $[X \overset{c}{\to}S^n]$ into the [[n-sphere]] to the [[preimage]] of any [[regular point]] (say $\{0\} \subset S^n$, for definiteness) of a [[smooth function|smooth]] representative $c$:

$$
  \Sigma_c \;\coloneqq\; c^{-1}\big( \{0\} \big)
  \,.
$$

To show that this construction is indeed [[injection|injective]], one needs that, similarly, the [[pre-image]] of any regular point of a [[smooth homotopy]]

$$
  X^d \times [0,1]
  \overset{\eta}{\longrightarrow} 
  S^d
$$

between two such smooth representatives $c_0, c_1$ is a [[cobordism]] between $\Sigma_{c_0}$ and $\Sigma_{c_1}$. But for a subspace of $X^d \times [0,1]$ to constitute a [[cobordism]] between submanifolds of $X^d$ it is necessary that its [[projection]] onto the $[0,1]$-factor is compact.

That this is implied here is guaranteed by the assumption that $X^d$ is [[closed manifold|closed]], hence [[compact topological space|compact]], [so that](compact+topological+space#ProductOfCompactSpacesIsCompact) also the [[product topological space|product space]] $X^d \times [0,1]$ is compact:

With this and since the [[n-sphere]] is, of course, [[Hausdorff space|Hausdorff]], Prop. \ref{MapsFromCompactSpacesToHausdorffSpacesAreClosed} implies that the maps $c_i$ and $\eta$ above are all [[proper maps|proper]], hence that the corresponding pre-images (of [[singleton]], hence compact, subspaces) are indeed compact, so that in particular the projection of the pre-image of $\eta$ to $[0,1]$ is compact (since [[continuous images of compact spaces are compact]]).



## Related statements

* [[continuous metric space valued function on compact metric space is uniformly continuous]]

* [[proper maps to locally compact spaces are closed]]

* [[CW-complexes are paracompact Hausdorff spaces]]

* [[Hausdorff implies sober]]

* [[continuous image of a compact space is compact]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff]]

* [[paracompact Hausdorff spaces are normal]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]

[[!redirects map from compact space to Hausdorff space]]
[[!redirects map from compact space to Hausdorff space]]
[[!redirects map from a compact space to a Hausdorff space]]
[[!redirects maps from a compact space to a Hausdorff space]]
[[!redirects maps from compact spaces to Hausdorff spaces]]

[[!redirects continuous bijections from compact spaces to Hausdorff spaces are homeomorphisms]]
