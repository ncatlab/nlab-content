
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

## Idea

### General

Generally, given some kind of [[space]] equipped with the [[action]] of a [[group]], the locus of _[[fixed points]]_ of the action may form a suitable sub-space: the _fixed point space_.

### For topological $G$-spaces

Specifically, given a [[topological group]] $G$ and a [[topological G-space]], its _fixed point space_ is the set of the set-theoretic [[fixed points]] of the $G$-[[action]], equipped with the [[subspace topology]].

For more see at _[[topological G-space]]_ the section _[Change of groups and fixed loci](topological+G-space#ChangeOfGroupsAndFixedLoci)_.

### In equivariant homotopy theory

The statement of [[Elmendorf's theorem]] is essentially that the [[equivariant homotopy theory]] of [[G-space|topological $G$-spaces]] is equivalently encoded in their systems of $H$-fixed point spaces, as $H$ varies over [[closed subspace|closed]] [[subgroups]] of $G$.

### In equivariant stable homotopy theory

In [[equivariant stable homotopy theory]] the concept of fixed point spaces branches into various closely related, but different concepts:

* [[fixed point spectra]],

* [[geometric fixed point spectra]]

* [[categorical fixed point spectra]]

### In equivariant differential topology

In [[equivariant differential topology]]:

+-- {: .num_prop #ExistenceOfGInvariantTubularNeighbourhoods}
###### Proposition
**(existence of $G$-invariant [[tubular neighbourhoods]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

If $\Sigma \overset{\iota}{\hookrightarrow} X$ is a [[closed manifold|closed]] [[smooth manifold|smooth]] [[submanifold]] inside the $G$-[[fixed locus]]

\begin{center}
  \begin{xymatrix}
    \Sigma 
    \ar@{^{(}->}[rr]^-{\iota^G}
    \ar@{^{(}->}[dr]_{\iota}
    &&
    X^G
    \ar@{^{(}->}[dl]
    \\
    & 
    X
  \end{xymatrix}
\end{center}


then $\Sigma$ admits a $G$-invariant [[tubular neighbourhood]] $\Sigma \subset U \subset X$.

Moreover, any two choices of such $G$-invariant tubular neighbourhoods are $G$-equivariantly [[isotopy|isotopic]].

=--

([Kankaanrinta 07, theorem 4.4, theorem 4.6](equivariant+differential+topology#Kankaanrinta07))


+-- {: .num_prop #FixedLociOfSmoothProperActionsAreSubmanifolds}
###### Proposition
**([[fixed loci]] of [[smooth function|smooth]] [[proper actions]] are [[submanifolds]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

Then the $G$-[[fixed locus]] $X^G \hookrightarrow X$ is a [[smooth manifold|smooth]] [[submanifold]].

=--

(see also [this MO discussion](https://math.stackexchange.com/a/1739784/58526))

+-- {: .proof}
###### Proof

Let $x \in X^G \subset X$ be any [[fixed point]]. Since this is in particular a closed invariant [[submanifold]], Prop. \ref{ExistenceOfGInvariantTubularNeighbourhoods} applies and shows that an [[open neighbourhood]] of $x$ in $X$ is $G$-equivariantly [[diffeomorphism|diffeomorphic]] to a [[linear representation]] $V \in RO(G)$. The [[fixed locus]] $V^G \subset V$ of that is hence [[diffeomorphism|diffeomorphic]] to an [[open neighbourhood]] of $x$ in $\Sigma$.

=--


+-- {: .num_remark}
###### Remark

Without the assumption of [[proper action]] in Prop. \ref{FixedLociOfSmoothProperActionsAreSubmanifolds} the conclusion generally fails. See [this MO comment](https://math.stackexchange.com/a/1739768/58526) for a counter-example.

=--

## Properties

### Fixed point adjunction
 {#FixedPointAdjunction}

For $G$ a [[topological group]], consider the [[category]] of [[TopologicalGSpaces]].

For $H \subset G$ any [[subgroup]], consider 

* the [[coset space]] $G/H \in Topological G Spaces$;

* the [[Weyl group]] $W_H(G) \coloneqq N_G(H)/H \in TopologicalGroups$.

Observing that for $X \in Topological G Spaces$ the $H$-fixed locus $X^H$ inherits a canonical action of $N(H)/H$, we have a [[functor]]


\[
  \label{TopologicalHFixedLociAsFunctorToWeylGroupSpaces}
  Topological G Spaces
  \overset{ 
    \;\;\;
      (-)^H
    \;\;\; 
  }{\longrightarrow }
  Topological N(H)/H Spaces
\]

Notice that $G$ [[action|acts]] canonically on the left of $G/H$, while $N(H)/H$ still acts from the _right_ (both by group multiplication on representatives):

$$
  \array{
    G/H \times N(H)/H 
    &\overset{}{\longrightarrow}&
    G/H
    \\
    \big( 
      g H, n H
    \big)
    &\mapsto&
    g H n H
    \mathrlap{
    \,=\,
    g n \underset{H}{\underbrace{n^{-1} H n}} H
    \,=\,
    g n H
    }
  }
$$

Therefore there exists a [[functor]] in the other direction:

$$
  \array{
    Topological N(H)/H Spaces
    &
      \overset{ 
        \;\;\;
        G/H \times_{N(H)/H} (-)
        \;\;\;
      }{\longrightarrow}
    &
    Topological G Spaces
  }
  \,.
$$

\begin{prop}\label{PassageToFixedLociIsRightAdjoint}
**(passage to fixed loci is a [[right adjoint]])** \linebreak
These are [[adjoint functors]], with the $H$-fixed locus functor (eq:TopologicalHFixedLociAsFunctorToWeylGroupSpaces) being the [[right adjoint]]:

\[
  \label{AdjunctionBetweenHFixedPointsAndNHExtension}
  Topological G Spaces
  \underoverset
    {
      \underset{
        (-)^H
      }{\longrightarrow}
    }
    {
      \overset{
        G/H \times_{N(H)/H} (-)
      }{
        \longleftarrow
      }
    }
    {\;\;\;\;\;\;\; \bot \;\;\;\;\;\;\;}
  Topological N(H)/H Spaces
  \,.
\]

\end{prop}

\begin{proof}

To see the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) characterizing this [[adjunction]], consider for $X \in Topological N(H)/H Spaces$ and $Y \in Topological G Spaces$ a $G$-[[equivariant]] [[continuous function]]

$$
  G/H \times_{N(H)/H}  Y
  \overset{
    \;\;\;
    f  
    \;\;\;
  }{\longrightarrow}
  X
  \,.
$$

This restricts to an $N(H)$-[[equivariant function]] on the $N(H)$-[[topological subspace]] 

$$
  \array{
    Y &\overset{\;\;\;}{\hookrightarrow}& G/H \times_{N(H)/H} Y
    \\
    y &\mapsto&  \big[ e H , y \big]
  }
$$

Since $Y$ is a fixed locus for $H \subset N(H)$, by [[equivariant function|equivariance]] this restriction has to factor through the $H$-fixed locus $X^H$ of $X$:

$$
  \array{
    Y &\subset& G/H \times_{N(H)/H} Y
    \\
    {}^{\mathllap{
      \tilde f
    }}
    \big\downarrow 
    &&
    \big\downarrow {}^{\mathrlap{f}}
    \\
    X^H &\subset& X
  }
$$

But given that and since every other point of $G/H \times_{N(H)/H} Y$ is an image under the $G$-action of a point in $Y \subset G/H \times_{N(H)/H}$, this restriction $\tilde f$ already determines $f$ uniquely. 

Since this construction is manifestly [[natural transformation|natural]] in $Y$ and $X$, we have a  [[natural bijection]] $f \leftrightarrow \tilde f$, which establishes the [hom-isomorphism](adjoint+functor#InTermsOfHomIsomorphism) for the pair of [[adjoint functors]] in (eq:AdjunctionBetweenHFixedPointsAndNHExtension).

\end{proof}

\begin{remark}

The adjunction (eq:AdjunctionBetweenHFixedPointsAndNHExtension) factors as:

\[
  Topological G Spaces
  \underoverset
    {
      \underset{
      }{\longrightarrow}
    }
    {
      \overset{
        G \times_{N(H)} (-)
      }{
        \longleftarrow
      }
    }
    {\;\;\;\;\;\;\; \bot \;\;\;\;\;\;\;}
  Topological N(H) Spaces
  \underoverset
    {
      \underset{
        (-)^H
      }{
        \longrightarrow
      }
    }
    {
      \overset{
        N(H)/H \times_{N(H)/H} (-)
      }{
        \longleftarrow
      }
    }
    {\;\;\;\;\;\;\; 
     \bot
     \;\;\;\;\;\;\;}
  Topological N(H)/H Spaces
  \,.
\]

Here the functor on the top right, $N(H)/H \times_{N(H)/H} (-)$, is the identity on the underlying topological spaces, but extends the action from $N(H)/H$ to $N(H)$, namely through the projection homomorphims $N(H) \to N(H)/H$.

For more on this see at _[Topological G-space -- Fixed loci with residual Weyl gorup action](topological+G-space#FixedLociWithResidualWeylGroupAction)_:

\begin{tikzcd}[column sep=large]
  G\mathrm{Spaces}
  \ar[
    rr,
    shift right=7pt,
    "(N(H) \hookrightarrow G)^\ast"{below}
  ]
  \ar[
    rr,
    phantom,
    "\scalebox{.7}{$\bot$}"
  ]
  \ar[
    rrrr,
    rounded corners,
    to path={ 
         -- ([yshift=-20pt]\tikztostart.south) 
         --node[below]{\scalebox{.7}{$(-)^H$}} ([yshift=-20pt]\tikztotarget.south) 
         -- (\tikztotarget.south)}
  ]
  &&
  N\!(H)\mathrm{Spaces}
  \ar[
    ll,
    shift right=7pt,
    "G \times_{N\!(H)} (-)"{above}
  ]
  \ar[
    rr,
    shift right=7pt,
    "{
      \mathrm{Maps}
      (
        N\!(H)\!/H,
        -
      )^{N\!(H)}
    }"{below}
  ]
  \ar[
    rr,
    phantom,
    "\scalebox{.7}{$\bot$}"
  ]
  &&
  \big(
    N\!(H)\!/H
  \big)\mathrm{Spaces}
  \ar[
    ll,
    shift right=7pt,
    "{
      ( N\!(H) \twoheadrightarrow N\!(H)\!/H )^\ast
    }"{above}
  ]
  \ar[
    llll,
    rounded corners,
    to path={
         -- ([yshift=+20pt]\tikztostart.north)
         --node[above]{\scalebox{.7}{$G/H \times_{N\!(H)\!/H}(-)$}} ([yshift=+20pt]\tikztotarget.north)
         -- (\tikztotarget.north)}
  ]
\end{tikzcd}


\end{remark}

\linebreak


## Related concepts

* [[homotopy fixed points]]

* [[Elmendorf's theorem]]

* [[equivariant differential topology]]

[[!redirects fixed point spaces]]

[[!redirects fixed point set]]
[[!redirects fixed point sets]]

[[!redirects fixed locus]]
[[!redirects fixed loci]]

[[!redirects fixed point subspace]]
[[!redirects fixed point subspaces]]


