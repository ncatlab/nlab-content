

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

\begin{defn}\label{CayleyDistanceKernel}
**(Cayley distance kernel)**
For $n \in \mathbb{N}$ a [[natural number]], with $Sym(n)$ denoting the [[symmetric group]] on $n$ elements, and 

$$  
  \array{
    Sym(n) \times Sym(n)
    &\overset{d_C}{\longrightarrow}&
    \mathbb{N}
  }
$$

denoting its [[Cayley distance]]-function, the corresponding *Cayley distance kernel* for $\lambda \in \mathbb{R}_+$ 

$$  
  \array{
    Sym(n) \times Sym(n)
    &
      \overset{
        e^{- \lambda \cdot d_C}
      }{
        \longrightarrow
      }
    &
    \mathbb{R}
  }
$$

is the [[exponential]] of the Cayley distance, weighted by $- \lambda$.

\end{defn}


## Examples 

\begin{example}
**([[Cayley distance kernel on Sym(3)]])**
The [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent) looks like

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

Hence if we order the 6 elements of $Sym(3)$ as

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

then the [[Cayley distance]], regarded as a $6 \times 6$ [[matrix]]

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

is

\[
  \label{ExplicitCayleyDistanceMatrix}
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
\]

One checks ([here](https://www.wolframalpha.com/input/?i=eigenvalues++exp%5B+-+ln%5Bkappa%5D+*++%7B++%7B0%2C1%2C1%2C1+%2C2%2C+2%7D%2C+%7B1%2C+0+%2C+2%2C+2%2C+1%2C+1%7D%2C+%7B1%2C+2%2C+0%2C+2%2C+1%2C+1%7D%2C+%7B1%2C2%2C+2%2C0%2C1%2C+1+%7D%2C+%7B2%2C+1%2C+1%2C+1%2C+0%2C+2+%7D%2C+%7B2%2C1%2C1%2C1%2C2%2C0%7D++%7D+%5D)) that the Cayley distance kernel

\[
  \label{CayleyDistanceKernel}
  \big[
    e^{- \lambda \cdot d_C}
  \big]
  \;\in\;
  Mat_{6 \times 6}(\mathbb{R})
\]


has the following [[eigenvalues]]:

$$
  \frac
    {
      (e^\lambda)^2 -1 
    }
    {(e^\lambda)^2}  
  \,,\;\;\;
  \frac
    {
      (e^\lambda)^2 \pm 3 (e^\lambda)  + 2 
    }
    {(e^\lambda)^2}  
  \,,
$$

where the first one appears with multiplicity 4. Exactly one of these can become non-positive for $\lambda \in \mathbb{R}_+$:

$$
  (e^\lambda)^2 - 3 (e^\lambda) + 2
  \;is\;
  \left\{
  \array{
    \lt 0 &\vert&  (e^\lambda) \lt 2
    \\
    = 0 &\vert& (e^\lambda) = 2
    \\
    \gt 0 &\vert& (e^\lambda) \gt 2
  }
  \right.
$$

In conclusion: The [[Cayley distance kernel]] (eq:CayleyDistanceKernel), regarded as a [[bilinear form]] on the [[linear span]] $\mathbb{R}[Sym(3)]$ is:

$$
  \array{
    \text{indefinite} & \text{for} & e^{\lambda} \lt 2
    \\
    \text{positive semi-definite} &\text{for}& e^{\lambda} = 2
    \\
    \text{positive definite} &\text{for}&  e^{\lambda} \gt 2
  }
$$

\end{example}



## Properties

### Gershogin radius

\begin{lemma}\label{SumOfExpLambdaNumCyclesOverPermutations}
  For $n \in \mathbb{N}$ and $Sym(n)$ denoting the [[symmetric group]] on $n$ elements, we have
  $$
    \underset{
      \sigma \in Sym(n)
    }{
      \sum
    }
    e^{ \lambda \cdot \left\vert Cycles(\sigma) \right\vert }
    \;=\;
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\lambda} + k
    \big)
    \,.
  $$
\end{lemma}
(e.g. [Stanley 11, Prop. 1.3.7](#Stanley11), see also discussion at [MO:q/245005](https://mathoverflow.net/q/245005/381), [MO:a/92051](https://math.stackexchange.com/a/92051/58526))


\begin{lemma}\label{SumOverFirstRowOfCayleyDistanceKernel}
**(sum over first row of Cayley distance kernel)** \linebreak
  For $n \in \mathbb{N}$, the [[sum]] over the first row of the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) equals
$$
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \lambda \cdot d_C(\sigma, e) }
  \;=\;  
  e^{- \lambda \cdot n }
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\lambda}
    + 
    k
  \big)
