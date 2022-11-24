
#Contents#
* table of contents 
{:toc}

## Idea

A **CMon-enriched monoidal category** is a [[monoidal category]] such that each [[hom-set]] is a [[commutative monoid]] and the [[tensor product]] on [[morphisms]] and the [[composition]] are [[bilinear]].

## Definition

In details, a **CMon-enriched monoidal category** is a monoidal category such that each hom-set $\mathcal{C}[A,B]$ is a commutative monoid (we write $f + g$ for the [[sum]] of two morphisms $f,g \colon A \rightarrow B$ and $0$ for the [[zero]] $A \rightarrow B$), such that for [[every]] $f,g \colon A \rightarrow B$, $h,i \colon C \rightarrow D$ and $j,k \colon B \rightarrow C$:

* $(f+g)\otimes h = f \otimes h + g \otimes h$
* $f \otimes (h+i) = f \otimes h + f \otimes i$
* $0 \otimes f = f \otimes 0 = 0$
* $(f+g);j = f;j + g;j$
* $f;(j+k) = f;j + f;k$
* $0;f = f;0 = 0$

## Properties

\begin{proposition}
If a CMon-enriched monoidal category possesses the [[binary products]], then they are [[biproducts]] and the category is thus [[semiadditive category|semiadditive]]. The same goes if it possesses the [[binary coproducts]].
\end{proposition}

\begin{proposition}
If a CMon-enriched monoidal category possesses a [[terminal object]], then it is a [[zero object]]. The same goes if it possesses an [[initial object]].
\end{proposition}

## Examples

\begin{proposition}
Every [[semiadditive category|semiadditive]] monoidal category is a CMon-enriched monoidal category.
\end{proposition}

## Related entries 

* [[CMon-enriched symmetric monoidal category]]

[[!redirects CMon-enriched monoidal categories]]