This is a sub-entry for [[gerbe]].

For related entries see

* [[bundle gerbe]]
* [[gerbe (general idea)]]
* [[gerbe (as a stack)]]


##Idea## 

Gerbes give a nice way to group together bundle data on a smooth manifold, but gerbes also naturally define degree two cohomology. Thus the idea of using gerbes in differential geometry is to have a nice language that relates geometric concepts such as connections and curvature to cohomological classifications.

In addition, one can use the analogies above that are made precise with gerbes to define other new concepts such as 3-curvature and "local" fiberwise connections.


##Definitions## 

*   Let $X$ be a smooth manifold. A *Dixmier-Douady sheaf of groupoids* over $X$ is a $\underline{\mathbb{C}}_X^*$-[[gerbe (as a stack)| gerbe]] on $X$ where $\underline{\mathbb{C}}_X^*$ is the sheaf of smooth $\mathbb{C}^*$-valued functions (not to be confused with the constant sheaf $\mathbb{C}_X^*$).

* We define $\mathbb{Z}(1)$ to be the term in the exponential sequence on $X$: $0\to \mathbb{Z}(1)\to \underline{\mathbb{C}}_X \to \underline{\mathbb{C}}_X^*\to 0$.


## Preliminaries##

Taking the associated sequence in cohomology to the exponential sequence gives us an isomorphism $H^2(X, \underline{\mathbb{C}}_X^*)\overset\sim\to H^3(X, \mathbb{Z}(1))$. 

We have a canonical isomorphism between the group of equivalence classes of Dixmier-Douady sheaves of groupoids over $X$ (basically by the definition of $\mathcal{A}$-gerbe) and $H^2(X, \underline{\mathbb{C}}_X^*)\simeq H^3(X, \mathbb{Z}(1))$.


##Geometric Interpretation of $H^3(X, \mathbb{Z}(1))$##

Idea: Classes in $H^3(X, \mathbb{Z}(1))$ correspond to principal $G$-[[principal bundle| bundles]] over $X$ where $G$ is the projective linear group of a separable [[Hilbert space]], namely $C^\infty (\mathbb{T})$.


+--{: .query}

Matt: I'll expand this section soon, and my guess is definitions and preliminaries will expand as needed.
=--



##References

* Jean-Luc Brylinski *Loop Spaces, Characteristic Classes, and Geometric Quantization*

* I. Moerdijk, _Introduction to the language of stacks and gerbes_ ([arXiv](http://arxiv.org/abs/math/0212266))

* Larry Breen, _Notes on 1- and 2-gerbes_ ([arXiv](http://arxiv.org/abs/math/0611317))

Further references are given in the other entries on gerbes.
