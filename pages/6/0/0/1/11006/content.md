
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An [[(∞,1)-functor]] is _conservative_ if its [[reflected limit|reflects]] [[equivalences in an (∞,1)-category]]. This means that on [[homotopy category of an (∞,1)-category|homotopy categories]] it is a [[conservative functor]].

## Examples

+-- {: .un_theorem}
###### Theorem
In an [[(∞,1)-topos]], [[(∞,1)-pullback]] along an [[effective epimorphism in an (∞,1)-category|effective epimorphism]] is a conservative (∞,1)-functor between [[slice (∞,1)-categories]].
=--
+-- {: .proof}
###### Proof

We write in the conjectural [[internal logic]] of an (∞,1)-topos expressed as [[homotopy type theory]], with [[slice (∞,1)-categories]] represented using [[dependent types]].  The reader is free to translate this manually into an [[(∞,1)-category theory|(∞,1)-category-theoretic]] proof.

Thus, suppose $f:A\to B$ is a surjection (i.e. $\prod_{b:B} \exists_{a:A} f(a)=b$, where $\exists$ denotes the [[propositional truncation]] of $\sum$).  Let $P,Q:B\to Type$ be dependent types with a fiberwise map $g:\prod_{b:B} P(b) \to Q(b)$ which becomes a fiberwise [[equivalence in homotopy type theory|equivalence]] upon restricting to $A$, i.e. such that $\prod_{a:A} IsEquiv(g(f(a)))$.  We must show that $g$ is itself a fiberwise equivalence.

Thus, let $b:B$; we must show $IsEquiv(g(b))$.  By assumption we have $\exists_{a:A} f(a)=b$.  But $IsEquiv(g(b))$ is an [[h-proposition]], so we may strip the truncation and obtain an $a:A$ such that $f(a)=b$.  Transporting along this equality, it suffices to show $IsEquiv(g(f(a)))$, but this follows from the other assumption.
=--

## References

In the context of [[quasi-categories]], def. 6.2.1 in

* {#RiehlVerity13} [[Emily Riehl]], [[Dominic Verity]], _Homotopy coherent adjunctions and the formal theory of monads_ ([arXiv:1310.8279](http://arxiv.org/abs/1310.8279))
 

[[!redirects conservative (∞,1)-functors]]

[[!redirects conservative (infinity,1)-functor]]
[[!redirects conservative (infinity,1)-functors]]