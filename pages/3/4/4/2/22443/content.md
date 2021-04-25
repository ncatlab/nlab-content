

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $n \in \mathbb{N}$ and for some parameter $\beta \in \mathbb{R}_+$ ("[[inverse temperature]]") the [[function]] on pairs $\sigma_1, \sigma_2 \in $ [[symmetric group|Sym(n)]] of [[permutations]] of $n$ elements which assigns the [[exponential|exponentiated]] [[Cayley distance]] $d_C$ between them, weighted by $- \beta$:

$$
  (\sigma_1, \sigma_2)
  \;\mapsto\;
  e^{ - \beta \cdot d_C(\sigma_1, \sigma_2) }
  \;\in\;
  \mathbb{R}
  \,,
$$

may naturally be called the *Cayley distance kernel* (though it does not seem to have a standard name in existing literature).

This is different from but akin to other [[kernel methods|kernels]] used in [[geometric group theory]], notably the more widely studied *[[Mallows kernel]]*, which is of the same form but using the [[Kendall distance]] instead of the [[Cayley distance]]. While these two [[distance]] [[functions]] are superficially similar (where the Cayley distance counts the minimum number of [[transpositions]] needed to turn one permutation into another, the [[Kendall distance]] counts minimum numbers of *adjacent* [[transpositions]]) the two resulting kernels behave qualitatively differently:

