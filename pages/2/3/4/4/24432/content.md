
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **CMon-enriched symmetric monoidal category** is a [[symmetric monoidal category]] such that each [[hom-set]] is a [[commutative monoid]] and both the [[tensor product]] and the [[composition]]-operation on [[morphisms]] are [[bilinear]].

Beware that in discussion of [[differential categories]] and of [[differential linear logic]] such categories are often referred to as "([[pre-additive category|pre-]])[[additive categories]]", while traditionally this terminology refers to [[enriched category|enrichment]] in [[abelian groups]] instead of just [[commutative monoids]]. The term "CMon-enriched symmetric monoidal category" is non-standard but used here to avoid this clash of terminology.


## Definition

In detail, a **CMon-enriched symmetric monoidal category** is a [[symmetric monoidal category]] such that each [[hom-set]] $\mathcal{C}[A,B]$ is a [[commutative monoid]] (we write $f + g$ for the [[sum]] of two morphisms $f,g \colon A \rightarrow B$ and $0$ for the [[zero]] $A \rightarrow B$), such that for [[every]] $f,g \colon A \rightarrow B$, $h,i \colon C \rightarrow D$ and $j,k \colon B \rightarrow C$:

* $(f+g)\otimes h = f \otimes h + g \otimes h$
* $f \otimes (h+i) = f \otimes h + f \otimes i$
* $0 \otimes f = f \otimes 0 = 0$
* $(f+g);j = f;j + g;j$
* $f;(j+k) = f;j + f;k$
* $0;f = f;0 = 0$

[[!redirects CMon-enriched symmetric monoidal categories]]

## Related entries 

* [[CMon-enriched monoidal category]]