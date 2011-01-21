
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _synthetic differential $\infty$-groupoid_ is an [[∞-groupoid]] equipped with a [[cohesive (∞,1)-topos|cohesive structure]] that subsumes that of [[smooth ∞-groupoid]]s as well as of [[infinitesimal object|infinitesimal]] $\infty$-groupoids: [[∞-Lie algebroid]]s.

In the [[cohesive (∞,1)-topos]] of synthetic differential $\infty$-groupoids the canonical [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\mathbf{\Pi}(X)$ factors through a version relative to [[Smooth∞Grpd]]: the [[infinitesimal singular simplicial complex|infinitesimal path ∞-functor]] $\mathbf{\Pi}_{inf}(X)$. In traditional terms this is the object modeled by the [[tangent Lie algebroid]] and the [[de Rham space]] of $X$. The [[quasicoherent ∞-stack]]s on $\mathbf{\Pi}_{inf}(X)$ are [[D-module]]s on $X$.


## Definition

+-- {: .un_def}
###### Definition

Let [[CartSp]]${}_{synthdiff}$ be the [[full subcategory]] of the category of [[smooth loci]] on the objects of the form $\mathbb{R}^n \times D$ that are [[product]]s of a [[Cartesian space]] $\mathbb{R}^n$ for $n \in \mathbb{N}$ and an [[infinitesimally thickened point]] $D$.

Equip this category with the [[coverage]] where a family of morphisms  is [[covering]] precisely if it is of the form $\{U_i \times D \stackrel{(f_i, Id_D)}{\to} U \times D\}$ for $\{f_i : U_i \to U\}$ a covering in [[CartSp]]${}_{smooth}$ (a [[good open cover]]).

=--

This appears as ([Kock, (5.1)]{#Kock}). 


+-- {: .un_remark}
###### Remark

The [[sheaf topos]] over [[CartSp]]${}_{synthdiff}$ is ([[equivalence of categories|equivalent]] to) the [[topos]] known as the [[Cahiers topos]], a [[smooth topos]] that constitutes a [[Models for Smooth Infinitesimal Analysis|well adapted model]] for [[synthetic differential geometry]].

=--

+-- {: .un_def}
###### Definition

We say the [[(∞,1)-topos]] of **synthetic differential $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  SynthDiff \infty Grpd := Sh_{(\infty,1)}(CartSp_{synthdiff})
$$

on $CartSp_{synthdiff}$. 

=--


## Properites


### Cohesiveness over $\infty Grpd$

+-- {: .un_prop}
###### Proposition

$SynthDiff \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]]. See there for details.

=--


### $\infty$-Connectedness over $Smooth \infty Grpd$ {#RelativeInftyConnectedness}

+-- {: .un_def}
###### Definition

Write $i : CartSp_{smooth} \hookrightarrow CartSp_{synthdiff}$ for the canonical [[full subcategory|embedding]].

=--

+-- {: .un_prop}
###### Observation

This functor has a [[right adjoint]], that exhibits a [[coreflective subcategory]]

$$
  (i \dashv p) : CartSp_{synthdiff}
    \stackrel{\overset{i}{\leftarrow}}{\underset{p}{\to}}
   CartSp_{smooth}
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

We have an [[essential geometric morphism|essential]] [[(∞,1)-geometric morphism]] 

$$
 (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf} )
  :
  SynthDiff \infty Grpd
    \stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^*}{\leftarrow}}{\underset{P_*}{\to}}}
  Smooth \infty Grpd
  \,,
$$

that exhibits $SynthDiff\infty Grpd$ as a [[totally ∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]].

=--



+-- {: .proof}
###### Proof

We [[presentable (∞,1)-category|present]] the [[(∞,1)-category]] $SynthDiff \infty Grpd$ by the [[model structure on simplicial presheaves]] [[Bousfield localization of model categories|left Bousfield localized]] at the [[covering]] [[sieve]] inclusions 

$$
  Sh_{(\infty,1)}(CartSp_{synthdiff}) \simeq
  ([CartSp_{synthdiff}^{op}, sSet]_{loc})^\circ
$$

(as discussed at [[models for ∞-stack (∞,1)-toposes|models for (∞,1)-sheaf (∞,1)-toposes]]).

Consider the right [[Kan extension]] $Ran_i : [CartSp_{smooth}^{op}, sSet] \to [CartSp_{synthdiff}^{op},sSet]$ of [[simplicial presheaves]] along the functor $i$. On an object $K \times D \in CartSp_{synthdiff}$ it is given by 

$$
  \begin{aligned}
    Ran_{i} F : K \times D 
    & \mapsto {\lim_\leftarrow}_{\{U \to K \times D\}} F(U)
    \\
    & \simeq {\lim_\leftarrow}_{\{U \to K\} } F(U)
    \\
    & \simeq F(K)
    \\
    & \simeq F(p(K \times D))
    \\
    & =: (p^* F)(K \times D)
   \end{aligned}
  \,,
$$

