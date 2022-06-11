
> under construction


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The concept of _[[solid topos]]_ is meant to be a characterization of _[[gros toposes]]_ which further refines that of [[elastic toposes]] and [[cohesive toposes]]. The idea is that we may consistently regard the [[objects]] of such toposes as [[generalized spaces]] for some flavor of [[geometry]], and that the axioms on the topos determine aspects of the geometric nature of these [[generalized spaces]], as follows:

| $\phantom{A}$[[gros topos]]$\phantom{A}$ | $\phantom{A}$[[generalized spaces]] obey...$\phantom{A}$ |
|-----|-----|
| $\phantom{A}$[[cohesion]] | $\phantom{A}$principles of [[differential topology]]$\phantom{A}$ |
| $\phantom{A}$[[elastic topos|elasticity]] | $\phantom{A}$principles of [[differential geometry]]$\phantom{A}$ |
| $\phantom{A}$[[solid topos|solidity]]$\phantom{A}$ | $\phantom{A}$principles of [[supergeometry]]$\phantom{A}$ |
{: style='margin:auto'}



## Definition


+-- {: .num_defn #SuperDifferentialCohesion}
###### Definition
**([[solid topos]])**

Let $\mathbf{H}_{bos}$ be an [[elastic topos]] ([this Def.](geometry+of+physics+--+categories+and+toposes#DifferentialCohesion)) over a [[cohesive topos]] $\mathbf{H}_{red}$ ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveTopos)). Then a _solid topos_ or _super-differentially cohesive topos_ over $\mathbf{H}_{bos}$ is a [[sheaf topos]] $\mathbf{H}$, which is 

1. a [[cohesive topos]] over [[Set]] ([this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveTopos)),

1. an [[elastic topos]] over $\mathbf{H}_{red}$ ([this Def.](geometry+of+physics+--+categories+and+toposes#DifferentialCohesion)).

1. equipped with a [[adjoint quadruple|quadruple]] of [[adjoint functors]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointFunctorsInTermsOfNaturalBijectionOfHomSets)) to $\mathbf{H}_{bos}$ of the form

   $$
     \mathbf{H}_{bos}
       \array{
         \overset{\phantom{A} even \phantom{A} }{\longleftarrow}
         \\
         \overset{\phantom{AA} \iota_{sup} \phantom{AA} }{\hookrightarrow}
         \\
         \overset{\phantom{AA} \Pi_{sup} \phantom{AA} }{\longleftarrow}
         \\
         \overset{\phantom{AA} Disc_{sup} \phantom{AA} }{\hookrightarrow}
       }
     \mathbf{H}
   $$

   hence with $\iota_{sup}$ and $Disc_{sup}$ being [[fully faithful functors]].


=--



+-- {: .num_lemma #ProgressionOfSubcategoriesOfSolidTopos}
###### Lemma
**(progression of ([[coreflective subcategory|co-]])[[reflective subcategories]] of [[solid topos]])**

Let $\mathbf{H}$ be a [[solid topos]] (Def. \ref{SuperDifferentialCohesion}) over an [[elastic topos]] $\mathbf{H}_{red}$:

$$
  Set
    \array{
      \overset{\phantom{A} \Pi_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} Disc_{red} \phantom{A} }{\hookrightarrow}
      \\
      \overset{\phantom{A} \Gamma_{red} \phantom{A} }{\longleftarrow}
      \\
      \overset{\phantom{A} coDisc_{red} \phantom{A} }{\hookrightarrow}
    }
  \mathbf{H}_{red}
    \array{
      \overset{\phantom{AA} \iota_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Pi_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc_{inf} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma_{inf} \phantom{AA} }{\longleftarrow}
      \\
      \phantom{A}
      \\
      \phantom{A \atop A}
    }
  \mathbf{H}_{bos}
    \array{
      \overset{\phantom{AA} even \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} \iota_{sup} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Pi_{sup} \phantom{AA} }{\longleftarrow}
      \\
      \overset{\phantom{AA} Disc_{sup} \phantom{AA} }{\hookrightarrow}
      \\
      \overset{\phantom{AA} \Gamma_{sup} \phantom{AA} }{\longleftarrow}
      \\
      \phantom{A}
      \\
      \phantom{A \atop A}
      \\
      \phantom{A \atop A}
    }
  \mathbf{H}
$$

Then these adjoint functors arrange and decompose as shown in the following [[diagram]]:

<center>
<img src="https://ncatlab.org/nlab/files/ProgressionSubcategoriesSuperCohesion.jpg" width="540">
</center>

Here the composite [[adjoint quadruple]]

$$
  Set
    \array{
      \overset{\Pi \simeq \Pi_{red}\Pi_{inf} \Pi_{sup} }{\longleftarrow}
      \\
      \overset{Disc = Disc_{sup} Disc_{inf} Disc_{red}}{\hookrightarrow}
      \\
      \overset{\Gamma = \Gamma_{sup} \Gamma_{inf} \Gamma_{red} }{\longleftarrow}
      \\
      \overset{\phantom{AA} coDisc \phantom{AA} }{\hookrightarrow}
    }
  \mathbf{H}
$$

exhibits the [[cohesion]] of $\mathbf{H}$ over [[Set]], and the composite adjoint quadruple

$$
  \mathbf{H}_{red}
    \array{
      \overset{\iota_{sup} \iota_{inf}}{\hookrightarrow}
      \\
      \overset{\Pi_{inf} \Pi_{sup} }{\longleftarrow}
      \\
      \overset{Disc_{inf} Disc_{red}}{\hookrightarrow}
      \\
      \overset{ \Gamma_{sup} }{\longleftarrow}
    }
  \mathbf{H}
$$

exhibits the [[elastic topos|elasticity]] of $\mathbf{H}$ over $\mathbf{H}_{red}$.


=--

+-- {: .proof}
###### Proof

As in the proof of [this Prop.](geometry+of+physics+--+categories+and+toposes#ProgressionOfSubcategoriesOfElasticTopos),  this is immediate by the essential uniqueness of adjoints ([this Prop.](geometry+of+physics+--+categories+and+toposes#UniquenessOfAdjoints)) and of the [[global section]]-[[geometric morphism]] ([this Example](geometry+of+physics+--+categories+and+toposes#GlobalSectionsGeometricMorphism)).

=--

+-- {: .num_defn #SuperDiffCohesiveModalities}
###### Definition
**([[adjoint modalities]] on [[solid topos]])** 

Given a [[solid topos]] $\mathbf{H}$ over $\mathbf{H}_{bos}$ (Def. \ref{SuperDifferentialCohesion}), [[composition]] of the functors in Lemma \ref{ProgressionOfSubcategoriesOfSolidTopos} yields, via [this Prop.](geometry+of+physics+--+categories+and+toposes#ModalOperatorsEquivalentToReflectiveSubcategories), the following [[adjoint modalities]] ([this Def.](geometry+of+physics+--+categories+and+toposes#AdjointModality))

$$
  \rightrightarrows
  \;\dashv\;
  \rightsquigarrow
  \;\dashv\;
  Rh
  \;\;\colon\;\;
  \mathbf{H}
    \array{
      \overset{ \rightrightarrows \;\coloneqq\; \iota_{sup} \circ even  }{\longleftarrow}
      \\
      \overset{\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}  }{\longrightarrow}
      \\
      \overset{ Rh \;\coloneqq\; Disc_{sup}  \circ \Pi_{sup} }{\longleftarrow}
    }
  \mathbf{H}
  \,.
$$

Since $\iota_{sup}$ and $Disc_{sup}$ are [[fully faithful functors]] by assumption, these are ([[comodal operator|co-]])[[modal operators]] ([this Def.](geometry+of+physics+--+categories+and+toposes#ModalOperator)) on the [[cohesive topos]], by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModalOperatorsEquivalentToReflectiveSubcategories).

We pronounce these as follows:

| $\phantom{A}$ [[fermionic modality]] $\phantom{A}$ | $\phantom{A}$ [[bosonic modality]] $\phantom{A}$ | $\phantom{A}$ [[rheonomy modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $\rightrightarrows \;\coloneqq\; \iota_{sup} \circ even$  $\phantom{A}$ | $\phantom{A}$ $\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ Rh \;\coloneqq\; Disc_{sup} \circ \Pi_{sup} $ $\phantom{A}$  |
{: style='margin:auto'}

and we refer to the corresponding [[modal objects]] ([this Def.](geometry+of+physics+--+categories+and+toposes#ModalObjects)) as follows:

* a $\rightsquigarrow$-[[comodal object]]

  $$
    \overset{\rightsquigarrow}{X}
      \underoverset{\simeq}{\epsilon^\rightsquigarrow_X}{\longrightarrow}
    X
  $$

  is called a _[[bosonic object]]_;

* a $Rh$-[[modal object]]

  $$
    X
      \underoverset{\simeq}{ \eta^{Rh}_X}{\longrightarrow}
    Rh X
  $$

  is called a _rheonomic object_;


=--


+-- {: .num_prop #ProgressionOfModalitiesOnElasticTopos}
###### Proposition
**(progression of [[adjoint modalities]] on [[solid topos]])**

Let $\mathbf{H}$ be a [[solid topos]] (Def. \ref{SuperDifferentialCohesion}) and consider the [[adjoint modalities]] which it inherits 

1. for being a [[cohesive topos]], from [this Def.](geometry+of+physics+--+categories+and+toposes#CohesiveModalities), 

1. for being an [[elastic topos]], from [this Def.](geometry+of+physics+--+categories+and+toposes#DiffCohesiveModalities), 

1. for being a [[solid topos]], from Def. \ref{SuperDiffCohesiveModalities}:


| $\phantom{A}$ [[shape modality]] $\phantom{A}$ | $\phantom{A}$ [[flat modality]] $\phantom{A}$ | $\phantom{A}$ [[sharp modality]] $\phantom{A}$ |
|--------------------|-------------------|--------------------|
|   $\phantom{A}$  $&#643; \;\coloneqq\; Disc \Pi$  $\phantom{A}$ | $\phantom{A}$ $\flat \;\coloneqq\; Disc \circ \Gamma$ $\phantom{A}$  | $\phantom{A}$ $\sharp \;\coloneqq\; coDisc \circ \Gamma $ $\phantom{A}$  |
|   |   |   |
| $\phantom{A}$ **[[reduction modality]]** $\phantom{A}$ | $\phantom{A}$ **[[infinitesimal shape modality]]** $\phantom{A}$ | $\phantom{A}$ **[[infinitesimal flat modality]]** $\phantom{A}$ |
|   $\phantom{A}$  $\Re \;\coloneqq\; \iota_{sup} \iota_{inf} \circ \Pi_{inf}\Pi_{sup}$  $\phantom{A}$ | $\phantom{A}$ $\Im \;\coloneqq\; Disc_{sup} Disc_{inf} \circ \Pi_{inf} \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ \& \;\coloneqq\; Disc_{sup} Disc_{inf} \circ \Gamma_{inf}\Gamma_{sup} $ $\phantom{A}$  |
|   |    |    |
| $\phantom{A}$ **[[fermionic modality]]** $\phantom{A}$ | $\phantom{A}$ **[[bosonic modality]]** $\phantom{A}$ | $\phantom{A}$ **[[rheonomy modality]]** $\phantom{A}$ |
|   $\phantom{A}$  $\rightrightarrows \;\coloneqq\; \iota_{sup} \circ even$  $\phantom{A}$ | $\phantom{A}$ $\rightsquigarrow \;\coloneqq\; \iota_{sup} \circ \Pi_{sup}$ $\phantom{A}$  | $\phantom{A}$ $ Rh \;\coloneqq\; Disc_{sup} \circ \Pi_{sup} $ $\phantom{A}$  |
{: style='margin:auto'}

Then these arrange into the following progression, via the [[preorder]] on modalities from [this Def.](geometry+of+physics+--+categories+and+toposes#PreorderOnModalities):

$$
  \array{    
    id &\dashv& id
    \\
    \vee && \vee
    \\
    \rightrightarrows &\dashv& \rightsquigarrow &\dashv& Rh
    \\
    && \vee && \vee
    \\
    && \Re &\dashv& \Im &\dashv& \&
    \\
    && && \vee && \vee
    \\
    && && &#643; &\dashv& \flat &\dashv& \sharp
    \\
    && && && \vee && \vee
    \\
    && && && \emptyset &\dashv& \ast
  }
$$

where we are displaying, for completeness, also the [[adjoint modalities]]  at the [[bottom]] $\emptyset \dashv \ast$ and the [[top]] $id \dashv id$  ([this Example](geometry+of+physics+--+categories+and+toposes#InitialAndFinalAdjointModality)).

=--

+-- {: .proof}
###### Proof

By [this Prop.](geometry+of+physics+--+categories+and+toposes#ProgressionOfModalitiesOnElasticTopos), it just remains to show that for all [[objects]] $X \in \mathbf{H}$

1. $\Im X$ is an $Rh$-[[modal object]], hence $Rh \Im X \simeq X$,

1. $\Re X$ is a [[bosonic object]], hence $\overset{\rightsquigarrow}{\Re X} \simeq \Re X$.

The proof is directly analogous to the proof of [that Prop.](geometry+of+physics+--+categories+and+toposes#ProgressionOfModalitiesOnElasticTopos), now using the decompositions from Lemma \ref{ProgressionOfSubcategoriesOfSolidTopos}:

$$
  \begin{aligned}
    Rh \Im 
    & =
    Disc_{sup} 
    \underset{
      \simeq id
    }{
    \underbrace{
      \Pi_{sup} \;\; Disc_{sup}
    } 
    }
    Disc_{inf} \Pi_{inf} \Pi_{sup}
    \\
    & \simeq 
    Disc_{sup} Disc_{inf} \Pi_{inf} \Pi_{sup}
    \\
    & = \Im
  \end{aligned}
$$

and

$$
  \begin{aligned}
    \rightsquigarrow \Re
    & =
    \iota_{sup} 
    \underset{\simeq id}{\underbrace{
    \Pi_{sup} \;\; \iota_{sup}}}
    \iota_{inf} \Pi_{inf}\Pi_{sub}
    \\
    & \simeq
    \iota_{sup} \iota_{inf} \Pi_{inf} \Pi_{sub}    
    \\
    & \simeq \Re
  \end{aligned}
$$

=--

## Examples

### Super formal smooth sets

The [[sheaf topos]] of [[super formal smooth sets]] is solid over that of [[formal smooth sets]], which is [[elastic topos|elastic]] over that of [[smooth sets]], which is [[cohesive topos|cohesive]] over [[Set]].

See [this Prop](geometry+of+physics+--+supergeometry#SuperSmoothSetsSystemOfAdjunctions) at _[[geometry of physics -- supergeometry]]_.

[[!redirects super-differentially cohesive topos]]

[[!redirects solid model topos]]
[[!redirects solid model toposes]]

[[!redirects ∞-solid site]]
[[!redirects ∞-solid sites]]

