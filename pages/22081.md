


#Contents#
* table of contents
{:toc}

## Definition

The __free simplicial abelian group functor__
$$\mathbf{Z}[-]\colon sSet \to sAb$$
from [[SimplicialSets]] to [[SimplicialAbelianGroups]]
is given by the functor
$$sSet = Fun(\Delta^{op}, Set) \to Fun(\Delta^{op}, Ab) = sAb,$$
where the middle functor applies the [[free abelian group functor]]
$$\mathbf{Z}[-]\colon Set \to Ab.$$

## Properties

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


## Applications

Free simplicial abelian groups
are the crucial ingredient of [[simplicial chains]] and [[simplicial cochains]],
and such also [[simplicial homology]] and [[simplicial cohomology]],
in particular, [[singular homology]] and [[singular cohomology]].
See these articles for more information.

## Related entries

* [[free abelian group]]

* [[simplicial chains]]

* [[simplicial cochains]]

[[!redirects free simplicial abelian group functor]]
[[!redirects free simplicial abelian group functors]]
[[!redirects free simplicial abelian groups]]

[[!redirects free simplicial abelian group functor]]
