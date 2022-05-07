
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $G$ a [[topological group]] [[action|acting]] on a [[topological space]] $X$, its _Borel construction_ or _Borel space_ is another topological space $X \times_G E G$, also known as the [[homotopy quotient]]. In many cases, its ordinary [[cohomology]] is the $G$-[[equivariant cohomology]] of $X$.

## Definition

For $X$ a [[topological space]], $G$ a [[topological group]] and $\rho\colon G \times X \to X$ a [[continuous map|continuous]] $G$-[[action]] (a [[topological G-space]]), the **Borel construction** of $\rho$ is [[generalized the|the]] [[topological space]] $X \times_G E G$, hence [[quotient]] of the [[product]] of $X$ with the total space of [[generalized the|the]] $G$-[[universal principal bundle]] $E G$ by the [[diagonal]] [[action]] of $G$ on both.

Analogously, for $\mathcal{G}$ a [[simplicial group]] and $\mathcal{G} \times X \xrightarrow{\;\;} X$ a [[simplicial group action]], its Borel construction is the [[quotient]]

\[
  \label{BorelConstructionInSimplicialSets}
  \frac
  { W \mathcal{G}  \times X}
  {\mathcal{G}}
  \;\;\;
  \in
  \;\;
  SimplicialSets
\]

of the [[Cartesian product]] of $X$ with the [[universal principal simplicial complex]] $W \mathcal{G}$ by the [[diagonal action]] of $\mathcal{G}$ on these.


## Properties

