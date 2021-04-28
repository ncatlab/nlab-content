+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition 

The concept of _adjoint functors_ is a key concept in [[category theory]], if not _the_ key concept.[^LawvereOnAdjointFunctors] It embodies the concept of [[representable functors]] and has as special cases [[universal constructions]] such as [[Kan extensions]] and hence of [[limits]]/[[colimits]]. 

[^LawvereOnAdjointFunctors]: "the universality of the concept
of adjointness, which was first isolated and named in the conceptual sphere of category theory" ([Lawvere 69](#Lawvere69)) "In all those areas where category theory is actively used the categorical concept of adjoint functor has come to play a key role." (first line from _[An interview with William Lawvere](https://ncatlab.org/nlab/show/William+Lawvere#Interview07)_, paraphrasing the first paragraph of _[Taking categories seriously](William+Lawvere#TakingCategoriesSeriously)_)

More abstractly, the concept of adjoint functors is itself just the special case of the general concept of an _[[adjunction]]_ in a [[2-category]], here for the 2-category [[Cat]] of all categories. But often "[[adjunction]]" is understood by default in this special case.


There are various different but equivalent characterizations of adjoint functors, some of which are discussed below.


### In terms of Hom isomorphism
 {#InTermsOfHomIsomorphism}

We discuss here the definition of adjointness of functors $L \dashv R$ in terms of a [[natural bijection]] between [[hom-sets]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} below):

$$
  \{L(c) \to d\} \;\simeq\; \{ c \to R(d) \}
$$

We show that this is equivalent to the abstract definition, in terms of an [[adjunction]] in the [[2-category]] [[Cat]], in Prop. \ref{AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat} below.

$\,$


+-- {: .num_defn #AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}
###### Definition
**([[adjoint functors]] in terms of [[natural bijections]] of [[hom-sets]])**

Let $\mathcal{C}$ and $\mathcal{D}$ be two [[categories]], and let 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

be a pair of [[functors]] between them, as shown. Then this is called a _pair of [[adjoint functors]]_ (or an _[[adjoint pair]] of [[functors]]_) with $L$ _[[left adjoint]]_ and $R$ _[[right adjoint]]_, denoted 


\begin{center}
  \begin{tikzcd}
    \mathcal{D}
     \arrow[r, shift right=6pt, "R"', "\bot"]
    & 
    \mathcal{C}
     \arrow[l, shift right=6pt, "L"']
  \end{tikzcd}
\end{center}


if there exists a [[natural isomorphism]] between the [[hom-functors]] of the following form:

\[
  \label{HomIsomorphismForAdjointFunctors}
  Hom_{\mathcal{D}}(L(-),-) \;\simeq\; Hom_{\mathcal{C}}(-,R(-))
  \,.
\]

This means that for all [[objects]] $c \in \mathcal{C}$ and $d \in \mathcal{D}$ there is a [[bijection]] of [[hom-sets]]

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d) 
      &\overset{\simeq}{\longrightarrow}& 
    Hom_{\mathcal{C}}(c,R(d))
    \\
    ( L(c) \overset{f}{\to} d )
    &\mapsto&
    (c \overset{\widetilde f}{\to} R(d))
  }
$$

which is [[natural bijection|natural]] in $c$ and $d$.  This isomorphism is the **adjunction isomorphism** and the [[image]] $\widetilde f$ of a morphism $f$ under this bijections is called the _[[adjunct]]_ of $f$. Conversely, $f$ is called the adjunct of $\widetilde f$.

Naturality here means that for every [[morphism]] $g \colon c_2 \to c_1$ in $\mathcal{C}$ and for every [[morphism]] $h\colon d_1\to d_2$ in $\mathcal{D}$, the resulting square

\[
  \label{NaturalitySquareForAdjointnessOfFunctors}
  \array{
    Hom_{\mathcal{D}}(L(c_1), d_1) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1, R(d_1))
    \\
    {}^{\mathllap{Hom_{\mathcal{D}}(L(g), h)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(g, R(h))}}
    \\
    Hom_{\mathcal{D}}(L(c_2),d_2)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2,R(d_2))
  }
\]

[[commuting square|commutes]] (see also at _[[hom-functor]]_ for the definition of the vertical maps here). 

Explicitly, this commutativity, in turn, means that for every morphism $f \;\colon\; L(c_1) \to d_1$ with [[adjunct]] $\widetilde f \;\colon\; c_1 \to R(d_1)$, the adjunct of the [[composition]] is

$$
  \array{
    L(c_1) & \overset{f}{\longrightarrow} & d_1
    \\
    {}^{\mathllap{L(g)}}\big\uparrow && \big\downarrow^{\mathrlap{h}}
    \\
    L(c_2) && d_2
  }
  \;\;\;=\;\;\;
  \array{
    c_1 &\overset{\widetilde f}{\longrightarrow}& R(d_1)
    \\
    {}^{\mathllap{g}}\big\uparrow && \big\downarrow^{\mathrlap{R(h)}}
    \\
    c_2 && R(d_2)
  }
$$

=--

+-- {: .num_defn #AdjunctionUnitFromHomIsomorphism}
###### Definition
**([[adjunction unit]] and [[adjunction counit|counit]] in terms of hom-isomorphism)

Given a pair of [[adjoint functors]] 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{C}
$$
according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} one says that 

1. for any $c \in \mathcal{C}$ the [[adjunct]] of the [[identity morphism]] on  $L(c)$ is the _[[unit of an adjunction|unit morphism]]_ of the adjunction at that object, denoted

   $$
     \eta_c \coloneqq \widetilde{id_{L(c)}} \;\colon\; c \longrightarrow R(L(c))
   $$

1. for any $d \in \mathcal{D}$ the [[adjunct]] of the [[identity morphism]] on  $R(d)$ is the _[[counit of an adjunction|counit morphism]]_ of the adjunction at that object, denoted

   $$
     \epsilon_d \;\colon\; L(R(d)) \longrightarrow d
   $$



=--

+-- {: .num_prop #GeneralAdjunctsInTermsOfAdjunctionUnitCounit}
###### Proposition
**(general [[adjuncts]] in terms of [[adjunction unit|unit/counit]])**

Consider a pair of [[adjoint functors]] 

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot}
  \mathcal{C}
$$

