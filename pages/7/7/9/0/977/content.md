
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Notions of subcategory
+-- {: .hide}
[[!include notions of subcategory]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The concept of a **dense subcategory** generalizes the concept of a [[dense subspace]] from [[topology]] to [[categories]]. Roughly speaking, a dense subcategory 'sees' enough of the ambient category to control the behavior and properties of the latter.

The concept forms part of a related family of concepts concerned with 'generating objects' and has some interesting interaction with [[set theory]] and [[measurable cardinals]].

## Definition

### In category theory

There are actually two different notions of _dense [[subcategory]]_ $D$ of a given [[category]] $C$:

1. A subcategory $D\subset C$ is __dense__ if every [[object]] in $C$ is canonically a [[colimit]] of objects in $D$.  

This is equivalent to saying that the inclusion [[functor]] $D\hookrightarrow C$ is a [[dense functor]].  

An older name for a dense subcategory in this sense is an **adequate subcategory**.

2. A subcategory $D\subset C$ is __dense__ if every object $c$ of $C$ has a $D$-expansion, that is a [[morphism]] $c\to\bar{c}$ of [[pro-objects]] in $D$ which is [[universal property|universal]] ([[initial object|initial]]) among all morphisms of pro-objects in $D$ with [[domain]] $c$. 

   This second notion is used in [[shape theory]]. An alternative name for this is a **pro-reflective subcategory**, that is a subcategory for which the inclusion has a [[proadjoint]].

### In shape theory
 {#InShapeTheory}

Beware that in [[shape theory]] a different notion of a "dense subcategory" is in use:



\begin{definition}\label{DExpansion}
**(D-expansion)** \linebreak
A _$D$-expansion_ of an [[object]] $X$ in a [[category]] $C$ is a [[morphism]] $X\to \mathbf{X}$ in the category $\mathrm{pro}C$ of [[pro-objects]] such that $\mathbf{X}$ is in $\mathrm{pro}D$ and $X$ is the rudimentary system (constant inverse system) corresponding to $X$; moreover one asks that the morphism is universal among all such morphisms $X\to\mathbf{Y}$. 

\end{definition}

\begin{definition}\label{ShapeDenseSubcategory}
**(shape-dense subcategory)** \linebreak
A [[full subcategory]] $D\subset C$ is __dense__ in the sense of shape theory, if every [[object]] in $C$ admits a $D$-expansion (Def. \ref{DExpansion})

\end{definition}

\begin{remark}
**(abstract shape category)**
Given a shape-dense subcategory $D\subset C$ (Def. \ref{ShapeDenseSubcategory}) one defines an **abstract shape category** $\mathrm{Sh}(C,D)$ which has the same objects as $C$, but the morphisms are the equivalence classes of morphisms in $\mathrm{pro}D$ of $D$-expansions (Def. \ref{DExpansion}).

\end{remark}



## Applications

* A [[dense functor]] $S \hookrightarrow C$ into a [[locally small category]] $C$ induces a good notion of [[nerve]] $N : C \to [S^{op}, Set]$ of objects in $C$ with values in the [[presheaves]] on $S$. See [[nerve]] and [[nerve and realization]] for more on this.

## Related concepts

There is also the notion of "[[dense subsite]]", but this is _not_ a special case of a dense subcategory. 

## Related entries

* [[dense functor]]

* [[codensity monad]]

* [[space and quantity]]

* [[measurable cardinal]]

* [[dense subtopos]]

## Related pages

* [[William Lawvere]], _John Isbell's Adequate Subcategories_ , TopCom **11** no.1 (2006). ([link](http://at.yorku.ca/t/o/p/d/65.htm)) 


## References

* {: #MR0175954 } [[John Isbell]], _Adequate subcategories_ , Illinois J. Math. **4** (1960) pp.541-552. [MR0175954](http://www.ams.org/mathscinet-getitem?mr=0175954) ([euclid](https://projecteuclid.org/euclid.ijm/1255456274)).
 
* [[John Isbell]], _Subobjects, adequacy, completeness and categories of algebras_ , Rozprawy Mat. **36** (1964) pp.1-32. ([toc](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-0dbcb276-0b92-49eb-b504-a9963119ea3e))([full text as pdf](http://pldml.icm.edu.pl/pldml/element/bwmeta1.element.desklight-0dbcb276-0b92-49eb-b504-a9963119ea3e/c/rm36_01.pdf))

* [[John Isbell]], _Small adequate subcategories_ , J. London Math. Soc. **43** (1968) pp.242-246.

* [[John Isbell]], _Locally finite small adequate subcategories_ , JPAA **36** (1985) pp.219-220.

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_ , Cambridge UP 1982. (Reprinted as [TAC reprint no.10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html) (2005); chapter 5, pp.85-112)

* [[Saunders Mac Lane]], _Categories for the Working Mathematician_ , Springer Heidelberg 1998&#178;. (section X.6, pp.245ff, 250)

* Horst Schubert, _Kategorien II_ , Springer Heidelberg 1970. (section 17.2, pp.29ff)

* [[Friedrich Ulmer]], _Properties of dense and relative adjoint functors_ , J. of Algebra **8** (1968) pp.77-95.


[[!redirects dense subcategories]]

[[!redirects pro-reflective subcategory]]
[[!redirects pro-reflective subcategories]]
