
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

A _formal smooth $\infty$-groupoid_ is an [[∞-groupoid]] equipped with a [[cohesive (∞,1)-topos|cohesive structure]] that subsumes that of [[smooth ∞-groupoid]]s as well as of [[infinitesimal object|infinitesimal]] $\infty$-groupoids -- [[∞-Lie algebroids]], hence equipped with "[[differential cohesion]]".

In the [[cohesive (∞,1)-topos]] of formal smooth $\infty$-groupoids the canonical [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]] $\mathbf{\Pi}(X)$ factors through a version relative to [[Smooth∞Grpd]]: the [[infinitesimal singular simplicial complex|infinitesimal path ∞-functor]] $\mathbf{\Pi}_{inf}(X)$. In traditional terms this is the object modeled by the [[tangent Lie algebroid]] and the [[de Rham space]] of $X$. The [[quasicoherent ∞-stack]]s on $\mathbf{\Pi}_{inf}(X)$ are [[D-module]]s on $X$.


## Definition

We consider [[(∞,1)-sheaves]] over a "twisted semidirect product" [[site]] or [[(∞,1)-site]] of 

* [[Cartesian spaces]] with [[smooth functions]] between them as for [[smooth ∞-groupoids]],

* and a [[category]] or [[(∞,1)-category]] of [[infinitesimally thickened points]].

First in 

