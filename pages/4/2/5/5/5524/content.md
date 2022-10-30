
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
  CartSp_{synthdiff} := 
   CartSp \ltimes InfPoint
$$ 

be the [[full subcategory]] of the category of [[smooth loci]] on the objects of the form 

$$
  U = \mathbb{R}^n \times D
$$ 

that are [[product]]s of a [[Cartesian space]] $\mathbb{R}^n \in$ [[CartSp]] for $n \in \mathbb{N}$ and an [[infinitesimally thickened point]] $D \in InfPoint$.

Equip this category with the [[coverage]] where a family of morphisms  is [[covering]] precisely if it is of the form $\{U_i \times D \stackrel{(f_i, Id_D)}{\to} U \times D\}$ for $\{f_i : U_i \to U\}$ a covering in [[CartSp]]${}_{smooth}$ (a [[good open cover]]).

=--

This appears as ([Kock, (5.1)]{#Kock}). 


+-- {: .num_note}
###### Note

The [[sheaf topos]] over [[CartSp]]${}_{synthdiff}$ is ([[equivalence of categories|equivalent]] to) the [[topos]] known as the [[Cahiers topos]], a [[smooth topos]] that constitutes a [[Models for Smooth Infinitesimal Analysis|well adapted model]] for [[synthetic differential geometry]].

=--

+-- {: .num_defn}
###### Definition

We say the [[(∞,1)-topos]] of **synthetic differential $\infty$-groupoids** is the [[(∞,1)-category of (∞,1)-sheaves]]

$$
  SynthDiff \infty Grpd := Sh_{(\infty,1)}(CartSp_{synthdiff})
$$

on $CartSp_{synthdiff}$. 

=--



## Properties


+-- {: .num_prop}
###### Proposition

$SynthDiff \infty Grpd$ is a [[cohesive (∞,1)-topos]].

=--

+-- {: .proof}
###### Proof

Because [[CartSp]]${}_{synthdiff}$ is an [[∞-cohesive site]]. See there for details.

=--

+-- {: .num_defn}
###### Definition

Write $FSmoothMfd \hookrightarrow SmoothAlg^{op}$ for the [[full subcategory]] of [[smooth loci]] on the 
 **[[formal smooth manifold]]s**: those modeled on [[CartSp]]${}_{synthdiff}$ equipped with the evident [[coverage]].

=--

+-- {: .num_prop #CartSpAsDenseSubOfFSmoothMfd}
###### Observation

$CartSp_{synthdiff}$ is a [[dense sub-site]] of $FSmoothMfd$.

=--

+-- {: .num_prop #EquivalenceToToposOverSoothSynthMfd}
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



+-- {: .num_defn}
###### Definition

Write $i : CartSp_{smooth} \hookrightarrow CartSp_{synthdiff}$ for the canonical [[full subcategory|embedding]].

=--


+-- {: .num_prop #CohesivenessUnderSmoothInfGrpd}
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

### $\infty$-Lie algebras and deformation theory   
 {#StrucLieTheory}

The discussion that goes here is at 

* [[∞-Lie algebroid]].


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



+-- {: .num_prop}
###### Proposition

For $U \times D \in CartSp_{smooth} \ltimes InfinSmoothLoc = CartSp_{synthdiff} \hookrightarrow SynthDiff\infty Grpd$
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





### Cohomology and principal $\infty$-bundles {#StrucCohomology}

We discuss the <a href="http://nlab.mathforge.org/nlab/show/cohesive%20(infinity,1)-topos#Cohomology">intrinsic cohomology in a cohesive (∞,1)-topos</a> realized in $SynthDiff\infty Grpd$.

#### Cohomology localization

+-- {: .num_prop}
###### Proposition

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

+-- {: .num_defn}
###### Definition

Write

$$
  \mathbf{L}_{sdiff} \hookrightarrow SynthDiff \infty Grpd
$$

for the [[cohomology localization]] of $SynthDiff\infty Grpd$ at $\mathbb{R}$-[[cohomology]]: the full [[sub-(∞,1)-category]] on the $W$-[[local object]] with respect to the [[class]] $W$ of [[morphism]]s that induce [[isomorphism]]s in all $\mathbb{R}$-cohomology groups.

=--

+-- {: .num_prop #PresentationOfCohomologyLocalization}
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
$SynthDiff\infty Grpd$ is equivalent to the [[hypercomplete (∞,1)-topos]] over [[formal smooth manifold]]s. This is [[presentable (∞,1)-category|presented]] by the [[nLab:Bousfield localization of model categories|left Bousfield localization]] of $[FSmoothMfd^{op}, sSet]_{proj,loc}$ at the [[∞-connected]] morphisms. But a fibrant object in $[FSmoothMfd^{op}, sSet]_{proj,loc}$ that is also [[n-truncated]] for $n \in \mathbb{N}$ is also fibrant in the hyperlocalization (only for the untruncated object there is an additional condition). Therefore the right Quillen functor claimed above indeed lands in truncated objects in $SynthDiff \inftyGrpd$.

The proof of the above statements is given in ([Stel](#Stel)), following ([To&#235;n](#Toen)). Some details are spelled out at 
[[function algebras on ∞-stacks]].

=--

#### Cohomology of Lie groups

+-- {: .num_prop #RealCohomologyOfCompactLieGroup}
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

For the full proof please see [[schreiber:differential cohomology in a cohesive topos|here, section 3.4]] for the moment.

+-- {: .num_prop }
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

This means that the intrinsic cohomology of [[compact topological space|compact]] [[Lie group]]s in [[Smooth∞Grpd]] and $SynthDiff\infty Grpd$ coincides for these coefficients with the Segal-Blanc-Brylinski refined Lie group cohomology ([Brylinski](#Brylinski)).

=--

#### Cohomology of $\infty$-Lie algebroids
 {#CohomologyOfLieAlgebroids}

+-- {: .num_prop #IntrinsicRealCohomologyByCECohomology}
###### Proposition

Let $\mathfrak{a} \in L_\infty \mathrm{Algd}$ be an [[L-∞ algebroid]]. 
Then its intrinsic real cohomoloogy in $\mathrm{SynthDiff}\infty \mathrm{Grpd}$

$$
  H^n(\mathfrak{a}, \mathbb{R})
  :=
  \pi_0 \mathrm{SynthDiff}\infty \mathrm{Grpd}(\mathfrak{a}, \mathbf{B}^n \mathbb{R})
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

Therefore using the Quillen bifunctor property of the coend over the tensoring in reverse to 
lemma \ref{CofibrantResolutionOfLinfinityAlgebroid} the above is equivalent to
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


We consider the [[de Rham theorem]] in $SynthDiff \infty Grpd$, with respect to the infinitesimal de Rham cohomology

$$
  H_{dR,inf}^n(X) := \pi_0 SynthDiff \infty Grpd(X, \mathbf{\flat}_{inf} \mathbf{B}^n \mathbb{R})
  \,.
$$



+-- {: .num_prop #deRhamTheorem}
###### Proposition


For all $n \in \mathbb{N}$ The canonical morphism

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
$X^{\Delta^\bullet_{inf}} \in [CartSp_{synthdiff}^{op}, sSet]$
for the [[tangent Lie algebroid]] regarded as a simplicial object (see [[L-infinity algebroid]] for the details). 

Then there is a morphism
$X^{\Delta^\bullet_{inf}} \to \mathbf{\Pi}_{inf}(X)$ which is an equivalence in $\mathbb{R}$-cohomology.

=--

(...)

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

[[!redirects synthetic-differential ∞-groupoid]]
[[!redirects synthetic-differential ∞-groupoids]]


[[!redirects SynthDiff∞Grpd]]