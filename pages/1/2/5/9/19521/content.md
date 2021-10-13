

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition


+-- {: .num_defn #DoubleCategoryOfModelCategories}
###### Definition
**([[double category]] of [[model categories]])**

The ([[very large category|very large]]) _[[double category]] of [[model categories]]_ $ModCat_{dbl}$ has 

1. as [[objects]]: [[model categories]] $\mathcal{C}$;

1. as [[vertical morphisms]]: [[left Quillen functors]] $\mathcal{C} \overset{L}{\longrightarrow} \mathcal{E}$;

1. as [[horizontal morphisms]]: [[right Quillen functors]] $\mathcal{C} \overset{R}{\longrightarrow}\mathcal{D}$;

1. as [[2-morphisms]] [[natural transformations]] between the [[composition|composites]] of underlying [[functors]].

   $$
     L_2\circ R_1
       \overset{\phi}{\Rightarrow}
     R_2\circ L_1
     \phantom{AAAAA}
     \array{
       \mathcal{C}
         &\overset{\phantom{AA}R_1\phantom{AA}}{\longrightarrow}&
       \mathcal{D}
       \\
       {}^{\mathllap{L_1}}\Big\downarrow
       &{}^{\mathllap{ \phi }}\swArrow&
       \Big\downarrow{}^{\mathrlap{L_2}}
       \\
       \mathcal{C}
         &\underset{\phantom{AA}R_2\phantom{AA}}{\longrightarrow}&
       \mathcal{D}
     }
   $$

and [[composition]] is given by ordinary [[composition]] of [[functors]], horizontally and vertically, and by [[whiskering]]-composition of [[natural transformations]].

=--

([Shulman 07, Example 4.6](#Shulman07))

There is hence a [[forgetful functor|forgetful]] [[double functor]]

$$
  F \;\colon\; ModCat_{dbl} \longrightarrow Sq(Cat)
$$

to the [[double category of squares]] in the [[2-category of categories]], which forgets the [[model category]]-[[structure]] and the [[Quillen functor]]-[[property]].

There is also another [[double pseudofunctor]] to $Sq(Cat)$ of interest, this is Prop. \ref{HomotopyDoublePseudofunctor} below.

## Properties

+-- {: .num_prop #HomotopyDoublePseudofunctor}
###### Proposition
**(homotopy [[double pseudofunctor]] on the [[double category of model categories]])**

There is a [[double pseudofunctor]]

$$
  Ho(-) \;\colon\; ModCat_{dbl} \longrightarrow Sq(Cat)
$$

from the double category of model categories (Def. \ref{DoubleCategoryOfModelCategories}) to the [[double category of squares]] in the [[2-category]] [[Cat]], which sends

1. a [[model category]] $\mathcal{C}$ to its [[homotopy category of a model category]];

1. a [[left Quillen functor]] to its [[left derived functor]];

1. a [[right Quillen functor]] to its [[right derived functor]];

1. a [[natural transformation]]

   $$
     \array{
       \mathcal{C}
       &\overset{R_1}{\longrightarrow}&
       \mathcal{D}
       \\
       {}^{\mathllap{L_1}}\Big\downarrow 
         &{}^{\mathllap{ \phi }}\swArrow& 
       \Big\downarrow{}^{\mathrlap{L_2}}
       \\
       \mathcal{E}
       &\underset{R_2}{\longrightarrow}&
       \mathcal{F}  
     }
   $$

   to the "[[derived natural transformation]]"

   $$
     \array{
       Ho(\mathcal{C})
       &\overset{\mathbb{R}R_1}{\longrightarrow}&
       Ho(\mathcal{D})
       \\
       {}^{\mathllap{\mathbb{L}L_1}}\Big\downarrow 
         &\overset{Ho(\phi)}{\swArrow}& 
       \Big\downarrow{}^{\mathrlap{\mathbb{L}L_2}}
       \\
       Ho(\mathcal{E})
       &\underset{\mathbb{R}R_2}{\longrightarrow}&
       Ho(\mathcal{F})  
     }
   $$

   given by the [[zig-zag]]

   \[
     \label{DerivedNaturalTransformation}
     Ho(\phi)
     \;\colon\;
     L_2 Q R_1 P
     \overset{}{\longleftarrow}
     L_2 Q R_1 Q P
     \longrightarrow
     L_2 R_1 Q P 
     \overset{\phi}{\longrightarrow}
     R_2 L_1 Q P 
     \longrightarrow
     R_2 P L1 Q P 
     \longleftarrow
     R_2 R L_1 Q
     \,,
   \]

    where the unlabeled morphisms are induced by [[fibrant resolution]] $c \to P c$ and [[cofibrant resolution]] $Q c \to c$, respectively.

=--

([Shulman 07, Theorem 7.6](#Shulman07))

+-- {: .num_prop #DerivedNaturalTransformationUpToIsos}
###### Proposition
**(recognizing derived natural isomorphisms)**

For the [[derived natural transformation]] $Ho(\phi)$ in (eq:DerivedNaturalTransformation) to be invertible in the [[homotopy category of a model category|homotopy category]], it is sufficient that for every [[object]] $c \in \mathcal{C}$ which is both [[fibrant object|fibrant]] and [[cofibrant object|cofibrant]] the following [[natural transformation]] 

$$
  R_2 Q L_1 c
    \overset{ R_2 p_{L_1 c} }{\longrightarrow}
  R_2 L_1 c
   \overset{\phi}{\longrightarrow}
  L_2 R_1 c
    \overset{ L_2 j_{R_1 c} }{\longrightarrow}
  L_2 P R_1 c  
$$ 

is invertible in the homotopy category, hence that the composite is a [[weak equivalences]] (by [this Prop.](geometry+of+physics+--+categories+and+toposes#MorphismIsWeakEquivalenceIfIsoInHomotopyCategoryForQuillen)).

=--

([Shulman 07, Remark 7.2](#Shulman07))


## Examples

+-- {: .num_example #DerivedFunctorOfLeftRightQuillenFunctor}
###### Example
**([[derived functor]] of left-right [[Quillen functor]])**

Let $\mathcal{C}$, $\mathcal{D}$ be [[model categories]], and let 

$$
  \mathcal{C} \overset{\phantom{A}F\phantom{A}}{\longrightarrow} \mathcal{C}
$$

be a functor that is both a [[left Quillen functor]] as well as a [[right Quillen functor]]. This means equivalently that there is a [[2-morphism]] in the [[double category of model categories]] (Def. \ref{DoubleCategoryOfModelCategories}) of the form

\[
  \label{DoubleMorphismExhibitingLeftRightQuillenFunctor}
  \array{
    \mathcal{C}
      &\overset{\phantom{AA}F\phantom{AA}}{\longrightarrow}&
    \mathcal{D}
    \\
    {}^{\mathllap{F}}\Big\downarrow 
      &{}^{id}\swArrow& 
    \Big\downarrow{}^{\mathrlap{id}}
    \\
    \mathcal{D}
      &\underset{\phantom{A}id\phantom{A}}{\longrightarrow}&
    \mathcal{D}
  }
\]

It follows that the [[left derived functor]] $\mathbb{L}F$ and [[right derived functor]] $\mathbb{R}F$ of $F$ are [[natural isomorphism|naturally isomorphic]]:

$$
  Ho(\mathcal{C})
    \overset{ \mathbb{L}F \simeq \mathbb{R}F }{\longrightarrow}
  Ho(\mathcal{D})
  \,.
$$

=--

([Shulman 07, corollary 7.8](#Shulman07))

+-- {: .proof}
###### Proof

To see the [[natural isomorphism]] $\mathbb{L}F \simeq \mathbb{R}F$: By Prop. \ref{HomotopyDoublePseudofunctor} this is implied once the [[derived natural transformation]] $Ho(id)$ of (eq:DoubleMorphismExhibitingLeftRightQuillenFunctor) is a [[natural isomorphism]]. By Prop. \ref{DerivedNaturalTransformationUpToIsos} this is the case, in the present situation, if the composition of


$$
  Q F c
    \overset{ p_{F c} }{\longrightarrow}
  F c
    \overset{  j_{F c} }{\longrightarrow}
  P F c  
$$ 

is a weak equivalence. But this is immediate, since the two factors are weak equivalences, by definition of [[fibrant resolution|fibrant/cofibrant resolution]].

=--

## Related concepts

* [[2Ho(CombModCat)]]

## References

* {#Shulman07} [[Michael Shulman]], _Comparing composites of left and right derived functors_, New York Journal of Mathematics 17 (2011), 75-125 ([arXiv:0706.2868](https://arxiv.org/abs/0706.2868))

[[!redirects double categories of model categories]]

[[!redirects derived natural transformation]]
[[!redirects derived natural transformations]]
