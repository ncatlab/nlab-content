

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Every [[sheaf topos]] $\mathcal{E}$ of sheaves with values in [[Set]] is canonically and essentially uniquely equipped with its [[global section]] [[geometric morphism]] $\Gamma : \mathcal{E} \to Set$. So in particular for $\mathcal{E} \to \mathcal{F}$ any other [[geometric morphism]], we have necessarily a [[diagram]]

$$
  \array{
    \mathcal{E} &&\to&& \mathcal{F}
    \\
    & \searrow &\swArrow_{\simeq}& \swarrow
    \\
    && Set
  }
$$

in the [[2-category]] [[Topos]]. 

Accordingly, if $\mathcal{E}$ and $\mathcal{F}$ are both equipped with [[geometric morphism]] to some other topos $\mathcal{S}$, it makes sense to restrict attention to those geometric morphisms between them that do form commuting triangles as before

$$
  \array{
    \mathcal{E} &&\to&& \mathcal{F}
    \\
    & \searrow &\swArrow_{\simeq}& \swarrow
    \\
    && \mathcal{S}
  }
$$

but now over the new _base topos_ $\mathcal{S}$. This is a [[morphism]] in the [[slice 2-category]] [[Topos]]$/\mathcal{S}$.

One can develop essentially all of [[topos theory]] in $Topos/\mathcal{S}$ instead of in $Topos$ itself.

To some extent it is also possible to speak of a base topos entirely [[internal logic|internally]] to a given topos. See for instance ([AwodeyKishida](#AwodeyKishida)).

## Constructions

+-- {: .num_defn}
###### Definition

To $\mathcal{S}$ itself we associate the $\mathcal{S}$-[[indexed category]] (the canonical self-indexing) $\mathbb{S}$ given by

$$
  \mathbb{S}^I = \mathcal{S}/I
  \,.
$$

To $p : \mathcal{E} \to \mathcal{S}$ a topos over a base $\mathcal{S}$, we associate the $\mathcal{S}$-[[indexed category]]

$$
  \mathbb{E} : \mathcal{S}^{op} \to Cat
$$

which sends an object $I \in \mathcal{S}$ to the [[over-topos]] of $\mathcal{E}$ over the [[inverse image]] of $I$ under the [[geometric morphism]] $p$

$$
  \mathcal{E}^I := \mathcal{E}/p^*(I)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The [[geometric morphism]] $p : \mathcal{E} \to \mathcal{S}$ induces an $\mathcal{S}$-indexed geometric morphism (hence a geometric morphism [[internalization|internal to]] the [[slice 2-category]] [[Topos]]$/\mathcal{S}$)

$$
  \mathbb{p} : \mathbb{E} \to \mathbb{S}
  \,.
$$

=--

By the discussion at [[indexed category]].

## Related concepts

* [[base (∞,1)-topos]]
* [[internal site]]
* [[internal sheaves]]
* [[bounded geometric morphism]]
* [[unbounded topos]]


## References

The general notion of base toposes is the topic of section B3 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

An internal description of base toposes in the context of [[modal logic]] appears in

* {#AwodeyKishida} [[Steve Awodey]], Kohei Kishida, _Topology and modality: the topological interpretation of first-order modal logic_ ([pdf](http://www.andrew.cmu.edu/user/awodey/preprints/FoS4.phil.pdf))
  

[[!redirects base toposes]]

[[!redirects topos over a base]]
[[!redirects toposes over a base]]

