
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

+-- {: .num_defn}
###### Definition

A [[geometric morphism]] $f : \mathcal{E} \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathcal{F}$ is called **atomic** if its [[inverse image]] $f^*$ is a [[logical functor]].

=--

+-- {: .num_defn}
###### Definition

A [[sheaf topos]] is called **atomic** if its [[global section]] geometric morphism is atomic.

Generally, a topos over a [[base topos]] $\Gamma : \mathcal{E} \to \mathcal{S}$ is called an **atomic topos** if $\Gamma$ is atomic.

=--

+-- {: .num_note}
###### Note

The term "atomic" is bad, but standard. 

=--

## Properties

+-- {: .num_prop}
###### Proposition

Atomic morphisms are closed under composition.

=--

+-- {: .num_cor}
###### Corollary

Let $\mathcal{E}$ be a [[Grothendieck topos]] with [[point of a topos|enough points]]. Then $\mathcal{E}$ is a [[Boolean topos]] precisely if it is an atomic topos.

=--

This appears as ([Johnstone, cor. 3.5.2](#Johnstone)).

+-- {: .proof}
###### Proof

If $\Gamma^*$ logical then it preserves the isomorphism $* \coprod * \simeq \Omega$ characterizing a [[Boolean topos]] and hence $\mathcal{E}$ is Boolean if it is atomic.

For the converse...

=--

## Examples

+-- {: .num_prop}
###### Proposition

Every [[etale geometric morphism]] is atomic.

=--

## References

Section C3.5 of

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

[[!redirect atomic geometric morphisms]]

[[!redirects atomic topos]]
[[!redirects atomic toposes]]
[[!redirects atomic topoi]]