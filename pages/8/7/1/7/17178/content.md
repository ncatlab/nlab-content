
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[stable homotopy theory]], a _sequential ([[prespectrum|pre-]])[[spectrum]]_ $E$ (also _Boardman spectrum_, after ([Boardman 65](#Boardman65))) is a sequence of [[pointed homotopy types]] ([[pointed topological spaces]], pointed [[simplicial sets]]) $E_n$, for $n \in \mathbb{N}$, together with maps $\Sigma E_n \to E_{n+1}$ from the [[reduced suspension]] of one into the next space in the sequence.

This is the original definition of _[[spectrum]]_ (or [[pre-spectrum]]), and still, the one predominantly meant to be default, as used in, say, the [[Brown representability theorem]]. But in view of many other definitions (all giving rise to equivalent [[stable homotopy theory]]) that involve systems of spaces indexed on more than just the integers (such as [[coordinate-free spectra]], [[excisive functors]], [[equivariant spectra]]) or that are of different flavor altogether (such as [[combinatorial spectra]]), one says _sequential spectrum_ for emphasis (e.g. [Schwede 12, def. 2.1](#Schwede12)).


## Definition

### In components

In what follows, [[sSet]] denotes the [[category]] of [[simplicial sets]] and $sSet^{\ast/}$ the category $\ast/sSet$ of [[pointed objects|pointed]] simplicial sets (the [[undercategory]] under the [[terminal object]] $\ast$), which may be thought of as a possible base of [[enriched category|enrichment]]. 

+-- {: .num_defn #SequentialSpectra}
###### Definition

A _sequential_ [[pre-spectrum]] in [[simplicial sets]], is an $\mathbb{N}$-[[graded object|graded]] [[pointed object|pointed]] [[simplicial set]] $X_\bullet$ equipped with morphisms $\sigma_n \colon S^1 \wedge X_n \to X_{n+1}$ for all $n \in \mathbb{N}$, where $S^1 \coloneqq \Delta[1]/\partial\Delta[1]$ is the minimal simplicial [[circle]], and where $\wedge$ is the [[smash product]] of [[pointed objects]].

A [[homomorphism]] $f \colon X \to Y$ of sequential prespectra is a collection $f_\bullet \colon X_\bullet \to Y_\bullet$ of homomorphisms of [[pointed simplicial sets]], such that all [[diagrams]] of the form

$$
  \array{
    S^1 \wedge X_n &\stackrel{S^1 \wedge f_n}{\longrightarrow}& S^1 \wedge Y_n
    \\
    \downarrow^{\mathrlap{\sigma_n^X}} && \downarrow^{\mathrlap{\sigma_n^Y}}
    \\
    X_{n+1} &\stackrel{f_{n+1}}{\longrightarrow}& Y_{n+1}
  }
$$

[[commuting diagram|commute]].

This gives a [[category]] $SeqSpec(sSet)$ of sequential prespectra.

=--

+-- {: .num_example #SmashProductOfSpectrumWithSimplicialSet}
###### Example

For $X \in SeqSpec(sSet)$ and $K \in $ [[sSet]], hence $K_+ \in sSet^{\ast/}$ then $X \wedge K_+$ is the spectrum which is degreewise given by the [[smash product]] of [[pointed objects]]

$$
  (X \wedge K_+)_n \coloneqq (X_n \wedge K_+)
$$

And whose structure maps are given by

$$
  S^1 \wedge (X_n \wedge K_+) \simeq (S^1 \wedge X_n) \wedge K_+ \stackrel{\sigma_n \wedge K_+}{\longrightarrow} X_{n+1}\wedge K_+
  \,.
$$

=--

+-- {: .num_prop #SimplicialEnrichment}
###### Proposition

The category $SeqSpec$ of def. \ref{SequentialSpectra} becomes a [[simplicially enriched category]] (in fact an $sSet^{\ast/}$-[[enriched category]]) with [[hom objects]] $[X,Y]\in sSet$ given by

$$
  [X,Y]_n \coloneqq Hom_{SeqSpec(sSet)}(X\wedge \Delta[n]_+,Y)
  \,.
$$

=--

+-- {: .num_defn #OmegaSpectrum}
###### Definition

An _[[Omega-spectrum]]_ in the following is a sequential prespectrum $X$, def. \ref{SequentialSpectra}, such that after [[geometric realization]]/[[Kan fibrant replacement]] ${\vert -\vert}$ the smash$\dashv$pointed-hom [[adjuncts]]

$$
  {\vert X_n\vert} \stackrel{}{\longrightarrow} {\vert X^{n+1}\vert}^{{\vert S^1\vert}}
$$

of the structure maps ${\vert \sigma_n\vert}$ are [[weak homotopy equivalences]].

=--

### As diagram spectra
 {#AsDiagramSpectra}

+-- {: .num_defn #CategoriesOfStandardSpheres}
###### Definition

Write $S^1_{std} \coloneqq \Delta[1]/\partial\Delta[1]\in sSet^{\ast/}$ for the standard minimal pointed simplicial [[1-sphere]].

Write 

$$
  \iota \;\colon\; StdSpheres \longrightarrow sSet^{\ast/}_{fin}
$$

for the non-full $sSet^{\ast/}$-[[enriched category|enriched]] [[subcategory]] of pointed [[simplicial object|simplicial]] [[finite sets]], def. \ref{SimplicialSetsPointedAndFinite} whose

* [[objects]] are the [[smash product]] powers $S^n_{std} \coloneqq (S^1_{std})^{\wedge^n}$ (the standard minimal simplicial [[n-spheres]]);

* [[hom-objects]] are

  $$
    [S^{n}_{std}, S^{n+k}_{std}]_{StdSpheres}
    \coloneqq
    \left\{
      \array{
        \ast & for & k \lt 0
        \\
        im(S^{k}_{std} \stackrel{}{\to} [S^n_{std}, S^{n+k}_{std}]_{sSet^{\ast/}_{fin}})
        & otherwise
      }
    \right.
  $$

=--

([Lydakis 98, def. 4.2](#Lydakis98)), see also ([MMSS 00](#MMSS00)) [this example](Model+categories+of+diagram+spectra#SequentialSpectraAsFunctorsOnFreeSSequModules).



+-- {: .num_prop #SequentialSpectraAsDiagramSpectra}
###### Proposition

There is an $sSet^{\ast/}$-[[enriched functor]] 

$$
  (-)^seq
  \;\colon\;
  [StdSpheres,sSet^{\ast/}]
    \longrightarrow
  SeqSpec(sSet)
$$

(from the category of $sSet^{\ast/}$-[[enriched presheaves|enriched copresheaves]] on the categories of standard simplicial spheres of def. \ref{CategoriesOfStandardSpheres} to the category of [[sequential prespectra]] in [[sSet]]) given on objects by sending $X \in [StdSpheres,sSet^{\ast/}]$ to the sequential prespectrum $X^{seq}$ with components

$$
  X^{seq}_n \coloneqq X(S^n_{std})
$$

and with structure maps

$$
  \frac{S^1_{std} \wedge X^{seq}_n \stackrel{\sigma_n}{\longrightarrow} X^{seq}_n}{S^1_{std} \longrightarrow [X^{seq}_n, X^{seq}_{n+1}]}
$$

given by

$$
  S^1_{std} 
    \stackrel{\widetilde{id}}{\longrightarrow}
  [S^n_{std}, S^{n+1}_{std}]
    \stackrel{X_{S^n_{std}, S^{n+1}_{std}}}{\longrightarrow}
  [X^{seq}_n, X^{seq}_{n+1}]
  \,.
$$

This is an $sSet^{\ast/}$ [[enriched category theory|enriched]] [[equivalence of categories]].

=--

([Lydakis 98, prop. 4.3](#Lydakis98)), see also ([MMSS 00](#MMSS00))


+-- {: .num_remark}
###### Remark

Prop. \ref{SequentialSpectraAsDiagramSpectra} is a special case of a more general statement expressing structured spectra equivalently as enriched functors. Analogous statements hold for [[symmetric spectra]] and [[orthogonal spectra]]. See at _[[Model categories of diagram spectra]]_ [this lemma](Model+categories+of+diagram+spectra#SModulesAsEnrichedFunctors) and [this example](Model+categories+of+diagram+spectra#SequentialSpectraAsFunctorsOnFreeSSequModules).

=--


## Properties

### Limits and colimits

+-- {: .num_prop #LimitsAndColimitsOfSequentialSpectra}
###### Proposition

The category $SeqSpec(Top_{cq})$ of sequential spectra (def. \ref{SequentialSpectra}) has all [[limits]] and [[colimits]], and they are computed objectwise: 

Given

$$
  X_\bullet
    \;\colon\;
  I
    \longrightarrow
  SeqSpec(Top_{cg})
$$

a [[diagram]] of sequential spectra, then:

1. its colimiting spectrum has component spaces the colimit of the component spaces formed in $Top_{cg}$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop) and [this corollary](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)):

   $$
     (\underset{\longrightarrow}{\lim}_i X(i))_n
     \simeq
      \underset{\longrightarrow}{\lim}_i X(i)_n
      \,,
   $$

1. its limiting spectrum has component spaces the limit of the component spaces formed in $Top_{cg}$ (via [this prop.](Introduction+to+Stable+homotopy+theory+--+P#DescriptionOfLimitsAndColimitsInTop) and [this corollary](Introduction+to+Stable+homotopy+theory+--+P#kTopIsCoreflectiveSubcategory)):

   $$
     (\underset{\longleftarrow}{\lim}_i X(i))_n
     \simeq
      \underset{\longleftarrow}{\lim}_i X(i)_n
      \,;
   $$

Moreover:

1. the colimiting spectrum has structure maps in the sense of def. \ref{SequentialSpectra} given by

   $$
     S^1 \wedge (\underset{\longrightarrow}{\lim}_i X(i)_n)
     \simeq
     \underset{\longrightarrow}{\lim}_i ( S^1 \wedge X(i)_n )
     \overset{\underset{\longrightarrow}{\lim}_i \sigma_n^{X(i)}}{\longrightarrow}
     \underset{\longrightarrow}{\lim}_i X(i)_{n+1}
   $$

   where the first isomorphism exhibits that $S^1 \wedge(-)$ preserves all colimits, since it is a [[left adjoint]] by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory};

1. the limiting spectrum has adjunct structure maps in the sense of def. \ref{SequentialSpectrumViaAdjunctStructureMaps} given by

   $$
     \underset{\longleftarrow}{\lim}_i X(i)_n
      \overset{\underset{\longleftarrow}{\lim}_i \tilde \sigma_n^{X(i)}}{\longrightarrow}
     \underset{\longleftarrow}{\lim}_i Maps(S^1, X(i)_n)_\ast 
     \simeq
     Maps(S^1, \underset{\longleftarrow}{\lim}_i X(i)_n)_\ast
   $$

   where the last isomorphism exhibits that $Maps(S^1,-)_\ast$ preserves all limits, since it is a [[right adjoint]] by prop. \ref{SuspensionAndLoopAdjunctionInClassicalHomotopyTheory}.

=--

+-- {: .proof}
###### Proof

That the limits and colimits exist and are computed objectwise follows via prop. \ref{SequentialSpectraAsDiagramSpectra} from the general statement for categories of topological functors ([prop.](Introduction+to+Stable+homotopy+theory+--+P#TopologicallyEnrichedCopresheavesHaveAllLimitsAndColimits)). But it is also immediate to directly check the [[universal property]].

=--

+-- {: .num_example #WedgeSumOfSpectra}
###### Example

The [[coproduct]] of [[spectra]] $X, Y \in SeqSpec(Top_{cg})$, called the **wedge sum of spectra** 

$$
  X \vee Y
    \coloneqq
  X \sqcup Y
$$

is componentwise the [[wedge sum]] of pointed topological spaces ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#WedgeSumAsCoproduct))

$$
  (X \vee Y)_n
  =
  X_n \vee Y_n
$$

with structure maps

$$
  \sigma_n^{X \vee Y}
    \;\colon\;
  S^1 \wedge (X \vee Y)
    \simeq
  S^1 \wedge X \,\vee\, S^1 \wedge Y
    \overset{(\sigma_n^X, \sigma_n^Y)}{\longrightarrow}
  X_{n+1} \vee Y_{n+1}
  \,.
$$


=--


### Tensoring and powering over pointed spaces

The following defines [[tensoring]] and [[powering]] of sequential spectra over [[pointed topological spaces]]/[[pointed simplicial sets]].

+-- {: .num_defn #TensoringAndPoweringOfSequentialSpectra}
###### Definition

Let $X$ be a sequential spectrum and $K$ a [[pointed topological space]]/[[pointed simplicial set]]. Then

1. $X \wedge K$ is the sequential spectrum with 

   * $(X \wedge K)_n \coloneqq X_n \wedge K$ ([[smash product]])

   * $\sigma_n^{X\wedge K} \coloneqq \sigma_n^{X} \wedge id_{K}$.

1. $X^K$ is the sequential spectrum with

   * $(X^K)_n \coloneqq (X_n)^K$ ([[pointed mapping space]])

   * $\sigma_n^{(X^k)} \colon S^1 \wedge X_n^K \to (S^1 \wedge X_n)^K \overset{(\sigma_n)^K}{\longrightarrow} (X_{n+1})^K$.
 
=--




### Model category structures
 {#ModelCategoryStructures}

There is a standard [[model structure on spectra]] for sequential spectra in [[Top]] the [[model structure on topological sequential spectra]] ([Kan 63](#Kan63), [MMSS 00](#MMSS00))  and in [[simplicial sets]], the [[Bousfield-Friedlander model structure]] ([Bousfield-Friedlander 78](#BousfieldFriedlander78)).

The _strict_ Bousfield-Friedlander model structure (of which the actual stable version is the [[Bousfield localization of model categories|left Bousfield localization]] at the [[stable weak homotopy equivalences]]) is equivalently the [[projective model structure on enriched functors]] for the presentation of sequential spectra from prop. \ref{SequentialSpectraAsDiagramSpectra}:

$$
  SeqSpec(sSet)_{stable}
  \stackrel{\longleftarrow}{\overset{Bousf.\;loc}{\longrightarrow}}
  SeqSpec(sSet)_{strict}
  =
  [StdSpheres, Top^{\ast/}_{Quillen}]_{proj}
  \,.
$$

### Suspension and looping
 {#SuspensionAndLooping}

There are _three_ common constructions of looping and suspension of sequential spectra (with analogues for [[highly structured spectra]]). While they are not isomorphic, they are stably equivalent. 

+-- {: .num_defn #ShiftedSpectrum}
###### Definition

For $X$ a [[sequential spectrum]] and $k \in \mathbb{Z}$, the $k$-fold **shifted spectrum** of $X$ is the sequential spectrum denoted $X[k]$ given by

* $(X[k])_n \coloneqq \left\{ \array{X_{n+k} & for \; n+k \geq 0 \\ \ast & otherwise } \right. $;

* $\sigma_n^{X[k]} \coloneqq \left\{ \array{ \sigma^X_{n+k} & for \; n+k \geq 0 \\ 0 & otherwise} \right. $.

=--


+-- {: .num_defn #SequentialSpectrumRealSuspension}
###### Definition

For $X$ a sequential spectrum, then

1. the **real suspension** of $X$ is $X \wedge S^1$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra};

1. the **real looping** of $X$ is $X^{S^1}$ according to def. \ref{TensoringAndPoweringOfSequentialSpectra}.

=--

+-- {: .num_defn #SequentialSpectrumFakeSuspension}
###### Definition

For $X$ a sequential spectrum, then

1. the **fake suspension** of $X$ is the sequential spectrum $\Sigma X$ with

   1. $(\Sigma X)_n \coloneqq S^1 \wedge X_n$

   1. $\sigma_n^{\Sigma X} \coloneqq S^1 \wedge (\sigma_n)$.

1. the **fake looping** of $X$ is the sequential spectrum $\Omega X$ with

   1. $(\Omega X)_n \coloneqq (X_n)^{S^1}$;

   1. $\tilde \sigma_n^{\Omega X} \coloneqq (\sigma_n)^{S^1}$.  

Here $\tilde \Sigma_n$ denotes the $(\Sigma\dashv \Omega)$-[[adjunct]] of $\sigma_n$.

=--

e.g. ([Jardine 15, section 10.4](#Jardine15)).

+-- {: .num_defn #ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra}
###### Remark

The looping and suspension operations in def. \ref{SequentialSpectrumRealSuspension} and def. \ref{SequentialSpectrumFakeSuspension} commute with shifting, def. \ref{ShiftedSpectrum}. Therefore in expressions like $\Sigma (X[1])$ etc. we may omit the parenthesis.

=--


+-- {: .num_defn }
###### Definition

The canonical morphism

1. $\Sigma X \longrightarrow X[1]$ is given in degree $n$ by $\sigma_n^X$.

1. $X[-1] \longrightarrow \Omega X$ is given in degree $n$ by $\tilde \sigma^X_{n-1}$.

=--

+-- {: .num_prop #AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}
###### Proposition

The constructions from def. \ref{ShiftedSpectrum}, def. \ref{SequentialSpectrumRealSuspension} and def. \ref{SequentialSpectrumFakeSuspension} form pairs of [[adjoint functors]] $SeqSpec \to SeqSpec$ like so:

1. $(-)[1] \;\dashv\; (-)[-1] \;\dashv\; (-)[1] \;\dashv\; \cdots $;

1. $(-)\wedge S^1 \dashv (-)^{S^1}$;

1. $\Sigma \dashv \Omega$.

=--

+-- {: .proof}
###### Proof

The first is immediate from the definition. 

The second is just degreewise the adjunction [[smash product]]$\dashv$[[pointed mapping space]] (discussed [here](pointed+object#ClosedMonoidalStructure)), since by definition the smash product and mapping spaces here do not interact non-trivially with the structure maps.

The third follows by applying the [[smash product]]$\dashv$[[pointed mapping space]]-adjunction isomorphism twice, like so:

Morphisms $f\colon \Sigma X \to Y$ are in components given by commuting diagrams of this form:

$$
  \array{  
    S^1 \wedge S^1 \wedge X_{n} 
      &\overset{S^1 \wedge f_{n}}{\longrightarrow}&
    S^1 \wedge Y_{n}
    \\
    {}^{\mathllap{S^1 \wedge \sigma_n^X}}\downarrow 
     && 
    \downarrow^{\mathrlap{\sigma^Y_n}}
    \\
    S^1 \wedge X_{n+1} &\underset{f_{n+1}}{\longrightarrow}& Y_{n+1}
  }
  \,.
$$

Applying the adjunction isomorphism diagonally gives a bijection to diagrams of this form:

$$
  \array{
   S^1 \wedge X_n &\overset{f_n}{\longrightarrow}& Y_n
   \\
   {}^{\mathllap{\sigma^X_n}}\downarrow && \downarrow^{\mathrlap{\tilde \sigma^Y_n}}
   \\
   X_{n+1} &\underset{\tilde f_{n+1}}{\longrightarrow}& (Y_{n+1})^{S^1}
  }
  \,.
$$

Then applying the same isomorphism diagonally once more gives a further bijection to  commuting diagrams of this form:

$$
  \array{
    X_n &\overset{\tilde f_n}{\longrightarrow}& (Y_n)^{S^1}
    \\
    {}^{\mathllap{\tilde \sigma_n}}\downarrow 
      && 
    \downarrow^{\mathrlap{(\tilde \sigma^Y_n)^{S^1}}}
    \\
    (X_{n+1})^{S^1}
    &\underset{(\tilde f_n)^{S^1}}{\longrightarrow}&
    \left((Y_{n+1})^{S^1}\right)^{S^1}
  }
  \,.
$$

This finally equivalently exhibits morphisms of the form

$$
  X \longrightarrow \Omega Y
  \,.
$$

=--

+-- {: .num_example}
###### Example

For $X$ a sequential spectrum, then $X[-1][1] = X$ while $X[1][-1]$ is $X$ with its 0-th component space set to the point. The [[adjunction unit]] $X \to X[1][-1]$ has components

$$
  \array{
     \vdots && \vdots
     \\
     X_2 &\overset{id}{\longrightarrow}& X_2
     \\
     X_1 &\overset{id}{\longrightarrow}& X_1
     \\
     \underbrace{X_0} &\overset{0}{\longrightarrow}& \underbrace{\;\ast\;}
     \\
     X &\overset{\eta}{\longrightarrow}& X[1][-1]
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $X$ a sequential spectrum, then (using remark \ref{ShiftingCommutesWithLoopingAndSuspensionOfSequentialSpectra} to suppress parenthesis)

1. the structure maps constitute a homomorphism

   $$
     \Sigma X[-1]
     \longrightarrow
     X
   $$

   and this is a stable equivalence.

1. the adjunct structure maps constitute a homomorphism

   $$
     X
     \longrightarrow
     \Omega X[1]
     \,.
   $$

   If $X$ is an [[Omega-spectrum]] (def. \ref{OmegaSpectrum}) then this is a weak equivalence in the strict model structure, hence in particular, a stable equivalence.

=--

+-- {: .proof}
###### Proof

The diagrams that need to commute for the structure maps to give a homomorphism as claimed are in degree 0 this one

$$
  \array{
    S^1 \wedge S^1 \wedge \ast &\overset{0}{\longrightarrow}& X_0
    \\
    {}^{\mathllap{S^1 \wedge 0}}\downarrow && \downarrow^{\mathrlap{\sigma_0}}
    \\
    S^1 \wedge X_0 &\underset{\sigma_0}{\longrightarrow}& X_1
  }
$$

and in degree $n \geq 1$ these:

$$
  \array{
     S^1 \wedge S^1 \wedge X_{n-1} 
        &\overset{S^1 \wedge \sigma_{n-1}}{\longrightarrow}& 
     X_n
     \\
     {}^{\mathllap{S^1 \wedge \sigma_{n-1}}}\downarrow
       &&
     \downarrow^{\mathrlap{\sigma_n}}
     \\
     S^1 \wedge X_{n} 
       &\underset{\sigma_n}{\longrightarrow}& 
     X_{n+1}
  }
  \,.
$$

But in all these cases, commutativity it trivially satisfied. 

Now as in the proof of prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}, under applying the $(S^1\wedge (-)) \dashv (-)^{S^1}$-adjunction isomorphism twice, these diagrams are in bijection to diagrams for $n \geq 1$ of the form

$$
  \array{
    X_{n-1} &\overset{\tilde \sigma_{n-1}}{\longrightarrow}& (X_n)^{S^1}
    \\
    {}^{\mathllap{\tilde \sigma_{n-1}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\tilde \sigma_n}}
    \\
    (X_n)^{S^1}
      &\underset{(\tilde \sigma_n)^{S^1}}{\longrightarrow}&
    \left((X_n)^{S^1}\right)^{S^1}
  }
  \,.
$$

This gives the claimed morphism $X \to \Omega X[-1]$.

If $X$ is an [[Omega-spectrum]], then by definition, this last morphism is already a weak equivalence in the strict model structure, hence in particular a weak equivalence in the stable model structure.

From this, it follows that also the first morphism is a stable equivalence, because for every [[Omega-spectrum]] $Y$, then by the adjunctions in prop. \ref{AdjunctionsBetweenLoopingAndDeloopingForSeqSpec}

$$
  \array{
     [X, Y]_{strict} &\overset{}{\longrightarrow}& [\Sigma X[-1],Y]_{strict}
     \\
     {}^{\mathllap{id}}\downarrow && \downarrow^{\mathrlap{\simeq}}
     \\
     [X,Y]_{strict}  &\underset{\simeq}{\longrightarrow}& [X, \Omega Y[1]]_{strict}
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $X$, a sequential spectrum in simplicial sets. Then there are stable equivalences

$$
  X\wedge S^1 \longrightarrow \Sigma X \longrightarrow X[1]
$$

between the real suspension (def. \ref{SequentialSpectrumRealSuspension}), the fake suspension (def. \ref{SequentialSpectrumFakeSuspension}) and the shift by +1 (def. \ref{ShiftedSpectrum}) of $X$.

If each $X_n$ is a [[Kan complex]], then there are stable equivalences

$$
  X^{S^1} \longrightarrow \Omega X \longrightarrow X[-1]
$$

between the real looping (def. \ref{SequentialSpectrumRealSuspension}), the fake looping (def. \ref{SequentialSpectrumFakeSuspension}) and the shift by -1 (def. \ref{ShiftedSpectrum}) of $X$.


=--

([Jardine 15, corollary 10.54](#Jardine15))



### Relation to excisive functors

We discuss aspects of the equivalence of sequential spectra carrying the [[Bousfield-Friedlander model structure]] with [[excisive (infinity,1)-functors]], modeled as [[simplicial functors]] carrying a [[model structure for excisive functors]].

+-- {: .num_defn #SimplicialSetsPointedAndFinite}
###### Definition

Write 

* [[sSet]] for the [[category]] of [[simplicial sets]];

* $sSet^{\ast/}$ for the category of [[pointed simplicial sets]];

* $sSet_{fin}^{\ast/}\simeq s(FinSet)^{\ast/} \hookrightarrow sSet^{\ast/}$ for the [[full subcategory]] of [[pointed simplicial set|pointed simplicial]] [[finite sets]].

Write

$$
  sSet^{\ast/}
  \stackrel{\overset{(-)_+}{\longleftarrow}}{\underset{u}{\longrightarrow}}
  sSet
$$

for the [[free-forgetful adjunction]], where the [[left adjoint]] functor $(-)_+$ freely adjoins a base point.

Write

$$
  \wedge \colon sSet^{\ast/} \times sSet^{\ast/} \longrightarrow sSet^{\ast/}
$$

for the [[smash product]] of [[pointed object|pointed]] [[simplicial sets]], similarly for its restriction to $sSet_{fin}^{\ast}$:

$$
  X \wedge Y 
    \coloneqq 
  cofib\left(
    \; 
    \left(\,
      (u(X),\ast) \sqcup (\ast, u(Y)) 
    \,\right) 
      \longrightarrow 
     u(X) \times u(Y) 
    \;
  \right)
  \,.
$$

This gives $sSet^{\ast/}$ and $sSet^{\ast/}_{fin}$ the structure of a [[closed monoidal category]] and we write 

$$
  [-,-]_\ast \;\colon\; (sSet^{\ast/})^{op} \times sSet^{\ast/} \longrightarrow sSet^{\ast/}
$$

for the corresponding [[internal hom]], the pointed [[function complex]] functor.

=--

We regard all the categories in def. \ref{SimplicialSetsPointedAndFinite} canonically as [[simplicially enriched categories]], and in fact regard $sSet^{\ast/}$ and $sSet^{\ast/}_{fin}$ as $sSet^{\ast/}$-[[enriched categories]]. 

The category that supports a [[model structure for excisive functors]] is the  $sSet^{\ast/}$-[[enriched functor category]]

$$
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]
  \,.
$$

([Lydakis 98, example 3.8, def. 4.4](#Lydakis98))



+-- {: .num_prop #QuillenEquivalenceBetweenSequentialBFAndExcisiveFunctors}
###### Proposition

The [[adjunction]]

$$
  (\iota_\ast \dashv \iota^\ast)
  \;\colon\;
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}
    \stackrel{\overset{\iota_\ast}{\longleftarrow}}{\underset{\iota^\ast}{\longrightarrow}}
  [StdSpheres, sSet^{\ast/}]
    \underoverset{\simeq}{(-)^{seq}}{\longrightarrow}
  SeqSpec(sSet)_{BF}
$$

(given by restriction $\iota^\ast$ along the defining inclusion $\iota$ of def. \ref{CategoriesOfStandardSpheres} and by left [[Kan extension]] $\iota_\ast$ along $\iota$, and combined with the equivalence $(-)^{seq}$ of prop. \ref{SequentialSpectraAsDiagramSpectra}) is a  [[Quillen adjunction]] and in fact a [[Quillen equivalence]] between the [[Bousfield-Friedlander model structure]] on sequential prespectra and Lydakis' [[model structure for excisive functors]].

=--

([Lydakis 98, theorem 11.3](#Lydakis98)) For more details see at _[[model structure for excisive functors]]_. The analogous statement for spectra in $Top$ is in ([MMSS 00](#MMSS00)).

+-- {: .num_remark}
###### Remark

Prop. \ref{QuillenEquivalenceBetweenSequentialBFAndExcisiveFunctors} shows why 
plain sequential spectra do not carry a [[symmetric smash product of spectra]]:

By [this remark](smash+product+of+spectra#WhySequentialSpectraHaveNoSymmetricSmashProduct) at _[[smash product of spectra]]_
the graded-commutativity implicit in the [[braiding]] of the [[smash product]] of [[n-spheres]] is not reflected after restricting from $(sSet^{\ast/}, \wedge)$ to the non-full subcategory $StdSpheres$.

=--

### Smash product
 {#SmashProduct}

The [[smash product of spectra]] realized on sequential spectra never has good properties before passage to the [[stable homotopy category]] or lift to better models (see [here](smash%20product+of+spectra#GradedCommutativity)), but it may still be defined in various ways:

+-- {: .num_defn #SmashProductByDoublingDegrees}
###### Definition

For $X,Y$ two sequential spectra, def. \ref{SequentialSpectra}, their smash product $X \wedge Y$ is the sequential spectrum which in even degrees is given by the [[smash product]] fo the pointed component spaces of half that degree

$$
  (X\wedge Y)_{2n} \coloneqq X_n \wedge Y_n
$$

and in odd degree by 

$$
  (X\wedge Y)_{2n+1} \coloneqq S^1 \wedge X_n \wedge Y_n
$$

with structure maps being in even degree, the identity

$$
  \sigma^{X \wedge Y}_{2 n} \colon S^1 \wedge (X \wedge Y)_{2n} = S^1 \wedge X_n \wedge Y_n = (X \wedge Y)_{2n+1}
$$

and in odd degree as the composite

$$
  \sigma^{X\wedge Y}_{2n+1} 
    \colon 
  S^1 \wedge (X \wedge Y)_{2n+1} 
  \simeq
  S^1 \wedge S^1 \wedge X_n \wedge Y_n
  \simeq
  S^1 \wedge X_n \wedge S^1 \wedge Y_n
  \stackrel{\sigma_n^X \wedge \sigma^Y_n}{\longrightarrow}  
  X_{n+1} \wedge Y_{n+1}
  \simeq
  (X\wedge Y)_{2n+2}
  \,.
$$

=--

([Lydakis 98, def. 10.20](#Lydakis98), [Lydakis 98b, def. 5.9](Gamma-space#Lydakis98), [MMSS 00, def. 11.6](#MMSS00))

+-- {: .num_prop #SmashProductCompatibleWithTheOneOnSpectra}
###### Proposition

Under the Quillen equivalence of prop. 
\ref{QuillenEquivalenceBetweenSequentialBFAndExcisiveFunctors} the symmetric monoidal [[Day convolution product]] on pre-[[excisive functors]] as well as the [[symmetric monoidal smash product of spectra|symmetric monoidal smash product]] of [[orthogonal spectra]] is identified with the  [[smash product of spectra]] realized on sequential spectra via def. \ref{SmashProductByDoublingDegrees}.

=--

([Lydakis 98, theorem 12.5](#Lydakis98), [MMSS 00, prop. 11.9](#MMSS00))

## Related concepts

* [[symmetric spectrum]], [[orthogonal spectrum]]

* [[spectrum object]]

* in [[homotopy type theory]]: [[sequential spectrum type]]

* [[cospectrum]]

## References

* {#Kan63} [[Daniel Kan]], _Semisimplicial spectra_, Illinois J. Math. Volume 7, Issue 3 (1963), 463-478. ([euclid.ijm/1255644953](http://projecteuclid.org/euclid.ijm/1255644953))

* {#Boardman65} [[Michael Boardman]], _Stable homotopy theory_, mimeographed notes, University of Warwick, 1965 onward

* {#Adams74} [[Frank Adams]], Part III, section 2 _[[Stable homotopy and generalised homology]]_, 1974

* {#Switzer75} [[Robert Switzer]], chapter 8 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/bousfield-friedlander.pdf))

 * {#Lydakis98} [[Manos Lydakis]], _Simplicial functors and stable homotopy theory_ Preprint, 1998 (Hopf archive [pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf), [[LydakisSimplicialFunctors.pdf:file]])

  (mostly on a [[model structure on excisive functors]] on [[simplicial sets]])

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], section 11 of _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

* {#Schwede12} [[Stefan Schwede]], _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))

  > (mostly on [[symmetric spectra]])

* {#Jardine15} [[John F. Jardine]], section 10 of: _[[Local homotopy theory]]_, 2016

  (with regards to [[sheaves of spectra]])

Symmetric spectra in more general [[model categories]] (using the [[Bousfield-Friedlander theorem]]) are discussed in 

* {#Schwede97} [[Stefan Schwede]], section 3 of _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))

* {#Hovey} [[Mark Hovey]], _Spectra and symmetric spectra in general model categories_, Journal of Pure and Applied Algebra Volume 165, Issue 1, 23 November 2001, Pages 63&#8211;127 ([arXiv:math/0004051](https://arxiv.org/abs/math/0004051))

[[!redirects sequential spectra]]

[[!redirects sequential prespectrum]]
[[!redirects sequential prespectra]]

[[!redirects sequential pre-spectrum]]
[[!redirects sequential pre-spectra]]


[[!redirects Boardman spectrum]]
[[!redirects Boardman spectra]]