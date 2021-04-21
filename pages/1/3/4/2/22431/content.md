
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The *Cayley distance* between two [[permutations]] is the [[minimum]] [[natural number|number]] of [[transpositions]] of elements needed to turn one into the other.

(This is in contrast to the [[Kendall distance]] which counts the minimum number of [[transpositions]] of *adjacent* pairs of elements.)



## Definition

\begin{definition}\label{CayleyDistance}
**(Cayley distance)**
For $n \in \mathbb{N}$ consider the [[symmetric group]] $Sym(n)$ with its [[mathematical structure|structure]] as a [[finitely generated group]] exhibited by the [[finite set]] of [[generators]] given by all [[transposition permutations]]

$$
  Gen
  \;\coloneqq\;
  \big\{
    \sigma_{i,j}
    \,\vert\,
    1 \leq i, j \lt n
  \big\}
  \;\subset\;
  Sym(n)
  \,.
$$

Then the *Cayley distance* (e.g [Diaconis 88, p. 112](#Diaconis88)) is the [[distance]] on $Sym(n)$ which is the [[graph distance]] of the corresponding [[Cayley graph]], hence the [[function]] 

$$
  d_C(-,-)
  \;\colon\;
   Sym(n) \times Sym(n)
 \longrightarrow
 \mathbb{N}
    \hookrightarrow
  \mathbb{R} 
$$

which sends any [[pair]] of [[permutations]] $\sigma_1, \sigma_2 \in Sym(n)$ to the [[minimum]] [[number]] $d(\sigma_1, \sigma_2) \in \mathbb{N}$ of [[transpositions]] $\sigma_{i_1, j_1}, \sigma_{i_2, j_2}, \cdots, \sigma_{i_d, j_d}$ such that 

$$
  \sigma_2
  \;=\;
  \sigma_{i_d, j_d}
  \circ
  \cdots
  \circ
  \sigma_{i_2, j_2}
  \circ
  \sigma_{i_1, j_1}
  \circ
  \sigma_1
  \,.
$$
\end{definition}

## Properties

### Invariance

The following is immediate from Def. \ref{CayleyDistance}:

\begin{prop}\label{CayleyMetricIsRightInvariant}
**(Cayley metric is right invariant)**
  The Cayley metric is an [[right invariant metric]] in that for all $\sigma \in Sym(n)$ we have

$$
  \sigma^\ast d_C(-,-)
  \;\coloneqq\;
  d_C
  \big(
    (-) \circ \sigma,
    ,\,
    (-) \circ \sigma
  \big)
  \;=\;
  d_C
  \big(
    -
    ,\,
    -
  \big)  
 \,.
$$
\end{prop}

### In terms of numbers of cycles
 {#InTermsOfNumbersOfCycles}

\begin{prop}\label{CayleyObservation}
**(Cayley's observation)**
  The Cayley distance between $\sigma_1, \sigma_2 \,\in\, Sym(n)$ equals $n$ minus the [[natural number|number]] of [[permutation cycles]] in $\sigma_1 \circ \sigma_2^{-1}$:

$$
  d_C(\sigma_1, \sigma_2)
  \;=\;
  n
  -
  \left\vert
     Cycles\big( \sigma_1 \circ \sigma_2^{-1}  \big)
  \right\vert
  \,.
$$
\end{prop}
(e.g. [Diaconis 88, p. 118](#Diaconis88))
\begin{proof}
  By right invariance (Prop. \ref{CayleyMetricIsRightInvariant}) it is sufficient to see the statement for the case that $\sigma_1 = e$ is the [[neutral element]] of $Sym(n)$, hence the [[identity function|identity]] [[permutation]].

Here we need to see that for $\sigma$ any permutation, the minimum number of transpositions whose product yields $\sigma$ equals $n$ minus the number of [[permutation cycle|cycles]] in $\sigma$.

Now observe that:

1. a [[cyclic permutation]] of $k$ elements is the composite of no less than $k-1$ transpositions:

   \[
     \label{CyclicPermutationAsProductOfTranspositions}
     \left(
       \array{
         1 & 2 & 3 & \cdots & k
         \\
         k & 1 & 2 & \cdots & k-1
       }
     \right)
     \;=\;
     \underset{
        k-1 \; factors
     }{
     \underbrace{
     \sigma_{k-1,k-2}
     \circ
     \cdots 
     \circ \sigma_{3,2} \circ \sigma_{2,1} \circ \sigma_{1,k}
     }
     }
   \]
  
1. Any $\sigma$ is the product of elements of the form (eq:CyclicPermutationAsProductOfTranspositions), one for each of its [[permutation cycles]].

Since it is $k-1$ transposition factors in (eq:CyclicPermutationAsProductOfTranspositions) for cycles of $k$ elements, each cycle reduces the number of transposition needed by one.
\end{proof}

## Examples

\begin{example}\label{CayleyDistanceOnSym3}
**([[Cayley distance on Sym(3)]])** \linebreak

The [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent) looks like this:

\begin{tikzcd}[row sep=-6pt, column sep=14pt]
  123
  \ar[rrrr,-]
  \ar[ddddd,-]
  \ar[ddrrr,-]
  &&
  &&
  132
  \ar[ddddd,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  &&&
  \scalebox{.8}{$321$}
  \ar[dddr,-]
  \\
  &
  \scalebox{1.2}{231}
  \ar[ddl,-]
  \ar[uuurrr,-, crossing over]
  \ar[urr,-]
  \\
  {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A} \atop {\phantom{A}}}}}}}}
  \\
  213
  \ar[rrrr,-]
  &&&&
  312
\end{tikzcd}

from which one readily reads off the Cayley distance: Ordering the 6 [[permutations]] as

$$
  \vec \sigma
  \;\coloneqq\;
  \left[
  \array{
    123
    \\
    213
    \\
    132
    \\
    321
    \\
    312
    \\
    231
  }
  \right]
$$

the [[Cayley distance]] on $Sym(3)$, regarded as a $6 \times 6$ [[matrix]]

$$
  [d_C]
  \;\coloneqq\;
  \big(
  d_C
  \big( 
    \sigma_i, \sigma_j
  \big)
  \big)_{i,j}
  \;\in\;
  Mat_{6 \times 6}(\mathbb{N})
$$

is this:

$$
  [d_c]
  \;=\;
  \left[
  \array{
    0 & 1 & 1 & 1  & 2 &  2
    \\
    1 & 0 & 2 & 2 & 1 & 1
    \\
    1 & 2 & 0 & 2 & 1 & 1
    \\
    1 & 2 & 2 & 0 & 1 & 1 
    \\
    2 & 1 & 1 & 1 & 0 & 2 
    \\
    2 & 1 & 1 & 1 & 2 & 0
  }
  \right]
$$

\end{example}


## cRelated concepts

* [[Kendall distance]]

* [[Cayley graph]]



## References

Textbook accounts:

* {#Diaconis88} [[Persi Diaconis]], Chapter 6B of: *Group Representations  in Probability  and  Statistics*, IMS Lecture Notes Monogr. Ser., 11: 198pp. (1988) ([jstor:i397389](https://www.jstor.org/stable/i397389), [ISBN: 0940600145](https://projecteuclid.org/ebooks/institute-of-mathematical-statistics-lecture-notes-monograph-series/Group-representations-in-probability-and-statistics/toc/10.1214/lnms/1215467407), [pdf](https://jdc.math.uwo.ca/M9140a-2012-summer/Diaconis.pdf))

See also:

* Richard G.E. Pinch, *The distance of a permutation from a subgroup of $S_n$* ([arXiv:math/0511501](https://arxiv.org/abs/math/0511501))

* Thaynara Arielly de Lima; Mauricio Ayala-Rincón, *Complexity of Cayley distance and other general metrics on permutation groups* ([doi:10.1109/ColombianCC.2012.6398020](https://doi.org/10.1109/ColombianCC.2012.6398020), [pdf](https://www.mat.unb.br/ayala/shortw4v2.pdf))

Discussion of the [[Cayley distance kernel]]:

* [[Michael A. Fligner]], [[Joseph S. Verducci]], Section 4 of: *Distance Based Ranking Models*, Journal of the Royal Statistical Society. Series B (Methodological) Vol. 48, No. 3 (1986), pp. 359-369 ([jstor:2345433](https://www.jstor.org/stable/2345433))

* [[Persi Diaconis]], [[Phil Hanlon]], Section 4 of: *Eigen Analysis for Some Examples of the Metropolis Algorithm*, in Donald Richards (ed.) *Hypergeometric Functions on Domains of Positivity, Jack Polynomials, and Applications*, Contemporary Mathematics Vol. 138, AMS 1992 ([doi:10.1090/conm/138](http://dx.doi.org/10.1090/conm/138), [EFS NSF 392](https://statistics.stanford.edu/research/eigen-analysis-some-examples-metropolis-algorithm), [pdf](https://statweb.stanford.edu/~cgates/PERSI/papers/eigen-metalg.pdf))

* [[Michael A. Fligner]], [[Joseph S. Verducci]] (eds.), p. xx of: *Probability Models and Statistical Analyses for Ranking Data*, Lecture Notes in Statistics **80**, Springer 1993 ([doi:10.1007/978-1-4612-2738-0](https://link.springer.com/book/10.1007/978-1-4612-2738-0))


[[!redirects Cayley distances]]

