
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[category]] is called **gaunt** if all its [[isomorphisms]] are in fact [[identities]]. This is a property of [[strict categories]]; that is, it is not [[principle of invariance|invariant]] under [[equivalence of categories]]. See below for some related concepts that are invariant.

## Properties

### Relation to skeletal categories, thin categories, poset categories

Gaunt categories are necessarily [[skeletal]]; a skeletal category is gaunt iff every [[automorphism]] is an [[identity morphism]]. Consequently a [[thin]] gaunt category is skeletal, and since a thin skeletal category is a [[poset category]] a thin gaunt category is also a poset category.

Note that a gaunt category need not be thin, since we may have parallel non-isomorphisms which are not equal. Similarly, a thin category need not be gaunt since we may have isomorphisms that aren't the identity.

### Relation to complete Segal spaces

The [[nerve]] [[simplicial set]] of a [[category]], regarded as a [[simplicial object]] in [[homotopy types]] under the inclusion $Set \hookrightarrow \infty Grpd$, is a _[[complete Segal space]]_ precisely if the category is gaunt. More discussion of this is at _[Segal space -- Examples -- In Set](Segal%20space#InSetByNervesOfCategories)_.

## Related invariant concepts

To make sense of the definition of a gaunt category, we need to use equality of objects: For every isomorphism $f : a \simeq b$, there is an equality $p : a = b$, relative to which $f$ equals the identity at $a$. Replacing the equality $p$ by an isomorphism $g : a \simeq b$, the resulting condition holds for all categories.
This echoes how one might understand the definition in [[univalent foundations]]: the univalence condition for a [[univalent category]] is another way of saying that every isomorphism is an identity (and uniquely so).

Alternatively, we could avoid the equality on objects by requiring only that every endoisomorphism $f : a \simeq a$ be equal to the identity at $a$. This amounts to requiring that the [[core]] be a [[thin category]], i.e., that parallel isomorphisms are equal.

Incidentally, we may view both strict categories and categories up to equivalence as embedded in the type of [[flagged category|flagged categories]]. Recall that a flagged category consists of a category $C$, a groupoid $X$, and a surjection $p:X\to C$ of groupoids from $X$ to the underlying groupoid of objects of $C$. In this way, we can view categories as those flagged categories where $p$ is an equivalence, and strict categories as those flagged categories where $X$ is a set (up to homotopy). The intersection of the categories and the strict categories within the type of flagged categories is then exactly this type of core-thin categories.


## References

The term "gaunt category" was apparently introduced in 

* [[Clark Barwick]], [[Chris Schommer-Pries]], _On the Unicity of the Homotopy Theory of Higher Categories_ ([arXiv:1112.0040](http://arxiv.org/abs/1112.0040), [slides](http://prezi.com/w0ykkhh5mxak/the-uniqueness-of-the-homotopy-theory-of-higher-categories/))
 {#BarwickSchommerPries}

in the context of a discussion of [[(infinity,n)-categories]].

In the [[Elephant]], gaunt categories are briefly mentioned under the name "stiff categories", in the paragraph preceding B1.3.11 (about [[split fibration|splitting]] of [[Grothendieck fibrations]]).


[[!redirects gaunt category]]
[[!redirects gaunt categories]]
[[!redirects stiff category]]
[[!redirects stiff categories]]