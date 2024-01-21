
#Contents#
* table of contents
{:toc}

## Idea

A **CMon-enriched symmetric monoidal category** is a [[symmetric monoidal category]] such that each [[hom-set]] is a [[commutative monoid]] and the [[tensor product]] on [[morphisms]] and the [[composition]] are [[bilinear]].

This notion is often referred to as [[additive category]] or [[pre-additive category]] in works on [[differential categories]] or [[differential linear logic]]. However these terms classically assume more structure, the most obvious being an enrichment over [[abelian groups]] and not only [[commutative monoids]]. In order to reduce confusion, we use a less ambiguous naming convention here.


## Definition

In detail, a **CMon-enriched symmetric monoidal category** is a symmetric monoidal category such that each hom-set $\mathcal{C}[A,B]$ is a commutative monoid (we write $f + g$ for the [[sum]] of two morphisms $f,g \colon A \rightarrow B$ and $0$ for the [[zero]] $A \rightarrow B$), such that for [[every]] $f,g \colon A \rightarrow B$, $h,i \colon C \rightarrow D$ and $j,k \colon B \rightarrow C$:

* $(f+g)\otimes h = f \otimes h + g \otimes h$
* $f \otimes (h+i) = f \otimes h + f \otimes i$
* $0 \otimes f = f \otimes 0 = 0$
* $(f+g);j = f;j + g;j$
* $f;(j+k) = f;j + f;k$
* $0;f = f;0 = 0$

[[!redirects CMon-enriched symmetric monoidal categories]]

## Related entries 

* [[CMon-enriched monoidal category]]