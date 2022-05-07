
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

The *Schur polynomials* $s_\lambda$, are [[polynomials]] in $n$ [[variables]] indexed by [[partitions]] $\lambda = \lambda_1 \geq \lambda_2 \geq \ldots \geq \lambda_n$ of $n$, which constitute a [[linear basis]] of the [[ring]] of [[symmetric polynomials]] in $n$ variables

## Definition

Given the [[partition]] $\lambda_1\geq \lambda_2\geq \ldots \geq \lambda_n$, the corresponding __Schur polynomial__ is defined as follows. First define the $n\times n$-[[determinant]] (for any partition $\alpha$ in $n$ parts)

$$
  a_\alpha \;\coloneqq\; det\big(x_i^{\alpha_j}\big).
$$

Let $\delta=(n-1, n-2, \dots, 1, 0)$. Then the Schur polynomial attached to $\lambda$ is the quotient

$$
  s_{\lambda}(x_1,x_2,\dots,x_n)
  =
  a_{\lambda+\delta}/a_{\delta}.
$$

As is usual in the theory of [[symmetric functions]] one can also deal with [[formal power series]] in infinitely many variables. To make this precise one uses an [[inverse limit]] (see [Macdonald 95](#Macdonald95)) and obtains a __Schur function__ $s_{\lambda}$ for each partition, depending on countably many variables $x_1, x_2,\dots,x_n,x_{n+1}, \dots$.

## Properties


### In terms of semistandard Young tableaux
 {#InTermsOfSemistandardYoungTableaux}

A *[[semistandard Young tableau]]* is a [[Young tableaux]] such that its values are:

1. weakly increasing to the right (along rows),

1. strictly increasing downwards (along columns).

For example:

$$
\array{
  1 & 1 & 1 & 3
  \\
  2 & 3
  \\
  4
}
$$

Given a [[semistandard Young tableau]] $T$, we write $X^T$ for  the [[monomial]] which contains one factor of the [[variable]] $x_k$ for each occurrence of $k$ in the Young tableau: 

\[
  \label{MonomialAssociatedWithSemistandardYoungTableau}
  x^T
  \;\coloneqq\;
  x_1^{\#1s}
  x_1^{\#2s}
  \cdots
  \,.
\]

We write 

\[
  \label{SetOfSemistandardYoungTableaux}
  ssYT_\lambda \;\supset\; ssYY_\lambda(N)
\]

for the set of semistandard Young tableaux whose underlying [[partition]] (i.e. forgetting its labels) is $\lambda$, and, respectively, for its [[subset]] on those whose labels are bounded as $T_{i,j} \leq N$.

\begin{prop}
  For $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, the corresponding Schur polynomial $s_\lambda$ is equal to the [[sum]] over the [[monomials]] (eq:MonomialAssociatedWithSemistandardYoungTableau) associated with all [[semistandard Young tableaux]] (eq:SetOfSemistandardYoungTableaux) of shape $\lambda$:

\[
  s_\lambda
  \;\;=\;\;
  \underset{
    {T \in ssYT(\lambda)},
  }{\sum}
  x^T
  \,.
\]
\end{prop}

([Sagan 01, Def. 4.4.1](#Sagan01), review in [Sagan Enc., p. 1](#SaganEnc))

This means that the Schur polynomial $s_\lambda$ in $N$ variables is the sum over semistandard Young tableaux (eq:SetOfSemistandardYoungTableaux) of shape $\lambda$ and with labels bounded as $T_{i,j} \leq N$:

\[
  \label{SchurPolynomialWithFiniteNumberOfvariablesAsSumOverssYT}
  s_\lambda
  \big(
    x_1, \cdots, x_N
  \big)
  \;\;=\;\;
  \underset{
    {T \in ssYT_\lambda(N)},
  }{\sum}
  x^T
  \,.
\]

In particular, the evaluation of a Schur polynomial at $N$ unit values is the number of [[semistandard Young tableaux]] with labels $\leq N$:

\[
  \label{SchurPolynomialCountsNumberOfSemiStandardYoungTableaux}
  s_\lambda
  \big(
    x_1\!=\!1, \cdots, x_N \!=\! 1
  \big)
  \;\;=\;\;
  \underset{
    {T \in ssYT_\lambda(N)},
  }{\sum}
  1
  \;\;=\;\;
  \left\vert
    ssYT_\lambda(N)
  \right\vert
  \,.
\]


An immediate consequence is:

\begin{prop}\label{CoefficientsOfMonomialsAreNaturalNumbers}
  The [[coefficient]] of any [[monomial]] $x_1^{n_1} x_2^{n_2} \cdots$ appearing in a Schur polynomial is non-negative.
\end{prop}



### In terms of $Sym(n)$-Characters
 {#InTermsOfSymnCharacters}

We discuss an expression of the Schur polynomials as [[symmetric polynomials]] with [[coefficients]] in the [[character of a linear representation|character]]-values of the symmetric group; this is Frobenius' formula in Prop. \ref{FrobeniusFormula} below.


First to set up some notation:

For the present purpose, a *[[partition]]* of a [[natural number]] $n \in \mathbb{N}$ is a weakly decreasing sequence

$$
  \lambda = (\lambda_1 \geq \lambda_2 \geq \cdots \geq \lambda_k)
$$

of [[natural numbers]] whose [[sum]] equals $n$:

$$
  \lambda_1 + \lambda_2 + \cdots + \lambda_k \;=\; n
  \,.
$$

By the [[representation theory of the symmetric group]], such partitions label its [[irreducible representations]] in the form of [[Specht modules]] $Specht^{(\lambda)}$. We write

\[
  \label{SpechtCharacter}
  \chi^{(\lambda)}(-)
  \;\coloneqq\;
  Tr_{Specht^{(\lambda)}}(-)
\]

for the [[irreducible character|irreducible]] [[character of a linear representation|character]] corresponding to this [[Specht module]].

We write

$$
  \array{
    Sym(n)
    &
      \overset{CycLengths}{\longrightarrow}
    &
    Part(n)
    \\
    \big\downarrow & \nearrow_{\mathrlap{\simeq}}
    \\
    Sym(n)/_{ad}Sym(n)
  }
$$

for the function that sends a [[permutation]] $\sigma$ of $n$ elements to the [[partition]] 

\[
  \label{CycleLengths}
  CycLengths(\sigma)
  \;=\;
  (l_1 \geq l_2 \geq \cdots \geq l_{\left\vert Cycles(\sigma)\right\vert})
\] 

of $n$ given by the lengths of its [[permutation cycles]] ([this Prop.](symmetric+group#ConjugacycClassesOfSymmetricGroupCorrespondToCycleSet)).

Given any such [[partition]] $(l_1 \geq l_2 \geq \cdots \geq l_k)$, we consider the following [[symmetric polynomial]] in $n$ [[variables]]:

\[
  \label{SymmetricFunctionIndecedByPartition}
  p_{
    (l_1 \geq l_2 \geq \cdots \geq l_k)
  }
  (x_1, x_2, \cdots, x_n)
  \;\;\;\coloneqq\;\;\;
  \big(
    x_1^{l_1} + \cdots + x_n^{l_1}
  \big)
  \cdot
  \big(
    x_1^{l_2} + \cdots + x_n^{l_2}
  \big)
  \cdots
  \big(
    x_1^{l_k} + \cdots + x_n^{l_k}
  \big)
  \,.
\]



\begin{prop}\label{FrobeniusFormula}
**(Frobenius formula)**

For $n \in \mathbb{N}$ and $\lambda$ a [[partition]] of $n$, the Schur polynomial $s_\lambda$ is equal to the [[sum]] over [[permutations]] $\sigma$ of the character values $\chi^{(\lambda)}$ (eq:SpechtCharacter) at $\sigma$ times the [[symmetric polynomial]] (eq:SymmetricFunctionIndecedByPartition) which is indexed by the cycle lengths (eq:CycleLengths) of $\sigma$:

$$
  s_\lambda
   \;=\;
  \frac{1}{n!}
  \underset
    {\sigma \in Sym(n)}
    {\sum}
  \chi^{(\lambda)}(\sigma)
  \cdot
  p_{CycLengths(\sigma)}
  \,.
$$
\end{prop}

([Sagan 01, Thm. 4.6.4](#Sagan01), review in [Sagan Enc., Thm. 3](#SaganEnc))

\linebreak


### Schur-Weyl duality


The Schur polynomials  are precisely the [[irreducible characters]] of [[finite dimensional vector space|finite dimensional]] polynomial [[linear representation|representations]] of [[general linear group|GL(n)]]. 

Also, the character $\chi_{\lambda}$ of $V_\lambda$, the irreducible representation of $S_k$ attached to $\lambda$ (for $k$ the size $|\lambda|$ of the partition) maps to the Schur polynomial under the character map
$ch$ from virtual characters to symmetric polynomials. 

This correspondence between [[linear representations]] of the [[symmetric groups]] and the [[general linear groups]] is called *[[Schur-Weyl duality]]*.


## Generalizations via Schur functors

[[Schur functors]] may be viewed as a [[categorification]] of Schur functions. In fact, the Schur functors make sense in more general [[symmetric monoidal categories]] than [[VectorSpaces]]. It is a theorem in the case of vector space that the [[trace]] of 
a Schur functor $\mathbf{S}_\lambda(V)\stackrel{\mathbf{S}_\lambda(g)}\to \mathbf{S}_\lambda(V)$ on an endomorphism $g\in GL(V)$ is the Schur function of the eigenvalues of $g$. Considering the trace of a Schur functor makes sense in a general situation allowing for Schur functors and for the trace ([[rigid monoidal category]]); of course choosing appropriate variables to express the trace may depend on a context. 

## Related concepts

* [[Schur positivity]]

* [[representation theory of the symmetric group]]

Generalizations:

* [[Jack polynomial]]

* [[Macdonald polynomial]]

* [[noncommutative Schur function]]

* [[quasisymmetric Schur function]]

\linebreak


## References

The concept first appears in work by [[Carl Jacobi]] on [[determinants]]. 

It is named after:

* [[Issai Schur]], *Über eine Klasse von Matrizen die sich einer gegeben Matrix zuordnen lassen*, Inaugural-Dissertation, Berlin (1901) JMF 32.0165.04

See also

* [[Richard Stanley]], Section II of: *Theory and application of plane partitions 1*, Studies in Applied Math. **50** 2 (1971), 167-188 ([pdf](http://www-math.mit.edu/~rstan/pubs/pubfiles/12-1.pdf), [[StanleyPlanePartitions1.pdf:file]])


Textbook accounts:

* {#Macdonald95} [[Ian G. Macdonald]], Section I.3 of: _Symmetric functions and Hall polynomials_, Oxford Math. Monographs, 2nd enlarged ed. 1995 ([ISBN:9780198739128](https://global.oup.com/academic/product/symmetric-functions-and-hall-polynomials-9780198739128?cc=ae&lang=en&))

* {#Stanley99} [[Richard Stanley]], Sections 7.10, 7.15 in: *Enumerative combinatorics 2*, Cambridge University Press (1999, 2010) ([doi:10.1017/CBO9780511609589](https://doi.org/10.1017/CBO9780511609589), [webpage](http://www-math.mit.edu/~rstan/ec/))


* {#Sagan01} [[Bruce Sagan]], Section 4.4 of: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

* Stuart Martin, _Schur algebras and representation theory_, Cambridge Univ. Press 1994 


Survey:

* {#SaganEnc} [[Bruce E. Sagan]], _Schur functions_, in: [[Michiel Hazewinkel]] (ed.), *[[eom|Encyclopaedia of Mathematics]]*, Springer 2002 ([pdf](http://www.mth.msu.edu/~sagan/Papers/Old/schur.pdf), [[SaganSchurFunctions.pdf:file]])

* Wikipedia, *[Schur polynomial](https://en.wikipedia.org/wiki/Schur_polynomial)*



See also:

* Olivier Blondeau-Fournier, Pierre Mathieu, _Schur superpolynomials: combinatorial definition and Pieri rule_, [arxiv/1408.2807](http://arxiv.org/abs/1408.2807)

* Miles Jones, Luc Lapointe, _Pieri rules for Schur functions in superspace_, [arxiv/1608.08577](https://arxiv.org/abs/1608.08577)

[[!redirects Schur functions]]

[[!redirects Schur polynomial]]
[[!redirects Schur polynomials]]


