
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Homotopy Theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

[[!redirects Natural homotopy]]
[[!redirects Natural Homotopy]]

#Contents#
* table of contents
{:toc}

##Idea

Viewing [[topos|toposes]] as generalized spaces, **natural homotopy** is an equivalence relation between [[geometric morphism|geometric morphisms]] generalizing the [[homotopy|homotopy relation]] between [[continuous map|continuous maps]].

This relation is "natural" in the metaphorical sense of being the most "basic" such relation and in the metonymical sense of being defined via [[natural transformation|natural transformations]].

The correspondance between [[geometric theory|geometric theories]] and (classifying) [[Grothendieck topos|Grothendieck toposes]] then induces an equivalence relation between theories finer than [[Morita equivalence]] that affords to define "homotopical" concepts for logic e.g. contractability of a theory.

## Definition

Given two [[Grothendieck toposes]] $\mathcal{E},\mathcal{F}$, let $[\mathcal{E},\mathcal{F}]$ denote the class of [[connected category|connected components]] of their Hom-category $Hom(\mathcal{E},\mathcal{F})$. Two [[geometric morphism|geometric morphisms]] $f,g:\mathcal{E}\to\mathcal{F}$ are called _naturally homotopical_ , denoted $f\simeq g$, if $[f]=[g]$, or in other words, if there exists a zigzag of [[natural transformation|natural transformations]] $f\leftarrow\cdot\rightarrow\cdot \dots\cdot\leftarrow\cdot\rightarrow g$.

### Remark

Under the correpondance $Hom(\mathcal{E},Set(\mathbb{T}))\cong \mathbb{T}-Mod(\mathcal{E})$ natural homotopy corresponds to an equivalence relation on $\mathbb{T}$-models in $\mathcal{E}$ given by zigzags of model homomorphisms.

## Properties

...

## Examples

...


## Topos homotopy via path spaces

The [[Sierpinski topos]] $Set^2$ is a connected, locally connected and local topos. As a result of [[Artin gluing]] along $Set\overset{id}{\to}Set$ it has two [[point of a topos|topos points]] (corresponding to the two points of the underlying [[Sierpinski space]]). It is [[exponentiable topos|exponentiable]] and, given a topos $\mathcal{E}$, we can accordingly view the exponential $\mathcal{E}^{Set^2}$ as a path space for $\mathcal{E}$ with respect to the abstract [[interval object]] $Set^2$.

(Cf. Beke [2000](#B00), p.11f)

## Related entries

* [[homotopy theory]]

* [[theory of model homomorphisms]]

* [[Sierpinski topos]]

* [[Eilenberg-Mac Lane space]]

* [[theory of presheaf type]]

## References

The concept originates with

* {#JW84}[[André Joyal]], [[Gavin Wraith]], _Eilenberg-Mac Lane Toposes and Cohomology_ , pp.117-131 in Cont. Math. **92** AMS 1984.

A overwiew of homotopy theory done in this "toposophical" context is

* {#B00}[[Tibor Beke]], _Homotopoi_ , ms. University of Massachusetts Lowell (2000). ([dvi](http://faculty.uml.edu/tbeke/topos.dvi))

A good source for the classical cohomology theory of toposes is chapter 8 of

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014)


