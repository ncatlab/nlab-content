+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

In general, given a [[category]] $\mathcal{C}$ and a [[class]] $W$ of [[morphisms]], one may ask for the _[[localization]]_ $\mathcal{C}[W^{-1}]$, or more specifically for the [[reflective subcategory]] of $W$-[[local objects]] (the [[reflective localization]]). Similarly for variants in [[higher category]], such as _[[localization of an (∞,1)-category]]_.

If $\mathcal{C}$ has [[finite products]], then for a given [[object]] $\mathbb{A} \in \mathcal{C}$, one may take $W \coloneqq W_{\mathbb{A}}$ to be the class of morphisms of the form 

$$
  X \times (\mathbb{A} \overset{\exists!}{\to} \ast)
  \;\;\colon\;\;
  X \times \mathbb{A}
    \overset{p_1}{\longrightarrow}
  X
  \,,
$$

where $X$ is any [[object]], and where $\ast$ is the [[terminal object]], and where $(-) \times (-) \colon \mathcal{C} \times \mathcal{C} \to \mathcal{C}$ denotes the [[Cartesian product]] [[functor]]. 

The [[reflective localization]] at such a class of morphisms $W_{\mathbb{A}}$ is often referred to as _homotopy localization at the object $\mathbb{A}$_ or similar. 

The idea is that if $\mathbb{A}$ is, or is regarded as, an [[interval object]], then "geometric" [[left homotopies]] between morphisms $X \to Y$ are, or would be, given by morphisms out of $X \times \mathbb{A}$, and hence forcing the projections $X \times \mathbb{A} \to X$ to be equivalences means forcing all morphisms to be _[[homotopy invariance|homotopy invariant]]_ with respect to $\mathbb{A}$.

Typically this is considered in the case that $\mathcal{C}$ is a [[locally presentable category]] with a [[small set]] of [[generators and relations|generating objects]] $G_i$ such that it becomes sufficient to enforce the localization only on the resulting [[small set]] of [[morphisms]] of the form $G_i \times (\mathbb{A} \to \ast)$.

## Examples


* The localization of the [[(∞,1)-category of (∞,1)-sheaves]] on the [[Nisnevich site]] at the [[affine line]] $\mathbb{A}^1$ is known as  _[[A1-homotopy theory]]_.

* The localization of [[smooth ∞-groupoids]] at the [[real line]] $\mathbb{R}^1$ is equivalently ([[geometrically discrete ∞-groupoids|geometrically discrete]]) [[∞-groupoids]]. 

  After realizing [[smooth ∞-groupoids]] as the [[(∞,1)-sheaves]] over [[CartSp]], $Smooth\infty Grpd \simeq Sh_{\infty}(CartSp)$, this follows from the following Prop. \ref{HomotopyLocalizationOverSiteOfAns}.


