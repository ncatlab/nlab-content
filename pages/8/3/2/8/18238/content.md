
> This page is about the concept in [[topology]]. For the more general concept see at _[[closed morphism]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn #OpenMap}
###### Definition
**([[open maps]] and [[closed maps]])**

A [[continuous function]] $f \colon (X,\tau_X) \to (Y, \tau_Y)$ is called

*  an _[[open map]]_ if the [[image]] under $f$ of an [[open subset]] of $X$ is an open subset of $Y$;

* a _[[closed map]]_ if the [[image]] under $f$ of a [[closed subset]] of $X$ (def. \ref{ClosedSubset}) is a closed subset of $Y$.

=--

## Examples

+-- {: .num_example}
###### Example
**([[image]] projections of [[open map|open]]/[[closed maps]] are themselves open/closed)**

If a [[continuous function]] $f \colon (X,\tau_X) \to (Y,\tau_Y)$ is an [[open map]] or [[closed map]] (def. \ref{OpenMap})
then so its its [[image]] projection $X \to f(X) \subset Y$, respectively, for $f(X) \subset Y$ regarded with its
[[subspace topology]].

=--

+-- {: .proof}
###### Proof

If $f$ is an open map, and $O \subset X$ is an open subset, so that $f(O) \subset Y$ is also open in $Y$, then, since $f(O) = f(O) \cap f(X)$, it is also still open in the subspace topology, hence $X \to f(X)$ is an open map.

If $f$ is a closed map, and $C \subset X$ is a closed subset so that also $f(C) \subset Y$ is a closed subset, then the [[complement]] $Y \backslash f(C)$ is open in $Y$ and  hence $(Y \backslash f(C)) \cap f(X) = f(X) \backslash f(C)$ is open in the subspace topology, which means that $f(C)$ is closed in the subspace topology.


=--

+-- {: .num_prop #MapsFromCompactSpacesToHausdorffSpacesAreClosed}
###### Proposition
**([[maps from compact spaces to Hausdorff spaces are closed and proper]])**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

Then $f$ is

1. a [[closed map]] (def. \ref{OpenMap});

1. a [[proper map]].

=--

+-- {: .num_prop}
###### Proposition
**([[proper maps to locally compact spaces are closed]])**

Let

1. $(X,\tau_X)$ be a [[topological space]],

1. $(Y,\tau_Y)$ a [[locally compact topological space]] according to def. \ref{LocallyCompactSpace},

1. $f \colon X \to Y$ a [[continuous function]].

Then:

If $f$ is a [[quasi-proper map]], then it is a [[closed map]].

=--



## Related concepts

* [[closed morphism]]

* [[embedding of topological spaces]]

* [[open map]], [[proper map]]

[[!redirects closed maps]]
[[!redirects closed mapping]]
[[!redirects closed mappints]]
