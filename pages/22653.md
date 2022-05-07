
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

For $n \in \mathbb{N}$, consider the [[complex numbers|complex]] [[group algebra]] $\mathbb{C}[Sym(n)]$ of the [[symmetric group]] on $n$ elements.


\begin{defn}\label{JucycMurphyElements}
The *Jucys-Murphy elements* 

$$
  J_k \;\in\; \mathbb{C}[Sym(n)] \;\;\;\; k \in \{1, \cdots, n\}
$$

are the following [[sums]] of [[transpositions]] $(i j) \in Sym(n) \subset \mathbb{C}[Sym(n)]$ in this [[group algebra]]:

$$
  J_1 \;\coloneqq\; 0
$$

$$
  J_k \;\coloneqq\; \underoverset{i = 1}{k-1}{\sum} (i k)
$$
\end{defn}

Here $J_k$ may be understood as the sum of all transpositions in $Sym(k)$ that are not in the [[subgroup]] $Sym(k-1) \subset Sym(k)$.

## Properties

Write $sYTableaux_n$ for the [[set]] of [[standard Young tableaux]] with $n$ boxes, and write

\[
  \label{VectorsInSeminormalRepresentations}
  \big\{ v_T \in \mathbb{C}[Sym(n)]\big\}_{T \in sYTableaux_n}
\]

for the canonical [[linear basis]] of Young's [[seminormal representation]].


\begin{prop}
  The $v_T$ (eq:VectorsInSeminormalRepresentations) are joint [[eigenvectors]] of the Jucys-Murphy elements (Def. \ref{JucycMurphyElements}) for [[eigenvalues]] the "content" $j - i$ of the box $(i,j)$ that contains the number $k$ in the standard Young tableau
$$
  J_k v_T \;=\; (j- i) v_T
  \,,
  \;\;\;
  T_{i,j} = k
  \,.
$$
\end{prop}

In particular, the Jucy-Murphy elements all commute with each other.

\begin{prop}
  The [[characteristic polynomial]] of the Jucys-Murphy elements is proportional to the [[Cayley distance kernel]]:

$$
  \big(
    t + J_1
  \big)
  \big(
    t + J_2
  \big)
  \cdots
  \big(
    t + J_n
  \big)
  \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ ln(t) \cdot \# cycles(\sigma) }
  \, \sigma 
  \;\;\;\;\;
  \in
  \mathbb{C}[Sym(n)][t]
$$
\end{prop}

This is stated on the [Wikipedia page](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element), attributed to Jucys but without explicit reference. Probably it is due to [Jucys 71](#Jucys71), judging by the title and its MathReview blurb.

\begin{corollary}
  The [[eigenvalues]] of the [[Cayley distance kernel]]
  $$
    e^{ - ln(t) \cdot d_C }
    \;=\;
    e^{- ln(t) \cdot n}
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    e^{ ln(t) \cdot \# cycles(\sigma) }
    \, \sigma \cdot
  $$
  (regarded on the right as the linear map given by right multiplication in the [[group algebra]]) are [[indexed set|indexed]] by [[Young diagrams]] $\lambda$ and are given by
  $$
    EigVals[e^{- ln(t) \cdot d_C}]_\lambda
    \;=\;  
    e^{ - ln(t) \cdot  n}
    \underset{
      { 1 \leq i \leq rows(\lambda) }
      \atop
      { 1 \leq j \leq \lambda_i }
    }{\prod}
    \big(
      t - j + i
    \big)
  $$
\end{corollary}

An alternative derivation of this statement, using the formula for [[Cayley graph spectra]] and the [[hook length formula]]/[[hook-content formula]] is [this Prop.](Cayley+distance+kernel#EigenvaluesInTermsOfJustBoxContent) at *[[Cayley distance kernel]]* ([CSS 21](Cayley+distance+kernel#CSS21)).

## References

* {#Jucys71} [[Algimantas Adolfas Jucys]], *Factorization of Young projection operators for the symmetric group*, Lietuvos Fizikos Rinkinys, **11** (1) 9 (1971) ([journal content](http://www.itpa.lt/%7Elfd/Lfz/Turiniai/Turi1971.html#))

* Wikipedia, *[Jucys-Murphy element](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element)*

[[!redirects Jucys-Murphy elements]]
