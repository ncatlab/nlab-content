
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
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

A _spherical space form_ is a [[quotient space]] $S^n/G$ of a [[round sphere|round]] [[Riemannian manifold|Riemannian]] [[n-sphere]] ($n \geq 2$) by a [[subgroup]] $G$ of its [[isometry group]], which [[action|acts]] [[free action|freely]] and [[properly discontinuous action|properly discontinuously]]. 

Equivalently, a spherical space form is a [[Riemannian manifold]] of [[constant function|constant]] [[positive number|positive]] [[sectional curvature]] (an [[elliptic geometry]]) which is [[connected topological space|connected]] and [[geodesically complete Riemannian manifold|geodesically complete]] (see e.g. [Gadhia 07, Lemma 5](#Gadhia07)).

The spherical space forms are one of three classical examples of _[[Clifford-Klein space forms]]_.

Their classification was raised as an open problem by [Killing 1891](#Killing1891) and a complete solution was finally compiled by ([Wolf 74](#Wolf74)) (reviewed in [Gadhia 07, section 2.2](#Gadhia07)). A re-proof of the classification is claimed in ([Allock 15](#Allock15)). 


For more on this see at _[[group actions on n-spheres]]_.


## Examples

### 7-dim spherical space forms with $Spin$-structure
 {#7DSphericalSpaceFormsWithSpinStructure}

For $n =7$ all the groups $G$ in [Wolf's classification](#Wolf74) [[action|act]] as [[subgroups]] of [[special orthogonal group|SO(8)]], the latter equipped with its defining action on $\mathbequib{R}^8$ restricted to the action on $S^7 = S(\mathbb{R}^8) \subset \mathbb{R}^8$.

Therefore one may consider the [[lift]] $\widehat{G}$ of these [[subgroups]] to subgroups of the [[spin group]] $Spin(8) \to SO(8)$ through the [[double cover]]-projection. Such a lift corresponds to a choice of [[spin structure]] on the [[spherical space form]] $S^7/G$.  These Spin-lifts $\widehat{G}$, have been classified in ([Gadhia 07](#Gadhia07)).

Given any such lift $\widehat{G} \subset Spin(8)$, one may consider its [[action|action]] on the two [[irreducible representation|irreducible]] [[real spin representations]] $\mathbf{8}_\pm$ of $Spin(8)$. Write

$$
  N_\pm \;\coloneqq\; dim_{\mathbb{R}}\left( \left(\mathbf{8}_{\pm}\right)^{\widehat{G}} \right)
$$

for the [[dimension]] of the subspace of [[spinors]] that are [[fixed point|fixed]] by the action of $\widehat{G}$. For $\widehat{G}$ non-[[trivial group|trivial]], we have 

$$
  (N_+, N_-) = (N,0)
  \phantom{AA} \text{or} \phantom{AA} 
  (N_+, N_-) = (0,N)
$$

and hence up to a choice of [[orientation]] there is a unique 

$$
  N \in \{0,1,\cdots, 8\}
$$

associated with each 7-dimensional [[spherical space form]] equipped with [[spin structure]].

Hence this allows to stratify [Wolf's classification](#Wolf74) of 7-dimensional spherical space forms, first into the cases that do and that do not admit any [[spin structure]], and then the former further into the dimension $N$ of the space of [[Killing spinors]] that they carry.

In the case  $N \geq 4$
It turns out that the resulting sub-classification demands $\widehat{G}$ to be a [[finite subgroup of SU(2)]]; hence this is an [[ADE classification]] ([MFFGME 09, Sections 3-7](#MFFGME09)):

* $N = 8$: here $\widehat{G} = \mathbb{Z}/2$, the [[cyclic group of order 2]];

* $N = 7$: does not occur;

* $N = 6$: here $\widehat{G} = \mathbb{Z}/k$ (for $k \gt 2)$, a [[cyclic group]];

* $N = 5$: here $\widehat{G} = $ a non-[[cyclic group|cyclic]] [[finite subgroup of SU(2)]], hence a [[binary dihedral group]] or the [[binary tetrahedral group]] or [[binary octahedral group]] or [[binary icosahedral group]], [[diagonal action|acting diagonally]] on $\mathbb{R}^8 \simeq \mathbb{H} \oplus \mathbb{H}$;

* $N = 4$: here $\widehat{G} = $ any [[finite subgroup of SU(2)]] _except_ the [[binary tetrahedral groups]], but acting via the [[diagonal action]] composed with a suitable non-trivial [[outer automorphism]] of $\widehat{G}$ on one of the two sides.

(In the last case, while there is one nontrivial outer automorphism of the binary tetrahedral group, its twisted action yields $N =5$, hence is equivalent to one of the previous cases ([MFFGME 09, section 7.3](#MFFGME09)).)


[[!include 7d spherical space forms -- table]]


This analysis applies to the classification of the [[near horizon geometry]] of smooth (i.e. non-[[orbifold]]) $\geq \tfrac{1}{2}$ [[BPS state|BPS]] [[black brane|black]] [[M2-brane]]-solutions of the [[equations of motion]] of [[11-dimensional supergravity]]:

These are the [[Cartesian product]] $AdS_4 \times (S^7/G)$ of 4-[[dimension|dimensional]] [[anti de Sitter spacetime]] with a 7-[[dimension|dimensional]] [[spherical space form]] $S^7/G$ with [[spin structure]] and $N \geq 4$, as above ([MFFGME 09](#MFFGME09)).

## Properties


### Concordances of higher gerbes over spherical space forms
 {#HigherGerbesOnSphericalSpaceForms}

We discuss the [[concordance]] [[infinity-groupoid|$\infty$-groupoid]] of $\Gamma$-[[principal bundles]] on [[spherical space forms]] $S^{n+2}/G$ (Def. \ref{ShapesOfMappingStacks} below)
in the case that the [[topological group]] $\Gamma$ is a [[braided infinity-group|braided]] [[homotopy n-type]] (Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms} below). 

The claim of Theorem \ref{ComparisonMapOfConcordanceInfinityGroupoidsIsEquivalence} below is that this is equivalently the [[hom infinity-groupoid|hom $\infty$-groupoid]] of maps of [[classifying spaces]] $B G \to B \Gamma$.

In the special case that $\Gamma \,=\, $ [[PU(ℋ)]], this result recovers (Example \ref{EquivariantClassifyingSpaceOfPUHBundles} below) the [[equivariant homotopy groups]] of the [[equivariant classifying space]] for [[equivariant principal bundles|equivariant $PU(\mathcal{H})$-principal bundles]] (originally due to [Uribe et al., 2014](twisted+equivariant+K-theory#BEJU14)) -- a statement which falls out of the scope of most traditional theory of [[equivariant principal bundles]] since [[PU(ℋ)]] is not a [[compact Lie group]].

Conversely, Thm. \ref{ComparisonMapOfConcordanceInfinityGroupoidsIsEquivalence} generalizes this classification of equivariant $PU(\mathcal{H})$-principal bundles to any [[braided infinity-group|braided]] [[homotopy n-type|$n$-truncated]] [[structure group]], at the (small) cost of requiring that the [[equivariance group]] corresponds to some $\geq n+2$-dimensional [[spherical space form]]  -- in which case it is essentially an incarnation (via the proof of Prop. \ref{ConcordancesOnSphericalSpaceFormIsMapsOfClassifyingSpaces} below) of the [[smooth Oka principle]] over that spherical space form.



\linebreak

* *[Preliminaries](#Preliminaries)*

* *[The classification theorem](#TheClassificationTheorem)*

* *[Lemmas and proofs](#LemmasAndProofs)*

\linebreak



#### Preliminaries
 {#Preliminaries}

Concretely, we consider the following situation:

\begin{definition}
\label{AssumptionForHigherGerbesOnSphericalSpaceForms}
**Assumption.** 
\linebreak
In the following, let

1. $n \in \mathbb{N}$ be a [[natural number]],

1. $\Gamma \,\in\, Grp(TopSp)$ be a [[topological group]] whose [[underlying]] [[homotopy type]] [[infinity-group|$\infty$-group]] $Shp(\Gamma) \,\in\, Grp\big( Grpd_\infty \big)$ is 

   1. a [[braided infinity-group|braided]] in that its [[delooping]] still has [[infinity-group|$\infty$-group]]-structure itself

      \[
        \label{DeloopingOfShapeIsInfinityGroup}
        B Shp(\Gamma) \,\in\, Grp\big( Grpd_\infty \big)
        \,.
      \]

   1. a [[homotopy n-type]], hence [[n-truncated object of an (infinity,1)-category|n-truncated]] for some $n \in \mathbb{N}$:

   \[
     \label{GammaIsNTruncated}
     \tau_n Shp(\Gamma) \,\simeq\, Shp(\Gamma)
     \;\;\;
     \in
     \;
     Grp_\infty
     \,.
   \]

1. $S^{n+2}/G$ be a [[spherical space form]] of [[dimension of a manifold|dimension]] $n+2$, hence the [[topological quotient space|quotient space]] of the [[n-sphere|$(n+2)$-sphere]] $S^{n+2}$ 
by a [[free action]] of a [[finite group]]
$G \,\in\, Grp(FinSet) \xhookrightarrow{\;} Grp(TopSp)$. 

   We write

   \[
     \label{CoprojectionInDiscussionOfGerbesOnSphericalSpaceForms}
     S^{n+2}
     \overset{\phantom{--} q \phantom{--}}{\twoheadrightarrow}
     S^{n+2}/G
     \;\;\;
     \in
     \;
     TopSp
   \]

   for the [[quotient space]] [[coprojection]] onto the corresponding [[spherical space form]].

\end{definition}

\begin{example}
The archetypical examples of [[topological groups]] which satisfy Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms} are: 

1. The [[circle group]], $\Gamma = $ [[U(1)]], whose underlying homotopy type is that of the [[Eilenberg-MacLane space]] $K(\mathbb{Z},1)$, which is [[homotopy n-type|n-truncated]] for $n \geq 1$ 
and which is not just [[braided infinity-group|braided]] but even [[abelian infinity-group|abelian]] (i.e. [[E-infinity space|$E_\infty$]]);
with [[delooping]] $K(\mathbb{Z},2)$;

1. the [[projective unitary group]] on a [[complex vector space|complex]] [[separable Hilbert space]],  $\Gamma \,=\,$ [[PU(ℋ)]], whose underlying homotopy type is that of the [[Eilenberg-MacLane space]] $K(\mathbb{Z},2)$,  which is [[homotopy n-type|n-truncated]] for $n \geq 2$, 
which is not just [[braided infinity-group|braided]] but even [[abelian infinity-group|abelian]] (i.e. [[E-infinity space|$E_\infty$]]) with [[delooping]]  $K(\mathbb{Z},3)$.

Hence for both of these [[structure groups]], the 7-dimensional spherical space forms discussed [above](#7DSphericalSpaceFormsWithSpinStructure) satisfy Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms}.
\end{example}

\begin{definition}
**([[topological groupoids]] and their underlying [[D-topological space|D-]][[topological stacks]])**
\linebreak
We will write:

\[
  \label{TheTopologicalDeloopingGroupoidOfGamma}
  \array{
    Grp(TopSp)
    &
    \xrightarrow{\; Dtoplg \;}
    &
    Grp(DiffSp)  
    &
    \xrightarrow{\;}
    &
    Grpd(SmthGrp_{\infty})
    &
    \xrightarrow{\;}
    &
    SmthGrp_\infty
    \\
    \Gamma \rightrightarrows \ast
    &&
    &\mapsto&
    &&
    \mathbf{B}\Gamma
    \\
    G \rightrightarrows \ast
    &&
    &\mapsto&
    &&
    \mathbf{B}G
    \\
    S^{n+2} \times G \rightrightarrows S^{n+2}
    &&
    &\mapsto&
    &&
    S^{n+2}/G
  }
\]

for

1. the [[topological groupoids]] which are

   1. the [[delooping groupoids]] of $G$ and of $\Gamma$, respectively,

   1. the [[action groupoid]] $S^{n+2} \times G \rightrightarrows S^{n+2}$ of the given $G$-[[group action|action]] on $S^{n+2}$

1. their associated [[D-topological space|D-]][[topological stacks]], regarded as objects in [[smooth infinity-groupoid|$SmthGrpd_\infty$]].

\end{definition}
Notice, as indicated in the last row of (eq:TheTopologicalDeloopingGroupoidOfGamma), that the [[smooth stack]] correspinding to the [[action groupoid]] of $G$ acting on $S^{n+2}$ is [[equivalence in an (infinity,1)-category|equivalent]] to the quotient [[smooth manifold]] $S^{n+2}/G$ itself, due to the condiiton that the $G$-action is [[free action|free]].



\begin{lemma}
\label{CanonicalCechGroupoidOfGammaPrincipalBundlesOnSphericalSpaceForm}
**(canonical [[Cech groupoid]] of $\Gamma$-[[principal bundles]] on [[spherical space form]])**
\linebreak
  Under the truncation condition (eq:GammaIsNTruncated), 
  the [[groupoid]] of $\Gamma$-[[principal bundles]]  over $S^{n+2}/G$ ([[internalization|internal to]] [[TopSp]]) is [[equivalence of groupoids|equivalent]] to the groupoid of [[topological functors]] out of the [[action groupoid]] into the [[delooping groupoid]] (eq:TheTopologicalDeloopingGroupoidOfGamma), with [[continuous functions|continuous]] [[natural transformations]] between them:
$$
  \Gamma PrnBdl(TopSp)_{S^{n+2}/G}
  \;\;
  \simeq
  \;\;
  TopFunc
  \big(
    ( S^{n+2} \times G \rightrightarrows S^{n+2} )
    ,\,
    ( \Gamma \rightrightarrows \ast )
  \big)
  \,.
$$
Moreover, the analogous statement holds for bundles over the [[product topological space]] $S^{n+2}/G \times \Delta^k$ with the [[topological k-simplex]] for all $k \in \mathbb{N}$:
$$
  \Gamma PrnBdl(TopSp)_{S^{n+2}/G \times \Delta^k}
  \;\;
  \simeq
  \;\;
  TopFunc
  \big(
    ( S^{n+2} \times G \rightrightarrows S^{n+2} )
    \times \Delta^k
    ,\,
    ( \Gamma \rightrightarrows \ast )
  \big)
  \,.
$$
\end{lemma}
\begin{proof}
The $n$-truncation condition (eq:GammaIsNTruncated) on $\Gamma$ implies that its [[classifying space]] $B \Gamma \,\simeq\, Shp( \left\vert \Gamma \rightrightarrows \ast \right\vert  )$ is an $(n+1)$-type

$$
  \tau_{n+1} B \Gamma \,\simeq\, B \Gamma
  \;\;\;
  \in
  \;
  Grp_\infty
$$

and hence, by [[classifying space|classifying theory]], that every $\Gamma$-principal bundle on $S^{n+2}$ is [[isomorphism|isomorphic]] to the [[trivial bundle]]:

\[
  \label{UniqueGerbesOnNSphere}
  \tau_0 
  \big(
     \Gamma PrnBdl(TopSp)_{S^{n+2}}
  \big)
  \;\;
  \simeq
  \;\;
  \tau_0
  \,
  Maps
  \big(
    Shp(S^{n+2}) 
    ,\,
    B \Gamma
  \big)
  \;\;
  \simeq
  \;\;
  \ast
  \,.
\]

Therefore, every $\Gamma$-[[principal bundle]] on the spherical space form $S^n/G$ trivializes after being [[pullback bundle|pulled back]] along the coprojection $q$ (eq:CoprojectionInDiscussionOfGerbesOnSphericalSpaceForms). The corresponding [[Cech cohomology|Cech cocycle]] is a [[topological functor]]

$$
  \big(
    S^{n+2} \times G^{op} \rightrightarrows S^{n+2}
  \big)
  \xrightarrow{\;\; 
    (c_1 \rightrightarrows \ast) 
  \;\;}
  \big(
    \ast \times \Gamma^{op} \rightrightarrows \ast
  \big)
  =
  \big(
    \Gamma \rightrightarrows \ast
  \big)
$$

out of the [[action groupoid]] $S^{n+2} \times G^{op} \rightrightarrows X$ of $G$ acting on $S^n$ into the [[delooping groupoid]] $\Gamma \rightrightarrows \ast$:

\begin{tikzcd}
    {}
    \ar[d,-, dotted]
    &&
    {}
    \ar[d,-, dotted]
    \\
    S^{n+2} \times  G \times G 
    \ar[rr, "{c_2}"{above}]
    \ar[d, shift left=12pt]
    \ar[d]
    \ar[d, shift right=12pt]
    &&
    \Gamma \times \Gamma
    \ar[d, shift left=12pt]
    \ar[d]
    \ar[d, shift right=12pt]
    \\
    S^{n+2} \times G 
    \ar[rr, "c_1"{above}]
    \ar[d, shift left=6pt]
    \ar[d, shift right=6pt]
    \ar[u, shift right=6pt]
    \ar[u, shift left=6pt]
    &&
    \Gamma
    \ar[d, shift left=6pt]
    \ar[d, shift right=6pt]
    \ar[u, shift right=6pt]
    \ar[u, shift left=6pt]
    \\
    S^{n+2}
    \ar[rr, "{ }"{below, name=s, pos=.4}]
    \ar[d, ->>, "{ }"{right, name=t, pos=.7 }]
    \ar[u]
    &&
    \ast
    \ar[u]
    \ar[d, ->>]
    \\
    S^{n+2}/G
    \ar[rr, "c"{below}]
    &&
    \mathbf{B}\Gamma
    %
    \ar[
      from=s,
      to=t,
      Rightarrow,
      "\sim"{sloped, below}
    ]
\end{tikzcd}
With every $\Gamma$-principal bundle trivialized over the covering by $S^{n+2}$ this way, morphisms between principal bundles correspond to Cech [[coboundaries]] between these Cech cocycles, which are canonically identified with continuous [[natural transformations]] between these functors $(c_1 \rightrightarrows \ast)$.
\end{proof}

\begin{definition}
\label{ShapesOfMappingStacks}
**($\infty$-groupoids of concordances of principal bundles on spherical space forms)**
\linebreak
Consider the following two [[infinity-groupoid|$\infty$-groupoids]]:

The [[shape modality|cohesive shape]] of the [[mapping stack]] from $\mathbf{B}G$ to $\mathbf{B}\Gamma$

\[
  \label{ShapeOfMappingStackFromBGToBGamma}
  \begin{aligned}
  &
  \esh
  \,
  Map
  \Big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \Big)
  \\
  &
  \;\simeq\;
  \esh
  \,
  Map
  \Big(
    \big(
      G \rightrightarrows \ast
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \\
  &
  \;\simeq\;
  \underset{\longrightarrow}{\lim}
  N
  TopFunc
  \Big(
    \big(
      G \rightrightarrows \ast
    \big) \times \Delta^{\bullet}
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)  
  \;\simeq\;
  \end{aligned}
  \!\!\!\!\!\!\!\!\!
  \left(
    \array{
      \vdots
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          G \rightrightarrows \ast
        \big)
        \times \Delta^2
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_2
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          G \rightrightarrows \ast
        \big)
        \times \Delta^1
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_1
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          G \rightrightarrows \ast
        \big)
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_0
    }
  \right)
\]

and the [[shape modality|cohesive shape]] of the [[mapping stack]] from the [[spherical space form]] $S^{n+2}/G$ to $\mathbf{B}\Gamma$

\[
  \label{ShapeOfMappingStackFromSphericalSpaceFormToBGamma}
  \begin{aligned}
  &
  \esh
  \,
  Map
  \Big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \Big)
  \\
  & \;\simeq\;
  \esh
  \,
  Map
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \\
  &
  \;\simeq\;
  \underset{\longrightarrow}{\lim}
  N
  TopFunc
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big) \times \Delta^{\bullet}
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)  
  \;\simeq\;
  \end{aligned}
  \!\!\!\!\!\!\!\!\!
  \left(
    \array{
      \vdots
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          S^{n+2} \times G \rightrightarrows S^{n+2}
        \big)
        \times \Delta^2
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_2
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          S^{n+2} \times G \rightrightarrows S^{n+2}
        \big)
        \times \Delta^1
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_1
      \\
      \big\downarrow
      \big\uparrow
      \big\downarrow
      \\
      TopFunc
      \Big(
        \big(
          S^{n+2} \times G \rightrightarrows S^{n+2}
        \big)
        ,\,
        \big(
          \Gamma \rightrightarrows \ast
        \big)
      \Big)_0
    }
  \right)
\]

In both cases we are showing on the right the canonical [[simplicial sets]] which present these $\infty$-groupoids, obtained by using

1. the expression of [[shape via cohesive path ∞-groupoid|snooth shape via the smooth path $\infty$-groupoid]] (by [this Prop.](shape+via+cohesive+path+∞-groupoid#SmoothShapeModelityGivenBySmoothPathInfinityGroupoid)),

1. the canonical [[Cech groupoid]]-presentation of groupoids of principal bundles, from Lem. \ref{CanonicalCechGroupoidOfGammaPrincipalBundlesOnSphericalSpaceForm},

1. the fact that the [[simplex category|simplicial]] [[homotopy colimit]] of $\infty$-groupoids presented by [[simplicial sets]] is given by the [[diagonal of a bisimplicial set|diagonal]] of the corresponding [[bisimplicial set]] (by [this Prop.](bisimplicial+set#DiagonalAsSimplicialHomotopyColimit)).

\end{definition}


#### The classification theorem
 {#TheClassificationTheorem}

\begin{proposition}
\label{ConcordancesOnSphericalSpaceFormIsMapsOfClassifyingSpaces}
  Under Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms}, 
  the $\infty$-groupoid of [[concordances]] of $\Gamma$-principal bundles on $S^{n+2}/G$ is [[equivalence of infinity-groupoids|equivalent]] to the [[hom infinity-groupoid|hom $\infty$-groupoid]] from $B G$ to $B \Gamma$:
$$
  \esh
  \,
  Maps
  \big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \big)
  \;\;  
  \simeq
  \;\;
  Maps
  \big( 
     B G
     ,\,
     B \Gamma
  \big)
  \,.
$$
\end{proposition}
\begin{proof}
  Since $S^{n+2}/G$ is a [[smooth manifold]], the [[smooth Oka principle]] ([here](shape+via+cohesive+path+∞-groupoid#ConsequenceSmoothOkaPrinciple)) gives that 
$$
  \begin{aligned}
  \esh
  \,
  Maps
  \big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \big)
  &
  \;\simeq\;
  Maps
  \big(
    \esh
    \,
    S^{n+2}/G
    ,\,
    \esh
    \,
    \mathbf{B}\Gamma
  \big)
  &
  \;=\;
  Maps
  \big(
    Shp
    (
      S^{n+2}/G
    )
    ,\,
    B \Gamma
  \big)
  \,.
  \end{aligned}
$$
From here, the claim follows by the following sequence of [[natural equivalences]] [[equivalence in an (infinity,1)-category|in]] [[Infinity-Grpd|$Grpd_\infty$]]:

\[
  \label{MapsIntoTruncatedBGammaSeeSphericalSpaceFormAsClassifyinSpace}
  \begin{array}{lll}
    Maps
    \big(
      Shp(S^{n+2}/G)
      ,\,
      B \Gamma
    \big)
    & 
    \;\simeq\;
    Maps
    \big(
      Shp(S^{n+2} \sslash G)
      ,\,
      B \Gamma
    \big)
    \\
    &
    \;\simeq\;
    Maps
    \big(
      Shp(S^{n+2}) \sslash G
      ,\,
      B \Gamma
    \big)
    \\
    &
    \;\simeq\;
    Maps
    \big(
      \underset{\longrightarrow}{\lim}
      \,
      Shp(S^{n+2}) \times G^{\times_\bullet}
      ,\,
      B \Gamma
    \big)
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    Maps
    \big(
      Shp(S^{n+2}) \times G^{\times_\bullet}
      ,\,
      B \Gamma
    \big)
    \\
    & \;\simeq\;
    \underset{\longleftarrow}{\lim}
    \,
    Maps
    \big(
      G^{\times_\bullet}
      ,\,
      B \Gamma
    \big)
    &
    \text{ by (eq:GammaIsNTruncated) }
    \\
    & \;\simeq\;
    Maps
    \big(
      \underset{\longrightarrow}{\lim}
      \,
      G^{\times_\bullet}
      ,\,
      B \Gamma
    \big)
    \\
    & \;\simeq\;
    Maps
    \big(
      B G
      ,\,
      B \Gamma
    \big)
  \end{array}
\]
\end{proof}

Moreover:

\begin{definition}
\label{ComparisonMorphismBetweenShapesOfMappingStacks}
There is a canonical comparison morphism between the shapes of mapping stacks in Def. \ref{ShapesOfMappingStacks},
given by [[precomposition]] with the [[terminal object|terminal morphism]] $S^{n+2} \xrightarrow{\; p\;} \ast$:

\[
  \label{ComparisonMorphismBetweenShapesOfMappingStacks}
  \esh
  \,
  Map
  \Big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \Big)
  \xrightarrow
  {\;\;\;
     \esh \, Map(p/\!\!/G,\,\mathbf{B}\Gamma)
  \;\;\;}
  \esh
  \,
  Map
  \Big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \Big)  
  \,
  \,.
\]
\end{definition}

\begin{theorem}
\label{ComparisonMapOfConcordanceInfinityGroupoidsIsEquivalence}
  Under Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms}, the comparison morphism (eq:ComparisonMorphismBetweenShapesOfMappingStacks) is an [[equivalence of infinity-groupoids|equivalence of $\infty$-groupoids]].
\end{theorem}
\begin{proof}
  The claim means that the comparison morphism is a [[weak homotopy equivalence]], hence that it induces [[isomorphisms]] on all [[homotopy groups]] $\pi_n$. For $\pi_0$ this is Prop. \ref{ComparisonMorphismBijectiveOnConnectedComponents} below, while for $\pi_1$ this is Prop. \ref{ComparisonMorphismIsoOnFundamentalGroups} below, whose proof has an evident generalization to all $n$.
\end{proof}

\begin{corollary}
 \label{SmoothOkaForMapsOutOfBGIntoBGammaIfGammaIsBraidedTruncated}
  Under Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms}, there is an [[equivalence of infinity-groupoids|equivalence of $\infty$-groupoids]] of the form:
\[
  \label{TheResultingSmoothOkaLikeEquivalence}
  \esh
  \,
  Map
  \big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \big)
  \;\;
  \simeq
  \;\;
  Map
  \big(
    B G
    ,\,
    B \Gamma
  \big)
\]
\end{corollary}
\begin{proof}
 This is the composite of 
Prop. \ref{ConcordancesOnSphericalSpaceFormIsMapsOfClassifyingSpaces}
with 
Thm. \ref{ComparisonMapOfConcordanceInfinityGroupoidsIsEquivalence}.
\end{proof}
\begin{remark}
Cor. \ref{SmoothOkaForMapsOutOfBGIntoBGammaIfGammaIsBraidedTruncated} is of the form of the [[smooth Oka principle]] but for [[domain]] not a [[smooth manifold]] but the [[delooping groupoid]] of the [[finite group]] $G$. 

In contrast to the case where the domain is a smooth manifold, equivalences of the form (eq:TheResultingSmoothOkaLikeEquivalence) fail in general, unless some extra condition like Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms} is imposed. 

For example, in the case that both $G$ and $\Gamma$ are [[compact Lie groups]], the $\infty$-groupoids on the left of (eq:TheResultingSmoothOkaLikeEquivalence) are the [[hom infinity-groupoid|hom $\infty$-groupoids]] of the [[global orbit category]] for compact Lie [[equivariance groups]]. 
\end{remark}

\begin{example}
\label{EquivariantClassifyingSpaceOfPUHBundles}
**(equivariant classifying space of $PU(\mathcal{H})$-bundles)**
\linebreak
In the case that 

* the [[structure group]] is $\Gamma = $ [[PU(ℋ)]] 

* the [[equivariance group]] $G$ is a [[finite group]] which has any [[free action]] on any [[n-sphere]] for $n \geq 4$

Cor. \ref{SmoothOkaForMapsOutOfBGIntoBGammaIfGammaIsBraidedTruncated} immediately implies that the [[homotopy groups]]

$$
  \pi_k
  \Big(
    Map
    \big(
      \mathbf{B}G 
      ,\,
      \mathbf{B}PU(\mathcal{H})
    \big)
  \Big)
  \;\;
  \simeq
  \;\;
  \pi_k
  \Big(
    Map
    \big(
      B G
      ,\,
      B^3 \mathbb{Z}
    \big)
  \Big)
  \;\;
  =
  \;\;
  H^{3-k}_{Grp}
  (
    G
    ;\,
    \mathbb{Z}
  )
$$

are given by the [[group cohomology]] of $G$ with [[coefficients]] in the [[integers]], as shown.

This recovers the statement of [Uribe & al. 2014, Thm. 1.10](twisted+equivariant+K-theory#BEJU14), see also [Uribe & Lück 2014, Thm. 15.17](twisted+equivariant+K-theory#UribeLueck14).
\end{example}

\linebreak

#### Lemmas and proofs
 {#LemmasAndProofs}


\begin{example}
\label{OneMorphismInShapeOfMappingStackFromSphericalSpaceFormToBGamma}
  A [[1-morphism]] in (eq:ShapeOfMappingStackFromSphericalSpaceFormToBGamma)
from a bundle $P_0\vert_0$ to a bundle $P_1\vert_1$ over $S^{n+2}/G$ is a diagram of [[homomorphisms]] of [[principal bundles]] of this form:

\begin{tikzcd}
    P_0\vert_0
    \ar[r]
    \ar[d]
    \ar[dr, phantom, "\mbox{\tiny (pb)}"]
    &
    P_0
    \ar[d, "p_0"]
    \ar[r, "\phi"{above}, "\sim"{below}] 
    &
    P_1
    \ar[d, "p_1"]
    \ar[dr, phantom, "\mbox{\tiny (pb)}"]
    &
    P_1\vert_1
    \ar[d]
    \ar[l]
    \\
    S^{n+2}/G \times \{0\}
    \ar[r, hook]
    &
    S^{n+2}/G \times [0,1]
    \ar[r,-,shift left=1pt]
    \ar[r,-,shift right=1pt]
    &
    S^{n+2}/G \times [0,1]
    &
    S^{n+2}/G \times \{1\}
    \ar[l, hook']
\end{tikzcd}
\end{example}

\begin{lemma}
\label{ThePresentationsForShapesOfMappingStacksAreKanComplexes}
  The simplicial set presentations for shapes of mapping stacks in Def. \ref{ShapesOfMappingStacks} have at least all 2-[[horn]] fillers.
\end{lemma}
\begin{proof}
It is useful to denote a 1-morphism
$$
  \big(
    c(-)
    \xrightarrow{\; \gamma(-) \;} 
    c'(-)
  \big)
  \;\;\;
  \in
  \;
  TopFunc
  \Big(
    (S^{n+2} \times G \rightrightarrows S^{n+2})
    \times [0,1]
    ,\,
    (\Gamma \rightrightarrows \ast)
  \Big)
  \,,
$$
namely a $[0,1]$-parameterized Cech coboundary
$$
  \gamma(-)
    \colon 
  [0,1] 
    \xrightarrow{\;}  
  Maps
  \big(
    S^{n+2}
    ,\, 
    \Gamma
  \big)
  \;\;\;
  \text{s.t.}
  \;\;\;
  \underset{ (t,x) \in [0,1] \times S^{n+2}}{\forall}
  \left(
  \begin{aligned}
    c'(t)(x,\, g ) 
    &
      \;=\; 
    c(t)(x,g)^{\gamma(t)(x)}
    \\
    &
    \,\coloneqq\,
    (\gamma(t)(x))^{-1} 
      \cdot 
    c(t)(x, g) 
     \cdot 
    \gamma(t)(x)
  \end{aligned}
  \right)
  \,.
$$
as follows:

\begin{tikzcd}[row sep={between origins, 60pt}, column sep={between origins, 60pt}]
    c(0)
    \ar[rr, "{\gamma(0)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(0)^{\gamma(0)}
    \ar[d,-, dotted]
    \\
    c(t)
    \ar[rr, "{\gamma(t)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(t)^{\gamma(t)}    
    \ar[d,-, dotted]
    \\
    c(1)
    \ar[rr, "{\gamma(1)}"{description, pos=.6}]
    &{}&
    c(1)^{\gamma(1)}
\end{tikzcd}

Then a pair of composable 1-morphisms, hence a $\Lambda^2_1$-[[horn]], looks like this:

\begin{tikzcd}[row sep={between origins, 60pt}, column sep={between origins, 60pt}]
    c(0)
    \ar[rr, "{\gamma(0)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(0)^{\gamma(0)}
    \ar[d,-, dotted]
    \\
    c(t)
    \ar[rr, "{\gamma(t)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(t)^{\gamma(t)}
    \ar[d,-, dotted]
    \\
    c(1)
    \ar[rr, "{\gamma(1)}"{description, pos=.6}]
    &{}&
    c(1)^{\gamma(1)}
    \ar[r, -, shift left=1pt]
    \ar[r, -, shift right=1pt]
    &[-20pt]
    c'(0)
    \ar[rr, "{\gamma'(0)}"{description, pos=.6}]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(0)^{\gamma'(0)}
    \ar[d, -, dotted]
    \\
    &&&
    c'(t')
    \ar[rr, "{\gamma'(t')}"{description, pos=.6}]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(t')^{\gamma'(t')}
    \ar[d, -, dotted]
    \\
    &&&
    c'(1)
    \ar[rr, "{\gamma'(1)}"{description, pos=.6}]
    &
    {}
    &
    c'(1)^{\gamma'(1)}
\end{tikzcd}

For any such we may form the following composable pair of 1-morphisms of cocycles over $S^{n+2}/G \times \big( \underset{\ni t}{[0,1]} \underset{\ast}{\sqcup} \underset{\ni t'}{[0,1]}  \big)$:

\begin{tikzcd}[row sep={between origins, 60pt}, column sep={between origins, 60pt}]
    c(0)
    \ar[rr, "{\gamma(0)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(0)^{\gamma(0)}
    \ar[d,-, dotted]
    \ar[rr, "\gamma'(0)"{description, pos=.6}]
    &
    {}
    \ar[d, -, shift left=1pt]
    \ar[d, -, shift right=1pt]
    &
    c(0)^{ \gamma(0) \mathrlap{\gamma'(0)} }
    \ar[d, -, dotted]
    \\
    c(t)
    \ar[rr, "{\gamma(t)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(t)^{\gamma(t)}
    \ar[d,-, dotted]
    \ar[rr, "\gamma'(0)"{description, pos=.6}]
    &
    {}
    \ar[d, -, shift left=1pt]
    \ar[d, -, shift right=1pt]
    &
    c(t)^{ \gamma(t) \mathrlap{\gamma'(0)} }
    \ar[d, -, dotted]
    \\
    c(1)
    \ar[rr, "{\gamma(1)}"{description, pos=.6}]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, shift left=1pt]
    \ar[d, -, shift right=1pt]
    &
    c'(0)
    \ar[rr, "{\gamma'(0)}"{description, pos=.6}]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(0)^{\gamma'(0)}
    \ar[d, -, dotted]
    \\
    c'(t')^{\gamma(1)^{-1}}
    \ar[
      rr,
      "{\gamma(1)}"{description, pos=.4}
    ]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, shift left=1pt]
    \ar[d, -, shift right=1pt]
    &
    c'(t')
    \ar[rr, "{\gamma'(t')}"{description, pos=.6}]
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(t')^{\gamma'(t')}
    \ar[d, -, dotted]
    \\
    c'(1)^{\gamma(1)^{-1}}
    \ar[
      rr,
      "{\gamma(1)}"{description, pos=.4}
    ]
    &
    {}
    &
    c'(1)
    \ar[rr, "{\gamma'(1)}"{description, pos=.6}]
    &
    {}
    &
    c'(1)^{\gamma'(1)}
\end{tikzcd}

When pulled back along the canonical topological horn filler retraction $\Delta^2 \to \Lambda^2_{1}$ this yields a 2-cell which fills the original 2-horn.

Similarly, a $\Lambda^2_0$-horn is the following type of data:

\begin{tikzcd}[row sep={between origins, 60pt}, column sep={between origins, 60pt}]
    c(0)
    \ar[rr, "{\gamma(0)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(0)^{\gamma(0)}
    \ar[d,-, dotted]
    \\
    c(t)
    \ar[rr, "{\gamma(t)}"{description, pos=.6}]
    \ar[d,-, dotted]
    &
    {}
    \ar[d,-, dotted]
    &
    c(t)^{\gamma(t)}
    \ar[d,-, dotted]
    \\
    c(1)
    \ar[rr, "{\gamma(1)}"{description, pos=.6}]
    &{}&
    c(1)^{\gamma(1)}
    \ar[r, -, shift left=1pt]
    \ar[r, -, shift right=1pt]
    &[-20pt]
    c'(1)^{\gamma'(1)}
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(1)
    \ar[ll, "{\gamma'(0)}"{description, pos=.6}]
    \ar[d, -, dotted]
    \\
    &&&
    c'(t')^{\gamma'(t')}
    \ar[d, -, dotted]
    &
    {}
    \ar[d, -, dotted]
    &
    c'(t')
    \ar[d, -, dotted]
    \ar[ll, "{\gamma'(t')}"{description, pos=.6}]
    \\
    &&&
    c'(0)^{\gamma'(0)}
    &
    {}
    &
    c'(0)
    \ar[ll, "{\gamma'(0)}"{description, pos=.6}]
\end{tikzcd}

and is filled by the evident directly analogous procedure.
\end{proof}


$\,$

\begin{lemma}
\label{ConjugacyClassesOfGroupHomomorphismsSurjectOnPrincipalBundlesOverSphericalSpaceForm}
  Under the truncation assumption (eq:GammaIsNTruncated),
  the canonical [[function]]
  $$
    Hom(G,\Gamma)_{/\sim_{conj}}
    \xrightarrow{\phantom{--}\sim\phantom{--}}
    \Big(
      \Gamma PrnBdl(TopSp)_{S^{n + 2}/G}
    \Big)_{/\sim_{iso}}
  $$
  is an [[isomorphism]].
\end{lemma}
\begin{proof}
The [[homotopy class]] of the [[classifying space|classifying map]] of a [[principal bundle]] is represented by the [[topological realization]] of any of its [[Cech cohomology|Cech cocycles]]. Therefore, Lemma \ref{CanonicalCechGroupoidOfGammaPrincipalBundlesOnSphericalSpaceForm} implies that in the following [[commuting diagram]] the left and the composite function are [[bijections]]:

\begin{tikzcd}[column sep=small]
  \Gamma \mathrm{PrnBdl}(\mathrm{TopSp})_{ S^{n+2}/G }
  \ar[r, "{\sim}"{yshift=-1pt}]
  \ar[
    rr,
    rounded corners,
    to path={
      -- ([yshift=-11pt]\tikztostart.south)
      -- node[below, yshift=1pt]{ \scalebox{.7}{$\sim$} }
         ([yshift=-08pt]\tikztotarget.south)
      -- (\tikztotarget.south)
    }
  ]
  &
  \tau_0
  \,
  \mathrm{TopFunc}
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \ar[
    r,
    "\color{blue}\sim"{above, yshift=-1pt}
  ]
  &
  \tau_0
  \,
  \mathrm{Maps}
  \Big(
    \mathrm{Shp}
    \big(
      S^{n+2} /\!/ G
    \big)
    ,\,
    B \Gamma
  \Big)
\end{tikzcd}

It follows by [[2-out-of-3]] that also the function on the right is a bijection: 
\[
  \label{CocyclesToClassifyingMapsIsBijection}
  \tau_0
  \,
  \mathrm{TopFunc}
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \xrightarrow{\;\; \sim \;\;}
  \tau_0
  \,
  \mathrm{Maps}
  \Big(
    \mathrm{Shp}
    \big(
      S^{n+2} /\!/ G
    \big)
    ,\,
    B \Gamma
  \Big)
\]

Observe that the composite of the [[weak homotopy equivalence|equivalences]] in (eq:MapsIntoTruncatedBGammaSeeSphericalSpaceFormAsClassifyinSpace) is again the morphism induced by pre-composition with 

$$
  S^{n+2} \xrightarrow{\; p \;} \ast
  \;\;\;\;
  \text{or}
  \;\;\;\;
  \ast \xrightarrow{\; i \;} S^{n+2}
  \,.
$$ 

Therefore, by [[functor|functoriality]] of the [[nerve]]-operation followed by [[topological realization of simplicial topological spaces|topological realization]], the following [[commuting diagram|diagram commutes]]:

\begin{tikzcd}[column sep=small]
  {}
  &[60pt]
  \tau_0
  \,
  \mathrm{TopFunc}
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \ar[
    r,
    "\sim"{above}
  ]
  \ar[d, hook, "{ i^\ast }"{left}]
  &
  \tau_0
  \,
  \mathrm{Maps}
  \Big(
    \mathrm{Shp}
    \big(
      S^{n+2} / G
    \big)
    ,\,
    B \Gamma
  \Big)
  \ar[d, , "{ i^\ast }"{left}, "\sim"{sloped, xshift=-6pt, yshift=+4pt}]
  &[150pt]
  {}
  \\
  {}
  &
  \mathllap{
    \mathrm{Hom}(G,\Gamma)_{/\sim_{\mathrm{conj}}}
    \;\simeq\;\;
  }
  \tau_0
  \,
  \mathrm{TopFunc}
  \Big(
    \big(
      G \rightrightarrows \ast
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \ar[d, ->>, "{ p^\ast }"{left}]
  \ar[r, ->>]
  &
  \tau_0
  \,
  \mathrm{Maps}
  \Big(
    \ast /\!/ G
    ,\,
    B \Gamma
  \Big)
  \mathrlap{
    \;\;\simeq\;
    \tau_0
    \,
    \mathrm{Maps}
    \Big(
      B G
      ,\,
      B \Gamma
    \Big)
  }
  \ar[
    d, "{ p^\ast }"{left}, "\sim"{sloped, xshift=-6pt, yshift=+4pt}
  ]
  &
  {}
  \\
  {}
  &
  \tau_0
  \,
  \mathrm{TopFunc}
  \Big(
    \big(
      S^{n+2} \times G \rightrightarrows S^{n+2}
    \big)
    ,\,
    \big(
      \Gamma \rightrightarrows \ast
    \big)
  \Big)
  \ar[
    r,
    "\sim"{above}
  ]
  &
  \tau_0
  \,
  \mathrm{Maps}
  \Big(
    \mathrm{Shp}
    \big(
      S^{n+2} / G
    \big)
    ,\,
    B \Gamma
  \Big)
  \mathrlap{
     \;\;\simeq\;
     \big(
       \Gamma \mathrm{PrnBld}(\mathrm{TopSp})_{S^{n+2}/G}
     \big)_{/\sim_{\mathrm{iso}}}
  }
  &
  {}
\end{tikzcd}

Here

* the top and bottom horizontal functions are bijections by (eq:CocyclesToClassifyingMapsIsBijection),

* the right vertical functions are bijections by (eq:MapsIntoTruncatedBGammaSeeSphericalSpaceFormAsClassifyinSpace).

By commutativity of the total rectangle, 
this implies that the left vertical functions exhibit a [[retraction]], as shown, in particular the bottom left function is [[surjective]]. (Moreover, the commutativity of the two squares separately each implies that the middle horizontal function is also a surjection, as shown.)

But the bottom left function is clearly also [[injective]]: If $\phi \colon S^{n+2} \xrightarrow{\;} \Gamma$ is a Cech coboundary between Cech cocycles that are constant along $S^{n+2}$, then $\phi(\ast)$ conjugates the corresponding [[group homomorphisms]] into each other. 

Therefore the bottom left morphism is both injective as well as surjective, hence bijective.
\end{proof}



More generally, the analogous conclusion evidently still holds for $\Gamma$-principal bundles on the [[topological product space]] $S^{n+2}/G \times \Delta^k$ with the [[topological k-simplex]]

$$
  \tau_0
  \,
  \Gamma PrnBdl(TopSp)_{S^{n+2}/G \times \Delta^k}
  \;\;
   \simeq
  \;\;
  \tau_0
  \,
  TopFunc
  \big(
    S^{n+2} \times G \times \Delta^k
    \rightrightarrows
    S^{n+2} \times \Delta^k
    ,\,
    \Gamma \rightrightarrows \ast
  \big)
  \,.
$$


\begin{lemma}
\label{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaEquivalentlyHaveConstantUnderlyingBundle}
  Every [[1-morphism]] 
  in 
  $\esh \,Maps\big( S^{n+2}/G ,\, \mathbf{B}\Gamma \big)$
  (Exp. \ref{OneMorphismInShapeOfMappingStackFromSphericalSpaceFormToBGamma})
  is equivalent (homotopic relative its endpoints) to 
  one of the form
  \[
  \label{OneMorphismInShapeOfMappingStacksOutOfAConstantBundle}
  \array{
    P \times \Delta^1
    &\xrightarrow{\phantom{--}}&
    P'
    \\
    \big\downarrow
    {}^{\mathrlap{p \times id_{[0,1]}}}
    &&
    \big\downarrow
    {}^{\mathrlap{p'}}
    \\
    S^{n+2}/G \times \Delta^1
    &=&
    S^{n+2}/G \times \Delta^1
  }
  \]
\end{lemma}
\begin{proof}
  By the [[classifying space|classification theory]] of principal bundles (or, more concretely, by the proof of [this Prop.](concordance#ConcordantTopologicalPrincipalBundlesAreIsomorphic)), every principal bundle on a [[cylinder]] like $S^{n+2}/G  \times [0,1]$ is isomorphic to the constant re-extension of its restriction to one end of the cylinder. With the given 1-morphism denoted as in Exp. \ref{OneMorphismInShapeOfMappingStackFromSphericalSpaceFormToBGamma} we write $\ell$ for such an isomorphism onto its $P_0$-component:

\begin{tikzcd}
    &
    P_0
    \ar[dd, "p_0"{description}]
    \\
    P_0\vert_0 \times \Delta^1
    \ar[dd, "p_0\vert_0 \,\times\, \mathrm{id}_{[0,1]}"{description}]
    \ar[ur, "\ell"{above}, "\sim"{below, sloped}]
    &
    \\
    &
    S^{n+2}/G \times \Delta^1
    \\
    S^{n+2}/G \times \Delta^1
    \mathrlap{\,,}
    \ar[ur, -, shift left=1pt]
    \ar[ur, -, shift right=1pt]
\end{tikzcd}

which is such that the restriction of $\ell$ to $\{0\} \subset [0,1]$ is the [[identity morphism]]

\[
  \label{RestrictionOfEllToLeftEndpointIsIdentity}
  \ell\vert_0 \;\colon\; P_0 \xrightarrow{\; id \;} P_0
  \mathrlap{\,.}
\]


From this we may construct the following  [[2-morphism]] in (eq:ShapeOfMappingStackFromSphericalSpaceFormToBGamma):

\[\label{A2MorphismInShapeOfMappingStackWithDegeenrateTwoFace}\]
\begin{tikzcd}[column sep={between origins, 90pt}]
    &
    s_0^\ast
    (
      P_0
    )
    \ar[dd]
    \ar[dr, "s_0^\ast\phi"{above}, "\sim"{sloped, below}]
    &[-6pt]
    \\
    s_0^\ast
    (
      P_0\vert_0 \times \Delta^1
    )
    \ar[ur, "s_0^\ast(\ell)"{above}, "\sim"{below, sloped}]
    \ar[rr, crossing over]
    \ar[dd]
    &
    &
    s_0^\ast
    (
      P_1
    )
    \ar[dd]
    \\
    &
    S^{n+2}/G \times \Delta^2
    \ar[dr, -, shift left=1pt]
    \ar[dr, -, shift right=1pt]
    \\
    S^{n+2}/G \times \Delta^2
    \ar[ur, -, shift left=1pt]
    \ar[ur, -, shift right=1pt]
    \ar[rr, -, shift left=1pt]
    \ar[rr, -, shift right=1pt]
    &&
    S^{n+2}/G \times \Delta^2
\end{tikzcd}

Here $\sigma_1 \,\colon\, \Delta^2 \to \Delta^1$ denotes the map of [[topological simplices]] which collapses the 2-[[face]]:

\begin{tikzcd}
    \Delta^1
    \ar[r, "\delta_2"]
    \ar[
      rr,
      rounded corners,
      to path={
        -- ([yshift=-7pt]\tikztostart.south)
        -- node[below]{\scalebox{.7}{$\mathrm{const}_0$}}
          ([yshift=-7pt]\tikztotarget.south)
        -- (\tikztotarget.south)        
      }
    ]
    &
    \Delta^2 
    \ar[r, "\sigma_1"]
    & 
    \Delta^1
    &[10pt]
    \Delta^1
    \ar[r, "\delta_{0,1}"]
    \ar[
      rr,
      rounded corners,
      to path={
        -- ([yshift=-7pt]\tikztostart.south)
        -- node[below]{\scalebox{.7}{$\mathrm{id}$}}
          ([yshift=-7pt]\tikztotarget.south)
        -- (\tikztotarget.south)        
      }
    ]
    &
    \Delta^2 
    \ar[r, "\sigma_1"]
    & 
    \Delta^1
    \mathrlap{\,.}
\end{tikzcd}

Therefore the 2-[[face]] of the above [[2-morphism]] (eq:A2MorphismInShapeOfMappingStackWithDegeenrateTwoFace) is degenerate (where the last step uses (eq:RestrictionOfEllToLeftEndpointIsIdentity)):

$$
  \begin{aligned}
    \delta_2^\ast
    \big(
      \sigma_1^\ast(\ell)
    \big)
    &
    \;=\;
    const_0^\ast(\ell)
    \\
    &
    \;=\;
    \ell\vert_0 \times id_{\Delta^1}
    \\
    &
    \;=\;
    id_{P_0} \times id_{\Delta^1}
    \;=\;
    id_{ P_0 \times \Delta^1 }
    \mathrlap{\,,}
  \end{aligned}
$$

while the 0-[[face]] is the original morphism $\phi$ 

$$
  \delta_0^\ast
  \big(
    s_0^\ast(\phi)
  \big)
  \;=\;
  \mathrm{id}_{\Delta^1}^\ast(\phi)
  \;=\;
  \phi
  \,,
$$

and the 1-[[face]] is of the claimed form (eq:OneMorphismInShapeOfMappingStacksOutOfAConstantBundle):

$$
  \begin{aligned}
    \delta_1^\ast
    \big(
      s_0^\ast(\phi)
      \circ
      s_0^\ast(\ell)
    \big)
    & 
    \;=\;
    \delta_1^\ast
    \big(
      s_0^\ast( \phi \circ \ell )
    \big)
    \\
    &
    \;=\;
    \phi \circ \ell
    \;\colon\;
    P_0\vert_0 \xrightarrow{\;} P_1
    \mathrlap{\,.}
  \end{aligned}
$$
Hence the 2-morphism (eq:A2MorphismInShapeOfMappingStackWithDegeenrateTwoFace) exhibits the claimed homotopy relative endpoints.
\end{proof}

\begin{lemma}\label{ComparisonMorphismIsInjectiveOnConnectedComponents}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is [[injective]] on [[connected components]].
\end{lemma}
\begin{proof}
Given a 1-morphism
$$
  c(-)
    \xrightarrow{\;\gamma(-)\;}
  c'(-)
$$
such that both $c(0)$ and $c'(1)$ are constant along $S^{n+2}$
$$
  \underset{x \in S^{n+2}}{\forall}
  \big(
    c(0)(x,g) \;=\; c(0)(\ast,g)
    \,,
    \;\;\;\;
    c'(1)(x,g) \;=\; c'(1)(\ast,g)   
  \big)
$$
we need to show that there is a 1-morphism between $c(0)$ and $c'(1)$ all whose components are constant along $S^{n+2}$.

Now by Lemma \ref{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaEquivalentlyHaveConstantUnderlyingBundle} we know that there is a 1-morphism $c(-) \xrightarrow{\gamma(-)} c'(-)$ such that $c$ is constant along $[0,1] \times S^{n+2}$, i.e. such that
$$  
  \underset{
    (t,x) \,\in\, [0,1] \times S^{n+2}
  }{\forall}
  \;\;
  c(t)(x,g) \,=\, c(0)(\ast,g)
  \,.
$$

But the remaining data is then all in $\gamma(-)$. Hence restricting $\gamma$ to $\ast \,\in\, S^{n+2}$ (and then re-extending it as a constant function on this value) yields a 1-morphism of the desired form.
\end{proof}

\begin{lemma}\label{ComparisonMorphismIsSurjectiveOnConnectedComponents}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is [[surjective]] on [[connected components]].
\end{lemma}
\begin{proof}
  We need to show that every cocycle $c(0)$ there exists a cocycle $c'(1)$ which is constant along $S^{n+2}$ and a 1-morphism $c(-) \xrightarrow{\gamma(-)} c'(-)$. But by Lemma \ref{ConjugacyClassesOfGroupHomomorphismsSurjectOnPrincipalBundlesOverSphericalSpaceForm} there is even a Cech coboundary $\gamma(0)$ with $c'(1) = c(0)^{\gamma(0)}$. Hence taking $c(t) \coloneqq c(0)$ and $\gamma(t) \coloneqq \gamma(1)$ gives the required morphism.
\end{proof}

\begin{proposition}\label{ComparisonMorphismBijectiveOnConnectedComponents}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is [[bijective]] on [[connected components]]:
$$
  \pi_0
  \big(
    \esh \, Map(p/\!\!/G,\,\mathbf{B}\Gamma)
  \big)
  \;\;
  \colon
  \;\;
  \pi_0
  \bigg(
  \esh
  \,
  Map
  \Big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \Big)
  \bigg)
  \xrightarrow
  {\;\;\;
     \sim
  \;\;\;}
  \pi_0
  \bigg(
  \esh
  \,
  Map
  \Big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \Big)  
  \bigg)
$$
\end{proposition}
\begin{proof}
  By Lemma \ref{ComparisonMorphismIsInjectiveOnConnectedComponents} it is injective, and by Lemma \ref{ComparisonMorphismIsSurjectiveOnConnectedComponents} it is surjective.
\end{proof}

\begin{lemma}
\label{ComparisonMorphisnInjectiveOnFundamentalGroups}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is [[injective]] on [[fundamental groups]].
\end{lemma}
\begin{proof}
  Since both simplicial sets have all 2-horn fillers, by Lem. \ref{ThePresentationsForShapesOfMappingStacksAreKanComplexes}, it is sufficient to show for $c(-) \xrightarrow{\gamma(-)} c(-)$ a 1-morphism with $c(0) = c(1)$ and all data constant along $S^{n+2}$ that if this is homotopic relative boundary to the identity on $c(0)$ by any 2-cell, then it is so by a 2-cell all whose data is constant along $S^{n+2}$.

Idea: As in Lem. \ref{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaEquivalentlyHaveConstantUnderlyingBundle} we find that the given homotopy is itself equivalent to one whose underlying cocycle is constant along $S^{n+2}$. The remaining data is all in $\gamma(-)$, so that restricting that to $\ast \in S^{n+2}$ (and then re-extending as a constant function) yields the desired homotopy.
\end{proof}

\begin{lemma}\label{DeformationOfCechCoboundaryGivesConcordanceOfCocycles}
  Let $c(-) \xrightarrow{\gamma(-)} c(-)^{\gamma(-)}$ be a 1-morphism such that $c(1)$ is trivial: $\underset{(x,g) \in S^{n+2} \times G}{\forall} \,  c(1)(x,g) = \mathrm{e}$. Then for every continuous function

$$
  \widehat{\gamma} \,\colon\,
  [0,1] \times [0,1] \times S^{n+2} \xrightarrow{\;\;} \Gamma
$$

with 

$$
  \widehat{\gamma}(0) \,=\, \gamma
  \,,
  \;\;\;
  \widehat{\gamma}(s)(1,\ast) \,=\, \gamma(1,\ast)
$$

this 1-morphism is homotopic relative boundary to 

$$
  c(-)
  \xrightarrow{ \widehat{\gamma}(1)(-) }
  c(-)^{ \widehat{\gamma}(1)(-) }
  \,.
$$
\end{lemma}
\begin{proof}
  There is the obvious way to turn $\widehat \gamma$ into 
a 2-morphism of the shape of the simplicial square whose two vertical 1-faces are degenerate (the right one by the assumption that $c(1)$ is trivial, so that $c(1)^{\gamma} \,=\, c(1)$):

\begin{tikzcd}[row sep={between origins, 30pt}, column sep={between origins, 40pt}]
    &&
    c(0)
    \ar[rrrrrrrr, "{\gamma(0)}"{description, pos=.5}]
    \ar[dddd,-, dashed]
    &&&&
    \phantom{AA}
    \ar[dddd,-, dotted, crossing over]
    &&&&
    c(0)^{\gamma(0)}
    \ar[dddd,-, dotted]
    \\
    &
    c(0)
    \ar[ur,-,dashed]
    \ar[dddd,-,dotted]
    \ar[rrrrrrrr, crossing over, "{\widehat{\gamma}(t')(0)}"{description}]
    &&&&
    \phantom{AA}
    \ar[ur,-,dotted]
    \ar[ddd,-,dotted, crossing over]
    &&&&
    c(0)^{\widehat{\gamma}(t')(0)}
    \ar[ur,-,dotted]
    \\
    c(0)
    \ar[ur,-,dashed]
    \ar[rrrrrrrr, crossing over, "{ \widehat{\gamma}(1)(0)}"{description}]
    \ar[dddr, -, dashed]
    &&&&
    \phantom{AA}
    \ar[ur,-,dotted]
    &&&&
    c(0)^{\widehat{\gamma}(1)(0)}
    \ar[ur, -, dotted]
    \\
    &&&&&
    {}
    \\
    &&
    c(t)
    \ar[rrrrrrrr, "{\gamma(t)}"{description, pos=.5}]
    \ar[dddd,-, dashed]
    &&&{}&
    \phantom{AA}
    \ar[dddd,-, dotted]
    &{}&&&
    c(t)^{\gamma(t)}
    \ar[dddd,-, dotted]
    \\
    &
    c(t)
    \ar[ur,-,dotted]
    \ar[dddd,-,dotted]
    \ar[rrrrrrrr, crossing over, "{ \widehat{\gamma}(t')(t) }"{description}]
    \ar[dddr, -, dashed]
    &&&&
    \phantom{AA}
    \ar[ur,-,dotted]
    \ar[uu, -, dotted, crossing over]
    \ar[ddd, -, dotted]
    &&&&
    c(t)^{ \widehat{\gamma}(t')(t) }
    \ar[ur,-,dotted]
    \ar[uuuu,-,dotted, crossing over]
    \\
    c(t)
    \ar[ur, -, dotted]
    \ar[uuuu, -, dashed]
    \ar[rrrrrrrr, crossing over, "\widehat{\gamma}(1)(t)"{description}]
    &&&& 
    \phantom{AA}
    \ar[ur, -, dotted]
    \ar[uuuu, -, dotted, crossing over]
    &&&&
    c(t)^{\widehat{\gamma}(1)(t)}
    \ar[ur, -, dotted]
    \ar[uuuu, -, dotted, crossing over]
    \\
    &
    &&&&
    {}
    \\
    &&
    c(1)
    \ar[rrrrrrrr, "{\gamma(1)}"{description, pos=.5}]
    &&&
    {}
    &
    {}
    &&&&
    c(1)^{\gamma(1)}
    \\
    &
    c(1)
    \ar[ur,-,dashed]
    \ar[rrrrrrrr, "{ \widehat{\gamma}(t')(1) }"{description}]
    &&&&
    \phantom{AA}
    \ar[ur,-,dotted]
    \ar[uu,-,crossing over, dotted]
    &&&&
    c(1)^{\widehat{\gamma}(t')(1)}
    \ar[ur,-,dotted]
    \ar[uuuu,-,crossing over, dotted]
    \\
    c(1)
    \ar[ur,-,dashed]
    \ar[uuuu,-,dashed]
    \ar[rrrrrrrr, "{ \widehat{\gamma}(1)(1) }"{description}]
    &&&&
    \phantom{AA}
    \ar[ur, -, dotted]    
    \ar[uuuu, -, dotted, crossing over]
    &&&&
    c(1)^{\widehat{\gamma}(1)(1)}
    \ar[ur, -, dotted]
    \ar[uuuu, -, dotted, crossing over]
\end{tikzcd}


\end{proof}

\begin{lemma}
\label{ComparisonMorphismSurjectiveOnFundamentalGroups}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is [[surjective]] on [[fundamental groups]].
\end{lemma}
\begin{proof}
  Since both simplicial sets have all 2-horn fillers, by Lem. \ref{ThePresentationsForShapesOfMappingStacksAreKanComplexes}, it is sufficient to show for $c(-) \xrightarrow{\gamma(-)} c(-)$ any 1-morphism with $c(0) = c(1)$ that it is homotopic relative boundary to one all whose data is constant along $S^{n+2}$, and by Lem. \ref{ComparisonMorphismIsSurjectiveOnConnectedComponents} it is sufficient to assume that the cocycle $c(0)$ is already constant along $S^{n+2}$.

Hence considering this case, Prop. \ref{OneMorphismsInShapeOfMapsFromSphericalFormToBGammaEquivalentlyHaveConstantUnderlyingBundle} give a homotopy relative boundary to a 1-morphism whose underlying cocycle $c(-)$ is constant along $S^{n+2}$. The remaining data is

$$
  \gamma(-)
  \;\colon\;
  [0,1] \times S^{n+2} \xrightarrow \Gamma
  \,.
$$

or equivalently

$$
  \tilde{\gamma}(-)
  \;\colon\;
  S^{n+2} \xrightarrow Maps\big([0,1],  \Gamma\big)
  \,.
$$

We need to show that any such map is pointed-homotopic to the map constant on the basepoint $t \mapsto \gamma(t)(\ast)$. By Lemma \ref{DeformationOfCechCoboundaryGivesConcordanceOfCocycles} this is the case if

$$
  \pi_{n+2} 
  \Big(
     Maps\big([0,1],  \Gamma\big)
  \Big)
  \;\simeq\;
  \pi_{n+2} 
  (
     \Gamma
  )
  \;\overset{!}{=}\;
  \ast
$$

and this holds by the truncation assumption (eq:GammaIsNTruncated).
\end{proof}

\begin{remark}
\label{ConcordancesOfHigherGerbesOnSphericalSpaceFormHaveGroupStructure}
  With (eq:DeloopingOfShapeIsInfinityGroup) in Assumption \ref{AssumptionForHigherGerbesOnSphericalSpaceForms}, Prop. \ref{ConcordancesOnSphericalSpaceFormIsMapsOfClassifyingSpaces} implies that the space of concordances has [[infinity-group|$\infty$-group]] structure:
$$
  \esh
  \,
  Maps
  \big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \big)
  \;\;\;
  \in
  \;
  Grp(Grpd_\infty) 
  \,.
$$
\end{remark}


\begin{proposition}
\label{ComparisonMorphismIsoOnFundamentalGroups}
The comparison morphism (Def. \ref{ComparisonMorphismBetweenShapesOfMappingStacks}) is an [[isomorphism]] on [[fundamental groups]] (for any basepoint):
$$
  \pi_1
  \big(
    \esh \, Map(p/\!\!/G,\,\mathbf{B}\Gamma)
  \big)
  \;\;
  \colon
  \;\;
  \pi_1
  \bigg(
  \esh
  \,
  Map
  \Big(
    \mathbf{B}G
    ,\,
    \mathbf{B}\Gamma
  \Big)
  \bigg)
  \xrightarrow
  {\;\;\;
     \sim
  \;\;\;}
  \pi_1
  \bigg(
  \esh
  \,
  Map
  \Big(
    S^{n+2}/G
    ,\,
    \mathbf{B}\Gamma
  \Big)  
  \bigg)
$$
\end{proposition}
\begin{proof}
  By Lemma \ref{ComparisonMorphisnInjectiveOnFundamentalGroups} this function is [[injective]] on fundamental groups.

In order to see surjectivity, we may use that the $\infty$-groupoid of concordances has 
[[infinity-group|group structure]] (Rem. \ref{ConcordancesOfHigherGerbesOnSphericalSpaceFormHaveGroupStructure}), which implies that all its [[connected components]] have isomorphic [[homotopy groups]]. Therefore it is sufficient to consider the connected component of the trivial cocycle $c$. Here, Lemma \ref{ComparisonMorphismSurjectiveOnFundamentalGroups} gives the surjectivity.
\end{proof}


(...)


## Literature

Historical articles:

* {#Killing1891} [[Wilhelm Killing]], _Ueber die Clifford-Klein’schen Raumformen_, Math. Ann. 39 (1891), 257–278 ([doi:10.1007/BF01206655](https://doi.org/10.1007/BF01206655))

Solution of the classification problem:

* {#Wolf74} [[Joseph Wolf]], _Spaces of constant curvature_, Publish or Perish, Boston, Third ed., 1974

Review:

* Ian Hambleton, _Topological spherical space forms_, Handbook of Group Actions (Vol. II), ALM 32 (2014), 151-172. International Press, Beijing-Boston ([arXiv:1412.8187](https://arxiv.org/abs/1412.8187))

* {#Allock15} Daniel Allcock, _Spherical space forms revisited_ ([arXiv:1509.00906](https://arxiv.org/abs/1509.00906))


Discussion for the [[7-sphere]] with application to [[near horizon geometries]] of [[M2-brane]] ([[AdS/CFT duality|AdS/CFT dual]] to the [[ABJM model]]):

* {#MFFGME09} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], [[Sunil Gadhia]], [[Elena Méndez-Escobar]], _Half-BPS quotients in M-theory: ADE with a twist_, JHEP 0910:038,2009 ([arXiv:0909.0163](http://arxiv.org/abs/0909.0163), [pdf slides](http://www.maths.ed.ac.uk/~jmf/CV/Seminars/YRM2010.pdf))

* {#Gadhia07} [[Sunil Gadhia]], _Supersymmetric quotients of M-theory and supergravity backgrounds_, PhD thesis, School of Mathematics, University of Edinburgh, 2007 ([spire:1393845](http://inspirehep.net/record/1393845/))





[[!redirects spherical space forms]]