* [1-localic definition](#Localic)

we consider the 1-site, then in 

* [∞-localic definition](#DerivedDefinition)

we consider the $(\infty,1)$-site.




### 1-localic definition
 {#Localic}

+-- {: .num_defn}
###### Definition

Let $T := $ [[CartSp]]${}_{smooth}$ be the [[syntactic category]] of the [[Lawvere theory]] of [[smooth algebra]]s: the category of [[Cartesian space]]s $\mathbb{R}^n$ and [[smooth function]]s between them.

Write

$$
  SmoothAlg := T Alg
$$

for its category of [[algebras over a Lawvere theory|T-algebras]] -- the [[smooth algebra]]s ($C^\infty$-rings).

Let

$$
  InfPoint \hookrightarrow SmoothAlg^{op}
$$

be the [[full subcategory]] on the [[infinitesimally thickened point]]s: this smooth algebras whose underlying abelian group is a [[vector space]] of the form $\mathbb{R} \oplus V$ with $V$ a finite-[[dimension]]al real [[vector space]] and nilpotent in the algebra structure.

=--


+-- {: .num_defn}
###### Definition


Let 

$$
  FormalCartSp \hookrightarrow SmoothLoc
$$ 

be the [[full subcategory]] of the category of [[smooth loci]] on the objects of the form 

$$
  U = \mathbb{R}^n \times D
$$ 

that are [[product]]s of a [[Cartesian space]] $\mathbb{R}^n \in$ [[CartSp]] for $n \in \mathbb{N}$ and an [[infinitesimally thickened point]] $D \in InfPoint$. (See at _[[FormalCartSp]]_.)

Equip this category with the [[coverage]] where a family of morphisms  is [[covering]] precisely if it is of the form $\{U_i \times D \stackrel{(f_i, Id_D)}{\to} U \times D\}$ for $\{f_i : U_i \to U\}$ a covering in [[CartSp]]${}_{smooth}$ (a [[good open cover]]).

=--

This appears as ([Kock 86, (5.1)]{#Kock86}). 


+-- {: .num_remark}
###### Note

The [[sheaf topos]] over [[FormalCartSp]] is ([[equivalence of categories|equivalent]] to) the [[topos]] known as the [[Cahiers topos]], a [[smooth topos]] that constitutes a [[Models for Smooth Infinitesimal Analysis|well adapted model]] for [[synthetic differential geometry]]. See at _[[Cahiers topos]]_ for further references.

=--

+-- {: .num_defn}
###### Definition

We say the [[(∞,1)-topos]] of **formal smooth $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  FormalSmooth \infty Grpd := Sh_{(\infty,1)}(FormalCartSp)
$$

on $FormalCartSp$. 

=--


### $\infty$-localic
 {#DerivedDefinition}

We now generalize the 1-category $InfPoint$ of [[infinitesimally thickened points]] to the [[(∞,1)-category]] $InfPoint_\infty$ of "derived infinitesimally thickened points", the formal dual of "small commutative $\infty$-algebras" from ([Hinich](#Hinich), [Lurie](#Lurie)).

(...)

## Properties


+-- {: .num_prop}
###### Proposition

$FormalSmooth \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[FormalCartSp]]  is an [[∞-cohesive site]]. See there for details.

=--

+-- {: .num_defn}
###### Definition

Write $FormalSmoothMfd \hookrightarrow SmoothAlg^{op}$ for the [[full subcategory]] of [[smooth loci]] on the 
 **[[formal smooth manifolds]]**: those modeled on [[FormalCartSp]] equipped with the evident [[coverage]].

=--

+-- {: .num_prop #CartSpAsDenseSubOfFSmoothMfd}
###### Observation

$FormalCartSp$ is a [[dense sub-site]] of $FormalSmoothMfd$.

=--

+-- {: .num_prop #EquivalenceToToposOverSoothSynthMfd}
###### Proposition

There is an [[equivalence of (∞,1)-categories]]

$$
  FormalSmooth\infty Grpd \simeq \hat Sh_{(\infty,1)}(FSmoothMfd)
$$

with the [[hypercomplete (∞,1)-topos]] over $FSmoothMfd$.

=--

+-- {: .proof}
###### Proof

With the [above observation](#CartSpAsDenseSubOfFSmoothMfd) this is directly analogous to the corresponding proof at [[ETop∞Grpd]]. 

=--



+-- {: .num_defn}
###### Definition

Write $i : CartSp_{smooth} \hookrightarrow FormalCartSp$ for the canonical [[full subcategory|embedding]].

=--


+-- {: .num_prop #CohesivenessUnderSmoothInfGrpd}
###### Proposition

The functor $i^*$ given by restriction along $i$ exhibits 
$FormalSmooth\infty Grpd$ as an 
<a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#LieTheory">infinitesimal cohesive neighbourhood</a>
of the [[(∞,1)-topos]] [[Smooth∞Grpd]] of [[smooth ∞-groupoids]] in that we have a quadruple of [[adjoint (∞,1)-functor]]s

$$
 ( i_! \dashv i^* \dashv i_* \dashv i^! )
  :
  Smooth \infty Grpd
  \stackrel{\overset{i_!}{\hookrightarrow}}{\stackrel{\overset{i^*}{\leftarrow}}{\stackrel{\overset{i_*}{\to}}{\stackrel{i^!}{\leftarrow}}}}
  FormalSmooth \infty Grpd
  \,,
$$

such that $i_!$ is a [[full and faithful (∞,1)-functor]].

=--



+-- {: .proof}
###### Proof

Since $i : CartSp_{smooth} \hookrightarrow CartSp_{formalsmooth}$ is an [infinitesimally ∞-cohesive site](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#InfinitesimalNeighbourhoodFromInfinitesimalSite) this follows with [a proposition](cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#InfinitesimalNeighbourhoodFromInfinitesimalSite) discussed at _[[cohesive (infinity,1)-topos -- infinitesimal cohesion]]_.

=--


## Structures

We discuss the realization of the general abstract <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#Structures">structures in a cohesive (∞,1)-topos</a> in $FormalSmooth \infty Grpd$.

Since by the [above discussion](#RelativeInftyConnectedness) $FormalSmooth\infty Grpd$ is strongly $\infty$-connected _relative_ to [[Smooth∞Grpd]] all of these structures that depend only on $\infty$-connectedness (and not on [[local (∞,1)-topos|locality]]) acquire a relative version.

### $\infty$-Lie algebroids and deformation theory   
 {#StrucLieTheory}

This subsection is at

* [[∞-Lie algebroid]].


### Paths and geometric Postnikov towers 
  {#StrucPaths}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos#Paths">intrinsic infinitesimal path adjunction</a> realized in $FormalSmooth\infty Grpd$.

$$
  (\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf}) 
   :=
  (i \circ \Pi_{inf} \dashv Disc_{inf} \Pi_{inf} \dashv Disc_{inf} \circ \Gamma_{inf})
  :
  FormalSmooth \infty Grpd
  \to 
  FormalSmooth \infty Grpd
  \,.
$$



+-- {: .num_prop}
###### Proposition

For $U \times D \in CartSp_{smooth} \ltimes InfinSmoothLoc = FormalCartSp \hookrightarrow FormalSmooth\infty Grpd$
we have that


$$
  \mathbf{Red}(U \times D) \simeq U
$$

is the **reduced [[smooth locus]]**: the [[Isbell duality|formal dual]] of the [[smooth algebra]] obtained by quotienting out all nilpotent elements in the [[smooth algebra]] $C^\infty(K \times D) \simeq C^\infty(K) \otimes C^\infty(D)$.

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

+-- {: .num_prop #PiInfYieldsDeRahmSpace}
###### Proposition


For $X \in SmoothAlg^{op}  \to FormalSmooth \infty Grpd$ a [[smooth locus]], we have that $\mathbf{\Pi}_{inf}(X)$ is the corresponding [[de Rham space]], the object
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
    FormalSmooth \infty Grpd(U \times D, \mathbf{\Pi}_{inf}(X))
    \\
    & \simeq 
    FormalSmooth \infty Grpd( \mathbf{Red}(U \times D), X)
    \\
    & \simeq
     FormalSmooth \infty Grpd( U, X )
  \end{aligned}
  \,.
$$

=--





### Cohomology and principal $\infty$-bundles {#StrucCohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive+(infinity%2C1)-topos+--+structures#Cohomology">intrinsic cohomology in a cohesive (∞,1)-topos</a> realized in $FormalSmooth\infty Grpd$.

#### Cohomology localization

+-- {: .num_prop}
###### Proposition

The canonical [[line object]] of the [[Lawvere theory]] [[CartSp]]${}_{smooth}$ is the [[real line]], regarded as
an object of the [[Cahiers topos]], and hence of
$FormalSmooth \infty Grpd$

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
$FormalSmooth\infty Grpd$. For $n \in \mathbb{N}$ write
$\mathbf{B}^n \mathbb{R} \in FormalSmooth\infty Grpd$ 
for its $n$-fold [[delooping]].

For $n \in \mathbb{N}$ and $X \in FormalSmooth\infty Grpd$ 
write 

$$
  H^n_{synthdiff}(X) := \pi_0 FormalSmooth\infty Grpd(X,\mathbf{B}^n \mathbb{R})
$$

for the [[cohomology group]] of $X$ with coefficients in the canonical line object in degree $n$.

+-- {: .num_defn}
###### Definition

Write

$$
  \mathbf{L}_{sdiff} \hookrightarrow FormalSmooth \infty Grpd
$$

for the [[cohomology localization]] of $FormalSmooth\infty Grpd$ at $\mathbb{R}$-[[cohomology]]: the full [[sub-(∞,1)-category]] on the $W$-[[local object]] with respect to the [[class]] $W$ of [[morphism]]s that induce [[isomorphism]]s in all $\mathbb{R}$-cohomology groups.

=--

+-- {: .num_prop #PresentationOfCohomologyLocalization}
###### Proposition

Let $SmoothAlg^{\Delta}_{proj}$ be the [[model structure on cosimplicial algebras|projective model structure on cosimplicial smooth algebras]] and let $j : (SmoothAlg^{\Delta})^{op} \to [FormalCartSp, sSet]$ be the prolonged external [[Yoneda embedding]]. 

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
     FormalSmooth\infty Grpd
   $$


1. The intrinsic $\mathbb{R}$-cohomology of any object $X \in FormalSmooth\infty Grpd$ is computed by the ordinary [[cochain cohomology]] of the [[Moore complex|Moore cochain complex]] underlying the cosimplicial abelian group of the image under the left [[derived functor]]$(\mathbb{L}\mathcal{O})(X)$ under the [[Dold-Kan correspondence]]:

   $$
      H_{fSmooth}^n(X) 
       \simeq 
      H^n_{cochain}(N^\bullet(\mathbb{L}\mathcal{O})(X))
      \,.
   $$

=--

+-- {: .proof}

###### Proof

First a remark on the sites. By the [above proposition](#EquivalenceToToposOverSoothSynthMfd)
$FormalSmooth\infty Grpd$ is equivalent to the [[hypercomplete (∞,1)-topos]] over [[formal smooth manifold]]s. This is [[presentable (∞,1)-category|presented]] by the [[nLab:Bousfield localization of model categories|left Bousfield localization]] of $[FSmoothMfd^{op}, sSet]_{proj,loc}$ at the [[∞-connected]] morphisms. But a fibrant object in $[FSmoothMfd^{op}, sSet]_{proj,loc}$ that is also [[n-truncated]] for $n \in \mathbb{N}$ is also fibrant in the hyperlocalization (only for the untruncated object there is an additional condition). Therefore the right Quillen functor claimed above indeed lands in truncated objects in $FormalSmooth \inftyGrpd$.

The proof of the above statements is given in ([Stel](#Stel)), following ([To&#235;n](#Toen)). Some details are spelled out at 
[[function algebras on ∞-stacks]].

=--

#### Cohomology of Lie groups

+-- {: .num_prop #RealCohomologyOfCompactLieGroup}
###### Proposition

Let $G \in SmoothMfd \hookrightarrow Smooth\infty Grpd \hookrightarrow FormalSmooth\infty Grpd $ be a [[Lie group]]. 

Then the intrinsic group cohomology in [[Smooth∞Grpd]] and in $FormalSmooth\infty Grpd$ of $G$ with coefficients in $\mathbb{R}$ coincides with [[Graeme Segal|Segal]]'s refined [[Lie group cohomology]] ([Segal](#Segal), [Brylinski](#Brylinski)).

$$
  H^n_{smooth}(\mathbf{B}G, \mathbb{R})
  \simeq
  H^n_{fsmooth}(\mathbf{B}G, \mathbb{R})
  \simeq
  H^n_{Segal}(G,\mathbb{R})
  \,.
$$


=--

For the full proof please see [[schreiber:differential cohomology in a cohesive topos|here, section 3.4]] for the moment.

+-- {: .num_cor }
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

+-- {: .num_note }
###### Note

This means that the intrinsic cohomology of [[compact topological space|compact]] [[Lie group]]s in [[Smooth∞Grpd]] and $FormalSmooth\infty Grpd$ coincides for these coefficients with the Segal-Blanc-Brylinski refined Lie group cohomology ([Brylinski](#Brylinski)).

=--

#### Cohomology of $\infty$-Lie algebroids
 {#CohomologyOfLieAlgebroids}

+-- {: .num_prop #IntrinsicRealCohomologyByCECohomology}
###### Proposition

Let $\mathfrak{a} \in L_\infty \mathrm{Algd}$ be an [[L-∞ algebroid]]. 
Then its intrinsic real cohomology in $\mathrm{FormalSmooth}\infty \mathrm{Grpd}$

$$
  H^n(\mathfrak{a}, \mathbb{R})
  :=
  \pi_0 \mathrm{FormalSmooth}\infty \mathrm{Grpd}(\mathfrak{a}, \mathbf{B}^n \mathbb{R})
$$

coincides with its ordinary [[∞-Lie algebroid cohomology|L-∞ algebroid cohomology]]: 
the cochain cohomology of its [[Chevalley-Eilenberg algebra]]

$$
  H^n(\mathfrak{a}, \mathbb{R})
   \simeq
  H^n(\mathrm{CE}(\mathfrak{a}))
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the [above propoposition](#PresentationOfCohomologyLocalization) we have that 

$$
  H^n(\mathfrak{a}, \mathbb{R}) \simeq
  H^n N^\bullet(\mathbb{L}\mathcal{O})(i(\mathfrak{a}))
  \,.
$$

By [this lemma](http://ncatlab.org/nlab/source/Lie+infinity-algebroid#CofibrantResolutionOfLinfinityAlgebroid)  this is

$$
  \cdots \simeq
  H^n N^\bullet
  \left(
    \int^{[k] \in \Delta} \mathbf{\Delta}[k] \cdot \mathcal{O}(i(\mathfrak{a})_k)
  \right)
  \,.
$$

Observe that $\mathcal{O}(\mathfrak{a})_\bullet$ is cofibrant in the Reedy model structure 
$[\Delta^{\mathrm{op}}, (\mathrm{SmoothAlg}^\Delta_{\mathrm{proj}})^{\mathrm{op}}]_{\mathrm{Reedy}}$ 
relative to the opposite of the projective model structure on cosimplicial algebras:  
the map from the latching object in degree $n$ in 
$\mathrm{SmoothAlg}^\Delta)^{\mathrm{op}}$ is dually in 
$\mathrm{SmoothAlg} \hookrightarrow \mathrm{SmoothAlg}^\Delta$ the projection 
$$
  \oplus_{i = 0}^n \mathrm{CE}(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
  \to
  \oplus_{i = 0}^{n-1} \mathrm{CE}(\mathfrak{a})_i \otimes \wedge^i \mathbb{R}^n
$$
hence is a surjection, hence a fibration in 
$\mathrm{SmoothAlg}^\Delta_{\mathrm{proj}}$ and therefore indeed a cofibration in 
$(\mathrm{SmoothAlg}^\Delta_{\mathrm{proj}})^{\mathrm{op}}$.

Therefore using the Quillen bifunctor property of the coend over the tensoring in reverse to [this lemma](http://ncatlab.org/nlab/source/Lie+infinity-algebroid#CofibrantResolutionOfLinfinityAlgebroid), the above is equivalent to
$$
  \cdots 
  \simeq
  H^n N^\bullet
  \left(
    \int^{[k] \in \Delta} \Delta[k] \cdot \mathcal{O}(i(\mathfrak{a})_k)
  \right)
$$
with the fat simplex replaced again by the ordinary simplex. But in brackets this is now by definition the image under the monoidal Dold-Kan correspondence of the Chevalley-Eilenberg algebra
$$
  \cdots 
  \simeq
  H^n( N^\bullet \Xi \mathrm{CE}(\mathfrak{a}) )
  \,.
$$

By the [[Dold-Kan correspondence]] we have hence

$$
  \cdots \simeq
  H^n(\mathrm{CE}(\mathfrak{a}))
  \,.
$$

=--

It follows that a degree-$n$ $\mathbb{R}$-cocycle on $\mathfrak{a}$ is presented by a morphism
$$
  \mu : \mathfrak{a} \to b^n \mathbb{R} 
  \,,
$$
where on the right we have the $L_\infty$-algebroid whose $\mathrm{CE}$-algebra is concentrated in
degree $n$. Notice that if $\mathfrak{a} = b \mathfrak{g}$ is the delooping of an $L_\infty$-
algebra $\mathfrak{g}$ this is equivalently a morphism of $L_\infty$-algebras
$$
  \mu : \mathfrak{g} \to b^{n-1} \mathbb{R} 
  \,.
$$

#### de Rham theorem

> under construction


We consider the [[de Rham theorem]] in $FormalSmooth \infty Grpd$, with respect to the infinitesimal de Rham cohomology

$$
  H_{dR,inf}^n(X) := \pi_0 FormalSmooth \infty Grpd(X, \mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R})
  \,.
$$



+-- {: .num_prop #deRhamTheorem}
###### Proposition


For all $n \in \mathbb{N}$, $n \gt 0$, The canonical morphism

$$
  \mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R}
  \to 
  \mathbf{\flat} \mathbf{B}^n \mathbb{R}
$$

is an [[equivalence in an (∞,1)-category|equivalence]].

=--

This means that for all $X \in \mathbf{H}$ the infinitesimal de Rham cohomology coincides with the ordinary real cohomology of the geometric realization of $X$

$$
  H^n_{dR, inf}(X)
   \simeq
  H^n(|X|, \mathbb{R})
  \,.
$$

+-- {: .proof}
###### Proof

Since all representables are formally smooth, we have a colimit

$$
  U \times_{\mathbf{\Pi}_{inf}(U)} U
  \stackrel{\to}{\to}
  U 
  \stackrel{}{\to}
  \mathbf{\Pi}_{inf}(U)
  \,.
$$

In the presentation over the site we have that 

$$
  X \times_{\mathbf{\Pi}_{inf}(X)} X : 
  K \times D \mapsto 
  \{
    f,g : K \times D \to U | K \to K \times D \stackrel{\to}{\to} U
  \} 
  \,.
$$

Therefore a morphism $\mathbf{\Pi}_{inf}(U) \to  \mathbb{R}$ is equivalently a morphism $\phi : U \to \mathbb{R}$ such that for all $K \times D \to U$ that coincide on $K$ we have that all the composites

$$
  K \times D \to U \stackrel{\phi}{\to} \mathbf{B}^n \mathbb{R}
$$

are equals. If $U$ is the point, then $\phi$ is necessarily constant. If $U$ is not the point, there is one nontrivial tangent vector $v$ in $U$. The composite produces the corresponding tangent vector $\phi_*(v)$ in $\mathbb{R}$. But all these tangent vectors must be equal.  Hence $\phi$ must be constant.


=--

This kind of argument is indicated in ([Simpson-Teleman, prop. 3.4](#SimpsonTeleman)).

+-- {: .num_prop #PiInfAndTangents}
###### Proposition

Let $X \in $ [[SmoothMfd]] and write 
$X^{\Delta^\bullet_{inf}} \in [CartSp_{formalsmooth}^{op}, sSet]$
for the [[tangent Lie algebroid]] regarded as a simplicial object (see [[L-infinity algebroid]] for the details). 

Then there is a morphism
$X^{\Delta^\bullet_{inf}} \to \mathbf{\Pi}_{inf}(X)$ which is an equivalence in $\mathbb{R}$-cohomology.

=--


(...)


### Formally &#233;tale morphisms and cohesive &#233;tale $\infty$-groupoids
 {#StructureSheaves}

We discuss [formally &#233;tale morphisms](#http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#FormallySmoothEtaleUnramified) and [&#233;tale objects](#)
with respect to the cohesive infinitesimal neighbourhood
$i :$ [[Smooth∞Grpd]] $\hookrightarrow FormalSmooth\infty Grpd$.

+-- {: .num_prop }
###### Proposition

Let $X_\bullet$ be a degreewise smooth [[paracompact topological space|paracompact]] [[simplicial manifold]], 
canonically regarded as an object of [[Smooth∞Grpd]]. 

Then
$j_! X_\bullet$ in $FormalSmooth \infty Grpd$ is presented by the
same simplicial manifold. 


=--

+-- {: .proof}
###### Proof

First consider an ordinary smooth paracompact manifold $X$. It admits a 
[[good open cover]] $\{U_i \to X\}$ and the corresponding [[Cech nerve]]
$C(\{U_i\}) in [CartSp_{smooth}^{op}, sSet]_{proj}$ is a 
[[cofibrant resolution]] of $X$. Therefore the 
$\infty$-functor $j_!$ is computed on $X$ by evaluating the corresponding
simplicial functor (of which it is the [[derived functor]]) on $C(\{U_i\})$.

Since the simplicial functor 

$$
  j_! 
   : 
  [CartSp_{smooth}^{op}, sSet]_{proj, loc}
    \to

  [CartSp_{formalsmooth}^{op}, sSet]_{proj, loc}
$$

is a [[left adjoint]] (indeed a [[left Quillen functor]]) it preserves the [[coproducts]] and [[coend]] that the Cech nerve is built from:

$$
  \begin{aligned}
    j_! C(\{U_i\})
    & =
    j_! \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_0, \cdots, i_n}
    U_{i_0, \cdots, i_n}
    \\
    & = 
    \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_0, \cdots, i_n}
    j_! (U_{i_0, \cdots, i_n})
    \\
    & = 
    \int^{[n] \in \Delta} \Delta[n] \cdot \coprod_{i_0, \cdots, i_n}
    U_{i_0, \cdots, i_n}
  \end{aligned}
  \,.
$$

Here we used that, by assumption on a [[good open cover]], all the 
$U_{i_0, \cdots, i_n}$ are [[Cartesian spaces]], and that 
$j_!$ coincides on [[representable functor|representables]] with the inclusion 
$CartSp_{smooth} \hookrightarrow CartSp_{formalsmooth}$.

Let now $X_\bullet$ be a general simplicial manifold. Assume that in each degree there is a [[good open cover]] $\{U_{p,i} \to X_p\}$ such that these fit into a simplicial system giving a bisimplicial Cech nerve such that there is a morphism of [[bisimplicial object|bisimplicial presheaves]]

$$
  C(\mathcal{U})_{\bullet, \bullet} \to X_{\bullet}
$$

with $X_\bullet$ regarded as simplicially constant in one direction. Each 
$C(\mathcal{U})_{p, \bullet} \to X_p$ is  a cofibrant resolution.

We claim that the [[coend]]

$$
  \int^{[n] \in \Delta} C(\mathcal{U})_{n, \bullet} \cdot \mathbf{\Delta}[n]
  \;\;\;
  \to
  \;\;\;
  X
$$

is a cofibrant resolution of $X$, where $\mathbf{\Delta}$ is the [[fat simplex]]. 
From this the proposition follows by again applying the left Quillen functor $j_!$ degreewise and pulling it through all the colimits.

This remaining claim follows from the same argument as used 
above in prop. \ref{RealCohomologyOfCompactLieGroup}.

=--

+-- {: .num_prop #RecoveringLocalDiffeomorphisms}
###### Proposition

A morphism in $FormalSmooth\infty Grpd$, is a [[formally étale morphism]] with respect to the [[infinitesimal cohesion]] $i \colon Smooth \infty Grpd \hookrightarrow FormalSmooth\infty Grpd$ precisely if for all [[infinitesimally thickened points]] $D$ the diagram

$$
  \array{
    X^D &\stackrel{f^D}{\to}& Y^D
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{f}{\to}& Y
  }
$$

is an $\infty$-pullback under $i^*$.

=--

+-- {: .num_remark}
###### Remark

Since $i^*$ preserves $\infty$-limits, this is the case in particular if the diagram is an $\infty$-pullback already in $FormalSmooth\infty Grod$. In this form, restricted to 0-truncated objects, hence to the 
[[Cahiers topos]], this characterization of formally &eacute;tale morphisms appears axiomatized around p. 82 of ([Kock 81, p. 82](#Kock)).

In particular, a [[smooth function]] $f : X \to Y$ in [[SmoothMfd]] $\hookrightarrow$ [[Smooth∞Grpd]] between [[smooth manifolds]] is a [[formally étale morphism]] with respect to the [[infinitesimal cohesion]] $Smooth \infty Grpd \hookrightarrow FormalSmooth\infty Grpd$ precisely if it is a [[local diffeomorphism]] in the traditional sense.

=--

+-- {: .proof}
###### Proof

We spell out the case for smooth manifolds.
Here we need to to show that 

$$
  \array{
    i_! X &\stackrel{i_! f}{\to}& i_! Y
    \\
    \downarrow && \downarrow
    \\
    i_* X &\stackrel{i_* f}{\to}& i_* Y
  }
$$

is a [[pullback]] in $Sh(CartSp_{formalsmooth})$ precisely if $f$ is a local diffeomorphism. This is a pullback precisely if for all $U \times D \in CartSp_{smooth} \ltimes InfPoint \simeq CartSp_{formalsmooth}$ the diagram of sets of plots

$$
  \array{
    Hom(U \times D, i_! X) &\stackrel{i_! f}{\to}& Hom(U \times D, i_! Y)
    \\
    \downarrow && \downarrow
    \\
    Hom(U \times D, i_* X) &\stackrel{i_* f}{\to}& Hom(U \times D, i_* Y)
  }
$$

is a pullback. Using, by the discussion at [[∞-cohesive site]], that $i_!$ preserves colimits and restricts to $i$ on representables, and using that $i^* (U \times D ) = U$, this is equivalently the diagram

$$
  \array{
    Hom(U \times D, X) &\stackrel{f_*}{\to}& Hom(U \times D, Y)
    \\
    \downarrow && \downarrow
    \\
    Hom(U , X) &\stackrel{f_*}{\to}& Hom(U , Y)
  }
  \,,
$$

where the vertical morphisms are given by restriction along the inclusion $(id_U, *) : U \to U \times D$.

For one direction of the claim it is sufficient to consider this situation for $U = *$ the point and $D$ the first order infinitesimal interval. Then $Hom(*,X)$ is the underlying set of points of the manifold $X$ and $Hom(D,X)$ is the set of tangent vectors, the set of points of the [[tangent bundle]] $T X$. The pullback 

$$
  Hom(*,X) \times_{Hom(*,Y)} Hom(D,Y)
$$

is therefore the set of pairs consisting of a point $x \in X$ and a tangent vector $v \in T_{f(x)} Y$. This set is in fiberwise bijection with $Hom(D, X) = T X$ precisely if for each $x \in X$ there is a bijection $T_x X \simeq T_{f(x)}Y $, hence precisely if $f$ is a [[local diffeomorphism]]. Therefore $f$ being a local diffeo is necessary for $f$ being formally &#233;tale with respect to the given notion of infinitesimal cohesion.

To see that this is also sufficient notice that this is evident for the case that $f$ is in fact a [[monomorphism]], and that since [[smooth function]]s are characterized locally, we can reduce the general case to that case.

=--


+-- {: .num_prop }
###### Proposition

A [[Lie groupoid]] $\mathcal{G}$ is an [[étale groupoid]] in the traditional sense, precisely if regarded as an object in $i :$ [[Smooth∞Grpd]] $\hookrightarrow$ [[FormalSmooth∞Grpd]] it is an [cohesive &#233;tale ∞-groupoid](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#EtaleObjects).

=--

+-- {: .proof}
###### Proof

Let $\mathcal{G}_0 \to \mathcal{G}$ be the inclusion of the smooth manifold of objects. This is an [[effective epimorphism in an (infinity,1)-category|effective epimorphism]]. It remains to show that this is [formally &#233;tale](http://ncatlab.org/nlab/show/cohesive+%28infinity%2C1%29-topos+--+infinitesimal+cohesion#FormallySmoothEtaleUnramified) with respect to the given cohesive neighbourhood.

By the discussion at _[[(∞,1)-pullback]]_ we may compute the characteristic $(\infty,1)$-pullback by an ordinary pullback of a [[fibration]] of [[simplicial presheaves]] that presents $\mathcal{G}_0 \to \mathcal{G}$.

By the [[factorization lemma]] such is given by 

$$
  \mathcal{G}^I \times_{\mathcal{G}} \mathcal{G}_0 \to \mathcal{G}
  \,.
$$

By inspection one see that this morphism is

* in degree 0 the target-map $t : Mor(\mathcal{G}) \to \mathcal{G}_0$;

* in degree 1 the projection $Mor(\mathcal{G}) {}_t\times_{s} Mor(\mathcal{G}) \to Mor(\mathcal{G})$.

By prop. \ref{RecoveringLocalDiffeomorphisms} both of these need to be 
[[étale maps]] in the ordinary sense. By definition, this is the case 
precisely if $\mathcal{G}$ is an [[étale groupoid]].

=--

### Formally smooth / formally unramified morphisms

As a direct consequence of prop. \ref{RecoveringLocalDiffeomorphisms} we have the following

+-- {: .num_prop}
###### Proposition

A [[smooth function]] $f : X \to Y$ between [[smooth manifolds]], 
is a [[submersion]] or [[immersion]], respectively, precisely
if, when canonically regarded as a morphism in $FormalSmooth \infty Grpd$, it is a [[formally smooth morphism]] or [[formally unramified morphism]], respectively.

=--

+-- {: .proof}
###### Proof

As in the proof of prop. \ref{RecoveringLocalDiffeomorphisms}
we find that the pullback $i_* X \times_{i_* Y} i_! Y$
is over the [[infinitesimal interval]] isomorphic to 

$$
  X \times_Y T Y
$$

and the canonical morphism from $i_! X $ into this pullback is

$$
  T X \to X \times_Y T Y
  \,.
$$

=--


### Lie differentiation
 {#LieDifferentiation}

We indicate how to formalize [[Lie differentiation]] in the context of formal smooth $\infty$-groupoids. 

Let

$$
  inf : InfPoint_\infty \hookrightarrow \mathbf{H}^{*/}
$$

be the canonical inclusion. By ([Lurie, theorem 0.0.13, remark 0.0.15](#Lurie), also [Pridham 07](#Formal+Moduli+Problems+and+DG-Lie+Algebras#Pridham)) we have a full inclusion

$$
  Lie_\infty \hookrightarrow Sh_\infty(InfPoint_\infty)
$$

on those objects whose space of global sections is contractible and which are [[cohesive (∞,1)-presheaf on E-∞ rings|infinitesimally cohesive]] (for a somewhat different notion of "infinitesimal cohesion", beware the terminology). Consider then the $\infty$-functor

$$
  Grp(\mathbf{H})
  \simeq
  \mathbf{H}^{*/}_{\geq 1}
   \stackrel{yoneda}{\to}
  PSh_\infty( \mathbf{H}^{*/})
  \stackrel{inf^*}{\to}
  PSh_\infty(InfPoint_\infty)
$$

which sends a pointed connected formal smooth $\infty$-groupoid $\mathbf{B}G$ to the $(\infty,1)$-presheaf of pointed morphisms

$$
  \mathbf{pt} \to \mathbf{B}G
$$

for $\mathbf{pt} \in InfPoint_\infty$.

By assumption that $\mathbf{B}G$ is connected (and we need to assume that it is [[geometric infinity-stack|geometric]], which will gives infinitesimal cohesion by the [[Artin-Lurie representability theorem]]) this factors as

$$
  \mathbf{H}^{*/}_{\geq 1} 
   \stackrel{Lie}{\to}
  Lie_\infty
   \hookrightarrow
  Sh_\infty(InfPoint_\infty)
  \,.
$$

The resulting $\infty$-functor

$$
  Lie : Grp(\mathbf{H}) \simeq \mathbf{H}^{*/}_{\geq 1} \to Lie_\infty
$$

is Lie differentiation.

For differentiation of smooth groupoids with [[atlas]] $U \to X$ to [[L-infinity algebroids]] this happens under $U$

$$
  \mathbf{H}^{U/}
$$

(...)

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[Euclidean-topological ∞-groupoid]]

[[!include geometries of physics -- table]]


## References

The site [[FormalCartSp]] is discussed in section 5 of

* {#Kock86} [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_ , Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0)).
 

For more on this see at _[[Cahiers topos]]_.

The notion of formally &eacute;tale maps as obtained here from the general abstract definition in [[differential cohesion]] coincided on 0-truncated objects with that defined on p. 82 of 

* {#Kock81} [[Anders Kock]], _Synthetic Differential Geometry_ (1981) ([pdf](http://home.imf.au.dk/kock/sdg99.pdf)) 
 

The [infinitesimal path ∞-groupoid adjunction](#StrucPaths) $(\mathbf{Red} \dashv \mathbf{\Pi}_{inf} \dashv \mathbf{\flat}_{inf})$ and the de Rham theorem for $\infty$-stacks is discussed at the level of [[homotopy categories]] in section 3 of 

* {#SimpsonTeleman} [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))
 


The $(\infty,1)$-topos $SynthDiff\infty Grpd$: 

* [[Urs Schreiber]], section 4.4 of: _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

* [[Hisham Sati]], [[Urs Schreiber]], Section 3.1.2 of: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[Urs Schreiber]], _[[schreiber:Introduction to Higher Supergeometry]]_, lecture at _[[Higher Structures in M-Theory 2018]]_, [Durham Symposium](http://www.maths.dur.ac.uk/lms/)

  published in parts as: _Higher Structures in M-Theory_ (with [[Branislav Jurčo]], [[Christian Saemann]], [[Martin Wolf]]), Fortschritte der Physik (2019) ([arXiv:1903.02807](https://arxiv.org/abs/1903.02807), [doi:10.1002/prop.201910001]( https://doi.org/10.1002/prop.201910001))


The [[cohomology localization]] of $SynthDiff\infty Grpd$ and the infinitesimal singular simplicial complex as a presentation for infinitesimal paths objects in $SynthDiff\infty Grpd$ is discussed in

* {#Stel} [[Herman Stel]], _$\infty$-Stacks and their function algebras -- with applications to $\infty$-Lie theory_ , master thesis (2010) ([[schreiber:master thesis Stel|web]])


The discussion of the cohomology localization of $SynthDiff\infty Grpd$ follows that in another context in

* {#Toen} [[nLab:Bertrand Toën]], _Champs affine_ ([arXiv:math/0012219](http://arxiv.org/abs/math/0012219))


The construction of the infinitesimal path object has been amplified and discussed by [[Anders Kock]] under the name _combinatorial differential forms_, for instance in

*  [[Anders Kock]], _Synthetic Geometry of Manifolds_ ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

The discussion that the normalized [[cosimplicial algebra]] of functions on the [[infinitesimal singular simplicial complex]] is the [[de Rham complex]] is further discussed in 

* Herman Stel, _[[schreiber:Cosimplicial C-infinity rings and the de Rham complex of Euclidean space]]_ ([arXiv:arXiv:1310.7407](http://arxiv.org/abs/arXiv:1310.7407))

The results on differentiable [[Lie group cohomology]] used above is in 

* {#Blanc} P. Blanc, _Cohomologie diff&eacute;rentiable et changement de groupes_ Ast&eacute;risque, vol. 124-125 (1985), pp. 113-130.


recalled in 

* {#Brylinski} [[Jean-Luc Brylinski]], _Differentiable Cohomology of Gauge Groups_ ([arXiv](http://arxiv.org/abs/math/0011069))


which parallels 

* {#Segal} [[Graeme Segal]], _Cohomology of topological groups_ , Symposia Mathematica, Vol IV (1970) (1986?) p. 377


The $(\infty,1)$-site of derived infinitesimal points is discussed in 

* {#Lurie} [[Jacob Lurie]], _[[Formal moduli problems]]_ 
 

following

* {#Hinich} [[Vladimir Hinich]], _DG coalgebras as formal stacks_, J. Pure Appl. Algebra, 162 (2001), 209-250  ([arXiv:math/9812034](http://arxiv.org/abs/math/9812034))
 

[[!redirects formal smooth infinity-groupoids]]

[[!redirects formal smooth ∞-groupoid]]
[[!redirects formal smooth ∞-groupoids]]

[[!redirects synthetic differential infinity-groupoid]]
[[!redirects synthetic differential infinity-groupoids]]

[[!redirects synthetic differential ∞-groupoid]]
[[!redirects synthetic differential ∞-groupoids]]

[[!redirects synthetic-differential ∞-groupoid]]
[[!redirects synthetic-differential ∞-groupoids]]

[[!redirects formal smooth homotopy type]]
[[!redirects formal smooth homotopy types]]

[[!redirects formal smooth groupoid]]
[[!redirects formal smooth groupoids]]

[[!redirects SynthDiff∞Grpd]]

[[!redirects FormalSmooth∞Groupoid]]
[[!redirects FormalSmooth∞Groupoids]]
[[!redirects FormalSmooth∞Grpd]]
