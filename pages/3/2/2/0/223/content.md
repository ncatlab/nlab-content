
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}


## Definition

A [[category]] is **small** if it has a [[small set]] of [[object]]s and a [[small set]] of [[morphism]]s.  

In other words, a small category is an [[internal category]] in the category [[Set]].

A category which is not small may be called [[large category|large]], especially when it is not *essentially* small (see below).


## Properties

Small categories are free of some of the subtleties that apply to large categories.

A category is said to be **essentially small** (or, rarely, **svelte**) if it is [[equivalence of categories|equivalent]] to a small category.  Assuming the [[axiom of choice]], this is the same as saying that it has a small [[skeleton]], or equivalently that it is [[locally small category|locally small]] and has a [[small set|small number]] of isomorphism classes of objects.

A category is said to be **Morita small** if it is [[Morita equivalent]] to a small category (i.e. its [[category of presheaves]] is [[equivalence of categories|equivalent]] to a the category of presheaves on a small category, or alternatively if it is [[equivalence in a 2-category|equivalent]] to a small category in the bicategory [[Dist]] of [[distributors]]).

A **small category structure** on a [[locally small category]] $C$ is an [[essentially surjective functor]] from a set (as a [[discrete category]]) to $C$.  A category is essentially small iff it is locally small and has a small category structure; unlike the previous paragraph, this result does not require the axiom of choice.

## Characterisations

The following are equivalent for a [[locally small]] category $B$ (see the linked [MathOverflow answer](#KoudenburgMathOverflow)).

1. $B$ is essentially small.
2. The [[category of presheaves]] $[B^{op}, Set]$ is [[locally small]].
3. For every presheaf $q : B^{op} \to Set$ and copresheaf $p : B \to Set$ the coend $\int^{y \in B} py \times qy$ is [[small presheaf|small]].
4. Every presheaf on $B$ is [[small presheaf|small]].
5. For every functor $F : B \to C$ with [[locally small]] codomain, and for every object $c \in C$, the presheaf $C(F{-}, c) : B^{op} \to Set$ is [[small presheaf|small]].

These different characterisations are useful, because they give a way to capture the notion of size in [[formal category theory]]. For instance, characterisation (2) is axiomatised in the formalism of **small objects** in [[Yoneda structures]]; whereas characterisation (5) is axiomatised in the formalism of **petit objects** in [[KZ-doctrines]] (see [DL23](#DL23)).

## Smallness in the context of universes
 {#SmallnessInTheContextOfUniverses}

If [[Grothendieck universe]]s are being used, then for $U$ a fixed Grothendieck universe, a category $C$ is **$U$-small** if its collection of objects and collection of morphisms are both elements of $U$. Thus, 

* a $U$-small category is a category [[internal category|internal to]] $U Set$.

This of course is a [[material set theory|material]] formulation. We may call $C$ **structurally $U$-small** if there is a [[bijection]] from its set of morphisms to an element of $U$ (the same for the set of objects follows). This gives an up-to-isomorphism version of $U$-smallness (see [[universe in a topos]] for an alternative structural formulation). Such structural $U$-smallness may be substituted in the discussion below. 

Let $U\Set$ be the category of $U$-small sets. Similar considerations lead us to say

* a $U$-category (a [[locally small category|locally U-small]])-category is a category [[enriched category|enriched over]] $U Set$,  

and that a category $C$ **essentially $U$-small** if it is locally $U$-small and admits an essentially surjective functor from a discrete $U$-small category. 

A category is **$U$-moderate** if its set of objects and set of morphisms are both subsets of $U$.  However, some categories (such as the category of $U$-moderate categories!) are larger yet.

## Related concepts

* **small category**, [[locally small category]], [[complete small category]]

* [[essentially small (∞,1)-category]]

* [[small site]]

* [[large category]]

## References

* [[Ross Street]] and [[Robert Walters]], _Yoneda structures on 2-categories_, Journal of Algebra, Vol. 50, No. 2, 1978, pp. 350-379. &lbrack;<a href="https://doi.org/10.1016/0021-8693(78)90160-6">doi:10.1016/0021-8693(78)90160-6</a>&rbrack;

* [[Peter Freyd]] and [[Ross Street]], _On the Size of Categories_, Theory and Applications of Categories, Vol. 1, No. 9, 1995, pp. 174-181. &lbrack;[TAC](http://www.tac.mta.ca/tac/volumes/1995/n9/1-09abs.html)&rbrack;

* {#DL23} [[Ivan Di Liberti]], [[Fosco Loregian]], *Accessibility and Presentability in 2-Categories*, Journal of Pure and Applied Algebra **227** 1 (2023) &lbrack;[arXiv:1804.08710](https://arxiv.org/abs/1804.08710), [doi:10.1016/j.jpaa.2022.107155](https://doi.org/10.1016/j.jpaa.2022.107155)&rbrack;

* [[Seerp Roald Koudenburg]], _Formal category theory in augmented virtual double categories_, Theory and Applications of Categories 41.10 (2024): 288-413.

* {#KoudenburgMathOverflow} [[Seerp Roald Koudenburg]], answer to "Is every petite category essentially small?": [MathOverflow](https://mathoverflow.net/a/474544)

The terminology **Morita small** appears, for instance, in:

* [[Nathanael Arkor]], [[Dylan McDermott]], _The nerve theorem for relative monads_ (2025), Theory and Applications of Categories, &lbrack;[arXiv:2404.01281](https://arxiv.org/abs/2404.01281)&rbrack;

though the notion has appeared earlier, e.g. it is simply called **small** in:


* [[Ross Street]], _Enriched categories and cohomology_, Quaestiones Mathematicae, Vol. 6, No. 1-3, 1983, pp. 265-283. &lbrack;[doi:10.1080/16073606.1983.9632304](https://doi.org/10.1080/16073606.1983.9632304)&rbrack;

[[!redirects small]]
[[!redirects small category]]
[[!redirects small categories]]
[[!redirects essentially small category]]
[[!redirects essentially small categories]]
[[!redirects moderate category]]
[[!redirects moderate categories]]
[[!redirects essentially moderate category]]
[[!redirects essentially moderate categories]]

[[!redirects svelte category]]
[[!redirects svelte categories]]

[[!redirects essentially small]]

[[!redirects Morita small]]
[[!redirects Morita small category]]
[[!redirects Morita small categories]]