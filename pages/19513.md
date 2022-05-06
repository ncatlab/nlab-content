

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The (right) [[derived functor]] of an [[enriched hom-functor]].

## Definition

### For enriched model categories
 {#ForEnrichedModelCategories}

We discuss the definition of the derived hom-functor (Def. \ref{DerivedHomFunctorPOnSimplicialModelCategory} below) for [[enriched model categories]] (recalled as Def. \ref{SimplicialModelCategory} below). The key point is to observe (Lemma  \ref{InSimplicialModelCategoryEnrichedHomIsHomotopical} below) that the axioms on [[enriched model categories]] imply that the ordinary [[enriched hom-functor]] is a [[homotopical functor]] when its first argument is [[cofibrant object|cofibrant]] and its second argument is [[fibrant object|fibrant]], so that its [[right derived functor]] exists.

$\,$

+-- {: .num_defn #SimplicialModelCategory}
###### Definition
**([[enriched model category]])**

Let $\mathcal{V}$ be a [[monoidal model category]]. Then a _$\mathcal{V}$-[[enriched model category]]_ is a [[category]] $\mathcal{C}$  equipped with

1. the [[structure]] of $\mathcal{V}$-[[enriched category]], which is also [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$;

1. the [[structure]] of a [[model category]],

such that these two structures are compatible in the following way:

* for every [[cofibration]] $X \overset{f}{\to} Y$ and every [[fibration]] $A \overset{g}{\to} B$ in $\mathcal{C}$, the induced [[pullback powering]]-morphism of [[hom-objects]] in $\mathcal{V}$

  \[
    \label{SimplicialModelCategoryComparisonMorphism}
    \mathcal{C}(Y,A)
      \longrightarrow
     \mathcal{C}(X,A) 
       \underset{\mathcal{C}(X,B)}{\times}
     \mathcal{C}(Y,B)
  \]

  is a [[fibration]], and is a [[weak equivalence]] as soon as one of the two morphisms is a [[weak equivalence]] in $\mathcal{C}$.

=--


+-- {: .num_lemma #InSimplicialModelCategoryEnrichedHomIsHomotopical}
###### Lemma
**(in [[enriched model category]] the [[enriched hom-functor]] out of [[cofibrant object|cofibrant]] into [[fibrant object|fibrant]] is [[homotopical functor]])**


Let $\mathcal{C}$ be an [[enriched model category]] (Def. \ref{SimplicialModelCategory}). 

If $Y \in \mathcal{C}$ is a [[cofibrant object]], then the [[enriched hom-functor]] out of $Y$

$$
  \mathcal{C}(Y,-)
  \;\colon\; 
  \mathcal{C}
    \longrightarrow
  \mathcal{V}
$$

preserves [[fibrations]] and [[acyclic fibrations]].

If $A \in \mathcal{C}$ is a [[fibrant object]], then the [[enriched hom-functor]] into $A$

$$
  \mathcal{C}(-,A)
  \;\colon\; 
  \mathcal{C}^{op}
    \longrightarrow
  \mathcal{V}
$$

sends [[cofibrations]] and [[acyclic cofibrations]] in $\mathcal{C}$ to fibrations and acyclic fibrations, respectively, in $\mathcal{V}$.

=--

+-- {: .proof}
###### Proof

In the first case, consider the comparison morphism (eq:SimplicialModelCategoryComparisonMorphism) for $X =\emptyset$ the [[initial object]], in the second case consider it for $B = \ast$ the [[terminal object]].

Since $\mathcal{C}$ is [[tensored and cotensored category|tensored and cotensored]] over $\mathcal{V}$, it follows (by [this Prop](powered+and+copowered+category#InTensoredCotensoredCategoryInitialObjectIsEnrichedInitial) that 

$$
  \mathcal{C}(\emptyset, -)
  \;\simeq\;
  \ast
  \phantom{AA}
  \text{and}
  \phantom{AA}
  \mathcal{C}(-,\ast)
  \;\simeq\;
  \ast\;
  \;\;\;
  \in \mathcal{V}
  \,.
$$

This means that in the first case the comparison morphism 
$$
    \mathcal{C}(Y,A)
      \longrightarrow
     \mathcal{C}(X,A) 
       \underset{\mathcal{C}(X,B)}{\times}
     \mathcal{C}(Y,B)
$$
(eq:SimplicialModelCategoryComparisonMorphism) becomes equal to the top morphism in the following diagram 

$$
  \array{
    \mathcal{C}(Y,A)
       &\overset{\mathcal{C}(Y,g)}{\longrightarrow}&
    \mathcal{C}(Y,B)
    \\
    \Big\downarrow
      &&
    \Big\downarrow
    \\
    \ast &\underset{\phantom{AAA}}{\longrightarrow}& \ast
  }
$$

while in the second case it becomes equal to the left morphism in

$$
  \array{
    \mathcal{C}(Y,A)
       &\overset{\phantom{\mathcal{C}(Y,g)}}{\longrightarrow}&
    \ast
    \\
    {}^{\mathllap{ \mathcal{C}(f,A) }}\Big\downarrow
      &&
    \Big\downarrow
    \\
    \mathcal{C}(X,A) 
      &\underset{\phantom{AAA}}{\longrightarrow}& 
    \ast
  }
$$

Hence the claim follows by the defining condition on the comparison morphism (eq:SimplicialModelCategoryComparisonMorphism) in an [[enriched model category]].

=--

+-- {: .num_defn #DerivedHomFunctorPOnSimplicialModelCategory}
###### Definition
**([[derived hom-functor]] of an [[enriched model category]])**

Let $\mathcal{C}$ be an [[enriched model category]] (Def. \ref{SimplicialModelCategory}). 

By Lemma \ref{InSimplicialModelCategoryEnrichedHomIsHomotopical} and by [[Ken Brown's lemma]], the [[enriched hom-functor]] has a [[right derived functor]] ([this Def.](geometry+of+physics+--+categories+and+toposes#LeftAndRightDerivedFunctorsOnModelCategories)) when its first argument is [[cofibrant object|cofibrant]] and its second argument is [[fibrant object|fibrant]]. This is called the _[[derived hom-functor]]_

$$
  \mathbb{R}hom
  \;\colon\;
  Ho(\mathcal{C})^{op} \times Ho(\mathcal{C})
  \longrightarrow
  Ho(\mathcal{V})
$$

In the presence of [[functorial factorization|functorial]] [[cofibrant resolution]] $Q$ and [[fibrant resolution]] $P$ this is given by the ordinary [[enriched hom-functor]] $\mathcal{C}(-,-)$ as

$$
  \mathbb{R}hom(X,Y)
  \;\simeq\;
  \mathcal{C}(Q X, P Y)
  \,.
$$

=--


## Examples

* For [[simplicial model categories]] see _[[derived hom-space]]_.

* For [[categories of chain complexes]] see _[[Ext]]_.

## Related concepts

* [[hom-set]], [[hom-object]]

* [[hom-functor]]

* [[enriched hom-functor]], [[internal hom-functor]]



[[!redirects derived hom-functors]]
