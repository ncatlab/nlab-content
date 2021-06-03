


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
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
 {#Idea}

Generally, for $G$ some [[group]], a _$G$-equivariant bundle_ is a [[bundle]], specifically a [[fiber bundle]] ([[principal bundle]], [[vector bundle]], etc.) all whose component spaces (total space $E$, base space $X$, [[fiber]] $F$, but also possibly the [[structure group]] $\Gamma$) are equipped with $G$-[[actions]], such that all structure morphisms (in particular the projection $E \overset{p}{\to} X$, but also the $\Gamma$-[[action]] for [[principal bundles]] etc.)  are $G$-[[equivariant functions]].

In short, this should mean ([[schreiber:TED cohomology|GSS 21]], Def. \ref{EquivariantPrincipalBundles} below) that $G$-equivariant (fiber-, principal-,...) bundles are (fiber-, principal, ...) bundles _[[internalization|internal]]_ to a [[category]] of [[G-spaces]] (e.g. [[topological G-spaces]], [[G-manifolds]] but also [[G-sets]] etc.).

While the existing literature does not state the definition of equivariant bundles via [[internalization]], one sees (Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles} below) that the explicit definition in [tom Dieck 69](#tomDieck69), [tom Dieck 87, Sec. I.8](#tomDieck87) (for the case of [[principal bundles]]) is the equivalent external description, _including_, thereby, an [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\Gamma$ -- together with the respective compatibility conditions, which equivalently say (as highlighted in
[tom Dieck 69, Sec. 1.2](#tomDieck69), also [Murayama-Shimakawa 95, below 1.1](#MurayamaShimakawa95), see the discussion [here](category+of+G-sets#InternalGroupActions)) that the joint action is that of the [[semidirect product group]] $\Gamma \rtimes G$.

Beware that this [[action]] of the [[equivariance group]] $G$ on the [[structure group]] $\Gamma$ of an [[equivariant principal bundle]] is often and traditionally disregarded, i.e. implicitly taken to be the [[trivial action]] (e.g. [Lashof 82](#Lashof82), [Lashof-May-Segal 83](#LashofMaySegal83)), which equivalently means that the [[semidirect product group]] that acts is reduced to the [[direct product group]] $\Gamma \times G$, meaning that the [[action]] of the [[equivariance group]] _commutes_ with that of the [[structure group]]. This special case is the default meaning of _equivariant bundle_ in much of the literature!

(The definition of "generalized equivariant bundles" proposed in [Lashof-May 86](#LashofMay86) and advertized in [Lewis-May-Steinberger 86, Sec. IV.1](#LewisMaySteinberger86) allows any [[group extension]] of $G$ by $\Gamma$ to act. This reduces to [[semidirect products]] $\Gamma \rtimes G$ for [[split sequence|split extensions]] (see [there](group+extension#SplitExtensionsAndSemidirectProductGroups)) where $\Gamma$ is a [[normal subgroup]], and that is the case that [May 90](#May90), [Guillou-May-Merling 17](#GuillouMayMerling17) falls back to).

Much of the literature on equivariant bundles is interested

* in [[equivariant vector bundles]] regarded as representing [[cocycles]] for [[equivariant K-theory]] ([Segal 68, Sec 1](#Segal68), [Wasserman 69, Sec. 2](#Wasserman69),[HJJS 08, Sec. 13](#HJJS08));

and/or

* as [[twisted cohomology|twists]] for [[twisted equivariant cohomology theories]], and here most of the existing literature focuses on [[twisted equivariant K-theory]] and specifically on its equivariant degree-3 twist by equivariant [[projective bundles]] (e.g. [Barcenas-Espinoza-Joachim-Uribe 12](#BarcenasEspinozaJoachimUribe12),  [Uribe-Lück 14, Sec. 15](#UribeLueck14)).

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
a _$G$-[[equivariant topological group]]_ $(\Gamma, \alpha)$ is a [[group object]] [[internalization|internal]] to [[topological G-spaces]] (Def. \ref{TopologicalGSpaces}):
  $$
    \big(
      \Gamma,
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
     \Gamma
     ,
     \alpha
   \big)
   &\mapsto&
   \Gamma
   \,.
  }
\]
\end{remark}



### Equivariant bundles

We say that a $G$-equivariant principal bundle is a [[principal bundle]] [[internalization|internal]] to [[topological G-spaces]].

(Beware that, following tradition in equivariant bundle theory, we do not impose a [[local trivialization|local trivializability condition]] at this point, but add this as an extra clause later and then speak explicitly of _locall trivial equivariant bundles_ -- for more on this see at _[Notions of equivariant local triviality](#NotionsOfEquivariantLocalTriviality)_.)

\begin{defn}\label{EquivariantPrincipalBundles}
(**[[equivariant principal bundle]]**)
  \linebreak
Given

  * an [[equivariance group]] $G \in Groups(TopologicalSpaces)$;

  * an [[equivariant topological group]] (Def. \ref{EquivariantTopologicalGroup})

    $
      (\Gamma, \alpha)
      \;\in\;
      Groups\big(  G Actions(TopologicalSpaces) \big)
    $

    to be called the $G$-equivariant _[[structure group]]_;

a _$G$-equivariant $(\Gamma,\alpha)$-principal bundle over $(X,\rho)$ is:

* a [[internalization|internal]] [[bundle]], namely a [[morphism]] $P \overset{p}{\to} X$ in [[topological G-spaces]];

* the [[mathematical structure|structure]] of a $(\Gamma,\alpha)$-[[action object]] on the total space $P$:

such that the following conditions holds:

* **(fiberwise action)** the [[action]] is over $X$, in that the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}
  \Gamma \times P
  \ar[
    rr,
    "\rho"
  ]
  \ar[
    dr,
    "p\circ \mathrm{pr}_2\;"{left}
  ]
  &&
  P
  \ar[
    dl,
    "\;p"{right}
  ]
  \\
  & X
\end{tikzcd}

* {#EquivariantPrincipality} **(principality)** the _[[shear map]]_

  $$
    \array{
      \Gamma \times P
      &\longrightarrow&
      P \times_X P
      \\
      (\gamma, p)
      &\mapsto&
      (\rho(\gamma)(p), p)
    }
  $$

  is an [[isomorphism]], hence this [[commuting diagram]] is moreover a [[pullback square]] (in [[topological G-spaces]]):


\begin{tikzcd}
  \Gamma \times P
  \ar[
    drr,
    bend left=20,
    "\rho"
  ]
  \ar[
    ddr,
    bend right=20,
    "\mathrm{pr}_2\;\;\;"{below}
  ]
  \ar[
    dr,
    dashed,
    "\simeq"{description}
  ]
  \\
  & 
  P \times_X P
  \ar[
    r
  ]
  \ar[d]
  \ar[
    dr,
    phantom,
    "\mbox{\tiny\rm(pb)}"{description}
  ]
  &
  P 
  \ar[
    d,
    "p"
  ]
  \\
  &
  P 
  \ar[
    r,
    "p"{below}
  ]
  & 
  X
\end{tikzcd}


\end{defn}

\begin{remark}\label{OnTheInternalDefinitionOfPrincipality}
**(on the internal definition of principality)**
Notice that in Def. \ref{EquivariantPrincipalBundles} we do *not* explicitly demand that the base space is the [[quotient space]] of the total space by the [[group action]] (it defines an [[internalization|internal]] [[pseudo-torsor]] instead of a [[torsor]]). This has several reasons:

1. The way the definition is stated, it involves only [[finite limits]] (no [[colimits]]), which means that this notion of equivariant principal bundle will be preserved by all [[right adjoint]] functors on the ambient category, such as notably the [[fixed locus]]-functors (see [there](topological+G-space#FixedLociWithResidualWeylGroupAction)).

1. Nevertheless, the expected quotient condition is both implied as well as circumvented, as need be:

   Once equivariant local trivializability is imposed [below](#NotionsOfEquivariantLocalTriviality) it follows that the underlying [[continuous function]] $P \to X$ is a [[locally trivial]] [[fiber bundle]]. There are then two cases:

   1. Either the [[typical fiber]] is [[inhabited set|inhabited]]. This implies that $P \to X$ is an [[effective epimorphism]], and with that property the shear map condition [above](#EquivariantPrincipality) implies that $X$ is the quotient of $P$ by $G$.

   1. Or the [[typical fiber]] is the [[empty space]]. This case, often disregarded in discussion of fiber bundles, is actually an example of Def. \ref{EquivariantPrincipalBundles}, because for the empty bundle the shear map is an isomorphism:

      $$
        \Gamma \times \varnothing
        \overset{\simeq}{\longrightarrow}
        \varnothing \times_X \varnothing
      $$

      (since both [[domain]] and [[codomain]] are isomorphic to the [[empty space]]): 

      *Empty bundles are principal! (and locally trivial!), in the above sense.*

      While this degenerate case is irrelevant for ordinary principal bundles, it is crucial for equivariant principal bundles, since their [[fixed loci]] often have empty total space. In fact, if the action $\alpha$ of $G$ on the [[structure group]] $\Gamma$ is trivial (as is often the case in applications) then it follows at once that any fixed locus of an equivariant principal bundle can have only one of two typical fibers, $\Gamma$ or $\varnothing$, while the structure group is $\Gamma$, in both cases.

\end{remark}


## Properties


### As $(G,\alpha,\Gamma)$-principal bundles


\begin{prop}\label{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles}
(**principal bundles internal to $G$-spaces are equivalent to tom Dieck-bundles**)
\linebreak
  The
  $G$-equivariant $(\Gamma,\alpha)$-principal bundles in the [[internalization|internal]] sense of Def. \ref{EquivariantPrincipalBundles} are [[equivalence of categories|equivalent]] to the $(G,\alpha,\Gamma)$-principal bundles in the sense of [tom Dieck 69](#tomDieck69) (both without any condition of [[local trivializability]], at this point).
\end{prop}
\begin{proof}
  This follows immediately by the fact ([this Prop.](equivariant+group#ActionsOfEquivariantGroupsAsSemidirectProductGroupActions)) that $G$-equivariant actions of [[equivariant groups]] $(G,\alpha)$ are equivalent to plain actions of the [[semidirect product group]] $\Gamma \rtimes_\alpha G$.
\end{proof}


### Restriction to fixed loci
 {#RestrictionToFixedLoci}

The [[internalization|internal]]-formulation of $G$-equivariant principal; bundles (Def. \ref{EquivariantPrincipalBundles}) serves to make manifest that they have good behaviour under passage to [[fixed loci]]:

Notice that for any [[subgroup]] $H \subset G$ we have the fixed point functor ([here](fixed+point+space#eq:TopologicalHFixedLociAsFunctorToWeylGroupSpaces))

\[
  \label{TopologicalHFixedLociAsFunctorToWeylGroupSpaces}
  (-)^H
  \;\colon\;
  Topological G Spaces
   \overset{\;\;\;\;\;}{\longrightarrow}
  Topological N(H)/H Spaces
  \,.
\]

\begin{prop}
  For $(\Gamma,\alpha)$ an $G$-equivariant topological group (Def. \ref{EquivariantTopologicalGroup}), $P \to X$ a $G$-equivariant $(\Gamma,\alpha)$-principal bundle (Def. \ref{EquivariantPrincipalBundles}) and $H \subset G$ any [[subgroup]], the $H$-fixed locus (eq:TopologicalHFixedLociAsFunctorToWeylGroupSpaces) $P^H \to X^H$ is canonically an $N(H)/H$-equivariant $(\Gamma^H, \alpha^H)$-principal bundle.
\end{prop}
\begin{proof}
  The point is that passage to $H$-fixed loci (eq:TopologicalHFixedLociAsFunctorToWeylGroupSpaces) is a [[right adjoint]] functor ([this Prop.](fixed+point+space#PassageToFixedLociIsRightAdjoint)) and therefore [[right adjoints preserve limits|preserves all limits]], and so in particular [[preserved limit|preserves]] [[Cartesian products]] and [[fiber products]], hence preserves [[internalization|internal]] [[group objects]] as well as the [principality condition](#EquivariantPrincipality). 
\end{proof}



### Over coset spaces
 {#OverCosetSpaces}

\begin{prop}\label{EquivariantCosetSpaceBundles}
**(semidirect product coset space bundles are locally trivial)**
  Let $H \subset G$ be a [[closed subgroup]],
  and let
  ${\widehat H}$ be a lift of $H$ to a [[closed subgroup]] of the [[semidirect product group]], as shown on the left here:

\[
  \label{EquivariantBundleOfCosetSpaces}
  \array{
    {\widehat H} &\subset& \Gamma \rtimes_\alpha G
    &{\phantom{A}}&
    \big(
      \Gamma \rtimes_\alpha G
    \big)
    \big/
    {\widehat H}
    \\
    {}^{\mathllap{\simeq}}
    \big\downarrow
    &&
    \big\downarrow
    {}^{\mathrlap{
      pr_2
    }}
    &&
    \big\downarrow
    {}^{ \mathrlap{p} }
    \\
    H &\subset& G
    &&
    G/H
    \mathrlap{
    \,.
    }
  }
\]

Then the induced [[bundle]] of [[coset spaces]], shown on the right of (eq:EquivariantBundleOfCosetSpaces):

1. is a $(\Gamma,\alpha)$-principal bundle (under Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})

1. is [[locally trivial]] as an ordinary $\Gamma$-[[fiber bundle]] in [[TopologicalSpaces]] as soon as the the [[coset space]] [[coprojection]] $G \to G/H$ [[coset space coprojection admitting local sections|admits local sections]].

\end{prop}

This is [tom Dieck 69, Lemma in Sec. 2.1](#tomDieck69)

\begin{proof}

The first statement is evident.

For the second statement, let $\sigma$ denote a local section over an open subset $U \subset G/H$:

$$
  \array{
    &&
    G_{\vert \mathcal{U}}
    &\longrightarrow&
    G
    \\
    &
    {}^{\mathllap{
      \sigma
    }}
    \nearrow
    &
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow
    \\
    U
    &=&
    U
    &\longrightarrow&
    G/H
    \mathrlap{\,,}
  }
$$

We claim that then

$$
  \array{
    \Gamma \times U
    &&
    \underoverset
     {\simeq}
     {
       (\gamma,u)
       \mapsto
       [\gamma,\sigma(u)]
     }
     {
      \longrightarrow
    }
    &&
    \Big(
      \big(
        \Gamma \rtimes_\alpha G
      \big) / {\widehat H}
    \Big)_{\vert U}
    \\
    & \searrow && \swarrow
    \\
    && U
  }
$$

is an [[isomorphism]], of $\Gamma$-[[principal bundles]] over $U \subset G/H$.

* It is clear by construction that the map is

  1. [[continuous function|continuous]].

  1. $\Gamma$-equivariant.

* To see that map is an isomorphism it is sufficient to see that it is so over each $u \in U$:

  * Injectivity here follows from the fact that ${\widehat H}$ is a lift of $H$, so that the unique element lifting the [[neutral element]] is the neutral element.

  * To see that the map is surjective over each $u \in U$:

    That $[\gamma, g] \in \big( \Gamma \rtimes_\alpha G \big)/{\widehat H}$ is in the fiber over $u$ means that $ g^{-1} \sigma(u) \in H \subset G$. Then for $\hat h \in \widehat H$ the unique element with $pr_2(\hat h) = g^{-1} \sigma(u)$ we see that $[\gamma, g] = \big[ (\gamma,g) \cdot q \big] = [\cdots, \sigma(u)]$, which is manifestly in the image of our map.

    (Filling in the ellipses here, which is straightforward but unenlightning, actually gives the continuous inverse map.)

\end{proof}


In fact every equivariant principal bundle over a coset space is of this form:


\begin{prop}\label{EquivariantPrincipalBundlesOverCosetSpacesAreSemidirectProductCosetsSpaceBundles}
**(equivariant principal bundle over coset spaces are semidirect product coset space bundles)**
  Let $H \subset G$ be a [[closed subgroup]]. Then every [[Hausdorff space]] $(\Gamma,\alpha)$-principal bundle (Def. \ref{EquivariantPrincipalBundles}) over the [[coset space]]

$$
  P \overset{p}{\longrightarrow} G/H
  \,,
$$

which is [[locally trivial]] as an ordinary $\Gamma$-[[principal bundle]], is [[isomorphism|isomorphic]]

\[
  \label{TrivializingBundleIosmorphismOverCosetSpace}
  \array{
    (\Gamma \rtimes_\alpha G)/{\widehat H}
    &&
    \underoverset
      {\simeq}
      { [\gamma,g] \mapsto (\gamma,g)\cdot p }
      {\longrightarrow}
    &&
    P
    \\
    &
    \searrow
    &&
    \swarrow
    \\
    &&
    G/H
  }
\]

to a [[coset space]]-bundle $(\Gamma \rtimes_\alpha G)/{\widehat H} \longrightarrow G/H$ from Prop. \ref{EquivariantCosetSpaceBundles}, for ${\widehat H}$ a lift of $H$ to a [[closed subgroup]] of the [[semidirect product group]]:

$$
  \array{
    {\widehat H} &\subset& \Gamma \rtimes_\alpha G
    \\
    {}^{\mathllap{\simeq}}
    \big\downarrow
    &&
    \big\downarrow
    {}^{\mathrlap{
      pr_2
    }}
    \\
    H &\subset& G
    \mathrlap{
    \,.
    }
  }
$$

\end{prop}

\begin{proof}

Regard $P$ as equipped with the [[action]] of the [[semidirect product group]] $\Gamma \rtimes_\alpha G$, by Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles}.

Let $e \in P_{[H]}$ be any point in the [[fiber]] over $[H] \in G/H$, and take

$$
  {\widehat H} \;\coloneqq\; Stab_{\Gamma \rtimes_\alpha G}(e)
$$

to be its [[stabilizer subgroup]] under the [[semidirect product group]]-action. We observe that this has the stated properties:

* ${\widehat H}$ is a [[closed subgroup]] because [stabilizer subgroups are closed subgroups](closed+subgroup#StabilizerSubgroupsOfContinuousActionsOnT1SpacesAreClosed) under the Hausdorff-ness assumption;

* under $\Gamma \rtimes_\alpha G \overset{pr_2}{\longrightarrow} G$ we have ${\widehat H} \to H$, since  for all $\hat h \in \widehat H$:

  $$
    \begin{aligned}
      [H]
      &= p(\hat h \cdot e)
      \\
      & = pr_2(\hat h) \cdot p(e)
      \\
      & = pr_2(\hat h) \cdot [H]
    \end{aligned}
  $$

* ${\widehat H} \to H$ is

  * a [[surjection]] because the action of $\Gamma$ on the [[fibers]] of $P$ is a [[transitive action]],

  * an [[injection]] because the action of $\Gamma$ on the [[fibers]] of $P$ is a [[free action]]

  (by [principality](#EquivariantPrincipality)).

Moreover, it is clear by construction that (eq:TrivializingBundleIosmorphismOverCosetSpace) is a $(\Gamma \rtimes_\alpha G)$-[[equivariant function|equivariant]] [[continuous function]] over $G/H$.

Hence to see that (eq:TrivializingBundleIosmorphismOverCosetSpace) is an [[isomorphism]] (a [[homeomorphism]] of underlying [[topological spaces]]) it is sufficient to see that after [[forgetful functor|forgetting]] the $G$-[[action]] we have a morphism between ordinary $\Gamma$-[[principal bundles]] over their common base space, because any such is an [[isomorphism]], as is manifest from its restriction to any common [[local trivialization]].

Therefore it is now sufficient to see that the coset bundle $(\Gamma \rtimes_\alpha G)/{\widehat H} \longrightarrow G/H$ is [[locally trivial]] as a $\Gamma$-[[principal bundle]]. But this is the statement of Prop. \ref{EquivariantCosetSpaceBundles}.

\end{proof}



### Notions of equivariant local triviality
 {#NotionsOfEquivariantLocalTriviality}


The literature considers various different notions of [[local triviality]] of equivariant bundles. We list them and then (...eventually...) discuss sufficient conditions under which these imply each other.

> under construction

\begin{definition}\label{tomDieckEquivariantLocalTrivialization}
**(tom Dieck's equivariant local triviality condition -- [tom Dieck 69, Def. 2.3](#tomDieck69), [tom Dieck 87, p. 58](#tomDieck87))**\linebreak
  An equivariant principal bundle
  (Def. \ref{EquivariantPrincipalBundles}, Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})
  $$
    P \overset{p}{\longrightarrow} B
    \;\;
    \in
    \;
    (\Gamma,\alpha)PrincipalBundles
  $$
  is **[[locally trivial]]** if there exists

1. an index-[[set]] $I$,

1. an $I$-[[indexed set]] of [[topological subspace|sub]]-[[topological G-space|G-spaces]]

   $$
     U_i \;\subset\; B
     \;\;
     \in
     G Actions
     \big(
      TopologicalSpaces
     \big)
   $$

1. an $I$-[[indexed set]] of [[closed subgroup]] $H_i \subset G$;

1. an $I$-[[indexed set]] of $E_i \overset{p_i}{\to} G/H_i \;\in\; (\Gamma,\alpha)PrincipalBundles$ over their [[coset spaces]];

such that

1. $\big\{ U_i \hookrightarrow B \big\}_{i \in I}$ is an [[open cover]] in [[TopologicalSpaces]];

1. for each $i \in I$ there is a [[homomorphism]] of $(\Gamma,\alpha)PrincipalBundles$

   \[
     \label{tomDieckLocalTrivalityHomomorphism}
     \array{
       E_{\vert U_i}
       &
         \overset{}{\longrightarrow}
       &
       E_i
       \\
       \big\downarrow
       &
         {}^{{}_{}}
       &
       \big\downarrow {}^{\mathrlap{p}}
       \\
       U_i
       &\longrightarrow&
       G/H
     }
   \]

   from the restriction of $E$ to $U_i$ and the given  equivariant bundle over the coset space (as [above](#OverCosetSpaces)).

\end{definition}

\begin{definition}\label{BierstoneEquivariantLocalTrivialization}
**(Bierstone's equivariant local triviality condition -- [Bierstone 78, Sec. 4, p. 619-620](#Bierstone78))**\linebreak
  An equivariant principal bundle
  (Def. \ref{EquivariantPrincipalBundles}, Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})

  $$
    P \overset{p}{\longrightarrow} X
    \;\;
    \in
    \;
    (\Gamma,\alpha)PrincipalBundles
  $$

  is **[[locally trivial]]** if for each point $x \in X$ (with [[isotropy
group]]/[[stabilizer group]] denoted $G_x \coloneqq Stab_G(x) \subset X$) there exists

1. an [[open neighbourhood]]

   $$
     U_x
       \;\subset\;
     X \;\; \in \; G_x Actions(TopologicalSpaces)
   $$

1. a $G_x$-[[equivariant function|equivariant]] [[homomorphism]] of $\Gamma PrincipalBundles$

   $$
     \array{
       P_{\vert U_x}
       &
         \longrightarrow
       &
       U_x \times p^{-1}(\{x\})
       \\
       {}^{\mathllap{ p_{\vert U_x} }}
       \big\downarrow
         &&
       \big\downarrow
       {}^{
         \mathrlap{ pr_1 }
       }
       \\
       U_x &=& U_x
     }
   $$

   from the restriction of $P$ to $U_x$ to the [[Cartesian product]] of $U_x$ with the [[fiber]] of $P$ over $x$.

\end{definition}

\begin{definition}\label{LashofEquivariantLocalTrivialization}
**(Lashof's equivariant local triviality condition --  [Lashof 82, p. 258](#Lashof82), [Lashof-May 86, p. 267](#LashofMay86))**\linebreak
  An equivariant principal bundle
  (Def. \ref{EquivariantPrincipalBundles}, Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles})

  $$
    P \overset{p}{\longrightarrow} X
    \;\;
    \in
    \;
    (\Gamma,\alpha)PrincipalBundles
  $$

  is **[[locally trivial]]** if for each point $x \in X$ (with [[isotropy
group]]/[[stabilizer group]] denoted $G_x \coloneqq Stab_G(x) \subset X$) there exists

1. an index-[[set]] $I$;

1. an $I$-[[indexed set]] of [[closed subgroups]] $H_i \subset G$;

1. an $I$-[[indexed set]] of $H_i$ [[slice theorem|slices]] $S_i \subset X$;

1. an $I$-[[indexed set]] of $\Gamma_i \;\in\; H_i Actions(TopologicalSpaces)$ lifting $\Gamma \in TopologicalSpaces$;

such that

1. the [[orbits]] of the [[slice theorem|slices]] $\big\{ G\cdot S_i \subset X \big\}_{i \in I}$ form an [[open cover]] over $X$;

1. for each $i \in I$ there is a $G$-[[equivariant function|equivariant]] [[homomorphism]] of $\Gamma PrincipalBundles$

   \[
     \label{LashofLocalTrivalityHomomorphism}
     \array{
       P_{\vert G\cdot S_i}
       &\longrightarrow&
       G
         \times_{H_i}
       \big(
         S_i \times \Gamma_i
       \big)
       \\
       \big\downarrow
       &&
       \big\downarrow
       \\
       G \cdot S_i
       &=&
       G \times_H S_i
     }
   \]

   from the restriction of $P$ over the orbit of the $i$th slice to ...

\end{definition}


* [Lashof-Rothenberg 78, p. 216](#LashofRothenberg78)

(...)

\begin{prop}

(...) Lashof82 $\leftrightarrow$ Bierstone78  (...)

\end{prop}

([Lashof 82, Lemmas 1.1, 1.3](#Lashof82))


\begin{lemma}\label{LashofLocalModelsAreLocallyTrivialAsOrdinaryFiberBundles}
**(Lashof's local models are locally trivial as ordinary fiber bundles)
  If the [[equivariance group]] $G$ is a [[compact Lie group]]
  then for every [[closed subgroup]] $H \subset G$ and [[topological G-space|topological H-spaces]] $S, F$ the canonical projection

$$
  \array{
    G \times_H 
    \big(
      S \times F
    \big)
    \\
    \big\downarrow
    \\
    G \times_H S
  }
$$

is a [[locally trivial]] $F$-[[fiber bundle]].

\end{lemma}

([Lashof 82, Cor. 1.2](#Lashof82))

\begin{proof}

Since $G$ is assumed to be a [[compact Lie group]], it admits a [[bi-invariant Riemannian metric]] ([this Prop.](compact+Lie+group#CompactLieGroupsAdmitBiinvariantMetrics)). With respect to this metric, consider a small open [[normal vector|normal]] $\epsilon$-neighbourhood to $H$ at $e$ in $G$

$$
  D_e
  \,\coloneqq\,
  D_\epsilon N_e H
  \,\subset \,
  N H 
  \;
    \underoverset{\simeq}{\exp}{\longrightarrow}
  \;
  T H
$$

i.e. of points that with respect to some choice of [[tubular neighbourhood]] of $H \subset G$ are a normal distance $\lt \epsilon$ from $H$.

Then the multiplication action

$$
  \array{
    D_e \times H 
    &
    \underoverset{ \simeq }{ (-)\cdot(-) }{\longrightarrow}
    &
    D_e \cdot H
    \\
    (d,h) &\mapsto& d \cdot h
  }
$$

is a [[diffeomorphism]], because, by right-invariance of the chosen metric, the operation

$$
  \array{
    D_e &\overset{}{\longrightarrow}& D_h
    \\
    d &\mapsto& d \cdot h
  }
$$

is even an [[isometry]], for each $h \in H$.

It follows 

1) by dimension reasons that 

$$
  D \cdot H \;\subset\; G
$$

is an [[open neighbourhood]] of $H$ in $G$, and hence that

$$
  \big(D \cdot H\big) \times_H S
  \hookrightarrow
  G \times_H S
$$

is an [[open neighbourhood]] of $S \subset G_H \times S$.

2) that the restriction of the projection to this neighbourhood is isomorphic to the trivial $F$-fiber bundle:

$$
  \array{
    D \times S \times F
    &
    \simeq
    & 
    (D \times H) \times_H (S \times F)
    &
    \overset{\simeq}{\longrightarrow}
    & 
    (D \cdot H)
    \times_H 
    (S \times F)
    &
    \longrightarrow
    & 
    G \times_H ( S \times F )
    \\
    \big\downarrow
    && && 
    \big\downarrow
    &
      {}^{{}_{(pb)}}
    &
    \big\downarrow
    \\
    D \times S
    &\simeq&
    (D \times H) \times_H S
    &
    \underoverset
      { m \times_H id }
      {\simeq}
      {\longrightarrow}
    &
    (D \cdot H) \times_H S
    &\hookrightarrow&
    G \times_H S
    \,.
  }
$$

Finally, since $G \times_H S$ is covered by left $G$-translates of the open subset $(D \cdot H) \times_H S$, and since the same argument applies to each of theses, by left-invariance of the metric, the claim follows.

\end{proof}



\begin{prop}\label{LashofLocalTrivializabilityImpliesTopDieckForTrivialAlpha}
**(Lashof's local trivializability implies tom Dieck's for $\alpha = 1$)**
  In the case that $\alpha = 1$ (in Def. \ref{EquivariantTopologicalGroup}), equivariant local trivializability in the sense of Lashof (Def. \ref{LashofEquivariantLocalTrivialization}) implies local trivializability in the sense of tom Dieck (Def. \ref{tomDieckEquivariantLocalTrivialization}).

\end{prop}

\begin{proof}
  It is sufficient to see that Lashof's local model bundles in (eq:LashofLocalTrivalityHomomorphism) are examples of tom Dieck's local model bundles in (eq:tomDieckLocalTrivalityHomomorphism).

So let $H \subset G$ be a [[closed subgroup]], $S \subset X$ be an $H$-[[slice theorem|slice]] and

\[
  \label{LashofActionOfHOnGammaInProofLashofImpliestoDieck}
  \phi \colon H \to \Gamma
\]

be the [[homomorphism]] through which $H$ acts on $\Gamma$ in Lashof's model for the equivariant bundle over the orbit of the slice.

$$
  \array{
    G \times_H
    (S \times \Gamma)
    \\
    \big\downarrow
    \\
    G \times_H S
    \,.
  }
$$

By Prop. \ref{EquivariantPrincipalBundlesOverCosetSpacesAreSemidirectProductCosetsSpaceBundles} and using that $\alpha = 1$ we obtain from $\phi$ an equivariant principal bundle over $G/H$ by taking the subgroup ${\widehat H}$ in (eq:EquivariantBundleOfCosetSpaces) to be the [[graph of a function|graph]] of $\phi$ (eq:LashofActionOfHOnGammaInProofLashofImpliestoDieck)

$$
  {\widehat H}
  \;\coloneqq\;
  graph(\phi)
  \;\subset\;
  \Gamma \times G
  \,.
$$

Observing that the [[coset space]] by a subgroup of this form coincindes with the quotient by the [[diagonal action]]

$$
  (\Gamma \times G)/ graph(\phi)
  \;\simeq\;
  G \times_H \Gamma
  \,,
$$

makes it evident that tom Dieck's condition (eq:tomDieckLocalTrivalityHomomorphism) is satisfied for Lashof's local model in that the following square is manifestly a [[pullback]]:

$$
  \array{
    G
    \times_H
    (S \times \Gamma)
    &
    \longrightarrow
    &
    G \times_H \Gamma
    &
    =
    &
    (\Gamma \times G)
    \big/
    ( graph(H \overset{\phi}{\to} \Gamma) )
    \\
    \big\downarrow
    &&
    \big\downarrow
    &
    \swarrow
    \\
    G \times_H S
    &
    \underoverset
      {}
      {}
      {\longrightarrow}
    &
    G \times_H H
  }
$$


\end{proof}

(...)

\begin{remark}\label{SufficientConditionForEquivariantEnhancementOfLocalTrivialization}
  **(sufficient condition for plain local trivialization to have equivariant enhancement)**
  Sufficient conditions for existence of plain local trivialization to imply a $G$-equivariant local trivialization, and hence for the inclusion in Prop. \ref{PrincipalBundlesInternalToGSpacesEquivalentTotomDieckBundles} to be an actual [[equivalence of categories]], are:

1. $G$ is a [[finite group]]; or

1. $X$ is a [[locally compact topological space|locally compact]] [[separable metric space]] of [[finite number|finite]] [[dimension of a separable metric space|dimension]] and with a [[finite number]] of $G$-[[orbit types]]; or

1. $\Gamma$ is a [[locally compact topological space|locally compact]] [[separable metric space]] such that for every $G$-[[orbit type]] $G/H \subset X$ the [[fixed locus]] $\Gamma^H$ is an [[absolute neighbourhood retract]] (such as a [[finite number|finite]]-[[dimension of a manifold|dimensional]] [[topological manifold]] or a [[finite number|finite]]-[[dimension of a cell complex|dimensional]] and [[locally finite CW-complex|locally finite]] [[CW-complex]], by the discussion [there](absolute+retract#Examples)).

Because ([Atiyah 66, p. 374](KR+cohomology+theory#Atiyah66)) then
for every plain local trivialization around any [[orbit]] the [[equivariant Tietze extension theorem]] implies the existence of an [[equivariant function]] to $\Gamma$ on an [[open neighbourhood]] of that orbit, which thus constitutes a $G$-equivariant local trivialization.

\end{remark}

\linebreak

### Universal equivariant principal bundles
 {#UniversalEquivariantPrincipalBundles}

\begin{defn}\label{calBGammaForDiscreteG}
**(Murayama-Shimakawa groupoid for discrete $G$)** \linebreak
  For $G$ a [[discrete group]] and $(\Gamma,\alpha)$ a $G$-[[equivariant group|equivariant]] [[topological group]] (hence a [[topological group]] equipped with an [[action]] $\alpha$ of $G$ by continuous group [[automorphisms]]), consider the [[topological groupoid]] which is the [[functor groupoid]] from the [[pair groupoid]] of $G$ to the [[delooping groupoid]] of $\Gamma$:

\[
  \label{HomGroupoidFromPairGroupoidOfGToDeloopingGroupoidOfGamma}
  \mathcal{B}\Gamma
  \;\coloneqq\;
  Groupoids(TopSpaces)
  \left(
    G \times G 
      \underoverset{pr_2}{pr_1}{\rightrightarrows}
    G,
    \;
    \Gamma \rightrightarrows \ast
  \right)
\]

but regarded as an [[internal groupoid]] in [[topological G-spaces]] 

$$
  \mathcal{B}\Gamma
  \;\in\;
  Groupoids
  \big(
    G Actions(TopologicalSpaces)
  \big)
$$

by equipping it with the $G$-[[group action|action]] given on [[functors]] $F$ and [[natural transformations]] $\eta$ in (eq:HomGroupoidFromPairGroupoidOfGToDeloopingGroupoidOfGamma) by:

$$
  (g \cdot F)
  (g_1, g_2)  
  \;\coloneqq\;
  \alpha(g)
  \big(
    F(g_1 g, g_2 g)
  \big)
  \,,
  {\phantom{AAA}}
  (g \cdot \eta)
  (g_1)
  \;\coloneqq\;
  \alpha(g)(\eta(g_1))
  \,.
$$

\end{defn}

> add word on choice of topology on the mapping spaces, see [Murayama-Shimakawa 95, p. 1293 (5 of 7)](#MurayamaShimakawa95)

\begin{prop}\label{RealizationOfMurayamaShimakawaGroupoidForDiscreteGIsClassifyingSpace}
  The [[fat geometric realization]] of the [[nerve]] of the $G$-topological groupoid from Def. \ref{HomGroupoidFromPairGroupoidOfGToDeloopingGroupoidOfGamma} 
$$
  \left\Vert
    \mathcal{B}\Gamma
  \right\Vert
  \;\;
  \in
  G Actions(TopSpaces)
$$
is a [[classifying space]] for $G$-equivariant $(\Gamma,\alpha)$-principal bundles.
\end{prop}
\begin{proof}
  This is Theorem 3.1 in [Murayama-Shimakawa 95](#MurayamaShimakawa95),
  using the remark on the bottom of p. 1294 (6 of 7) that for discrete group $G$ the construction in Theorem 3.1 may be simplified.

For $G$ discrete and $\Gamma$ [[discrete group|discrete]] or [[compact Lie group|compact Lie]] the same statement appears as [Guillou, May & Merling 17, Thm. 3.11](#GuillouMayMerling17). Notice that  Scholium 3.12 there doubts that [Murayama-Shimakawa 95](#MurayamaShimakawa95)'s result holds in more generality than this.
\end{proof}


\begin{prop}\label{FixedLociOfcalBGammaForDiscreteG}
  Let $H \subset G$ any [[subgroup]], there is an [[equivalence]] of [[topological groupoids]] between the $H$-[[fixed locus]] of the $G$-groupoid from Def. \ref{calBGammaForDiscreteG} and

1. for trivial $\alpha$: the [[functor groupoid]] between the [[delooping groupoids]] of $G$ and $\Gamma$:

   $$
     \big(
       \mathcal{B}\Gamma
     \big)^H
     \;\;
     \simeq
     \;\;
     Groupoids(TopSpaces)
     \big(
       G \rightrightarrows \ast,
       \,,
       \Gamma \rightrightarrows \ast
     \big)
   $$

1. for general $\alpha$: the [[action groupoid]] of the [[conjugation action]] of $\Gamma \overset{\gamma \mapsto (\gamma,e)}{\hookrightarrow} \Gamma \rtimes_\alpha G$ on [[group homomorphisms]] $\phi \colon G \to \Gamma \rtimes_\alpha G$ which are [[sections]] ($pr_2 \circ \phi = id_G$) of $pr_2 \colon \Gamma \rtimes_\alpha G \to G$:

   $$
     \big(
       \mathcal{B}\Gamma
     \big)^H
     \;\;
     \simeq
     \;\;
     \Big(
       Groups(TopSpaces)_{/G}
       \big(
         G, \, \Gamma \rtimes_\alpha G
       \big)
     \Big)
     \sslash
     \Gamma
     \,.
   $$

\end{prop}
\begin{proof}
  The first statement is the evident specialization of the second. It may help to go through the proof first in this special case of trivial $\alpha$, as the presence of $\alpha$ can tend to obscure the simple logic behind it.

  First consider the case $H = G$.
  Here the point to notice is that $G$-invariance of a functor
  $
    F 
    \colon 
    G \times G 
    \to
    \Gamma
  $
  means that its value depends only on the difference of its arguments
  $$
    F(g_1, g_2) = F'( g_1 g_2^{-1} )
  $$
  and functoriality then means equivalently that $g \mapsto (F'(g), g)$
  is a group homomorphism to $\Gamma \rtimes_\alpha$.

  Similarly, $G$-invariance of a naturaltrans formation
  $\eta \colon G \to \Gamma$ means that its components are fixed by
  its values on $e \in G$ via

  $$
    \eta( g^{-1} ) \;=\; \alpha(g)(\eta(e))
    \,.
  $$

  With this, the naturality square for $\eta$ commutes precisely
  if two sections $g \mapsto (F'(g), g)$, as above, 
  are related by conjugation with $\gamma_e \in \Gamma \rtimes_\alpha G$.

  This proves the equivalence in the case $H = G$.

  Next to see the claim for general $H \subset G$, notice that 
  restriction along 
  $(H \times H \rightrightarrows H) \hookrightarrow (G \times G \rightrightarrows G)$ followed by the above equivalence (now for $G$ replaced by $H$) gives a canonical comparison functor $p$. We claim
that a homotopy-inverse is given by the evident inclusion functor $i$ that fills up unspecified data by neutral elements. It is clear that $p \circ i = id$ and one checks that there is a homotopy $(id \Rightarrow i \circ p )$ (which is straightforward if one chooses good diagrammatic notation...).

\end{proof}

\begin{remark}
  To the extent that passage to fixed loci commutes with 
  realization (this would be guaranteed if we could use ordinary
  geometric realization in Prop. \ref{RealizationOfMurayamaShimakawaGroupoidForDiscreteGIsClassifyingSpace} which works as soon as $\Gamma$ is compact Lie),
  Prop. \ref{FixedLociOfcalBGammaForDiscreteG} immediately implies
  the behaviour of equivariant classifying spaces under 
  fixed loci according to [Lashof 82, Thm. 2.17](#Lashof82) and [Lashof & May 86, Thm. 10](#LashofMay86).
  
  Related discussion is in [Guillou, May & Merling 17, pp. 15](#GuillouMayMerling17).
\end{remark}



(...)

\linebreak


## Examples

* [[equivariant tautological line bundle]]

* in [[arithmetic geometry]]: [[shtuka]]

## Related concepts

* [[twisted bundle]]

* [[equivariant differential topology]]

* [[equivariant cohomology]]

* [[equivariant connection]]

* [[equivariant K-theory]]



## References

### Equivariant fiber bundles

On general (topological) equivariant [[fiber bundles]]/[[principal bundles]]:

Precursor discussion:

* T. E. Stewart, *Lifting Group Actions in Fibre Bundles*, Annals of Mathematics Second Series, Vol. 74, No. 1 (1961), pp. 192-198 ([jstor:1970310](https://www.jstor.org/stable/1970310))

  > (for [[structure group]] commuting with the [[equivariance group]], but noticing already that a [[normal subgroup]]-extension could be considered, more generally)


The original definition:

* {#tomDieck69} [[Tammo tom Dieck]], _Faserb&uuml;ndel mit Gruppenoperation_, Arch. Math 20, 136–143 (1969) ([doi:10.1007/BF01899003](https://doi.org/10.1007/BF01899003))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#Bierstone78} [[Edward Bierstone]], _The equivariant covering homotopy property for differentiable $G$-fibre bundles_, J. Differential Geom. 8(4): 615-622 (1973) ([doi:10.4310/jdg/1214431963](https://projecteuclid.org/journals/journal-of-differential-geometry/volume-8/issue-4/The-equivariant-covering-homotopy-property-for-differentiable-G-fibre-bundles/10.4310/jdg/1214431963.full))

  > (for [[structure group]] commuting with the [[equivariance group]], but with [[equivariant differential topology|differentiable structure]])


* [[Goro Nishida]], Section 2 of: _The transfer homomorphism in equivariant generalized cohomology theories_, J. Math. Kyoto Univ. 18(3): 435-451 (1978) ([doi:10.1215/kjm/1250522505](https://projecteuclid.org/journals/kyoto-journal-of-mathematics/volume-18/issue-3/The-transfer-homomorphism-in-equivariant-generalized-cohomology-theories/10.1215/kjm/1250522505.full))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])


* {#LashofRothenberg78} [[Richard Lashof]], [[Melvin Rothenberg]], Section 1 of: _$G$-Smoothing theory_, p. 211-266 in: _Algebraic and Geometric Topology_, Proceedings of Symposia in Pure Mathematics, Vol. XXXII, Part 1, American Mathematical Society 1978 ([doi:10.1090/pspum/032.1](https://doi.org/10.1090/pspum/032.1), [[LashofRothenbergGSmoothingTheory.pdf:file]])

  > (for [[structure group]] commuting with the [[equivariance group]], but with [[equivariant differential topology|differentiable structure]])


* {#Lashof82} [[Richard Lashof]], _Equivariant bundles_, Illinois J. Math. 26(2): 257-271, 1982 ([doi:10.1215/ijm/1256046796](https://doi.org/10.1215/ijm/1256046796))

  > (for [[structure group]] commuting with the [[equivariance group]])

* {#LashofMay86} [[Richard Lashof]], [[Peter May]], _Generalized equivariant bundles_, Bull. Soc. Math. Belg. Sér. A 38, 265-271, 1986 ([pdf](http://math.uchicago.edu/~may/PAPERS/55.pdf), [[LashofMayGeneralizedEquivariantBundles.pdf:file]])

  > (for [[structure group]] [[group extension|extending]] the [[equivariance group]])


* {#LewisMaySteinberger86} [[L. Gaunce Lewis]], [[Peter May]], and Mark Steinberger, Section IV.1 of: _Equivariant stable homotopy theory_, Springer Lecture Notes in Mathematics Vol.1213. 1986 ([pdf](http://www.math.uchicago.edu/~may/BOOKS/equi.pdf), [doi:10.1007/BFb0075778](https://link.springer.com/book/10.1007/BFb0075778))

  > (for [[structure group]] [[group extension|extending]] the [[equivariance group]])

* {#tomDieck87} [[Tammo tom Dieck]], Section I.8 of: _[[Transformation Groups]]_, de Gruyter 1987  ([doi:10.1515/9783110858372]( https://doi.org/10.1515/9783110858372))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])


With [[abelian group|abelian]] [[structure group]]:

* {#LashofMaySegal83} [[Richard Lashof]], [[Peter May]], [[Graeme Segal]], _Equivariant bundles with abelian structural group_, Contemporary Mathematics,  Volume 19, 1983 ([doi:10.1090/conm/019](http://dx.doi.org/10.1090/conm/019), [pdf](http://www.math.uchicago.edu/~may/PAPERS/45.pdf), [[LashofMaySegalEquivariantBundles.pdf:file]])

  > (for [[structure group]] commuting with the [[equivariance group]])

* [[Andrzej Kozlowski]], _Equivariant Bundles and Cohomology_, Transactions of the American Mathematical Society, Vol. 296, No. 1 (Jul., 1986), pp. 181-190 ([jstor:2000568](https://www.jstor.org/stable/2000568))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

More on [[equivariant principal bundles]] and their [[classifying spaces]]/[[universal principal bundles]]:

* {#May90} [[Peter May]], _Some remarks on equivariant bundles and classifying spaces_, Théorie de l'homotopie, Astérisque, no. 191 (1990), 15 p. ([numdam:AST_1990__191__239_0](http://www.numdam.org/item/?id=AST_1990__191__239_0))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#MurayamaShimakawa95} [[Mitutaka Murayama]], [[Kazuhisa Shimakawa]], _Universal equivariant bundles_, Proc. Amer. Math. Soc. 123 (1995), 1289-1295 ([doi:10.1090/S0002-9939-1995-1231040-9](https://doi.org/10.1090/S0002-9939-1995-1231040-9))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

* {#UribeLueck14} [[Bernardo Uribe]], [[Wolfgang Lück]], _Equivariant principal bundles and their classifying spaces_, Algebr. Geom. Topol. 14 (2014) 1925-1995 ([arXiv:1304.4862](https://arxiv.org/abs/1304.4862), [doi:10.2140/agt.2014.14.1925](http://dx.doi.org/10.2140/agt.2014.14.1925))

  > (back to [[structure group]] commuting with the [[equivariance group]])

* {#GuillouMayMerling17} [[Bertrand Guillou]], [[Peter May]], [[Mona Merling]] _Categorical models for equivariant classifying spaces_, Algebr. Geom. Topol. 17 (2017) 2565-2602 ([arXiv:1201.5178](https://arxiv.org/abs/1201.5178), [doi:10.2140/agt.2017.17.2565](https://doi.org/10.2140/agt.2017.17.2565))

  > (for [[structure group]] [[semidirect product group|split]]-[[group extension|extending]] the [[equivariance group]])

Review and examples over the [[2-sphere]]:

* [[Eyup Yalcinkaya]], *Equivariant Principal Bundles over the 2-Sphere* ([arXiv:1902.06293](https://arxiv.org/abs/1902.06293))

See also:

* {#Zou20} [[Foling Zou]], _Notes on equivariant bundles_ ([arXiv:2008.01268](https://arxiv.org/abs/2008.01268))




### Equivariant vector bundles

On equivariant [[vector bundles]]:

* [tom Dieck 87, Section I.9](#tomDieck87)

In the context of [[equivariant K-theory]]:

* {#Segal68} [[Graeme Segal]], Section 1 of: _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 (1968) p. 129-151 ([numdam:PMIHES_1968__34__129_0](http://www.numdam.org/item/PMIHES_1968__34__129_0))

* {#HJJS08} [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin  Schottenloher]], Section 13 of: _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Springer Lecture Notes in Physics __726__, 2008, ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf), [doi:10.1007/978-3-540-74956-1](https://link.springer.com/book/10.1007/978-3-540-74956-1))

In a context of [[equivariant differential topology]]:

* {#Wasserman69} [[Arthur Wasserman]], section 2 of: _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 (<a href="https://doi.org/10.1016/0040-9383(69)90005-6">doi:10.1016/0040-9383(69)90005-6</a>[pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))




### As twists for twisted equivariant K-theory

On equivariant pricipal bundles with [[structure group]] the [[projective unitary group]], hence providing twists for [[twisted equivariant K-theory]]:


* {#BarcenasEspinozaJoachimUribe12} Noe Barcenas, Jesus Espinoza, [[Michael Joachim]], [[Bernardo Uribe]], _Universal twist in Equivariant K-theory for proper and discrete actions_ ([doi:10.1112/plms/pdt061](https://doi.org/10.1112/plms/pdt061), [arXiv:1202.1880](https://arxiv.org/abs/1202.1880))

* [Uribe-Lueck 14, Sec 15](#UribeLueck14)


### For equivariant elliptic cohomology

In a context of [[equivariant elliptic cohomology]]:

* [[Matthew Ando]], [[John Greenlees]], Part I of: _Circle-equivariant classifying spaces and the rational equivariant sigma genus_, Math. Z. 269, 1021–1104 (2011) ([arXiv:0705.2687](https://arxiv.org/abs/0705.2687), [doi:10.1007/s00209-010-0773-7](https://doi.org/10.1007/s00209-010-0773-7))

### For gauge theory on orbifolds

The general notion of equivariant bundles from [tom Dieck 69](#tomDieck69) (with [[action]] of the [[semidirect product]] of the [[gauge group]] with the [[equivariance group]]) gets a brief mentioning in

* {#Horava96} [[Petr Hořava]], Section 5.3 of: _Chern-Simons Gauge Theory on Orbifolds: Open Strings from Three Dimensions_, J. Geom. Phys. 21:1-33, 1996 ([arXiv:hep-th/9404101](https://arxiv.org/abs/hep-th/9404101))

in a context of [[Chern-Simons theory]] on [[orbifolds]].


[[!redirects equivariant bundles]]

[[!redirects equivariant principal bundle]]
[[!redirects equivariant principal bundles]]

[[!redirects equivariant fiber bundle]]
[[!redirects equivariant fiber bundles]]

[[!redirects equivariant vector bundle]]
[[!redirects equivariant vector bundles]]

