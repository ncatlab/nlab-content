
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

While the [[eigenvalues]] of a [[diagonal matrix]] are, of course, [[equality|equal]] to its diagonal entries, *Gershgorin's circle theorem* ([Gershgorin 31](#Gershgorin31), Prop. \ref{GershgorinTheorem} below) provides upper bounds (the *Gershgorin radii, Def. \ref{GershgorinDiscs} below) for general [[square matrices]] over the [[complex numbers]] on how far, in the [[complex plane]], the eigenvalues can be from the values of the diagonal entries. 




## Statement

Let $n \in \mathbb{N}$ be a [[natural number]].

\begin{definition}\label{GershgorinDiscs}
**(Gershgorin discs)** \linebreak
 Let $A \in Mat_{n \times n}(\mathbb{C})$ be a [[square matrix]] with [[complex numbers|complex]] entries. For $j \in \{1, \cdots, n\}$ define 

* the $j$th *Gershgorin radius* of $A$ to be the [[sum]] of [[absolute values]] of off-diagonal entries in the $j$th row:

  \[
    \label{GershoginRadiusFormula}
    r_j^A
    \;\coloneqq\;
    \underset{k \neq j}{\sum}
    \left\vert
      a_{j k}
    \right\vert
  \]

* the $j$th *Gershgorin disc* to be the [[closed disk]] in the [[complex plane]] centered at the $j$th diagonal entry with radius the above $j$th Gershgorin radius:

  \[
    \label{GershoginDiscFormula}
    D_j^A
    \;\coloneqq\;
    \Big\{
      z \in \mathbb{C}
      \,\Big\vert\,
      \left\vert
        z - a_{j j}
      \right\vert
      \,\leq\,
      r_j^A
    \Big\}
    \,.
  \]

\end{definition}


\begin{proposition}\label{GershgorinTheorem}
**(Gershgorin disc theorem)** \linebreak
 For $A \in Mat_{n \times n}(\mathbb{C})$ a [[square matrix]] with [[complex numbers|complex]] entries, each of its [[eigenvalues]] is contained in at least one Gershgorin disc (Def. \ref{GershgorinDiscs}):

$$
  \underset{
    c \in EV(A)
  }{\forall}
  \;\;
  \underset{
    1 \leq j \leq n
  }{\exists}
  \;\;
  \big(
    c \,\in\, D_j^A \,\subset\, \mathbb{C}
  \big)
  \,.
$$

\end{proposition}

(see, e.g., [Meckes 19, Thm. 7.1](#Meckes19))

## Related theorems

* [[Cauchy interlace theorem]]

## References

The original article:

* {#Gershgorin31} [[Semyon Aranovich Gershgorin]], *Über die Abgrenzung der Eigenwerte einer Matrix*, Bulletin de l'Académie des Sciences de l'URSS. Classe des sciences mathématiques et na, 1931, Issue 6, Pages 749–754 ([mathnet:eng/izv5235](http://mi.mathnet.ru/eng/izv5235))

Lecture notes:

* {#Meckes19} [[Mark Meckes]], Section 7.1 of: *Lecture notes on matrix analysis*, 2019 ([pdf](https://case.edu/artsci/math/mwmeckes/matrix-analysis.pdf), [[MeckesMatrixAnalysis.pdf:file]])

Exposition:

* Zack Cramer, *The Gershgorin circle theorem*  2017 ([[CramerGershgorinCircleTheorem.pdf:file]])


See also:

* Wikipedia, *[Gershgorin circle theorem](https://en.wikipedia.org/wiki/Gershgorin_circle_theorem)*


Strengthening for matrices with non-negative entries:

* Imre Bárány, József Solymosi, *Gershgorin disks for multiple eigenvalues of non-negative matrices* ([arXiv:1609.07439](https://arxiv.org/abs/1609.07439))



[[!redirects Gershgorin circle theorems]]

[[!redirects Gershgorin disc]]
[[!redirects Gershgorin discs]]

[[!redirects Gershgorin radius]]
[[!redirects Gershgorin radii]]


