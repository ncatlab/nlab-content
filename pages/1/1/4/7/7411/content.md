
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


## Definition 

+-- {: .num_defn}
###### Definition 

A **monoidal monad** is a [[monad]] in the [[2-category]] of [[monoidal category|monoidal categories]], [[lax monoidal functor|lax monoidal functors]], and monoidal transformations. 

=-- 

+-- {: .num_remark}
###### Remark

The notion of monoidal monad is equivalent to the notion of _[[commutative monad]]_. To put it another way: to give a commutative strength for a monad $T$ is to give a monoidal monad whose underlying monad is $T$. We explore this connection below. 

=--

## Tensorial strengths and commutative monads 

As a preliminary, let $V$ be a [[monoidal category]]. We say a functor $T \colon V \to V$ is **strong** if there are given left and right [[tensorial strength|tensorial strengths]] 
$$\tau_{A, B} \colon A \otimes T(B) \to T(A \otimes B)$$

$$\,$$ 

$$\sigma_{A, B} \colon T(A) \otimes B \to T(A \otimes B).$$ 

which are suitably compatible with one another. The full set of [[coherence]] conditions may be summarized by saying $T$ preserves the two-sided monoidal [[action]] of $V$ on itself, in an appropriate [[2-category theory|2-categorical]] sense. More precisely: the two-sided action of $V$ on itself is a [[lax functor]] of 2-categories  
$$\tilde{V} \colon B V \times (B V)^{op} \to Cat$$ 
($B V$ is the one-object 2-category associated with a monoidal category $V$, and $(B V)^{op}$ is the same 2-category but with 1-cell composition (= tensoring) in reverse order), and the two-sided strength means we have a structure of [[lax natural transformation]] $\tilde{V} \to \tilde{V}$. 


+-- {: .num_remark}
###### Remark

In the setting where $V$ is _[[symmetric monoidal category|symmetric]]_ monoidal, we will assume that the left and right strengths $\tau$ and $\sigma$ are related by the symmetry in the obvious way, by a commutative square 

$$\array{
A \otimes T(B) & \stackrel{\tau_{A, B}}{\to} & T(A \otimes B) \\
 ^\mathllap{c} \downarrow & & \downarrow^\mathrlap{T(c)} \\
T(B) \otimes A & \underset{\sigma_{B, A}}{\to} & T(B \otimes A)
}$$ 

where the $c$'s are instances of the symmetry isomorphism. 

=--

There is a category of strong functors $V \to V$, where the morphisms are transformations $\lambda \colon S \to T$ which are compatible with the strengths in the obvious sense. Under composition, this is a strict monoidal category. 

