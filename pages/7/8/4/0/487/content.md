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
A category is **balanced** if every [[morphism]] which is both a [[monomorphism]] and an [[epimorphism]] is already an [[isomorphism]].  
\end{definition}

\begin{remark}
The possibility of monic epics that are not isomorphisms does not survive any strengthening of "monic" or "epic."  Any monic [[extremal epimorphism]] is necessarily an isomorphism, and therefore so is any monic [[strong epimorphism]] or [[regular epimorphism]] (and dually).  It follows that if all epics, or all monos, are extremal, then the category is automatically balanced.

In an "unbalanced" category it is frequently the case that the monomorphisms, the epimorphisms, or both, are not the "right" notion to consider and should be replaced by their [[extremal epimorphism|extremal]], [[strong epimorphism|strong]], or [[regular epimorphism|regular]] counterparts.
\end{remark}



## Examples and non-examples 
 {#Examples}

\begin{example}\label{SetIsBalanced}
  The category [[Set]] is balanced (Def. \ref{BalancedCategory}).
\end{example}
More generally:
\begin{example}
Any [[topos]] and in fact any [[pretopos]] is balanced.  
\end{example}
(eg. [Johnstone 1977, Cor. 1.22](#Johnstone77))
\begin{remark}
 Beware the [[counterexample]]:
 A [[quasitopos]], need *not* be balanced.
\end{remark}

\begin{example}\label{AbelianCategoriesAreBalanced}
Any [[abelian category]] is balanced. 

In particular categories [[Mod]] of [[modules]] and [[Vect]] of [[vector spaces]] are balanced.
\end{example}
\begin{remark}
  An [[additive category]] need not be balanced:  A [[counterexample]] is the category of [[torsion subgroup]]-free abelian groups, each nonzero homomorphism $\mathbb{Z} \to \mathbb{Z}$ is both monic and epic. 
\end{remark}

\begin{example}
The [[Grp|the category of groups]] is balanced (see [here](regular+monomorphism#Examples) and [here](Grp#eq)).
\end{example}

\begin{remark}
Not all categories of [[algebra|algebraic]] [[structures]] are balanced. 

As a [[counterexample]],
the [[category of rings]] is not balanced: $\mathbb{Z}\hookrightarrow \mathbb{Q}$ is monic and epic but not an isomorphism. 

On similar grounds, the [[category of commutative monoids]] is not balanced, as the inclusion $\mathbb{N} \hookrightarrow \mathbb{Z}$ is both monic and epic. 
\end{remark}

\begin{remark}
Topological categories are rarely balanced. In [[Top]], for example, the monic epimorphisms are the continuous bijections.  
\end{remark}
However:
\begin{example}
The category of [[compact Hausdorff spaces]] is balanced.
\end{example}

\begin{remark}
In a [[free category]] on a [[directed graph]], and also in any
[[partial order|poset]] and  generally in any _[[thin category]]_, _every_ morphism is both monic and epic while only the [[identity morphisms]] are invertible; thus such categories are "as far as possible from being balanced."
\end{remark}

## References

* {#Johnstone77} [[Peter Johnstone]], Cor. 1.22 in: _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press (1977), Dover (2014)

* [[Roy L. Crole]], p. 115 of: *Categories for types*, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9781139172707](https://doi.org/10.1017/CBO9781139172707)&rbrack;


[[!redirects balanced categories]]