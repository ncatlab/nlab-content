
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _inverse functor_ is the generalization of that of _[[inverse function]]_ from [[sets]] to [[categories]]. Where the existence of an inverse function exhibits a [[bijection]] of sets, the existence of an inverse functor exhibits an [[equivalence of categories]].

## Definition

Given a [[functor]]

$$
  F \;\colon\; \mathcal{C} \longrightarrow \mathcal{D}
$$

then an _inverse_ to $F$ is a [[functor]] going the other way around

$$
  G \;\colon\; \mathcal{D} \longrightarrow \mathcal{C}
$$

together with [[natural isomorphisms]] relating their [[composition|composites]] to the respective [[identity functors]]:

$$
  G\circ F \simeq id_{\mathcal{C}}
  \phantom{AAAA}
  F \circ G  \simeq id_{\mathcal{D}}
  \,.
$$

## Related concepts

* [[inverse]], [[inverse morphisms]]




[[!redirects inverse functors]]