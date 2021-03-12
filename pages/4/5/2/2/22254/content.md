
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

By a _$G$-equivariant group_ we mean a [[group object]] [[internalization|internal]] to $G$-[[actions]], e.g. [[internalization|internal]] to [[G-sets]], [[G-spaces]], or [[G-manifolds]], etc.

Beware that the term "equivariant group" for this notion is non-standard; or rather: there is no other established term for this notion at all.
The term is meant to rhyme on the established terminology of _[[equivariant principal bundles]]_, in which context it serves to make nicely transparent the full (but often hidden) [[internalization|internal]] nature of the concept.


## Definition

We discuss  equivariant groups in/as [[topological spaces]], for definiteness and due to their relevance as models in [[equivariant homotopy theory]]. Much of the discussion generalizes, say to [[smooth manifolds]] or general [[toposes]].

\begin{defn}\label{TopologicalGSpaces}
(**topological $G$-spaces**)\linebreak

For $G$ be a [[topological group]] we write 
$$
  G Actions(TopologicalSpaces)
  \;\in\;
  Categories
$$ 
for the [[category]] of [[topological spaces]] equipped with [[continuous function|continuous]] $G$-[[actions]] and with $G$-[[equivariant function|equivariant]] [[continuous functions]] between them ("maps"); i.e. for the category of "[[G-spaces]]", often denote "$G Spaces$" or even $G Sp$ or similar.

In the following we refer to this $G$ as the _[[equivariance group]]_.
\end{defn} 

\begin{remark}
(**further conditions on the equivariance group**) \linebreak

For purposes of [[equivariant homotopy theory]] one needs (for instance for [[Elmendorf's theorem]] to hold) the [[topological group|topological]] [[equivariance group]] $G$ in Def. \ref{TopologicalGSpaces} to be that underlying a [[compact Lie group]], such as a [[finite group]]. But for the plain [[point-set topology]] of equivariant bundles, this condition is not necessary.
\end{remark}

\begin{defn}\label{EquivariantTopologicalGroup}
(**equivariant topological groups**) \linebreak

Given an [[equivariance group]] $G$ (Def. \ref{TopologicalGSpaces}), 
a _$G$-[[equivariant topological group]]_ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]]
  $$
    \mathcal{G}
    \;\in\;
    Groups
    \big(
      G Actions
      (
        TopologicalSpaces
      )
    \big)
    \,.
  $$
\end{defn}

\begin{prop}\label{EquivariantGroupsAsSemidirectProductGroups}
  (**Equivariant groups as semidirect product groups**) \linebreak

The [[category]] of $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) is [[equivalence of categories|equivalent]] to that of [[semidirect products]] $(-) \rtimes G$ regarded as [[pointed objects]] in the [[slice category]] of [[Groups]] over $G$:

$$
  \array{
    Groups
      \big(
        G Actions
        (
          TopologicalSpaces
        )
      \big)
    &
      \overset{
         \;\;
         \;\;
      }{\hookrightarrow}
    &
    Groups^{G/}_{/G}
    \\
    \mathcal{G}
    &\mapsto&
    \mathcal{G} \rtimes G
    \,.
  }
$$
\end{prop}

\begin{prop}\label{ActionsOfEquivariantGroupsAsSemidirectProductGroupActions}
  (**Equivariant group actions as semidirect product group actions**) \linebreak

  Under the identification of $G$-[[equivariant groups]] $\mathcal{G}$
  with [[semidirect product groups]] $\mathcal{G} \rtimes G$ 
  (Prop. \ref{EquivariantGroupsAsSemidirectProductGroups})
  we have an [[equivalence of categories|equivalence]] of their
  [[actions]]:
  $$
    \array{
      \mathcal{G}
      Actions
      \big(
        G Actions
        (
          TopologicalSpaces
        )
      \big)
      &\overset{\simeq}{
        \longrightarrow
      }&
      (
        \mathcal{G} \rtimes G
      )
      Actions( TopologicalSpaces )
    }
  $$
\end{prop}


## Related concepts

* [[equivariant bundle]]

* [category of G-sets -- For internal group actions](category+of+G-sets#InternalGroupActions)

\linebreak

[[!redirects equivariant groups]]

[[!redirects equivariant topological group]]
[[!redirects equivariant topological groups]]


