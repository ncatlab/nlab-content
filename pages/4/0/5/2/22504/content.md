
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
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

In [[combinatorics]] a *(semi-)standard Young tableau* is a labelling of the boxes of a [[Young diagram]] with [[positive number|positive]] [[natural numbers]] (a [[Young tableau]]) satisfying extra conditions, at the *minimum* that labels do not decrease to the right and do increase downwards.

The number of (semi-)standard Young tableau of given shape (underlying [[Young diagram]]) govern various objects in the [[representation theory]] [[representation theory of the symmetric group|of the symmetric-]] [[representation theory of the general linear group|and general linear group]].

## Definition

\begin{definition}\label{YoungDiagram}
**([[Young diagram]])** \linebreak
For $n \in \mathbb{N}$ a [[positive number|positive]] [[natural number]],  a *[[Young diagram]] with $n$ boxes* is a [[partition]] of $n$, hence a sequence of weakly decreasing [[positive number|positive]] [[natural numbers]]

$$
  (\lambda_1 \geq \lambda_2 \geq \cdots \geq \lambda_{rows(\lambda)} )
  \,,
  \;\;
  \lambda_i \in \mathbb{N}_+
$$

whose [[sum]] is $n$:

\[
  \label{NumberOfBoxes}
  n \;=\;  \underset{i}{\sum} \lambda_i
  \,,
\]

\end{definition}


\begin{definition}\label{SemistandardYoungTableau}
**([[semistandard Young tableau]])** \linebreak

Given a [[Young diagram]]/[[partition]] $\lambda$ (Def. \ref{YoungDiagram}),
a *semistandard Young tableau* $T$ *of shape* $\lambda$ 

* is an [[indexed set]] of [[positive number|positive]] [[natural numbers]] of the following form (a *[[Young tableau]]*):

  \[
    \big(
      T_{i, j}
      \in
      \mathbb{N}_+
    \big)_{ 
      {1 \leq i \leq rows(\lambda)} \atop { 1 \leq j \leq \lambda_i } 
    }
    \,;
  \]

* such that these labels are:

  1. weakly increasing to the right/along rows;

     \[
       \label{RowsAreWeaklyIncreasing}
       \underset{
         i
       }{\forall} 
       \;\;\;\;\;\;
         j_1 \lt j_2 \;\Rightarrow\; T_{i, j_1} \leq T_{i, j_2} 
     \]

  1. strictly increasing downwards/along columns:

     \[
       \label{ColumnsAreStrictlyIncreasing}
       \underset{ j }{\forall}
       \;\;\;\;\;\;
       i_1 \lt i_2 \;\Rightarrow\; T_{i_1, j} \lt T_{i_2,  j} 
     \]

\end{definition}

\begin{remark}
Beware that in a semistandard Young tableau (Def. \ref{SemistandardYoungTableau}):

* the label $T_{1,  1}$ in the top left box is *not required* to be 1; 

* in *some* applications (e.g. (eq:RelationToSchurPolynomialsOfFinitelyManyVariables) below), though not in general, the labels are in addition required to be bounded $T_{i, j} \leq k$.

\end{remark}

\begin{definition}\label{StandardYoungTableau}
**([[standard Young tableau]])** \linebreak
A [[semistandard Young tableau]] (Def. \ref{SemistandardYoungTableau}) is called a [[standard Young tableau]] if, in addition to (eq:RowsAreWeaklyIncreasing) and (eq:ColumnsAreStrictlyIncreasing), it satisfies the following equivalent conditions:

* every element of $\big\{1, \cdots, n\}$ appears exactly once;

* the following two conditions hold:

  1. not just the columns but also the rows are strictly increasing,

  1. the last label is $T_{rows(\lambda), \lambda_{rows(\lambda)}} = n$ (eq:NumberOfBoxes)

(Which implies that the first label of a standard Young tableau must be $T_{1,1} = 1$.)

\end{definition}



## Examples

The following is a semistandard Young tableau that does happen to start with 1 but is not a standard Young tableau:

$$
\array{
  1 & 1 & 1 & 3
  \\
  2 & 3
  \\
  4
}
$$

## Properties

Given a [[partition]] $\lambda \in Part(n)$, we write

\[
  \label{SetOfssYTOfFixedShape}
  ssYT_\lambda
  \;in\;
  Set
\]

for the [[set]] of semistandard Young tableaux (Def. \ref{SemistandardYoungTableau}) whose underlying [[Young diagram]] (i.e. forgetting its labels) is given by $\lambda$.

Given moreover a [[natural number]] $N \in \mathbb{N}$ we write

\[
  \label{SetOfssYTOfFixedShapeWithBoundedLabels}
  ssYT_\lambda(N)
  \;\subset\;
  ssYT_\lambda
\]

