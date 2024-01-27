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

[[algebra over a monad|Algebras]] over a [[commutative monad]], in many cases, admit a [[tensor product]] analogous to the traditional [[tensor product of modules]] over a [[ring]]. 

This tensor product satisfies a universal property analogous to the one of the tensor product of modules, namely it [[representable multicategory|represents]] [[multimorphisms]] in the same way in which the tensor product of modules represents [[bilinear maps]]. 


## Construction of the tensor product

Let $(T,\mu,\eta)$ be a commutative monad on a symmetric monoidal category $(C,\otimes,1)$. 
Denote the [[monoidal functor|monoidal multiplication]] of $T$ by $\nabla$.

Given [[algebra over a monad|$T$-algebras]] $(A,a)$ and $(B,b)$, their **tensor product** is, if it exists, the object $A\otimes_T B$ given by the coequalizer in the [[Eilenberg-Moore category]] $C^T$

 \begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
  T(TA \otimes TB) \ar[bend right=10]{rr}[swap]{T(a\otimes b)} \ar{r}{T\nabla} & TT(A\otimes B) \ar{r}{\mu} & T(A\otimes B) \ar{r} & A\otimes_T B.
 \end{tikzcd}

We say that $C^T$ **has tensors** if such equalizers exist for all $(A,a)$ and $(B,b)$. In that case, $\otimes_T$ is a functor $C^T\times C^T\to C^T$.

