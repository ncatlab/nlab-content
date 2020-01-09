+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

[[algebra over a monad|Algebras]] over a [[monoidal monad|commutative monad]], in many cases, admit a [[tensor product]] analogous to the traditional [[tensor product of modules]] over a [[ring]]. 


## Construction of the tensor product

Let $(T,\mu,\eta)$ be a commutative monad on a symmetric monoidal category $(C,\otimes,1)$. 
Denote the [[monoidal functor|monoidal multiplication]] of $T$ by $\nabla$.

Given [[algebra over a monad|$T$-algebras]] $(A,a)$ and $(B,b)$, their **tensor product** is, if it exists, the object $A\otimes_T B$ given by the coequalizer in the [[Eilenberg-Moore category]] $C^T$

 \begin{tikzcd}[column sep=large]
  T(TA \otimes TB) \ar[bend right=10]{rr}[swap]{T(a\otimes b)} \ar{r}{T\nabla} & TT(A\otimes B) \ar{r}{\mu} & T(A\otimes B) \ar{r} & A\otimes_T B.
 \end{tikzcd}

We say that $C^T$ **has tensors** if such equalizers exist for all $(A,a)$ and $(B,b)$. In that case, $\otimes_T$ is a functor $C^T\times C^T\to C^T$.

+-- {: .num_theorem #sealthms}
###### Theorem
Suppose that either:

* $C^T$ has tensors, and $\otimes_T$ preserves [[reflexive coequalizers]] in both variables separately ([[reflexive coequalizer#properties|hence jointly]]);

or that

* $C$ has [[reflexive coequalizers]], and that the functor $T(-\otimes -)$ preserves them in both variables separately ([[reflexive coequalizer#properties|hence jointly]]).

Then $\otimes_T$ makes $C^T$ a [[monoidal category]], with

* Monoidal unit given by $T1$, where $1$ is the monoidal unit of $C$;
* Unitors and associators induced by those of $\otimes$.

Moreover, if $\otimes$ is [[symmetric monoidal category|symmetric]], $\otimes_T$ is symmetric too, with [[braiding]] induced by the one of $\otimes$.
=--

([Seal '12, Corollary 2.5.6 and Theorem 2.6.4](#Seal12))



## Universal property in terms of bimorphisms

(...)

## For monoidal closed categories

(...)

## Examples

* [[tensor product of modules]]
* [[tensor product of abelian groups]]
* [[tensor product of algebras]]

## References

* {#Brandenburg2014} Martin Brandenburg, _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))
