
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Cohesive toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _Cahier topos_ is a [[cohesive topos]] that constitutes a [[Models for Smooth Infinitesimal Analysis|well-adapted model]] for [[synthetic differential geometry]] (a "[[smooth topos]]").

It is the [[sheaf topos]] on the [[site]] [[FormalCartSp]] of [[infinitesimal object|infinitesimally thickened]] [[Cartesian spaces]].

## Definition

+-- {: .num_defn}
###### Definition

Let [[FormalCartSp]] be the [[full subcategory]] of the category of [[smooth loci]] on those of the form 

$$
  \mathbb{R}^n \times \ell W
  \,,
$$

consisting of a [[product]] of a [[Cartesian space]] with an [[infinitesimally thickened point]], i.e. a formal dual of a _Weil algebra_ .

Dually, the [[opposite category]] is the [[full subcategory]] $FormalCartSp^{op} \hookrightarrow SmoothAlg$ of [[smooth algebras]] on those of the form

$$
  C^\infty( \mathbb{R}^k \times \ell W)
  = 
  C^\infty(\mathbb{R}^k) \otimes W
  \,.
$$

=--

This appears for instance in [Kock Reyes (1)](#KockReyes).

+-- {: .num_defn}
###### Definition

Define a structure of a [[site]] on [[FormalCartSp]] by declaring a [[covering]] family to be a family of the form

$$
  \{
    U_i \times \ell W \stackrel{p_i \times Id}{\to} U \times \ell W
  \}
$$

where $\{U_i \stackrel{p_i}{\to} U\}$ is an [[open cover]] of the [[Cartesian space]] $U$ by Cartesian spaces $U_i$. 

=--

This appears as [Kock (5.1)](#Kock). 

+-- {: .num_defn}
###### Definition


The **Cahiers topos** $\mathcal{CT}$ is the [[category of sheaves]] on this site:

$$
  \mathcal{CT} := Sh(FormalCartSp)  
  \,.
$$

=--

This site of definition appears in [Kock, Reyes](#KockReyes). The original definition is due to [Dubuc](#Dubuc)

## Properties

### Synthetic differential geometry

+-- {: .num_prop #ModelForSynthetic}
###### Proposition


The Cahiers topos is a well-adapted model for [[synthetic differential geometry]].

=--

This is due to [Dubuc](#Dubuc).

### Connectedness, locality and cohesion

+-- {: .num_prop}
###### Proposition

The Cahiers topos is a [[cohesive topos]]. See [[synthetic differential infinity-groupoid]] for details.

=--


### Convenient vector spaces
 {#ConvenientVectorSpaces}

+-- {: .num_prop}
###### Proposition

The [[category]] of [[convenient vector spaces]] with [[smooth functions]] between them embeds as a [[full subcategory]] into the Cahiers topos.

The embedding is given by sending a convenient vector space $V$ to the sheaf given by

$$
  V
  : 
  \mathbb{R}^k \times \ell W
  \mapsto 
  C^\infty(\mathbb{R}^k, V) \otimes W
  \,.
$$

=--

This result was announced in [Kock](#Kock). See the corrected proof in ([KockReyes](#KockReyes)).

+-- {: .num_remark}
###### Remark

Together with prop. \ref{ModelForSynthetic}
this means that the [[differential geometry]] on
convenient vector spaces may be treated synthetically
in the Cahiers topos.

=--

### Synthetic tangent bundles of smooth spaces

### Synthetic tangent spaces
 {#RelationToSyntheticTangentSpaces}

We discuss here induced [[synthetic tangent spaces]] of [[smooth spaces]] in the sense of [[diffeological spaces]] and more general [[sheaves]] on the site of [[smooth manifolds]] after their canonical embedding into the Cahiers topos.

+-- {: .num_defn}
###### Definition

Write $SmoothLoc$ for the [[category]] of [[smooth loci]]. Write 

$$
  CartSp \hookrightarrow SmoothLoc
$$

for the [[full subcategory]] on the [[Cartesian spaces]] $\mathbb{R}^n$ ($n \in \mathbb{N}$). Write 

$$
  InfThPoint \hookrightarrow SmoothLoc
$$

for the [[full subcategory]] on the [[infinitesimally thickened points]], and write

$$
  CartSp_{synthdiff} \hookrightarrow SmoothLoc
$$

for the full subcategory on those smooth loci which are the [[cartesian product]] of a [[Cartesian space]] $\mathbb{R}^n$ ($n \in \mathbb{N}$) and an [[infinitesimally thickened point]].

We regard [[CartSp]] as a [[site]] by equipping it with the [[good open cover]] [[coverage]]. We regard $InfThPoint$ as equipped with the trivial coverage and $CartSp_{synthdiff}$ as equipped with the induced product coverage.

The [[sheaf topos]] $Sh(CartSp)$ is that of _[[smooth spaces]]_. The sheaf topos $Sh(CartSp_{synthdiff})$ is the _Cahier topos_.

=--

+-- {: .num_example #InfinitesimalInterval}
###### Example

We write

$$
  D \coloneqq \ell(\mathbb{R}[\epsilon]/(\epsilon^2))
  \in 
  InfThPt \hookrightarrow CartSp_{synthdiff}
$$

for the [[infinitesimal space|infinitesimal interval]], the [[smooth locus]] dual to the [[smooth algebra]] "[[ring of dual numbers|of dual numbers]]".

=--

+-- {: .num_defn #SyntheticTangentBundle}
###### Definition

For $X \in Sh(CartSp_{synthdiff})$ any object in the Cahier topos, its **[[synthetic tangent bundle]]** in the sense of [[synthetic differential geometry]] is the [[internal hom]] space $X^D$, equipped with the projection map

$$
  X(\ast \to D) \colon X^D \to X
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The canonical inclusion functor $i \colon CartSp \to CartSp_{synthdiff}$ induces an [[adjoint pair]]

$$
  Sh(CartSp)
   \stackrel{\overset{i_\ast}{\to}}{\underset{i^\ast}{\leftarrow}}
  Sh(CartSp_{synthdiff})
$$

where $i^\ast$ is given by precomposing a [[presheaf]] on $CartSp_{synthdiff}$ with $i$. The [[left adjoint]] $i_\ast$ has the interpretation of the inclusion of [[smooth spaces]] as [[reduced objects]] in the Cahiers topos.

=--

This is discussed in more detail at _[[synthetic differential infinity-groupoid]]_.

+-- {: .num_prop #CharacterizationOfImageInCahiersTopos}
###### Proposition

For $X \in Sh(CartSp)$ a [[smooth space]], and for $\ell(W) \in InfThPoint$ an infinitesimally thickened point, the morphisms

$$
  \ell(W) \to i_\ast X
$$

in $Sh(CartSp_{synthdiff})$ are in natural [[bijection]] to [[equivalence classes]] of pairs of morphisms

$$
  \ell(W) \to \mathbb{R}^n \to X
$$

consisting of a morphism in $CartSp_{synth}$ on the left and a morphism in $Sh(CartSp)$ on the right (which live in different categories and hence are not composable, but usefully written in juxtaposition anyway). The [[equivalence relation]] relates two such pairs if there is a [[smooth function]] $\phi \colon \mathbb{R}^n \to \mathbb{R}^{n'}$ such that in the diagram

$$
  \array{
    && \mathbb{R}^n
    \\
    & \nearrow & & \searrow
    \\
    \ell(W) && \downarrow^{\mathrlap{\phi}} && X
    \\
    & \searrow && \nearrow
    \\
    && \mathbb{R}^{n'}
  }
$$

the left triangle commutes in $CartSp_{synthdiff}$ and the right one in $Sh(CartSp)$.

=--

+-- {: .proof}
###### Proof

By general properties of [[left adjoints]] of functors of [[presheaves]], $i_\ast X$ is the [[left Kan extension]] of the presheaf $X$ along $i$. By the [[Yoneda lemma]] and the [[coend]] formula for these (as discussed there), we have that the set of maps $\ell(W) \to i_\ast X$ is naturally identified with

$$
  (i_\ast X)(\ell(W))
  =
  (Lan_i X)(\ell(W))
  =
  \int^{\mathbb{R}^n \in CartSp}
  Hom_{CartSp_{synthdiff}}(\ell(W), \mathbb{R}^n)
  \times 
  X(\mathbb{R}^n)
  \,.
$$ 

Unwinding the definition of this [[coend]] as a [[coequalizer]] yields the above description of equivalence classes.

=--



## Variants and generalizations

When restricting the [[site]] of infinitesimally thickened Cartesian spaces to that of plain [[Cartesian spaces]] one obtaines the topos discussed at _[[smooth space]]_. This is still a [[cohesive topos]], but no longer a model for [[synthetic differential geometry]].

The [[(∞,1)-sheaf (∞,1)-topos]] over $CartSp_{th}$ is disucssed at [[synthetic differential ∞-groupoid]]. It contains that Cahiers topos as the sub-[[(n,1)-topos|(1,1)-topos]] of [[0-truncated]] objects.


## References

The Cahiers topos was introduced in 

* [[Eduardo Dubuc]], _Sur les mod&#232;les de la g&#233;om&#233;trie diff&#233;rentielle synth&#233;tique_ [[Cahiers]] de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no. 3 (1979), p. 231-279  ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)).
 {#Dubuc}

and got its name from this journal publication. The definition appears in theorem 4.10 there, which asserts that it is a well-adapted model for [[synthetic differential geometry]].

A review discussion is in section 5 of

* [[Anders Kock]], _Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17  ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_1_3_0))
  {#Kock}

and with a corrected definition of the site of definition in

* [[Anders Kock]], [[Gonzalo Reyes]], _Corrigendum and addenda to: Convenient vector spaces embed into the Cahiers topos_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 27 no. 1 (1986), p. 3-17 ([numdam](http://www.numdam.org/item?id=CTGDC_1987__28_2_99_0))
 {#KockReyes}

It appears briefly mentioned in example 2) on p. 191 of the standard textbook

* [[Anders Kock]], _Synthetic differential geometry_ ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

With an eye towards [[Frölicher space]]s the site is also considered in section 5 of 

* Hirokazu Nishimura, _Beyond the Regnant Philosophy of Manifolds_ ([arXiv:0912.0827](http://arxiv.org/abs/0912.0827))


The [[(∞,1)-topos]] analog of the Cahiers topos ([[synthetic differential ∞-groupoids]]) is discussed in section 3.4 of

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