Where the [[Mallows kernel]] is [[positive definite bilinear form|positive definite]] for all $\beta \geq 0$ ([Jiao-Vert 18, Thm. 1](Kendall+tau+distance#JiaoVert18)), the Cayley distance kernel becomes [[indefinite bilinear form|indefinite]], for sufficiently small non-integer values of $e^\beta$, see Example \ref{CayleyDistanceKernelOnSym3} and Prop. \ref{FailureOfPositivityForBetaBelowLn2} below.

Curiously, computer experiment suggests ([CSS21](#CSS21)) that for *integer* values of $N \coloneqq e^\beta$ the Cayley distance kernel is always positive (semi-)definite, see Example \ref{CayleyDistanceKernelOnSym4}. At exactly these values the Cayley distance kernel equals ([CSS21](#CSS21)) the [[fundamental representation|fundamental]] $\mathfrak{gl}(N)$-[[Lie algebra weight system]] on [[horizontal chord diagrams]] (for the [[general linear Lie algebra]] $\mathfrak{gl}(n)$ regarded as a [[metric Lie algebra]] with the [[trace]] in its defining [[fundamental representation]], as in [Bar-Natan 95](stringy+weight+systems+span+classical+Lie+algebra+weight+systems#BarNatan95)) under the [[monoid]]-[[homomorphism]] 

$$
  \array{
    \mathcal{D}^{pn}_n
    &\overset{perm}{\longrightarrow}&
    Sym(n)
    \\
    (i_d j_d)
      \cdot \cdots \cdot
    (i_1 j_1)
    &\mapsto&
    t_{i_d j_d}
      \circ
    \cdots
      \circ
    t_{i_1 j_1}
  }
$$

that sends the [[horizontal chord diagram#MonoidOfHorizontalChordDiagrams|chord]] $(i j)$ to that [[permutation]] of $n$ elements (strands) which is given by the [[transposition]] $t_{i j}$ of the $i$th with the $j$th strand.

\linebreak

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

denoting its [[Cayley distance]]-function, the corresponding *Cayley distance kernel* for $\beta \in \mathbb{R}_+$ 

\[
  \label{CayleyDistanceKernel}
  \array{
    Sym(n) \times Sym(n)
    &
      \overset{
        e^{- \beta \cdot d_C}
      }{
        \longrightarrow
      }
    &
    \mathbb{R}
  }
\]

is the [[exponential]] of the Cayley distance, weighted by $- \beta$.

This may and often is regarded as a [[square matrix]] over the [[real numbers]] and as such often conflated with the corresponding [[bilinear form]] on the [[linear span]] of $Sym(n)$.

\end{defn}


## Examples 

\begin{example}\label{CayleyDistanceKernelOnSym3}
**([[Cayley distance kernel on Sym(3)]])**
The [[Cayley graph]] of the [[symmetric groups]] on 3 elements, $Sym(3)$, with [[edges]] corresponding to any [[transposition]] (not necessarily adjacent) looks as follows:

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
    e^{- \beta \cdot d_C}
  \big]
  \;\in\;
  Mat_{6 \times 6}(\mathbb{R})
\]

has the following [[eigenvalues]]:

$$
  \frac
    {
      (e^\beta)^2 -1 
    }
    {(e^\beta)^2}  
  \,,\;\;\;
  \frac
    {
      (e^\beta)^2 \pm 3 (e^\beta)  + 2 
    }
    {(e^\beta)^2}  
  \,,
$$

where the first one appears with multiplicity 4. Exactly one of these can become non-positive for $\beta \in \mathbb{R}_+$:

$$
  (e^\beta)^2 - 3 (e^\beta) + 2
  \;is\;
  \left\{
  \array{
    \lt 0 &\vert&  (e^\beta) \lt 2
    \\
    = 0 &\vert& (e^\beta) = 2
    \\
    \gt 0 &\vert& (e^\beta) \gt 2
  }
  \right.
$$

The following plot (via WolframAlpha, [here](https://www.wolframalpha.com/input/?i=min%5B+%7B+N%5E2+-+1+%7D%2C+%7B+N%5E2+%2B+3+*+N+%2B+2+%7D%2C+%7B+N%5E2+-+3+*+N+%2B+2+%7D+%5D++for+0.6+%3C+N+%3C+3)) shows ($e^{2 \beta}$ times) the lowest eigenvalue of the Cayley distance kernel on $Sym(3)$, as a function of the exponentiated inverse temperature $N \coloneqq e^{\beta}$:


<a href="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym3.jpg">
<img src="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym3.jpg" width="350">
</a>


In conclusion: The [[Cayley distance kernel]] (eq:CayleyDistanceKernel), regarded as a [[bilinear form]] on the [[linear span]] $\mathbb{R}[Sym(3)]$ is:

$$
  \array{
    \text{indefinite} & \text{for} & e^{\beta} \lt 2
    \\
    \text{positive semi-definite} &\text{for}& e^{\beta} = 2
    \\
    \text{positive definite} &\text{for}&  e^{\beta} \gt 2
  }
$$

The asymptotic behaviour is generic (Prop. \ref{FailureOfPositivityForBetaBelowLn2}, Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity} below).
Computer experiment ([CSS21](#CSS21)) suggest that the exceptional positive semi-definiteness at integer values of $e^\beta$ holds generally.


\end{example}



\begin{example}\label{CayleyDistanceKernelOnSym4}
**(Cayley distance kernel on Sym(4))**

Similar analysis shows that the eigenvalues of the Cayley distance kernel $e^{- \beta \cdot d_C}$ on $Sym(4)$ are the following:

$$
  \array{
    eigenvalue & multiplicity
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 + 6 (e^{\beta})^2 + 11 (e^{\beta}) + 6
      \;
    \big)
    & 
    1
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 - 6 (e^{\beta})^2 + 11 (e^{\beta}) - 6
      \;
    \big)
    &
    1
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 \phantom{\; + 0 (e^{\beta})^2 \;} - 1 (e^{\beta}) \phantom{ + 0 }
      \;
    \big)
    &
    4
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 + 2 (e^{\beta})^2 - 1 (e^{\beta}) - 2
      \;
    \big)
    &
    9
    \\
    e^{-3 \beta}
    \big(
      \;
      + (e^{\beta})^3 - 2 (e^{\beta})^2 - 1 (e^{\beta}) + 2
      \;
    \big)
    &
    9
  }
$$

{#PlotOfEigenvalueOfKernelOnSym4AsFunctionOfExponentiatedBeta} The following plot (via WolframAlpha, [here](https://www.wolframalpha.com/input/?i=min%5B+%7B++N%5E3+%2B+6+*+N%5E2+%2B+11+*+N+%2B+6+%2C+N%5E3+-+6+*+N%5E2+%2B+11+*+N++-+6+%2C+N%5E3+-+N+%2C+N%5E3+%2B+2+*+N%5E2+-+N+-+2%2C+N%5E3+-+2+*+N%5E2+-+N++%2B+2+%7D+%5D++for+0.6+%3C+N+%3C+4)) shows ($e^{3 \beta}$ times) the lowest eigenvalue of the Cayley distance kernel on $Sym(4)$ as a function of the exponentiated inverse temperature $N \coloneqq e^\beta$:


<a href="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym4-b.jpg">
<img src="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym4-b.jpg" width="540">
</a>

One sees that the kernel is

$$
  \array{
    \text{indefinite} & \text{for} & e^{\beta} \lt 2
    \\
    \text{positive semi-definite} &\text{for}& e^{\beta} = 2, 3
    \\
    \text{positive definite} &\text{for}&  e^{\beta} \gt 3
  }
$$

The asymptotic behaviour is generic (Prop. \ref{CayleyDistanceKernelIsIndefiniteForEBetaNonIntegralAndSmallernminusone}, Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity} below).
Computer experiment ([CSS21](#CSS21)) suggest that the exceptional positive semi-definiteness at integer values of $e^\beta$ holds generally.


\end{example}




## Properties

### Sum over one row

We give a useful expression (Lemma \ref{SumOverFirstRowOfCayleyDistanceKernel} below) for the sum over the first row of the Cayley distance kernel. This appears both in the expression for its Gershgorin radius (Prop. \ref{GershgorinRadiiOfCayleyDistanceKernel}) as well as being the eigenvalue of the kernel on the homogeneous distribution (Example \ref{HomogeneousDistributionIsEigenvalue}).

\begin{lemma}\label{SumOfExpLambdaNumCyclesOverPermutations}
For $n \in \mathbb{N}$, with $Sym(n)$ denoting the [[symmetric group]] on $n$ elements, and for any [[variable]] $\beta$, we have (as an [[equation]] between [[polynomials]] in $e^\beta$):
  $$
    \underset{
      \sigma \in Sym(n)
    }{
      \sum
    }
    e^{ \beta \cdot \left\vert Cycles(\sigma) \right\vert }
    \;=\;
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\beta} + k
    \big)
    \,.
  $$
\end{lemma}
In [Stanley 11, Prop. 1.3.7](#Stanley11) are offered four proofs of this lemma, see also discussion at [MO:q/245005](https://mathoverflow.net/q/245005/381); we now spell out the proof idea given in [Math.SE:a/92051](https://math.stackexchange.com/a/92051/58526):
\begin{proof}
Notice that every [[permutation]] $\sigma$ has a *unique* representative in [[cycle notation]]
\[
  \label{NormalizedCycleNotation}
  \begin{aligned}
    \sigma
    & = \;
    (h_1 t_{11} t_{12} \cdots)
    (h_2 t_{21} t_{22} \cdots)
    (h_3 t_{31} t_{32} \cdots)
    \cdots 
    \\
    & =
    \vert
    h_1 t_{11} t_{12} \vert
    h_2 t_{21} t_{22} \vert
    h_3 t_{31} t_{32} \vert \cdots 
  \end{aligned}
\]
with the property that the following two conditions hold:

1. heads are smallest in their cycle: $h_i \lt t_{i j}$,

1. cycles are ordered by their heads: $h_i \lt h_{i + 1}$. 

This yields a [[bijection]] between the set of permutations and the set of [[sections]] $sec$ of the following [[indexed family]] of sets

\[
  \label{SectionDeterminingAPermutation}
  \array{
    \underset{
      k \in \{1, \cdots, n\}  
    }{\sqcup}
    \{0, \cdots, k-1\}
    \\
    {}^{\mathllap{p_n}}
    \big\downarrow
    \;
    \big\uparrow {}^{\mathrlap{sec}}
    \\
    \{1, \cdots, n\}
  }
\]

as follows:

To a given section $sec$, assign the permutation whose normalized cycle notation (eq:NormalizedCycleNotation) has underlying it (forgetting the bars "$\vert$") the [[list]] obtained by setting

$$
  list_0
  \;\coloneqq\;
  \varnothing
$$

and then [[recursion|recursively]] adding the element $k+1$ to the list at stage $k$ by 

* either appending it on the right, if $sec(k+1) = 0$;

* or inserting it *after* the $sec(k+1)$-st element already in the list:

$$
  list_{k+1}
  \;\coloneqq\;
  \left\{
  \array{
    [ list_k, k+1 ] &if& sec(k+1) = 0
    \\
    [ list_k^{ \leq sec(k+1)}, k+1 , list_k^{\gt sec(k+1)} ]
    & if & sec(k+1) \gt 0 
  }
  \right.
$$

The resulting $list_n$, with a bar "$\vert$" inserted right before each element $k$ with $sec(k) = 0$, is a normalized cycle notation (eq:NormalizedCycleNotation) for a permutation, and every such arises this way, uniquely.

Via this bijection, the number of cycles of a permutation equals the number of times that the corresponding section $sec$ (eq:SectionDeterminingAPermutation) takes the value 0. Therefore we have:

$$
  \begin{aligned}
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{\beta \cdot \left\vert Cycles(\sigma) \right\vert}
  \;\;\;
  & = \;
  \underset{
    sec \in \Gamma(p_n)
  }{\sum}
  e^{ \beta \cdot \left\vert sec^{-1}(\{0\}) \right\vert }
  \\
  & = \;
  \underset{
    sec \in \Gamma(p_n)
  }{\sum}
  \underoverset
    {k = 1}
    {n}
    {\prod} 
  \left\{
  \array{
    e^{\beta} &\vert& sec(k) = 0
    \\
    1 &\vert& otherwise
  }  
  \right.
  \\
  & = \;
  \underoverset
    {k = 1}
    {n }
    {\prod}
  \;
  \underset{
    sec(k) \in \{0, \cdots, k-1\}
  }{\sum}
  \;
  \left\{
  \array{
    e^{\beta} &\vert& sec(k) = 0
    \\
    1 &\vert& otherwise
  }  
  \right.
  \\
  & = \;
  \underoverset
    {k = 1}
    {n  }
    {\prod}
  \;
  \big(
     e^{\beta}
     +
     (k-1)
  \big)
  \\
  & =
  \underoverset
    {k = 0}
    {n -1 }
    {\prod}
  \;
  \big(
     e^{\beta}
     +
     k
  \big)
  \end{aligned}
$$
\end{proof}

An immediate variant of Lemma \ref{SumOfExpLambdaNumCyclesOverPermutations}:

\begin{lemma}\label{SumOfSgnExpLambdaNumCyclesOverPermutations}
For $n \in \mathbb{N}$, with $Sym(n)$ denoting the [[symmetric group]] on $n$ elements, and for any [[variable]] $\beta$, we have (as an [[equation]] between [[polynomials]] in $e^\beta$):
  $$
    \underset{
      \sigma \in Sym(n)
    }{
      \sum
    }
    sgn(\sigma)
      \cdot
    e^{ \beta \cdot \left\vert Cycles(\sigma) \right\vert }
    \;=\;
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\beta} - k
    \big)
    \,,
  $$
  where 
  $sgn(\sigma)$ denotes the [[signature of a permutation]]. 
\end{lemma}
This is mentioned, without proof, at [MO:q/245010](https://mathoverflow.net/a/245010/).
\begin{proof}
  We compute as follows:
$$
  \begin{aligned}
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      e^{\beta} - k
    \big)
    & 
    \;=\;
    (-1)^n
    \underoverset    
      {k = 0}
      {n-1}
      {\prod}
    \big(
      - e^{\beta} + k
    \big)
    \\
    & 
    \;=\;
    (-1)^n
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-e^\beta)^{\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-1)^{n - \left\vert Cycles(\sigma)\right\vert}
    \cdot
    (e^\beta)^{\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    (-1)^{\left\vert EvenLengthCycles(\sigma)\right\vert}
    \cdot
    (e^\beta)^{\left\vert Cycles(\sigma)\right\vert}
    \\
    & \;=\;
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    sgn(\sigma)
    \cdot
    (e^\beta)^{\left\vert Cycles(\sigma)\right\vert}
  \end{aligned}
$$

Here the second step is Lemma \ref{SumOfExpLambdaNumCyclesOverPermutations}.

To see the fourth step, notice that if $n$ is even/odd there must be an even/odd number of permutations of odd length. Therefore $n$ plus the number of odd-length permutations cancels out in signs and thus leaves the sign of the number of even permutations.

The last step is the observation that the signature of a permutation is the sign of its number of even-length permutations, since for each cycle there is one less transposition than elements in the cycle (see [here](Cayley+distance#eq:CyclicPermutationAsProductOfTranspositions)).
\end{proof}


Another immediate consequence of Lemma \ref{SumOfExpLambdaNumCyclesOverPermutations} is this:

\begin{lemma}\label{SumOverFirstRowOfCayleyDistanceKernel}
**(sum over first row of Cayley distance kernel)** \linebreak
  For $n \in \mathbb{N}$, the [[sum]] over the first row of the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) equals
\[
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \beta \cdot d_C(\sigma, e) }
  \;=\;  
  e^{- \beta \cdot n }
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    + 
    k
  \big)
\]
\end{lemma}
\begin{proof}
We compute as follows:
$$
  \begin{aligned}
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \beta \cdot d_C(\sigma, e) }
  &
  \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ - \beta \cdot (n - \left\vert Cycles(\sigma) \right\vert ) }
  \\
  & 
  \;=\;
  e^{- \beta \cdot n }
  \,
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  e^{ \beta \cdot  \left\vert Cycles(\sigma) \right\vert }  
  \\
  & =\;
  e^{- \beta \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
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



### Gershgorin disc

We discuss the [[Gershgorin radius]] of the Cayley distance kernel, in Prop. \ref{GershgorinRadiiOfCayleyDistanceKernel} below.


\begin{prop}\label{GershgorinRadiiOfCayleyDistanceKernel}
**([[Gershgorin radius]] of [[Cayley distance kernel]])**
  For $n \in \mathbb{N}$, 
 the [[Gershgorin radii]] of the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) are all equal to
\[
  \label{GershgorinRadiusExpression}
    r(\beta)
    \;=\;
  e^{- \beta \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    + 
    k
  \big)
  - 
  1
\]
\end{prop}
\begin{proof}
  By [[right invariant metric|right invariance]] of the [[Cayley distance]] ([this Prop.](Cayley+distance#CayleyMetricIsRightInvariant)) the sum over entries of any row is equal to that of the first row.
Since moreover 

* all entries are [[real number|real]] and non-[[negative number|negative]],  hence equal to their [[absolute value]],

* the diagonal elements are all equal to $1 = e^{ - \beta \cdot 0 }$,

it follows that this sum over the first row equals the Gershgorin radius plus 1 (by its defining formula [here](Gershgorin+circle+theorem#eq:GershoginRadiusFormula)). Therefore the statement follows by Lemma \ref{SumOverFirstRowOfCayleyDistanceKernel}.
\end{proof}




\linebreak

### Eigenvectors

We discuss some [[eigenvectors]] of the Cayley distance kernel. 


#### The homogeneous distribution

\begin{example}\label{HomogeneousDistributionIsEigenvalue}
Clearly $(1)_{\sigma \in Sym(n)}$ is an eigenvector with eigenvalue $e^{- \beta \cdot n }
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}\big(e^{\beta}+ k \big)$.
\end{example}
(by Lemma \ref{SumOfExpLambdaNumCyclesOverPermutations})

#### The signature distribution

\begin{prop}\label{SignatureDistributionIsEigenvector}
A further [[eigenvector]] of the Cayley distance kernel is $(sgn(\sigma))_{\sigma \in Sym(n)}$ with corresponding [[eigenvalue]] 

\[
  \label{EigenvectorOfSignDistribution}
  EV
  \big
    (sgn(\sigma))_{\sigma \in Sym(n)}  
  \big)
  \;=\;
  e^{- \beta \cdot n }
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}\big(e^{\beta}- k \big)
  \,.
\]

\end{prop}
\begin{proof}
That this is an eigenvector follows from the following calculation:

The $\tau$ component of the image of this vector is 

$$
\begin{aligned}
\underset{
    \sigma \in Sym(n)
  }{\sum} sgn(\sigma)
  e^{ - \beta \cdot d_C(\sigma, \tau) }
  &\;=\; 
\underset{
    \sigma \in Sym(n)
  }{\sum} sgn(\tau)sgn(\sigma \cdot \tau^{-1})
  e^{ - \beta \cdot d_C(\sigma \cdot \tau^{-1}, e) }
\\
 & \;=\; 
sgn(\tau)\underset{
    \sigma \in Sym(n)
  }{\sum} sgn(\sigma)
  e^{ - \beta \cdot d_C(\sigma, e) }.
\end{aligned}
$$
  

This follows from the [[right invariant metric|right invariance]] of the [[Cayley distance]] ([here](Cayley+distance#Invariance)) and the fact that $sgn$ is a multiplicative character, $sgn(\sigma \cdot \tau) = sgn(\sigma)\cdot sgn(\tau)$. Thus $(sgn(\sigma))_{\sigma \in Sym(n)}$ is an eigenvector and the corresponding eigenvalue equals the signed sum of, in particular, the first row of the Cayley distance kernel. This is as claimed by Lemma \ref{SumOverSgnFirstRowOfCayleyDistanceKernel}.
\end{proof}



\begin{lemma}\label{SumOverSgnFirstRowOfCayleyDistanceKernel}
**(signed sum over first row of Cayley distance kernel)** \linebreak
  For $n \in \mathbb{N}$, the [[sum]] over the first row of the signed Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) equals
$$
  \underset{
    \sigma \in Sym(n)
  }{\sum}
 sgn(\sigma) \cdot e^{ - \beta \cdot  d_C(\sigma, e) }
  \;=\;  
  e^{- \beta \cdot n }
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    - 
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
  sgn(\sigma) \cdot e^{ - \beta \cdot  d_C(\sigma, e) }
  &
  \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  sgn(\sigma) \cdot e^{ - \beta \cdot (n - \left\vert Cycles(\sigma) \right\vert ) }
  \\
  & 
  \;=\;
  e^{- \beta \cdot n }
  \,
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  sgn(\sigma) \cdot e^{ \beta \cdot  \left\vert Cycles(\sigma) \right\vert }  
  \\
  & =\;
  e^{- \beta \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    - 
    k
  \big)
  \mathrlap{\,,}
  \end{aligned}
$$
where:

* the first step is [Cayley's observation](Cayley+distance#CayleyObservation),

* the last step uses Lemma \ref{SumOfSgnExpLambdaNumCyclesOverPermutations}.

\end{proof}

\begin{prop}\label{SignOfTheEigenvalueOfTheSigantureDistribution}
The sign of the eigenvalue (eq:EigenvectorOfSignDistribution) is as follows:
\[
  \label{TheSignOfTheEigenvalueOfTheSignatureDistribution}
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  \!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!\!
  EV
  \big(
    (sgn(\sigma))_{\sigma \in Sym(n)}  
  \big)
  \;is\;
  \left\{
  \array{
     \gt 0 
       & for & 
     \mathrlap{
       e^\beta \gt n-1
     }
     \\
     = 0 
       & for & 
     \mathrlap{
       e^\beta \in \{1,2, \cdots, n-1\}
     }
     \\
     \lt 0 
       & for & 
     \mathrlap{
       e^{\beta} \in (n-2a-2,  n-2a-1),\, a \in \mathbb{N}
     }
  }
  \right.
\]
\end{prop}
\begin{proof}
  Since the prefactor $e^{- \beta \cdot n}$  in (eq:EigenvectorOfSignDistribution) is always positive, we need to equivalently discuss the sign of the polynomial
  $$
    \underoverset
      {k = 0}
      {n - 1}
      {\prod}\big(e^{\beta} - k \big)
    \,.
  $$
  Here the first two statements are immediate. For the last last statement, observe that all roots of the polyonomial appear with unit multiplicity, so that the polynomial must change sign as $e^\beta$ crosses over any of its zeros. Therefore the value which is positive for $e^\beta \gt n-1$, by the first statement, must become negative as $e^\beta$ drops below $n=1$, then positive again as it drops below the next zero at $n - 2$, and negative once more as $e^\beta$ drops below $n - 3$, and so on.
\end{proof}



#### Further eigenvectors

\begin{remark}
Since Example \ref{HomogeneousDistributionIsEigenvalue} and Prop. \ref{SignatureDistributionIsEigenvector} rely on $1(\sigma)$
and $sgn(\sigma)$ being multiplicative [[group characters]], and the only multiplicative characters of a symmetric group are these two, the trivial one and the [[sign representation|sign]], the other eigenvectors must be found by other means.
\end{remark}


\linebreak

### Positivity
 {#Positivity}

\begin{prop}\label{FailureOfPositivityForBetaBelowLn2}
  For all $n \geq 3$ and all $0 \lt \beta \lt ln(2)$, the Cayley distance kernel $ e^{- \beta \cdot d_C}$ *fails* to be positive semi-definite on $Sym(n)$.
\end{prop}
\begin{proof}
By Example \ref{CayleyDistanceKernelOnSym3} the statement holds for $n = 3$. But the kernel for this case is a [[principal submatrix]] of the kernels in all other cases (see [this Prop.](Cayley+distance#CayleyDistancePreservedByInclusionOfSymmetricGroups)), and positivity fails as soon as it fails on any principal submatrix. (This is immediate from the definition, but also a direct consequence of [[Cauchy's interlace theorem]].)
\end{proof}

More generally:


\begin{prop}\label{CayleyDistanceKernelIsIndefiniteForEBetaNonIntegralAndSmallernminusone}
The Cayley distance kernel $e^{- \beta \cdot d_C}$ (Def. \ref{CayleyDistanceKernel}) on $Sym(n)$
is indefinite for all
$$
  e^{\beta}
  \;\in\;
  (
    n - 2a - 2,  \lt n - 2a - 1
  )
  \,,
  \;\;
  a \in \mathbb{N}
  \,,
$$
or equivalently: 

For $0 \lt e^\beta \lt n-1$ the Cayley distance kernel is indefinite except possibly at [[integer]] values.
\end{prop}
\begin{proof}
With the third statement in Prop. \ref{SignOfTheEigenvalueOfTheSigantureDistribution} the claim follows for every *second* open unit [[interval]] between 0 and $n-1$. But by the same argument the analogous statement is then true on every *other* of these unit intervals for the kernel on $Sym(n-1)$.
Now since the kernel on $Sym(n-1)$ is a [[principal submatrix]] of that for $Sym(n)$ (see [this Prop.](Cayley+distance#CayleyDistancePreservedByInclusionOfSymmetricGroups)), the [[Cauchy interlace theorem]] implies that the kernel on $Sym(n)$ must have a negative eigenvalue as soon as that on $Sym(n-1)$ does.
\end{proof}



\begin{prop}
  A sufficient condition for the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) on $Sym(n)$ to be [[positive semi-definite bilinear form|positive semi-definite]] is that its [[inverse temperature]] $\beta$ satisfies the following [[inequality]]:

\[
  \label{GershgorinBoundOnTemperatureForPositivity}
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    + 
    k
  \big)
  \;\leq\;
  2
  e^{\beta \cdot n }
  \,.
\]
\end{prop}
\begin{proof}
  By the [[Gershgorin circle theorem]] and using Prop. \ref{GershgorinRadiiOfCayleyDistanceKernel},
  all the [[eigenvalues]] of the kernel are within a distance $r(\beta)$ (eq:GershgorinRadiusExpression) from its diagonal values, which are all equal to $1 = e^{- \beta \cdot 0}$. 
Since, moreover, all eigenvalues are [[real numbers|real]], the condition
$$ 
  r(\beta)
    \;=\;
  e^{- \beta \cdot n }
  \,
  \underoverset
    {k = 0}
    {n - 1}
    {\prod}
  \big(
    e^{\beta}
    + 
    k
  \big)
  - 
  1
\;\;\leq\;\; 
1
$$
implies that all eigenvalues are contained in the [[interval]] $[0,2] \subset \mathbb{R}$ and hence in particular that they are non-negative.
\end{proof}

\begin{prop}\label{ExplicitBoundForInverseTemperatureEnsuringPositivity}
  For [[inverse temperature]] being the [[natural logarithm]] of a [[natural number]]
\[
  \label{InverseTemperatureEqualToNaturalLogarithmOfNaturalNumber}
  \beta
  \;=\;
  \ln(N)
  \,,
  \;\;\;
  N \,\in\, \mathbb{N}
\]
a sufficient condition for the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) to be [[positive semi-definite bilinear form|positive semi-definite]] on $Sym(n)$ is that 
$$
  N
    \;\geq\;
  \frac{
    n-1
  }{
    2^{1/n} - 1
  }  
  \,.
$$
\end{prop}
\begin{proof}
In the given case (eq:InverseTemperatureEqualToNaturalLogarithmOfNaturalNumber)
the Gershgorin bound (eq:GershgorinBoundOnTemperatureForPositivity) for positive semi-definity of the Cayley distance kernel reads
$$   
  \underset{
   = (N + n - 1)! / (N - 1)!
  }{
  \underbrace{
    N
    (N + 1)
    (N + 2)
    \cdots
    (N + n - 1)
  }
  }
  \;\leq\;
  2
  N^n
$$
and hence may equivalently be expressed as
\[
  \label{GershgorinPositivityBoundForInverseTemperatureTheLogOfNaturalNumber}
  \array{
  &
  \frac{
    N (N + 1 ) \cdots (N + n -1) 
  }{
    N^n
  }
  &
  \;\leq\;
  2   
  \\
  \Leftrightarrow
  &
  \left(
    { N + n - 1 }
    \atop
    { N -1 }
  \right)
  \cdot
  \frac{
    n !
  }{
    N^n 
  }
  &
  \;\leq\;
  2   
  }
  \;\;\;\;\;\;
    \Rightarrow
  \;\;\;\;\;\;
  e^{- ln(N) \cdot d_C}
  \,
  \text{is positive semi-definite on}
  \,
  Sym(n)
  \,.
\]

With the evident bound
$$
  \frac{
    N (N + 1 ) \cdots (N + n -1) 
  }{
    N^n
  }
  \;\leq\;
  \left(
    \frac{
      N + n - 1
    }{
      N
    }
  \right)^n
  \;=\;
  \left(
  1 
    + 
  \frac{
    n - 1
  }{
    N
  }
  \right)^n
  \,,
$$
the condition (eq:GershgorinPositivityBoundForInverseTemperatureTheLogOfNaturalNumber) is satisfied as soon as
$$
  \begin{aligned}
  & 
  \left(
  1 
    + 
  \frac{
    n - 1
  }{
    N
  }
  \right)^n
  \;\leq\;
  2
  \\
  \Leftrightarrow
  \;\;\;
  &
  N
    \;\geq\;
  \frac{
    n-1
  }{
    2^{1/n} - 1
  }
  \end{aligned}
$$
\end{proof}

\begin{remark}
  Computer-experiment suggests ([CSS21](#CSS21)) that the above bounds (Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity}) are extremely loose: For the first few values of $N$, at least, the inverse temperature $\beta = ln(N-1)$ is already sufficient for positive semi-definiteness.
\end{remark}





## Related concepts

* [[Mallows kernel]], [[Kendall kernel]]

* [[kernel method]]


## References

Mentioning of the Cayley distance kernel:

* [[Michael A. Fligner]], [[Joseph S. Verducci]], Section 4 of: *Distance Based Ranking Models*, Journal of the Royal Statistical Society. Series B (Methodological) Vol. 48, No. 3 (1986), pp. 359-369 ([jstor:2345433](https://www.jstor.org/stable/2345433))

* [[Persi Diaconis]], [[Phil Hanlon]], Section 4 of: *Eigen Analysis for Some Examples of the Metropolis Algorithm*, in Donald Richards (ed.) *Hypergeometric Functions on Domains of Positivity, Jack Polynomials, and Applications*, Contemporary Mathematics Vol. 138, AMS 1992 ([doi:10.1090/conm/138](http://dx.doi.org/10.1090/conm/138), [EFS NSF 392](https://statistics.stanford.edu/research/eigen-analysis-some-examples-metropolis-algorithm), [pdf](https://statweb.stanford.edu/~cgates/PERSI/papers/eigen-metalg.pdf))

* [[Michael A. Fligner]], [[Joseph S. Verducci]] (eds.), p. xx of: *Probability Models and Statistical Analyses for Ranking Data*, Lecture Notes in Statistics **80**, Springer 1993 ([doi:10.1007/978-1-4612-2738-0](https://link.springer.com/book/10.1007/978-1-4612-2738-0))

The above discussion is largely motivated from and overlaps with:

* {#CSS21} *[[schreiber:Weight systems that are quantum states]]*


Supplementary references:

* {#Stanley11} [[Richard Stanley]], *[Enumerative combinatorics](http://www-math.mit.edu/~rstan/ec/)* -- [Volume 1](http://www-math.mit.edu/~rstan/ec/ec1/), Wadsworth & Brooks/Cole Mathematics Series book series 1986, 1997 ([doi:10.1007/978-1-4615-9763-6](https://link.springer.com/book/10.1007/978-1-4615-9763-6)) reprinted in: Cambridge Studies in Advanced Mathematics, Cambridge University Press 2011 ([ISBN:9781107602625](https://www.cambridge.org/us/academic/subjects/mathematics/discrete-mathematics-information-theory-and-coding/enumerative-combinatorics-volume-1-2nd-edition?format=PB&isbn=9781107602625), [pdf](http://www-math.mit.edu/~rstan/ec/ec1.pdf))



[[!redirects Cayley distance kernels]]
