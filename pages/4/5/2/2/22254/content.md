
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
The term is meant to rhyme on the established terminology of _[[equivariant principal bundles]]_, in which context it serves to make nicely transparent the full (but often hidden) [[internalization|internal]] nature of the concept: equivariant principal bundles have, in general, equivariant groups as their [[structure groups]].


## Definition

We discuss  equivariant groups in/as [[topological spaces]], for definiteness and due to their relevance as models in [[equivariant homotopy theory]].  All of the discussion generalizes, say to [[smooth manifolds]] or general [[toposes]].

### Preliminaries

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
For $G$ be a [[topological group]] -- to be called the _[[equivariance group]]_ -- we write 
$$
  G Actions(TopologicalSpaces)
  \;\in\;
  Categories
$$ 
for the [[category]] whose 

* [[objects]] $(X,\rho)$ are [[topological spaces]] $X$ equipped with [[continuous function|continuous]] $G$-[[actions]]

  $$
    G \times X \overset{}{\longrightarrow} X
    \;\;\;\;\;\;
    \leftrightarrow
    \;\;\;\;\;\;
    G \overset{\rho}{\longrightarrow} Aut(X) \subset Maps(X,X)
    \,;
  $$

* [[morphisms]] are $G$-[[equivariant function|equivariant]] [[continuous functions]] between them ("maps"); i.e. for the category of "[[G-spaces]]", often denote "$G Spaces$" or even $G Sp$ or similar.

\end{defn} 

\begin{remark}
(**further conditions on the equivariance group**)
\linebreak
For purposes of [[equivariant homotopy theory]] one typically assumes the [[topological group|topological]] [[equivariance group]] $G$ in Def. \ref{TopologicalGSpaces} to be that underlying a [[compact Lie group]], such as a [[finite group]] (as that guarantees that [[G-CW-complexes]] are well-behaved and that the [[equivariant Whitehead theorem]] holds). But for the plain [[point-set topology]] of equivariant bundles, this condition is not necessary.
\end{remark}


\begin{remark}\label{GSpacesAreCartesianMonoidal}
(**[[topological G-spaces]] are [[Cartesian monoidal category|cartesian monoidal]]**)
  The category of [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}) is a [[Cartesian monoidal category]]: The [[Cartesian product]] of two [[topological G-spaces]] $(X_i, \rho_i)$ is the underlying [[product topological space]] equipped with the [[diagonal action]] by $G$:
$$
  (X_1, \rho_1)
  \times
  (X_2, \rho_2)
  \;=\;
  \Big(
    X_1 \times X_2,
   \,
   \rho_{1,2}(g)(x_1,x_2)
   \,=\,
   \big(
     \rho_1(x_1), \rho_2(x_2)
   \big)
  \Big)
  \,.
$$
\end{remark}
In a [[Cartesian monoidal category]] there is a notion of [[internalization|internal]] [[group objects]]:

### Equivariant groups

\begin{defn}\label{EquivariantTopologicalGroup}
(**equivariant topological groups**) 
\linebreak
Given an [[equivariance group]] $G$ (Def. \ref{TopologicalGSpaces}), 
a _$G$-[[equivariant topological group]]_ $(\mathcal{G}, \alpha)$ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}):
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
Since the [[forgetful functor]] from [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}) to underlying [[topological spaces]]
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
[[preserved limit|preserves]] [[Cartesian products]] (explicitly so by Remark \ref{GSpacesAreCartesianMonoidal}), it preserves [[group objects]] and hence sends $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) to underlying plain [[topological groups]]:
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



## Properties

### Equivalence with semidirect products with $G$

\begin{prop}\label{EquivariantGroupsAsSemidirectProductGroups}
  (**Equivariant groups as semidirect product groups**) 
\linebreak
The [[category]] of $G$-equivariant topological groups (Def. \ref{EquivariantTopologicalGroup}) is [[equivalence of categories|equivalent]] to that of [[semidirect product groups]] of the form $(-) \rtimes G$ and regarded as [[pointed objects]] in the [[slice category]] of [[Groups]]:

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
Here $\mathcal{G} \rtimes_\alpha G$ is regarded as equipped with the homomorphisms
$$
  \array{
    G
    &\longrightarrow&
    \mathcal{G} \times_\alpha G
    &\longrightarrow&
    G
    \\
    && 
    (\gamma,g) &\mapsto& g
    \\
    g &\mapsto& (e_{\mathcal{g}},g)
    \,.
  }
$$

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

\[
  \label{FunctorialAssignmentOfSemidirectProductGroupsToEquivariantGroups}
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
\]

is clearly [[functor|functorial]]. 