according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, with [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ according to Def. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Then

1. The [[adjunct]] $\widetilde f$ of any morphism $L(c) \overset{f}{\to} d$ is obtained from $R$ and $\eta_c$ as the [[composition|composite]]

   \[
     \label{AdjunctFormula}
     \widetilde f 
     \;\colon\;
     c 
       \overset{\eta_c}{\longrightarrow} 
     R(L(c))
       \overset{R(f)}{\longrightarrow}
     R(d)
   \]

   Conversely, the [[adjunct]] $f$ of any morphism $c \overset{\widetilde f}{\longrightarrow} R(d)$ is obtained from $L$ and $\epsilon_d$ as

   \[
     \label{ConverseAdjunctFormula}
     f
     \;\colon\;
     L(c) 
       \overset{L(\widetilde f)}{\longrightarrow} 
     L(R(d))
       \overset{\epsilon_d}{\longrightarrow}
     d
   \]

1. The [[adjunction units]] $\eta_c$ and [[adjunction counits]] $\epsilon_d$ are components of [[natural transformations]] of the form

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

1. The [[adjunction unit]] and [[adjunction counit]] satisfy the [[triangle identities]], saying that

   $$
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   $$

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

For the first statement, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c)}
     \in 
    &
    Hom_{\mathcal{D}}(L(c), L(c)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c, R(L(c)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(id), f)}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(id, R(f))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c), d)
    &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}( c, R(d) )
  }
$$

and consider the element $id_{L(c_1)}$ in the top left entry. Its image under going down and then right in the diagram is $\widetilde f$, by Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}. On the other hand, its image under going right and then down is $ R(f)\circ \eta_{c}$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown, for the adjunct of $f$.

The converse formula follows analogously.

The third statement follows directly from this by applying these formulas for the [[adjuncts]] twice and using that the result must be the original morphism:

$$
  \begin{aligned}
    id_{L(c)}
    & =
    \widetilde \widetilde { id_{L(c)} }
    \\
    & = \widetilde{ c \overset{\eta_c}{\to} R(L(c))  }
    \\
    & = 
     L(c) 
       \overset{L(\eta_c)}{\longrightarrow} 
     L(R(L(c))) 
       \overset{\epsilon_{L(c)}}{\longrightarrow}
     L(c)
  \end{aligned}
$$

For the second statement, we have to show that for every morphism $f \colon c_1 \to c_2$ the following [[commuting square|square commutes]]:

$$
  \array{    
     c_1 &\overset{f}{\longrightarrow}& c_2
     \\
     {}^{\mathllap{\eta_{c_1}}}\big\downarrow 
       && 
     \big\downarrow^{\mathrlap{\eta_{c_2}}}
     \\
     R(L(c_1))
      &\underset{ R(L(f)) }{\longrightarrow}&
     R(L(c_2))
  }
$$

To see this, consider the [[naturality square]] (eq:NaturalitySquareForAdjointnessOfFunctors) in the form 

$$
  \array{
    id_{L(c_2)}
    \in
    & Hom_{\mathcal{D}}(L(c_2), L(c_2)) 
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_2, R(L(c_2)))
    \\
    &
    {}^{\mathllap{Hom_{\mathcal{D}}(L(f),id_{L(c_2)})}}\big\downarrow
     &&
    \big\downarrow^{\mathrlap{Hom_{\mathcal{C}}(f, R(id_{L(c_2)}))}}
    \\
    &
    Hom_{\mathcal{D}}(L(c_1),L(c_2))
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(c_1,R(L(c_2)))
  }
$$

The image of the element $id_{L(c_2)}$ in the top left along the right and down is $ \eta_{c_2} \circ f$, by Def. \ref{AdjunctionUnitFromHomIsomorphism}, while its image down and then to the right is $\widetilde{L(f)} = R(L(f)) \circ \eta_{c_1}$, by the previous statement. Commutativity of the diagram means that these two morphisms agree, which is the statement to be shown.

The argument for the naturality of $\epsilon$ is directly analogous.


=--

+-- {: .num_prop #AdjointnessInTermsOfHomIsomorphismEquivalentToAdjunctionInCat}
###### Proposition
**(adjointness in terms of hom-isomorphism equivalent to adjunction in $Cat$)**

Two functors

$$
  \mathcal{D}
    \underoverset
      {\underset{R}{\longrightarrow}}{\overset{L}{\longleftarrow}}{}
  \mathcal{C}
$$

are an [[adjoint pair]] in the sense that there is a [[natural isomorphism]] (eq:HomIsomorphismForAdjointFunctors) according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, precisely if they participate in an [[adjunction]] in the [[2-category]] [[Cat]], meaning that 

1. there exist [[natural transformations]] 

   $$
     \eta \;\colon\; Id_{\mathcal{C}} \Rightarrow R \circ L
   $$

   and

   $$
     \epsilon \;\colon\; L \circ R \Rightarrow Id_{\mathcal{D}}
   $$

2. which satisfy the [[triangle identities]]

   $$
      id_{L(c)}
      \;\colon\;
      L(c) 
        \overset{L(\eta_c)}{\longrightarrow} 
      L(R(L(c))) 
        \overset{\epsilon_{L(c)}}{\longrightarrow}
      L(c)
   $$

   and

   $$
     id_{R(d)}
     \;\colon\;
     R(d)
       \overset{\eta_{R(d)}}{\longrightarrow}
     R(L(R(d)))
       \overset{R(\epsilon_d)}{\longrightarrow}
     R(d)
   $$

=--

+-- {: .proof}
###### Proof

That a hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) implies units/counits satisfying the [[triangle identities]] is the statement of the second two items of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

Hence it remains to show the converse. But the argument is along the same lines as the proof of Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}: We now _define_ forming of adjuncts by the formula (eq:AdjunctFormula). That the resulting assignment $f \mapsto \widetilde f$ is an [[isomorphism]] follows from the computation

$$
  \begin{aligned}
    \widetilde {\widetilde f}
    & =
    \widetilde{ c \overset{\eta_c}{\to} R(L(c)) \overset{R(f)}{\to} R(d) }
    \\
    & =
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c))) \overset{L(R(f))}{\to} L(R(d)) \overset{\epsilon_d}{\to} d
    \\ 
    & = 
    L(c) \overset{L(\eta_c)}{\to} L(R(L(c)))
         \overset{ \epsilon_{L(c)} }{\to}  L(c)
         \overset{f}{\longrightarrow} d
    \\
    & =  L(c) \overset{f}{\longrightarrow} d
  \end{aligned}
$$

where, after expanding out the definition, we used [[natural transformation|naturality]] of $\epsilon$ and then the [[triangle identity]]. 

Finally, that this construction satisfies the naturality condition (eq:NaturalitySquareForAdjointnessOfFunctors) follows from the functoriality of the functors involved, and the naturality of the unit/counit: 

