+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _geometric [[homotopy group]]s_ of a [[Lie groupoid]] $X$ are those of its [[nLab:geometric realization]] $|X|$ when regarded as a [[simplicial manifold]]. Equivalently, regarding $X$ as an object in the [[(∞,1)-topos]] [[∞LieGrpd]], its homotopy groups are those of the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\Pi(X) \in $ [[∞Grpd]].
 
## Definition

For $X = (X_1 \stackrel{\to}{\to} X_0)$ a [[Lie groupoid]] and $x : * \to X$ a [[point]], let 

$$
  X_\bullet = 
  \left(
    \cdots
    X_1 \times_{X_0} X_1 \times_{X_0} X_1 
   \stackrel{\to}{\stackrel{\to}{\to}}X_1 \times_{X_0} X_1 \stackrel{\to}{\to} X_0
  \right)
$$

be its [[nerve]] regarded as a [[simplicial manifold]]. 

+-- {: .un_remark}
###### Remark

When regarding each manifold $X_n$ as a [[diffeological space]], hence a [[sheaf]] on the [[site]] [[CartSp]] then $X_\bullet in PSh(CartSp)^{\Delta^{op}} \simeq [CartSp^{op},sSet]$ is the [[simplicial presheaf]] on [[CartSp]] that presents $X$ as an object in the [[(∞,1)-topos]] [[∞LieGrpd]] of [[∞-Lie groupoid]]s.

=--

+-- {: .un_defn}
###### Definition

Regard $X_\bullet$ as a [[simplicial topological space]] by forgetting the [[smooth structure]]. Write $|X_\bullet| \in $ [[Top]] for its [[geometric realization of simplicial topological spaces|geometric realization as a simplicial topological space]].

The **geometric homotopy groups** of $X$ are defined to be the ordinary [[homotopy group]]s of the [[topological space]] $|X_\bullet|$:

$$
  \pi_n(X,x) := \pi_n(|X_\bullet|,x)
  \,.
$$


=--

In this form the definition originates in ([Segal](#Segal)).


## Properties

Regard $X$ as an [[∞-Lie groupoid]] under the natural embedding $LieGrpd \hookrightarrow \infty LieGrpd$. By the discussion at [[∞LieGrpd]] this is a [[locally ∞-connected (∞,1)-topos]], which means that its terminal [[geometric morphism]] comes with a further [[left adjoint]] $\Pi$

$$
  (\Pi \dashv \Delta \dashv \Gamma) : \infty LieGrpd \to \infty Grpd
  \,.
$$

We say that $\Pi(X) \in \infty Grpd \simeq Top$ is the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] of $X$.


+-- {: .un_prop}
###### Observation

The geometric homotopy groups of $X$ are those of $\Pi(X) \in Top$.

=--

+-- {: .proof}
###### Proof


By the discussion at [[∞-Lie groupoid]] we have precisely that $\Pi(X)$ is presented by the [[geometric realization]] of the [[simplicial topological space]] underlying the [[nerve]] of $X$.

=--



## References

The definition of the homotopy groups of a Lie groupoid as those of its geometric realization appearently goes back to 

* [[Graeme Segal]], _Classifying spaces and spectral sequences_ , IHES Publ. Math. 34 (1968) 105&#8211;112.
{#Segal}

An equivalent definition is in

* A. Haefliger, Groupo&#239;des d'holonomie et espaces classiants , Ast&#233;risque 116 (1984), 70-97

reproduced in section 3 of

* [[Graeme Segal]], _Classifying spaces related to foliations_ , Topology 17 (1978), 367-382.


[[!redirects fundamental group of a Lie groupoid]]

[[!redirects homotopy groups of Lie groupoids]]