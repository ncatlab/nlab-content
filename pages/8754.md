+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
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
**Theories of presheaf type** though being [[geometric theory|geometric theories]] of a particular "simple" and tractable type are yet ubiquitous in the sense that every geometric theory is a [[quotient theory]] of some theory of presheaf type.


## Definition

+-- {: .num_defn }
###### Definition

A [[geometric theory]] $T$ is **of presheaf type** if its [[classifying topos]] is [[equivalence of categories|equivalent]] to a [[presheaf topos]].

=--

## Examples

* Any [[cartesian theory]] $\mathbb{T}$ being (modulo neglectable size issues[^iss]) classified by $Set^{\mathbb{T}-Mod_{fp}(Set)}$ is of presheaf type with $\mathbb{T}-Mod_{fp}(Set)$ the category of finitely presentable $\mathbb{T}$-models in $Set$.

* More concretely, e.g. the [[theory of objects]] or the [[classifying topos#ForIntervals|theory of intervals]] are of presheaf type being classified by the [[classifying topos for the theory of objects|object classifier]] respectively by the [[simplicial sets|topos of simplicial sets]].

## Properties

+-- {: .num_prop }
###### Proposition

A theory is of presheaf type if and only if its category of [[models]] in [[Set]] is a finitely [[accessible category]], and if and only if it is [[sketch|sketchable]].

=--

Cf. Caramello ([2018](#Cara18), p.199). In particular, any consistent theory of presheaf type has models in $Set$.

[^iss]: This means that the essentially small category $\mathbb{T}-Mod_{fp}(Set)$ has to be replaced by its skeleton.

## Related entries

* [[Gabriel-Ulmer duality]]

* [[Diaconescu theorem]]

* [[natural homotopy]]

## References

* [[Tibor Beke]], _Theories of presheaf type_ ([pdf](http://faculty.uml.edu/tbeke/jsl.pdf))

* {#Cara18}[[Olivia Caramello]], _Theories, Sites, Toposes_ , Oxford UP 2018.


[[!redirects theories of presheaf type]]
