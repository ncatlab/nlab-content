
**[[generalized spaces]] via [[generators and relations]]:**

| $\phantom{A}$[[free cocompletion]]$\phantom{A}$ <br/> $\phantom{A}=$[[category of presheaves|presheaves]]$\phantom{A}$  | $\phantom{A}$[[reflective subcategory]]$\phantom{A}$ <br/> $\phantom{A}$of [[category of presheaves|presheaves]]$\phantom{A}$ | $\phantom{A}$[[locally presentable category|loc. presentable category]]$\phantom{A}$ | $\phantom{A}$[[sheaf topos]]$\phantom{AAAA}$ |  
|-----|---|-------|------|
| $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAA}}{\longrightarrow}}{\overset{}{\longleftarrow}}{\simeq} [\mathcal{C}^{op},Set]$  | $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAAA}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{\text{left exact}}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ |


+-- {: .num_prop}
###### Proposition

Let $\mathcal{C}$ be an [[∞-cohesive site]], and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj, loc}$ for its local projective [[model category of simplicial presheaves]].

Assume that $\mathcal{C}$ contains an [[object]] $\mathbb{A} \in \mathcal{C}$, such that every other object is a [[finite product]] $\mathbb{A}^n \coloneqq \underset{n \; \text{factors}}{\underbrace{\mathbb{A} \times \cdots \times \mathbb{A}}}$, for some $n \in \mathbb{N}$. (In other words, assume that $\mathcal{C}$ is also the [[syntactic category]] of [[Lawvere theory]].)

Consider the [[reflective localization|reflective]] $\mathbb{A}^1$-[[localization of an (∞,1)-category|localization]] (in the sense of  [[localization at an object]]) of the [[(∞,1)-sheaf (∞,1)-topos]]

$$
  Sh_\infty(\mathcal{C})_{\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}\iota\phantom{AA}}{\hookrightarrow}}
      {\overset{L}{\longleftarrow}}
      {\bot}
  Sh_\infty(\mathcal{C})
$$

hence the [[left Bousfield localization]] of [[model categories]]

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc,\mathbb{A}}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{id}{\longleftarrow}}
      {\phantom{{}_{Qu}}\bot_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc}
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

Then this is [[equivalence of (∞,1)-categories|equivalent]] to [[∞Grpd]], in that the ([[constant functor]] $\dashv$ [[limit]])-[[adjunction]]

\[
  \label{QuillenEquivalenceInABousfLocalization}
  [\mathcal{C}^{op}, sSet_{Qy}]_{proj,loc,\mathbb{A}}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} = ev_{\ast}}{\longrightarrow}}
      {\overset{ const }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
\]

is a [[Quillen equivalence]] ([this Def.](geometry+of+physics+--+homotopy+types#QuillenEquivalence)).

=--

+-- {: .proof}
###### Proof

First to see that (eq:QuillenEquivalenceInABousfLocalization) is a [[Quillen adjunction]]. By ... we have a [[simplicial Quillen adjunction]] before localization

$$
  [\mathcal{C}^{op}, sSet_{Qy}]_{proj}
    \underoverset
      {\underset{ \underset{\longleftarrow}{\lim} = ev_{\ast}}{\longrightarrow}}
      {\overset{ const }{\longleftarrow}}
      {\bot}
  sSet_{Qu}    
$$

and hence by [this Prop.](Quillen+adjunction#RecognitionOfSimplicialQuillenAdjunctions) it is sufficient to see that $const$ sends [[Kan complexes]] to fibrant objects in $[\mathcal{C}^{op}, sSet_{Qu}]_{proj,loc,\mathbb{A}}$. But constant presheaves are Cech-local by the discussion at _[[∞-cohesive site]]_ and are triviallay $\mathbb{A}$-local.

Now to see that this Quillen adjunction is a [[Quillen equivalence]]...

=--