$$
\end{lemma}
\begin{proof}
We compute as follows:
$$
  \begin{aligned}
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \lambda \cdot d_C(\sigma, e) }
  &
  \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \lambda \cdot (n - \left\vert Cycles(\sigma) \right\vert ) }
  \\
  & 
  \;=\;
  e^{- \lambda \cdot n }
  \,
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ \lambda \cdot  \left\vert Cycles(\sigma) \right\vert }  
  \\
  & =\;
  e^{- \lambda \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\lambda}
    + 
    k
  \big)
  \mathrlap{\,,}
  \end{aligned}
$$
where:

* the first step is [Cayley's observation](Cayley+distance#CayleyObservation),

* the last step uses Lemma \ref{SumOfExpLambdaNumCyclesOverPermutations}.

\end{proof}


\begin{prop}\label{GershgorinRadiiOfCayleyDistanceKernel}
**([[Gershogin radius]] of [[Cayley distance kernel]])**
  For $n \in \mathbb{N}$, 
 the [[Gershogin radii]] of the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) are all equal to
  $$
    r
    \;=\;
  e^{- \lambda \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\lambda}
    + 
    k
  \big)
  - 
  1
  $$
\end{prop}
\begin{proof}
  By [[right invariant metric|right invariance]] of the [[Cayley distance]] ([this Prop.](Cayley+distance#CayleyMetricIsRightInvariant)) the sum over entries of any row is equal to that of the first row.
Since moreover 

* all entries are [[real number|real]] and non-[[negative number|negative]],  hence equal to their [[absolute value]],

* the diagonal elements are all equal to 1,

it follows that this sum over the first row already equals the Gershogin radius plus 1 (by its defining formula [here](Gershgorin+circle+theorem#eq:GershoginRadiusFormula)). Therefore the statement follows by Lemma \ref{SumOverFirstRowOfCayleyDistanceKernel}.
\end{proof}


## Related concepts

* [[Mallows kernel]], [[Kendall kernel]]

* [[kernel method]]


## References

Mentioning of the Cayley distance kernel:

* [[Michael A. Fligner]], [[Joseph S. Verducci]], Section 4 of: *Distance Based Ranking Models*, Journal of the Royal Statistical Society. Series B (Methodological) Vol. 48, No. 3 (1986), pp. 359-369 ([jstor:2345433](https://www.jstor.org/stable/2345433))

* [[Persi Diaconis]], [[Phil Hanlon]], Section 4 of: *Eigen Analysis for Some Examples of the Metropolis Algorithm*, in Donald Richards (ed.) *Hypergeometric Functions on Domains of Positivity, Jack Polynomials, and Applications*, Contemporary Mathematics Vol. 138, AMS 1992 ([doi:10.1090/conm/138](http://dx.doi.org/10.1090/conm/138), [EFS NSF 392](https://statistics.stanford.edu/research/eigen-analysis-some-examples-metropolis-algorithm), [pdf](https://statweb.stanford.edu/~cgates/PERSI/papers/eigen-metalg.pdf))

* [[Michael A. Fligner]], [[Joseph S. Verducci]] (eds.), p. xx of: *Probability Models and Statistical Analyses for Ranking Data*, Lecture Notes in Statistics **80**, Springer 1993 ([doi:10.1007/978-1-4612-2738-0](https://link.springer.com/book/10.1007/978-1-4612-2738-0))


Supplementary references:

* {#Stanley11} [[Richard Stanley]], *[Enumerative combinatorics](http://www-math.mit.edu/~rstan/ec/)* -- [Volume 1](http://www-math.mit.edu/~rstan/ec/ec1/), 2011 ([pdf](http://www-math.mit.edu/~rstan/ec/ec1.pdf))
