#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $C$ an ordinary [[category]] and $c \in C$ an [[object]] of $C$, the ordinary [[over category]] $C\downarrow c$ satisfies the universal property that for any other category $C'$ there is a natural bijection of hom-sets

$$
  Hom(C',C\downarrow c) \simeq
  Hom_{c}(C' \star \{\top\}, C)
  \,,
$$
where

* $C' \star \{\top\}$ denotes the category $C'$ with a freely adjoined [[terminal object]] $\top$;

* $Hom_{c}(\cdots)$ denotes the subset of functors which send $\top$ to $c$.

The idea of the definition of [[over category]] in the context of [[quasi-category|quasi-categories]] is to mimic this universal property. This relies crucially on generalizing the construction $C' \star \{\top\}$ to the context of quasi-categories, in terms of the [[join of quasi-categories]].

## Definition

Let $C$ be a [[quasi-category]]. let $K$ be any [[simplicial set]] and let $F : K \to C$ be a morphism of simplicial sets (hence a morphism of quasi-categories if $K$ itself is a quasi-category).

The **over-quasi-category** $C_{/F}$ is the simplicial set characterized by the property that for any other simplicial set $S$ there is a natural bijection of hom-sets

$$
  Hom_{SSet}(S, C_{/F})
  \simeq
  Hom_{F}(
    S \star K, C
  )
  \,,
$$
where

* $S \star K$ is the [[join of simplicial sets]] of $S$ with $K$;

* the Hom-set on the right is the subset of morphism $f : S \star K \to C$ such that $f|_K = F$.

## References

See [proposition 1.2.9.2, p. 44](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=44) and the text leading to and including [proposition 1.2.9.3](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf#page=44) of

* J. Lurie, _Higher topos theory_ ([pdf](http://arxiv.org/PS_cache/math/pdf/0608/0608040v4.pdf))


[[!redirects over-category in quasi-categories]]
[[!redirects over quasicategory]]
[[!redirects over-quasi-category]]
[[!redirects over-quasicategory]]
[[!redirects overquasicategory]]
[[!redirects slice quasi-category]]
[[!redirects slice quasicategory]]