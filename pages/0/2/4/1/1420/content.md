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

$Pos$ is the [[category]] whose [[objects]] are [[posets]] and whose [[morphisms]] are monotone (weakly increasing) maps.

## Properties

The [[hom-sets]] of $Pos$ themselves have the structure of posets, because $Pos$ is a [[cartesian closed category]]. This means $Pos$ is a [[2-poset]] (aka $(1,2)$-category) or [[locally posetal 2-category]].  If [[Set]] is the primordial example of a [[category]] and [[Cat]] is the primordial example of a [[2-category]], then $Pos$ is the primordial example of a $2$-poset. 

The category $Pos$ is [[topological functor|topological]] over $Set$, and is also a [[locally presentable category]]. Either statement implies that it is [[complete category|complete]] and [[cocomplete category|cocomplete]]. As a very special case, it has coequalizers; concretely, to form the coequalizer of a pair of poset maps $f, g: X \rightrightarrows Y$, one first takes their coequalizer $q: Y \to Z$ in $Set$, and endows $Z$ with the smallest reflexive transitive relation that makes $q$ order-preserving. This makes $Z$ a [[preorder]]; then one passes to the poset [[reflective subcategory|reflection]] of this preorder (i.e., identifying $z$ and $z'$ in $Z$ if $z \leq z'$ and $z' \leq z$). 

## Related categories

* [[Set]]

* [[Grpd]], [[∞Grpd]]

* [[Cat]], [[(∞,1)Cat]]

* [[(∞,n)Cat]]


category: category