were the [[limit]]s are over the [[opposite category|opposite]] [[comma categories]] $(i/K \times D)$ and $Id_{CartSp_{smooth}}/K$, respectively, and where we are using in the first step that there is a unique terminal morphism from $K \in CartSp_{smooth}$ to the [[infinitesimally thickened point]] $D$ and in the second step the [[Yoneda reduction]]-form of the [[Yoneda lemma]]. The rest is notation.

This shows that $p^*$ does have the further [[left adjoint]] given by restriction along $i$. 

From this are directly induced the corresponding [[simplicial Quillen adjunction]]s on the global projective and injective [[model structure on simplicial presheaves]]

$$
  ((-)\circ i \dashv (-) \circ p) : 
  [CartSp_{synthdiff}, sSet]_{proj}
   \stackrel{\overset{(-)\circ i}{\to}}{\underset{(-)\circ p}{\leftarrow}}
  [CartSp_{smooth}, sSet]_{proj}
  \,.
$$

$$
  ((-) \circ p \dashv Ran_p) : 
  [CartSp_{synthdiff}, sSet]_{inj}
   \stackrel{\overset{(-)\circ p}{\leftarrow}}{\underset{Ran_p}{\to}}
  [CartSp_{smooth}, sSet]_{inj}
  \,.
$$

By the discussion at [[simplicial Quillen adjunction]] for this to descent to the Cech-local [[model structure on simplicial presheaves]] it suffices that the [[right adjoint]]s preserve locally fibrant objects. By the properties of [[Bousfield localization of model categories|left Bousfield localization]] this in turn is implied if  the [[left adjoint]]s preserve [[covering]]s. This is clearly the case by the very definition of the site structure on [[CartSp]]${}_{synthdiff}$.

It follows that $\Pi_{inf} : SynthDiff \infty Grpd \to Smooth \infty Grpd$ is given by the left [[derived functor]] of restriction along $i$. Since [[(∞,1)-limit]]s of [[(∞,1)-sheaves]] are computed objectwise, this shows that $\Pi_{inf}$ preserves these.

=--


+-- {: .un_remark}
###### Remark

Accordingly the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] has a _relative_ analog $\Pi_{inf}$, as indicated above. In the discussion of [Paths and geometric Postnikov towers](#StrucPaths) below we identify this with the [[(∞,1)-functor]] that assigns [[∞-groupoid]]s of  [[infinitesimal object|infinitesimal]] paths.

=--

## Structures

We discuss the realization of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> in $SynthDiff \infty Grpd$.

### Concrete objects {#StrucConcreteObjects}

(...)

### Geometry and structure sheaves {#StrucGeometry}

(...)

### Cohesive $\infty$-groups {#StrucInfinGroups}

(...)

### Cohomology and principal $\infty$-bundles {#StrucCohomology}

(...)

### Concordance {#StrucConcordance}

(...)

### Geometric homotopy and Galois theory {#StrucGeometricHomotopy}

(...)

### van Kampen theorem {#StrucVanKampen}

(...)

### Paths and geometric Postnikov towers {#StrucPaths}

+-- {: .un_def}
###### Definition

The **infinitesimal path $\infty$-functor** is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Paths">intrinsic path ∞-groupoid</a> for the _[relative](#RelativeInftyConnectedness)_ [[strongly ∞-connected (∞,1)-topos|strongly ∞-connected structure]] $\Pi_{inf} : SynthDiff \infty Grpd \to Smooth\infty Grpd$:

$$
  (\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf}) :=
  (Disc_{inf} \Pi_{inf} \dashv Disc_{inf} \circ \Gamma_{inf})
  :
  SynthDiff \infty Grpd
  \to 
  SynthDiff \infty Grpd
  \,.
$$

=--


+-- {: .un_prop}
###### Observation

For $X$ a [[smooth locus]], $\mathbf{\Pi}_{inf}(X)$ is the corresponding [[de Rham space]]. 

$$
  \mathbf{\Pi}_{inf}(X) : U \times D \mapsto X(U)
  \,.
$$

=--
(...)


### Universal coverings and geometric Whitehead towers {#StrucWhitehead}

(...)


### Flat $\infty$-connections and local systems {#StrucFlat}

(...)

### de Rham cohomology {#StrucDeRham}

(...)


### $\infty$-Lie algebras {#StrucLieAlg}

(...)


### Maurer-Cartan forms and curvature characteristic forms {#StrucCurvatureForms}

(...)

### Differential cohomology {#StrucDifferentialCohomology}

(...)


### Chern-Weil homomorphism and $\infty$-connections {#StrucChernWeil}

(...)

### Higher holonomy and Chern-Simons functional {#StrucChernSimons}

(...)

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * **synthetic differential ∞-groupoid**
## References

The $(\infty,1)$-topos $SynthDiff\infty Grpd$ is discussed in  section 3.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

The site [[CartSp]]${}_{synthdiff}$ is discussed in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).

The infinitesimal path $\infty$-groupoid adjunction $(\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ is discussed at the level of [[homotopy categories]] in section 3 of 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))


[[!redirects synthetic differential ∞-groupoid]]

[[!redirects SynthDiff∞Grpd]]