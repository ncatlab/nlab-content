Figure:

$$
\begin{svg}<svg width="113" height="97" xmlns="http://www.w3.org/2000/svg" xmlns:svg="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:math="http://www.w3.org/1998/Math/MathML" se:nonce="23626">
 <g class="layer">
  <title>Layer 1</title>
  <foreignObject height="22" width="14" font-size="16" id="svg_23626_1" y="36" x="2">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>C</mi>
     </mrow>
     <annotation encoding="application/x-tex">C</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_23626_2" height="22" width="14" font-size="16" y="35" x="99">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>D</mi>
     </mrow>
     <annotation encoding="application/x-tex">D</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_23626_8" height="22" width="14" font-size="16" y="0" x="50">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>F</mi>
     </mrow>
     <annotation encoding="application/x-tex">F</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_23626_14" height="22" width="14" font-size="16" y="75" x="49">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>G</mi>
     </mrow>
     <annotation encoding="application/x-tex">G</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path id="svg_23626_20" d="m15,34c20,-20 60,-20 80,0" stroke-width="2" stroke="#000000" fill="none" marker-end="url(#se_marker_end_svg_23626_20)"/>
  <path marker-end="url(#se_marker_end_svg_23626_3)" fill="none" stroke="#000000" stroke-width="2" d="m15,54c20,20 60,20 80,0" id="svg_23626_3"/>
  <g id="svg_23626_11">
   <line fill="none" stroke="#000000" stroke-width="6" x1="56" y1="24" x2="56" y2="62" id="svg_23626_6"/>
   <line id="svg_23626_9" y2="62" x2="56" y1="24" x1="56" stroke-width="2" stroke="#ffffff" fill="none"/>
   <path fill="none" stroke="#000000" stroke-width="2" d="m49,58l7,7l7,-7" id="svg_23626_7"/>
  </g>
 </g>
 <defs>
  <marker id="se_marker_end_svg_23626_20" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_23626_4" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#000000" stroke="#000000" stroke-width="10"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_23626_3">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_23626_5"/>
  </marker>
 </defs>
</svg>\end{svg}
$$

**[[generalized spaces]] via [[generators and relations]]:**

| $\phantom{A}$[[free cocompletion]]$\phantom{A}$ <br/> $\phantom{A}=$[[category of presheaves|presheaves]]$\phantom{A}$  | $\phantom{A}$[[reflective subcategory]]$\phantom{A}$ <br/> $\phantom{A}$of [[category of presheaves|presheaves]]$\phantom{A}$ | $\phantom{A}$[[locally presentable category|loc. presentable category]]$\phantom{A}$ | $\phantom{A}$[[sheaf topos]]$\phantom{AAAA}$ |  
|-----|---|-------|------|
| $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAA}}{\longrightarrow}}{\overset{}{\longleftarrow}}{\simeq} [\mathcal{C}^{op},Set]$  | $\phantom{A}\mathbf{H} \underoverset{\underset{\phantom{AAAA}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ | $\phantom{A}\mathbf{H} \underoverset{\underset{\text{accessible}}{\hookrightarrow}}{\overset{\text{left exact}}{\longleftarrow}}{\bot} [\mathcal{C}^{op}, Set]$ |


+-- {: .num_prop}
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

(by [this Example](geometry+of+physics+--+categories+and+toposes#HomotopyLimitOfSimplicialSets)) and since both [[model categories]] here are [[left proper model category|left proper]] [[simplicial model categories]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#SimplicialPresheavesIsProperCombinatorialSimplicial)), and since [[left Bousfield localization]] does not change the class of [[cofibrations]] ([this Def.](geometry+of+physics+--+categories+and+toposes#BousfieldLocalizationOfModelCategories)) it is sufficient to show that $\underset{\longleftarrow}{\lim}$ preserves [[fibrant objects]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#RecognitionOfSimplicialQuillenAdjunction)).

But by assumption $\mathcal{C}$ has a [[terminal object]] $\ast = \mathbb{A}^0$, which is hence the [[initial object]] of $\mathcal{C}^{op}$, so that the [[limit]] operation is given just by evaluation on that object:

$$
  \underset{\longleftarrow}{\lim}
  \mathbf{X}
  \;=\;
  \mathbf{X}(\mathbb{A}^0)
  \,.
$$

Hence it is sufficient to see that an injectively fibrant simplicial presheaf $\mathbf{X}$ is objectwise a [[Kan complex]]. This is indeed the case, by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModelCategoriesOfSimplicialPresheaves).

To check that (eq:QuillenEquivalenceInABousfLocalization) is actually a [[Quillen equivalence]], we check that the derived adjunction unit and counit are equivalences:

For $X \in sSet$ any simplicial set (necessarily cofibrant), the derived [[adjunction unit]] is 

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

which is hence also a weak equivalence. Hence for the derived adjunction counit

$$
  const (Q \mathbf{X})(\mathbb{A}^0)
    \overset{const(p_{\mathbf{X}}(\mathbb{A}^0))}{\longrightarrow}
  const (\mathbf{X}(\mathbb{A}^0))
   \underoverset{\in W}{\epsilon}{\longrightarrow}
  \mathbf{X}
$$

to be a weak equivalence, it is now sufficient to see that the value of a [[cofibrant replacement]] $p_{\mathbf{X}}$ on $\mathbb{A}^0$ is a weak equivalence. But by definition of the weak equivalences of simplicial presheaves these are objectwise weak equivalences.


=--


