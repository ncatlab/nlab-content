

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

A _lens space_ is the [[quotient space]] 

$$
  L\big(n,\{l_i\}_{i=0}^d\big)
  \;\coloneqq\;
  S^{2d+1} / \mathbb{Z}_n
  \;\coloneqq\;
  S
  \big(
    \mathbb{C}_{l_0}
    \oplus
    \cdots
    \oplus
    \mathbb{C}_{l_d}
  \big)
  / \mathbb{Z}_n
$$


of a [[n-sphere|(2d+1)-dimensional sphere]] by a [[free action]] of a [[finite group|finite]] [[cyclic group]] $\mathbb{Z}_n$; specifically -- 
under the identification of $S^{2d+1}$ with the [[unit sphere]] in the [[real vector space]] underlying $\mathbb{C}^{d+1}$ -- 
by the [[action]] induced from a [[linear representation]] of the form

$$
  \array{
    \mathbb{Z}_n 
      \times
    \mathbb{C}^{d+1} 
    &
      \overset{
      }{
        \longrightarrow
      } 
    &
    \mathbb{C}^{d+1}
    \\
    \big(
      [k], (z_0, \cdots, z_{d}) 
    \big)
    &\mapsto&
    \Big(
      \exp( 2 \pi \mathrm{i} \tfrac{l_0}{n} ) \cdot z_0
      ,
      \cdots
      ,
      \exp( 2 \pi \mathrm{i} \tfrac{l_d}{n} ) \cdot z_d
    \Big)
  }
$$

for [[natural numbers]] $l_i$ [[coprime integer|coprime]] to $n$: $gcd(l_i,n) = 1$.

Often this is considered by default for $2d + 1 = 3$, in which case lens spaces are examples of [[3-manifolds]], and as such are in some sense the simplest after the [[3-sphere]] $S^{3}$ and the [[product manifold]] $S^{2} \times S^{1}$ of the [[2-sphere]] with the [[circle]]. 

## Properties

### Homotopy theory

Lens spaces are the only [[3-manifolds]] with [[finite group|finite]], [[cyclic group|cyclic]], [[trivial group|non-trivial]] [[fundamental group]]. The reverse direction of this statement (that a 3-manifold with such a fundamental group must be a lens space) is closely related to the [[Poincaré conjecture]].

Lens spaces are important in [[geometric topology]]. They offer the simplest examples of [[smooth manifolds]] which cannot be distinguished by [[homotopy theory]].

### Via Dehn surgery

The 3-dimensional lens space $L(p,q) \coloneqq L(p, \{1,q\})$, for [[coprime integers]] $p$ and $q$, can be constructed by [[Dehn surgery]] on an [[unknot]] with coefficient $-\frac{p}{q}$. One can instead construct $L(p,q)$ by an _integral_ Dehn surgery on the framed 'generalised Hopf link' 

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

## Related concepts

* [[Seifert 3-manifold]]

## References

See also

* [[Manifold Atlas]], _[Lens spaces](http://www.map.mpim-bonn.mpg.de/Lens_spaces)_.

* Wikipedia, _[Lens space](https://en.wikipedia.org/wiki/Lens_space)_.

In the context of [[orbifolds]]:

* Siddhartha Gadgil, _Equivariant framings, lens spaces and contact structures_, Pacific Journal of Mathematics, Vol. 208 (2003), No. 1, 73–84 ([doi:10.2140/pjm.2003.208.73](http://dx.doi.org/10.2140/pjm.2003.208.73))

* Michel Boileau, Steven Boyer, Radu Cebanu, Genevieve S. Walsh, Section 3 of: _Knot commensurability and the Berge conjecture_, Geom. Topol. 16 (2012) 625-664 ([arXiv:1008.1034](https://arxiv.org/abs/1008.1034))

On the [[3d-3d correspondence]] for lens spaces:

* [[Du Pei]], Chapter III of: _3d-3d correspondence for Seifert manifolds_, 2016 ([spire:1469350](https://inspirehep.net/literature/1469350), [pdf](https://inspirehep.net/files/d509ff9e32448da3a5674f286b93224a))




[[!redirects lens spaces]]