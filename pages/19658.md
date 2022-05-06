\tableofcontents

\section{Introduction}

The _longitude_ of a [[knot]], or more generally of a component of a [[link]], plays a crucial role in the link-theoretic approach to [[3-manifolds]] by means of the [[Lickorish-Wallace theorem]] and the [[Kirby calculus]]. It can be defined either geometrically or combinatorially. 

\section{Combinatorial definition}

The longitude of a knot or of a link component can be defined purely within [[diagrammatic knot theory]]. We describe this in this section.

\begin{defn} Let $C$ be a component of a [[link diagram]] $L$. Pick an orientation of $L$, and pick a point $p$ of $C$. The _longitude_ of $C$ with respect to $p$ and the chosen orientation of $L$ is the [[word]] in the [[free group]] of the set of [[arcs|arc of a link diagram]] of $L$ defined inductively as follows. 

1. Begin at $p$ with the empty word.

1. Walk along $L$ following the orientation of $L$ until one reaches a crossing of $L$ which one approaches by means of an under-edge (one does not stop at crossings which one approaches and leaves by means of over-edges). If the orientation of the crossing is as follows, add the arc $a$ to the end of the word obtained thus far.

\begin{tikzpicture}

\draw[->] (0,1) -- (0,-1);
\draw[shorten >= 0.5em] (-1,0) -- (0,0);
\draw[->, shorten <= 0.5em] (0,0) -- (1,0);

\end{tikzpicture}

If the orientation of the crossing is instead as follows, add the arc $a^{-1}$ to the end of the word obtained thus far.

\begin{tikzpicture}

\draw[<-] (0,1) -- (0,-1);
\draw[shorten >= 0.5em] (-1,0) -- (0,0);
\draw[->, shorten <= 0.5em] (0,0) -- (1,0);

\end{tikzpicture}

The arc $a$ is not required to, and may not, belong to $C$. 

1. Repeat Step 2. until we return to $p$.

\end{defn}

[[!redirects longitude of a knot]]