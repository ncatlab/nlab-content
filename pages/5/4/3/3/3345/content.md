
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
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

There is a [[model category]] structure on the [[category]] $[\Box^{op},Set]$ of [[cubical set]]s whose [[homotopy theory]] is that of the standard [[model structure on simplicial sets]].

Using this version of the [[homotopy hypothesis]]-theorem, cubical sets are a way to describe the [[homotopy type]] of [[∞-groupoid]]s using of all the [[geometric shapes for higher structures]] the [[cube]].


## Definition

There is an evident [[simplicial set]]-valued [[functor]]

$$
  \Box \to sSet
$$

from the [[cube category]] to [[sSet]], which sends the cubical $n$-cube to the simplicial $n$-cube

$$
  \mathbf{1}^n \mapsto (\Delta[1])^{\times n}
  \,.
$$

Similarly there is a canonical [[Top]]-valued functor

$$
  \Box \to Top
$$

$$
  \mathbf{1}^n \mapsto (\Delta^1_{Top})^n
  \,.
$$

The corresponding [[nerve and realization]] [[adjunction]]

$$
  (|-| \dashv Sing_\Box) : Top \stackrel{\overset{|-|}{\leftarrow}}{\underset{Sing_\Box}{\to}} Set^{\Box^{op}}
$$

is the cubical analogue of the simplicial nerve and realization discussed [above](#ForKanComplexes).

+-- {: .un_theorem}
###### Theorem


There is a [[model structure on cubical sets]] $Set^{\Box^{op}}$ whose

* weak equivalences are the morphisms that become weak equivalences under geometric realization $|-|$;

* cofibrations are the [[monomorphism]]s.

=--

This is ([Jardine, section 3](#Jardine)).

The following theorem establishes a form of the [[homotopy hypothesis]] for cubical sets.

+-- {: .un_theorem}
###### Theorem

The [[unit of an adjunction|unit of the adjunction]]

$$
  A \to Sing_\Box(|A|)
$$

is a weak equivalence in $Set^{{\Box}^{op}}$ for every cubical set $A$.

The counit of the adjunction

$$
  |Sing_\Box X| \to X
$$

is a weak equivalence in $Top$ for every topological space $X$.

It follows that we have an [[equivalence of categories]] induced on the [[homotopy categories]]

$$
  Ho(Top) \simeq Ho(Set^{\Box^{op}})
  \,.
$$

=--

This is [Jardine, theorem 29, corollary 30](#Jardine).


## References

* Jardine, _Model structure on cubical sets_ (2002) ([pdf](http://hopf.math.purdue.edu/Jardine/cubical2.pdf)) 
{#Jardine}