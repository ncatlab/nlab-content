
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

### Eigenvalues

Write $sYTableaux_n$ for the [[set]] of [[standard Young tableaux]] with $n$ boxes, and write

\[
  \label{VectorsInSeminormalRepresentations}
  \big\{ v_T \in \mathbb{C}[Sym(n)]\big\}_{T \in sYTableaux_n}
\]

for the canonical [[linear basis]] of Young's [[seminormal representation]].


\begin{prop}\label{EigenvaluesOfJMElements}

  The $v_T$ (eq:VectorsInSeminormalRepresentations) are joint [[eigenvectors]] of the Jucys-Murphy elements (Def. \ref{JucycMurphyElements}) for [[eigenvalues]] the "content" $j - i$ of the box $(i,j)$ that contains the number $k$ in the standard Young tableau
$$
  J_k v_T \;=\; (j - i) v_T
  \,,
  \;\;\;
  T_{i,j} = k
  \,.
$$

\end{prop}

In particular, the Jucys-Murphy elements all commute with each other.

This is due to [Jucys 71](#Jucys71), recalled as [Jucys 74 (12)](#Jucys74).


### Factorization of Cayley-Distance kernel


\begin{prop}\label{FactorizationOfCayleyDistanceKernelAsCharPolynomialOfJMElements}
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
This is attributed on the [Wikipedia page](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element), Jucys but without explicit reference. Possibly due to [Jucys 71](#Jucys71).

\begin{proof}

  By multiplying out and observing that this yields minimal factorizations of permutations into [[transpositions]], as [here](Cayley+distance#eq:CyclicPermutationAsProductOfTranspositions).

\end{proof}

Combining 
Prop. \ref{EigenvaluesOfJMElements} with 
Prop. \ref{FactorizationOfCayleyDistanceKernelAsCharPolynomialOfJMElements}
yields:

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

The Jucy-Murphy elements are independently due to:

* [[Algimantas Adolfas Jucys]], *Symmetric polynomials and the center of the symmetric group ring*, Rep. Mathematical Phys.5 (1974), pp. 107–112 (<a href="https://doi.org/10.1016/0034-4877(74)90019-6">doi:10.1016/0034-4877(74)90019-6</a>)

* [[G. E. Murphy]], *A new construction of Young's seminormal representation of the symmetric groups*, Journal of Algebra Volume 69, Issue 2, April 1981, Pages 287-297 (<a href="https://doi.org/10.1016/0021-8693(81)90205-2">doi:10.1016/0021-8693(81)90205-2</a>)

Their eigenvalues seem to be due to

* {#Jucys71} [[Algimantas Adolfas Jucys]], *Factorization of Young projection operators for the symmetric group*, Lietuvos Fizikos Rinkinys, **11** (1) 9 (1971) ([journal content](http://www.itpa.lt/%7Elfd/Lfz/Turiniai/Turi1971.html#))

recalled in

* {#Jucys74} [[Algimantas Adolfas Jucys]], *Symmetric polynomials and the center of the symmetric group ring*, Reports on Mathematical Physics, Volume 5, Issue 1, February 1974, Pages 107-112 (<a href="https://doi.org/10.1016/0034-4877(74)90019-6">doi:10.1016/0034-4877(74)90019-6</a>)

Review:

* Wikipedia, *[Jucys-Murphy element](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element)*

Further discussion:

* {#Chan18} Kelvin Tian Yi Chan, *Induction Relations in the Symmetric Groups and Jucys-Murphy Elements*, 2018 ([hdl:10012/13601](http://hdl.handle.net/10012/13601), [pdf](https://uwspace.uwaterloo.ca/bitstream/handle/10012/13601/Chan_Kelvin.pdf?sequence=3&isAllowed=y))

[[!redirects Jucys-Murphy elements]]
