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

## Idea

The left part of a pair of [[adjoint functor]]s is one of two best approximations to a [[weak inverse]] of the other functor of the pair.  (The other best approximation is the functor's [[right adjoint]], if it exists.)  Note that a weak inverse itself, if it exists, must be a left adjoint, forming an [[adjoint equivalence]].

A left adjoint to a [[forgetful functor]] is called a [[free functor]]. Many left adjoints can be constructed as quotients of free functors.

The concept generalises immediately to [[enriched category|enriched categories]] and in [[2-category|2-categories]].


## Definitions

\subsection{For categories}

\begin{defn} \label{DefinitionLeftAdjointForCategories} Given categories $\mathcal{C}$ and $\mathcal{D}$ and a functor $R: \mathcal{D} \to \mathcal{C}$, a _left adjoint_ of $R$ is a functor $L: \mathcal{C} \to \mathcal{D}$ together with [[natural transformation|natural transformations]]
$\iota: id_\mathcal{C} \to R \circ L$ and $\epsilon: L \circ R \to id_\mathcal{D} $ such that the following diagrams (known as the [[triangle identities]]) commute, where $\cdot$ denotes [[whiskering]] of a functor with a natural transformation.

\begin{centre}
  \begin{tikzcd} 
    L \ar[r, "L \cdot \iota"] \ar[dr, swap, "id"] & L \circ R \circ L \ar[d, "\epsilon \cdot L"] \\
                                                     & L 
  \end{tikzcd}
\end{centre}

\begin{centre}
  \begin{tikzcd} 
    R \ar[r, "\iota \cdot R"] \ar[dr, swap, "id"] & R \circ L \circ R \ar[d, "R \cdot \epsilon"] \\
                                                     & R 
  \end{tikzcd}
\end{centre}
 
\end{defn}

\begin{rmk} \label{RemarkEquivalentDefinitionLeftAdjointForCategories} Definition \ref{DefinitionLeftAdjointForCategories} is equivalent to requiring that there is a [[natural isomorphism]] between the [[hom-functor|Hom functors]]

$$ 
  Hom_\mathcal{C}\left(L(-),-\right), Hom_\mathcal{D}\left(-,R(-)\right): D^{op} \times C \to \mathsf{Set}.
$$

Depending upon one's interpretation of $\mathsf{Set}$, the [[category of sets]], one may strictly speaking need to restrict to [[locally small category|locally small]] categories for this equivalence to parse. 
\end{rmk}

\subsection{For enriched categories}

The equivalent formulation of Definition \ref{DefinitionLeftAdjointForCategories} given in Remark \ref{RemarkEquivalentDefinitionLeftAdjointForCategories} generalises immediately to the setting of [[enriched category|enriched categories]].

\begin{defn} Given $\mathbb{V}$-enriched categories $\mathcal{C}$ and $\mathcal{D}$ and a $\mathbb{V}$-[[enriched functor]] $R: \mathcal{D} \to \mathcal{C}$, a _left adjoint_ of $R$ is a $\mathbb{V}$-enriched functor $L: \mathcal{C} \to \mathcal{D}$ together with a $\mathbb{V}$-[[enriched natural transformation|enriched natural isomorphism]] between the [[hom-functor|Hom functors]]

$$ 
  Hom_\mathcal{C}\left((L(-),-\right), Hom_\mathcal{D}\left(-,R(-)\right): D^{op} \times C \to \mathbb{V}.
$$

\end{defn}

\subsection{In a 2-category}

Definition \ref{DefinitionLeftAdjointForCategories} generalises immediately from [[CAT]], the 2-category of (large) categories, to any [[2-category]].

\begin{defn} \label{DefinitionLeftAdjointInA2Category} Let $\mathcal{A}$ be a 2-category. Given objects $\mathcal{C}$ and $\mathcal{D}$ and a 1-arrow $R: \mathcal{D} \to \mathcal{C}$ of $\mathcal{A}$, a _left adjoint_ of $R$ is a 1-arrow $L: \mathcal{C} \to \mathcal{D}$ together with 2-arrows
$\iota: id_\mathcal{C} \to R \circ L$ and $\epsilon: L \circ R \to id_\mathcal{D} $ such that the following diagrams commute, where $\cdot$ denotes [[whiskering]] in $\mathcal{A}$.

\begin{centre}
  \begin{tikzcd} 
    L \ar[r, "L \cdot \iota"] \ar[dr, swap, "id"] & L \circ R \circ L \ar[d, "\epsilon \cdot L"] \\
                                                     & L 
  \end{tikzcd}
\end{centre}

\begin{centre}
  \begin{tikzcd} 
    R \ar[r, "\iota \cdot R"] \ar[dr, swap, "id"] & R \circ L \circ R \ar[d, "R \cdot \epsilon"] \\
                                                     & R 
  \end{tikzcd}
\end{centre}
 
\end{defn}

\begin{rmk} If one assumes that one's ambient 2-category has more structure, bringing it closer to being a [[2-topos]], for example a [[Yoneda structure]], one should be able to give an equivalent formulation of Definition \ref{DefinitionLeftAdjointInA2Category} akin to that of Remark \ref{RemarkEquivalentDefinitionLeftAdjointForCategories}.  \end{rmk} 

\subsection{For preorders and posets}

Restricted to [[preorder|preorders]] or [[poset|posets]], Definition \ref{DefinitionLeftAdjointForCategories} in its equivalent formulation of Remark \ref{RemarkEquivalentDefinitionLeftAdjointForCategories} can be expressed in the following terminology.

\begin{defn} Given [[partial order|posets]] or [[preorder|preorders]] $\mathcal{C}$ and $\mathcal{D}$ and a [[monotone function]] $R: \mathcal{D} \to \mathcal{C}$, a _left adjoint_ of $R$ is a monotone function $L: \mathcal{C} \to \mathcal{D}$ such that, for all $x$ in $\mathcal{D}$ and $y$ in $\mathcal{C}$, we have that $L(x) \leq y$ holds if and only if $x \leq R(y) $ holds. \end{defn}



## Properties

* [[left adjoints preserve colimits]]

* left adjoints preserve [[epimorphisms]].

### In homotopy type theory
 {#InHomotopyTypeTheory}

Note: the [[HoTT book]] calls a [[internal category in HoTT]] a "precategory" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

\begin{lemma}\label{Lemma932}
**(Lemma 9.3.2 in the [[HoTT book]])**
\linebreak
If $A$ is an [[univalent category]] and $B$ is a [[category]] then the type "$F$ is a left adjoint" is a [[mere proposition]].
\end{lemma}

\begin{proof}
Suppose we are given $(G, \eta, \epsilon)$ with the triangle identities and also $(G', \eta', \epsilon')$. Define $\gamma: G \to G'$ to be $(G' \epsilon )(\eta G')$. Then

$$ \begin{aligned}
  \delta \gamma &= (G \epsilon')(\eta G')(G' \epsilon) (\eta' G)\\
  &= (G \epsilon')(G F G' \epsilon_))\eta G' F G)(\eta' G)\\
  &= (G \epsilon ')(G \epsilon' F G)(G F \eta' G)(\eta G)\\
  &= (G \epsilon)(\eta G)\\
  &= 1_G
\end{aligned} $$
using Lemma 9.2.8 (see [[natural transformation]]) and the triangle identities. Similarly, we show $\gamma \delta=1_{G'}$, so $\gamma$ is a [[natural isomorphism]] $G \cong G'$. By Theorem 9.2.5 (see [[functor category]]), we have an [[identity]] $G=G'$.

Now we need to know that when $\eta$ and $\epsilon$ are [[transported]] along this [[identity]], they become equal to $\eta'$ and $\epsilon '$. By Lemma 9.1.9,

+--{.query}
Lemma 9.1.9 needs to be included. For now as transports are not yet written up I didn't bother including a reference to the page [[category]]. -Ali
=--

this [[transport]] is given by composing with $\gamma$ or $\delta$ as appropriate. For $\eta$, this yields

$$(G' \epsilon F)(\eta' G F)\eta = (G' \epsilon F)(G' F \eta)\eta'=\eta'$$

using Lemma 9.2.8 (see [[natural transformation]]) and the traingle identity. The case of $\epsilon$ is similar. FInally, the triangle identities transport correctly automatically, since hom-sets are sets.
\end{proof}

\section{Examples}

* The left adjoint of the [[nerve functor]] $N: \mathsf{Grpd} \to \mathsf{Set}^{\Delta^{op}}$ from the [[category of groupoids]] to the [[category of simplicial sets]] is the [[fundamental groupoid]] functor. 

## Related entries

* [[Galois connection]] for more on left adjoints of monotone functions.
* [[adjoint functor]] for more on left adjoints of functors.
* [[adjunction]] for more on left adjoints in $2$-categories.
* [[examples of adjoint functors]] for examples.
* [[pro-left adjoint]]
* [[2-adjunction]] for a categorified notion of adjunction.

[[!redirects left adjoints]]

[[!redirects left adjoint functor]]
[[!redirects left adjoint functors]]
