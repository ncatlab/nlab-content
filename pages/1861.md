
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

### General

_Cohomotopy cohomology theory_ $\pi^\bullet$ is the ([[non-abelian cohomology|non-abelian]]) [[generalized cohomology theory]] whose [[cocycle spaces]] are [[spaces of maps]] into an [[n-sphere]], hence whose [[cohomology classes]] are [[homotopy classes]] of [[maps]] into an [[n-sphere]]: 

$$
  \pi^n(X) \;\coloneqq\; Maps\big( X, S^n\big)/_{\sim_{homotopy}}
$$

So, dually to how [[homotopy groups]] 

$$
  \pi_n(X)\coloneqq Maps\big( S^n, X\big)/_{\sim_{homotopy}}
$$

are [[groups]] of [[homotopy classes]] of maps _out_ of [[spheres]], Cohomotopy sets are sets of homotopy classes of maps _into_ spheres, whence the [[duality|dual]] name.

If instead one considers only the [[stable homotopy theory|stable]] aspect of Cohomotopy sets, by mapping into the [[stabilization]] of the spheres, hence into (some [[suspension spectrum|suspension]] of) the [[sphere spectrum]], then one speaks of _[[stable Cohomotopy]]_, written

$$
  \mathbb{S}^n(X) 
    \;\coloneqq\; 
  Maps
  \big(
    \Sigma^\infty X , \Sigma^{\infty} S^n
  \big)/_{\sim_{homotopy}}
  \,.
$$

In other words, the [[generalized (Eilenberg-Steenrod) cohomology]] theory which is [[Brown representability theorem|represented]] by the [[sphere spectrum]] is _[[stable Cohomotopy]]_.

+-- {: .num_remark #RemarkOnTerminology}
###### Remark
**(terminology)**

Therefore "Cohomotopy theory" is really shorthand for "Cohomotopy cohomology theory" and as such is [[duality|dual]] to _homotopy homology theory_, which in the stable case is known as _[[stable homotopy homology theory]]_.

In particular, cohomotopy theory is a [[concrete particular]] and not dual to the [[abstract general]] of [[homotopy theory]]; and is hence also not on par with the [[abstract general]] of [[cohomology theory]]. Rather, Cohomotopy theory is one _instance_ of a [[generalized cohomology|cohomology theory]], and as such is a sibling of [[ordinary cohomology theory]] ([[HR]]-theory)), [[K-theory]], etc.

To emphasize this, one might, in the [[stable cohomotopy theory|stable case]], say _$\mathbb{S}$-theory_ instead of "stable Cohomotopy theory"; where $\mathbb{S}$ denotes the [[sphere spectrum]]. In the unstable case there is no widely adopted notation, but one might consider saying "$\mathbf{\pi}$-theory" (with $\pi$ the established symbol for (co)[[homotopy groups]]) or _$S$-theory_ (with "$S$" for [[n-spheres]] $S^n$) for unstable Cohomotopy theory.

In any case, to highlight that Cohomotopy theory is a [[concrete particular]] and not an [[abstract general]], it makes good sense to capitalize the term and speak of _Cohomotopy cohomology theory_ or just _Cohomotopy theory_, for short.

The following table indicates the pattern:

| [[generalized cohomology theory]] |  [[generalized homology theory]] | [[classifying space]] | [[Brown representability theorem|representing]] [[spectrum]] |
|--|--|--|--|
| [[Cohomotopy theory]] <br/> ([[non-abelian cohomology|non-abelian]]) |  | [[n-sphere]] <br/> $S^n$ |  |
| [[stable Cohomotopy theory]] <br/> ([[generalized (Eilenberg-Steenrod) cohomology theory|abelian]]) | [[stable homotopy homology theory]] | [[sphere spectrum]] <br/> $\mathbb{S}$  | $\,$ | [[sphere spectrum]] <br/> $\mathbb{S}$ |
| [[ordinary cohomology]]: <br/> [[HR]]-[[generalized (Eilenberg-Steenrod) cohomology theory|cohomology theory]] |  [[ordinary homology]]: [[HR]]-[[generalized homology theory|homology theory]] | [[Eilenberg-MacLane space]] $K(R,n)$  |  [[Eilenberg-MacLane spectrum]] <br/> $H R$ | 
| [[topological K-theory|K-cohomology theory]] | [[K-homology theory]] | [[stable unitary group]] <br/> [[stable unitary group|BU]]  | [[K-theory spectrum]] <br/> [[KU]], ... |

=--

As for any [[generalized cohomology theory]] there are immediate variants to plain Cohomotopy theory, as shown in the following table:

[[!include flavours of cohomotopy -- table]]