$$
  \array{
    c_2 &\overset{ \eta_{c_2} }{\longrightarrow}& R(L(c_2))
    \\
    {}^{\mathllap{g}}\downarrow && \downarrow^{\mathrlap{R(L(g))}}
    & \searrow^{\mathrlap{ R( L(g) \circ f ) }}
    \\
    c_1 
      &\overset{\eta_{c_1}}{\longrightarrow}& 
    R(L(c_1))
     &\overset{R(f)}{\longrightarrow}&
    R(d_1)
    \\
    && & {}_{R( h\circ f)}\searrow & \downarrow^{\mathrlap{ R(h) }}
    \\
    && && R(d_2)
  }
$$


=--


### In terms of representable functors
 {#InTermsOfRepresentableFunctors}

The condition (eq:HomIsomorphismForAdjointFunctors) on adjoint functors $L \dashv R$ in Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets} implies in particular that for every [[object]] $d \in \mathcal{D}$ the functor $Hom_{\mathcal{D}}(L(-),d)$ is a _[[representable functor]]_ with _[[representing object]]_ $R(d)$. The following Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} observes that the existence of such [[representing objects]] for all $d$ is, in fact, already sufficient to imply that there is a right adjoint functor.

This equivalent perspective on adjoint functors makes manifest that:

1. adjoint functors are, if they exist, unique up to natural isomorphism, this is Prop. \ref{UniquenessOfAdjoints} below;

1. the concept of adjoint functors makes sense also _[[relative adjoint functor|relative]]_ to a [[full subcategory]] on which representing objects exists, this is the content of Remark \ref{RelativeAdjointFunctors} below.


#### Global definition

+-- {: .num_prop #AdjointFunctorFromObjectwiseRepresentingObject}
###### Proposition
**(adjoint functor from objectwise [[representing object]])**

A [[functor]] $L \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$ has a [[right adjoint]] $R \;\colon\; \mathcal{D} \to \mathcal{C}$, according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}, already if 
for all [[objects]] $d \in \mathcal{D}$ there is an object $R(d) \in \mathcal{C}$ such that there is a [[natural isomorphism]]

   $$ 
     Hom_{\mathcal{D}}(L(-),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(-,R(d))
     \,,
   $$

   hence for each [[object]] $c \in \mathcal{C}$ a [[bijection]]

   $$
     Hom_{\mathcal{D}}(L(c),d)
     \underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}
     Hom_{\mathcal{C}}(c,R(d))
   $$

   such that for each [[morphism]] $g \;\colon\; c_2 \to c_1$, the following [[commuting diagram|diagram commutes]]

   \[
     \label{HalfNaturalitySquareForAdjointnessOfFunctors}
     \array{
       Hom_{\mathcal{D}}(L(c_1),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_1,R(d))
       \\
       {}^{\mathllap{ Hom_{\mathcal{C}}(L(g),id_d) }}
       \big\downarrow 
       &&
       \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( f, id_{R(d)}  ) }}
       \\
       Hom_{\mathcal{D}}(L(c_2),d)
         &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
       Hom_{\mathcal{C}}(c_2,R(d))
     }
   \]

   (This is as in (eq:NaturalitySquareForAdjointnessOfFunctors), except that only naturality in the first variable is required.)

In this case there is a unique way to extend $R$ from a function on [[objects]] to a function on [[morphisms]] such as to make it a [[functor]] $R \colon \mathcal{D} \to \mathcal{C}$ which is [[right adjoint]] to $L$.
, and hence the statement is that with this, naturality in the second variable is already implied.

=--

+-- {: .proof}
###### Proof

Notice that 

1. in the language of [[presheaves]] the assumption is that for each $d \in \mathcal{D}$ the presheaf 

   $$
     Hom_{\mathcal{D}}(L(-),d)
     \;\in\;
     [\mathcal{C}^{op}, Set]
   $$

   is [[representable functor|represented]] by the object $R(d)$, and [[natural transformation|naturally]] so. 

1. In terms of the [[Yoneda embedding]]

   $$
     y 
       \;\colon\;
     \mathcal{C}
      \hookrightarrow
     [\mathcal{C}^{op}, Set]
   $$ 

   we have 

   \[
     \label{YonedanotationForRepresentable}
     Hom_{\mathcal{C}}(-,R(d))
     =
     y(R(d))
   \]



The condition (eq:NaturalitySquareForAdjointnessOfFunctors) says equivalently that $R$ has to be such that for all [[morphisms]] $h \;\colon\; d_1 \to d_2 $ the following diagram in the [[category of presheaves]] $[\mathcal{C}^{op}, Set]$ [[commuting diagram|commutes]]

$$
  \array{
    Hom_{\mathcal{D}}(L(-),d_1)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-,R(d_1))
    \\
    {}^{\mathllap{ Hom_{\mathcal{C}}( L(-) , h ) }}
    \big\downarrow 
    &&
    \big\downarrow^{\mathrlap{ Hom_{\mathcal{C}}( -, R(h)  ) }}
    \\
    Hom_{\mathcal{D}}(L(-),d_2)
      &\underoverset{\simeq}{\widetilde{(-)}}{\longrightarrow}&
    Hom_{\mathcal{C}}(-, R(d_2))
  }
$$

This manifestly has a unique solution 

$$
  y(R(h))
  \;=\;
  Hom_{\mathcal{C}}(-,R(h))
$$ 

