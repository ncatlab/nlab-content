

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

1. as [[objects]]: [[model categories]];

1. as [[vertical morphisms]]: [[left Quillen functors]];

1. as [[horizontal morphisms]]: [[right Quillen functors]];

1. as [[2-morphisms]] [[natural transformations]] between the [[composition|composites]] of underlying [[functors]].

=--

([Shulman 07, Example 4.6](#Shulman07))

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
         &\swArrow_{\mathrlap{\phi}}& 
       \Big\downarrow{}^{\mathrlap{L_2}}
       \\
       \mathcal{E}
       &\underset{R_2}{\longrightarrow}&
       \mathcal{F}  
     }
   $$

   to the _derived natural transformation_

   $$
     \array{
       Ho(\mathcal{C})
       &\overset{\mathbb{R}R_1}{\longrightarrow}&
       Ho(\mathcal{D})
       \\
       {}^{\mathllap{\mathbb{L}L_1}}\Big\downarrow 
         &\swArrow_{\mathrlap{Ho(\phi)}}& 
       \Big\downarrow{}^{\mathrlap{\mathbb{L}L_2}}
       \\
       Ho(\mathcal{E})
       &\underset{\mathbb{R}R_2}{\longrightarrow}&
       Ho(\mathcal{F})  
     }
   $$

   given by the [[zig-zag]]

   $$
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
   $$

    where the unlabeled morphisms are induced by [[fibrant resolution]] $c \to P c$ and [[cofibrant resolution]] $Q c \to c$, respectively.

=--

([Shulman 07, Theorem 7.6](#Shulman07))

## Related concepts

* [[Ho(CombModCat)]]

## References

* {#Shulman07} [[Michael Shulman]], _Comparing composites of left and right derived functors_, New York Journal of Mathematics 17 (2011), 75-125 ([arXiv:0706.2868](https://arxiv.org/abs/0706.2868))

[[!redirects double categories of model categories]]