+-- {: .num_prop #HomotopyLocalizationOverSiteOfAns}
###### Proposition
**([[homotopy localization]] at $\mathbb{A}^1$ over the [[site]] of $\mathbb{A}^n$s)**

Let $\mathcal{C}$ be any [[site]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Coverage)), and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj, loc}$ for its local projective [[model category of simplicial presheaves]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#TopologicalLocalization)).

Assume that $\mathcal{C}$ contains an [[object]] $\mathbb{A} \in \mathcal{C}$, such that every other object is a [[finite product]] $\mathbb{A}^n \coloneqq \underset{n \; \text{factors}}{\underbrace{\mathbb{A} \times \cdots \times \mathbb{A}}}$, for some $n \in \mathbb{N}$. (In other words, assume that $\mathcal{C}$ is also the [[syntactic category]] of [[Lawvere theory]].)

Consider the  $\mathbb{A}^1$-[[homotopy localization]] ([this Def.](geometry+of+physics+--+categories+and+toposes#HomotopyLocalizationOfCombinatorialModelCategories)) of the [[(∞,1)-sheaf (∞,1)-topos]] over $\mathcal{C}$ ([this Prop.](geometry+of+physics+--+categories+and+toposes#TopologicalLocalization))

$$
  Sh_\infty(\mathcal{C})_{\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
      {\overset{L_{\mathbb{A}}}{\longleftarrow}}
      {\bot}
  Sh_\infty(\mathcal{C})
  \;\;
  \in
  Ho(CombModCat)
$$

hence the [[left Bousfield localization]] of [[model categories]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc,\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc}
  \;\;
  \in 
  CombModCat
$$

at the set of morphisms

$$
  S
    \;\coloneqq\;
  \big\{
    \mathbb{A}^n \times \mathbb{A}
      \overset{p_1}{\longrightarrow}
    \mathbb{A}^n
  \big\}
$$

(according to [this Prop.](geometry+of+physics+--+categories+and+toposes#ExistenceOfLeftBousfieldLocalization)).

Then this is [[equivalence of (∞,1)-categories|equivalent]] ([this Def.](geometry+of+physics+--+categories+and+toposes#HoCombModCat)) to [[∞Grpd]] ([this Example](geometry+of+physics+--+categories+and+toposes#InfinityGroupoid)),


$$
  \infty Grpd
  \;\simeq\;
  Sh_\infty(\mathcal{C})_{\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
      {\overset{L_{\mathbb{A}}}{\longleftarrow}}
      {\bot}
  Sh_\infty(\mathcal{C})
  \;\;
  \in
  Ho(CombModCat)
$$

in that the ([[constant functor]] $\dashv$ [[limit]])-[[adjunction]] ([this Def.](geometry+of+physics+--+categories+and+toposes#Limits))

\[
  \label{QuillenEquivalenceInABousfLocalization}
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj, loc, \mathbb{A}}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
      {\overset{ \phantom{AA}const\phantom{AA} }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
  \;\;\;\;
  \in 
  CombModCat
\]

is a [[Quillen equivalence]] ([this Def.](geometry+of+physics+--+homotopy+types#QuillenEquivalence)).

=--

+-- {: .proof}
###### Proof

First to see that (eq:QuillenEquivalenceInABousfLocalization) is a [[Quillen adjunction]]: Since we have a [[simplicial Quillen adjunction]] before localization

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
      {\overset{ \phantom{AA}const\phantom{AA} }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
$$

(by [this Example](geometry+of+physics+--+categories+and+toposes#HomotopyLimitOfSimplicialSets)) and since both [[model categories]] here are [[left proper model category|left proper]] [[simplicial model categories]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#SimplicialPresheavesIsProperCombinatorialSimplicial) and [this Prop.](geometry+of+physics+--+categories+and+toposes#ExistenceOfLeftBousfieldLocalization)), and since [[left Bousfield localization]] does not change the class of [[cofibrations]] ([this Def.](geometry+of+physics+--+categories+and+toposes#BousfieldLocalizationOfModelCategories)) it is sufficient to show that $\underset{\longleftarrow}{\lim}$ preserves [[fibrant objects]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#RecognitionOfSimplicialQuillenAdjunction)).

But by assumption $\mathcal{C}$ has a [[terminal object]] $\ast = \mathbb{A}^0$, which is hence the [[initial object]] of $\mathcal{C}^{op}$, so that the [[limit]] operation is given just by evaluation on that object:

$$
  \underset{\longleftarrow}{\lim}
  \mathbf{X}
  \;=\;
  \mathbf{X}(\mathbb{A}^0)
  \,.
$$

Hence it is sufficient to see that an injectively fibrant simplicial presheaf $\mathbf{X}$ is objectwise a [[Kan complex]]. This is indeed the case, by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModelCategoriesOfSimplicialPresheaves).

To check that (eq:QuillenEquivalenceInABousfLocalization) is actually a [[Quillen equivalence]], we check that the [[derived adjunction unit]] and [[derived adjunction counit]] are [[weak equivalences]]:

For $X \in sSet$ any simplicial set (necessarily cofibrant), the [[derived adjunction unit]] is 

$$
  X 
    \overset{id_X}{\longrightarrow} 
  const(X)(\mathbb{A}^0)
    \overset{ const(j_X)(\mathbb{A}^0) }{\longrightarrow}
  const(P X)(\mathbb{A}^0)
$$

where $X \overset{j_X}{\longrightarrow} P X$ is a [[fibrant replacement]] ([this Def.](geometry+of+physics+--+categories+and+toposes#FibrantCofibrantReplacementFunctorToHomotopyCategory)). But $const(-)(\mathbb{A}^0)$ is clearly the [[identity functor]] and the plain adjunction unit is the [[identity morphism]], so that this composite is just $j_X$ itself, which is indeed a weak equivalence.

For the other case, let $\mathbf{X} \in [\mathcal{C}^{op}, sSet_{Qu}]_{inj, loc, \mathbb{A}^1}$ be fibrant. This means (by [this Prop.](geometry+of+physics+--+categories+and+toposes#ExistenceOfLeftBousfieldLocalization)) that $\mathbf{X}$ is fibrant in the injective [[model structure on simplicial presheaves]] as well as in the local model structure, and is a derived-$\mathbb{A}^1$-[[local object]] ([this Def.](geometry+of+physics+--+categories+and+toposes#DerivedLocalObjects)), in that the [[derived hom-functor]] out of any $\mathbb{A}^n \times \mathbb{A}^1 \overset{p_1}{\longrightarrow} \mathbb{A}^n$  into $\mathbf{X}$ is a [[weak homotopy equivalence]]:

$$
  \mathbb{R}Hom( p_1 )
  \;\colon\;
  \mathbb{R}Hom( \mathbb{A}^n , \mathbf{X})
  \overset{\in W}{\longrightarrow}
  \mathbb{R}Hom( \mathbb{A}^n \times \mathbb{A}^1 , \mathbf{X})
$$

But since $\mathbf{X}$ is fibrant, this derived hom is equivalent to the ordinary [[hom-functor]] ([this Lemma](geometry+of+physics+--+categories+and+toposes#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)), and hence with the [[Yoneda lemma]] ([this Prop.](geometry+of+physics+--+categories+and+toposes#YonedaLemma)) we have that

$$
  \mathbf{X}(p_1)
  \;\colon\;
  \mathbf{X}(\mathbb{A}^n)
  \overset{\in W}{\longrightarrow}
  \mathbf{X}(\mathbb{A}^{n+1})
$$

is a weak equivalence, for all $n \in \mathbb{N}$. By [[induction]] on $n$ this means that in fact 

$$
  \mathbf{X}(\mathbb{A}^0)
   \overset{\in W}{\longrightarrow} 
  \mathbf{X}(\mathbb{A}^n) 
$$

is a weak equivalence for all $n \in \mathbb{N}$. But these are just the components of the [[adjunction counit]]

$$
  const (\mathbf{X}(\mathbb{A}^0))
   \underoverset{\in W}{\epsilon}{\longrightarrow}
  \mathbf{X}
$$

which is hence also a weak equivalence. Hence for the [[derived adjunction counit]]

$$
  const (Q \mathbf{X})(\mathbb{A}^0)
    \overset{const(p_{\mathbf{X}}(\mathbb{A}^0))}{\longrightarrow}
  const (\mathbf{X}(\mathbb{A}^0))
   \underoverset{\in W}{\epsilon}{\longrightarrow}
  \mathbf{X}
$$

to be a weak equivalence, it is now sufficient to see that the value of a [[cofibrant replacement]] $p_{\mathbf{X}}$ on $\mathbb{A}^0$ is a weak equivalence. But by definition of the weak equivalences of simplicial presheaves these are objectwise weak equivalences.


=--

## References

* {#MorelVoevodsky99} [[Fabien Morel]], [[Vladimir Voevodsky]], Def. 3.1 in _$\mathbb{A}^1$-homotopy theory of schemes_, Publications Mathématiques de l'IHÉS, Volume 90 (1999), p. 45-143  ([Numdam:PMIHES_1999__90__45_0](http://www.numdam.org/item/?id=PMIHES_1999__90__45_0) [K-Theory:0305](http://www.math.uiuc.edu/K-theory/0305/) )

For more references see also at _[[motivic homotopy theory]]_.

[[!redirects homotopy localization]]
[[!redirects homotopy localizations]]

[[!redirects homotopy localization at an object]]
[[!redirects homotopy localizations at an object]]

[[!redirects localization at an object]]
[[!redirects localizations at an object]]

[[!redirects localization at objects]]
[[!redirects localizations at objects]]
