
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

## Background

+-- {: .num_defn #LocallyCompactSpace}
###### Definition
**([[locally compact topological space]])**

A [[topological space]] $X$ is called _[[locally compact topological space|locally compact]]_
if for every point $x \in X$ and every [[open neighbourhood]] $U_x \supset \{x\}$
there exists a smaller open neighbourhood $V_x \subset U_x$ whose [[topological closure]]
is [[compact topological space|compact]] and still contained in $U$:

$$
  \{x\} \subset V_x \subset \underset{\text{compact}}{Cl(V_x)} \subset U_x
  \,.
$$

=--

## Statement and proof

+-- {: .num_prop}
###### Proposition
**(proper maps to locally compact spaces are closed)**

Let

1. $(X,\tau_X)$ be a [[topological space]],

1. $(Y,\tau_Y)$ a [[locally compact topological space]] according to def. \ref{LocallyCompactSpace},

1. $f \colon X \to Y$ a [[continuous function]].

Then:

If $f$ is a [[proper map]], then it is a [[closed map]].

=--



+-- {: .proof}
###### Proof

Let $C \subset X$ be a [[closed subset]]. We need to show that every $y \in Y \backslash f(C)$ has an open neighbourhood $U_y \supset \{y\}$ not intersecting $f(C)$ (by [this prop.](Introduction+to+topology+--+1#UnionOfOpensGivesClosure)).

By local compactness of $(Y,\tau_Y)$ (def. \ref{LocallyCompactSpace}), $y$ has an open neighbourhood $V_y$ whose topological closure $Cl(V_y)$ is compact. Hence since $f$ is proper, also $f^{-1}(Cl(V_y)) \subset X$ is compact. Then also the intersection $C \cap f^{-1}(Cl(V_y))$ is compact, and hence so is 

$$
  f(C \cap f^{-1}(Cl(V_y)))
  =
  f(C) \cap (Cl(V))
  \;
  \subset Y
  \,.
$$ 

This is also a [[closed subset]], since [[compact subspaces of Hausdorff spaces are closed]]. Therefore

$$
  U_y \coloneqq V_y \backslash ( f(C) \cap (Cl(V_y)) ) = V_y \backslash f(C)
$$

is an open neighbourhod of $y$ not intersecting $f(C)$.

=--

## Related statements

* [[injective proper maps to locally compact spaces are equivalently the closed embeddings]]

* [[closed injections are embeddings]]

* [[maps from compact spaces to Hausdorff spaces are closed and proper]]

* [[CW-complexes are Hausdorff spaces]]

* [[Hausdorff spaces are sober]], [[schemes are sober]]

* [[continuous image of a compact space is compact]]

* [[closed subsets of compact spaces are compact]]

* [[compact subspaces of Hausdorff spaces are closed]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]

* [[quotient projections out of compact Hausdorff spaces are closed precisely if the codomain is Hausdorff]]

* [[paracompact Hausdorff spaces are normal]]

* [[paracompact Hausdorff spaces equivalently admit subordinate partitions of unity]]
