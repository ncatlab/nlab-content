

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _lens space_ is an example of a [[3-manifold]], the simplest after the [[3-sphere]] $S^{3}$ and $S^{2} \times S^{1}$. Lens spaces are the only 3-manifolds with [[finite group|finite]], [[cyclic group|cyclic]], [[trivial group|non-trivial]] [[fundamental group]]. Proving the reverse direction of this (that a 3-manifold with such a fundamental group must be a lens space) is closely related to the [[Poincaré conjecture]].

Lens spaces are very important in [[geometric topology]]. They offer the simplest examples of [[smooth manifolds]] which cannot be distinguished by [[homotopy theory]].

There is a lens space $L(p,q)$ for every [[pair]] of [[integers]] $p$ and $q$, which can be constructed by [[Dehn surgery]] on an [[unknot]] with coefficient $-\frac{p}{q}$. One can instead construct $L(p,q)$ by an _integral_ Dehn surgery on the framed 'generalised Hopf link' 

\begin{centre}
  \begin{tikzpicture}
     \draw[shorten >= 0.5em] (0,0) -- (2,0) -- (2,-1);
     \draw[shorten <= 0.5em] (2,-1) to (2,-2) to node[auto] {$a_{1}$} (0,-2) to (0,0);
     \draw[shorten >= 0.5em] (1,1) -- (1,0);
     \draw[shorten <= 0.5em, shorten >= 0.5em] (1,0) -- (1,-1) -- (2.25,-1);
     \draw[shorten <= 0.5em] (2.25, -1) to (3,-1) to (3,1) to node[auto, swap] {$a_{2}$} (1,1);
     \draw[shorten >= 0.5em] (4.25,0) -- (3,0);
     \draw[shorten <= 0.5em] (3,0) to (2.25,0) to (2.25,-2) to node[auto, swap] {$a_{3}$} (4.25,-2);
     \node at (5, -1) {$\cdots$}; 
     \draw[shorten >= 0.5em] (6,1) to node[auto] {$a_{n-1}$} (8,1) to (8,-1) to (7,-1); 
     \draw[shorten <= 0.5em] (7,-1) -- (6,-1);
     \draw[shorten >= 0.5em] (9,0) -- (8,0);
     \draw[shorten <= 0.5em] (8,0) to (7,0) to (7,-2) to node[auto, swap] {$a_{n}$} (9,-2) to (9,0); 
  \end{tikzpicture}
\end{centre}

where the unknots have framings $a_{1}$, $\ldots$, $a_{n}$ from left to right, for a [[continued fraction]] representation of $-\frac{p}{q}$ as follows.

$$
a_{1} - \frac{1}{a_{2} - \frac{1}{\cdots - \frac{1}{a_{n}}}}
$$

## References

See also

* [[Manifold Atlas]], _[Lens spaces](http://www.map.mpim-bonn.mpg.de/Lens_spaces)_.

* Wikipedia, _[Lens space](https://en.wikipedia.org/wiki/Lens_space)_.

For [[orbifolds]]:

* Siddhartha Gadgil, _Equivariant framings, lens spaces and contact structures_, Pacific Journal of Mathematics, Vol. 208 (2003), No. 1, 73–84 ([doi:10.2140/pjm.2003.208.73](http://dx.doi.org/10.2140/pjm.2003.208.73))

[[!redirects lens spaces]]