
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

The idea of a commutative monad could be motivated as either

* The [[monad]] equivalent of a [[commutative algebraic theory]], generalized to either non-finitary theories or to categories other than [[Set]]. Intuitively, the operations involved have a commutativity property analogous to [[commutative monoid|the one that monoids can have]];
* A [[monad]] on a [[monoidal category]] whose underlying functor is [[monoidal functor|lax monoidal]], and whose unit and multiplication are [[monoidal natural transformation|monoidal]]. The interpretation is that the monad plays well with the monoidal product of the category, encoding for example products of formal expressions;
* A [[monad]] on a [[monoidal category]] whose [[strong monad|left-strength]] and [[strong monad|right-strength]] commute with each other. 

It turns out that all these concepts coincide (see below, as well as the articles on [[commutative algebraic theories]] and [[monoidal monads]]).


## Definition 

Let $(T,\mu,\eta)$ be a [[monad]] on a [[symmetric monoidal category]] $C$, equipped with a [[strong monad|left-strength]] $\sigma$ (and with the right-strength $\tau$ induced from $\sigma$ and the [[braiding]]). 

We say that $T$ (or $\sigma$) is **commutative** if the following diagram commutes for all objects $X$ and $Y$ of $C$. 
\begin{tikzcd}
& T X \otimes T Y \ar{dl}[swap]{\sigma} \ar{dr}{\tau} \\
T(T X \otimes Y) \ar{d}[swap]{T\tau} && T(X\otimes T Y) \ar{d}{T\sigma} \\
TT(X\otimes Y) \ar{dr}[swap]{\mu} && TT(X\otimes Y) \ar{dl}{\mu} \\
& T(X\otimes Y)
\end{tikzcd}


## Equivalence with monoidal monads

