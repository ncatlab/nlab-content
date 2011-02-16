
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

Since $i : CartSp_{smooth} \hookrightarrow CartSp_{synthdiff}$ is an <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalNeighBourhoodSite">infinitesimally ∞-cohesive site</a> this follows with <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#InfinitesimalNeighbourhoodFromInfinitesimalSite">a proposition</a> discussed at [[cohesive (∞,1)-topos]].

=--


## Structures

We discuss the realization of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> in $SynthDiff \infty Grpd$.

Since by the [above discussion](#RelativeInftyConnectedness) $SynthDiff\infty Grpd$ is strongly $\infty$-connected _relative_ to [[Smooth∞Grpd]] all of these structures that depend only on $\infty$-connectedness (and not on [[local (∞,1)-topos|locality]]) acquire a relative version.


### Cohomology and principal $\infty$-bundles {#StrucCohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Cohomology">intrinsic cohomology in a cohesive (∞,1)-topos</a> realized in $SynthDiff\infty Grpd$.

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

+-- {: .un_prop #PresentationOfCohomologyLocalization}
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


1. The intrinsic $\mathbb{R}$-cohomology of any object $X \in SynthDiff\infty Grpd$ is computed by the ordinary [[cochain cohomology]] of the [[Moore complex|Moore cochain complex]] underlying the cosimplicial abelian group of the image under the left [[derived functor]]$(\mathbb{L}\mathcal{O})(X)$ under the [[Dold-Kan correspondence]]:

   $$
      H_{synthdiff}^n(X) 
       \simeq 
      H^n_{cochain}(N^\bullet(\mathbb{L}\mathcal{O})(X))
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

+-- {: .un_prop #RealCohomologyOfCompactLieGroup}
###### Proposition

Let $G \in SmoothMfd \hookrightarrow Smooth\infty Grpd \hookrightarrow SynthDiff\infty Grpd $ be a [[Lie group]]. 

Then the intrinsic group cohomology in [[Smooth∞Grpd]] and in $SynthDiff\infty Grpd$ of $G$ with coefficients in $\mathbb{R}$ coincides with [[Graeme Segal|Segal]]'s refined [[Lie group cohomology]] ([Segal](#Segal), [Brylinski](#Brylinski)).

$$
  H^n_{smooth}(\mathbf{B}G, \mathbb{R})
  \simeq
  H^n_{synthdiff}(\mathbf{B}G, \mathbb{R})
  \simeq
  H^n_{Segal}(G,\mathbb{R})
  \,.
$$


=--

+-- {: .proof}
###### Proof

We show the equivalence 
$H_{synthdiff}^n(\mathbf{B}G, \mathbb{R})\simeq H_{Segal}^n(G,\mathbb{R})$
by demonstrating that there is a component-formula that expresses $H^n_{synthdiff}(\mathbf{B}G, \mathbb{R})$ which coincides with a formula known to descibe [[Graeme Segal|Segal]]-Blanc-[[Jean-Luc Brylinski|Brylinski]]'s refined [[Lie group cohomology]] -- _<a href="http://nlab.mathforge.org/nlab/show/Lie+group+cohomology#definition_11">differential group cohomology</a>_ $H^n_{diffgrp}(G, \mathbb{R})$ .

The further equivalence

$$
  H_{smooth}^n(\mathbf{B}G, \mathbb{R})
  \simeq
  H_{synthdiff}^n(\mathbf{B}G, \mathbb{R})
$$

holds because the embeddding $i_! : Smooth\infty Grpd \hookrightarrow SynthDiff\infty Grpd$ is a [[full and faithful (∞,1)-functor]] and because by the [above proposition](#EmbeddingOfSmoothRepresentables) it sends $\mathbb{R} \in Smooth\infty Grpd$ to $\mathbb{R} \in SynthDiff\infty Grpd$.

To see the first equivalence, let $\mathbf{B}G_c \in [\Delta^{op}, [CartSp_{synthdiff}^{op}, Set]] = [CartSp_{sythdiff}^{op}, sSet]$ be the standard presentation of $\mathbf{B}G \in SynthDiff\infty Grpd$ by the [[nerve]] of the [[Lie groupoid]] $(G \stackrel{\to}{\to} *)$ (as discussed <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#LieGroups">here</a>). We may write this as

$$
  \mathbf{B}G_c = \int^{[k] \in \Delta} \Delta[k] \cdot G^{\times_k}
  \,.
$$

Similarly let $\mathbf{B}^n \mathbb{R}_{chn} \in [CartSp_{synthdiff}^{op}, sSet]$ be the standard presentation of $\mathbf{B}^n \mathbb{R} \in SynthDiff\infty Grpd$. By the discussion <a href="http://ncatlab.org/nlab/show/smooth+infinity-groupoid#CircleLienGroup">here</a> this is fibrant in $[CartSp_{synthdiff}^{op}, sSet]_{proj,loc}$. Therefore in order to compute the [[derived hom-space]] from $\mathbf{B}G_c$ to $\mathbf{B}^n \mathbb{R}_{chn}$ we need to consider a cofibrant replacement of $Q\mathbf{B}G_c \stackrel{\simeq}{\to} \mathbf{B}G_c$. We shall now find such and then use the [above proposition](#PresentationOfCohomologyLocalization) to conclude that the $\mathbb{R}$-cohomology in question is the [[cochain cohomology]] of the [[Moore complex|cochain complex]] of the [[cosimplicial object|cosimplicial]] algebra $\mathcal{O}Q\mathbf{B}G_c$.


We may always choose for each $k \in \mathbb{N}$ a [[good open cover]] $\{U_i^{(k)} \to G^{\times_k}\}_{i \in I_k}$ in a way that is compatible with the face an degeneracy maps in $\mathbf{B}G_c$, in the sense that

* the index sets arrange themselves into a [[simplicial set]]
  $I : [k] \mapsto I_k$;

* and for $d_j(U^k_i)$ and $s_j(U^k_i)$ the images of the
  face and degeneracy maps of $G^{\times\bullet}$ we have

  $$
    d_j(U^k_i) \subset U^{k-1}_{d_j(i)}
  $$ 

  and

  $$
    s_j(U^k_i) \subset U^{k+1}_{s_j(i)}
    \,.
  $$

For instance start with a [[good open cover]] $\{U^1_i \to G\}$ and define a good open cover $\{U^2_{i_0 i_1 i_2}\}$ of $G \times G$ by $U^2_{i_0 i_1 i_2} := d_0^* U^1_{i_0} \cap d_1^* U^1_{i_1} \cap d_2^* U^1_{i_2}$. And so on.

By the discussion at [[Smooth∞Grpd]] for each $k$ the [[Cech nerve]] projection $C(\{U_i^{(k)}\}_i) \to G^{\times_k}$ is a cofibrant [[resolution]] in $[CartSp_{synthdiff}^{op}, sSet]_{proj,loc}$. Accordingly the morphism

$$
  \int^{[k] \in \Delta}
    \Delta[k] \cdot C(\{U_i^{(k)}\}_i)
  \stackrel{\simeq}{\to} 
  \int^{[k] \in \Delta}
    \Delta[k] \cdot G^{\times_k}
  = 
  \mathbf{B}G_{c}  
$$

exists and is a weak equivalence in $[CartSp^{op}_{synthdiff}, sSet]_{inj}$, hence in $[CartSp_{synthdiff}, sSet]_{proj}$, hence in $[CartSp_{synthdiff}, sSet]_{proj,loc}$, because

1. $\Delta \in [\Delta, sSet_{Quillen}]_{Reedy}$ is cofibrant in the [[Reedy model structure]] (see there);

1. every simplicial object in simplicial presheaves is cofibrant in $[\Delta^{op}, [CartSp_{synthdiff}^{op}, sSet]_{inj}]_{Reedy}$

1. the [[coend]] over the tensoring

   $$
     \int^\Delta \;:\; [\Delta, sSet_{Quillen}]_{Reedy} \times
      [\Delta^{op}, [CartSp_{synthdiff}^{op}, sSet]_{inj}]_{Reedy}
     \to
      [CartSp_{synthdiff}^{op}, sSet]_{inj}
   $$

   is a left [[Quillen bifunctor]] (as discussed there)

To make it a total cofibrant resolution we can further pull back along the [[fat simplex]] projection $\mathbf{\Delta} \to \Delta$ to obtain a weak equivalence

$$
  Q \mathbf{B}G_c
   :=
  \int^{[k] \in \Delta}
    \mathbf{\Delta}[k] \cdot C(\{U_i^{(k)}\}_i)
  \stackrel{\simeq}{\to} 
  \mathbf{B}G_{c}  
$$

where we are using again the left [[Quillen bifunctor]] property and the fact that $\mathbf{\Delta} \to \Delta$ is a weak equivalence between cofibrant objects in $[\Delta, sSet]_{Reedy}$. Finally that this is indeed cofibrant follows from

1. the left [[Quillen bifunctor]] property of

   $$
     \int^\Delta [\Delta, sSet_{Quillen}]_{proj} \times
      [\Delta^{op}, [CartSp_{synthdiff}^{op}, sSet]_{proj}]_{inj}
     \to
      [CartSp_{synthdiff}^{op}, sSet]_{proj}
   $$

1. the fact that the [[fat simplex]] is cofibrant $\emptyset \hookrightarrow \mathbf{\Delta}$ in $[\Delta, sSet]_{proj}$.

Observe that the functor 

$$
  [\Delta^{op}, \mathcal{O}] : 
  [\Delta^{op}, [CartSp_{synthdiff}^{op}, sSet]_{proj,loc}]
  \to
  [\Delta^{op}, SmoothAlg^{op}]
$$

preserves [[Reedy model structure|Reedy cofibrant]] objects because the left [[Quillen adjunction|Quillen functor]] $\mathcal{O}$ preserves [[colimit]]s and cofibrations and hence the property that the morphisms $L_k X \to X_k$ out of latching objects ${\lim_\to}_{s \stackrel{+}{\to} k} X_s$ are cofibrations.

Therefore we may again apply the [[Bousfield-Kan map]] after application of $\mathcal{O}$ to find that there is a weak equivalence

$$
  \mathcal{O}\mathbf{Q} \mathbf{B}G_c
  =
  \int^{[k] \in \Delta}
    \mathbf{\Delta}[k] \cdot \mathcal{O}((C(\{U_i^{(k)}\}_i))
    \simeq
  \int^{[k] \in \Delta}
    \Delta[k] \cdot \mathcal{O}((C(\{U_i^{(k)}\}_i))
$$

in $(SmoothAlg^{\Delta})^{op}$ to the object where the [[fat simplex]] is replaced back with the ordinary [[simplex]]. Therefore by the [above proposition](#PresentationOfCohomologyLocalization) the 
$\mathbb{R}$-cohomology that we are after is equivalently computed as the [[cochain cohomology]] of the [[Moore complex|normalized cochain complex]] 

$$
  N^\bullet
    \mathcal{O}
    (
    \int^{[k] \in \Delta}
   \Delta[k] \cdot ((C(\{U_i^{(k)}\}_i))
 )
$$

of the object on the right.
(In other words, for computing the $\mathbb{R}$-cohomology of $\mathbf{B}G$ it is sufficient to perform a degreewise cofibrant replacement and then apply $\mathcal{O}$; while the fully cofibrant replacement is not necessary. )

Observing that for $S_{\bullet,\bullet}$ a [[bisimplicial set]] (see there for details) we have that the [[coend]] $\int^{[k] \in \Delta} \Delta[k] \cdot S_{\bullet, k}$ is the diagonal simplicial set and then using the [[Eilenberg-Zilber theorem]] we have that this is the total complex of the Cech/group double comples of cochains with coefficients in $\mathbb{R}$. This is the formula for $H_{diffgrp}^n(G,\mathbb{R})$, as observed in ([Brylinski](#Brylinski)).


=--

+-- {: .un_prop }
###### Corollary

For $G$ a [[compact topological space|compact]] [[Lie group]] we have for all $n \geq 1$ that

$$
  H^n_{smooth}(G,U(1))
  \simeq H_{top}^{n+1}(B G, \mathbb{Z})
  \,.
$$

=--

+-- {: .proof}
###### Proof

This follows from applying the [above result](#RealCohomologyOfCompactLieGroup) to the [[fiber sequence]] induced by the sequence $\mathbb{Z} \to \mathbb{R} \to \mathbb{R}/\mathbb{Z} = U(1)$.

=--

+-- {: .un_remark }
###### Remark

This means that the intrinsic cohomology of [[compact topological space|compact]] [[Lie group]]s in [[Smooth∞Grpd]] and $SynthDiff\infty Grpd$ coincides for these coefficients with the Segal-Blanc-Brylinski refined Lie group cohomology ([Brylinski](#Brylinski)).

=--

### Paths and geometric Postnikov towers 
  {#StrucPaths}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Paths">intrinsic infinitesimal path adjunction</a> realized in $SynthDiff\infty Grpd$.

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

For $U \times D \in CartSp_{smooth} \ltimes InfinSmoothLoc = CartSp_{synthdiff} \hookrightarrow SynthDiff\infty Grpd$
we have that

$$
  \mathbf{Red}(U \times D) \simeq U
$$

is the **reduced [[smooth locus]]**: the [[Isbell duality|formal dual] of the [[smooth algebra]] obtained by quotienting out all nilpotent elements in the [[smooth algebra]] $C^\infty(K \times D) \simeq C^\infty(K) \otimes C^\infty(D)$.

=--

+-- {: .proof}
###### Proof

By the [[model category]] presentation of 
$\mathbf{Red} \simeq  \mathbb{L} Lan_i \circ \mathbb{R}i^*$ of the [above proof](#CohesivenessUnderSmoothInfGrpd) and using that every [[representable functor|representable]] is cofibrant and fibrant in the local projective [[model structure on simplicial presheaves]] we have

$$
  \begin{aligned}
    \mathbf{Red}(U \times D)
    & 
    \simeq
     (\mathbb{L}Lan_i) (\mathbb{R}i^*) (U \times D)
    \\
     &\simeq
     (\mathbb{L}Lan_i) i^* (U \times D)
     \\
     & \simeq
     (\mathbb{L} Lan_i) U
     \\
     & \simeq
     Lan_i U
     \\
    & \simeq U
  \end{aligned}
$$

(using that $i$ is a [[full and faithful functor]]).

=--

+-- {: .un_prop #PiInfYieldsDeRahmSpace}
###### Corollary


For $X \in SmoothAlg^{op}  \to SynthDiff \infty Grpd$ a [[smooth locus]], we have that $\mathbf{\Pi}_{inf}(X)$ is the corresponding [[de Rham space]], the object
in which all [[infinitesimal object|infinitesimal]] neighbour points in $X$ are equivalent, characterized by

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


### Flat differential cohomology and local systems 
  {#StrucFlat}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">intrinsic flat differential cohomology</a> in any [[cohesive (∞,1)-topos]] realized in $SynthDiff\infty Grpd$.

We state and demonstrate the generalization of the [[de Rham theorem]] from [[SmoothMfd]] to [[Smooth∞Grpd]] and $SynthDiff\infty Grpd$.

+-- {: .un_prop}
###### Proposition

For all $n \in \mathbb{N}$ we have an [[equivalence in an (∞,1)-category|equivalence]]

$$
  \mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R}
   \simeq
  \mathbf{\flat} \mathbf{B}^n \mathbb{R}
$$

between the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#StrucInfinitesimalLocalSystem">infinitesimal flat coefficients</a> and genuine <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#FlatDifferentialCohomology">flat coefficients</a> of $\mathbf{B}^n \mathbb{R}$.

=--


+-- {: .proof}
###### Proof

We present the situation in the local [[model structure on simplicial presheaves]] $[CartSp_{synthdiff}, sSet]_{proj,loc}$.

By the general discussion at [[∞-cohesive site]] and specifically the discussion of <a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#FlatCoefficientsForCircleNGroup">flat differential coefficient objects</a> in [[Smooth∞Grpd]] we have that $\mathbf{\flat}\mathbf{B}^n \mathbb{R}$ is presented by the constant simplicial presheaf

$$
  \mathbf{\flat}\mathbf{B}^n \mathbb{R}_c
  :
  U \mapsto
  \Xi \mathbb{R}[n]  
  \,,
$$

where $\mathbb{R}[n]$ is the [[chain complex]] concentrated on the [[abelian group]] or [[real number]]s in degree $n$ and  $\Xi : Ch_\bullet^+ \to sAb \to sSet$ is the [[Dold-Kan correspondence]].

This is a fibrant object in $[CartSp_{synthdiff}, sSet]_{proj,loc}$ (for instance since the constant presheaf functor of which $Disc$ is the right [[derived functor]] is a right [[Quillen adjunction|Quillen functor]]).

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
  [\Delta^{op}, [CartSp_{synthdiff}^{op}, sSet]_{proj}]_{inj}
  \to 
  [CartSp_{synthdiff}^{op}, sSet]_{proj}
$$

and the fact that the [[fat simplex]] is (as discussed there) a cofibrant resolution of the [[simplex]] in $[\Delta, sSet_{Quillen}]_{proj}$, we have that 

$$
  \mathbf{\Pi}_{inf}(U\times D)_{c}
  :=
  \int^{[k] \in \Delta}
    \mathbf{\Delta}[k] \cdot (U \times D \times \tilde D(...,k))
$$

is cofibrant for all $U \times D \in CartSp_{synthdiff}$. Moreover (by the discussion at [[Reedy model structure]] and [[Bousfield-Kan map]]) it is weakly equivalent to $(U \times D)^{(\Delta^k_{inf})}$. Notice that this construction extends to a functor

$$
  \mathbf{\Pi}_{inf}(-)_c :
  CartSp_{synthdiff}
  \to 
  [CartSp_{synthdiff}^{op}, sSet]
  \,.
$$

Then using the left [[Quillen bifunctor]] (see the discussion there)

$$
  \int^{CartSp_{synthdiff}} (-)\cdot (-)
  : 
  [CartSp_{synthdiff}^{op}, sSet_{Quillen}]_{proj}
  \times
  [CartSp_{synthdiff}, [CartSp_{synthdiff}^{op}, sSet]_{proj,loc}]_{inj}
  \to 
  [CartSp_{synthdiff}, sSet]_{proj,loc}
$$

we have that the [[Yoneda extension]] of $\mathbf{\Pi}_{inf}(-)_c$ (which we denote by the same symbol)

$$
  \mathbf{\Pi}_{inf}(-)_c
  :
  [CartSp_{synthdiff}^{op}, sSet]_{proj}
  \to 
  [CartSp_{synthdiff}^{op}, sSet]_{proj}
$$

given by

$$
  \mathbf{\Pi}_{inf}(-)_c : 
  X \mapsto
  \int^{(U \times D) \in CartSp_{synthdiff}} 
  X(U\times D) \cdot \mathbf{\Pi}_{inf}(U \times D)_c
$$

is the [[left adjoint]] of a [[simplicial Quillen adjunction]], whose [[right adjoint]] is 

$$
  \mathbf{\flat}_{inf}(-)_c : 
  [CartSp_{synthdiff}^{op}, sSet](\mathbf{\Pi}_{inf}(-)_c, -)
  \,.
$$

We now claim that this Quillen adjunction does descend to the local model structure and that the right [[derived functor]] of $\mathbf{\flat}_{inf}(-)_c$ is the infinitesimal flat coefficient functor $\mathbf{\flat}_{inf}$.

Both of these claims are consequences of the following observation:

for all $U\times D, U' \times D' \in CartSp_{synthdiff}$ we have a natural weak equivalence 

$$
  \mathbb{R}Hom_{glob}(U' \times D', \mathbf{\Pi}_{inf}(U \times D))
  \stackrel{\simeq}{\to}
  [CartSp_{synthdiff}, sSet](U' \times D', (U \times D)^{(\Delta^\bullet_{inf})}) 
  \simeq
  CartSp_{smooth}(U', U)
  \,.
$$

The first characterization of the [[derived hom-space]] follows from the fact that, by the above discussion, the object
$(U \times D)^{(\Delta^\bullet_{inf})}$ is a globally fibrant resolution of $\mathbf{\Pi}_{inf}(U \times D)_c$ and that every representable is cofibrant.

The second equivalence is conveniently seen by [[synthetic differential geometry|synthetic differential geometry]] reasoning: a morphism $D' \to (U \times D)^{(\Delta^\bullet_{inf})}$ is an infinitesimal blob of points in $U \times D$. But in the [[Kan complex]]
$(U \times D)^{(\Delta^\bullet_{inf})}$ all infinitesimal neighbour points are equivalent, by an essentially unique equivalence. (This is effectively the definition of this object.)

With the [above discussion](#PiInfYieldsDeRahmSpace) it follows first of all that the left [[derived functor]] of $\mathbf{\Pi}_{inf}(-)_c$  on [[(∞,1)-presheaves]] does coincide with $\mathbf{\Pi}_{inf}$ on representables in $CartSp_{synthdiff}$. 

Moreover, this means that it sends covers to generalized covers, by the argument for $p^*$ in the [above proof](#CohesivenessUnderSmoothInfGrpd). This means that $\mathbf{\flat}_{inf}(-)_c$ preserves locally fibrant objects. Since the [[model structure on simplicial presheaves]] is a [[left proper model category]] this is, by the discussion at  [[simplicial Quillen adjunction]], sufficient to deduce that we also have a local [[Quillen adjunction]]

$$
  (\mathbf{\Pi}(-)_c \dashv 
  \mathbf{\flat}(-)_c) : 
  [CartSp_{synthdiff}^{op}, sSet]_{proj,loc}
  \stackrel{\leftarrow}{\to}
  [CartSp_{synthdiff}^{op}, sSet]_{proj,loc}
$$

whose [[derived functor]]s are eqivalent to the [[adjoint (∞,1)-functor]]s $(\mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf}) : SynthDiff\infty Grpd \to SynthDiff \infty Grpd$.

Using this presentation we can now complete the argument that we have an [[equivalence in an (∞,1)-category|∞-equivalence]] $\mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R} \simeq \mathbf{\flat} \mathbf{B}^n \mathbb{R}$  by observing that we have a local weak equivalence $\mathbf{\flat}_{inf}\mathbf{B}^n \mathbb{R}_c \simeq \mathbf{\flat} \mathbf{B}^n \mathbb{R}_c$:

We may check this by checking it on all representables. 
By the [above proposition](#PresentationOfCohomologyLocalization) we have that 

$$
  \begin{aligned}
    \pi_n SynthDiff \infty Grpd(U\times D, \mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R})
     & \simeq
    \pi_n SynthDiff \infty Grpd(\mathbf{\Pi}_{inf}(U\times D), \mathbf{B}^n \mathbb{R})
    \\
    & \simeq
     H_{cochain}^n( N^\bullet (\mathbb{L}\mathcal{O})(\mathbf{\Pi}_{inf}(U \times D)))
   \\
    & \simeq 
     H_{cochain}^n( N^\bullet (\mathbb{L}\mathcal{O})( 
     (U \times D)^{(\Delta^\bullet_{inf})} ) )
  \end{aligned}
  \,.
$$

Here in the last step we used 

1. that $\mathbf{\Pi}_{inf}((U \times D)_c$ is cofibrant so that $\mathbb{L}\mathcal{O}$ applied to it is equivalently just $\mathcal{O}$ applied to it;

1. that every object in $SmoothAlg^{op}$ is cofibrant, so that we have a weak equivalence

   $$
    \begin{aligned}
      \mathcal{O} \mathbf{\Pi}_{inf}(U \times D)
      & \simeq
      \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathcal{O}((U \times D)^{(\Delta^k_{inf})})
      \\
      & \simeq
      \int^{[k] \in \Delta} \Delta[k] \cdot \mathcal{O}((U \times D)^{(\Delta^k_{inf})})
      \\
      & = 
      \mathcal{O}((U \times D)^{(\Delta^\bullet_{inf})})
    \end{aligned}
   $$

   in $SmoothAlg^{op}$.

As essentially observed and amplified by ([Kock](#Kock)) -- see the discussion in ([Stel](#Stel)) for our context -- we have for $X$ a [[smooth manifold]] an [[isomorphism]] of [[dg-algebra]]s

$$
  N^\bullet(\mathcal{O}(X^{(\Delta^\bullet_{inf})}))
    \simeq
  \Omega^\bullet(X) 
$$

with the [[de Rham complex]] on the right. In particular the cohomology on the left is [[de Rham cohomology]].

With this our statement is finally reduced to the ordinary [[de Rham theorem]]. In fact we only need to observe that it holds over [[Cartesian space]]s to complete our proof. 

=--

+-- {: .un_cor}
###### Corollary
**(de Rham theorem for smooth $\infty$-groupoids)**

Let $X \in SynthDiff \infty Grpd$ be any synthetic differential $\infty$-groupoid.

For all $n \in \mathbb{N}$ we have an equivalence of [[cocycle]]
[[∞-groupoid]]s

$$
  SynthDiff\infty Grpd(\mathbf{\Pi}_{inf}(X), \mathbf{B}^n \mathbb{R})
  \simeq
  SynthDiff\infty Grpd(\mathbf{\Pi}(X), \mathbf{B}^n \mathbb{R})
$$

and hence in particular [[isomorphism]]s in cohomology

$$
  H_{infflat}^n(X, \mathbb{R}) \simeq H_{flat}^n(X,\mathbb{R})
  \simeq
  H^n(|X|, \mathbb{R})
  \,,
$$

where on the right we have the [[ordinary cohomology]] of the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Paths">intrinsic geometric realization</a> $|X| \in Top$. 

Finally, for $n \geq 2$ and $X \in Smooth\infty Grpd$ this also coincides with the 
<a href="http://nlab.mathforge.org/nlab/show/smooth+infinity-groupoid#StrucDeRham">intrinsic smooth de Rham cohomology</a> of $X$

$$
  \cdots \simeq H^n_{dR}(X)
  \,.
$$

=--

Essentially this statement (in a slightly different context and on homotopy categories) is in ([SimpsonTeleman, section 3](#SimpsonTeleman)).


### $\infty$-Lie algebras and deformation theory   {#StrucLieTheory}

For the moment see [[infinity-Lie algebroid]] for more



## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * **synthetic differential ∞-groupoid**

## References

The site [[CartSp]]${}_{synthdiff}$ is discussed in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ , Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).

The [infinitesimal path ∞-groupoid adjunction](#StrucPaths) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ and the de Rham theorem for $\infty$-stacks is discussed at the level of [[homotopy categories]] in section 3 of 

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
{#SimpsonTeleman}


The $(\infty,1)$-topos $SynthDiff\infty Grpd$ is discussed in  section 3.4 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

The [[cohomology localization]] of $SynthDiff\infty Grpd$ and the infinitesimal singular simplicial complex as a presentation for infinitesimal paths objects in $SynthDiff\infty Grpd$ is discussed in

* [[Herman Stel]], _$\infty$-Stacks and their function algebras -- with applications to $\infty$-Lie theory_ , master thesis (2010) ([[schreiber:master thesis Stel|web]])
{#Stel}

The discussion of the cohomology localization of $SynthDiff\infty Grpd$ follows that in another context in

* [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))
{#Toen}

The construction of the infinitesimal path object has been amplified and discussed by [[Anders Kock]] under the name _combinatorial differential forms_, for instance in

*  [[Anders Kock]], _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

The results on differentiable [[Lie group cohomology]] used above is in 

* P. Blanc, _Cohomologie diff&eacute;rentiable et changement de groupes_ Ast&eacute;risque, vol. 124-125 (1985), pp. 113-130.
{#Blanc}

recalled in 

* [[Jean-Luc Brylinski]], _Differentiable Cohomology of Gauge Groups_ ([arXiv](http://arxiv.org/abs/math/0011069))
{#Brylinski}

which parallels 

* [[Graeme Segal]], _Cohomology of topological groups_ , Symposia Mathematica, Vol IV (1970) (1986?) p. 377
{#Segal}

[[!redirects synthetic differential ∞-groupoid]]
[[!redirects synthetic differential ∞-groupoids]]


[[!redirects SynthDiff∞Grpd]]