
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

# $\mathcal{F}$-categories
* table of contents
{: toc}

## Idea

An **$\mathcal{F}$-category** is like a [[2-category]], but with two types of 1-morphism, one of which we think of as "stricter" than the other.  The stricter morphisms are called **tight** and the less strict ones are called **loose**.

## Definition

### Strict $\mathcal{F}$-categories

Let $\mathcal{F}$ denote the category whose [[objects]] are [[functors]] that are [[fully faithful functors|fully faithful]] and injective on objects, and whose [[morphisms]] are [[commutative squares]] (a [[full subcategory]] of the [[arrow category]] of [[Cat]]).  We call the objects of $\mathcal{F}$, for the nonce, _full embeddings_.  Then $\mathcal{F}$ is [[cartesian closed category|cartesian closed]], [[complete category|complete]] and [[cocomplete category|cocomplete]], hence a [[Benabou cosmos]].

A **strict $\mathcal{F}$-category** is a [[enriched category|category enriched over]] $\mathcal{F}$.  Therefore, between every two objects, an $\mathcal{F}$-category $K$ has an object $K(x,y)\in \mathcal{F}$, hence a full embedding $K(x,y)_\tau \to K(x,y)_\lambda$.  The objects of $K(x,y)_\tau$ are called **tight morphisms** $x\to y$, and the objects of $K(x,y)_\lambda$ are called **loose morphisms** $x\rightsquigarrow y$.

Since full embeddings are injective on objects, "being tight" is a [[stuff, structure, property|property]] of a loose morphism.  (This would still be true in the "up to unique isomorphism" sense even if we did not ask for injectivity on objects, but when dealing with strict things, it is easier to keep them as strict as possible.)  And since full embeddings are fully faithful, the 2-cells between two tight morphisms are the same whether we regard them as tight or as loose.

For any $\mathcal{F}$-category $K$, the objects, tight morphisms, and 2-cells form a strict 2-category $K_\tau$, and the objects, loose morphisms, and 2-cells form a strict 2-category $K_\lambda$.  There is an obvious strict 2-functor
$$K_\tau \to K_\lambda$$
which is the identity on objects, strictly [[faithful functor|faithful]] on 1-morphisms, and [[locally fully faithful 2-functor|locally fully faithful]].  Since $K$ can be recovered from this 2-functor, an equivalent definition of a strict $\mathcal{F}$-category is as a strict 2-functor with these properties.

### Weak $\mathcal{F}$-categories

Probably the best "fully weak" version of $\mathcal{F}$-categories is obtained by redefining $\mathcal{F}$ to consist of fully faithful functors, with squares that commute up to specified isomorphism, and then by considering $\mathcal{F}$-[[enriched bicategories]] rather than enriched categories.  Such a thing would be equivalent to an identity-on-objects and locally-fully-faithful pseudofunctor between bicategories.

One could consider semi-strict versions as well, in which (for example) the tight morphisms form a strict 2-category.

## Examples

* Any [[proarrow equipment]] is an $\mathcal{F}$-category (perhaps weak, perhaps semi-strict).

* An example of a semi-strict $\mathcal{F}$-category is the [[localization]] 2-functor $Cat(S) \to Cat(S)[W^{-1}]$ for a class of [[weak equivalences]] $W$.

* For any ([[strict 2-monad|strict]]) [[2-monad]] $T$, there are strict $\mathcal{F}$-categories of $T$-algebras whose tight and loose morphisms are, respectively:

  1. strict and pseudo $T$-morphisms
  1. strict and [[lax morphism|lax]] $T$-morphisms
  1. strict and colax $T$-morphisms
  1. pseudo and lax $T$-morphisms
  1. pseudo and colax $T$-morphisms

  In fact, this can be generalized to any $\mathcal{F}$-monad on an $\mathcal{F}$-category.

* Any 2-category gives rise to two $\mathcal{F}$-categories:

  * In a **chordate** $\mathcal{F}$-category, all morphisms are tight.
  * In an **inchordate** $\mathcal{F}$-category, only identities are tight.

* The [[lax slice 2-category]] is an $\mathcal{F}$-category whose tight 2-category is the (pseudo) slice 2-category.  This $\mathcal{F}$-category allows a definition of [[fibration in a 2-category|fibrations]] using [[lax F-adjunctions]].

* $\mathcal{F}$ itself becomes an $\mathcal{F}$-category in the usual way.  Its tight morphisms are just the morphisms in the underlying ordinary category $\mathcal{F}$, while its loose morphisms are simply functors between the loose parts (the codomains of the full embeddings).

## $\mathcal{F}$-weighted limits

The general machinery of [[enriched category]] theory applied to $\mathcal{F}$ gives us a notion of [[weighted limit]].  Note first that an $\mathcal{F}$-enriched *diagram* in an $\mathcal{F}$-category is a diagram of morphisms in which some are required to be tight, and others are not (but could "accidentally" be tight).

In general, a weighted limit of such a diagram in a (strict) $\mathcal{F}$-category is a weighted (strict) [[2-limit]] in its 2-category of loose morphisms, with the property that certain specified projections from the limit object are tight and "jointly detect tightness", in the sense that a morphism into the limit is tight if and only if its composites with all of the specified projections are tight.  Details and examples can be found in ([LS](#LS)).

One of the most important things about $\mathcal{F}$-categories is that they allow us to define the classes of [[rigged limits]], which are the $\mathcal{F}$-weighted limits that are [[created limit|created]] by the forgetful functors from the various $\mathcal{F}$-categories of algebras and strict/pseudo/lax/colax morphisms over a 2-monad (or an $\mathcal{F}$-monad).

## Related pages

* [[rigged limit]]

* [[F-functor]]

* [[lax F-natural transformation]]

* [[lax F-adjunction]]

The [[1-category]]-theoretic version:

* [[relative categories]]$\;$[as enriched categories](relative+category#AsEnrichedCategories)

## References

* {#LS} [[Stephen Lack]] and [[Mike Shulman]], "Enhanced 2-categories and limits for lax morphisms", [arXiv](http://arxiv.org/abs/1104.2111).
 

[[!redirects F-category]]
[[!redirects F-categories]]
[[!redirects strict F-category]]
[[!redirects strict F-categories]]
[[!redirects tight morphism]]
[[!redirects tight morphisms]]
[[!redirects loose morphism]]
[[!redirects loose morphisms]]
