+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$\infty$-algebra over an $(\infty,1)$-operad_ is an [[∞-groupoid]] equipped with higher algebraic operations as encoded by an [[(∞,1)-operad]].  Since there is not really any other sensible notion of algebra for an $(\infty,1)$-operad, we feel free to drop the prefix (although in other cases it can be helpful to disambiguate).

This is the [[(∞,1)-category theory]]-analog of the notion of [[algebra over an operad]]. Notice that in the literature one frequently sees [[model category]] presentations of $(\infty,1)$-operads by ordinary [[operad]]s enriched in a suitable [[monoidal model category]]. In these models $\infty$-algebras are be presented by ordinary algebras over cofibrant [[resolution]]s of ordinary enriched operads. This is directly analogous to how [[(∞,1)-categories]] may be presented by [[simplicially enriched categories]].

Also notice that the enrichment used in these models is not necessarily over [[Top]] / [[sSet]] (the standard [[presentable (∞,1)-category|presentations]] of [[∞Grpd]]) but often notably over a [[category of chain complexes]]. But at least for connective chain complexes, the [[Dold-Kan correspondence]] says that these, too, are in turn models for certain [[∞-groupoid]]s. This, in turn, is in direct analogy to how a [[stable (∞,1)-category]] may be presented by a [[dg-category]].

## Definition

### In terms of $(\infty,1)$-categories of operators

We discuss $\infty$-algebras with [[(∞,1)-operads]] viewed in terms of their [[(∞,1)-categories of operators]] as in ([Lurie](#Lurie)).

In full generality we have:

+-- {: .num_defn}
###### Definition

For $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ a [[fibration of (∞,1)-operads]], then for $\mathcal{P}^\otimes \to \mathcal{O}^\otimes$ any other [[morphism of (∞,1)-operads|homomorphism]], an [[(∞,1)-algebra over an (∞,1)-operad|(∞,1)-algebra over]] $\mathcal{P}^\otimes$ in $\mathcal{C}^\otimes$ is a homomorphism of [[(∞,1)-operads]] from $\mathcal{P}$ to $\mathcal{C}$ over $\mathcal{O}$

=--

Specifically if $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ is a [[coCartesian fibration of (∞,1)-operads]] then this exhibits $\mathcal{C}$ as equipped with the structure of an $\mathcal{O}$-[[monoidal (∞,1)-category]]. Then a [[section]] $A \colon \mathcal{O}^\otimes \to \mathcal{C}^{\otimes}$ is a $\mathcal{O}$-algebra in $\mathcal{C}$ with respect to this structure. (The "[[microcosm principle]]").

## Model category presentations

We discuss [[presentable (∞,1)-category|presentations]] of [[(∞,1)-categories]] of $\infty$-algebras over [[(∞,1)-operad]]s by [[model category]] structures on categories of [[algebra over an operad|algebras over an operad]] enriched in some suitable [[monoidal model category]].

(...)

For the moment see

* [[model structure on algebras over an operad]].

## Examples

See also

* [[homotopy algebra]].


## Related concepts

* [[algebra over a monad]]

  [[∞-algebra over an (∞,1)-monad]] 

* [[algebra over an algebraic theory]] 

  [[∞-algebra over an (∞,1)-algebraic theory]] 

  * [[homotopy T-algebra]] / [[model structure on simplicial T-algebras]]


* [[(∞,1)-operad]], [[model structure on operads]]

  * [[algebra over an operad]], **algebra over an (∞,1)-operad**, [[model structure on algebras over an operad]]

    * [[module over an algebra over an (∞,1)-operad]], [[model structure on modules over an algebra over an operad]]

    * [[rectification]]



## References

* [[Gijs Heuts]]: [algebras over ∞-operads, Arxiv:math/1110.1776](http://arxiv.org/pdf/1110.1776.pdf)

Model category structures for $\infty$-algebras are discussed in

* [[Clemens Berger]], [[Ieke Moerdijk]], _Resolution of coloured operads and rectification of homotopy algebras_ ([arXiv:math/0512576](http://arxiv.org/abs/math/0512576))
{#BergerMoerdijk}

Section 2.1.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#Lurie}

[[!redirects ∞-algebra over an (∞,1)-operad]]
[[!redirects ∞-algebras over an (∞,1)-operad]]
[[!redirects ∞-algebras over (∞,1)-operads]]

[[!redirects (∞,1)-algebra over an (∞,1)-operad]]
[[!redirects (∞,1)-algebras over an (∞,1)-operad]]
[[!redirects (∞,1)-algebras over (∞,1)-operads]]


[[!redirects infinity-algebras over an (infinity,1)-operad]]
[[!redirects infinity-algebras over (infinity,1)-operads]]

[[!redirects (infinity,1)-algebras over an (infinity,1)-operad]]
[[!redirects (infinity,1)-algebras over (infinity,1)-operads]]


[[!redirects algebra over an (∞,1)-operad]]
[[!redirects algebras over an (∞,1)-operad]]
[[!redirects algebras over (∞,1)-operads]]

[[!redirects algebra over an (infinity,1)-operad]]
[[!redirects algebras over an (infinity,1)-operad]]
[[!redirects algebras over (infinity,1)-operads]]