+-- {: .num_theorem #sealthms}
###### Theorem
([Seal '12, Corollary 2.5.6 and Theorem 2.6.4](#Seal12))
Suppose that either:

* $C^T$ has tensors, and $\otimes_T$ preserves [[reflexive coequalizers]] in both variables separately ([[reflexive coequalizer#properties|hence jointly]]);

or that

* $C$ has [[reflexive coequalizers]], and that the functor $T(-\otimes -)$ preserves them in both variables separately ([[reflexive coequalizer#properties|hence jointly]]).

Then $\otimes_T$ makes the [[Eilenberg-Moore category]] $C^T$ a [[monoidal category]], with

* [[unit object]] given by $T1$, where $1$ is the unit object of $C$;
* [[unitors]] and [[associators]] induced by those of $\otimes$.

Moreover, if $\otimes$ is [[symmetric monoidal category|symmetric]], $\otimes_T$ is symmetric too, with [[braiding]] induced by the one of $\otimes$.
=--




## Bimorphisms and universal property

[[commutative monad|Commutative monads]] admit a notion of [[multimorphism]] of algebras analogous to the notion of [[bilinear]] and [[multilinear map]]. 

**Caveat.** Some authors call the analogue of a bilinear map a _bimorphism_. This is a distinct notion from the one given [[bimorphism|in this page]] (a morphism which is both epi and mono). 
A less ambiguous term is [[binary morphism]].

Let $(A,a)$, $(B,b)$ and $(R,r)$ be $T$-algebras. A **binary morphism** of algebras, or **$T$-balanced map**, or **$T$-bilinear** (or **bimorphism**, see the caveat above) from $A$ and $B$ to $R$ is a morphism $f:A\otimes B\to R$ of $C$ such that the following diagram commutes.

\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
  TA \otimes TB \ar{d}{a\otimes b} \ar{r}{\nabla} & T(A\otimes B) \ar{r}{Tf} & TR \ar{d}{r} \\
  A\otimes B \ar{rr}{f} && R
\end{tikzcd}

For $n$ inputs, we can define a **multimorphism of algebras** in the same way.

We can view a binary morphism as a morphism which is a "morphism of algebras in each variable separately". This intuition can be made precise as follows. 

+-- {: .num_theorem #bimorphs}
###### Proposition
([Kock '71, Theorem 1.1](#Kock71bilin), [Seal '12, Proposition 2.1.2](#Seal12))
A morphism $f:A\otimes B\to R$ of $C$ is a binary morphism of algebras if and only if both the following two diagrams commute. (The maps $s$ and $t$ denote the [[strong monad|strength and costrength]] of the monad $T$.)
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
A \otimes TB \ar{d}{1\otimes b} \ar{r}{s} & T(A\otimes B) \ar{r}{Tf} & TR \ar{d}{r}  && TA \otimes B \ar{d}{a\otimes 1} \ar{r}{t} & T(A\otimes B) \ar{r}{Tf} & TR \ar{d}{r}  \\
A \otimes B \ar{rr}{f} && R && A \otimes B \ar{rr}{f} && R
\end{tikzcd}
=--

We can denote by $C^T(A,B;C)$ the set of binary morphisms from $A$ and $B$ to $C$ this is a functor $(C^T)^{op}\times(C^T)^{op}\times C^T\to Set$. Analogous assignments can be given for $n$ inputs; this equips $C^T$ with the structure of a [[multicategory]] extending its usual category structure. 
The most prominent example of this is [[multilinear maps]] extending [[linear maps]]. 

As in the case of multilinear maps, we have that the tensor product of algebras, if it exists, represent multimorphisms.

+-- {: .num_theorem #uniprop}
###### Theorem
([Seal '12, Proposition 2.3.4](#Seal12))
Suppose that $C^T$ has tensors. For each $T$-algebras $(A,a)$, $(B,b)$ and $(R,r)$ there is a bijection
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
C^T(A\otimes_T B, C) \ar{r}{\cong} & C^T(A,B; C) ,
\end{tikzcd}
natural in $A$, $B$ and $C$. 
=--
In other words, $C^T$ with $\otimes_R$ is a [[representable multicategory]]. 

The proof (see the reference above) follows closely the classical case of modules over a ring.

## For monoidal closed categories

The treatment of the closed case goes back to [the work done in the 70s by Anders Kock](#Kock71closed). A treatment of that case has been recently given also in [the thesis of Martin Brandenburg](#Brandenburg2014). 

If $C$ is a [[monoidal closed category]] and has [[equalizers]], and $C^T$ has tensors, the first hypothesis of [the theorem above](#sealthms) is satisfied, and so $(C^T,\otimes_T,T1)$ is a monoidal category. Moreover, $C^T$ can be equipped with an [[internal hom]] $[A,B]_T$ which makes $C^T$ closed (see [[internal hom of algebras over a commutative monad]]).
In that case the natural bijection
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
C(A\otimes B, C)  \ar{r}{\cong} & C(A ,{[B,C]})
\end{tikzcd}
given by the [[hom-tensor adjunction]] of $C$ induces a natural bijection
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
C^T(A\otimes_T B, C) \ar{r}{\cong} & C^T(A, {[B,C]}_T)
\end{tikzcd}
which makes $C^T$ itself a [[closed monoidal category]].

This generalizes the [[hom-tensor adjunction]] of [[modules]], [[abelian groups]] and [[vector spaces]].

See also [[commutative algebraic theory#ClosedMonoidalStructureOnAlgebras|closed monoidal structure on algebras over a commutative algebraic theory]].


## Examples

* [[tensor product of modules]]
* [[tensor product of abelian groups]]
* [[tensor product of algebras]]


## See also 

* [[monoidal monad]], [[commutative monad]], [[strong monad]], [[commutative algebraic theory]]
* [[tensor product]], [[tensor product of modules]], [[multilinear map]], [[representable multicategory]]
* [[internal hom of algebras over a commutative monad]]
* [[monoidal category]], [[closed category]], [[closed monoidal category]]


## References

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

* {#Keigher78} [[William Keigher]], _Symmetric monoidal closed categories generated by commutative adjoint monads_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978), p. 269-293  ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf))

* {#Kock70monads} [[Anders Kock]], _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 

* {#Kock70closed} [[Anders Kock]], _Strong functors and monoidal monads_, Arhus Universitet, Various Publications Series No. 11 (1970).  [PDF](http://home.imf.au.dk/kock/SFMM.pdf).

* {#Kock71closed} [[Anders Kock]], _Closed categories generated by commutative monads_, 1971 ([[KockMonoidalMonads.pdf:file]])

* {#Kock71bilin} [[Anders Kock]], _Bilinearity and cartesian closed monads_, Mathematica Scandinavica, 29, 1971.

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))





[[!redirects tensor product of algebras over commutative monads]]
[[!redirects tensor product of algebras of a commutative monad]]
[[!redirects tensor product of algebras of commutative monads]]
[[!redirects tensor product of algebras for a commutative monad]]
[[!redirects tensor product of algebras for commutative monads]]
[[!redirects tensor product for algebras over a commutative monad]]
[[!redirects tensor product for algebras over commutative monads]]
[[!redirects tensor product for algebras of a commutative monad]]
[[!redirects tensor product for algebras of commutative monads]]
[[!redirects tensor product for algebras for a commutative monad]]
[[!redirects tensor product for algebras for commutative monads]]