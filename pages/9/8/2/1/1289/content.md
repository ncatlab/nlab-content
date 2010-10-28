
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
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

[[Vop?nka's principle]] is equivalent to the statement:

For $C$ a [[locally presentable category]],  every [[full subcategory]] $D \hookrightarrow C$ which is closed under [[colimit]]s is a [[coreflective subcategory]].

=--

This is ([AdamekRosicky, theorem 6.28](#AdamekRosicky)).


## Examples

* the inclusion of [[Kelley space]]s into [[Top]], where the right adjoint "kelleyfies"

## Related concepts

* [[reflective subcategory]] / [[reflective sub-(∞,1)-category]]

* **coreflective subcategory**

## References

* [[Jiri Adamek]], [[Ji?í Rosický]], _Locally presentable and accessible categories_ London Mathematical Society Lecture Note Series 189
{#AdamekRosicky}

[[!redirects coreflective subcategories]]