for every morphism $h \colon d_1 \to d_2$ under  $y(R(-))$ (eq:YonedanotationForRepresentable). But the [[Yoneda embedding]] $y$ is a [[fully faithful functor]] ([this prop.](Yoneda+embedding#YonedaEmbeddingIsFullyFaithful)), which means that thereby also $R(h)$ is uniquely fixed.

=--

+-- {: .num_remark}
###### Remark

In more fancy language, the statement of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} is the following:

By precomposition $L$ defines a functor of [[presheaf categories]]

$$
  L^* \;\colon\; [\mathcal{D}^{op}, Set] \to [\mathcal{C}^{op}, Set]
  \,.
$$

By [[restriction]] along the [[Yoneda embedding]] $y \;\colon\; \mathcal{D} \to [\mathcal{D}^{op}, Set]$ this yields the functor

$$
  \bar L 
  \;\colon\; 
  \array{
    \mathcal{D} 
      &\overset{y}{\longrightarrow}&
    [\mathcal{D}^{op}, Set] 
      &\overset{L^*}{\longrightarrow}&
    [\mathcal{C}^{op}, Set]
    \\
    d 
      &\mapsto& 
    Hom_{\mathcal{D}}(-,d)
      &\mapsto&
    Hom_{\mathcal{D}}(L(-),d)
 }
 \,.
$$

The statement is that for all $d \in D$ this presheaf $\bar L(d)$ is [[representable functor|representable]], then it is functorially so in that there exists a functor $R \colon \mathcal{D} \to \mathcal{C}$ such that

$$
  \bar L \;\simeq\; y \circ R
  \,.
$$

=--


#### Local definition 
 {#LocalDefinition}

+-- {: .num_remark #RelativeAdjointFunctors}
###### Remark
**([[relative adjoint functors]])**

The perspective of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} has the advantage that it yields useful information even if the adjoint functor $R$ does not exist globally, i.e. as a functor on all of $\mathcal{D}$:

It may happen that

$$
  \bar L(d) \coloneqq Hom_D(L(-),d) \in [C^{op}, Set]
$$

is [[representable functor|representable]] for _some_ [[object]] $d \in \mathcal{D}$ but not for all $d$. The representing object may still usefully be thought of as $R(d)$, and in fact it may be viewed as a right adjoint to $L$ _relative to_ the inclusion of the [[full subcategory]] determined by those $d$s for which $\bar L(d)$ is representable; see [[relative adjoint functor]] for more.

This _global_ versus _local_ evaluation of adjoint functors induces the global/local pictures of the definitions

* [[limit]] / [[homotopy limit]]

* [[Kan extension]]

as discussed there.

=--


### In terms of universal factorization through a (co)unit
 {#UniversalArrows}

We have seen in Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit} that the [[unit of an adjunction]] and [[counit of an adjunction]] plays a special role. One may amplify this by characterizing these morphisms as _[[universal arrows]]_ in the sense of the following Def. \ref{UniversalArrow}. In fact the existence of these is already equivalent to the existence of an adjoint functor, this is the statement of Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} below.

$\,$

+-- {: .num_defn #UniversalArrow}
###### Definition
**(universal arrow)**

Given a [[functor]] $R \;\colon\; \mathcal{D} \to \mathcal{C}$, and an object $c\in \mathcal{C}$, a _universal arrow_ from $c$ to $R$ is an [[initial object]] of the [[comma category]] $(c/R)$.  This means that it consists of 

1. an [[object]] $L(c)\in \mathcal{D}$ 

1. a [[morphism]] $\eta_c \;\colon\; c \to R(L(c))$, to be called the _[[adjunction unit|unit]]_,

such that for any $d\in \mathcal{D}$, any morphism $f \colon c\to R(d)$ factors through this unit $\eta_c$ as 

\[
  \label{UniversalArrowFactorization}
  \array{
    && c 
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d)
    \\
    \\
    L(c) &&\underset{ \widetilde f}{\longrightarrow}&& d
  }
\]

for a unique $\widetilde f  \;\colon\; L(c) \longrightarrow d$, to be called the [[adjunct]] of $f$.  

=--

(e.g [Borceux, vol 1, Def. 3.1.1](#Borceux))


+-- {: .num_prop #UniversalMorphismsAreInitialObjectsInCommaCategory}
###### Proposition
**([[universal morphisms]] are [[initial objects]] in the [[comma category]])**

Let $R: \mathcal{D} \to \mathcal{C}$ be a [[functor]] and $c \in \mathcal{C}$ an [[object]]. Then the following are equivalent:

1. $c \overset{\eta_c}{\to} R(L(c))$ is a [[universal morphism]] into $R(L(c))$ (Def. \ref{UniversalArrow});

1. $(c, \eta_c)$ is the [[initial object]] in the [[comma category]] $c/R$.


=--


+-- {: .num_prop #CollectionOfUniversalArrowsEquivalentToAdjointFunctor}
###### Proposition
**(collection of [[universal arrows]] equivalent to [[adjoint functor]])**

Let $R \;\colon\; \mathcal{D} \to \mathcal{C}$ be a [[functor]]. Then the following are equivalent:

1. $R$ has a [[left adjoint]] functor $L \colon \mathcal{C} \to \mathcal{D}$ according to Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets},

1. for every [[object]] $c \in \mathcal{C}$ there is a universal arrow $c \overset{\eta_c}{\longrightarrow} R(L(c))$, according to Def. \ref{UniversalArrow}.

=--


+-- {: .proof}
###### Proof

In one direction, assume a [[left adjoint]] $L$ is given. Define the would-be universal arrow at $c \in \mathcal{C}$ to be the [[unit of an adjunction|unit of the adjunction]] $\eta_c$ via Def. \ref{AdjunctionUnitFromHomIsomorphism}. Then the statement that this really is a universal arrow is implied by Prop. \ref{GeneralAdjunctsInTermsOfAdjunctionUnitCounit}.

In the other direction, assume that universal arrows $\eta_c$ are given. The uniqueness clause in Def. \ref{UniversalArrow} immediately implies  [[bijections]] 

$$
  \array{
    Hom_{\mathcal{D}}(L(c),d) 
      &\overset{\simeq}{\longrightarrow}& 
    Hom_{\mathcal{C}}(c,R(d))
    \\
    \left( 
      L(c) \overset{\widetilde f}{\to} d
    \right)
      &\mapsto&
    \left(
      c \overset{\eta_c}{\to} R(L(c)) \overset{ R(\widetilde f) }{\to} R(d)
    \right)
  }
$$

Hence to satisfy (eq:HomIsomorphismForAdjointFunctors) it remains to show that these are [[natural transformation|natural]] in both variables. In fact, by Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} it is sufficient to show naturality in the variable $d$. But this is immediate from the functoriality of $R$ applied in (eq:UniversalArrowFactorization): For $h \colon d_1 \to d_2$ any [[morphism]], we have

$$
  \array{
    && c 
    \\
    & {}^{\mathllap{\eta_c}}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R (L(c)) &&\underset{R (\widetilde f)}{\longrightarrow}&& R(d_1)
    \\
    && {}_{\mathllap{ R( h\circ \widetilde f ) }}\searrow && \downarrow^{\mathrlap{R(h)}}
    \\
    && && R(d_2)
  }
$$


=--

+-- {: .num_example}
###### Example
**([[localization]] via [[universal arrows]])**

The characterization of adjoint functors in terms of universal factorizations through the unit and counit (Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor}) is of particular interest in the case that $R$ is a [[full and faithful functor]] 

$$
  R \;\colon\;
  \mathcal{D} \hookrightarrow \mathcal{C}
$$

exhibiting $\mathcal{D}$ as a [[reflective subcategory]] of $\mathcal{C}$. In this case we may think of $L$ as a [[localization]] and of objects in the [[essential image]] of $L$ as **local objects**. Then the above says that:

* every morphism $c \to R d$ from $c$ into a local object factors throught the localization of  $c$.

=--


### In terms of cographs/correspondences/heteromorphisms
 {#InTermsOfCographsHeteromorphisms}

Every [[profunctor]]

$$
  k : C^{op} \times D \to S
$$

defines a category $C *^k D$ with $Obj(C *^k D) = Obj(C) \sqcup Obj(D)$ and with [[hom set]] given by

$$
  Hom_{C^{op} \times D}(X,Y)
  = 
  \left\{
    \array{
      Hom_C(X,Y) & if X, Y \in C
      \\
      Hom_{D}(X,Y) & if X,Y \in D
      \\
      k(X,Y) & if X \in C and Y \in D
      \\
      \emptyset & otherwise
    }
  \right.
$$

($k(X,Y)$ is also called the _[[heteromorphisms]]_).

This category naturally comes with a functor to the [[interval]] category

$$
  C *^k D \to \Delta^1
  \,.
$$

Now, every functor $L : C \to D$ induces a [[profunctor]]

$$
  k_L(X,Y) = Hom_D(L(X), Y)
$$

and every functor $R : D \to C$ induces a [[profunctor]]

$$
  k_R(X,Y) = Hom_C(X, R(Y))
  \,.
$$

The functors $L$ and $R$ are adjoint precisely if the [[profunctors]] that they define in the above way are equivalent. This in turn is the case if
$C \star^L D \simeq (D^{op} \star^{R^{op}} C^{op})^{op}$.

We say that $C \star^k D$ is the [[cograph of a functor|cograph of the functor]] $k$. See there for more on this.


### In terms of graphs/2-sided discrete fibrations

Functors $L : C \to D$ and $R : D \to C$ are adjoint precisely if we have a commutative diagram

$$
    \array{
       (L \downarrow Id_D) &&\stackrel{\cong}{\to}&& (Id_C \downarrow R)
       \\
       & \searrow && \swarrow
       \\   
       && C \times D
    }
$$

where the downwards arrows are the maps induced by the projections of the comma categories. This definition of adjoint functors was introduced by [[Lawvere]] in his [[Functorial Semantics of Algebraic Theories|Ph.D. thesis]], and was the original motivation for [[comma categories]].

This diagram can be recovered directly from the image under the equivalence $[C^{op} \times D, Set] \stackrel{\simeq}{\to} DFib(D,C) $ described at [[2-sided fibration]] of the isomorphism of induced [[profunctors]] $C^{op} \times D \to Set$ (see above at "In terms of Hom isomorphism"). Its relation to the hom-set definition of adjoint functors can thus be understood within the general paradigm of [[Grothendieck construction]]-like correspondences.



### in terms of Kan extensions/liftings

Given $L \colon C \to D$, we have that it has a [[right adjoint]] $R\colon D \to C$ precisely if the [[left Kan extension]] $Lan_L 1_C$ of the [[identity]] along $L$ exists and is [absolute](/nlab/show/Kan+extension#AbsoluteKanExtension), in which case

$$
  R \simeq \mathop{Lan}_L 1_C
  \,.
$$ 

In this case, the universal 2-cell $1_C \to R L$ corresponds to the 
[[unit of an adjunction|unit of the adjunction]]; the counit and the verification of the triangular identities can all be obtained through properties of Kan extensions and absoluteness.

It is also possible to express this in terms of Kan liftings: $L$ has a right adjoint $R$ if and only if:

- $R \simeq \mathop{Rift}_L 1_D$ and this [[Kan lift]] is [[Kan lift|absolute]]

In this case, we get the counit as given by the universal cell $L R \to 1_D$, while the rest of the data and properties can be derived from it through the absolute Kan lifting assumption.

Dually, we have that for $R\colon D \to C$, it has a left adjoint $L \colon C \to D$ precisely if 

- $L \simeq \mathop{Ran}_R 1_D$, and this Kan extension is [[Kan extension|absolute]]

or, in terms of left Kan liftings:

- $L \simeq \mathop{Lift}_R 1_C$, and this Kan lifting is [[Kan lift|absolute]]

The formulations in terms of liftings generalize to [[relative adjoint|relative adjoints]] by allowing an arbitrary functor $J$ in place of the identity; see there for more.



## Properties
 {#Properties}


### Basic properties

+-- {: .num_prop #UniquenessOfAdjoints}
###### Proposition
**([[adjoint functors]] are unique up to [[natural isomorphism]])**

The [[left adjoint]] or [[right adjoint]] to a [[functor]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}), if it exists, is unique up to  [[natural isomorphism]].

=--

+-- {: .proof}
###### Proof

Suppose the functor $L \colon \mathcal{D} \to \mathcal{C}$ is given, and we are asking for uniqueness of its right adjoint, if it exists. The other case is directly analogous.

Suppose that $R_1, R_2 \;\colon\; \mathcal{C} \to \mathcal{D}$ are two [[functors]] which are [[right adjoint]] to $L$. Then for each $d \in \mathcal{D}$ the corresponding two hom-isomorphisms (eq:HomIsomorphismForAdjointFunctors) combine to say that there is a [[natural isomorphism]]

$$
  \Phi_d
  \;\colon\;
  Hom_{\mathcal{C}}(-,R_1(d))
  \;\simeq\;
  Hom_{\mathcal{C}}(-,R_2(d))
$$

As in the proof of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject}, the [[Yoneda lemma]] implies that 

$$
  \Phi_d \;=\; y( \phi_d )
$$

for some [[isomorphism]]

$$
  \phi_d \;\colon\;  R_1(d) \overset{\simeq}{\to} R_2(d)
  \,.
$$

But then the uniqueness statement of Prop. \ref{AdjointFunctorFromObjectwiseRepresentingObject} implies that the collection of these isomorphisms for each object constitues a [[natural isomorphism]] between the functors.

=--

+-- {: .num_prop #AdjointsPreserveCoLimits}
###### Proposition
**([[left adjoints preserve colimits and right adjoints preserve limits]])**

Let $(L \dashv R) \colon \mathcal{D} \to \mathcal{C}$ be a pair of [[adjoint functors]] (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Then

* $L$ [[preserved limit|preserves]] all [[colimits]] that exist in $\mathcal{C}$, 

* $R$ preserves all [[limits]] in $\mathcal{D}$.  

=--

+-- {: .proof}
###### Proof

Let $y : I \to \mathcal{D}$ be a [[diagram]] whose [[limit]] $\lim_{\leftarrow_i} y_i$ exists. Then we have a sequence of [[natural isomorphism]]s, natural in $x \in C$

$$
  \begin{aligned}
    Hom_{\mathcal{C}}(x, R {\lim_\leftarrow}_i y_i)
    &  \simeq
    Hom_{\mathcal{D}}(L x, {\lim_\leftarrow}_i y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{D}}(L x, y_i)
    \\
    & \simeq
    {\lim_\leftarrow}_i Hom_{\mathcal{C}}( x, R y_i)
    \\  
    & \simeq
    Hom_{\mathcal{C}}( x, {\lim_\leftarrow}_i R y_i)
    \,,
  \end{aligned}
$$

where we used the hom-isomorphism (eq:HomIsomorphismForAdjointFunctors) and the fact that any [[hom-functor]] preserves limits (see there). Because this is natural in $x$ the [[Yoneda lemma]] implies that we have an [[isomorphism]]

$$
  R {\lim_\leftarrow}_i y_i
  \simeq
  {\lim_\leftarrow}_i R y_i
  \,.
$$

The argument that shows the preservation of colimits by $L$ is analogous.

=--

+-- {: .num_remark #AdjointFunctorTheorem}
###### Remark

A partial converse to Prop. \ref{AdjointsPreserveCoLimits} is provided by the [[adjoint functor theorem]]. See also _[Pointwise Expression](#PointwiseExpression)_ below.

=--

+-- {: .num_prop #FullyFaithfulAndInvertibleAdjoints}
###### Proposition


Let $L \dashv R$ be a pair of adjoint functors (Def. \ref{AdjointFunctorsInTermsOfNaturalBijectionOfHomSets}). Then the following holds:

* $R$ is [[faithful functor|faithful]] precisely if the component of the [[unit of an adjunction|counit]] over every object $x$ is an [[epimorphism]] $L R x \stackrel{}{\to} x $;

* $R$ is [[full functor|full]] precisely if the component of the [[unit of an adjunction|counit]] over every object $x$ is a [[split monomorphism]] $L R x \stackrel{}{\to} x $;

* $L$ is [[faithful functor|faithful]] precisely if the component of the [[unit of an adjunction|unit]] over every object $x$ is a [[monomorphism]] $x \hookrightarrow R L x $;

* $L$ is [[full functor|full]] precisely if the component of the [[unit of an adjunction|unit]] over every object $x$ is a [[split epimorphism]] $x \to R L x $;

* $R$ is [[full and faithful functor|full and faithful]] 
  (exhibits a [[reflective subcategory]])
  precisely if
  the [[unit of an adjunction|counit]] is a [[natural isomorphism]] 
  $\epsilon : L \circ R \stackrel{\simeq}{\to} Id_D$

* $L$ is [[full and faithful functor|full and faithful]]
  (exhibits a [[coreflective subcategory]]) precisely if
  the [[unit of an adjunction|unit]] 
  is a natural isomorphism 
  $\eta : Id_C \stackrel{\simeq}{\to} R \circ L$.

* The following are equivalent:

  * $L$ and $R$ are both [[full and faithful functor|full and faithful]];

  * $L$ is an [[equivalence of categories|equivalence]];

  * $R$ is an [[equivalence of categories|equivalence]].

=--

|   |    |    |
|---|----|----|
| $\phantom{A}$**[[adjunction]]**$\phantom{A}$  |  |  $\phantom{A}$[[adjunction unit|unit]] is [[isomorphism|iso]]:$\phantom{A}$  | 
|  |  | $\phantom{A}$[[coreflective subcategory|coreflection]]$\phantom{A}$ | 
| $\phantom{A}$[[adjunction counit|counit]] is [[isomorphism|iso]]:$\phantom{A}$ | $\phantom{A}$[[reflective subcategory|reflection]]$\phantom{A}$ | $\phantom{A}$[[adjoint equivalence of categories|adjoint equivalence]]$\phantom{A}$  |  
{: style='margin:auto}


+-- {: .proof}
###### Proof

For the characterization of faithful $R$ by epi counit components, notice (as discussed at _[[epimorphism]]_ ) that $L R x \to x$ being an epimorphism is equivalent to the induced [[function]]

$$
  Hom(x, a) \to Hom(L R x, a)
$$

being an [[injection]] for all objects $a$. Then use that, by adjointness, we have an isomorphism

$$
  Hom(L R x , a ) \stackrel{\simeq}{\to} Hom(R x, R a)
$$ 

and that, by the formula for [[adjuncts]] and the [[zig-zag identity]], this is  such that the composite

$$
 R_{x,a} :  Hom(x,a) \to Hom(L R x, a) \stackrel{\simeq}{\to}
    Hom(R x, R a)
$$

is the component map of the functor $R$:

$$
  \begin{aligned}
    (x \stackrel{f}{\to} a) & \mapsto 
    (L R x \to x \stackrel{f}{\to} a)
    \\
    & \mapsto 
    (R L R x \to R x \stackrel{R f}{\to} R a)
    \\
    & \mapsto 
    (R x \to R L R x \to R x \stackrel{R f}{\to} R a)     
    \\
    & = (R x \stackrel{R f}{\to} R a)
  \end{aligned}
  \,.
$$

Therefore $R_{x,a}$ is injective for all $x,a$, hence $R$ is faithful, precisely if $L R x \to x$ is an epimorphism for all $x$. The characterization of $R$ full is just the same reasoning applied to the fact that $\epsilon_x \colon L R x \to x$ is a [[split monomorphism]] iff for all objects $a$ the induced function
\[
  Hom(x, a) \to Hom(L R x, a)
\]
is a surjection.

For the characterization of faithful $L$ by monic units notice that analogously (as discussed at [[monomorphism]]) $x \to R L x$ is a monomorphism if for all objects $a$ the function

$$
  Hom(a,x ) \to Hom(a, R L x)
$$

is an injection. Analogously to the previous argument we find that this is equivalent to 

$$
  L_{a,x} : Hom(a,x ) \to Hom(a, R L x) \stackrel{\simeq}{\to} Hom(L a, L x)
$$

being an injection. So $L$ is faithful precisely if all $x \to R L x$ are monos. For $L$ full, it's just the same applied to $x \to R L x$ [[split epimorphism]] iff the induced function
$$
  Hom(a,x ) \to Hom(a, R L x)
$$
is a surjection, for all objects $a$.

The proof of the other statements proceeds analogously.

=--

Parts of this statement can be strengthened:

+-- {: .num_prop #ReflectionRecognizedByIdempotency}
###### Proposition

Let $(L \dashv R) : D \to C$ be a pair of [[adjoint functors]] such that there is _any_ [[natural isomorphism]] 

$$
  L R \simeq Id
  \,,
$$

then also the [[unit of an adjunction|counit]] $\epsilon : L R \to Id$ is an [[isomorphism]].

=--

This appears as ([Johnstone, lemma 1.1.1](#Johnstone)).

+-- {: .proof}
###### Proof

Using the given [[isomorphism]], we may transfer the [[comonad]] structure on $L R$ to a comonad structure on $Id_D$. By the [[Eckmann-Hilton argument]] the [[endomorphism monoid]] of $Id_D$ is commutative. Therefore,  since the coproduct on the comonad $Id_D$ is a [[left inverse]] to the counit (by the co-[[unitality]] property applied to this degenerate situation), it is in fact a two-sided [[inverse]] and hence the $Id_D$-counit is an [[isomorphism]]. Transferring this back one finds that also the counit of the comand $L R$, hence of the adjunction $(L \dashv R)$ is an isomorphism.

=--

### Pointwise expression
 {#PointwiseExpression}



+-- {: .num_prop #PointwiseExpressionOfLeftAdjoints}
###### Proposition
**(pointwise expression of [[left adjoints]] in terms of [[limits]] over [[comma categories]])**

A [[functor]] $R \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}$  has a [[left adjoint]] $L \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}$ precisely if 

1. $R$ [[preserved limit|preserves]] all [[limits]] that exist in $\mathcal{C}$; 

1. for each [[object]] $d \in \mathcal{D}$, the [[limit]] of the canonical functor out of the [[comma category]] of $R$ under $d$

   $$
     d/R \longrightarrow \mathcal{C}
   $$

   exists.

In this case the value of the [[left adjoint]] $L$ on $d$ is given by that limit:

\[
  \label{FormulaForLeftAdjointByPointwiseLimit}
  L(d)
  \;\simeq\;
  \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} c
\]

=--


(e.g. [[Categories Work|MacLane, chapter X, theorem 2]])


+-- {: .proof}
###### Proof

First assume that the left adjoint exist. Then 

1. $R$ is a [[right adjoint]] and hence preserves limits since all [[right adjoints preserve limits]];

1. by Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} the [[adjunction unit]] provides a [[universal morphism]] $\eta_d$ into $L(d)$, and hence, by Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}, exhibits $(L(d), \eta_d)$ as the [[initial object]] of  the [[comma category]] $d/R$. The limit over any category with an initial object exists, as it is given by that initial object.

Conversely, assume that the two conditions are satisfied and let $L(d)$ be given by (eq:FormulaForLeftAdjointByPointwiseLimit). We need to show that this yields a left adjoint.

By the assumption that $R$ preserves all limits that exist, we have

\[
  \label{RAppliedtoFormulaForLeftAdjointByPointwiseLimit}
  \array{
    R(L(d))
    & =
    R\left(
    \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} c
  \right)
   \\
   & \simeq
    \underset{\underset{ \left( c,  \array{ d \\ \downarrow^{\mathrlap{f}} \\ R(c) } \right)  \in d/R }{\longleftarrow}}{\lim} R(c)
  }
\]

Since the $d \overset{f}{\to} R(d)$ constitute a [[cone]] over the [[diagram]] of the $R(d)$, there is universal morphism

$$
  d \overset{\phantom{AA} \eta_d \phantom{AA}}{\longrightarrow} R(L(d))
  \,.
$$

By Prop. \ref{CollectionOfUniversalArrowsEquivalentToAdjointFunctor} it is now sufficient to show that $\eta_d$ is a [[universal morphism]] into $L(d)$, hence that for all $c \in \mathcal{C}$ and $d \overset{g}{\longrightarrow} R(c)$ there is a unique morphism $L(d) \overset{\widetilde f}{\longrightarrow} c$ such that

$$
  \array{
    && d
    \\
    & {}^{\mathllap{ \eta_d }}\swarrow && \searrow^{\mathrlap{f}}
    \\
    R(L(d)) && \underset{\phantom{AA}R(\widetilde f)\phantom{AA}}{\longrightarrow} && R(c)
    \\
    L(d) 
      &&\underset{\phantom{AA}\widetilde f\phantom{AA}}{\longrightarrow}&&
    c
  }
$$

By Prop. \ref{UniversalMorphismsAreInitialObjectsInCommaCategory}, this is equivalent to $(L(d), \eta_d)$ being the [[initial object]] in the [[comma category]] $c/R$, which in turn is equivalent to it being the [[limit]] of the [[identity functor]] on $c/R$ ([this prop.](initial+object#LimitOverIdentityFunctorIsInitialObject)). But this follows directly from the limit formulas (eq:FormulaForLeftAdjointByPointwiseLimit) and (eq:RAppliedtoFormulaForLeftAdjointByPointwiseLimit).

=--

See at _[[adjoint functor theorem]]_ for more.


### Relation to monads
 {#RelationToMonads}

Every [[adjunction]] $(L \dashv R)$ induces a [[monad]] $R \circ L$ and a [[comonad]] $L \circ R$. There is in general more than one adjunction which gives rise to a given monad this way, in fact there is a [[category]] of adjunctions for a given monad. The [[initial object]] in that category is the adjunction over the [[Kleisli category]] of the monad and the [[terminal object]] is that over the [[Eilenberg-Moore category]] of algebras. (e.g. [Borceux, vol 2. prop. 4.2.2](#Borceux)) The latter is called the _[[monadic adjunction]]_.

Moreover, passing from [[adjunctions]] to monads and back to their [[monadic adjunctions]] constitutes itself an [[adjunction]] between adjunctions and monads, called the _[[semantics-structure adjunction]]_.


## Examples 
 {#Examples}


The central point about examples of adjoint functors is:

_Adjoint functors are ubiquitous_ . 

To a fair extent, [[category theory]] is all about adjoint functors and the other [[universal construction]]s: [[Kan extension]]s, [[limit]]s, [[representable functor]]s, which are all special cases of adjoint functors -- and adjoint functors are special cases of these.

Listing examples of adjoint functors is much like listing examples of [[integral]]s in [[analysis]]: one can and does fill books with these. (In fact, that analogy has more to it than meets the casual eye: see [[coend]] for more).


Keeping that in mind, we do list some special cases and special classes of examples that are useful to know. But any list is necessarily wildly incomplete.


### General

* A pair of adjoint functors between [[posets]] is a _[[Galois correspondence]]_.

* A pair of adjoint functors $(L \dashv R)$ where $R$ is a [[full and faithful functor]] exhibits a [[reflective subcategory]]. 

  In this case $L$ may be regarded as a [[localization]]. The fact that the adjunction provides universal factorization through unit and counit in this case means that every morphism $f : c \to R d$ into a local object factors through the localization of $c$.

* A pair of adjoint functors that is also an [[equivalence of categories]] is called an [[adjoint equivalence]].

* A pair of adjoint functors where $C$ and $D$ have finite [[limit]]s and $L$ preserves these finite limits is a [[geometric morphism]]. These are one kind of morphisms between [[topos]]es. If in addition $R$ is full and faithful, then this is a [[geometric embedding]].

* The left and right adjoint functors $p_!$ and $p_*$ (if they exist) to a functor $p^* : [K',C] \to [K,C]$ between [[functor categories]] obtained by precomposition with a functor $p : K \to K'$ of [[diagram]] categories are called the left and right [[Kan extension]] functors along $p$

  $$
    (Lan_p \dashv p^* \dashv Ran_p)
    :=
    (p_! \dashv p^* \dashv p_*) : 
    [K,C]
     \stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^*}{\leftarrow}}{\underset{p_*}{\to}}}
    [K',C]
    \,.
  $$

  If $K' = {*}$ is the [[terminal category]] then this are the [[limit]] and [[colimit]] functors on $[K,C]$.

  If $C = $ [[Set]] then this is the [[direct image]] and [[inverse image]] operation on [[presheaves]].


* if $R$ is regarded as a [[forgetful functor]] then its left adjoint $L$ is a regarded as a [[free functor]].


* If $C$ is a category with small [[colimit]]s and $K$ is a [[small category]] (a [[diagram]] category)  and $Q : K \to C$ is any functor, then this induces a [[nerve and realization]] pair of adjoint functors

  $$
    (|-|_Q \dashv N_Q) : C \stackrel{\overset{|-|_Q}{\leftarrow}}{\underset{N_Q}{\to}}
    [K^{op}, Set]
  $$

  between $C$ and the [[category of presheaves]] on $K$, where

  * the [[nerve]] functor is given by

    $$
      N_Q(c) := Hom_C(Q(-),c) : k \mapsto Hom_C(Q(k),c)
    $$

  * and the realization functor is given by the [[coend]]

    $$
      |F|_Q := \int^{k \in K} Q(k)\cdot F(k)

      \,,
    $$

    where in the integrand we have the canonical [[copower|tensoring]] of
    $C$ over [[Set]] ($Q(k) \cdot F(k) = \coprod_{s \in F(k)} Q(k)$).

  A famous examples of this is obtained for $C = $ [[Top]], $K = \Delta$
  the [[simplex category]] and $Q : \Delta \to Top$ the functor that sends
  $[n]$ to the standard topological $n$-[[simplex]]. In this case
  the nerve functor is the 
  [[fundamental infinity-groupoid|singular simplicial complex]] functor
  and the realization is ordinary [[geometric realization]].


## Related concepts

* **adjoint functor**, [[adjunction]]

  * [[strong adjoint functor]]

  * [[adjoint triple]], [[adjoint quadruple]], [[recollement]]

  * [[dual adjunction]]

  * [[ambidextrous adjunction]]

  * [[adjoint monad]]

  * [[fixed point of an adjunction]]

  * [[enriched adjunction]]

* [[proadjoint]], [[Hopf adjunction]]

* [[2-adjunction]]
  
  [[biadjunction]], [[lax 2-adjunction]], [[pseudoadjunction]]

* [[adjoint (∞,1)-functor]]

* [[(∞,n)-category with adjoints]]

* [[multi-adjoint]], [[weak adjoint]], [[solution set condition]]


## References
 {#References}

For the basics, see any text on [[category theory]] (and see the references at _[[adjunction]]_), for instance:

* {#Borceux94} [[Francis Borceux]], Vol 1, Section 3 of _[[Handbook of Categorical Algebra]]_

* {#Johnstone} [[Peter Johnstone]], first pages of _[[Elephant|Sketches of an Elephant]]_
 
* _[[geometry of physics -- categories and toposes]] -- [Adjunctions](https://ncatlab.org/nlab/show/geometry+of+physics+--+categories+and+toposes#Adjunctions)_

Though the definition of an [[adjoint equivalence]] appears in [[Grothendieck|Grothendieck's]] [[Tohoku]] paper, the idea of adjoint functors in general goes back to 

* [[Daniel Kan]], _Adjoint functors_, Transactions of the American Mathematical Society Vol. 87, No. 2 (Mar., 1958), pp. 294-329 ([jstor](http://www.jstor.org/stable/1993102))

and its fundamental relevance for [[category theory]] was realized due to 

* {#Freyd64} [[Peter Freyd]], _Abelian categories -- An introduction to the theory of functors_, Harper's  Series  in  Modern  Mathematics, Harper  &  Row,   New  York, 1964 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/freydab.pdf)).

* {#Lawvere69} [[William Lawvere]], _Adjointness in Foundations_, ([TAC](http://www.emis.de/journals/TAC/reprints/articles/16/tr16abs.html)), Dialectica 23 (1969), 281-296

The history of the idea that adjoint functors formalize aspects of [[dialectics]] is recounted in 

* {#Lambek82} [[Joachim Lambek]], _The Influence of Heraclitus on Modern Mathematics_, In _Scientific Philosophy Today: Essays in Honor of Mario Bunge_, edited by Joseph Agassi and Robert S Cohen, 111&#8211;21. Boston: D. Reidel Publishing Co. (1982) ([doi:10.1007/978-94-009-8462-2_6](https://doi.org/10.1007/978-94-009-8462-2_6))

  (more along these lines at _[[adjoint modality]]_)


See also 

* Wikipedia, [Adjoint Functors](http://en.wikipedia.org/wiki/Adjoint_functors)

* [[The Catsters]] ([list](http://www.youtube.com/view_play_list?p=54B49729E5102248))

-  

[[!redirects adjoint functors]]

[[!redirects adjoint pair of functors]]
[[!redirects adjoint pairs of functors]]

[[!redirects universal arrow]]
[[!redirects universal arrows]]

[[!redirects universal morphism]]
[[!redirects universal morphisms]]


