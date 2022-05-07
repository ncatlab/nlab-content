

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--
# Contents
* table of contents
{:toc}



## Idea

In [[topology]], a not necessarily [[continuous function|continuous]] [[function]] $ \colon X \to Y$ between [[Hausdorff space|Hausdorff spaces]] is _dominant_, or _dense_, in the sense that the [[image]] of $f$ is a [[dense subspace]] of $Y$, precisely if every [[continuous function]]  $g \colon Y \to Z$ to any  [[Hausdorff space]] $Z$ is uniquely determined by the [[composition]] $g \circ f$.

In [[category theory]], the concept of a **dense functor** is a generalization of this concept to [[functors]]. 

An important special case that was also historically the source of the concept, is the case of a [[dense subcategory]] [[fully faithful functor|inclusion]]: a [[subcategory]] $S$ of category $C$ is _dense_ if every [[object]] $c$ of $C$ is a [[colimit]] of a [[diagram]] of objects in $S$, in a canonical way. 

## Definition 

\begin{definition}\label{DenseFunctor}
**(dense functor)**\linebreak
A [[functor]] $i \colon S \to C$ is __dense__ if it satisfies the following equivalent conditions:

1. every [[object]] $c$ of $C$ is the [[colimit]]

   $
     \underset{\longrightarrow}{\lim}
     \Big(
       (i/c)
       \overset{\mathrm{pr}_S}{
         \longrightarrow
       } 
       S 
       \overset{i}{\longrightarrow} 
       C
     \Big)
   $

   over the [[comma category]] $(i/c)$:

1. every [[object]] $c$ of $C$ is the $C(i-,c)$-[[weighted colimit]] of $i$.  

   (This version generalizes readily to the [[enriched category theory]]).

1. the corresponding [[restricted Yoneda embedding]] $C \to [S^{op},Set]$ is [[full and faithful functor|fully faithful]]. 

\end{definition}