It remains to see that this functor is a [[full subcategory]]-inclusion, hence a [[fully faithful functor]], hence that  it is a [[bijection]] on [[hom-sets]] for any [[pair]] of [[objects]]: 

But by (eq:FunctorialAssignmentOfSemidirectProductGroupsToEquivariantGroups) the homomorphisms of [[semidirect product groups]] in its [[image]] are precisely those of the product form $\phi \times id_G$, and this is exactly the form of the homomorphisms between semidirect product groups that is picked out by [[slice category|slicing over]] [[undercategory|and under]] $G$ (noticing that group homomorphisms out of 
$\mathcal{G} \rtimes_\alpha G$ 
are fixed by their restriction to 
$\mathcal{G} \times \{ e_G \}$ 
and 
$\{ e_{\mathcal{G}} \} \times G$
).
\end{proof}


### Equivariant group actions
 {#EquivariantGroupActions}

\begin{prop}\label{ActionsOfEquivariantGroupsAsSemidirectProductGroupActions}
  (**equivariant group actions as semidirect product group actions**) \linebreak
  Under the identification from Prop. \ref{EquivariantGroupsAsSemidirectProductGroups} of $G$-[[equivariant groups]] 
  $\big(\mathcal{G}, \alpha \big)$
  with [[semidirect product groups]] $\mathcal{G} \rtimes_\alpha G$,
  we have an [[equivalence of categories|equivalence]] of their
  [[actions]], given by:
  \[
    \label{EquivalenceBetweenEquivariantActionsAndSemidirecProductActions}
    \array{
      \mathcal{G}
      Actions
      \big(
        G Actions
        (
          TopologicalSpaces
        )
      \big)
      &
      \overset{\simeq}{
        \longrightarrow
      }
      &
      (
        \mathcal{G} \rtimes G
      )
      Actions( TopologicalSpaces )
      \\
      (
        \mathcal{G}, \alpha
      )
      \overset{
        R
      }{
        \to
      }
      Aut
      \big(
        (X, \rho)  
      \big)
      &\mapsto&
      \mathcal{G} \rtimes_\alpha G
      \overset{
        (R,\rho)
      }{\longrightarrow}
      Aut(X)
    }
  \]
  with
  $$
    \underset{\gamma,g,x}{\forall}
    \;\;\;
    (R,\rho)(\gamma, g)(x)
    \;\coloneqq\;
    R(\gamma)\big( \rho(g)(x) \big)
    \,.
  $$
\end{prop}

\begin{proof}

We observe that the given formula in fact establishes a [[bijection]] between the two kinds of actions.

First, it is clear that;

1. the action property of $\rho$ is equivalently the action property of $(R,\rho)$ on elements of the form $(e, g)$;

1. the action-property of $R$ on the underlying topological spaces is equivalently the action property of $(R,\rho)$ on elements of the form $(\gamma,e)$

and that the full action property of $(R,\rho)$ is equivalent to its restriction to these two cases and to the mixed case:

$$
  \underset{
    \gamma,g,x
  }{\forall}
  \;\;\;
  (R,\rho)
  \big(
    \underset{
      \big(
        \alpha(g)(\gamma),
        g
      \big)
    }{
      \underbrace{
        (e,g) \cdot (\gamma,e)
      }
    }
  \big)
  (x)
  \;=\;
  (R,\rho)(e,g)
  \big(
    (R,\rho)(\gamma,e)
    (x)
  \big)
  \,.
$$

Now by definition of $(R,\rho)$, this mixed action condition is equivalent to the condition

$$
  \underset{
    \gamma,g,x
  }{\forall}
  \;\;\;
  R
  \big(
    \alpha(g)(\gamma)
  \big)
  \big(
    \rho(g)(x)
  \big)
  \;=\;
  \rho(g)
  \big(
    R(\gamma)(x)
  \big)
  \,.
$$

But this is equivalently the condition of $G$-equivariance on $R$.

In conclusion, $(R,\rho)$ is an action of the semidirect product group $\mathcal{G} \rtimes_\alpha G$ on $X$ iff $R$ is a $G$-equivariant action of $\mathcal{G}$ on $X$. 

This implies immediately that the condition for a map $X \to X$ to be an action homomorphisms on both sides are the same. 

And so the functor (eq:EquivalenceBetweenEquivariantActionsAndSemidirecProductActions) is in fact an [[isomorphism]] on both objects as well as morphisms, hence in particular an [[equivalence of categories]],
\end{proof}

## Related concepts

* [[equivariant bundle]]

* [category of G-sets -- For internal group actions](category+of+G-sets#InternalGroupActions)

* [[equivariance group]]

\linebreak




[[!redirects equivariant groups]]

[[!redirects equivariant topological group]]
[[!redirects equivariant topological groups]]


