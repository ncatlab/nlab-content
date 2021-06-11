
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An _enriched model category_ is an [[enriched category]] $C$ together with the structure of a [[model category]] on the [underlying category](http://ncatlab.org/nlab/show/enriched+category#BaseChange) $C_0$ such that both structures are compatible in a reasonable way.


## Definition

Let $V$ be a [[monoidal model category]].

A **$V$-enriched model category** is

* an V-[[enriched category]] $C$

  * which is [[powered and copowered category|powered and copowered]] over $V$;

* with the structure of a [[model category]] on the [underlying category](enriched+category#BaseChange) $C_0$

* such that 

  * {#PullbackPowerAxiom} **([[pullback-power axiom]])** for every [[cofibration]] $i \colon A \to B$ and [[fibration]] $p \colon X \to Y$ in $C_0$ the [[pullback powering]] morphism (dual to the [[pushout product]]) with respect to the powering in $V$ 

    $$
      C(B,X) \stackrel{(i^* , p_*)}{\to} C(A,X) \times_{C(A,Y)} C(B,Y)
    $$ 

    is a fibration with respect to the model structure on $V$;

  * and is an [[acyclic fibration]] whenever $i$ or $p$ are acyclic.

The last two conditions here are equivalent to the fact that the [[copower]]

$$
  \otimes : C \times V \to C
$$

is a [[Quillen bifunctor]].

## Properties

### Change of enrichment

(...)


## Examples

* The most familiar examples of enriched model categories are [[simplicial model categories]].

* For a [[pointed category|pointed]] model category or even [[stable model category]] there is enrichment in [[pointed]] simplicial sets with the [[smash product]] as tensor product.

## Related concepts

* [[derived hom-functor]]

* [[enriched homotopical category]].

* [[pushout-product]], [[pushout-product  axiom]]
 
* [[pullback power]]

## References

Textbook account:

* [[Jacob Lurie]], Def. A.3.1.5 in: _[[Higher Topos Theory]]_, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

See also:

* [[Bertrand Guillou]], [[Peter May]], _Enriched model categories and presheaf categories_, New York J. Math. 26 (2020) 37–9 ([arXiv:1110.3567](http://arxiv.org/abs/1110.3567), [](https://www.emis.de/journals/NYJM/j/2020/26-3.html), [NYJM:2020/26-3](https://www.emis.de/journals/NYJM/j/2020/26-3.html))

[[!redirects enriched model categories]]

[[!redirects enriched model structure]]
[[!redirects enriched model structures]]

[[!redirects enriched model category theory]]


