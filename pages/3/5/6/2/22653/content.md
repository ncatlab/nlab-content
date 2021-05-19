
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

are the following [[sums]] of [[transpositions]] $(i,j) \in Sym(n) \subset \mathbb{C}[Sym(n)]$ in this [[group algebra]]:

\[
  \label{J1IsZero}
  J_1 \;\coloneqq\; 0
\]

\[
  \label{JkAsSum}
  J_k \;\coloneqq\; \underoverset{i = 1}{k-1}{\sum} (i,k)
\]

\end{defn}

([Murphy 81, p. 287 (1 of 11)](#Murphy81), [Murphy 83, p. 259 (2 of 8)](#Murphy83))

Notice that $J_k$ may be understood as the sum of all transpositions in $Sym(k)$ that are not in the [[subgroup]] $Sym(k-1) \subset Sym(k)$.

## Properties

### Eigenvalues

Write $sYTableaux_n$ for the [[set]] of [[standard Young tableaux]] with $n$ boxes, and write

\[
  \label{VectorsInSeminormalRepresentations}
  \big\{ v_{T,k} \in \mathbb{C}[Sym(n)]\big\}_{
    { T \in sYTableaux_n}
    \atop
    { 1 \leq m \leq dim(S^{(\left\vert T\right\vert)})  }
  }
\]

for the [[Gelfand-Tsetlin basis]] (Young's [[seminormal representation]]).

We'll notationally suppress the multiplicity index $m$ in the following.

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

On the [Wikipedia page](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element) this is attributed to Jucys, but without explicit reference. It might be in [Jucys 71](#Jucys71) (but is not mentioned in the review in [Jucys 74](#Jucys74)). However, it is not much of a theorem, anyways:
\begin{proof}
By [[induction]]: 

For $n = 1$ the claim reduces to 

$$
  \big(
    t + J_1
  \big)
  \;=\;
  e^{ ln(t) \cdot 1 }
  \,,  
$$

which holds by (eq:J1IsZero).

Now assume that the statement is true for $n \in \mathbb{N}$. 

Observe that every permutation $\sigma \in Sym(n+1)$ may be written as product

$$
  \sigma
  \;=\;
  c_1(\sigma)
  \cdot
  c_2(\sigma)
  \cdots
  c_{\# cycles(\sigma)}(\sigma)
$$

of products of transpositions of the form

$$
  c_i(\sigma)
  \;\;
  \;=\;
   (i_{\ell_i-1},i_{\ell_i-2})
   \circ
   \cdots 
   \circ 
   (i_3,i_2)
   \circ 
   (i_2,i_1) 
   \circ 
   (i_1,i_{\ell_i})
  \,,
$$

where $\ell_i$ is the length of the $i$th [[permutation cycle]].

Here we may assume without restriction that 

$$
  i_j 
    \lt
  i_{\ell_i} 
  \,,
  {\phantom{AAA}}
  \text{and}
  {\phantom{AAA}}
  i \lt j 
   \;\;
   \Rightarrow
   \;\;
   i_{\ell_i} \lt j_{\ell_j}
$$

because if not then we may (1) rearrange the $c_i(\sigma)$ within their product (these commute with each other, since they contain permutations among elements within distinct cycles) and (2) cyclically rearrange the factors withing each $c_i(\sigma)$.

Once all permutations are uniquely represented as products this way, the representative of any $\sigma \in Sym(n+1)$ is uniquely obtained from the representative of an element in $Sym(n)$, by either:

1. multiplying from the right with a transposition $(k, n+1)$ for $k \leq n$, in which case the $n+1$st element will be part of a cycle that was already present;

1. by retaining the previous product as is, in which case the $n+1$st element will be its own new cycle.

This means that

$$
    \underset{\sigma \in Sym(n+1)}{\sum}
    t^{ \# cycles(\sigma) }
    \,
    \sigma
    \;
    =
    \;
    \underset{\sigma' \in Sym(n)}{\sum}
    t^{ \# cycles(\sigma') }    
    \, 
    \sigma' (t + J_{n+1})
$$
and hence the claim follows by the induction assumption.
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



### Projectors
 {#Projectors}

[Murphy 81, p. 291 (5 of 11)](#Murphy81)

[Murphy 83, p. 259 (2 of 8)](#Murphy83)

[MathOverflow:a/151375](https://mathoverflow.net/a/151375/381)

## References

The Jucys-Murphy elements are independently due to:

* {#Jucys71} [[Algimantas Adolfas Jucys]], *Factorization of Young projection operators for the symmetric group*, Lietuvos Fizikos Rinkinys, **11** (1) 9 (1971) ([journal content](http://www.itpa.lt/%7Elfd/Lfz/Turiniai/Turi1971.html#))

* {#Jucys74} [[Algimantas Adolfas Jucys]], *Symmetric polynomials and the center of the symmetric group ring*, Reports on Mathematical Physics, Volume 5, Issue 1, February 1974, Pages 107-112 (<a href="https://doi.org/10.1016/0034-4877(74)90019-6">doi:10.1016/0034-4877(74)90019-6</a>)

and

* {#Murphy81} [[G. E. Murphy]], *A new construction of Young's seminormal representation of the symmetric groups*, Journal of Algebra Volume 69, Issue 2, April 1981, Pages 287-297 (<a href="https://doi.org/10.1016/0021-8693(81)90205-2">doi:10.1016/0021-8693(81)90205-2</a>)

* {#Murphy83} [[G. E. Murphy]], *The idempotents of the symmetric group and Nakayama's conjecture*, Journal of Algebra Volume 81, Issue 1, March 1983, Pages 258-265 ([pdf](https://core.ac.uk/download/pdf/82692868.pdf))

* {#Murphy92} [[G. E. Murphy]], *On the representation theory of the symmetric groups and associated Hecke algebras*, J. Algebra 152 (1992) 492–513 ([pdf](https://core.ac.uk/download/pdf/82422274.pdf), <a href="https://doi.org/10.1016/0021-8693(92)90045-N">doi:10.1016/0021-8693(92)90045-N</a>))


(According to [Vershik-Okounkov 04, Footnote 2](representation+theory+of+the+symmetric+group#VershikOkounkov04), [Jucys 74](#Jucys74) "remained unnoticed" until [Murphy 81](#Murphy81) first re-discovered the results, and then Jucys' paper. In fact [Jucys 71](#Jucys71), which must have the actual proofs, seems to remain electronically unavailable.)


Review:

* Wikipedia, *[Jucys-Murphy element](https://en.wikipedia.org/wiki/Jucys%E2%80%93Murphy_element)*

Further discussion:

* {#Chan18} Kelvin Tian Yi Chan, *Induction Relations in the Symmetric Groups and Jucys-Murphy Elements*, 2018 ([hdl:10012/13601](http://hdl.handle.net/10012/13601), [pdf](https://uwspace.uwaterloo.ca/bitstream/handle/10012/13601/Chan_Kelvin.pdf?sequence=3&isAllowed=y))

[[!redirects Jucys-Murphy elements]]
