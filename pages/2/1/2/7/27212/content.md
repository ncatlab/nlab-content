+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A **strictification theorem** is a theorem of the form: *every weak structure is suitably equivalent to a semi-strict structure*.

There are typically two varieties of strictification theorems:

1. Every weak structure is weakly equivalent to a semi-strict structure.
1. Every *free* weak structure is weakly equivalent to a *free* semi-strict structure.

For instance, in the case of [[monoidal categories]], the following are true.

1. Every [[monoidal category]] is monoidally [[equivalent]] to a [[strict monoidal category]].
1. Every free [[monoidal category]] is monoidally [[equivalent]] to a free [[strict monoidal category]].

However, one must be careful not to assume that it is always possible to strictify everything. For instance, the strictification theorem for [[symmetric monoidal categories]] states the following.

1. Every [[symmetric monoidal category]] is monoidally [[equivalent]] to a [[symmetric strict monoidal category]] (*not* a [[strict symmetric monoidal category]]).
1. Every free [[monoidal category]] is monoidally [[equivalent]] to a free [[symmetric strict monoidal category]].

This is why we use the term "semi-strict" above: a strictification theorem expresses the extent to which a structure may be strictified, which may not be completely. Another classical example is [[tricategories]], which may be strictified to [[Gray-categories]], but not in general to [[3-categories]].

Strictification theorems are related to, but not the same as, [[coherence theorems]].

## Examples of strictification theorems

See [[coherence theorem]] for a list of coherence theorems that also include strictification results.

## Approaches to strictification

There exist several approaches for proving strictification theorems.

 for describing "doctrines" or algebraic structures on categories, which can be used to describe free algebras and state coherence theorems.  All are closely related.

### 2-monads {#2monads}

A [[2-monad]] can be regarded as the "extensional essence" of an algebraic structure on categories (or on objects of some other 2-category).  Of course, if $T$ is a 2-monad describing some structure, then $T A$ is the free such structure on $A$; thus the first sort of coherence theorem can be precisely stated as "describe $T A$ as explicitly as possible in terms of $A$."

However, the notion of monad is so general that in practice, for proving coherence theorems it is useful to have a more explicit way of "presenting" a monad in terms of generating operations and relations; this is the purpose of the structures presented below, such as [[operads]] and [[clubs]].  Not all monads can be presented in such a more explicit way, but for those that can, it is a very useful simplification.

The notion of *strict* 2-monad on a [[strict 2-category]] also provides a general way to state a strictification theorem, although one must beware that this theorem is not always true, and when it is true, it doesn't necessarily give what one was looking for.  This general "coherence theorem schema" for a 2-monad $T$ would be that every [[pseudoalgebra for a 2-monad|pseudo]] $T$-algebra is equivalent to a strict one.  A stronger statement, which is true in most cases when the weaker version is, would be that the inclusion
$$ Str T Alg \hookrightarrow Ps T Alg $$
of the 2-category of strict $T$-algebras and strict $T$-morphisms into the 2-category of pseudo $T$-algebras and pseudo $T$-morphisms has a strict left 2-adjoint, usually written $(-)'$, and moreover for a pseudo algebra $A$, the unit $A \to A'$ is an [[equivalence]] in $Ps T Alg$.  Thus $A$ is not only equivalent to a strict $T$-algebra, it is equivalent to a canonically defined one which is characterized by a universal property.

This "coherence theorem" is true in a lot of generality, although there are 2-monads for which it fails (see ([Shulman](#Shulman))).  However, often it leaves a lot of work to be done in order to extract what is commonly thought of as a coherence theorem.  This is because the notion of pseudo $T$-algebra is always an *unbiased* weak structure, whereas it is more usual to study biased structures.  Moreover, in most cases, proving an equivalence between biased and unbiased notions requires the full strength of the coherence theorem (in the description-of-free-algebras sense) for the biased notion!

### Operads

For now, see [[operad]].

### Clubs

For now, see [[club]].

### Yoneda embedding

For now, see [[strictification theorem for bicategories with finite limits]], which gives an example of this approach.

## Strictification versus coherence

See [[strictification versus coherence]].

## List of strictification theorems

* [[coherence and strictification for monoidal categories]]
* [[coherence and strictification for symmetric monoidal categories]]
* [[strictification for bicategories with finite limits]]

## Related pages

* [[coherence theorem]]

## References

* [[Steve Lack]], Codescent objects and coherence, [MR](http://www.ams.org/mathscinet-getitem?mr=1935980)

* [[Mike Shulman]], "Not every pseudoalgebra is equivalent to a strict one", *Adv. Math.* 229 no. 3 (2012), 2024&#8211;2041, [arXiv](http://arxiv.org/abs/1005.1520)
{#Shulman}

[[!redirects strictification theorems]]
[[!redirects strictification]]