## Properties
  {#Properties}

\begin{remark}\label{DenseFunctorsNotClosedUnderComposition}
**(dense functors not closed under composition)** \linebreak
Beware that the [[class]] of dense functors (Def. \ref{DenseFunctor}) is *not* closed under [[composition]] of functors.

For a counter-example see Example \ref{DenseSubcategoriesOfSimplexCategory} below.

\end{remark}




## Examples
 {#Examples}

\begin{example}
The inclusion of the [[discrete category]] on the [[singleton set]] into all of [[Sets]] is a [[dense subcategory]] inclusion.

More generally, if $C$ is an essentially small category, then the [[Yoneda embedding]] $C \to [C^{op},Set]$ is dense.
\end{example}

\begin{example}
Let $V$ be a category of [[algebras]] and $n \in \mathbb{N}$ such that $V$ has a presentation with operations of at most arity $n$.  Let $v$ be the free $V$-algebra on $n$ generators.  Then the [[full subcategory]] with object $v$ is dense in $V$.

More generally, if $V$ is a $\kappa$-[[accessible category]], then the full subcategory inclusion $V_\kappa \subseteq V$ of $\kappa$-[[presentable objects]] is dense. This means in particular that if $C$ is a small category, then the canonical inclusion $C \to Ind(C)$ into the [[Ind category]] is dense, and that categories of sheaves have small dense subcategories.
\end{example}

\begin{example}\label{DenseSubcategoriesOfSimplexCategory}
  Consider the [[simplex category]] $\Delta$, regarded in the usual way as a [[subcategory]] of [[Cat]]. Let $\Delta_{\leq [1]} \subset \Delta$ be the full subcategory with object set $\{[0],[1]\}$ -- i.e. comprising the 0-dimensional simplex and the 1-dimensional simplex.

Then 

1. $\Delta_{\leq [1]} \hookrightarrow \Delta$ is a [[dense subcategory]] inclusion;

1. $\Delta \hookrightarrow \mathbf{Cat}$ is a [[dense subcategory]] inclusion, 

1. but the composite $\Delta_{\lt 2} \hookrightarrow \Delta \hookrightarrow Cat$ is *not* dense in $\mathbf{Cat}$ (see Remark \ref{DenseFunctorsNotClosedUnderComposition}).

\end{example}

\begin{example}
The category $Top$ of [[topological spaces]] does not have any small full subcategory which is dense. Indeed, $Top$ is not generated under colimits by any small subcategory.

The category $Set^{op}$ has a small full subcategory which is dense if and only if there is not a proper class of [[measurable cardinals]], a result due to Isbell.
\end{example}



## Related entries

* [[dense subcategory]]

* [[codensity monad]]

* [[space and quantity]]

* [[dominant geometric morphism]]


## Terminology and History ##
 
[[John Isbell]] introduced [[dense subcategory|dense subcategories]] in a seminal paper [(Isbell 1960)](#MR0175954) under the name *left adequate*.  The dual notion of *right adequate* was also introduced and subcategories satisfying both were called *adequate*. It was also shown that while the relation of being left (or right) adequate is not transitive, being adequate is transitive. He also brought out interesting connections with [[set theory]] and [[measurable cardinals]].

Later in the mid 60s, [[Friedrich Ulmer]] considered the concept for more general functors $F:C\to D$, not only inclusions $I:C\hookrightarrow D$, and introduced the name _dense_ for them.

Independently, [[Pierre Gabriel]] worked on this concept and their work coalesced to what was to become the concept of a [[locally presentable category]] of their [1971 monograph](#GabrielUlmer71). It is also good to keep in mind the '_Abelian_' subcontext in the background, in particular the developments in module theory e.g. Lazard's (1964) characterization of flat modules as filtered colimits of finitely generated free modules.

More recently, [[Jacob Lurie]] has referred to the analogue notion for [[(∞,1)-categories]] as *strongly generating* in a version (arXiv v4) of his [[Higher Topos Theory|HTT]], but that term normally means [[strong generator|something different]].


## References

* Tom Avery, [[Tom Leinster]], _Isbell conjugacy and the reflexive completion_, arXiv:2102.08290 (2021). ([abstract](https://arxiv.org/abs/2102.08290))

* {#GabrielUlmer71} [[Pierre Gabriel|Peter Gabriel]], [[Friedrich Ulmer]], _Lokal pr&#228;sentierbare Kategorien_ , LNM **221** Springer Heidelberg 1971. (&#167; 3, pp.38-44)

* {: #MR0175954 } [[John Isbell]], _Adequate subcategories_ , Illinois J. Math. **4** (1960) pp.541-552. [MR0175954](http://www.ams.org/mathscinet-getitem?mr=0175954). ([euclid](https://projecteuclid.org/euclid.ijm/1255456274))
 
* [[John Isbell]], _Subobjects, adequacy, completeness and categories of algebras_ , Rozprawy Mat. **36** (1964) pp.1-32. ([toc](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-0dbcb276-0b92-49eb-b504-a9963119ea3e), [pdf](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-0dbcb276-0b92-49eb-b504-a9963119ea3e/c/rm36_01.pdf))

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_ , Cambridge UP 1982. (Reprinted as [TAC reprint no.10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html) (2005); chapter 5, pp.85-112)

* [[William Lawvere]], _John Isbell's Adequate Subcategories_, TopCom **11** no.1 2006. ([link](http://at.yorku.ca/t/o/p/d/65.htm))

* [[Saunders Mac Lane]], _Categories for the Working Mathematician_ , Springer Heidelberg 1998&#178;. (section X.6, pp.245ff, 250)

* Horst Schubert, _Kategorien II_ , Springer Heidelberg 1970. (section 17.2, pp.29ff)

* [[Friedrich Ulmer]], _Properties of dense and relative adjoint functors_ , J. of Algebra **8** (1968) pp.77-95.

[[!redirects adequate subcategory]]
[[!redirects left adequate subcategory]]
