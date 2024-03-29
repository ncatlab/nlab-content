
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

A [[geometric morphism]] $f : \mathcal{X} \to \mathcal{Y}$ of [[toposes]] is **separated** if the [[diagonal]] $\mathcal{X} \to \mathcal{X} \times_{\mathcal{Y}} \mathcal{X}$ is a [[proper geometric morphism]].

In particular if $\mathcal{Y}$ is the [[terminal object]] in [[Topos]], hence the canonical [[base topos]] [[Set]], we say that a topos $\mathcal{X}$ is a **Hausdorff topos** if $\mathcal{X} \to \mathcal{X} \times \mathcal{X}$ is a proper geometric morphism.

More generally, since there is a hierarchy of notions of _[[proper geometric morphism]]_, there is accordingly a hierarchy of separatedness conditions. 

## Examples

+-- {: .num_prop}
###### Proposition

For $G$ a [[discrete group]] and $\mathbf{B}G = (G \stackrel{\to}{\to} *)$ its [[delooping]] [[groupoid]], the [[presheaf topos]] $G Set \simeq [\mathbf{B}G, Set]$ is Hausdorff precisely if $G$ is a [[finite group]].

=--

In ([Johnstone](#Johnstone)) this is example C3.2.24

## Related concepts

* [[Hausdorff topological space]]
* [[quasi-separated scheme]]
* [[separated scheme]], [[separated morphism of schemes]]

## References

Chapter II of 

* [[Ieke Moerdijk]], Jacob Vermeulen,  _Relative compactness conditions for toposes_ ([pdf](http://igitur-archive.library.uu.nl/math/2001-0702-142944/1039.pdf)) and _Proper maps of toposes_ , American Mathematical Society (2000)
  {#MoerdijkVermeulen}

Around def. C3.2.12 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

[[!redirects Hausdorff topos]]
[[!redirects strongly Hausdorff topos]]

[[!redirects Hausdorff toposes]]
[[!redirects strongly Hausdorff toposes]]

[[!redirects Hausdorff topoi]]
[[!redirects strongly Hausdorff topoi]]

[[!redirects separated geometric morphisms]]
