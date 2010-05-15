## Statement

The enriched Yoneda lemma is the generalization of the usual [[Yoneda lemma]] to enriched category theory. We discuss here two forms of the Yoneda lemma. 

Let $V$ be a (locally small) [[closed monoidal category|closed symmetric monoidal category]], so that $V$ is enriched in itself via its internal hom. A _weak form_ of the enriched Yoneda lemma says that given a $V$-[[enriched functor]] $F: C \to V$ and an object $c$ of $C$, the _set_ of $V$-[[enriched natural transformation]]s $\alpha: \hom_C(c, -) \to F$ is in natural bijection with the set of elements of $F(c)$, i.e., the set of morphisms $I \to F(c)$, obtained by composition: 

$$I \stackrel{1_c}{\to} \hom_C(c, c) \stackrel{\alpha c}{\to} F(c)$$

Now suppose that $V$ is in addition (small-)complete. Then, given a small $V$-category $C$ and $V$-functors $F, G: C \to V$, one may construct the _object_ of $V$-natural transformations as an enriched [[end]]: 

$$V^C(F, G) = \int_c V(F(c), G(c))$$ 

(which may in turn be expressed as an ordinary limit in $V$). 

A _strong form_ of the enriched Yoneda lemma specifies a $V$-natural isomorphism 

$$V^C(\hom_C(c, -), F) \cong F(c).$$ 

This implies the weak form by applying the functor $\hom(I, -): V \to Set$. 

## Reference 

* G.M. Kelly, _Basic Concepts of Enriched Category Theory_, Cambridge University Press, Lecture Notes in Mathematics 64 (1982) [(pdf)](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html)