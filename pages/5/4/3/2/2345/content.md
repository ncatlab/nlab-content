+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A __$2$-functor__ is the [[categorification]] of the notion of a [[functor]] to the setting of [[2-category|2-categories]]. At the 2-categorical level there are several possible versions of this notion one might want depending on the given setting, some of which collapse to the standard definition of a functor between categories when considered on $2$-categories with discrete hom-categories (viewed as $1$-categories). The least restrictive of these is a [[lax functor]], and the strictest is (appropriately) called a [[strict 2-functor]].

For the various separate definitions that do collapse to standard functors, see:

*  [[strict 2-functor]]
*  [[pseudo functor]]

There is also a notion of '[[lax functor]]', however this notion does not necessarily yield a standard functor when considered on discrete hom-categories.

For the generalisation of this to higher categories, see [[semistrict higher category]].

##Definition##

Here we present explicitly the definition for the middling notion of a pseudofunctor, and comment on alterations that yield the stronger and weaker notions.

####Pseudofunctor

Let $\mathfrak{C}$ and $\mathfrak{D}$ be [[2-categories]]. A pseudofunctor $F:\mathfrak{C}\to\mathfrak{D}$ consists of

* A function $P:Ob_\mathfrak{C}\to Ob_\mathfrak{D}$, and for each pair of objects $A,B\in Ob_\mathfrak{C}$ a functor 

\begin{centre}

$P_{A,B}:\mathfrak{C}(A,B)\to\mathfrak{D}(P(A),P(B)).$ 

\end{centre} 

We will generally write the function and functors as $P$.

* For each pair of horizontally composable 1-cells $(f,g)\in Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$, a $2$-cell isomorphism $\gamma_{f,g}:P(g\circ f)\Rightarrow P(g)\circ P(f)$ called the _associator_ as below 

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell^{P(g\circ f)}_{P(g)\circ P(f)}{\;\;\;\;\gamma_{f,g}} & P(C)

\end{xymatrix}

\end{centre}

* For each object object $A\in Ob_\mathfrak{C}$, a $2$-cell isomorphism $\iota_A:P(1_A)\Rightarrow1_{P(A)}$ called the _unitor_ as below

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell^{P(1_A)}_{1_{P(A)}}{\;\;\;\;\iota_A} & P(A)

\end{xymatrix}

\end{centre}

These are subject to the following two axioms:

1. For any composable triplet of $1$-cells $(f,g,h)\in Ob_{\mathfrak{C}(C,D)}\times Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$\gamma_{f\circ g,h}\circ(\gamma_{f,g}\star 1_{P(h)})=\gamma_{f,g\circ h}\circ(1_{P(f)}\star\gamma_{g,h}),$

\end{centre}

where $\circ$ denotes vertical composition and $\star$ denotes horizontal composition, as illustrated by the following commutative $2$-cell diagram in $\mathfrak{D}(P(A),P(D))$:

\begin{centre}

\begin{xymatrix@R20mm@C20mm}

P(f)\circ P(g)\circ P(h) \ar@2{->}[d]_{\gamma_{f,g}\star 1_{P(h)}} \ar@2{->}[r]^{1_{P(f)}\star\gamma_{g,h}} & P(f)\circ P(g\circ h)\ar@2{->}[d]^{\gamma_{f,g\circ h}} \\ P(f\circ g)\circ P(h)\ar@2{->}[r]_{\gamma_{f\circ g,h}} & P(f\circ g\circ h)

\end{xymatrix}

\end{centre}

2. For any composable $1$-cells $(f,g)\in Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$\iota_B\star 1_{P(B)}=\gamma_{1_B,g},$

\end{centre}

\begin{centre}

$1_{P(f)}\star\iota_B=\gamma_{f,1_B},$

\end{centre}

as illustrated by the commutative $2$-cell diagrams below

\begin{centre}

\begin{xymatrix@R30mm@C35mm}

P(A)\rtwocell^{P(g)}_{P(g)}{\;\;\;\;\;\;1_{P(g)}} \drtwocell<5.5>_{P(g)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\;P(1_B)\circ P(g)}{\;\;\;\;\;\;\;\gamma_{1_B,g}} & P(B) \dtwocell^{\;\;\;\;\;\;P(1_B)}_{1_{P(B)\;\;\;\;\;\;}}{\iota_B} \\ & P(B)

\end{xymatrix} &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  \begin{xymatrix@R30mm@C35mm}

P(B) \rtwocell^{P(1_B)}_{1_{P(B)}}{\;\;\;\;\iota_B} \drtwocell<5.5>_{P(f)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\;P(1_C)\circ P(f)}{\;\;\;\;\;\;\;\gamma_{f,1_B}} & P(B) \dtwocell<4>^{\;\;\;\;P(f)}_{P(f)\;\;\;\;}{1_{P(f)}} \\ & P(C)

\end{xymatrix}

\end{centre}

####Lax Functor

To obtain the notion of a lax functor we only require that the associators $\gamma_{f,g}$ and unitors $\iota_A$ be $2$-cells, not necessarily $2$-cell isomorphisms -- this prevents us from going back and forth between preimages and images of identity $1$-cells and horizontally composed $1$-cells/$2$-cells.

####Strict 2-Functor

To obtain the notion of a strict $2$-functor we require that the associators $\gamma_{f,g}$ and unitors $\iota_A$ be identity arrows, so horizontal composition and $1$-cell identities literally factor through each functor in the same way vertical composition and $2$-cell identities do. 

###Discussion###

There is a notion of a 'weak 2-category', however it usually doesn\'t make sense to speak of strict $2$-functors between weak $2$-categories[^1], but it does make sense to speak of lax (or 'weak') $2$-functors between strict $2$-categories.  Indeed, the weak $3$-[[3-category|category]] [[Bicat]] of bicategories, pseudofunctors, [[pseudonatural transformations]], and [[modifications]] is  [[equivalence of categories|equivalent]] to its full sub-3-category spanned by the strict 2-categories.  However, it is not equivalent to the $3$-category [[Str2Cat]] of strict $2$-categories, *strict* $2$-functors, transformations, and modifications. (For discussion of the terminological choice "$2$-functor" and $n$-functor in general, see [[higher functor]].)

## Related concepts

* [[function]]

* [[functor]]

* **2-functor** / [[pseudofunctor]] / [[(2,1)-functor]]

* [[n-functor]]

* [[(∞,1)-functor]]

* [[(∞,n)-functor]]

[^1]: Although there are certain contexts in which it does.  For instance, there is a [[model structure]] on the category of [[bicategories]] and strict 2-functors between them, which models the homotopy theory of bicategories and weak 2-functors.

[[!redirects 2-functors]]
[[!redirects strict 2-functor]]
[[!redirects strict 2-functors]]