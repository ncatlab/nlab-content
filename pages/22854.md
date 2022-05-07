
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A *simplicial abelian group* is

* an [[abelian group|abelian]] [[group object]] [[internalization|internal to]] [[SimplicialSets]];

* a [[simplicial object]] [[internalization|internal to]] [[AbelianGroups]].

## Properties

### Basic properties

\begin{proposition}\label{FreeSimplicialAbelianGroupAdjunction}
**([[free simplicial abelian group]]-[[adjunction]])** \linebreak
  There is a [[pair]] of [[adjoint functors]]
  (a [[free functor|free]]$\dashv$[[forgetful]]-[[adjunction]])
  $$
    sAb
      \underoverset
        {\underset{ frgt }{\longrightarrow}}
        {\overset{\mathbb{Z}(-)}{\longleftarrow}}
        {\;\;\;\;\;\bot\;\;\;\;\;}
    sSet
  $$

  between [[SimplicialAbelianGroups]] and [[SimplicialSets]], where

  * the [[left adjoint]] is the [[free simplicial abelian group]]-[[functor]];

  * the [[right adjoint]] is the [[functor]] that assigns [[underlying]] [[simplicial sets]].

  This is a [[Quillen adjunction]] with respect to the [[classical model structure on simplicial sets]] and the projective [[model structure on simplicial abelian groups]].
\end{proposition}

### More properties

* [[Dold-Kan correspondence]]

* [[Eilenberg-Zilber theorem]]

* [[model structure on simplicial abelian groups]]

## Related concepts

* [[Moore complex]]

* [[Eilenberg-Zilber map]]

* [[simplicial group]], [[simplicial topological group]]

* [[free simplicial abelian group]]

[[!redirects simplicial abelian groups]]

[[!redirects sAb]]
[[!redirects sAbGrp]]
[[!redirects SimplicialAbelianGroups]]


