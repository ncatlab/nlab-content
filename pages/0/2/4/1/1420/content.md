+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categories of categories
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

$Pos$ (or $Poset$ or $Posets$) is the [[category]] whose [[objects]] are [[posets]] and whose [[morphisms]] are monotone (weakly increasing) maps.

Since posets can be identified with [[(0,1)-categories]], $Pos$ can be identified with the full subcategory of [[Cat]] spanned by these; thus it might also be called $(0,1)Cat$.

## Properties

The [[hom-sets]] of $Pos$ themselves have the structure of posets, because $Pos$ is a [[cartesian closed category]]. This means $Pos$ is a [[2-poset]] (aka $(1,2)$-category) or [[locally posetal 2-category]].  If [[Set]] is the primordial example of a [[category]] and [[Cat]] is the primordial example of a [[2-category]], then $Pos$ is the primordial example of a $2$-poset. 

The category $Pos$ is a [[locally presentable category]]. This implies it is [[complete category|complete]] and [[cocomplete category|cocomplete]]. This can also be seen by viewing $Pos$ as a [[reflective subcategory]] of [[PreOrd]] (see [[posetal reflection]]), which is [[topological functor|topological]] over $Set$ and therefore cocomplete. 

We may illustrate the latter point of view by showing how to construct coequalizers in $Pos$. Concretely, to form the coequalizer of a pair of poset maps $f, g: X \rightrightarrows Y$, one first takes their coequalizer $q: Y \to Z$ in $Set$, and endows $Z$ with the smallest reflexive transitive relation that makes $q$ order-preserving. This makes $Z$ a [[preorder]]; it is the coequalizer of $f, g$ in $PreOrd$. Then one passes to the poset [[reflective subcategory|reflection]] of this preorder (i.e., identifying $z$ and $z'$ in $Z$ if $z \leq z'$ and $z' \leq z$) to form the coequalizer in $Pos$. 

## Related categories

* [[Set]]

* [[Grpd]], [[∞Grpd]]

* [[Cat]], [[(∞,1)Cat]]

* [[(∞,n)Cat]]

[[!redirects Poset]]
[[!redirects Posets]]
[[!redirects category of posets]]
[[!redirects (0,1)Cat]]
[[!redirects (0,1)-Cat]]

category: category