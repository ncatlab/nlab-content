
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

### For elements of $\mathbb{N}$-rings

+-- {: .num_defn #NRing}
###### Definition

A _unital $\mathbb{N}$-ring_ is a [[ring]] such that 

1. the underlying [[abelian group]] is [[free abelian group]];

1. there exists a finite $\mathbb{N}$-[[basis]]: a [[finite set]] $I$ of elements $X_i \in R$, $i \in I$, such that 

   $$
     X_i X_j = \sum_{k \in I} c_{i j}^k X_k
   $$

   for $c_{i j}^k \in \mathbb{N}$

1. the ring unit 1 is among these basis elements.

=--

+-- {: .num_defn #FPDimension}
###### Definition


Let $R$ be a unital $\mathbb{N}$-ring (def. \ref{NRing}) with finite $\mathbb{N}$-[[basis]] $I$, $\vert I\vert = n \in \mathbb{N}$. 

For every $X \in R$, let $(N_X)_{i j}\in \mathbb{N}$ be its [[matrix]] of left multiplication, defined by

$$
  X X_j  =  \sum_{i \in I} (N_X)_{i j} X_i
  \,.
$$

By the [[Frobenius-Perron theorem]], these matrices $N_X$ have non-negative [[eigenvalues]]. This implies that for each of them there is a [[maximum|maximal]] [[eigenvalue]]. This maximal eigenvalue is called the **Frobenius-Perron dimension** of $X$, $FPdim(X)$.

=--

### For objects of fusion categories

Let $\mathcal{C}$ be a [[fusion category]], i.e. a [[tensor category]] which is [[finite abelian category|finite]] and [[semisimple category]] (i.e. it has a [[finite number]] of [[isomorphism classes]] $[X_i]$ of [[simple objects]], all finite [[direct sums]] of these exist, and every object is isomorphic to such).

+-- {: .num_defn #FPDimension}
###### Definition

Then the [[isomorphism classes]] $[X]$ of objects of $\mathcal{C}$ form an $\mathbb{N}$-ring (def. \ref{NRing}) under [[tensor product]], the _[[fusion ring]]_.

The **Frobenius-Perron dimension of $X \in \mathcal{C}$ is that of its isomorphism class $[X]$ as an element of the [[fusion ring]], according to def. \ref{FPDimension}:

$$
  FPdim(X) \coloneqq FPDim([X])
  \,.
$$

=--

## References

* [[Damien Calaque]], [[Pavel Etingof]], section 4 of  _Lectures on tensor categories_ ([arXiv:0401246](https://arxiv.org/abs/math/0401246))

* {#EGNO15} [[Pavel Etingof]], Shlomo Gelaki, Dmitri Nikshych, [[Victor Ostrik]], section 3.3 in _Tensor categories_, Mathematical Surveys and Monographs, Volume 205, American Mathematical Society, 2015 ([pdf](http://www-math.mit.edu/~etingof/egnobookfinal.pdf
))
