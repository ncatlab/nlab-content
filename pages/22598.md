

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The "hook-content formula" expresses the [[number]] of [[semistandard Young tableaux]] with fixed underlying [[Young diagram]] and upper bound on its labels in terms of the "hook lengths" and the "content of boxes" of the underlying diagram. 

If the dependency in the "contents" is removed, the formula reduces to the *[[hook length formula]]* that counts [[standard Young tableaux]] of the given shape.

Both of these formulas equivalently give [[dimensions]] of [[irreps]] in [[representation theory]]:

[[!include hook length and content formulas -- table]]

See at *[[hook length formula]]* for more on this.


## Preliminaries

Given a [[Young diagram]], the *hook* at any one of its boxes is the collection of boxes to the right and below that box, and including the box itself. We write "$\ell hook$" for the *length* of such a hook, i.e. for the number of boxes it contains. Formally:

\begin{defn}
**(hook length)** \linebreak
Let $\lambda = (\lambda_1 \geq \cdots \geq \lambda_{rows(\lambda)})$ be a [[partition]]/[[Young diagram]]. Then for 

* $i \in \{1, \cdots, rows(\lambda)\}$,

* $j \in \{1, \cdots, \lambda_i\}$

the *hook length* at $(i,j)$ is

$$
  \ell hook(i,j)
  \;\coloneqq\;
  1 +
  (\lambda_i - j) + (\lambda'_j - 1)
  \,,
$$

where $\lambda'$ denotes the *conjugate partition* (see [there](Young+diagram#Conjugation)).

\end{defn}

Alongside this terminology one says that

$$
  content(i,j)
  \;\coloneqq\;
  j - i
  \;\;
  \in
  \mathbb{Z}
$$

is the *content* of the box $(i,j)$.

\linebreak

Consider in the following:

* $n \in \mathbb{N}$ a [[natural number]];

* $\lambda = (\lambda_1 \geq \cdots \geq \lambda_{rows(\lambda)})$ a [[partition]] of $n$, $\underset{i}{\sum} \lambda_i = n$, 

  equivalently a [[Young diagram]] with $n$ boxes;

* $N \in \mathbb{N}_+$ a [[positive number|positive]] [[natural number]];

Write:

* $ssYT_\lambda(N)$ for the [[set]] of [[semistandard Young tableaux]] $T$

  * of shape (i.e. with underlying [[Young diagram]]) $\lambda$,

  * with labels $T_{i,j} \leq N$ (i.e. with $T_{i,j} \in \{1, \cdots, N\}$).

* $n(T) = \sum_{i,j} T_{i,j}$ for the [[sum]] of all the labels.

## Statement

### Standard hook-content formula

\begin{prop}
  For $\lambda$ a [[partition]]/[[Young diagram]] and $N \in \mathbb{N}_+$, the [[number]] $\left\vert ssYTableaux_\lambda(N)\right\vert$ of [[semistandard Young tableaux]] $T$ of shape $\lambda$ 
([hence](Schur+function#eq:SchurPolynomialCountsNumberOfSemiStandardYoungTableaux) the value of the [[Schur polynomial]] $s_\lambda$ on $N$ unit argument)
and entries bounded by $T_{i,j} \leq N$ is:

\[
  \left\vert ssYTableaux_\lambda(N)\right\vert
  \;=\;
  s_{\lambda}
  \big(
    x_1 \!=\! 1,
    \cdots,
    x_N \!=\! 1
  \big)  
  \;\;
    = 
  \;\;
  \underset{
    (i,j)
  }{\prod}
  \frac{
     N + content(i,j)
  }{
    \ell hook_\lambda(i,j)
  }
  \,.
\]
\end{prop}

([Stanley 71, Thm. 15.3](#Stanley71), [Stanley 99, Thm. 7.21.2](#Stanley99))

### $q$-Deformed hook-content formula

With the above ingredients, we have the following [[equalities]] of [[polynomials]] in a [[variable]] $q$:


$$
  \underset{
    T \in ssYT_\lambda(N)
  }{\sum}
  q^{ n(T) }
  \;\;=\;\;
  q^{ \sum_i i \cdot \lambda_i }
    \cdot
  \!\!\!\!\!\!\!
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
$$

([Krattenthaler 98, Thm. 1](#Krattenthaler98))

## Related concepts

* [[hook length formula]]


## References

### Standard

The original statement and proof:

* {#Stanley71} [[Richard Stanley]], Theorem 15.3 in: *Theory and application of plane partitions 2*, Studies in Applied Math. **50** 3 (1971), 259-279 ([pdf](http://www-math.mit.edu/~rstan/pubs/pubfiles/12-2.pdf), [[StanleyPlanePartitions2.pdf:file]])

Review:

* {#Stanley99} [[Richard Stanley]], Thm. 7.21.2 in: *Enumerative combinatorics 2*, Cambridge University Press (1999, 2010) ([doi:10.1017/CBO9780511609589](https://doi.org/10.1017/CBO9780511609589), [webpage](http://www-math.mit.edu/~rstan/ec/))

See also:

* Graham Hawkes, *An Elementary Proof of the Hook Content Formula* ([arXiv:1310.5919](https://arxiv.org/abs/1310.5919))


### Generalized
 {#Generalized}

* [[Christian Krattenthaler]], *An Involution Principle-Free Bijective Proof of Stanley's Hook-Content Formula*, Discrete Mathematics and Theoretical Computer Science **3**, 1998, 11–32 ([hal:hal-00958904](https://hal.inria.fr/hal-00958904), [pdf](https://hal.inria.fr/hal-00958904/document))

* {#Krattenthaler98} [[Christian Krattenthaler]], *Another involution principle-free bijective proof of Stanley's hook-content formula*, J. Combin. Theory Ser. A 88 (1999), 66-92 ([arXiv:math/9807068](https://arxiv.org/abs/math/9807068))

See also:

* Mark Wildon, *A corollary of Stanley's Hook Content Formula* ([arXiv:1904.08904](https://arxiv.org/abs/1904.08904))

[[!redirects hook-content formulas]]

[[!redirects hook/content formula]]
[[!redirects hook/content formulas]]


[[!redirects hook content formula]]
[[!redirects hook content formulas]]


