
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _proper map of toposes_ is the generalization to [[toposes]] of the notion of [[proper map]] of [[topological spaces]].

## Definition

+-- {: .num_defn}
###### Definition

A [[sheaf topos]] $\mathcal{E}$ is called a **[[compact topos]]** if the [[direct image]] of the [[global section geometric morphism]] $\Gamma : \mathcal{E} \to Set$ preserves [[directed colimit|directed]] [[joins]] of [[subterminal objects]].

It is called **strongly compact** if $\Gamma$ commutes even with all [[filtered colimits]] ([MV, p. 53](#MoerdijkVermeulen)).

=--

A [[geometric morphism]] $f : \mathcal{F} \to \mathcal{E}$ is called **proper** if it exhibits $\mathcal{F}$ as a [[compact topos]] over $\mathcal{E}$.

It is called **tidy** if it exhibits $\mathcal{F}$ as a strongly compact topos over $\mathcal{E}$.


## Examples

+-- {: .num_prop}
###### Proposition

Examples of strongly compact toposes $\mathcal{E}$ include the following.

1. Every [[coherent topos]] is strongly compact.

1. The [[sheaf topos]] over a [[compact topological space|compact]] [[Hausdorff space|Hausdorff]] [[topological space]] is strongly compact.

=--

([MV, Examples III.1.1](#MoerdijkVermeulen))

+-- {: .num_prop}
###### Proposition

An object $X \in \mathcal{T}$ in a topos $\mathcal{T}$ is a [[Kuratowski finite object]] precisely if the [[étale geometric morphism]]

$$
  \mathcal{T}_{/X} \to \mathcal{T}
$$

out of the [[slice topos]] is a proper geometric morphism. And precisely if $X$ is even _decidable_ is this a tidy geometric morphism.

=--

([Moerdijk-Vermeulen, examples III 1.4](#MoerdijkVermeulen))


## References

* [[Ieke Moerdijk]], J. Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](http://igitur-archive.library.uu.nl/math/2001-0702-142944/1039.pdf)) and _Proper maps of toposes_ , American Mathematical Society (2000)
  {#MoerdijkVermeulen}

[[!redirects proper maps of toposes]]

[[!redirects proper geometric morphism]]
[[!redirects proper geometric morphisms]]

[[!redirects compact topos]]