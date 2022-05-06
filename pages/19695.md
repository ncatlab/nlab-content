
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


