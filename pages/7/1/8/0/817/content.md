
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of $V$-[[enriched category theory]] (with $V$ any suitable [[cosmos for enrichment]]) for $\mathbf{C}$, $\mathbf{D}$ a [[pair]] of [[enriched categories|$V$-enriched categories]], there is, fist of all, an ordinary [[category]] whose 

* [[objects]] are the [[enriched functors]] $F \colon \mathbf{C} \longrightarrow \mathbf{D}$,

* [[morphisms]] $\eta \colon F \Rightarrow F'$ are the [[enriched natural transformations]].

This notion is a generalization of the plain notion of the *[[functor category]]* between [[locally small categories]], to which it reduces in the case that $V \equiv $ [[Set]] equipped with its [[cartesian monoidal category|cartesian monoidal]]-[[structure]]. 

As such one may and does call this ordinary category the "enriched functor category" between $\mathbf{C}$ and $\mathbf{D}$, in the sense of the "category of enriched functors".

However, this category of enriched functors canonically enhances further to a $V$-[[enriched category]] itself, hence to an "enriched-functor enriched-category", then traditionally often denoted $[\mathbf{C}, \mathbf{D}]$ or similar.

Namely, for
$
  F, G \,\colon\, \mathbf{C} \longrightarrow \mathbf{D}
$
a [[pair]] of $V$-[[enriched functors]] between $V$-[[enriched categories]], the collection of [[enriched natural transformations]] from $F$ to $G$ can also be given the [[structure]] of an [[object]] in $V$, in a compatible way:


## Definition

For $\mathbf{C}$ and $\mathbf{D}$ $V$-[[enriched categories]], there is a $V$-[[enriched category]], denoted $[\mathbf{C},\,\mathbf{D}]$, whose

* [[objects]] are the $V$-[[enriched functors]] $F \colon \mathbf{C} \longrightarrow \mathbf{D}$

* [[hom-objects]] $\;[C,D](F,G)$ between $V$-functors $F, G$ are given by the $V$-enriched [[end]]
$$
  [\mathbf{C},\mathbf{D}](F,G) 
  \;\coloneqq\; 
  \textstyle{\int}_{c \in \mathbf{C}} 
  \mathbf{D}\big(F(c),\, G(c)\big)
$$
over the [[enriched hom-functor]]
$$
  \mathbf{D}\big(
    F(-)
    ,\,
    G(-)
  \big) 
  \;\colon\; 
  \mathbf{C}^{op} 
    \otimes 
  \mathbf{C} 
    \longrightarrow
  V
  \,,
$$

* the [[composition]] operation 

$$
  \circ_{K,F,G} 
    \,\colon\, 
  [\mathbf{C},\mathbf{D}](F,G)
    \otimes 
  [\mathbf{C},\mathbf{D}](K,F) 
   \longrightarrow 
  [\mathbf{C},\mathbf{D}](K,G)
$$
is the universal morphism into the [[end]] $[\mathbf{C},\mathbf{D}](K,F)$ obtained from observing that the composites
$$
  [\mathbf{C},\mathbf{D}](F,G)
    \otimes 
  [\mathbf{C},\mathbf{D}](K,F)
    \stackrel{E_c\otimes E_d}{\longrightarrow}
  \mathbf{D}\big(F(c),G(c)\big) 
    \otimes 
  \mathbf{D}\big(K(c),F(c)\big)
    \stackrel{\circ_{K(c), F(c), G(c)}}{\longrightarrow}
  \mathbf{D}\big(K(c), F(c)\big)
$$

  (where $E_c \colon [\mathbf{C},\mathbf{D}](F,G) \to \mathbf{D}\big(F(c),G(c)\big)$ denotes the canonical [[morphism]] out of the [[end]], i.e. the counit)

  form an [[extranatural transformation|extra $V$-natural]] family, equivalently that
