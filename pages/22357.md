
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A common condition on [[subgroups]] of a [[topological group]] is that they be [[closed subspaces|closed]]. 

This is typically required in [[equivariant differential topology]]/[[equivariant homotopy theory]], for instance in the definition of the [[orbit category]].

## Definition

\begin{defn}\label{ClosedSubgroup}
**(closed subgroup)**\linebreak

A [[topological group|topological]] [[subgroup]] $H \subset G$ of a [[topological group]] $G$ is called a _closed subgroup_ if as a [[topological subspace]] it is a [[closed subspace]].

\end{defn}

## Examples

### Stabilizer subgroup

\begin{prop}\label{StabilizerSubgroupsOfContinuousActionsOnT1SpacesAreClosed}
**([[stabilizer subgroups]] of [[topological G-space|continuous actions]] on [[T1-spaces]] are closed)**
  Let $G$ be a [[topological group]] and let $X \in G Actions(TopologicalSpaces)$ a [[topological G-space]] whose underlying [[topological space]] is a [[T1-space]], e.g. a [[Hausdorff space]].

Then for all [[points]] $x \in X$  their [[isotropy groups]], hence their [[stabilizer subgroup]]

  $$
    G_x 
    \;\coloneqq\;
    Stab_G(x)
    \;\subset\;
    G
    \,,
  $$

  is a closed subgroup (Def. \ref{ClosedSubgroup}).

\end{prop}
\begin{proof}
  We may understand $G_x$ as the [[pre-image]] 

$$
  G_x 
  \;\simeq\;
  \big(
    \rho(-)(x)
  \big)^{-1}
  \big(
    \{x\}
  \big)
$$

of the [[singleton set|singleton]] [[subset]] $\{x\} \subset X$ under the [[continuous function]] which sends $x$ to its [[image]] under the given $G$-[[action]]:

$$
  \array{
    G 
    &\overset{\rho(-)(x)}{\longrightarrow}&
    X
    \\
    g &\mapsto& g \cdot x
    \,.
  }
$$

Since this is a [[continuous function]], and since $x \in X$ is a [[closed point]] by assumption that $X$ is [[T1 topological space|T1]], hence since $\{x\} \subset X$ is a [[closed subset]], it follows that $G_x \subset G$ is a closed subset, since [continuous preimages of closed subsets are closed](continuous+map#PropertiesPreservedByAContinuousFunction).


\end{proof}


### Localic subgroups

Any localic subgroup of a [[localic group]] is closed (see [this Theorem](https://ncatlab.org/nlab/show/localic+group#LocalicSubgroupsAreClosed)).

## Related concepts

* [[maximal compact subgroup]]

* [[locally compact topological group]]

* [[compact Lie group]]


[[!redirects closed subgroups]]