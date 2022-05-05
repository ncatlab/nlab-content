
**[[generalized spaces]] via [[generators and relations]]:**

| $\phantom{A}$[[free cocompletion]]$\phantom{A}$ <br/> $\phantom{A}=$[[category of presheaves|presheaves]]$\phantom{A}$  | $\phantom{A}$[[reflective subcategory]]$\phantom{A}$ <br/> $\phantom{A}$of [[category of presheaves|presheaves]]$\phantom{A}$ | $\phantom{A}$[[locally presentable category|loc. presentable category]]$\phantom{A}$ | $\phantom{A}$[[sheaf topos]]$\phantom{AAAA}$ |  
|-----|---|-------|------|
| $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAA}}{\longrightarrow}}{\overset{}{\longleftarrow}}{\simeq} [\mathcal{C}^{op},Set]$  | $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAAA}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{\text{left exact}}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ |


+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be an [[∞-cohesive site]], and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj, loc}$ for its local projective [[model category of simplicial presheaves]].

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

Then this is [[equivalence of (∞,1)-categories|equivalent]] ([this Def.](geometry+of+physics+--+categories+and+toposes#HoCombModCat)) to [[∞Grpd]] (Example \ref{#InfinityGroupoid}),


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
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc,\mathbb{A}}
    \underoverset
      {\underset{ \phantom{AA}const\phantom{AA} }{\longleftarrow}}
      {\overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}}
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
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
    \underoverset
      {\underset{ const }{\longleftarrow}}
      {\overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}}
      {\bot}
  sSet_{Qu}    
$$

(by [this Example](geometry+of+physics+--+categories+and+toposes#HomotopyLimitOfSimplicialSets)) and since both [[model categories]] here are [[left proper model category|left proper]] [[simplicial model categories]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#SimplicialPresheavesIsProperCombinatorialSimplicial)), and since [[left Bousfield localization]] does not change the class of [[cofibrations]] ([this Def.](geometry+of+physics+--+categories+and+toposes#BousfieldLocalizationOfModelCategories)) it is sufficient to show that $const$ preserves [[fibrant objects]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#RecognitionOfSimplicialQuillenAdjunction)).

By [this Prop.](geometry+of+physics+--+categories+and+toposes#ExistenceOfLeftBousfieldLocalization) this means to check that constant [[simplicial presheaves]] are both Cech-local and $\mathbb{A}$-local. The first of these is proven at _[[∞-cohesive site]]_, the second is immediate.

Now to see that this Quillen adjunction is a [[Quillen equivalence]]...

=--



