
> This entry is about the concept in  [[topology]]. For variants see at _[[proper morphism]]_.

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

+-- {: .num_defn #ProperContinuous}
###### Definition
**([[proper maps]])**

A [[continuous function]] $f  \colon (X, \tau_X) \to (Y, \tau_Y)$
is called _[[proper map|proper]]_ if for all [[compact topological space|compact]] [[topological subspace|subspaces]] $C$ of $Y$, the [[pre-image]] $f^{-1}(C)$ is [[compact topological space|compact]] in $X$.

=--

## Properties

+-- {: .num_prop #MapsFromCompactSpacesToHausdorffSpacesAreClosed}
###### Proposition
**([[maps from compact spaces to Hausdorff spaces are closed and proper]])**

Let $f \colon (X, \tau_X) \longrightarrow (Y, \tau_Y)$ be a [[continuous function]] between [[topological spaces]] such that

1. $(X,\tau_X)$ is a [[compact topological space]];

1. $(Y,\tau_Y)$ is a [[Hausdorff topological space]].

Then $f$ is

1. a [[closed map]];

1. a [[proper map]] (def. \ref{ProperContinuous}))

=--

+-- {: .num_defn #LocallyCompactSpace}
###### Definition
**([[locally compact topological space]])**

A [[topological space]] $X$ is called _[[locally compact topological space|locally compact]]_
if for every point $x \in X$ and every [[open neighbourhood]] $U_x \supset \{x\}$
there exists a smaller open neighbourhood $V_x \subset U_x$ whose [[topological closure]]
is [[compact topological space|compact]] (def. \ref{CompactTopologicalSpace}) and still contained in $U$:

$$
  \{x\} \subset V_x \subset \underset{\text{compact}}{Cl(V_x)} \subset U_x
  \,.
$$

=--


+-- {: .num_prop}
###### Proposition
**([[proper maps to locally compact spaces are closed]])**

Let

1. $(X,\tau_X)$ be a [[topological space]],

1. $(Y,\tau_Y)$ a [[locally compact topological space]] according to def. \ref{LocallyCompactSpace},

1. $f \colon X \to Y$ a [[continuous function]].

Then:

If $f$ is a proper map (def. \ref{ProperContinuous}), then it is a [[closed map]].

=--




## Related concepts

* [[locally proper map]]

* [[proper morphism]]

* [[open map]], [[closed map]]

* [[proper group action]]

* [[proper homotopy]]

* [[proper equivariant homotopy theory]]

[[!redirects proper maps]]
[[!redirects proper continuous map]]
[[!redirects proper continuous maps]]

[[!redirects proper continuous function]]
[[!redirects proper continuous functions]]