for the subset on those semistandard Young tableau $T$ whose labels are bounded by $N$ in that $\underset{i,j}{\forall}\; T_{i, j } \;\leq\; N$.


### Relation to Schur polynomials
 {#RelationToSchurPolynomials}

Given a [[semistandard Young tableau]] $T$, we write $X^T$ for the [[monomial]] which contains one factor of the [[variable]] $x_k$ for each occurrence of $k$ in the Young tableau: 

\[
  \label{MonomialAssociatedWithSemistandardYoungTableau}
  x^T
  \;\coloneqq\;
  x_1^{\#1s}
  x_1^{\#2s}
  \cdots
  \,.
\]


\begin{prop}
  For $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, the corresponding [[Schur polynomial]] $s_\lambda$ is equal to the [[sum]] over the [[monomials]] (eq:MonomialAssociatedWithSemistandardYoungTableau) associated with all [[semistandard Young tableau]] of shape $\lambda$ (eq:SetOfssYTOfFixedShape):

$$
  s_\lambda(x_1, x_2, \cdots)
  \;\;=\;\;
  \underset{
    {T \in ssYT_\lambda},
  }{\sum}
  x^T
  \,.
$$
\end{prop}

([Sagan 01, Def. 4.4.1](#Sagan01), review in [Sagan Enc., p. 1](#SaganEnc))

This means that Schur polynomials in a [[finite set]] $\{x_1, \cdots, x_N\}$ of [[variables]] count semistandard Young tableau (of fixed shape and) with bounded labels (eq:SetOfssYTOfFixedShapeWithBoundedLabels):

\[
  \label{RelationToSchurPolynomialsOfFinitelyManyVariables}
  s_\lambda(x_1, \cdots, x_N)
  \;\;=\;\;
  \underset{
    {T \in ssYT_\lambda(N)},
  }{\sum}
  x^T
  \,.
\]



### Hook-length formula

See at *[[hook length formula]]*.

### Hook-content formula
 {#HookContentFormula}

The *[[hook-content formula]]* expresses the number of semistandard Young-Tableau $T$ with

1. shape $\lambda = (\lambda_1 \geq \cdots \geq \lambda_i)$ (a [[partition]]),

1. labels in $\{1, \cdots, N\}$,

1. sum of labels $\sum_{i,j} T_{i,j}$ 

through the following identification of the *generating function* for numbers of semistandard Young tableaux (ssYT) as a [[polynomial]] in a [[variable]] $q$:

$$
  \underset{
    T \in ssYT_\lambda(N)
  }{\sum}
  q^{ \sum_{i,j} T_{i,j} }
  \;\;=\;\;
  q^{ \sum_i i \cdot \lambda_i }
  \underset{
    { i \in \{1, \cdots, rows(\lambda)\} }
    \atop
    {j \in \{1, \cdots, \lambda_j\}}
  }{\prod}
  \frac{
    1 - q^{N + content(i,j)}
  }{
    1 - q^{\ell hook(i,j)}
  }
  \,,
$$

where 

$$
  content(i,j) \;\coloneqq\; j - 1
  \,,
  {\phantom{AAAA}}
  \ell hook(i,j) 
  \;=\;
  \text{length of hook at (i,j)th box}
  \,.
$$

See at *[[hook-content formula]]* for more.

### Relation to dimensions of irreps


[[!include hook length and content formulas -- table]]

### Number of sYT with bounded number of rows
  {#NumberOfSYTWithBoundedNumberOfRows}

We discuss formulas for the number 

$$
  \left\vert
    sYT_n(N)
  \right\vert
  \;=\;
  \underset{
    { \lambda \in Part(n) }
    \atop
    { rows(\lambda) \leq N }
  }{
    \sum
  }
  \left\vert
     sYT_n
  \right\vert
$$

of standard Young tableaux with $n$ boxes and $\leq N$ rows.

#### Asymptotic formulas for large $n$

{#AsymptoticFormulaForNumberOfSYTWIthBoundedHeight} Asymptotically for large $n$ this is ([Regev 81, (F.4.5.1)](#Regev81)):

\[
 \label{AsymoptoticsOfSYTOfBoundedHeightRegevForm}
  \begin{aligned}
  \left\vert
    sYT_n(N)
  \right\vert  
  &
  \;
  \overset{
    n \to \infty
  }{\sim}
  \;
  \left(
    \frac{N}{n}
  \right)^{ \tfrac{1}{4} N(N-1) }
  \cdot
  \frac
    {N^n}
    {N!}
  \cdot
  \big( 
    \underset{
       \sqrt{\pi}/2
    }{
    \underbrace{
      \Gamma(3/2)
    }
    }
  \big)^{- N}
  \cdot
  \underoverset
    {j=1}
    {N}
    {\prod}
    \Gamma
    \left(
      1 + \tfrac{1}{2}j
    \right)
  \end{aligned}
\]

Later this appears again as a conjecture in [Kotěšovec 13](#Kotesovec13):

\[
 \label{AsymoptoticsOfSYTOfBoundedHeightKotesovecForm}
  \begin{aligned}
  \left\vert
    sYT_n(N)
  \right\vert  
  &
  \;\sim\;
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \underset{
    \Gamma(1 + j/2) \tfrac{2}{j}
  }{
  \underbrace{
    \Gamma(j/2)
  }
  }
  \cdot
  \frac{N^n}{\pi^{N/2}}
  \cdot
  \left( 
    \frac{N}{n}
  \right)^{ \tfrac{1}{4}(N(N-1)) }  
  \\
  & \;=\;
  \underoverset
    {j = 1}
    {N}
    {\prod}
  \Gamma
  \big(
    1 + j/2
  \big)
  \cdot
  \frac{2^N}{N!}
  \cdot
  \frac{N^n}{\pi^{N/2}}
  \cdot
  \left( 
    \frac{N}{n}
  \right)^{ \tfrac{1}{4}(N(N-1)) }  
  \,.
  \end{aligned}
\]

(The first line is the expression conjectured in [Kotěšovec 13](#Kotesovec13), under the brace we use the [translation formula](Gamma+function#eq:TranslationFormula), and the second line shows agreement with [Regev 81 (F.4.5.1)](#Regev81) as in (eq:AsymoptoticsOfSYTOfBoundedHeightRegevForm).)

This may further be re-expressed ([Kotěšovec 13, p. 2](#Kotesovec13)) in terms of the [[Barnes G-function]] $G(-)$ (see [there](Barnes+G-function#MultiplicationFormulaForGammaFunctionInTermsOfGFunction)):

\[
  \label{AsymoptoticsOfSYTOfBoundedHeightInTermsOfBarnesGFunction}
  \begin{aligned}
  \left\vert
    sYT_n(N)
  \right\vert  
  &
  \;\underset{n \to \infty}{\sim}\;
  \underset{
  \mathclap{
    \frac
      {
        G(N/2 + 1)
        \cdot
        G(N/2 + 1/2)
      }
      {
        G(1/2)
      }
  }
  }{
    \underbrace{
    \underoverset
      {j = 1}
      {N}
      {\prod}
    \Gamma(j/2)
    }
  }
  \cdot
  \frac{N^n}{\pi^{N/2}}
  \cdot
  \left( 
    \frac{N}{n}
  \right)^{ \tfrac{1}{4}(N(N-1)) }  
  \end{aligned}
\]


#### Asymptotic formulas for large $n$ and large $N$

Using the large-$N$ asymptotic expansion ([here](Barnes+G-function#AsymptoticExpansion)) of the [[Barnes G-function]] 

$$
  G(N/2 + 1)
  \underset{N \to \infty}{\sim}
  \exp
  \left(
    \tfrac{1}{8}
    N^2 ln (N)
    -
    \left(
      \tfrac{3}{16}
      +
      \tfrac{ln(2)}{8}
    \right)
    N^2
    + 
    \tfrac{ln(2\pi)}{4} N
    -
    \tfrac{1}{12} ln(N)
    +
    \big(
      \zeta^'(-1)      
      -
      \tfrac{ln(2)}{12}
    \big)
  \right)
$$

inside the large-$n$ asymptotic expansion (eq:AsymoptoticsOfSYTOfBoundedHeightInTermsOfBarnesGFunction), we obtain the doubly asymptotic expansion of the number of standard Yound tableaux with $n$ boxes and $\leq N$ rows:

\[
  \label{DoublyAsymoptoticsOfSYTOfBoundedHeight}
  \begin{aligned}
  & 
  ln
  \big(
  \left\vert
    sYT_n(N)
  \right\vert  
  \big)
  \\
  &
  \;
  \underset{
    { n \to \infty } 
    \atop
    { N \to \infty }
  }{\sim}\;
   n ln(N)
   -
   \tfrac{1}{4}N^2 ln(n)
   +
   \tfrac{1}{4}N ln(n)
   \\
   &
    \phantom{
      \underset{
        { n \to \infty } 
        \atop
        { N \to \infty }
      }{\sim}\;
    }
   +
   \tfrac{1}{2}
    N^2 ln(N)
   -
    \left(
      \tfrac{3}{8}
      +
      \tfrac{ln(2)}{4}
    \right)
    N^2
   - 
   \tfrac{1}{4} N ln(N)
   + 
    \tfrac{ln(2)}{2} 
    N
    -
    \tfrac{1}{6} ln(N)
    \\
    & 
    \;
    \phantom{
      \underset{
        { n \to \infty } 
        \atop
        { N \to \infty }
      }{\sim}\;
    }
    +
    \big(
      2 \zeta^'(-1)      
      -
      \tfrac{ln(2)}{6}
      -
      ln G(1/2)
    \big)
  \end{aligned}
\]



#### Exact formulas for small $N$

Exact formulas for small $N$:

$$
  \left\vert
    sYT_{2n}(2)
  \right\vert
  \;=\;
  \frac{
    (2n)!
  }{
    (n!)^2
  }
  \,,
  \;\;\;\;\;\;
  \left\vert
    sYT_{2n+1}(2)
  \right\vert
  \;=\;
  \frac{
    (2n + 1)!
  }{
    n! (n+1)!
  }
$$

$$
  \left\vert
    sYT_{n}(3)
  \right\vert
  \;=\;
  \underoverset
    {i = 0}
    { \rfloor n/2 \lfloor }
    {\sum}
    \left( 
      n \atop {2i}
    \right)
    Catalan(i)
  \;=\;
   Motzkin(n)
  \,,
$$

where 

* $Catalan(k) \;=\; \frac{(2k)!}{k! (k+1)!}$ are the [[Catalan numbers]];

* $Motzkin(-)$ are the [[Motzkin numbers]].

This is attributed in [Gouyou-Beauchamps 89](#Gouyou-Beauchamps89) to [Regev 81](#Regev81).


For $N = 4,5$: 

$$
  \left\vert
    sYT_{2n-1}(4)
  \right\vert
  \;=\;
  Catalan(n) Catalan(n)
  \,,
  \;\;\;\;\;\;
  \left\vert
    sYT_{2n}(4)
  \right\vert
  \;=\;
  Catalan(n) Catalan(n+1)
$$

due to [Gouyou-Beauchamps 89](#Gouyou-Beauchamps89).



## References

### General

Textbook account:

* {#Sagan01} [[Bruce Sagan]], Def. 2.9.5 of: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

Survey in the context of [[Schur functions]]:

* {#SaganEnc} [[Bruce E. Sagan]], _Schur functions_, in: [[Michiel Hazewinkel]] (ed.), *[[eom|Encyclopaedia of Mathematics]]*, Springer 2002 ([pdf](http://www.mth.msu.edu/~sagan/Papers/Old/schur.pdf), [[SaganSchurFunctions.pdf:file]])

Specifically for standard Young tableaux:

* [[Ron M. Adin]], [[Yuval Roichman]], *Enumeration of Standard Young Tableaux*, Chapter 14 in: Miklós Bóna, *Handbook of Enumerative Combinatorics*, CRC Press 2015  ([arXiv:1408.4497](https://arxiv.org/abs/1408.4497), [ISBN:9781482220858](https://www.routledge.com/Handbook-of-Enumerative-Combinatorics/Bona/p/book/9781482220858))


See also the references at *[[Young tableau]]*.


### Counting for bounded number of rows

* {#Regev81} [[Amitai Regev]], *Asymptotic values for degrees associated with strips of young diagrams*, Advances in Mathematics Volume 41, Issue 2, August 1981, Pages 115-136 (<a href="https://doi.org/10.1016/0001-8708(81)90012-8">doi:10.1016/0001-8708(81)90012-8</a>)

* {#Gouyou-Beauchamps89} [[Dominique Gouyou-Beauchamps]], *Standard Young Tableaux of Height 4 and  5*, Europ. J. Combinatorics (1989) 10, 69-82 (<a href="https://doi.org/10.1016/S0195-6698(89)80034-4">doi:10.1016/S0195-6698(89)80034-4</a>, [pdf](https://core.ac.uk/download/pdf/82423471.pdf))

* Marilena Barnabei, Flavio Bonetti, and Matteo Silimbani: *Combinatorial properties of the numbers oftableaux of bounded height* ([arXiv:0803.2112](https://arxiv.org/abs/0803.2112), [pdf](http://amsacta.unibo.it/2443/1/bounded_height.pdf))

* {#Kotesovec13} Václav Kotěšovec, *Asymptotic of Young tableaux of bounded height*, 2013 ([pdf](http://www.kotesovec.cz/math_articles/kotesovec_young_tableaux_conjecture.pdf), [[KotesovecAsymptoticsOfBoundedYoungTableaux.pdf:file]])


[[!redirects semistandard Young tableaux]]

[[!redirects semi-standard Young tableau]]
[[!redirects semi-standard Young tableaux]]

[[!redirects semi standard Young tableau]]
[[!redirects semi standard Young tableaux]]

[[!redirects standard Young tableau]]
[[!redirects standard Young tableaux]]

