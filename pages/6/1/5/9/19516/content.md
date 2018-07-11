
> under construction

#Contents#
* table of contents
{:toc}

## Idea

The concept of [[adjoint triples]] generalized form [[adjoint functors]] to [[Quillen adjunctions]].

## Definition

A _Quillen adjoint triple_ may be defined to be:

1. a [[pair]] of [[Quillen adjunction]] 

   $\mathcal{C}_1 \underoverset{\underset{\phantom{AA}C_1\phantom{AA}}{\longrightarrow}}{\overset{L}{\longleftarrow}}{\bot_{Qu}} \mathcal{D}_1$

   and

   $\mathcal{D}_2 \underoverset{\underset{R}{\longrightarrow}}{\overset{\phantom{AA}C_2\phantom{AA}}{\longleftarrow}}{\bot_{Qu}} \mathcal{C}_2$

1. a [[pair]] of [[Quillen equivalences]]

   $$
     \mathcal{C}_2 
       \underoverset
         {\underset{\phantom{AAAA}}{\longrightarrow}}
         {\overset{}{\longleftarrow}}
         {\simeq_{Qu}}
     \mathcal{C}_1
   $$

   $$
     \mathcal{D}_2 
       \underoverset
         {\underset{\phantom{AAAAA}}{\longrightarrow}}
         {\overset{}{\longleftarrow}}
         {\simeq_{Qu}}
     \mathcal{D}_1
   $$

1. a [[natural isomorphism]] 

   $$
     \array{
       Ho(\mathcal{C}_1)
         &\overset{\mathbb{R}C_1}{\longrightarrow}&
       Ho(\mathcal{D}_1)
       \\
       \big\downarrow\mathrlap{\simeq}
       & \swArrow &
       \big\downarrow\mathrlap{\simeq}
       \\
       Ho(\mathcal{C}_2)
         &\underset{\mathbb{L}C_2}{\longrightarrow}&
       Ho(\mathcal{D}_2)      
     }
   $$

   between [[derived functors]] on [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)). 

By essential uniqueness of ordinary adjoints, this implies that the two derived adjunctions on [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) combine to an ordinary [[adjoint triple]]

$$
  Ho(\mathcal{C})
  \;
    \array{
      \overset{\phantom{AA}\mathbb{L}L\phantom{AA}}{\longleftarrow}
      \\
      \overset{\mathbb{R}C_1 \simeq \mathbb{L}C_2}{\longrightarrow}
      \\
      \overset{\phantom{AA}\mathbb{R}R\phantom{AA}}{\longleftarrow}
    }
  \;
  Ho(\mathcal{D})
$$

If $\mathcal{C}$ and $\mathcal{D}$ are equipped with the structure of [[simplicial model categories]] with $\mathcal{C}^\circ$ and $\mathcal{D}^\circ$ denoting their [[full subcategories|full]] [[Kan complex]]-[[enriched category|enriched]] subcategories on the fibrant-and-cofibrant object, we should say that a _simplicial Quillen adjoint triple_ are [[simplicial Quillen adjunctions]], as above, together with an [[enriched natural transformation]]

   $$
     \array{
       \mathcal{C}^\circ_1
         &\overset{\mathbb{R}C_1}{\longrightarrow}&
       \mathcal{D}^\circ_1
       \\
       {}^{\mathllap{\simeq}}\big\downarrow
       & \swArrow &
       \big\downarrow\mathrlap{}^{\simeq}
       \\
       \mathcal{C}^\circ_2
         &\underset{\mathbb{L}C_2}{\longrightarrow}&
       \mathcal{D}^\circ_2      
     }
   $$

whose components are [[homotopy equivalences]].


## Examples 


+-- {: .num_example #HomotopyLimitQuillenAdjointTriple}
###### Example
**([[Quillen adjoint triple]] of [[homotopy limits]]/[[homotopy colimits|colimits]] of [[simplicial sets]])**

Let $\mathcal{C}$ be a [[small category]], and write $[\mathcal{C}^{op}, sSet_{Qu}]_{proj/inj}$ for the projective/injective [[model structure on simplicial presheaves]] over $\mathcal{C}$, which participate in a [[Quillen equivalence]] of the form 

$$
  [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
    \underoverset
      {\underset{\phantom{AA}id\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}id\phantom{AA}}{\longleftarrow}}
      {\simeq_{Qu}}
  [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
$$

(by [this Prop.](geometry+of+physics+--+categories+and+toposes#ModelCategoriesOfSimplicialPresheaves)).

Moreover, the [[constant functor|constant diagram]]-assigning functor

$$
  [\mathcal{C}^{op}, sSet_{Qu}] \overset{const}{\longleftarrow} sSet_{Qu}
$$

is clearly a [[left Quillen functor]] for the injective model structure, and a [[right Quillen functor]] for the projective model structure.

Therefore we have a Quillen adjoint triple of the form

$$
  \array{
    [\mathcal{C}^{op}, sSet_{Qu}]_{proj}
      &
      \underoverset
        {\underset{\phantom{AA}const\phantom{AA}}{\longleftarrow}}
        {\overset{ \underset{\longrightarrow}{\lim} }{\longrightarrow}}
        {\bot_{Qu}}
      &
    sSet_{Qu}
    \\
    {}^{\mathllap{id}}\Big\downarrow {}^{\underset{Qu}{\simeq}} \Big\uparrow{}^{\mathrlap{id}}
    &&
    {}^{\mathllap{id}}\Big\downarrow {}^{\underset{Qu}{\simeq}}\Big\uparrow{}^{\mathrlap{id}}
    \\
    [\mathcal{C}^{op}, sSet_{Qu}]_{inj}
      &
      \underoverset
        {\underset{ \underset{\longleftarrow}{\lim} }{\longrightarrow}}
        {\overset{\phantom{AA}const\phantom{AA}}{\longleftarrow}}
        {\bot_{Qu}}
      &
    sSet_{Qu}
  }  
$$

The induced [[adjoint triple]] of [[derived functors]] on the [[homotopy category of a model category|homotopy categories]] (via [this Prop.](geometry+of+physics+--+categories+and+toposes#QuillenAdjunctionInducesAdjunctionOnHomotopyCategories)) is the [[homotopy colimit]]/[[homotopy limit]] adjoint triple

$$
  Ho([\mathcal{C}^{op}, sSet])
  \;
    \array{
       \overset{\phantom{AA}\mathbb{L}\underset{\longrightarrow}{\lim}\phantom{AA}}{\longrightarrow}
       \\
       \overset{\phantom{AA}const\phantom{AA}}{\longleftarrow}
       \\
       \overset{\phantom{AA}\mathbb{R}\underset{\longleftarrow}{\lim}\phantom{AA}}{\longrightarrow}
    }
  \;
  Ho(sSet)
$$ 

=--

[[!redirects Quillen adjoint triples]]

[[!redirects Quillen adjoint quadruple]]
[[!redirects Quillen adjoint quadruples]]

