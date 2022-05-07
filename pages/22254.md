
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

For $G$ a fixed [[group]], to be called the _[[equivariance group]]_, then
by a _$G$-equivariant group_ we mean a [[group object]] [[internalization|internal]] to $G$-[[actions]], e.g. [[internalization|internal]] to [[G-sets]], [[G-spaces]], or [[G-manifolds]], etc.

Beware that the term "equivariant group" for this notion is non-standard; or rather: there is no other established term for this notion at all.
The term is meant to rhyme on the established terminology of _[[equivariant principal bundles]]_, in which context it serves to make nicely transparent the full (but often hidden) [[internalization|internal]] nature of the concept.


## Definition

We discuss  equivariant groups in/as [[topological spaces]], for definiteness and due to their relevance as models in [[equivariant homotopy theory]].  Much of the discussion generalizes, say to [[smooth manifolds]] or general [[toposes]].

\begin{defn}
(**convenient category of topological spaces**)
\linebreak
We write
$$
  TopologicalSpaces
  \;\in\;
  Categories
$$
for any [[convenient category of topological spaces]] whose [[mapping space]] serves as an [[internal hom]], such as

* [[D-topological spaces]]

* [[compactly generated topological spaces]].

This means in particular that for $X,Y,A \,\in\, TopologicalSpaces$, we have a [[natural bijection]]

\[
  \label{HomAdjunctInTopologicalSpaces}
  X \times Y
    \longrightarrow
  A
  \;\;\;\;\;\;\;
  \overset{adjuncts}{\leftrightarrow}
  \;\;\;\;\;\;\;
  X 
    \longrightarrow 
  Maps(Y,A)
\]

between [[maps]] (meaning: [[continuous functions]]) out of the [[product topological space]] with $Y$ and maps into the [[mapping space]].
  
\end{defn}

\begin{defn}\label{TopologicalGSpaces}
(**topological $G$-spaces**)
\linebreak
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
(**further conditions on the equivariance group**)
\linebreak
For purposes of [[equivariant homotopy theory]] one typically assumes the [[topological group|topological]] [[equivariance group]] $G$ in Def. \ref{TopologicalGSpaces} to be that underlying a [[compact Lie group]], such as a [[finite group]] (as that guarantees that [[G-CW-complexes]] are well-behaved and that the [[equivariant Whitehead theorem]] holds). But for the plain [[point-set topology]] of equivariant bundles, this condition is not necessary.
\end{remark}

\begin{defn}\label{EquivariantTopologicalGroup}
(**equivariant topological groups**) 
\linebreak
Given an [[equivariance group]] $G$ (Def. \ref{TopologicalGSpaces}), 
a _$G$-[[equivariant topological group]]_ $(\mathcal{G}, \alpha)$ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]]
  $$
    \big(
      \mathcal{G},
      \,
      \alpha
    \big)
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
(See Prop. \ref{EquivariantGroupsAsSemidirectProductGroups} below for the choice of notation used here.)
\begin{remark}\label{UnderlyingTopologicalGroupOfAnEquivariantTopologicalGroup}
Since the [[forgetful functor]]
$$
  \array{
    G Actions
    (
      TopologicalSpaces
    )
   &
     \overset{
     }{\longrightarrow}
   &
   TopologicalSpaces
  }  
$$
[[preserved limit|preserves]] [[Cartesian products]], it sends $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) to underlying plain [[topological groups]]
\[
  \label{ForgetfulFunctorFromEquivariantTopologicalGroupsToTopologicalGroups}
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
     }{\longrightarrow}
   &
   Groups
   (
     TopologicalSpaces
   )
   \\
   \big(
     \mathcal{G}
     ,
     \alpha
   \big)
   &\mapsto&
   \mathcal{G}
   \,.
  }  
\]
\end{remark}

\begin{prop}\label{EquivariantGroupsAsSemidirectProductGroups}
  (**Equivariant groups as semidirect product groups**) 
