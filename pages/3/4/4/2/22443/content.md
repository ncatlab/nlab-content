

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

We prove below (following [CSS21](#CSS21)) that for *integer* values of $N \coloneqq e^\beta$ the Cayley distance kernel is always positive (semi-)definite, see Example \ref{CayleyDistanceKernelOnSym4}. At exactly these values the Cayley distance kernel equals ([CSS21](#CSS21)) the [[fundamental representation|fundamental]] $\mathfrak{gl}(N)$-[[Lie algebra weight system]] on [[horizontal chord diagrams]] (for the [[general linear Lie algebra]] $\mathfrak{gl}(n)$ regarded as a [[metric Lie algebra]] with the [[trace]] in its defining [[fundamental representation]], as in [Bar-Natan 95](stringy+weight+systems+span+classical+Lie+algebra+weight+systems#BarNatan95)) under the [[monoid]]-[[homomorphism]] 

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

This exhibits the general behaviour discussed as 
Prop. \ref{FailureOfPositivityForBetaBelowLn2}, 
Prop. \ref{PositiveSemidefinitenessAtLowIntegerValuedOfEBeta}, 
Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity} below.


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

One sees that the kernel is:

$$
  \array{
    \mathllap{
      \text{indefinite} 
    }
    & \text{for} & 
    \mathrlap{
      e^{\beta} \in (1,2)
    }
    \\
    \mathllap{
      \text{positive semi-definite} 
    }
    &\text{for}& 
    \mathrlap{
      e^{\beta} = 2
    }
    \\
    \mathllap{
      \text{indefinite} 
    }
    & \text{for} & 
    \mathrlap{
      e^{\beta} \in (2,3)
    }
    \\
    \mathllap{
      \text{positive semi-definite} 
    } 
    &\text{for}& 
    \mathrlap{
      e^{\beta} = 3
    }
    \\
    \mathllap{
      \text{positive definite}
    } 
    &\text{for}&  
    \mathrlap{
      e^{\beta} \gt 3
    }
  }
$$

This exhibits the general behaviour discussed as 
Prop. \ref{CayleyDistanceKernelIsIndefiniteForEBetaNonIntegralAndSmallernminusone},
Prop. \ref{PositiveSemidefinitenessAtLowIntegerValuedOfEBeta} and
, Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity} below.


\end{example}


\begin{example}\label{CayleyDistanceKernelOnSym6}
**(Cayley distance kernel on Sym(6))**

