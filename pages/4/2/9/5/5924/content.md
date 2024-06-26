
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


## Definition


Let $\mathcal{S}$ be a [[topos]], regarded as a [[base topos]].


+-- {: .num_defn}
###### Definition

An **$\mathcal{S}$-indexed topos** $\mathbb{E}$ is an $\mathcal{S}$-[[indexed category]] such that

* for each object $I \in \mathcal{S}$ the fiber $\mathbb{E}^I$ is a [[topos]];

* for each morphism $x : I \to J$ in $\mathcal{S}$ the corresponding transition functor $x^* : \mathbb{E}^J \to \mathbb{E}^I$ is a [[logical morphism]].

An **$\mathcal{S}$-indexed geometric morphism** is an $\mathcal{S}$-indexed [[adjunction]] $(f^* \dashv f_*)$ between $\mathcal{S}$-indexed toposes, such that $f^*$ is left exact. 

This yields a [[2-category]] $Topos_{\mathcal{S}}$ of $\mathcal{S}$-indexed toposes.

=--

This appears at ([Johnstone, p. 369](#Johnstone)).


## Examples

* For $p : \mathcal{E} \to \mathcal{S}$ a [[geometric morphism]], the induced morphism $\mathbb{E} \to \mathbb{S}$ (discussed at [[base topos]]) is an $\mathcal{S}$-indexed topos.


## Properties

+-- {: .num_prop}
###### Proposition

Write [[Topos]]$/\mathcal{S}$ for the [[slice 2-category]] of toposes over $\mathcal{S}$. This is a [[full sub-2-category]] of the 2-category of$\mathcal{S}$-indexed toposes:

$$
  Topos/{\mathcal{S}} \hookrightarrow Topos_{\mathcal{S}}
  \,.
$$

=--

This appears as ([Johnstone, prop. 3.1.3](#Johnstone)).

## Related concepts

* [[topos]], [[base topos]]

* [[indexed category]]

* [[hyperdoctrine]]

## References

Section B3.1 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

[[!redirects indexed toposes]]
[[!redirects indexed topoi]]