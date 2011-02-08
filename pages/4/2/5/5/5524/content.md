
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

### Cohesion

+-- {: .un_prop}
###### Proposition

$SynthDiff \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]]. See there for details.

=--

+-- {: .un_def}
###### Definition

Write $FSmoothMfd \hookrightarrow SmoothAlg^{op}$ for the [[full subcategory]] of [[smooth loci]] on the 
 **[[formal smooth manifold]]s**: those modeled on [[CartSp]]${}_{synthdiff}$ equipped with the evident [[coverage]].

=--

+-- {: .un_prop #CartSpAsDenseSubOfFSmoothMfd}
###### Observation

$CartSp_{synthdiff}$ is a [[dense sub-site]] of $FSmoothMfd$.

=--

+-- {: .un_prop #EquivalenceToToposOverSoothSynthMfd}
###### Proposition

There is an [[equivalence of (∞,1)-categories]]

$$
  SynthDiff\infty Grpd \simeq \hat Sh_{(\infty,1)}(FSmoothMfd)
$$

with the [[hypercomplete (∞,1)-topos]] over $FSmoothMfd$.

=--

+-- {: .proof}
###### Proof

With the [above observation](#CartSpAsDenseSubOfFSmoothMfd) this is directly analogous to the corresponding proof at [[ETop∞Grpd]]. 

=--



### Infinitesimal cohesion

+-- {: .un_def}
###### Definition

Write $i : CartSp_{smooth} \hookrightarrow CartSp_{synthdiff}$ for the canonical [[full subcategory|embedding]].

=--


+-- {: .un_prop #CohesivenessUnderSmoothInfGrpd}
###### Proposition

The functor $i^*$ given by restriction along $i$ exhibits 
$SynthDiff\infty Grpd$ as an 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#LieTheory">infinitesimal cohesive neighbourhood</a>
of the [[(∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoid]]s in that we have a quadruple of [[adjoint (∞,1)-functor]]s

$$
 ( i_! \dashv i^* \dashv i_* \dashv i^! )
  :
  Smooth \infty Grpd
  \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\to}}{\stackrel{i^!}{\leftarrow}}}}
  SynthDiff \infty Grpd
  \,,
$$

such that $i_!$ is a [[full and faithful (∞,1)-functor]].

=--



+-- {: .proof}
###### Proof

We [[presentable (∞,1)-category|present]] the [[(∞,1)-category]] $SynthDiff \infty Grpd$ by the [[model structure on simplicial presheaves]] [[Bousfield localization of model categories|left Bousfield localized]] at the [[covering]] [[sieve]] inclusions 

$$
  Sh_{(\infty,1)}(CartSp_{synthdiff}) \simeq
  ([CartSp_{synthdiff}^{op}, sSet]_{loc})^\circ
$$

(as discussed at [[models for ∞-stack (∞,1)-toposes|models for (∞,1)-sheaf (∞,1)-toposes]]).


Notice that the functor $i$ has a [[right adjoint]] given by

$$
  p : (K \times D) \mapsto D
  \,,
$$

that exhibits a [[coreflective subcategory]]

$$
  (i \dashv p) : CartSp_{synthdiff}
    \stackrel{\overset{i}{\leftarrow}}{\underset{p}{\to}}
   CartSp_{smooth}
  \,.
$$


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

where the [[limit]]s are over the [[opposite category|opposite]] [[comma categories]] $(i/(K \times D))^{op}$ and $(Id_{CartSp_{smooth}}/K)^{op}$, respectively, and where we are using in the first step that there is a unique terminal morphism from $K \in CartSp_{smooth}$ to the [[infinitesimally thickened point]] $D$ and in the second step the [[Yoneda reduction]]-form of the [[Yoneda lemma]]. The rest is notation.

This shows that the right adjoint to $(-)\circ i$ is itself given by precomposition with a functor, and hence has itself a further right adjoint, which gives us a total of four [[adjoint functor]]s

$$
  [CartSp_{smooth}^{op}, sSet]  
    \stackrel{\overset{Lan_i}{\to}}{\stackrel{\overset{(-)\circ i}{\leftarrow}}{\stackrel{\overset{(-)\circ p}{\to}}{\underset{Ran_p}{\leftarrow}}}}
  [CartSp_{synthdiff}^{op}, sSet]
  \,.
$$


From this are directly induced the corresponding [[simplicial Quillen adjunction]]s on the global projective and injective [[model structure on simplicial presheaves]]

$$
  (Lan_i \dashv (-) \circ i) : 
  [CartSp_{smooth}^{op}, sSet]_{proj}
   \stackrel{\overset{Lan_i}{\to}}{\underset{(-)\circ i}{\leftarrow}}
  [CartSp_{synthdiff}^{op}, sSet]_{proj}
  \,;
$$

$$
  ((-)\circ i \dashv (-) \circ p) : 
  [CartSp_{smooth}^{op}, sSet]_{proj}
   \stackrel{\overset{(-)\circ i}{\leftarrow}}
    {\underset{(-)\circ p}{\to}}
  [CartSp_{synthdiff}^{op}, sSet]_{proj}
  \,;
$$

$$
  ((-) \circ p \dashv Ran_p) : 
  [CartSp_{smooth}^{op}, sSet]_{inj}
   \stackrel{\overset{(-)\circ p}{\to}}{\underset{Ran_p}{\leftarrow}}
  [CartSp_{synthdiff}^{op}, sSet]_{inj}
  \,.
$$



By the discussion at [[simplicial Quillen adjunction]] for these Quillen adjunctions to descent to the Cech-local [[model structure on simplicial presheaves]] it suffices that the [[right adjoint]]s preserve locally fibrant objects. 
Moeover, by the properties of [[Bousfield localization of model categories|left Bousfield localization]] this in turn is implied if  the [[left adjoint]]s preserve [[covering]]s. 

It is directly see that $(-) \circ i$ prserves fibrant objects, as it just restricts these to fewer objects and hence a subset of covers. That $(-) \circ i$ also preserves covers follows from observing that

$$
  (-) \circ i : \{U_i \times D \stackrel{(f_i,Id_D)}{\to} U \times D\}
    \mapsto
      \{U_i \stackrel{f_i}{\to} U\}
   \,.
$$

Therefore $(-) \circ i$ is a left and right local Quillen functor with left local Quillen adjoint $Lan_i$ and right local Quillenadjoint $(-)\circ p$.


It follows that $i^* : SynthDiff \infty Grpd \to Smooth \infty Grpd$ is given by the left [[derived functor]] of restriction along $i$, and 
$i_* : Smooth \infty Grpd \to SynthDiff \infty Grpd$ is given by the right [[derived functor]] of restriction along $p$. 

Finally to see that $(-) \circ p$ preserves covers notice that for every covering family $\{U_i \to U\}$ in $CartSp_{smooth}$ and every morphism $K \times D \to p^* U$ in $CartSp_{synthdiff}$ we may find a covering $\{K_{j} \times D \to K \times D\}$ of $K \times D$ such that we find commuting diagrams on the left of

$$
  \array{
    K_j \times D &\to& p^* U_{i(j)}
    \\
    \downarrow && \downarrow
    \\
    K \times D &\to& p^* U
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    K_j & =&  i^*(K_j \times D) &\to&  U_{i(j)}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    K &= & i^*(K \times D= &\to&  U
  }
  \,,
$$

because by adjunction these correspond to commuting diagrams as indicated on the right, which exist by definition of [[coverage]] on $CartSp_{smooth}$.

This implies that $\{p^* U_i \to p^* U\}$ is a _generalized cover_ in the terminology at [[model structure on simplicial presheaves]], which by the discussion there implies that the corresponding [[Cech nerve]] equivalent to the [[sieve]] inclusion is a weak equivalence.

This establishes the quadruple of [[adjoint (∞,1)-functor]]s as claimed.

It remains to see that $i_!$ is full and faithful and preserves the terminal object. 

For the first statement notice the general fact that left 
[[Kan extension]] (see the propeties discussed there) along a [[full and faithful functor]] $i$ satisfies $Lan_i \circ i \simeq id$. It remains to observe that since $(-)\circ i$ is not only right but also left Quillen by the above, we have that $i^* Lan_i$ applied to a cofibrant object is already the [[derived functor]] of the composite.

For the second statement, notice that the point, being representable is cofibrant in $[CartSp_{smooth}, sSet]_{proj,loc}$. Therefore we may compute 
the [[derived functor]] $i_!(*)$ as the ordinary left [[Kan extension]] $Lan_i(*)$. The [[coend]] formula gives on any $K \times D \in CartSp_{synthdiff}$

$$
  \begin{aligned}
    (Lan_i *) : K \times D & \mapsto 
     \int^{U \in CartSp_{smooth}}
      CartSp_{synthdiff}(K \times D, U) \cdot
       CartSp_{smooth}(U,*)
      \\
      & \simeq 
      {\lim_\to}_{U \in CartSp_{smooth}} 
       CartSp_{synthdiff}(K \times D , U)
      \\
      & \simeq *
  \end{aligned}
  \,,
$$

where the last step follows since we have a [[colimit]] over a category with a [[terminal object]].



=--


+-- {: .un_remark}
###### Remark

Conversely this implies that $SynthDiff\infty Grpd$ is a [[strongly ∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]], exhibited by the triple of adjunctions

$$
  (i^* \dashv i_* \dashv i^!) : 
  SynthDiff \infty Grpd \to Smooth \infty Grpd
  \,.
$$


=--


## Structures

We discuss the realization of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> in $SynthDiff \infty Grpd$.

Since by the [above discussion](#RelativeInftyConnectedness) $SynthDiff\infty Grpd$ is strongly $\infty$-connected _relative_ to [[Smooth∞Grpd]] all of these structures that depend only on $\infty$-connectedness (and not on [[local (∞,1)-topos|locality]]) acquire a relative version.


### Cohomology and principal $\infty$-bundles {#StrucCohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Cohomology">intrinsic cohomology in a cohesive (∞,1)-topos</a> realized in $SynthDiff∞Grpd$.

+-- {: .un_prop}
###### Observation

The canonical [[line object]] of the [[Lawvere theory]] [[CartSp]]${}_{smooth}$ is the [[real line]], regarded as
an object of the [[Cahiers topos]], and hence of
$SynthDiff \infty Grpd$

$$
  \mathbb{A}^1_{CartSp_{smooth}} = \mathbb{R}
  \,.
$$ 

=--

We shall write $\mathbb{R}$ also for the underlying 
additive group

$$
  \mathbb{G}_a = \mathbb{R}
$$

regarded as an abelian [[∞-group]] object in
$SynthDiff\infty Grpd$. For $n \in \mathbb{N}$ write
$\mathbf{B}^n \mathbb{R} \in SynthDiff\infty Grpd$ 
for its $n$-fold [[delooping]].

For $n \in \mathbb{N}$ and $X \in SynthDiff\infty Grpd$ 
write 

$$
  H^n_{synthdiff}(X) := \pi_0 SynthDiff\infty Grpd(X,\mathbf{B}^n \mathbb{R})
$$

for the [[cohomology group]] of $X$ with coefficients in the canonical line object in degree $n$.

+-- {: .un_def}
###### Definition

Write

$$
  \mathbf{L}_{sdiff} \hookrightarrow SynthDiff \infty Grpd
$$

for the [[cohomology localization]] of $SynthDiff\infty Grpd$ at $\mathbb{R}$-[[cohomology]]: the full [[sub-(∞,1)-category]] on the $W$-[[local object]] with respect to the [[class]] $W$ of [[morphism]]s that induce [[isomorphism]]s in all $\mathbb{R}$-cohomology groups.

=--

+-- {: .un_prop}
###### Proposition

Let $SmoothAlg^{\Delta}_{proj}$ be the [[model structure on cosimplicial algebras|projective model structure on cosimplicial smooth algebras]] and let $j : (SmoothAlg^{\Delta})^{op} \to [CartSp_{synthdiff}, sSet]$ be the prolonged external [[Yoneda embedding]]. 

1. This constitutes the [[right adjoint]] of a [[Quillen adjunction]]
 
   $$
    (\mathcal{O} \dashv j) 
    :  
     (SmoothAlg^\Delta)^{op}
     \stackrel{\overset{\mathcal{O}}{\leftarrow}}{\underset{j}{\to}}
     [FSmoothMfd^{op}, sSet]_{proj,loc}
     \,.
   $$

1. Restricted to [[simplicial object|simplicial]] [[formal smooth manifold]]s along

   $$
      FSmoothMfd^{\Delta^{op}}
      \hookrightarrow
      (SmoothAlg^\Delta)^{op}
   $$

   the right [[derived functor]] of $j$ is a [[full and faithful (∞,1)-functor]] that factors through the [[cohomology localization]] and thus identifies a full [[reflective sub-(∞,1)-category]]

   $$
     (FSmoothMfd^{\Delta^{op}})^\circ
     \hookrightarrow
     \mathbf{L}_{sdiff}
     \hookrightarrow
     SynthDiff\infty Grpd
   $$


1. The intrinsic $\mathbb{R}$-cohomology of any object $X \in SynthDiff\infty Grpd$ is computed by the ordinary [[cochain cohomology]] of the [[Moore complex|Moore cochain complex]] underlying the cosimplicial abelian group $\mathcal{O}(X)$ under the [[Dold-Kan correspondence]]:

   $$
      H_{synthdiff}^n(X) 
       \simeq 
      H^n_{cochain}(N^\bullet\mathcal{O}(X))
      \,.
   $$

=--

+-- {: .proof}
###### Proof

First a remark on the sites. By the [above proposition](#EquivalenceToToposOverSoothSynthMfd)
$SynthDiff\infty Grpd$ is equivalent to the [[hypercomplete (∞,1)-topos]] over [[formal smooth manifold]]s. This is [[presentable (∞,1)-category|presented]] by the [[nLab:Bousfield localization of model categories|left Bousfield localization]] of $[FSmoothMfd^{op}, sSet]_{proj,loc}$ at the [[∞-connected]] morphisms. But a fibrant object in $[FSmoothMfd^{op}, sSet]_{proj,loc}$ that is also [[n-truncated]] for form $n \in \mathbb{N}$ is also fibrant in the hyperlocalization (only for the untruncated object there is an additional condition). Therefore the right Quillen functor claimed above indeed lands in truncated objects in $SynthDiff \inftyGrpd$.

The proof of the above statements is given in ([Stel](#Stel)), following ([To&#235;n](#Toen)). Some details are spelled out at 
[[function algebras on ∞-stacks]].


=--

### Flat differential cohomology and local systems 
  {#StrucFlat}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat differential cohomology</a> in any [[cohesive (∞,1)-topos]] realized in $SynthDiff∞Grpd$.

+-- {: .un_prop}
###### Proposition

For all $n \in \mathbb{N}$ we have an [[equivalence in an (∞,1)-category|equivalence]]

$$
  \mathbf{\flat}_{inf} \mathbf{B}^n \magthbb{R}
   \simeq
  \mathbf{\flat} \mathbf{B}^n \mathbb{R}
$$

between the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#StrucInfinitesimalLocalSystem">infinitesimal flat coefficients</a> and genuine <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">flat coefficients</a>

=--


+-- {: .proof}
###### Proof

We present the situation in the local [[model structure on simplicial presheaves]] $[CartSp_{synthdiff}, sSet]_{proj,loc}$.

By the general discussion at [[∞-cohesive site]] and specifically the discussion of <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#FlatCoefficientsForCircleNGroup">flat differential coefficient objects</a> in [[Smooth∞Grpd]] we have that $\mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}$ is presented by the constant simplicial presheaf

$$
  \mathbf{\flat}_{dR}\mathbf{B}^n \mathbb{R}_c
  U \mapsto
  \Xi \mathbb{R}[n]  
  \,,
$$

where $\mathbb{R}[n]$ is the [[chain complex]] concentrated on the [[abelian group]] or [[real number]]s in degree $n$ and  $\Xi : Ch_\bullet^+ \to sAb \to sSet$ is the [[Dold-Kan correspondence]].

This is a fibrant object in $[CartSp_{synthdiff}, sSet]_{proj,loc}$ (for instance since the constant presheaf functor of which $Disc_{\mathbf{H}_{th}}$ is the right [[derived functor]] is a right [[Quillen adjunction|Quillen functor]]).

We now similarly construct a fibrant presentation for $\mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R}$.

For $U \times D \in CartSp_{synthdiff}$, let 

$$
  (U \times D)^{(\Delta^n_{inf})} \in
  [CartSp_{synthdiff}, Set]
  \hookrightarrow
  [CartSp_{synthdiff}, sSet]
$$

be the [[smooth locus]] of <a href="http://nlab.mathforge.org/nlab/show/infinitesimal%20object#SpacOfInfSimpl">infinitesimal n-simplices</a>. Notice that this is not an [[internal hom]] with an [[infinitesimal object]]. Instead, due to the [[Cartesian space]] nature of $U$, this is of the simple form

$$
  (U \times D)^{(\Delta^n_{inf})}
  \simeq
  U \times D \times \tilde D(dim(U)+ dim(D),n)
$$

where $\tilde D(-,-)$ is the [[infinitesimal object|infinitesimal smooth locus]] discussed <a href="http://nlab.mathforge.org/nlab/show/infinitesimal%20object#SpacOfInfSimpl">here</a>. 
(See [Kock](#Kock), and [Stel](#Stel)).

This means that the simplicial presheaf

$$
  (U \times D)^{(\Delta^\bullet_{inf})}
  = 
  \int^{[k] \in \Delta}
    \Delta[k] \cdot (U \times D \times \tilde D(...,k))
  \in
  [CartSp_{synthdiff}, sSet]_{proj,loc}
$$

is degreewise cofibrant. Using the left [[Quillen bifunctor]] (see the discussion there)

$$
  \int^{\Delta} (-)\cdot (-)
  : 
  [\Delta, sSet_{Quillen}]_{proj}
  \times
  [\Delta^{op}, [CartSp_{synthdiff}, sSet]_{proj,loc}]_{inj}
  \to 
  [CartSp_{synthdiff}, sSet]_{proj,loc}
$$

and the fact that the [[fat simplex]] is (as discussed there) a cofibrant resolution of the [[simplex]] in $[\Delta, sSet_{Quillen}]_{proj}$, we have that 

$$
  \mathbf{\Pi}_{inf}(U\times D)_{c}
  :=
  \int^{[k] \in \Delta}
    \mathbf{\Delta}[k] \cdot (U \times D \times \tilde D(...,k))
$$

is cofibrant for all $U \times D \in CartSp_{synthdiff}$. Moreover (by the discussion at [[Reedy model structure]] and [[Bousfield-Kan map]]) it is weakly equivalent to $(U \times D)^{(\Delta^\bullet_k)}$. Notice that this extends to a functor

$$
  \mathbf{\Pi}_{inf}(-)_c :
  CartSp_{synthdiff}
  \to 
  [CartSp_{synthdiff}^{op}, sSet]
  \,.
$$

Then using the left [[Quillen bifunctor]]

$$
  \int^{CartSp_{synthdiff}} (-)\cdot (-)
  : 
  [CartSp_{synthdiff}^{op}, sSet_{Quillen}]_{proj}
  \times
  [CartSp_{synthdiff}, [CartSp_{synthdiff}^{op}, sSet]_{proj,loc}]_{inj}
  \to 
  [CartSp_{synthdiff}, sSet]_{proj,loc}
$$



We claim now that the left [[derived fuctor]] of this left Quillen functor is equivalent to $\mathbf{\Pi}_{inf}$

=--


### Geometric homotopy and Galois theory {#StrucGeometricHomotopy} 

Regarding $SynthDiff  \infty Grpd$ as being a [[strongly ∞-connected (∞,1)-topos]] over [[Smooth∞Grpd]] by the [above discussion](#RelativeInftyConnectedness) we write


$$
  (\Pi_{inf} \dashv Disc_{inf} \dashv \Gamma_{inf})
  :=
  (i^* \dashv i_* \dashv i^!)
  : 
  SynthDiff\infty Grpd
    \stackrel{\overset{\Pi_{inf}}{\to}}{\stackrel{\overset{Disc_{inf}}{\leftarrow}}{\underset{\Gamma_{inf}}{\to}}}
  Smooth \infty Grpd
$$

for the corresponding relative [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]].


### Paths and geometric Postnikov towers {#StrucPaths}

+-- {: .un_def}
###### Definition

The **infinitesimal path $\infty$-functor** is the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Paths">intrinsic path ∞-groupoid</a> for the _[relative](#RelativeInftyConnectedness)_ [[strongly ∞-connected (∞,1)-topos|strongly ∞-connected structure]] $\Pi_{inf} : SynthDiff \infty Grpd \to Smooth\infty Grpd$:

$$
  (\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf}) 
   :=
  (i \circ \Pi_{inf} \dashv Disc_{inf} \Pi_{inf} \dashv Disc_{inf} \circ \Gamma_{inf})
  :
  SynthDiff \infty Grpd
  \to 
  SynthDiff \infty Grpd
  \,.
$$

=--


+-- {: .un_prop}
###### Observation

For $U \times D \in CartSp_{synthdiff} \hookrightarrow SynthDiff\infty Grpd$
we have that

$$
  \mathbf{Red}(K \times D) \simeq U
$$

is the **reduced smooth locus** the formal dual of the [[smooth algebra]] obtained by quotienting out all nilpotent elements in the [[smooth algebra]] $C^\infty(K \times D) \simeq C^\infty(K) \otimes C^\infty(D)$.

=--

+-- {: .proof}
###### Proof

By the [[model category]] presentation of $\mathbf{Red} = i \circ \Pi_{inf} = i_! \circ i^*$ of the [above proof](#CohesivenessUnderSmoothInfGrpd) and using that every [[representable functor|representable]] is cofibrant and fibrant in the local projective [[model structure on simplicial presheaves]] we have

$$
  \begin{aligned}
    \mathbf{Red}(U \times D)
    & 
    \simeq
     (\mathbb{L}i_!) (\mathbb{R}i^*) (U \times D)
    \\
     &\simeq
     (\mathbb{L}i_!) i^* (U \times D)
     \\
     & \simeq
     (\mathbb{L}i_!) U
     \\
     & \simeq
     i_! U
     \\
    & \simeq U
  \end{aligned}
  \,.
$$

=--

+-- {: .un_prop}
###### Corollary


For $X \in SmoothAlg^{op}  \to SynthDiff \infty Grpd$ a [[smooth locus]], we have that $\mathbf{\Pi}_{inf}(X)$ is the corresponding [[de Rham space]], the [[∞-stack]] on $CartSp_{synthdiff}$ in which all [[infinitesimal object|infinitesimal]] neighbour points in $X$ are equivalent: given by the assignment

$$
  \mathbf{\Pi}_{inf}(X) : U \times D \mapsto X(U)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf})$-adjunction relation

$$
  \begin{aligned}
    \mathbf{\Pi}_{inf}(X)(U \times D)
    & =
    SynthDiff \infty Grpd(U \times D, \mathbf{\Pi}_{inf}(X))
    \\
    & \simeq 
    SynthDiff \infty Grpd( \mathbf{Red}(U \times D), X)
    \\
    & \simeq
     SynthDiff \infty Grpd( U, X )
  \end{aligned}
  \,.
$$
=--

### Infinitesimal cohesion, $\infty$-Lie algebras and deformation theory {#StrucLieTheory}

An [[∞-Lie algebra]] is indeed an infinitesimal object in $SynthDiff\infty Grpd$. See [[∞-Lie algebroid]] for details for the moment.




## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * **synthetic differential ∞-groupoid**

## References

The site [[CartSp]]${}_{synthdiff}$ is discussed in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ , Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).

The [infinitesimal path ∞-groupoid adjunction](#StrucPaths) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ is discussed at the level of [[homotopy categories]] in section 3 of 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

The $(\infty,1)$-topos $SynthDiff\infty Grpd$ is discussed in  section 3.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

The [[cohomology localization]] of $SynthDiff\infty Grpd$ and the infinitesimal singular simplicial complex as a presentation for infinitesimal paths objects in $SynthDiff\infty Grpd$ is discussed in

* [[Herman Stel]], _$\infty$-Stacks and their function algebras -- with applications to $\infty$-Lie theory_ , master thesis (2010) ([[schreiber:master thesis Stel|web]])
{#Stel}

The discussion of the cohomology localization of $SynthDiff\infty Grpd$ follows that in another context in

* [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

The construction of the infinitesimal path object has been amplified and discussed by [[Anders Kock]] under the name [[combinatorial differential forms]], for instance in

*  [[Anders Kock]], _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))


[[!redirects synthetic differential ∞-groupoid]]
[[!redirects synthetic differential ∞-groupoids]]


[[!redirects SynthDiff∞Grpd]]