$$
 [\mathbf{C},\mathbf{D}](F,G)
   \otimes 
 [\mathbf{C},\mathbf{D}](K,F)
   \stackrel
    {\prod_{c \in Obj(c)}E_c\otimes E_c}
    {\longrightarrow}
 \prod_{c \in Obj(c)}
 \mathbf{D}\big(F(c),G(c)\big) 
   \otimes 
 \mathbf{D}\big(K(c),\,F(c)\big)
 \stackrel{\prod_{c \in Obj(c)}
   \circ_{K(c), F(c), G(c)}}{\longrightarrow}
 \prod_{c \in Obj(c)}
   \mathbf{D}\big(K(c),\,G(c)\big)
$$
equalizes the two maps appearing in the [[equalizer]]-definition of the [[end]].


+-- {: .un_prop}
###### Proposition

For $V = $[[Set]], so that $V$-enriched categories are just ordinary [[locally small category|locally small categories]], the $V$-enriched functor category coincides with the ordinary [[functor category]].

=--

(For more see the example [below](#OrdinaryFunctorCategories).)

## Examples

### Ordinary functor categories
 {#OrdinaryFunctorCategories}

To understand the role of the [[end]] here, it is useful to spell this out for the case where $V =$ [[Set]], where we are dealing with ordinary [[locally small category|locally small]] categories.

So let $V = Set$ where set is equipped with its [[cartesian monoidal category|cartesian monoidal structure]].

Recall the definition of the [[end]] over

$$
  \mathbf{D}\big(
    F(-),G(-)
  \big) 
  \,\colon\, 
  \mathbf{C}^{op} \otimes \mathbf{C} 
    \longrightarrow 
  Set
$$

as an [[equalizer]]: it is the [[universal property|universal]] [[subobject]] 

$$
  \textstyle{\int}_{c \in C} \mathbf{D}\big(F(c),\, G(c)\big)
  \hookrightarrow
  \prod_{c \in Obj(C)} \mathbf{D}\big(F(c),\, G(c)\big)
$$

of the [[product]] of all [[hom-sets]] in $D$ between the [[images]] of [[objects]] in $C$ under the [[functors]] $F$ and $G$. So one element $ \eta \in \int_{c \in \mathbf{C}} \mathbf{D}\big(F(c), G(c)\big)$ is a collection of morphisms

$$
  \big( 
    F(c) 
      \stackrel{\eta_c}{\longrightarrow} 
    G(c)
  \big)_{c \in Obj(c)}
$$

such that the "left and right [[action]]" (in the sense of [[distributors]]) of $\mathbf{D}\big(F(-),G(-)\big)$ on these elements coincides. Unwrapping what this action is (see the details at [[end]]) one find that 

* the "right [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the postcomposition $
  (F(c) \stackrel{\eta_c}{\to} G(c)) \mapsto
  (F(c) \stackrel{\eta_c}{\to} G(c) \stackrel{G(f)}{\to} G(d))
$

* the "left [[action]]" by a morphism $c \stackrel{f}{\to} d$ is the precomposition $
  (F(d) \stackrel{\eta_d}{\to} G(d)) \mapsto
  (F(c) \stackrel{F(f)}{\to} F(d) \stackrel{\eta_d}{\to} G(d) )
$.

So the [[invariants]] under the combined action are those $\eta$ for which for all $f \colon c \to d$ in $C$ the [[diagram]]
$$
  \array{
    F(c) &\stackrel{\eta_c}{\longrightarrow} & G(c)
    \\
    \Big\downarrow\mathrlap{{}^{F(f)}}
    &&
    \Big\downarrow\mathrlap{{}^{G(f)}}
    \\
    F(d) 
    &
      \stackrel{\eta_d}{\longrightarrow} 
    & 
    G(d)
  }
$$

[[commuting diagram|commutes]]. Evidently, this means that the elements $\eta$ of the [[end]] $\int_{c \in \mathbf{C}} \mathbf{D}\big(F(c), G(c)\big)$ are precisely the [[natural transformation]]s between $F$ and $G$.

### Pointwise order

For categories enriched in [[truth values]], the enriched functor category is given by the [[pointwise order]].




## Properties
 {#Properties}


### Enhanced enrichment
 {#EnhancedEnrichment}

It happens that a $V$-enriched functor category $Func(\mathbf{X},\mathbf{C})$ --- which by the above discussion is a priori a $\mathbf{V}$-enriched category --- carries an enhanced enrichment over the functor category $Func(\mathbf{X},\mathbf{V})$.

A common kind of example are categories of [[simplicial objects]] in an ordinary $Set$-enriched category -- hence functor categories $Func(\Delta^{op}, C)$ on the [[opposite category|opposite]] [[simplex category]] -- which one wants to regard not just enriched in $Set$, but as enriched in $Func(\Delta^{op}, Set) \,\equiv\,$ [[sSet]], namely in [[simplicial sets]]. 

We may bootstrap the discussion of this situation by first considering the case where $\mathbf{C} = \mathbf{V}$ itself, where it means that $Func(\mathbf{X},\mathbf{V})$ is closed monoidal under the $\mathbf{X}$-objectwise tensor product taken in $\mathbf{V}$.
In the base case where $\mathbf{V} = $ [[Set]] this reduces to the statement of the [[closed monoidal structure on presheaves]].

\begin{proposition}
\label{EnhancedEnichmentFormulas}
Let

* $(V, \otimes)$ be a [[bicomplete category|bicomplete]] [[closed monoidal category]], canonically regarded as a $V$-[[enriched category|enriched]] $\mathbf{V}$ 

  via its [[internal hom]] $[-,-]$;

* $\mathbf{C}$ a [[bicomplete category|bicomplete]] $V$-[[enriched category]] which is 

  also $V$-[[tensoring|tensored]], via $\mathbf{V} \times \mathbf{C} \overset{(\text{-})\cdot(\text{-})}{\longrightarrow} \mathbf{C}$,

  and $V$-[[cotensoring|cotensored]] via $\mathbf{V}^{op} \times \mathbf{C} \overset{(\text{-})^{(\text{-})}}{\longrightarrow} \mathbf{C}$;

* $\mathbf{X}$ a [[small category|small]] $V$-enriched category.

Then the enriched functor category...

1. ...$\mathbf{V}^{\mathbf{X}} \,\coloneqq\, Func(\mathbf{X},\,\mathbf{V})$ carries [[closed monoidal category]]  structure

   given by the $\mathbf{X}$-objectwise [[tensor product]]

   $$
     \mathcal{S}_{\mathbf{X}}
     ,\,
     \mathcal{T}_{\mathbf{X}}
     \,\in\,
     \mathbf{V}^{\mathbf{X}}
     \;\;\;\;\;\;\;\;\;\;
     \vdash
     \;\;\;\;\;\;\;\;\;\;
     \mathcal{S}_{\mathbf{X}}
     \otimes
     \mathcal{T}_{\mathbf{X}}
     \;\colon\;
     x \;\mapsto\;
     (\mathcal{S}_{\mathbf{X}} \otimes \mathcal{T}_{\mathbf{X}})_x
     \;\;
       \coloneqq
     \;\;
     \mathcal{S}_x \otimes \mathcal{T}_x
   $$

   and with corresponding [[internal hom]] given by:

   $$
     \mathcal{S}_{\mathbf{X}}
     ,\,
     \mathcal{T}_{\mathbf{X}}
     \,\in\,
     \mathbf{V}^{\mathbf{X}}
     \;\;\;\;\;\;\;\;\;\;
     \vdash
     \;\;\;\;\;\;\;\;\;\;
     \big[
       \mathcal{S}_{\mathbf{X}}
       ,\,
       \mathcal{T}_{\mathbf{X}}
     \big]    
     \;\colon\;
     x \;\mapsto\;
     \big[
       \mathcal{S}_{\mathbf{X}}
       ,\,
       \mathcal{T}_{\mathbf{X}}
     \big]_x
     \;\;
       \coloneqq
     \;\;    
     \textstyle{\int}_{x' \in \mathbf{X}}
     \mathbf{V}\big(
       \mathbf{X}(x,x') 
         \otimes
       \mathcal{S}_{x'}
       ,\,
       \mathcal{T}_{x'}
     \big)
     \,.
   $$

1. ... $\mathbf{C}^{\mathbf{X}}$ becomes [[enriched category|enriched]], [[tensoring|tensored]] and  [[cotensoring|cotensored]] over $\mathbf{V}^{\mathbf{X}}$, via the following [[end]]-formulas, respectively:

   $$
     \begin{array}{rccl}
       \mathscr{V}_{\mathbf{X}}
       ,\,
       \mathscr{W}_{\mathbf{X}}
       \;\in\;
       \mathbf{C}^{\mathbf{X}}
       &\;\;\;\vdash\;\;\;&
       \mathbf{C}^{\mathbf{X}}
       \big(
         \mathscr{V}_{\mathbf{X}}
         ,\,
         \mathscr{W}_{\mathbf{X}}
       \big)
       &
       \coloneqq\;
       \Big(
         x 
           \,\mapsto\,
         \textstyle{\int}_{x' \in \mathbf{X}}
         \mathbf{C}\big(
           \mathbf{X}(x,x')
           \cdot
           \mathscr{V}_{x'}
           ,\,
           \mathscr{W}_{x'}
         \big)
       \Big) 
       \;\;\;
       \in
       \;
       \mathbf{V}^{\mathbf{X}}
       \\
       \mathcal{S}_{\mathbf{X}}
       \,\in\, \mathbf{V}^{\mathbf{X}}
       ;\;
       \mathscr{V}_{\mathbf{X}}
       \in\,
       \mathbf{C}^{\mathbf{X}}
       &\vdash&
       \mathcal{S}_{\mathbf{X}}
       \cdot
       \mathscr{V}_{\mathbf{X}}
       &
       \coloneqq\;
       \big(
         x
         \,\mapsto\,
         \mathcal{S}_{x'} \cdot \mathscr{V}_{x'}
       \big)
       \;\;\;
       \in
       \;
       \mathbf{C}^{\mathbf{X}}
       \\
       \mathcal{S}_{\mathbf{X}}
       \,\in\, \mathbf{V}^{\mathbf{X}}
       ;\;
       \mathscr{V}_{\mathbf{X}}
       \in\,
       \mathbf{C}^{\mathbf{X}}
       &\vdash&
       \big(\mathscr{V}_{\mathbf{X}}\big)^{
         \mathcal{S}_{\mathbf{X}}      
       }
       &
       \coloneqq\;
       \Big(
         x
         \,\mapsto\,
         \textstyle{\int}_{x' \in \mathbf{X}}
         \big(\mathscr{W}_{x'}\big)^{
           \mathbf{X}(x,x')
           \otimes
           \mathcal{S}_{x'}
         }
       \Big)
       \;\;\;
       \in
       \;
       \mathbf{C}^{\mathbf{X}}
       \mathrlap{\,.}
     \end{array}  
   $$ 

\end{proposition}
\begin{proof}
Observe the following sequence of [[natural isomorphisms]]:
$$
  \begin{array}{ll}
  Func(\mathbf{X},\,\mathbf{V})
  \big(
    \mathcal{R}_{\mathbf{X}}
    \;,\;
    [\mathcal{S}_{\mathbf{X}},\, \mathcal{T}_{\mathbf{X}}]
  \big)  
  \\
  \;\simeq\;
  \textstyle{\int}_{x \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \mathcal{R}_{x}
    \;,\;
    \int_{y \in \mathbf{X}}
    \mathbf{V}
    \big(
      \mathbf{X}(x,y)
      \otimes
      \mathcal{S}_{y}
      \;,\; 
      \mathcal{T}_{y}
    \big)
  \Big)  
  &
  \text{by the definitions}
  \\
  \;\simeq\;
  \int_{x \in \mathbf{X}}
  \int_{y \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \mathcal{R}_{x}
    \;,\;
    \mathbf{V}
    \big(
      \mathbf{X}(x,y)
      \otimes
      \mathcal{S}_{y}
      \;,\;
      \mathcal{T}_{y}
    \big)
  \Big)  
  &
  \text{ since internal homs preserve limits }
  \\
  \;\simeq\;
  \int_{x \in \mathbf{X}}
  \int_{y \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \mathbf{X}(x,y)
    \otimes
    \mathcal{R}_{x}
    \otimes
    \mathcal{S}_{y}
    \;,\;
    \mathcal{T}_{y}
  \Big) 
  & 
  \text{by closed monoidal structure of}\;\mathbf{V}
  \\
  \;\simeq\;
  \int_{y \in \mathbf{X}}
  \int_{x \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \mathbf{X}(x,y)
    \otimes
    \mathcal{R}_{x}
    \otimes
    \mathcal{S}_{y}
    \;,\;
    \mathcal{T}_{y}
  \Big)  
  &
  \text{ by Fubini theorem for ends }
  \\
  \;\simeq\;
  \int_{y \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \big(
    \int^{x \in \mathbf{X}}
    \mathbf{X}(x,y)
    \otimes
    \mathcal{R}_{x}
    \big)
    \otimes
    \mathcal{S}_{y}
    \;,\;
    \mathcal{T}_{y}
  \Big)  
  &
  \text{ since internal homs preserve limits }
  \\
  \;\simeq\;
  \int_{y \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \mathcal{R}_{y}
    \otimes
    \mathcal{S}_{y}
    \;,\;
    \mathcal{T}_{y}
  \Big)  
  &
  \text{ by co-Yoneda lemma }
  \\
  \;\simeq\;
  \int_{y \in \mathbf{X}}
  \mathbf{V}
  \Big(
    \big(
    \mathcal{R}_{\mathbf{X}}
    \otimes
    \mathcal{S}_{\mathbf{X}}
    \big)_{y}
    \;,\;
    \mathcal{T}_{y}
  \Big)  
  &
  \text{ by definition }
  \\
  \;\simeq\;
  Func(\mathbf{X},\mathbf{V})
  \big(
    \mathcal{R}_{\mathbf{X}}
    \otimes
    \mathcal{S}_{\mathbf{X}}
    \;,\;
    \mathcal{T}_{\mathbf{X}}
  \big)
  &
  \text{ by definition, }
  \end{array}
$$
where we used, apart from the above definitions:

1. that [[internal hom-functors preserve limits]]

1. the [Fubini theorem for ends](end#Fubini)

1. the [[co-Yoneda lemma]].

This establishes that $[-,-]$ is an internal hom in $Func(\mathbf{X},\mathbf{V})$ for the objectwise tensor product, as claimed.

The natural isomorphisms needed to exhibit the (co)tensoring of $\mathbf{C}^{\mathbf{X}}$ both follow essentially the same sequence of steps, just up to the relevant substitutions. For definiteness we spell it out again, but now proceeding in the reverse order of steps:

Given 

* $\mathcal{S}_{\mathbf{X}} \in Func(\mathbf{X},\mathbf{V})$,

* $\mathscr{V}_{\mathbf{X}},\, \mathscr{W}_{\mathbf{X}}  \in Func(\mathbf{X},\mathbf{V})$,

* $x \in \mathbf{X}$,

consider the following sequence of [[enriched natural transformation|$V$-enriched natural]] isomorphisms in these variables: 

Starting with
$$
  \begin{array}{ll}
    \mathbf{C}^{\mathbf{X}}
    \big(
      \mathcal{S}_{\mathbf{X}}
      \cdot
      \mathscr{V}_{\mathbf{X}}
      \;,\;
      \mathscr{W}_{\mathbf{X}}
    \big)_x
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \mathbf{C}\Big(
      \mathbf{X}(x,z)
      \cdot
      \big(
        \mathcal{S}_{\mathbf{X}} 
        \cdot
        \mathscr{V}_{\mathbf{X}}
      \big)_{z}
      ,\,
      \mathscr{W}_{z}
    \Big)
    &
    \text{ by definition }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \mathbf{C}\big(
      \mathbf{X}(x,z)
      \cdot
      \mathcal{S}_{z} 
      \cdot
      \mathscr{V}_{z}
      \;,\;
      \mathscr{W}_{z}
    \big)
    &
    \text{ by definition }
    \\
    \;\simeq\;
    \cdots
  \end{array}
$$
we invoke the [[co-Yoneda lemma]], either to introduce a fresh variable on $\mathbf{X}(x,-) \cdot \mathcal{S}_{(-)}$ 
$$
  \begin{array}{ll}
    \cdots
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \mathbf{C}\Big(
      \int^{y \in \mathbf{X}}
      \mathbf{X}(y,z)
      \cdot
      \big(
        \mathbf{X}(x,y)
        \cdot
        \mathcal{S}_{y} 
      \big)
      \cdot
      \mathscr{V}_{z}
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ co-Yoneda lemma }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{C}\Big(
      \mathbf{X}(y,z)
      \cdot
      \mathbf{X}(x,y)
      \cdot
      \mathcal{S}_{y} 
      \cdot
      \mathscr{V}_{z}
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{V}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{S}_{y} 
      \;,\;
      \mathbf{C}\big(
        \mathbf{X}(y,z)
        \cdot
        \mathscr{V}_{z}
        \;,\;
        \mathscr{W}_{z}
      \big)
    \Big)
    &
    \text{ tensoring iso of }\; \mathbf{C}
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \int_{z \in \mathbf{X}}
    \mathbf{V}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{S}_{y} 
      \;,\;
      \mathbf{C}\big(
        \mathbf{X}(y,z)
        \cdot
        \mathscr{V}_{z}
        \;,\;
        \mathscr{W}_{z}
      \big)
    \Big)
    &
    \text{ Fubini theorem for ends }
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \mathbf{V}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{S}_{y} 
      \;,\;
      \int_{z \in \mathbf{X}}
      \mathbf{C}\big(
        \mathbf{X}(y,z)
        \cdot
        \mathscr{V}_{z}
        \;,\;
        \mathscr{W}_{z}
      \big)
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \mathbf{V}\Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{S}_{y} 
      \;,\;
      \mathbf{C}^{\mathbf{X}}
      \big(
        \mathscr{V}_{\mathbf{X}}
        ,\,
        \mathscr{W}_{\mathbf{X}}
      \big)_y
    \Big)
    &
    \text{ definition }
    \\
    \;\simeq\;
    \mathbf{V}^{\mathbf{X}}\Big(
      \mathcal{S}_{\mathbf{X}} 
      \;,\;
      \mathbf{C}^{\mathbf{X}}
      \big(
        \mathscr{V}_{\mathbf{X}}
        ,\,
        \mathscr{W}_{\mathbf{X}}
      \big)
    \Big)_x
    &
    \text{ definition }
  \end{array}
$$
or to get a fresh variable on $\mathbf{X}(x,-) \cdot \mathscr{V}_{(-)}$:
$$
  \begin{array}{ll}
    \cdots
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathcal{S}_z
      \cdot
      \int^{y \in \mathbf{X}}
      \mathbf{X}(y,z)
      \cdot
      \big(
        \mathbf{X}(x,y)
        \cdot
        \mathcal{V}_{y}
      \big)
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ co-Yoneda lemma }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathbf{X}(y,z)
      \cdot
      \mathcal{S}_z
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \mathscr{W}_{z}
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{z \in \mathbf{X}}
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ cotensoring iso of }\; \mathbf{C}
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \int_{z \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ Fubini theorem for ends }
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \Big(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \int_{z \in \mathbf{X}}
      \big(\mathscr{W}_{z}\big)^{
        \mathbf{X}(y,z)
        \cdot
        \mathcal{S}_z
      }
    \Big)
    &
    \text{ enriched homs preserve enriched limits }
    \\
    \;\simeq\;
    \int_{y \in \mathbf{X}}
    \mathbf{C}
    \bigg(
      \mathbf{X}(x,y)
      \cdot
      \mathcal{V}_{y}
      \;,\;
      \Big(
        \big(
          \mathscr{W}_{\mathbf{X}}
        \big)^{
          \mathcal{S}_{\mathbf{X}}
        }
      \Big)_y
    \bigg)
    &
    \text{ definition }
    \\
    \;\simeq\;
    \mathbf{C}^{\mathbf{X}}
    \Big(
      \mathcal{V}_{\mathbf{X}}
      \;,\;
      \big(\mathscr{W}_{\mathbf{X}}\big)^{
        \mathcal{S}_{\mathbf{X}}
      }
    \Big)_x
    &
    \text{ definition }
  \end{array}
$$

By naturality in $x \in \mathbf{X}$, these constitute the required $\mathbf{V}^{\mathbf{X}}$-[[enriched natural transformation|-enriched]] [[natural isomorphisms]] for exhibiting the claimed (co)tensoring:
$$
  \mathbf{C}^{\mathbf{X}}
  \big(
    \mathcal{S}_{\mathbf{X}}
    \cdot
    \mathscr{V}_{\mathbf{X}}
    \;,\;
    \mathscr{W}_{\mathbf{X}}
  \big)
  \;\simeq\;
  \mathbf{V}^{\mathbf{X}}
  \Big(
    \mathcal{S}_{\mathbf{X}}
    \;,\;
    \mathbf{C}^{\mathbf{X}}\big(
      \mathscr{V}_{\mathbf{X}}
      \;,\;
      \mathscr{W}_{\mathbf{X}}
    \big)
  \Big)
  \;\simeq\;
  \mathbf{C}^{\mathbf{X}}
  \Big(
    \mathscr{V}_{\mathbf{X}}
    \;,\;
    \big(\mathscr{W}_{\mathbf{X}}\big)^{
      \mathcal{S}_{\mathbf{X}}
    }
  \Big)
  \,.
$$
From this, finally, follows an $\mathbf{V}^{\mathbf{X}}$-enriched composition operation
$$
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{R}_{\mathbf{X}}
    ,\,
    \mathscr{V}_{\mathbf{X}}
  \big)
  \otimes
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{V}_{\mathbf{X}}
    ,\,
    \mathscr{W}_{\mathbf{X}}
  \big)
  \longrightarrow
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{R}_{\mathbf{X}}
    ,\,
    \mathscr{W}_{\mathbf{X}}
  \big)
$$
to be defined as the [[adjunct]] (via the just established adjunctions) of the consecutive [[evaluation maps]] (being themselves the respective [[counit of an adjunction|adjunction counits]]):
$$
  \mathscr{R}_{\mathbf{X}}
  \cdot
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{R}_{\mathbf{X}}
    ,\,
    \mathscr{V}_{\mathbf{X}}
  \big)
  \cdot
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{V}_{\mathbf{X}}
    ,\,
    \mathscr{W}_{\mathbf{X}}
  \big)
  \overset{ev}{\longrightarrow}
  \mathscr{V}_{\mathbf{X}}
  \cdot
  \mathbf{C}^{\mathbf{X}}\big(
    \mathscr{V}_{\mathbf{X}}
    ,\,
    \mathscr{W}_{\mathbf{X}}
  \big)
  \overset{ev}{\longrightarrow}
  \mathscr{W}_{\mathbf{X}}
  \,.
$$
\end{proof}



## Related concepts

* [[enriched Reedy category]]

* [[model structure on homotopical presheaves]]

* [[model structure on sSet-presheaves]]

## References

An original article:

* [[Brian Day]], [[Max Kelly]], *Enriched functor categories*, in: *Reports of the Midwest Category Seminar III*, Lecture Notes in Mathematics **106** (1969) 178-191 &lbrack;[doi:10.1007/BFb0059146](https://doi.org/10.1007/BFb0059146), [pdf](https://link.springer.com/content/pdf/10.1007/BFb0059146.pdf)&rbrack;

Review includes

* {#Day70} [[Brian Day]], _On closed categories of functors_, Reports of the Midwest Category Seminar IV, Lecture Notes in Mathematics Vol. 137. Springer-Verlag, 1970, pp 1-38 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/DayReport.pdf))

* [[Max Kelly]], [section 2.2 p. 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=29) of: _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;


[[!redirects enriched functor categories]]

[[!redirects enriched-functor category]]
[[!redirects enriched-functor categories]]

[[!redirects enriched functor-category]]
[[!redirects enriched functor-categories]]


[[!redirects enriched presheaf category]]
[[!redirects enriched presheaf categories]]

[[!redirects category of enriched presheaves]]
[[!redirects categories of enriched presheaves]]




