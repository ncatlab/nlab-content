## Definitions

There are three inequivalent definitions of a proper map in the literature.

The first one is the oldest definition, still found in some analysis books.

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ (or __quasi-proper__) if for every [[compact]] subset $K\subset Y$, the preimage $f^{-1}K$ is a compact subset of $X$.
\end{definition}

The second definition was introduced by [[Bourbaki]] to make proper maps closed under [[base changes]].

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ if it is __universally closed__: every [[base change]] of $f$ is a [[closed map]] of topological spaces.
\end{definition}

Other equivalent characterizations include the following:

* For every [[topological space]] $Z$ the map $f\times id_Z\colon X\times Z\to Y\times Z$ is a [[closed map]].  (The original formulation used by Bourbaki.)

* The map $f$ is quasi-proper and closed.

* The map $f$ is closed and every fiber of $f$ is [[compact]].

The third definition was introduced by [[Grothendieck]].  It is in the same relation to the previous definition as [[compact Hausdorff spaces]] are to [[compact spaces]].

\begin{definition}
A continuous map $f\colon X\to Y$ of [[topological spaces]] is __proper__ if it is universally closed and [[separated map|separated]].
\end{definition}

Recall that $f$ is separated if its relative diagonal $$X\to X\times_Y X$ is a [[closed map]].

If $Y=\{*\}$ is the terminal [[topological space]], then the first two definitions amount to saying $X$ is [[compact]], whereas the last definition makes $X$ compact and [[Hausdorff]].

