
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


\tableofcontents

\section{Introduction}

The _longitude_ of a [[knot]], or more generally of a component of a [[link]], plays a crucial role in the link-theoretic approach to [[3-manifolds]] by means of the [[Lickorish-Wallace theorem]] and the [[Kirby calculus]]. It can be defined either geometrically or combinatorially. 

\section{Combinatorial definition}

The longitude of a knot or of a link component can be defined purely within [[diagrammatic knot theory]]. We describe this in this section.

\begin{defn} \label{DefinitionLongitudeOfALinkComponent} Let $C$ be a component of a [[link diagram]] $L$, viewed as defining a link with the [[blackboard framing]]. Pick an [[orientation of a link diagram|orientation]] of $L$, and pick a point $p$ of $C$. The _longitude_ of $C$ with respect to $p$ and the chosen orientation of $L$ is the [[word]] in the [[free group]] of the set of [[arc of a link diagram|arcs]] of $L$ defined inductively as follows. 

1) Begin at $p$ with the empty word.

2) Walk along $L$ following the orientation of $L$ until one reaches a crossing of $L$ which one approaches by means of an under-edge (one does not stop at crossings which one approaches and leaves by means of over-edges). If the orientations of the crossings are as follows, add $a$ to the end of the word obtained thus far.

\begin{centre}

\begin{tikzpicture}

\draw[->, semithick] (0,1) -- (0,-1);
\draw[shorten >= 0.5em, semithick] (-1,0) -- (0,0);
\draw[->, shorten <= 0.5em, semithick] (0,0) -- (1,0);

\node[anchor=north] at (0,-1) {$a$};

\end{tikzpicture}

\end{centre}

If the orientations of the arcs of the crossing are instead as follows, add  $a^{-1}$ to the end of the word obtained thus far.

\begin{centre}

\begin{tikzpicture}

\draw[<-, semithick] (0,1) -- (0,-1);
\draw[shorten >= 0.5em, semithick] (-1,0) -- (0,0);
\draw[->, shorten <= 0.5em, semithick] (0,0) -- (1,0);

\node[anchor=north] at (0,-1) {$a$};

\end{tikzpicture}

\end{centre}

The arc $a$ is not required to, and may not, belong to $C$. 

3) Repeat Step 2) until we return to $p$.

\end{defn}

\begin{rmk} There is an alternative definition if one works with [[framed link diagrams]], which involves first replacing one's original link diagram with one to which a certain number of twists (i.e. [[R1 move|R1 moves]]) have been applied according to the framing, and then using Definition \ref{DefinitionLongitudeOfALinkComponent}. \end{rmk}

\begin{example} Consider the [[trefoil]] with a chosen point $p$ and orientation as shown below. Labels have been chosen for the arcs. 

\begin{centre}

\begin{tikzpicture}

\usetikzlibrary{decorations.markings}

\path (-2.5,-2.5) -- (-2.5,1.5) -- (3.5,1.5) -- (2.5,-2.5) -- (2.5,-2.5);

\draw[semithick, shorten <= 0.5em, shorten >= 0.5em] (2,0) -- (0,0) -- (0,-1) -- (1,-1);
\draw[semithick, shorten <= 0.5em, shorten >= 0.5em] (1,-1) -- (2,-1) -- (2,1) -- (1,1) -- (1,0);
\draw[semithick, shorten <= 0.5em, shorten >= 0.5em] (1,0) -- (1,-2) -- (3,-2) -- (3,0) -- (2,0);

\filldraw[black] (0,-0.5) circle (2pt);

\node[anchor=south] at (0.5,0) {$a$};
\node[anchor=north] at (1.6,-1) {$b$};
\node[anchor=east] at (1,-1.6) {$c$};

\node at (-0.25, -0.5) {$p$};

\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (2,-1) -- (2,0);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (2,1) -- (1,1);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (2,0) -- (1,0);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (1,-2) -- (3,-2);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (0,-1) -- (1,-1);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (3,-2) -- (3,0);

\end{tikzpicture}

\end{centre}

The longitude of the trefoil with respect to $p$ and this orientation is then $c a b$.

\end{example} 

\begin{example} Consider the [[Hopf link]], in which both components have been equipped with a chosen point and an orientation as shown below. Labels have been chosen for the arcs. 

\begin{centre}

\begin{tikzpicture}

\usetikzlibrary{decorations.markings}

\path (-1.5, -2.5) -- (-1.5, 1.5) -- (2.5, 1.5) -- (2.5, -2.5) -- (-1.5, -2.5);

\draw[semithick, shorten <= 0.5em, shorten >= 0.5em] (0,-1) -- (1,-1) -- (1,1) -- (-1,1) -- (-1,-1) -- (0,-1);
\draw[semithick, shorten <= 0.5em, shorten >= 0.5em] (1,0) -- (0,0) -- (0,-2) -- (2,-2) -- (2,0) -- (1,0);

\filldraw[black] (0,1) circle (2pt);
\filldraw[black] (2,-1) circle (2pt);

\node[anchor=east] at (-1,-0.5) {$a$};
\node[anchor=north] at (1,-2) {$b$};

\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (-1,-1) -- (-1,1);
\path[decoration = { markings, mark=at position 0.65 with {\arrow[scale=2]{<}}}, postaction = {decorate}] (0,-1) -- (1,-1);
\path[decoration = { markings, mark=at position 0.5 with {\arrow[scale=2]{<}}}, postaction = {decorate}] (0,-2) -- (0,-1);
\path[decoration = { markings, mark=at position 0.55 with {\arrow[scale=2]{>}}}, postaction = {decorate}] (2,0) -- (1,0);

\end{tikzpicture}

\end{centre}

The longitude of the component to which the arc $a$ belongs is $b^{-1}$. The longitude of the component to which the arc $b$ belongs is $a^{-1}$. 

\end{example} 

\begin{rmk} The longitude of a component of an oriented link diagram is unique up to [[rotation permutation]]: the longitude obtained using any one choice of $p$ is a rotation permutation of the longitude obtained using any other choice of $p$. 

When it comes to 3-manifolds, for example when describing the [[fundamental group]], everything is typically invariant under rotation permutation. Thus it is usual to speak of _the_ longitude of a component of an oriented link diagram. \end{rmk}

category: knot theory


[[!redirects longitude of a knot]]