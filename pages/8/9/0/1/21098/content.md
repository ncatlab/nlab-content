+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Mapping spaces
+--{: .hide}
[[!include mapping space - contents]]
=--
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

[[algebra over a monad|Algebras]] over a [[commutative monad]], in many cases, admit an [[internal hom]] analogous to the one of [[modules]] over a [[commutative ring]]. 

On a [[monoidal closed category]], this internal hom is in many cases [[adjoint functor|right-adjoint]] to a [[tensor product of algebras over a commutative monad|tensor product]], giving a [[hom-tensor adjunction]] for the algebras too. 
Again, this generalizes the case of [[modules]].


## Construction 

Let $C$ be a [[closed category]] with [[equalizers]], denote its [[unit]] by $1$ and its [[internal homs]] by $[X,Y]$.
Let also $(T,\mu,\eta)$ be a [[commutative monad]] as defined for closed categories ([[commutative monad#on_closed_and_monoidal_closed_categories|here]]), with [[strong monad#strong_monads_are_enriched_monads|strength]] $t':[X,Y]\to [T X, T Y]$ and [[strong monad#costrength_and_pointwise_structure|costrength]] $s':T[X,Y]\to [X, T Y]$. 

Let now $(A,a)$ and $(B,b)$ be $T$-[[algebra over a monad|algebras]]. Thanks to the costrength, the [[internal hom]] $[A,B]$ of $C$ has a canonical "pointwise" $T$-algebra structure,
$$
T[A,B] \to [A, T B] \to [A,B].
$$
(See [[strong monad#algebra_structure_on_the_internal_homs|here]] for the details.)

The **internal hom** of $A$ and $B$ in $C^T$ is defined to be the [[equalizer]] of the following parallel pair:
\begin{tikzcd}[%
nodes={scale=1.25}, arrows={thick},%
]
{[A,B]} \ar[bend right=10]{rr}[swap]{a^*} \ar{r}{t'} & {[TA, TB]} \ar{r}{b_*} & {[TA,B]}, \\
\end{tikzcd}
where $a^*:[A,B]\to [T A,B]$ is the internal precomposition with $a:T A\to A$, and $b_*:[T A,T B]\to [T A,B]$ is the internal postcomposition with $b:T B\to B$.

Denote this object by $[A,B]_T$.

(See [Brandenburg, Remark 6.4.1](#Brandenburg2014), as well as the original work [Kock '71, Section 2](#Kock71closed).)


+-- {: .num_theorem}
###### Theorem
([Kock '71, Theorem 2.2](#Kock71closed))
Let $C$ be a [[closed category]] with [[equalizers]], and $(T,\mu,\eta)$ a [[commutative monad]] on $C$. 
Then $[-,-]_T$ makes the [[Eilenberg-Moore category]] $C^T$ itself a [[closed category]], with

* [[unit object]] given by the free algebra $T1$, where $1$ is the unit object of $C$;
* All the structure maps induced by those of $C$. 
=--



### Interpretation

The internal hom $[A,B]$ of $A$ and $B$ in $C$ can be thought of as "containing all the morphisms $A\to B$ of $C$". However, not all those morphisms are necessarily [[algebra over a monad#morphisms_of_algebras|morphisms of $T$-algebras]]. A map $f:A\to B$ is a morphism of algebras if and only if $b\circ T f = f\circ a$. In terms of internal homs, this condition is exactly given by the parallel maps above. The equalizer of that pair can be thought of as of containing "all the maps satisfying that condition".


## Examples and implications

* The [[internal hom]] of [[modules]] over a [[commutative ring]] as the most prominent example. Note that the ring has to be commutative: this corresponds to the [[commutative monad|commutativity of the monad]]. 
* The [[vector space]] of [[linear maps]] between two given vector spaces is a particular example.

The fact that "linear maps form themselves a vector space" is a general phenomenon for [[commutative monads]] on categories with [[equalizers]]. For instance,

* For the case of the [[distribution monad]], this says that _convex combinations of affine functions are affine_;
* For the case of the [[power set]] monad, this says that _pointwise suprema of join-preserving maps between join-semilattices are join-preserving_.



## On monoidal closed categories

If the category $C$ is [[closed monoidal category|monoidal closed]], under some condition the internal hom of algebras is part of a closed monoidal structure on the algebras themselves. See [[tensor product of algebras over a commutative monad#for_monoidal_closed_categories|here]] for more information.


## See also 

* [[monoidal monad]], [[commutative monad]], [[strong monad]], [[commutative algebraic theory]]
* [[tensor product of algebras over a commutative monad]]
* [[tensor product]], [[tensor product of modules]], [[multilinear map]], [[representable multicategory]]
* [[monoidal category]], [[closed category]], [[closed monoidal category]], [[internal hom]]


## References

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

* {#Keigher78} [[William Keigher]], _Symmetric monoidal closed categories generated by commutative adjoint monads_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978), p. 269-293  ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf))

* {#Kock70monads} [[Anders Kock]], _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 

* {#Kock70closed} [[Anders Kock]], _Strong functors and monoidal monads_, Arhus Universitet, Various Publications Series No. 11 (1970).  [PDF](http://home.imf.au.dk/kock/SFMM.pdf).

* {#Kock71closed} [[Anders Kock]], _Closed categories generated by commutative monads_, 1971 ([[KockMonoidalMonads.pdf:file]])


* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))