\linebreak
The [[category]] of $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) is [[equivalence of categories|equivalent]] to that of [[semidirect products]] $(-) \rtimes G$ regarded as [[pointed objects]] in the [[slice category]] of [[Groups]] over $G$:

\[
  \label{EquivalenceOfEquivariantTopologicalGroupsToSemidirectProductTopGroups}
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
    \big(
      \mathcal{G},
      \alpha
    \big)
    &\mapsto&
    \mathcal{G} \rtimes_{\alpha} G
    \,.
  }
\]
\end{prop}

\begin{proof}
  This is a straightforward matter of unwinding the definitions:

First to see that we have a [[functor]] as claimed:

A [[group object]] in $G Actions(TopologicalSpaces)$ is, by definition, a plain [[topological group]] $\mathcal{G}$ whose underlying topological space is equipped with a continuous $G$-[[action]] and such such this $G$-action preserves all its group operations. In other words, this is a group $\mathcal{G}$ and a [[homomorphism]] 
$\alpha \;\colon\;G \longrightarrow Aut_{Grp}(\mathcal{G})$ to the group-[[automorphism group]] (whose [[internal hom|hom]]-[[adjunct]] (eq:HomAdjunctInTopologicalSpaces) is [[continuous function|continuous]]).

This is exactly the data that determines the [[semidirect product group]]

\[
  \label{ASemidirectProductGroup}
 \mathcal{G} \rtimes_\alpha G
  \;\;
   \coloneqq
  \;\;
  \Big(
    \mathcal{G} \times G
    \,,
    \;
    (\gamma_1, g_1) \cdot (\gamma_2, g_2)
    \;\coloneqq\;
    \big(
      \gamma_1 \cdot \alpha(g_1)(\gamma_2) 
      ,\,
      g_1 \cdot g_2
    \big)
  \Big)
  \,.
\]

Moreover, a [[homomorphism]] of equivariant groups $(\mathcal{G}_1, \alpha_1) \longrightarrow (\mathcal{G}_2, \alpha_2)$ is a continuous [[group homomorphism]] $\phi \,\colon\, \mathcal{G}_1 \longrightarrow \mathcal{G}_2$ whose underlying map is $G$-[[equivariant function|equivariant]] in that

$$
  \underset{
    g \in G
  }{\forall}
  \;\;
  \;\;
  \phi \circ \alpha_1(g) \;=\; \alpha_2(g) \circ \phi
  \,.
$$

By (eq:ASemidirectProductGroup) this means that $\phi$ induces a [[group homomorphism]] of [[semidirect product groups]] of the form

$$
  \array{
    \mathcal{G}_1 \rtimes_{\alpha_1} G
    &
      \overset{
      }{\longrightarrow}
    &
    \mathcal{G}_2 \rtimes_{\alpha_2} G
    \\
    \mathcal{G}_1 \times G
    &
      \overset{
        \phi \times id_G
      }{\longrightarrow}
    &
    \mathcal{G}_2 \times G    
  }
$$

This construction

$$
  \array{
    (\mathcal{G}_1, \alpha_1)
    &&
    &&
    \mathcal{G}_1 \rtimes_{\alpha_1} G
    \\
    \big\downarrow  
     {}^{_{\mathrlap{\phi}}}
    &&
      \mapsto
    &&
    \big\downarrow  
     {}^{_{\mathrlap{\phi \times id_G}}}
    \\
    (\mathcal{G}_2, \alpha_2)    
    &&
    &&
    \mathcal{G}_2 \rtimes_{\alpha_2} G
  }
$$

is clearly functorial. 

It remains to see that it is a [[bijection]] on [[hom-sets]]. But by construction, the homomorphisms of [[semidirect product groups]] in its [[image]] are precisely those of the product for $\phi \times id_G$, and this is exactly the form of the homomorphisms that is picked out by [[slice category|slicing over]] [[undercategory|and under]] $G$.
\end{proof}

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

* [[equivariance group]]

\linebreak

[[!redirects equivariant groups]]

[[!redirects equivariant topological group]]
[[!redirects equivariant topological groups]]


