+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

The _Reidemeister moves_ are local changes to [[link diagrams]] which can be realised as [[isotopy|isotopies]] between the link diagrams from which they arise. Because of Reidemeister's theorem, Theorem \ref{TheoremReidemeister}, they are of fundamental importance in knot theory, allowing knots and links to be treated purely combinatorially and diagrammatically. 

The moves were introduced in the book [Reidemeister](#Reidemeister). 

## Definition

The convention below is that part of a [[link diagram]] is shown with the 'move' indicated, but that outside that, the diagram of the link is unchanged. As usual in knot theory, everything is up to planar [[isotopy]].

\begin{defn} The _first Reidemeister move_, or _R1 move_, allows either of the following replacements of a fragment of a link diagram to be made.

[[!include Reidemeister move 1 - SVG]]

\end{defn}

\begin{defn} The _second Reidemeister move_, or _R2 move_, allows either of the following replacements of a fragment of a link diagram to be made.

[[!include Reidemeister move 2 - SVG]]

\end{defn}

\begin{defn} The _third Reidemeister move_, or _R3 move_, allows the following replacement of a fragment of a link diagram to be made.

[[!include Reidemeister move 3 - SVG]]

\end{defn}

\begin{defn} A pair of link diagrams $D$ and $D'$ are  _isotopic_, or _isotopic by moves_, or _equivalent_ if there is a finite sequence of the moves R1, R2 and R3 taking $D$ to $D'$ up to planar isotopy. \end{defn} 

\begin{defn} A pair of link diagrams $D$ and $D'$ are  _regularly isotopic_ if there is a finite sequence of the moves R2 and R3 taking $D$ to $D'$ up to [[planar isotopy]]. \end{defn}

\begin{rmk} Both isotopy and and regular isotopy define equivalence relations on link diagrams. \end{rmk}

\begin{rmk} There are a number of variants of the R3 move. All of them can be obtained as a finite sequence of the Reidemeister moves as defined above. \end{rmk}

##Reidemeister's theorem

The following crucial theorem establishes that the Reidemeister moves are of central significance in knot theory.

\begin{thm} \label{TheoremReidemeister} Let $L_{1}$ and $L_{2}$ be [[links]], and let $D_{1}$ and $D_{2}$ be [[link diagrams]] of $L_{1}$ and $L_{2}$ respectively. Then $D_{1}$ and $D_{2}$ are equivalent if and only if $L_{1}$ is [[isotopy|isotopic]] to $L_{2}$. \end{thm}

The key idea of the proof is that of subdivision. Working piecewise-linearly, one can reduce to the consideration of a few 'minimal' moves on knot diagrams, which one shows can be obtained as a finite sequence of Reidemeister moves. See for example section 2.1 of [Kauffman](#KauffmanKnotDiagrammatics).

##Consequences of Reidemeister's theorem

Because of Theorem \ref{TheoremReidemeister}, we can use the Reidemeister moves to verify invariance of a potential [[link invariant]]. For instance, as none of the moves alters the number of components of a link diagram, the number of components is an isotopy invariant (which is not at all surprising!). We can conclude that the [[Hopf link]] and the [[Borromean rings]] are not isotopic. 

A slightly deeper observation is that the [[linking number]] is a link invariant, for which see that entry.

[[colourable knot|3-colourability]] is a [[knot invariant]] as is easy to check. This shows, for instance, that the trefoil knot is not equivalent to the unknot, and hence shows, very simply, that non-trivial knots exist. It also shows that the figure eight knot is not equivalent to the trefoil.


## Related concepts

* [[Yang-Baxter equation]]


## References

The original article:

* {#Reidemeister} [[Kurt Reidemeister]], _Knotentheorie,_ Ergebnisse der Mathematik (1932)


Simple examples of invariants under the Reidemeister Moves are given in, for instance, the following.

* [[Nick Gilbert]], [[Tim Porter]], *Knots and surfaces*, Oxford University Press (1994) &lbrack;[ISBN:9780198514909](https://global.oup.com/academic/product/knots-and-surfaces-9780198514909?cc=de&lang=en&)&rbrack;

* {#KauffmanKnotDiagrammatics}
 [[Louis Kauffman | Louis H. Kauffman]], _Knot diagrammatics_, Handbook of knot theory, Elsevier, 233 - 318, 2005 [arXiv:math/0410329](https://arxiv.org/abs/math/0410329)

Most texts on [[Knot Theory]] contain discussions of the Reidemeister Moves.

category: knot theory

[[!redirects Reidemeister moves]]
[[!redirects Reidemeister's theorem]]
[[!redirects first Reidemeister move]]
[[!redirects 1st Reidemeister move]]
[[!redirects R1 move]]
[[!redirects second Reidemeister move]]
[[!redirects 2nd Reidemeister move]]
[[!redirects R2 move]]
[[!redirects third Reidemeister move]]
[[!redirects 3rd Reidemeister move]]
[[!redirects R3 move]]


