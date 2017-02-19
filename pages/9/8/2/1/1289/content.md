
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
#### Modalities, Closure and Reflection
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

A __coreflective subcategory__ is a [[full subcategory]] whose inclusion functor has a [[right adjoint]] $R$ (a [[cofree functor]]):

$$
  C \stackrel{\overset{i}{\hookrightarrow}}{\underset{R}{\leftarrow}} D
  \,.
$$



The dual concept is that of a [[reflective subcategory]]. See there for more details.

## Properties

+-- {: .un_theorem}
###### Theorem

[[Vopěnka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[colimit]]s is a [[coreflective subcategory]].

=--

This is ([AdamekRosicky, theorem 6.28](#AdamekRosicky)).


## Examples

* the inclusion of [[Kelley space]]s into [[Top]], where the right adjoint "kelleyfies"

* the inclusion of [[torsion theory|torsion]] [[abelian groups]] into [[Ab]], where the right adjoint takes the [[torsion subgroup]].

* the inclusion of groups into monoids, where the right adjoint takes a monoid to its group of units.

* [[Lie integration]], which constructs a [[simply connected space|simply connected]] [[Lie group]] from a finite-dimensional real [[Lie algebra]]. The coreflector is Lie differentiation (taking a Lie group to its associated Lie algebra), and the [[counit]] is the natural map to a given Lie group $G$ from the universal [[covering space]] of the [[connected space|connected component]] at the identity of $G$. 

## References

* [[Jiri Adamek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, London Mathematical Society Lecture Note Series 189
{#AdamekRosicky}


* Robert El Bashir, Jiri Velebil, _Simultaneously Reflective And Coreflective Subcategories of Presheaves_ ([TAC](http://www.tac.mta.ca/tac/volumes/10/16/10-16abs.html))

[[!redirects coreflective subcategories]]