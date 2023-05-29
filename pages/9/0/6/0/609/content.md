
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The notion of *simplicial groupoids* pairs the concepts of *[[groupoids]]* and *[[simplicial sets]]*. Via the [[Dwyer-Kan loop groupoid]] functor &lbrack;[Dwyer & Kan (1984)](#DwyerKan84)&rbrack; their [[homotopy]] theory is equivalent to the [[classical model structure on simplicial sets|classical]] homotopy theory of [[simplicial sets]]/[[Kan complexes]] (both being models for [[infinity-groupoids|$\infty$-groupoids]]).


## Definition
 {#Definition}

A priori, the term *simplicial groupoid* may refer to [[simplicial objects]] in the ([[1-category|1-]])[[category]] [[Grpd]] of ([[small category|small]]) [[strict category|strict]] [[groupoids]].

However (cf. discussion at *[[simplicial category]]*), in applications (notably in [[homotopy theory]]) one is interested only in those simplicial objects in [[Grpd]] whose [[underlying]] simplicial [[sets]] of [[objects]] are *simplicially constant*. This more restrictive notion --- equivalent to *[[sSet]]-[[enriched groupoids]]* --- is traditionally still referred to as "simplicial groupoids" &lbrack;e.g. [Dwyer & Kan (1984),  §1.2.(ii)](#DwyerKan84), [Goerss & Jardine (2009), V.7](GoerssJardine09)&rbrack;; but for the moment let us call these instead "simplicial DK-groupoids", for clarity, and let us denote the [[full subcategory]] they form by

$$
  sSet\text{-}Grpd
  \;\simeq\;
  sGrpd_{DK} 
    \overset{\phantom{---}}{\hookrightarrow} 
  Func(\Delta^{op}, Grpd)
  \,.
$$

So given such a simplicial DK-groupoid $\mathcal{C}_\bullet \,\in\, sGrpd_{DK}$ we have:

1. a plain [[set]] of [[objects]] $Obj(\mathcal{C}_\bullet) \,\in\, Sets$;

1. for every [[pair]] $x, y \,\in\, Obj(\mathcal{C}_\bullet)$ of [[objects]] the degree-wise [[hom-sets]] form a [[simplicial set]] 

   $$
     \mathcal{C}_\bullet(x,y)
     \;\coloneqq\;
     Hom_{\mathcal{C}_\bullet}(x,y)
     \;\in\;
     sSet
     \,;
   $$

1. where the degreewise [[composition]] operations constitutes an [[sSet]]-[[enriched category|enriched]] composition operation

   $$
     \mathcal{C}_\bullet(x,y)
     \,\times\,
     \mathcal{C}_\bullet(y,z)
     \overset{\circ}{\longrightarrow}
     \mathcal{C}_\bullet(x,z)
   $$

1. making $\mathcal{C}_\bullet$ an [[sSet-enriched category]].

Conversely, simplical DK-groupoids are therefore in [[bijection]] to those [[sSet-enriched categories]] whose degreewise [[categories]] formed by the $n$-cell [[morphisms]] for any $n \,\in\, \mathbb{N}$ are [[groupoids]].

This makes the category $sGrpd_{DK}$ be a [[full subcategory]] of the category of ([[small category|small]]) [[sSet-enriched categories]]:

$$
  sGrpd_{DK} 
    \overset{\phantom{---}}{\hookrightarrow} 
  sSet Cat
  \,.
$$


## Remarks
 
*  Simplicially enriched groupoids are related to [[simplicial set|simplicial sets]] via an [[adjoint functor|adjunction]] found independently by Dwyer & Kan and Joyal & Tierney; see *[[Dwyer-Kan loop groupoid]]*.  This adjunction gives an [[equivalence of categories|equivalence]] of [[homotopy category|homotopy categories]] so that simplicially enriched groupoids model all [[homotopy type|homotopy types]].

   *  This is a groupoidal version of the equivalence between [[quasi-category|quasi-categories]] and [[simplicially enriched category|simplicially enriched categories]] via the [[homotopy coherent nerve]].

*  A simplicially enriched groupoid having exactly one object is essentially the same as a [[simplicial group]]. Notationally however it is often important to distinguish a simplicial group form the corresponding single object simplicially enriched groupoid.

*  Many constructions on simplicial groups, such as that of its [[Moore complex]] carry over to simplicialy enriched groupoids without difficulty.

## Properties

### Relation to simplicial groups
 {#RelationToSimplicialGroups}

\begin{example}\label{SimplicialDeloopingGroupoids}
**([[simplicial groupoid|simplicial]] [[delooping groupoid]])**
\linebreak
For $\mathcal{G} \,\in\, Grp(sSet)$ a [[simplicial group]], we obtain its simplicial [[delooping groupoid]] $\mathbf{B}\mathcal{G}$ by setting

* $Obj(\mathbf{B}\mathcal{G}) \,\coloneqq\, \ast$ (the [[singleton set]]),

* $(\mathbf{B}\mathcal{G})(\ast,\ast) \,\coloneqq\, \mathcal{G}$

* with [[composition]] given by the group operation of $\mathcal{G}$.

Conversely, for $\mathcal{X} \,\in\, sSet\text{-}Grpd$ and $x \,\in\, Obj(\mathcal{X})$, the [[endomorphism]]-[[hom-object]] at $x$ canonically carries the [[structure]] of a [[simplicial group]]:
$$
  \mathcal{X}(x,x) \,\in\, Grp(sSet)
  \,.
$$
\end{example}

\begin{definition}
**(some notation)**
\linebreak
For $\mathcal{X} \,\in\, sSet\text{-}Grpd$ a DK-simplicial groupoid, write:

* $\mathcal{X}_0 \,\in\, Grpd$ for its [[underlying]] plain (i.e. [[Set]]-enriched) [[groupoid]] (its [[change of enrichment]] along the [[terminal category|terminal]] functor $sSet \to \ast$)

* $\pi_0(\mathcal{X}) \,\coloneqq\, \pi_0(\mathcal{X}_0) \,\in\, Set$ for the set of [[isomorphism classes]] of [[objects]], hence for the set of *[[connected components]]* of $\mathcal{X}$,

* $\mathcal{X}_{[x]} \hookrightarrow \mathcal{X}$ for the enriched [[full subcategory]] on all objects in the connected component $[x] \,\in\, \pi_0(\mathcal{X})$.

\end{definition}

\begin{proposition}
**(simplicial groupoids adjoint equivalent to skeletons)**
\linebreak
  Assuming the [[axiom of choice]], every [[sSet]]-[[enriched groupoid]] is [[sSet]]-[[enriched adjoint equivalence|enriched adjoint equivalent]] to a [[skeletal groupoid|skeletal]] simplicial groupoid, namely to a [[disjoint union]] of simplicial delooping groupoids (Exp. \ref{SimplicialDeloopingGroupoids}), one for each [[connected components]], in that given a choice of representative [[objects]] $(i, x_i) \,\in\, \big(i \in \pi_0(\mathcal{X})\big) \times Obj(\mathcal{X}_i)$ of all the [[connected components]], the [[full subcategory|inclusion]] [[enriched functor]]
\[
  \label{FullInclusionOfConnectedComponents}
  \iota
  \,\colon\,
  \left(
  \underset{i \in \pi_0(\mathcal{X})}{\amalg}
  \mathbf{B}\big(\mathcal{X}(x_i,\,x_i)\big)
  \right)
  \xhookrightarrow{\phantom{---}}
  \mathcal{X}
\]
has a strict [[left inverse]] and a [[right inverse]] up to [[enriched natural transformation|enriched natural]] [[isomorphism]].
\end{proposition}
\begin{proof}
  This follows in direct [[enriched category theory|enriched]]-analogy to the corresponding statement for plain [[groupoids]] (as for instance spelled out [here](Introduction+to+Topology+--+2#EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings)) using (only) that the [[cosmos]] [[sSet]] is [[cartesian monoidal category|cartesian monoidal]]:

Choosing for each $x \in Obj(\mathcal{X})$ an element 

$$
  \gamma_x 
  \,\colon\, 
  \ast \to \mathcal{X}(x_{[x]}, x)
$$ 

induces

1. an [[enriched functor]]

   \[
     \label{ContractionOntoConnectedComponents}
     \array{
       \mathcal{X} 
         &\xrightarrow{
          \phantom{----}
          p
          \phantom{----}
         }& 
       \underset{i \in \pi_0(\mathcal{X})}{\amalg}
       \mathbf{B}\big( \mathcal{X}(x_i,\,x_i) \big)
       \\
       x &\mapsto& x_{[x]}
       \\
       \mathcal{X}(x,y) 
         &\xrightarrow{
            \phantom{----}
            p_{x,y}
            \phantom{----}
         }&
       \mathcal{X}(x_{[x]}, x_{[y]})
       \\
       \mathllap{\simeq}\Big\downarrow
       &&
       \Big\uparrow\mathrlap{\circ}
       \\
       \ast \times \mathcal{X}(x,y) \times \ast
       &
       \underset{
         \big((-)^{-1}\circ \gamma_y\big)
         \times
         id
         \times
         \gamma_x
       }{\longrightarrow}
       &
         \mathcal{X}(y,x_{[y]})
         \times
         \mathcal{X}(x,y)
         \times
         \mathcal{X}(x_{[x]},x)
     }
   \]

1. an [[enriched natural transformation]]

   \[
     \label{ContractingHomotopy}
     \gamma 
       \,\colon\, 
     \iota \circ p 
       \longrightarrow 
     id_{\mathcal{X}}
   \]

   with components $\gamma_x$ (which satisfies its "enriched [[naturality square]]-condition" [here](enriched+natural+transformation#eq:ExtranaturalitySquare) essentially by construction of $p$).

Similarly there is an enriched transformation $id_{\mathcal{X}} \longrightarrow  p \circ \iota$, and these make the [[adjunction unit|unit]] and [[adjunction counit|counit]] of an "enriched [[adjoint equivalence]]".
But if we choose $\gamma_{x_{[x]}} \coloneqq id_{x_{[x]}}$ --- as we may --- then there is already an [[equality]] $p \circ \iota = id$.
\end{proof}

Some consequences:

\begin{remark}
\label{sSetPresheavesOnSimplicialGroupoidsAreProductsOfsSetGroupActions}
**([[simplicial presheaves]] on [[simplicial groupoids]] are [[equivalence of categories|equivalently]] [[products]] of [[simplicial group actions]])**
\linebreak
  For 

  * $\mathcal{X}$ a DK-enriched groupoid regarded as an [[sSet-enriched category]]

  * $\mathbf{C}$ any [[sSet-enriched category]]

the [[enriched functor category]] between the two is [[equivalence of categories|equivalent]] (as a plain [[locally small category]]) to a [[product category|product]] of [[enriched functor categories]] on simplicial delooping groupoids (Exp. \ref{SimplicialDeloopingGroupoids}), one for each connected component of $\mathcal{X}$, 
$$
  sFunc(\mathcal{X},\,\mathbf{C})
  \;\simeq\;
  \underset{
   i \in \pi_0(\mathcal{X})
  }{\prod}
  sFunc\big(
    \mathbf{B}\mathcal{X}(x_i,x_i)
    ,\,
    \mathbf{C}
  \big)
  \,.
$$

This follows by observing that the functor of precomposion with the inclusion (eq:FullInclusionOfConnectedComponents)
$$
  \iota^\ast
  \;\colon\;
  sFunc(\mathcal{X},\,\mathbf{C})
  \longrightarrow
  \underset{
   i \in \pi_0(\mathcal{X})
  }{\prod}
  sFunc\big(
    \mathbf{B}\mathcal{X}(x_i,x_i)
    ,\,
    \mathbf{C}
  \big)  
$$
is inverse to $p^\ast$ (eq:ContractionOntoConnectedComponents)
up to a [[natural isomorphism]] whose component at any [[enriched functor]] $F \colon \mathcal{X} \longrightarrow \mathbf{C}$ is the [[enriched natural transformation]] $p^\ast \iota^\ast F\longrightarrow F$ obtained as the [[horizontal composition]] ("[[whiskering]]" of enriched transformations, see [there](enriched+natural+transformation#RightWhiskering)) by $F$ of the enriched transformation (eq:ContractingHomotopy). Notice that this is already an [[adjoint equivalence]].

If $\mathbf{C}$ is moreover [[tensoring|tensored]] over [[sSet]], then this, in turn, is [[equivalence of categories|equivalent]] to a product of categories of [[simplicial group|simplicial]]$\;$[[group actions]] on objects in $\mathbf{C}$:
$$
  sFunc(\mathcal{X},\,\mathbf{C})
  \;\simeq\;
  \underset{
   i \in \pi_0(\mathcal{X})
  }{\prod}
  \Big(
  \big(\mathcal{X}(x_i,x_i)\big)
  Act(\mathbf{C})
  \Big)
  \,.
$$
\end{remark}

\begin{example}
\label{BorelModelStructureOnSimplicialGroupActions}
**([[Borel model structure]] on [[simplicial group actions]] over simplicial groupoids)**
\linebreak
For $\mathcal{G} \,\in\, Grp(sSet)$ a [[simplicial group]] with [[sSet]]-[[enriched groupoid|enriched]] [[delooping groupoid]] denoted $\mathbf{B}\mathcal{G} \in sSet\text{-}Grpd$, an [[sSet]]-[[enriched functor]] $\mathbf{B}\mathcal{G} \longrightarrow sSet$ is equivalently a [[simplicial group action]] of $\mathcal{G}$.

Under this identification, the projective model structure on [[simplicial functors]] ([this Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors)) is equivalently the *[[Borel model structure]]* on [[simplicial group actions]], a context of Borel-[[equivariant homotopy theory]]:

$$
  sFunc\big(
    \mathbf{B}\mathcal{G}
    ,\,
    sSet
  \big)_{proj}
  \;\;
  =
  \;\;
  \mathcal{G}Act(sSet)_{Borel}
  \,.
$$

More generally, for $\mathcal{X} \in sSet\text{-}Grpd$ an [[sSet]]-[[enriched groupoid]] (Dwyer-Kan [[simplicial groupoid]]) with a single [[connected component]] $\pi_0(\mathcal{X}) \simeq \{[x]\}$, so that the inclusion
$$
  \iota 
    \,\colon\, 
  \mathbf{B}(\mathcal{X}(x,x))
  \xhookrightarrow{\phantom{---}}
  \mathcal{X}
$$
is an [[sSet]]-[[enriched adjoint equivalence]] (see discussion [there](simplicial+groupoid#RelationToSimplicialGroups)) the projective model structure on [[simplicial functors]] (from [that Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors)) is [[transferred model structure|transferred]] under the induced [[adjoint equivalence]] of [[sSet]]-[[enriched functor categories]]
$$
  sFunc\big(
    \mathcal{X}
    ,\,
    sSet
  \big)_{proj}
  \underoverset
    {\underset{\iota^\ast}{\longrightarrow}}
    {\overset{\iota_!}{\longleftarrow}}
    {\;\; \bot_{\simeq} \;\;}
  sFunc\Big(
    \mathbf{B}\big(\mathcal{X}(x,x)\big)
    ,\,
    sSet
  \Big)_{proj}
  \;=\;
  \big(\mathcal{X}(x,x)\big) Act(sSet)_{Borel}
$$
By [this example](transferred+model+structure#RightTransferAlongAdjointEquivalence) it follows that morphisms in all three classes $(\mathrm{W}, Fib, Cof)$ in $sFunc(\mathcal{X}, \, sSet)_{proj}$ are those which restrict on $x \in Obj(\mathcal{X})$ to the respective class in $\big(\mathcal{X}(x,x)\big) Act(sSet)_{Borel}$.

It follows that for $\mathcal{X} \,\in\, sSet\text{-}Grpd$ a [[simplicial groupoid]] with any set $\pi_0(\mathcal{X})$ of [[connected components]], the projective model structure of simplicial functors over it is the [product model structure](model+category#ProductModelStructure) of the [[Borel model structures]] of [[simplicial group actions]], one for each connected component:
$$
  sFunc\big(
    \mathcal{X}
    ,\,
    sSet
  \big)_{proj}
  \underoverset
    {\underset{\iota^\ast}{\longrightarrow}}
    {\overset{\iota_!}{\longleftarrow}}
    {\;\; \bot_{\simeq} \;\;}
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  sFunc\Big(
    \mathbf{B}\big(\mathcal{X}(x_i,x_i)\big)
    ,\,
    sSet
  \Big)_{proj}
  \;=\;
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  \big(\mathcal{X}(x_i,x_i)\big) Act(sSet)_{Borel}
  \,.
$$

The analogous statement holds (still by [that Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors)) for the [[codomain]] [[sSet]] replaced by any [[combinatorial simplicial model category]] $\mathbf{C}$:
$$
  sFunc\big(
    \mathcal{X}
    ,\,
    \mathbf{C}
  \big)_{proj}
  \underoverset
    {\underset{\iota^\ast}{\longrightarrow}}
    {\overset{\iota_!}{\longleftarrow}}
    {\;\; \bot_{\simeq} \;\;}
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  sFunc\Big(
    \mathbf{B}\big(\mathcal{X}(x_i,x_i)\big)
    ,\,
    \mathbf{C}
  \Big)_{proj}
  \;=\;
  \underset{i \in \pi_0(\mathcal{X})}{\prod}
  \big(\mathcal{X}(x_i,x_i)\big) Act(\mathbf{C})_{Borel}
  \,.
$$

Moreover, if $I_{\mathbf{C}}, J_{\mathbf{C}} \,\subset\, \mathbf{C}$ denote [[classes]] of (acyclic) [[generating cofibrations]] of $\mathbf{C}$, then [that Prop.](model+structure+on+functors#ExistenceOfProjectiveStructureOnEnrichedFunctors) gives [[generating cofibrations]] of $\mathcal{G}Act(\mathbf{C})_{Borel}$ to be
$$
  I^{\mathcal{G}}_{\mathbf{C}} \,\coloneqq\,
  \big\{
    \mathcal{G} \cdot i
    \;\vert\;
    i \in I_{\mathbf{C}}
  \big\}
  \,,\;\;\;\;
  J^{\mathcal{G}}_{\mathbf{C}} \,\coloneqq\,
  \big\{
    \mathcal{G} \cdot j
    \;\vert\;
    i \in J_{\mathbf{C}}
  \big\}
  \,.
$$
\end{example}




### Cartesian closed structure
 {#CartesianClosedStructure}

We discuss how the [[category]] of Dwyer-Kan simplicial groupoids ([[sSet]]-[[enriched groupoids]]) is a [[cartesian closed category]] (with [[internal hom]] given in Def. \ref{SimplicialMappingGroupoid} below). Since this is a property inherited from [[sSet-enriched categories]], we denote the category of simplicial groupoids now by $sSet\text{-}Grpd$.

\begin{definition}\label{SimplicialIntervalCategory}
  For $n \in \mathbb{N}$ write $\mathcal{I}^{(n+1)} \,\in\, sSet\text{-}Cat$ for the [[sSet-enriched category]] with

* precisely two [[objects]] $Obj(I^{(n+1)}) \,\coloneqq\, \{0,1\}$

* with trivial [[endomorphism]] [[hom-objects]] 

  $\mathcal{I}^{(n+1)}(0,0) \,\coloneqq\, \ast$

  $\mathcal{I}^{(n+1)}(1,1) \,\coloneqq\, \ast$

* [[empty set|empty]]$\;$[[hom-object]] from $1$ to $0$

  $\mathcal{I}^{(n+1)}(1,0) \,\coloneqq\, \varnothing$

* [[hom-object]] from $0$ to $1$ being the simplicial [[n-simplex]] $\Delta[n] \,\coloneqq\, \Delta(-,[n]) \colon \Delta^{op} \to sSet$:

  $\mathcal{I}^{(n+1)}(0,1) \,\coloneqq\, \Delta[n]$.  

With this minimalistic collection of morphisms, there are no nontrivial [[composition]]-operations to be specified.

Finally we declare that $\mathcal{I}^{(0)} \,\in\, sSet\text{Cat}$ is the [[terminal category|terminal]] simplicial category, i.e. that with a single object $\ast$ and $\mathcal{I}^{(0)}(\ast, \ast) \,\coloneqq\, \ast$.
\end{definition}

\begin{remark}\label{CoRepresentingNMorphismsOfSimplicialGroupoids}
  For $\mathcal{X} \,\in\, sSet\text{Grpd} \hookrightarrow sSet\text{Cat}$, morphisms from the simplicial category of Def. \ref{SimplicialIntervalCategory}
$$
  \mathcal{I}^{(n+1)} \longrightarrow \mathcal{X}
$$
are in [[natural bijection]] with [[n-morphism|$(n+1)$-morphisms]] of $\mathcal{X}$, hence the [[1-morphisms]] in $\mathcal{X}_n$:
$$
  Hom_{sSet\text{Cat}}( \mathcal{I}^{(n+1)},\, \mathcal{X} )
  \;\simeq\;
  Mor\big(\mathcal{X}_{n}\big)
  \,.
$$
Similarly:
$$
  Hom_{sSet\text{Cat}}( \mathcal{I}^{(0)},\, \mathcal{X} )
  \;\simeq\;
  Obj(\mathcal{X})
  \,.
$$
\end{remark}

\begin{definition}
  \label{CartesianProductOfsSetCategories}
  For $\mathcal{C},\mathcal{C}' \,\in\, sSet\text{-}Cat$ a [[pair]] of [[sSet-enriched categories]], their [[Cartesian product]] is the $sSet$-category
$$
  \mathcal{C} \times \mathcal{C}' 
  \,\in\,
  sSet\text{-}Cat
$$ 
with

* $
    Obj\big( \mathcal{C} \times \mathcal{C}' \big)
    \,\coloneqq\,
    Obj(\mathcal{C}) \times Obj(\mathcal{C}')  
  $

* $(\mathcal{C} \times \mathcal{C}')\big((X, X'), \, (Y,Y')\big) \,\coloneqq\, \mathcal{C}(X,\,Y) \times \mathcal{C}(X',\,Y')$

* [[composition]] inherited component-wise from that of $\mathcal{C}$ and $\mathcal{C}$'.

In other words, $\mathcal{C} \times \mathcal{C}'$ is in each degree a [[product category]]:

$$
  (\mathcal{C} \times \mathcal{C}')_n
  \;\coloneqq\;
  \mathcal{C}_n \times \mathcal{C}'_n
  \,.
$$

\end{definition}

\begin{definition}\label{SimplicialMappingGroupoid}
**(simplicial mapping groupoid)**
\linebreak
  For $\mathcal{X},\mathcal{Y} \,\in\, sSet\text{-}Grpd$ define their [[mapping object]]
  $$
    Maps(\mathcal{X},\,\mathcal{Y})
    \;\;\in\;\;
    sSet\text{-}Grpd
  $$

to be the simplicial groupoid whose $n$-morphisms are the homomorphism of [[sSet-enriched categories]] to $\mathcal{Y}$ from the cartesian product (Def. \ref{CartesianProductOfsSetCategories}) of $\mathcal{X}$ with $\mathcal{I}^{n}$ (Def. \ref{SimplicialIntervalCategory}):

* $Obj\big(Maps(\mathcal{X},\,\mathcal{Y})\Big) \,\coloneqq\, Hom_{sSet\text{-}Grpd}(\mathcal{X},\,\mathcal{Y})$,

* $Mor\big(Maps(\mathcal{X},\,\mathcal{Y})\Big)_n \,\coloneqq\, Hom_{sSet\text{-}Grpd}\big(\mathcal{X} \times \mathcal{I}^{(n+1)},\,\mathcal{Y}\big)$

* with [[face and degeneracy maps]] induced from $\Delta[\bullet] \,=\, Hom\big( \mathcal{I}^{(\bullet + 1)} \big)$,

* with [[composition]] induced from composition in $\mathcal{Y}$.

\end{definition}

\begin{proposition}
  The simplicial mapping groupoid construction of Def. \ref{SimplicialMappingGroupoid} makes $sSet\text{-}Grpd$ a [[cartesian closed category]] in that there are [[natural isomorphisms]]
\[
  \label{MappingObjectHomIsomorphism}
  Hom_{sSet\text{-}Grpd}
  \big(
    \mathcal{X} \times \mathcal{Y}
    ,\,
    \mathcal{Z}
  \big)
  \;\;\simeq\;\;
  Hom_{sSet\text{-}Grpd}
  \big(
    \mathcal{X}
    ,\,
    Maps(\mathcal{Y},\,\mathcal{Z})
  \big)
  \,.
\]
\end{proposition}
\begin{proof}
This is a standard argument. The point of Def. \ref{SimplicialMappingGroupoid}, in view of Rem. \ref{CoRepresentingNMorphismsOfSimplicialGroupoids}, is that we have [[natural bijections]] of [[hom-sets]]
$$
  Hom\big(
    \mathcal{I}^{(n)}
    ,\,
    Maps(\mathcal{Y},\,\mathcal{Z})
  \big)
  \;\simeq\;
  Hom\big(
    \mathcal{Y} \times \mathcal{I}^{(n)}
    ,\,
    \mathcal{Z}
  \big)
  \,.
$$
Since the [[hom-functor preserves limits|hom-functor preserves products]] in its second argument
$$
  Hom\big(
    \mathcal{I}^{(n)}
    ,\,
    \mathcal{X} \times \mathcal{Y}
  \big)
  \;\simeq\;
  Hom\big(
    \mathcal{I}^{(n)}
    ,\,
    \mathcal{X}
  \big)
  \,\times\,
  Hom\big(
    \mathcal{I}^{(n)}
    ,\,
    \mathcal{Y}
  \big)
$$
this establishes an [[underlying]] bijection of component [[sets]] in (eq:MappingObjectHomIsomorphism) via the [[cartesian closed monoidal category]]-structure of [[Set]] itself. It remains to see that this is compatible with the structure morphisms, which is degree-wise the same argument which shows that a [[functor category]] is an [[internal hom]] in [[Cat]].
\end{proof}



## Related concepts

* [[model structure on simplicial groupoids]]

* [[simplicial category]]
  
  * [[simplicially enriched category]]

  * [[simplicial object in Cat]]

* [[relation between quasi-categories and simplicial categories]]

* [[model structure on presheaves of simplicial groupoids]]

## References

Original discussion in the context of a [[model structure on simplicial groupoids]]:

* {#DwyerKan84} [[William Dwyer]], [[Daniel Kan]],  _Homotopy theory and simplicial groupoids_, Indagationes Mathematicae (Proceedings) **87** 4 (1984) 379-385 &lbrack;<a href="https://doi.org/10.1016/1385-7258(84)90038-6">doi:10.1016/1385-7258(84)90038-6</a>&rbrack;
 
with a detailed textbook account in:

* {#GoerssJardine09} [[Paul Goerss]], [[J. F. Jardine]], Section V.7 of: _[[Simplicial homotopy theory]]_, Progress in Mathematics, Birkh&#228;user (1999) Modern Birkh&#228;user Classics (2009) &lbrack;[doi:10.1007/978-3-0346-0189-4](https://link.springer.com/book/10.1007/978-3-0346-0189-4), [webpage](http://web.archive.org/web/19990208220238/http://www.math.uwo.ca/~jardine/papers/simp-sets/)&rbrack; 

See also:

* [[Philip Ehlers]], _Simplicial groupoids as models for homotopy type_, Master's thesis (1991) &lbrack;[pdf](https://ncatlab.org/nlab/files/Ehlers-MSc-thesis.pdf)&rbrack;

* [[Philip J. Ehlers]], *Algebraic Homotopy in Simplicially Enriched Groupoids*, PhD thesis (1993) &lbrack;[[Ehlers-thesis.pdf|pdf:file]]&rbrack;


[[!redirects simplicial groupoids]]
[[!redirects simplicially enriched groupoids]]
[[!redirects simplicially enriched groupoid]]