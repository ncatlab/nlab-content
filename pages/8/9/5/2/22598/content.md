

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

A formula counting [[semistandard Young tableaux]] with fixed underlying [[Young diagram]] and upper bound on its labels.

## Preliminaries

Given a [[Young diagram]], the *hook* at any one of its boxes is the collection of boxes to the right and below that box, and including the box itself. We write $\ell hook$ for the "length" of such a hook, i.e. for the number of boxes it contains. Formally:

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

With the above ingredients, we have the following [[equality]] of [[polynomials]] in one [[variable]] $q$, where the left hand side is called the *generating function* for numbers of semistandard Young tableaux with (fixed shape $\lambda$ and entries $\leq N$ and) fixed sum of labels:

$$
  \underset{
    T \in ssYT_\lambda(N)
  }{\sum}
  q^{ n(T) }
  \;\;=\;\;
  q^{ \sum_i i \cdot \lambda_i }
  \underset{
    { i \in \{1, \cdots, rows(\lambda)\} }
    \atop
    {j \in \{1, \cdots, \lambda_j\}}
  }{\prod}
  \frac{
    1 - q^{N + j - 1}
  }{
    1 - \ell hook(i,j)
  }
$$

## References

Due to:

* [[Richard Stanley]], Theorem 15.3 in: *Theory and application of plane partitions 2*, Studies in Applied Math. **50** 3 (1971), 259-279 ([pdf](http://www-math.mit.edu/~rstan/pubs/pubfiles/12-2.pdf), [[StanleyPlanePartitions2.pdf:file]])

Further proofs:

* [[Christian Krattenthaler]], *An Involution Principle-Free Bijective Proof of Stanley’sHook-Content Formula*, Discrete Mathematics and Theoretical Computer Science **3**, 1998, 11–32 ([hal:hal-00958904](https://hal.inria.fr/hal-00958904), [pdf](https://hal.inria.fr/hal-00958904/document))

* [[Christian Krattenthaler]], *Another involution principle-free bijective proof of Stanley's hook-content formula*, J. Combin. Theory Ser. A 88 (1999), 66-92 ([arXiv:math/9807068](https://arxiv.org/abs/math/9807068))

* Graham Hawkes, *An Elementary Proof of the Hook Content Formula* ([arXiv:1310.5919](https://arxiv.org/abs/1310.5919))


See also:

* Mark Wildon, *A corollary of Stanley's Hook Content Formula* ([arXiv:1904.08904](https://arxiv.org/abs/1904.08904))


[[!redirects hook content formulas]]

[[!redirects hook-content formula]]
[[!redirects hook-content formulas]]