A commutative monad is equivalently a [[monoidal monad]], namely a [[monad#definition|monad in the bicategory]] of [[monoidal categories]], [[lax monoidal functors]] and [[monoidal natural transformations]]. 

For the details see [[monoidal monad]].


## On closed and monoidal closed categories

One can define [[strong monad|left-strength and right-strength]] on a [[closed category]], in a way that's analogous to the definition in a [[monoidal category]], and on [[monoidal closed categories]] the two definitions coincide (see [[strong monad#on_closed_and_monoidal_closed_categories|strong monad - on closed and monoidal closed categories]]). 
The same is true for the notion of commutativity: one can define commutative monads on closed categories, and on closed monoidal categories the definition coincides with the definition given in this article. 

More in detail, let $C$ be a [[closed category]], and denote its [[internal homs]] by $[X,Y]$. 
Let $t':[X,Y]\to [T X, T Y]$ be a left-strength for $T$ (as defined [[strong monad#strong_monads_are_enriched_monads|here]]), and let $s':T[X,Y]\to [X, T Y]$ be a right-strength (as defined [[strong monad#right-strength_and_pointwise_structure|here]]).
We say that $t'$ and $s'$ _commute_, or that $T$ is _commutative_, if the following diagram commutes.
\begin{tikzcd}
& T{[X,Y]} \ar{dl}[swap]{s'} \ar{dr}{Tt'} \\
{[X,T Y]} \ar{d}[swap]{t'} && T{[T X, T Y]} \ar{d}{s'} \\
{[T X, T T Y]} \ar{dr}[swap]{{[T X,\mu]}} && {[T X, T T Y]} \ar{dl}{{[T X,\mu]}} \\
& {[T X, T Y]}
\end{tikzcd}
It can be shown by [[currying]] that on a [[monoidal closed category]], this condition is equivalent to the "monoidal" definition of commutativity.
A reference for this is [Kock '71, Section 2](#kock71closed).


## Tensor product of algebras and multimorphisms

In many situations, [[algebra over a monad|algebras]] over a commutative monad are canonically equipped with a [[tensor product]] analogous to the [[tensor product of modules]] over a ring. 
In particular, commutative monads come equipped with a notion of [[multimorphisms]] of algebras, analogous to [[bilinear]] and [[multilinear maps]].

On a [[closed category]], analogously, the category of algebras inherits an [[internal hom]], just like the one of [[modules]]. If the category is [[closed monoidal category|monoidal closed]], the [[tensor product]] and the [[internal hom]] are [[adjoint]] to each other, making the category of algebra itself monoidal closed. This, once again, generalizes the hom-tensor adjunction of [[modules]] and [[vector spaces]].

For the details, see [[tensor product of algebras over a commutative monad]], and the [[tensor product of algebras over a commutative monad#bimorphisms_and_universal_property|section on the universal property]] for multimorphisms, as well as [[internal hom of algebras over a commutative monad]].


## Examples

In many of the examples, one can see how the property of commutativity (as opposed to just the structure of a [[strong monad|strength]]) has really the meaning of the operations being commutative.

* The free _commutative_ monoid monad on [[Set]] is commutative, the free monoid monad is not.
* If $M$ is a [[monoid]], the [[action monad]] $X\mapsto M\times X$ on [[Set]] is commutative if and only if $M$ is commutative as a monoid. 
* More generally, in an arbitrary [[symmetric monoidal category]], the [[action monad]] induced by tensoring with an [[internal monoid]] is commutative if and only the monoid object is commutative. (See for example [Brandenburg, Example 6.3.12](#Brandenburg2014).)

Since commutative monads are the same as monoidal monads, monads encoding structures which admit products are commutative:

* Most [[probability monads]] are commutative, with monoidal structure given by forming the [[product probability]].
* The [[power set]] monad is commutative, with monoidal structure given by forming the product of subsets.


For a concrete example, consider the free commutative monoid monad $T$, and given a set $X$, write the elements of $TX$ as formal sums, such as $x_1+x_2$.  
The commutativity condition says that these two compositions have the same result,
\begin{tikzcd}[row sep=0]
TX \times TY \ar{r}{\sigma} & T(TX\times Y) \ar{r}{T\tau} & TT(X\times Y) \ar{r}{\mu} & T(X\times Y) \\
(x_1+x_2, y_1+y_2) \ar[mapsto]{r} & (x_1+x_2, y_1) + (x_1+x_2, y_2) \ar[mapsto]{r} & ((x_1, y_1) + (x_2, y_1)) + ((x_1, y_2) + (x_2, y_2)) \ar[mapsto]{r} & (x_1, y_1) + (x_2, y_1) + (x_1, y_2) + (x_2, y_2)
\end{tikzcd}
and
\begin{tikzcd}[row sep=0]
TX \times TY \ar{r}{\tau} & T(X\times TY) \ar{r}{T\sigma} & TT(X\times Y) \ar{r}{\mu} & T(X\times Y) \\
(x_1+x_2, y_1+y_2) \ar[mapsto]{r} & (x_1, y_1+y_2) + (x_2, y_1+y_2) \ar[mapsto]{r} & ((x_1, y_1) + (x_1, y_2)) + ((x_2, y_1) + (x_2, y_2)) \ar[mapsto]{r} & (x_1, y_1) + (x_1, y_2) + (x_2, y_1) + (x_2, y_2)
\end{tikzcd}
Note that these two expressions are not the same on the nose, they are the same because addition is commutative.

(See also the explanations at [[commutative algebraic theory]].)

## See also

* [[monoidal monad]], [[commutative algebraic theory]], [[strong monad]], [[tensorial strength]]
* [[tensor product of algebras over a commutative monad]]
* [[internal hom of algebras over a commutative monad]]


## References

* [[Anders Kock]], _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 

* [[Anders Kock]], _Strong functors and monoidal monads_, Arhus Universitet, Various Publications Series No. 11 (1970).  [PDF](http://home.imf.au.dk/kock/SFMM.pdf).

* {#kock71closed} [[Anders Kock]], _Closed categories generated by commutative monads_ ([[KockMonoidalMonads.pdf:file]])

* H. Lindner, _Commutative monads_ in _Deuxi&#233;me colloque sur l'alg&#233;bre des cat&#233;gories_. Amiens-1975. R&#233;sum&#233;s des conf&#233;rences, pages 283-288. Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 16, nr. 3, 1975.

* {#Keigher78} [[William Keigher]], _Symmetric monoidal closed categories generated by commutative adjoint monads_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978), p. 269-293  ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf))

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))


[[!redirects commutative monads]]

[[!redirects commutative strength]]
[[!redirects commutative strengths]]

[[!redirects commutative strong monad]]
[[!redirects commutative strong monads]]