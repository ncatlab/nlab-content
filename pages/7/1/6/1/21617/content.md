

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


of a [[n-sphere|(2d+1)-dimensional sphere]] by a [[free action]] of a [[finite group|finite]] [[cyclic group]] $\mathbb{Z}_n$ (cf. *[[group actions on spheres]]*); specifically --- under the identification of $S^{2d+1}$ with the [[unit sphere]] in the [[real vector space]] [[underlying]] $\mathbb{C}^{d+1}$ --- by the [[action]] induced from a [[linear representation]] of the form

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
      \exp\big( 
        2 \pi \mathrm{i} \tfrac{l_0}{n} 
      \big) 
      \cdot z_0
      ,\,
      \cdots
      ,\,
      \exp\big( 
        2 \pi \mathrm{i} \tfrac{l_d}{n} 
      \big) 
      \cdot z_d
    \Big)
    \,m
  }
$$

for [[natural numbers]] $l_i \in \mathbb{N}$ [[coprime integer|coprime]] to $n$: $gcd(l_i,n) = 1$.

Often this is considered by default for $2d + 1 = 3$, in which case lens spaces are examples of [[3-manifolds]], and as such are in some sense the simplest after the [[3-sphere]] $S^{3}$ and the [[product manifold]] $S^{2} \times S^{1}$ of the [[2-sphere]] with the [[circle]]. 


## Properties

### Classification

\begin{theorem}

