
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
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

The notion of **$sSet$-site** is the incarnation of the notion of [[(∞,1)-site]] when [[(∞,1)-categories]] are incarnated as [[simplicially enriched categories]].

## Definition

+-- {: .un_defn}
###### Definition

An **$sSet$-site** is a [[simplicially enriched category]] $C$ together with the structure of a [[site]] on its [[homotopy category of an (infinity,1)-category|homotopy category]] $Ho(C)$.

=--

This appears as ([Toën & Vezzosi 005, def. 3.1.1](#ToënVezzosi05))


## Properties

### Relation to $(\infty,1)$-sites

+-- {: .un_defn}
###### Proposition

Under the identification of [[simplicially enriched categories]] with models for [[(∞,1)-categories]], $sSet$-sites correspond to [[(∞,1)-site]]s.

=--

Because, as discussed at [[(∞,1)-site]], that is equivalently an [[(∞,1)-category]] equipped with the structure of a site on its [[homotopy category of an (∞,1)-category]].

### Relation to $(\infty,1)$-toposes

+-- {: .un_defn}
###### Proposition

For $C$ an $sSet$-site, the local [[model structure on sSet-presheaves]] is a [[presentable (∞,1)-category|presentation]] of the [[(∞,1)-topos]] $Sh_\infty(C)$ over the [[(∞,1)-site]] corresponding to $C$

$$
 ([C^{op}, sSet]_{loc})^\circ \simeq Sh_\infty(C)
  \,.
$$

=--



## Examples

* [[simplicial Stein site]]


## Related concepts

* [[site]]

* [[2-site]]

* [[(∞,1)-site]]

  * [[model site]], **simplicial site**

  * [[model topos]]

## References

* {#ToënVezzosi05} [[Bertrand Toën]], [[Gabriele Vezzosi]],  p. 4 and Def. 3.1.1 of:  _Homotopical Algebraic Geometry I: Topos theory_, Advances in Mathematics **193** 2 (2005) 257-372 &lbrack;[arXiv:0207028](http://arxiv.org/abs/math/0207028)&rbrack;




[[!redirects SSet-site]]
[[!redirects simplicial site]]
[[!redirects SSet-sites]]
[[!redirects simplicial sites]]

[[!redirects simplicially enriched site]]
[[!redirects simplicially enriched sites]]
