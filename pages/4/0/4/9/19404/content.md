
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

We discuss the [[concordance]] [[infinity-groupoid|$\infty$-groupoid]] of $\Gamma$-[[principal bundles]] on [[spherical space forms]] $S^{n+2}/G$ in that case that the [[topological group]] $\Gamma$ is a [[homotopy n-type]].

In more detail:

Let $\Gamma \,\in\, Grp(TopSp)$ be a [[topological group]] whose [[underlying]] [[homotopy type]] is a [[homotopy n-type]], hence [[n-truncated object of an (infinity,1)-category|n-truncated]] for some $n \in \mathbb{N}$:

\[
  \label{GammaIsNTruncated}
  \tau_n Shp(\Gamma) \,\simeq\, Shp(\Gamma)
  \;\;\;
  \in
  \;
  Grp_\infty
  \,.
\]

(For example, $\Gamma = $ [[U(1)]] for any $n \geq 1$, or $\Gamma \,=\,$ [[PU(ℋ)]] for any $n \geq 2$.)

Moreover, let  $S^{n+2}/G$ be a [[spherical space form]] of [[dimension of a manifold|dimension]] $n+2$, hence the [[topological quotient space|quotient space]] of the [[n-sphere|$(n+2)$-sphere]] $S^{n+2}$ 
by a [[free action]] of a [[finite group]]
$G \,\in\, Grp(FinSet) \xhookrightarrow{\;} Grp(TopSp)$. We write

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


We will write:

$$
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
  }
$$

for 

1. the [[delooping groupoid]] of $\Gamma$, regarded as a [[topological groupoid]] $\Gamma \rightrightarrows \ast$, 

1. its associated [[D-topological space|D-]][[topological stack]] $\mathbf{B}\Gamma$ regarded as an object in [[smooth infinity-groupoid|$SmthGrpd_\infty$]].


\begin{definition}
\label{ShapesOfMappingStacks}
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

In both cases we are showing on the right the canonical [[simplicial sets]] which present these $\infty$-groupoids, obtained by 

1. using the expression of [[shape via cohesive path ∞-groupoid|snooth shape via the smooth path $\infty$-groupoid]] (by [this Prop.](shape+via+cohesive+path+∞-groupoid#SmoothShapeModelityGivenBySmoothPathInfinityGroupoid)),

1. the fact that the [[simplex category|simplicial]] [[homotopy colimit]] of $\infty$-groupoids presented by [[simplicial sets]] is given by the [[diagonal of a bisimplicial set|diagonal]] of the corresponding [[bisimplicial set]] (by [this Prop.](bisimplicial+set#DiagonalAsSimplicialHomotopyColimit)).

\end{definition}

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

We now discuss what this morphism does on [[homotopy groups]].. 

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
The $n$-truncation condition (eq:GammaIsNTruncated) on $\Gamma$ implies that its [[classifying space]] $B \Gamma \,\simeq\, Shp( \left\vert \Gamma \rightrightarrows \ast \right\vert  )$ is an $(n+1)$-type

$$
  \tau_{n+1} Shp(\Gamma) \,\simeq\, Shp(\Gamma)
  \;\;\;
  \in
  \;
  Grp_\infty
$$

and hence that every $\Gamma$-principal bundle on $S^{n+2}$ is [[isomorphism|isomorphic]] to the [[trivial bundle]]:

\[
  \label{UniqueGerbesOnNSphere}
  \tau_0 \Gamma PrnBdl(TopSp)_{S^{n+2}}
  \;\;
  \simeq
  \;\;
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

Therefore, every $\Gamma$-[[principal bundle]] on the spherical space form $S^n/G$ trivializes when [[pullback bundle|pulled back]] along the coprojection $q$ (eq:CoprojectionInDiscussionOfGerbesOnSphericalSpaceForms). The corresponding [[Cech cohomology|Cech cocycle]] is a [[topological functor]]

$$
  \big(
    S^{n+2} \times G \rightrightarrows S^{n+2}
  \big)
  \xrightarrow{\;\; 
    c_1 \rightrightarrows \ast 
  \;\;}
  \big(
    \Gamma \rightrightarrows \ast
  \big)
$$

out of the [[action groupoid]] $S^{n+2} \times G \rightrightarrows X$ of $G$ acting on $S^n$ into the [[delooping groupoid]] $\Gamma \rightrightarrows \ast$:

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

Hence the operation of assigning [[Cech cohomology|Cech cocycles]] relative to the [[covering space]] by $S^{n+2}$ is an  
[[equivalence of groupoids]] between the [[groupoid]] of $\Gamma$-principal bundles on $S^{n+2}/G$ and that of [[topological functors]] and [[continuous map|continuous]] [[natural transformations]] between the [[action groupoid]] and the [[delooping groupoid]]. But the [[homotopy class]] of the [[classifying space|classifying map]] of a principal bundle is represented by the [[topological realization]] of any of its [[Cech cohomology|Cech cocycles]], so that in the following [[commuting diagram]] the left and the composite function are [[bijections]]:

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

Moreover, notice the following sequence of [[natural equivalences]] [[equivalence in an (infinity,1)-category|in]] [[Infinity-Grpd|$Grpd_\infty$]]:

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

The composite of these [[weak homotopy equivalence|equivalences]] (eq:MapsIntoTruncatedBGammaSeeSphericalSpaceFormAsClassifyinSpace) is again the morphism induced by pre-composition with 

$$
  S^{n+2} \xrightarrow{\; p \;} \ast
  \;\;\;\;
  \text{or}
  \;\;\;\;
  \ast \xrightarrow{\; i \;} S^{n+2}
  \,.
$$ 

Now, by [[functor|functoriality]] of the [[nerve]]-operation followed by [[topological realization of simplicial topological spaces|topological realization]], the following [[commuting diagram|diagram commutes]]:

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