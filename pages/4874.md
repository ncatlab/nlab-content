+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

A _link diagram_ is, roughly speaking, the combinatorial object obtained by projecting a [[link]] in 'general position' to a plane. [[Reidemeister's theorem]] establishes that one does not lose any essential information by passing from a link to its diagram, and thus it is possible to study knot theory in a way which takes link diagrams as primary: this is sometimes known as [[diagrammatic knot theory]].

## Formal definition

The formal definition of a link diagram is in itself independent of the notion of a [[link]].

\begin{defn} \label{DefinitionConnectedLinkDiagram} A _connected link diagram_ is a [[connected graph|connected]] (undirected) 4-valent [[plane graph]] $G$ equipped with the following data for every vertex $v$ of $G$.

1. A choice of division of the four edges incident to $v$ into two pairs, say $(e_{0}, e_{1})$ and $(e_{2}, e_{3})$. We refer to the two edges in the first pair as _over-edges_, and to the two edges $(e_{1}, e_{2})$ in the second pair as _under-edges_.

1. A cyclic ordering of the four edges of $G$ incident to $v$ so that the over-edges and under-edges alternate.

\end{defn} 

\begin{defn} \label{DefinitionLinkDiagram} A _link diagram_ is a planar graph such that each connected component satisfies either 1. or 2. below.

1. It is (up to homeomorphism) a circle, disjoint from the rest of the link diagram.

1. It is a connected link diagram in the sense of Definition \ref{DefinitionConnectedLinkDiagram}. 

\end{defn}

\begin{rmk} It is important to note that a plane graph consists, by definition, of an abstract [[graph]] together with a _chosen_ embedding into the plane. There exist non-equivalent link diagrams which have the same underlying abstract graph, but for which the embedding in the plane is different. \end{rmk}

\begin{terminology} A component of a link diagram which satisfies 1. in Definition \ref{DefinitionLinkDiagram} is typically referred to as an _unknot_, or an _unknotted component_. \end{terminology}

\begin{terminology} \label{TerminologyCrossingsOfALinkDiagram} The vertices $v$ of a link diagram $L$ which do not belong to an unknotted component, together with the data of 1. and 2. in Definition \ref{DefinitionConnectedLinkDiagram} for $v$, are referred to as the _crossings_ of $L$. 

\end{terminology}

## Obtaining a link diagram from a link

A link diagram can be obtained from a [[link]] by choosing a plane in $\mathbb{R}^{3}$, and projecting the link onto this plane. A small change in the direction of projection will ensure that it is one-to-one except at the double points, which will become the crossings of the link diagram in the sense of Terminology \ref{TerminologyCrossingsOfALinkDiagram}, where the image curve of the knot crosses itself once transversely. Which strand of the two intersecting at the double point is the 'over strand' and which is the 'under strand' is recorded as the data needed for 1. and 2. in Definition \ref{DefinitionConnectedLinkDiagram}.

Consider for example the parallel projection

$$p: \mathbb{R}^3 \to \mathbb{R}^2$$

defined by $p(x,y,z) = (x,y,0)$.  

(If you prefer your knots to be in $S^3$, of course, you can remove a single point from the complement of $K$ and then project down to $\mathbf{R}^3$. It does not matter which point you use.)

A point $\mathbf{x}$ in the image $pK$ is called a *multiple point* if $p^{-1}(\mathbf{x})$ contains more than one point of $K$.  A *double point* occurs when there are exactly two points of $K$ in this, and similarly for a *triple point*, etc. Multiple points of infinite order could occur.

A knot is in *regular position* or _general position_ with respect to $p$ if there are only double points and these are genuine crossings (i.e. no tangential touching occurs in the projected curve).

Any smooth or PL link $L$ is equivalent under an arbitrarily small rotation of $\mathbf{R}^3$ to one in regular position with respect to $p$.

A proof can be found in Crowell and Fox (page 7). 

\begin{terminology} A _knot diagram_ is a link diagram which arises from a projection of a [[knot]]. 
\end{terminology}

## Related concepts

* [[Reidemeister move]]

category: knot theory

[[!redirects knot diagram]]
[[!redirects knot diagrams]]
[[!redirects link diagrams]]