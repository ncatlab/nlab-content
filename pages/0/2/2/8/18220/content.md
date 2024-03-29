+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
Given a [[first-order structure|model]] $M$ of a (not necessarily complete) [[first-order theory]] $T$, one can canonically associate theories $T_{\mathsf{Diag}(M)}$ and $T_{\mathsf{EDiag}(M)}$ whose models are precisely the models $N \models T$ into which $M$ embeds as a substructure and [[elementary embedding|elementary substructure]], respectively.

In the case of the latter, this gives a theory whose category of models is precisely the [[co-slice category]] $M/\mathbf{Mod}(T)$ of models under $M$ in $\mathbf{Mod}(T)$.

## Definition
Let $M$ be a [[first-order structure]] in the language $\mathcal{L}$. We obtain an expanded language $\mathcal{L}(M)$ by adding to $\mathcal{L}$ new constant symbols $c_m$ for each $m \in M$, and $M$ is naturally an $\mathcal{L}(M)$-structure by interpreting each new constant as its namesake. The **elementary diagram** of $M$, written $\mathsf{EDiag}(M)$, is the set of all $\mathcal{L}$-sentences possibly using constants $c_m$ which are true in $M$, i.e. the $\mathcal{L}(M)$-theory of $M$.

The **quantifier-free diagram** of $M$, written $\mathsf{Diag}(M)$, is obtained the same way as $\mathsf{EDiag}(M)$, but only allowing quantifier-free $\mathcal{L}(M)$-sentences.

If $N$ models $\mathsf{EDiag}(M)$, then $N$ contains $M$ as an elementary substructure. If $N$ models $\mathsf{Diag}(M)$, then $N$ contains $M$ as an induced substructure.

If we are given $M$ and $T$ as above, we simply obtain $T_{\mathsf{Diag}(M)}$ and $T_{\mathsf{EDiag}(M)}$ as the union of $T$ (viewed as an $\mathcal{L}(M)$-theory) with $\mathsf{Diag}(M)$ and $\mathsf{EDiag}(M)$, respectively.

## Examples
* A trivial example is [[ACF]]$_0$, the theory of [[algebraically closed field|algebraically closed fields]] of characteristic zero (in the language of rings). Since $\mathbb{Q}$ is the prime field of characteristic zero, any algebraically closed field models $\mathsf{Diag}(\mathbb{Q})$, and in fact since each element of $\mathbb{Q}$ is already definable in [[ACF]]$_0$, $\mathsf{Diag}(\mathbb{Q})$ is just the quantifier-free part of [[ACF]]$_0$.

* Let $R$ be the [[countable random graph]]. Since it is an [[omega-categorical structure]], any countable model of $\mathsf{EDiag}(R)$ will again be isomorphic to $R$. This is not true if we replace $\mathsf{EDiag}(R)$ with $\mathsf{Diag}(R)$, since there are all sorts of ways to extend $R$ while ensuring it no longer satisfies the almost-sure theory of finite graphs. (For example, we could add a new vertex and connect it to all the vertices from $R$.)

## Remarks
* For $T' = T_{\mathsf{Diag}(M)}$ or $T_{\mathsf{EDiag}(M)}$ there is an obvious interpretation $T \to T'$ which induces for every $N \models T'$ a map of automorphism groups $\operatorname{Aut}_{\mathcal{L}(M)}(N) \to \operatorname{Aut}_{\mathcal{L}}(N)$, corresponding to the inclusion

$$
\operatorname{Aut}_{\mathcal{L}}(N/M) \hookrightarrow \operatorname{Aut}_{\mathcal{L}}(N)
$$

of the pointwise [[stabilizer]] of $M$ in $N$ into the full automorphism group of $N$.

* To add a distinct constant symbol to a theory is to adjoin a new [[global point]] to its [[syntactic category]]. This doesn't do very much unless if you additionally specify its [[type (in model theory)|type]], i.e. the [[ultrafilter]] of subobjects above it. When we pass to the quantifier-free diagram of a model, we specify constants named after the model up to quantifier-free types, and when we pass to the elementary diagram of a model, we specify constants named after the model up to complete types.

* A [[first-order theory]] T [[quantifier elimination|eliminates quantifiers]] if and only if it is "substructure-complete": given any model $M$ of $T$ and any _substructure_ $N \subseteq M$, $T_{\mathsf{Diag}(N)}$ is complete.

+-- {: .num_remark}
###### Remark

The process of passing from $T$ to $T_{\mathsf{Diag}(M)}$ (resp. $\mathsf{EDiag}$) is [[functorial]] in the way you would expect the process of passing from a category of models to a co-slice category of models to be on corepresenting objects.

That is (now [[elimination of imaginaries|eliminating imaginaries]] and working with the [[pretopos completion|pretopos completions]] of [[syntactic category|syntactic categories]]): if $T'$ is an $\mathcal{L}'$-theory and $M$ is an $\mathcal{L}'$-structure, and $T$ is an $\mathcal{L}$-theory over $T'$ via an interpretation $T \overset{F}{\to} T'$, then there are naturally-induced interpretations

$$T'_{\mathsf{Diag}(F^*M)} \to T_{\mathsf{Diag}(M)} $$

and

$$T'_{\mathsf{EDiag}(F^*M)} \to T_{\mathsf{EDiag}(M)}.$$

=--

+-- {: .proof}
###### Proof

The [[interpretation]] $F$ induces a "taking reducts" functor

$$F^* \overset{\operatorname{df}}{=} \mathbf{Mod}(F) = \mathbf{Pretop}(F, \mathbf{Set}) : \mathbf{Mod}(T) \to \mathbf{Mod}(T').$$

We restrict $F^*$ to the full subcategory consisting of those models of $T$ embedding (resp. elementarily embedding) the structure $M$. These are [[elementary class|elementary classes]], and so those full subcategories are sub-[[ultracategory|ultracategories]] of $\mathbf{Mod}(T)$. The restrictions of $F^*$ are ultrafunctors

$$ \underline{\mathbf{Mod}}(T_{\mathsf{Diag}(M)}) \to  \underline{\mathbf{Mod}}(T'_{\mathsf{Diag}(F^*M)})$$

and

$$  \underline{\mathbf{Mod}}(T_{\mathsf{EDiag}(M)}) \to \underline{\mathbf{Mod}}(T'_{\mathsf{EDiag}(F^*M)})$$

because $F^*$ already was, and so by Makkai's [[strong conceptual completeness]], must be reflected by the desired interpretations.

(That the latter functor is well-defined just follows from the fact that specifying an object $c \in \mathbf{C}$ and a functor $G : \mathbf{C} \to \mathbf{D}$ naturally induces a functor on the [[co-slice category|co-slice categories]] $c/\mathbf{C} \to G(c)/\mathbf{D}$. That the former functor is well-defined is less automatic but still trivial to check.)

=--


## Related concepts
* [[first-order structure]]

* [[first-order theory]]

* [[quantifier elimination]]

* For the [[property]] of a theory $T$ that $T_{\mathsf{Diag}(A)}$ is complete for all substructures $A$, see [[substructure completeness]].

* For the [[property]] of a theory $T$ that $T_{\mathsf{EDiag}(M)}$ is complete for all models $M$, see [[model completeness]].

## References

* Dave Marker, (2002), _Model theory: an introduction_, section 2.3

[[!redirects elementary diagram]]
[[!redirects quantifier-free diagram]]
[[!redirects diagram (in model theory)]]