### As the absolute cohomology theory
 {#AsTheAbsoluteCohomologyTheory}

In some sense Cohomotopy is the most fundamental of all [[generalized cohomology theories]] ("[[The Music of the Spheres]]").

Concretely, [[stable Cohomotopy cohomology theory]] is the [[initial object]] among [[multiplicative cohomology theories]], in that the [[sphere spectrum]] is the [[initial object in an (infinity,1)-category|initial object]] in ([[E-infinity ring|E-infinity]]) [[ring spectra]]. This means that for any other [[multiplicative cohomology theory|multiplicative]] [[generalized (Eilenberg-Steenrod) cohomology theory|cohomology theory]] $E$ there is an essentially unique multiplicative [[natural transformation]]  

\[
  \label{BoardmanHomomorphism}
  \mathbb{S}^\bullet(X)
  \overset{\beta(X)}{\longrightarrow}
  E^\bullet(X)
\]

from Cohomotopy cohomology groups to $E$-cohomology groups -- the _[[Boardman homomorphism]]_.

Specifically for $E = K \mathbb{F}$ the [[algebraic K-theory]] of a [[field]] $\mathbb{F}$ (such as a [[prime field]] $\mathbb{F}_p$) there is such a comparison morphism; and another way how stable Cohomotopy is the most fundamental of all K-theories is that it is equivalently the [[algebraic K-theory]] over the "absolute base", namely over the "[[field with one element]]" $\mathbb{F}_1$ (see [there](stable+cohomotopy#AsAlgebraicKTheoryOverTheFieldWithOneElement) for more):

$$
  \mathbb{S}^\bullet(X) 
  \;\simeq\;
  K\mathbb{F}_1 ^ \bullet(X)
  \,.
$$

For example, for $E = $ [[KU]] and in the case of $G$-[[equivariant cohomology theory]] ([[equivariant Cohomotopy theory]] and [[equivariant K-theory]]) the [[Boardman homomorphism]] (eq:BoardmanHomomorphism) gives the comparison map

$$
  \mathbb{S}^0_G(\ast)
  \simeq
  R_{\mathbb{F}_1}(G)
  \simeq
  A(G)
  \overset{\mathbb{C}[-]}{\longrightarrow}
  R_{\mathbb{C}}(G)
  \simeq
  KU^0_G(\ast)
$$

from the [[Burnside ring]] to the [[representation ring]] of the [[finite group]] $G$, by forming [[permutation representations]]; where we may think of the [[Burnside ring]] as being the [[representation ring]] over the "[[field with one element]]" (see e.g. [Chu-Lorscheid-Santhanam 10](field+with+one+element#ChuLorscheidSanthanam10)), as indicated above.

So far, this applies to [[stable Cohomotopy theory]], which historically has received almost all the attention. But, while [[stabilization]]  makes the immensely rich nature of [[homotopy theory]] a tad more tractable, it is only an approximation (just the first [[Goodwillie calculus|Goodwillie derivative]]!) of full unstable/[[non-abelian cohomology]].
Hence the one concept more fundamental than stable Cohomotopy theory is actual Cohomotopy theory.

For example, the classification of [[Yang-Mills instantons]] on $\mathbb{R}^4$ is typically regarded in the [[non-abelian cohomology]] theory represented by the [[classifying space]] $B SU(N)$ of the [[special unitary group]] (for $N \geq 2$, starting with [[SU(2)]])

$$
  (B SU(N))^0
  \Big(
    \big(
      \mathbb{R}^{4}
    \big)^{cpt}
  \Big)
  \;\coloneqq\;
  \Big\{ 
    \big(
      \mathbb{R}^{4}
    \big)^{cpt}
    \to
    B SU(N)
  \Big\}/_{\sim_{homotopy}}
  \;\simeq\;
  \underset{
    \mathclap{
    \color{blue}
    {\text{instanton} \atop \text{number}}
    }
  }{
    \mathbb{Z}
  }
  \,.
$$

But since the [[one-point compactification]] of 4d [[Euclidean space]] is the [[4-sphere]] $\big( \mathbb{R}^4\big)^{cpt} \simeq S^4$, this classification factors through one in unstable Cohomotopy theory, via the "unstable Boardman homomorphism" $S^4 \longrightarrow B SU(N)$ representing the generator of the 4th [[homotopy group]] of $B SU(N)$ (see [there](unitary+group#HomotopyGroups))

$$
  \pi^0
  \Big(
    \big(
      \mathbb{R}^{4}
    \big)^{cpt}7
  \Big)
  \;\coloneqq\;
  \Big\{ 
    \big(
      \mathbb{R}^{4}
    \big)^{cpt}
    \to
    S^4
  \Big\}/_{\sim_{homotopy}}
  \;\simeq\;
  \underset{
    \mathclap{
    \color{blue}
    {\text{instanton} \atop \text{number}}
    }
  }{
    \mathbb{Z}
  }
  \,.
$$

(see [SS 19, p. 9-10](#SatiSchreiber19)) This is the tip of an iceberg. Which needs to be discussed elsewhere.

\linebreak

## Properties

### Hopf degree theorem

+-- {: .num_prop}
###### Proposition
**([[Hopf degree theorem]])**

Let $n \in \mathbb{N}$ be a [[natural number]] and $X \in Mfd$ be a [[connected topological space|connected]] [[orientation|orientable]] [[closed manifold]] of [[dimension]] $n$. Then the $n$th [[cohomotopy]] classes $\left[X \overset{c}{\to} S^n\right] \in \pi^n(X)$ of $X$ are in [[bijection]] to the [[degree of a continuous function|degree]] $deg(c) \in \mathbb{Z}$ of the representing functions, hence the canonical function

$$
  \pi^n(X) 
    \underoverset{\simeq}{S^n \to K(\mathbb{Z},n)}{\longrightarrow}
   H^n(X,\mathbb{Z}) 
     \;\simeq\;   
   \mathbb{Z}
$$

from $n$th [[cohomotopy]] to $n$th [[integral cohomology]] is a [[bijection]].

=--

(e.g. [Kosinski 93, IX (5.8)](#Kosinski93))


### Poincaré–Hopf theorem

* [[Poincaré–Hopf theorem]]

### Relation to Freudenthal suspension theorem

relation to the [[Freudenthal suspension theorem]] ([Spanier 49, section 9](#Spanier49))

### Smooth representatives

For $X$ a [[compact topological space|compact]] [[smooth manifold]], there is a [[smooth function]] $X \to S^n$ representing every cohomotopy class (with respect to the standard [[smooth structure]] on the [[sphere]] [[manifold]]).


### Reduced Cohomotopy
 {#ReducedCohomotopy}

For some purposes (such as in stating [[Pontryagin's theorem]] [below](#RelationToCobordismGroup)) it is more natural to use [[reduced cohomology|reduced]] Cohomotopy:

For $(X,x)$ a [[pointed homotopy type]]/cofibrant [[pointed topological space]], its **reduced $n$-Cohomotopy** is the set of connected components in the [[compact-open topology|mapping space]] of pointed functions to the [[n-sphere]] (for any choice of basepoint on the latter, then naturally thought of as $\infty \in (\mathbb{R}^n)^{cpt} \simeq S^n$):

\[
  \label{ReducedCohomotopySet}
  {\widetilde \pi}{}^n
  (X,x)
  \;\coloneqq\;
  \pi_0 
  Maps^{\ast/}
  \big(
    (X,x),
    (S,\infty)
  \big)
  \,.
\]

However, the difference between reduced and unreduced Cohomotopy is small:

\begin{prop}
  For $n \geq 1$ a [[positive number|positive]] [[natural number]] and $(X,x)$ a [[pointed topological space]]/[[pointed homotopy type]], the canonical [[morphism]] from reduced (eq:ReducedCohomotopySet) to unreduced Cohomotopy of $X$ in degree $n$ is an [[isomorphism]]:

$$
  {\widetilde \pi}^{n \geq 1}(X,x)
    \overset{\;\;\simeq\;\;}{\longrightarrow}
  {\pi}^{n \geq 1}(X)
  \,.
$$
\end{prop}
(e.g. [Hatcher, 4A.2, 4A.3](algebraic+topology#Hatcher))
\begin{proof}
Observe that 

$$
  Maps^{\ast/}\big((X,x),(S^n,\infty) \big)
    \overset{fib(ev_x)}{\longrightarrow}
  Maps\big(X,S^n \big)
    \overset{ev_x}{\longrightarrow}
  S^n
$$

(where $ev_x$ is the [[evaluation map]] at $x \in X$) is a [[homotopy fiber sequence]] as soon as $X$ is represented by a [[cell complex]] (e.g. [[CW-complex]]). This follows either from the [pullback-power axiom](enriched+model+category#PullbackPowerAxiom) in the [[classical model structure on topological spaces]], or, more abstractly from the characterization of [[derived hom-spaces]] in [[slice (infinity,1)-category|coslice (infinity,1)-categories]] [here](slice+infinity-category#HamSpacesInASlice).

Therefore we have the corresponding [[long exact sequence of homotopy groups]], which starts out as

\begin{xymatrix@C=20pt}
  \pi_1\big( S^n \big)
  \ar[r]
  \ar@{=}[d]
  & 
  \pi_0 \mathrm{Maps}^{\ast/}\big((X,x),(S^n,\infty) \big)
  \ar[r]^{  }
  \ar@{=}[d]
  &
  \pi_0 \mathrm{Maps}\big(X,S^n \big)
  \ar[r]
  \ar@{=}[d]
  &
  \pi_0(S^n)
  \ar@{=}[d]
  \\
  {\overbrace{
  \begin{array}{ccc}
    \mathbb{Z} &\!\!\vert\!\!& n = 1
    \\
    \ast &\!\!\vert\!\!& n \geq 2
  \end{array}
  }}
  \ar[r]
  &
  {\widetilde \pi}{}^n(X,x)    
  \ar[r]
  &
  {\pi}{}^n(X)
  \ar[r]
  &
  \ast
  \,.
\end{xymatrix}

By [[exact sequence|exactness]], this yields the claim for $n \geq 2$; while for $n = 1$ it gives the desired isomorphism only up to a possibly non-trivial [[quotient set|quotient]] by an [[action]] of $\mathbb{Z} \simeq \pi_1(S^1)$:

$$
  {\widetilde \pi}{}^1(X,x)/\pi_1(S^1)
  \simeq
  \pi^1(X)
  \,.
$$

Hence it is now sufficient to see that the $\pi_1(S^1)$-[[action]] on reduced 1-Cohomotopy is always trivial:

Now, the action of $n \in \pi_1(S^1)$ takes $\big[ (X,x) \overset{ \;c\; }{\longrightarrow} (S^1,\ast) \big]$ to any $\big[ (X,x) \overset{ \;c'\; }{\longrightarrow} (S^1,\ast) \big]$ such that $[X \overset{c}{\longrightarrow} S^1] \overset{\eta}{\Rightarrow} [X \overset{c'}{\longrightarrow} S^1]$ in $\pi^1(X)$, with $[\eta(x,-)] = n \in \pi_1(S^1)$. 
But using the [[group]]-structure on $S^1 = \mathbb{R}/\mathbb{Z}$  we have that one such $\eta$ is given by $\eta(x,t) \coloneqq c(x) + n t \,mod\, \mathbb{Z}$, which yields $c'(x) = c(x) + n \,mod\, \mathbb{Z}$ and hence $c' = c$.
\end{proof}


### Pontryagin isomorphism between Cohomotopy and framed Cobordism
  {#RelationToCobordismGroup}

_[[Pontryagin's theorem]]_ ([Pontryagin 38](#Pontryagin38), [Pontryagin 55](#Pontryagin55)) is an identification of [[cobordism classes]] of [[normally framed submanifolds]] of [[codimension]] $n$ in a [[closed manifold]] $X^d$ with the $n$-[[Cohomotopy]] of that manifold -- the [[homotopy classes]] of [[maps]] into the [[n-sphere]], which is exhibited by the _[[Cohomotopy charge map]]_, often known as the [[Pontryagin-Thom collapse construction]]_:

$$
  Cob^n_Fr(X)
  \overset{\simeq}{\longrightarrow}
  \pi^n(X)
  \,.
$$

The analogous statement identifying [[cobordism classes]] of [[normally oriented submanifolds]] with [[homotopy classes]] of maps into the [[universal vector bundle|universal]] [[special orthogonal group|special orthogonal]] [[Thom space]] $M SO(n)$ is _[[Thom's theorem]]_ ([Thom 54](#Thom54)). Both statements, as well as their joint generalization to other [[tangential structures]] and notably their [[stabilization]] to [[Whitehead-generalized cohomology theory|Whitehead-generalized]] [[Cobordism cohomology theory]], have come to be widely known as the _[[Pontryagin-Thom collapse construction]]_, or similar, and form the basis of modern [[cobordism theory]] and its application in [[stable homotopy theory]].

\linebreak

For $X$ a [[closed manifold|closed]] [[smooth manifold]] of [[dimension]] $D$, the assignment of [[Cohomotopy charge]] (the _[[Pontryagin-Thom construction]]_, in this unstable and framed version due to [Pontrjagin 55](#Pontrjagin55), see review in [Kosinski 93, IX.5](#Kosinski93), [Milnor 97](#Milnor97)) identifies the [[set]] 

$$
  SubMfd_{/bord}^{d}(X)
$$

of [[cobordism classes]] of  [[closed manifold|closed]] and [[normally framed submanifolds]] $\Sigma \overset{\iota}{\hookrightarrow} X$ of [[dimension]] $d$ inside $X$ with the [[cohomotopy]] $\pi^{D-d}(X)$ of $X$ in degree $D- d$

$$
  SubMfd_{/bord}^{d}(X)
    \underoverset{\simeq}{\;\;\;PT\;\;\;}{\longrightarrow}
  \pi^{D-d}(X)
  \,.
$$

(e.g. [Kosinski 93, IX Theorem (5.5)](#Kosinski93))

In particular, by this [[bijection]] the canonical [[group]] [[structure]] on [[cobordism groups]] in sufficiently high [[codimension]] (essentially given by [[disjoint union]] of [[submanifolds]]) this way induces a group structure on the cohomotopy sets in sufficiently high degree.



{#PontrjaginThomConstructionGraphics}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/PontrjaginThomConstructionI.jpg" width="800">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)

Here the [[normal framing]] of the submanifolds plays the role of the [[charge]] in [[Cohomotopy]] which they carry:

{#nCohomotopyChargeOfSubmanifoldsIsNormalFraming}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyChargeOfSubmanifoldsIsNormalFraming.jpg" width="800">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


For example:

{#nCohomotopyOfEuclideanNSpaceIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/nCohomotopyOfEuclideanNSpace.jpg" width="840">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


This construction generalizes to [[equivariant cohomotopy]], see [there](equivariant+cohomotopy#PontryaginThomConstruction).

With the [[equivariant Hopf degree theorem]] the above example has the following $\mathbb{Z}_2$-[[equivariant homotopy theory|equivariant]] version (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationSpheres)):

{#EquivariantnCohomotopyOfEuclideanNOrientifoldIllustration}$\,$


<center>
<img src="https://ncatlab.org/nlab/files/EquivariantNCohomotopyOfEuclideanNOrientifold.jpg" width="840">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)


Further by the [[equivariant Hopf degree theorem]] (see [there](equivariant+Hopf+degree+theorem#EquivariantCohomotopyOfRepresentationTori)), this example generalizes to [[equivariant cohomotopy]] of [[toroidal orbifold|toroidal]] [[orientifolds]]:


{#EquivariantnCohomotopyOfToroidalNOrientifoldIllustration}$\,$

<center>
<img src="https://ncatlab.org/nlab/files/EquivariantCohomotopyOfToroidalOrientifold.jpg" width="850">
</center>

> graphics grabbed form [Sati-Schreiber 19](#SatiSchreiber19)

\linebreak

### Composition/product in Cohomotopy
  {#ProductInCohomotopy}

Under the [[Pontryagin-Thom isomorphism]] ([above](#RelationToCobordismGroup)) the product in Cohomotopy, i.e. the [[composition]] operation

$$
  \array{
    \pi^{n_1}
    \big( 
      S^{n_2 + n_1}
    \big)
    \times
    \pi^{n_2 + n_1}(X)
    &\overset{}{\longrightarrow}&
    \pi^{n_1}(X)
    \\
    (c_1, c_2) &\mapsto& c_1 \circ c_2
  }
  \,,
$$

corresponds to forming [[product manifolds]] of submanifolds, in that (see also [Kosinski 93, Section IX 6.1](#Kosinski93)):


$$
    \mathrm{PT}^{-1}(c_1 \circ c_2)
    \;\simeq\;
    \Big[
      \mathrm{PT}^{-1}(c_2) \times \mathrm{PT}^{-1}(c_1)
      \;\subset\;
      \mathrm{PT}^{-1}(c_2) \times \mathbb{R}^{n_2 + n_1}
      \;\subset\;
      X
    \Big]
  \,.
$$

This is exhibited by the following [[pasting diagram]] of [[pullbacks]]/[[fiber products]] (repeatedly using the [[pasting law]]):

\begin{imagefromfile}
        "file_name": "ProductInCohomotopyUnderPT.jpg",
        "web": "nlab",
        "width": 600,
        "unit": "px",
        "margin": {
            "top": -20,
            "right": 0,
            "bottom": 20,
            "left": 20,
            "unit": "px"
        },
        "alt": "product in Cohomotopy under the PT isomorphism",
        "caption": "from [SS21](https://ncatlab.org/schreiber/show/Equivariant+Cohomotopy+and+Oriented+Cohomology+Theory)"
\end{imagefromfile}

Here the vertical inclusions are the defining ones of the [[submanifolds]] or of their [[normal bundles]], identified with some choice of [[tubular neighbourhoods]].



\linebreak



### Cohomotopy charge map and Relation to configuration spaces
 {#RelationToConfigurationSpaces}


The _[[Cohomotopy charge map]]_ is the [[function]] that assigns to a [[configuration space of points|configuration of points]] their total [[charge]] as measured in [[Cohomotopy]]-[[generalized cohomology|cohomology theory]].

This is alternatively known as the "electric field map" ([Salvatore 01](Cohomotopy+charge#Salvatore01) following [Segal 73, Section 1](Cohomotopy+charge#Segal73), see also [Knudsen 18, p. 49](Cohomotopy+charge#Knudsen18)) or the "scanning map" ([Kallel 98](Cohomotopy+charge#Kallel98)).


For $D \in \mathbb{N}$ the _Cohomotopy charge map_ is the  [[continuous function]]

\[
  \label{CohomotopyChargeMapOnEuclideanSpace}
  Conf\big( \mathbb{R}^D \big)
  \overset{cc}{\longrightarrow}
  \mathbf{\pi}^D
  \Big( 
    \big( \mathbb{R}^D \big)^{cpt}
  \Big)
  =
  Maps^{\ast/\!}\Big( \big(\mathbb{R}^D\big)^{cpt} , S^D\big)
  =
  \Omega^{D} S^D
\]

from the [[configuration space of points]] in the [[Euclidean space]] $\mathbb{R}^D$ to the $D$-[[Cohomotopy]] [[cocycle space]] [[vanishing at infinity]] on the [[Euclidean space]](which is equivalently the [[space of maps|space of pointed maps]] from the [[one-point compactification]] $S^D \simeq \big( \mathbb{R}^D \big)$ to itself, and hence equivalently the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]]), which sends a configuration of points in $\mathbb{R}^D$, each regarded as carrying unit [[charge]] to their total [[charge]] as measured in  [[Cohomotopy]]-[[generalized cohomology|cohomology theory]] ([Segal 73, Section 3](Cohomotopy+charge#Segal73)).

This has evident generalizations to other manifolds than just Euclidean spaces, to spaces of labeleed configurations and to [[equivariant Cohomotopy]]. The following graphics illustrates the Cohomotopy charge map on [[G-space]] [[tori]] for $G = \mathbb{Z}_2$ with values in $\mathbb{Z}_2$-[[equivariant Cohomotopy]]:

<center>
<a href="https://arxiv.org/pdf/1909.12277.pdf#page=24">
<img src="https://ncatlab.org/schreiber/files/EquivariantCohomotopyTadpoleCancellationN.jpg" width="700">
</a>
</center>

> graphics grabbed from [SS 19](#SatiSchreiber19)

In some situations the [[Cohomotopy charge map]] is a [[weak homotopy equivalence]] and hence exhibits, for all purposes of [[homotopy theory]], the [[Cohomotopy]] [[cocycle space]] of Cohomotopy charges as an equivalent reflection of the [[configuration space of points]]. 



+-- {: .num_prop #GroupCompletionOfConfigurationSpaceIsIteratedBasedLoopSpace}
###### Proposition
**([[group completion]] on [[configuration space of points]] is [[iterated based loop space]])**

The [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    cc
  }{\longrightarrow}
  \Omega^D S^D
$$

from the full unordered and unlabeled configuration space ([here](configuration+space+of+points#eq:UnorderedUnlabeledConfigurationSpace)) of [[Euclidean space]] $\mathbb{R}^D$  to the $D$-fold [[iterated based loop space]] of the [[n-sphere|D-sphere]], exhibits the [[group completion]] ([here](configuration+space+of+points#eq:GroupCompletionOfConfigurationSpaceMonoid)) of the configuration space monoid 

$$
  \Omega B_{{}_{\sqcup}\!} 
  Conf
  \big(
    \mathbb{R}^D
  \big)
  \overset{
    \simeq
  }{\longrightarrow}
  \Omega^D S^D
$$

=--

([Segal 73, Theorem 1](Cohomotopy+charge#Segal73))

+-- {: .num_prop #CohomotopyChargeMapIsEquivalenceOnSPhereLabeledConfihgurationSpace}
###### Proposition
**([[Cohomotopy charge map]] is [[weak homotopy equivalence]] on sphere-labeled [[configuration space of points]])**

For $D, k \in \mathbb{N}$ with $k \geq 1$, the [[Cohomotopy charge map]] (eq:CohomotopyChargeMapOnEuclideanSpace)

$$
  Conf
  \big(
    \mathbb{R}^D,
    S^k
  \big)
  \underoverset{\simeq}{cc}{\longrightarrow}
  \Omega^D S^{D + k}
$$

is a [[weak homotopy equivalence]] from the configuration space ([here](configuration+space+of+points#eq:UnorderedLabeledCOnfigurationSpace)) of unordered points with labels in $S^k$ and vanishing at the base point of the label space to the $D$-fold [[iterated loop space]] of the [[n-sphere|D+k-sphere]].

=--

([Segal 73, Theorem 3](Cohomotopy+charge#Segal73))


The May-Segal theorem \ref{ScanningMapEquivalenceOverCartesianSpace} generalizes from [[Euclidean space]] to [[closed manifold|closed]] [[smooth manifolds]] if at the same time one passes from plain [[Cohomotopy]] to [[twisted Cohomotopy]], twisted, via the [[J-homomorphism]], by the [[tangent bundle]]:

+-- {: .num_prop #ScanningMapEquivalenceOverClosedManifold}
###### Proposition

Let 

1. $X^n$ be a [[smooth manifold|smooth]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ J-twisted Cohomotopy space}}
  }{
    Maps_{{}_{/B O(n)}}
    \Big(
      X^n 
      \;,\; 
      S^{
        \mathbf{n}_{def} + \mathbf{k}_{\mathrm{triv}}    
      }
      \!\sslash\!
      O(n)
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. the [[J-homomorphism|J]]-[[twisted Cohomotopy|twisted (n+k)-Cohomotopy]] space of $X^n$, hence the [[space of sections]] of the $(n + k)$-[[spherical fibration]] over $X$ which is [[associated fiber bundle|associated]] via the [[tangent bundle]] by the [[O(n)]]-[[action]] on $S^{n+k} = S(\mathbb{R}^{n} \times \mathbb{R}^{k+1})$

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--

([Bödigheimer 87, Prop. 2](Cohomotopy+charge#Boedigheimer87), following [McDuff 75](Cohomotopy+charge#McDuff75))

+-- {: .num_prop #ScanningMapEquivalenceOverClosedFramedManifold}
###### Remark

In the special case that the [[closed manifold]] $X^n$ in Prop. \ref{ScanningMapEquivalenceOverClosedManifold} is [[parallelizable manifold|parallelizable]], hence that its [[tangent bundle]] is [[trivial bundle|trivializable]], the statement of Prop. \ref{ScanningMapEquivalenceOverClosedManifold} reduces to this:

Let

1. $X^n$ be a [[parallelizable manifold|parallelizable]] [[closed manifold]] of [[dimension]] $n$;

1. $1 \leq k \in \mathbb{N}$ a [[positive number|positive]] [[natural number]].

Then the [[Cohomotopy charge map]] constitutes a [[weak homotopy equivalence]]

$$
  \underset{
    \color{blue}
    { \phantom{a} \atop \text{ Cohomotopy space}}
  }{
    Maps
    \Big(
      X^n 
      \;,\; 
      S^{
       n + k    
      }
    \Big)
  }
  \underoverset
  {\simeq}
  {
    \color{blue}
    \text{Cohomotopy charge map}
  }
  {\longleftarrow}
  \underset{
    \mathclap{
    \color{blue}
      {
        \phantom{a}
        \atop
        {
          \text{configuration space}
          \atop 
          \text{of points}
        }
      }
    }
  }{
    Conf
    \big(
      X^n,
      S^k
    \big)
  }
$$

between 

1. $(n+k)$-[[Cohomotopy]] space of $X^n$, hence the [[space of maps]] from $X$ to the [[n-sphere|(n+k)-sphere]]

1. the [[configuration space of points]] on $X^n$ with labels in $S^k$.

=--


\linebreak

### Complex-rational Cohomotopy and moduli space of Yang-Mills monopoles

The assignment of [[scattering amplitudes]] of [[monopoles]] in [[SU(2)]]-[[Yang-Mills theory]] is a  [[diffeomorphism]]

$$
  \mathcal{M}_k
  \overset{ S }{\longrightarrow}
  R_k
$$

identifying the [[moduli space of monopoles]] of number $k$ with the space of complex-[[rational functions]] form the [[Riemann sphere]] to itself, of [[degree of a continuous function|degree]] $k$ (hence the [[cocycle space]] of complex-rational 2-[[Cohomotopy]]).

([Atiyah-Hitchin 88, Theorem 2.10](moduli+space+of+monopoles#AtiyahHitchin88))

{#Illustration} $\,$


<center>
<img src="https://ncatlab.org/nlab/files/AtiyahHitchinChargeQuantizationII.jpg" width="640">
</center>

This is a [[non-abelian group|non-abelian]] analog of the [[Dirac charge quantization]] of the [[electromagnetic field]], with [[ordinary cohomology]] replaced by [[Cohomotopy]] [[generalized cohomology theory|cohomology theory]].



## Examples

### Cohomotopy in the lowest dimensions

Since the [[0-sphere]] is the disjoint union of two points, $0$-cohomotopy corresponds to the powerset of the connected components of a space.

Further, the $(-1)$-sphere is understood as the [[empty space]]. Since the only map to the empty space is the identity map from the empty space, the $(-1)$-cohomotopy of a space is measuring whether that space is empty. In the context of [[homotopy type theory]], this is the same as [[negation]].



### Of projective spaces

Cohomotopy sets of [[projective spaces]] are computed in [West 71](#West71)

### Of 4-Manifolds
 {#On4Manifolds}

Let $X$ be a [[4-manifold]] which is [[connected topological space|connected]] and [[orientation|oriented]].

The [[Pontryagin-Thom construction]] as [above](#RelationToCobordismGroup) gives for $n \in \mathbb{Z}$ the [[commuting diagram]] of sets

$$
  \array{
     \pi^n(X) 
       &\overset{\simeq}{\longrightarrow}&
     \mathbb{F}_{4-n}(X)
     \\
     {}^{ \mathllap{h^n} }
     \downarrow
       &&
     \downarrow^{ h_{4-n} }
     \\
     H^n(X,\mathbb{Z})
       &\underset{\simeq}{\longrightarrow}&
     H_{4-n}(X,\mathbb{Z})
     \,,
  }
$$

where $\pi^\bullet$ denotes cohomotopy sets, $H^\bullet$ denotes [[ordinary cohomology]], $H_\bullet$ denotes [[ordinary homology]] and $\mathbb{F}_\bullet$ is [[normal bundle|normally]] [[framing|framed]] [[cobordism classes]] of [[normal bundle|normally]] [[framing|framed]] [[submanifolds]]. Finally $h^n$ is the operation of pullback of the generating integral cohomology class on $S^n$ (by the nature of [[Eilenberg-MacLane spaces]]):

$$
  h^n(\alpha) \;\colon\; X \overset{\alpha}{\longrightarrow} S^n \overset{generator}{\longrightarrow} B^n \mathbb{Z}
  \,.
$$

Now 

* $h^0$, $h^1$, $h^4$ are [[isomorphisms]]

* $h^3$ is an isomorphism if $X$ is "odd" in that it contains at least one closed oriented [[surface]] of odd self-intersection, otherwise $h^3$ becomes an isomorphism on a $\mathbb{Z}/2$-[[quotient group]] of $\pi^3(X)$ (which is a group via the [[group]]-[[structure]] of the [[3-sphere]] ([[special unitary group|SU(2)]]))

([Kirby-Melvin-Teichner 12](#KirbyMelvinTeichner12))


\linebreak

## Related concepts

[[!include flavours of cohomotopy -- table]]

* [[differential cohomotopy]]

\linebreak

[[!include Segal completion -- table]]

\linebreak

* [[Cohomotopy charge map]]

## References

### General

Original articles:

* {#Borsuk36} [[Karol Borsuk]], _Sur les groupes des classes de transformations continues_, CR Acad. Sci. Paris 202.1400-1403 (1936): 2 ([doi:10.24033/asens.603](https://doi.org/10.24033/asens.603))

* {#Pontryagin38a} [[Lev Pontrjagin]], _[[Classification of continuous maps of a complex into a sphere]]_, _Communication I_, Doklady Akademii Nauk SSSR 19(3) (1938), 147-149
 
* {#Spanier49} [[Edwin Spanier]], _Borsuk's Cohomotopy Groups_, Annals of Mathematics Second Series, Vol. 50, No. 1 (Jan., 1949), pp. 203-245 ([jstor:1969362](http://www.jstor.org/stable/1969362))

* [[Franklin Peterson]], _Some Results on Cohomotopy Groups_, American Journal of Mathematics Vol. 78, No. 2 (Apr., 1956), pp. 243-258 ([jstor:2372514](https://www.jstor.org/stable/2372514))

* [[Jan Jaworowski]], _Generalized cohomotopy groups as limit groups_, Fundamenta Mathematicae 50 (1962), 393-402 ([doi:10.4064/fm-50-4-333-340](https://www.impan.pl/en/publishing-house/journals-and-series/fundamenta-mathematicae/all/50/4), [pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm50/fm50133.pdf))


See also 

* Wikipedia, _[Cohomotopy group](http://en.wikipedia.org/wiki/Cohomotopy_group)_

* [[eom]], _[Cohomotopy group](https://www.encyclopediaofmath.org/index.php/Cohomotopy_group)_


Further discussion of Cohomotopy:

* [[Laurence Taylor]], _The principal fibration sequence and the second cohomotopy set_, Proceedings of the Freedman Fest, 235251, Geom. Topol. Monogr., 18, Coventry, 2012 ([arXiv:0910.1781](https://arxiv.org/abs/0910.1781), [doi:10.2140/gtm.2012.18.235](http://dx.doi.org/10.2140/gtm.2012.18.235))



[[!include Pontryagin-Thom construction -- references]]



### Examples 

Cohomotopy sets of [[projective spaces]]:

* {#West71} Robert West, _Some Cohomotopy of Projective Space_, Indiana University Mathematics Journal Vol. 20, No. 9 (March, 1971), pp. 807-827 ([jstor:24890146](https://www.jstor.org/stable/24890146))

Cohomotopy sets of [[4-manifolds]]:

* Nobuo Shimada, _Homotopy classification of mappings of a 4-dimensional complex into a 2-dimensional sphere_, Nagoya Math. J., Volume 5 (1953), 127-144 ([euclid:nmj/1118799399](https://projecteuclid.org/euclid.nmj/1118799399))

* [[Daniel Freed]], [[Karen Uhlenbeck]], Appendix B of: _Instantons and Four-Manifolds_, Mathematical Sciences Research Institute Publications, Springer 1991 ([doi:10.1007/978-1-4613-9703-8](https://link.springer.com/book/10.1007/978-1-4613-9703-8))

* {#KirbyMelvinTeichner12} [[Robion Kirby]], [[Paul Melvin]], [[Peter Teichner]], _Cohomotopy sets of 4-manifolds_, Geometry & Topology Monographs 18 (2012) 161–190 ([arXiv:1203.1608](https://arxiv.org/abs/1203.1608), [doi:10.2140/gtm.2012.18.161](http://dx.doi.org/10.2140/gtm.2012.18.161))

Cohomotopy sets of [[Thom spaces]]:

* [[Thomas Rot]], _Homotopy classes of proper maps out of vector bundles_,  Arch. Math. 114, 107–117 (2020 ([arXiv:1808.08073](https://arxiv.org/abs/1808.08073), [doi:10.1007/s00013-019-01372-z](https://doi.org/10.1007/s00013-019-01372-z))

In relation to [[quaternionic line bundles]] over [[5-manifolds]]:

* [[Panagiotis Konstantis]], _Vector bundles and cohomotopies of spin 5-manifolds_, Homology, Homotopy and Applications Volume 23 (2021) Number 1 ([arXiv:1812.06547](https://arxiv.org/abs/1812.06547), [doi:10.4310/HHA.2021.v23.n1.a9](https://dx.doi.org/10.4310/HHA.2021.v23.n1.a9))


Cohomotopy sets of [[spin structure|spin]]-manifolds in co-degree 1:

* [[Panagiotis Konstantis]], _A counting invariant for maps into spheres and for zero loci of sections of vector bundles_,  Abh. Math. Semin. Univ. Hambg. (2020) ([arXiv:1911.03214](https://arxiv.org/abs/1911.03214), [doi:10.1007/s12188-020-00228-6](https://doi.org/10.1007/s12188-020-00228-6))


### Cohomotopy cocycle spaces

Discussion of Cohomotopy [[cocycle spaces]] (i.e. [[spaces of maps]] into an [[n-sphere]]):

* {#Hansen74} [[Vagn Lundsgaard Hansen]], _The homotopy problem for the components in the space of maps on the $n$-sphere_, Quart. J. Math. Oxford Ser. (3) 25 (1974), 313-321 ([DOI:10.1093/qmath/25.1.313](https://doi.org/10.1093/qmath/25.1.313))

* {#Hansen81} [[Vagn Lundsgaard Hansen]], _On Spaces of Maps of $n$-Manifolds Into the $n$-Sphere_, Transactions of the American Mathematical Society
Vol. 265, No. 1 (May, 1981), pp. 273-281 ([jstor:1998494](https://www.jstor.org/stable/1998494))

* [[Victor Vassiliev]], _Twisted homology of configuration spaces, homology of spaces of equivariant maps, and stable homology of spaces of non-resultant systems of real homogeneous polynomials_ ([arXiv:1809.05632](https://arxiv.org/abs/1809.05632))



Discussion of [[cocycle spaces]] for [[rational Cohomotopy]] (see also at _[[rational model of mapping spaces]]_):

* {#MollerRaussen85} [[Jesper Møller]], [[Martin Raussen]], _Rational Homotopy of Spaces of Maps Into Spheres and Complex Projective Spaces_, Transactions of the American Mathematical Society Vol. 292, No. 2 (Dec., 1985), pp. 721-732 ([jstor:2000242](https://www.jstor.org/stable/2000242)) 

### Relation to knots and links

 Relation to [[knots]] and [[links]]:

* Maths.SE, _[Framed Cobordism Classes of links in $\mathbb{R}^3$](https://math.stackexchange.com/q/426482/58526)_

### In computational topology

Discussion of [[Cohomotopy]]-sets in [[computational topology]]:

* [[Martin Čadek]], [[Marek Krčál]], Jiří Matoušek, [[Francis Sergeraert]], [[Lukáš Vokřínek]], [[Uli Wagner]], _Computing all maps into a sphere_, Journal of the ACM, Volume 61 Issue 3, May 2014 Article No. 1 ([arxiv:1105.6257](https://arxiv.org/abs/1105.6257))

* [[Lukáš Vokřínek]], _Decidability of the extension problem for maps into odd-dimensional spheres_,  Discrete Comput Geom (2017) 57: 1 ([arXiv:1401.3758](https://arxiv.org/abs/1401.3758))



[[!include cohomotopy in topological data analysis -- references]]




### Equivariant Cohomotopy

Discussion of the [[stable cohomotopy|stable]] cohomotopy ([[framed manifold|framed]] [[cobordism cohomology theory]]) in the [[equivariant cohomology]]-version of cohomotopy ([[equivariant cohomotopy]]):

* {#Wasserman69} [[Arthur Wasserman]], section 3 of _Equivariant differential topology_, Topology Vol. 8, pp. 127-150, 1969 ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/wasserman.pdf))

* {#Cruickshank03} [[James Cruickshank]], _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)

and in the [[twisted cohomology]]-version ([[twisted cohomotopy]])

* {#Cruickshank03} [[James Cruickshank]], Section 7 of _Twisted homotopy theory and the geometric equivariant 1-stem_, Topology and its Applications Volume 129, Issue 3, 1 April 2003, Pages 251-271 (<a href="https://doi.org/10.1016/S0166-8641(02)00183-9">arXiv:10.1016/S0166-8641(02)00183-9</a>)


Discussion of [[M-brane]] physics in terms of [[equivariant rational homotopy theory|rational equivariant]] cohomotopy:

* [[John Huerta]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Equivariant homotopy and super M-branes|Real ADE-equivariant (co)homotopy and Super M-branes]]_ ([arXiv:1805.05987](https://arxiv.org/abs/1805.05987))

and in terms of [[twisted cohomotopy]]:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], Section 3 of _[[schreiber:Twisted Cohomotopy implies M-theory anomaly cancellation]]_ ([arXiv:1904.10207](https://arxiv.org/abs/1904.10207))

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Twisted Cohomotopy implies M5 WZ term level quantization|Twisted Cohomotopy implies level quantization of the full 6d Wess-Zumino-term of the M5-brane]]_ ([arXiv:1906.07417](https://arxiv.org/abs/1906.07417))

* {#SatiSchreiber19} [[nLab:Hisham Sati]], [[nLab:Urs Schreiber]], _[[schreiber:Equivariant Cohomotopy implies orientifold tadpole cancellation]]_ ([arXiv:1909.12277](https://arxiv.org/abs/1909.12277))

### In spectral geometry

Discussion of [[smooth functions]] into the [[4-sphere]] in the context of [[Connes-Lott models]] in spectral [[non-commutative geometry]]:

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Quanta of Geometry: Noncommutative Aspects_, Phys. Rev. Lett. 114 (2015) 9, 091302 ([arXiv:1409.2471](https://arxiv.org/abs/1409.2471))

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Geometry and the Quantum: Basics_, JHEP 12 (2014) 098 ([arXiv:1411.0977](https://arxiv.org/abs/1411.0977))

* {#Connes17} [[Alain Connes]], section 4 of _Geometry and the Quantum_, in _Foundations of Mathematics and Physics One Century After Hilbert_, Springer 2018. 159-196 ([arXiv:1703.02470](https://arxiv.org/abs/1703.02470), [doi:10.1007/978-3-319-64813-2](https://www.springer.com/gp/book/9783319648125))


[[!redirects Cohomotopy]]

[[!redirects cohomotopy theory]]
[[!redirects Cohomotopy theory]]

[[!redirects cohomotopy set]]
[[!redirects cohomotopy sets]]
[[!redirects Cohomotopy set]]
[[!redirects Cohomotopy sets]]


[[!redirects cohomotopy group]]
[[!redirects cohomotopy groups]]
[[!redirects Cohomotopy group]]
[[!redirects Cohomotopy groups]]


[[!redirects cohomotopy cohomology ]]
[[!redirects cohomotopy cohomology theory]]
[[!redirects Cohomotopy cohomology ]]
[[!redirects Cohomotopy cohomology theory]]


