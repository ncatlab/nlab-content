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

The [[category of functors]] on a [[monoidal category]] canonically inherits itself a monoidal category structure via a [[categorification|categorified]] [[convolution product]]. This holds generally in the context of [[enriched category theory]]. This was first observed by ([Day 70](#Day70)) and accordingly these monoidal structures are called _Day convolution_ products.

In more detail, just as there is [[convolution]] of  [[functions]] $f : G \to \mathbb{C}$ whenever $G$ carries the structure of a  [[group]], or more generally just the structure of a [[monoid]], so there is convolution of  [[functors]] $f \colon  \mathcal{G} \to Set$ whenever the [[category]] $\mathcal{G}$ carries the structure of a [[monoidal category]].  

This may be generalized by replacing [[Set]] with a more general [[cocomplete category|cocomplete]] [[symmetric monoidal category]] $V$. The technical condition is that the [[tensor product]] $u \otimes v$ preserves [[colimits]] in its two arguments separately; hence that the functors $u \otimes -$ and $- \otimes v$ preserve colimits. This occurs notably when $V$ is symmetric [[closed monoidal category|closed monoidal]] (so that these functors are [[left adjoints]]). 

## Definition

### For monoidal categories
 {#ForMonoidalCategories}

Let $V$ be a [[closed monoidal category|closed]] [[symmetric monoidal category]] with all small [[limits]] and [[colimits]].

For $\mathcal{C}$ a  $V$-[[enriched category]], write $[\mathcal{C},V]$ for the $V$-[[enriched functor category]] to $V$, etc.

We discuss two equivalent ways of defining Day convolution

1. _[In terms of coends](#InTermsOfCoends)_

1. _[In terms of profunctors](#InTermsOfProfunctors)_

#### In terms of coends
 {#InTermsOfCoends}

+-- {: .num_defn #TopologicalDayConvolutionProduct}
###### Definition

Let $(\mathcal{C}, \otimes, 1)$ be a [[small category|small]] $V$-enriched monoidal category.

Then the **Day convolution tensor product** on $[\mathcal{C},V]$ 

$$
  \otimes_{Day} 
    \;\colon\; 
  [\mathcal{C},V] \times [\mathcal{C},V] 
    \longrightarrow 
  [\mathcal{C},V]
$$

is given by the following [[coend]] 

$$
  X \otimes_{Day} Y
    \;\colon\;
  c 
    \;\mapsto\;
  \overset{(c_1,c_2)\in \mathcal{C}\times \mathcal{C}}{\int}
    \mathcal{C}(c_1 \otimes c_2, c) \otimes_V X(c_1) \otimes_V Y(c_2)
  \,.
$$

=--

We observe now that [[Day convolution]] is equivalently a [[left Kan extension]]. This will be key for understanding [[monoids]] and [[modules]] with respect to Day convolution.

+-- {: .num_defn #ExternalTensorProduct}
###### Definition

Let $\mathcal{C}$ be a [[small category|small]] $V$-monoidal category. Its **[[external tensor product]]** is 

$$
  \overline{\otimes} 
   \;\colon\; 
  [\mathcal{C}, V] 
    \times 
  [\mathcal{C}, V] 
    \longrightarrow 
  [\mathcal{C}\times \mathcal{C}, V]
$$

given by 

$$
  X \overline{\otimes} Y  
    \;\coloneqq\; 
  \otimes_V \circ (X,Y)
  \,,
$$

i.e.

$$
  (X \overline\otimes Y)(c_1,c_2)
  =
  X(c_1)\otimes_V Y(c_2)
  \,.
$$

=--


+-- {: .num_prop #DayConvolutionViaKanExtensionOfExternalTensorAlongTensor}
###### Proposition

The [[Day convolution]] product (def. \ref{TopologicalDayConvolutionProduct}) of two functors is equivalently the [[left Kan extension]] of their external tensor product (def. \ref{ExternalTensorProduct}) along the tensor product $\otimes_{\mathcal{C}}$: there is a [[natural isomorphism]]

$$
  X \otimes_{Day} Y
  \simeq
  Lan_{\otimes_{\mathcal{C}}} (X \overline{\otimes} Y)
  \,.
$$

Hence the [[adjunction unit]] is a [[natural transformation]] of the form

$$
  \array{
    \mathcal{C} \times \mathcal{C}
    &&
      \overset{X \overline{\otimes} Y}{\longrightarrow}
    &&
      V
    \\
    & {}^{\mathllap{\otimes}}\searrow 
     &\Downarrow&
    \nearrow_{\mathrlap{X \otimes_{Day} Y}}
    \\
    && \mathcal{C}
  }
  \,.
$$

=--

This perspective is highlighted in ([MMSS 00, p. 60](#MMSS00)).

+-- {: .proof}
###### Proof

By prop. \ref{TopologicalLeftKanExtensionBCoend} we may compute the left Kan extension as the following [[coend]]:

$$
  \begin{aligned}
     Lan_{\otimes_{\mathcal{C}}} (X\overline{\otimes} Y)(c)
     &
     \simeq
      \overset{(c_1,c_2)}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c )
      \wedge
      (X\overline{\otimes}Y)(c_1,c_2)
     \\
    & =
    \overset{(c_1,c_2)}{\int}
    \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_2, c) 
    \wedge
     X(c_1) \otimes_V Y(c_2) 
  \end{aligned} 
  \,.
$$


=--

Proposition \ref{DayConvolutionViaKanExtensionOfExternalTensorAlongTensor} implies the following fact, which is the key for the identification of "[[functors with smash product]]".

+-- {: .num_cor #DayConvolutionViaNaturalIsosInvolvingExternalTensorAndTensor}
###### Corollary

The operation of [[Day convolution]] $\otimes_{Day}$ (def. \ref{TopologicalDayConvolutionProduct}) is universally characterized by the property that there are [[natural isomorphisms]]

$$
  [\mathcal{C}, V](X \otimes_{Day} Y, Z) 
    \simeq 
  [\mathcal{C}\times \mathcal{C}, V](
    X \overline{\otimes} Y,\; Z \circ \otimes_C
  )
  \,,
$$

where $\overline{\otimes}$ is the external product of def. \ref{ExternalTensorProduct}.

=--





#### In terms of profunctors
 {#InTermsOfProfunctors}

The Day convolution can also be expressed in terms of [[profunctors]].  The tensor product $\otimes :\mathcal{C}\otimes \mathcal{C}\to \mathcal{C}$ induces a representable profunctor $\mathcal{C}(\otimes,1): \mathcal{C} &#8696; \mathcal{C}\otimes \mathcal{C}$.  The above definition can be interpreted to say that if $X,Y\in [\mathcal{C},V]$ are regarded as profunctors $\mathcal{C} &#8696; I$, where $I$ is the unit $V$-category, then $X\otimes_{Day} Y$ is the composite of profunctors
$$ \mathcal{C} \xrightarrow{\mathcal{C}(\otimes,1)} \mathcal{C}\otimes \mathcal{C} \xrightarrow{X\otimes Y} I\otimes I \cong I. $$
A more "global" way to say the same thing is to consider the "evaluation" functor $[\mathcal{C},V] \otimes \mathcal{C} \to V$ to be a profunctor $E:\mathcal{C}&#8696;[\mathcal{C},V]^{op}$.  Then the profunctor composite
$$ \mathcal{C} \xrightarrow{\mathcal{C}(\otimes,1)} \mathcal{C}\otimes \mathcal{C} \xrightarrow{E\otimes E} [\mathcal{C},V]^{op} \otimes [\mathcal{C},V]^{op}$$
is a functor $\mathcal{C}\otimes [\mathcal{C},V] \otimes [\mathcal{C},V] \to V$, which by exponential transpose gives a functor $[\mathcal{C},V] \otimes [\mathcal{C},V] \to [\mathcal{C},V]$; this is the Day convolution product.


### For promonoidal categories

The [above](#InTermsOfProfunctors) description in terms of profunctors makes it clear that the construction only depends on the representable profunctor induced by $\otimes : \mathcal{C}\otimes \mathcal{C}\to \mathcal{C}$, i.e. on the underlying [[promonoidal category]] of $\mathcal{C}$.  In the original article ([Day 70](#Day70)), a stronger form of the convolution is discussed, in which $\mathcal{C}$ is assumed only to be a [[promonoidal category]].

Before continuing our discussion, we comment a bit on a convention adopted in [(Day's thesis)](#Day70Thesis). To define [[promonoidal structures]], Day used functors of the form $P\colon\mathcal{A}^\mathrm{op}\times\mathcal{A}^\mathrm{op}\times\mathcal{A}$, whereas the nLab convention is that a [[profunctor]] $P\colon\mathcal{A}\times\mathcal{A}$⇸$\mathcal{A}$ is a functor $P\colon\mathcal{A}^\mathrm{op}\times\mathcal{A}\times\mathcal{A}$. Following modern usage and [(Corner 2016)](#Corner2016), instead of defining Day convolution for $\mathcal{V}$-[[enriched functors]], we do so for $\mathcal{V}$-presheaves.

Let $\mathcal{V}$ be a [[Bénabou cosmos]], $(\mathcal{C},P,I,\lambda,\rho,\alpha)$ be a small $\mathcal{V}$-[[enriched category]] equipped with the structure of a [[promonoidal category]], and write $P^A_{B,C}$ for $P(A,B,C)$ (this is called the Einstein notation for profunctors; see ([Loregian 2019, Definition 5.1.10](#Fosco))).

+-- {: .num_defn #DayConvolutionForPromonoidalCategories}
###### Definition

The **Day convolution tensor product** on $[\mathcal{C}^\mathsf{op},\mathcal{V}]$ is the bifunctor

$$\otimes_{Day}\colon[\mathcal{C}^\mathsf{op},\mathcal{V}]\times[\mathcal{C}^\mathsf{op},\mathcal{V}]\longrightarrow[\mathcal{C}^\mathsf{op},\mathcal{V}]$$

defined on objects by the [[coend]] 

$$F\otimes_{Day}G=\overset{A,B\in\mathcal{C}}{\int}F(A)\otimes_V G(B)\otimes_V P^{(-)}_{A,B}.$$

=--

+-- {: .num_prop}
###### Proposition

There is an [[equivalence of categories]] between the category of [[pro-monoidal structures]] on $\mathcal{C}$ with strong pro-monoidal functors between them and the category of biclosed monoidal structures on $[\mathcal{C}^{op},V]$ with [[strong monoidal functors]] between them.

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

This may be deduced fairly abstractly from the [above](#InTermsOfProfunctors) description of Day convolution in terms of profunctors, using the associativity of the promonoidal structure on $\mathcal{C}$.  


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

or equivalently by the end

$$ [X,Y]_{Day}(c) = \int_{c_1} V\left(X(c_1),Y(c\otimes c_1)\right) $$

=--

+-- {: .proof}
###### Proof

First note that the equivalence between the two formulas follows from the [[Yoneda lemma]].  (We mention them both, even though the second is undoubtedly simpler, because the more general case of a promonoidal $\mathcal{C}$ this simplification is unavailable.)

In analogy to the cartesian [[closed monoidal structure on presheaves]]
we see that if the [[internal hom]] in $[\mathcal{C},V]$ exists at all, 
(with $[X,-]_{Day}$ [[right adjoint]] to $(-) \otimes_{Day} X$) then by the [[enriched Yoneda lemma]] and by the [[end]]-expression for the [[hom-objects]] in the [[enriched functor category]] $[\mathcal{C},V]$ it has to be given by

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
    \underset{c_1}{\int} V((y(c) \otimes_{Day} X)(c_1), Y(c_1))
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

In functional programming, these monoids give rise to the notion of Applicative.

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
  R Free_{\mathcal{C}}Mod \hookrightarrow R Mod
$$

for the [[full subcategory]] of the [[category of modules]] over $R$ on those that are [[free modules]] and moreover free on objects in $\mathcal{C}$ (under the [[Yoneda embedding]]). Hence the [[objects]] of $R Free_{\mathcal{C}}Mod$ are those of $\mathcal{C}$ and the [[hom-objects]] are

$$
    R Free_{\mathcal{C}}Mod(c_1,c_2)
      \;\coloneqq\;
    R Mod( y(c_1) \otimes_{Day} R , y(c_2) \otimes_{Day} R)
  \,.
$$

=--

+-- {: .num_prop #ModulesInDayConvolutionAreFunctorsOnFreeModulesOp}
###### Proposition

For $(\mathcal{C},\otimes, I)$ a [[small category|small]] $V$-[[enriched category]], and for $R \in Mon([\mathcal{C}, V],\otimes_{Day})$ a [[monoid object]] with respect to [[Day convolution]] over $\mathcal{C}$, then there is an [[equivalence of categories]]

$$
  Mod_R \simeq [R Free_{\mathcal{C}}Mod^{op}, V]
$$

between the [[category of modules|category of right modules]] over $R$ and the [[enriched functor category]] out of the [[opposite category]] of that of free $R$-modules from def. \ref{FreeModulesOverAMonoidInDayConvolution}.

=--

([MMSS 00, theorem 2.2](#MMSS00))

+-- {: .proof}
###### Proof idea


Use the identification from prop. \ref{DayMonoidsAreLaxMonoidalFunctorsOnTheSite} of $R$ with a [[lax monoidal functor]] and of any $R$-[[module object]] $N$ as a functor with the structure of a [[module over a monoidal functor]], given by [[natural transformations]]

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

Now observe that the hom-objects of $R Free_{\mathcal{C}}Mod$ (def. \ref{FreeModulesOverAMonoidInDayConvolution}) have just this structure:

$$
  \begin{aligned}
    R Free_{\mathcal{C}}Mod(c_2,c_1)
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

We claim that under this identification, composition in $R Free_{\mathcal{C}}Mod$ is given by

$$
  \begin{aligned}
    R Free_{\mathcal{C}}Mod(c_2, c_1) \otimes_V R Free_{\mathcal{C}}Mod(c_3, c_2)
    & =
    \left(
    \overset{c_4}{\int} \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4, c_2)     
     \otimes_V R(c_4)
    \right)
      \otimes_V
    \left(
    \overset{c_5}{\int} \mathcal{C}(c_2 \otimes_{\mathcal{C}} c_5, c_3 )
     \otimes_V R(c_5)
    \right)
    \\
    & \simeq
    \overset{c_4, c_5}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4  , c_2  )
        \otimes_V 
      \mathcal{C}(c_2 \otimes_{\mathcal{C}} c_5, c_3)
        \otimes_V
      R(c_4) \otimes_V R(c_5)
    \\
    & \longrightarrow
      \overset{c_4,c_5}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4 \otimes_{\mathcal{C}}  c_5 , c_2 \otimes_{\mathcal{C}} c_5  )
        \otimes_V 
      \mathcal{C}(c_2 \otimes c_5, c_3)
        \otimes_V
      R(c_4 \otimes_{\mathcal{C}} c_5 )
     \\
     & \longrightarrow
      \overset{c_4, c_5}{\int} 
      \mathcal{C}(c_1\otimes_{\mathcal{C}} c_4 \otimes_{\mathcal{C}} c_5 , c_3)
        \otimes_V
      R(c_4 \otimes_{\mathcal{C}} c_5 )
     \\
     & \longrightarrow
      \overset{c_4}{\int} 
      \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4 , c_3)
        \otimes_V
      R(c_4 )
  \end{aligned}
  \,,
$$

where

1. the first morphism is, in the integrand, the tensor product of 

   1. forming the tensor product of hom-objects of $\mathcal{C}$ with the identity of $c_5$

      $$
        \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4, c_2 ) \simeq 
       \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4, c_2 ) \otimes_V 1_V
       \overset{}{\longrightarrow}
       \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4, c_2 ) \otimes \mathcal{C}(c_5,c_5)
       \longrightarrow
       \mathcal{C}(c_1 \otimes_{\mathcal{C}} c_4 \otimes_{\mathcal{C}} c_5, c_2 \otimes_{\mathcal{C}} c_5)
      $$

   1. the monoidal functor incarnation $R(c_4) \otimes_V R(c_5)\longrightarrow R(c_4 \otimes_{\mathcal{C}} c_5 )$ of the monoid structure on $R$;

1. the second morphism is, in the integrand, given by composition in $\mathcal{C}$;

1. the last morphism is the morphism induced on [[coends]] by regarding [[extranatural transformation|extranaturality]] in $c_4$ and $c_5$ separately as a special case of extranaturality in $c_6 \coloneqq c_4 \otimes c_5$ (and then renaming).

It is fairly straightforward to see that, under the above identifications, functoriality under this composition is equivalently functoriality in $\mathcal{C}$ together with the action property over $R$.


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

* {#Day70} [[Brian Day]], _On closed categories of functors_, Reports of the Midwest Category Seminar IV, Lecture Notes in Mathematics Vol. 137. Springer-Verlag, 1970, pp 1-38 ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/DayReport.pdf)),

as well as in Day's thesis

* {#Day70Thesis} [[Brian Day]], _Construction of Biclosed Categories_, PhD thesis. School of Mathematics of the University of New South Wales, September 1970. [Link](http://unsworks.unsw.edu.au/fapi/datastream/unsworks:58748/SOURCE01?view=true).

(Note that some unproven statements in [(Day's report)](#Day70) are proved in [(Day's thesis)](#Day70Thesis) and vice versa.)

The universal property of the Day convolution, in the sense of free monoidal cocompletion, is discussed in

* Geun  Bin Im and G. M. Kelly, _A universal property of the convolution monoidal structure_, J. Pure Appl. Algebra 43 (1986), no. 1, 75-88.

General discussion includes

* [[Todd Trimble]] on Day convolution [here](http://golem.ph.utexas.edu/category/2008/01/the_concept_of_a_space_of_stat.html#c014365)

The application of Day convolution to the construction of [[symmetric smash products of spectra]] for [[highly structured spectra]] is due to

* {#MMSS00} [[Michael Mandell]], [[Peter May]], [[Stefan Schwede]], [[Brooke Shipley]], _[[Model categories of diagram spectra]]_, Proceedings London Mathematical Society Volume 82, Issue 2, 2000 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/mmssLMSDec30.pdf), [publisher](http://plms.oxfordjournals.org/content/82/2/441.short?rss=1&ssource=mfc))

and for [[excisive functors]] due to

* {#Lydakis98} Lydakis, _Simplicial functors and stable homotopy theory_ Preprint, available via Hopf archive, 1998 ([pdf](http://hopf.math.purdue.edu/Lydakis/s_functors.pdf))

(see also at [[functors with smash product]]).

Day convolution for [[monoidal bicategories]] is developed in

* {#Corner2016} [[Alexander Corner]], _Day convolution for monoidal bicategories_, School of Mathematics and Statistics of the University of Sheffield. Available through the [White Rose theses database](http://etheses.whiterose.ac.uk/16767/).

Day convolution for [[(∞,1)-categories]] is discussed in

* Saul Glasman, _Day convolution for infinity-categories_ ([arXiv:1308.4940](http://arxiv.org/abs/1308.4940))

Other references cited in this page:

* {#Fosco} [[Fosco Loregian]], _Coend calculus_ ([arXiv](http://arxiv.org/abs/1501.02503)).


[[!redirects Day convolutions]]

[[!redirects day convolution]]


[[!redirects Day tensor product]]
[[!redirects Day tensor products]]

[[!redirects Day convolution product]]
[[!redirects Day convolution products]]