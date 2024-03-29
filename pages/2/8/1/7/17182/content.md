
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Bousfield-Friedlander model structure_ ([Bousfield-Friedlander 78, section 2](#BousfieldFriedlander78)) is a [[model structure for spectra]], specifically it is a standard [[model structure on sequential spectra]] in [[simplicial sets]]. An immediate variant works for [[sequential spectra]] in [[topological spaces]], see at _[[model structure on topological sequential spectra]]_.

As such, the Bousfield-Friedlander model structure [[presentable (infinity,1)-category|presents]] the [[stable (infinity,1)-category of spectra]] of [[stable homotopy theory]], hence, in particular, its [[homotopy category]] is the classical [[stable homotopy category]].


## Background on sequential spectra

### Sequential pre-spectra

Write $S^1 \coloneqq \Delta[1]/\partial\Delta[1]$ for the minimal [[simplicial set|simplicial]] [[circle]]. Write

$$
  \wedge 
  \;\colon\;
  sSet^{\ast/}
  \times
  sSet^{\ast/}
  \longrightarrow
  sSet^{\ast/}
$$

for the [[smash product]] of [[pointed simplicial sets]].


+-- {: .num_defn #SequentialSpectra}
###### Definition

A **[[sequential spectrum|sequential]] [[prespectrum]] in [[simplicial sets]]**, or just **[[sequential spectrum]]** for short (or even just **[[spectrum]]), is

* an $\mathbb{N}$-[[graded object|graded]] [[pointed simplicial set]] $X_\bullet$ 

* equipped with morphisms $\sigma_n \colon S^1 \wedge X_n \to X_{n+1}$ for all $n \in \mathbb{N}$.

 A [[homomorphism]] $f \colon X \to Y$ of spectra is a sequence $f_\bullet \colon X_\bullet \to Y_\bullet$ of homomorphisms of pointed simplicial sets, such that all [[diagrams]] of the form

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

Write $SeqSpec(sSet)$ for this [[category]] of sequential spectra.

=--

+-- {: .num_example #SmashProductOfSpectrumWithSimplicialSet}
###### Example

For $X \in SeqSpec(sSet)$ and $K \in $ [[sSet]], hence $K_+ \in sSet^{\ast/}$ then $X \wedge K_+$ is the sequential spectrum degreewise given by the [[smash product]] of pointed objects

$$
  (X \wedge K_+)_n \coloneqq (X_n \wedge K_+)
$$

and with structure maps given by

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

+-- {: .num_defn #StableHomotopyGroups}
###### Definition

The [[stable homotopy groups]] of a [[sequential spectrum]] $X$, def. \ref{SequentialSpectra}, is the $\mathbb{Z}$-[[graded abelian groups]] given by the [[colimit]] of [[homotopy groups]] of [[geometric realizations]] of the component spaces

$$
  \pi_\bullet(X)
  \coloneqq
  \underset{\longrightarrow}{\lim}_k
  \pi_{\bullet+k}({\vert X_n \vert})
  \,.
$$

This constitutes a [[functor]]

$$
  \pi_\bullet \;\colon\; SeqSpec(sSet) \longrightarrow Ab^{\mathbb{Z}}
  \,.
$$

=--

+-- {: .num_defn #StableWeakEquivalenceOfSequentialsSetSpectra}
###### Definition

A morphism $f \colon X \longrightarrow Y$ of [[sequential spectra]], def. \ref{SequentialSpectra}, is called a [[stable weak homotopy equivalence]], if its image under the [[stable homotopy group]]-functor of def. \ref{StableHomotopyGroups} is an [[isomorphism]]

$$
  \pi_\bullet(f) \;\colon\; \pi_\bullet(X) \longrightarrow \pi_\bullet(Y)
  \,.
$$

=--



### Omega-spectra

+-- {: .num_defn #OmegaSpectrum}
###### Definition

A _[[Omega-spectrum]]_ is a sequential spectrum $X$, def. \ref{SequentialSpectra}, such that after [[geometric realization]]/[[Kan fibrant replacement]] the ([[smash product]] $\dashv$ [[pointed mapping space]])-[[adjuncts]]

$$
  {\vert X_n\vert} \stackrel{}{\longrightarrow} {\vert X^{n+1}\vert}^{{\vert S^1\vert}}
$$

of the structure maps ${\vert \sigma_n\vert}$ are [[weak homotopy equivalences]].

=--

+-- {: .num_remark #StableHomotopyGroupsOfOmegaSpectrum}
###### Remark

If a [[sequential spectrum]] $X$ is an [[Omega-spectrum]], def. \ref{OmegaSpectrum}, 
then its colimiting [[stable homotopy groups]], def. \ref{StableHomotopyGroups}, are attained as the actual homotopy groups of its components:

$$
  \pi_k(X) \simeq 
  \simeq
  \left\{
    \array{
      \pi_k {\vert X_0 \vert} & if\; k \geq 0
      \\
      \pi_0 {\vert X_k \vert} & if \; k \lt 0
    }
  \right.
  \,.
$$

=--



+-- {: .num_defn #Spectrification}
###### Definition

The canonical _$\Omega$-[[spectrification]]_ $Q X$ of a [[sequential spectrum]] $X$ of [[simplicial sets]], def. \ref{SequentialSpectra}, is the operation of forming degreewise the [[colimit]] of higher [[loop space objects]] $\Omega(-)\coloneqq (-)^{S^1}$

$$
  (Q X)_n
  \coloneqq
  \underset{\longrightarrow}{\lim}_{k }
  Sing \Omega^k {\vert X_{n+k}\vert }
  \,,
$$

where $Sing$ denotes the [[singular simplicial complex]] functor.

This constitutes an [[endofunctor]]

$$
  Q \;\colon\;  SeqSpec(sSet) \longrightarrow SeqSpec(sSet)
  \,.
$$

Write

$$
 \eta \;\colon\; id \longrightarrow Q
$$

for the [[natural transformation]] given in degree $n$ by the $({\vert-\vert}\dashv Sing)$-[[adjunction unit]] followed the 0-th component map of the colimiting [[cocone]]:

$$
  (\eta_X)_n 
    \;\colon\; 
  X_n 
    \longrightarrow
  Sing{\vert X_n\vert}
    \stackrel{\iota_0}{\longrightarrow}
  \underset{\longrightarrow}{\lim}_{k }
  Sing \Omega^k {\vert X_{n+k}\vert }
  \,.
$$


=--

+-- {: .num_prop #PropertiesOfStandardSpectrification}
###### Proposition

The [[spectrification]] of def. \ref{Spectrification} satisfies 

1. $Q X$ is an [[Omega-spectrum]], def. \ref{OmegaSpectrum};

1. $\eta_X \colon X \longrightarrow Q X$ is a [[stable weak homotopy equivalence]], def. \ref{StableWeakEquivalenceOfSequentialsSetSpectra};

1. if for a homomorphims of sequential spectra $f \colon X \longrightarrow Y$ each $f_n$ is a [[weak homotopy equivalence]], then also each $(Q X)_n$ is a weak homotopy equivalence;

1. $(Q\eta_X)$ is degreewise a weak homotopy equivalence.

=--

+-- {: .num_cor #StableWeakHomotopyEquivalencesofSeqsSetSpectraIsDegreewsieWeakHomotopyEquivalencesOfSpectrification}
###### Corollary

A homomorphism of [[sequential spectra]], def. \ref{SequentialSpectra}, is a [[stable weak homotopy equivalence]], def. \ref{StableWeakEquivalenceOfSequentialsSetSpectra}, precisely if its [[spectrification]] $Q f$ , def. \ref{PropertiesOfStandardSpectrification}, is degreewise a [[weak homotopy equivalence]].

=--


## The strict model structure on sequential spectra
 {#TheStrictModelStructure}

The [[model category]] structure on [[sequential spectra]] which [[presentable (infinity,1)-category|presents]] [[stable homotopy theory]] is the "stable model structure" discussed [below](#TheStableModelStructure). Its fibrant-cofibrant objects are (in particular) [[Omega-spectra]], hence are the proper [[spectrum objects]] among the pre-spectrum objects.

But for technical purposes it is useful to also be able to speak of a model structure on pre-spectra, which sees their homotopy theory as sequences of simplicial sets equipped with suspension maps, but not their stable structure. This is called the "strict model structure" for sequential spectra. It's main point is that the stable model structure of interest arises fromit via [[Bousfield localization of model categories|left Bousfield localization]].


+-- {: .num_defn #ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(sSet)$, def. \ref{SequentialSpectra} is

* a **strict weak equivalence** if each component $f_n \colon X_n \to Y_n$ is a weak equivalence in the [[classical model structure on simplicial sets]] (hence a [[weak homotopy equivalence]] of [[geometric realizations]]);

* a **strict fibration** if each component $f_n \colon X_n \to Y_n$ is a fibration in the [[classical model structure on simplicial sets]] (hence a [[Kan fibration]]);

* a **strict cofibration** if the simplicial maps $f_0\colon X_0 \to Y_0$ as well as all [[pushout products]] of $f_n$ with the structure maps of $X$

  $$
    X_{n+1}\underset{S^1 \wedge X_n}{\coprod} S^1 \wedge Y_n
    \longrightarrow
    Y_{n+1}
  $$

  are cofibrations of simplicial sets in the  [[classical model structure on simplicial sets]] (i.e.: [[monomorphisms]] of simplicial sets);

=--

+-- {: .num_prop #StrictModelStructureOnSequentialPrespectraIsModelCategory}
###### Proposition

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} give the structure of a [[model category]] $SeqSpec(sSet)_{strict}$, called the **strict model structure** on sequential spectra.

Moreover, this is

* a [[proper model category]];

* a [[simplicial model category]] with respect to the simplicial enrichment of prop. \ref{SimplicialEnrichment}.

=--

([Bousfield-Friedlander 78, prop. 2.2](#BousfieldFriedlander78)).


+-- {: .proof}
###### Proof

The representation of [sequential spectra as diagram spectra](sequential%20spectrum#AsDiagramSpectra) says that the category of sequential spectra is [[equivalence of categories|equivalently]] an [[enriched functor category]]

$$
  SeqSpec(sSet)
  \simeq
  [StdSpheres, sSet^{\ast/}]
$$

([this proposition](sequential+spectrum#SequentialSpectraAsDiagramSpectra)). Accordingly, this carries the [[projective model structure on enriched functors]], and unwinding the definitions, this gives the statement for the fibrations and the weak equivalences.

It only remains to check that the cofibrations are as claimed. To that end, consider a [[commuting square]] of sequential spectra

$$
  \array{
    X_\bullet &\stackrel{h_\bullet}{\longrightarrow}& A_\bullet
    \\
    \downarrow^{\mathrlap{f_\bullet}} && \downarrow
    \\
    Y_\bullet &\longrightarrow& B_\bullet
  }
  \,.
$$

By definition, this is equivalently a $\mathbb{N}$-collection of commuting diagrams of simplicial sets of the form

$$
  \array{
    X_n &\stackrel{h_n}{\longrightarrow}& A_n
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow
    \\
    Y_n &\longrightarrow& B_n
  }
$$

such that all structure maps are respected.

$$
  \array{
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{f_{n+1}}}
    \\
    Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    \\
    & \searrow && \searrow
    \\
    && B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \;\;\;
  \Rightarrow
  \;\;\;
  \array{
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    & \searrow^{\mathrlap{h_n}} && \searrow^{\mathrlap{h_{n+1}}}
    \\
    && A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
    \\
    && \downarrow && \downarrow
    \\
    && B_n &\stackrel{\sigma_n^B}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

Hence a [[lifting]] in the original diagram is a lifting in each degree $n$, such that the lifting in degree $n+1$ makes these diagrams of structure maps commute.

Since components are parameterized over $\mathbb{N}$, this condition has solutions by [[induction]]. First of all there must be an ordinary lifting in degree 0. Then assume a lifting $l_n$ in degree $n$ has been found

$$
  \array{
    X_n &\stackrel{h_n}{\longrightarrow}& A_n
    \\
    \downarrow^{\mathrlap{f_n}} &\nearrow_{\mathrlap{l_n}}& \downarrow
    \\
    Y_n &\longrightarrow& B_n
  }
$$

the lifting $l_{n+1}$ in the next degree has to also make the following diagram commute

$$
  \array{
    X_n &\stackrel{\sigma_n^X}{\longrightarrow}& X_{n+1}
    \\
    \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{h_{n+1}}}
    & \searrow 
    \\
    Y_n &\stackrel{\sigma_n^Y}{\longrightarrow}& Y_{n+1}
    && 
    \\
    & \searrow^{\mathrlap{l_n}} && \searrow^{\mathrlap{l_{n+1}}} & \downarrow
    \\
    && A_n &\stackrel{\sigma_n^A}{\longrightarrow}& A_{n+1}
  }
  \,.
$$

This is a [[cocone]] under the the commuting square for the structure maps, and therefore the outer diagram is equivalently a morphism out of the [[domain]] of the [[pushout product]] $f_n \Box \sigma_n^X$, while the compatible lift $l_{n+1}$ is equivalently a lift against this pushout product:

$$
  \array{
    Y_n \underset{X_n}{\sqcup} X_{n+1}
    &\stackrel{(\sigma_n^A l_n,h_{n+1})}{\longrightarrow}&
    A_{n+1}
    \\
    \downarrow &{}^{\mathllap{l_{n+1}}}\nearrow& \downarrow
    \\
    Y_{n+1} &\stackrel{}{\longrightarrow}& B_{n+1}
  }
  \,.
$$


=--


## The stable model structure on sequential spectra
 {#TheStableModelStructure}

+-- {: .num_defn #ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}
###### Definition

Say that a homomorphism $f_\bullet \colon X_\bullet \to Y_\bullet$ in the category $SeqSpec(sSet)$, def. \ref{SequentialSpectra} is

* a **stable weak equivalence** if it is a [[stable weak homotopy equivalence]], def. \ref{StableWeakEquivalenceOfSequentialsSetSpectra};

* a **stable cofibration** if the simplicial maps $f_0\colon X_0 \to Y_0$ as well as all [[pushout products]] of $f_n$ with the structure maps of $X$

  $$
    X_{n+1}\underset{S^1 \wedge X_n}{\coprod} S^1 \wedge Y_n
    \longrightarrow
    Y_{n+1}
  $$

  are cofibrations of simplicial sets in the [[classical model structure on simplicial sets]] (i.e.: [[monomorphisms]] of simplicial sets);

* a **stable fibration** if it is degreewise a fibration of simplicial sets, hence degreewise a [[Kan fibration]], and if in addition the naturality squares of the [[spectrification]], def. \ref{Spectrification},

  $$
    \array{
      X_n &\stackrel{}{\longrightarrow}& (Q X)_n
      \\
      \downarrow^{\mathrlap{f_n}} && \downarrow^{\mathrlap{Q f_n}}
      \\
      Y_n &\stackrel{}{\longrightarrow}& (Q Y)_n
    }
  $$

  are [[homotopy pullback]] squares (with respect to the [[classical model structure on simplicial sets]]).

=--

+-- {: .num_prop #StableModelStructureOnSequentialSpectraIsModelCategory}
###### Proposition

The classes of morphisms in def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra} give the structure of a [[model category]] $SeqSpec(sSet)_{stable}$, called the **stable model structure** on sequential spectra.

Moreover, this is

* a [[proper model category]];

* a [[simplicial model category]] with respect to the simplicial enrichment of prop. \ref{SimplicialEnrichment}.

=--

([Bousfield-Friedlander 78, theorem 2.3](#BousfieldFriedlander78)).

+-- {: .proof}
###### Proof


By corollary \ref{StableWeakHomotopyEquivalencesofSeqsSetSpectraIsDegreewsieWeakHomotopyEquivalencesOfSpectrification}, the stable model structure $SeqSpectra(sSet)_{stable}$ is, if indeed it exists, the [[left Bousfield localization]] of the strict model structure of prop. \ref{StrictModelStructureOnSequentialPrespectraIsModelCategory} at the morphisms that become weak equivalences under the [[spectrification]] functor $Q \colon SeqSpectra(sSet) \longrightarrow SeqSpectra(sSet)$, def. \ref{Spectrification}. By prop. \ref{PropertiesOfStandardSpectrification}  $Q$ satisfies the conditions of the [[Bousfield-Friedlander theorem]], and this implies the claim.

=--


+-- {: .num_remark}
###### Remark

A spectrum $X \in SeqSpec(sSet)_{stable}$ is

* fibrant precisely if it is an [[Omega-spectrum]], def. \ref{OmegaSpectrum}, and each $X_n$ is a [[Kan complex]];

* cofibrant precisely if all the structure maps $S^1 \wedge X_n \to X_{n+1}$ are cofibrations of simplicial sets, i.e. [[monomorphisms]].

=--


## Properties

### Fibrations and cofibrations
 {#FibrantAndCofibrantObjects}

+-- {: .num_prop}
###### Proposition

A [[sequential spectrum]] $X\in SeqSpec(sSet)_{stable}$ is cofibrant precisely if all its structure morphisms $S^1 \wedge X_n \to X_{n+1}$ are [[monomorphisms]].

=--

+-- {: .proof}
###### Proof

A morphism $\ast \to X$ is a cofibration according to def. \ref{ClassesOfMorphismsOfTheStrictModelStructureOnSequentialSpectra} (in either the strict or stable model structure, they have the same cofibrations) if 

1. $X_0$ is cofibrant; this is no condition in [[sSet]];

1. $$
     \ast_{n+1}\underset{S^1 \wedge \ast_n}{\coprod} S^1 \wedge X_n
     \longrightarrow
     X_{n+1}
   $$

   is a cofibration. But in this case the [[pushout]] reduces to just its second summand, and so this is now equivalent to

   $$
     S^1 \wedge X_n \longrightarrow X_{n+1}
   $$

   being cofibrations;  hence inclusions.

=--

### Relation to sequential spectra in $Top$ and to combinatorial spectra

+-- {: .num_prop}
###### Proposition

There is a [[zig-zag]] of [[Quillen equivalences]] relating the Bousfield-Friedlander model structure $SeqSpec(sSet)_{stable}$, def. \ref{ClassesOfMorphismsOfTheStableModelStructureOnSequentialSpectra}, prop. \ref{StableModelStructureOnSequentialSpectraIsModelCategory} with standard model structures on [[sequential spectra]] in [[topological spaces]] (the [[model structure on topological sequential spectra]]) and with Kan's [[combinatorial spectra]].

=--

([Bousfield-Friedlander 78, section 2.5](#BousfieldFriedlander78)).

### Relation to symmetric spectra

There is a [[Quillen equivalence]] to the [[model structure on symmetric spectra]] ([Hovey-Shipley-Smith 00, section 4.3](#HoveyShipleySmith00), [Mandell-May-Schwede-Shipley 01, theorem 0.1](#MandellMaySchwedeShipley01)).

### Relation to excisive functors
 {#RelationToExcisiveFunctors}

There is a [[Quillen equivalence]] between the Bousfield-Friedlander model structure and a [[model structure for excisive functors]] ([Lydakis 98](#Lydakis98)).

+-- {: .num_defn #SimplicialSetsPointedAndFinite}
###### Definition

Write

* [[sSet]] for the [[category]] of [[simplicial sets]];

* $sSet^{\ast/}$ for the category of [[pointed object|pointed]] simplicial sets;

* $sSet_{fin}^{\ast/}\simeq s(FinSet)^{\ast/} \hookrightarrow sSet^{\ast/}$ for the [[full subcategory]] of [[pointed object|pointed]] [[simplicial object|simplicial]] [[finite sets]].

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

In order to compare this to to [[sequential spectra]] consider also the following variant.

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

([Lydakis 98, def. 4.2](#Lydakis98))



+-- {: .num_prop #SequentialSpectraAsSimplicialFunctorsOnStandardSpheres}
###### Proposition

There is an $sSet^{\ast/}$-[[enriched functor]]

$$
  (-)^seq
  \;\colon\;
  [StdSpheres,sSet^{\ast/}]
    \longrightarrow
  SeqSpec(sSet)
$$

(from the category of $sSet^{\ast/}$-[[enriched presheaves|enriched copresheaves]] on the categories of standard simplicial spheres of def. \ref{CategoriesOfStandardSpheres} to the category of sequential spectra in [[sSet]], def. \ref{Spectra}) given on objects by sending $X \in [StdSpheres,sSet^{\ast/}]$ to the sequential spectrum $X^{seq}$ with components

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

([Lydakis 98, prop. 4.3](#Lydakis98))


+-- {: .num_prop}
###### Proposition

The [[adjunction]]

$$
  (\iota_\ast \dashv \iota^\ast)
  \;\colon\;
  [sSet^{\ast/}_{fin}, sSet^{\ast/}]_{Ly}
    \stackrel{\overset{\iota_\ast}{\longleftarrow}}{\underset{\iota^\ast}{\longrightarrow}}
  [StdSpheres, sSet^{\ast/}]
    \underoverset{\simeq}{(-)^{seq}}{\longrightarrow}
  SeqSpec(sSet)_{stable}
$$

(given by restriction $\iota^\ast$ along the defining inclusion $\iota$ of def. \ref{CategoriesOfStandardSpheres} and by left [[Kan extension]] $\iota_\ast$ along $\iota$ and combined with the equivalence $(-)^{seq}$ of prop. \ref{SequentialSpectraAsSimplicialFunctorsOnStandardSpheres}) is a  [[Quillen adjunction]] and in fact a [[Quillen equivalence]] between the [[Bousfield-Friedlander model structure]] on sequential spectra and Lydakis' [[model structure for excisive functors]].

=--

([Lydakis 98, theorem 11.3](#Lydakis98)) For more details see at _[[model structure for excisive functors]]_.



## Related concepts

* [[model structure on topological sequential spectra]]



## References

The original construction is due to

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math., Vol. 658, Springer, Berlin, 1978, pp. 80-130. ([pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf), [[BousfieldFriedlanderSpectra.pdf:file]])

Generalization of this model structure from sequential pre-spectra in [[sSet]]$^{\ast/}$ to sequential spectra in more general [[proper model category|proper]] [[pointed category|pointed]] [[simplicial model categories]] is in

* {#Schwede97} [[Stefan Schwede]], _Spectra in model categories and applications to the algebraic cotangent complex_, Journal of Pure and Applied Algebra 120 (1997) 77-104 ([pdf](http://www.math.uni-bonn.de/people/schwede/modelspec.pdf))


Discussion of the [[Quillen equivalence]] to the [[model structure on excisive functors]] (which does have a [[symmetric smash product of spectra]]) is in

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))

Discussion of the [[Quillen equivalence]] to the [[model structure on symmetric spectra]] is in

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

* {#MandellMaySchwedeShipley01} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], theorem 0.1 of _Model categories of diagram spectra_, Proceedings of the London Mathematical Society, 82 (2001), 441-512 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf))

[[!redirects Bousfield-Friedlander model category]] 

[[!redirects Bousfield-Friedlander model structures]]
