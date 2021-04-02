



+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

(...)

## Preliminaries

\begin{defn}\label{SlicesDef}
  Let $G$ be a [[topological group]] and $X$ a [[topological G-space]].

For $H \subset G$ a [[closed subspace|closed]] [[subgroup]], 
a [[topological subspace]] $S \subset X$ is called:

* an *$H$-kernel* if it is the [[preimage]] of the base point $[H] \in G/H$ in the [[coset space]] under a $G$-[[equivariant function|equivariant]] [[continuous function]] $f$ from the $G$-[[orbit]] of $S$:

  $$
    \underset{
      G\cdot S
      \overset{f}{\to}
      G/H
    }
    {
      \exists
    }
    \;
    S 
      \;\simeq\;
    f^{-1}
    \big(
      [H]
    \big)
  $$

* an *$H$-slice* if it is an $H$-kernel and its [[orbit]] is an [[open subspace]]:

  $$
    G \cdot S
    \underset{open}
      {\subset}
    X
  $$

* a *slice through $x$* if it is a $G_x$-slice for some $x \in S \subset X$ with [[stabilizer group]] $G_x \coloneqq Stab_G(x) \simeq H$.

\end{defn}

([Palais 61, Def. 2.1.1](#Palais61), recalled as [Karppinen 16, Def. 6.1.1](#Karppinen16))

\begin{example}
  For $n \in \mathbb{N}$ consider the defining [[action]] of the [[orthogonal group]] $G = O(n+1)$ on the [[Cartesian space]] $\mathbb{R}^{n+1}$. Then for every point $0 \neq x \in \mathbb{R}^{n+1}$ we have $G_x = O(n)$ and $G/G_x = S^n$ the [[n-sphere]]. 

The ray $ \{c \cdot x \vert c \in \mathbb{R}_{\gt 0}\} \subset$ has [[orbit]] the [[complement]] of the origin and is thus a slice through $x$ as exhibited by the radial quotient map 
$$
  \mathbb{R}^{n+1} 
    \setminus 
  \{0\}
    \longrightarrow
  S^n
   =
  O(n+1)/O(n)
  \,.
$$
\end{example}

## Statement

A _slice theorem_ is a statement of sufficient conditions such that there is a slice through each point of a given [[topological G-space]].

\begin{prop}
  Let $G$ be the [[topological group]] underlying a [[Lie group]] and let $X$ be a [[topological G-space]] with [[proper action]].

Then for every point $x \in X$
there exists a slice through $x$ (Def. \ref{SlicesDef}).
\end{prop}

This appears as [Palais 61, Prop. 2.3.1](#Palais61).


## Related concepts

* [[topological G-space]], [[G-manifold]]

* [[compact Lie group]]

* [[equivariant bundle]]

* [[equivariant differential topology]]

* [[equivariant Tietze extension theorem]]

## References

Original discussion:

* [[Andrew Gleason]], _Spaces With a Compact Lie Group of Transformations_, Proceedings of the American Mathematical Society
Proceeding, Vol. 1, No. 1 (Feb., 1950), pp. 35-43 ([jstor:2032430](https://www.jstor.org/stable/2032430), [doi:10.2307/2032430](https://doi.org/10.2307/2032430))

* [[Deane Montgomery]], [[Chung Tao Yang]], _The existence of a slice_, Ann. of Math. 65 (1957), 108-116 ([jstor:1969667](https://www.jstor.org/stable/1969667), [doi:10.2307/1969667](https://doi.org/10.2307/1969667))

* [[George Mostow]], _Equivariant embeddings in Euclidean space_,  Ann. of Math. 65 (1957), 432-446 ([jhir:1774.2/46183](http://jhir.library.jhu.edu/handle/1774.2/46183), [pdf scan](https://jscholarship.library.jhu.edu/bitstream/handle/1774.2/46183/Mostow_Mar57.pdf?sequence=1&isAllowed=y))

* {#Palais60} [[Richard Palais]], _Slices and equivariant embeddings_, chapter VIII in: [[Armand Borel]] (ed.), _Seminar on Transformation Groups_, Annals of Mathematics Studies 46, Princeton University Press 1960 ([jstor:j.ctt1bd6jxd](https://www.jstor.org/stable/j.ctt1bd6jxd))

* {#Palais61} [[Richard Palais]], _On the Existence of Slices for Actions of Non-Compact Lie Groups_, Annals of Mathematics
Second Series, Vol. 73, No. 2 (Mar., 1961), pp. 295-323 ([jstor:1970335](https://www.jstor.org/stable/1970335), [doi:10.2307/1970335](https://doi.org/10.2307/1970335), [pdf](http://vmm.math.uci.edu/ExistenceOfSlices.pdf))



* [[Glen Bredon]], Section II.4 of: _[[Introduction to compact transformation groups]]_, Academic Press  1972 ([ISBN:9780080873596](https://www.elsevier.com/books/introduction-to-compact-transformation-groups/bredon/978-0-12-128850-1), [pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))


Review:

* {#Karppinen16} [[Sini Karppinen]], _The existence of slices in $G$-spaces, when $G$ is a Lie group_, Helsinki 2016 ([hdl:10138/190707](http://hdl.handle.net/10138/190707))

[[!redirects slice theorems]]



