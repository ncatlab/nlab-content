+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The [[category of presheaves]] over the [[opposite category|opposite]] of a [[monoidal category]] canonically inherits itself a monoidal category structure via a [[categorification|categorified]] [[convolution product]]. This holds generally in the context of [[enriched category theory]]. This was first observed by ([Day 70](#Day70)) and accordingly these monoidal structures are called _Day convolutions_ products.

More in detail, just as there is [[convolution]] of  [[functions]] $f : G \to \mathbb{C}$ whenever $G$ carries the structure of a  [[group]], or more generally just the structure of a [[monoid]], so there is convolution of  [[functors]] $f \colon  \mathcal{G} \to Set$ whenever the [[category]] $\mathcal{G}$ carries the structure of a [[monoidal category]].  

This may be generalized by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]] $V$. The technical condition is that the [[tensor product]] $u \otimes v$ preserves [[colimits]] in its two arguments separately; hence that the functors $u \otimes -$ and $- \otimes v$ preserve colimits. This occurs notably when $V$ is symmetric [[closed monoidal category|closed monoidal]] (so that these functors are [[left adjoints]]). 

## Definition

### For monoidal categories
 {#ForMonoidalCategories}

Let $V$ be [[closed monoidal category|closed]] [[symmetric monoidal category]] with all small [[limits]] and [[colimits]].

For $\mathcal{C}$ a  $V$-[[enriched category]], write $[\mathcal{C},V]$ for the $V$-[[enriched functor category]] to $V$, etc.

+-- {: .num_defn #DayConvolutionProduct}
###### Definition

For $(\mathcal{C}, \otimes_{\mathcal{C}}, I)$ a [[small category|small]] [[monoidal category|monoidal]] $V$-[[enriched category]], the _Day convolution product_ on the [[enriched functor category]] $[\mathcal{C},V]$ is the [[functor]]

$$
  \otimes_{Day} \;\colon\; [\mathcal{C},V] \times [\mathcal{C},V] \longrightarrow [\mathcal{C},V]
$$

given by the [[coend]]

$$
  X \otimes_{Day} Y
  \;\colon\;
  c \mapsto
  \int^{c_1, c_2 \in \mathcal{C}}
   \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c) \otimes_V X(c_1) \otimes_V Y(c_2) 
  \,.
$$

=--

We may think of this equivalently as a [[Kan extension]]:

+-- {: .num_defn #ExternalTensorProduct}
###### Definition

For $(\mathcal{C}, \otimes_{\mathcal{C}})$ a [[monoidal category|monoidal]] $V$-[[enriched category]], its _[[external tensor product]]_ is the $V$-functor

$$
  \widetilde \otimes_V 
    \;\colon\; 
  [\mathcal{C},V] \times [\mathcal{C},V] 
    \longrightarrow 
  [\mathcal{C}\times \mathcal{C}, V]
$$

given by 

$$
  X \widetilde \otimes_V Y  
    \coloneqq 
  \otimes_V \circ (X,Y)
  \,.
$$

=--


+-- {: .num_prop #DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}
###### Proposition

The Day convolution product, def. \ref{DayConvolutionProduct}, is equivalently given by left [[Kan extension]] $Lan_{\otimes_{\mathcal{C}}}$ (along the tensor product $\otimes_{\mathcal{C}}$) of the result of the external tensor product, def. \ref{ExternalTensorProduct}: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes_{\mathcal{C}}} (X \widetilde \otimes_V Y)
  \,.
$$

=--

This perspective is highlighted in ([MMSS 00, p. 60](#MMSS00)).

+-- {: .proof}
###### Proof

The general formula for pointwise Kan extension via coends ([here](Kan%20extension#PointwiseByCoEnds)) says that left Kan extension of any $F \colon \mathcal{D} \to V$ along some $p \colon \mathcal{D} \to \mathcal{E}$ is given by 

$$
  Lan_p F \;\colon\; e \mapsto \int^{d\in \mathcal{D}} \mathcal{E}(p(d), e) \otimes F(d)
  \,.
$$

In our case 

* $\mathcal{D} = \mathcal{C}\times \mathcal{C}$;

* $\mathcal{E} = \mathcal{C}$;

* $p = \otimes_{\mathcal{C}}$;

*  $F = X \widetilde \otimes_V X$ 

and hence the general formula here becomes

$$
  \begin{aligned}
    (Lan_{\otimes_{\mathcal{C}}} X \widetilde \otimes_V Y)(c)
    & \simeq
    \int^{(c_1,c_2) \in \mathcal{C}\times \mathcal{C}}
    \mathcal{C}( c_1 \otimes_{\mathcal{C}} c_2, c ) \otimes_V ( (X \widetilde \otimes Y)(c_1,c_2) )
    \\
    & \simeq 
    \int^{(c_1,c_2) \in \mathcal{C}\times \mathcal{C}}
    \mathcal{C}( c_1 \otimes_{\mathcal{C}} c_2, c ) \otimes_V ( X(c_1) \otimes_V Y(c_2) )
  \end{aligned}
  \,.
$$

=--

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

Day convolution $\otimes_{Day}$, def. \ref{DayConvolutionProduct}, is universally characterized by the property that there are [[natural isomorphisms]]

$$
  [\mathcal{C},V](X \otimes_{Day} Y, Z) 
    \simeq 
  [\mathcal{C}\times \mathcal{C},V](
    X \widetilde{\otimes}_V Y, 
    Z \circ \otimes_{\mathcal{D}}
  )
  \,,
$$

where $\widetilde \otimes_V$ is the external tensor product of def. \ref{ExternalTensorProduct}.

=--

+-- {: .proof}
###### Proof

By prop. \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} and since left [[Kan extension]] along any $f$ is the [[left adjoint]] to precomposition with $f$.

=--

Write

$$
  y \colon \mathcal{C}^{op} \longrightarrow [\mathcal{C}, V]
$$

for the $V$-[[Yoneda embedding]], so that for $c\in \mathcal{C}$ any [[object]], $y(c)$ is the [[representable functor|corepresented functor]] $y(c)\colon c' \mapsto [c,c']$.





### For promonoidal categories

In the original article ([Day 70](#Day70)), a stronger form of the convolution is discussed, in which $A$ is assumed only to be a [[promonoidal category]].

Let $V$ be a [[Benabou cosmos]], and $A$ a small $V$-[[enriched category]].


+-- {: .num_prop}
###### Proposition

There is an [[equivalence of categories]] between the category of [[pro-monoidal structures]] on $A$ with strong pro-monoidal functors between them and the category of biclosed monoidal structures on $V^{A^{op}}$ with [[strong monoidal functors]] between them.  

=--

This is claimed without proof in ([Day 70](#Day70)).



## Properties 
  {#Properties}


### Closed monoidal structure
 {#ClosedMonoidalStructure}

+-- {: .num_prop #DayConvolutionYieldsMonoidalCategoryStructure}
###### Proposition

For $(\mathcal{C}, \otimes_{\mathcal{C}}, I)$ a [[small category|small]] [[monoidal category|monoidal]] $V$-[[enriched category]],
the Day convolution product $\otimes_{Day}$ of def. \ref{DayConvolutionProduct} makes

$$
  ( [\mathcal{C}, V], \otimes_{Day}, y(I))
$$

a [[monoidal category]] with [[tensor unit]] $y(I)$ co-represented by the tensor unit $I$ of $\mathcal{C}$. 
=--

+-- {: .proof}
###### Proof

Regarding [[associativity]], observe that

$$
  \begin{aligned}
    (X \otimes_{Day} ( Y \otimes_{Day} Z ))(c)
    & \simeq
    \overset{(c_1,c_2)}{\int}
      \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2, \,c) 
        \otimes_V
      X(c_1) 
       \otimes_V
      \overset{(d_1,d_2)}{\int}
       \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c_2 )
       (Y(d_2) \otimes_V Z(d_2))
    \\
    &\simeq \overset{c_1, d_1, d_2}{\int}
    \underset{\simeq \mathcal{C}(c_1 \otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c )}{
      \underbrace{
       \overset{c_2}{\int} 
         \mathcal{C}(c_1 \otimes_{\mathcal{D}} c_2 , c)
           \otimes_V
         \mathcal{C}(d_1 \otimes_{\mathcal{C}}d_2, c_2 )
      }
    }
    \otimes_V X(c_1) \otimes_V (Y(d_1) \otimes_V Z(d_2))
    \\
    &\simeq 
    \overset{c_1, d_1, d_2}{\int}
     \mathcal{C}(c_1\otimes_{\mathcal{C}} d_1 \otimes_{\mathcal{C}} d_2, c ) 
       \otimes_V  
     X(c_1) \otimes_V (Y(d_1) \otimes_V Z(d_2))
  \end{aligned}
  \,,
$$

where we used the [[Fubini theorem]] for coends, and the [[co-Yoneda lemma]].
Similarly for $((X \otimes_{Day} Y) \otimes_{Day} Z)(c)$. Hence associativity follows from the associativity of $\otimes_{\mathcal{C}}$ and $\otimes_V$.

To see that $y(I)$ is the tensor unit for $\otimes_{Day}$, 
use the [[Fubini theorem]] for [[coends]] and then twice the [[co-Yoneda lemma]] to get for any $X \in [\mathcal{C},V]$ that

$$
  \begin{aligned}
     X \otimes_{Day} y(I)
     & 
     =
     \int^{c_1,c_2 \in \mathcal{C}}
     X(c_1) \otimes_V [I,c_2] \otimes_V [c_1 \otimes_{\mathcal{C}} c_2,-]
     \\
     & \simeq 
     \int^{c_1\in \mathcal{C}}
      X(c_1) 
         \otimes_V  
      \int^{c_2 \in \mathcal{C}}  [I,c_2] \otimes_V [c_1\otimes_{\mathcal{C}} c_2,-]
    \\
    & \simeq 
      \int^{c_1\in \mathcal{C}}
      X(c_1) 
         \otimes_V
      [c_1 \otimes_{\mathcal{C}} I, -]
    \\
    & \simeq 
      \int^{c_1\in \mathcal{C}}
      X(c_1) 
         \otimes_V
      [c_1, -]  
    \\
    & \simeq
    X(-)
    \\
    & \simeq 
    X
  \end{aligned}
  \,.
$$


=--

+-- {: .num_prop #DayMonoidalStructureIsClosed}
###### Proposition

For $(\mathcal{C}, \otimes_{\mathcal{C}}, I)$ a [[small category|small]] [[monoidal category|monoidal]] $V$-[[enriched category]], the monoidal category with Day convolution $([\mathcal{C},V], \otimes_{Day}, y(I))$ from def. \ref{DayConvolutionYieldsMonoidalCategoryStructure} is a [[closed monoidal category]]. Its [[internal hom]] $[-,-]_{Day}$ is given by the [[end]]

$$
  [X,Y]_{Day}(c)
  \simeq
   \underset{c_1,c_2}{\int}
      V\left( 
        \mathcal{C}(c \otimes_{\mathcal{C}} c_1,c_2),
        V(X(c_1), Y(c_2)) 
      \right)       
  \,.
$$

=--

+-- {: .proof}
###### Proof

In analogy to the cartesian [[closed monoidal structure on presheaves]]
we see that if the [[internal hom]] in $[\mathcal{C},V]$ exists at all, 
(with $[-,X]_{Day}$ [[right adjoint]] to $(-) \otimes_{Day} X$) then by the [[enriched Yoneda lemma]] and by the [[end]]-expression for the [[hom-objects]] in the [[enriched functor category]] $[\mathcal{C},V]$ it has to be given by

$$
  \begin{aligned}
    [X,Y]_{Day}(c) 
      & \simeq 
    [\mathcal{C},V](y(c), [X,Y])
    \\
    &
    \simeq 
      [\mathcal{C},V](y(c) \otimes_{Day} X, Y)
    \\
    & \simeq
    \underset{c_1}{\int} V((y(c) \otimes_{\mathcal{C}} X)(c_1), Y(c_1))
    \\
    &\simeq
    \underset{c_1}{\int} 
      V\left(
         \overset{d_2}{\int}
         \overset{d_1}{\int}
         \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c_1)
           \otimes_V
         \mathcal{C}(c,d_1)
         \otimes_V
         X(d_2)
         ,
         Y(c_1)
      \right)
    \\
    & \simeq
    \underset{c_1}{\int} 
    \underset{d_2}{\int}
      V\left(
        \underset{\simeq \mathcal{C}(c \otimes_{\mathcal{C}} d_2, c_1 )}{
          \underbrace{
            \overset{d_1}{\int}
            \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c_1)
              \otimes_V
            \mathcal{C}(c,d_1)
           }
         }
         \otimes_V
         X(d_2)
         ,
         Y(c_1)
      \right)
      \\
      & \simeq
      \underset{c_1,d_2}{\int}
      V\left( 
        \mathcal{C}(c \otimes_{\mathcal{C}} d_2,c_1),
        V(X(d_2), Y(c_1)) 
      \right)
      \\
      & =
      \underset{c_1,c_2}{\int}
      V\left( 
        \mathcal{C}(c \otimes_{\mathcal{C}} c_1,c_2),
        V(X(c_1), Y(c_2)) 
      \right)       
  \end{aligned}
  \,.
$$

This exists, by the assumption that $\mathcal{C}$ is [[small category|small]] and that $V$ has all small limits. Now to check that this really gives a right adjoint:

$$
  \begin{aligned}
     [\mathcal{C},V]( X, [Y,Z]_{Day} )
       & \simeq
     \underset{c}{\int} V\left(
        X(c), 
        \underset{c_1,c_2}{\int}
        V\left( 
          \mathcal{C}(c \otimes_{\mathcal{C}} c_1 , c_2),
          V(Y(c_1), Z(c_2)) 
        \right)
     \right)
     \\
     &
     \simeq
     \underset{c}{\int}
     \underset{c_1,c_2}{\int}
     V\left(
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \otimes_V
       X(c)
         \otimes_V 
       Y(c_1)
       ,\;
       Z(c_2)
     \right)
     \\
     & \simeq
     \underset{c_2}{\int}
     V\left(
       \overset{c,c_1}{\int}
       \mathcal{C}(c \otimes_{\mathcal{C}} c_1, c_2)
         \otimes_V
       X(c)
         \otimes_V 
       Y(c_1)
       ,\;
       Z(c_2)
     \right)
     \\
     &\simeq
     \underset{c_2}{\int}
       V\left(
         (X \otimes_{Day} Y)(c_2),
         Z(c_2)
       \right)
     \\
     &\simeq
     [\mathcal{C},V](X \otimes_{Day} Y, Z)
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The [[Yoneda embedding]] constitutes a  [[strong monoidal functor]] $(\mathcal{C},\otimes_{\mathcal{C}}, I) \hookrightarrow ([\mathcal{C},V], \otimes_{Day}, y(I))$.

=--

+-- {: .proof}
###### Proof

That the [[tensor unit]] is respected is part of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure}. To see that the tensor product is respected, apply the [[co-Yoneda lemma]] twice to get the following natural isomorphism

$$
  \begin{aligned}
    (y(c_1) \otimes_{Day} y(c_2))(c)
    &
    \simeq
    \overset{d_1, d_2}{\int} 
      \mathcal{C}(d_1 \otimes_{\mathcal{C}} d_2, c )
    \otimes_V
      \mathcal{C}(c_1,d_1)
    \otimes_V
      \mathcal{C}(c_2,d_2)
    \\
    & \simeq \mathcal{C}(c_1\otimes_{\mathcal{C}}c_2 , c )
    \\
    & 
    = y(c_1 \otimes_{\mathcal{C}} c_2 )(c)
  \end{aligned}
  \,.
$$

=--




### Monoids with respect to Day convolution
 {#Monoids}

Given any [[monoidal category]] then one may consider [[monoid objects]] and [[module objects]] inside it.

+-- {: .num_prop #DayMonoidsAreLaxMonoidalFunctorsOnTheSite}
###### Proposition

For $(\mathcal{C}, \otimes)$ a [[small category|small]] ([[symmetric monoidal category|symmetric]]) [[monoidal category|monoidal]] $V$-[[enriched category]],
then ([[commutative monoid object|commutative]]) [[monoid objects]] in the Day convolution monoidal category $([\mathcal{C},V], \otimes_{Day}, y(I))$ of prop. \ref{DayConvolutionYieldsMonoidalCategoryStructure} are equivalent to ([[symmetric monoidal functor|symmetric]]) [[lax monoidal functors]] $\mathcal{C} \to V$:

$$
  Mon([\mathcal{C},V], \otimes_{Day}, y(I))
  \simeq
  MonFunc(\mathcal{C},V)
$$

$$
  CMon([\mathcal{C},V], \otimes_{Day}, y(I))
  \simeq
  SymMonFunc(\mathcal{C},V)
  \,.
$$

Moreover, [[module objects]] over these monoid objects are equivalent to the corresponding [[modules over monoidal functors]].

=--

This is stated in some form in ([Day 70, example 3.2.2](#Day70)). It was highlighted again in ([MMSS 00, prop. 22.1](#MMSS00)). See also MO discussion [here](http://mathoverflow.net/a/130619/381).

+-- {: .proof}
###### Proof

A [[lax monoidal functor]] $F \colon \mathcal{C} \to V$ is given by [[natural transformations]]

$$
  I_V \longrightarrow F(I_{\mathcal{C}})
$$

$$
  F(c_1) \otimes_V F(c_2) \longrightarrow F(c_1 \otimes_{\mathcal{C}} c_2)
$$

satisfying compatibility conditions. Under the [[natural isomorphism]] of corollary \ref{DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor} these are identified with natural transformations

$$
  y(I) \to F
$$

$$
  F \otimes_{Day} F \longrightarrow F
$$

satisfying analogous conditions. This is just the structure of a [[monoid object]] on $F$ under $\otimes_{Day}$.

Similarly for [[module objects]] and [[modules over monoidal functors]].

=--


+-- {: .num_example}
###### Example

In the case that $V$ is [[pointed topological spaces]] or pointed [[simplicial sets]] equipped with the [[smash product]] of [[pointed objects]] and that $\mathcal{C}$ is a diagram category for [[spectra]], then monoids in prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} are known as [[ring spectra]] and the [[lax monoidal functors]] in prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} are known as the incarnation of ring spectra as "[[functors with smash product]]".

=--

([MMSS 00, section 22](#MMSS00)).

### Modules with respect to Day convolution
 {#Modules}

+-- {: .num_defn #FreeModulesOverAMonoidInDayConvolution}
###### Definition

For $(\mathcal{C},\otimes, I)$ a [[small category|small]] [[monoidal category|monoidal]] $V$-[[enriched category]], and for $R \in Mon([\mathcal{C}, V],\otimes_{Day})$ a [[monoid object]] with respect to [[Day convolution]] over $\mathcal{C}$, write

$$
  R FreeMod \hookrightarrow R Mod
$$

for the [[full subcategory]] of the [[category of modules]] over $R$ on those that are [[free modules]]. Hence the [[objects]] of $R FreeMod$ are those of $\mathcal{C}$ and the [[hom-objects]] are

$$
    R FreeMod(c_1,c_2)
      \;\coloneqq\;
    R Mod( y(c_1) \otimes_{Day} R , y(c_2) \otimes_{Day} R)
  \,.
$$

=--

+-- {: .num_prop #ModulesInDayConvolutionAreFunctorsOnFreeModulesOp}
###### Proposition

For $(\mathcal{C},\otimes, I)$ a [[small category|small]] $V$-[[enriched category]], and for $R \in Mon([\mathcal{C}, V],\otimes_{Day})$ a [[monoid object]] with respect to [[Day convolution]] over $\mathcal{C}$, then there is an [[equivalence of categories]]

$$
  Mod_R \simeq [R FreeMod^{op}, V]
$$

between the [[category of modules|category of right modules]] over $R$ and the [[enriched functor category]] out of the [[opposite category]] of that of free $R$-modules from def. \ref{FreeModulesOverAMonoidInDayConvolution}.

=--

([MMSS 00, theorem 2.2](#MMSS00))

+-- {: .proof}
###### Proof idea

First observe that the hom-objects in $R FreeMod$ are equivalently rewritten as follows

$$
  \begin{aligned}
    R FreeMod(c_2,c_1)
      & =
    R Mod( y(c_2) \otimes_{Day} R , y(c_1) \otimes_{Day} R)
    \\
      & \simeq
    [\mathcal{C},V](y(c_2), y(c_1) \otimes_{Day} R)
    \\
      & \simeq
    (y(c_1) \otimes_{Day} R)(c_2)
    \\
      & \simeq
     \overset{c_3,c_4}{\int}
       \mathcal{C}(c_3 \otimes c_4,c_2)
         \otimes_V
       \mathcal{C}(c_1, c_3) \otimes_V R(c_4)
     \\
     & \simeq 
     \overset{c_4}{\int}
       \mathcal{C}(c_1 \otimes c_4,c_2)
       \otimes_V R(c_4)
  \end{aligned}
  \,.
$$

Then use the identification from prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} of $R$ with a [[lax monoidal functor]] and of any $R$-[[module object]] $N$ as a functor with the structure of a [[module over a monoidal functor]], given by [[natural transformations]]

$$
  N(c_1) \otimes R(c_2) \longrightarrow N(c_1 \otimes c_2)
  \,.
$$

Notice that these transformations have just the same structure as those of the [[enriched functor|enriched functoriality]] of $N$ of the form

$$
  \mathcal{C}(c_1,c_2) \otimes N(c_1) \longrightarrow N(c_2)
  \,.
$$

Hence we may unify these two kinds of transformations into a single kind of the form

$$
   \mathcal{C}(c_1 \otimes c_4, c_2) 
        \otimes 
      R(c_4)
      \otimes
    N(c_1)   
      \longrightarrow
    \mathcal{C}(c_1 \otimes c_4, c_2) 
      \otimes
    N(c_1 \otimes c_4)    
      \longrightarrow
    N(c_2)
$$

and subject to certain identifications.

It remains to see that this identification is compatible with the various conditions.

=--



 

## Examples

+-- {: .num_example}
###### Example

Let $C$ be a [[discrete category]] over a set, which is hence a [[monoid]] (for instance a [[group]]) with product $\cdot$. 

Then the Day convolution product is

$$
  F \star G : e \mapsto \oplus_{c \cdot d = e} F(c) \times G(d)
  \,.
$$

Notice that if we regard the presheaves $F$ and $G$ here, assuming they take values in finite sets, as [[vertical categorification|categorifications]] of $\mathbb{N}$-valued functions $|F|, |G| : C \to \mathbb{N}$, where $|\cdot| : Set \to \mathbb{N}$ is the cardinality operation on finite sets, then this reproduces precisely the ordinary convolution product of these $\mathbb{N}$-valued functions

$$
  \begin{aligned}
    |F \star G| : e &\mapsto 
       \sum_{c,d \in C}
        |F(c)| \times |G(d)| \times \delta(e, c \otimes d)       
       & =
       \sum_{c \cdot d = e} |F(c)| \cdot |F(d)|
  \end{aligned}
$$

This uses in particular that for every object $c \in C$ the functor

$$
  Hom_C(c,-) = \delta_c
$$

is in this sense the Kronecker delta-function on the set $C$ supported at $c \in C$. Precisely because by assumption $C$ has only identity morphisms.

$$
 Hom_C(c,d) = \left\{ \array{
   * & if c = d
   \\
   \emptyset & if c \neq d
 } \right.
$$


=--

Further examples:

* There is an obvious monoidal structure on the [[cube category]]. By Day convolution this induces a monoidal structure on [[cubical set|cubical sets]]. This in turn induces a monoidal structure on [[strict omega-category|strict omega-categories]].

* There is a monoidal structure on the [[augmented simplex category]] which by Day convolution induces a monoidal structure on the category of [[augmented simplicial sets]], which by restriction induces the [[join of simplicial sets|join operation]] on [[simplicial sets]].

* If $C$ is a [[large category]] in one [[universe]], then its [[universe enlargement]] to a bigger universe can be given a closed monoidal structure via Day convolution.

* The [[semantics]] of [[linear logic]] obtained from Girard's "phase spaces", or more generally from [[ternary frames]], is essentially Day convolution for [[posets]].


+-- {: .num_example #SymmetricSmashProductOfSpectra}
###### Example

The [[symmetric smash product of spectra]] on, in particular,  [[symmetric spectra]] and  [[orthogonal spectra]] is the Day convolution product for [[Top]]-[[enriched functors]] on monoidal categories of [[symmetric groups]] of [[orthogonal groups]], respectively ([MMSS 00, theorem 1.7 and section 21.](#MMSS00)).

Similarly the [[symmetric smash product of spectra]] on the [[model structure for excisive functors]] is Day convolution for [[sSet]]-[[enriched functors]] on the plain [[smash product]] of finite pointed [[simplicial sets]] ([Lydakis 98](#Lydakis98)).

See also at _[[functor with smash products]]_.

=--

## Related concepts

* [[monoidal topos]]

## References
 {#References}

The concept originates in

* {#Day70} [[Brian Day]], _On closed categories of functors_, Reports of the Midwest Category Seminar IV, Lecture Notes in Mathematics Vol. 137. Springer-Verlag, 1970, pp 1-38 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/DayReport.pdf))

General discussion includes

* [[Todd Trimble]] on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

The application of Day convolution to the construction of [[symmetric smash products of spectra]] for [[highly structured spectra]] is due to

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

and for [[excisive functors]] due to

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))



(see also at [[functors with smash product]]).


Day convolution for [[(∞,1)-categories]] is discussed in

* Saul Glasman, _Day convolution for infinity-categories_ ([arXiv:1308.4940](http://arxiv.org/abs/1308.4940))


[[!redirects Day convolutions]]

[[!redirects day convolution]]


[[!redirects Day tensor product]]
[[!redirects Day tensor products]]

[[!redirects Day convolution product]]
[[!redirects Day convolution products]]