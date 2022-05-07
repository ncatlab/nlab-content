

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In abstract generality, a _differential cohomology diagram_ is the hexagonal [[diagram]] in a [[cohesive (∞,1)-topos]] formed by the two [[fracture squares]] of the [[unit of a monad|unit]] and [[counit of a comonad|counit]] of, respectively, the [[shape modality]] $\Pi$ and the [[flat modality]] $\flat$. The exactness properties of this diagram for any [[stable homotopy type]] $\hat E$ in the corresponding [[tangent cohesive (∞,1)-topos]] express $\hat E$ as being the [[coefficients]] for a [[differential cohomology]] refinement by differential form data $\flat_{dR} \hat E$ of the [[generalized (Eilenberg-Steenrod) cohomology theory]] which is [[Brown representability theorem|represented]] by the [[shape modality|shape]] [[spectrum]] $E \coloneqq \Pi(\hat E)$.

Historically, it had been shown in ([Simons-Sullivan 07](#SimonsSullivan07)) for [[ordinary differential cohomology]] and in ([Freed-Lott 10](#FreedLott10), [Simons-Sullivan 08](#SimonsSullivan08)) for [[differential K-theory]] that these cohomology theories are characterized as sitting in the middle of a hexagonal [[diagram]] of interlocking [[exact sequences]] of [[cohomology groups]], which expresses, on the one hand, how every differential cohomology class has underlying it a non-differential cohomology class ("of a [[principal ∞-bundle]]") as well as a [[curvature]] [[differential form]] datum, and, on the other hand, how the special cases of trivial underlying classes equipped with differential form datum and of [[flat connection|flat]] differential form data sit inside the differential cohomology classes.

At this schematic conceptual level a differential cohomology diagram looks as follows (where all unlabelled arrows are meant to be read as "evident inclusions");

$$
  \array{
    &&  {{connection\;forms}\atop{on\;trivial\;bundles}} && \stackrel{de\;Rham\;differential}{\longrightarrow} && {{curvature}\atop{forms}}
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{curvature}} && \searrow^{\mathrlap{de\;Rham\;theorem}}
    \\
    {{flat}\atop{differential\;forms}}  && 
    && {{geometric\;bundles}\atop{with\;connection}} && && 
    {{rationalized}\atop{bundle}}
    \\
    & \searrow &  & \nearrow & & \searrow^{\mathrlap{topol.\;class}} && \nearrow_{\mathrlap{Chern\;character}}
    \\
    && {{geometric\;bundles}\atop{with\;flat\;connection}} && \underset{comparison/regulator\;map}{\longrightarrow} && {{shape}\atop{of\;bundle}}
  }
$$

One characteristic property is that the two outer sequences are [[exact sequences]]. This expresses (at this rough schematic level) for instance (for the upper part) that the connections $A$ on trivial bundles whose curvature vanishes in that $\mathbf{d}A = 0$, are exactly the flat connections; as well as (for the lower part) that bundles with [[flat connections]] have [[torsion subgroup|torsion]] Chern-clases.

So a [[differential cohomology]] theory would be one whose [[cocycles]]/[[cohomology classes]] have the interpretation of (stable) [[principal ∞-bundles]] with [[connection on an ∞-bundle|connection]] such as in the middle of this diagram.

The characterization/construction of [[differential cohomology]] via [[homotopy fiber products]] (of [[mapping spectra]] with [[differential form]] data) due to ([Hopkins-Singer 02](#HopkinsSinger02)) provides an incarnation of this kind of diagram genuinely in [[stable homotopy theory]], so that the outer parts are indeed [[homotopy fiber sequences]] and the two squares are homotopy cartesian (are [[homotopy pullbacks]]/[[homotopy pushouts]]).

In ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)) it was observed (see [Schreiber 13, section 4.1.2](#Schreiber13) for the generality in which we present this here) that every [[stable homotopy type]] $\hat E$ in a [[cohesive (∞,1)-topos]] $\mathbf{H}$ canonically sits inside a diagram of this form, being formed from the [[fracture squares]] of the units and counits of the [[shape modality]] $\Pi$ and the [[flat modality]] $\flat$, which in the right part are interpreted as the [[Maurer-Cartan form]] $\theta_E$ and the [[Chern character]] $ch_E$:

$$
  \array{
    &&  \Pi_{dR} {\hat E} && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}{\hat E}
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_{\hat E}}} && \searrow
    \\
    \Pi_{dR} \flat  {\hat E}  && && {\hat E} && && \Pi \flat_{dR}  \hat E
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{ch_E}}
    \\
    && \flat {\hat E} && \longrightarrow && \Pi \hat E
  }
  \,.
$$

This is theorem \ref{TheDifferentialDiagram} below.

For the special case that $\mathbf{H} = T Smooth\infty Grpd$ is the [[tangent (∞,1)-topos]] of [[smooth ∞-groupoids]] ([[∞-stacks]] over the [[site]] of [[smooth manifolds]]) this subsumes the cases mentioned above. But there are many examples of cohomology theories not of the form of ([Hopkins-Singer 02](#HopkinsSinger02)) but represented by [[stable homotopy types]] in a [[cohesive (∞,1)-topos]] (see [Schreiber 13](#Schreiber13), [BunkeNikolausV&#246;lkl 13](#BunkeNikolausVoelkl13)) and hence fitting into such a diagram, where the interpretation of the pieces of the diagram is just as it should be. 




Therefore it makes sense to define generally that a _differential cohomology diagram_ is the above combined [[fracture squares]] with its outer [[homotopy fiber sequences]] for [[shape modality]] and [[flat modality]] in any [[cohesive (∞,1)-topos]].

## Definition/Construction

### Differential coefficients and Maurer-Cartan forms

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]], write $T\mathbf{H}$ for its [[tangent cohesive (∞,1)-topos]] and write $T_\ast \mathbf{H} \hookrightarrow T \mathbf{H}$ for the [[stable (∞,1)-category]] of [[spectrum objects]] inside it.

As usual, we use the following notation.