+-- {: .num_defn #StrongMonad}
###### Definition 

Monoids in this monoidal category are called **[[strong monads]]**. 

=--

+-- {: .num_defn #CommutativeMonad}
###### Definition 

A [[strong monad]] $(T \colon V \to V, m \colon T T \to T, u: 1 \to T)$ (def. \ref{StrongMonad}) is a **[[commutative monad]]** if there is an equality of [[natural transformations]] $\alpha = \beta$ where 

* $\alpha$ is the composite 
$$T A \otimes T B \stackrel{\sigma_{A, T B}}{\to} T(A \otimes T B) \stackrel{T(\tau_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B).$$ 

* $\beta$ is the composite 
$$T A \otimes T B \stackrel{\tau_{T A, B}}{\to} T(T A \otimes B) \stackrel{T(\sigma_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B).$$ 
=-- 

## From monoidal monads to commutative monads 

Let $(T \colon V \to V, u \colon 1 \to T, m \colon T T \to T)$ be a monoidal monad, with structural constraints on the underlying functor denoted by 

$$\alpha_{A, B} \colon T(A) \otimes T(B) \to T(A \otimes B), \qquad \iota = u I: I \to T(I).$$ 

Define [[tensorial strength|strengths]] on both the left and the right by 

$$\tau_{A, B} = (A \otimes T(B) \stackrel{u A \otimes 1}{\to} T(A) \otimes T(B) \stackrel{\alpha_{A, B}}{\to} T(A \otimes B)),$$ 

$$\,$$ 

$$\sigma_{A, B} = (T(A) \otimes B \stackrel{1 \otimes u B}{\to} T(A) \otimes T(B) \stackrel{\alpha_{A, B}}{\to} T(A \otimes B)).$$ 

+-- {: .num_prop}
###### Proposition 
$(m \colon T T \to T, u \colon 1 \to T)$ is a commutative monad. 
=-- 

+-- {: .proof} 
###### Proof 
In fact, the two composites 

$$T A \otimes T B \stackrel{\sigma_{A, T B}}{\to} T(A \otimes T B) \stackrel{T(\tau_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B)$$ 

$$\,$$ 

$$T A \otimes T B \stackrel{\tau_{T A, B}}{\to} T(T A \otimes B) \stackrel{T(\sigma_{A, B})}{\to} T T(A \otimes B) \stackrel{m(A \otimes B)}{\to} T(A \otimes B)$$

are both equal to $\alpha_{A, B}$. We show this for the second composite; the proof is similar for the first. If $\alpha_T$ denotes the monoidal constraint for $T$ and $\alpha_{T T}$ the constraint for the composite $T T$, then by definition $\alpha_{T T}$ is the composite given by  
$$T T X \otimes T T Y \stackrel{\alpha_T T}{\to} T(T X \otimes T Y) \stackrel{T\alpha_T}{\to} T T(X \otimes Y)$$ 
and so, using the properties of monoidal monads, we have a commutative diagram 

$$\array{
 & & T T X \otimes T Y & \stackrel{\alpha_T}{\to} & T(T X \otimes Y) \\
 & ^\mathllap{u \otimes 1} \nearrow & \downarrow^\mathrlap{1 \otimes T u} & & \downarrow^\mathrlap{T(1 \otimes u)} \\
T X \otimes T Y & \stackrel{u \otimes T u}{\to} & T T X \otimes T T Y & \stackrel{\alpha_T T}{\to} & T(T X \otimes T Y) \\
 & ^\mathllap{1} \searrow & \downarrow^\mathrlap{m \otimes m} & \searrow^\mathrlap{\alpha_{T T}} & \downarrow^\mathrlap{T\alpha_T} \\
 & & T X \otimes T Y & & T T(X \otimes Y) \\
& & & ^\mathllap{\alpha_T} \searrow & \downarrow^\mathrlap{m} \\
 & & & & T(X \otimes Y)
}$$ 

which completes the proof. 
=-- 

## Functoriality of the correspondence

The correspondence between monoidal monads and [[commutative monads]] is [[functorial]]. More precisely, 

+-- {: .num_thm #cf}
###### Proposition 

Given monoidal monads $S$ and $T$ on a [[monoidal category]] $C$, a [[monad#the_bicategory_of_monads|morphism of monads]] $\alpha:S\Rightarrow T$ is a [[morphism]] of [[strong monads]] if and only if it is a [[monoidal natural transformation]].

=--

For a reference, see [FPR '19, Proposition C.5](#support).


## Tensor product of algebras and multimorphisms

See [[commutative monad#tensor_product_of_algebras_and_multimorphisms|here]].


## Monoidal structure on the Kleisli category

The [[Kleisli category]] of a monoidal monad $T$ on $C$ inherits the [[monoidal structure]] from $C$.
In particular, the [[tensor product]] is given

* On objects, by the tensor product $\otimes$ of $C$;
* On morphisms, given $k:X\to TA$ and $h:Y\to TB$, their product is the map $X\otimes Y \to T(A\otimes B)$ obtained by the composition
\begin{tikzcd}
X\otimes Y \ar{r}{f\otimes g} & TA \otimes TB \ar{r}{\nabla} & T(A\otimes B),
\end{tikzcd}
where $\nabla$ is the monoidal multiplication of $T$.
* The associator and unitor are induced by those of $C$.


## Examples

See [[commutative monad#examples|examples of commutative monads]].


## See also

* [[strong monad]], [[tensorial strength]]
* [[monoidal functor]]
* [[commutative monad]], [[commutative algebraic theory]]


## References


* [[Anders Kock]], _Monads on symmetric monoidal closed categories_, Arch. Math. 21 (1970), 1--10. 

* [[Anders Kock]], _Strong functors and monoidal monads_, Arhus Universitet, Various Publications Series No. 11 (1970).  [PDF](http://home.imf.au.dk/kock/SFMM.pdf).

* [[Anders Kock]], _Closed categories generated by commutative monads_ ([[KockMonoidalMonads.pdf:file]])

* H. Lindner, _Commutative monads_ in _Deuxi&#233;me colloque sur l'alg&#233;bre des cat&#233;gories_. Amiens-1975. R&#233;sum&#233;s des conf&#233;rences, pages 283-288. Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle cat&#233;goriques, tome 16, nr. 3, 1975.

* {#Keigher78} [[William Keigher]], _Symmetric monoidal closed categories generated by commutative adjoint monads_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 19 no. 3 (1978), p. 269-293  ([NUMDAM](http://www.numdam.org/numdam-bin/fitem?id=CTGDC_1978__19_3_269_0), [pdf](http://archive.numdam.org/article/CTGDC_1978__19_3_269_0.pdf))

* {#Seal12} Gavin J. Seal, _Tensors, monads and actions_ ([arXiv:1205.0101](http://arxiv.org/abs/1205.0101))

* {#Brandenburg2014} [[Martin Brandenburg]], _Tensor categorical foundations of algebraic geometry_ ([arXiv:1410.1716](https://arxiv.org/abs/1410.1716))

A statement in the text appears in Appendix C of

* {#support} [[Tobias Fritz]], [[Paolo Perrone]] and Sharwin Rezagholi, _Probability, valuations, hyperspace: Three monads on Top and the support as a morphism_, 2019 ([arXiv:1910.03752](https://arxiv.org/abs/1910.03752))


[[!redirects monoidal monads]]

