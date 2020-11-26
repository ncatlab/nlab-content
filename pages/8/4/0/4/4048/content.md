
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _enriched Yoneda lemma_ is the generalization of the usual [[Yoneda lemma]] from [[category theory]] to [[enriched category theory]]. 

## Statement

We discuss here two forms of the Yoneda lemma. 

Let $V$ be a ([[locally small category|locally small]]) [[closed monoidal category|closed]] [[symmetric monoidal category]], so that $V$ is enriched in itself via its [[internal hom]].


### Weak form

 A _weak form_ of the enriched Yoneda lemma says that given a $V$-[[enriched functor]] $F: C \to V$ and an object $c$ of $C$, the _[[set]]_ of $V$-[[enriched natural transformation]]s $\alpha: \hom_C(c, -) \to F$ is in [[natural isomorphism|natural bijection]] with the set of elements of $F(c)$, i.e., the set of morphisms $I \to F(c)$, obtained by composition: 

$$I \stackrel{1_c}{\to} \hom_C(c, c) \stackrel{\alpha c}{\to} F(c)$$

### Strong form

Now suppose that $V$ is in addition (small-)complete (has all small [[limit]]s). Then, given a [[small category|small]] $V$-[[enriched category]] $C$ and $V$-[[enriched functor]]s $F, G: C \to V$, one may construct the _object_ of $V$-natural transformations as an enriched [[end]]: 

$$V^C(F, G) = \int_c V(F(c), G(c))$$ 

(which may in turn be expressed as an ordinary limit in $V$). This is the [[hom-object]] in the [[enriched functor category]].


A _strong form_ of the enriched Yoneda lemma specifies a $V$-[[natural isomorphism]]

$$V^C(\hom_C(c, -), F) \cong F(c).$$ 

This implies the weak form by applying the functor $\hom(I, -): V \to Set$. 

## References 

Textbook accounts include

* [[Max Kelly]], sect. 1.9 (weak form) and 2.4 (strong from) of _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics 64 (1982) [(pdf)](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html)

* {#Borceux94} [[Francis Borceux]], theorem 6.3.5 of _[[Handbook of Categorical Algebra]]_, Volume 2, Cambridge University Press (1994)


Generalizations to the case that the enriching monoidal category is not [[closed monoidal category|closed]] or [[symmetric monoidal category|symmetric]] (using [[skew-symmetric category|skew-symmetric categories]] or [[tensored category|tensored categories]]) can be found in 

* {#Street12} [[Ross Street]], _Skew-closed categories_ ([arXiv:1205.6522](https://arxiv.org/abs/1205.6522))

* {#Hinich16} [[Vladimir Hinich]], _Enriched Yoneda lemma_, Theory and Applications of Categories, Vol. 31, 2016, No. 29, pp 833-838 ([TAC](http://www.tac.mta.ca/tac/volumes/31/29/31-29abs.html))

