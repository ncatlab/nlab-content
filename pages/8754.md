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

A [[geometric theory]] $\mathbb{T}$ is **of presheaf type** if its [[classifying topos]] $Set[\mathbb{T}]$ is [[equivalence of categories|equivalent]] to a [[presheaf topos]].

=--

## Examples

* Any [[cartesian theory]] $\mathbb{T}$ being (modulo neglectable size issues[^iss]) classified by $Set^{\mathbb{T}-Mod_{fp}(Set)}$ is of presheaf type with $\mathbb{T}\text{-}Mod_{fp}(Set)$ the category of finitely presentable $\mathbb{T}$-models in $Set$.

* More concretely, e.g. the [[theory of objects]] or the [[classifying topos#ForIntervals|theory of intervals]] are of presheaf type being classified by the [[classifying topos for the theory of objects|object classifier]] respectively by the [[simplicial sets|topos of simplicial sets]].

* The _inconsistent theory_ with axiom $\top\vdash\bot$ is of presheaf type since it is classified by the initial Grothendieck topos $\mathbf{1}\simeq Pr(\emptyset)$, the presheaf topos on the empty category.

## Properties

+-- {: .num_prop }
###### Proposition

For a [[category]] $\mathcal{M}$ the following are equivalent:

* $\mathcal{M}$ is finitely [[accessible category|accessible]].

* $\mathcal{M}\simeq Pts(Set^{\mathcal{C}})$ the [[point of a topos|category of points]] of some presheaf topos.

* $\mathcal{M}\simeq \mathbb{T}\text{-}Mod(Set)$ for some theory $\mathbb{T}$ of presheaf type.

* $\mathcal{M}\simeq Ind \text{-}\mathcal{C}$ for some small category $\mathcal{C}$.

=--

Cf. Beke ([2004](#Beke04), p.923) and the references given there. In fact, these equivalences are mostly (direct consequences of) classical results in the theory of accessible categories or Grothendieck toposes.

Note that despite the above equivalences the finite accessibility of $\mathbb{T}\text{-}Mod(Set)$ does _not_ imply that $\mathbb{T}$ itself is of presheaf type! One sees this already in case $\mathbb{T}\text{-}Mod(Set)=\emptyset$ since there famously are non trivial (Boolean sheaf) toposes lacking points ("non empty generalized spaces without points") yet up to [[Morita equivalence]] the only theory of presheaf type corresponding to the finite accessibility of the empty category is the inconsistent theory.

The following proposition shows in which sense theories of presheaf type are still determined by their (finitely presentable) models in $Set$:

+-- {: .num_prop }
###### Proposition

A [[geometric theory]] $\mathbb{T}$ is of presheaf type iff (modulo neglectable size issues[^iss])
$$Set[\mathbb{T}]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]\, .$$

=--

**Proof**. "$\Rightarrow$":

(Cf. [Caramello 2018](#Cara18), pp.198f)

By assumption $Set[\mathbb{T}]\simeq [\mathcal{C}, Set]$. Since $[\mathcal{C},Set]\simeq [\hat{\mathcal{C}}, Set]$ (by [Johnstone 2002](#JT02), p.10) we can assume that $\mathcal{C}$ is [[Cauchy complete category|Cauchy complete]].

We have:

* $Ind\text{-}\mathcal{C}\simeq Flat(\mathcal{C}^{op}, Set)$ (by [Johnstone 2002](#JT02), p.723, or [Caramello 2018](#Cara18), p.198)

* $(Ind\text{-}\mathcal{C})_{fp}\simeq \mathcal{C}$ (by [Johnstone 2002](#JT02) 4.2.2.(iii), p.724)

* $\mathbb{T}\text{-}Mod(Set)\simeq Flat(\mathcal{C}^{op}, Set)$ (from [[Diaconescu theorem|Diaconescu’s theorem]]).

Whence $(Ind\text{-}\mathcal{C})_{fp}\simeq (\mathbb{T}\text{-}Mod (Set))_{fp} =\mathbb{T}\text{-}Mod_{fp}(Set)\simeq \mathcal{C}$ and, accordingly, $[\mathcal{C},Set]]\simeq  [\mathbb{T}\text{-}Mod_{fp}(Set),Set]$. $\qed$

In other words, theories of presheaf type are precisely those [[geometric theory|geometric theories]] $\mathbb{T}$ such that their classifying toposes $Set[\mathbb{T}]$ can be represented as presheaf toposes $Set^{\mathbb{T}\text{-}Mod_{fp}(Set)}$.

This implies e.g. that any consistent theory of presheaf type has models in $Set$.

[^iss]: This means here (and in the following) that the essentially small category $\mathbb{T}\text{-}Mod_{fp}(Set)$ has to be replaced by a skeleton.

## Related entries

* [[Gabriel-Ulmer duality]]

* [[Diaconescu theorem]]

* [[natural homotopy]]

## References

* {#Beke04}[[Tibor Beke]], _Theories of presheaf type_ , JSL **69** no.3 (2004) pp.923-934. ([pdf](http://faculty.uml.edu/tbeke/jsl.pdf))

* {#Cara18}[[Olivia Caramello]], _Theories, Sites, Toposes_ , Oxford UP 2018. (chapters 6-9)

* {#JT02}[[Peter Johnstone]], _[[Sketches of an Elephant]] vols.1-2_ , Oxford UP 2002.

[[!redirects theories of presheaf type]]
[[!redirects Theory of presheaf type]]
