
#Contents#
* table of contents
{:toc}

## Definition

A morphism $f:X\to Y$ of [[schemes]] is an __open immersion__ if the underlying morphism of topological spaces is a [[homeomorphism]] onto an open [[image]] and the [[comorphism]] $f^\sharp : \mathcal{O}_Y\to f_*\mathcal{O}_X$ is an [[isomorphism]] of sheaves when restricted to the image of $f$. In other words, an open immersion is a morphism of schemes which decomposes uniquely into an isomorphism of schemes and the identity [[inclusion morphism|inclusion]] of an [[open subscheme]].  

## Properties

+-- {: .num_prop}
###### Proposition

Every open immersion of schemes is an [[étale morphism of schemes]]

=--

(e.g. [[The Stacks Project|Stacks Project, lemma 28.37.9]])

## Examples


+-- {: .num_example}
###### Example

For $R$ a [[ring]], $S \hookrightarrow U(R)$ a [[multiplicative subset]],  and $R \longrightarrow R[S^{-1}]$ the projection onto the [[localization of a commutative ring|localization]] at $S$, then the [[Isbell duality|formal dual]] map on [[spectrum of a commutative ring|spectra]] $Spec(R[S^{-1}]) \longrightarrow Spec(R)$ is an open immersion. 

These are the _standard opens_ that define the [[Zariski topology]] on [[algebraic varieties]]

=--

## Related concepts

* [[closed immersion of schemes]]

* [[immersion]], [[open map]]

* [[closed immersion of schemes]]

* [[Zariski topology]]

[[!redirects open immersion]]
[[!redirects open immersions]]

[[!redirects open immersions of schemes]]

category: algebraic geometry