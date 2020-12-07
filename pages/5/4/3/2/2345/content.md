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

####Pseudofunctor between strict $2$-categories

Let $\mathfrak{C}$ and $\mathfrak{D}$ be strict [[2-categories]]. A pseudofunctor $P:\mathfrak{C}\to\mathfrak{D}$ consists of

* A function $P:Ob_\mathfrak{C}\to Ob_\mathfrak{D}$.

* For each pair of objects $A,B\in Ob_\mathfrak{C}$ a functor 

\begin{centre}

$P_{A,B}:\mathfrak{C}(A,B)\to\mathfrak{D}(P(A),P(B)).$ 

\end{centre} 

We will generally write the function and functors as $P$.

* For each triplet of objects $A,B,C\in Ob_\mathfrak{C}$, a natural isomorphism

\begin{centre}

\begin{xymatrix@C20mm}

\mathfrak{C}(B,C)\times\mathfrak{C}(A,B) \rtwocell^{P\circ\Gamma}_{\Gamma\circ(P\times P)}{\gamma} & \mathfrak{D}(P(A),P(C))

\end{xymatrix}

\end{centre}

whose components are $2$-cell isomorphisms $\gamma_{f,g}:P(f\circ g) \Rightarrow P(f)\circ P(g)$ as below 

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell_{P(f)\circ P(g)}^{P(f\circ g)}{\;\;\;\;\gamma_{f,g}} & P(C)

\end{xymatrix}

\end{centre}

* For each object object $A\in Ob_\mathfrak{C}$, a natural isomorphism

\begin{centre}

\begin{xymatrix@C20mm}

1 \rtwocell^{P\circ id_A\;\;\;\;\;\;}_{id_{P(A)}\;\;\;\;\;\;}{\iota\;\;\;\;\;\;\;\;\;\;} & \mathfrak{D}(P(A),P(A))

\end{xymatrix}

\end{centre}

where $1$ denotes the terminal category and $id_A$ is the identity-selecting functor at $A$. Its component is a $2$-cell isomorphism $\iota_{_*}:P(1_A)\Rightarrow 1_{P(A)}$ as below

\begin{centre}

\begin{xymatrix@C20mm}

P(A) \rtwocell_{1_{P(A)}}^{P(1_A)}{\;\;\;\;\iota_*} & P(A)

\end{xymatrix}

\end{centre}

These are subject to the following axioms:

1. For any composable triplet of $1$-cells $(f,g,h)\in Ob_{\mathfrak{C}(C,D)}\times Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$(\gamma_{f,g}\star 1_{P(h)})\circ\gamma_{f\circ g,h}=(1_{P(f)}\star\gamma_{g,h})\circ\gamma_{f,g\circ h},$

\end{centre}

where $\circ$ denotes vertical composition and $\star$ denotes horizontal composition, as illustrated by the following commutative $2$-cell diagram in $\mathfrak{D}(P(A),P(D))$:

\begin{centre}

\begin{xymatrix@R20mm@C20mm}

P(f)\circ P(g)\circ P(h) & \ar@2{->}[l]_{1_{P(f)}\star\gamma_{g,h}} P(f)\circ P(g\circ h) \\ P(f\circ g)\circ P(h) \ar@2{->}[u]^{\gamma_{f,g}\star 1_{P(h)}} & \ar@2{->}[l]^{\gamma_{f\circ g,h}} \ar@2{->}[u]_{\gamma_{f,g\circ h}} P(f\circ g\circ h)

\end{xymatrix}

\end{centre}

2. For any composable $1$-cells $(f,g)\in Ob_{\mathfrak{C}(B,C)}\times Ob_{\mathfrak{C}(A,B)}$ we have that 

\begin{centre}

$\iota_B\star 1_{P(g)}=\gamma_{1_B,g}^{-1},$

\end{centre}

\begin{centre}

$1_{P(f)}\star\iota_B=\gamma_{f,1_B}^{-1},$

\end{centre}

as illustrated by the commutative $2$-cell diagrams below

\begin{centre}

\begin{xymatrix@R30mm@C35mm}

P(A)\rtwocell^{P(g)}_{P(g)}{\;\;\;\;\;\;1_{P(g)}} \drtwocell<5.5>_{P(g)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\; P(1_B)\circ P(g)}{\;\;\;\;\;\;\;\gamma_{1_B,g}^{-1}} & P(B) \dtwocell^{\;\;\;\;\;\;P(1_B)}_{1_{P(B)\;\;\;\;\;\;}}{\iota_B} \\ & P(B)

\end{xymatrix} &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;  \begin{xymatrix@R30mm@C35mm}

P(B) \rtwocell^{P(1_B)}_{1_{P(B)}}{\;\;\;\;\iota_B} \drtwocell<5.5>_{P(f)\;\;\;\;\;}^{\;\;\;\;\;\;\;\;\;\;\;\;\;\; P(f)\circ P(1_B)}{\;\;\;\;\;\;\;\gamma_{f,1_B}^{-1}} & P(B) \dtwocell<4>^{\;\;\;\;P(f)}_{P(f)\;\;\;\;}{1_{P(f)}} \\ & P(C)

\end{xymatrix}

\end{centre}

####Lax Functor

To obtain the notion of a __lax functor__ we only require that the coherence morphisms $\gamma_{f,g}$ and $\iota_A$ be $2$-cells, not necessarily $2$-cell isomorphisms.  This prevents us from going back and forth between preimages and images of identity $1$-cells and horizontally composed $1$-cells/$2$-cells.  Similarly, to obtain an __oplax functor__ we reverse the direction of these 2-cells.

####Strict 2-Functor

To obtain the notion of a strict $2$-functor we require that $\gamma_{f,g}$ and $\iota_A$ are identity arrows, so horizontal composition and $1$-cell identities literally factor through each functor in the same way vertical composition and $2$-cell identities do. 

###Discussion###

There is a notion of a 'weak 2-category', however it usually doesn\'t make sense to speak of strict $2$-functors between weak $2$-categories[^1], but it does make sense to speak of lax (or 'weak') $2$-functors between strict $2$-categories.  Indeed, the weak $3$-[[3-category|category]] [[Bicat]] of bicategories, pseudofunctors, [[pseudonatural transformations]], and [[modifications]] is  [[equivalence of categories|equivalent]] to its full sub-3-category spanned by the strict 2-categories.  However, it is not equivalent to the $3$-category [[Str2Cat]] of strict $2$-categories, *strict* $2$-functors, transformations, and modifications. (For discussion of the terminological choice "$2$-functor" and $n$-functor in general, see [[higher functor]].)

## Related concepts

* [[function]]

* [[functor]]

* **2-functor** / [[pseudofunctor]] / [[(2,1)-functor]]

* [[n-functor]]

* [[(∞,1)-functor]]

* [[(∞,n)-functor]]


[[!include properties of functors -- contents]]



[^1]: Although there are certain contexts in which it does.  For instance, there is a [[model structure]] on the category of [[bicategories]] and strict 2-functors between them, which models the homotopy theory of bicategories and weak 2-functors.

[[!redirects 2-functors]]
[[!redirects strict 2-functor]]
[[!redirects strict 2-functors]]