Two lens spaces $L\big(n,\{l_i\}_{i=0}^d\big)$ and $L\big(n,\{l'_i\}_{i=0}^d\big)$ are [[homotopy equivalent]] iff there exists a $k\in\mathbb{N}$ with
$$
  l_0\cdot\ldots\cdot l_d
  \;\equiv\; 
  k^d l'_0 \cdot \ldots \cdot l'_d \mod n
  \,.
$$
\end{theorem}

([Olum 1953](#Olum53))

\begin{theorem}
Two lens spaces $L\big(n,\{l_i\}_{i=0}^d\big)$ and $L\big(n,\{l'_i\}_{i=0}^d\big)$ are [[homeomorphic]] iff there exists a $k\in\mathbb{N}$ and a [[permutation]] $\sigma\in Sym_d$ with
$$
  l_i
  \;\equiv\; 
  \pm k l'_{\sigma(i)} \mod n
$$
for all $i=0,\ldots, d$.

\end{theorem}

([Brody 1960](#Brody60), [Milnor 1966](#Milnor66))

In both theorems, the same $n$ for both lens spaces is a necessary condition for them to be [[homeomorphic]] or [[homotopy equivalent]] as follows with their respective [[fundamental group]].

### Cohomology
 {#Cohomology}

The [[ordinary cohomology|ordinary]] [[integral cohomology]] of the lens space $L(n,q) \coloneqq L\big(n,\{q,q, \cdots, q\}\big)$ is &lbrack;e.g. [Maxim, p. 2](#Maxim)&rbrack;:

\[
  \label{IntegralCohomologyOfLensSpace}
  H^i
  \big(
    L(n,q)
    ;\,
    \mathbb{Z}
  \big)
  \;\;
  \simeq
  \;\;
  \left\{
    \begin{array}{lcl}
      \mathbb{Z} &\vert& i = 0
      \\
      \mathbb{Z}\!/\!q &\vert& i = 2j \leq 2n
      \\
      \mathbb{Z} &\vert& i = 2n + 1
      \\
      0 &\vert& \text{otherwise,}
    \end{array}
  \right.
\]

(where $\mathbb{Z}\!/\!q$ is the [[cyclic group]] or [[order of a group|order]] $q$, hence a [[torsion group]]).


### Homotopy

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

where the unknots have [[framed knot|framings]] $a_{1}$, $\ldots$, $a_{n}$ from left to right, for a [[continued fraction]] representation of $-\frac{p}{q}$ as follows.

$$
  a_{1} - \frac{1}{a_{2} - \frac{1}{\cdots - \frac{1}{a_{n}}}}
$$

\linebreak

\begin{imagefromfile}
    "file_name": "EHI-SurgeryForLensSpace.jpg",
    "width": 670,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [EHI 2020](#EHI20)"
\end{imagefromfile}


[[:file]]


## Related concepts

* [[Seifert 3-manifold]]


## References

See also

* [[Manifold Atlas]], _[Lens spaces](http://www.map.mpim-bonn.mpg.de/Lens_spaces)_.

* Wikipedia, _[Lens space](https://en.wikipedia.org/wiki/Lens_space)_.

* [[Neil Strickland]], section 9 of: *A Bestiary of Topological Objects* \[<a href="https://strickland1.org/courses/bestiary/bestiary.pdf">pdf</a>, [[Strickland-BestiaryTopological.pdf:file]]\]


In the context of [[orbifolds]]:

* Siddhartha Gadgil, _Equivariant framings, lens spaces and contact structures_, Pacific Journal of Mathematics, Vol. 208 (2003), No. 1, 73–84 ([doi:10.2140/pjm.2003.208.73](http://dx.doi.org/10.2140/pjm.2003.208.73))

* Michel Boileau, Steven Boyer, Radu Cebanu, Genevieve S. Walsh, Section 3 of: _Knot commensurability and the Berge conjecture_, Geom. Topol. 16 (2012) 625-664 ([arXiv:1008.1034](https://arxiv.org/abs/1008.1034))

On classification of lens spaces:

* {#Olum53} [[Paul Olum]], _Mappings of manifolds and the notion of degree_, Ann. of Math. (2) *58* (1953), p. 458–480. [JSTOR:1969748](https://www.jstor.org/stable/1969748)

* {#Brody60} [[E. J. Brody]], _The topological classification of the lens spaces_, Ann. of Math. **71** 1 (1960) 163–184. &lbrack;[doi:10.2307/1969884](https://doi.org/10.2307/1969884), [jstor:](https://www.jstor.org/stable/1969884), MR0116336 (22 #7125) Zbl 0119.18901&rbrack;

* {#Milnor66} [[John Milnor]], *Whitehead torsion*, Bull. Amer. Math. Soc. **72** (1966) 358–426 &lbrack;[doi:10:1090/S0002-9904-1966-11484-2](https://www.ams.org/journals/bull/1966-72-03/S0002-9904-1966-11484-2), [maths.ed.ac.uk](https://web.archive.org/web/20160529051526/http://www.maths.ed.ac.uk/~s1122173/surgerygroup12/milnorwh.pdf), [jstor:bams/1183527946](https://projecteuclid.org/journals/bulletin-of-the-american-mathematical-society-new-series/volume-72/issue-3/Whitehead-torsion/bams/1183527946.full)&rbrack;

On the [[ordinary cohomology]] of lens spaces:

* {#Maxim} Laurentio-George Maxim, *Cohomology of Lens Spaces* &lbrack;[pdf](https://people.math.wisc.edu/~lmaxim/753f13w7.pdf), [[Maxim-CohomologyOfLensSpaces.pdf:file]]&rbrack;

Via [[Dehn surgery]]:

* {#EHI20} Mohamed Elhamdadi, Mustafa Hajij, Kyle Istvan, Fig 23 in: *Framed Knots*, Math Intelligencer **42** (2020) 7–22 &lbrack;[doi:10.1007/s00283-020-09990-0](https://doi.org/10.1007/s00283-020-09990-0), [arXiv:1910.10257](https://arxiv.org/abs/1910.10257)&rbrack;


On lens spaces in [[cosmic topology]]:

* {#AurichLustig12} Ralf Aurich, Sven Lustig, *A survey of lens spaces and large-scale CMB anisotropy*, Mon. Not. Roy. Astron. Soc. **424** (2012) 1556-1562 &lbrack;[arXiv:1203.4086](https://arxiv.org/abs/1203.4086), [doi:10.1111/j.1365-2966.2012.21363.x](https://doi.org/10.1111/j.1365-2966.2012.21363.x)&rbrack;

On the [[3d-3d correspondence]] for lens spaces:

* [[Du Pei]], Chapter III of: _3d-3d correspondence for Seifert manifolds_, 2016 ([spire:1469350](https://inspirehep.net/literature/1469350), [pdf](https://inspirehep.net/files/d509ff9e32448da3a5674f286b93224a))



[[!redirects lens spaces]]