### Homotopy-theoretic properties
 {#ModelCategoryTheoreticProperties}

#### In simplicial sets

\begin{prop}\label{BorelConstructionIsRightQuillenFunctor}
  The simplicial Borel construction (eq:BorelConstructionInSimplicialSets) is a [[right Quillen functor]] in a [[Quillen equivalence]]

$$
  \big(
    W \mathcal{G} \times (-)
  \big)
  \;\;
  \colon
  \;\;
  \mathcal{G}Actions(sSet)_{proj}
  \xrightarrow{\;\;\;}
  \big(sSet_{Qu}\big)_{\overline W \mathcal{G}}
$$
from the projective [[model structure on simplicial group actions]] to the [[slice model structure]] of the [[classical model structure on simplicial sets]] over the [[simplicial classifying space]] of $\mathcal{G}$.
\end{prop}

([DDK 80, Prop. 2.3, Prop. 2.4](#DDK80), see at *[[Borel model structure]]* for more)

As an example:

\begin{example}\label{ProjectionToSimplicialClassifyingSpaceIsKanFibration}
  If the underlying simplicial set $X \in sSet$ is a [[Kan complex]],
  then the quotient projection from the Borel construction (eq:BorelConstructionInSimplicialSets) to the [[simplicial classifying space]] is a [[Kan fibration]]
  $$
    \big(
      W\mathcal{G} \times X
    \big)
    \big/
    \mathcal{G}
    \xrightarrow{\in Fib} 
    \overline{W}\mathcal{G}
    \,,
  $$

This follows because the morphism is the image of the terminal morphism $X \xrightarrow{\;} \ast$ under the [[right Quillen functor]] from Prop. \ref{BorelConstructionIsRightQuillenFunctor}, hence is a fibration if $X \to \ast$ is.
\end{example}
For generalization of this statement to [[simplicial presheaves]] see [NSS 12b, Thm. 3.91](#NSS12b).

#### In topological spaces
 {#HomotopyPropertiesInTopologicalSpaces}

In the following, we write $TopSp$ for the [[convenient category of topological spaces|convenient category]] of [[compactly generated weak Hausdorff spaces]].

Let 

* $G \,\in\, Grp(TopSp)$ be a [[topological group]] which is [well-pointed](simplicial+topological+group#WellPointedSimplicialTopologicalGroup) in that the inclusion of the [[neutral element]] is a [[Hurewicz cofibration]] [hence](Hurewicz+cofibration#HurewiczCofibrationsInCGWHSpacesAreClosed) a [[closed cofibration]].

* $X \,\in\, G Act(TopSp)$ be a ([[compactly generated weak Hausdorff space|cgwh]])-[[topological G-space]].

\begin{prop}\label{HomotopyFiberSequenceofTopologicalBorelConstruction}
Then the topological [[Borel construction]] $(X \times E G)/G$ fits into a [[homotopy fiber sequence]] of the form

\[
  \label{HomotopyFiberSequenceOfTopologicalBorelConstruction}
  X 
    \xrightarrow{\;\;} 
  \frac{ 
    X \times EG
  }{
    G
  } 
    \xrightarrow{\;\;}
  B G
  \,.
\]

\end{prop}
\begin{proof}
  The sequence (eq:HomotopyFiberSequenceOfTopologicalBorelConstruction) is the image under [[geometric realization of simplicial topological spaces]] of the sequence of [[simplicial topological spaces]]

\[
  \label{TopologiCALBorelConstructionFiberSequenceLevelOfSimplicialSpaces}
  const(X)_\bullet
    \xrightarrow{\;\;\;}
  X \times G^{\times^\bullet}
    \xrightarrow{\;\;\;}
  G^{\times^\bullet}
\]

which, in turn, is the image under passage to [[nerves]] of the sequence of [[topological groupoids]]

$$
  (X \rightrightarrows X)
    \xrightarrow{\;\;}
  (X \times G \rightrightarrows X)
    \xrightarrow{\;\;}
  (G \rightrightarrows \ast)
  \,,
$$

with the [[action groupoid]] in the middle and the [[delooping groupoid]] on the right.

Therefore, by the general respect of geometric realization for homotopy fiber products ([this Prop.](geometric+realization+of+simplicial+topological+spaces#SufficientConditionsForRealizationToPreserveHomotopyPullback)) it is now sufficient to observe that

1. the simplicial topological spaces appearing in (eq:TopologiCALBorelConstructionFiberSequenceLevelOfSimplicialSpaces) are all [[good simplicial topological space|good]] (so that their geometric realization models their [[homotopy colimit]]);

1. the sequence (eq:TopologiCALBorelConstructionFiberSequenceLevelOfSimplicialSpaces) of simplicial topological spaces is degreewise a homotopy fiber sequence of topological spaces;

1. the morphism $X \times G^{\times^\bullet} \to G^{\times^\bullet}$ is a homotopical Kan fibration (see [here](geometric+realization+of+simplicial+topological+spaces#eq:HomotopyTheoreticKanFibration)).

For the first condition observe that the degeneracy maps of the [[nerve]] of an  [[action groupoid]] are all of the form $X \times G^{n} \times ( \{e\} \xhookrightarrow{\;} G)$, hence are closed cofibrations (by [this Example](Hurewicz+cofibration#KifiedProductsOfCofibrationsWithCompactlyGeneratedSpaces)).

For the second condition, observe  that [[projections]] $X \times G^n \to G^n$ are evidently [[Serre fibrations]] whose ordinary [[fiber]] is $X$, so that $X \to X \times G^n \to G^n$ is a [[homotopy fiber sequence]] (by [this Prop.](homotopy+pullback#HomotopyPullbackByOrdinaryPullback)).

For the third point, notice that in the present case the horn-filling map [here](geometric+realization+of+simplicial+topological+spaces#eq:HomotopyTheoreticKanFibration) is in fact an [[isomorphism]], hence certainly surjective on connected components. 
\end{proof}


### As the realization of the action groupoid

This Borel construction is naturally understood as being the [[geometric realization of simplicial topological spaces|geometric realization]] of the [[topological groupoid|topological]] [[action groupoid]] $X // G$ of the [[action]] of $G$ on $X$:

the [[nerve]] of this topological groupoid is the [[simplicial topological space]]

$$
  (X \sslash G)_\bullet =
  \left(
 \cdots X \times G \times G \stackrel{\to}{\stackrel{\to}{\to}} X \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}} X
  \right)
  \,.
$$ 

Observing that $E G = G \sslash G$ itself as a groupoid has the nerve

$$
  (E G)_\bullet
   = 
   \left(
   \cdots 
   G \times G \times G 
     \stackrel{\to}{\stackrel{\to}{\to}}
   G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}} G
  \right)
$$

(where "$\cdot$" denotes the multiplication action of $G$ on itself) and regarding $X$ and $G$ as topological 0-groupoids ($G$ as a group object in topological 0-groupoids), hence with simplicially constant nerves, we have an [[isomorphism]] of simplicial topological spaces

$$
  (X //G)_\bullet 
    \simeq_{iso}
  X \times_G (E G)_\bullet
  \,.
$$

If this is set up in a sufficiently nice category of topological spaces, then, by the discussion at [[geometric realization of simplicial topological spaces]], the geometric realization ${\vert{-}\vert}\colon Top^{\Delta^{op}} \to Top$ manifestly takes this to the Borel construction (since, by the discussion there, it preserves the product and the quotient).

### As a homotopy colimit over the category associated to $G$

If $G$ is the topological category associated to the group $G$, then a $G$-space is precisely a Top-enriched functor $G\to Top$ in a similar fashion to the fact that an  R-module is an Ab-enriched functor. If $X$ is a $G$-space, the ordinary quotient $X/G$ is the colimit of the diagram associated to $X$ and the Borel construction is (a model of) the homotopy colimit of that diagram. This is a reason for calling the Borel construction homotopy quotient in some contexts.

### In rational homotopy theory

The image of the Borel construction in [[rational homotopy theory]] is the [[Weil model]] for [[equivariant de Rham cohomology]]. See there for more.

\begin{xymatrix}
  &
  X \times E G \ar@(ul,ur)^G
  \ar[d]^-{ q }
  &
  \Omega^\bullet( X )
  \otimes 
  W(g)
  \ar@(ur,ul)_{ g }
  \ar@{<-^{)}}[d]^-{ q^\ast }
  \\
  \;
  X // G
  \ar@{}[r]|-{
    \simeq_{\mathrm{whe}}
  }
  &  
  \big(
    X \times E G 
  \big)/G
  &
  \big(
    \Omega^\bullet( X )
    \otimes 
    W(g)
  \big)_{\mathrm{basic}} 
  \ar@{<-}[r]^-{ :\exp\big( t^a \iota_a\big): }_-{\simeq}
  &
  \big(
    \Omega^\bullet( X )\big[ r^a \big]
  \big)^G
  \\
  &
  \mbox{Borel construction}
  &
  \mbox{Weil model}
  &
  \mbox{Cartan model}
\end{xymatrix}



## Related concepts

* [[simplicial classifying space]]

* [[Borel equivariant cohomology]]

  * [[equivariant ordinary cohomology]]

  * [[equivariant de Rham cohomology]]



## References

As a [[right Quillen functor]] on the [[model structure on simplicial group actions]]:

* {#DDK80} [[Emmanuel Dror]], [[William Dwyer]], [[Daniel Kan]], _Equivariant maps which are self homotopy equivalences_, Proc. Amer. Math. Soc. 80 (1980), no. 4, 670&#8211;672 ([jstor:2043448](http://www.jstor.org/stable/2043448))

Lecture notes in classical [[topology]]:

* [[Stephen Mitchell]], _Notes on principal bundles and classifying spaces_, 2011 ([pdf](https://sites.math.washington.edu/~mitchell/Notes/prin.pdf), [[MitchellPrincipalBundles.pdf:file]])

General statement in [[simplicial homotopy theory]] of [[simplicial presheaves]]:

* [[J. F. Jardine]], _Stacks and the homotopy theory of simplicial sheaves_ ([pdf](http://www.math.uiuc.edu/K-theory/0450/stacks3.pdf))

* {#NSS12b} [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], Prop. 3.73 in: _Principal $\infty$-bundles -- Presentations_,  Journal of Homotopy and Related Structures, Volume 10, Issue 3 (2015), pages 565-622 ([arXiv:1207.0249](http://arxiv.org/abs/1207.0249), [doi:10.1007/s40062-014-0077-4](http://link.springer.com/article/10.1007/s40062-014-0077-4))


The nature of the Borel construction as the geometric realization of the action groupoid is mentioned for instance in 

* [[Alejandro Adem]], Michele Klaus, _Lectures on orbifolds and group cohomology_ ([pdf](http://www.math.ubc.ca/~adem/hangzhou.pdf))


[[!redirects Borel construction]]
[[!redirects Borel constructions]]

[[!redirects Borel space]]
[[!redirects Borel spaces]]