+-- {: .num_defn #DifferentialCoefficients}
###### Definition (Notation)

Write 

* $\Pi$ for the  [[shape modality]] 

* $\flat$ for the [[flat modality]] 

restricted to $Stab(\mathbf{H}) \hookrightarrow  T \mathbf{H}$, respectively. 


Given $E \in $ [[Spectra]] we say that $\hat E \in Stab(\mathbf{H})$ with an [[equivalence]] 

$$
  \Pi(\hat E) \simeq E
$$ 

is a _cohesive refinement_ or _differential refinement_ of $E$.

Write 

* $\flat_{dR}$ for the [[homotopy fiber]] of the [[suspension]] of the $\flat$-[[counit of a comonad|counit]] 

* $\Pi_{dR}$ for the [[homotopy cofiber]] of the looping of the [[unit of a monad|unit]] of $\Pi$. 


* $\theta \;\colon\; id \longrightarrow \flat_{dR}$  for the canonical morphism (itself the [[homotopy fiber]] of $\flat_{dR} \to \flat$) which has the interpretation of being the [[Maurer-Cartan form]].

Notice that on [[stable homotopy types]] we have

$$
  \flat_{dR}A \simeq cofib(\flat A \to A) =  A/(\flat A)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Warning: Elsewhere we often write $\flat_{dR} \Sigma$ for $\flat_{dR}$ above and $\Pi_{dR}\Omega$ for what is $\Pi_{dR}$ here. That other convention has its advanages in the context of unstable cohesion. Here with stable cohesion the present convention is more natural.

=--

+-- {: .num_remark}
###### Remark

As discussed at _[structures in a cohesive ∞-topos -- de Rham cohomology](cohesive+%28infinity%2C1%29-topos+--+structures#deRhamCohomology)_ there (and as is discussed below at [de Rham coefficients](#DeRhamCoefficients)) for $A \in \mathbf{T}_\ast H$ a [[cohesive homotopy type]] then we may think of $\Pi_{dR} A$ and of  $\flat_{dR}  A$  as being the [[de Rham complex]] with [[coefficients]] in $\Pi(\flat_{dR} \Sigma A)$, truncated to negative degree and to non-negative degree, respectively; the canonical map

$$
  \array{
    \Pi_{dR}A && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}A
    \\
    & \searrow && \nearrow
    \\
    && A
  }
$$

interpreting as the [[de Rham differential]].

Beware that this is a very general conceptualization of de Rham coefficients. In standard examples $\flat_{dR}$ does come from traditional [[differential form]] data (see at _[Deligne coefficients](#DeligneCoefficients)_ and at _[Hopkins-Singer coefficients](#HopkinsSingerCoefficients)_ below), but generally it may have quite different looking models. But in any case $\flat_{dR} \Sigma A$ always has the interpretation of the home of the _[[curvature forms]]_ of cohomology with coefficients in $A$, which makes thinking of $\flat_{dR}$ as producing generalized form data useful.

=--



### Chern character and the differential fracture squares
 {#ChernCharacterAndFractureSquares}


+-- {: .num_defn #GeneralChernCharacter}
###### Definition

The [[shape modality|shape]] of the [[Maurer-Cartan form]]  $\theta$, def. \ref{DifferentialCoefficients}, we call the _[[Chern character]]_

$$
  ch \coloneqq \Pi \theta
  \,.
$$

Its component on $\hat E\in T_\ast \mathbf{H}$ we write $ch_{\hat E}$ or $ch_E$, for short.

=--


+-- {: .num_prop #TheDifferentialFractureSquare}
###### Proposition
**(differential fracture square)**


For every $\hat E \in T_\ast \mathbf{H}$ the [[natural transformation|naturality square]] 

$$
  \array{
    \hat E &\stackrel{}{\longrightarrow}& \flat_{dR} \hat E
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(\hat E) &\stackrel{ch_E}{\longrightarrow}& \Pi \flat_{dR} \hat E
  }
$$

(of the [[shape modality]] applied to the [[homotopy cofiber]] of the [[counit of a comonad|counit]] of the [[flat modality]]) is an [[(∞,1)-pullback]] square (hence also an [[(∞,1)-pushout]]).

Dually, also the square

$$
  \array{   
    \Pi_{dR} \flat \hat E &\longrightarrow& \Pi_{dR} \hat E 
    \\
    \downarrow && \downarrow 
    \\
    \flat \hat E & \longrightarrow & \hat E 
  }
$$

is homotopy cartesian.


=--

This fact was observed in ([Bunke-Nikolaus-V&#246;lkl 13, prop. 3.5](#BunkeNikolausVoelkl13)). It may be thought of as an incarnation of the concept of a _[[fracture theorem]]_.

+-- {: .proof}
###### Proof 

By [[cohesion]] and [[stable (infinity,1)-category|stability]] we have the diagram

$$
  \array{
    \flat \hat E &\longrightarrow & \hat E &\stackrel{}{\longrightarrow}& \flat_{dR} \hat E
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow && \downarrow
    \\
    \Pi(\flat \hat E) &\longrightarrow& \Pi(\hat E) &\stackrel{}{\longrightarrow}& \Pi(\flat_{dR} \hat E)
  }
$$

where both rows are [[homotopy fiber sequences]]. By [[cohesion]] the left vertical map is an [[equivalence in an (infinity,1)-category|equivalence]]. The claim now follows with the [homotopy fiber characterization](homotopy+pullback#HomotopyFiberCharacterization) of [[homotopy pullbacks]].

The second statement follows dually: 

$$
  \array{   
    \Pi_{dR} \flat \hat E &\longrightarrow& \Pi_{dR} \hat E &\longrightarrow& \Pi_{dR} \flat_{dR} \hat E
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    \flat \hat E & \longrightarrow & \hat E &\longrightarrow&\flat_{dR} \hat E
  }
  \,.
$$

=--

Notice that generally $\flat_{dR} \hat E$ is a [[flat modality]] "[[anti-modal type]]" in that it is annihilated by $\flat$:

$$
  \flat (\flat_{dR} \hat E) \simeq 0
  \,.
$$

($\flat$-anti-modal types are called "pure" in ([Bunke-Nikolaus-V&#246;lkl 13, prop. 3.5](#BunkeNikolausVoelkl13))).

The following says that not only does, by prop.\ref{TheDifferentialFractureSquare}, the $(\Pi \dashv \flat)$-[[fracture square]] exhibit any stable cohesive homotopy type as the pullback of a $\flat$-[[anti-modal type]] along a map of $\Pi$-modal types into its [[shape modality|shape]], but that conversely all homotopy pullbacks of this form are $(\Pi \dashv \flat)$-fracture squares.


+-- {: .num_lemma #ReconstructionOfFractureSquare}
###### Lemma

For 

1. $E$ a [[shape modality|shape]]-[[modal type]] 

1. $\Omega^{\bullet \geq 0}$ a [[flat modality|flat]]-[[anti-modal type]];

1. $E \stackrel{f}{\longrightarrow} \Pi \Omega^{\bullet \gt 0}$ a morphism;

then the [[homotopy pullback]] square for the [[homotopy fiber product]] 

$$
  \hat E \coloneqq E \underset{\Pi\Omega^{\bullet \geq 0}}{\times} \Omega^{\bullet \geq 0}
$$

is equivalently the $(\Pi\dashv \flat)$-[[fracture square]] of $\hat E$
according to prop. \ref{TheDifferentialFractureSquare}:

$$
  \array{
    & \hat E &\longrightarrow& \flat_{dR} \hat E & \simeq \Omega^{\bullet \geq 0}
    \\
    & \downarrow && \downarrow
    \\
    E \simeq & \Pi \hat E &\stackrel{f \simeq ch_{\hat E}}{\longrightarrow}& 
    \Pi \flat_{dR} \hat E & \simeq \Pi \Omega^{\bullet \geq 0}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof 

First we observe that indeed $\Omega^{\bullet\geq 0}\simeq \flat_{dR} \hat E$. For that consider the following morphisms of homotopy pullback diagrams

$$
  \array{
    0 \simeq & \flat \Omega^{\bullet \geq 0} &\longrightarrow& \Omega^{\bullet \geq 0} &\longrightarrow& \Omega^{\bullet \geq 0}
    \\
    & \downarrow && \downarrow && \downarrow
    \\
    & \flat \Pi \Omega^{\bullet \geq 0} &\stackrel{\simeq}{\longrightarrow}& \Pi \Omega^{\bullet \geq 0} &\longrightarrow& 0
    \\
    & \uparrow && \uparrow^{\mathrlap{f}} && \uparrow
    \\
    & \flat E &\stackrel{\simeq}{\longrightarrow}& E &\longrightarrow& 0
    \\
    \\
    \underset{\leftarrow}{\lim}(-) \simeq& \flat \hat E &\longrightarrow& \hat E &\longrightarrow& \flat_{dR}\hat E
  }
$$

Here in the middle column we are showing the homotopy fiber product defining $\hat E$. On the left we have its image under $\flat$, with the $\flat$-counits running horizontally and using that $\flat$ preserves [[(∞,1)-limits]] and that $E$ and $\Pi \Omega^{\bullet \geq 0}$ are $\flat$-[[modal types]] by assumption and by [[cohesion]], while $\Omega^{\bullet \geq 0}$ is $\flat$-[[anti-modal type|anti modal]] by assumption. This and using that by [[stability]] all [[finite (∞,1)-limits]] and [[finite (∞,1)-colimits]] commute produces the [[homotopy cofiber]] morphisms going to the right. 

This shows that $\Omega^{\bullet \geq 0} \simeq \flat_{dR} \hat E$ and that the [[projection]] $E \underset{\Pi_{dR}\Omega^{\bullet \geq 0}}{\times} \Omega^{\bullet \geq 0} \to \Omega^{\bullet \geq 0}$ is equivalently the $\flat_{dR}$-[[unit of a monad|unit]] on $\hat E$.

Applying the [[shape modality]] to the right half of this diagram, using that by stability it preserves the homotopy pullbacks gives

$$
  \array{
    & \Pi \Omega^{\bullet \geq 0} 
      &\stackrel{\simeq}{\longrightarrow}& 
    \Pi \Omega^{\bullet \geq 0}
    \\
    & \downarrow^{\mathrlap{\simeq}} && \downarrow
    \\
    & \Pi \Omega^{\bullet \geq 0} &\longrightarrow& 0
    \\
    & \uparrow^{\mathrlap{f}} && \uparrow
    \\
    & E &\longrightarrow& 0
    \\
    \\
    \underset{\leftarrow}{\lim}(-) \simeq
    & 
    E 
   &\stackrel{ch_{\hat E}}{\longrightarrow}& 
   \Pi \flat_{dR}\hat E
  }
  \,.
$$


This shows that $ch_{\hat E} \simeq f$.

Finally, the dual argument

$$
  \array{
    & \Omega^{\bullet \geq 0}
    &\stackrel{}{\longrightarrow}&
    \Pi \Omega^{\bullet \geq 0} 
    \\
    & \downarrow && \downarrow^{\mathrlap{\simeq}}
    \\
    & \Pi \Omega^{\bullet \geq 0}
    &\stackrel{}{\longrightarrow}&
    \Pi \Omega^{\bullet \geq 0}
    \\
    & \uparrow && \uparrow
    \\
    & E
    &\stackrel{}{\longrightarrow}&
    \Pi E
    & \simeq E
    \\
    \\
    \underset{\leftarrow}{\lim}(-)
    \simeq
    &
    \hat E &\longrightarrow& \Pi(\hat E) & \simeq E
  }
$$

shows that the other [[projection]] $E \underset{\Pi_{dR}\Omega^{\bullet \geq 0}}{\times} \Omega^{\bullet \geq 0} \to E$ is equivalently the [[shape modality|shape]]-[[unit of a monad|unit]] of $\hat E$.

=--

The following proposition says that the construction in lemma \ref{ReconstructionOfFractureSquare} extends to a decomposition of the [[(∞,1)-category]] of cohesive  stable types as a [[homotopy fiber product]] of the [[(∞,1)-category]] of moprhisms of stable [[shape modality|shape]]-[[modal types]] with that of [[flat modality|flat]]-[[anti-modal types]]:
 
+-- {: .num_prop}
###### Proposition

There is an [[(∞,1)-pullback]] of [[(∞,1)-categories]] of the form

$$

  \array{
    Stab(\mathbf{H}) &\stackrel{\flat_{dR} \Sigma}{\longrightarrow}&
    ker(\flat)
    \\
    \downarrow^{\mathrlap{ch}} && \downarrow^{\mathrlap{\Pi}}
    \\
    Spectra^I &\stackrel{cod}{\longrightarrow}& Spectra
  }
  \,,
$$

where the bottom map is the [[codomain fibration]] of the [[(∞,1)-category of spectra]], $\Pi$ denotes the [[shape modality]] restricted to stable $\flat$-[[anti-modal types]],  $ch$ assigns the [[Chern character map]] of def. \ref{GeneralChernCharacter} and $\flat_{dR} \Sigma$ assigns de Rham coefficients as in def. \ref{DifferentialCoefficients}.

=--

([Bunke-Nikolaus-V&#246;lkl 13, prop. 3.5](#BunkeNikolausVoelkl13))

Dually:


+-- {: .num_prop}
###### Proposition

For every $A \in T_\ast \mathbf{H}$ the [[natural transformation|naturality square]] 

$$
  \array{
    \flat(\Pi_{dR} \Sigma^{-1} A) &\longrightarrow & \Pi_{dR}(\Sigma^{-1} A)
    \\
    \downarrow && \downarrow
    \\
    \flat A &\stackrel{}{\longrightarrow}& A 
  }
$$

(of the [[flat modality]] applied to the [[homotopy fiber]] of the [[unit of a monad|unit]] of the [[shape modality]]) is an [[(∞,1)-pullback]] square.

=--

+-- {: .proof}
###### Proof 

As before but dually, the diagram extends to a morphism of 
[[homotopy cofiber]] diagrams of the form

$$
  \array{
    \flat(\Pi_{dR}  A) &\longrightarrow & \Pi_{dR}(A)
    \\
    \downarrow && \downarrow
    \\
    \flat A &\stackrel{}{\longrightarrow}& A 
    \\
    \downarrow && \downarrow 
    \\
    \flat \Pi(A) &\stackrel{\simeq}{\longrightarrow}& \Pi(A) 
  }
  \,,
$$

and by [[cohesion]] the bottom horizontal morphism is an [[equivalence in an (infinity,1)-category|equivalence]].

=--

### The hexagon diagram
 {#TheHexagonDiagram}


Combining these two statements yields the following ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)).

+-- {: .num_theorem #TheDifferentialDiagram}
###### Theorem

For $\mathbf{H}$ a [[cohesive (∞,1)-topos]] with [[shape modality]] $\Pi$ and [[flat modality]] $\flat$, then for every [[stable homotopy type]] $A \in Stab(\mathbf{H}) \hookrightarrow T \mathbf{H}$ the canonical hexagon diagram 

$$
  \array{
    &&  \Pi_{dR} A && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR} A
    \\
    & \nearrow & & \searrow & & \nearrow_{\mathrlap{\theta_A}} && \searrow
    \\
    \Pi_{dR} \flat  A  && \Downarrow^{\mathrlap{a}} && A && \Downarrow^{\mathrlap{b}} && \Pi \flat_{dR} A
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow_{\mathrlap{ch_A}}
    \\
    && \flat A && \longrightarrow && \Pi A
  }
  \,,
$$

formed from the $\Pi$-[[unit of a monad|unit]] and $\flat$-counit  -- the "differential cohomology hexagon" -- is homotopy exact in that

1. the two squares are [[homotopy pullback]] squares ("[[fracture squares]]");

1. the two diagonals are the [[homotopy fiber sequences]] of the [[Maurer-Cartan form]] $\theta_A$ and its dual; 

1. the bottom morphism is the canonical [[points-to-pieces transform]];

1. the top and bottom outer sequences are long [[homotopy fiber sequences]].

=--

+-- {: .proof}
###### Proof 

Only the last statement remains to be shown, for that use the [[pasting law]]: this gives the following diagram in which every square and every [[pasting diagram|pasting]] rectangle is a [[homotopy pullback]]

$$
  \array{
    \Pi_{dR} \flat A  &\to & \flat A  &\to& 0
    \\
    \downarrow^{\mathrlap{f_1}} &\swArrow_{\mathrlap{a^{-1}}}& \downarrow && \downarrow
    \\
    \Pi_{dR} A  &\stackrel{f_{2}}{\to}& A &\stackrel{\theta_A}{\to}& \flat_{dR} A
    \\
    \downarrow && \downarrow & \swArrow_{\mathrlap{b}} & \downarrow^{\mathrlap{f_3}}
    \\
    0 &\to& \Pi A &\to& \Pi \flat_{dR} A
  }
  \,.
$$

This exhibits the sequence  $\stackrel{f_1}{\to}\stackrel{\theta_A \circ f_{2}}{\longrightarrow} \stackrel{f_3}{\to}$, which is the top part of the hexagon, as a [[homotopy fiber sequence]].

The dual argument shows that the bottom part of the hexagon is a [[homotopy cofiber sequence]].

=--

+-- {: .num_remark}
###### Remark

Theorem \ref{TheDifferentialDiagram} in particular implies that for [[stable homotopy types|stable]] [[cohesive homotopy types]] $A$ there are natural equivalences

* $\Pi_{dR} A \simeq \Pi_{dR} \flat_{dR} A$

* $\flat \Pi_{dR} A\simeq \Pi \flat_{dR} A$

Given that conceptually, as made explicit in the [Idea-section](#Idea) above, we may think of cocycles in $\Pi \flat_{dR} A$ as the rationalized characteristic classes and of coycles in $\flat \Pi_{dR} A$ as flat differential forms, this expresses the conceptual content of the [[de Rham theorem]].

=--


## Examples

### Ordinary differential cohomology
 {#OrdinaryDifferentialCohomology}

We discuss differential refinements in $\mathbf{H} =$ [[Smooth∞Grpd]] of [[ordinary cohomology]], hence of cohomology with [[coefficients]] in [[chain complexes]] or equivalently, via the [[stable Dold-Kan correspondence]], cohomology [[Brown representability theorem|represented]] by [[spectra]] underlying [[Eilenberg-MacLane spectrum]]-[[module spectra]].

#### De Rham coefficients
 {#DeRhamCoefficients}

We briefly recall the [[smooth spectra]] given by the [[de Rham complex]] (tensored with any [[chain complex]]) from _[smooth spectrum -- Examples -- De Rham spectra](smooth+spectrum#ExamplesDeRhamSpectra)_.

Write $Ch_\bullet$ for the [[(∞,1)-category of chain complexes]] (of [[abelian groups]], hence over the [[ring]] $\mathbb{Z}$ of [[integers]]). It is convenient to choose for $A_\bullet \in Ch_\bullet$ the grading convention

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    A_{-1}
    \\
    \downarrow
    \\
    A_0
    \\
    \downarrow
    \\
    A_1
    \\
    \downarrow
    \\
    \vdots
   }
$$

such that under the [[stable Dold-Kan correspondence]] 

$$
  DK \;\colon\; Ch_\bullet \stackrel{}{\longrightarrow} Spectra
$$

the [[homotopy groups]] of spectra relate to the [[homology groups]] by


$$
  \pi_n(DK(A_\bullet)) \simeq  H_{-n}(A_\bullet)
  \,.
$$

In particular for $A \in $ [[Ab]] an [[abelian group]] then $A[n]$ denotes the chain complex concentrated on $A$ in degree $-n$ in this counting.

The grading is such as to harmonize well with the central example of a sheaf of chain complexes over the site of [[smooth manifolds]], which is the [[de Rham complex]], regarded as a [[smooth spectrum]] via the discussion at _[smooth spectrum -- from chain complexes of smooth modules](smooth+spectrum#FromChainComplexesOfSmoothModules)_

$$
  \Omega^\bullet \in Sh_\infty(SmthMfd, Ch_\bullet) \longrightarrow Sh_\infty(SmthMfd, Spectra) \hookrightarrow T \mathbf{H}
$$

$$
  \Omega^{\bullet} \;\colon\;  X\mapsto (\cdots \to 0 \to 0 \to \Omega^0(X) \stackrel{\mathbf{d}}{\to} \Omega^1(X)\stackrel{\mathbf{d}}{\to} \cdots)
$$

with $\Omega^0(X) = C^\infty(X, \mathbb{R})$ in degree 0.

Throughout we keep the inclusion 

$$
  C \in Ch_\bullet \stackrel{DK}{\longrightarrow}
  Spectra \stackrel{Disc}{\hookrightarrow}
  Stab(\mathbf{H})
$$ 

notationally implicit, regarding bare chain complexes as geometrically discrete spectrum objects in smooth differential geometry.


We consider for $n \in \mathbb{N}$ the truncated sheaves of de Rham complexes with [[coefficients]] in a given [[chain complex]]:

+-- {: .num_defn}
###### Definition

Write

$$
  \Omega^{\bullet \geq n} \in Sh_\infty(SmthMfd, Ch_\bullet) \longrightarrow Sh_\infty(SmthMfd, Spectra) \hookrightarrow T \mathbf{H}
$$

for the [[smooth spectrum]] given under the [[stable Dold-Kan correspondence]] by the sheaf of truncated [[de Rham complexes]]

$$
  \Omega^{\bullet \geq n} \;\colon\;  X\mapsto (\cdots \to 0 \to 0 \to \Omega^n(X) \stackrel{\mathbf{d}}{\to} \Omega^{n+1}(X)\stackrel{\mathbf{d}}{\to} \cdots)
$$

with $\Omega^n(X)$ in degree $n$ (the $p$th stage in the [[Hodge filtration]]).

=--

More genereally:

+-- {: .num_defn #DeRhamComplexesWithCoefficients}
###### Definition


For $C \in Ch_\bullet$ a [[chain complex]], 

write 

$(\Omega \otimes C)^{\bullet \geq n}$ for the [[smooth spectrum]] given over each manifold $X$ by the [[tensor product of chain complexes]] followed by truncation as indicated:

$$
  \begin{array}
  (\Omega \otimes C)^{\bullet \geq n}
  &=& 
  (\cdots &\to& 0 &\to& 0 &\to& \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-k} &\stackrel{\mathbf{d} \pm d_{C}}{\to}& \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-k+1}&\stackrel{\mathbf{d}\pm d_{C}}{\to}& \cdots)
  \\
  \\
   deg && && && n-1 && n && n+1 && 
  \end{array}
 \,.
$$

where the first non-trivial term displayed is in taken to be in degree $n$;

and write $(\Omega \otimes C)^{\bullet \lt n}$ for

$$
  \begin{array}
  (\Omega \otimes C)^{\bullet \lt n}
  &=& 
  (
    \cdots
    &\stackrel{\mathbf{d} \pm d_{C}}{\to}&
    \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-2-k}
    &\stackrel{\mathbf{d} \pm d_{C}}{\to}&
    \oplus_{k \in \mathbb{N}} \Omega^{k}(X) \otimes C_{n-1-k}
    0 &\to& 0 &\to& \cdots )
    \\
    \\
    deg &&  && n-1 && n && n+1  &&
  \end{array}
$$

where again the first non-trivial term displayed is taken to be in degree $n$.

=--

+-- {: .num_remark}
###### Remark

Beware of the degree conventions in 
def. \ref{DeRhamComplexesWithCoefficients}: in the first clause the tensor product of complexes is truncated without any shifting, while in the second case the truncation is shifted by one. This notation turns out to well reflect the way that the hexagon, theorem \ref{TheDifferentialDiagram}, decomposes these [[smooth spectra]]  by prop. \ref{DifferentialComponentsOfDeRhamTensorC} and remark \ref{OnDecompositionOfDeRhamWithCoefficients} below.

=--

+-- {: .num_prop #DifferentialComponentsOfDeRhamTensorC}
###### Proposition

For $C \in Ch_\bullet(\mathbb{R})$ a [[chain complex]] of [[real number|real]] [[vector spaces]] and
for all $n \in \mathbb{Z}$

1. $\Pi ((\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n})\simeq C^\bullet$

1. $\flat ((\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n}) 
   \simeq 
   C^{\bullet \geq n} $


1. $\flat_{dR}  (\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n} 
   \simeq 
   (\Omega \otimes_{\mathbb{R}} C^{\bullet \leq n-1})^{\bullet \geq n}$


1. $\Pi_{dR} (\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n} 
   \simeq 
   (\Omega \otimes_{\mathbb{R}} C )^{\bullet \leq n-1}[-1]$

1. $\Pi \flat_{dR} (\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n} \simeq C^{\bullet \leq n-1}$

1. $ch \;\colon\; C \to C_{\bullet\leq n-1} $ is the canonical projection.

=--

([Bunke-Nikolaus-V&#246;lkl 13, lemma 4.4](#BunkeNikolausVoelkl13))

+-- {: .num_remark #OnDecompositionOfDeRhamWithCoefficients}
###### Remark

Prop. \ref{DifferentialComponentsOfDeRhamTensorC} means first of all that the [[de Rham complex]] $(\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq n}$ is a differential refinement, def. \ref{DifferentialCoefficients}, of the chain complex $C$ (for all $n$)

Moreover it says that $\flat_{dR} \Sigma (-)$ and $\Pi_{dR} \Omega(-)$ are similarly the high degree and low degree truncation, respectively, of the [[de Rham complex]] with coefficients in $\Pi \flat_{dR} \Sigma (-)$.

Specifically for $n = 0$, only the connected part 

$$
  D C_{\bullet \leq -1}
$$ 

appears in the de Rham coefficients, and we have 

$$
  \array{
    \Pi_{dR}(\cdots) && \stackrel{\mathbf{d}}{\longrightarrow} &&
    \flat_{dR}(\cdots)
    \\
    \simeq && \simeq  && \simeq
    \\
    \Omega(-,D)^{\bullet \lt 0}
    &&
      \stackrel{\mathbf{d}_{dR} \pm d_{C}}{\longrightarrow}
    &&
    \Omega(-,D)^{\bullet \geq 0}
  }
  \,.
$$

=--


#### Deligne coefficients
 {#DeligneCoefficients}

We discuss the differential cohomology hexagon for smooth [[Deligne cohomology]] and hence smooth [[circle n-bundles with connection]] realizedin $\mathbf{H}= $ [[Smooth∞Grpd]].


+-- {: .num_defn}
###### Definition

For $C \in Ch_\bullet(\mathbb{Z})$ be a [[chain complex]] of [[abelian groups]]. For $n \in \mathbb{N}$ an [[integer]], write $C_{conn,-n}$ for the [[homotopy fiber product]] in

$$
  \array{
    C_{conn,-n} &\longrightarrow& (\Omega \otimes_{\mathbb{Z}} C)^{\bullet \geq n}
    \\
    \downarrow && \downarrow
    \\
    C 
     &\longrightarrow&
    C \otimes \mathbb{R} & \simeq \Pi((\Omega \otimes_{\mathbb{Z}} C)^{\bullet \geq n})
  }
  \,,
$$

where the right map is the [[unit of a monad|unit]] of the [[shape modality]] according to prop. \ref{DifferentialComponentsOfDeRhamTensorC}.

=--

([Bunke-Nikolaus-V&#246;lkl 13, 4.3](#BunkeNikolausVoelkl13))

+-- {: .num_prop #DecompositionForGeneralSmoothDeligneCoefficients} 
###### Proposition

For all $n \in \mathbb{Z}$


1. $\Pi(C_{conn,-n}) \simeq C$

1. $\flat_{dR} C_{conn,-n} \simeq (\Omega \otimes C_{\leq n-1})^{\bullet \geq n}$

=--

([Bunke-Nikolaus-V&#246;lkl 13, lemma 4.5](#BunkeNikolausVoelkl13))

+-- {: .num_example #ExampleOrdinaryDeligneCohomology}
###### Example
**(ordinary Deligne cohomology)**

For $C = \mathbb{Z}[n+1]$ we have

$$

  (\Omega \otimes (\mathbb{Z}[n+1]\otimes \mathbb{R}))^{\bullet \geq 0}
  \simeq
  (\Omega \otimes \mathbb{R}[n+1])^{\bullet \geq 0}
  \simeq
  \Omega^{n+1}_{cl}(-)
$$

(with the last term being in degree 0) and more generally for $n \in \mathbb{N}$

$$
  (\Omega \otimes (\mathbb{Z}[n+1]\otimes \mathbb{R}))^{\bullet \geq -n}
  \simeq
  (\Omega \otimes \mathbb{R}[n+1])^{\bullet \geq -n}
  \simeq
  (\Omega^1(-) 
     \stackrel{\mathbf{d}}{\to} 
   \Omega^2(-)
      \stackrel{\mathbf{d}}{\to}
      \cdots
      \stackrel{\mathbf{d}}{\to}
   \Omega^{n+1}_{cl}(-)
  )
$$

(with the last term being in chain degrees $-n$ to 0 (hence homotopy group degrees $n$ to 0)).

{#PastingForDeligneTower} We have a pasting diagram of [[homotopy pullbacks]]
$$
  \array{
    B^n U(1)_{conn} &\to& \Omega^{n+1}_{cl}
    \\
    \downarrow && \downarrow
    \\
     &\stackrel{}{\longrightarrow}& (\Omega \otimes \mathbb{R}[n+1])^{\bullet \geq -1}
    \\
    \downarrow && \downarrow
    \\
    \vdots && \vdots
    \\
    \downarrow && \downarrow    
    \\
    \mathbf{B}^n U(1) &\stackrel{}{\longrightarrow}& (\Omega \otimes \mathbb{R}[n+1])^{\bullet \geq -n}
    \\
    \downarrow && \downarrow
    \\
    B^{n+1}\mathbb{Z} &\to& B^{n+1} \mathbb{R}
  }
$$

where on the right runs the [[Hodge filtration]],
with the notation $\mathbf{B}^n U(1) = \mathbb{Z}[n+1]_{conn,n}$ as at [[circle n-group]] and  $\mathbf{B}^n U(1)_{conn} = \mathbb{Z}[n+1]_{conn,0}$ as at _[[circle n-bundle with connection]]_.

Hence for all $n \in \mathbb{N}$

$$
  \mathbb{Z}[n+1]_{conn,n} \simeq \mathbf{B}^n U(1)
  \simeq
  (C^\infty(-,U(1)) \to 0 \to \cdots\to 0)
$$

and

$$
  \mathbb{Z}[n+1]_{conn,0} \simeq \mathbf{B}^n U(1)_{conn}
  \simeq
  (C^\infty(-,U(1))\stackrel{\mathbf{d}log}{\to}\Omega^1(-) \stackrel{\mathbf{d}}{\to} \cdots \stackrel{\mathbf{d}}{\to}\Omega^n)
  \,.
$$

is represented by the [[Deligne complex]].

The intermediate cases in between these two as in ([Schreiber 13, def. 3.9.46](#Schreiber13), [FRS 13, remark 2.3.15](#FRS13)) (discussed also for instance at _[Courant algebroid -- Relation to Atiyah Lie 2-algebroid](http://ncatlab.org/nlab/show/Courant+algebroid#RelationToAtiyahGroupoids)_).

Notice that by prop. \ref{DecompositionForGeneralSmoothDeligneCoefficients} the above homotopy pullback diagrams are all indeed the right part of the differential cohomology hexagon, theorem \ref{TheDifferentialDiagram}, e.g. 

$$
  \array{
     \mathbf{B}^n U(1)_{conn}
     &\stackrel{\theta_{\mathbf{B}^n U(1)_{conn}}}{\longrightarrow}&
     \Omega^{n+1}_{cl}
     \\
     \downarrow && \downarrow
     \\
     \vdots && \vdots
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}^n U(1)
     &\stackrel{\theta_{\mathbf{B}^n U(1)}}{\longrightarrow}&
     (\Omega^1 \to \cdots\to \Omega^{n+1}_{cl})
     \\
     \downarrow && \downarrow
     \\
     \mathbf{B}^{n+1}\mathbb{Z} &\stackrel{\Pi(\theta_{\mathbf{B}^n U(1)})}{\longrightarrow}&\mathbf{B}^{n+1}\mathbb{R}
  }
  \,.
$$

The differential cohomology hexagon obtained from this is on cohomology classes for each [[smooth manifold]] $X$ and each $n \in \mathbb{N}$

$$
  \array{
    && \Omega^{n}(X)/im(\mathbf{d}) && \stackrel{\mathbf{d}}{\longrightarrow} &&  \Omega^{n+1}_{cl}(X)
    \\
    & \nearrow && \searrow^{\mathrlap{a}} && \nearrow && \searrow
    \\
    H^{n}(X, \mathbb{R})
    && &&
    H^0(X,\mathbf{B}^n U(1)_{conn})
    && &&
    H^{n+1}(X,\mathbb{R})
    \\
    & \searrow && \nearrow && \searrow && \nearrow
    \\
    && H^{n}(X,U(1)) && \underset{}{\longrightarrow} && H^{n+1}(X,\mathbb{Z})
  }
$$

It is common (e.g. [Simons-Sullivan 07](#SimonsSullivan07)) to display this after quotienting out the [[kernel]] of $a$ (which is the group $\Omega^n(X)_{\mathbb{Z}}$ of [[closed differential forms]] with [[integer|integral]] [[periods]]), which is such as to make the top-left to bottom-right diagonal sequence be not just [[exact sequence|exact]] at the middle term, but be a [[short exact sequence]]:

$$
  \label{OrdinarCohomologyHexagon}
  \array{
    0 & && && && & 0
    \\
    & \searrow && && &&  \nearrow 
    \\
    && \Omega^{n}(X)/\Omega^n(X)_{\mathbb{Z}} && \stackrel{\mathbf{d}}{\longrightarrow} &&  \Omega^{n+1}_{cl}(X)
    \\
    & \nearrow && \searrow^{\mathrlap{a}} && \nearrow && \searrow
    \\
    H^{n}(X, \mathbb{R})
    && &&
    H^0(X,\mathbf{B}^n U(1)_{conn})
    && &&
    H^{n+1}(X,\mathbb{R})
    \\
    & \searrow && \nearrow && \searrow && \nearrow
    \\
    && H^{n}(X,U(1)) && \underset{\beta}{\longrightarrow} && H^{n+1}(X,\mathbb{Z})
    \\
    & \nearrow && && &&  \searrow 
    \\
    0 & && && && & 0
  }
  \,.
$$

Here the diagonals are now the "curvature exact sequence" and the "characteristic class exact sequence" as discussed at _[ordinary differential cohomology -- Properties -- curvature and characteristic class](ordinary+differential+cohomology#CurvatureAndCharClass)_.

The bottom horizontal map is the [[Bockstein homomorphism]] of the [[exponential sequence]] ([this example](Bockstein+homomorphism#Mod2BocksteinAndExponentialExactSequence)).

=--

### Hopkins-Singer coefficients
 {#HopkinsSingerCoefficients}

We discuss how the [[differential function complexes]] of ([[Quadratic Functions in Geometry, Topology,and M-Theory|Hopkins-Singer 05]]), providing differential refinements of geometrically discrete [[spectra]], and how they fit into their differential cohomology hexagon (following [Bunke-Nikolaus-V&#246;lkl 13, section 4.4.](#BunkeNikolausVoelkl13)).

Let again $\mathbf{H} = $ [[Smooth∞Grpd]].

Throughout, we leave notationally implicit 

1. the [[stable Dold-Kan correspondence]] $DK \;\colon\;Ch_\bullet \longrightarrow Spectra$;

1. the inclusion $Spectra \stackrel{Stab}{\hookrightarrow} Stab(\mathbf{H})$;


hence always regard a [[chain complex]] as the corresponding [[spectrum]] and regard any bare spectrum always as a [[geometrically discrete infinity-groupoid|geometrically discrete]] [[smooth spectrum]].




+-- {: .num_defn #HopkinsSingerPullback}
###### Definition

For 


1. $E \in Spectra \stackrel{Disc}{\hookrightarrow} Stab(\mathbf{H})$
a [[spectrum]], 

1. $C \in Ch_\bullet(\mathbb{R})$ a [[chain complex]] of [[real number|real]] [[vector spaces]];

1. $c \colon E \longrightarrow C$ a [[homomorphism]] of [[spectra]] from $E$ to the image of $C$ under the [[stable Dold-Kan correspondence]];

1. $n \in \mathbb{N}$

write $E_{conn_c,-n}$ for the [[homotopy fiber product]] in


$$
  \array{
    E_{conn_c,-n} &\longrightarrow& (\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq -n}
    \\
    \downarrow && \downarrow
    \\
    E &\longrightarrow& C & \simeq \Pi((\Omega \otimes C)^{\bullet \geq -n})
  }
  \,,
$$

where the map on the right is the [[unit of a monad|unit]] of the [[shape modality]] according to prop. \ref{DifferentialComponentsOfDeRhamTensorC}.

We abbreviate

$$
  E_{conn_c} \coloneqq E_{conn_c,0}
  \,.
$$

=--

This appears in ([Bunke-Nikolaus-V&#246;lkl 13, 4.4](#BunkeNikolausVoelkl13)), with an earlier version in ([Bunke-Gepner 13, def. 2.1](#BunkeGepner13)).

+-- {: .num_remark}
###### Remark

Specifically when $C \simeq E \wedge DK(\mathbb{R})$ is a model for the rationalization (realification) of $E$ and $c \colon E \to C$ is the canonical map, then it is a model for the [[Chern character]] and def. \ref{HopkinsSingerPullback} is essentially the definition of ([[Quadratic Functions in Geometry, Topology,and M-Theory|Hopkins-Singer 05]]).

=--

+-- {: .num_prop #DifferentialComponentsOfHopkinsSingerCoefficients}
###### Proposition

For all $n \in \mathbb{Z}$ 

1. $\flat_{dR}  E_{conn_c,-n} \simeq (\Omega \otimes_{\mathbb{R}}  C_{\bullet \leq -n -1})^{\bullet\geq n}$ 

1. $\Pi(E_{conn_c,-n}) \simeq E$.

=--

([Bunke-Nikolaus-V&#246;lkl 13, lemma 4.7](#BunkeNikolausVoelkl13))


+-- {: .num_remark}
###### Remark

Beware that in prop. \ref{DifferentialComponentsOfHopkinsSingerCoefficients} 
the intrinsic de Rham coefficients $\flat_{dR} \Sigma E_{conn_c,-n}$ in general differ by a truncation from the de Rham complex $(\Omega \otimes_{\mathbb{R}} C)^{\bullet \geq -n}$ which is being pulled back in definition \ref{HopkinsSingerPullback}.

But by prop. \ref{DifferentialComponentsOfHopkinsSingerCoefficients} and theorem \ref{TheDifferentialDiagram} composition with the truncation map preserves the [[homotopy pullback]], hence in the differential cohomology hexagon the two differ only in the exactness property in the top right entry.

=--

+-- {: .num_cor}
###### Corollary

Given $E_{conn_c} \coloneqq E_{conn_c,0}$ as in def. \ref{HopkinsSingerPullback},
then for each [[smooth manifold]] $X$ (indeed for each [[smooth ∞-groupoid]] $X$) the differential cohomology diagram on cohomology classes is of the following form

$$
  \array{
    && (\Omega(X) \otimes_{\mathbb{R}} C)^{-1}/{im(\mathbf{d})}
    && \stackrel{\mathbf{d}}{\longrightarrow} && 
    (\Omega(X)\otimes_{\mathbb{R}} C)^0_{cl}
    \\
    & \nearrow && \searrow && \nearrow && \searrow
    \\
    H^{-1}(X,C)
    && &&
    E_{conn_c}^0(X)
    && &&
    H^0(X,C)
    \\
    & \searrow && \nearrow && \searrow && \nearrow
    \\
    && \flat E^0(X)
    && \longrightarrow &&
    E^0(X)
  }
  \,.
$$

=--


([Bunke-Nikolaus-V&#246;lkl 13, (25)-(26)](#BunkeNikolausVoelkl13))

### Differential K-theory
 {#DifferentialKTheory}

We discuss several differential refinements, def. \ref{DifferentialCoefficients}, to [[smooth spectra]], of the complex [[topological K-theory]] spectrum [[KU]] or of its [[connective cover]] $ku$, hence versions of [[differential K-theory]].

#### Hopkins-Singer differential $ku$
 {#HSDifferentialKU}

Let $\mathbb{C}[b]$ be the [[polynomial ring]] with [[complex numbers]] [[coefficients]] on a single generator $b$. With $b$ regarded as in degree 2, regard this as a [[chain complex]] with vanishing [[differentials]]. 

Then the complex ordinary [[Chern character]] on K-theory is a map

$$
  ch\;\colon\; ku \longrightarrow \mathbb{C}[b]
  \,.
$$


+-- {: .num_defn #HSDifferentialKu}
###### Definition

Write

$$
  ku_{conn_ch}
  \in
  Stab(Smooth\infty Grpd)
$$ 

for the [[smooth spectrum]] induced by def. \ref{HopkinsSingerPullback}) from the standard [[Chern character]] $c \coloneqq ch$ on connective [[KU|ku]].

=--


([Hopkins-Singer 02, section 4.4](#HopkinsSinger02), [Bunke-Nikolaus-V&#246;lkl 13, section 6.1](#BunkeNikolausVoelkl13))




#### Algebraic K-theory of smooth manifolds and the $e$-invariant
 {#SoothVectorBundlesWithConnectionAndEInvariant}


Write 

1. $\mathbf{Vect}^{\oplus} \in Sh(SmthMfd) \hookrightarrow \mathbf{H} = Sh_\infty(SmthMfd)$ for the [[stack]] of (complex) [[vector bundles]] equipped with the [[direct sum]];

1. $\mathbf{Vect}_{conn}^{\oplus} \in Sh(SmthMfd)$ for the [[stack]] of (complex) [[vector bundles]] with [[connection on a vector bundle|connection]], equipped with direct sum;

Write

$$
  \mathcal{K} \;\colon\;  CMon_\infty(\infty Cat) \longrightarrow Spectra
$$

for the [[(∞,1)-functor]] from [[symmetric monoidal (∞,1)-categories]]
into [[spectra]] which produces the [[algebraic K-theory of symmetric monoidal (∞,1)-categories]].

+-- {: .num_defn #KTheoryOfStackOfVectorBundles}
###### Definition

Forming objectwise the [[algebraic K-theory of symmetric monoidal (∞,1)-categories]] and then [[∞-stackification|∞-stackifying]] (which we leave notationally implicit) produces [[smooth spectra]] 

$$
  \mathcal{K}(\mathbf{Vect}_{conn}^\oplus),\;\mathcal{K}(\mathbf{Vect}^\oplus)
  \in 
  Stab(Smooth\infty Grpd)
  \,.
$$

This may be called the _[[algebraic K-theory of smooth manifolds]]_.

=--



+-- {: .num_prop #FlatAndPiForDifferentialKTheory}
###### Proposition

The [[smooth spectra]] $\mathcal{K}(\mathbf{Vect})$ and $\mathcal{K}(\mathbf{Vect}_{conn})$ are both differential refinements, def. \ref{DifferentialCoefficients}, of connective [[KU|ku]], both whose underlying [[geometrically discrete infinity-groupoid|geometrically discrete spectrum]] is the [[algebraic K-theory]] $K \mathcal{C}$ of the [[complex numbers]]:

1. $\Pi(\mathcal{K}(Vect^\oplus)) \simeq \Pi(\mathcal{K}(Vect_{conn}^\oplus))\simeq ku$;

1. $\flat(\mathcal{K}(Vect^\oplus)) \simeq \flat(\mathcal{K}(Vect_{conn}^\oplus))\simeq K \mathbb{C}$.

1. in both cases the [[points-to-pieces transform]] $\flat \to \Pi$ is the [[comparison map between algebraic and topological K-theory]] $K \mathbb{C}\to ku$.

=--

([Bunke-Nikolaus-V&#246;lkl 13, lemma 6.3, corollary 6.5](#BunkeNikolausVoelkl13))


+-- {: .num_prop #SmoothRegulator}
###### Proposition

The traditonal [[Chern character]] induces, via the [[universal property]] of the [[homotopy pullback]] in def. \ref{HopkinsSingerPullback}, a morphism


$$
  \mathcal{K}(\mathbf{Vect}_{conn}^\oplus)
  \longrightarrow
  ku_{conn_{ch}}
$$

from the differential refinement of $ku$ given by def. \ref{KTheoryOfStackOfVectorBundles}, to that given by def. \ref{HSDifferentialKu}.

Its [[secondary characteristic class]], hence its image under the [[flat modality]], is in [[homotopy groups]] the [[regulator]]

$$
  \array{
    K\mathbb{C}_{tor} &\stackrel{\simeq}{\longrightarrow}& \mathbb{Q}/\mathbb{Z}
    \\
    \downarrow && \downarrow
    \\
    K\mathbb{C} &\stackrel{\pi_{2k-1}}{\longrightarrow}& \mathbb{C}/\mathbb{Z}
  }
$$

related to the [[Adams e-invariant]] via ([Bunke 11, section 5.3](#Bunke11)).

=--

([Bunke-Nikolaus-V&#246;lkl 13, example 6.9](#BunkeNikolausVoelkl13))


#### Via smooth Snaith's theorem
 {#ViaSmoothSnaithTheorem}

The ordinary [[Snaith theorem]] realizes [[KU]] as the localization of the [[∞-group ∞-ring]] of the [[circle 2-group]] $B U(1)$ at the [[Bott element]] $b\in \pi_2(KU)$.

$$
  KU \simeq (\Sigma_+^\infty B U(1))[b^{-1}]
  \,.
$$

With due care to define smooth geometric looping and taking the [[Hopf fibration]] as an actual smooth bundle over the smooth 2-sphere, this lifts to the smooth circle 2-group $\mathbf{B}U(1)$ and with more care to $\mathbf{B}U(1)_{conn}$ to produce [[smooth spectra]]

$$
  (\Sigma_+ \mathbf{B}U(1))[b^{-1}]
$$

and

$$
  (\Sigma_+ \mathbf{B}U(1)_{conn})[b^{-1}]
$$

which both are differential refinements, def. \ref{DifferentialCoefficients}, of [[KU]].

([Bunke-Nikolaus-V&#246;lkl 13, section 6.3](#BunkeNikolausVoelkl13))


### Complex-analytic differential generalized cohomology

The above examples all take place in the $T$[[Smooth∞Grpd]], modelling [[higher differential geometry]]. Another fundamental example of a [[cohesive (∞,1)-topos]] is [[ComplexAnalytic∞Grpd]], modelling [[complex analytic higher geometry]].

Differential cohomology in the complex-analytic context is discussed in ([Hopkins-Quick 12](#HopkinsQuick12)), see at
_[complex analytic ∞-groupoid -- Properties -- Differential cohomology](complex+analytic+∞-groupoid#DifferentialCohomology)_ for more.

### $E_\infty$-Arithmetic geometry

[[!include arithmetic cohesion -- table]]

## Related concepts


* [[intermediate Jacobian]]

## References
 {#References}

The differential cohomology hexagon was maybe first highlighted in the context of [[ordinary differential cohomology]]

* {#SimonsSullivan07} [[James Simons]], [[Dennis Sullivan]], _Axiomatic Characterization of Ordinary Differential Cohomology_,  Journal of Topology 1.1 (2008): 45-56. ([arXiv:math/0701077](http://arxiv.org/abs/math/0701077))

and in the context of [[differential K-theory]] in 

* {#SimonsSullivan08} [[James Simons]], [[Dennis Sullivan]], _Structured vector bundles define differential K-theory_ ([arXiv:0810.4935](http://arxiv.org/abs/0810.4935))

proven also in

* {#FreedLott10} [[Daniel Freed]], [[John Lott]], _An index theorem in differential K-theory_, Geometry and Topology 14 (2010) ([pdf](http://math.berkeley.edu/~lott/gt-2010-14-021p.pdf))


An artistic impression of the differential cohomology hexagon as a dance choreography inspired by a talk by [[James Simons]] is at

* Kyla Barkin, Aaron Selissen, _Differential Cohomology_, 2011 ([full video (37 min)](http://vimeo.com/32903887), [sequence of "The March Back" (4 min)](http://www.dancemedia.com/v/7044), [press release](http://www.businessinsider.com/jim-simons-mathematical-genius-inspired-a-ballet-2011-1))

That the differential cohomology hexagon exists not just at the level of [[exact sequences]] of [[cohomology classes]] but already at the level of [[homotopy fiber sequences]] of [[cocycle]] spaces was observed for [[ordinary differential cohomology]] and for [[differential K-theory]] in 

* Man-Ho Ho, _Refined hexagons for differential cohomology_ ([arXiv:1310.0582](http://arxiv.org/abs/1310.0582))

That generally the [[homotopy fiber product]]-construction of differential refinements of [[generalized (Eilenberg-Steenrod) cohomology]] theories due to

* {#HopkinsSinger02} [[Mike Hopkins]] and [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_ ([arXiv:math/0211216](http://arxiv.org/abs/math/0211216))

constitutes the right one of the two squares in the homotopy-theoretic version of the diagram is discussed explicitly for instance in prop 4.57 of

* {#Bunke12} [[Ulrich Bunke]], _Differential cohomology_ ([arXiv:1208.3961](http://arxiv.org/abs/1208.3961))

That every [[stable homotopy type]] in a [[cohesive (∞,1)-topos]] naturally sits in a differential cohomology diagram was observed (focusing on [[Smooth∞Grpd]]) in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_, Journal of Homotopy and Related Structures October 2014 ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))

following

* {#Schreiber13} [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_ ([arXiv:1310.7930](http://arxiv.org/abs/1310.7930))

where in section 4.1.2 a fully general abstract account is given. This in turn follows

* {#Schreiber09} [[Urs Schreiber]], _[[schreiber:Background fields in twisted differential nonabelian cohomology]]_, talk at Oberwolfach Workshop Strings, Fields, Topology (2009), Oberwolfach Report No. 28/2009 ([pdf](https://www.mfo.de/document/0924/OWR_2009_28.pdf))


Surveys/expositions of this:

* {#Schreiber14a} [[Urs Schreiber]], _[[schreiber:Differential generalized cohomology in Cohesive homotopy type theory]]_, talk at IHP trimester on _Semantics of proofs and certified mathematics_, _Workshop 1: Formalization of Mathematics_, Institut Henri Poincar&#233;, Paris, 5-9 May 2014

* {#Schreiber14b} [[Urs Schreiber]], _[[schreiber:Differential cohomology is Cohesive homotopy theory]]_, talk at _[Higher Geometric Structures along the Lower Rhine June 2014](http://www.ru.nl/math/research/vmconferences/2014-higher/)_, 19-20 June  2014

Exposition from the point of view of [[modal homotopy type theory|modal homotopy theory]]:

* [[Urs Schreiber]], _[[nLab:differential cohesion and idelic structure|Fractures, Ideles and the Differential Hexagon]]_, talk at _[Workshop on differential cohomologies](http://qcpages.qc.cuny.edu/~swilson/cunyworkshop14.html)_, CUNY Graduate Center, August 12-14 2014 ([video recording](http://videostreaming.gc.cuny.edu/videos/video/1806/in/channel/55/))

* [[Urs Schreiber]], _[[schreiber:Differential cohesion and Arithmetic geometry]]_, talk at [Karslruher Weihnachts-Workshop 2015](http://www.math.kit.edu/iag3/~herrlich/seite/weihnachts-workshops)


Formalization in [[cohesive homotopy type theory|cohesive]] [[modal homotopy type theory|modal homotopy type theory]] [[homotopy type theory]]: 

* [[David Jaz Myers]], _Modal Fracture of Higher Groups_,  talk at _[CMU-HoTT Seminar](https://www.cmu.edu/dietrich/philosophy/hott/seminars/index.html), 2021 ([pdf](http://davidjaz.com/Talks/CMU_March_2021.pdf), [[MyersModalFracture2021.pdf:file]])


For discussion of the hexagon in an [[equivariant cohomology|equivariant]] setting, see 

* [[Andreas Kübel]], [[Andreas Thom]], _Equivariant Differential Cohomology_, ([arXiv:1510.06392](https://arxiv.org/abs/1510.06392))

See also

* {#Bunke11} [[Ulrich Bunke]], _On the topological contents of eta invariants_ ([arXiv:1103.4217](http://arxiv.org/abs/1103.4217))

* {#HopkinsQuick12} [[Michael Hopkins]], [[Gereon Quick]], _Hodge filtered complex bordism_ ([arXiv:1212.2173](http://arxiv.org/abs/1212.2173))

* {#FRS13} [[Domenico Fiorenza]], [[Urs Schreiber]], [[Chris Rogers]], _Higher geometric prequantum theory_ ([arxiv:1304.0236](http://arxiv.org/abs/1304.0236))

* {#BunkeGepner13} [[Ulrich Bunke]], [[David Gepner]], _Differential function spectra, the differential Becker-Gottlieb transfer, and applications to differential algebraic K-theory_ ([arXiv:1306.0247](http://arxiv.org/abs/1306.0247))


[[!redirects differential cohomology diagrams]] 

[[!redirects differential cohomology hexagon]]

[[!redirects differential hexagon]]