Similarly, here is the graph of the lowest eigenvalue of the Cayley distance kernel on $Sym(6)$ (from [Bar-Natan 21](#BarNatan21)):

<a href="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym6.jpg">
<img src="https://ncatlab.org/nlab/files/LowestEigenvalueOfCayleyDistanceKernelOnSym6.jpg" width="440">
</a>



\end{example}


## Properties

### Some lemmas

#### Sum over one row

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



#### Gershgorin radius

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
 {#TheSignatureDistribution}

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

\begin{lemma}\label{SignOfTheEigenvalueOfTheSigantureDistribution}
The sign of the eigenvalue (eq:EigenvectorOfSignDistribution) of the signature distribution is as follows:
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
       e^\beta \gt n-1 \;or\; e^{\beta} \in (n-2a-3,  n-2a-2),\, a \in \mathbb{N}
     }
     \\
     = 0 
       & for & 
     \mathrlap{
       e^\beta \in \{0,1,2, \cdots, n-1\}
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
\end{lemma}
\begin{proof}
  Since the prefactor $e^{- \beta \cdot n}$  in (eq:EigenvectorOfSignDistribution) is always positive, we need to equivalently discuss the sign of the polynomial
  $$
    \underoverset
      {k = 0}
      {n - 1}
      {\prod}\big(e^{\beta} - k \big)
    \,.
  $$
  Here the first two statements are immediate. For the last last statement, observe that all roots of the polynomial appear with unit multiplicity, so that the polynomial must change sign as $e^\beta$ crosses over any of its zeros. Therefore the value which is positive for $e^\beta \gt n-1$, by the first statement, must become negative as $e^\beta$ drops below $n=1$, then positive again as it drops below the next zero at $n - 2$, and negative once more as $e^\beta$ drops below $n - 3$, and so on.
\end{proof}



#### General eigenvectors

The general eigenvectors and eigenvalues of the Cayley distance kernel are given as explicit expressions in the [[irreducible characters]] of the [[symmetric group]], by the *[character formula](Cayley+graph+spectrum#CharacterFormulaForCayleyGraphSpectra) of [[Cayley graph spectra]]*:

To be able to apply this formula, one just has to observe that the exponentiated [[Cayley distance]] in a single variable

$$
  \array{
    Sym(n)
    &\longrightarrow&
    \mathbb{R} 
    \mathrlap{
      \hookrightarrow \mathbb{C}
    }
    \\
    \sigma &\mapsto& e^{- \beta \cdot d_C(\sigma,e)}
  }
$$

is a [[class function]] for all $\beta$, which is immediate by [Cayley's observation](Cayley+distance#CayleyObservation) that $d_c(\sigma,e) = n - \left\vert Cycles(\sigma)\right\vert$.

It thus follows from the general [character formula](Cayley+graph+spectrum#CharacterFormulaForCayleyGraphSpectra) and the [[representation theory of the symmetric group]] ([here](representation+theory+of+the+symmetric+group#IrreducibleRepresentations)) that:


\begin{prop}\label{CharacterFormulaForEigenvalues}
**(character formula for eigenvalues)** \linebreak
  The [[eigenvalues]] of the Cayley distance kernel $e^{- \beta \cdot d_C}$ on $Sym(n)$ are:

1. labeled by [[partitions]] $\lambda$ of $n$:

   \[
     \label{EigenvaluesLabeledByPartitions}
     \big(
       EigVals[e^{-\beta \cdot d_C}]_\lambda
     \big)_{\lambda \in Part(n)}
   \]

1. have multiplicity the square $\big(\chi^{(\lambda)}(e)\big)^2$ of the [[dimension]] of the $\lambda$th [[Specht module]];

1. are given by

   \[
     \label{CharacterFormulaForEigenvalueOfCayleyDistanceKernel}
     EigVals[e^{- \beta\cdot d_C}]_\lambda
     \;=\;
     \tfrac{1}{\chi^{(\lambda)}(e)}
     \underset{ \sigma \in Sym(n) }{\sum}
     e^{ \beta \cdot ( \left\vert Cycles(\sigma)\right\vert - n )   }
     \cdot
     \chi^{(\lambda)}(\sigma)
     \,,
   \]
 
   where $\chi^{(\lambda)}$ is the [[irreducible character]] corresponding to the $\lambda$th [[Specht module]].

1. correspond to [[eigenvectors]] given by the [[complex conjugation|complex conjugate]] of the $(i,j)$-components, for fixed $i,j  \in \big\{1, \cdots, \chi^{(\lambda)}(e) \big\}$, of the $\lambda$th [[Specht module]] $S^{(\lambda)} \colon Sym(n) \to U\big(\chi^{(\lambda)}(e)\big)$ regarded for each [[permutation]] $\sigma$ as a [[unitary matrix]] $\big(S^{(\lambda)}(\sigma)_{i,j}\big)_{i,j}$:

   \[
     \label{EigenvectorsOfCayleyDistanceKernel}
     \left\vert 
       \lambda, (i,j)
     \right\rangle
     \;\coloneqq\;
     EigVects[e^{-\beta \cdot d_X}]_{\lambda, i, j}
     \;=\;
     \big(
       \bar S^{(\lambda)}(\sigma)_{i j}
     \big)_{\sigma \in Sym(n)}
     \;\;
     \in
     \;
     \mathbb{C}[Sym(n)]
     \,.
   \]
 
\end{prop}

\linebreak

{#EigenvaluesFurther} We further characterize these eigenvalues (Prop. \ref{EigenvaluesAtLogIntegerInvTemViaYoungTabl} below) at the special inverse temperatures of the form $\beta = ln(N)$. First we need some notation and a lemma:

\begin{defn}\label{SetsOfSemistandardYoungTableau}
  **(notation for sets of semistandard Young tableaux)** \linebreak
  For $n, N \in \mathbb{N}$, write 

  $$
    ssYT_n(N)
    \;\in\;
    Set
  $$

  for the [[set]] of [[semistandard Young tableau]]

  * with $n$ boxes, and 

  * all labels $\leq N$.

  Moreover for $\lambda \in Part(n)$ write

  $$
    ssYT_{\lambda \vdash n}(N)  
    \;\coloneqq\;
    \big\{
      T \in ssYT_n(N)
      \;\vert\;
      \lambda 
        = 
      \left\vert T \right\vert
    \big\}
    \;\subset\;
    ssYT_{n}(N)      
  $$

  for the [[subset]] on those tableau $T$ whose underlying [[Young diagram]] $\left\vert T \right\vert$ corresponds to the partition $\lambda$.

\end{defn}

\begin{lemma}\label{CharacterForumlaForIntegerExponentialByCycleNumber}
**(character formula for integer exponential by cycle number)** \linebreak  
  For $N \in \mathbb{N}$ the [[exponential]] of $N$ to the number of [[permutation cycles|cycles of a permutation]] is, as a [[class function]], equal to the sum of [[irreducible characters]] weighted by the number of corresponding [[semistandard Young tableaux]] (Def. \ref{SetsOfSemistandardYoungTableau}):

$$
  N^{\left\vert Cycles(-) \right\vert}
  \;=\;
  \underset{
    T \in ssYT_n(N)
  }{\sum}
  \chi^{ \left\vert T \right\vert }(-)
  \,.
$$

\end{lemma}

This is the statement of [Gnedin, Gorin & Kerov 11, Prop. 2.4](#GnedinGorinKerov11) (with notation from Prop. 2.1).

\begin{proposition}\label{EigenvaluesAtLogIntegerInvTemViaYoungTabl}
**(Eigenvalues of Cayley distance kernel at $\beta = ln(N)$ count semistandard Young tableaux)** \linebreak

For $N \in \mathbb{N}$
and $\lambda \in Part(n)$, the $\lambda$th eigenvalue (eq:EigenvaluesLabeledByPartitions) of the Cayley distance kernel at $\beta = ln(N)$ on $Sym(n)$ is proportional to the number $\left\vert ssYT_{\lambda \vdash n}(N)\right\vert$ of [[semistandard Young tableaux]] (Def. \ref{SetsOfSemistandardYoungTableau})

\[
  \label{EigenvaluesAtLogIntegerInverseTempeteratureCountingYoungTableaux}
  EigVals[e^{- ln(N) \cdot d_c}]_\lambda
  \;=\;
  \tfrac{n!}{N^n \cdot \chi^{(\lambda)}(e)}
  \left\vert ssYT_{\lambda}(N)\right\vert 
  \,.
\]

\end{proposition}

\begin{proof}

  We compute as follows:
  $$
    \begin{aligned}
      \mathrm{EigVals}[e^{-\mathrm{ln}(N) \cdot d_C}]_\lambda
      & 
      \;=\;
      \frac{
        e^{- \mathrm{ln}(N)\cdot n}
      }{
        \chi^{(\lambda)}(e)
      }
      \underset{\sigma \in \mathrm{Sym}(n)}{\sum}
      \chi^{(\lambda)}(\sigma)
        \cdot
      N^{\# \mathrm{cycles}(\sigma)}
      \\
      &
      \;=\; 
      \frac{
        e^{- \mathrm{ln}(N)\cdot n}
      }{
        \chi^{(\lambda)}(e)
      }
      \underset{\sigma \in \mathrm{Sym}(n)}{\sum}
      \chi^{(\lambda)}(\sigma)
        \cdot
      \big(
        N \cdot 1^{\ell_1(\sigma)} 
      \big)
      \big(
        N \cdot 1^{\ell_2(\sigma)}
      \big)
      \cdots
      \big(
        N \cdot 1^{\ell_{\#\mathrm{cycles}(\sigma)}(\sigma)}
      \big)
      \\
      & 
      \;=\;
      n!
      \frac{
        e^{- \mathrm{ln}(N)\cdot n}
      }{
        \chi^{(\lambda)}(e)
      }
      \cdot
      s_\lambda
      \big(
        x_1 \!=\! 1,
        \cdots,
        x_N \!=\! 1
      \big)
      \\
      &
      \;=\;
      n!
      \frac{
        e^{- \mathrm{ln}(N)\cdot n}
      }{
        \chi^{(\lambda)}(e)
      }
      \,
      \cdot
      \,
      \# \mathrm{ssYT}_\lambda\!(N)
      \,.
    \end{aligned}
  $$

Here 

* the first line is the [character formula for kernel spectra](Cayley+graph+spectrum#CharacterFormulaForCayleyGraphSpectra) \eqref{CharacterFormulaForEigenvalueOfCayleyDistanceKernel},

* the third step is the [character formula for Schur polynomials](Schur+function#FrobeniusFormula),

* the last step is their [counting property](Schur+function#eq:SchurPolynomialCountsNumberOfSemiStandardYoungTableaux).


Alternatively, using Lemma \ref{CharacterForumlaForIntegerExponentialByCycleNumber} we may compute as follows:

$$
  \begin{aligned}
    EigVals[e^{- ln(N) \cdot d_C}]_\lambda
    & 
    \;=\;
    \tfrac{1}{\chi^{(\lambda)}(e)}
    \underset{\sigma \in Sym(n)}{\sum}
    e^{ ln(N) ( \left\vert Cycles(\sigma) \right\vert ) - n }
    \cdot
    \chi^{(\lambda)}(\sigma)
    \\
    &
    \;=\;
    \tfrac{1}{\chi^{(\lambda)}(e)}
    \underset{\sigma \in Sym(n)}{\sum}
    e^{ ln(N) ( \left\vert Cycles(\sigma) \right\vert ) - n }
    \cdot
    \bar \chi^{(\lambda)}(\sigma)
    \\
    &
    \;=\;
    \tfrac{1}{N^n \cdot \chi^{(\lambda)}(e)}
    \underset{\sigma \in Sym(n)}{\sum}
    N^{ \left\vert Cycles(\sigma) \right\vert  }
    \cdot
    \bar \chi^{(\lambda)}(\sigma)
    \\
    &
    \;=\;
    \tfrac{1}{N^n \cdot \chi^{(\lambda)}(e)}
    \underset{
      T \in ssYT_n(N)
    }{\sum}
    \underset{\sigma \in Sym(n)}{\sum}
    \chi^{ \left\vert T \right\vert }(\sigma)
    \cdot
    \bar \chi^{(\lambda)}(\sigma)
    \\
    &
    \;=\;
    \tfrac{n!}{N^n \cdot \chi^{(\lambda)}(e)}
    \underset{
      T \in ssYT_n(N) 
    }{\sum}
    \delta^{ \left\vert T\right\vert, \lambda }
  \end{aligned}
$$

Here the first line is the character expression (eq:CharacterFormulaForEigenvalueOfCayleyDistanceKernel) of the eigenvalues from Prop. \ref{CharacterFormulaForEigenvalues}. The second line passes to the [[complex conjugation]] using that all eigenvalues are real (the Cayley distance kernel being a real symmetric matrix). 
The fourth step inserts the character formula from Lemma \ref{CharacterForumlaForIntegerExponentialByCycleNumber}. 
The last step follows with [[Schur orthogonality]] ([this equation](Schur+orthogonality+relation#eq:FirstSchurOrthogonalityRelation)).

\end{proof}

As a corollary we obtain:

\begin{prop}\label{PositivitiViaCountingOfYoungTableaux}
**(non-negativity of Cayley distance kernel at log-integer inverse temperature)** \linebreak

For the Cayley distance kernel at $\beta = ln(N)$ with $N \in \mathbb{N}$:

1. all eigenvalues (eq:EigenvaluesLabeledByPartitions) are non-negative 

   $$
     \underset{\lambda \in Part(n)}{\forall}
     \,
     EigVals[e^{- ln(N) \cdot d_c}]_\lambda
     \;\geq\;
     0  
     \,;
   $$

1. zero is an eigenvalue for $N \lt n$ 

   $$
     N \leq n - 1
     \;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;
     \underset{\lambda \in Part(n)}{\exists}
     \,     
     EigVals[e^{- ln(N) \cdot d_c}]_\lambda
     \;=\;
     0   
     \,;
   $$

1. all eigenvalues are positive if $N \geq n$:

   $$
     N \geq n 
     \;\;\;\;\;\;\;
     \Rightarrow
     \;\;\;\;\;\;\;
     \underset{\lambda \in Part(n)}{\forall}
     \,     
     EigVals[e^{- ln(N) \cdot d_c}]_\lambda
     \;\gt\;
     0  
     \,.
   $$

\end{prop}

\begin{proof}
By (eq:EigenvaluesAtLogIntegerInverseTempeteratureCountingYoungTableaux) in
Prop. \ref{EigenvaluesAtLogIntegerInvTemViaYoungTabl} the eigenvalues at $\beta = ln(N)$ count possible numbers of colorings of Young diagrams to [[semistandard Young tableaux]] (ssYT). This gives the first statement.

Since in a ssYT the labels must strictly increase downwards, there is no possible ssYT-coloring if there are fewer labels than rows. This gives the second claim.

But conversely, since in an ssYT the labels may be constant horizontally, there is at least one coloring once there never are more rows than labels. This gives the last claim.
\end{proof}




\linebreak

We give further [[combinatorics|combinatorial]] expressions of the eigenvalues of the Cayley distance kernel, using the [[hook length formula]] and the [[hook-content formula]]:


\begin{prop}\label{EigenvaluesInTermsOfHookContent}
 **(Eigenvalues of Cayley distance kernel via [[hook-content formula]])**
 
  The eigenvalues (eq:CharacterFormulaForEigenvalueOfCayleyDistanceKernel)
  of the Cayley distance kernel for all $e^\beta \in \mathbb{R}_+$ may be expressed as:

$$
  EigVals[e^{- \beta \cdot d_C}]_\lambda
  \;=\;
  \frac
    {n!}
    {\chi^{(\lambda)}}
  e^{- \beta \cdot N}
  \underset
    {
      { 1 \leq i \leq rows(\lambda) }
      \atop
      { 1 \leq j \leq \lambda_i }
    }
    {\prod}
    \frac{
      e^{\beta}+ j - i
    }{
      \ell hook_\lambda(i,j)
    }
   \,.
$$
  
\end{prop}
The following proof was pointed out by [[Abdelmalek Abdesselam]].
\begin{proof}
  By Prop. \ref{EigenvaluesAtLogIntegerInvTemViaYoungTabl} the $\lambda$th eigenvalue at integer values 

$$
  e^{\beta} = N \in \mathbb{N}_+
$$ 

is a positive multiple of the number of semi-standard Young tableau, and hence is given by the *[[hook-content formula]]*, as follows:

$$
  \begin{aligned}
    \frac
      {  \chi^{(\lambda)}(e) }
      { n!  }
    N^n
    \cdot
    EigVals[e^{- ln(N)} \cdot d_C]_\lambda
    &
    \;=\;
    \left\vert ssYT_\lambda(N) \right\vert
    \\
    &
    \;=\;
    \underset{(i,j)}{\prod}
    \frac
      { N + content(i,j) }
      { \ell hook_\lambda(i,j)  }
  \end{aligned}
  \,,
  {\phantom{AAAA}}
  N \in \mathbb{N}_+
  \,.
$$

We may regard this set of equations as the specialization of the following more general equation

$$
  \frac
    {  \chi^{(\lambda)}(e) }
    { n!  }
  (e^\beta)^n
  \cdot
  EigVals[e^{- \beta} \cdot d_C]_\lambda
  \;=\;
  \underset{(i,j)}{\prod}
    \frac
      { e^\beta + content(i,j) }
      { \ell hook_\lambda(i,j) }
$$

to all integer values of $e^\beta$. But since both sides of this equation are [[polynomials]] in $e^\beta$ -- the right hand manifestly so, the left hand side by (eq:CharacterFormulaForEigenvalueOfCayleyDistanceKernel) -- the fact that the equation holds at infinite many distinct points $e^\beta \in \mathbb{N}_+$ implies that in fact it holds for all $e^\beta \in \mathbb{R}_+$.

\end{proof}

In fact:

\begin{prop}\label{EigenvaluesInTermsOfJustBoxContent}
**(Eigenvalues if Cayley distance kernel in terms of just box content)**
  \linebreak
  The Eigenvalues (eq:CharacterFormulaForEigenvalueOfCayleyDistanceKernel)
  of the Cayley distance kernel for all $e^\beta \in \mathbb{R}_+$ may be expressed as:

$$
  EigVals[e^{- \beta \cdot d_C}]_\lambda
  \;=\;
  e^{- \beta \cdot N}
  \underset
    {
      { 1 \leq i \leq rows(\lambda) }
      \atop
      { 1 \leq j \leq \lambda_i }
    }
    {\prod}
    \big(
      e^{\beta}+ j - i
    \big)
   \,.
$$
\end{prop}
This is essentially, the result of [Jucys 71](Jucys-Murphy+element#Jucys71), see at *[[Jucys-Murphy element]]*.
\begin{proof}

The point is that the [[hook length formula]] (see [here](hook+length+formula#eq:HookLengthFormulaMeasuresDimensionOfIrrepOfSymmetricGroup)) also gives the dimension of the [[irreps]] of the [[symmetric group]]:

\[
  \label{HookLengthFormulaForDimensionOfIrrepsOfSymmetricGroup}
  \chi^{(\lambda)}(e)
  \;=\;
  dim
  \big(
    S^{(\lambda)}
  \big)
  \;=\;
  \frac
    { n! }
    {
      \underset{(i,j)}{\prod}  \ell hook_\lambda(i,j)
    }
  \,.
\]

Using this, we compute as follows:

$$
  \begin{aligned}
  EigVals[e^{- \lambda \cdot d_C}]_\lambda
  & \;=\;
  \frac
    {n!}
    {\chi^{(\lambda)}}
  e^{- \beta \cdot N}
  \underset
    {
      { 1 \leq i \leq rows(\lambda) }
      \atop
      { 1 \leq j \leq \lambda_i }
    }
    {\prod}
    \frac{
      e^{\beta}+ j - i
    }{
      \ell hook_\lambda(i,j)
    }
  \\
  & \;=\;
  e^{- \beta \cdot N}
  n! 
    \frac
      { \underset{(i,j)}{\prod} \ell hook_\lambda(i,j) }
      {n!}
  \underset
    {
      (i,j)
    }
    {\prod}
    \frac{
      e^{\beta}+ j - i
    }{
      \ell hook_\lambda(i,j)
    }  
  \\
  & \;=\;
  e^{- \beta \cdot N}
  \underset
    {
      { 1 \leq i \leq rows(\lambda) }
      \atop
      { 1 \leq j \leq \lambda_i }
    }
    {\prod}
    \big(
      e^{\beta}+ j - i
    \big)
    \,.
  \end{aligned}
$$
Here the first line is Prop. \ref{EigenvaluesInTermsOfHookContent} and the second step inserts (eq:HookLengthFormulaForDimensionOfIrrepsOfSymmetricGroup).


\end{proof}














#### Dual basis
 {#DualBasis}

We make explicit the [[inner product]] with respect to which the Cayley distance kernel is a [[hermitian matrix]]:

\begin{defn}\label{CartesianInnerProduct}
**(Cartesian inner product)**

Let 

$$
  \array{
    \mathbb{C}[Sym(n)]
    \times
    \mathbb{C}[Sym(n)]
    &
    \overset{  
      \;\;\;\;\;\;
      \langle -,-\rangle
      \;\;\;\;\;\;
    }{
      \longrightarrow
    }
    &
    \mathbb{C}
    \\
    \Big(
      \big(
        v_1(\sigma)
      \big)_{\sigma \in Sym(n)},
      \;
      \big(
        v_2(\sigma')
      \big)_{\sigma' \in Sym(n)}
    \Big)
    &
      \mapsto
    &
    \underset{\sigma \in Sym(n)}{\sum}
      \bar 
      v_1(\sigma) 
      \cdot 
      v_2(\sigma)
  }
$$

denote the [[sesquilinear form]] induced by the canonical [[linear basis]] of the [[linear span]] $\mathbb{C}[Sym(n)]$.

\end{defn}

\begin{prop}\label{DualEigenvectorBasis}
**(dual eigenvector basis)**

With respect to the Cartesian inner product from Def. \ref{CartesianInnerProduct}, the eigenvectors (eq:EigenvectorsOfCayleyDistanceKernel) from Prop. \ref{CharacterFormulaForEigenvalues} have a [[dual basis]] given by

\[
  \label{TheDualEigenvectorBasis}
  \left\langle
   \lambda, (i, j)
  \right\vert
  \;\coloneqq\;
  \frac
  {
    \chi^{(\lambda)}(e)
  }
  {
    n!
  }
  EigVects[e^{- \beta \cdot d_C}]_\lambda
  \;=\;
  \frac
  {
    \chi^{(\lambda)}(e)
  }
  {
    n!
  }
  \big(
    \bar S^{(\lambda)}_{i j}(\sigma)
  \big)_{\sigma \in Sym(n)}
  \,.
\]
\end{prop}
Beware that the original eigenvector basis (eq:EigenvectorsOfCayleyDistanceKernel) already involves the [[complex conjugate]] $\bar S$ of component entries.

\begin{proof}
  This is a restatement of the [[Schur orthogonality relation]] for [[irreps]], here for the [[Specht modules]] $S^{(\lambda)}$:

  We compute as follows:
$$
  \begin{aligned}
    \big\langle
      \lambda_1, (i_1, j_1)
    \big\vert
      \lambda_2, (i_2, j_2)
    \big\rangle
    & 
    \;=\;
    \frac{ \chi^{(\lambda_1)}(e) }{ n! }
    \underset{\sigma \in Sym(n)}{\sum}
    S^{(\lambda_1)}(\sigma)_{j_1 i_1}
    \overline{
      S^{(\lambda_2)}(\sigma)_{i_2 j_2}
    }
    \\
    & \;=\;
    \delta^{\lambda_1 \lambda_2}
    \delta_{i_1 i_2} \delta_{j_1 j_2}
    \,.
  \end{aligned}
$$

Here the first step unwinds the definitions 
(using (eq:TheDualEigenvectorBasis) and (eq:EigenvectorsOfCayleyDistanceKernel) in Def. \ref{CartesianInnerProduct}), 
and the last step is the [[grand Schur orthogonality relation]] 
(eq:SchurOrthogonalityForIrreps).

\end{proof}


\linebreak


### Positivity
 {#Positivity}

We discuss at which values of the [[inverse temperature]] $\beta$, the Cayley distance kernel on $Sym(n)$ is, as a [[bilinear form]], indefinite or positive (semi-)definite.

#### Indefiniteness for $e^{\beta} \in (0,1) \cup (1,2) \cup \cdots \cup (n-2,n-1)$

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
  (0,1) \cup (1,2) \cup \cdots \cup (n-2, n-1)
  \,,
$$

or equivalently: 

For $0 \lt e^\beta \lt n-1$ the Cayley distance kernel is indefinite except possibly at [[integer]] values.
\end{prop}
\begin{proof}
With the third statement in Lemma \ref{SignOfTheEigenvalueOfTheSigantureDistribution} the claim follows for every *second* open unit [[interval]] between 0 and $n-1$. But by the same argument the analogous statement is then true on every *other* of these unit intervals for the kernel on $Sym(n-1)$.
Now since the kernel on $Sym(n-1)$ is a [[principal submatrix]] of that for $Sym(n)$ (see [this Prop.](Cayley+distance#CayleyDistancePreservedByInclusionOfSymmetricGroups)), the [[Cauchy interlace theorem]] implies that the kernel on $Sym(n)$ must have a negative eigenvalue as soon as that on $Sym(n-1)$ does.
\end{proof}


#### Semi-definiteness for $e^\beta \in \{1,2,\cdots, n-1\}$
 {#PositiveSemiDefinitenessAtLowNaturalNumbers}


\begin{lemma}\label{EigenvaluesNonNegativeAtNBetween1Andn}
  For $e^\beta = N \in \{1, 2, \cdots, n-1\}$
  all the eigenvalues of the Cayley distance kernel 
  $e^{- \beta \cdot d_C}$ on $Sym(n)$
  are non-negative
  and for $e^\beta = n$ they are all positive.
\end{lemma}
\begin{proof}
  We observe that the eigenvalues at these particular 
  values of $\beta$ appear, up to a positive multiple, as [[coefficients]] of [[monomials]] in [[Schur polynomials]], but all such coefficients are non-negative integers ([this Prop.](Schur+function#CoefficientsOfMonomialsAreNaturalNumbers)). 

  Concretely, for $\lambda$ any [[partition]] of $n$, with corresponding [[Schur polynomial]] $\s_\lambda$  and [[irreducible character|irreducible]] [[Specht module|Specht]] [[character of a linear representation|character]] $\chi^{(\lambda)}$, consider the following computation:

\[
  \label{ExpressingSchurPolynomialsInTermsOfKernelEigenvalues}
  \begin{aligned}
  s_{\lambda}
  \big(
    \underset{
      N \; args
    }{
      \underbrace{
        x, x, \cdots, x
      }
    }
    ,
    \underset{
      n - N \; args
    }{ 
      \underbrace{
        0, 0, \cdots, 0 
      }
    }
  \big)
  & \;=\;
  \frac{1}{n!}
  \underset{ \sigma \in Sym(n) }{\sum}
    \chi^{(\lambda)}(\sigma)
    \cdot
    \big(
      N x^{l_1} 
    \big)
    \big(
      N x^{l_2} 
    \big)
    \cdots
    \big(
      N x^{l_{\left\vert Cycles(\sigma)\right\vert}} 
    \big)
  \\
  & \;=\;
  \left(
    \frac{1}{n!}
    \underset{ \sigma \in Sym(n) }{\sum}
      \chi^{(\lambda)}(\sigma)
      \cdot
      N^{ \left\vert Cycles(\sigma) \right\vert }
  \right)
  \cdot
  x^n
  \\
  &
  \;=\;\;
  \underset{
    \in \, \mathbb{N}
  }{
  \underbrace{
  \left(
    \tfrac
      {\chi^{(\lambda)}(1)}
      {n!}
    e^{ln(N) \cdot n}
    \cdot
    EV_\lambda (e^{- ln(N) \cdot d_C})
  \right)
  }
  }
  \cdot
  x^n
  \end{aligned}
\]

Here we used:

1. the Frobenius formula for Schur functions ([this Prop.](Schur+function#FrobeniusFormula));

1. some evident re-arrangements;

1. the character formula for the eigenvalues ([this Prop](#CharacterFormulaForEigenvalues)).

This shows the first part of the statement. Finally, that the eigenvalues for $e^\beta = N$ are in fact positive follows since in this case all the arguments $x_i$ on the top left of (eq:ExpressingSchurPolynomialsInTermsOfKernelEigenvalues) are non-vanishing, so that none of the monomials contributing to $x^n$ vanishes.

\end{proof}


\begin{prop}\label{PositiveSemidefinitenessAtLowIntegerValuedOfEBeta}
  For $e^\beta = N \in \{1,2, \cdots, n-1\}$
  the Cayley distance kernel $e^{- \beta \cdot d_C}$
  is positive semi-definite.

  For $e^{\beta} = n$  it is positive definite.
\end{prop}
\begin{proof}
  By Lemma \ref{EigenvaluesNonNegativeAtNBetween1Andn} the
  eigenvalues at all these values are non-negative
  and positive for the special case $e^{\beta} = n$,
  while by Lemma \ref{SignOfTheEigenvalueOfTheSigantureDistribution} they do contain 0  away from this special case.
\end{proof}

Alternatively, this follows from Prop. \ref{PositivitiViaCountingOfYoungTableaux}.


#### Definiteness for $e^\beta \in \{n,  n+1 , n+2, \cdots \}$

\begin{prop}\label{PositiveDefiniteneddForIntegerValuesLargerequaln}
  The Cayley distance kernel on $Sym(n)$ is positive definite for all 
  $e^\beta \in \{n, n+1, n+2, \cdots\}$.
\end{prop}
\begin{proof}
  By Prop. \ref{PositiveSemidefinitenessAtLowIntegerValuedOfEBeta} the CD kernel on $Sym(n + k)$ is positive definite 
  at $e^\beta = n + k$, which holds for all $k \in \mathbb{N}$. But the CD kernel in question is a [[principal submatrix]] of this positive one (see [this Prop.](Cayley+distance#CayleyDistancePreservedByInclusionOfSymmetricGroups)), and hence cannot be less than positive itself, by the [[Cauchy interlace theorem]].
\end{proof}

Alternatively, this follows from the third clause of Prop. \ref{PositivitiViaCountingOfYoungTableaux}


#### Definiteness for $\e^\beta \gt n  $
 {#DefinitenessForEBetaGreaterThann}

\begin{prop}
  \label{CayleyDistanceKernelPositiveForEBetaGreaterThann}
  The Cayley distance kernel $e^{- \beta \cdot d_C}$ on $Sym(n)$ is positive definite for $e^\beta \gt n - 1$.
\end{prop}
\begin{proof}

With the $\lambda$th eigenvalue expressed 
either via Prop. \ref{EigenvaluesInTermsOfHookContent}
or Prop. \ref{EigenvaluesInTermsOfJustBoxContent},
it is manifest that
a sufficient condition for their positivity is clearly that 
$$
  e^\beta + content(i,j)
  \;\coloneqq\;
  e^{\beta} + j - i
  \;\gt\;
  0
$$

for all $(i,j)$ that appear in the product, hence that

$$
  e^{\beta} + 1 - i
  \;\gt\;
  0
$$

for all $i$ that appear. But the index $i$ labels the rows of [[Young diagrams]] of $n$ boxes, and hence the condition is that

$$
  e^{\beta} 
    \;\gt\; 
  \underset{
    {
      \lambda \in Part(n)
    }
    \atop
    {
      1 \leq i \leq rows(\lambda)
    }    
  }{max}
  (i - 1)
  \;=\;
  n - 1
  \,.
$$
\end{proof}


\linebreak

The following is an alternative proof of a much weaker lower bound, not relying on the [[hook-content formula]] from [[combinatorics]], but on the [[Gershgorin circle theorem]] from [[analysis]]:

\begin{prop}
  A sufficient condition for the Cayley distance kernel (Def. \ref{CayleyDistanceKernel}) on $Sym(n)$ to be [[positive definite bilinear form|positive definite]] is that its [[inverse temperature]] $\beta$ satisfies the following [[inequality]]:

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
  \;\lt\;
  2
  e^{\beta \cdot n }
  \,.
\]
\end{prop}
\begin{proof}
  By the [[Gershgorin circle theorem]] and using Prop. \ref{GershgorinRadiiOfCayleyDistanceKernel},
  all the [[eigenvalues]] of the kernel are within a distance $r(\beta)$ (eq:GershgorinRadiusExpression) from its diagonal values, which are all equal to $1 = e^{- \beta \cdot 0}$. 
Since, moreover, all eigenvalues are [[real numbers|real]], the condition
\[
  \label{GershgorinRadiusConditionForNonNegativeEigenvalues}
  \begin{aligned}
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
  &
  \;\;\lt\;\; 
  1
  \\
  \Leftrightarrow
  \;\;\;
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
  &
  \;\;\lt\;\; 
  2  
  \end{aligned}
\]
implies that all eigenvalues are contained in the [[interval]] $(0,2) \subset \mathbb{R}$ and hence in particular that they are [[positive number|positive]].
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
    \;\gt\;
  \frac{
    n-1
  }{
    q^{1/n} - 1
  }  
$$
for $q = 3$.
\end{prop}
\begin{proof}
First consider the case of $q =2$:

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
  \;\lt\;
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
  \;\lt\;
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
  \;\lt\;
  2   
  }
  \;\;\;\;\;\;
    \Rightarrow
  \;\;\;\;\;\;
  e^{- ln(N) \cdot d_C}
  \,
  \text{is positive definite on}
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
  \;\lt\;
  2
  \\
  \Leftrightarrow
  \;\;\;
  &
  N
    \;\gt\;
  \frac{
    n-1
  }{
    2^{1/n} - 1
  }
  \end{aligned}
$$

Now to improve this to $q =3$: Since we may assume that at least $N \gt n-1$, we know that the eigenvalues of the homogeneous distribution (Example \ref{HomogeneousDistributionIsEigenvalue}) and of the signature distribution (Prop. \ref{SignatureDistributionIsEigenvector}) are non-negative (by Lemma \ref{SignOfTheEigenvalueOfTheSigantureDistribution}). But by the character formula for [[Cayley graph spectra]] ([this Prop](Cayley+graph+spectrum#CharacterFormula)) these are precisely the two eigenvalues with unit multiplicity. Therefore a strengthening of the [[Gershgorin circle theorem]] applies to all the remaining eigenvalues, saying ([this Prop.](Gershgorin+circle+theorem#StrengtheningForNonNegativeMatrices)) that these are in fact within *half* the Gershgorin radius (eq:GershgorinRadiusExpression). This allows us to put a factor of 1/2 on the left hand side of the first row of  (eq:GershgorinRadiusConditionForNonNegativeEigenvalues), which amounts to replacing the "2" by a "3" on the right of the second row.
\end{proof}

\begin{remark}
  Computer-experiment suggests ([CSS21](#CSS21), [Bar-Natan 21](#BarNatan21)) that the above bounds (Prop. \ref{ExplicitBoundForInverseTemperatureEnsuringPositivity}) are rather loose: For the first few values of $N$, at least, the inverse temperature $\beta \geq ln(N-1)$ is already sufficient for positive semi-definiteness.
\end{remark}

\linebreak

### Cayley state on the group algebra
 {#CayleyStateOnTheGroupAlgebra}

> under construction

We observe that for $e^\beta \in \mathbb{R}_+$ integral or greater than $n-1$, the Cayley distance kernel $e^{- \beta \cdot d_C}$ defines a [[quantum state]] (in the sense of [[state on a star-algebra]]) 

$$
  \big\langle
    -
  \big\rangle_\beta
  \;\colon\;
  \mathbb{C}[Sym(n)]
    \longrightarrow
  \mathbb{C}
$$

on the [[group algebra]] canonically regarded as a [[star algebra]]. Then we exhibit it as a [[mixed state]] given by a [[probability distribution]] on [[pure states]] which are labeled by [[standard Young tableaux]].

> unpolished notes


#### The algebra

We regard the [[linear span]] $\mathbb{C}[Sym(n)]$ as equipped with the [[sesquilinear form]] given by

$$
  (a_1 \sigma_1, a_2 \sigma_2)
  \;\coloneqq\;
  \bar a_1 
  \,
   a_2
  \,
  \delta_{\sigma_1, \sigma_2}
  \,,
  \;\;\;\;\;
  for \; a_1, a_2 \in \mathbb{C}, \; \sigma_1, \sigma_2 \in Sym(n)
  \,.
$$

We regard any [[linear map|linear]] [[endomorphism]] $\phi$ on the [[linear span]] $\mathbb{C}[Sym(n)]$ as a [[matrix]] $[\phi]$ with respect to the canonical [[linear basis]] 

$$
  [\phi]_{\sigma_1, \sigma_2}
  \;\coloneqq\;
  \big(
    \sigma_1, \phi(\sigma_2)
  \big)
  \,.
$$

We denote [[matrix multiplication]] by "$\cdot$", so that 

$$
  [ \phi_2 \circ \phi_1 ]
  \;=\;
  [\phi_2]
  \cdot
  [\phi_1]
  \,.
$$

Next, with $\mathbb{C}[Sym(n)]$ regarded as the [[group algebra]],
we will write the algebra product as $\bullet$. 

This way, for $A_1, A_2 \in \mathbb{C}[Sym(n)]$ and with any element of the group algebra conflated with the endomorphism of left multiplication by this element, we have

$$
  [ A \bullet B]
  \;=\;
  [A] \cdot [B]
$$

Notice that in this notation 

$$
  A \;=\; A \bullet e \;=\; [A] \cdot e
  \,,
$$

reflecting that $e \in \mathbb{C}[Sym(n)]$ is a [[cyclic vector]].



Finally, we consider $\mathbb{C}[Sym(n)]$ as a complex [[star-algebra]] via

$$
  (a \, \sigma)^\ast \;=\; \bar a \, \sigma^{-1}
  \,.
$$

Noticing

$$
  \big(
    [A^\ast] \cdot [\sigma_1]
    ,\,
    [\sigma_2]
  \big)
  \;=\;
  a_{ \sigma_1 \sigma_2^{-1} }
  \;=\;
  \big(
    [\sigma_1]
    ,\,
    [A]\cdot [\sigma_2]
  \big)
$$

we see that 

$$
  [A]^\dagger \;=\; \big[ A^\ast \big]
$$

and so that 

$$  
  \mathbb{C}[Sym(n)] 
    \overset{ [-] }{\longrightarrow}
  Mat(n! \times n!, \mathbb{C})
$$

is a homomorphism of complex star-algebras.

\linebreak

#### The state
  {#TheCayleyState}

For 

$$
  e^\beta \in \{1,2, \cdots, n-1\} \cup \mathbb{R}_{\gt n-1}
$$ 

a [[state on a star-algebra|state]] on this algebra is given by sending any 

$$
  A \;=\; \underset{\sigma \in Sym(n)}{\sum} a_\sigma \sigma
$$ 

to

$$
  \big\langle
    A
  \big\rangle_{\beta}
  \;\coloneqq\;
  \big(
    e,
    [e^{-\beta \cdot d_C}] 
    \cdot 
    A
  \big)
  \;\coloneqq\;
  \underset{ 
    \sigma \in Sym(n) 
  }{\sum} 
  a_\sigma 
  \cdot
  e^{ -\beta \cdot d_C(e, \sigma ) }
  \;=\;
  e^{- \beta \cdot n}
  \underset{ 
    \sigma \in Sym(n) 
  }{\sum} 
  a_\sigma 
  \cdot
  e^{ \beta \cdot \# cycles(\sigma) }
  \,.
$$

This is indeed a state, because 

$$
  \begin{aligned}
  \big\langle
    A^\ast \bullet A
  \big\rangle_{\beta}
  & \;\coloneqq\;
  \Big(  
    e,
    \big[ e^{-\beta \cdot d_C} \big] 
      \cdot 
    (A^\ast \bullet A )
  \Big)
  \\
  &
  \;\coloneqq\;
  \underset{ 
    \sigma_1, \sigma_2 \in Sym(n) 
  }{\sum} 
  \bar a _{\sigma_1}
  a_{\sigma_2}
  \cdot
  e^{ -\beta \cdot d_C(e, \sigma_1^{-1} \sigma_2 ) }
  \\
  & \;=\;
  \underset{ 
    \sigma_1, \sigma_2 \in Sym(n) 
  }{\sum} 
  \bar a _{\sigma_1}
  a_{\sigma_2}
  \cdot
  e^{ -\beta \cdot d_C(\sigma_1,  \sigma_2 ) }
  \\
  & \;=\;
  \Big(
    A,
    \,
    [e^{- \beta \cdot d_C}] \cdot A
  \Big)
  \\
  & \;\geq \; 0 
  \end{aligned}
$$

by left-invariance and by positive (semi-)definity of the Cayley distance kernel at the given $\beta$.

\linebreak

#### Idempotent decomposition
 {#CayleyStatePrimitiveIdempotents}


Regarding $\mathbb{C}[Sym(n)]$ as the [[regular representation]] of $Sym(n)$ it [decomposes into irreps](regular+representation#RegularRepDecomposedIntoIrreps) ([[Specht modules]]) $S^{(\lambda)}$ with multiplicity their dimension.

For $\lambda \in Part(n)$ and $1 \leq i \leq dim\big( S^{(\lambda)}\big)$ write 

$$
  P^{(\lambda)}_i
  \;\colon\;
  \mathbb{C}[Sym(n)]
  \longrightarrow
  \mathbb{C}[Sym(n)]
$$

for the linear projection onto the linear span of

$$
  \left\{
    \underset{ \sigma \in Sym(n) }{\sum}
    \bar S^{(\lambda)}_{k i}(\sigma) \sigma
    \;\in\;
    \mathbb{C}[Sym(n)]
  \right\}
    _{ 1 \leq k \leq dim(S^{(\lambda)}) }
  \,.
$$


Thus

$$
  \underset{
    { \lambda \in Part(n) }
    \atop
    {1 \leq i_\lambda \leq dim(S^{(\lambda)})}
  }{ \sum }
  P^{(\lambda)}_{i_\lambda}
  \;=\;
  id
  \,.
$$

Notice that each $P^{(\lambda)}_{j_\lambda}\big( \mathbb{C}[Sym(n)]  \big)$ is a left ideal of the group algebra:


$$
  \begin{aligned}
  \sigma' 
    \;\bullet\;
  \left(
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  \bar S^{(\lambda)}(\sigma)_{i j}
  \,
  \sigma
  \right)
  & \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  \bar S^{(\lambda)}(\sigma)_{i j}  
  \,
  \sigma' \bullet \sigma
  \\
  & =
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  \bar S^{(\lambda)}( (\sigma')^{-1} \sigma)_{i j}  
  \,
  \sigma
  \\
  & \;=\;
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  \underset{ 1 \leq k \leq dim(S^{(\lambda)}) }{\sum}
  S^{(\lambda)}( \sigma' )_{i k}  
  \bar S^{(\lambda)}( \sigma)_{k j}  
  \,
  \sigma
  \\
  & \;=\;
  \underset{ 
    1 \leq k \leq dim(S^{(\lambda)}) 
  }{\sum}
  S^{(\lambda)}( \sigma' )_{i k}  
  \left(
  \underset{
    \sigma \in Sym(n)
  }{\sum}
  \bar S^{(\lambda)}( \sigma)_{k j}  
  \,
  \sigma
  \right)
  \end{aligned}
$$

Hence 

$$
  \mathbb{C}[Sym(n)]
  \;\simeq\;  
  \underset{
    { \lambda \in Part(n) }
    \atop
    {1 \leq i_\lambda \leq dim(S^{(\lambda)})}
  }{\oplus}
  P^{(\lambda)}_i\big( \mathbb{C}[Sym(n)]  \big)
$$

is a decomposition into left [[ideals]].

In fact, this is a decomposition into [[minimal ideals]]: 

The minimal left ideals of any complex [[group algebra]] $\mathbb{C}[G]$ are labeled by pairs consisting of an [[irrep]] $V \in Rep(G)$ and a left ideal in the linear [[endomorphism algebra]] $End_{\mathbb{C}}(V)$ (by [this Prop.](group+algebra#ComplexGroupAlgebraOfFiniteGroupAsDirectSumOfEndomorphismAlgebras)). The latter is isomorphic to a [[matrix algebra]] and hence its left minimal ideals are the $dim(V)$-many single-column matrixes. Therefore minimal ideals in $\mathbb{C}[G]$ are labeled by pairs consisting of an irrep and a postitive natural number no larger than the dimension of the irrep. This is the same number/cardinality of ideals we found above, hence they must already be minimal.

(It's also the same number of primitive idempotents as used in the discussion of [[Jucys-Murphy elements]], see [there](Jucys-Murphy+element#Projectors).)

\linebreak

This decomposition of the group algebra into left ideals implies that for all $A \in \mathbb{C}[Sym(n)]$ we have

$$
  [P^{(\lambda)}_{i_\lambda}] \cdot [A]
  \;=\;
  [A] \cdot [P^{(\lambda)}_{i_\lambda}]
$$

Moreover, we have 

$$
  [e^{- \beta \cdot d_C}] 
    \cdot 
  [P^{(\lambda)}_{i_\lambda}]
  \;=\;
  [P^{(\lambda)}_{i_\lambda}]
    \cdot
  [e^{- \beta \cdot d_C}] 
$$

by the fact that the $\underset{ \sigma }{ \sum } \bar S^{(\lambda)}(\sigma) \, \sigma $ are eigenvectors of the Cayley distance kernel.

Finally, we have

$$
  \left(  
    P^{(\lambda)}_{i_\lambda}( \bar S^{(\lambda_1)}_{i_1, j_1} ),
    \,
    \bar S^{(\lambda_2)}_{i_2, j_2} 
  \right)
  \;=\;
  \left(  
    \bar S^{(\lambda_1)}_{i_1, j_1},
    \,
    P^{(\lambda)}_{i_\lambda}
    (
    \bar S^{(\lambda_2)}_{i_2, j_2} 
    )
  \right)  
$$

hence 

$$
  [P^{(\lambda)}_{i_\lambda}]^\dagger = [P^{(\lambda)}_{i_\lambda}]
$$ 

(by grand Schur orthogonality, see [this Prop.](Cayley+distance+kernel#DualEigenvectorBasis)).


#### The mixture

Using the above properties of the projectors $[P^{(\lambda)}_{i_\lambda}]$, we observe that each

$$
  \big\langle
    -
  \big\rangle_{\beta, (\lambda, i_\lambda)}
  \;\coloneqq\;
  \frac{1}{ 
    \big\langle  P^{(\lambda)}_{i_\lambda}(e) \big\rangle_\beta
  }
  \,
  \big\langle 
    P^{(\lambda)}_{i_\lambda}(-)
  \big\rangle_\beta
$$

is still a [[state on a star-algebra|state]]:

$$
  \begin{aligned}
    \big\langle 
      P^{(\lambda)}_{i_\lambda}( A^\ast \bullet A)
    \big\rangle_\beta  
    & \;=\;
    \big(
      e
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot
      [P^{(\lambda)}_{i_\lambda}] 
        \cdot 
      [A]^\dagger 
        \cdot 
      [A]
      \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      e
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot
      [P^{(\lambda)}_{i_\lambda}] 
        \cdot
      [P^{(\lambda)}_{i_\lambda}] 
        \cdot 
      [A]^\dagger 
        \cdot 
      [A]
      \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      e
      ,\,
      [P^{(\lambda)}_{i_\lambda}] 
        \cdot
      [e^{- \beta \cdot d_C}]
        \cdot
      [A]^\dagger 
        \cdot 
      [P^{(\lambda)}_{i_\lambda}] 
        \cdot
      [A]
        \cdot
      e
    \big)
    \\
    & \;=\;
    \big(
      P^{(\lambda)}(A)
      ,\,
      [e^{- \beta \cdot d_C}]
        \cdot 
      P^{(\lambda)}_{i_\lambda}(A)
    \big)
    \\
    & \;\geq\; 0
  \end{aligned}
$$

It follows that we have decomposed our state into a [[convex combination]] of other states as follows:

\[
  \label{TheConvexCombination}
  \big\langle    
     -
  \big\rangle_\beta
  \;=\;
  \underset{ 
     { \lambda \in Part(n) }
     \atop
    {1 \leq i_\lambda \leq dim(S^{(\lambda)})}
  }{ \sum }
  p_{\lambda, i_\lambda}
  \cdot
  \big\langle    
     -
  \big\rangle_{\beta, (\lambda, i_\lambda)}
  \,,
\]

where

$$
  p_{\lambda, i_\lambda}
  \;\coloneqq\;
  \big\langle  P^{(\lambda)}_{i_\lambda}(e) \big\rangle_\beta
  \,.
$$



**Claim**. The $\langle  - \rangle_{\beta, (\lambda, i_\lambda)}$
are [[pure states]].

This must hold because the $P^{(\lambda)}_{i_\lambda}(\mathbb{C}[Sym(n)])$ are [[minimal ideals]], by the discussion [above](#CayleyStatePrimitiveIdempotents), whence the projectors $P^{(\lambda)}_{i_\lambda}$ are given by left multiplication with primitive idempotents in the group algebra. Under the [[GNS construction]], these correspond to projectors onto 1-dimensional subspaces, hence to [[pure states]].

\linebreak

But this means that (eq:TheConvexCombination) exhibits our state as a [[mixed state|mixture]] in which the $\lambda$th pure state appears with probability $p_{\lambda, i_\lambda}$.


#### The probability distribution
  {#TheCayleyStateProbabilityDistribution}

Now to express these probabilities more explicitly:

First observe the expansion of the neutral element in our eigenvector basis, evident from [[Schur orthogonality]]:

$$
  \begin{aligned}
  e
  & \;=\;
  \frac{1}{n!}
  \underset{\lambda, \sigma}{\sum} 
    \chi^{(\lambda)}(e)
    \chi^{\lambda}(\sigma) 
    \, \sigma
  \\
  & \;=\;
  \frac{1}{n!}
  \underset{\lambda, \sigma, i}{\sum} 
    \chi^{(\lambda)}(e)
    S^{\lambda}(\sigma)_{i i} 
    \, \sigma
  \end{aligned}
  \,.
$$

But this means that 

$$
  \big(   
     e, P^{(\lambda)}_i(e)
  \big)
  \;=\;
  \frac{1}{n!} 
  \chi^{(\lambda)}(e)
  S^{(\lambda)}(e)_{i i}
  \;=\; 
  \frac{\chi^{(\lambda)}(e)}{n!} 
$$

and so the probabilities are:

$$  
  p_{\lambda, i}
  \;=\;
  \big(   
     e, [e^{-\beta \cdot d_C}] \cdot P^{(\lambda)}_i(e)
  \big)
  \;=\;
  \frac{\chi^{(\lambda)}(e)}{n!} 
  EigVals[e^{- \beta \cdot d_C}]
  \,.
$$

As a sanity check, we have unit total probability:

$$
  \begin{aligned}
    \underset{\lambda, i}{\sum}
    p_{(\lambda,i)}  
    & \;=\;
    \underset{\lambda}{\sum}
    \frac{\big(\chi^{(\lambda)}(e)\big)^2}{n!} 
    EigVals[e^{- \beta \cdot d_C}]
    \\
    &
    \;=\; 
    \frac{1}{n!}
    \underset{
      \lambda \in Part(n)
    }{\sum}
    \big(
      \chi^{(\lambda)}(e)
    \big)^2
    \cdot
    \left(
       \frac{
         1
       }{
         \chi^{(\lambda)}(e)
       }
       \underset{\sigma \in Sym(n)}{\sum}
       e^{ \beta \cdot (\left\vert Cycles(\sigma) \right\vert - n  ) }
       \cdot
       \chi^{(\lambda)}(\sigma)
    \right)
    \\
    & \;=\;
    \frac{1}{n!}
    \underset{
      \sigma \in Sym(n)
    }{\sum}
    e^{ \beta \cdot (\left\vert Cycles(\sigma) \right\vert - n  ) }
    \underset{
      = \delta_{e,\sigma} n!
    }{
    \underbrace{
    \underset{
      \lambda \in Part(n)
    }{\sum}
    \chi^{(\lambda)}(e)
      \cdot
    \chi^{(\lambda)}(\sigma)
    }
    }
    \\
    & \;=\;
    1
  \end{aligned}
$$

In fact, by (eq:EigenvaluesAtLogIntegerInverseTempeteratureCountingYoungTableaux) in
Prop. \ref{EigenvaluesAtLogIntegerInvTemViaYoungTabl} this is the [[probability distribution]] on [[Young diagrams]] with $n$ boxes proportionate to their number of [[semistandard Young tableaux]] with labels bounded by $N$: 

\[
  \label{ProbabilitiesCountingSemistandardYoungTableaux}
  p^{Cay}_{\lambda, i}
  \;=\;
  \tfrac
    {\left\vert ssYT_{\lambda}(N)\right\vert}
    {N^n}
  \,.
\]

{#SchurWeylMeasure} If follows that the [[pushforward measure|pushforward]] of this probality distribution along the forgetful function

\[
  \label{ForgetfulFunctionFromstandardTableauxToYoungDiagrams}
  sYTableaux_n
  \overset{ q }{\longrightarrow}
  YDiagrams_n
\]

is 

$$
  q_\ast
  p
  \;:\;
  \lambda \;\mapsto\;
  \frac{
    \left\vert
      sYTableaux_\lambda
    \right\vert
    \cdot
    \left\vert
     ssYTableaux_\lambda(N)
    \right\vert
  }
  {N^n}
  \;=\;
  \frac{
    dim\big(S^{(\lambda)}\big)
    \cdot
    dim\big(V^{(\lambda)}\big)
  }
  {N^n}
  \,.
$$

This is the [[Schur-Weyl measure]].

Since the Cayley measure is constant on the [[fibers]] of $q$ (eq:ForgetfulFunctionFromstandardTableauxToYoungDiagrams) it is exactly that probability distribution on standard Yound tableaux which maximizes the entropy subject to the condition that the pushforward to Young diagrams is the [[Schur-Weyl measure]].




### Entropy of the Cayley state

Now to compute the [[von Neumann entropy]] of the Cayley state, hence the [[Shannon entropy]] of the [above](#TheCayleyStateProbabilityDistribution) probability distribution:

$$
  S
  \;\coloneqq\;
  \underset{\lambda, i}{\sum}
    p^{Cay}_{\lambda, i}
    \ln 
    \big(
      p^{Cay}_{\lambda, i}
    \big)
$$

as a function of $n$.

Recall the bounds

[[Hartley entropy]] $\geq$ [[Shannon entropy]] $\geq$ [[min-entropy]].

$$
  S_0 \;\geq\; S_1 \;geq\; S_\infty
  \,.
$$

#### Hartley entropy
 {#HartleyEntropyOfCayleyState}

Observe that a [[Young diagram]] ([[partition]]) $\lambda$ admits a decoration to at least one [[semi-standard Young tableau]] with labels bounded by $N$ if and only if it has at most $N$ rows.

Therefore the [[Hartley entropy]] of the probability distribution (eq:ProbabilitiesCountingSemistandardYoungTableaux) is the [[logarithm]] of the number of [[standard Young tableaux]] with $N$ boxes and at most $N$ rows: 

$$
  S_0
  \big(
    p^{Cay}
  \big)
  \;\;
    =
  \;\;
  sYT_n(N)
  \;\;
    \coloneqq
  \;\;
  ln
  \left(
  \underset
  {
    {
      \lambda \in Part(n)
    }
    \atop
    {
      rows(\lambda) \leq N
    }
  }{\sum}
  \underset{
    \chi^{(\lambda)}(e)
  }{
  \underbrace{
  \left\vert
     sYT_\lambda
  \right\vert
  }
  }
  \right)
  \,.
$$

For discussion of these numbers $\left\vert sYT_n(N) \right\vert$ see [there](semistandard+Young+tableau#NumberOfSYTWithBoundedNumberOfRows).

(...)


\linebreak


## Related concepts

* [[Mallows kernel]], [[Kendall kernel]], [[Markov kernel]]

* [[kernel method]]


## References

Mentioning of the Cayley distance kernel:

* [[Michael A. Fligner]], [[Joseph S. Verducci]], Section 4 of: *Distance Based Ranking Models*, Journal of the Royal Statistical Society. Series B (Methodological) Vol. 48, No. 3 (1986), pp. 359-369 ([jstor:2345433](https://www.jstor.org/stable/2345433))

* [[Persi Diaconis]], [[Phil Hanlon]], Section 4 of: *Eigen Analysis for Some Examples of the Metropolis Algorithm*, in Donald Richards (ed.) *Hypergeometric Functions on Domains of Positivity, Jack Polynomials, and Applications*, Contemporary Mathematics Vol. 138, AMS 1992 ([doi:10.1090/conm/138](http://dx.doi.org/10.1090/conm/138), [EFS NSF 392](https://statistics.stanford.edu/research/eigen-analysis-some-examples-metropolis-algorithm), [pdf](https://statweb.stanford.edu/~cgates/PERSI/papers/eigen-metalg.pdf))

* [[Michael A. Fligner]], [[Joseph S. Verducci]] (eds.), p. xx of: *Probability Models and Statistical Analyses for Ranking Data*, Lecture Notes in Statistics **80**, Springer 1993 ([doi:10.1007/978-1-4612-2738-0](https://link.springer.com/book/10.1007/978-1-4612-2738-0))

The above discussion of the positivity of the Cayley distance kernel in dependence of the inverse temperature follows:

* {#CSS21} [[David Corfield]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:Fundamental weight systems are quantum states]]* ([arXiv:2105.02871](https://arxiv.org/abs/2105.02871))

Further computations in:

* {#BarNatan21} [[Dror Bar-Natan]], *[AcademicPensieve](http://drorbn.net/AcademicPensieve/)* [2021-05](http://drorbn.net/AcademicPensieve/2021-05/), *The Cayley distance kernel following arXiv://2105.0287 by Corfield, Sati, and Schreiber* ([nb](http://drorbn.net/AcademicPensieve/2021-05/CayleyDistanceKernel.nb), [pdf](http://drorbn.net/AcademicPensieve/2021-05/nb/CayleyDistanceKernel.pdf), [[BarNatanCayleyDistanceKernelnb.pdf:file]])

Related discussion in:

* {#ABS22} Iskander Azangulov, Viacheslav Borovitskiy, Andrei *Smolensky On power sum kernels on symmetric groups* &lbrack;[arXiv:2211.05650](https://arxiv.org/abs/2211.05650)&rbrack;


Supplementary references:


* {#Kaski02} [[Petteri Kaski]], *Eigenvectors and spectra of Cayley graphs*, 2002 ([pdf](http://www.tcs.hut.fi/Studies/T-79.300/2002S/esitelmat/kaski_paper_020506.pdf), [[KaskiSpectraOfCayleyGraphs.pdf:file]])

* {#Stanley11} [[Richard Stanley]], *[Enumerative combinatorics](http://www-math.mit.edu/~rstan/ec/)* -- [Volume 1](http://www-math.mit.edu/~rstan/ec/ec1/), Wadsworth & Brooks/Cole Mathematics Series book series 1986, 1997 ([doi:10.1007/978-1-4615-9763-6](https://link.springer.com/book/10.1007/978-1-4615-9763-6)) reprinted in: Cambridge Studies in Advanced Mathematics, Cambridge University Press 2011 ([ISBN:9781107602625](https://www.cambridge.org/us/academic/subjects/mathematics/discrete-mathematics-information-theory-and-coding/enumerative-combinatorics-volume-1-2nd-edition?format=PB&isbn=9781107602625), [pdf](http://www-math.mit.edu/~rstan/ec/ec1.pdf))

* {#GnedinGorinKerov11} [[Alexander Gnedin]], [[Vadim Gorin]], [[Sergei Kerov]], *Block characters of the symmetric groups*, Journal of Algebraic Combinatorics, 38, no. 1 (2013), 79-101 ([arXiv:1108.5044](https://arxiv.org/abs/1108.5044), [doi:10.1007/s10801-012-0394-9](https://doi.org/10.1007/s10801-012-0394-9))

[[!redirects Cayley distance kernels]]
