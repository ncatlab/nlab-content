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

\begin{definition}\label{BalancedCategory}
A category is **balanced** if every [[monomorphism|monic]] [[epimorphism|epic]] morphism is an [[isomorphism]].  
\end{definition}


## Remarks 

* The possibility of monic epics that are not isomorphisms does not survive any strengthening of "monic" or "epic."  Any monic [[extremal epimorphism]] is necessarily an isomorphism, and therefore so is any monic [[strong epimorphism]] or [[regular epimorphism]] (and dually).  It follows that if all epics, or all monos, are extremal, then the category is automatically balanced.

* In an "unbalanced" category it is frequently the case that the monomorphisms, the epimorphisms, or both, are not the "right" notion to consider and should be replaced by their [[extremal epimorphism|extremal]], [[strong epimorphism|strong]], or [[regular epimorphism|regular]] counterparts.


## Examples and non-examples 

\begin{example}\label{SetIsBalanced}
  The category [[Set]] is balanced (Def. \ref{BalancedCategory}).
\end{example}
More generally:
\begin{example}
Any [[topos]] and in fact any [[pretopos]] is balanced.  
\end{example}
\begin{remark}
 A [[quasitopos]], however, need *not* be balanced.
\end{remark}

* Some algebraic categories, such as [[Grp|the category of groups]] (see [here](regular+monomorphism#Examples) and [here](https://ncatlab.org/nlab/show/Grp#eq)), are balanced.

* Any [[abelian category]] is balanced. An [[additive category]] need not be; for example in the category of [[torsion subgroup]]-free abelian groups, each nonzero homomorphism $\mathbb{Z} \to \mathbb{Z}$ is both monic and epic. 

* The [[category of rings]] is not balanced; $Z\hookrightarrow Q$ is monic and epic but not an isomorphism. On similar grounds, the [[category of commutative monoids]] is not balanced, as the inclusion $\mathbb{N} \hookrightarrow \mathbb{Z}$ is both monic and epic. 

* Topological categories are rarely balanced; in [[Top]], for example, the monic epimorphisms are the continuous bijections.  However, the category of [[compact Hausdorff space]]s is balanced.

* In a [[partial order|poset]] or a [[quiver]], or more generally any _[[thin category]]_, _every_ morphism is both monic and epic; thus such categories are "as far as possible from being balanced."


[[!redirects balanced categories]]